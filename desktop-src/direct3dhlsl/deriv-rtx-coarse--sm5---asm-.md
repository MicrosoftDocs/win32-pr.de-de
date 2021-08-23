---
title: deriv_rtx_coarse (sm5 - asm)
description: Berechnet die Änderungsrate der Komponenten. | deriv_rtx_coarse (sm5 - asm)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50066fe58c3d0a0cdd903de9fbb479a8fbab2c3a20c622ebca138c0937aaf0dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986640"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a>deriv \_ rtx \_ coarse (sm5 - asm)

Berechnet die Änderungsrate der Komponenten.



| deriv \_ rtx \_ coarse sat \[ \_ \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , |
|----------------------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten im Vorgang.<br/>             |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung berechnet die Änderungsrate der Inhalte jeder float32-Komponente von *src0* (post-swizzle) im Hinblick auf renderTarget x direction (rtx) oder RenderTarget y direction [(siehe deriv \_ rty \_ coarse](deriv-rty-coarse--sm5---asm-.md)). Für jeden 2x2-Stempel von Pixeln wird nur ein einzelnes x,y-Ableitungspaar berechnet.

Die Daten im aktuellen Pixel-Shaderaufruf können an der Berechnung der angeforderten Ableitung beteiligt sein, da die Ableitung nur einmal pro 2 x 2 Quad berechnet wird. Beispielsweise könnte die x-Ableitung ein Delta aus der oberen Pixelzeile sein, und die y-Richtung ([deriv \_ rty \_ coarse](deriv-rty-coarse--sm5---asm-.md)) könnte ein Delta aus der linken Pixelspalte sein. Die genaue Berechnung liegt beim Hardwareanbieter. Es gibt auch keine Spezifikation, die ankündigt, wie die 2x2-Quads ausgerichtet oder über einem primitiv angeordnet werden.

Ableitungen werden auf einer groben Ebene berechnet, einmal pro 2 x 2 Pixel Quad. Diese Anweisung und [deriv \_ rty \_ coarse](deriv-rty-coarse--sm5---asm-.md) sind Alternativen zur Ableitung von [ \_ rtx \_ fine](deriv-rtx-fine--sm5---asm-.md) und [deriv \_ rty \_ fine.](deriv-rty-fine--sm5---asm-.md) Diese \_ groben \_ und feinen Ableitungsanweisungen sind ein Ersatz für **die Ableitung von \_ rtxderiv \_ rty** aus vorherigen Shadermodellen.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

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

 

 





