# Instalación y configuración de bluetooth audio en Debian.

1. Vamos a instalar el programa para KDE, ya que existe otro programa para gnome (tales como blueman y gnome-bluetooth). los paquetes a instalar y todas sus dependencias son los siguientes: bluetooth, bluez,

`sudo apt-get install bluetooth `  

`sudo apt-get install bluez`

`sudo apt-get install bluedevil`

`sudo apt-get install bluez-firmware`

`sudo apt-get install bluez-tools`

- Yo utilizo también blueman, pero vosotros elegís el que más os guste.

2. Mi notebook posee bluetooth, le instalé Xubuntu 14.04 y anda maravillosamente para conectar mi Android. Pero al momento de intentar escuchar música con un equipo externo (usando un adaptador H163), el equipo reconocía el dispositivo pero no podía usarlo como salida de audio, no conseguía “emparejarlo”. El mensaje de error era: “Fallo en la conexión: Stream setup failed”. En ese caso:

**Asegurarse de que el paquete indicado está instalado**

`sudo apt-get install pulseaudio-module-bluetooth`

**¿Sigue sin emparejar correctamente? Ingresa esto en la terminal:**

`pactl load-module module-bluetooth-discover`

**Nota:** Reinicia el PC para asegurarte de que funciona ya correctamente. Utiliza `bluedevil-wizard` para emparejar o también `blueman-applet`.
