## Prueba 1: Chat con subida de archivos
#### Stephanie Muñoz, Mateo Borja, Stiven López
#### Link de Youtube: https://www.youtube.com/watch?v=sN4DZB5ccbQ
#### Video posteado en Twitter: https://twitter.com/MateoNBR/status/1469420720992231426
#### Video posteado en Facebook: https://www.facebook.com/photo/?fbid=10225583277104706&set=a.1829198645663


Esta es una aplicación realizada con Ionic y utilizando FireStore de FireBase. En las siguientes figuras se muestra la estructura del proyecto, el cual consta de varias páginas y servicios

![1](https://user-images.githubusercontent.com/66144847/145636022-eac49af1-d352-4652-ad32-5b0491b0786d.jpeg)

*Fig. 1 Estructura del proyecto (1)*

![1](https://user-images.githubusercontent.com/66144847/145636171-0804434e-0ac7-45aa-80e4-fea1c70d9979.jpeg)

*Fig. 2 Estructura del proyecto (2)*

La aplicación cuenta con las siguientes partes:

#### Página de ingreso:

En esta página se deberá iniciar sesión o registrarse antes de acceder al chat, existen botones para estas opciones así como un enlace que permite reestablecer la contraseña. Si el usuario ya está registrado, podrá ingresar con su correo y contraseña.

![1](https://user-images.githubusercontent.com/66144847/145636733-a34a0673-cb4c-4ba2-a94d-10eb8b444a96.jpeg)

*Fig. 3 Página de ingreso*

En su HTML se pueden observar los botones así como los diferentes mensajes que se muestran si el usuario no ingresa sus credenciales correctamente

![image](https://user-images.githubusercontent.com/66144847/145636905-a49591c2-c5e8-42b3-9b23-b77fe014e853.png)

*Fig. 4 login.page.html*

El archivo TS contiene las funciones para validar las credenciales así como registrar una nueva cuenta o acceder con una existente, todo esto se realiza a través de campos de formulario y alertas. Si todo sale bien, la aplicación redirigirá al chat.

![image](https://user-images.githubusercontent.com/66144847/145637546-2fb37440-6597-43e1-bfec-f6c69b01bb8c.png)

*Fig. 5 login.page.ts con validación de credenciales*

![image](https://user-images.githubusercontent.com/66144847/145637597-327fd9f9-7f28-4710-adda-4626bb934fd2.png)

*Fig. 6 Función de registro*

![image](https://user-images.githubusercontent.com/66144847/145637628-f42489e3-ffb1-4534-870d-d11b2558522b.png)

*Fig. 7 Función de ingreso y getters de los campos*

#### Reestablecimiento de Contraseña:
Si se hace click en la opción de olvido de contraseña ubicada bajo los botones de ingreso y registro, se redirigirá a una página sencilla donde se debe ingresar el correo electrónico registrado, es importante que este correo sea válido ya que se utilizará para enviar un mensaje con un link que permite reestablecer la contraseña. Una vez hecho esto, se podrá ingresar con la nueva contraseña.

![image](https://user-images.githubusercontent.com/66144847/145638047-4043d67b-1057-4f72-ac05-cbc6db718bac.png)

*Fig. 8 Ingreso de correo para reestablecer contraseña*

![image](https://user-images.githubusercontent.com/66144847/145638134-85d6932a-528c-42dd-b528-1aadb47a88bc.png)

*Fig. 9 Mensaje enviado al correo*

![image](https://user-images.githubusercontent.com/66144847/145638181-0cd8cf42-5c75-43bf-a49d-c94009f26776.png)

*Fig. 10 Reestableciendo la contraseña*

Lá página de reestablecimiento es muy sencilla, su HTML refleja esto

![image](https://user-images.githubusercontent.com/66144847/145638440-b8464bf1-60e6-4522-9e68-2fd55f007315.png)

*Fig. 11 forgotpass.page.html*

En archivos TS se encuentran las funciones de reseteo de contraseña, así como un servicio de autenticación que envía el mensaje al correo

![image](https://user-images.githubusercontent.com/66144847/145638739-1558266a-2def-481e-a317-07418c9031c8.png)

*Fig. 12 forgotpass.page.ts*

![image](https://user-images.githubusercontent.com/66144847/145638782-dd80178e-8a13-406b-901c-b3b2b0739985.png)

*Fig. 13 auth.service.ts*

#### Chat y Subida de Archivos
Una vez validado el ingreso se mostrará el chat, este es similar en apariencia al de cualquier red social. Al ingresar, se observarán los mensajes enviados en anteriores sesiones, esto es posible gracias a que estos se almacenan en FireStore. Se podrá escribir un mensaje y enviarlos con el botón de la derecha.

![image](https://user-images.githubusercontent.com/66144847/145639754-8aa38ba7-b20f-43a0-aafc-7cc69f8eef45.png)

*Fig. 14 Pantalla de chat*

Arriba del input para escribir un mensaje está el botón que permite cargar un archivo, al presionarlo se abrirá la ventana que permitirá seleccionar el archivo para subir, este puede ser de cualquier formato. Se mostrará una barra de progreso, cuando esta se complete, el archivó se encontrará subido y su ruta se imprimirá para que el usuario pueda accederla o copiarla al chat de ser necesario.

![image](https://user-images.githubusercontent.com/66144847/145640070-17921dff-62e3-49bd-8903-5bb6f74ba6ce.png)

*Fig. 15 Archivo subido*

En el HTML del chat, se pueden destacar las barras de progreso de subida que muestran que tantos bytes se han subido y el porcentaje total; así como el input para enviar el mensaje

![image](https://user-images.githubusercontent.com/66144847/145640732-d6aed041-2d31-4793-8ed9-a00280315b52.png)

*Fig. 16 chat.page.html (1)*

![image](https://user-images.githubusercontent.com/66144847/145640804-cc3a15e9-b756-4d68-aa4b-33f205aa57dc.png)

*Fig. 17 chat.page.html (2)*

El TS del chat es el más largo, conteniendo una lista de variables y funciones detalladas que le dan toda la funcionalidad a la página, todo esto se muestra en las siguientes figuras:

![image](https://user-images.githubusercontent.com/66144847/145641069-89d35749-db2e-4c76-938b-c3600c79f3c6.png)

*Fig. 18 Constructor y lista de variables

![image](https://user-images.githubusercontent.com/66144847/145641586-f4faa319-e0a8-4eba-b73c-980d0092a473.png)

*Fig. 19 Funciones de recuperación de mensajes, envío de mensajes y salida de sesión

![image](https://user-images.githubusercontent.com/66144847/145642305-cc4851a3-e364-4c75-8793-935446dbbb26.png)

*Fig. 20 Función de subida de archivos, notese las variables de control de subida del archivo*

![image](https://user-images.githubusercontent.com/66144847/145642507-3d210ced-80a6-4c24-843b-c48f673f7e50.png)

*Fig. 21 Recuperación de la ruta del archivo*

Además se tiene otro archivo TS donde se detallan los servicios que tambien le dan funcionalidad al chat

![image](https://user-images.githubusercontent.com/66144847/145642858-6cb9ebc7-6029-4e1d-8e5c-6996543236cf.png)

*Fig. 22 Servicios de registro e ingreso*

![image](https://user-images.githubusercontent.com/66144847/145642968-8bbfda87-e20e-4ea4-8ed0-031fc8870306.png)

*Fig. 23 Servicio de recuperación de mensajes*

![image](https://user-images.githubusercontent.com/66144847/145643042-4e5f47d0-4142-4c65-8070-163cd67f8fe2.png)

*Fig. 23 Servicio de detalle de mensajes*

Por último, cabe mencionar que se necesita introducir las credenciales que permiten conectarse a FireBase y las rutas de la aplicación, estos dos se hallán en archivos separados, el formato del archivo a subirse también se detalla en otro archivo.

![image](https://user-images.githubusercontent.com/66144847/145643456-10236929-3128-4c09-acac-b958932f398b.png)

*Fig. 24 Formato del archivo subido*

![image](https://user-images.githubusercontent.com/66144847/145643653-7e4cc749-8f1f-4824-ad11-8bd45c946b51.png)

*Fig. 25 Rutas de la aplicación*

![image](https://user-images.githubusercontent.com/66144847/145643711-7492672d-6b0c-4a45-8e01-26ff05e9e988.png)

*Fig. 26 Credenciales de FireBase*

