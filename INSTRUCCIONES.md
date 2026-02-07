# FinControl PWA — Instrucciones de Instalación en Android

## Archivos incluidos

```
fincontrol-pwa/
├── index.html          ← App principal
├── manifest.json       ← Configuración PWA
├── sw.js              ← Service Worker (funciona offline)
└── icons/
    ├── icon-192.png   ← Ícono app
    └── icon-512.png   ← Ícono app HD
```

## Opción 1: Hosting gratuito (recomendado)

### Con GitHub Pages:
1. Crea un repositorio en GitHub (ej: `fincontrol`)
2. Sube todos los archivos del ZIP al repositorio
3. Ve a **Settings → Pages → Source: main branch**
4. Tu app estará en: `https://tu-usuario.github.io/fincontrol/`
5. Abre esa URL en Chrome en tu Android
6. Aparecerá un banner "Instalar FinControl" → toca **Instalar**

### Con Netlify (más fácil):
1. Ve a [netlify.com](https://netlify.com) y crea cuenta gratis
2. Arrastra la carpeta descomprimida al panel de Netlify
3. Te dará una URL pública
4. Abre en Chrome Android → **Instalar**

### Con Firebase Hosting:
```bash
npm install -g firebase-tools
firebase login
firebase init hosting   # Elige la carpeta fincontrol-pwa como public
firebase deploy
```

## Opción 2: Servidor local en tu red

Si solo quieres usarlo en tu red WiFi:

```bash
# Con Python (en la carpeta del proyecto)
cd fincontrol-pwa
python3 -m http.server 8080

# Con Node.js
npx serve .
```
Luego abre `http://TU-IP-LOCAL:8080` desde Chrome en Android.

> ⚠️ Para que la instalación PWA funcione, necesitas HTTPS o localhost.
> GitHub Pages y Netlify ya incluyen HTTPS automáticamente.

## Instalación en Android

1. Abre la URL de tu app en **Google Chrome**
2. Si aparece el banner inferior, toca **"Instalar"**
3. Si no aparece, toca el menú ⋮ → **"Instalar app"** o **"Añadir a pantalla de inicio"**
4. La app aparecerá como ícono en tu launcher
5. Se abre a pantalla completa, sin barra del navegador
6. Funciona **sin conexión** después de la primera carga

## Características Android

- ✅ Funciona offline (Service Worker)
- ✅ Ícono en pantalla de inicio
- ✅ Pantalla completa sin barra del navegador
- ✅ Inputs optimizados para táctil (mínimo 44px)
- ✅ Soporte para notch/safe areas
- ✅ Datos guardados en localStorage del dispositivo
- ✅ Exportar/Importar JSON para respaldos
