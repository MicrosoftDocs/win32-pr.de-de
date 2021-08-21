---
title: deriv_rtx_fine (sm5 – asm)
description: Berechnet die Änderungsrate von Komponenten. | deriv_rtx_fine (sm5 – asm)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6666750be76d673ddc6c5f0d66d23131096812c93b71be52eb7e0f6ebb403ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792654"
---
# <a name="deriv_rtx_fine-sm5---asm"></a>deriv \_ rtx \_ fine (sm5 – asm)

Berechnet die Änderungsrate von Komponenten.



| deriv \_ rtx \_ fine sat \[ \_ \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , |
|--------------------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten im Vorgang.<br/>             |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung berechnet die Änderungsrate der Inhalte jeder float32-Komponente von *src0* (post-swizzle) in Bezug auf renderTarget x direction (rtx) oder RenderTarget y direction (siehe [deriv \_ rty \_ fine](deriv-rty-fine--sm5---asm-.md)). Jedes Pixel im 2x2-Stempel erhält ein eindeutiges Paar von x/y-Ableitungsberechnungen.

Die Daten im aktuellen Pixel-Shaderaufruf nehmen immer an der Berechnung der angeforderten Ableitung teil. Im 2x2-Pixel-Quader, in dem das aktuelle Pixel liegt, ist die x-Ableitung das Delta der Zeile von 2 Pixeln einschließlich des aktuellen Pixels. Die y-Ableitung ist das Delta der Spalte von 2 Pixeln einschließlich des aktuellen Pixels. Es gibt keine Spezifikation, die diktiert, wie die 2x2-Quader auf einem Primitiven ausgerichtet oder gekachelt werden.

Ableitungen werden auf einer hohen Ebene berechnet (eindeutige Berechnung des x/y-Ableitungspaars für jedes Pixel in einem 2x2-Quad). Diese Anweisung und [deriv \_ rty \_ fine](deriv-rty-fine--sm5---asm-.md) sind Alternativen zu [deriv \_ rtx \_ coarse](deriv-rtx-coarse--sm5---asm-.md) und [deriv \_ rty \_ coarse](deriv-rty-coarse--sm5---asm-.md). Diese \_ groben und \_ feinen Ableitungsanweisungen sind ein Ersatz für **deriv \_ rtx** Diese \_ groben und \_ feinen Ableitungsanweisungen sind ein Ersatz für **deriv \_ rtx** und **deriv \_ rty** von früheren Shadermodellen.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

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

 

 





