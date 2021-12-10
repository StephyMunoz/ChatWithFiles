## Prueba 1: Chat con subida de archivos
#### Stephanie Muñoz, Mateo Borja, Stiven López

Esta es una aplicación realizada con Ionic y utilizando FireStore de FireBase. En las siguientes figuras se muestra la estructura del proyecto, el cual consta de varias páginas y servicios

![1](https://user-images.githubusercontent.com/66144847/145636022-eac49af1-d352-4652-ad32-5b0491b0786d.jpeg)
Fig. 1 Estructura del proyecto (1)

![1](https://user-images.githubusercontent.com/66144847/145636171-0804434e-0ac7-45aa-80e4-fea1c70d9979.jpeg)
Fig. 2 Estructura del proyecto (2)

La aplicación cuenta con las siguientes partes:

#### Página de ingreso:

En esta página se deberá iniciar sesión o registrarse antes de acceder al chat, existen botones para estas opciones así como un enlace que permite reestablecer la contraseña. Si el usuario ya está registrado, podrá ingresar con su correo y contraseña.

![1](https://user-images.githubusercontent.com/66144847/145636733-a34a0673-cb4c-4ba2-a94d-10eb8b444a96.jpeg)
Fig. 3 Página de ingreso

En su HTML se pueden observar los botones así como los diferentes mensajes que se muestran si el usuario no ingresa sus credenciales correctamente

![image](https://user-images.githubusercontent.com/66144847/145636905-a49591c2-c5e8-42b3-9b23-b77fe014e853.png)
Fig. 4 login.page.html

El archivo TS contiene las funciones para validar las credenciales así como registrar una nueva cuenta o acceder con una existente, todo esto se realiza a través de campos de formulario y alertas. Si todo sale bien, la aplicación redirigirá al chat.

![image](https://user-images.githubusercontent.com/66144847/145637546-2fb37440-6597-43e1-bfec-f6c69b01bb8c.png)
Fig. 5 login.page.ts con validación de credenciales

![image](https://user-images.githubusercontent.com/66144847/145637597-327fd9f9-7f28-4710-adda-4626bb934fd2.png)
Fig. 6 Función de registro

![image](https://user-images.githubusercontent.com/66144847/145637628-f42489e3-ffb1-4534-870d-d11b2558522b.png)
Fig. 7 Función de ingreso y getters de los campos

#### Reestablecimiento de Contraseña:
Si se hace click en la opción de olvido de contraseña ubicada bajo los botones de ingreso y registro, se redirigirá a una página sencilla donde se debe ingresar el correo electrónico registrado, es importante que este correo sea válido ya que se utilizará para enviar un mensaje con un link que permite reestablecer la contraseña. Una vez hecho esto, se podrá ingresar con la nueva contraseña.

![image](https://user-images.githubusercontent.com/66144847/145638047-4043d67b-1057-4f72-ac05-cbc6db718bac.png)
Fig. 8 Ingreso de correo para reestablecer contraseña

![image](https://user-images.githubusercontent.com/66144847/145638134-85d6932a-528c-42dd-b528-1aadb47a88bc.png)
Fig. 9 Mensaje enviado al correo

![image](https://user-images.githubusercontent.com/66144847/145638181-0cd8cf42-5c75-43bf-a49d-c94009f26776.png)
Fig. 10 Reestableciendo la contraseña

Lá página de reestablecimiento es muy sencilla, su HTML refleja esto

![image](https://user-images.githubusercontent.com/66144847/145638440-b8464bf1-60e6-4522-9e68-2fd55f007315.png)
Fig. 11 forgotpass.page.html

En archivos TS se encuentran las funciones de reseteo de contraseña, así como un servicio de autenticación que envía el mensaje al correo

![image](https://user-images.githubusercontent.com/66144847/145638739-1558266a-2def-481e-a317-07418c9031c8.png)
Fig. 12 forgotpass.page.ts

![image](https://user-images.githubusercontent.com/66144847/145638782-dd80178e-8a13-406b-901c-b3b2b0739985.png)
Fig. 13 auth.service.ts


