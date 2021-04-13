---
title: Transformations Zustandsvariablen
description: Transformations Zustandsvariablen
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- Transformations Zustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3434fe9f9aa528aa8d201b56ed363753c594690f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312737"
---
# <a name="transformation-state-variables"></a>Transformations Zustandsvariablen

<dl> <dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL- \_ Modelview- \_ Matrix</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Modelview-Matrix Stapel             |
| Attribut Gruppe: |                                    |
| Anfangswert:   | Identity                           |
| Get-Befehl:     | [**glgetfloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL- \_ Projektions \_ Matrix</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Projektions Matrix Stapel                                                        |
| Attribut Gruppe: |                                                                                |
| Anfangswert:   | Identity                                                                       |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL- \_ Textur \_ Matrix</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Textur Matrix Stapel                                                           |
| Attribut Gruppe: |                                                                                |
| Anfangswert:   | Identity                                                                       |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL- \_ Viewport</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Ursprung und Block des Viewports                                                       |
| Attribut Gruppe: | Viewport                                                                         |
| Anfangswert:   |                                                                                  |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL- \_ tiefen \_ Bereich</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Tiefenbereich nah und weit                                                       |
| Attribut Gruppe: | Viewport                                                                       |
| Anfangswert:   | 0, 1                                                                           |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>\_ \_ Stapel Tiefe von GL Modelview \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Modelview-Matrix Stapelzeiger                                                   |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 1                                                                                |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>\_ \_ Stapel \_ Tiefe der GL-Projektion</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Projektions Matrix Stapelzeiger                                                  |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 1                                                                                |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL- \_ Textur \_ Stapel \_ Tiefe</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Textur Matrix-Stapelzeiger                                                     |
| Attribut Gruppe: |                                                                                  |
| Anfangswert:   | 1                                                                                |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL- \_ Matrix \_ Modus</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Aktueller Matrix Modus                                                              |
| Attribut Gruppe: | Transformieren                                                                        |
| Anfangswert:   | GL \_ Modelview                                                                    |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL \_ normalize</dt> <dd> 

|                  |                                     |
|------------------|-------------------------------------|
| Beschreibung:     | Aktuelle normale Normalisierung ein/aus |
| Attribut Gruppe: | Transformieren/aktivieren                    |
| Anfangswert:   | GL \_ false                           |
| Get-Befehl:     | [**glisenabled**](glisenabled.md)  |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ - \_ clippinbene *i*</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Beschreibung:     | Benutzer Clipping-Ebenen Koeffizienten         |
| Attribut Gruppe: | Transformieren                                |
| Anfangswert:   | 0, 0, 0, 0                               |
| Get-Befehl:     | [**glgetclipplane**](glgetclipplane.md) |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ - \_ clippinbene *i*</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | *i* . Benutzer Clippingebene aktiviert |
| Attribut Gruppe: | Transformieren/aktivieren                   |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> </dl>

 

 




