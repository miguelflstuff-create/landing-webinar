# Landing Page — Clase Abierta Closer Digital

Landing page de registro para la clase gratuita en vivo de **Closers Digitales**, donde Luis Romero enseña cómo generar 3.000€/mes de forma remota como Closer Digital.

---

## Contexto del proyecto

**¿Para qué sirve esta landing?**
Capturar registros de personas interesadas en asistir a una clase gratuita en vivo donde se explica cómo trabajar como Closer Digital de forma remota.

**Evento:**
- Clase en vivo con Luis Romero
- Martes 28 de Abril · 19:00h (hora España)
- 100% online y gratuita

**Oferta posterior (backend):**
Al final de la clase se presenta la Academia de Closers Digitales (2.000€), que incluye formación completa y posicionamiento garantizado en proyectos reales.

**Tráfico:**
La página recibe tráfico principalmente de publicidad pagada (Meta Ads). Los UTMs se capturan automáticamente en el formulario.

**Público objetivo:**
Hombres de 20 a 40 años en España interesados en generar ingresos online con un trabajo real y remoto.

---

## Estructura del proyecto

```
closers-landing/
│
├── README.md                  ← Este archivo
│
├── index.html                 ← Versión completa en un solo archivo (referencia)
├── styles.css                 ← CSS global de la versión completa
│
└── ghl-sections/              ← ⭐ CARPETA PRINCIPAL — Secciones para GoHighLevel
    ├── 01-TOPBAR.html
    ├── 02-HERO.html
    ├── 03-NUMEROS.html
    ├── 04-PARA-QUIEN-ES.html
    ├── 05-QUE-VAS-A-APRENDER.html
    ├── 06-LUIS-ROMERO-foto.html
    ├── 07-LA-OPORTUNIDAD.html
    ├── 08-FORMULARIO.html
    └── 09-FOOTER.html
```

---

## Cómo usar en GoHighLevel

Cada archivo en `ghl-sections/` es una sección independiente. Se copian y pegan una a una en el builder de GoHighLevel.

### Orden de implementación

| # | Archivo | Descripción |
|---|---|---|
| 1 | `01-TOPBAR.html` | Barra roja de urgencia con fecha del evento |
| 2 | `02-HERO.html` | Headline principal + countdown + botón de registro |
| 3 | `03-NUMEROS.html` | Barra de social proof (+300 alumnos, 3 años, etc.) |
| 4 | `04-PARA-QUIEN-ES.html` | Bullets de identificación del cliente ideal |
| 5 | `05-QUE-VAS-A-APRENDER.html` | 6 tarjetas con el contenido de la clase |
| 6 | `06-LUIS-ROMERO-foto.html` | Bio de Luis Romero con foto y estadísticas |
| 7 | `07-LA-OPORTUNIDAD.html` | Preview de la academia (oferta backend) |
| 8 | `08-FORMULARIO.html` | Formulario de registro + captura de UTMs |
| 9 | `09-FOOTER.html` | Footer legal |

### Pasos en GHL
1. Abre el builder de tu página en GoHighLevel
2. Añade una nueva sección
3. Agrega un elemento **Custom HTML**
4. Abre el archivo correspondiente de `ghl-sections/`
5. Copia todo el contenido y pégalo en el bloque Custom HTML
6. Repite para cada sección en orden

---

## Cosas que personalizar antes de publicar

### 1. Foto de Luis Romero
Archivo: `06-LUIS-ROMERO-foto.html`

```
Busca esta línea:
src="AQUI-VA-LA-URL-DE-LA-FOTO"

Pasos:
1. Sube la foto de Luis en GHL → Media Library
2. Copia la URL que genera GHL
3. Pégala en el src
```

### 2. Formulario o Survey
Archivo: `08-FORMULARIO.html`

```
OPCIÓN A — Survey nativo de GHL (recomendada):
1. Crea tu Survey en GHL
2. Copia el código embed
3. Borra el bloque <form>...</form>
4. Pega el embed en su lugar

OPCIÓN B — Webhook:
Cambia: action="TU-WEBHOOK-GHL"
Por:    action="https://tu-url-de-webhook.com"
```

### 3. Fecha del countdown
Archivo: `02-HERO.html`

```javascript
// Busca esta línea en el script:
var target = new Date('2025-04-28T19:00:00+02:00');

// Si el evento cambia de fecha, actualiza aquí.
```

### 4. Links del footer
Archivo: `09-FOOTER.html`

```
Actualiza los href="#" con las URLs reales de:
- Política de privacidad
- Aviso legal
- Contacto
```

---

## Diseño

- **Estilo:** Dark mode profesional (navy oscuro + dorado)
- **CSS:** Cada sección tiene su propio `<style>` embebido — sin dependencias externas
- **Fuente:** System fonts (-apple-system, BlinkMacSystemFont, Segoe UI) — carga instantánea
- **Responsive:** Optimizado para móvil y escritorio
- **Velocidad:** Sin librerías externas, sin frameworks, CSS mínimo por sección

---

## Equipo

| Nombre | Rol |
|---|---|
| Luis Romero | Fundador / Instructor |
| Tu nombre aquí | Desarrollador web |

---

## Notas importantes

- Los UTMs de los ads (`utm_source`, `utm_medium`, `utm_campaign`, `utm_term`) se capturan automáticamente en el formulario — no tocar el script de UTMs.
- El countdown apunta a `2025-04-28T19:00:00+02:00` (hora de España en verano, CEST). Si el evento cambia, actualizar en `02-HERO.html`.
- La sección 7 (academia) **no menciona precio** — el precio se revela en la clase. Esto es intencional.
