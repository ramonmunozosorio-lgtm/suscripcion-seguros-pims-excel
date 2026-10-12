# 🛡️ Sistema de Cuadratura y Auditoría de Suscripción Masiva (PIMS)

## 📌 Descripción del Proyecto
Proyecto de desarrollo de un modelo operativo automatizado en Excel avanzado para la recepción, validación y control de calidad de solicitudes de seguros masivos. Diseñado para mitigar riesgos operativos de socios comerciales externos (retail y call centers) antes de la inyección en el core de sistemas PIMS.

## ⚙️ Arquitectura y Controles Defensivos (3 Capas)
1. **Integridad y Completitud:** Validación previa de campos obligatorios y formato de fechas (`DATEDIF`).
2. **Identidad y Normativa Chilena:** Motor de validación de Cédula de Identidad mediante algoritmo **Módulo 11**, detectando anomalías, falta de guiones o dígitos verificadores erróneos.
3. **Elegibilidad y Tarificación Financiera:** Cruce dinámico contra el Catálogo Oficial de Planes (rangos etarios permitidos de 18 a 65 años) y control de cuadratura de primas (`RECHAZADO_DESCALCE_PRIMA`).

## 📊 Estructura del Libro Máster (`Laboratorio_Suscripcion_Seguros_PIMS_v2.xlsx`)
- **`Base_Altas_Recibidas`:** Matriz transaccional con motor de validación en cascada y numeración de rechazos por índice.
- **`Catalogo_Planes_PIMS`:** Arancel oficial, límites de edad y coberturas de referencia.
- **`Dashboard_Cuadratura_Diaria`:** KPIs ejecutivos, tasas de efectividad, prima suscrita y desglose analítico por canal.
- **`Auditoria_Rechazos_PIMS`:** Reporte dinámico de excepciones y tarjetas de control con validación de balance cero (`CUADRA OK`).
- **`Pruebas_Control`:** Plan de pruebas UAT (User Acceptance Testing) con escenarios de validación de reglas de negocio.

## 🚀 Cómo utilizar este repositorio
1. Descarga el archivo `Laboratorio_Suscripcion_Seguros_PIMS_v2.xlsx`.
2. Reemplaza los datos en la pestaña `Base_Altas_Recibidas` (desde la fila 5 hacia abajo en las columnas A–I) con tu lote de solicitudes diarias.
3. El motor de validación y el dashboard se actualizarán automáticamente.

---
*Autor: Ramón Muñoz Osorio | Analista de Datos y Operaciones*
