# Taller práctico 03: Laboratorio: Ecosistema Odoo

**Módulo:** Lenguaje de Marcas
**Alumno:** Elena Sáez Lascurain
---
## Fases de la actividad:

### Fase 1 — Integración de Módulos
1. Instalar módulos de **Inventario** y **Facturación** desde Apps.
2. Importar clientes desde el archivo `clientes_mock.csv` a través de *Ventas > Clientes > Importar registros*.
3. Completar el ciclo de negocio completo: **Presupuesto → Pedido → Albarán → Factura**.

### Fase 2 — Elaboración de Informes (QWeb)
1. En *Ajustes > Técnico > Vistas*, localizar `sale.report_saleorder_document`.
2. Inyectar bloque HTML/CSS con aviso legal y texto RGPD al final del documento.
3. Validar que el PDF generado muestra el CIF en rojo y el texto de protección de datos.

### Fase 3 — Exportación de Información
1. En *Facturación > Clientes*, seleccionar todos los registros.
2. Exportar en formato **CSV** con campos: nombre, email, teléfono y `country_id/name`.
3. Verificar codificación **UTF-8** abriendo el archivo en VS Code.

---

## Archivos del proyecto

| Archivo | Descripción |
|---|---|
| `clientes_mock.csv` | Datos sintéticos de 10 clientes españoles |
| `Contacto (res.partner).csv` | Exportación final de clientes desde Odoo |

---
