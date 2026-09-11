## Primer proyecto InteliJ con control de versiones
- Una vez instalado InteliJ lo ejecutamos y nos saldra la siguiente pantalla donde seleccionaremos Customize

![IntelliJ1.png](img/IntelliJ1.png)

- Nos vamos a la sección Git y si hemos instalado correctamente git en nuestro sistema podemos darle al boton Test

![IntelliJ2.png](img/IntelliJ2.png)

- Una vez realizadas las comprobaciones pasamos a integrar nuestra cuenta de Github en la sección Github y añadiendo nuestra cuenta

![IntelliJ3.png](img/IntelliJ3.png)

- Nos pedira autorizar a que el Ide pueda acceder a nuestra cuenta de Github, 

![IntelliJ4.png](img/IntelliJ4.png)

- Autorizamos
 
![IntelliJ5.png](img/IntelliJ5.png)

- Confirmamos password

![IntelliJ6.png](img/IntelliJ6.png)


## Creando el proyecto proyectos integrado con Github

- Creamos un nuevo proyecto (Recordad que IntelliJ nos permite poner varios subproyectos dentro de un proyecto y será este único proyecto en el que mantendremos todas las prácticas del módulo)

![IntelliJ7.png](img/IntelliJ7.png)

- Nos aparecerá el jdk instalado en nuestro sistema o bien el que lleva integrado IntelliJ
- Intentaremos utilizar versiones LTS 8,11,17,21,25 según el proyecto o módulo que implementemos
- Intentaremos coger las implementaciones de Oracle aunque tenemos una versión descargable desde el IDE de Oracle más ligera
- Descargaremos y utilizaremos de forma general graalvm-jdk-21 aunque para algún módulo establezcamos otra.

![IntelliJ8.png](img/IntelliJ8_menusdk.png)

- Proseguimos creando el proyecto.

![IntelliJ8.png](img/IntelliJ8.png)

-Tomamos el template básico  y le ponemos el nombre proyectos

![IntelliJ9.png](img/IntelliJ9.png)

- Nos abrá creado la estructura básica del proyecto
 
![IntelliJ10.png](img/IntelliJ10.png)
 
- Nos vamos a la opcion VCS (Control de versiones y habilitamos la integración con el control de versiones para el proyecto

![IntelliJ11.png](img/IntelliJ11.png)

- Una vez habilitado en la sección del Git compartimos el proyecto en Github de forma privada
 
![IntelliJ12.png](img/IntelliJ12.png)

- Hacemos el primer commit, aunque lo habitual es excluir con un .ignore los archivos propios del entorno local utilizado en el desarrollo en este caso añadiendo todos los ficheros del proyecto al igual que su configuración para comprobar la correcta configuración
 
![IntelliJ13.png](img/IntelliJ13.png)

- Si todo ha ido bien debe sacarnos el siguiente mensaje 
 
![IntelliJ14.png](img/IntelliJ14.png)

- Si nos vamos a nuesta cuenta de Github debe habernos creado el repositorio privado 
 
![IntelliJ15.png](img/IntelliJ15.png)

- Al hacer click sobre el nos aparecerá el repositorio con nuestro código
 
![IntelliJ16.png](img/IntelliJ16.png)

- Solo nos queda poner de colaborador a nuestro profesor a la cuenta que os solicite para que pueda ver o modificar el código. Hacemos click en settings
 
![IntelliJ17.png](img/IntelliJ17.png)

- Accedemos a Manage Access e invitamos a nuestro profesor ( m.arnauhuerta@edu.gva.es)
 
![IntelliJ18.png](img/IntelliJ18.png)

