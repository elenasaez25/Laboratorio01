# Taller práctico 03: Laboratorio: Ecosistema Odoo

**Módulo:** Lenguaje de Marcas  
**Alumno:** Elena Sáez Lascurain

---

## Fases de la actividad:

### Fase 1 — Integración de Módulos

1. Instalación de Apps Inventario y Facturación a través del menú principal:

   <img width="336" height="109" alt="image" src="https://github.com/user-attachments/assets/75ca7e76-8228-4ce0-a963-7ecc15abc02e" />
   <img width="332" height="107" alt="image" src="https://github.com/user-attachments/assets/68629e50-4a5c-4fa4-a361-3612086a86d6" />

   1.1 Observación de los Logs cuando se instalan las Apps:

   <img width="1487" height="266" alt="image" src="https://github.com/user-attachments/assets/6bc95ccc-9a5b-4b5e-a314-0c87377db9ae" />

2. Para no cargar una práctica de ERP con una base de datos vacía, implemento unos datos proporcionados por el docente.

   2.2 Estos datos los voy a guardar en un archivo llamado `clientes_mock.csv`, el cual está subido al repositorio para que se puedan consultar los datos con los que voy a estar trabajando durante esta práctica.

   <img width="682" height="286" alt="image" src="https://github.com/user-attachments/assets/05c1f05a-f3bc-4d61-8130-a6dfde3ee354" />

   2.3 Para esta práctica, sigo la recomendación de mi docente y me instalo la extensión **Rainbow CSV** de **mechatroner** ya que me permitirá:

   - i. Resaltar las columnas en archivos CSV, TSV, separados por punto y coma, y por barra vertical con colores distintos.
   - ii. Consultar, transformar y filtrar datos utilizando un lenguaje integrado similar a SQL (RBQL).
   - iii. Seguimiento mejorado de hasta 3 columnas de interés con decoraciones auxiliares.
   - iv. Alinear las columnas gráficamente o con espacios adicionales y reducir el espacio (eliminando los espacios de los campos).
   - v. Línea de encabezado fija opcional.

   2.4 Subo el archivo dentro de Ventas > Pedidos > Clientes mediante **la herramienta de importación.**

   <img width="782" height="414" alt="image" src="https://github.com/user-attachments/assets/054166ad-75bc-41ca-bd14-46e0669bf703" />
   <img width="1906" height="901" alt="image" src="https://github.com/user-attachments/assets/e6ce8b31-cc49-4ff3-a680-4d109f6830c7" />

   2.5 Presiono el botón **"Test"** para validar que el tipo de dato coincide con la base de datos. Si todo sale en azul, significa que está correcto.

   <img width="661" height="103" alt="image" src="https://github.com/user-attachments/assets/365ae619-50b2-4d94-8e46-54f1d85e3d8c" />

   Como en mi caso me sale así, lo importo:

   <img width="952" height="559" alt="image" src="https://github.com/user-attachments/assets/fee957fd-f102-4c60-8614-bf477dd09f11" />

3. Creo un producto para después crear un presupuesto para un nuevo cliente.

   <img width="1213" height="559" alt="image" src="https://github.com/user-attachments/assets/7b74bdcc-f738-4e54-a72b-bd84f9695413" />
   <img width="400" height="153" alt="image" src="https://github.com/user-attachments/assets/d5cac6c2-f27f-422e-a272-acc910c3fa83" />

   3.1 Confirmo el producto y luego creo el presupuesto:

   <img width="904" height="483" alt="image" src="https://github.com/user-attachments/assets/3045f26b-30b8-4966-81d2-fbbb6d6fff77" />

   3.2 Luego, creo una **Factura normal** a través de la opción de facturación, donde marco que la factura ya está completada y lista para empezar su trámite:

   <img width="1212" height="717" alt="image" src="https://github.com/user-attachments/assets/a43cb68e-4293-460c-bef3-8b523b591902" />

### Fase 2 — Elaboración de Informes

1. En *Ajustes > Técnico > Vistas*, localizo `sale.report_saleorder_document`, la vista que renderiza el esqueleto HTML que luego el motor *wkhtmltopdf* convierte a PDF.

   <img width="943" height="181" alt="image" src="https://github.com/user-attachments/assets/02e40f90-3298-4c96-b5f6-efd579321d37" />

   1.1 Dentro del documento, lo modifico con un código que me ha proporcionado el docente, colocándolo al final de la última etiqueta `</div>`.

   <img width="801" height="183" alt="image" src="https://github.com/user-attachments/assets/c36bf028-c0e6-40e3-94e4-9e0278dbd8f1" />

   1.2 Luego, lo guardo manualmente y no me salta ningún error:

   <img width="309" height="113" alt="image" src="https://github.com/user-attachments/assets/0bc545e3-f2ce-47cb-80d5-1c831e34123f" />

   1.3 Por último, me genera el PDF correctamente estando el CIF en rojo y el texto de protección de datos, el cual también está subido al repositorio.

### Fase 3 — Exportación de Información

1. En *Facturación > Clientes*, selecciono todos los registros:

   <img width="947" height="561" alt="image" src="https://github.com/user-attachments/assets/7f282776-a6a3-415b-be9b-2dac16e10e13" />

2. Lo exporto en formato **CSV** con campos: nombre, email, teléfono y `country_id/name`:

   <img width="290" height="87" alt="image" src="https://github.com/user-attachments/assets/346e527e-df75-4a8f-bd14-2732021913c8" />

3. Para finalizar, reviso que la codificación **UTF-8** sea correcta abriendo el archivo en VS Code:

   <img width="828" height="584" alt="image" src="https://github.com/user-attachments/assets/b3cbeeb2-acc6-4539-9a48-448bdf03b213" />
   <img width="983" height="292" alt="image" src="https://github.com/user-attachments/assets/2c6851b1-ec2b-4abc-8bb7-d67d5cdb1b45" />

---
