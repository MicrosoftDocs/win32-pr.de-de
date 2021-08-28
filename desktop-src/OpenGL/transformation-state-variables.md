---
title: Statusvariablen für Transformationen
description: Statusvariablen für Transformationen
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- Transformationszustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c79b4363419d97a64184dd2408a9f6221ada52adc49adbb28eb3d049a4b2a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011918"
---
# <a name="transformation-state-variables"></a>Statusvariablen für Transformationen

<dl> <dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL \_ MODELVIEW \_ MATRIX</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Modelview-Matrixstapel             |
| Attributgruppe: |                                    |
| Anfangswert:   | Identität                           |
| Get-Befehl:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>\_GL-PROJEKTIONSMATRIX \_</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Projektionsmatrixstapel                                                        |
| Attributgruppe: |                                                                                |
| Anfangswert:   | Identität                                                                       |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL \_ TEXTURE \_ MATRIX</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Texturmatrixstapel                                                           |
| Attributgruppe: |                                                                                |
| Anfangswert:   | Identität                                                                       |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL \_ VIEWPORT</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Viewport-Ursprung und -Umfang                                                       |
| Attributgruppe: | Viewport                                                                         |
| Anfangswert:   |                                                                                  |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL \_ DEPTH \_ RANGE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Tiefenbereich nah und fern                                                       |
| Attributgruppe: | Viewport                                                                       |
| Anfangswert:   | 0, 1                                                                           |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL \_ MODELVIEW \_ STACK \_ DEPTH</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Modelview-Matrixstapelzeiger                                                   |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 1                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL \_ \_ PROJEKTIONSSTAPELTIEFE \_</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Projektionsmatrixstapelzeiger                                                  |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 1                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL \_ \_ TEXTURSTAPELTIEFE \_</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Texturmatrixstapelzeiger                                                     |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 1                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>\_ \_ GL-MATRIXMODUS</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Aktueller Matrixmodus                                                              |
| Attributgruppe: | Transformieren                                                                        |
| Anfangswert:   | GL \_ MODELVIEW                                                                    |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL \_ NORMALIZE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|-------------------------------------|
| Beschreibung:     | Aktuelle Normalisierung ein/aus |
| Attributgruppe: | Transformieren/Aktivieren                    |
| Anfangswert:   | GL \_ FALSE                           |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md)  |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ CLIP \_ PLANE *i*</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------------|
| Beschreibung:     | Koeffizienten der Benutzerausschneideebene         |
| Attributgruppe: | Transformieren                                |
| Anfangswert:   | 0, 0, 0, 0                               |
| Get-Befehl:     | [**glGetClipPlane**](glgetclipplane.md) |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ CLIP \_ PLANE *i*</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | *i* th user clipping plane enabled (Beschneidungsebene des Benutzers aktiviert) |
| Attributgruppe: | Transformieren/Aktivieren                   |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> </dl>

 

 




