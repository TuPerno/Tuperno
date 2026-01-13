# TuPerno - Landing Page Prototipo

Protitipo Landing page  para TuPerno, ferretería especializada en pernos y fijaciones ubicada en San Pedro de la Paz, Región del Biobío, Chile.

##  Inicio Rápido

```bash
# 1. Instalar dependencias
npm install

# 2. Iniciar servidor de desarrollo
npm run dev

# 3. Abrir en navegador: http://localhost:4321
```

## Descripción del Proyecto

Landing page moderna y optimizada para SEO, diseñada para generar conversiones y contacto directo con clientes a través de WhatsApp. Arquitectura componentizada con datos centralizados para fácil mantenimiento y modificación.

## Características Principales

-  **Hero Section** con título impactante y doble CTA (WhatsApp + Ubicación)
-  **Carousel automatizado** con 10 fotos reales de productos
- **3 Beneficios clave** con checkmarks y descripciones
-  **Marcas comercializadas** (Stanley, W-MAX)
- **Formulario de conversión** que redirige a WhatsApp
- **5 Testimonios reales** de clientes con calificaciones
-  **Sección de ubicación** con mapa de Google Maps integrado
-  **Métodos de pago POS TUU** con 4 opciones visualizadas
-  **Footer completo** con horarios, contacto y derechos
-  **100% Responsive** - optimizado para móvil, tablet y escritorio
-  **SEO optimizado** con meta tags y schema markup

## Tecnologías Utilizadas

- **[Astro 5.16.7](https://astro.build/)** - Framework web moderno
- **[Tailwind CSS v4](https://tailwindcss.com/)** - Framework de estilos con Vite
- **TypeScript** - Tipado estático
- **JavaScript Vanilla** - Para interactividad del carousel

## Estructura del Proyecto

```
tuperno-landing/
├── public/
│   ├── favicon.svg                    # Ícono de perno personalizado
│   ├── images/                        # Assets de branding y logos
│   │   ├── logo.png                   # Logo de TuPerno (40x40px recomendado)
│   │   ├── pernos.png                 # Imagen de fondo del hero
│   │   └── TuPernoLocal.png           # Foto del local físico
│   └── productos/                     # 10 fotos reales de productos
│       ├── Captura de pantalla 2026-01-07 125622.png
│       ├── Captura de pantalla 2026-01-07 125645.png
│       └── ... (8 imágenes más)
├── src/
│   ├── components/                    # Componentes reutilizables
│   │   ├── SocialBar.astro            # Barra superior con logo y redes
│   │   ├── Hero.astro                 # Sección hero con CTAs
│   │   ├── ProductCarousel.astro      # Carousel interactivo de productos
│   │   ├── Features.astro             # Beneficios (Stock, Atención, Precios)
│   │   ├── ContactForm.astro          # Formulario con integración WhatsApp
│   │   ├── Testimonials.astro         # Testimonios de clientes
│   │   └── CTAFooter.astro            # Footer con contacto y CTA final
│   ├── config/                        # Configuración centralizada
│   │   ├── constants.ts               # Contacto, horarios, colores
│   │   ├── products.ts                # Array de productos del carousel
│   │   └── testimonials.ts            # Array de testimonios de clientes
│   ├── layouts/
│   │   └── Layout.astro               # Layout principal con SEO
│   ├── pages/
│   │   └── index.astro                # Landing page (63 líneas)
│   └── styles/
│       └── global.css                 # Estilos globales con Tailwind v4
├── astro.config.mjs                   # Configuración de Astro + Tailwind
├── package.json
├── tsconfig.json
└── README.md
```

## Identidad Visual

### Colores Principales
- **Azul Principal**: `#1E3A8A` - Títulos y elementos principales
- **Naranja Acento**: `#F59E0B` - CTAs y elementos destacados
- **Gris**: `#64748B` - Textos secundarios

### Tipografía
- Fuente del sistema (optimizada para rendimiento)
- Títulos: Font-weight 700-900 (Bold/Black)
- Cuerpo: Font-weight 400-600

## Información de Contacto

- **WhatsApp**: +56 9 5199 7763
- **Dirección**: Av. Pedro Aguirre Cerda 1973, San Pedro de la Paz
- **Región**: Biobío, Chile

## Instalación y Uso

### Requisitos Previos
- Node.js 18+ instalado
- npm o pnpm

### Instalación

1. Clonar o tener el proyecto en tu máquina

2. Instalar dependencias:
```bash
npm install
```

### Comandos Disponibles

| Comando | Acción |
|---------|--------|
| `npm run dev` | Inicia servidor de desarrollo en `http://localhost:4321` (o siguiente puerto disponible) |
| `npm run build` | Genera build de producción en `./dist/` |
| `npm run preview` | Previsualiza el build de producción localmente |
| `npm run astro check` | Verifica errores en el proyecto |

### Desarrollo

1. Iniciar servidor de desarrollo:
```bash
npm run dev
```

2. Abrir navegador en `http://localhost:4321` (o el puerto indicado)

3. Los cambios se recargan automáticamente en caliente (Hot Module Replacement)

### Producción

1. Generar build optimizado:
```bash
npm run build
```

2. El sitio estático se genera en la carpeta `dist/`

3. Subir contenido de `dist/` a tu hosting (Netlify, Vercel, etc.)

##  Cómo Hacer Modificaciones

### Cambiar Información de Contacto

**Archivo**: `src/config/constants.ts`

```typescript
export const CONTACT_INFO = {
  phone: '+56951997763',           // Cambiar número de teléfono
  email: 'tupernorw90@gmail.com',  // Cambiar email
  address: 'Av. Pedro Aguirre Cerda 1973',  // Cambiar dirección
  city: 'San Pedro de la Paz',
  region: 'Región del Biobío',
  whatsappMessage: 'Hola! Me gustaría...',  // Cambiar mensaje por defecto
};

export const BUSINESS_HOURS = {
  weekdays: 'Lunes a Viernes: 9:00 - 19:00',  // Cambiar horarios
  saturday: 'Sábados: 9:00 - 14:00',
  sunday: 'Domingos: Cerrado',
};

export const SOCIAL_MEDIA = {
  facebook: 'https://facebook.com/tuperno',
  instagram: 'https://www.instagram.com/tuperno_90/',  // Cambiar URLs
  whatsapp: 'https://wa.me/56951997763',
  email: 'mailto:tupernorw90@gmail.com',
};
```

###  Cambiar Colores de la Marca

**Archivo**: `src/config/constants.ts`

```typescript
export const THEME_COLORS = {
  primary: '#1E3A8A',      // Azul principal (títulos, fondo)
  secondary: '#F59E0B',    // Naranja (CTAs, acentos)
  accent: '#3B82F6',       // Azul claro (hover, detalles)
};
```

### Cambiar Logo

1. Reemplazar el archivo en: `public/images/logo.png`
2. Tamaño recomendado: **200x50px** (proporción horizontal)
3. Formato: PNG con fondo transparente
4. Se ajusta automáticamente en el componente `SocialBar.astro`

###  Agregar/Quitar Fotos del Carousel

**Archivo**: `src/config/products.ts`

```typescript
export const products: Product[] = [
  {
    image: '/productos/tu-nueva-imagen.png',  // Agregar ruta
    alt: 'Descripción SEO del producto',       // Texto alternativo
  },
];
```

**Pasos**:
1. Agregar imagen en `public/productos/`
2. Añadir objeto al array en `products.ts`
3. El carousel se actualiza automáticamente

###  Modificar Testimonios

**Archivo**: `src/config/testimonials.ts`

```typescript
export const testimonials: Testimonial[] = [
  {
    name: 'Nombre del Cliente',
    initials: 'NC',              // Iniciales para avatar
    comment: 'El testimonio completo aquí...',
    rating: 5,                   // Calificación 1-5
    featured: true,              // true = destacado, false = grid
    color: '#3B82F6',           // Color del avatar
  },
  // Agregar más testimonios...
];
```

### Modificar Componentes Visuales

**Todos los componentes están en**: `src/components/`

#### SocialBar.astro
- Barra superior con logo y redes sociales
- **Modificar**: Logo, enlaces de redes, colores

#### Hero.astro
- Sección principal con título y CTAs
- **Modificar**: Título, descripción, textos de botones

#### ProductCarousel.astro
- Carousel automático de productos
- **Modificar**: Velocidad (línea 42: `setInterval(..., 4000)`)

#### Features.astro
- 3 beneficios principales
- **Modificar**: Textos, íconos SVG

#### ContactForm.astro  
- Formulario de contacto
- **Modificar**: Campos, validaciones, redirección WhatsApp

#### Testimonials.astro
- Muestra testimonios de clientes
- **Lee datos de**: `config/testimonials.ts`

#### CTAFooter.astro
- Footer con CTA, info de contacto, métodos de pago
- **Modificar**: Textos de CTA, métodos de pago

###  Cambiar SEO y Meta Tags

**Archivo**: `src/layouts/Layout.astro`

```astro
<title>Tu Nuevo Título SEO</title>
<meta name="description" content="Tu nueva descripción..." />
<meta property="og:title" content="Título para redes sociales" />
<meta property="og:description" content="Descripción para compartir" />
```

###  Cambiar Favicon

Reemplazar: `public/favicon.svg`
- Usar formato SVG para mejor resolución
- O reemplazar por PNG/ICO si prefieres

##  Componentes Principales

### SocialBar (`src/components/SocialBar.astro`)
- Barra superior con logo y enlaces a redes sociales
- **Editar**: Logo (`/images/logo.png`), enlaces sociales
- **Responsive**: Logo 40px desktop, 32px móvil

### Hero (`src/components/Hero.astro`)
- Sección principal con título grande y CTAs
- **Editar**: Título, descripción, textos de botones
- **Fondo**: Imagen `pernos.png` con opacidad

### ProductCarousel (`src/components/ProductCarousel.astro`)
- Carousel interactivo con navegación
- **Auto-avance**: Cada 4 segundos
- **Lee datos de**: `src/config/products.ts`
- **Features**: Touch/drag, flechas, dots, pausa al hover

### Features (`src/components/Features.astro`)
- 3 beneficios principales (Stock, Atención, Precios)
- **Editar**: Textos e íconos SVG inline
- **Layout**: Grid 1-3 columnas responsive

### ContactForm (`src/components/ContactForm.astro`)
- Formulario que redirige a WhatsApp
- **Campos**: Nombre, Email, Teléfono, Mensaje
- **Acción**: Construye mensaje personalizado para WhatsApp
- **Imagen**: `TuPernoLocal.png`

### Testimonials (`src/components/Testimonials.astro`)
- Muestra 1 testimonio destacado + 4 en grid
- **Lee datos de**: `src/config/testimonials.ts`
- **Features**: Avatares con iniciales, colores personalizados, ratings

### CTAFooter (`src/components/CTAFooter.astro`)
- CTA final + Información de contacto
- Tarjetas con: Ubicación, Teléfono, Email, Horarios
- **Métodos de pago**: Tarjetas, NFC, Transferencia, Efectivo
- **Footer**: Copyright, redes sociales
- **Botón scroll-to-top**: Aparece al bajar 300px

##  Archivos de Configuración

### `src/config/constants.ts`
Centraliza toda la información de contacto, horarios, redes sociales y colores de la marca.

**Contenido**:
- `CONTACT_INFO`: Teléfono, email, dirección, mensaje WhatsApp
- `BUSINESS_HOURS`: Horarios de atención
- `SOCIAL_MEDIA`: URLs de redes sociales
- `THEME_COLORS`: Colores principales del diseño

### `src/config/products.ts`
Array de productos para el carousel.

**Estructura**:
```typescript
interface Product {
  image: string;  // Ruta a la imagen
  alt: string;    // Texto alternativo SEO
}
```

### `src/config/testimonials.ts`
Array de testimonios de clientes.

**Estructura**:
```typescript
interface Testimonial {
  name: string;       // Nombre completo
  initials: string;   // Iniciales para avatar
  comment: string;    // Comentario del cliente
  rating: number;     // 1-5 estrellas
  featured: boolean;  // true = destacado
  color: string;      // Color del avatar (#hex)
}
```

##  Guía de Personalización Rápida

### Escenario 1: Cambiar toda la información de contacto
1. Abrir `src/config/constants.ts`
2. Modificar `CONTACT_INFO` con tus datos
3. Guardar → Los cambios se reflejan en toda la página automáticamente

### Escenario 2: Agregar nuevos productos
1. Colocar imágenes en `public/productos/`
2. Abrir `src/config/products.ts`
3. Agregar objetos al array: `{ image: '/productos/nuevo.png', alt: 'Descripción' }`
4. Guardar → El carousel se actualiza automáticamente

### Escenario 3: Cambiar colores de la marca
1. Abrir `src/config/constants.ts`
2. Modificar `THEME_COLORS`
3. Los colores se aplican globalmente en todos los componentes

### Escenario 4: Personalizar el Hero
1. Abrir `src/components/Hero.astro`
2. Editar líneas 5-10: Título y descripción
3. Editar líneas 12-20: Textos de los botones CTA

### Escenario 5: Modificar testimonios
1. Abrir `src/config/testimonials.ts`
2. Agregar/editar objetos en el array
3. Usar `featured: true` para destacar uno
4. Guardar → Se actualizan automáticamente

### Escenario 6: Cambiar redes sociales
1. Abrir `src/config/constants.ts`
2. Modificar URLs en `SOCIAL_MEDIA`
3. Para agregar/quitar redes: editar `src/components/SocialBar.astro`


**Última actualización**: Enero 2026 | Versión con arquitectura componentizada
