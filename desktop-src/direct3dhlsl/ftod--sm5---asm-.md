---
title: ftod (sm5 - asm)
description: Komponentenweise Konvertierung von Gleitkommadaten mit nur einer Genauigkeit in Gleitkommadaten mit doppelter Genauigkeit.
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d31396aa0f2b82dc4ea366bbdde704d55fa850d0d0a9f2f1f3de539a763facb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982430"
---
# <a name="ftod-sm5---asm"></a>ftod (sm5 - asm)

Komponentenweise Konvertierung von Gleitkommadaten mit nur einer Genauigkeit in Gleitkommadaten mit doppelter Genauigkeit.



| ftod dest \[ .mask \] , \[ - \] src \[ .swizzle \] , |
|-------------------------------------------|



 



| Element                                                            | Beschreibung                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse der konvertierten Daten.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die zu konvertierten Daten.<br/>          |



 

## <a name="remarks"></a>Hinweise

Jede Komponente der Quelle wird von der Darstellung mit nur einer Genauigkeit in die Darstellung mit doppelter Genauigkeit konvertiert.

Die *gültigen Destmasken* sind .xy, .zw und .xyzw. .xy empfängt das Ergebnis der ersten Konvertierung, und .zw empfängt das Ergebnis der zweiten Konvertierung.

*dest* ist ein double vec2 über (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).

*src ist* ein float-vec2 über x und y (zw ignoriert) (post swizzle).

Für float32<->double-Konvertierungen können Implementierungen float32-Denormale entweder unterstützen oder leeren.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





