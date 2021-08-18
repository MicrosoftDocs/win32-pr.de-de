---
title: ddiv (sm5 – asm)
description: Berechnet eine komponentenweise Division mit doppelter Genauigkeit.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4730849b8ccc9070f538a58709bcd99fb9bfa552973c365fb3225806caf7aca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986660"
---
# <a name="ddiv-sm5---asm"></a>ddiv (sm5 – asm)

Berechnet eine komponentenweise Division mit doppelter Genauigkeit.



| ddiv \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Das Ergebnis des Vorgangs. Der Ergebniswert muss auf 0,5 ULP genau sein. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Der Dividend.<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Der Divisor.<br/>                                                                |



 

## <a name="remarks"></a>Hinweise

Die DDIV-Anweisung wird vom HLSL-Compiler ausgegeben, wenn der Divisionsoperator mit Doubles verwendet wird. Die Genauigkeit dieser Anweisung muss 0,5 ULP sein.

Shader, die diese Anweisung verwenden, werden mit einem Shaderflag gekennzeichnet, das dazu führt, dass sie nicht gebunden werden, es sei denn, alle folgenden Bedingungen sind erfüllt.

-   Das System unterstützt DirectX 11.1.
-   Das System enthält einen WDDM 1.2-Treiber.
-   Der Treiber meldet Unterstützung für diese Anweisung über **D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** ist auf **TRUE** festgelegt.

In der folgenden Tabelle sind die Ergebnisse aufgeführt, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen auftreten, vorausgesetzt, dass weder Überlauf noch Unterlauf auftreten.

In dieser Tabelle bedeutet F endliche reelle Zahl.



| **src0 src1 ->** | **-inf** | **-F** | **-1.0** | **-0** | **+0** | **+1.0** | **+F** | **+inf** | **NaN** |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| **-inf**            | NaN      | +inf   | +inf     | +inf   | -inf   | -inf     | -inf   | NaN      | NaN     |
| **-F**              | +0       | +F     | -src0    | +inf   | -inf   | src0     | -F     | -0       | NaN     |
| **-0**              | +0       | +0     | +0       | NaN    | NaN    | -0       | -0     | -0       | NaN     |
| **+0**              | -0       | -0     | -0       | NaN    | NaN    | +0       | +0     | +0       | NaN     |
| **+F**              | -0       | -F     | -src0    | -inf   | +inf   | src0     | +F     | +0       | NaN     |
| **+inf**            | NaN      | -inf   | -inf     | -inf   | +inf   | +inf     | +inf   | NaN      | NaN     |
| **NaN**             | NaN      | NaN    | NaN      | NaN    | NaN    | NaN      | NaN    | NaN      | NaN     |



 

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

 

 





