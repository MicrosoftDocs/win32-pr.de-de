---
title: Texturierungsstatusvariablen
description: Texturierungsstatusvariablen
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Texturing-Zustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a9894e9f3723cca957fdeeb2882ede8f689ee7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342316"
---
# <a name="texturing-state-variables"></a>Texturierungsstatusvariablen

<dl> <dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL \_ Textur \_ *x*</dt> <dd> 

|                  |                                                       |
|------------------|-------------------------------------------------------|
| Beschreibung:     | True, wenn die *x*   -D-Texturierung aktiviert ist (*x* ist 1-d oder 2D). |
| Attribut Gruppe: | Textur/aktivieren                                        |
| Anfangswert:   | GL \_ false                                             |
| Get-Befehl:     | [**glisenabled**](glisenabled.md)                    |



 

</dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL- \_ Textur</dt> <dd> 

|                  |                                              |
|------------------|----------------------------------------------|
| Beschreibung:     | *x*   -D Textur Bild auf Detailebene *i* |
| Attribut Gruppe: |                                              |
| Anfangswert:   |                                              |
| Get-Befehl:     | [**glgetteximage**](glgetteximage.md)       |



 

</dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL- \_ Textur \_ Breite</dt> <dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| Beschreibung:     | *x*   -D *Textur Bild*   Breite                       |
| Attribut Gruppe: |                                                          |
| Anfangswert:   | 0                                                        |
| Get-Befehl:     | [**glgettexlevelparameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL- \_ Textur \_ Höhe</dt> <dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| Beschreibung:     | *x*   -D *Textur Bild meine*   Höhe                      |
| Attribut Gruppe: |                                                          |
| Anfangswert:   | 0                                                        |
| Get-Befehl:     | [**glgettexlevelparameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL- \_ Textur Rahmen \_</dt> <dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| Beschreibung:     | *x*   -D Textur Bild *i* Rahmen                        |
| Attribut Gruppe: |                                                          |
| Anfangswert:   | 0                                                        |
| Get-Befehl:     | [**glgettexlevelparameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL- \_ Textur \_ Komponenten</dt> <dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| Beschreibung:     | Textur Bild Komponenten                                 |
| Attribut Gruppe: |                                                          |
| Anfangswert:   | 1                                                        |
| Get-Befehl:     | [**glgettexlevelparameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>Rahmenfarbe des GL- \_ Textur Rahmens \_ \_</dt> <dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| Beschreibung:     | Textur Rahmenfarbe                           |
| Attribut Gruppe: | Struktur                                        |
| Anfangswert:   | 0, 0, 0, 0                                     |
| Get-Befehl:     | [**glgettexparameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL- \_ Textur- \_ Min- \_ Filter</dt> <dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| Beschreibung:     | Textur Minimierung-Funktion                  |
| Attribut Gruppe: | Struktur                                        |
| Anfangswert:   | \_nächste nächste \_ MipMap ( \_ linear)                    |
| Get-Befehl:     | [**glgettexparameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL- \_ Textur- \_ mag- \_ Filter</dt> <dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| Beschreibung:     | Textur Vergrößerungsfunktion                 |
| Attribut Gruppe: | Struktur                                        |
| Anfangswert:   | GL \_ linear                                     |
| Get-Befehl:     | [**glgettexparameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL- \_ Textur Umbruch \_ \_ *x*</dt> <dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| Beschreibung:     | Textur Umbruch Modus (*x*   ist S oder T)              |
| Attribut Gruppe: | Struktur                                        |
| Anfangswert:   | GL. \_ Wiederholung                                     |
| Get-Befehl:     | [**glgettexparameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL- \_ Textur \_ env- \_ Modus</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Beschreibung:     | Textur-Anwendungsfunktion         |
| Attribut Gruppe: | Struktur                              |
| Anfangswert:   | GL \_ modulate                         |
| Get-Befehl:     | [**glgettexenviv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL- \_ Textur Gesamt \_ \_ Farbe</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Beschreibung:     | Textur Umgebungs Farbe            |
| Attribut Gruppe: | Struktur                              |
| Anfangswert:   | 0, 0, 0, 0                           |
| Get-Befehl:     | [**glgettexendvfv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL \_ Textur \_ gen \_ *x*</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Beschreibung:     | TEXGEN ist aktiviert (*x*   ist S, T, R oder Q). |
| Attribut Gruppe: | Textur/aktivieren                           |
| Anfangswert:   | GL \_ false                                |
| Get-Befehl:     | [**glisenabled**](glisenabled.md)       |



 

</dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL- \_ Augen \_ Ebene</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Beschreibung:     | Formel für die Formel der TEXGEN-Ebene   |
| Attribut Gruppe: | Struktur                              |
| Anfangswert:   |                                      |
| Get-Befehl:     | [**glgettexgenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL- \_ Objekt \_ Ebene</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Beschreibung:     | Lineare Koeffizienten für TEXGEN-Objekte    |
| Attribut Gruppe: | Struktur                              |
| Anfangswert:   |                                      |
| Get-Befehl:     | [**glgettexgenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL- \_ Textur \_ gen- \_ Modus</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Beschreibung:     | Für TEXGEN verwendete Funktion             |
| Attribut Gruppe: | Struktur                              |
| Anfangswert:   | GL- \_ Eye \_ linear                      |
| Get-Befehl:     | [**glgettexgeniv**](glgettexgen.md) |



 

</dd> </dl>

 

 




