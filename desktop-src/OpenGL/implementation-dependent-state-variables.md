---
title: Implementation-Dependent Statusvariablen
description: Implementation-Dependent Statusvariablen
ms.assetid: 6778b50c-a6ac-4106-9dd6-3a123c257687
keywords:
- Implementation-Dependent Zustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Implementation-Dependent State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb42c13765678218efcaf58f2b02a01d2f0e160
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038004"
---
# <a name="implementation-dependent-state-variables"></a>Implementation-Dependent Statusvariablen

<dl> <dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>maximale GL- \_ \_ Beleuchtung</dt> <dd> 

|                  |                                        |
|------------------|----------------------------------------|
| Beschreibung:     | Maximale Anzahl von Lichtern               |
| Attribut Gruppe: |                                        |
| Anfangswert:   | 8                                      |
| Get-Befehl:     | [**glgetintegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>Max. Ausschneide Flächen für GL \_ \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Anzahl von Benutzer Clippingebenen                                           |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 6                                                                                |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>\_Max. maximale \_ Modelview- \_ Stapel \_ Tiefe</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Länge von Modelview-Matrix Stapeln                                             |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 32                                                                               |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>\_Maximale maximale \_ Projektions \_ Stapel \_ Tiefe von GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Projektion-Matrix Stapel Tiefe                                            |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 2                                                                                |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>\_Maximale maximale \_ Textur \_ Stapel \_ Tiefe von GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Tiefe des Textur Matrix Stapels                                            |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 2                                                                                |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>GL- \_ \_ subpixelbits</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Anzahl der Bits der unter Pixelgenauigkeit in *x*   und *y*                              |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 4                                                                                |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>\_Maximale maximale \_ Textur \_ Größe von GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Höhe oder Breite eines Textur Bilds (ohne Rahmen)                     |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 64                                                                               |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>GL. \_ Maximale \_ Pixel Map- \_ \_ Tabelle</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Größe einer **glpixelmap** -Übersetzungstabelle                               |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 32                                                                               |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>\_Maximale \_ Namen \_ Stapel \_ Tiefe von GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Stapel Tiefe für Auswahl Name                                               |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 64                                                                               |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>maximal zulässige Schachtelungs \_ \_ Liste \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Schachtelungs Schachtelungs Schachtelung                                                |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 64                                                                               |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>\_Maximale \_ eval- \_ Reihenfolge von GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale auswerlungs-Polynoms-Reihenfolge                                               |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 8                                                                                |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>maximale Anzahl von GL. \_ \_ \_ viewportdims</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale viewportdimensionen                                                      |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   |                                                                                  |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>\_Max. maximale \_ attrb- \_ Stapel \_ Tiefe</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Maximale Tiefe des Attribut Stapels                                             |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 16                                                                               |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>GL. \_ aux- \_ Puffer</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Anzahl der zusätzlichen Puffer                                                      |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 0                                                                                |
| Get-Befehl:     | [**glgetbooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>GL \_ RGBA- \_ Modus</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | True, wenn die Farb Puffer den RGBA speichern                                                 |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   |                                                                                  |
| Get-Befehl:     | [**glgetbooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>GL- \_ Index \_ Modus</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | True, wenn Farb Puffer Indizes speichern                                              |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   |                                                                                  |
| Get-Befehl:     | [**glgetbooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>GL \_ Double Buffer</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | True, wenn Vorder-und Hintergrund Puffer vorhanden sind.                                             |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   |                                                                                  |
| Get-Befehl:     | [**glgetbooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>GL- \_ Stereo</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | True, wenn der linke und der Rechte Puffer vorhanden sind.                                           |
| Attribut Gruppe: |                                                                                |
| Anfangswert:   |                                                                                |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>Bereich für GL- \_ Punkt \_ Größe \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Bereich (niedrig bis hoch) der Punktgrößen mit Antialiasing                                 |
| Attribut Gruppe: |                                                                                |
| Anfangswert:   | 1, 1                                                                           |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>Größe der GL- \_ \_ Punktgröße \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Granularität der Größe von Antialiasing Punkten                                             |
| Attribut Gruppe: |                                                                                |
| Anfangswert:   |                                                                                |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>Bereich für GL- \_ Linien \_ Breite \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Bereich (niedrig bis hoch) der Zeilen Breiten mit Antialiasing                                 |
| Attribut Gruppe: |                                                                                |
| Anfangswert:   | 1, 1                                                                           |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>Granularität der GL- \_ Linien \_ Breite \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Granularität der Zeilenbreite mit Antialiasing                                             |
| Attribut Gruppe: |                                                                                |
| Anfangswert:   |                                                                                |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




