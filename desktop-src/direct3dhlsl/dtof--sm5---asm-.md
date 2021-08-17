---
title: dtof (sm5 – asm)
description: Komponentenweise Konvertierung von Gleitkommadaten mit doppelter Genauigkeit in Gleitkommadaten mit einfacher Genauigkeit.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d16ddf79b1a201bf78e0b45d1206169576bee4193b8c8158469055131768efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792327"
---
# <a name="dtof-sm5---asm"></a>dtof (sm5 – asm)

Komponentenweise Konvertierung von Gleitkommadaten mit doppelter Genauigkeit in Gleitkommadaten mit einfacher Genauigkeit.



| dtof dest \[ .mask \] , \[ - \] src \[ .swizzle \] , |
|-------------------------------------------|



 



| Element                                                            | Beschreibung                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse der konvertierten Daten.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die zu konvertierenden Daten.<br/>          |



 

## <a name="remarks"></a>Hinweise

Jede Komponente der Quelle wird von der Darstellung mit doppelter Genauigkeit in die Darstellung mit einfacher Genauigkeit konvertiert, indem rundend auf die nächste gerade Rundung gerundet wird.

Die gültigen Swizzles für den Quellparameter sind .xyzw, .xyxy, .zwxy, .zwzw.

Die gültigen *Destmasken* sind eine oder zwei Komponenten. Das heißt: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw Das Ergebnis der ersten Konvertierung geht an die erste Komponente in der Maske, und das Ergebnis der zweiten Komponente geht in die zweite Komponente in der Maske, sofern vorhanden.

*Dest-Komponenten* sind float32.

*src* ist ein double vec2 across (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB) post swizzle.

Bei float32-<->double-Konvertierungen können Implementierungen float32-Denormen entweder berücksichtigt oder leeren.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

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

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





