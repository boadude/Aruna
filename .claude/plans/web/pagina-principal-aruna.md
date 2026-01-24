# Pagina Web ARUNA - Vinyasa Yoga

## Metadata
- **Feature**: Sitio web completo ARUNA
- **Fecha**: 2025-01-24
- **Prioridad**: Alta
- **Modulo**: Web principal

---

## Overview

### Que es esta feature?
Sitio web de una sola pagina (landing page) para ARUNA Vinyasa Yoga, un estudio de yoga orientado a mujeres. El sitio debe transmitir paz, calma y refugio desde el primer momento, funcionando como una extension digital de la experiencia que se vive en el estudio.

### Por que es necesaria?
ARUNA necesita presencia digital que refleje fielmente su esencia: un espacio de contencion donde las mujeres pueden desconectar de la rutina, respirar y volver a si mismas. No es una web comercial ni fitness - es una invitacion a encontrar bienestar.

### Quienes la usaran?
Mujeres que buscan un espacio para reconectarse consigo mismas, alejarse del estres cotidiano y mejorar su calidad de vida a traves del yoga.

---

## Vision y Sensacion

### Mensaje Central (sin decirlo explicitamente)
"Aqui puedes descansar, volver a ti y sentirte mejor."

### Sensaciones a Transmitir
- Paz y calma desde el primer segundo
- Refugio y contencion
- Libertad de juicio
- Presencia y suavidad
- Como entrar a una sala tranquila donde el cuerpo puede relajarse

### Lo que NO debe ser
- No comercial
- No fitness
- Sin ruido visual
- Sin abrumar con informacion

---

## Identidad Visual

### Logo
- Archivo: `logo.png` (raiz del proyecto)
- Estilo: Linea fina, flor elegante con texto "ARUNA - VINYASA YOGA"
- Debe estar visible y destacado

### Paleta de Colores
| Color | Hex | Uso sugerido |
|-------|-----|--------------|
| Gris calido | #c2bcb0 | Acentos, bordes sutiles |
| Beige oscuro | #ada59a | Textos secundarios |
| Beige claro | #dad2c5 | Fondos de secciones alternadas |
| Marron caramelo | #baa087 | Acentos, hover states |
| Beige medio | #d0c4af | Elementos decorativos |
| Crema/Blanco calido | #f2efe6 | Fondo principal |

### Tipografia (Recomendacion)
- **Titulos**: Fuente serif elegante y ligera (ej: Cormorant Garamond, Playfair Display Light)
- **Cuerpo**: Sans-serif limpia y legible (ej: Karla, Inter, Source Sans Pro)
- **Caracteristicas**: Espaciado generoso entre letras, pesos ligeros (300-400)

---

## Estructura de la Pagina

### 1. Header / Navegacion
**Que debe verse:**
- Logo de ARUNA visible y centrado o a la izquierda
- Menu minimalista con pocas opciones
- Fondo transparente o del color principal (#f2efe6)

**Opciones de menu sugeridas:**
- Inicio
- Clases
- Sobre ARUNA
- Contacto

**Comportamiento:**
- Menu fijo al hacer scroll (opcional, con transicion suave)
- En movil: menu hamburguesa elegante

### 2. Hero Section
**Que debe verse:**
- Texto principal breve y evocador
- Mucho espacio en blanco
- Posible frase: "Un espacio para volver a ti"

**Medio visual (elegir uno):**

| Opcion | Descripcion | Placeholder |
|--------|-------------|-------------|
| **VIDEO (recomendado)** | Video en loop, sin sonido, movimiento lento (mujer respirando, clase tranquila, luz natural) | `[VIDEO: hero-video.mp4]` |
| Imagen | Foto grande que transmita calma (mujer en postura de yoga, ambiente sereno) | `[IMAGEN: hero-image.jpg]` |

*Nota: El video aporta mas a la sensacion de calma y movimiento sutil. Referencia: omvocado.com usa videos con musica tenue.*

**Sensacion:**
- Ritmo lento, invita a quedarse
- No hay prisa, no hay presion
- Como la primera respiracion profunda al entrar al estudio

**Referencia visual:**
- Similar a drishti.cl: foto grande debajo del menu
- Similar a omvocado.com: overlay sutil, mensaje centrado, video de fondo

### 3. Seccion "Sobre ARUNA"

**Medio visual:**
| Tipo | Descripcion | Placeholder |
|------|-------------|-------------|
| Imagen | Foto del estudio o de una practica grupal, ambiente calido | `[IMAGEN: about-image.jpg]` |
**Que debe comunicar:**
- ARUNA es mas que clases, es un espacio de contencion
- Las mujeres se sienten escuchadas y libres de juicio
- Venir aqui mejora la calidad de vida
- Despues de una practica, sales mas liviana y conectada

**Formato:**
- Texto breve, parrafos cortos
- Posible imagen complementaria
- Mucho espacio alrededor del texto

### 4. Seccion "Clases" o "Practica"
**Que debe mostrar:**
- Tipos de clases disponibles (si aplica)
- Horarios (formato limpio, no tabla abrumadora)
- Mensaje de que cualquier dia es bueno para empezar, sin importar el animo

**Medio visual:**
| Tipo | Descripcion | Placeholder |
|------|-------------|-------------|
| Imagen | Detalle de practica, manos en mudra, mat de yoga, ambiente zen | `[IMAGEN: practice-image.jpg]` |

**Tono:**
- Bienvenida incondicional
- "Incluso en esos dias que cuesta, dan ganas de venir"

### 5. Seccion de Contacto / Ubicacion

**Estructura:**

```
[Titulo]
Ven a conocernos

[Texto]
Si sientes que este puede ser tu espacio, te esperamos.

[Boton Principal - WhatsApp]
"Escribenos" → Abre WhatsApp con mensaje predefinido

[Informacion Secundaria]
- Instagram: @aruna.vinyasayoga (con icono)
- Email: hola@arunayoga.cl (con icono)
- Direccion: Av. Alemania 1234, Valdivia (con icono)
```

**Boton WhatsApp:**
- Estilo elegante acorde a la paleta (no verde WhatsApp)
- Color: #baa087 (marron caramelo) o #ada59a
- Hover suave
- Abre: `https://wa.me/56912345678?text=Hola,%20me%20gustaría%20saber%20más%20sobre%20ARUNA`

**Iconos:**
- Minimalistas, linea fina
- Color sutil (#ada59a o similar)

**Nota:** No incluir mapa por ahora (agrega peso visual). La direccion es suficiente.

### 6. Footer
**Contenido:**
- Logo pequeno
- Links de navegacion
- Redes sociales (iconos sutiles)
- Copyright

---

## Animaciones y Transiciones

### Principios
- Todo debe sentirse lento y suave
- Transiciones de 0.3s a 0.5s
- Ease-out o ease-in-out
- Nada abrupto ni rapido

### Implementacion Tecnica

**Lenis (Smooth Scroll)**
- Scroll suave y fluido en toda la pagina
- Sensacion "sedosa" al navegar
- Configuracion con velocidad lenta para mantener la calma

**CSS + IntersectionObserver**
- **Fade-in al scroll**: Elementos aparecen suavemente al entrar en viewport
- **Parallax sutil**: Imagenes de fondo con movimiento leve usando CSS transforms
- **Hover suaves**: Cambios de color graduales en links y botones con `transition`
- **Texto revelado**: Frases que aparecen con delays escalonados

**Tailwind Utilities**
- `transition-all duration-500 ease-out` para transiciones
- `opacity-0` / `opacity-100` para fade effects
- `translate-y` para movimientos sutiles

### Futuro (a considerar)
- Pequenos videos con musica tenue (referencia: omvocado.com)
- Animaciones de respiracion sutiles

---

## Requerimientos Funcionales

### Performance
- La pagina debe cargar rapido
- Imagenes optimizadas (WebP, lazy loading)
- CSS y JS minimos necesarios
- Score alto en Lighthouse

### Responsive Design
- Funcionar perfectamente en movil, tablet y desktop
- Mantener la sensacion de calma en todos los dispositivos
- Menu adaptado para movil

### SEO y Metadata

**Meta tags basicos:**
- Titulo descriptivo
- Descripcion que refleje la esencia
- Keywords relevantes

**Open Graph (para compartir en Facebook, Instagram, WhatsApp):**
- og:title
- og:description
- og:image (imagen optimizada para preview)
- og:url
- og:type

**Otros:**
- Favicon (ya existe)
- Apple touch icon
- Canonical URL
- Idioma (es-CL)

### Accesibilidad
- Contraste adecuado
- Textos legibles
- Navegacion por teclado

---

## Flujo del Usuario

1. Usuario llega a la pagina
2. Ve el hero con imagen serena y mensaje evocador
3. Siente invitacion a quedarse, no presion
4. Hace scroll lento, descubriendo secciones
5. Lee sobre ARUNA y se siente identificada
6. Ve las clases disponibles
7. Encuentra como contactar o ubicar el estudio
8. Sale con sensacion de haber encontrado "su lugar"

---

## Criterios de Aceptacion

### Visuales
- [ ] Logo de ARUNA visible en header
- [ ] Paleta de colores aplicada correctamente
- [ ] Tipografia elegante y legible
- [ ] Mucho espacio en blanco entre secciones
- [ ] Imagenes que transmiten calma y serenidad

### Experiencia
- [ ] La pagina invita a quedarse y recorrer con calma
- [ ] No hay sensacion de prisa ni de venta agresiva
- [ ] Las transiciones son suaves y lentas
- [ ] El ritmo visual es pausado

### Tecnico
- [ ] Carga rapida (< 3 segundos)
- [ ] Funciona correctamente en movil
- [ ] Animaciones fluidas sin lag
- [ ] Responsive en todos los breakpoints

### Contenido
- [ ] Cada seccion tiene texto apropiado
- [ ] El mensaje central se transmite sin decirlo explicitamente
- [ ] Informacion de contacto visible

---

## Referencias Visuales

### omvocado.com (Referencia Principal)
Esta es la referencia principal para la estetica y sensacion de ARUNA:
- Videos con musica tenue en el hero
- Overlay sutil con mensaje centrado
- Sensacion de presencia, calma y equilibrio
- Mucho espacio en blanco
- Ritmo lento, invita a quedarse
- Paleta de colores calidos y neutros
- Tipografia elegante y espaciada
- Transmite bienestar, no comercio

### drishti.cl (Solo elementos puntuales)
De esta pagina solo tomamos como referencia:
- Estructura del menu (limpio, horizontal)
- Concepto de foto/video grande debajo del header

*Nota: drishti.cl tiene un enfoque mas comercial (venta de productos). La estetica y sensacion de ARUNA debe seguir mas a omvocado.com.*

---

## SEO y Metadata - Contenido

### Meta Tags

```
Titulo: ARUNA Vinyasa Yoga | Un espacio para volver a ti
Descripcion: ARUNA es un estudio de yoga en Valdivia donde las mujeres encuentran un refugio para reconectarse consigo mismas. Clases de Vinyasa Yoga en un ambiente de calma y contencion.
Keywords: yoga santiago, vinyasa yoga, yoga mujeres, estudio yoga providencia, clases yoga, bienestar, mindfulness
```

### Open Graph (Facebook, LinkedIn, WhatsApp)

```
og:title: ARUNA Vinyasa Yoga
og:description: Un espacio para volver a ti. Clases de Vinyasa Yoga en un ambiente de calma y contencion.
og:image: /og-image.jpg (1200x630px)
og:url: https://arunayoga.cl (dummy)
og:type: website
og:locale: es_CL
```

### Otros Meta Tags

```html
<html lang="es-CL">
<link rel="canonical" href="https://arunayoga.cl">
<meta name="robots" content="index, follow">
<meta name="author" content="ARUNA Vinyasa Yoga">
<meta name="theme-color" content="#f2efe6">
```

---

## Assets Multimedia Necesarios

### Resumen de archivos a preparar

| Seccion | Tipo | Archivo | Obligatorio |
|---------|------|---------|-------------|
| Hero | VIDEO | `hero-video.mp4` | Recomendado |
| Hero | Imagen | `hero-image.jpg` | Alternativa |
| About | Imagen | `about-image.jpg` | Si |
| Practice | Imagen | `practice-image.jpg` | Opcional |
| SEO | Imagen | `og-image.jpg` | Si |

### Sugerencias Creativas para cada Asset

**Hero - Video (`hero-video.mp4`)**
> Idea: Tamara en el estudio, de espaldas o perfil, haciendo una respiracion profunda con los ojos cerrados. Luz natural entrando por la ventana. Movimiento minimo, solo el subir y bajar del pecho al respirar. Sin rostro completo necesariamente, puede ser silueta. Transmite: "aqui hay calma, aqui puedes parar".

**Hero - Imagen alternativa (`hero-image.jpg`)**
> Idea: Vista del estudio vacio con luz de manana. Un mat desenrollado esperando. O Tamara sentada en postura de meditacion, vista desde atras, mirando hacia una ventana con luz suave. Transmite: "este espacio te esta esperando".

**About - Imagen (`about-image.jpg`)**
> Idea: Momento real de una clase grupal. Mujeres en diferentes posturas (no perfectas, reales). O Tamara ajustando suavemente a una alumna. Rostros relajados, sonrisas sutiles. Ambiente calido. Transmite: "aqui no hay juicio, todas son bienvenidas tal como son".

**Practice - Imagen (`practice-image.jpg`)**
> Idea: Detalle de manos en mudra sobre las rodillas. O pies descalzos sobre el mat. O una taza de te junto a bloques de yoga y una manta. Angulo cerrado, intimidad. Transmite: "los pequenos detalles importan, esto es autocuidado".

**OG Image - Redes sociales (`og-image.jpg`)**
> Idea: Logo de ARUNA centrado sobre fondo del color crema (#f2efe6). Opcionalmente con la frase "Un espacio para volver a ti" debajo en tipografia elegante. Minimalista. Debe verse bien en tamano pequeno (preview de WhatsApp). Transmite: "esto es algo especial, quiero saber mas".

### Especificaciones tecnicas

**Video Hero:**
- Formato: MP4 (H.264)
- Duracion: 10-15 segundos en loop
- Sin audio (se reproduce en mute)
- Resolucion: 1920x1080 minimo
- Contenido sugerido: mujer respirando, clase tranquila, luz natural entrando

**Imagenes:**
- Formato: JPG o WebP
- Resolucion: 1920px ancho minimo
- Estilo: luz natural, tonos calidos, ambiente sereno

**Imagen Open Graph (og-image.jpg):**
- Resolucion exacta: 1200x630px
- Debe verse bien como preview en WhatsApp, Facebook, LinkedIn
- Sugerencia: Logo de ARUNA + fondo calido o foto sutil del estudio
- Texto opcional: "Un espacio para volver a ti"

*Nota: Por ahora usare placeholders en el codigo. Cuando tengan los archivos, solo hay que reemplazarlos en la carpeta `public/`.*

---

## Fuera de Alcance (Primera Version)

- Sistema de reservas online
- Pasarela de pagos
- Blog o articulos
- Videos integrados (se puede agregar despues)
- Galeria de fotos extensa
- Testimonios (se puede agregar despues)
- Integraciones con redes sociales avanzadas

---

## Stack Tecnologico

- **Framework**: Astro 5.x
- **CSS**: Tailwind CSS 4.x
- **Smooth Scroll**: Lenis (~3KB)
- **Animaciones**: CSS puro + Tailwind (transiciones, keyframes, IntersectionObserver)
- **Estructura**: Single Page Application (landing)

### Arquitectura de Componentes

Cada seccion de la pagina sera un componente Astro independiente. Esto permite:
- Modificar una seccion sin afectar las demas
- Reutilizar componentes si se necesitan en otras paginas
- Codigo mas limpio y mantenible

**Estructura de archivos:**

```
src/
├── components/
│   ├── Header.astro         # Navegacion y logo
│   ├── Hero.astro           # Seccion principal con imagen y titulo
│   ├── About.astro          # Seccion "Sobre ARUNA"
│   ├── Practice.astro       # Seccion "La Practica" con horarios
│   ├── Contact.astro        # Seccion de contacto y ubicacion
│   └── Footer.astro         # Footer con links y copyright
├── layouts/
│   └── Layout.astro         # Layout base con meta tags, fonts, Lenis
├── pages/
│   └── index.astro          # Pagina principal que ensambla componentes
└── styles/
    └── global.css           # Estilos globales y variables de color
```

**Pagina principal (index.astro):**
```astro
---
import Layout from '../layouts/Layout.astro'
import Header from '../components/Header.astro'
import Hero from '../components/Hero.astro'
import About from '../components/About.astro'
import Practice from '../components/Practice.astro'
import Contact from '../components/Contact.astro'
import Footer from '../components/Footer.astro'
---

<Layout>
  <Header />
  <Hero />
  <About />
  <Practice />
  <Contact />
  <Footer />
</Layout>
```

Asi, si quieres redisenar el Hero, solo editas `src/components/Hero.astro`.

### Decision sobre Animaciones

Se opta por **CSS puro + Lenis** en lugar de librerias como Magic UI, Framer Motion o GSAP por las siguientes razones:

1. **Rendimiento**: Cero dependencias pesadas = carga rapida
2. **Estetica**: Las animaciones sutiles y lentas se logran perfectamente con CSS nativo
3. **Lenis**: Agrega smooth scroll premium que mejora la sensacion de fluidez y calma
4. **Mantenibilidad**: Menos codigo, menos complejidad
5. **Coherencia**: El minimalismo del codigo refleja el minimalismo del diseno

---

## Contenido de la Pagina

### Hero Section

**Titulo principal:**
> Un espacio para volver a ti

**Subtitulo (opcional):**
> Respira. Suelta. Reconectate.

---

### Seccion "Sobre ARUNA"

**Titulo:**
> Mas que clases, un refugio

**Texto:**
> ARUNA nacio como un espacio donde las mujeres pueden hacer una pausa en medio del ruido cotidiano. Aqui no hay expectativas, no hay juicios, no hay prisa.

> Sabemos que la vida a veces pesa. Que hay dias en que cuesta levantarse, en que el cuerpo esta cansado y la mente no para. Por eso creamos este lugar: para que puedas llegar tal como estas, respirar profundo y soltar.

> Cada clase es una invitacion a reconectarte contigo misma. A moverte con suavidad, a escuchar tu cuerpo y a recordar que mereces este momento de calma.

> Despues de practicar, algo cambia. Sales mas liviana, mas presente, con una sensacion de bienestar que se queda contigo. Y eso, con el tiempo, transforma tu vida.

---

### Seccion "La Practica"

**Titulo:**
> Vinyasa Yoga

**Texto:**
> Una practica fluida que conecta movimiento y respiracion. No necesitas experiencia previa ni flexibilidad. Solo necesitas llegar.

> En ARUNA adaptamos cada clase a quienes estan presentes. Hay espacio para todas: para la que viene por primera vez, para la que lleva anios practicando, para la que hoy solo necesita descansar.

**Horarios (dummy):**

| Dia | Horario |
|-----|---------|
| Lunes | 10:00 - 11:15 |
| Miercoles | 10:00 - 11:15 |
| Viernes | 10:00 - 11:15 |
| Sabado | 09:30 - 10:45 |

**Nota bajo horarios:**
> Los horarios pueden variar. Escribenos para confirmar disponibilidad.

---

### Seccion "Contacto"

**Titulo:**
> Ven a conocernos

**Texto:**
> Si sientes que este puede ser tu espacio, te esperamos.

**Boton WhatsApp:**
> Escribenos

**Datos (dummy):**
- **Instagram:** @aruna.vinyasayoga
- **Email:** hola@arunayoga.cl
- **Direccion:** Av. Alemania 1234, Valdivia
- **WhatsApp:** +56 9 1234 5678

*El boton abre WhatsApp con mensaje predefinido: "Hola, me gustaria saber mas sobre ARUNA"*

---

### Footer

**Texto breve:**
> ARUNA Vinyasa Yoga - Un espacio para volver a ti

**Copyright:**
> 2025 ARUNA. Todos los derechos reservados.

---

### Textos Alternativos para el Hero (opciones)

**Opcion 1:**
> Aqui puedes soltar, respirar y simplemente ser

**Opcion 2:**
> Tu momento de calma en medio del ruido

**Opcion 3:**
> Un lugar donde volver cuando el mundo pesa

---

## Notas Adicionales

La clave de esta pagina no esta solo en lo que muestra, sino en lo que NO muestra. El minimalismo extremo, el espacio en blanco generoso y el ritmo lento son fundamentales para transmitir la esencia de ARUNA.

Cada decision de diseno debe pasar por el filtro: "Esto ayuda a que alguien se sienta en calma, o lo distrae?"
