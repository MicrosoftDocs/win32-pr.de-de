---
title: Pixelvorgänge
description: Pixelvorgänge
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- Pixelvorgänge OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d36fc22ace4ee18303ce0eb16c5a10f901510f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908878"
---
# <a name="pixel-operations"></a>Pixelvorgänge

<dl> <dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL \_ SCISSOR \_ TEST</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Scissoring aktiviert                 |
| Attributgruppe: | scissor/enable                     |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL \_ SCISSOR \_ BOX</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Scissor-Feld                                                                      |
| Attributgruppe: | Schere                                                                          |
| Anfangswert:   |                                                                                  |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_GL-SCHABLONENTEST \_</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Schablonen aktiviert                 |
| Attributgruppe: | Schablonenpuffer/Aktivieren              |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL \_ STENCIL \_ FUNC</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Schablonenfunktion                                                                 |
| Attributgruppe: | Schablonenpuffer                                                                   |
| Anfangswert:   | GL \_ ALWAYS                                                                       |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL \_ STENCIL \_ VALUE \_ MASK</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Schablonenmaske                                                                     |
| Attributgruppe: | Schablonenpuffer                                                                   |
| Anfangswert:   | 1 s                                                                              |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL \_ STENCIL \_ REF</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Schablonenverweiswert                                                          |
| Attributgruppe: | Schablonenpuffer                                                                   |
| Anfangswert:   | 0                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>FEHLER \_ BEI GL-SCHABLONE \_</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Schablonen-Fehleraktion                                                              |
| Attributgruppe: | Schablonenpuffer                                                                   |
| Anfangswert:   | GL \_ KEEP                                                                         |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>FEHLER \_ BEI GL-SCHABLONENPASSTIEFE \_ \_ \_</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Fehleraktion für Schablonentiefepuffer                                                 |
| Attributgruppe: | Schablonenpuffer                                                                   |
| Anfangswert:   | GL \_ KEEP                                                                         |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL \_ STENCIL \_ PASS \_ DEPTH \_ PASS</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Pufferdurchlaufaktion für Schablonentiefe                                                 |
| Attributgruppe: | Schablonenpuffer                                                                   |
| Anfangswert:   | GL \_ KEEP                                                                         |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL \_ ALPHA \_ TEST</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Alphatest aktiviert                 |
| Attributgruppe: | Farbpuffer/Aktivieren                |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL \_ ALPHA \_ TEST \_ FUNC</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Alphatestfunktion                                                              |
| Attributgruppe: | Farbpuffer                                                                     |
| Anfangswert:   | GL \_ ALWAYS                                                                       |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL \_ ALPHA \_ TEST \_ REF</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Alphatestverweiswert                                                       |
| Attributgruppe: | Farbpuffer                                                                     |
| Anfangswert:   | 0                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL \_ DEPTH \_ TEST</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Tiefenpuffer aktiviert               |
| Attributgruppe: | Tiefenpuffer/Aktivieren                |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL \_ DEPTH \_ FUNC</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Testfunktion "Tiefenpuffer"                                                       |
| Attributgruppe: | Tiefenpuffer                                                                     |
| Anfangswert:   | GL \_ LESS                                                                         |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL \_ BLEND</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Blending aktiviert                   |
| Attributgruppe: | Farbpuffer/Aktivieren                |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL \_ BLENC \_ SRC</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Blending-Quellfunktion                                                         |
| Attributgruppe: | Farbpuffer                                                                     |
| Anfangswert:   | GL \_ ONE                                                                          |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL \_ BLEND \_ DST</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Blendingzielfunktion                                                    |
| Attributgruppe: | Farbpuffer                                                                     |
| Anfangswert:   | GL \_ ZERO                                                                         |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL \_ DITHER</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Dithering aktiviert                  |
| Attributgruppe: | Farbpuffer/Aktivieren                |
| Anfangswert:   | GL \_ TRUE                           |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL \_ LOGIC \_ OP</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | Logischer Vorgang aktiviert          |
| Attributgruppe: | Farbpuffer/Aktivieren                |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL \_ LOGIC \_ OP \_ MODE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Logische Vorgangsfunktion                                                       |
| Attributgruppe: | Farbpuffer                                                                     |
| Anfangswert:   | GL \_ COPY                                                                         |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




