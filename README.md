# 💫 About Me:
💻 Developer Frontend


## 🌐 Socials:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/https://www.linkedin.com/in/gerardo-montini/) 

# 💻 Tech Stack:
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![GithubPages](https://img.shields.io/badge/github%20pages-121013?style=for-the-badge&logo=github&logoColor=white) ![Firebase](https://img.shields.io/badge/firebase-%23039BE5.svg?style=for-the-badge&logo=firebase) ![Netlify](https://img.shields.io/badge/netlify-%23000000.svg?style=for-the-badge&logo=netlify&logoColor=#00C7B7) ![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white) ![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB) ![SASS](https://img.shields.io/badge/SASS-hotpink.svg?style=for-the-badge&logo=SASS&logoColor=white) ![Angular](https://img.shields.io/badge/angular-%23DD0031.svg?style=for-the-badge&logo=angular&logoColor=white) ![Angular.js](https://img.shields.io/badge/angular.js-%23E23237.svg?style=for-the-badge&logo=angularjs&logoColor=white) ![Bootstrap](https://img.shields.io/badge/bootstrap-%238511FA.svg?style=for-the-badge&logo=bootstrap&logoColor=white) ![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
# 📊 GitHub Stats:
![](https://github-readme-stats.vercel.app/api?username=Gerardo Montini&theme=tokyonight&hide_border=false&include_all_commits=false&count_private=false)<br/>
![](https://github-readme-streak-stats.herokuapp.com/?user=Gerardo Montini&theme=tokyonight&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=Gerardo Montini&theme=tokyonight&hide_border=false&include_all_commits=false&count_private=false&layout=compact)

---
[![](https://visitcount.itsvg.in/api?id=Gerardo Montini&icon=0&color=0)](https://visitcount.itsvg.in)

<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->

Este repositorio contiene el código de un juego de adivinanza implementado en Javascript. El juego consiste en adivinar un número aleatorio generado por el programa en un rango del 1 al 100.

## Código Javascript

El archivo Javascript principal es `script.js`, que contiene las siguientes funciones y variables:

### Generar un número aleatorio

    let numeroAzar = Math.floor(Math.random() * 100) + 1;

Esta línea de código genera un número aleatorio entre 1 y 100 y lo guarda en la variable `numeroAzar`. Utilizamos `Math.random()` para generar un número decimal entre 0 y 1, luego lo multiplicamos por 100 para obtener un número entre 0 y 100, y finalmente utilizamos `Math.floor()` para redondear hacia abajo y obtener un número entero entre 0 y 99. Al sumar 1 al resultado, obtenemos un número aleatorio entre 1 y 100.

### Obtener elementos del DOM

    let numeroEntrada = document.getElementById('numeroEntrada');
    let mensaje = document.getElementById('mensaje');

Estas líneas de código obtienen referencias a los elementos del Document Object Model (DOM) utilizando el método `getElementById()`. El elemento con el id "numeroEntrada" representa el campo de entrada donde el usuario ingresa su número, y el elemento con el id "mensaje" muestra mensajes de retroalimentación al usuario.

### Función para comprobar el número ingresado

    function chequearResultado() {
        let numeroIngresado = parseInt(numeroEntrada.value);
    
        if (isNaN(numeroIngresado) || numeroIngresado < 1 || numeroIngresado > 100) {
            mensaje.textContent = 'Por favor, introduce un número válido entre 1 y 100.';
            return;
        }
    
        if (numeroIngresado === numeroAzar) {
            mensaje.textContent = '¡Felicidades! ¡Has adivinado el número correcto!';
            mensaje.style.color = 'green';
            numeroEntrada.disabled = true;
        } else if (numeroIngresado < numeroAzar) {
            mensaje.textContent = 'El número es mayor. Intenta de nuevo.';
            mensaje.style.color = 'red';
        } else {
            mensaje.textContent = 'El número es menor. Intenta de nuevo.';
            mensaje.style.color = 'red';
        }
    }

Esta función se llama cuando el usuario presiona el botón de "Comprobar". Primero, obtiene el número ingresado por el usuario utilizando `numeroEntrada.value` y lo convierte a un número entero utilizando `parseInt()`. Luego, verifica si el número ingresado es un número válido dentro del rango esperado (1-100). Si el número no es válido, se muestra un mensaje de error en el elemento "mensaje" y se devuelve de la función.

Si el número ingresado es válido, se compara con el número generado aleatoriamente. Si son iguales, se muestra un mensaje de felicitación y se deshabilita el campo de entrada. Si el número ingresado es menor que el número aleatorio, se muestra un mensaje indicando que el número es mayor. Si es mayor, se muestra un mensaje indicando que el número es menor. En ambos casos, el mensaje se muestra en el elemento "mensaje" y se cambia el color del texto al rojo.

## Uso del juego

1.  Clona o descarga este repositorio en tu computadora.
2.  Abre el archivo `index.html` en tu navegador web.
3.  Verás una interfaz de usuario con un campo de entrada y un botón de "Comprobar".
4.  Ingresa un número válido entre 1 y 100 en el campo de entrada y presiona el botón de "Comprobar".
5.  Dependiendo de tu número ingresado, recibirás mensajes indicando si el número es mayor o menor que el número aleatorio, o si has adivinado correctamente.
6.  Si adivinas correctamente, el campo de entrada se deshabilitará y se mostrará un mensaje de felicitación.

¡Diviértete jugando y practicando tus habilidades en Javascript!
