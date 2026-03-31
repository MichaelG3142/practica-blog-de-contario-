# Blog con Patrones de Diseño

Este repositorio contiene **dos versiones** del mismo blog para fines educativos:

- **Código Malo**: Versión intencionalmente terrible (anti-ejemplo)
- **Código Bueno**: Versión profesional usando patrones de diseño

---

## Estructura del Proyecto


```plaintext
blog_malo/
├── index.html          # Página principal + visual + lógica mezclada
├── acciones.php        # Toda la lógica del sistema (conexión, inserts, emails)
└── base.sql            # Script de creación de la base de datos

---

blog_bueno/
├── config/
│   └── Database.php                 # Conexión segura (Singleton)
│
├── models/
│   ├── Contenido.php                # Interface base
│   ├── Article.php
│   ├── VideoContent.php
│   └── GalleryContent.php
│
├── core/
│   ├── BlogManager.php              # Singleton + núcleo del sistema
│   ├── ContenidoFactory.php         # Factory
│   ├── FiltroBusqueda.php           # Strategy
│   └── Observer.php                 # Interfaces para Observer
│
├── decorators/
│   ├── PremiumDecorator.php         # Decorator abstracto
│   ├── DestacadoDecorator.php       # Decorador concreto
│   └── PatrocinadoDecorator.php     # Decorador concreto
│
├── adapters/
│   └── SocialAdapter.php            # Adapter + implementaciones
│
├── public/
│   └── index.php                    # Interfaz principal del usuario
│
└── base.sql                         # Script de base de datos
