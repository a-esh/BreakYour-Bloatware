# Tutorial: Desinstalar Bloatware en Android con ADB

---

## 1. Introducción al Bloatware

El bloatware es un software no deseado preinstalado en los dispositivos Android por los fabricantes. Comprender por qué se incorpora es crucial para decidir si eliminarlo. En este tutorial, aprenderás a desinstalar bloatware de forma segura utilizando ADB.

---

## 2. Herramientas Necesarias

Para realizar la eliminación de bloatware de manera segura, necesitarás las siguientes herramientas:

* **ADB (Android Debug Bridge):** Una herramienta de línea de comandos que te permite interactuar con un dispositivo Android conectado a tu computadora.
  
* **ADB Drivers:** Asegúrate de tener los controladores ADB instalados en tu computadora para reconocer tu dispositivo.

Para descargar el SDK Platform Tools desde el sitio oficial de Android Developers, sigue estos pasos:

1. **Accede al Sitio Oficial:**
   Abre tu navegador web y ve a la página oficial de Android Studio Platform Tools: [https://developer.android.com/studio/releases/platform-tools?hl=es-419](https://developer.android.com/studio/releases/platform-tools?hl=es-419).

2. **Desplázate hacia Abajo:**
   Desplázate hacia abajo en la página hasta que encuentres la sección "Descargas de herramientas de plataforma".

3. **Selecciona tu Sistema Operativo:**
   Haz clic en el enlace de descarga correspondiente a tu sistema operativo. Puedes elegir entre Windows, macOS o Linux.

4. **Descarga del Archivo ZIP:**
   Serás redirigido a la sección de descargas. Haz clic en el enlace para descargar el archivo ZIP de Platform Tools.

5. **Extraer el Contenido:**
   Una vez que la descarga esté completa, extrae el contenido del archivo ZIP a una ubicación en tu computadora.

6. **Agregar a la Ruta del Sistema (Opcional):**
   Para facilitar el uso de las herramientas desde cualquier ubicación en la línea de comandos, puedes agregar la carpeta donde extrajiste Platform Tools a la variable de entorno PATH. Esto permite ejecutar comandos ADB desde cualquier directorio.

   - **En Windows:**
     Agrega la ruta completa de la carpeta a la variable de entorno PATH siguiendo [estos pasos](https://www.architectryan.com/2018/03/17/add-to-the-path-on-windows-10/).

   - **En Linux o macOS:**
     Abre el archivo `~/.bashrc`, `~/.bash_profile`, o `~/.zshrc` con un editor de texto y añade la línea:
     ```bash
     export PATH=$PATH:/ruta/del/directorio/platform-tools
     ```
     Luego, ejecuta `source ~/.bashrc`, `source ~/.bash_profile`, o `source ~/.zshrc` para aplicar los cambios.

>¡Ahora deberías tener ADB y otras herramientas de Platform Tools listas para usar en tu sistema! Puedes verificar la instalación ejecutando `adb version` en la línea de comandos.

* **Editor de Texto (Opcional):** Para crear listas personalizadas de bloatware a desinstalar.

---

## 3. Identificación del Bloatware

Es importante diferenciar entre las aplicaciones esenciales del sistema y el bloatware. Puedes encontrar listas de bloatware específicas para tu dispositivo en [este enlace](https://github.com/A-esh/BreakYour-Bloatware/tree/main/lists_Bloatware).

---

## 4. Deshabilitación Segura

Sigue estos pasos para deshabilitar aplicaciones no deseadas sin acceso root:

**a. Conectar el Dispositivo:**
   Conecta tu dispositivo Android a la computadora mediante un cable USB y acepta la depuración usb con el ordenador.

**b. Verificar Conexión:**
   Abre una terminal y ejecuta el siguiente comando para verificar que el dispositivo está conectado:
   ```
   adb devices
   ```
> Error:  El término 'adb' no se reconoce como nombre de un cmdlet, función, archivo de script o programa ejecutable.
>Compruebe si escribió correctamente el nombre o, si incluyó una ruta de acceso, compruebe que dicha ruta es correcta e
>inténtelo de nuevo.
>
> No se encontró el comando adb, pero existe en la ubicación actual. Windows PowerShell no carga comandos de la ubicación actual de forma predeterminada.
> Para solucionar este error usa el sufijo `.\` Ejemplo:
>```
>  .\adb devices
>```

> El siguiente error es provocado por no haber autorizado la depuracíon usb desde el smartphone, reactiva la depuración usb y revoca las autorizaciones existentes.
>```
><ANDROID_SDK_HOME>\platform-tools>adb devices
>List of devices attached
>0a0a0b0a0a0b0a0      unauthorized
>```
**c. Acceder al Shell:**
   Accede al shell del dispositivo con el siguiente comando:
   ```
   adb shell
   ```

**d. Listar Todas las Aplicaciones:**
   Utiliza el siguiente comando para listar todas las aplicaciones instaladas:
   ```
   pm list package
   ```

**e. Desinstalar Aplicación:**
   Para desinstalar una aplicación específica, usa el siguiente comando:
   ```
   pm uninstall -k --user 0 com.package.app
   ```

---

## 5. Consejos y Precauciones

* **Copia de Seguridad:**
   Antes de desinstalar cualquier aplicación, realiza una copia de seguridad de tus datos importantes para evitar pérdidas accidentales.

* **Revertir Cambios:**
   Si experimentas problemas, puedes revertir los cambios realizados al restablecer el dispositivo a la configuración de fábrica.

---

## 6. Contribuciones y Problemas

¡Invitamos a la comunidad a contribuir! Comparte métodos adicionales, herramientas y experiencias sobre la eliminación de bloatware en [GitHub](https://github.com/A-esh/BreakYour-Bloatware). Si encuentras problemas o necesitas ayuda, puedes informarlos [aquí](https://github.com/A-esh/BreakYour-Bloatware/issues).

---

**¡Recuerda!** La eliminación de bloatware puede variar según el fabricante y modelo del dispositivo. Siempre ten precaución y sigue las recomendaciones específicas para tu dispositivo.

---

Documentación creada por **@abraham_esh** para **ByteYourCode by abraham_esh**. 

<br>

 **Apache License 2.0** 

[TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION](https://github.com/A-esh/BreakYour-Blotware/blob/main/LICENSE).

---

[![GitHub](https://img.shields.io/badge/GitHub-Mi_perfil-5B47ED?style=for-the-badge&logo=github&logoColor=white&labelColor=101010)](https://github.com/A-esh)

[![Youtube](https://img.shields.io/badge/Youtube_Programación-Byte_Your_Code-FF0000?style=for-the-badge&logo=youtube&logoColor=white&labelColor=101010)](https://www.youtube.com/channel/UCSki3rWVSXcFRTKYY9F0wjQ)

### Redes:
[![Youtube](https://img.shields.io/badge/Youtube_Personal-abraham_esh-FF0000?style=for-the-badge&logo=youtube&logoColor=white&labelColor=101010)](https://www.youtube.com/channel/UCSH1XcdzydJAUu388EhaQwA) [![Twitch](https://img.shields.io/badge/Twitch-Directos-9146FF?style=for-the-badge&logo=twitch&logoColor=white&labelColor=101010)](https://twitch.com/abraham_esh) [![Linkedin](https://img.shields.io/badge/Linkedin-Perfil_Profesional-2867B2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=101010)](https://www.linkedin.com/in/abraham-esh/) [![X](https://img.shields.io/badge/Twitter-X-000000?style=for-the-badge&logo=x&logoColor=white&labelColor=101010)](https://twitter.com/abraham_esh)[![Tiktok](https://img.shields.io/badge/TikTok-Tutoriales%20rapidos-ff0050?style=for-the-badge&logo=tiktok&logoColor=white&labelColor=000000)](https://www.tiktok.com/@abraham_esh) 

### Comunidad:
[![Discord](https://img.shields.io/badge/Discord-Canal_de_la_comunidad-5865F2?style=for-the-badge&logo=discord&logoColor=white&labelColor=101010)](https://discord.gg/eh7BFDB)
