---
title: Statusvariablen für Auswertungen
description: Statusvariablen für Auswertungen
ms.assetid: e7d710be-de17-46a0-8ad8-0f65b943ece8
keywords:
- Auswertungszustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Evaluator State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 747ed7c19817757570d6517c68a987c2c75aa340c74ecfbac9fe258b1091f00e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082510"
---
# <a name="evaluator-state-variables"></a>Statusvariablen für Auswertungen

<dl> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>GL \_ ORDER</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------|
| Beschreibung:     | 1D-Karten reihenfolge                  |
| Attributgruppe: |                                |
| Anfangswert:   | 1                              |
| Get-Befehl:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>GL \_ ORDER</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------|
| Beschreibung:     | 2D-Zuordnungsaufträge                 |
| Attributgruppe: |                                |
| Anfangswert:   | 1,1                            |
| Get-Befehl:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------|
| Beschreibung:     | 1D-Kontrollpunkte             |
| Attributgruppe: |                                |
| Anfangswert:   |                                |
| Get-Befehl:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------|
| Beschreibung:     | 2D-Kontrollpunkte             |
| Attributgruppe: |                                |
| Anfangswert:   |                                |
| Get-Befehl:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>GL \_ DOMAIN</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------|
| Beschreibung:     | 1D-Domänenendpunkte           |
| Attributgruppe: |                                |
| Anfangswert:   |                                |
| Get-Befehl:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>GL \_ DOMAIN</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------|
| Beschreibung:     | 2D-Domänenendpunkte           |
| Attributgruppe: |                                |
| Anfangswert:   |                                |
| Get-Befehl:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_MAP1_x"></span><span id="gl_map1_x"></span><span id="GL_MAP1_X"></span>GL \_ MAP1 \_ x</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | 1D-Zuordnung aktiviert: *x* ist kartentyp   |
| Attributgruppe: | eval/enable                        |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP2_x"></span><span id="gl_map2_x"></span><span id="GL_MAP2_X"></span>GL \_ MAP2 \_ x</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | 2D-Zuordnung aktiviert: *x* ist kartentyp   |
| Attributgruppe: | eval/enable                        |
| Anfangswert:   | GL \_ FALSE                          |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_DOMAIN"></span><span id="gl_map1_grid_domain"></span>GL \_ MAP1 \_ GRID \_ DOMAIN</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | 1D-Rasterendpunkte                                                             |
| Attributgruppe: | eval                                                                           |
| Anfangswert:   | 0,1                                                                            |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP2_GRID_DOMAIN"></span><span id="gl_map2_grid_domain"></span>GL \_ MAP2 \_ GRID \_ DOMAIN</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | 2D-Rasterendpunkte                                                             |
| Attributgruppe: | eval                                                                           |
| Anfangswert:   | 0, 1; 0, 1                                                                     |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>GL \_ \_ MAP1– \_ RASTERSEGMENTE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|------------------------------------|
| Beschreibung:     | 1D-Rasterbereiche                 |
| Attributgruppe: | eval                               |
| Anfangswert:   | 1                                  |
| Get-Befehl:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>GL \_ \_ MAP1– \_ RASTERSEGMENTE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | 2D-Rastersegmente                                                              |
| Attributgruppe: | eval                                                                           |
| Anfangswert:   | 1, 1                                                                           |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span>GL \_ AUTO \_ NORMAL</dt> <dd> 

| Eigenschaft | Wert |
|------------------|---------------------------------------------|
| Beschreibung:     | True, wenn die automatische normale Generierung aktiviert ist |
| Attributgruppe: | eval                                        |
| Anfangswert:   | GL \_ FALSE                                   |
| Get-Befehl:     | [**glIsEnabled**](glisenabled.md)          |



 

</dd> </dl>

 

 




