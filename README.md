# Generador Automático de APK desde HTML (GitHub Actions + Capacitor)

Este repositorio convierte automáticamente cualquier archivo HTML en un `.apk` instalable en Android, incluyendo icono personalizado, pantalla de carga (*Splash Screen*), permisos de cámara/micrófono y soporte para descarga de archivos generados desde JavaScript (`Blob` / `data:`).

## Estructura de carpetas

- **`.github/workflows/build-apk.yml`**: Flujo automático de compilación en la nube.
- **`www/index.html`**: Tu aplicación web (reemplaza este archivo por tu HTML).
- **`assets/`**:
  - `icon-only.png` (1024×1024 px): Icono de la aplicación.
  - `splash.png` (2732×2732 px): Imagen centrada de pantalla de carga.
- **`capacitor.config.json`**: Nombre de la app (`appName`) e identificador único (`appId`).

## Cómo usarlo

1. Sube todos los archivos de este ZIP a un repositorio nuevo en GitHub (manteniendo la carpeta oculta `.github/workflows/`).
2. Edita `capacitor.config.json` si quieres cambiar el nombre de la aplicación (`appName`) o su ID (`appId`).
3. Si quieres cambiar el icono o la pantalla de inicio, sustituye `assets/icon-only.png` y `assets/splash.png` respetando esos nombres y tamaños.
4. Sustituye `www/index.html` por tu archivo HTML y guarda los cambios (*Commit*).
5. Entra en la pestaña **Actions** de GitHub, abre la última ejecución completada y descarga el archivo **`Aplicacion-Android-APK`** en la sección **Artifacts**.
