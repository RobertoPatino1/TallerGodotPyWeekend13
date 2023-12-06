# Taller de Godot PyWeekend 13ava edición
Dictado por: Roberto Patiño

## Introducción
En este taller teórico-práctico se estudiará a fondo el uso del motor de desarrollo de videojuegos Godot así como cada uno de sus componentes y características principales.<br>
Al finalizar las sesiones del taller los asistentes estarán en la capacidad de desarrollar un videojuego robusto en Godot y exportarlo para su ejecución en dispositivos Android.

## Herramientas requeridas
- [Godot Game Engine](https://godotengine.org/) 
- [JDK 17](https://adoptium.net/es/temurin/releases/?variant=openjdk17)
- [Android Studio](https://developer.android.com/studio?gclid=Cj0KCQiAsburBhCIARIsAExmsu4zb2t9v_2GhhZJd011FGPlvG8UlfV9CCersYc5mjEtH1QhoNKl1cIaAum2EALw_wcB&gclsrc=aw.ds&hl=es-419)


## Configuraciones requeridas
### Descargar paquetes dentro del SDK manager en Android Studio
Para garantizar la compatibilidad con dispositivos Android se deben
instalar ciertos paquetes desde el SDK manager en Android Studio.
A continuación se provee el siguiente [enlace](https://developer.android.com/studio/intro/update?hl=es-419#sdk-manager) con la guía para instalar dichos
paquetes.<br>
Los paquetes requeridos son:
- Android SDK Platform-Tools version 30.0.5 or later
- Android SDK Build-Tools version 33.0.2
- Android SDK Platform 33
- Android SDK Command-line Tools (latest)
- CMake version 3.10.2.4988404
- NDK version r23c (23.2.8568313)


### Crear un archivo debug keystore
Android requiere de un archivo debug keystore para instalar y distribuir
APKs en los dispositivos a usar.
Para esto se debe abrir una terminal/consola de comandos dentro de
una carpeta, luego se debe ejecutar el siguiente comando
```bash
keytool -keyalg RSA -genkeypair -alias androiddebugkey -keypass android -keystore debug.keystore -storepass android -dname "CN=Android Debug,O=Android,C=US" -validity 9999 -deststoretype pkcs12
```

Una vez ejecutado el comando se creará un archivo llamado debug.keystore en la carpeta actual. Se debe tomar en cuenta la carpeta donde este se encuentra guardado. De preferencia colocarlo en la misma carpeta del proyecto Godot.


### Vincular las configuraciones con Godot
Una vez creado un proyecto en Godot se deben seguir sólo las
instrucciones correspondientes a la sección [Instalándolo en Godot](https://docs.godotengine.org/es/4.x/tutorials/export/exporting_for_android.html#setting-it-up-in-godot) de la documentación oficial. <br>

Finalmente se debe exportar el proyecto siguiendo los pasos presentes
en la sección [Exportar para la Google Play Store](https://docs.godotengine.org/es/4.x/tutorials/export/exporting_for_android.html#exporting-for-google-play-store)


## Material de consulta adicional

### Documentación y tutoriales
- [Documentación oficial de Godot](https://docs.godotengine.org/es/4.x/)
- [Documentación oficial de Godot - Despliegue en Android](https://docs.godotengine.org/es/4.x/tutorials/export/one-click_deploy.html)
- [Documentación oficial de Godot - Exportación para Android](https://docs.godotengine.org/es/4.x/tutorials/export/exporting_for_android.html)
- [Tutorial paso a paso para ejecutar/exportar juegos desde Godot
a Android (ES - Windows)](https://www.youtube.com/watch?v=B0fq_hC3hM4&ab_channel=LeedeoStudio)
- [Tutorial paso a paso para ejecutar/exportar juegos desde Godot
a Android (EN - Linux)](https://www.youtube.com/watch?v=-N5ETg6cBu0&ab_channel=BlenderLetsPlay%21)

### Manejo de errores
- [Solución para posible error ETC2/ASTC (EN)](https://www.reddit.com/r/godot/comments/16d15in/error_when_trying_to_export_project_on_android/)
- [Solución para posible error No se muestra el ícono de android en Godot
(EN)](https://www.reddit.com/r/godot/comments/e11l22/the_android_icon_is_not_showing_up_in_the_godot/)
