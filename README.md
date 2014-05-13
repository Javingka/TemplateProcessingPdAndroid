TemplateProcessingPdAndroid
===========================

Template to develop Android projects using Processing (with multiTouch) and Puredata (with libPd) in Eclipse

Este proyecto es una plantilla para el desarrollo de aplicaciones Android en Eclipse, usando Processing y Puredata para el 
desarrollo de soluciones visuales y sonoras. Incluye una clase para acceder fácil y directamente a información Multitouch y
otra clase para definir los aspectos necesarios para el uso de Puredata por medio de la libreria libPd, y al mismo tiempo 
ofrece un set de métodos CallBacks que agiliza y facilita el uso de esta libreria programando con Processing.

...........

1.- Copiar el directorio

2.- Cambiar el nombre del paquete en AndroidManifest.xml y de la aplicación en /res/values/strings.xml

3.- Luego se renombra el paquete principal con Refractor en todas las carpetas dentro de /src
	Se renombra también en el import en MainActivity.java

4- Dentro de la clase "MainActivity.java", hay que reemplazar dentro de la función mGlobal_OnClickListener el 
caminho de el path " com.example.template. ", por el nombre nuevo del paquete.

5- Comprime el patch de pure data junto a todos los archivos asociados en un .zip de nombre "patch.zip"

6- Colocar el archivo .zip dentro de la carpeta res/raw 

7- dentro de PAppletInicial, en el metodo Oncreate() tienes que colocar el nombre del patch de PD que vas a utilizar
 y reemplazar nuevamente el nombre del paquete. 
 Modifica el siguiente método
 pdManager.openPatch(" nome_do_patch.pd ", com.example.template.R.raw.patch); 
 
5.- Dentro de OnCreate() en la clase PAppletInicial() tienes que declarar todos los strings que definiran los mensajes que se 
 reciben de PD
 
 
