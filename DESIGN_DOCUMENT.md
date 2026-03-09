# CloudsHorizon - Complete Redesign Document

## Project Overview
Redesign of cloudshorizon.com from WordPress to Next.js 14 + React
Client: CloudsHorizon Consulting (IT Cloud Consulting Firm, Google Cloud Partners)
Design inspiration: sada.com + missioncloud.com
Languages: English / Spanish (toggle)

---

## TECH STACK
- Next.js 14 (App Router, SSG)
- TypeScript
- Tailwind CSS
- Framer Motion (scroll animations)
- React Hook Form (contact form)
- next-intl or custom i18n (EN/ES)

---

## COLOR PALETTE
| Role            | Hex       | Usage                              |
|-----------------|-----------|-------------------------------------|
| Primary Navy    | #0F172A   | Nav, hero bg, dark sections         |
| Primary Blue    | #2563EB   | CTAs, links, active states          |
| Accent Teal     | #06B6D4   | Secondary accent, AWS section       |
| Accent Orange   | #F59E0B   | GCP section accent, highlights      |
| Light BG        | #F8FAFC   | Light section backgrounds           |
| White           | #FFFFFF   | Cards, content areas                |
| Dark Text       | #1E293B   | Headings                            |
| Body Text       | #64748B   | Paragraphs, descriptions            |
| Success Green   | #10B981   | Metrics, positive indicators        |
| Border          | #E2E8F0   | Card borders, dividers              |

## TYPOGRAPHY
- Headings: Inter (800 weight) - clean, modern, enterprise
- Body: Inter (400/500 weight)
- Sizes: H1=4rem, H2=2.5rem, H3=1.5rem, Body=1rem, Small=0.875rem

---

## NAVIGATION (Sticky Header)
### Desktop:
```
[Logo: Clouds Horizon Consulting]  Home | Services v | Google Cloud | AWS | About | Partners | Contact  [EN/ES toggle] [Get a Quote - button]
```

### Services Dropdown (mega-menu style like Mission Cloud):
- Cloud Migration
- Cloud Infrastructure
- DevOps & CI/CD
- Cybersecurity
- AI & Machine Learning
- Managed Services

### Mobile:
- Hamburger menu
- Full-screen slide-in overlay
- Language toggle at top
- CTA button at bottom

---

## SECTION 1: HERO
### Layout: Full viewport height, dark gradient background with subtle particle/grid animation
### Design: Inspired by Mission Cloud hero - bold headline, supporting text, dual CTAs, partner badges

**Background:** Dark navy (#0F172A) to deep blue (#1E3A5F) gradient with subtle animated grid pattern (CSS-only, no heavy libraries)

**Content (EN):**
```
Headline: "Your Cloud. Our Expertise."
Subheadline: "We help businesses migrate, optimize, and scale on Google Cloud and AWS. As certified cloud partners, we deliver enterprise-grade solutions with security at the core."
CTA 1: "Get a Free Consultation" (primary blue button)
CTA 2: "Explore Our Services" (outline/ghost button)
```

**Content (ES):**
```
Headline: "Tu Nube. Nuestra Experiencia."
Subheadline: "Ayudamos a las empresas a migrar, optimizar y escalar en Google Cloud y AWS. Como socios certificados en la nube, ofrecemos soluciones empresariales con la seguridad como prioridad."
CTA 1: "Obtener Consulta Gratuita"
CTA 2: "Explorar Nuestros Servicios"
```

**Partner badges below CTAs:**
- Google Cloud Partner badge
- AWS Partner badge
(Side by side, smaller size, white/light variants)

**Visual:** Subtle floating cloud/network node animation in background (CSS keyframes)

### Image/Asset Requirements:
- No hero image needed - using gradient + CSS animation pattern
- Google Cloud Partner logo (SVG) - source from: https://seeklogo.com/vector-logo/513594/google-cloud-partner
- AWS Partner logo (SVG) - source from: https://seeklogo.com/vector-logo/483148/aws-partner
- Client logo PNG already in /logo folder

---

## SECTION 2: TRUST BAR (Social Proof Strip)
### Layout: Light gray (#F8FAFC) horizontal strip, auto-scrolling logo carousel

**Content (EN):**
```
Label: "Trusted by innovative companies worldwide"
```
**Content (ES):**
```
Label: "Empresas innovadoras confian en nosotros"
```

**Logos:** Google Cloud + AWS logos + placeholder client logos (will use generic company icon placeholders until real clients are provided)

**Credibility Metrics (4 cards in a row):**
| Metric | EN | ES |
|--------|----|----|
| Icon: Shield | "Google Cloud Partner" | "Socio de Google Cloud" |
| Icon: Award | "AWS Certified" | "Certificado AWS" |
| Icon: Users | "50+ Projects Delivered" | "50+ Proyectos Entregados" |
| Icon: Clock | "24/7 Support" | "Soporte 24/7" |

---

## SECTION 3: SERVICES (Tabbed Layout - Mission Cloud style)
### Layout: White background, left-side vertical tabs (desktop) / horizontal scroll tabs (mobile)
### Each tab shows: Title + Description + Icon + CTA button

**Section Header (EN):** "What We Do" / "Our Services"
**Section Header (ES):** "Que Hacemos" / "Nuestros Servicios"
**Subheader (EN):** "End-to-end cloud solutions tailored to your business"
**Subheader (ES):** "Soluciones cloud de principio a fin adaptadas a tu negocio"

### Tabs:

**Tab 1: Cloud Migration**
- EN: "Seamlessly migrate your workloads to Google Cloud or AWS with zero downtime. We handle assessment, planning, execution, and validation to ensure a smooth transition."
- ES: "Migre sus cargas de trabajo a Google Cloud o AWS sin tiempo de inactividad. Gestionamos la evaluacion, planificacion, ejecucion y validacion para garantizar una transicion fluida."
- Icon: Cloud with arrow (upload icon)
- Image: Server room / migration visual
- CTA: "Start Your Migration" / "Inicie Su Migracion"

**Tab 2: Cloud Infrastructure**
- EN: "Design and deploy scalable, resilient cloud infrastructure. From virtual machines to Kubernetes clusters, we architect solutions that grow with your business."
- ES: "Disene e implemente infraestructura cloud escalable y resiliente. Desde maquinas virtuales hasta clusters de Kubernetes, diseamos soluciones que crecen con su negocio."
- Icon: Server stack
- Image: Infrastructure diagram / network visual
- CTA: "Build Your Infrastructure" / "Construya Su Infraestructura"

**Tab 3: DevOps & CI/CD**
- EN: "Accelerate your development lifecycle with automated pipelines, containerization, and infrastructure as code. Ship faster, break less."
- ES: "Acelere su ciclo de desarrollo con pipelines automatizados, contenedores e infraestructura como codigo. Despliegue mas rapido, con menos errores."
- Icon: Infinity loop / pipeline
- Image: Code/terminal visual
- CTA: "Automate Your Pipeline" / "Automatice Su Pipeline"

**Tab 4: Cybersecurity**
- EN: "Protect your digital assets with comprehensive security solutions. From threat detection to compliance, we keep your cloud environment secure."
- ES: "Proteja sus activos digitales con soluciones de seguridad integrales. Desde la deteccion de amenazas hasta el cumplimiento normativo, mantenemos su entorno cloud seguro."
- Icon: Shield with lock
- Image: Security/lock visual
- CTA: "Secure Your Cloud" / "Asegure Su Nube"

**Tab 5: AI & Machine Learning**
- EN: "Leverage the power of AI and machine learning on Google Cloud and AWS. From data analytics to predictive models, we turn your data into insights."
- ES: "Aproveche el poder de la IA y el aprendizaje automatico en Google Cloud y AWS. Desde analisis de datos hasta modelos predictivos, transformamos sus datos en conocimiento."
- Icon: Brain/chip
- Image: AI/data visualization
- CTA: "Explore AI Solutions" / "Explore Soluciones de IA"

**Tab 6: Managed Services**
- EN: "Let us manage your cloud environment so you can focus on your business. 24/7 monitoring, optimization, and support."
- ES: "Permita que gestionemos su entorno cloud para que usted se enfoque en su negocio. Monitoreo, optimizacion y soporte 24/7."
- Icon: Gear/wrench
- Image: Dashboard/monitoring visual
- CTA: "Get Managed Support" / "Obtenga Soporte Administrado"

### Image Requirements for Services:
Use Unsplash/Pexels free images:
- Cloud Migration: https://unsplash.com/s/photos/cloud-computing (server with cables)
- Infrastructure: https://unsplash.com/s/photos/server-room (server racks with blue LED lights)
- DevOps: https://unsplash.com/s/photos/programming (code on screen)
- Cybersecurity: https://unsplash.com/s/photos/cybersecurity (lock/shield visual)
- AI/ML: https://unsplash.com/s/photos/artificial-intelligence (abstract AI visual)
- Managed Services: https://unsplash.com/s/photos/monitoring-dashboard (dashboard screen)

**ALTERNATIVE:** Use Lucide React icons (included with Next.js) instead of photos for a cleaner, SADA-like approach. Each service gets a large icon + text. This is simpler and avoids image licensing concerns entirely.

---

## SECTION 4: GOOGLE CLOUD SECTION
### Layout: White background, 2-column (text left, visual right)
### Design: Feature the GCP Partner badge prominently

**Content (EN):**
```
Badge: "Google Cloud Partner"
Headline: "Google Cloud Solutions"
Description: "As a Google Cloud Partner, we bring certified expertise to every project. From Compute Engine to BigQuery, we help you leverage the full power of Google's cloud platform."

Services grid (3x2):
- Compute Engine: "Scalable virtual machines for any workload"
- Google Kubernetes Engine: "Managed Kubernetes for containerized apps"
- BigQuery: "Serverless data warehouse for analytics"
- Cloud Run: "Fully managed serverless platform"
- Cloud Storage: "Secure and durable object storage"
- Cloud AI Platform: "ML tools and pre-trained models"

CTA: "Explore Google Cloud Services"
```

**Content (ES):**
```
Badge: "Socio de Google Cloud"
Headline: "Soluciones de Google Cloud"
Description: "Como Socio de Google Cloud, aportamos experiencia certificada a cada proyecto. Desde Compute Engine hasta BigQuery, le ayudamos a aprovechar todo el poder de la plataforma cloud de Google."

Services grid (3x2):
- Compute Engine: "Maquinas virtuales escalables para cualquier carga"
- Google Kubernetes Engine: "Kubernetes administrado para apps en contenedores"
- BigQuery: "Data warehouse serverless para analitica"
- Cloud Run: "Plataforma serverless completamente administrada"
- Cloud Storage: "Almacenamiento de objetos seguro y duradero"
- Cloud AI Platform: "Herramientas de ML y modelos pre-entrenados"

CTA: "Explorar Servicios de Google Cloud"
```

### Visual: Google Cloud logo (official) + subtle GCP color accents (blue, red, yellow, green)
### Image: Abstract cloud network illustration or GCP architecture diagram style
- Source: Use CSS-drawn GCP service icons (Lucide icons) + Google Cloud logo SVG

---

## SECTION 5: AWS SECTION
### Layout: Dark background (#0F172A), 2-column (visual left, text right) - inverted from GCP section
### Design: AWS orange accent color

**Content (EN):**
```
Badge: "AWS Partner"
Headline: "Amazon Web Services Solutions"
Description: "We deliver comprehensive AWS solutions to power your digital transformation. From compute to AI, we architect and manage your AWS environment for peak performance."

Services grid (3x2):
- Amazon EC2: "Secure, resizable compute capacity"
- AWS Lambda: "Run code without thinking about servers"
- Amazon S3: "Scalable storage in the cloud"
- Amazon RDS: "Managed relational database service"
- Amazon EKS: "Managed Kubernetes on AWS"
- Amazon SageMaker: "Build, train, and deploy ML models"

CTA: "Explore AWS Services"
```

**Content (ES):**
```
Badge: "Socio de AWS"
Headline: "Soluciones de Amazon Web Services"
Description: "Ofrecemos soluciones integrales de AWS para impulsar su transformacion digital. Desde computo hasta IA, diseamos y administramos su entorno AWS para el maximo rendimiento."

Services grid (3x2):
- Amazon EC2: "Capacidad de computo segura y escalable"
- AWS Lambda: "Ejecute codigo sin preocuparse por servidores"
- Amazon S3: "Almacenamiento escalable en la nube"
- Amazon RDS: "Servicio de base de datos relacional administrado"
- Amazon EKS: "Kubernetes administrado en AWS"
- Amazon SageMaker: "Construya, entrene y despliegue modelos de ML"

CTA: "Explorar Servicios de AWS"
```

### Visual: AWS logo (official) + orange (#F59E0B / #FF9900) accent color
### Image: Same approach as GCP - use Lucide icons for each service + AWS logo SVG

---

## SECTION 6: HOW WE WORK (Interactive Stepper)
### Layout: Light background, horizontal stepper with animated progress line
### Design: 4 steps with icons, click/scroll to expand each step

**Section Header (EN):** "How We Work"
**Section Header (ES):** "Como Trabajamos"
**Subheader (EN):** "A proven methodology for cloud success"
**Subheader (ES):** "Una metodologia probada para el exito en la nube"

### Steps (REWRITTEN - cloud-specific, not academic):

**Step 1: Discovery**
- Icon: Magnifying glass / search
- EN: "We audit your current infrastructure, identify pain points, and define your cloud goals. Through stakeholder interviews and technical assessments, we build a complete picture of your needs."
- ES: "Auditamos su infraestructura actual, identificamos puntos de dolor y definimos sus objetivos cloud. A traves de entrevistas con partes interesadas y evaluaciones tecnicas, construimos una imagen completa de sus necesidades."

**Step 2: Architecture**
- Icon: Blueprint / drafting
- EN: "We design your cloud solution with detailed architecture diagrams, migration roadmaps, and security frameworks. Every solution is tailored to your specific requirements and budget."
- ES: "Disenamos su solucion cloud con diagramas de arquitectura detallados, hojas de ruta de migracion y marcos de seguridad. Cada solucion se adapta a sus requisitos y presupuesto especificos."

**Step 3: Implementation**
- Icon: Rocket / code
- EN: "We execute the migration and deployment with minimal disruption. Our team handles infrastructure provisioning, data migration, testing, and validation to ensure everything works flawlessly."
- ES: "Ejecutamos la migracion y el despliegue con minima interrupcion. Nuestro equipo gestiona el aprovisionamiento de infraestructura, la migracion de datos, pruebas y validacion para garantizar que todo funcione perfectamente."

**Step 4: Optimize & Scale**
- Icon: Chart trending up
- EN: "We continuously monitor, optimize costs, and scale your cloud environment. With 24/7 support and proactive management, your infrastructure stays performant and cost-effective."
- ES: "Monitoreamos continuamente, optimizamos costos y escalamos su entorno cloud. Con soporte 24/7 y gestion proactiva, su infraestructura se mantiene eficiente y rentable."

### Animation: Steps reveal on scroll, connecting line animates between steps

---

## SECTION 7: WHY CHOOSE US
### Layout: White background, 4 cards in grid (2x2 desktop, 1 column mobile)
### Design: Icon + metric + description cards with subtle hover animation

**Section Header (EN):** "Why Choose CloudsHorizon?"
**Section Header (ES):** "Por Que Elegir CloudsHorizon?"

### Cards:

**Card 1: Experience & Expertise**
- Icon: Award/trophy
- Metric: "Certified Experts"
- EN: "Our team holds certifications across Google Cloud and AWS, bringing deep expertise to every engagement."
- ES: "Nuestro equipo posee certificaciones en Google Cloud y AWS, aportando profunda experiencia a cada proyecto."

**Card 2: Customization**
- Icon: Sliders/settings
- Metric: "Tailored Solutions"
- EN: "No cookie-cutter approaches. Every solution is custom-designed to meet your specific business needs and goals."
- ES: "Sin soluciones genericas. Cada solucion esta disenada a medida para cumplir sus necesidades y objetivos de negocio especificos."

**Card 3: Security First**
- Icon: Shield with check
- Metric: "Enterprise Security"
- EN: "We implement industry-leading security measures and compliance frameworks to protect your data and operations."
- ES: "Implementamos medidas de seguridad lideres en la industria y marcos de cumplimiento para proteger sus datos y operaciones."

**Card 4: Ongoing Support**
- Icon: Headset/support
- Metric: "24/7 Support"
- EN: "We don't just build and leave. Our team provides continuous monitoring, optimization, and technical support."
- ES: "No solo construimos y nos vamos. Nuestro equipo proporciona monitoreo continuo, optimizacion y soporte tecnico."

---

## SECTION 8: CTA BANNER
### Layout: Full-width, gradient background (blue to teal), centered text

**Content (EN):**
```
Headline: "Ready to Transform Your Cloud Journey?"
Subtext: "Let's discuss how we can help your business leverage the full power of cloud computing."
CTA 1: "Schedule a Consultation" (white button)
CTA 2: "Call Us: +1 904-830-8747" (outline button)
```

**Content (ES):**
```
Headline: "Listo para Transformar su Viaje a la Nube?"
Subtext: "Hablemos sobre como podemos ayudar a su empresa a aprovechar todo el poder del cloud computing."
CTA 1: "Agendar una Consulta"
CTA 2: "Llamenos: +1 904-830-8747"
```

---

## SECTION 9: CONTACT
### Layout: 2-column - Form (left) + Contact info (right)
### Background: Light gray (#F8FAFC)

**Form Fields:**
- Full Name / Nombre Completo
- Email / Correo Electronico
- Company / Empresa
- Phone (optional) / Telefono (opcional)
- Service Interested In (dropdown) / Servicio de Interes
  - Cloud Migration / Migracion Cloud
  - Cloud Infrastructure / Infraestructura Cloud
  - DevOps & CI/CD
  - Cybersecurity / Ciberseguridad
  - AI & Machine Learning / IA y Aprendizaje Automatico
  - Managed Services / Servicios Administrados
  - Other / Otro
- Message / Mensaje
- Submit: "Send Message" / "Enviar Mensaje"

**Contact Info (EN):**
```
"Get in Touch"
Phone: +1 904-830-8747
WhatsApp: +57 321 636 3814
Email: amazabael@cloudshorizon.com
Location: United States / Colombia
LinkedIn: [link]
YouTube: [link]
```

**Contact Info (ES):**
```
"Contactenos"
Telefono: +1 904-830-8747
WhatsApp: +57 321 636 3814
Email: amazabael@cloudshorizon.com
Ubicacion: Estados Unidos / Colombia
LinkedIn: [link]
YouTube: [link]
```

---

## SECTION 10: FOOTER
### Layout: Dark (#0F172A), 4-column grid
### Design: Like Mission Cloud footer

**Columns:**
1. Logo + Company description + Social icons (LinkedIn, YouTube)
2. Services: Cloud Migration, Infrastructure, DevOps, Cybersecurity, AI/ML, Managed Services
3. Company: About, Partners, Contact, Careers
4. Contact: Phone, WhatsApp, Email

**Bottom bar:** Copyright 2026 CloudsHorizon Consulting. All rights reserved. | Privacy Policy | Terms of Service

---

## ANIMATIONS (Framer Motion)
- **Hero:** Fade-in + slide-up on load (staggered: headline > subtext > CTAs > badges)
- **Sections:** Fade-in-up on scroll into viewport (IntersectionObserver)
- **Service tabs:** Smooth slide transition between tab content
- **How We Work:** Step-by-step reveal with animated connecting line
- **Metrics:** Count-up animation when scrolled into view
- **Cards:** Subtle scale(1.02) + shadow elevation on hover
- **Navigation:** Background blur + shadow on scroll
- **Language toggle:** Smooth text transition

---

## RESPONSIVE BREAKPOINTS
- Desktop: 1280px+
- Tablet: 768px - 1279px
- Mobile: < 768px

### Mobile-specific changes:
- Hamburger navigation
- Single-column layouts
- Horizontal scroll tabs for services
- Stacked contact form / info
- Reduced font sizes
- Touch-friendly buttons (min 48px tap target)

---

## IMAGE & ASSET PLAN

### Approach: CSS/SVG-first, minimal stock photos
For a clean, professional look like SADA, we'll use:
1. **Lucide React icons** for all service icons (included, no extra dependency)
2. **CSS gradients and animations** for hero and section backgrounds
3. **SVG logos** for Google Cloud and AWS (recreated as inline SVGs)
4. **Client logo** from /logo/Screenshot_25.png
5. **Minimal stock images** only where necessary (service section backgrounds)

### Stock images needed (from Unsplash, free commercial use):
- 1 hero background: Abstract tech/cloud pattern OR use pure CSS gradient
- 6 service images (optional - can use icon-only approach):
  - Search: unsplash.com/s/photos/cloud-computing
  - Search: unsplash.com/s/photos/server-room
  - Search: unsplash.com/s/photos/programming
  - Search: unsplash.com/s/photos/cybersecurity
  - Search: unsplash.com/s/photos/artificial-intelligence
  - Search: unsplash.com/s/photos/monitoring-dashboard

### SVG Logos to create inline:
- Google Cloud logo (multicolor cloud icon + text)
- AWS logo (text + orange arrow)
- CloudsHorizon logo (recreate from PNG as SVG component)

---

## i18n STRATEGY
- Custom React Context-based language provider
- JSON translation files (en.json / es.json)
- Language toggle in navbar
- localStorage persistence for language preference
- No URL-based routing needed (single landing page)

---

## PERFORMANCE TARGETS
- Lighthouse Performance: 95+
- First Contentful Paint: < 1.5s
- Largest Contentful Paint: < 2.5s
- Cumulative Layout Shift: < 0.1
- Total Bundle Size: < 200KB (gzipped)
