---
title: Statusvariablen für aktuelle Werte und zugeordnete Daten
description: Statusvariablen für aktuelle Werte und zugeordnete Daten
ms.assetid: 8e47b119-a065-43c5-b7f5-76deaf975ad8
keywords:
- Zustandsvariablen für aktuelle Werte und zugeordnete Daten OpenGL
topic_type:
- apiref
api_name:
- State Variables for Current Values and Associated Data
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d99a9504a673d23d6923d5faf0e99770f20fe55e1cdd6b63d9adcbe68282584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553710"
---
# <a name="state-variables-for-current-values-and-associated-data"></a>Statusvariablen für aktuelle Werte und zugeordnete Daten

<dl> <dt><span id="GL_CURRENT_COLOR"></span><span id="gl_current_color"></span>GL \_ CURRENT \_ COLOR</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------------------------------------------|
| Beschreibung:     | Aktuelle Farbe                                                                                                        |
| Attributgruppe: | Aktuell                                                                                                              |
| Anfangswert:   | 1, 1, 1, 1                                                                                                           |
| Get-Befehl:     | [**glGetIntegerv**](glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_INDEX"></span><span id="gl_current_index"></span>GL \_ CURRENT \_ INDEX</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung:     | Aktueller Farbindex                                                                                                                                            |
| Attributgruppe: | Aktuell                                                                                                                                                        |
| Anfangswert:   | 1                                                                                                                                                              |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_TEXTURE_COORDS"></span><span id="gl_current_texture_coords"></span>GL \_ CURRENT \_ TEXTURE \_ COORDS</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Aktuelle Texturkoordinaten                                                    |
| Attributgruppe: | Aktuell                                                                        |
| Anfangswert:   | 0, 0, 0, 1                                                                     |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_NORMAL"></span><span id="gl_current_normal"></span>GL \_ CURRENT \_ NORMAL</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Aktuelle Normalität                                                                 |
| Attributgruppe: | Aktuell                                                                        |
| Anfangswert:   | 0, 0, 1                                                                        |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION"></span><span id="gl_current_raster_position"></span>GL \_ AKTUELLE \_ RASTERPOSITION</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Aktuelle Rasterposition                                                        |
| Attributgruppe: | Aktuell                                                                        |
| Anfangswert:   | 0, 0, 0, 1                                                                     |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_DISTANCE"></span><span id="gl_current_raster_distance"></span>GL \_ AKTUELLER \_ \_ RASTERABSTAND</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Aktueller Rasterabstand                                                        |
| Attributgruppe: | Aktuell                                                                        |
| Anfangswert:   | 0                                                                              |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_COLOR"></span><span id="gl_current_raster_color"></span>GL \_ AKTUELLE \_ \_ RASTERFARBE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung:     | Der Rasterposition zugeordnete Farbe                                                                                                                          |
| Attributgruppe: | Aktuell                                                                                                                                                        |
| Anfangswert:   | 1, 1, 1, 1                                                                                                                                                     |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_INDEX"></span><span id="gl_current_raster_index"></span>GL \_ AKTUELLER \_ \_ RASTERINDEX</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung:     | Farbindex, der der Rasterposition zugeordnet ist                                                                                                                    |
| Attributgruppe: | Aktuell                                                                                                                                                        |
| Anfangswert:   | 1                                                                                                                                                              |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_TEXTURE_COORDS"></span><span id="gl_current_raster_texture_coords"></span>GL \_ CURRENT \_ RASTER \_ TEXTURE \_ COORDS</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Texturkoordinaten, die der Rasterposition zugeordnet sind                            |
| Attributgruppe: | Aktuell                                                                        |
| Anfangswert:   | 0, 0, 0, 1                                                                     |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION_VALID"></span><span id="gl_current_raster_position_valid"></span>GL \_ AKTUELLE \_ \_ RASTERPOSITION \_ GÜLTIG</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Gültiges Bit für Rasterposition                                                        |
| Attributgruppe: | Aktuell                                                                          |
| Anfangswert:   | GL \_ TRUE                                                                         |
| Get-Befehl:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_EDGE_FLAG"></span><span id="gl_edge_flag"></span>GL \_ \_ EDGE-FLAG</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Edgeflag                                                                        |
| Attributgruppe: | Aktuell                                                                          |
| Anfangswert:   | GL \_ TRUE                                                                         |
| Get-Befehl:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




