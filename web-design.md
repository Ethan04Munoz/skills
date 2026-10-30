# Front-End UI & Anti-AI Slop Directive (`SKILL.md`)

## Descripción y Propósito
Esta skill establece estándares de diseño de interfaz de nivel sénior para proyectos web. Su objetivo principal es erradicar patrones genéricos producidos por modelos de lenguaje ("AI Slop") y garantizar la creación de aplicaciones con personalidad de marca, jerarquía clara y arquitectura limpia.

---

## 1. Reglas Anti-AI Slop (Baneo de Clichés Visuales)

Al generar o refactorizar interfaces web, **queda estrictamente prohibido**:

* **Gradientes genéricos:** `from-purple-600 to-indigo-500` o degradados neón sobre fondos oscuros sin justificación de marca.
* **Tipografías por defecto:** `Inter`, `Roboto`, `Arial` o pilas del sistema no declaradas expresamente.
* **Estructura estandarizada en el Hero:** Encabezados centralizados con subtítulos idénticos y botones con sombras genéricas.
* **La "Regla de las 3 Tarjetas":** Secciones compuestas por tres tarjetas perfectamente cuadradas con iconos circulares idénticos en la parte superior.
* **Insignias flotantes (Badges/Pills):** Elementos tipo `v1.0.0 is live!` flotando sobre el título principal como adorno vacío.
* **Falsas ventanas de terminal:** Bloques oscuros imitando código en landing pages cuando no se trate de una herramienta para desarrolladores.

---

## 2. Comandos de la Skill (`UI.sh` Engine)

La IA interpretará las siguientes directivas cuando el usuario las convoque en el chat o en comentarios:

### `/design` — Dirección de Arte y Maquetado Expresivo
1. **Tipografía con carácter:** Exigir siempre un par tipográfico con contraste marcado.
   * *Editorial / Elegante:* Cormorant Garamond / Plus Jakarta Sans
   * *Tech / Táctico:* Space Grotesk / Satoshi
   * *Neobrutalista / Expresivo:* Syne / Outfit
2. **Composición espacial:** 
   * Romper la simetría horizontal y vertical.
   * Implementar rejillas asimétricas (`grid-cols-12` con tramos desproporcionados como `span-7` y `span-5`).
   * Usar variaciones drásticas de densidad: zonas de texto denso o listas técnicas intercaladas con espacios negativos amplios.
3. **Color y textura:**
   * Definir un color de acento dominante (terroso, saturado o monocromático alto) con contraste WCAG AAA.
   * Usar bordes definidos (`border-slate-800`), sombras proyectadas sin desenfoque (`shadow-[4px_4px_0px_0px_rgba(0,0,0,1)]`) o micro-texturas cuando aplique.

### `/ideas` — Prototipado Multitarea
Antes de generar el código final, presentar 3 enfoques visuales marcadamente distintos en la respuesta:
* **Opción A (Editorial Minimalista):** Enfocada en tipografía de gran escala, líneas finas y ritmo de lectura.
* **Opción B (Táctica / Densidad de Información):** Inspirada en tableros analíticos, bordes duros y alta concentración de datos.
* **Opción C (Brutalista / Neo-Digital):** Acentos cromáticos saturados, bloques asimétricos y micro-interacciones marcadas.

### `/componentize` — Arquitectura y Modularidad
1. Descomponer vistas monolíticas en componentes aislados con responsabilidades únicas.
2. Extraer valores duros (colores, espaciados, estados) a variables CSS o constantes del sistema de diseño.
3. Validar estados vacíos (*empty states*), estados de carga (*skeletons* con animaciones no genéricas) y estados de error antes de dar por terminado un componente.

### `/canonicalize` — Limpieza de Tailwind CSS
1. **Orden sintáctico:** Formatear las clases en el orden estándar:
   `Posicionamiento -> Display -> Layout (Flex/Grid) -> Spacing -> Sizing -> Typography -> Visuals (Color, Borders) -> Interactivity`.
2. **Eliminar redundancias:** Remover clases duplicadas o contradictorias (ejemplo: `flex flex-row`).
3. **Sustituir arbitrarios:** Convertir clases como `w-[324px]` a escalas designadas en el archivo de configuración `tailwind.config.js`.

---

## 3. Lista de Verificación Pre-Entrega (Quality Gate)

Antes de entregar cualquier fragmento de código frontend, la IA debe confirmar el cumplimiento de este checklist:

- [ ] ¿El diseño es reconocible como un sitio único sin parecer una plantilla predeterminada de Vercel/Tailwind?
- [ ] ¿Los contrastes de texto sobre fondo cumplen con la norma WCAG AA como mínimo?
- [ ] ¿La interfaz responde correctamente a layouts móviles sin romper la jerarquía tipográfica?
- [ ] ¿Se evitaron las sombras suavizadas excesivas (`shadow-2xl`) a favor de bordes estructurados o sombras sólidas?
- [ ] ¿Las transiciones duran entre `150ms` y `300ms` con curvas de aceleración naturales (`ease-out`)?