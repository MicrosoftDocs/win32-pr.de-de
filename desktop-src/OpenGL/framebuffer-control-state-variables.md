---
title: Statusvariablen für Framebuffer-Steuerelemente
description: Statusvariablen für Framebuffer-Steuerelemente
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Framebuffer-Steuerelementzustandsvariablen OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 276019f790e5f4750e446cf4ae2d035e0178d0e79130100a5a5e1954cbdcb73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061912"
---
# <a name="framebuffer-control-state-variables"></a>Statusvariablen für Framebuffer-Steuerelemente

<dl> <dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL \_ DRAW \_ BUFFER</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------|
| Beschreibung:     | Für das Zeichnen ausgewählte Puffer           |
| Attributgruppe: | Farbpuffer                           |
| Anfangswert:   |                                        |
| Get-Befehl:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL \_ INDEX \_ WRITEMASK</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Farbindexschreibmaske                                                            |
| Attributgruppe: | Farbpuffer                                                                     |
| Anfangswert:   | 1                                                                              |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL \_ COLOR \_ WRITEMASK</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Farbschreibzugriff aktiviert; R, G, B oder A                                               |
| Attributgruppe: | Farbpuffer                                                                     |
| Anfangswert:   | GL \_ TRUE                                                                         |
| Get-Befehl:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL \_ DEPTH \_ WRITEMASK</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Für das Schreiben aktivierter Tiefenpuffer                                                 |
| Attributgruppe: | Tiefenpuffer                                                                     |
| Anfangswert:   | GL \_ TRUE                                                                         |
| Get-Befehl:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL \_ STENCIL \_ WRITEMASK</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Schablonenpuffer-Schreibmaske                                                         |
| Attributgruppe: | Schablonenpuffer                                                                   |
| Anfangswert:   | 1                                                                              |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL \_ COLOR \_ CLEAR \_ VALUE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Farbpuffer-Clear-Wert (RGBA-Modus)                                           |
| Attributgruppe: | Farbpuffer                                                                   |
| Anfangswert:   | 0, 0, 0, 0                                                                     |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL \_ INDEX \_ CLEAR \_ VALUE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Farbpuffer-Clear-Wert (Farbindexmodus)                                    |
| Attributgruppe: | Farbpuffer                                                                   |
| Anfangswert:   | 0                                                                              |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL \_ DEPTH \_ CLEAR \_ VALUE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Tiefenpuffer-Clear-Wert                                                         |
| Attributgruppe: | Tiefenpuffer                                                                     |
| Anfangswert:   | 1                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL \_ STENCIL \_ CLEAR \_ VALUE</dt> <dd> 

| Eigenschaft | Wert |
|------------------|----------------------------------------------------------------------------------|
| Beschreibung:     | Stencil-buffer clear value                                                       |
| Attributgruppe: | Schablonenpuffer                                                                   |
| Anfangswert:   | 0                                                                                |
| Get-Befehl:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL- \_ UND \_ GL-WERT LÖSCHEN \_</dt> <dd> 

| Eigenschaft | Wert |
|------------------|--------------------------------------------------------------------------------|
| Beschreibung:     | Klarwert des Akkumulationspuffers                                                |
| Attributgruppe: | bufferm-buffer                                                                   |
| Anfangswert:   | 0                                                                              |
| Get-Befehl:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




