---
title: dmul (SM5-ASM)
description: Multiplizieren der Komponenten Weise mit doppelter Genauigkeit.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18cce59ae237610b1038d90e02dff429812b4f00
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993054"
---
# <a name="dmul-sm5---asm"></a>dmul (SM5-ASM)

Multiplizieren der Komponenten Weise mit doppelter Genauigkeit.



| dmul \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des Vorgangs Ergebnisses.<br/> *dest*  =  *src0* \* *Quelle1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den Komponenten, die mit *Quelle1* multipliziert werden sollen.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] den Komponenten, die mit *src0* multipliziert werden sollen.<br/>                                          |



 

## <a name="remarks"></a>Bemerkungen

Die gültigen Werte für die Quellparameter lauten ". xyzw", ". xyxy", ". zwxy", ". zwzw". Die gültigen *dest* -Masken sind. XY,. zw und. xyzw. Die folgenden *src* -Zuordnungen sind Post-Swizzle:

-   *dest* ist eine doppelte vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).
-   *src0* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).
-   *Quelle1* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).

In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt

F bedeutet eine endliche reelle Zahl.



|                    |          |        |          |        |        |          |        |          |         |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| **src0 Quelle1->** | **-INF** | **-F** | **-1,0** | **-0** | **+0** | **+ 1,0** | **+ F** | **+ INF** | **NaN** |
| **-INF**           | +inf     | +inf   | +inf     | NaN    | NaN    | -inf     | -inf   | -inf     | NaN     |
| **-F**             | +inf     | + F     | -src0    | +0     | -0     | src0     | -F     | -inf     | NaN     |
| **-1.0 f**          | +inf     | -Quelle1  | + 1,0     | +0     | -0     | -1.0     | -Quelle1  | -inf     | NaN     |
| **-0**             | NaN      | +0     | +0       | +0     | -0     | -0       | -0     | NaN      | NaN     |
| **+0**             | NaN      | -0     | -0       | -0     | +0     | +0       | +0     | NaN      | NaN     |
| **+ 1,0**           | -inf     | src1   | -1.0     | -0     | +0     | +1       | src1   | +inf     | NaN     |
| **+ F**             | -inf     | -F     | -src0    | -0     | +0     | src0     | + F     | +inf     | NaN     |
| **+ INF**           | -inf     | -inf   | -inf     | NaN    | NaN    | +inf     | +inf   | +inf     | NaN     |
| **NaN**            | NaN      | NaN    | NaN      | NaN    | NaN    | NaN      | NaN    | NaN      | NaN     |



 

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

 

 





