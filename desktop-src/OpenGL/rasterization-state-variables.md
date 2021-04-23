---
title: Rasterungszustandsvariablen
description: Rasterungszustandsvariablen
ms.assetid: 57ce3dc0-3983-449a-bbe1-153232727ff8
keywords:
- Rasterungszustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Rasterization State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6210f93c23dc52f19f3e01ea01ebe8fc9d631c8c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909838"
---
# <a name="rasterization-state-variables"></a>Rasterungszustandsvariablen

<dl> <dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>\_ \_ GL-PUNKTGRÖßE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Punktgröße                         |
| Attributgruppe: | point                              |
| Anfangswert:   | 1.0                                |
| Get-Befehl:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>GL \_ POINT \_ SMOOTH</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Pointaliasing on                  |
| Attributgruppe: | point/enable                       |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>GL \_ LINE \_ WIDTH</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Linienstärke                                                                     |
| Attributgruppe: | line                                                                           |
| Anfangswert:   | 1.0                                                                            |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>GL \_ LINE \_ SMOOTH</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Line antialiasing on               |
| Attributgruppe: | line/enable                        |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>GL \_ LINE \_ STIPPLE \_ PATTERN</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Zeilenausschnitt                                                                     |
| Attributgruppe: | line                                                                             |
| Anfangswert:   | 1 s                                                                              |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>GL \_ LINE \_ STIPPLE \_ REPEAT</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Zeilenausschnitt wiederholen                                                              |
| Attributgruppe: | line                                                                             |
| Anfangswert:   | 1                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>GL \_ LINE \_ STIPPLE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Zeilentipple aktivieren                |
| Attributgruppe: | line/enable                        |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>GL \_ CULL \_ FACE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Polygon-Culling aktiviert            |
| Attributgruppe: | polygon/enable                     |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>GL \_ CULL \_ FACE \_ MODE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Cull-Polygone mit Vorder-/Rückseite                                           |
| Attributgruppe: | polygon                                                                          |
| Anfangswert:   | GL \_ BACK                                                                         |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>GL \_ FRONT \_ FACE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | CW/CCW-Indikator für Polygonfront                                              |
| Attributgruppe: | polygon                                                                          |
| Anfangswert:   | GL \_ CCW                                                                          |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>GL \_ POLYGON \_ SMOOTH</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Polygon antialiasing on            |
| Attributgruppe: | polygon/enable                     |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>\_ \_ GL-POLYGONMODUS</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Polygonrasterungsmodus (front und back)                                      |
| Attributgruppe: | polygon                                                                          |
| Anfangswert:   | GL \_ FILL                                                                         |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>GL \_ POLYGON \_ STIPPLE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Polygonstipple aktivieren             |
| Attributgruppe: | polygon/enable                     |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 



| Eigenschaft | Wert |
|------------------|----------------------------------------------------|
| Beschreibung:     | Polygonstipplemuster                            |
| Attributgruppe: | polygon-stipple                                    |
| Anfangswert:   | 1 s                                                |
| Get-Befehl:     | [**glGetPolygonStipple**](glgetpolygonstipple.md) |



 

</dd> </dl>

 

 




