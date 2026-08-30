Password Purr (HelloPurrStarter)

Documentación del Proyecto — MIT App Inventor


Autora: Brenda Arana Gutiérrez


Descripción del Proyecto

La aplicación implementa una pantalla de inicio de sesión previa donde el usuario debe
ingresar una contraseña secreta fija (&quot;meowcat&quot;). Al autenticarse correctamente, el sistema
redirige a una segunda pantalla interactiva con la imagen de un gato que reproduce un sonido
de maullido al ser presionado.

Características Principales

Autenticación Basada en Contraseña: Validación condicional de credenciales en el
cliente antes de otorgar acceso.
Navegación Multipantalla (Multi-Screen Navigation): Transición fluida entre la pantalla
de autenticación (Screen1) y la pantalla interactiva principal (Screen2).
Manejo de Controles de Texto y Limpieza: En caso de contraseña incorrecta, se reinicia
el campo de texto (PasswordTextBox1.Text) para nuevos intentos.
Interacción Multimedia &amp; Audio: Reproducción de archivos de audio (meow.mp3 /
kitty.png) utilizando el componente Sound mediante eventos táctiles.

Lógica de Programación y Bloques Implementados

La arquitectura de bloques de la aplicación se divide según las dos pantallas activas:
 Screen1 (Autenticación):
 Button1.Click: Evalúa la condición if PasswordTextBox1.Text == &quot;meowcat&quot;.
 Si la contraseña coincide, ejecuta open another screen screenName: &quot;Screen2&quot;.
 Si no coincide (else), vacía el campo asignando &quot;&quot; a PasswordTextBox1.Text.
 Screen2 (Pantalla Interactiva):
 Button1.Click (Botón/Imagen de Gato): Al hacer clic sobre la imagen del gato, invoca
call Sound1.Play para reproducir el maullido subido a los medios del proyecto.


Arquitectura del Flujo de Aplicación
[Screen1: Contraseña &quot;meowcat&quot;] ➔ (Si es Correcta) ➔ [Screen2: &quot;Pet the Cat!&quot;]

➔ (Click en Imagen) ➔ [Sound1.Play (meow.mp3)]
