Notas de la versión
**************************************************
Siga las instrucciones en el manual ` manual de actualización <../Installing-AndroidAPS/Update-to-new-version.html>`_. También puede encontrar una sección de resolución de problemas que se ocupa de las dificultades más comunes cuando se actualiza en la página de actualización manual.

Recibirá la siguiente información tan pronto como se disponga de una nueva actualización:

.. imagen:: ../images/AAPS_LoopDisable90days.png
  :alt: Información de actualización

Entonces tienes 60 días para actualizarte. Si no actualiza dentro de estos 60 días, la AAPS retrocederá a LGS (suspensión de glucosa baja -ver `glosario <../Getting-Started/Glossary.html>`_) como en el `objetivo 6 <../Usage/Objectives.html>`_.

Si no se actualiza durante otros 30 días (90 días a partir de la fecha de la nueva versión), AAPS cambiará a Lazo Abierto.

Por favor, entienda que este cambio no tiene la intención de molestarlo, sino que se debe a razones de seguridad. Las nuevas versiones de AndroidAPS no sólo proporcionan nuevas características, sino también importantes arreglos de seguridad. Por lo tanto, son necesarias que todas las actualizaciones de usuario a.s.a.p. (Lo antes posible).. Desafortunadamente, todavía hay informes de error de versiones muy antiguas, por lo que esto es un intento de mejorar la seguridad para cada usuario y toda la comunidad de DIY. Gracias por tu comprensión.

Version 2.6.1
==============
Release date: 21-03-2020

Please use `Android Studio 3.6.1 <https://developer.android.com/studio/>`_ or newer to build the apk.

Nuevas características importantes
-----
* Allow to enter only https:// in NSClient settings
* Fixed `BGI <../Getting-Started/Glossary.html>`_ displaying bug on watches
* Fixed small UI bugs
* Fixed Insight crashes
* Fixed future carbs with Combo pump
* Fixed `LocalProfile -> NS sync <../Configuration/Config-Builder.html#upload-local-profiles-to-nightscout>`_
* Insight alerts improvements
* Improved detection of boluses from pump history
* Fixed NSClient connection settings (wifi, charging)
* Fixed sending of calibrations to xDrip

Version 2.6.0
==============
Release date: 29-02-2020

Please use `Android Studio 3.6.1 <https://developer.android.com/studio/>`_ or newer to build the apk.

Nuevas características importantes
-----
* Small design changes (startpage...)
* Careportal tab / menu removed - more details `here <../Usage/CPbefore26.html>`_
* New `Local Profile plugin <../Configuration/Config-Builder.html#local-profile-recommended>`_

  * Local profile can hold more than 1 profile
  * Profiles can be cloned and edited
  * Ability of upload profiles to NS
  * Old profile switches can be cloned to new profile in LocalProfile (timeshift and percentage is applied)
  * Veritical NumberPicker for targets
* SimpleProfile is removed
* `Extended bolus <../Usage/Extended-Carbs.html#id1>`_ feature - closed loop will be disabled
* MDT plugin: Fixed bug with duplicated entries
* Units are not specified in profile but it's global setting
* Added new settings to startup wizard
* Different UI and internal improvements
* `Wear complications <../Configuration/Watchfaces.html>`_
* New `SMS commands <../Children/SMS-Commands.html>`_ BOLUS-MEAL, SMS, CARBS, TARGET, HELP
* Fixed language support
* Objectives: `Allow to go back <../Usage/Objectives.html#go-back-in-objectives>`_, Time fetching dialog
* Automation: `allow sorting <../Usage/Automation.html#sort-automation-rules>`_
* Automation: fixed bug when automation was running with disabled loop
* New status line for Combo
* GlucoseStatus improvement
* Fixed TempTarget NS sync
* New statistics activity
* Allow Extended bolus in open loop mode
* Android 10 alarm support
* Tons on new translations

Versión 2.5.1
==================================================
Fecha de lanzamiento: 31-10-2019

Tenga en cuenta las `notas importantes <../Installing-AndroidAPS/Releasenotes.html#important-notes>` _ y `limitaciones <../Installing-AndroidAPS/Releasenotes.html#is-this-update-for-me-actualmente-is-not-soportado>` _ listados para `version 2.5.0 <../Installing-AndroidAPS/Releasenotes.html#version-2-5-0>`_. 
* Se corrigió un error en el receptor de estado de red que conduce a muchos fallos (no críticos, sino que desperdiciarían mucha energía en el recálculo de cosas).
* Nuevo mantenimiento de versiones que permitirá realizar actualizaciones menores sin activar la notificación de actualización.

Versión 2.5.0
==================================================
Fecha de lanzamiento: 26-10-2019

Notas importantes
--------------------------------------------------
* Utilice `Android Studio Version 3.5.1 <https://developer.android.com/studio/>`_ o más reciente para `crear el apk <../Installing-AndroidAPS/Building-APK.html>` _ o `actualización <../Installing-AndroidAPS/Update-to-new-version.html>`_.
* Si está utilizando xDrip `identificar el receptor <../Configuration/xdrip.html#identify-receiver>`_ debe establecerse.
* Si utiliza Dexcom G6 con el `la app Dexcom parchada <../Hardware/DexcomG6.html#if-using-g6-with-patched-dexcom-app>` _ necesitará la versión de la `carpeta 2.4 <https://github.com/dexcomapp/dexcomapp/tree/master/2.4>`_.
* Glimp is supported from version 4.15.57 and newer.

¿Es esta actualización para mí? Actualmente NO es soportado
--------------------------------------------------
* Android 5 e inferiores
* Poctech
* 600SeriesUploader
* Dexcom Parchado desde el directorio 2.3

Nuevas características importantes
--------------------------------------------------
* Cambio interno de targetSDK a 28 (Android 9), soporte de jetpack
* Soporte de RxJava2, Okhttp3, Retrofit
* Viejo bombas "Medtronic" `Medtronic <../Configuration/MedtronicPump.html>`_ soporte (se necesita RileyLink)
* Nuevo " plugin de Automatización <../Usage/Automation.html>`_
* Permitir `solo una parte de bolo <../Configuration/Preferences.html#advanced-settings>` _ desde el asistente de cálculo de bolos
* Representación de la actividad de la insulina
* Ajustar las predicciones de IOB por el resultado de autodetección
* Nuevo soporte para los apks de Dexcom parcheados (` 2.4 carpeta <https://github.com/dexcomapp/dexcomapp/tree/master/2.4>`_)
* Verificador de firma
* Permite saltar objetivos para usuarios de OpenAPS
* Nuevos `objetivos <../Usage/Objectives.html>`_ - examinar, manejo de aplicaciones
   
   (Si ha iniciado al menos el objetivo "Iniciar en un lazo abierto" en las versiones anteriores, el examen es opcional.)
* Corregido el bug en controladores Dana* donde se informó una falsa diferencia de tiempo
* Se ha corregido el error en `SMS communicator <../Children/SMS-Commands.html>`_

Versión 2.3
==================================================
Fecha de lanzamiento: 25-04-2019

Nuevas características importantes
--------------------------------------------------
* Mejora de seguridad importante para Insight (realmente importante si se utiliza Insight!)
* Se corrigió el Historial
* Se corrigieron los cálculos delta
Actualización de idiomas
* Se verifica el GIT y se advierte sobre la actualización de gradle
* Más pruebas automáticas
* Arreglo de accidentes potenciales en el servicio AlarmSound (gracias a @lee-b!)
* Revisión de difusión de datos de BG (ahora funciona de forma independiente de los permisos de SMS!)
* Nuevo Verificador de Versiones


Versión 2.2.2
==================================================
Fecha de lanzamiento: 07-04-2019

Nuevas características importantes
--------------------------------------------------
* Arreglo de autosens: desactive el objetivo temporal de elevación/baja de TT
Nuevas traducciones
* Corrección de controladores de bomba Insight
* Arreglo de plug-in de SMS


Versión 2.2
==================================================
Fecha de lanzamiento: 29-03-2019

Nuevas características importantes
--------------------------------------------------
* `Arreglo DST <../Usage/Timezone-traveling.html#time-adjustment-daylight-savings-time-dst>`_
* Actualización de reloj
* `Plugin de SMS <../Children/SMS-Commands.html>`_ actualización
* Volver a los objetivos.
* Detener lazo si la memoria del teléfono está llena


Versión 2.1
==================================================
Fecha de lanzamiento: 03-03-2019

Nuevas características importantes
--------------------------------------------------
* `Accu-Chek Insight <../Configuration/Accu-Chek-Insight-Pump.html>`_ soporte (by Tebbe Ubben and JamOrHam)
* Luces de estado en la pantalla principal (Nico Schmitz)
* Horario de de verano (Roumen Georgiev)
* Arreglo de nombres de perfiles de NS (Johannes Mockenhaupt)
* Arreglo de Bloqueo de UI (Johannes Mockenhaupt)
* Soporte para la app actualizada del G5 (Tebbe Ubben y Milos Kozak)
* G6, Poctech, Tomate, Eversense BG soporte de origen (Tebbe Ubben y Milos Kozak)
* Se ha corregido la desactivación de SMB en preferencias (Johannes Mockenhaupt)

Misceláneo
--------------------------------------------------
* Si utiliza un valor no predeterminado `smbmaxminutes`, tienes que volver a configurar este valor


Versión 2.0
==================================================
Fecha de lanzamiento: 03-11-2018

Nuevas características importantes
--------------------------------------------------
* soporte oref1/SMB (`oref1 documentation <https://openaps.readthedocs.io/en/latest/docs/Customize-Iterate/oref1.html>`_) Esté seguro de leer la documentación para conocer que esperar de SMB, como se va a comportar, que puede alcanzar, como usarlo y operarlo suavemente.
* `_Accu-Chek Combo <../Configuration/Accu-Chek-Combo-Pump.html>`_ soporte de la bomba
* Asistente de configuración: le guiará a través del proceso de configuración de AndroidAPS

Valores para ajustar cuando se cambia de AMA a SMB
--------------------------------------------------
* El objetivo 10 debe iniciarse para que las SMB estén habilitadas (la pestaña SMB muestra generalmente las restricciones que se aplican)
* maxIOB ahora incluye _all_ IOB, no sólo el basal añadido. Es decir, si se le da un bolo de 8 U para una comida y maxIOB es 7 U, no se entregarán SMB hasta que el IOB caiga por debajo de 7 U.
* El valor predeterminado de min_5m_carbimpact ha cambiado de 3 a 8 llendo de AMA a SMB. Si está actualizando desde AMA a SMB, tiene que cambiarlo manualmente
* Nota cuando se construya AndroidAPS 2.0 apk: La configuración personalizada no está soportada por la versión actual del plugin de Android Gradle! Si la compilación falla con un error en la configuración personalizada, puede realizar lo siguiente:

   * Abra la ventana de Preferencias, haga clic en Archivo > Configuración (en Mac, Android Studio > Preferencias).
   * En el panel de la izquierda, pulse Compilar, Ejecución, Deployment > Compilador.
   * Desmarque la casilla de verificación Configurar bajo demanda.
   * Haga clic en Aplicar o en Aceptar.

Pestaña general
--------------------------------------------------
* La cinta de arriba da acceso a suspensión/desactivación del lazo, ver/ajuste perfil y a inicio/detención de objetivos temporales (TTs). Los TTs utilizan los valores predeterminados establecidos en las preferencias. La nueva opción de Hypo TT es una temporal alta TT para evitar que el lazo haga una sobrecorrección muy agresiva en el rescate de carbohidratos.
* Botones de tratamiento: el botón de tratamiento viejo aún está disponible, pero está oculto de forma predeterminada. Ahora la visibilidad de los botones se puede configurar. Nuevo botón de insulina, nuevo botón de carbohidratos (incluyendo `eCarbs/carbs extendidos <../Usage/Extended-Carbs.html>`_)
* `Las líneas de predicción tienen colores <../Getting-Started/Screenshots.html#section-e>`_
* Opción para mostrar un campo de notas en los diálogos de insulina/carbs/calculadora/cebado + relleno, que se suben a NS
* Actualizado el dialogo cebado/relleno permite el cebado y la creación de entradas para el careportal para el cambio de sitio y de cambio de los cartuchos

Reloj
--------------------------------------------------
* Se eliminó la variante de compilación separada, incluida en la compilación completa regular ahora. Para utilizar los controles de bolo desde el reloj, habilite este valor en el teléfono
* El asistente ahora sólo solicita carbohidratos (y el porcentaje si está habilitado en la configuración del reloj). Los parámetros que se incluyen en el cálculo se pueden configurar en la configuración del teléfono
* Las confirmaciones y los diálogos de información ahora funcionan también en el reloj 2.0
* Se añade Entrada de menú de eCarbs

Nuevos plugins
--------------------------------------------------
* PocTech app como fuente de BG
* Dexcom app parcheada como fuente BG
* Plugin de sensibilidad oref1

Misceláneo
--------------------------------------------------
* La aplicación ahora utiliza el cajón para mostrar todos los plugins; los plugins seleccionados como visibles en el creador de configuración se muestran como pestañas en la parte superior (favoritos)
* Revisión para las pestañas del constructor de configuración y objetivos, añadiendo descripciones
* Nuevo icono de la aplicación
* Muchas mejoras y correcciones de errores
* Alertas independientes de Nightscout si la bomba es inalcanzable durante más tiempo (p.ej. batería de bomba agotada) y lecturas de BG perdidas (ver _Local alerts_ en configuración)
* Opción para mantener la pantalla encendida
* Opción de mostrar notificaciónes como notificación Android
* Filtrado avanzado (que permite siempre habilitar SMB y 6h después de las comidas) soportado con el app de Dexcom o xDrip patched con el modo nativo G5 como fuente BG.
