# ComPlan — Dashboard de Planes Comunicacionales

Dashboard web de una sola página (`index.html`) para gestionar planes comunicacionales organizados en **cuentas → campañas → acciones**. No requiere servidor, base de datos ni dependencias instaladas: funciona directo en el navegador.

---

## 🗂 Estructura de cuentas

| Cuenta | Descripción |
|---|---|
| **CEUSS** | Centro de Extensión USS |
| **VcM** | Vinculación con el Medio |
| **Investigación** | Difusión e Impacto Científico |
| **Centinela** | Velero Escuela |

---

## ✨ Funcionalidades

- **Navegación lateral** entre las 4 cuentas, con conteo de campañas y acciones.
- **Tarjetas de campaña** expandibles con barra de progreso automática (% de acciones completadas).
- **Tabla de acciones** por campaña con columnas: nombre, tipo, canal, estado, prioridad, responsable y fecha de vencimiento.
- **CRUD completo**: crear, editar y eliminar campañas y acciones mediante modales.
- **Indicador de vencimiento**: las acciones con fecha pasada se resaltan en rojo automáticamente.
- **Filtros y búsqueda** por estado de campaña y texto libre.
- **Exportar CSV** de la cuenta activa con todos los datos.
- **Persistencia local** con `localStorage`: los datos se conservan al cerrar el navegador.
- **Datos de demo** precargados para comenzar a explorar de inmediato.

---

## 🚀 Uso rápido

### Opción A — Abrir directo
```bash
# Descarga el archivo y ábrelo en tu navegador
open dashboard_comunicaciones.html
```

### Opción B — GitHub Pages (recomendado)
1. Sube el repositorio a GitHub.
2. Ve a **Settings → Pages**.
3. En *Source* selecciona la rama `main` y la carpeta `/ (root)`.
4. Renombra el archivo a `index.html` (ver abajo).
5. Accede a la URL que GitHub te asigna.

---

## 📁 Archivos del repositorio

```
/
├── index.html          ← renombrar dashboard_comunicaciones.html a este
└── README.md
```

> **Importante:** para que GitHub Pages sirva el archivo automáticamente debe llamarse `index.html`.

---

## 🛠 Personalización rápida

| Qué cambiar | Dónde en el código |
|---|---|
| Nombres o colores de cuentas | Objeto `ACCOUNTS` (~línea 210) |
| Tipos de acción disponibles | Array `TYPES` (~línea 230) |
| Canales disponibles | Array `CHANNELS` (~línea 231) |
| Datos de demo | Objeto `INITIAL_DATA` (~línea 237) |
| Colores globales (tema) | Variables CSS en `:root` (~línea 10) |

---

## 🔒 Persistencia de datos

Los datos se guardan en el `localStorage` del navegador bajo la clave `complan_v2`. Si necesitas limpiar y volver a los datos de demo, ejecuta en la consola del navegador:

```javascript
localStorage.removeItem('complan_v2'); location.reload();
```

---

## 📦 Tecnologías

- HTML5, CSS3 y JavaScript vanilla — sin frameworks ni dependencias.
- Fuentes Google Fonts: **DM Sans** y **Syne** (cargadas por CDN).
- Compatible con Chrome, Firefox, Edge y Safari modernos.

---

## 📄 Licencia

Uso interno. Puedes adaptar libremente para tus proyectos.
