# FuncionesVariasJS
Funciones Varias en Javascript

---

## Texto a Imagen, no legible por BOTS
#### _Diseñado para incluir correos personales en nuestros sitios webs_
Function Javascript
```
function runCanv(id){
	var canvas = document.getElementById(id);
	var ctx = canvas.getContext("2d");
	var this_t = canvas.getAttribute('data-text');
	var this_c = canvas.getAttribute('data-color');
	var this_b = canvas.getAttribute('data-background');
	var this_w = canvas.getAttribute('width');
	var this_h = canvas.getAttribute('height');
	ctx.fillStyle = this_b;
	ctx.fillRect(0, 0, this_w, this_h); 
	ctx.font = "16px Arial";
	ctx.fillStyle = this_c;
	ctx.fillText(atob(this_t),3,16);
}
```

Uso con HTML Canvas
```
<canvas id="contactEmail" data-color="#4caf50" data-background="#4c4c4c" data-text="QnlASmF2aWVydElOQw" width="110" height="20">
		Si ves este texto, tu navegador, no soporta o está bloqueando Canvas y/o Javascript.
	</canvas>
```

Ejecutar la funcion:
```
runCanv("contactEmail");
```
