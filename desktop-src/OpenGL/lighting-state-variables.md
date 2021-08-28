---
title: Statusvariablen für die Helligkeit
description: Statusvariablen für die Helligkeit
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- Beleuchtungszustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfeb867f979a0f5f2da838cdd225c91da2b67913c18cdda89c5d40a3f8ed6b88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034910"
---
# <a name="lighting-state-variables"></a>Statusvariablen für die Helligkeit

<dl> <dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>\_GL-BELEUCHTUNG</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | True, wenn die Beleuchtung aktiviert ist        |
| Attributgruppe: | Beleuchtung/Aktivierung                    |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL \_ COLOR \_ MATERIAL</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | TRUE, wenn die Farbnachverfolgung aktiviert ist  |
| Attributgruppe: | Belichtung                           |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL \_ COLOR \_ MATERIAL \_ PARAMETER</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Materialeigenschaften, die die aktuelle Farbe nachverfolgen                                       |
| Attributgruppe: | Belichtung                                                                         |
| Anfangswert:   | GL \_ AMBIENT \_ UND \_ DIFFUSE                                                        |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL \_ COLOR \_ MATERIAL \_ FACE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Von der Farbnachverfolgung betroffene Gesichter                                                 |
| Attributgruppe: | Belichtung                                                                         |
| Anfangswert:   | GL \_ FRONT \_ AND \_ BACK                                                             |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL \_ AMBIENT</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------------|
| Beschreibung:     | Umgebungsmaterialfarbe                   |
| Attributgruppe: | Belichtung                                 |
| Anfangswert:   | (0.2,0.2,0.2,1.0)                        |
| Get-Befehl:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ DIFFUSE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------------|
| Beschreibung:     | Diffuse Materialfarbe                   |
| Attributgruppe: | Belichtung                                 |
| Anfangswert:   | (0.8,0.8,0.8,1.0)                        |
| Get-Befehl:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ SPECULAR</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------------|
| Beschreibung:     | Specular material color (Farbe des Specular-Materials)                  |
| Attributgruppe: | Belichtung                                 |
| Anfangswert:   | (0.0,0.0,0.0,1.0)                        |
| Get-Befehl:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>\_GL-FEHLER</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------------|
| Beschreibung:     | Farbiges Material                  |
| Attributgruppe: | Belichtung                                 |
| Anfangswert:   | (0.0,0.0,0.0,1.0)                        |
| Get-Befehl:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>\_GL-GL-SCHLÄFRIGKEIT</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------------|
| Beschreibung:     | Specular exponent of material            |
| Attributgruppe: | Belichtung                                 |
| Anfangswert:   | 0,0                                      |
| Get-Befehl:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL \_ LIGHT \_ MODEL \_ AMBIENT</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Umgebungsszenenfarbe                                                            |
| Attributgruppe: | Belichtung                                                                       |
| Anfangswert:   | (0.2,0.2,0.2,1.0)                                                              |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL \_ LIGHT \_ MODEL \_ LOCAL \_ VIEWER</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Viewer ist lokal                                                                  |
| Attributgruppe: | Belichtung                                                                         |
| Anfangswert:   | GL \_ FALSE                                                                        |
| Get-Befehl:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL \_ LIGHT \_ MODEL \_ TWO \_ SIDE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Verwenden der zweiseitigen Beleuchtung                                                           |
| Attributgruppe: | Belichtung                                                                         |
| Anfangswert:   | GL \_ FALSE                                                                        |
| Get-Befehl:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL \_ AMBIENT</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Umgebungsstärke des Lichts *i*     |
| Attributgruppe: | Belichtung                           |
| Anfangswert:   | (0.0,0.0,0.0,1.0)                  |
| Get-Befehl:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ DIFFUSE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Diffuse Intensität des Lichts *i*     |
| Attributgruppe: | Belichtung                           |
| Anfangswert:   |                                    |
| Get-Befehl:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ SPECULAR</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Specular intensity of light *i*    |
| Attributgruppe: | Belichtung                           |
| Anfangswert:   |                                    |
| Get-Befehl:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL \_ POSITION</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Position des Lichts *i*              |
| Attributgruppe: | Belichtung                           |
| Anfangswert:   | (0.0,0.0,1.0,0.0)                  |
| Get-Befehl:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL \_ CONSTANT \_ ATTENUATION</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Konstanter Dämpfungsfaktor        |
| Attributgruppe: | Belichtung                           |
| Anfangswert:   | 1.0                                |
| Get-Befehl:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>GL \_ \_ LINEARE DÄMPFUNG</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Linearer Dämpfungsfaktor          |
| Attributgruppe: | Belichtung                           |
| Anfangswert:   | 0,0                                |
| Get-Befehl:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL \_ QUADRATISCHE \_ DÄMPFUNG</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Quadratischer Dämpfungsfaktor       |
| Attributgruppe: | Belichtung                           |
| Anfangswert:   | 0,0                                |
| Get-Befehl:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL \_ SPOT \_ DIRECTION</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Blickpunktrichtung des Lichts *i*   |
| Attributgruppe: | Belichtung                           |
| Anfangswert:   | (0.0,0.0,-1.0)                     |
| Get-Befehl:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL \_ SPOT \_ EXPONENT</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Spotlight-Exponent des Lichts *i*    |
| Attributgruppe: | Belichtung                           |
| Anfangswert:   | 0,0                                |
| Get-Befehl:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL \_ SPOT \_ CUTOFF</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Blickpunktwinkel des Lichts *i*       |
| Attributgruppe: | Belichtung                           |
| Anfangswert:   | 180.0                              |
| Get-Befehl:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ LIGHT *i*</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | True, wenn "light *i"* aktiviert ist          |
| Attributgruppe: | Beleuchtung/Aktivierung                    |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL \_ COLOR \_ INDEXES</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | *C (a)*, *C (d)* und *C (s)* für die Farbindexbeleuchtung                         |
| Attributgruppe: | Beleuchtung/Aktivierung                                                                |
| Anfangswert:   | 0,1,1                                                                          |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




