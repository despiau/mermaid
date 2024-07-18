¡Entendido! Aquí están los diagramas en español, formateados para Markdown y listos para su uso en modo oscuro.

### 1. Programa de Limpieza
```mermaid
gantt
    title Programa de Limpieza
    dateFormat  YYYY-MM-DD
    section Baños
    Baño 1       :done,    des1, 2024-07-17,2024-07-17
    Baño 2       :active,  des2, 2024-07-17, 2024-07-18
    Baño 3       :         des3, 2024-07-18, 2024-07-19
    Baño 4       :         des4, 2024-07-19, 2024-07-20
    section Oficinas
    Oficina 1    :done,    des5, 2024-07-17, 2024-07-17
    Oficina 2    :active,  des6, 2024-07-17, 2024-07-18
    Oficina 3    :         des7, 2024-07-18, 2024-07-19
    Oficina 4    :         des8, 2024-07-19, 2024-07-20
    section Áreas Comunes
    Cocina       :done,    des9, 2024-07-17, 2024-07-17
    Sala de Reuniones  :active, des10, 2024-07-17, 2024-07-18
    Recepción     :         des11, 2024-07-18, 2024-07-19
    Sala de Espera  :         des12, 2024-07-19, 2024-07-20
```

### 2. Organigrama de la Empresa
```mermaid
graph TD
    A[CEO] --> B[Director de Operaciones]
    A --> C[Director de Marketing]
    A --> D[Director de Finanzas]
    B --> E[Gerente de Limpieza]
    B --> F[Gerente de Logística]
    C --> G[Coordinador de Publicidad]
    C --> H[Coordinador de Redes Sociales]
    D --> I[Contador]
    D --> J[Analista Financiero]
```

### 3. Proceso de Limpieza de Oficinas
```mermaid
flowchart LR
    A[Inicio] --> B[Inspección de la Oficina]
    B --> C[Planificación del Trabajo]
    C --> D[Limpieza General]
    D --> E[Limpieza Detallada]
    E --> F[Inspección Final]
    F --> G[Entrega del Informe]
```

### 4. Estrategia de Marketing en Redes Sociales
```mermaid
mindmap
  root((Estrategia de Marketing))
    Redes Sociales
      Facebook
      Twitter
      Instagram
      LinkedIn
      TikTok
    Publicidad Pagada
      Google Ads
      Facebook Ads
      Instagram Ads
      LinkedIn Ads
    Contenido
      Blog
      Videos
      Infografías
      Artículos
      Noticias
```

### 5. Mapa de Ubicación de Oficinas
```mermaid
erDiagram
    Oficina ||--|| Baño: tiene
    Oficina {
      int id
      string nombre
      string ubicación
    }
    Baño {
      int id
      string nombre
      string ubicación
    }
    Oficina ||--|| Cocina: tiene
    Cocina {
      int id
      string nombre
      string ubicación
    }
    Oficina ||--|| SalaDeReuniones: tiene
    SalaDeReuniones {
      int id
      string nombre
      string ubicación
    }
```

### 6. Proceso de Facturación
```mermaid
sequenceDiagram
    Cliente->>+SmartCleaning: Solicita Cotización
    SmartCleaning->>+Cliente: Envía Cotización
    Cliente->>+SmartCleaning: Acepta Cotización
    SmartCleaning->>+Cliente: Envía Factura
    Cliente->>+Banco: Realiza Pago
    Banco->>+SmartCleaning: Confirma Pago
    SmartCleaning->>+Cliente: Confirma Servicio
```

### 7. Análisis de Costos
```mermaid
pie
    title Análisis de Costos
    "Salarios": 45
    "Materiales de Limpieza": 25
    "Transporte": 15
    "Publicidad": 10
    "Otros": 5
```

### 8. Certificaciones y Licencias
```mermaid
stateDiagram-v2
    [*] --> Aplicación
    Aplicación --> Revisión
    Revisión --> Aprobación
    Aprobación --> Emisión
    Emisión --> [*]
    Emisión --> Renovación
    Renovación --> [*]
```

### 9. Base de Datos de Clientes
```mermaid
classDiagram
    class Cliente {
      +int id
      +string nombre
      +string dirección
      +string teléfono
      +string email
    }
    class Factura {
      +int id
      +date fecha
      +float monto
      +int clienteId
    }
    Cliente "1" -- "0..*" Factura: genera
```

### 10. Feedback del Cliente
```mermaid
journey
    title Feedback del Cliente
    section Experiencia del Cliente
      Satisfecho: 5: Cliente
      Neutral: 3: Cliente
      Insatisfecho: 1: Cliente
    section Resolución de Problemas
      Contacto Inicial: 5: SmartCleaning
      Solución Propuesta: 3: SmartCleaning
      Implementación de Solución: 1: SmartCleaning
```

Estos diagramas están ahora en español y adaptados para un entorno de modo oscuro. Puedes copiarlos y pegarlos en tu documento Markdown para visualizarlos correctamente.
