# PCB_esp — Holter (Grupo 11, IEE2913)

Proyecto KiCad 10 de la placa del ESP32 (avance 90 %). Abrir `PCB_esp.kicad_pro`.

> Requiere **KiCad 10**: los archivos están guardados en formato 10 y versiones anteriores no los abren.

Las librerías propias vienen dentro del repo (`libs/`) y se cargan con `${KIPRJMOD}`
(tablas `sym-lib-table` y `fp-lib-table` del proyecto), así que no hay que configurar
nada. El ESP32-S2-WROVER usa la librería estándar `RF_Module` y su modelo 3D usa
`${KICAD10_3DMODEL_DIR}`, que KiCad 10 instala por defecto.

## Componentes

| Ref | Componente | Símbolo | Footprint |
|-----|------------|---------|-----------|
| U1 | ESP32-S2-WROVER | `RF_Module` (estándar) | `RF_Module` (estándar) |
| U2 | AD8232 (SparkFun SEN-12650) | `SEN-12650` | `SEN-12650` |
| U3 | HX711 (módulo) | `HX711_Module` | `HX711_Module` |
| U4 | Sensor de presión MPS20N0040D | `MPS20N0040D` | `MPS20N0040D` |
| U5 | OLED 0,96" DM-OLED096-636 | `DM-OLED096-636` | `DM-OLED096-636` |
| U6 | Módulo microSD mini | `MicroSD_Mini_Module` | `MicroSD_Mini_KiCad` |

## Estructura

- `libs/symbols/` símbolos propios (`.kicad_sym`)
- `libs/footprints/` footprints propios (`.pretty`)
- `libs/3d/` modelos 3D propios (el `.step` del OLED se enlaza con `${KIPRJMOD}`)
