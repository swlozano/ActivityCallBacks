# Proyecto Android - Manejo de Cambios de Configuración

Este proyecto de Android demuestra cómo manejar cambios de configuración en una actividad cuando se modifica la orientación, el diseño de pantalla o el tamaño de pantalla.

## Captura de Pantalla

![Captura de Pantalla](https://github.com/user-attachments/assets/b682d99e-302e-4caa-8add-e59a6152d3a5)

## Configuración en `AndroidManifest.xml`

Para evitar que la actividad se reinicie al cambiar ciertas configuraciones, se define la propiedad `android:configChanges` dentro del `AndroidManifest.xml`:

```xml
<activity
    android:name=".MainActivity"
    android:exported="true"
    android:configChanges="orientation|screenLayout|screenSize">
</activity>
```

## Manejo de Cambios de Configuración en `MainActivity`

Para capturar y manejar cambios de configuración sin reiniciar la actividad, se sobrescribe el método `onConfigurationChanged` en `MainActivity`:

```kotlin
override fun onConfigurationChanged(newConfig: Configuration) {
    super.onConfigurationChanged(newConfig)
    Log.d(TAG, "onConfigurationChanged: $newConfig")
}
```

### Explicación
- `onConfigurationChanged` se activa cuando ocurre un cambio en la configuración definida en `configChanges`.
- Se registra el evento en los logs mediante `Log.d(TAG, "onConfigurationChanged: $newConfig")` para facilitar la depuración.

## Cómo Ejecutar el Proyecto
1. Clonar este repositorio.
2. Abrir el proyecto en Android Studio.
3. Ejecutar la aplicación en un dispositivo o emulador.
4. Cambiar la orientación del dispositivo y observar los logs en Logcat.

## Requisitos
- Android Studio instalado.
- Dispositivo físico o emulador configurado.

## Contribuciones
Las contribuciones son bienvenidas. Por favor, abre un issue o envía un pull request con mejoras o correcciones.

## Licencia
Este proyecto está bajo la licencia [MIT](LICENSE).

