---
title: drcp (sm5 – asm)
description: Berechnet einen komponentenweisen Kehrwert mit doppelter Genauigkeit.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 770159f5007b08f5482ba8b58634b44e7f3e6ef0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998337"
---
# <a name="drcp-sm5---asm"></a>drcp (sm5 – asm)

Berechnet einen komponentenweisen Kehrwert mit doppelter Genauigkeit.



| rcp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse der Ergebnisse<br/> *dest*  =  **1.0**  /  *src0*. Der Ergebniswert muss auf 1,0 ULP genau sein.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Zahl, von der der Kehrwert annimmt wird.<br/>                                                                         |



 

## <a name="remarks"></a>Hinweise

Die DRCP-Anweisung wird vom HLSL-Compiler nur ausgegeben, wenn sie explizit über die systeminterne rcp()-Anweisung aufgerufen wird, wenn ein Double als Argument verwendet wird. Die Genauigkeit dieser Anweisung muss 1,0 ULP sein.

Shader, die diese Anweisung verwenden, werden mit einem Shaderflag gekennzeichnet, das dazu führt, dass sie nicht gebunden werden, es sei denn, alle folgenden Bedingungen sind erfüllt.

-   Das System unterstützt DirectX 11.1.
-   Das System enthält einen WDDM 1.2-Treiber.
-   Der Treiber meldet Unterstützung für diese Anweisung über **D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** ist auf **TRUE** festgelegt.

Die folgende Tabelle zeigt die Ergebnisse, die beim Ausführen der Anweisung mit verschiedenen Klassen von Zahlen erzielt werden, vorausgesetzt, dass weder Überlauf noch Unterlauf auftreten.

In dieser Tabelle bedeutet F endliche reelle Zahl.



| **Src**->  | **-inf** | **-F** | **-0** | **+0** | **+F** | **+inf** | **NaN** |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| **Dest**-> | -0       | -F     | -inf   | +inf   | +F     | +0       | NaN     |



 

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





