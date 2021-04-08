---
title: Statusvariablen des Framebuffer-Steuer Elements
description: Statusvariablen des Framebuffer-Steuer Elements
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Framebuffer-Steuerelement Zustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d44327858ae43212fcaa4364ed23045de5e0296f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857072"
---
# <a name="framebuffer-control-state-variables"></a>Statusvariablen des Framebuffer-Steuer Elements

<dl> <dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL- \_ Zeichnungs \_ Puffer</dt> <dd> 

|                  |                                        |
|------------------|----------------------------------------|
| Beschreibung:     | Puffer zum Zeichnen ausgewählt           |
| Attribut Gruppe: | Farb Puffer                           |
| Anfangswert:   |                                        |
| Get-Befehl:     | [**glgetintegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL- \_ Index- \_ Schreib Vorfrage</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Farb Index-Schreib Vorfrage                                                            |
| Attribut Gruppe: | Farb Puffer                                                                     |
| Anfangswert:   | 1                                                                              |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL- \_ Farb \_ schreibfrage</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Farbschreib Zugriff aktiviert; R, G, B oder a                                               |
| Attribut Gruppe: | Farb Puffer                                                                     |
| Anfangswert:   | GL \_ true                                                                         |
| Get-Befehl:     | [**glgetbooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_ausführliche \_ Schreib vorschreibfrage</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Der für das Schreiben aktivierte tiefen Puffer                                                 |
| Attribut Gruppe: | tiefen Puffer                                                                     |
| Anfangswert:   | GL \_ true                                                                         |
| Get-Befehl:     | [**glgetbooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL. \_ Schablonen \_ schreibfrage</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Schablone-Puffer schreibfrage                                                         |
| Attribut Gruppe: | Schablone-Puffer                                                                   |
| Anfangswert:   | 1                                                                              |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>Füllwert für GL- \_ Farbe \_ \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Unklarer Wert des Farb Puffers (RGBA-Modus)                                           |
| Attribut Gruppe: | Farb Puffer                                                                   |
| Anfangswert:   | 0, 0, 0, 0                                                                     |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>Wert für GL- \_ Index \_ Löschen \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Unklarer Wert des Farb Puffers (Farb Index Modus)                                    |
| Attribut Gruppe: | Farb Puffer                                                                   |
| Anfangswert:   | 0                                                                              |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL- \_ Tiefe \_ Clear- \_ Wert</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Tiefen Puffer-Clear-Wert                                                         |
| Attribut Gruppe: | tiefen Puffer                                                                     |
| Anfangswert:   | 1                                                                                |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>Lösch Wert für GL- \_ Schablone \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Stencil-Puffer Clear-Wert                                                       |
| Attribut Gruppe: | Schablone-Puffer                                                                   |
| Anfangswert:   | 0                                                                                |
| Get-Befehl:     | [**glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>Wert für GL- \_ Accum \_ Clear \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Kumulations Puffer-Clear-Wert                                                |
| Attribut Gruppe: | Accum-Buffer                                                                   |
| Anfangswert:   | 0                                                                              |
| Get-Befehl:     | [**glgetfloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




