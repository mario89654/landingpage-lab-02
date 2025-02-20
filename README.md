
# Media Queries Implementadas en el Proyecto

## Breakpoints Definidos

### 1. **Pantallas de hasta 1024px de ancho**

**Regla:** `@media (max-width: 1024px)`

- Se aplica cuando el ancho de la pantalla es **igual o menor a 1024px**.

- **Ajustes realizados:**
  - La galería de imágenes (`.knife-gallery li`) cambia a **2 columnas** en lugar de 3.

```css
@media (max-width: 1024px) {
  .knife-gallery li {
    flex: 1 1 calc(50% - 20px); /* 2 columnas en pantallas medianas */
  }
}
```

---

### 2. **Pantallas de hasta 768px de ancho**

**Regla:** `@media (max-width: 768px)`

- Se aplica cuando el ancho de la pantalla es **igual o menor a 768px**.
- **Ajustes realizados:**
  - El menú de navegación (`nav`) cambia a un diseño en **columna**.
  - Los elementos del menú (`.menu`) se centran y tienen un espaciado superior.
  - La galería de imágenes (`.knife-gallery`) se muestra en **una sola columna**.

```css
@media (max-width: 768px) {
  nav {
    flex-direction: column;
    text-align: center;
  }
  .menu {
    justify-content: center;
    padding-top: 10px;
  }
  .knife-gallery {
    flex-direction: column;
    align-items: center;
  }
  .knife-gallery li {
    flex: 1 1 100%; /* 1 columna en pantallas pequeñas */
  }
}
```

---

 **Conclusión:** Estas media queries mejoran la experiencia de usuario en tablets y móviles, garantizando que el diseño se adapte correctamente a diferentes dispositivos.
