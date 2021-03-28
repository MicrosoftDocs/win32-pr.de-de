---
title: dtof (SM5-ASM)
description: Komponenten Weise Konvertierung von Gleit Komma Daten mit doppelter Genauigkeit in Gleit Komma Daten mit einfacher Genauigkeit.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a66e72cf4c2cb1ac49adc492a586b4cbb9eef3b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313626"
---
# <a name="dtof-sm5---asm"></a>dtof (SM5-ASM)

Komponenten Weise Konvertierung von Gleit Komma Daten mit doppelter Genauigkeit in Gleit Komma Daten mit einfacher Genauigkeit.



| dtof dest \[ . mask \] , \[ - \] src \[ . Swizzle \] , |
|-------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse der konvertierten Daten.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den zu konvertierenden Daten.<br/>          |



 

## <a name="remarks"></a>Bemerkungen

Jede Komponente der Quelle wird von der Darstellung mit doppelter Genauigkeit in die Darstellung mit einfacher Genauigkeit konvertiert und verwendet gleichmäßige Rundung.

Die gültigen Streifen für den Quellparameter lauten. xyzw,. xyxy,. zwxy,. zwzw.

Die gültigen *dest* -Masken sind eine oder zwei Komponenten. Das heißt:. x,. y,. z,. w,. XY,. XZ,. XW,. YZ,. yw,. zw das Ergebnis der ersten Konvertierung wird an die erste Komponente in der Maske weitergeleitet, und das Ergebnis der zweiten Komponente wechselt in die zweite Komponente in der Maske, falls vorhanden.

die *dest* -Komponenten sind float32.

*src* ist eine doppelte vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb) Post-Swizzle.

Bei<->Double-Konvertierungen können Implementierungen entweder float32 denorms beachten oder Sie leeren.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Anweisung wird in den folgenden shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





