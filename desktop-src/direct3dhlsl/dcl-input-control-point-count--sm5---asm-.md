---
title: dcl_input_control_point_count (sm5 - asm)
description: Deklarieren Sie im Deklarationsabschnitt des Hüllen-Shaders die Anzahl der Eingabesteuerungspunkte für den Hüllen-Shader.
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c5414d5c660cf0bbce2b6219769cd36d4da9bbf3e59d9d130bfce0e0dceea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789880"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a>Anzahl der \_ \_ dcl-Eingabekontrollpunkt \_ \_ (sm5 - asm)

Deklarieren Sie im Deklarationsabschnitt des Hüllen-Shaders die Anzahl der Eingabesteuerungspunkte für den Hüllen-Shader.



| dcl \_ input control point count \_ \_ \_ {1..32} |
|-------------------------------------------|



 



| Element                                                   | Beschreibung                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[in \] Die Anzahl der Eingabesteuerungspunkt.<br/> |



 

## <a name="remarks"></a>Hinweise

Mindestens ein Eingabesteuerungspunkt ist erforderlich. sie kann leer sein, wenn sie nicht benötigt wird.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | X    |        |          |       |         |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





