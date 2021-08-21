---
title: Statusvariablen für Texturen
description: Statusvariablen für Texturen
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Texturieren von Zustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7393fc6e700b028ba3783e5c78d8175e0c3fba4937bf3830d5cae8897aa0d4db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776580"
---
# <a name="texturing-state-variables"></a>Statusvariablen für Texturen

<dl> <dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL \_ TEXTURE \_ *x*</dt> <dd> 

| Eigenschaft | Wert |
|------------------|-------------------------------------------------------|
| Beschreibung:     | True, wenn *x* – D Texturing aktiviert ist (*x* ist 1-D oder 2D) |
| Attributgruppe: | textur/enable                                        |
| Anfangswert:   | GL \_ FALSE                                             |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md)                    |



 

</dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL \_ TEXTURE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------|
| Beschreibung:     | *x* – D Texturbild auf Detailebene *i* |
| Attributgruppe: |                                              |
| Anfangswert:   |                                              |
| Get-Befehl:     | [**glGetTexImage**](glgetteximage.md)       |



 

</dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL \_ \_ TEXTURBREITE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------|
| Beschreibung:     | *x* – D Texturbild *i* es width                       |
| Attributgruppe: |                                                          |
| Anfangswert:   | 0                                                        |
| Get-Befehl:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL \_ \_ TEXTURHÖHE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------|
| Beschreibung:     | *x* – D Texturbild *i* es height                      |
| Attributgruppe: |                                                          |
| Anfangswert:   | 0                                                        |
| Get-Befehl:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL \_ TEXTURE \_ BORDER</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------|
| Beschreibung:     | *x* – D Texturbild *i* es border                      |
| Attributgruppe: |                                                          |
| Anfangswert:   | 0                                                        |
| Get-Befehl:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>\_ \_ GL-TEXTURKOMPONENTEN</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------|
| Beschreibung:     | Texturbildkomponenten                                 |
| Attributgruppe: |                                                          |
| Anfangswert:   | 1                                                        |
| Get-Befehl:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL \_ TEXTURE \_ BORDER \_ COLOR</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------------------|
| Beschreibung:     | Textur-Rahmenfarbe                           |
| Attributgruppe: | Struktur                                        |
| Anfangswert:   | 0, 0, 0, 0                                     |
| Get-Befehl:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL \_ TEXTURE \_ MIN \_ FILTER</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------------------|
| Beschreibung:     | Texturvergrößerungsfunktion                  |
| Attributgruppe: | Struktur                                        |
| Anfangswert:   | GL \_ NEAREST \_ MIPMAP \_ LINEAR                    |
| Get-Befehl:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL \_ TEXTURE \_ MAG \_ FILTER</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------------------|
| Beschreibung:     | Texturvergrößerungsfunktion                 |
| Attributgruppe: | Struktur                                        |
| Anfangswert:   | GL \_ LINEAR                                     |
| Get-Befehl:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL \_ TEXTURE \_ WRAP \_ *x*</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------------------|
| Beschreibung:     | Texturumbruchmodus (*x* ist S oder T)              |
| Attributgruppe: | Struktur                                        |
| Anfangswert:   | GL \_ REPEAT                                     |
| Get-Befehl:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL \_ TEXTURE \_ ENV \_ MODE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------|
| Beschreibung:     | Texturanwendungsfunktion         |
| Attributgruppe: | Struktur                              |
| Anfangswert:   | GL \_ MODULATE                         |
| Get-Befehl:     | [**glGetTexEnviv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL \_ TEXTURE \_ ENV \_ COLOR</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------|
| Beschreibung:     | Farbe der Texturumgebung            |
| Attributgruppe: | Struktur                              |
| Anfangswert:   | 0, 0, 0, 0                           |
| Get-Befehl:     | [**glGetTexEnvfv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL \_ TEXTURE \_ GEN \_ *x*</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------------|
| Beschreibung:     | Texgen ist aktiviert (*x* ist S, T, R oder Q) |
| Attributgruppe: | textur/enable                           |
| Anfangswert:   | GL \_ FALSE                                |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md)       |



 

</dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL \_ EYE \_ PLANE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------|
| Beschreibung:     | Koeffizienten der Texgenebenengleichung   |
| Attributgruppe: | Struktur                              |
| Anfangswert:   |                                      |
| Get-Befehl:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>\_ \_ GL-OBJEKTEBENE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------|
| Beschreibung:     | Lineare Koeffizienten des Texgen-Objekts    |
| Attributgruppe: | Struktur                              |
| Anfangswert:   |                                      |
| Get-Befehl:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL \_ TEXTURE \_ GEN \_ MODE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------|
| Beschreibung:     | Für Texgen verwendete Funktion             |
| Attributgruppe: | Struktur                              |
| Anfangswert:   | GL \_ EYE \_ LINEAR                      |
| Get-Befehl:     | [**glGetTexGeniv**](glgettexgen.md) |



 

</dd> </dl>

 

 




