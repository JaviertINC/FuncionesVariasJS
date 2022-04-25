# jtT2I - Texto a Imagen
Diseñado para incluir correos electrónicos en nuestros sitios web y que no sean rastreados por _bots mailhunters_  

## Función en Javascript
```js
function jtT2I(id){
	let canvas = document.getElementById(id);
	let ctx = canvas.getContext("2d");
	let this_t = canvas.getAttribute('data-text');
	let this_c = canvas.getAttribute('data-color');
	let this_b = canvas.getAttribute('data-background');
	let this_w = canvas.getAttribute('width');
	let this_h = canvas.getAttribute('height');
	ctx.fillStyle = this_b;
	ctx.fillRect(0, 0, this_w, this_h); 
	ctx.font = "16px Arial";
	ctx.fillStyle = this_c;
	ctx.fillText(atob(this_t),3,16);
}
```

## Uso con HTML Canvas
Debes indicar el texto a convertir en el atributo `data-text` codificado en base64.
También puedes personalizar color del texto `data-color`, color del fondo `data-background`, el ancho y la altura.
```html
<canvas id="contactEmail" data-color="#4caf50" data-background="#4c4c4c" data-text="QnlASmF2aWVydElOQw" width="110" height="20">
	Si ves este texto, tu navegador, no soporta o está bloqueando Canvas y/o Javascript.
</canvas>
```

## Ejecución de la funcion:
```js
jtT2I("contactEmail");
```
