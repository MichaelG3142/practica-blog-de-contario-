estructura del codigo bueno del blog de comentario 

blog_bueno/
├── config/
│   └── Database.php                 ← Conexión segura (Singleton)
├── models/
│   ├── Contenido.php                ← Interface base
│   ├── Article.php
│   ├── VideoContent.php
│   └── GalleryContent.php
├── core/
│   ├── BlogManager.php              ← Singleton + núcleo del sistema
│   ├── ContenidoFactory.php         ← Factory
│   ├── FiltroBusqueda.php           ← Strategy
│   └── Observer.php                 ← Interfaces Observer
├── decorators/
│   ├── PremiumDecorator.php
│   ├── DestacadoDecorator.php
│   └── PatrocinadoDecorator.php
├── adapters/
│   └── SocialAdapter.php            ← Adapter
├── public/
│   └── index.php                    ← Interfaz principal
└── base.sql                         ← Script de base de datos

estructura del codigo malo
 
 blog_malo/
├── index.html          ← Página principal + visual + lógica mezclada
├── acciones.php        ← Toda la lógica del sistema (conexión, inserts, etc.)
└── base.sql            ← Script de creación de la base de datos
