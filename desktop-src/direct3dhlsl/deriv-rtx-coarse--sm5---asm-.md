---
title: deriv_rtx_coarse (SM5-ASM)
description: Berechnet die Änderungs Rate der Komponenten. | deriv_rtx_coarse (SM5-ASM)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2355b6db6aef9e85959d6359053fea76b48af0a5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995398"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a>DERIV \_ RTX \_ grob (SM5-ASM)

Berechnet die Änderungs Rate der Komponenten.



| DERIV \_ RTX \_ grob \[ \_ sa \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , |
|----------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den Komponenten des Vorgangs.<br/>             |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung berechnet die Rate der Inhalts Änderungen jeder float32-Komponente von *src0* (Post-Swizzle) in Bezug auf die Richtung renderTarget x Direction (RTX) oder renderTarget y (siehe [DERIV \_ Eigenschaft \_ grob](deriv-rty-coarse--sm5---asm-.md)). Nur ein einzelnes x-, y-abgeleitetes Paar wird für jeden 2 x 2-Stempel von Pixel berechnet.

Die Daten im aktuellen pixelshaderaufruf können nicht an der Berechnung der angeforderten Ableitung beteiligt sein, da die Ableitung nur einmal pro 2 x 2 Quad berechnet wird. Beispielsweise könnte die x-Ableitung ein Delta von der obersten Zeile der Pixel sein, und die y-Richtung ([DERIV \_ Eigenschaft \_ grob](deriv-rty-coarse--sm5---asm-.md)) kann ein Delta aus der linken Spalte der Pixel sein. Die genaue Berechnung erfolgt bis zum Hardwarehersteller. Es gibt auch keine Angabe, wie die 2 x 2-Quads über einen primitiven ausgerichtet oder gekachelt werden.

Ableitungen werden auf einer groben Ebene berechnet, einmal pro 2 x 2 Pixel Quad. Diese Anweisung und [DERIV \_ Eigenschaft \_ grob](deriv-rty-coarse--sm5---asm-.md) sind Alternativen zu [DERIV \_ RTX \_ Fine](deriv-rtx-fine--sm5---asm-.md) und [DERIV \_ Eigenschaft \_ ](deriv-rty-fine--sm5---asm-.md). Diese \_ groben und differenzierten \_ Anweisungen sind ein Ersatz für **DERIV \_ rtxderiv \_ Eigenschaft** aus früheren shadermodellen.

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

 

 





