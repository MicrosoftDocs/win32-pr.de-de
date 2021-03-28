---
title: ddiv (SM5-ASM)
description: Berechnet eine Komponenten Weise Division mit doppelter Genauigkeit.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f5c3aae9d416d24f41de8d8308c5a69be9d016
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993015"
---
# <a name="ddiv-sm5---asm"></a>ddiv (SM5-ASM)

Berechnet eine Komponenten Weise Division mit doppelter Genauigkeit.



| ddiv \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[im \] Ergebnis des Vorgangs. Der Ergebniswert muss auf 0,5 ULP genau sein. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der Dividende.<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[im \] Divisor.<br/>                                                                |



 

## <a name="remarks"></a>Bemerkungen

Die ddiv-Anweisung wird vom HLSL-Compiler immer dann ausgegeben, wenn der Divisions Operator mit Double-Wert verwendet wird. Die Genauigkeit dieser Anweisung muss 0,5 ULP sein.

Shader, die diese Anweisung verwenden, werden mit einem shaderflag gekennzeichnet, das dazu führt, dass Sie nicht gebunden werden, es sei denn, die folgenden Bedingungen sind erfüllt.

-   Das System unterstützt DirectX 11,1.
-   Das System enthält einen WDDM 1,2-Treiber.
-   Der Treiber meldet die Unterstützung für diese Anweisung über **D3D11 \_ Feature \_ Data \_ D3D11 \_ options. "Extendeddoublesshaderinstructions** " ist auf " **true**" festgelegt.

In der folgenden Tabelle werden die Ergebnisse angezeigt, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen aufgetreten sind. dabei wird davon ausgegangen, dass weder Überlauf noch Unterlauf auftreten.

In dieser Tabelle steht F für eine endliche reelle Zahl.



|                     |          |        |          |        |        |          |        |          |         |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| **src0 Quelle1->** | **-INF** | **-F** | **-1,0** | **-0** | **+0** | **+ 1,0** | **+ F** | **+ INF** | **NaN** |
| **-INF**            | NaN      | +inf   | +inf     | +inf   | -inf   | -inf     | -inf   | NaN      | NaN     |
| **-F**              | +0       | + F     | -src0    | +inf   | -inf   | src0     | -F     | -0       | NaN     |
| **-0**              | +0       | +0     | +0       | NaN    | NaN    | -0       | -0     | -0       | NaN     |
| **+0**              | -0       | -0     | -0       | NaN    | NaN    | +0       | +0     | +0       | NaN     |
| **+ F**              | -0       | -F     | -src0    | -inf   | +inf   | src0     | + F     | +0       | NaN     |
| **+ INF**            | NaN      | -inf   | -inf     | -inf   | +inf   | +inf     | +inf   | NaN      | NaN     |
| **NaN**             | NaN      | NaN    | NaN      | NaN    | NaN    | NaN      | NaN    | NaN      | NaN     |



 

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

 

 





