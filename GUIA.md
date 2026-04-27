# TEENS CUP — GUÍA DE USO

Esta carpeta tiene todo lo necesario para que tu landing page funcione.
Leéla 5 minutos y vas a poder editar todo solo.

---

## ESTRUCTURA DE LA CARPETA

```
teenscup-web/
├── index.html          ← TU PÁGINA. Acá editás todo.
├── GUIA.md             ← Esto que estás leyendo.
├── media/              ← Tus videos van acá.
├── images/
│   └── galeria/        ← Tus fotos van acá.
└── sponsors/           ← Tus logos de sponsors van acá.
```

---

## PARTE 1 — EDITAR TEXTOS

### Cómo abrir el archivo para editar

**En Mac:**
1. Click derecho en `index.html` → Abrir con → TextEdit (NO Word)
2. Ojo: en TextEdit, andá a Format → "Make Plain Text" antes de editar.

**En Windows:**
1. Click derecho en `index.html` → Abrir con → Bloc de notas

**Mejor opción (gratis y mucho más cómodo):**
- Bajate **VS Code** desde code.visualstudio.com
- Abrí la carpeta entera con VS Code
- Editás el HTML con colores y todo se ve clarísimo

---

### Lo más importante: el bloque CONFIG

**Anda al final del archivo `index.html`** y buscá esto (Ctrl+F → `const CONFIG`):

```js
const CONFIG = {
  whatsapp: "5491100000000",
  ...
}
```

Ahí cambiás:

#### 1. Tu número de WhatsApp (OBLIGATORIO)
```js
whatsapp: "5491155556666",
```
- **Sin espacios, sin "+", sin guiones**
- Formato: 549 + tu número con código de área
- Ejemplo Argentina: `5491155556666` (Buenos Aires)

> ⚠️ Si no cambiás esto, los botones no funcionan. Es lo PRIMERO que tenés que hacer.

#### 2. Mensajes pre-armados de WhatsApp
```js
whatsappMessages: {
  default:   "Hola! Quiero más info sobre Teens Cup.",
  inscribir: "Hola! Quiero inscribir un equipo en Teens Cup. ¿Me pasan info?",
  info:      "Hola! Vi la web de Teens Cup y quiero más detalles.",
  mundial:   "Hola! Quiero participar del Mundial Teens Cup 2026."
}
```
Cambialos por como vos hablás.

#### 3. Email y redes
```js
email:     "hola@teenscup.com.ar",
instagram: "https://instagram.com/teenscup",
tiktok:    "https://tiktok.com/@teenscup",
```

#### 4. Stats (números que se muestran en la página)
```js
stats: {
  teams:    "+120",     ← cambiá por tu número real
  players:  "+2.400",
  matches:  "+300",
  editions: "5",
  teamsBig:    "120",   ← misma info pero sin "+"
  playersBig:  "2400",
  matchesBig:  "300",
  editionsBig: "5"
}
```

#### 5. Hero (los textos del título principal)
```js
hero: {
  kicker:   "Inscripciones abiertas · Edición 2026",
  location: "Buenos Aires · Argentina",
  line1:    "Tu colegio.",
  line2:    "Tu equipo.",
  line3:    "Tu mundial.",
  sub:      "El torneo de fútbol interescolar..."
}
```

---

### Editar otros textos (Experiencia, FAQ, Sponsors)

Esos están directamente en el HTML. Para editarlos:

1. Apretá Ctrl+F (Cmd+F en Mac) en el editor.
2. Buscá la frase que querés cambiar.
3. Cambiala. Guardá. Listo.

**Reglas básicas:**
- No borres los `<` ni `>` ni nada que parezca código.
- Solo cambiá el texto entre etiquetas. Por ejemplo:

  ANTES:
  ```html
  <h3 class="exp-card__title">Cancha pro</h3>
  ```

  DESPUÉS:
  ```html
  <h3 class="exp-card__title">Estadios profesionales</h3>
  ```

- Si tenés dudas, hacé una copia del archivo antes de editar.

---

## PARTE 2 — AGREGAR VIDEO AL HERO

1. Conseguí un video del torneo:
   - 10 a 30 segundos
   - MP4 (formato más usado)
   - Recomendado: máximo 8 MB
   - Sin audio (la página lo silencia igual)

2. Renombralo como **`hero.mp4`** (exactamente, en minúsculas).

3. Copialo dentro de la carpeta **`media/`** de tu sitio.

4. Refrescá la página. El video aparece automáticamente con un overlay oscuro
   para que el texto se siga leyendo bien.

> Si no tenés video, la página queda igual de linda con el fondo oscuro y la luz naranja.

**Para comprimir un video pesado:**
- handbrake.fr (gratis, descargás programa)
- veed.io (gratis online)
- compress-video-online.com

---

## PARTE 3 — AGREGAR FOTOS A LA GALERÍA

1. Elegí 6 buenas fotos del torneo (acción, festejos, equipos posando, etc).

2. Renombralas exactamente así:
   - `galeria-1.jpg` ← la mejor, va GRANDE
   - `galeria-2.jpg`
   - `galeria-3.jpg`
   - `galeria-4.jpg`
   - `galeria-5.jpg`
   - `galeria-6.jpg`

3. Copialas dentro de **`images/galeria/`**

4. Refrescá la página. Las fotos aparecen automáticamente.

**Si solo tenés 3 fotos:**
- Poné solo las que tengas (galeria-1, galeria-2, galeria-3)
- Las que faltan muestran un placeholder elegante (no rompe la página)

**Optimizá las fotos antes de subirlas:**
- 1200×900 px aproximadamente
- Comprimilas en tinypng.com (gratis, online) — bajan a 200-400 KB sin perder calidad
- Si las fotos pesan mucho, la página carga lento

---

## PARTE 4 — CAMBIAR EL TEXTO DE SPONSORS POR LOGOS

Por defecto, la sección de sponsors muestra texto. Para poner logos reales:

1. Conseguí los logos en **PNG con fondo transparente**, preferentemente blancos
   (porque la sección tiene fondo oscuro).

2. Copialos dentro de la carpeta **`sponsors/`** con nombres como:
   - `estudiantes.png`
   - `sponsor-2.png`
   - etc.

3. Abrí `index.html` y buscá: `<!-- SPONSORS -->` o `class="sponsor"`

4. Vas a ver 6 bloques así:
   ```html
   <div class="sponsor">Estudiantes<br>La Plata</div>
   ```

5. Reemplazá uno por uno por la versión con imagen:
   ```html
   <div class="sponsor">
     <img src="sponsors/estudiantes.png" alt="Estudiantes" style="max-height:60%; max-width:80%;">
   </div>
   ```

---

## PARTE 5 — CAMBIAR EL LOGO

El logo de Teens Cup ya viene embebido en el HTML (no tenés que hacer nada).

Si en el futuro querés cambiar el logo:
1. Andá a base64-image.de o similar
2. Subí tu logo PNG
3. Copiá el código que te da (empieza con `data:image/png;base64,...`)
4. En `index.html` buscá `const LOGO = "data:image/png;base64,`
5. Reemplazá el código entero por el nuevo

---

## PARTE 6 — PROBARLO ANTES DE PUBLICAR

Antes de subirlo, **mirá cómo se ve en tu compu**:

1. Doble click en `index.html` → se abre en tu navegador.
2. Mirá:
   - Que el WhatsApp abra el chat correcto al tocar los botones.
   - Que las fotos y video se vean.
   - Probá en celular: abrí desde WhatsApp Web o copiá el archivo al celu.

---

## PARTE 7 — SUBIRLO A NETLIFY (LO MÁS FÁCIL DEL MUNDO)

### Opción 1: Netlify Drop (sin cuenta, sin nada, en 30 segundos)

1. Andá a: **https://app.netlify.com/drop**
2. **Arrastrá la carpeta entera** `teenscup-web/` a la zona indicada.
3. Esperá 10 segundos. Te da una URL tipo `mistico-pavlov-12345.netlify.app`.
4. Esa URL es tu sitio LIVE. Compartila, mandala por WhatsApp, lo que quieras.

> ⚠️ Si subís SIN cuenta, el sitio dura 1 hora. Para que sea permanente,
> creá una cuenta gratis en netlify.com (3 segundos con Google) y "claim" el sitio.

### Opción 2: Desde tu cuenta Netlify (recomendado)

1. Creá cuenta gratis en **netlify.com** (entrás con Google, sin tarjeta).
2. Click en "Add new site" → "Deploy manually"
3. Arrastrá la carpeta `teenscup-web/`
4. Tu sitio ya está online y permanente.

### Conectar el dominio teenscup.com.ar

Una vez que tengas el sitio en Netlify:

1. En el panel de Netlify: **Domain settings** → **Add custom domain**
2. Escribí `teenscup.com.ar` → Verify.
3. Netlify te da dos opciones:

   **Opción A (más fácil): cambiar nameservers**
   - Netlify te da 4 direcciones (tipo `dns1.p01.nsone.net`)
   - Andá a donde compraste el dominio (NIC.ar, GoDaddy, etc.)
   - Cambiá los nameservers a los que te da Netlify
   - Esperá 24-48 horas (a veces es más rápido)

   **Opción B: agregar registros DNS**
   - En el panel de tu dominio, agregás un registro tipo "A" o "CNAME"
   - Netlify te dice exactamente qué valores poner

4. SSL/HTTPS se activa automático y gratis.

---

## PARTE 8 — ACTUALIZAR EL SITIO DESPUÉS

Cada vez que cambies algo (texto, fotos, video):

1. Editás los archivos en tu carpeta local.
2. Vas a Netlify → tu sitio → **Deploys**
3. Arrastrás la carpeta entera de nuevo a la zona "Drag and drop your site folder here"
4. Listo. El sitio se actualiza en 30 segundos.

---

## PROBLEMAS COMUNES

**"El WhatsApp no abre"**
→ No cambiaste el número en CONFIG. Andá al final del HTML y editá `whatsapp: "..."`.

**"La galería no muestra mis fotos"**
→ Revisá:
- Los archivos están en `images/galeria/` (no en otro lado).
- Se llaman exactamente `galeria-1.jpg`, `galeria-2.jpg`, etc.
- Son JPG (no JPEG, no PNG). Si tenés PNG, cambialos a JPG online en convertio.co.

**"El video no aparece"**
→ Revisá:
- Está en `media/` con nombre exacto `hero.mp4`.
- Es MP4 (no .mov, no .avi). Convertilo si hace falta.
- No pesa más de 15 MB (ideal: 5-8 MB).

**"Cambié algo y la página se rompió"**
→ Probablemente borraste un `<` o `>` por error. Si guardás todo lo que editás
   con la versión original a mano, podés volver. Por eso siempre hacé una copia
   de respaldo antes de editar.

---

## CHECKLIST FINAL ANTES DE PUBLICAR

- [ ] Cambié el número de WhatsApp en CONFIG
- [ ] Cambié los stats por mis números reales
- [ ] Edité los textos del FAQ con info actualizada
- [ ] Subí al menos 3 fotos a `images/galeria/`
- [ ] Subí el video del hero a `media/hero.mp4` (opcional pero recomendado)
- [ ] Cambié los textos de sponsors o agregué los logos reales
- [ ] Probé el sitio en mi compu (doble click en index.html)
- [ ] Probé que el WhatsApp abra bien desde celular
- [ ] Listo para subir a Netlify

---

Cualquier duda, escribime.
