---
title: Pixel Vorgänge
description: Pixel Vorgänge
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- Pixel Vorgänge OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda15342b246ba979bdbe60184eeb632368f36b4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857275"
---
# <a name="pixel-operations"></a>Pixel Vorgänge

<dl> <dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL- \_ Scissor- \_ Test</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Scissoring aktiviert                 |
| Attribut Gruppe: | Scissor/enable                     |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>Feld "GL \_ Scissor" \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Scissor-Feld                                                                      |
| Attribut Gruppe: | Scheren                                                                          |
| Anfangswert:   |                                                                                  |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL- \_ Schablonen \_ Test</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Aktivierte Schablone                 |
| Attribut Gruppe: | Schablone-Puffer/aktivieren              |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL- \_ Schablone \_ Func</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Schablone-Funktion                                                                 |
| Attribut Gruppe: | Schablone-Puffer                                                                   |
| Anfangswert:   | immer GL. \_                                                                       |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL- \_ Schablonen \_ Wert \_ Maske</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Schablonen Maske                                                                     |
| Attribut Gruppe: | Schablone-Puffer                                                                   |
| Anfangswert:   | 1                                                                              |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL- \_ Schablone \_ Ref</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Schablonen Referenzwert                                                          |
| Attribut Gruppe: | Schablone-Puffer                                                                   |
| Anfangswert:   | 0                                                                                |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL- \_ Schablone \_ schlägt fehl</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Schablone-Fehler Aktion                                                              |
| Attribut Gruppe: | Schablone-Puffer                                                                   |
| Anfangswert:   | GL \_ beibehalten                                                                         |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>Fehler beim Übergeben der GL- \_ Schablone \_ \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Aktion für Schablone-tiefen Puffer Fehler                                                 |
| Attribut Gruppe: | Schablone-Puffer                                                                   |
| Anfangswert:   | GL \_ beibehalten                                                                         |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>bestandungs Tiefe für GL- \_ Schablone \_ \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Aktion für Schablone-tiefen Puffer Durchlauf                                                 |
| Attribut Gruppe: | Schablone-Puffer                                                                   |
| Anfangswert:   | GL \_ beibehalten                                                                         |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL- \_ alpha \_ Test</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Alpha Test aktiviert                 |
| Attribut Gruppe: | Farb Puffer/-Aktivierung                |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL- \_ alpha \_ Test- \_ Func</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Alpha-Testfunktion                                                              |
| Attribut Gruppe: | Farb Puffer                                                                     |
| Anfangswert:   | immer GL. \_                                                                       |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL- \_ alpha- \_ Test \_ Ref</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Alpha-Test Verweis Wert                                                       |
| Attribut Gruppe: | Farb Puffer                                                                     |
| Anfangswert:   | 0                                                                                |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL- \_ tiefen \_ Test</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Tiefen Puffer aktiviert               |
| Attribut Gruppe: | tiefen Puffer/aktivieren                |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL- \_ Tiefe \_ Func</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Tiefen Puffer-Testfunktion                                                       |
| Attribut Gruppe: | tiefen Puffer                                                                     |
| Anfangswert:   | GL \_ weniger                                                                         |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL \_ Blend</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Blending aktiviert                   |
| Attribut Gruppe: | Farb Puffer/-Aktivierung                |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL \_ blenc \_ src</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Blending der Quell Funktion                                                         |
| Attribut Gruppe: | Farb Puffer                                                                     |
| Anfangswert:   | GL \_ 1                                                                          |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL \_ Blend \_ DST</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Zielfunktion wird gemischt                                                    |
| Attribut Gruppe: | Farb Puffer                                                                     |
| Anfangswert:   | GL \_ null                                                                         |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL \_ .</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Dithering aktiviert                  |
| Attribut Gruppe: | Farb Puffer/-Aktivierung                |
| Anfangswert:   | GL \_ true                           |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL- \_ Logik- \_ op</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | Logischer Vorgang aktiviert          |
| Attribut Gruppe: | Farb Puffer/-Aktivierung                |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL- \_ Logik- \_ op- \_ Modus</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Logische Vorgangs Funktion                                                       |
| Attribut Gruppe: | Farb Puffer                                                                     |
| Anfangswert:   | GL- \_ Kopie                                                                         |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




