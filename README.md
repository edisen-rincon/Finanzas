# FinControl PWA — Instrucciones de Instalación (Android + iPhone)

## Archivos incluidos

```
fincontrol-pwa/
├── index.html                  ← App principal
├── manifest.json               ← Configuración PWA
├── sw.js                       ← Service Worker (funciona offline)
└── icons/
    ├── icon-152.png            ← Ícono iPad
    ├── icon-180.png            ← Ícono iPhone
    ├── icon-192.png            ← Ícono Android
    ├── icon-512.png            ← Ícono HD
    ├── splash-750x1334.png     ← Splash iPhone SE/8
    ├── splash-1170x2532.png    ← Splash iPhone 12/13
    ├── splash-1179x2556.png    ← Splash iPhone 14/15
    └── splash-1284x2778.png    ← Splash iPhone Pro Max
```

## Paso 1: Subir a un hosting con HTTPS

### Opción A — GitHub Pages (gratis):
1. Crea un repositorio en GitHub
2. Sube **los archivos sueltos** (NO el .zip) a la raíz del repositorio
3. Ve a Settings → Pages → Source: main branch → Save
4. Espera 2 min. Tu URL será: `https://tu-usuario.github.io/tu-repo/`

### Opción B — Netlify (más fácil):
1. Ve a netlify.com y crea cuenta gratis
2. Arrastra la carpeta descomprimida al panel de Netlify
3. Te dará una URL pública con HTTPS automático

---

## Paso 2: Instalar en Android

1. Abre la URL de tu app en **Google Chrome**
2. Aparecerá un banner inferior "Instalar FinControl" → toca **Instalar**
3. Si no aparece el banner:
   - Toca el menú ⋮ (tres puntos arriba a la derecha)
   - Toca **"Instalar app"** o **"Añadir a pantalla de inicio"**
4. La app aparecerá como ícono en tu launcher

---

## Paso 3: Instalar en iPhone / iPad

⚠️ **IMPORTANTE: Debes usar Safari.** Chrome, Firefox y otros navegadores en iOS NO soportan la instalación de PWAs.

1. Abre la URL de tu app en **Safari**
2. Toca el ícono de **Compartir** ⬆️ (cuadrado con flecha hacia arriba, en la barra inferior)
3. Desplázate hacia abajo en el menú
4. Toca **"Agregar a pantalla de inicio"** (Add to Home Screen)
5. Personaliza el nombre si quieres → toca **"Agregar"**
6. La app aparecerá como ícono en tu pantalla de inicio
7. Al abrirla, se ejecuta a pantalla completa (sin barra de Safari)

### Notas para iPhone:
- La primera vez necesitas internet para cargar. Después funciona offline.
- Los datos se almacenan en el dispositivo. No se sincronizan entre dispositivos.
- Si borras los datos de Safari, se pierden los datos de la app. Usa Exportar periódicamente.
- Las splash screens (pantallas de carga) solo aparecen cuando abres la app desde el ícono de inicio.

---

## Características

| Característica         | Android | iPhone |
|------------------------|---------|--------|
| Funciona offline       | ✅      | ✅     |
| Ícono en launcher      | ✅      | ✅     |
| Pantalla completa      | ✅      | ✅     |
| Splash screen          | ✅      | ✅     |
| Instalación automática | ✅      | ❌ (manual) |
| Navegador requerido    | Chrome  | Safari |
| Notificaciones push    | ✅      | ✅ (iOS 16.4+) |

---

## Solución de Problemas

### "No me aparece la opción de instalar" (Android)
- Asegúrate de usar **Google Chrome** (no Samsung Internet, Firefox, etc.)
- Asegúrate de estar en la URL del sitio web (github.io), no del repositorio (github.com)
- Limpia caché: Chrome → Configuración → Privacidad → Borrar datos de navegación

### "No veo Agregar a pantalla de inicio" (iPhone)
- **SOLO funciona en Safari.** Chrome en iPhone NO soporta PWAs.
- El ícono de compartir ⬆️ está en la barra inferior de Safari
- Si no ves la opción, desplázate hacia abajo en el menú de compartir

### La app muestra error 404
- Verifica que `index.html` esté en la **raíz** del repositorio (no dentro de una subcarpeta)
- Si subiste un .zip, debes descomprimirlo y subir los archivos sueltos
