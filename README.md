# Taller 02 – Modelo de Información y Diagrama de Contexto

## Integrantes

- Jorge Steven Doncel Bejarano – Código: 282296 / Usuario GitHub: [gevengood](https://github.com/gevengood) / Correo: [jorgedobe@unisabana.edu.co](mailto:jorgedobe@unisabana.edu.co)
- David Santiago Buendia Londoño – Código: 306487 / Usuario GitHub: [Santiagoob7](https://github.com/Santiagoob7)) /Correo: [davidbulo@unisabana.edu.co](mailto:davidbulo@unisabana.edu.co)

## Descripción

Repositorio del Taller 02 de Arquitectura Empresarial. El objetivo es modelar las entidades principales del dominio y los flujos de información entre actores y sistemas mediante dos artefactos:

- Un **Modelo Entidad–Relación (ERD)**, para representar las entidades, atributos, relaciones y cardinalidades del dominio.
- Un **Diagrama de Contexto**, para identificar actores externos, sistemas internos, sistemas externos, límite organizacional y flujos de información.

El taller se desarrolló en dos partes: primero, el caso base de la Clínica Salud Viva trabajado en clase; después, la aplicación de las mismas metodologías al cliente real, Insuclínicos Ltda.

## Parte 1 – Caso base Clínica Salud Viva

En esta parte se desarrollaron dos modelos del caso base:

- Un Modelo Entidad–Relación (ERD) para representar las entidades Paciente, Cita, Médico, Especialidad y Factura.
- Un Diagrama de Contexto para representar los actores, sistemas internos, sistema externo y flujos de información de la Clínica Salud Viva.

Los archivos de la Parte 1 se encuentran en la carpeta `clase/`:

- [`modelo-er-borrador.drawio`](clase/modelo-er-borrador.drawio)
- [`contexto-borrador.drawio`](clase/contexto-borrador.drawio)
- [`notas.md`](clase/notas.md)

## Parte 2 – Cliente real: Insuclínicos Ltda.

La Parte 2 adapta el modelo de información al dominio de **Gestión y Cumplimiento de Pedido** de Insuclínicos Ltda., empresa dedicada a fabricar y comercializar prendas e insumos médicos desechables en tela quirúrgica.

El análisis se concentra en la información necesaria para relacionar al cliente con sus pedidos, los productos solicitados, las órdenes de producción, las materias primas consumidas y el despacho. También representa el contexto actual de herramientas y comunicación: Excel, WhatsApp, correo electrónico, documentos físicos, remisiones manuales y plataforma de facturación electrónica.

### Modelo Entidad–Relación

El ERD final incluye ocho entidades principales:

- Cliente
- Pedido
- DetallePedido
- Producto
- OrdenProduccion
- MateriaPrima
- ConsumoMateriaPrima
- Despacho

La entidad **ConsumoMateriaPrima** resuelve la relación muchos-a-muchos entre OrdenProduccion y MateriaPrima, ya que una orden puede consumir varios materiales y un mismo material puede ser utilizado en varias órdenes.

### Diagrama de contexto

El diagrama de contexto identifica:

- **Actores externos:** Cliente y Proveedor.
- **Sistemas internos:** Excel Operativo, WhatsApp/Correo y Documentos Físicos/Remisiones Manuales.
- **Sistema externo:** Plataforma de Facturación Electrónica.
- **Flujos de información:** solicitudes de pedido, cotizaciones, confirmaciones, datos de inventario, solicitudes de compra, registros de producción, remisiones y datos de facturación.

Los archivos de la Parte 2 se encuentran en la carpeta `entrega/`:

| Archivo | Contenido |
|---|---|
| [`modelo-final-er.drawio`](entrega/modelo-final-er.drawio) | Modelo ER final de Insuclínicos con atributos, claves primarias, relaciones y cardinalidades. |
| [`diagrama-contexto-final.drawio`](entrega/diagrama-contexto-final.drawio) | Diagrama de contexto del flujo actual de información entre actores, herramientas internas y plataforma externa. |
| [`informe.md`](entrega/informe.md) | Informe técnico con decisiones de modelado, análisis, supuestos e investigación complementaria. |
| [`referencias.md`](entrega/referencias.md) | Fuentes académicas, guía del curso y levantamiento de información con el cliente. |

## Estructura del repositorio

```text
taller-02-modelo-informacion/
├── README.md
├── clase/
│   ├── modelo-er-borrador.drawio          # ERD del caso base — Parte 1
│   ├── contexto-borrador.drawio           # Contexto del caso base — Parte 1
│   └── notas.md                           # Notas de trabajo en clase
└── entrega/
    ├── modelo-final-er.drawio             # ERD de Insuclínicos — Parte 2
    ├── diagrama-contexto-final.drawio     # Contexto de Insuclínicos — Parte 2
    ├── informe.md                         # Informe técnico
    └── referencias.md                     # Referencias consultadas
```

## Cliente

**Insuclínicos Ltda.** es una empresa de Bogotá dedicada a la fabricación y comercialización de prendas e insumos desechables elaborados principalmente en tela quirúrgica. Atiende clínicas, consultorios odontológicos, spas y organizaciones que requieren elementos para procedimientos médicos, estéticos y ambientes controlados.

## Confidencialidad

La información se utiliza exclusivamente con fines académicos, previa autorización del cliente. Los datos personales, financieros, comerciales y sensibles de Insuclínicos Ltda., sus empleados, clientes y proveedores se omiten o se anonimizan.
