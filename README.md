# HW---OS-Hardening-script
Un script para el fortalecimiento y la automatización del servidor, en lenguaje de secuencias de comandos  Bash.

- La secuencia de comandos debe registrar el resultado de cada actividad en un archivo de registro log

*Actualizaciones del sistema operativo:*

- Ejecute la actualización del administrador de paquetes para actualizar cualquier paquete al último nivel. Debes
asegurarte de actualizar todo.

*Políticas de cuenta de usuario:*

• Contraseña:
- Asegúrese de que la contraseña caduque cada 3 meses
- Actualice el algoritmo hash de contraseña a SHA-512

• PAM
- Hacer cumplir contraseñas seguras (8 caracteres al menos)
- Hacer cumplir 1 política de nuevo juicio

• Sudoers
- Debería poder iniciar sesión con otro usuario que no sea root y saltar a la raíz haciendo
"sudo su -" sin solicitar una contraseña.

• Configurar un banner de inicio de sesión
  
• Permisos y propiedad de archivos predeterminados
- El comando umask (máscara de modo de creación de archivos de usuario) es un comando integrado de shell
que determina elpor defecto permisos de archivo para archivos recién creados.
  
- Haga todos los archivos creados por el usuario que definió con permisos predeterminados 700, si el archivo es
creado por un usuario diferente, entonces debería ser 755.
  
*Configuración de la red*
  
• Cortafuegos
- Habilite el Firewall y bloquee todo el tráfico entrante y permita todo el tráfico saliente.
  
• SElinux
- Deshabilitarlo, no permisivo.
  
• Antivirus
- Asegúrese de instalar un antivirus gratuito para su servidor
  
• Ajuste de SSH
- Bloquear la cuenta raíz desde el inicio de sesión a través de SSH directamente
- Asegúrese de que la directiva "modo estricto" esté habilitada
- Establezca SSH LogLevel en INFO
  
• Seguridad del núcleo:
- Habilitar protección de cookies TCP SYN
- Habilitar protección de falsificación de IP
- Habilitar ignorar solicitudes ICMP

• Inicio sesión
- Mensajes del sistema
- Rote el registro de mensajes todos los días y cree un archivo .tar con la fecha de cada rotación.
