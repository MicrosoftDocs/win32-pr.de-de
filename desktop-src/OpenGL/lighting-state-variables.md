---
title: Beleuchtungs Zustandsvariablen
description: Beleuchtungs Zustandsvariablen
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- Beleuchtungs Zustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7144e284b5be5abd5a6dc4e08fe2228b621465
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857399"
---
# <a name="lighting-state-variables"></a>Beleuchtungs Zustandsvariablen

<dl> <dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL- \_ Beleuchtung</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | True, wenn Beleuchtung aktiviert ist.        |
| Attribut Gruppe: | Beleuchtung/Aktivierung                    |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL- \_ Farb \_ Material</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | True, wenn die Farb Verfolgung aktiviert ist.  |
| Attribut Gruppe: | Belichtung                           |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL- \_ Farb \_ Material \_ Parameter</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Material Eigenschaften Nachverfolgung der aktuellen Farbe                                       |
| Attribut Gruppe: | Belichtung                                                                         |
| Anfangswert:   | GL \_ AMBIENT \_ und \_ diffuse                                                        |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL- \_ Farb \_ Material \_ Gesicht</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Von der Farbüberwachung betroffene Gesichter                                                 |
| Attribut Gruppe: | Belichtung                                                                         |
| Anfangswert:   | GL \_ vor \_ und \_ zurück                                                             |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL- \_ AMBIENT</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Beschreibung:     | Umgebungs Material Farbe                   |
| Attribut Gruppe: | Belichtung                                 |
| Anfangswert:   | (0,2, 0,2, 0,2, 1.0)                        |
| Get-Befehl:     | [**glgetmaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL- \_ diffuses</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Beschreibung:     | Farbe für Diffuses Material                   |
| Attribut Gruppe: | Belichtung                                 |
| Anfangswert:   | (0,8, 0.8, 0.8, 1.0)                        |
| Get-Befehl:     | [**glgetmaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ Glanz</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Beschreibung:     | Glanz Material Farbe                  |
| Attribut Gruppe: | Belichtung                                 |
| Anfangswert:   | (0,0, 0,0, 0,0, 1.0)                        |
| Get-Befehl:     | [**glgetmaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL \_ -Ausgabe</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Beschreibung:     | Emissive Material Farbe                  |
| Attribut Gruppe: | Belichtung                                 |
| Anfangswert:   | (0,0, 0,0, 0,0, 1.0)                        |
| Get-Befehl:     | [**glgetmaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL \_ .</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Beschreibung:     | Glanz Exponent von Material            |
| Attribut Gruppe: | Belichtung                                 |
| Anfangswert:   | 0,0                                      |
| Get-Befehl:     | [**glgetmaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL- \_ Light- \_ Modell \_ AMBIENT</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Ambiente-Szene Farbe                                                            |
| Attribut Gruppe: | Belichtung                                                                       |
| Anfangswert:   | (0,2, 0,2, 0,2, 1.0)                                                              |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>\_ \_ \_ lokaler \_ Viewer für GL-Light-Modell</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Viewer ist lokal                                                                  |
| Attribut Gruppe: | Belichtung                                                                         |
| Anfangswert:   | GL \_ false                                                                        |
| Get-Befehl:     | [**glgetbooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL- \_ Light- \_ Modell auf \_ zwei \_ Seiten</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Verwenden der zweiseitigen Beleuchtung                                                           |
| Attribut Gruppe: | Belichtung                                                                         |
| Anfangswert:   | GL \_ false                                                                        |
| Get-Befehl:     | [**glgetbooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL- \_ AMBIENT</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Umgebungs Intensität von Light *i*     |
| Attribut Gruppe: | Belichtung                           |
| Anfangswert:   | (0,0, 0,0, 0,0, 1.0)                  |
| Get-Befehl:     | [**glgetlightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL- \_ diffuses</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Diffuses Intensität von Light *i*     |
| Attribut Gruppe: | Belichtung                           |
| Anfangswert:   |                                    |
| Get-Befehl:     | [**glgetlightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ Glanz</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Glanz Intensität von Light *i*    |
| Attribut Gruppe: | Belichtung                           |
| Anfangswert:   |                                    |
| Get-Befehl:     | [**glgetlightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL- \_ Position</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Position von Light *i*              |
| Attribut Gruppe: | Belichtung                           |
| Anfangswert:   | (0,0, 0,0, 1.0, 0,0)                  |
| Get-Befehl:     | [**glgetlightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL- \_ Konstante \_ Dämpfung</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Faktor für konstante Dämpfung        |
| Attribut Gruppe: | Belichtung                           |
| Anfangswert:   | 1.0                                |
| Get-Befehl:     | [**glgetlightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>\_lineare \_ Dämpfung von GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Faktor für lineare Dämpfung          |
| Attribut Gruppe: | Belichtung                           |
| Anfangswert:   | 0,0                                |
| Get-Befehl:     | [**glgetlightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL. \_ quadratische \_ Dämpfung</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Faktor für die quadratische Dämpfung       |
| Attribut Gruppe: | Belichtung                           |
| Anfangswert:   | 0,0                                |
| Get-Befehl:     | [**glgetlightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL- \_ Spot- \_ Richtung</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Spotlight-Richtung von Light *i*   |
| Attribut Gruppe: | Belichtung                           |
| Anfangswert:   | (0,0, 0,0,-1,0)                     |
| Get-Befehl:     | [**glgetlightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL- \_ Spot- \_ Exponent</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Spotlight-Exponent von Light *i*    |
| Attribut Gruppe: | Belichtung                           |
| Anfangswert:   | 0,0                                |
| Get-Befehl:     | [**glgetlightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL. \_ Spot- \_ cuumff</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Spotlight-Winkel des Lichts *i*       |
| Attribut Gruppe: | Belichtung                           |
| Anfangswert:   | 180,0                              |
| Get-Befehl:     | [**glgetlightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ Light *i*</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | True, wenn Light *i* aktiviert ist.          |
| Attribut Gruppe: | Beleuchtung/Aktivierung                    |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL- \_ Farb \_ Indizes</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | *C (a)*, *c (d)* und *c (s)* für die Farb Index Beleuchtung                         |
| Attribut Gruppe: | Beleuchtung/Aktivierung                                                                |
| Anfangswert:   | 0, 1, 1                                                                          |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




