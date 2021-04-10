---
title: Evaluatorstatusvariablen
description: Evaluatorstatusvariablen
ms.assetid: e7d710be-de17-46a0-8ad8-0f65b943ece8
keywords:
- Auswerters-Statusvariablen OpenGL
topic_type:
- apiref
api_name:
- Evaluator State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 615e7cde4a8f82c3f4a9a95791912c5dc3f77ff3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948206"
---
# <a name="evaluator-state-variables"></a>Evaluatorstatusvariablen

<dl> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>GL- \_ Bestellung</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Beschreibung:     | 1D-Zuordnungs Reihenfolge                  |
| Attribut Gruppe: |                                |
| Anfangswert:   | 1                              |
| Get-Befehl:     | [**glgetmapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>GL- \_ Bestellung</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Beschreibung:     | 2D-Kartenbestellungen                 |
| Attribut Gruppe: |                                |
| Anfangswert:   | 1, 1                            |
| Get-Befehl:     | [**glgetmapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL. \_ coeff</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Beschreibung:     | 1D-Steuerungs Punkte             |
| Attribut Gruppe: |                                |
| Anfangswert:   |                                |
| Get-Befehl:     | [**glgetmapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL. \_ coeff</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Beschreibung:     | 2D-Steuerungs Punkte             |
| Attribut Gruppe: |                                |
| Anfangswert:   |                                |
| Get-Befehl:     | [**glgetmapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>GL- \_ Domäne</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Beschreibung:     | 1-D-Domänen Endpunkte           |
| Attribut Gruppe: |                                |
| Anfangswert:   |                                |
| Get-Befehl:     | [**glgetmapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>GL- \_ Domäne</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Beschreibung:     | 2-D-Domänen Endpunkte           |
| Attribut Gruppe: |                                |
| Anfangswert:   |                                |
| Get-Befehl:     | [**glgetmapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_MAP1_x"></span><span id="gl_map1_x"></span><span id="GL_MAP1_X"></span>GL \_ zuordnung1 \_ x</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | 1-D-Zuordnung aktiviert: *x* ist ein Kartentyp.   |
| Attribut Gruppe: | Eval/enable                        |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP2_x"></span><span id="gl_map2_x"></span><span id="GL_MAP2_X"></span>GL \_ map2 \_ x</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | 2D-Zuordnung aktiviert: *x* ist ein Kartentyp   |
| Attribut Gruppe: | Eval/enable                        |
| Anfangswert:   | GL \_ false                          |
| Get-Befehl:     | [**glisenabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_DOMAIN"></span><span id="gl_map1_grid_domain"></span>GL \_ zuordnung1 \_ Raster \_ Domäne</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | 1D-Raster Endpunkte                                                             |
| Attribut Gruppe: | eval                                                                           |
| Anfangswert:   | 0, 1                                                                            |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP2_GRID_DOMAIN"></span><span id="gl_map2_grid_domain"></span>GL \_ map2 \_ Raster \_ Domäne</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | 2D-Raster Endpunkte                                                             |
| Attribut Gruppe: | eval                                                                           |
| Anfangswert:   | 0, 1; 0, 1                                                                     |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>GL \_ zuordnung1 \_ Raster \_ Segmente</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Beschreibung:     | 1-D-Raster Bereiche                 |
| Attribut Gruppe: | eval                               |
| Anfangswert:   | 1                                  |
| Get-Befehl:     | [**glgetfloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>GL \_ zuordnung1 \_ Raster \_ Segmente</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | 2D-Raster Segmente                                                              |
| Attribut Gruppe: | eval                                                                           |
| Anfangswert:   | 1, 1                                                                           |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span>GL \_ Auto \_ Normal</dt> <dd> 

|                  |                                             |
|------------------|---------------------------------------------|
| Beschreibung:     | True, wenn die automatische normale Generierung aktiviert ist. |
| Attribut Gruppe: | eval                                        |
| Anfangswert:   | GL \_ false                                   |
| Get-Befehl:     | [**glisenabled**](glisenabled.md)          |



 

</dd> </dl>

 

 




