# Agrupar varios envíos en una única factura en Business Central: menos fricción, más control y mejor experiencia de cliente

En muchas empresas, la facturación no sigue una secuencia simple y lineal. Un pedido puede entregarse en varias expediciones por disponibilidad de stock, calendario logístico o acuerdos con el cliente. Cuando eso sucede, emitir una factura por cada envío suele traducirse en más carga administrativa, más documentos por revisar y una experiencia menos fluida para el cliente.

Aquí es donde Microsoft Dynamics 365 Business Central ofrece una capacidad muy útil: **agrupar varios envíos en una única factura**. La funcionalidad está pensada para consolidar envíos ya contabilizados, manual o automáticamente, siempre que cumplan unas condiciones concretas. Bien aplicada, puede aportar eficiencia, mejorar el control documental y simplificar el proceso financiero.

## Qué resuelve esta funcionalidad

La documentación oficial de Microsoft Learn indica que Business Central permite agrupar envíos de pedidos de venta o de servicio en una sola factura. La condición base es clara: deben existir varios envíos ya contabilizados pero no facturados, correspondientes al mismo cliente y en la misma divisa.

Esto responde a un problema operativo muy habitual. Cuando la entrega de mercancía o la prestación de un servicio se hace en varios hitos, es frecuente que el área administrativa termine gestionando un exceso de documentos. La consolidación permite transformar varias expediciones en una sola factura final, manteniendo la coherencia del proceso.

## Dos formas de hacerlo

### 1) Proceso manual

En el modo manual, el usuario crea una nueva factura de venta y utiliza la acción **Obtener líneas de envío** para incorporar las expediciones que quiere incluir. Esta opción es interesante cuando se necesita revisar con detalle qué líneas van a formar parte de la factura o cuando la casuística del cliente requiere control individual.

Es un enfoque muy útil para cuentas estratégicas, escenarios con validación previa o procesos en los que el equipo de administración quiere decidir exactamente cuándo consolidar y qué incluir.

### 2) Proceso automático

Business Central también permite automatizar el proceso mediante la tarea por lotes **Combinar envíos**. Según la documentación, el sistema toma únicamente aquellos pedidos de venta donde se haya elegido la opción de combinar envíos. Además, puede registrar las facturas automáticamente si se marca la casilla correspondiente.

Este modelo resulta especialmente atractivo cuando el volumen de expediciones es elevado y el patrón de facturación es repetitivo. En otras palabras: menos clics, menos trabajo manual y más escalabilidad.

## Un matiz importante: cliente de envío y cliente de facturación

Uno de los puntos más interesantes del artículo oficial es la observación sobre el **cliente de envío** y el **cliente de facturación**. Si ambos son distintos, algunas líneas pueden no aparecer inicialmente en el proceso de recuperación de envíos. Microsoft explica que en esos casos puede ser necesario personalizar la página para mostrar el campo adecuado y eliminar el filtro que las oculta.

Es un detalle funcional importante, porque refleja algo muy real en implantaciones B2B: no siempre quien recibe la mercancía es quien recibe la factura. Tener esto controlado evita incidencias y consultas posteriores.

## Qué pasa al contabilizar la factura combinada

Cuando se registra la factura consolidada, Business Central crea la factura contabilizada para las líneas incluidas y actualiza la cantidad facturada del pedido original. Sin embargo, los pedidos pueden seguir existiendo como documentos abiertos incluso si ya están completamente enviados y facturados.

Por eso, la propia documentación menciona la acción **Eliminar pedidos de ventas facturados** como mecanismo para limpiar esos documentos cuando corresponda. Este punto es muy relevante desde la gobernanza operativa: consolidar facturas también debe ir acompañado de una buena higiene documental.

## Beneficio de negocio: mucho más que emitir menos facturas

Aunque el procedimiento técnico es relativamente sencillo, el valor de negocio es considerable:

- Reduce la carga administrativa del equipo de facturación.
- Simplifica la revisión de documentos por parte del cliente.
- Mejora la trazabilidad entre expedición, pedido y factura.
- Ayuda a disminuir errores por duplicidad o dispersión documental.
- Refuerza una experiencia de cliente más ordenada y profesional.

Además, Microsoft Learn incluye esta materia en su módulo de facturación a clientes, donde se contempla tanto la facturación manual de múltiples envíos como la combinación para varios clientes al mismo tiempo. Esto confirma que no estamos ante un truco aislado, sino ante una práctica funcional relevante dentro del estándar de Business Central.

## Cuándo conviene implantarlo

Esta funcionalidad suele encajar muy bien en empresas con:

- Entregas parciales por disponibilidad de stock.
- Expediciones recurrentes al mismo cliente.
- Necesidad de facturación periódica consolidada.
- Operaciones donde logística y administración trabajan en tiempos distintos.
- Objetivo claro de reducir volumen documental sin perder trazabilidad.

## Mi recomendación

Si trabajas con Business Central y tu empresa gestiona varios envíos por cliente antes de facturar, esta capacidad merece una revisión prioritaria. No requiere reinventar el proceso: aprovecha el estándar, mejora la operativa y ofrece una base sólida para evolucionar hacia automatización real.

Y, como ocurre con muchas funciones “pequeñas” del ERP, su impacto no está en la complejidad técnica, sino en el ahorro acumulado y en la calidad del proceso diario.

---

**Referencia oficial:** [Procedimiento: Agrupamiento de envíos en una factura única - Business Central](https://learn.microsoft.com/es-es/dynamics365/business-central/sales-how-to-combine-shipments-on-a-single-invoice)
