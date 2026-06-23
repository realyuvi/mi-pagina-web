# Mi Página Web - Modelos 3D

Repositorio para servir modelos 3D (`.glb`) e imágenes mediante GitHub Pages.

## 📁 Estructura

```
mi-pagina-web/
├── modelos/
│   └── modelo.glb
├── imagenes/
│   └── imagen.jpg
└── README.md
```

## 🚀 Cómo usar

### 1. Subir tus archivos
- Coloca tus modelos `.glb` en la carpeta `/modelos/`
- Coloca tus imágenes en la carpeta `/imagenes/`

### 2. URLs públicas
Una vez activado GitHub Pages, tus archivos estarán disponibles en:
- **Modelos:** `https://realyuvi.github.io/mi-pagina-web/modelos/tumodelo.glb`
- **Imágenes:** `https://realyuvi.github.io/mi-pagina-web/imagenes/tuimagen.jpg`

### 3. Usar en Wix
Inserta un elemento HTML en Wix y copia el código siguiente, reemplazando las URLs:

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<div id="canvas-container" style="width: 100%; height: 500px;"></div>
<script>
    const scene = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera(75, window.innerWidth / 500, 0.1, 1000);
    const renderer = new THREE.WebGLRenderer({ antialias: true });
    renderer.setSize(window.innerWidth, 500);
    document.getElementById('canvas-container').appendChild(renderer.domElement);

    const loader = new THREE.GLTFLoader();
    loader.load('https://realyuvi.github.io/mi-pagina-web/modelos/tumodelo.glb', (gltf) => {
        scene.add(gltf.scene);
    });

    camera.position.z = 5;
    function animate() {
        requestAnimationFrame(animate);
        renderer.render(scene, camera);
    }
    animate();
</script>
```

## ⚙️ Activar GitHub Pages

1. Ve a **Settings** del repositorio
2. Selecciona **Pages** en el menú lateral
3. En "Source", selecciona la rama `main`
4. Guarda los cambios

Tu sitio estará disponible en: `https://realyuvi.github.io/mi-pagina-web/`

---

## ⚖️ Licencia

© 2026 Realyuvi. **Todos los derechos reservados.**

❌ **Prohibido:**
- Reproducir, distribuir o usar sin autorización explícita
- Modificar, adaptar o crear obras derivadas
- Usar con fines comerciales

**Contacta conmigo para solicitar permisos de uso.**

---

✨ ¿Necesitas ayuda subiendo archivos o personalizando el código?
