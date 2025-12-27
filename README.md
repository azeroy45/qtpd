# 🚀 ESQUEMA DEL PROYECTO MILLONARIO - SaaS COMPLETO

## 📁 ESTRUCTURA DE ARCHIVOS

```
millonario/
│
├── 📱 FRONTEND (Next.js 15)
│   ├── app/
│   │   ├── layout.tsx                    # Layout principal
│   │   ├── page.tsx                      # Landing page / Home
│   │   ├── pricing/
│   │   │   └── page.tsx                  # Página de precios
│   │   ├── (auth)/
│   │   │   ├── login/
│   │   │   │   └── page.tsx              # Login
│   │   │   ├── register/
│   │   │   │   └── page.tsx              # Registro
│   │   │   ├── verify-email/
│   │   │   │   └── page.tsx              # Verificación email
│   │   │   └── reset-password/
│   │   │       └── page.tsx              # Reset password
│   │   ├── onboarding/
│   │   │   └── page.tsx                  # Onboarding paso a paso
│   │   ├── dashboard/
│   │   │   ├── layout.tsx                # Layout del dashboard (con sidebar)
│   │   │   ├── page.tsx                  # Dashboard principal (métricas)
│   │   │   ├── leads/
│   │   │   │   ├── page.tsx              # Lista de leads
│   │   │   │   ├── [id]/
│   │   │   │   │   └── page.tsx         # Detalle del lead
│   │   │   │   └── export/
│   │   │   │       └── page.tsx         # Exportar leads (CSV/Excel)
│   │   │   ├── templates/
│   │   │   │   ├── page.tsx              # Lista de plantillas
│   │   │   │   ├── editor/
│   │   │   │   │   └── page.tsx          # Editor tipo Wix (drag & drop)
│   │   │   │   ├── [id]/
│   │   │   │   │   ├── page.tsx         # Vista previa/editar plantilla
│   │   │   │   │   ├── link/
│   │   │   │   │   │   └── page.tsx     # Configurar link y Facebook Pixel
│   │   │   │   │   └── preview/
│   │   │   │   │       └── page.tsx     # Vista previa del link público
│   │   │   │   └── gallery/
│   │   │   │       └── page.tsx         # Galería de plantillas pre-hechas
│   │   │   ├── links/
│   │   │   │   ├── page.tsx              # Lista de links generados
│   │   │   │   └── [slug]/
│   │   │   │       └── page.tsx         # Página pública del link (landing)
│   │   │   ├── whatsapp/
│   │   │   │   ├── page.tsx              # Conexión WhatsApp
│   │   │   │   ├── qr/
│   │   │   │   │   └── page.tsx          # QR para conectar
│   │   │   │   └── settings/
│   │   │   │       └── page.tsx          # Configuración WhatsApp
│   │   │   ├── analytics/
│   │   │   │   ├── page.tsx              # Panel principal de analytics
│   │   │   │   ├── conversions/
│   │   │   │   │   └── page.tsx          # Métricas de conversión
│   │   │   │   ├── visits/
│   │   │   │   │   └── page.tsx          # Análisis de visitas
│   │   │   │   ├── credits/
│   │   │   │   │   └── page.tsx          # Gasto de créditos y ROI
│   │   │   │   └── links/
│   │   │   │       └── page.tsx          # Analytics por link
│   │   │   ├── settings/
│   │   │   │   ├── page.tsx              # Configuración general
│   │   │   │   ├── credits/
│   │   │   │   │   └── page.tsx          # Comprar créditos y historial
│   │   │   │   ├── team/
│   │   │   │   │   └── page.tsx          # Gestión de equipo
│   │   │   │   └── api-keys/
│   │   │   │       └── page.tsx          # API Keys (Enterprise)
│   │   │   └── usage/
│   │   │       └── page.tsx              # Uso actual de créditos y líneas activas
│   │   └── api/
│   │       ├── auth/
│   │       │   ├── [...nextauth]/route.ts # NextAuth config
│   │       │   ├── register/route.ts      # Registro
│   │       │   ├── verify-email/route.ts  # Verificar email
│   │       │   └── reset-password/route.ts # Reset password
│   │       ├── whatsapp/
│   │       │   ├── connect/route.ts      # Conectar WhatsApp
│   │       │   ├── disconnect/route.ts   # Desconectar
│   │       │   ├── status/route.ts       # Estado conexión
│   │       │   ├── send/route.ts         # Enviar mensaje
│   │       │   ├── webhook/route.ts       # Recibir mensajes
│   │       │   └── qr/route.ts            # Obtener QR
│   │       ├── leads/
│   │       │   ├── route.ts              # CRUD de leads
│   │       │   ├── [id]/route.ts         # Operaciones específicas
│   │       │   ├── export/route.ts       # Exportar leads
│   │       │   └── bulk/route.ts         # Operaciones masivas
│   │       ├── templates/
│   │       │   ├── route.ts              # CRUD de plantillas
│   │       │   ├── [id]/route.ts         # Operaciones específicas
│   │       │   └── gallery/route.ts      # Plantillas pre-hechas
│   │       ├── links/
│   │       │   ├── route.ts              # CRUD de links
│   │       │   ├── [slug]/route.ts       # Obtener link por slug
│   │       │   ├── [slug]/lead/route.ts  # Registrar lead desde link
│   │       │   └── [slug]/pixel/route.ts # Facebook Pixel tracking
│   │       ├── ai/
│   │       │   ├── validate/route.ts     # Validar lead con IA
│   │       │   └── analyze/route.ts      # Análisis avanzado
│   │       ├── analytics/
│   │       │   ├── route.ts              # Dashboard general de analytics
│   │       │   ├── conversions/route.ts  # Métricas de conversión
│   │       │   ├── visits/route.ts        # Análisis de visitas
│   │       │   ├── credits/route.ts     # Gasto de créditos y ROI
│   │       │   ├── links/route.ts        # Analytics por link
│   │       │   └── export/route.ts       # Exportar reportes
│   │       ├── credits/
│   │       │   ├── purchase/route.ts     # Comprar créditos
│   │       │   ├── history/route.ts      # Historial de compras
│   │       │   └── balance/route.ts      # Saldo actual de créditos
│   │       ├── team/
│   │       │   ├── invite/route.ts       # Invitar miembro
│   │       │   ├── members/route.ts      # Listar miembros
│   │       │   └── [id]/route.ts         # Gestión miembro
│   │       └── usage/
│   │           └── route.ts              # Uso actual y límites
│   │
│   ├── components/
│   │   ├── ui/                           # Componentes base (shadcn/ui)
│   │   │   ├── button.tsx
│   │   │   ├── input.tsx
│   │   │   ├── card.tsx
│   │   │   ├── dialog.tsx
│   │   │   ├── dropdown-menu.tsx
│   │   │   ├── table.tsx
│   │   │   ├── badge.tsx
│   │   │   ├── progress.tsx
│   │   │   └── ...
│   │   ├── layout/
│   │   │   ├── Sidebar.tsx                # Sidebar del dashboard
│   │   │   ├── Header.tsx                 # Header con usuario
│   │   │   ├── Footer.tsx                 # Footer
│   │   │   └── Navigation.tsx             # Navegación principal
│   │   ├── auth/
│   │   │   ├── LoginForm.tsx              # Formulario login
│   │   │   ├── RegisterForm.tsx          # Formulario registro
│   │   │   └── ProtectedRoute.tsx         # Wrapper para rutas protegidas
│   │   ├── credits/
│   │   │   ├── CreditBalance.tsx         # Saldo de créditos
│   │   │   ├── PurchaseCredits.tsx       # Comprar créditos
│   │   │   ├── CreditHistory.tsx         # Historial de compras
│   │   │   ├── CreditPackages.tsx        # Paquetes de créditos
│   │   │   └── LineUsageTracker.tsx       # Rastreador de uso por línea
│   │   ├── editor/                       # Editor tipo Wix
│   │   │   ├── Canvas.tsx                # Área de trabajo
│   │   │   ├── Toolbar.tsx               # Barra de herramientas
│   │   │   ├── Sidebar.tsx               # Panel lateral
│   │   │   ├── ElementPalette.tsx        # Elementos arrastrables
│   │   │   ├── PropertyPanel.tsx         # Panel de propiedades
│   │   │   ├── LinkSettings.tsx          # Configuración de link y pixel
│   │   │   └── blocks/
│   │   │       ├── TextBlock.tsx         # Bloque de texto
│   │   │       ├── ImageBlock.tsx        # Bloque de imagen
│   │   │       ├── ButtonBlock.tsx       # Bloque de botón genérico
│   │   │       ├── VariableBlock.tsx     # Variables dinámicas
│   │   │       ├── DividerBlock.tsx      # Separador
│   │   │       └── LeadButtonBlock.tsx    # Botón específico que redirige a WhatsApp
│   │   ├── links/
│   │   │   ├── PublicLanding.tsx         # Landing page pública del link
│   │   │   └── FacebookPixel.tsx         # Componente Facebook Pixel
│   │   ├── leads/
│   │   │   ├── LeadCard.tsx              # Tarjeta de lead
│   │   │   ├── LeadList.tsx              # Lista de leads
│   │   │   ├── LeadTable.tsx             # Tabla de leads
│   │   │   ├── LeadFilters.tsx           # Filtros de leads
│   │   │   ├── LeadStatus.tsx            # Estado del lead
│   │   │   ├── LeadValidation.tsx        # Panel de validación IA
│   │   │   └── LeadExport.tsx            # Exportar leads
│   │   ├── whatsapp/
│   │   │   ├── QRDisplay.tsx             # Mostrar QR
│   │   │   ├── ConnectionStatus.tsx      # Estado conexión
│   │   │   ├── MessagePreview.tsx        # Vista previa mensaje
│   │   │   └── ChatHistory.tsx           # Historial de chat
│   │   ├── analytics/
│   │   │   ├── AnalyticsDashboard.tsx    # Panel principal de analytics
│   │   │   ├── MetricsCard.tsx           # Tarjeta de métrica
│   │   │   ├── Chart.tsx                 # Gráficos genéricos
│   │   │   ├── ConversionFunnel.tsx      # Embudo de conversión
│   │   │   ├── ConversionRate.tsx         # Tasa de conversión
│   │   │   ├── VisitsChart.tsx           # Gráfico de visitas
│   │   │   ├── CreditsSpending.tsx       # Gasto de créditos
│   │   │   ├── ROICalculator.tsx         # Calculadora de ROI
│   │   │   ├── LinkPerformance.tsx       # Rendimiento por link
│   │   │   ├── LeadSourceChart.tsx       # Gráfico de fuentes
│   │   │   ├── DateRangePicker.tsx        # Selector de rango de fechas
│   │   │   └── AnalyticsExport.tsx       # Exportar reportes
│   │   └── team/
│   │       ├── MemberList.tsx            # Lista de miembros
│   │       ├── InviteMember.tsx          # Invitar miembro
│   │       └── RoleBadge.tsx             # Badge de rol
│   │
│   ├── lib/
│   │   ├── utils.ts                      # Utilidades generales
│   │   ├── db.ts                         # Cliente de base de datos
│   │   ├── auth.ts                       # Configuración NextAuth
│   │   ├── credits.ts                    # Gestión de créditos
│   │   ├── whatsapp.ts                   # Cliente WhatsApp Web.js
│   │   ├── ai.ts                         # Integración con IA (OpenAI/Claude)
│   │   ├── template-engine.ts            # Motor de plantillas
│   │   ├── email.ts                      # Servicio de emails (Resend/SendGrid)
│   │   ├── rate-limit.ts                 # Rate limiting
│   │   └── validations.ts                # Validaciones con Zod
│   │
│   ├── middleware.ts                     # Middleware Next.js (auth, rate limit)
│   │
│   ├── hooks/
│   │   ├── useAuth.ts                    # Hook de autenticación
│   │   ├── useCredits.ts                 # Hook de créditos
│   │   ├── useWhatsApp.ts               # Hook para WhatsApp
│   │   ├── useTemplateEditor.ts          # Hook para editor
│   │   ├── useLeadValidation.ts          # Hook para validación
│   │   ├── useAnalytics.ts               # Hook para analytics
│   │   └── useLineUsage.ts               # Hook para uso de líneas
│   │
│   ├── types/
│   │   ├── lead.ts                       # Tipos de Lead
│   │   ├── template.ts                   # Tipos de Plantilla
│   │   ├── whatsapp.ts                   # Tipos de WhatsApp
│   │   ├── user.ts                       # Tipos de Usuario
│   │   ├── credits.ts                    # Tipos de Créditos
│   │   ├── organization.ts               # Tipos de Organización
│   │   └── line.ts                       # Tipos de Línea WhatsApp
│   │
│   └── styles/
│       └── globals.css
│
├── 🤖 BACKEND (Servicios)
│   ├── services/
│   │   ├── auth-service.ts               # Servicio de autenticación
│   │   ├── credits-service.ts            # Gestión de créditos
│   │   ├── payment-service.ts            # Procesamiento de pagos (futuro)
│   │   ├── line-service.ts               # Gestión de líneas WhatsApp
│   │   ├── whatsapp-service.ts           # Servicio WhatsApp (gestión de sesiones únicas)
│   │   ├── session-manager.ts            # Gestor de sesiones únicas (evita conflictos)
│   │   ├── lead-extractor.ts             # Extractor de leads
│   │   ├── lead-capture.ts               # Captura de leads desde links
│   │   ├── ai-validator.ts               # Validador con IA
│   │   ├── template-renderer.ts           # Renderizador de plantillas
│   │   ├── link-service.ts               # Gestión de links públicos
│   │   ├── facebook-pixel.ts             # Integración Facebook Pixel
│   │   ├── email-service.ts              # Servicio de emails
│   │   ├── analytics-service.ts          # Servicio de analytics
│   │   ├── team-service.ts               # Gestión de equipo
│   │   └── notification-service.ts       # Notificaciones
│   │
│   ├── middleware/
│   │   ├── auth.middleware.ts            # Middleware de autenticación
│   │   ├── credits.middleware.ts         # Verificar créditos disponibles
│   │   ├── line-usage.middleware.ts      # Verificar uso de líneas
│   │   └── rate-limit.middleware.ts      # Rate limiting
│   │
│   └── workers/
│       ├── message-processor.ts          # Procesar mensajes entrantes
│       ├── lead-scorer.ts                # Calificar leads
│       ├── credit-consumer.ts             # Consumir créditos inmediatamente cuando llega primer lead del día
│       └── line-status-checker.ts        # Verificar estado de líneas
│
├── 💾 BASE DE DATOS (Prisma)
│   ├── prisma/
│   │   ├── schema.prisma                 # Schema completo
│   │   │   # Modelos:
│   │   │   # - User (usuarios)
│   │   │   # - Organization (organizaciones/tenants)
│   │   │   # - Credit (créditos disponibles)
│   │   │   # - CreditTransaction (historial de créditos)
│   │   │   # - WhatsAppLine (líneas conectadas)
│   │   │   # - Template (plantillas)
│   │   │   # - TemplateLink (links públicos generados)
│   │   │   # - Lead (leads)
│   │   │   # - Message (mensajes)
│   │   │   # - TeamMember (miembros del equipo)
│   │   │   # - LinkVisit (visitas a links)
│   │   │   # - LinkClick (clics en botones)
│   │   │   # - Conversion (conversiones y métricas)
│   │   │   # - Analytics (métricas agregadas)
│   │   │   # - ApiKey (API keys para Enterprise)
│   │   │
│   │   └── migrations/                   # Migraciones Prisma
│   │
│   └── seeds/
│       └── seed.ts                       # Datos iniciales
│
├── 📦 CONFIGURACIÓN
│   ├── package.json
│   ├── tsconfig.json
│   ├── next.config.js
│   ├── .env.example
│   └── .gitignore
│
├── 💾 ALMACENAMIENTO DE SESIONES
│   └── sessions/
│       └── [organizationId]/
│           └── [lineId]/
│               └── [sessionId]/
│                   └── # Archivos de sesión WhatsApp Web.js
│                   # Cada línea tiene su propia carpeta única
│                   # Aislamiento completo entre sesiones
│
└── 📚 DOCUMENTACIÓN
    ├── README.md
    └── API.md
```

---

## 🎯 FLUJO DE FUNCIONAMIENTO

### 1. **CONEXIÓN WHATSAPP (Sesiones Únicas)**
   - Usuario crea una nueva línea de WhatsApp
   - Sistema genera **sessionId único** para esa línea
   - Sistema crea **ruta única de almacenamiento** (sessionPath) para la sesión
   - Usuario escanea QR con su WhatsApp
   - WhatsApp Web.js se conecta con **sesión completamente aislada**
   - Cada WhatsApp tiene su propia instancia independiente
   - **No hay compartimiento de datos entre sesiones** (evita bloqueos)
   - Listo para enviar/recibir mensajes de forma independiente
   - Puedes tener múltiples WhatsApp conectados simultáneamente sin conflictos

### 2. **CREACIÓN DE PLANTILLA (Editor tipo Wix)**
   - Usuario arrastra elementos (texto, imágenes, botones)
   - Puede usar variables: `{{nombre}}`, `{{telefono}}`, etc.
   - **Configura botón específico para generar leads** (botón configurable)
   - Configura link único (ej: `tuapp.com/link/abc123`)
   - Configura Facebook Pixel personalizado para ese link
   - Guarda la plantilla y genera link público

### 3. **CAPTURA DE LEADS (Flujo Completo)**

**Paso 1: Landing Page**
   - Usuario comparte su link público (ej: `tuapp.com/link/abc123`)
   - Visitante entra al link y ve la plantilla renderizada
   - Facebook Pixel se activa automáticamente (si está configurado)
   - Visitante ve el contenido y el botón configurado

**Paso 2: Redirección a WhatsApp**
   - Visitante hace clic en el botón configurado
   - Se redirige a WhatsApp (web o app) con el número de la **línea conectada al link**
   - Cada link tiene máximo 1 línea de WhatsApp conectada
   - Se abre conversación con el número de WhatsApp de esa línea
   - **Aún NO es un lead** (solo visitante)

**Paso 3: Conversión en Lead**
   - Cuando el visitante **llega a WhatsApp y envía un mensaje** (o inicia conversación)
   - **AHÍ se convierte en LEAD**
   - Sistema detecta el mensaje entrante por WhatsApp API
   - El lead se asocia automáticamente a la **línea conectada al link**
   - **Se obtiene información automáticamente de WhatsApp:**
     - Nombre: Del nombre de usuario de WhatsApp
     - Teléfono: Del número de WhatsApp
     - Mensaje: El mensaje enviado por el usuario
   - Lead se registra en la base de datos (asociado al link y a la línea)
   - **Se consume 1 crédito inmediatamente** para esa línea (si es el primer lead del día en esa línea)

### 4. **CONSUMO DE CRÉDITOS (Mismo Día, Por Línea)**
   - **Cada link tiene máximo 1 línea conectada**, por lo que es fácil saber qué línea gasta créditos
   - Cuando llega el **primer lead del día en una línea específica**:
     - Sistema identifica qué línea de WhatsApp recibió el lead (a través del link)
     - Sistema verifica si ya se consumió crédito ese día para esa línea
     - Si NO se ha consumido crédito ese día para esa línea → consume **1 crédito inmediatamente**
     - Si ya se consumió crédito ese día para esa línea → NO consume más créditos (solo 1 por línea por día)
     - Registra el consumo en el historial (asociado a la línea y al link)
   - **Ejemplo con múltiples links y líneas:** 
     - Tienes 50 links, cada uno con 1 línea conectada (50 líneas en total)
     - Día 1: 100 visitantes hacen clic en diferentes links → 50 llegan a WhatsApp y envían mensaje
     - Si los 50 leads llegan a 50 líneas diferentes (1 lead por link) → se consumen **50 créditos** (1 por línea)
     - Si los 50 leads llegan a solo 10 líneas (algunos links comparten la misma línea) → se consumen **10 créditos** (1 por cada línea que recibió al menos 1 lead)
     - Los leads adicionales en la misma línea ese día NO consumen créditos adicionales
   - **Ventaja:** Sabes exactamente qué línea está gastando créditos porque cada link tiene máximo 1 línea

### 5. **PROCESAMIENTO DEL LEAD**
   - Sistema crea registro de lead en BD
   - Se envía mensaje automático a WhatsApp con la plantilla
   - IA analiza el lead y asigna puntuación (0-100)
   - Lead queda registrado en el dashboard

### 6. **VALIDACIÓN Y CONFIRMACIÓN**
   - IA verifica si es válido, spam, o necesita seguimiento
   - Lead recibe mensaje automático con plantilla
   - Si responde positivamente → Lead confirmado ✅
   - Si no responde o es negativo → Lead descartado ❌

---

## 💳 SISTEMA DE CRÉDITOS (Cómo Funciona)

### 🎯 Concepto Principal
**1 crédito = 1 día para 1 línea de WhatsApp (sin importar la cantidad de leads en esa línea)**

- Puedes comprar **1 crédito** o múltiples créditos
- Los créditos se consumen **por línea y por día**
- Si tienes 1 línea y recibes 1 lead o 100 leads → consumes **1 crédito ese día**
- Si tienes 50 líneas y todas reciben leads → consumes **50 créditos ese día** (1 por línea)
- Si tienes 50 líneas pero solo 10 reciben leads → consumes **10 créditos ese día** (1 por cada línea que recibió leads)
- El consumo se hace **inmediatamente** cuando llega el primer lead del día en cada línea

### 📊 Ejemplos Prácticos

**Ejemplo 1: Cliente con 1 línea y 100 créditos**
- Día 1, 8:00 AM: Llega primer lead en línea 1 → consume **1 crédito inmediatamente** (quedan 99)
- Día 1, resto del día: Llegan 99 leads más en línea 1 → NO consumen créditos (ya se consumió 1 ese día para esa línea)
- Día 2, 9:00 AM: Llega primer lead en línea 1 → consume **1 crédito inmediatamente** (quedan 98)
- **Resultado:** 100 créditos duran 100 días (siempre que reciba al menos 1 lead por día en esa línea)

**Ejemplo 2: Cliente con 10 líneas y 100 créditos**
- Día 1, 8:00 AM: Llega primer lead en línea 1 → consume **1 crédito** (quedan 99)
- Día 1, 9:00 AM: Llega primer lead en línea 2 → consume **1 crédito** (quedan 98)
- Día 1, 10:00 AM: Llega primer lead en línea 3 → consume **1 crédito** (quedan 97)
- ... (continúa para las 10 líneas)
- Día 1, 5:00 PM: Llega primer lead en línea 10 → consume **1 crédito** (quedan 90)
- **Total Día 1:** Consumió **10 créditos** (1 por cada línea que recibió al menos 1 lead)
- Día 1, resto del día: Llegan 500 leads más en todas las líneas → NO consumen créditos (ya se consumió 1 por línea ese día)

**Ejemplo 3: Cliente con 50 líneas y 1,000 créditos**
- Día 1: Las 50 líneas reciben leads → consume **50 créditos** (1 por línea) = quedan 950
- Día 2: Solo 30 líneas reciben leads → consume **30 créditos** (1 por cada línea que recibió leads) = quedan 920
- Día 3: Las 50 líneas reciben leads → consume **50 créditos** = quedan 870
- **Resultado:** 1,000 créditos duran aproximadamente 20 días (si todas las líneas reciben leads todos los días)

**Escenario 4: Optimización**
- Tienes 50 líneas pero solo necesitas 20 activas
- Pausas 30 líneas → Solo consumes créditos de las 20 líneas activas
- Si las 20 líneas reciben leads → consumes 20 créditos/día
- **Ahorro:** 30 créditos/día = 900 créditos/mes

### ⚙️ Funcionamiento Técnico

1. **Compra de Créditos:**
   - Usuario puede comprar **1 crédito** o múltiples
   - Créditos se agregan a su balance
   - Puede comprar más cuando quiera

2. **Creación de Link:**
   - Usuario crea plantilla en el editor
   - Configura botón específico para generar leads
   - Sistema genera link único: `tuapp.com/link/[slug]`
   - Usuario configura Facebook Pixel personalizado para ese link
   - Link queda activo y listo para compartir

3. **Flujo de Captura de Leads:**
   - **Paso 1:** Visitante entra a landing page (`tuapp.com/link/[slug]`)
   - **Paso 2:** Visitante hace clic en botón → se redirige a WhatsApp
   - **Paso 3:** Visitante llega a WhatsApp y **envía mensaje** → **AHÍ se convierte en LEAD**
   - Sistema detecta mensaje entrante por WhatsApp API
   - **Se obtiene información automáticamente de WhatsApp:**
     - Nombre: Del nombre de usuario de WhatsApp
     - Teléfono: Del número de WhatsApp
     - Mensaje: El mensaje enviado por el usuario
   - Lead se registra en la base de datos con fecha del día
   - **Se consume 1 crédito inmediatamente** cuando llega el primer lead del día

4. **Consumo Inmediato de Créditos (Por Línea):**
   - Cuando llega un lead y es el **primer lead del día en esa línea específica**:
     - Sistema identifica qué línea de WhatsApp recibió el lead
     - Sistema verifica si ya se consumió crédito ese día para esa línea
     - Si NO se ha consumido crédito ese día para esa línea → consume **1 crédito inmediatamente**
     - Si ya se consumió crédito ese día para esa línea → NO consume más créditos
     - Registra el consumo en `CreditTransaction` (asociado a la línea)
     - Actualiza el balance de créditos
   - **Ejemplo con múltiples líneas:**
     - Día 1, 8:00 AM: Llega primer lead en Línea 1 → consume **1 crédito** (quedan 99)
     - Día 1, 8:30 AM: Llegan 50 leads más en Línea 1 → NO consumen créditos (ya se consumió 1 para Línea 1)
     - Día 1, 9:00 AM: Llega primer lead en Línea 2 → consume **1 crédito** (quedan 98)
     - Día 1, 9:30 AM: Llegan 30 leads más en Línea 2 → NO consumen créditos (ya se consumió 1 para Línea 2)
     - Día 1, 10:00 AM: Llega primer lead en Línea 3 → consume **1 crédito** (quedan 97)
     - **Total Día 1:** Si tienes 50 líneas y todas reciben al menos 1 lead → consumes **50 créditos** (1 por línea)

5. **Sin Créditos:**
   - Cuando balance = 0:
     - **Los links dejan de funcionar** (no redirigen a WhatsApp)
     - **Los leads NO se guardan** (no se almacenan en la base de datos)
     - El landing page muestra mensaje de error o se desactiva
     - Usuario recibe alerta para recargar créditos
     - Una vez recargue créditos, los links vuelven a funcionar normalmentes

6. **Historial:**
   - Todas las transacciones se registran:
     - Compra de créditos (individual o paquetes)
     - Consumo diario (1 crédito por día con leads)
     - Fecha y cantidad de leads recibidos ese día
     - Reembolsos (si aplica)

### 🔗 Sistema de Links Propios

- **Cada plantilla genera un link único:** `tuapp.com/link/[slug]`
- **Links son de la plataforma** (no dominio del usuario)
- **Cada link puede tener:**
  - Su propia plantilla renderizada
  - Su propio Facebook Pixel configurado
  - Su propio botón para generar leads
  - Tracking de conversiones

### 🎨 Editor con Botón Configurable

- **Botón específico en el editor** que redirige a WhatsApp
- Usuario puede:
  - Configurar texto del botón
  - Configurar número de WhatsApp destino
  - Configurar mensaje pre-escrito para WhatsApp (opcional)
  - Configurar estilo y diseño del botón
- **Datos del lead se obtienen automáticamente:**
  - Nombre: Se obtiene del nombre de usuario de WhatsApp
  - Teléfono: Se obtiene del número de WhatsApp
  - No hay formularios, solo redirección directa a WhatsApp

### 💰 Ventajas del Modelo

✅ **Pay-per-day:** Pagas por días con leads, no por cantidad de leads
✅ **Económico:** Si recibes 1 lead o 100 leads el mismo día → solo 1 crédito
✅ **Flexible:** Compra 1 crédito o 1,000
✅ **Transparente:** Ves exactamente cuánto consumes
✅ **Sin compromisos:** No hay planes mensuales fijos
✅ **Links propios:** No necesitas dominio propio
✅ **Facebook Pixel:** Tracking personalizado por link
✅ **Escalable:** Crea tantos links como necesites
✅ **Conversión real:** Solo pagas cuando el visitante realmente llega a WhatsApp y envía mensaje

---

## 📱 SISTEMA DE SESIONES ÚNICAS DE WHATSAPP

### 🎯 Cómo Funciona (Múltiples WhatsApp Sin Bloqueos)

**Cada WhatsApp es completamente único e independiente:**

1. **Creación de Línea:**
   - Usuario crea una nueva línea de WhatsApp
   - Sistema genera `sessionId` único (UUID global)
   - Sistema crea `sessionPath` único para almacenar la sesión
   - Ejemplo: `sessions/org-123/line-456/session-789/`
   - **Cada sesión está completamente aislada**

2. **Conexión:**
   - Usuario escanea QR con su WhatsApp
   - WhatsApp Web.js crea instancia independiente
   - Sesión se guarda en ruta única (no se comparte con otras líneas)
   - Cada WhatsApp mantiene su propia autenticación

3. **Operación Independiente:**
   - Cada línea envía/recibe mensajes de forma independiente
   - No hay compartimiento de datos entre sesiones
   - Rate limiting independiente por línea
   - Cada línea tiene su propio estado de conexión

4. **Prevención de Bloqueos:**
   - **Aislamiento completo:** Cada WhatsApp es una instancia separada
   - **Sesiones únicas:** No hay conflictos entre sesiones
   - **Almacenamiento separado:** Cada sesión en su propia carpeta
   - **Identificadores únicos:** sessionId y sessionPath únicos globalmente
   - **Sin interferencia:** Si una línea se bloquea, las demás siguen funcionando

### 🔒 Ventajas del Sistema

✅ **Múltiples WhatsApp simultáneos:** Puedes tener 10, 50, 100+ WhatsApp conectados
✅ **Sin bloqueos cruzados:** Si un WhatsApp se bloquea, los demás no se afectan
✅ **Escalable:** Agrega tantas líneas como necesites
✅ **Aislamiento total:** Cada línea es completamente independiente
✅ **Gestión fácil:** Sabes exactamente qué línea está activa o inactiva
✅ **Recuperación rápida:** Si una línea se desconecta, solo afecta a esa línea

### 📊 Ejemplo Práctico

- Tienes 50 líneas de WhatsApp conectadas
- Cada una tiene su propia sesión única
- Línea 1 envía 100 mensajes/día → funciona normal
- Línea 2 envía 200 mensajes/día → funciona normal
- Línea 3 se bloquea → Solo la línea 3 se afecta, las otras 49 siguen funcionando
- Puedes desconectar/reconectar líneas individualmente sin afectar las demás

---

## 🔗 SISTEMA DE LINKS Y FACEBOOK PIXEL

### 🎯 Cómo Funciona

1. **Creación de Link:**
   - Usuario crea plantilla en el editor
   - Configura botón para generar leads
   - **Conecta máximo 1 línea de WhatsApp al link** (de las líneas disponibles)
   - Sistema genera link único: `tuapp.com/link/[slug-único]`
   - Link es propiedad de la plataforma (no necesita dominio propio)
   - **Importante:** Cada link solo puede tener 1 línea conectada, así sabes exactamente qué línea gasta créditos

2. **Configuración de Facebook Pixel:**
   - Usuario puede configurar su propio Facebook Pixel ID por link
   - Cada link puede tener un Pixel diferente
   - Pixel se carga automáticamente en la landing page pública
   - Tracking de eventos: PageView, Lead, etc.

3. **Landing Page Pública:**
   - Visitante entra a `tuapp.com/link/[slug]`
   - Ve la plantilla renderizada (diseño del editor)
   - Facebook Pixel se activa automáticamente
   - Visitante interactúa con la página

4. **Redirección a WhatsApp:**
   - Visitante hace clic en el botón configurado
   - Se redirige a WhatsApp (web o app) con número preconfigurado
   - Se abre conversación con el número de WhatsApp
   - **Aún NO es un lead** (solo visitante redirigido)

5. **Conversión en Lead:**
   - Cuando el visitante **llega a WhatsApp y envía un mensaje**
   - **AHÍ se convierte en LEAD**
   - Sistema detecta mensaje entrante por WhatsApp API
   - **Se obtiene información automáticamente de WhatsApp:**
     - Nombre: Del nombre de usuario de WhatsApp
     - Teléfono: Del número de WhatsApp
     - Mensaje: El mensaje enviado por el usuario
   - Lead se registra en la base de datos
   - Facebook Pixel registra evento "Lead" (si está configurado)
   - **Se consume 1 crédito inmediatamente** (si es el primer lead del día en esa línea)

6. **Procesamiento:**
   - Lead se valida con IA
   - Se asigna puntuación (0-100)
   - Aparece en el dashboard del usuario
   - Usuario puede hacer seguimiento

### 💡 Ventajas

✅ **Links propios:** No necesitas comprar dominio
✅ **Facebook Pixel personalizado:** Cada link tiene su propio tracking
✅ **Pay-per-lead:** Solo pagas cuando se captura un lead
✅ **Escalable:** Crea tantos links como necesites
✅ **Tracking completo:** Sabes de dónde viene cada lead

---

## 💰 ¿POR QUÉ ESTO NOS VA A HACER MILLONARIOS?

### 🎨 **Explicación para un niño de 5 años:**

Imagina que tienes una **tienda de juguetes** y muchas personas quieren comprar. Pero no sabes cuáles son clientes de verdad y cuáles solo están mirando.

**Nuestro sistema es como un ayudante mágico que:**

1. **Habla con todos los clientes por WhatsApp** (como si fuera tu asistente)
2. **Les pregunta cosas importantes** usando plantillas bonitas (como un cuestionario)
3. **Un robot inteligente decide** quién es un cliente de verdad (como un detective)
4. **Te avisa** cuáles son los clientes que realmente van a comprar

### 💵 **¿Por qué la gente pagará por esto?**

**Problema real:**
- Las empresas reciben 100 mensajes al día
- Solo 5 son clientes reales
- Pierden tiempo hablando con los 95 que no compran

**Nuestra solución:**
- Automatiza todo el proceso
- Filtra los clientes buenos automáticamente
- Ahorra horas de trabajo
- Aumenta las ventas

### 📊 **Modelo de negocio (Sistema de Créditos Enterprise):**

**1 crédito = 1 día para 1 línea de WhatsApp (sin importar cantidad de leads en esa línea)**
**Precio: $3 USD por crédito (mínimo)**

**Perfil de Cliente:**
- **Clientes Enterprise y Grandes Empresas**
- **30 a 60 líneas de WhatsApp por cliente**
- Alto volumen de leads diarios
- Necesitan múltiples campañas simultáneas

**Cómo funciona:**
- Los leads llegan por WhatsApp (API) o desde links públicos
- **Cada línea que recibe al menos 1 lead en un día → consume 1 crédito inmediatamente** (cuando llega el primer lead a esa línea)
- Si tienes 30 líneas y todas reciben leads → consumes 30 créditos ese día = **$90/día**
- Si tienes 60 líneas y todas reciben leads → consumes 60 créditos ese día = **$180/día**
- Si una línea no recibe leads un día → NO consumes crédito para esa línea ese día

**Ejemplo práctico - Cliente Enterprise:**
- Cliente con **50 líneas de WhatsApp activas**
- Día 1: Las 50 líneas reciben leads → consume 50 créditos = **$150**
- Día 2: 45 líneas reciben leads → consume 45 créditos = **$135**
- Día 3: Las 50 líneas reciben leads → consume 50 créditos = **$150**
- **Gasto mensual estimado:** ~$4,500 (si todas las líneas reciben leads todos los días)

**Paquetes de créditos:**
- **Crédito individual:** $3 USD
- **Paquetes con descuento por volumen** (para clientes enterprise)

**Ventajas:**
- **Pay-per-day-per-line:** Pagas por días con leads por línea, no por cantidad de leads
- **Económico:** Si una línea recibe 1 lead o 1000 leads el mismo día, solo pagas 1 crédito ($3) por esa línea
- **Escalable:** Agrega más líneas cuando necesites, cada una consume 1 crédito por día con leads
- **Links propios:** No necesitas dominio propio
- **Facebook Pixel:** Tracking personalizado por link
- **Sesiones únicas:** Cada WhatsApp es independiente, evita bloqueos
- Con nuestro sistema:
  - Ahorra 6 horas/día de trabajo
  - Encuentra los 10 clientes buenos automáticamente
  - Aumenta ventas 30%
  - **Paga $99/mes y gana $10,000+ más**

**Resultado:** Están felices de pagar porque ganan mucho más.

---

## 🔑 TECNOLOGÍAS CLAVE

### Frontend
- **Next.js 15:** Framework React con App Router
- **TypeScript:** Tipado estático
- **Tailwind CSS:** Estilos rápidos
- **shadcn/ui:** Componentes UI bonitos
- **React DnD:** Drag & drop para editor
- **Recharts/Chart.js:** Gráficos y analytics
- **Zustand/Redux:** Estado global

### Backend
- **Next.js API Routes:** API endpoints
- **NextAuth.js:** Autenticación
- **Prisma:** ORM para base de datos
- **PostgreSQL:** Base de datos (o MySQL)
- **WhatsApp Web.js:** Integración WhatsApp
- **OpenAI/Claude API:** IA para validación
- **Facebook Pixel SDK:** Tracking de conversiones

### SaaS Essentials
- **Sistema de créditos:** Propio (sin Stripe por ahora)
- **Resend/SendGrid:** Emails transaccionales
- **Vercel/PlanetScale:** Hosting y DB
- **Upstash Redis:** Rate limiting y cache
- **Sentry:** Monitoreo de errores
- **PostHog/Mixpanel:** Analytics de producto
- **Stripe (futuro):** Para pagos de créditos cuando esté listo

### DevOps
- **Docker:** Contenedores
- **GitHub Actions:** CI/CD
- **Vercel:** Deploy automático

---

---

## 🏗️ FUNCIONALIDADES SaaS COMPLETAS

### 1. **AUTENTICACIÓN Y USUARIOS**
- ✅ Registro con email/contraseña
- ✅ Login con NextAuth.js
- ✅ Verificación de email
- ✅ Recuperación de contraseña
- ✅ Autenticación de dos factores (2FA)
- ✅ Sesiones seguras
- ✅ Logout

### 2. **MULTI-TENANCY (Organizaciones)**
- ✅ Cada usuario pertenece a una organización
- ✅ Un usuario puede tener múltiples organizaciones
- ✅ Datos completamente aislados por organización
- ✅ Cambio de organización en el dashboard

### 3. **SISTEMA DE CRÉDITOS (Pay-per-Day-per-Line)**
- ✅ Modelo basado en créditos (no suscripciones)
- ✅ **1 crédito = 1 día para 1 línea de WhatsApp** (sin importar cantidad de leads en esa línea)
- ✅ Puedes comprar **1 crédito** o múltiples
- ✅ Compra de créditos individuales o en paquetes
- ✅ Historial de transacciones de créditos (por línea)
- ✅ Saldo de créditos en tiempo real
- ✅ **Consumo inmediato automático** (1 crédito por línea cuando llega el primer lead del día a esa línea)
- ✅ Si tienes 1 línea y recibes 1 lead o 100 leads → solo 1 crédito ese día
- ✅ Si tienes 50 líneas y todas reciben leads → 50 créditos ese día (1 por línea)
- ✅ Si una línea no recibe leads un día → NO consume crédito para esa línea ese día
- ✅ Alertas cuando se acaban los créditos
- ✅ Links dejan de funcionar completamente sin créditos (no redirigen, no guardan leads)

### 4. **EDITOR CON BOTÓN CONFIGURABLE**
- ✅ Editor tipo Wix con drag & drop
- ✅ **Botón específico configurable** que redirige a WhatsApp
- ✅ Configuración de número de WhatsApp destino
- ✅ Configuración de mensaje pre-escrito para WhatsApp
- ✅ Configuración de texto del botón
- ✅ Configuración de estilo y diseño del botón
- ✅ Preview en tiempo real

### 5. **SISTEMA DE LINKS PROPIOS**
- ✅ Cada plantilla genera un **link único propio** (ej: `tuapp.com/link/abc123`)
- ✅ Links son de la plataforma (no necesitas dominio propio)
- ✅ Cada link tiene su propia plantilla renderizada
- ✅ **Cada link puede tener máximo 1 línea de WhatsApp conectada**
- ✅ Esto permite saber exactamente qué línea está gastando créditos
- ✅ Si un link no tiene línea conectada, no puede recibir leads
- ✅ Links públicos y compartibles
- ✅ Tracking de visitas y conversiones por link
- ✅ Dashboard de links generados con información de la línea conectada

### 6. **FACEBOOK PIXEL POR LINK**
- ✅ Cada link puede tener su **propio Facebook Pixel** configurado
- ✅ Configuración independiente por link
- ✅ Tracking de eventos personalizados
- ✅ Integración automática en la landing page
- ✅ Dashboard de eventos de Pixel por link

### 7. **GESTIÓN DE LÍNEAS WHATSAPP (Múltiples WhatsApp Únicos)**
- ✅ Cada WhatsApp conectado = 1 línea única e independiente
- ✅ **Cada WhatsApp tiene su propia sesión única** (sessionId único globalmente)
- ✅ **Cada sesión se almacena en ruta única** (sessionPath) para evitar conflictos
- ✅ Múltiples líneas por organización (sin límite)
- ✅ **Cada línea es completamente independiente** (evita bloqueos cruzados)
- ✅ **Cada línea puede estar conectada a múltiples links** (pero cada link solo puede tener 1 línea)
- ✅ Estado de cada línea (connected/disconnected/paused/authenticating)
- ✅ Envío automático de leads a WhatsApp
- ✅ Dashboard de líneas activas con información de qué links están conectados
- ✅ **Tracking de créditos por línea:** Sabes exactamente qué línea gasta créditos porque cada link tiene máximo 1 línea
- ✅ **Prevención de bloqueos:**
  - Cada WhatsApp tiene sesión completamente aislada
  - No hay compartimiento de datos entre sesiones
  - Cada número de WhatsApp es único por organización
  - Rate limiting independiente por línea

### 5. **GESTIÓN DE EQUIPO**
- ✅ Invitar miembros al equipo
- ✅ Roles: Owner, Admin, Member
- ✅ Permisos por rol
- ✅ Eliminar miembros
- ✅ Transferir propiedad de organización

### 6. **ANALYTICS Y REPORTES (Panel Dedicado)**
- ✅ **Panel principal de Analytics** con métricas en tiempo real
- ✅ **Métricas de Conversión:**
  - Tasa de conversión (visitas → clics → leads)
  - Conversiones totales
  - Conversiones por día/semana/mes
  - Embudo de conversión completo
  - Conversiones por link
  - Conversiones por línea de WhatsApp
- ✅ **Métricas de Visitas:**
  - Visitas totales
  - Visitas únicas
  - Visitas por día/semana/mes
  - Visitas por link
  - Visitas por dispositivo (mobile/desktop/tablet)
  - Visitas por país/ciudad
  - Tasa de rebote
  - Tiempo en página
- ✅ **Métricas de Gasto:**
  - Créditos gastados totales
  - Créditos gastados por día/semana/mes
  - Créditos gastados por link
  - Créditos gastados por línea
  - Costo por lead (créditos/leads)
  - ROI (Retorno de Inversión)
  - Proyección de gasto mensual
- ✅ **Métricas Adicionales:**
  - Leads totales
  - Leads validados vs descartados
  - Fuentes de leads
  - Gráficos de tendencias
  - Comparación de periodos
- ✅ **Filtros y Segmentación:**
  - Por rango de fechas
  - Por link específico
  - Por línea de WhatsApp
  - Por dispositivo
  - Por país/región
- ✅ **Exportar datos** (CSV, Excel, PDF)
- ✅ **Reportes personalizados** y programados
- ✅ **Alertas y notificaciones** cuando se alcanzan metas

### 7. **ONBOARDING**
- ✅ Tour guiado para nuevos usuarios
- ✅ Pasos: Conectar WhatsApp → Crear plantilla → Ver primer lead
- ✅ Tooltips y ayuda contextual

### 8. **NOTIFICACIONES**
- ✅ Notificaciones en la app
- ✅ Emails de eventos importantes
- ✅ Alertas de límites de uso
- ✅ Notificaciones de nuevos leads

### 9. **SEGURIDAD**
- ✅ Rate limiting en todas las APIs
- ✅ Validación de datos con Zod
- ✅ Sanitización de inputs
- ✅ HTTPS obligatorio
- ✅ CORS configurado
- ✅ Logs de auditoría

### 10. **API PARA ENTERPRISE**
- ✅ Generación de API keys
- ✅ Documentación de API (Swagger)
- ✅ Rate limiting por key
- ✅ Webhooks personalizados

---

## 📊 MODELO DE DATOS (Prisma Schema)

```prisma
// Modelo basado en créditos
model User {
  id            String   @id @default(cuid())
  email         String   @unique
  password      String
  name          String?
  emailVerified DateTime?
  createdAt     DateTime @default(now())
  organizations OrganizationMember[]
}

model Organization {
  id             String   @id @default(cuid())
  name           String
  slug           String   @unique
  members        OrganizationMember[]
  credits        Credit[]
  creditTransactions CreditTransaction[]
  whatsappLines  WhatsAppLine[]
  leads          Lead[]
  templates      Template[]
  visits         LinkVisit[]
  clicks         LinkClick[]
  conversions    Conversion[]
  analytics      Analytics[]
  createdAt      DateTime @default(now())
}

model Credit {
  id             String   @id @default(cuid())
  organizationId String
  organization   Organization @relation(fields: [organizationId], references: [id])
  balance        Int      @default(0)  // Créditos disponibles
  createdAt      DateTime @default(now())
  updatedAt      DateTime @updatedAt
}

model CreditTransaction {
  id             String   @id @default(cuid())
  organizationId String
  organization   Organization @relation(fields: [organizationId], references: [id])
  lineId         String?  // Línea que generó el consumo
  line           WhatsAppLine? @relation(fields: [lineId], references: [id])
  type           String   // 'purchase', 'line_consumption', 'refund'
  amount         Int      // Cantidad de créditos (+ o -)
  date           DateTime // Fecha del consumo
  description    String?
  createdAt      DateTime @default(now())
}

model DailyLineUsage {
  id             String   @id @default(cuid())
  organizationId String
  organization   Organization @relation(fields: [organizationId], references: [id])
  lineId         String
  line           WhatsAppLine @relation(fields: [lineId], references: [id])
  date           DateTime // Fecha (solo fecha, sin hora)
  leadsCount     Int      @default(0) // Cantidad de leads recibidos ese día en esa línea
  creditConsumed Boolean  @default(false) // Si ya se consumió el crédito ese día para esta línea
  creditConsumedAt DateTime? // Timestamp exacto cuando se consumió el crédito
  createdAt      DateTime @default(now())
  updatedAt      DateTime @updatedAt
  
  @@unique([lineId, date]) // Una entrada por línea por día
}

model WhatsAppLine {
  id             String   @id @default(cuid())
  organizationId String
  organization   Organization @relation(fields: [organizationId], references: [id])
  name           String?  // Nombre personalizado de la línea
  phoneNumber    String   // Número de WhatsApp (único por organización)
  sessionId      String   @unique // ID de sesión único WhatsApp Web.js (único globalmente)
  sessionPath     String   @unique // Ruta única donde se almacena la sesión (evita conflictos)
  qrCode         String?  // QR code para conectar (temporal)
  qrExpiresAt    DateTime? // Expiración del QR
  status         String   // 'connected', 'disconnected', 'paused', 'authenticating'
  lastConnectedAt DateTime? // Última vez que se conectó
  isActive       Boolean  @default(true) // Si está activa y puede recibir leads
  links          TemplateLink[] // Links conectados a esta línea (cada link solo puede tener 1 línea)
  leads          Lead[]   // Leads recibidos en esta línea
  creditTransactions CreditTransaction[] // Consumos de créditos de esta línea
  dailyUsage     DailyLineUsage[] // Uso diario de esta línea
  createdAt      DateTime @default(now())
  updatedAt      DateTime @updatedAt
  
  @@unique([organizationId, phoneNumber]) // Cada número es único por organización
}

model Template {
  id             String   @id @default(cuid())
  organizationId String
  organization   Organization @relation(fields: [organizationId], references: [id])
  name           String
  content        Json     // Contenido de la plantilla (bloques del editor)
  link           TemplateLink? // Link generado para esta plantilla
  createdAt      DateTime @default(now())
  updatedAt      DateTime @updatedAt
}

model TemplateLink {
  id             String   @id @default(cuid())
  templateId     String   @unique
  template       Template @relation(fields: [templateId], references: [id])
  organizationId String
  organization   Organization @relation(fields: [organizationId], references: [id])
  lineId         String?  @unique // Máximo 1 línea conectada por link
  line           WhatsAppLine? @relation(fields: [lineId], references: [id])
  slug           String   @unique // URL única: tuapp.com/link/[slug]
  facebookPixelId String? // ID del Facebook Pixel configurado
  isActive       Boolean  @default(true)
  leads          Lead[]
  creditTransactions CreditTransaction[]
  visits         LinkVisit[]
  clicks         LinkClick[]
  conversions    Conversion[]
  analytics      Analytics[]
  createdAt      DateTime @default(now())
  updatedAt      DateTime @updatedAt
}

model Lead {
  id             String   @id @default(cuid())
  organizationId String
  organization   Organization @relation(fields: [organizationId], references: [id])
  lineId         String   // Línea de WhatsApp que recibió el lead
  line           WhatsAppLine @relation(fields: [lineId], references: [id])
  linkId         String? // Link que generó el lead (si aplica)
  link           TemplateLink? @relation(fields: [linkId], references: [id])
  phone          String   // Número de WhatsApp (obtenido automáticamente)
  name           String?  // Nombre de usuario de WhatsApp (obtenido automáticamente)
  message        String?  // Mensaje enviado por el usuario
  status         String   // 'pending', 'validated', 'confirmed', 'rejected'
  aiScore         Int?     // 0-100
  receivedDate   DateTime // Fecha en que se recibió (para consumo diario por línea)
  click          LinkClick? // Click que generó este lead
  conversion     Conversion? // Conversión asociada
  createdAt      DateTime @default(now())
}

model LinkVisit {
  id             String   @id @default(cuid())
  linkId         String
  link           TemplateLink @relation(fields: [linkId], references: [id])
  organizationId String
  organization   Organization @relation(fields: [organizationId], references: [id])
  ipAddress      String?
  userAgent      String?
  referrer       String?
  country        String?
  city           String?
  device         String?  // 'mobile', 'desktop', 'tablet'
  browser        String?
  clicks         LinkClick[] // Clics desde esta visita
  conversions    Conversion[] // Conversiones desde esta visita
  createdAt      DateTime @default(now())
}

model LinkClick {
  id             String   @id @default(cuid())
  linkId         String
  link           TemplateLink @relation(fields: [linkId], references: [id])
  organizationId String
  organization   Organization @relation(fields: [organizationId], references: [id])
  visitId        String?  // Relación con la visita
  visit          LinkVisit? @relation(fields: [visitId], references: [id])
  clickedAt      DateTime @default(now())
  converted      Boolean  @default(false) // Si se convirtió en lead
  leadId         String?  // Si se convirtió, referencia al lead
  lead           Lead?    @relation(fields: [leadId], references: [id])
  conversions    Conversion[] // Conversiones desde este click
  createdAt      DateTime @default(now())
}

model Conversion {
  id             String   @id @default(cuid())
  organizationId String
  organization   Organization @relation(fields: [organizationId], references: [id])
  linkId         String?
  link           TemplateLink? @relation(fields: [linkId], references: [id])
  leadId         String   @unique
  lead           Lead @relation(fields: [leadId], references: [id])
  visitId        String?  // Visita que generó la conversión
  visit          LinkVisit? @relation(fields: [visitId], references: [id])
  clickId        String?  // Click que generó la conversión
  click          LinkClick? @relation(fields: [clickId], references: [id])
  conversionValue Float?   // Valor de la conversión (si aplica)
  conversionDate DateTime @default(now())
  createdAt      DateTime @default(now())
}

model Analytics {
  id             String   @id @default(cuid())
  organizationId String
  organization   Organization @relation(fields: [organizationId], references: [id])
  linkId         String?
  link           TemplateLink? @relation(fields: [linkId], references: [id])
  date           DateTime // Fecha del reporte
  visits         Int      @default(0) // Visitas del día
  clicks         Int      @default(0) // Clics del día
  conversions    Int      @default(0) // Conversiones del día
  creditsSpent   Int      @default(0) // Créditos gastados
  conversionRate Float?   // Tasa de conversión (%)
  costPerLead    Float?   // Costo por lead (créditos/leads)
  createdAt      DateTime @default(now())
  updatedAt      DateTime @updatedAt
  
  @@unique([organizationId, linkId, date]) // Un reporte por link por día
}

// ... más modelos (Template, Message, TeamMember, etc.)
```

---

## 📊 SISTEMA DE TRACKING Y ANALYTICS

### 🎯 Cómo Funciona el Tracking

1. **Tracking de Visitas:**
   - Cuando un visitante entra a un link (`tuapp.com/link/[slug]`)
   - Se registra automáticamente una visita (`LinkVisit`)
   - Se captura información: IP, user agent, referrer, país, ciudad, dispositivo, navegador
   - Se asocia a la organización y al link específico

2. **Tracking de Clics:**
   - Cuando el visitante hace clic en el botón de WhatsApp
   - Se registra un clic (`LinkClick`)
   - Se asocia a la visita original
   - Se marca si se convirtió en lead posteriormente

3. **Tracking de Conversiones:**
   - Cuando el visitante llega a WhatsApp y envía mensaje (se convierte en lead)
   - Se crea un registro de conversión (`Conversion`)
   - Se vincula con: visita, clic, lead y link
   - Se calcula la tasa de conversión automáticamente

4. **Cálculo de Métricas:**
   - **Tasa de conversión:** (Conversiones / Visitas) × 100
   - **Costo por lead:** Créditos gastados / Leads generados
   - **ROI:** Valor de conversiones / Costo en créditos
   - **Embudo:** Visitas → Clics → Conversiones

### 📈 Métricas Disponibles en el Panel

**Dashboard Principal:**
- Resumen general de todas las métricas
- Comparación con periodo anterior
- Gráficos de tendencias
- Top links por rendimiento

**Panel de Conversiones:**
- Tasa de conversión total y por link
- Embudo de conversión completo
- Conversiones por día/semana/mes
- Conversiones por línea de WhatsApp

**Panel de Visitas:**
- Visitas totales y únicas
- Visitas por dispositivo (mobile/desktop/tablet)
- Visitas por país/ciudad
- Visitas por link
- Tasa de rebote
- Tiempo promedio en página

**Panel de Gasto:**
- Créditos gastados totales
- Créditos gastados por día/semana/mes
- Créditos gastados por link
- Costo por lead
- Proyección de gasto mensual
- ROI calculado

**Panel por Link:**
- Rendimiento individual de cada link
- Comparación entre links
- Métricas específicas por link
- Historial de rendimiento

---

## ✅ PRÓXIMOS PASOS (Cuando quieras programar)

### FASE 1: Fundación (Semana 1-2)
1. ✅ Inicializar proyecto Next.js 15 + TypeScript
2. ✅ Configurar Prisma + PostgreSQL
3. ✅ Crear schema de base de datos completo
4. ✅ Configurar NextAuth.js (autenticación)
5. ✅ Crear páginas de login/registro
6. ✅ Sistema de multi-tenancy (organizaciones)

### FASE 2: Core Features (Semana 3-4)
7. ✅ Sistema de créditos (compra individual o paquetes, balance, historial)
8. ✅ Gestión de líneas WhatsApp (múltiples líneas)
9. ✅ **Sistema de sesiones únicas** (sessionId y sessionPath únicos por línea)
10. ✅ **Gestor de sesiones** (aislamiento completo entre WhatsApp)
11. ✅ Dashboard principal con métricas
12. ✅ Integrar WhatsApp Web.js
13. ✅ Sistema de conexión WhatsApp (QR) con sesiones únicas
14. ✅ Almacenamiento de sesiones en rutas únicas (evita conflictos)
15. ✅ Detección automática de mensajes entrantes por WhatsApp API
16. ✅ Obtención automática de datos del lead (nombre y teléfono desde WhatsApp)

### FASE 3: Editor y Plantillas (Semana 5-6)
13. ✅ Construir editor drag & drop (tipo Wix)
14. ✅ Sistema de plantillas (CRUD)
15. ✅ **Botón configurable para generar leads** en el editor
16. ✅ Motor de renderizado de plantillas
17. ✅ Variables dinámicas en plantillas
18. ✅ **Sistema de links propios** (generación de slugs únicos)
19. ✅ **Páginas públicas de links** (landing pages)
20. ✅ Galería de plantillas pre-hechas

### FASE 4: Links, Pixel y Consumo de Créditos (Semana 7)
21. ✅ **Integración Facebook Pixel** (configuración por link)
22. ✅ **Sistema de redirección a WhatsApp desde botón**
23. ✅ **Detección de mensajes entrantes por WhatsApp API**
24. ✅ **Conversión de visitante a lead cuando llega a WhatsApp**
25. ✅ **Consumo inmediato automático de créditos** (cuando llega el primer lead del día)
26. ✅ Landing page pública con botón configurable
27. ✅ Integrar OpenAI/Claude API
28. ✅ Sistema de validación de leads con IA
29. ✅ Scoring de leads (0-100)
30. ✅ Clasificación automática (válido/spam/necesita seguimiento)

### FASE 5: Analytics y Reportes (Semana 8)
31. ✅ **Sistema de tracking de visitas** (LinkVisit)
32. ✅ **Sistema de tracking de clics** (LinkClick)
33. ✅ **Sistema de tracking de conversiones** (Conversion)
34. ✅ **Panel principal de analytics** con métricas en tiempo real
35. ✅ **Panel de conversiones** (tasa, embudo, por link)
36. ✅ **Panel de visitas** (totales, por dispositivo, por país)
37. ✅ **Panel de gasto** (créditos gastados, costo por lead, ROI)
38. ✅ **Panel por link** (rendimiento individual)
39. ✅ Gráficos interactivos y visualizaciones
40. ✅ Filtros y segmentación avanzada
41. ✅ Sistema de exportación (CSV, Excel, PDF)
42. ✅ Reportes personalizados y programados
43. ✅ Alertas cuando se alcanzan metas

### FASE 6: SaaS Essentials (Semana 9-10)
29. ✅ Sistema de compra de créditos (individual y paquetes)
30. ✅ Gestión de equipo (invitar/eliminar)
31. ✅ Control de uso de créditos y tracking de leads
32. ✅ Notificaciones (email + in-app) - alertas de créditos bajos
33. ✅ Onboarding guiado
34. ✅ Dashboard de links generados y estadísticas
35. ✅ Analytics de Facebook Pixel por link

### FASE 7: Pulido y Deploy (Semana 11-12)
31. ✅ Testing (unitarios + integración)
32. ✅ Optimización de performance
33. ✅ SEO y landing page
34. ✅ Documentación
35. ✅ Deploy a producción (Vercel)
36. ✅ Monitoreo (Sentry)

---

## 🎯 MÉTRICAS DE ÉXITO

### KPIs del Producto
- **MRR (Monthly Recurring Revenue):** Meta $10K en 6 meses
- **Churn Rate:** < 5% mensual
- **Conversion Rate:** 3-5% (visitante → cliente)
- **NPS (Net Promoter Score):** > 50

### Métricas Técnicas
- **Uptime:** 99.9%
- **Tiempo de respuesta API:** < 200ms
- **Tiempo de carga página:** < 2s
- **Error rate:** < 0.1%

---

---

