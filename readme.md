# Taller de JavaScript: Animaciones

![Resultado](/images/result.png)

Autor: Eduardo Oviedo Blanco

Para usar este taller efectivamente, clone el código en su ambiente local.
```
git clone https://github.com/edWAR6/Javascript-Animations-Workshop.git
```
Si desea subir el taller en su repositorio personal.
Cree un repositorio en su perfil, luego:
```
git remote set-url origin https://github.com/<tu usuario>/Javascript-Animations-Workshop.git
```

> El nombre del repositorio puede cambiar. Siga las instrucciones y guarde sus cambios.

## Propósito

Este taller demuestra la creación de animaciones en CSS.

## Instrucciones

1. Inicie analizando el HTML y el CSS ya incluidos.

2. Para crear la primer animación, cree el *keyframes* que se ve a continuación.
```css
@keyframes pulse {
  0% {
    background-color: #dc1b5e;
  }

  100% {
    background-color: #FF4136;
  }
}
```

3. Para hacer uso de ese keyframes, asigne la propiedad *animation* al body del HTML en el CSS.
```css
body {
  ...
  animation: pulse 3s infinite alternate;
}
```

4. Note como solo con este ahora el body cambia de color.

5. Ahora cree una animación para el elemento *circle* creando un nuevo *keyframes*.
```css
@keyframes stretch {
  0% {
    transform: scale(.3);
    background-color: red;
    border-radius: 100%;
  }

  50% {
    background-color: orange;
  }

  100% {
    transform: scale(1.5);
    background-color: yellow;
  }
}
```

6. Asigne esta animación al elemento *circle*.
```css
.circle {
  animation-name: stretch;
  animation-duration: 1.5s;
  animation-timing-function: ease-out;
  animation-delay: 0;
  animation-direction: alternate;
  animation-iteration-count: infinite;
  animation-fill-mode: none;
  animation-play-state: running;
}
```

7. Note como ahora el circulo está animado.

8. Experimente con todas las sub-propiedades de la animación.

9. Ahora cree una tercer animación.
```css
@keyframes nudge {
  0%, 100% {
    transform: translate(0, 0);
  }

  50% {
    transform: translate(150px, 0);
  }

  80% {
    transform: translate(-150px, 0);
  }
}
```

10. En este caso al asignar la animación, observe como es posible hacerlo con múltiples animaciones al mismo tiempo.
```css
.square {
  animation:
    pulse 3s ease 2s infinite alternate, 
    nudge 5s linear infinite alternate;
}
```

## Conclusión

Este taller solo explora de manera superficial todo lo que se puede hacer con animaciones. Pero las posibilidades son muchas.