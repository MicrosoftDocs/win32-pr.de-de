---
title: dmin (sm5 - asm)
description: Komponentenweises Minimum mit doppelter Genauigkeit.
ms.assetid: 77331B4D-C4B5-49B2-BB6A-77BD5050B575
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20977a24113db111e85bc644ed68eccaa7e75db91c18bf71d80ac89f5ee19547
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855120"
---
# <a name="dmin-sm5---asm"></a>dmin (sm5 - asm)

Komponentenweises Minimum mit doppelter Genauigkeit.



| dmin \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/> *dest*  =  *src0*  <  *src1* ? *src0* : *src1*<br/> < wird anstelle von <= verwendet, sodass bei min(x,y) = x dann max(x,y) = y. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten, die mit *src1 verglichen werden.*<br/>                                                                                                                                                     |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die Komponenten, die mit *src0 verglichen werden.*<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Hinweise

NaN verfügt über eine besondere Behandlung. Wenn ein Quellopernd NaN ist, wird der andere Quellopernd zurückgegeben. Die Auswahl erfolgt pro Komponente. Wenn beide NaN sind, wird eine beliebige NaN-Darstellung zurückgegeben.

Die gültigen Swizzles für die Quellparameter sind .xyzw, .xyxy, .zwxy, .zwzw. Die *gültigen Destmasken* sind .xy, .zw und .xyzw. Die folgenden *src-Zuordnungen* sind post swizzle:

-   *dest* ist ein double vec2 über (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).
-   *src0* ist eine doppelte Vec2 zwischen (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).
-   *src1* ist ein double-vec2 zwischen (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
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

 

 





