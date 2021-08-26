---
title: dcl_output_control_point_count (sm5 - asm)
description: Deklariert die Anzahl der Ausgabekontrollpunkt des Hüllen-Shaders.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93dc28a2af3ac50c835fa7ec38d7d344029af76a11cb2b84945dbf5009d68473
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024700"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a>dcl \_ output control point count \_ \_ \_ (sm5 - asm)

Deklariert die Anzahl der Ausgabekontrollpunkt des Hüllen-Shaders.



| dcl \_ output control point count \_ \_ \_ N |
|--------------------------------------|



 



| Element                                                   | BESCHREIBUNG                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[in \] Ein ganzzahliger Wert zwischen 0 und 32, der die Anzahl der Ausgabekontrollpunkt angibt.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Hüllen-Shader kann 0 Kontrollpunkte ausstellen, wenn sie nicht benötigt werden.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf                 | Domain | Geometrie | Pixel | Compute |
|--------|----------------------|--------|----------|-------|---------|
|        | Abschnitt "Deklarationen" |        |          |       |         |



 

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

 

 





