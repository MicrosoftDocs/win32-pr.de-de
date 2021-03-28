---
title: deriv_rtx_fine (SM5-ASM)
description: Berechnet die Änderungs Rate der Komponenten. | deriv_rtx_fine (SM5-ASM)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73061e3220704cf2c19e28b4d6d434fda43fb941
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995607"
---
# <a name="deriv_rtx_fine-sm5---asm"></a>DERIV \_ RTX \_ einwandfrei (SM5-ASM)

Berechnet die Änderungs Rate der Komponenten.



| DERIV \_ RTX \_ fein \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , |
|--------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den Komponenten des Vorgangs.<br/>             |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung berechnet die Rate der Inhalts Änderungen jeder float32-Komponente von *src0* (Post-Swizzle) in Bezug auf die Richtung renderTarget x Direction (RTX) oder renderTarget y (siehe [DERIV \_ Eigenschaft \_ Fine](deriv-rty-fine--sm5---asm-.md)). Jedes Pixel im 2 x 2-Stempel erhält ein eindeutiges Paar von x/y-abgeleiteten Berechnungen.

Die Daten im aktuellen Pixelshader-Aufruf sind immer an der Berechnung der angeforderten Ableitung beteiligt. Im 2 x 2-Pixel-Quad liegt das aktuelle Pixel in. die x-Ableitung ist das Delta der Zeile von 2 Pixeln, einschließlich des aktuellen Pixels. Die y-Ableitung ist das Delta der Spalte mit 2 Pixeln, einschließlich des aktuellen Pixels. Es gibt keine Spezifikation, die bestimmt, wie die 2 x 2-Quads durch ein primitiv ausgerichtet oder gekachelt werden.

Ableitungen werden auf feiner Ebene berechnet (eindeutige Berechnung des x/y-abgeleiteten Paars für jedes Pixel in einem 2 x 2 Quad). Diese Anweisung und [DERIV \_ Eigenschaft \_ ](deriv-rty-fine--sm5---asm-.md) sind Alternativen zu [DERIV \_ RTX \_ grob](deriv-rtx-coarse--sm5---asm-.md) und [DERIV \_ Eigenschaft \_ grob](deriv-rty-coarse--sm5---asm-.md). Diese \_ groben und differenzierten \_ Anweisungen sind ein Ersatz für **DERIV \_ RTX** . diese \_ groben und differenzierten \_ Anweisungen sind ein Ersatz für **DERIV \_ RTX** und **DERIV \_ Eigenschaft** aus früheren Shader-Modellen.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

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

 

 





