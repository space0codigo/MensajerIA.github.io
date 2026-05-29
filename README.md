# MensajeIA — Landing Page

Página web de presentación para un servicio de **automatización de mensajería con inteligencia artificial**. Construida en HTML/CSS/JS puro, sin dependencias externas ni frameworks.

---

## Vista previa

> Incluye modo claro y modo oscuro con toggle interactivo en la barra de navegación.

| Sección | Descripción |
|---|---|
| Hero | Titular principal, subtítulo y demo de chat animado |
| Estadísticas | Métricas clave del servicio |
| Funciones | 6 tarjetas de características |
| Canales | 8 plataformas compatibles |
| Cómo funciona | Flujo de 4 pasos |
| Precios | 3 planes (Starter, Pro, Empresa) |
| CTA final | Llamada a la acción de conversión |

---

## Estructura del archivo

```
index.html
│
├── <style>          # Estilos CSS completos con variables de tema
├── .page.light      # Variables de color para modo claro
├── .page.dark       # Variables de color para modo oscuro
│
├── <nav>            # Barra de navegación fija con toggle de tema
├── <section.hero>   # Hero con chat demo animado
├── .stats-row       # Fila de estadísticas
├── <section>        # Funciones (features grid)
├── .channels-section# Canales compatibles
├── <section>        # Cómo funciona (flow steps)
├── <section>        # Planes de precios
├── .cta-section     # Sección de conversión final
└── <footer>         # Footer con enlaces
```

---

## Tecnologías utilizadas

- **HTML5** — estructura semántica
- **CSS3** — variables CSS para temas, transiciones, grid y flexbox
- **JavaScript** — toggle de tema claro/oscuro (vanilla JS, sin librerías)
- **Google Fonts** — tipografías `Syne` (títulos) y `DM Sans` (cuerpo)
- **Tabler Icons** — iconografía via CDN (`https://cdn.jsdelivr.net/npm/@tabler/icons-webfont`)

---

## Instalación y uso

No requiere instalación ni servidor. Basta con abrir el archivo en cualquier navegador moderno.

```bash
# Clonar o descargar el archivo
git clone https://github.com/tu-usuario/mensajeia-landing.git

# Abrir directamente en el navegador
open index.html
```

O simplemente arrastra el archivo `index.html` a tu navegador.

---

## Personalización

### Cambiar nombre de marca

Busca y reemplaza `MensajeIA` en el HTML por el nombre de tu empresa.

### Cambiar colores principales

El color de acento principal es `#1D9E75` (verde). Para cambiarlo, reemplaza todas sus apariciones en el `<style>`:

```css
/* Color primario actual */
#1D9E75   /* acento principal */
#0F6E56   /* hover / más oscuro */
#5DCAA5   /* más claro */
#E1F5EE   /* fondo suave */
#04342C   /* fondo oscuro CTA */
```

### Cambiar precios

Edita los valores dentro de `.plan-price` en cada tarjeta de plan:

```html
<div class="plan-price">$79<span style="font-size:16px; font-weight:400">/mes</span></div>
```

### Agregar o quitar canales

En la sección `.channels-grid`, cada canal es un elemento:

```html
<div class="channel-pill">
  <span class="channel-dot" style="background:#25D366"></span>
  WhatsApp
</div>
```

### Cambiar el tema por defecto

El tema inicial se define en la clase del elemento raíz. Cambia `light` por `dark` para que inicie en modo oscuro:

```html
<!-- Modo claro por defecto (actual) -->
<div class="page light" id="page">

<!-- Modo oscuro por defecto -->
<div class="page dark" id="page">
```

---

## Funcionalidades

- **Toggle de tema** — Cambia entre modo claro y oscuro con transición suave de 0.3s
- **Diseño responsivo** — Grid con `auto-fit` y `minmax` que se adapta a distintos anchos
- **Animación de escritura** — Indicador de "escribiendo..." animado en el chat demo
- **Navbar fija** — Se mantiene visible al hacer scroll
- **Sin JavaScript externo** — El toggle funciona con menos de 10 líneas de JS nativo

---

## Despliegue

### GitHub Pages

```bash
git init
git add index.html
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/tu-usuario/mensajeia-landing.git
git push -u origin main
# Activar Pages en Settings > Pages > Branch: main
```

### Netlify (drag & drop)

1. Ir a [netlify.com](https://netlify.com)
2. Arrastrar el archivo `index.html` al área de deploy
3. La página queda publicada en segundos

### Vercel

```bash
npm i -g vercel
vercel deploy
```

---

## Próximas mejoras sugeridas

- [ ] Formulario de registro con validación
- [ ] Integración con backend para captura de leads (Formspree, Supabase, etc.)
- [ ] Sección de testimonios / casos de éxito
- [ ] Animaciones de entrada con `IntersectionObserver`
- [ ] Versión multiidioma (ES / EN)
- [ ] Meta tags SEO y Open Graph
- [ ] Google Analytics o Plausible

---

## Licencia

MIT — libre para uso personal y comercial.
