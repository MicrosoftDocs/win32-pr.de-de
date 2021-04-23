---
title: Transformationszustandsvariablen
description: Transformationszustandsvariablen
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
ms.openlocfilehash: 8c7b53e0abae08447df86d8968a33a361be08a1e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908828"
---
# <a name="transformation-state-variables"></a>Transformationszustandsvariablen

<dl> <dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL \_ MODELVIEW \_ MATRIX</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Modellansichtsmatrixstapel             |
| Attributgruppe: |                                    |
| Anfangswert:   | Identity                           |
| Get-Befehl:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>\_GL-PROJEKTIONSMATRIX \_</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Projektionsmatrixstapel                                                        |
| Attributgruppe: |                                                                                |
| Anfangswert:   | Identity                                                                       |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL \_ TEXTURE \_ MATRIX</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Texturmatrixstapel                                                           |
| Attributgruppe: |                                                                                |
| Anfangswert:   | Identity                                                                       |
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
| Beschreibung:     | Modellansichtsmatrixstapelzeiger                                                   |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 1                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>\_ \_ GL-PROJEKTIONSSTAPELTIEFE \_</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Projektionsmatrixstapelzeiger                                                  |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 1                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL \_ TEXTURE \_ STACK \_ DEPTH</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Texturmatrixstapelzeiger                                                     |
| Attributgruppe: |                                                                                  |
| Anfangswert:   | 1                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL \_ \_ MATRIX-MODUS</dt> <dd> 

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

 

 




