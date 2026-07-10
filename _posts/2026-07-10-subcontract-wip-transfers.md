---
title: "Transferencias WIP entre subcontratistas en Business Central: control real del producto semiterminado"
date: 2026-07-10
categories:
  - Dynamics 365 Business Central
  - Fabricación
  - Subcontratación
tags:
  - business central
  - fabricación
  - subcontracting
  - wip
  - work in progress
  - transfer orders
  - supply chain
  - microsoft
description: "Analizamos cómo Business Central gestiona las transferencias WIP entre subcontratistas, qué requisitos exige y qué beneficios aporta a fabricantes, partners y consultores."
image:
  path: 01-portada.png
  alt: "Ilustración corporativa sobre transferencias WIP entre subcontratistas en Business Central"
media_subpath: /assets/posts/subcontract-wip-transfers/
---

En los entornos de fabricación en los que intervienen varios terceros, el producto semiterminado rara vez permanece estático. Puede salir del almacén propio, pasar por distintos subcontratistas y volver a la empresa para continuar o finalizar su proceso productivo. Este movimiento físico plantea una cuestión clave: ¿cómo registrar el desplazamiento del trabajo en curso sin tratarlo como si fuera un stock convencional?

La funcionalidad de transferencias WIP entre subcontratistas en Dynamics 365 Business Central responde precisamente a ese reto. Su objetivo es documentar el movimiento del producto en curso entre ubicaciones de subcontratación o entre la planta propia y el proveedor externo, manteniendo al mismo tiempo la lógica financiera y operativa del pedido de producción.

Para fabricantes con procesos complejos, esta capacidad supone una mejora relevante en trazabilidad, control operativo y coherencia de costes. También abre nuevas oportunidades para partners y consultores que trabajan en escenarios de producción avanzada, multioperación y logística externa.

## Qué es

Una transferencia WIP (Work in Progress) en Business Central representa el movimiento del artículo principal de una orden de producción mientras aún está en proceso. En lugar de registrar ese movimiento como una transferencia de inventario estándar, la solución lo trata como parte del flujo productivo del pedido.

Esto es importante porque el producto semiterminado no se considera un artículo independiente que cambie de valoración cada vez que se mueve. Sigue bajo el paraguas de costes de la orden de producción. Por eso, al contabilizar una transferencia WIP no se generan movimientos estándar de producto, valor o almacén; el seguimiento se realiza en un registro específico de WIP de subcontratación.

La funcionalidad está pensada para escenarios de subcontratación en varias etapas, incluyendo movimientos entre subcontratista y subcontratista. De esta forma, Business Central refleja mejor la realidad operativa sin forzar procesos de inventario que no corresponden al contexto del producto en curso.

## Principales características

Las transferencias WIP se activan desde la ruta de fabricación mediante un indicador específico en la línea de operación subcontratada. Ese enfoque evita duplicar líneas o modelados artificiales del proceso. La propia línea de ruta controla cuándo una operación debe provocar el traslado del producto semiterminado.

Entre sus capacidades más destacadas se encuentran:

- Uso de pedidos de transferencia para documentar envíos y recepciones del WIP.
- Registro del movimiento en un libro específico de WIP de subcontratación.
- Cálculo automático de ubicaciones de origen y destino según la fase del proceso.
- Determinación de cantidades iniciales y posteriores basada en la orden de producción o en el saldo WIP existente.
- Compatibilidad con escenarios de subcontratación en múltiples fases.
- Posibilidad de ajustar manualmente cantidades WIP cuando existen discrepancias.
- Opción de limpieza automática del WIP restante al finalizar la orden de producción.

Además, Business Central permite definir descripciones específicas por operación, algo útil cuando el mismo artículo principal atraviesa varias etapas y conviene identificar el grado de avance que se está transfiriendo.

## Beneficios para las empresas

Desde una perspectiva empresarial, esta funcionalidad aporta tres ventajas claras: mayor visibilidad del flujo físico, mejor alineación entre operaciones y costes, y menor riesgo de inconsistencias en producción.

### 1. Trazabilidad más fiel al proceso real
Las empresas pueden saber dónde se encuentra el producto semiterminado en cada fase: en tránsito, en el subcontratista actual o pendiente de retorno. Esto mejora el seguimiento del pedido y facilita la coordinación entre producción, compras y logística.

### 2. Menos distorsiones contables
Al no convertir el WIP en movimientos estándar de inventario, se evita mezclar un tránsito productivo con una transacción de stock tradicional. El sistema mantiene el coste bajo la orden de producción, lo que ofrece una lectura más coherente del proceso.

### 3. Mayor control en entornos complejos
Cuando existen operaciones paralelas, movimientos entre varios proveedores o necesidades de devolución, el sistema conserva una lógica unificada de seguimiento. Esto reduce el uso de controles manuales y mejora la capacidad de auditoría.

### 4. Soporte para correcciones operativas
Si el stock físico no coincide con el registrado, se pueden realizar ajustes del WIP sin alterar el diseño del flujo productivo. También es posible limpiar cantidades sobrantes al cerrar la orden, lo que ayuda a dejar el sistema en un estado consistente.

## Beneficios para partners y consultores

Para partners y consultores de Business Central, las transferencias WIP entre subcontratistas representan una funcionalidad con alto valor en proyectos industriales.

- Permiten diseñar soluciones más cercanas al proceso real del cliente, especialmente en fabricación por fases.
- Ayudan a reducir desarrollos ad hoc en escenarios donde antes se recurría a personalizaciones para controlar producto semiterminado fuera de planta.
- Facilitan conversaciones de preventa y diagnóstico funcional al ofrecer una respuesta clara para la logística del WIP.
- Abren oportunidades de consultoría en parametrización, rutas, ubicaciones, transfer routes y gobierno de datos de producción.
- Mejoran la propuesta de valor en implantaciones para sectores con operaciones externas recurrentes, como metal, mecanizado, tratamiento de superficies o ensamblaje especializado.

En términos prácticos, esta funcionalidad puede simplificar el blueprint durante la fase de análisis, porque permite separar mejor qué parte del flujo corresponde a compras, cuál pertenece a producción y cuál debe tratarse como tránsito productivo.

## Casos de uso

### Subcontratación secuencial de varias operaciones
Una empresa envía una pieza a un proveedor para mecanizado, después a un segundo proveedor para tratamiento térmico y finalmente a un tercero para acabado. Business Central permite registrar cada movimiento como parte del WIP sin convertir cada fase en stock estándar.

### Envío inicial desde almacén propio al primer proveedor
Cuando la primera operación subcontratada empieza fuera de planta, el sistema calcula la transferencia desde la ubicación de la orden de producción hacia la ubicación del subcontratista.

### Movimiento entre subcontratistas
Si el producto ya está en una ubicación externa y debe pasar a otra operación también subcontratada, el sistema determina el origen a partir del proveedor anterior y genera la transferencia correspondiente.

### Retorno del producto semiterminado a la empresa
Si el WIP necesita volver a la ubicación propia, se pueden generar transferencias de retorno según las cantidades registradas en el libro WIP.

### Ajuste de discrepancias y cierre de orden
Cuando existe diferencia entre la cantidad física y la registrada, el equipo puede ejecutar ajustes. Al finalizar la orden, también puede realizar una limpieza automática del WIP pendiente.

## Requisitos y configuración

Para que la funcionalidad encaje correctamente en una implantación, conviene revisar varios elementos de configuración.

### 1. Ruta de fabricación
La operación subcontratada debe estar asociada a un centro de trabajo de subcontratación. En esa línea de ruta se activa el indicador de transferencia WIP.

### 2. Proveedor y ubicación de subcontratación
Cada subcontratista necesita una ubicación asociada en su ficha. La recomendación práctica es definir una ubicación separada para cada proveedor para evitar ambigüedades operativas.

### 3. Rutas de transferencia
Si se trabaja con tránsito o con configuraciones de almacén avanzadas, es especialmente recomendable definir transfer routes con código in-transit entre ubicaciones propias y externas, tanto a la ida como al retorno.

### 4. Pedido de compra de subcontratación
La creación de la orden de transferencia WIP parte del pedido de compra de subcontratación. Por tanto, el diseño del ciclo debe contemplar la relación entre orden de producción, compra subcontratada y movimientos logísticos.

### 5. Gobierno de almacén y restricciones
Hay restricciones importantes: no se admiten números de serie o lote en líneas WIP, no se generan ciertos documentos de picking o ubicación para estas líneas y algunas combinaciones de almacén requieren especial cuidado al trabajar con transferencias directas.

## Buenas prácticas

- Crear una ubicación específica por subcontratista.
- Usar rutas de transferencia con ubicación en tránsito cuando existan configuraciones avanzadas de almacén.
- Revisar que la operación subcontratada no provoque efectos no deseados al contabilizar recepciones si es la última operación del proceso.
- Definir descripciones de transferencia por operación para diferenciar etapas del producto.
- Establecer un procedimiento de conciliación periódica entre saldo WIP físico y saldo WIP registrado.
- Formar al equipo de producción, compras y logística sobre la diferencia entre transferencia estándar y transferencia WIP.
- Probar escenarios de retorno, operaciones paralelas y cierre de orden antes del arranque.

## Checklist de implantación

- [ ] Confirmar que el proceso del cliente requiere seguimiento del producto semiterminado entre terceros.
- [ ] Identificar operaciones subcontratadas en la ruta de fabricación.
- [ ] Asignar centros de trabajo de subcontratación y proveedores.
- [ ] Crear una ubicación de subcontratación por proveedor.
- [ ] Configurar transfer routes con in-transit cuando aplique.
- [ ] Activar la opción de transferencia WIP en las operaciones correspondientes.
- [ ] Validar la generación de pedidos de compra de subcontratación.
- [ ] Probar transferencias desde planta, entre subcontratistas y de retorno.
- [ ] Verificar ajustes manuales de WIP.
- [ ] Definir criterio de limpieza WIP al finalizar órdenes.

## Resumen de funcionalidades

| Funcionalidad | Beneficio | Impacto |
|---------------|------------|----------|
| Transferencia WIP desde pedido de compra subcontratado | Conecta compras, producción y logística | Reduce pasos manuales |
| Libro específico de WIP | Separa el seguimiento operativo del inventario estándar | Mejora la coherencia de costes |
| Cálculo automático de ubicaciones | Agiliza movimientos entre fases y proveedores | Menos errores operativos |
| Ajuste manual de cantidades | Permite corregir discrepancias | Mayor fiabilidad del dato |
| Limpieza WIP al cierre | Evita saldos pendientes al finalizar | Mejora el cierre de producción |
| Soporte multi-stage subcontracting | Da cobertura a procesos industriales complejos | Escalabilidad funcional |

## Conclusiones

La nueva gestión de transferencias WIP entre subcontratistas en Business Central responde a una necesidad muy concreta de los fabricantes: controlar el producto semiterminado cuando sale de la planta, sin desvirtuar su naturaleza como parte de una orden de producción.

Su valor no está solo en registrar movimientos, sino en hacerlo con una lógica funcional más precisa. Esto ayuda a alinear el mundo físico del taller, la logística externa y el control económico del proceso productivo.

Para empresas industriales, la funcionalidad aporta trazabilidad y orden. Para partners y consultores, ofrece una pieza sólida para construir soluciones de fabricación más maduras y menos dependientes de desarrollos a medida. Y para el usuario final, simplifica la operativa diaria en escenarios donde el WIP ya no puede gestionarse con simples notas o controles externos.

En definitiva, estamos ante una mejora especialmente relevante para organizaciones que trabajan con subcontratación por fases y necesitan gobernar con rigor el flujo del producto en curso.

## Referencias

Fuente original:

[https://learn.microsoft.com/en-us/dynamics365/business-central/subcontract-wip-transfers](https://learn.microsoft.com/en-us/dynamics365/business-central/subcontract-wip-transfers)
