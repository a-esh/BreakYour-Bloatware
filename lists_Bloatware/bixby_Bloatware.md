# Bloatware de Samsung Bixby

Al deshabilitar Samsung Bixby, puedes reasignar fácilmente el botón power-cum-Bixby en tu dispositivo Samsung utilizando una aplicación de reasignación de botones de la Play Store.

1. **com.samsung.android.bixby.wakeup**
   - Despertador de Bixby en dispositivos Samsung.

2. **com.samsung.android.app.spage**
   - Lanzador de la página de inicio de Bixby.

3. **com.samsung.android.app.routines**
   - Rutinas de Bixby.

4. **com.samsung.android.bixby.service**
   - Funciones de Bixby.

5. **com.samsung.android.visionintelligence**
   - Visión de Bixby.

6. **com.samsung.android.bixby.agent**
   - Bixby Voice.

7. **com.samsung.android.bixby.agent.dummy**
   - Aplicación de depuración Bixby.

8. **com.samsung.android.bixbyvision.framework**
   - Marco de visión de Bixby.

Después de deshabilitar Bixby, puedes explorar aplicaciones de reasignación de botones en la Play Store para personalizar la función del botón dedicado a Bixby en tu dispositivo Samsung.

Recuerda tener precaución al deshabilitar aplicaciones del sistema, ya que algunas pueden estar interconectadas con funciones esenciales del sistema operativo.

**Copiar y pegar en la consola de PowerShell:**
```powershell
pm uninstall -k --user 0 com.samsung.android.bixby.wakeup
pm uninstall -k --user 0 com.samsung.android.app.spage
pm uninstall -k --user 0 com.samsung.android.app.routines
pm uninstall -k --user 0 com.samsung.android.bixby.service
pm uninstall -k --user 0 com.samsung.android.visionintelligence
pm uninstall -k --user 0 com.samsung.android.bixby.agent
pm uninstall -k --user 0 com.samsung.android.bixby.agent.dummy
pm uninstall -k --user 0 com.samsung.android.bixbyvision.framework
```