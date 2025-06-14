# 📋 Guía de Mejores Prácticas - HTML

## 🎯 HTML Semántico

### Estructura Básica Recomendada
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Descripción clara y concisa">
    <title>Título descriptivo - Marca</title>
    <link rel="stylesheet" href="assets/css/main.css">
</head>
<body>
    <header>
        <nav><!-- Navegación principal --></nav>
    </header>
    
    <main>
        <section><!-- Contenido principal --></section>
    </main>
    
    <aside><!-- Contenido secundario --></aside>
    
    <footer><!-- Información del sitio --></footer>
</body>
</html>
```

## ♿ Accesibilidad

### Elementos Esenciales
- **Alt text**: `<img src="foto.jpg" alt="Descripción clara">`
- **Labels**: `<label for="email">Email:</label><input id="email">`
- **Headings**: Orden jerárquico h1 → h2 → h3
- **Focus**: Navegación por teclado funcional
- **ARIA**: `aria-label`, `aria-describedby`, `role`

### Colores y Contraste
- Contraste mínimo 4.5:1 para texto normal
- Contraste mínimo 3:1 para texto grande
- No usar solo color para transmitir información

## 📱 Responsive Design

### Meta Viewport
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Imágenes Adaptables
```html
<img src="imagen.jpg" alt="Descripción" style="max-width: 100%; height: auto;">
```

### Media Queries Básicas
```css
/* Móviles */
@media (max-width: 768px) { }

/* Tablets */
@media (min-width: 769px) and (max-width: 1024px) { }

/* Desktop */
@media (min-width: 1025px) { }
```

## 🔍 SEO Básico

### Meta Tags Importantes
```html
<meta name="description" content="Descripción única de 150-160 caracteres">
<meta name="keywords" content="palabras, clave, relevantes">
<meta name="author" content="Tu Nombre">
<link rel="canonical" href="https://tu-sitio.com/pagina">
```

### Open Graph
```html
<meta property="og:title" content="Título de la página">
<meta property="og:description" content="Descripción para redes sociales">
<meta property="og:image" content="imagen-preview.jpg">
<meta property="og:url" content="https://tu-sitio.com">
```

## ⚡ Performance

### Optimización de Imágenes
- Usar formatos modernos: WebP, AVIF
- Tamaños apropiados para cada dispositivo
- Lazy loading: `<img loading="lazy">`

### CSS y JavaScript
- Minificar archivos en producción
- Combinar archivos CSS/JS similares
- Usar CDNs para librerías externas

### Preload Recursos Críticos
```html
<link rel="preload" href="font.woff2" as="font" crossorigin>
<link rel="preload" href="critical.css" as="style">
```

## 🛡️ Seguridad

### Formularios
```html
<!-- Validación HTML5 -->
<input type="email" required>
<input type="password" minlength="8" required>

<!-- Prevención CSRF -->
<input type="hidden" name="csrf_token" value="token_aqui">
```

### Enlaces Externos
```html
<a href="sitio-externo.com" target="_blank" rel="noopener noreferrer">
```

## 📝 Comentarios y Documentación

### HTML Bien Comentado
```html
<!-- Navegación principal -->
<nav class="navbar">
    <!-- Logo y marca -->
    <div class="navbar-brand">...</div>
    
    <!-- Menú de navegación -->
    <ul class="navbar-nav">...</ul>
</nav>

<!-- Contenido principal -->
<main>
    <!-- Sección hero -->
    <section class="hero">...</section>
</main>
```

## 🧪 Testing

### Herramientas Recomendadas
- **HTML Validator**: https://validator.w3.org/
- **Lighthouse**: Auditoria de performance y accesibilidad
- **Wave**: Test de accesibilidad web
- **Responsive Design Checker**: Varios tamaños de pantalla

### Checklist de Testing
- [ ] HTML válido (sin errores en validator)
- [ ] CSS válido
- [ ] Funciona sin JavaScript
- [ ] Accesible por teclado
- [ ] Responsive en móviles y tablets
- [ ] Carga rápida (< 3 segundos)
- [ ] Funciona en navegadores principales

## 🎨 CSS Moderno

### Variables CSS
```css
:root {
  --primary-color: #007bff;
  --font-size: 1rem;
  --spacing: 1rem;
}

.elemento {
  color: var(--primary-color);
  font-size: var(--font-size);
  margin: var(--spacing);
}
```

### Flexbox y Grid
```css
/* Layout con Flexbox */
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

/* Layout con Grid */
.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1rem;
}
```

## 📚 Recursos Adicionales

### Documentación Oficial
- [MDN Web Docs](https://developer.mozilla.org/)
- [W3C HTML5 Specification](https://www.w3.org/TR/html52/)
- [Web Content Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)

### Herramientas de Desarrollo
- **VS Code Extensions**: HTML CSS Support, Live Server, Auto Rename Tag
- **Chrome DevTools**: Inspector, Lighthouse, Network tab
- **Emmet**: Shortcuts para HTML/CSS rápido

---

💡 **Recuerda**: Estas son guías generales. Siempre adapta las prácticas según las necesidades específicas de tu proyecto.