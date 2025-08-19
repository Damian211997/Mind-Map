# 🧠 Mind-Map Visualizer

> **Template Interactivo para Visualización de Mapas Mentales** - Código libre y personalizable para proyectos

[![GitHub](https://img.shields.io/badge/GitHub-Damian211997%2FMind--Map-blue?style=flat-square&logo=github)](https://github.com/Damian211997/Mind-Map)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-✓-orange?style=flat-square&logo=html5)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-✓-blue?style=flat-square&logo=css3)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-✓-yellow?style=flat-square&logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

## 📋 Descripción

**Mind-Map Visualizer** es un template HTML interactivo y completamente funcional para crear y visualizar mapas mentales de manera dinámica. Diseñado con un enfoque modular y personalizable, permite organizar ideas, conceptos y proyectos de forma visual e intuitiva.

### ✨ Características Principales

- 🎯 **Interfaz Intuitiva**: Diseño moderno con gradientes y animaciones suaves
- 🖱️ **Drag & Drop**: Arrastra y suelta ramas completas para reorganizar
- 📱 **Responsive**: Adaptable a dispositivos móviles y tablets
- 🎨 **Personalizable**: Fácil modificación de colores, estilos y contenido
- ⌨️ **Navegación por Teclado**: Controles rápidos con atajos de teclado
- 🔄 **Controles Interactivos**: Botones para expandir, colapsar y resetear
- 📊 **Estructura Jerárquica**: 4 niveles de organización (Principal → Rama → Subcategoría → Detalle)

## 🚀 Instalación y Uso

### Requisitos
- Navegador web moderno (Chrome, Firefox, Safari, Edge)
- No requiere instalación de dependencias

### Instalación Rápida
```bash
# Clonar el repositorio
git clone https://github.com/Damian211997/Mind-Map.git

# Navegar al directorio
cd Mind-Map

# Abrir el template en tu navegador
open docs/mindmap-template.html
```

### Uso Directo
1. Descarga el archivo `docs/mindmap-template.html`
2. Ábrelo en cualquier navegador web
3. ¡Listo para usar!

## 🎮 Funcionalidades

### Controles de Interfaz

| Función | Botón | Atajo de Teclado | Descripción |
|---------|-------|------------------|-------------|
| **Expandir Todo** | `Expandir Todo` | `Enter` | Muestra todos los detalles |
| **Colapsar Todo** | `Colapsar Todo` | `Escape` | Oculta todos los detalles |
| **Resetear Posiciones** | `Resetear Posiciones` | - | Restaura posiciones originales |
| **Resetear Vista** | `Resetear Vista` | `Espacio` | Resetea todo y va al inicio |

### Interacciones del Usuario

#### 🖱️ Mouse
- **Click en Subcategorías**: Expande/colapsa detalles
- **Click en Ramas Principales**: Expande/colapsa todas las subcategorías
- **Arrastrar Ramas**: Mueve ramas completas por el canvas
- **Hover**: Auto-expansión después de 500ms

#### ⌨️ Teclado
- `Enter`: Expandir todas las subcategorías
- `Escape`: Colapsar todas las subcategorías  
- `Espacio`: Resetear vista completa

## 🏗️ Estructura del Template

### Niveles de Organización

```
📋 Nodo Principal (Centro)
├── 🎯 Rama Principal 1
│   ├── Subcategoría 1.1
│   │   ├── Detalle 1.1.1
│   │   └── Detalle 1.1.2
│   └── Subcategoría 1.2
│       ├── Detalle 1.2.1
│       ├── Detalle 1.2.2
│       └── Detalle 1.2.3
├── 🔍 Rama Principal 2
│   ├── Subcategoría 2.1
│   └── Subcategoría 2.2
└── ... (hasta 10 ramas principales)
```

### Clases CSS Principales

| Clase | Función | Estilo |
|-------|---------|--------|
| `.root-node` | Nodo central principal | Gradiente azul oscuro |
| `.main-node` | Ramas principales | Gradiente azul |
| `.sub-node` | Subcategorías | Fondo blanco con borde azul |
| `.detail-node` | Detalles específicos | Fondo gris claro |

## 🎨 Personalización

### Modificar Colores
```css
/* Cambiar color del nodo principal */
.root-node {
    background: linear-gradient(135deg, #tu-color-1 0%, #tu-color-2 100%);
}

/* Cambiar color de las ramas principales */
.main-node {
    background: linear-gradient(135deg, #tu-color-1 0%, #tu-color-2 100%);
}
```

### Agregar Nuevas Ramas
```html
<!-- Nueva Rama -->
<div class="branch" id="branch11" style="top: 20%; left: 15%;">
    <div class="main-node">🆕 Nueva Rama</div>
    <div class="sub-nodes">
        <div class="sub-node" onclick="toggleDetails(this)">
            Nueva Subcategoría
            <div class="detail-nodes">
                <div class="detail-node">Nuevo Detalle</div>
            </div>
        </div>
    </div>
</div>
```

### Modificar Posiciones
```javascript
// En el objeto initialPositions
const initialPositions = {
    // ... posiciones existentes
    branch11: { top: '20%', left: '15%' }
};
```

## 📱 Responsive Design

El template se adapta automáticamente a diferentes tamaños de pantalla:

- **Desktop**: Vista completa con controles en esquinas
- **Tablet**: Ajustes de tamaño y espaciado
- **Mobile**: Controles reorganizados, texto más pequeño

### Breakpoints
```css
@media (max-width: 768px) {
    /* Estilos para dispositivos móviles */
}
```

## 🔧 Tecnologías Utilizadas

- **HTML5**: Estructura semántica y accesible
- **CSS3**: 
  - Flexbox para layouts
  - Gradientes y sombras
  - Animaciones y transiciones
  - Media queries para responsive
- **JavaScript Vanilla**:
  - Drag & Drop personalizado
  - Event listeners
  - Manipulación del DOM
  - Navegación por teclado

## 📁 Estructura del Proyecto

```
Mind-Map/
├── docs/
│   └── mindmap-template.html    # Template principal
├── README.md                    # Este archivo
└── LICENSE                      # Licencia del proyecto
```

## 🎯 Casos de Uso

### Ideal para:
- 📚 **Planificación de Proyectos**: Organizar tareas y objetivos
- 🧠 **Lluvia de Ideas**: Visualizar conceptos relacionados
- 📊 **Análisis de Datos**: Estructurar información compleja
- 🎓 **Educación**: Crear mapas conceptuales
- 💼 **Presentaciones**: Mostrar jerarquías de información
- 🔍 **Investigación**: Organizar hallazgos y conclusiones

## 🚀 Próximas Características

- [ ] **Exportación**: Guardar como imagen o PDF
- [ ] **Temas**: Múltiples esquemas de colores
- [ ] **Zoom**: Funcionalidad de zoom in/out
- [ ] **Colaboración**: Edición en tiempo real
- [ ] **Persistencia**: Guardar cambios en localStorage
- [ ] **Animaciones**: Transiciones más elaboradas

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Para contribuir:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

### Guías de Contribución
- Mantén el código limpio y bien documentado
- Sigue las convenciones de nomenclatura existentes
- Prueba en múltiples navegadores
- Asegúrate de que sea responsive

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 👨‍💻 Autor

**Damian211997**
- GitHub: [@Damian211997](https://github.com/Damian211997)
- Repositorio: [Mind-Map](https://github.com/Damian211997/Mind-Map)

## 🙏 Agradecimientos

- Inspirado en técnicas de mapas mentales de Tony Buzan
- Diseño inspirado en herramientas modernas de visualización
- Comunidad de desarrolladores web por las mejores prácticas

## 📞 Soporte

Si tienes preguntas o necesitas ayuda:

- 📧 Abre un [Issue](https://github.com/Damian211997/Mind-Map/issues)
- 💬 Discute en [Discussions](https://github.com/Damian211997/Mind-Map/discussions)
- 📖 Revisa la documentación en este README

---

<div align="center">

⭐ **Si este proyecto te es útil, ¡dale una estrella!** ⭐

</div>
