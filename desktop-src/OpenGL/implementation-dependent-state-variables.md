---
title: Implementierungsabhängige Statusvariablen
description: Implementierungsabhängige Statusvariablen
ms.assetid: 6778b50c-a6ac-4106-9dd6-3a123c257687
keywords:
- Implementation-Dependent State Variables OpenGL
topic_type:
- apiref
api_name:
- Implementation-Dependent State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da38f841408bd6ddf481473837f36544d21d896f2764317957c65158be27fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061458"
---
# <a name="implementation-dependent-state-variables"></a>Implementierungsabhängige Statusvariablen

<dl> <dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>GL \_ MAX \_ LIGHTS</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------|
| Beschreibung:     | Maximale Anzahl von Beleuchtungen               |
| Attributgruppe: |                                        |
| Anfangswert:   | 8                                      |
| Get-Befehl:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>GL \_ MAX \_ CLIP \_ PLANES</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Anzahl von Benutzer-Clippingebenen                                           |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 6                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>GL \_ MAX \_ MODELVIEW \_ STACK \_ DEPTH</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Modellansichtsmatrixstapeltiefe                                             |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 32                                                                               |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>GL \_ MAX \_ \_ PROJEKTIONSSTAPELTIEFE \_</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Projektionsmatrixstapeltiefe                                            |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 2                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>GL \_ \_ MAX. \_ TEXTURSTAPELTIEFE \_</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Tiefe des Texturmatrixstapels                                            |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 2                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>\_GL-SUBPIXELBITS \_</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Anzahl der Bits mit Subpixelgenauigkeit in *x* und *y*                              |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 4                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>GL \_ \_ MAX. \_ TEXTURGRÖßE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Höhe oder Breite eines Texturbilds (ohne Rahmen)                     |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 64                                                                               |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>GL \_ MAX \_ PIXEL \_ MAP \_ TABLE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Größe einer **glPixelMap-Übersetzungstabelle**                               |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 32                                                                               |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>GL \_ MAX \_ NAME \_ STACK \_ DEPTH</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Stapeltiefe für Auswahlname                                               |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 64                                                                               |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>GL \_ MAX \_ LIST \_ NESTING</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Schachtelung von Anzeigelistenaufrufen                                                |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 64                                                                               |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>GL \_ MAX \_ EVAL \_ ORDER</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale polynomiale Reihenfolge der Auswertung                                               |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 8                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>GL \_ MAX \_ VIEWPORT \_ DIMS</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Viewportdimensionen                                                      |
| Attributgruppe: |                                                                                  |
| Anfangswert:   |                                                                                  |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>GL \_ MAX \_ ATTRIB \_ STACK \_ DEPTH</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Tiefe des Attributstapels                                             |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 16                                                                               |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>GL \_ \_ AUX-PUFFER</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Anzahl der Hilfspuffer                                                      |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 0                                                                                |
| Get-Befehl:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>GL \_ \_ RGBA-MODUS</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | True, wenn Farbpuffer RGBA speichern                                                 |
| Attributgruppe: |                                                                                  |
| Anfangswert:   |                                                                                  |
| Get-Befehl:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>GL \_ \_ INDEX-MODUS</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | True, wenn Farbpuffer Indizes speichern                                              |
| Attributgruppe: |                                                                                  |
| Anfangswert:   |                                                                                  |
| Get-Befehl:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>GL \_ DOUBLEBUFFER</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | TRUE, wenn Front- und Back-Puffer vorhanden sind                                             |
| Attributgruppe: |                                                                                  |
| Anfangswert:   |                                                                                  |
| Get-Befehl:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>GL \_ STEREO</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | TRUE, wenn linke und rechte Puffer vorhanden sind                                           |
| Attributgruppe: |                                                                                |
| Anfangswert:   |                                                                                |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>GL \_ POINT \_ SIZE \_ RANGE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Bereich (niedrig bis hoch) von Antialiasingpunktgrößen                                 |
| Attributgruppe: |                                                                                |
| Anfangswert:   | 1, 1                                                                           |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>GRANULARITÄT \_ DER \_ \_ GL-PUNKTGRÖßE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Granularität der Punktgröße mit Antialiasing                                             |
| Attributgruppe: |                                                                                |
| Anfangswert:   |                                                                                |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>GL \_ LINE \_ WIDTH \_ RANGE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Bereich (niedrig bis hoch) von Geradlinienbreiten mit Antialiasing                                 |
| Attributgruppe: |                                                                                |
| Anfangswert:   | 1, 1                                                                           |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>GL \_ \_ \_ LINIENBREITENGRANULARITÄT</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Granularität mit Gealiasenbreite                                             |
| Attributgruppe: |                                                                                |
| Anfangswert:   |                                                                                |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




