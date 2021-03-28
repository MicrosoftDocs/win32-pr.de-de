---
title: DRCP (SM5-ASM)
description: Berechnet eine gegenseitige Komponenten Weise doppelte Genauigkeit.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b678f4e8b3464817215de9132298fdde1f6feec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313692"
---
# <a name="drcp-sm5---asm"></a>DRCP (SM5-ASM)

Berechnet eine gegenseitige Komponenten Weise doppelte Genauigkeit.



| RCP \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse der Ergebnisse<br/> *dest*  =  **1,0**  /  *src0*. Der Ergebniswert muss auf 1,0 ULP genau sein.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der Zahl, von der die gegenseitige übernommen wird.<br/>                                                                         |



 

## <a name="remarks"></a>Bemerkungen

Die DRCP-Anweisung wird vom HLSL-Compiler nur ausgegeben, wenn Sie explizit über die systeminterne Funktion RCP () aufgerufen wird, wenn ein Double als Argument verwendet wird. Die Genauigkeit dieser Anweisung muss 1,0 ULP sein.

Shader, die diese Anweisung verwenden, werden mit einem shaderflag gekennzeichnet, das dazu führt, dass Sie nicht gebunden werden, es sei denn, die folgenden Bedingungen sind erfüllt.

-   Das System unterstützt DirectX 11,1.
-   Das System enthält einen WDDM 1,2-Treiber.
-   Der Treiber meldet die Unterstützung für diese Anweisung über **D3D11 \_ Feature \_ Data \_ D3D11 \_ options. "Extendeddoublesshaderinstructions** " ist auf " **true**" festgelegt.

In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt

In dieser Tabelle steht F für eine endliche reelle Zahl.



|               |          |        |        |        |        |          |         |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| **src**->  | **-INF** | **-F** | **-0** | **+0** | **+ F** | **+ INF** | **NaN** |
| **dest**-> | -0       | -F     | -inf   | +inf   | + F     | +0       | NaN     |



 

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

 

 





