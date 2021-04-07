---
title: Rasterization-Zustandsvariablen
description: Rasterization-Zustandsvariablen
ms.assetid: 57ce3dc0-3983-449a-bbe1-153232727ff8
keywords:
- Rasterization-Zustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Rasterization State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1667c530ea1db8c9e463be0edad5de98e8b107
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718498"
---
# <a name="rasterization-state-variables"></a>Rasterization-Zustandsvariablen

<dl> <dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>GL- \_ Punkt \_ Größe</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Punktgröße                         |
| Attribut Gruppe: | point                              |
| Anfangswert:   | 1.0                                |
| Get-Befehl:     | [**glgetfloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>GL- \_ Punkt \_ glatt</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Punkt Aliasing am                  |
| Attribut Gruppe: | Punkt/Aktivierung                       |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>GL- \_ Linien \_ Breite</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Linienstärke                                                                     |
| Attribut Gruppe: | line                                                                           |
| Anfangswert:   | 1.0                                                                            |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>GL- \_ Linie \_ glatt</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Zeilen-Antialiasing am               |
| Attribut Gruppe: | Zeile/Aktivierung                        |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>GL- \_ Linien \_ stippingmuster \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Zeilen Stippel                                                                     |
| Attribut Gruppe: | line                                                                             |
| Anfangswert:   | 1                                                                              |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>GL- \_ Zeilen \_ Stippel \_ Wiederholen</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Zeilen Stippel wiederholen                                                              |
| Attribut Gruppe: | line                                                                             |
| Anfangswert:   | 1                                                                                |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>GL- \_ Zeilen \_ Stippel</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Zeilen Stippel aktivieren                |
| Attribut Gruppe: | Zeile/Aktivierung                        |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>GL. Ober \_ \_ Fläche</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Polygon-cullinger aktiviert            |
| Attribut Gruppe: | Polygon/aktivieren                     |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>GL- \_ cull- \_ Gesichts \_ Modus</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Nach-oben-und rückwärts gerichtete Polygone                                           |
| Attribut Gruppe: | polygon                                                                          |
| Anfangswert:   | GL \_ zurück                                                                         |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>GL- \_ Vorderseite \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Polygon-Front-Face-CW/CCW-Indikator                                              |
| Attribut Gruppe: | polygon                                                                          |
| Anfangswert:   | GL- \_ CCW                                                                          |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>GL- \_ Polygon \_ glatt</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Polygon-Antialiasing am            |
| Attribut Gruppe: | Polygon/aktivieren                     |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>GL- \_ Polygon- \_ Modus</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Polygon-rasterisierungsmodus (vor und hinten)                                      |
| Attribut Gruppe: | polygon                                                                          |
| Anfangswert:   | Ausfüllen von GL \_                                                                         |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>GL- \_ Polygon- \_ Stippel</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Polygon-Stippel aktivieren             |
| Attribut Gruppe: | Polygon/aktivieren                     |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 



|                  |                                                    |
|------------------|----------------------------------------------------|
| Beschreibung:     | Polygon stippingmuster                            |
| Attribut Gruppe: | Polygon-Stippel                                    |
| Anfangswert:   | 1                                                |
| Get-Befehl:     | [**glgetpolygonstippel**](glgetpolygonstipple.md) |



 

</dd> </dl>

 

 




