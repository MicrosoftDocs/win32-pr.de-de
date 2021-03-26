---
title: Dadd (SM5-ASM)
description: Komponenten weises addieren mit doppelter Genauigkeit.
ms.assetid: 416F1103-E27B-4AFC-9ED1-492FF8A93492
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e217a03a5ba9e4da0d365bbfd15e4283f1a69cb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389499"
---
# <a name="dadd-sm5---asm"></a>Dadd (SM5-ASM)

Komponenten weises addieren mit doppelter Genauigkeit.



| Dadd \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des Vorgangs Ergebnisses.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den Komponenten, die mit *Quelle1* hinzugefügt werden sollen.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] den Komponenten, die mit *src0* hinzugefügt werden sollen<br/>           |



 

## <a name="remarks"></a>Bemerkungen

Die gültigen Werte für die Quellparameter lauten ". xyzw", ". xyxy", ". zwxy", ". zwzw". Die gültigen *dest* -Masken sind. XY,. zw und. xyzw. Die folgenden Zuordnungen sind Post-Swizzle:

-   *dest* ist eine doppelte vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).
-   *src0* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).
-   *Quelle1* ist ein doppeltes vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).

In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt

F bedeutet eine endliche reelle Zahl.



<table>
<tbody>
<tr class="odd">
<td><dl> <strong>src0</strong><br />
<strong>Quelle1-></strong><br />
</dl></td>
<td><strong>-INF</strong></td>
<td><strong>-F</strong></td>
<td><strong>-0</strong></td>
<td><strong>+0</strong></td>
<td><strong>+ F</strong></td>
<td><strong>+ INF</strong></td>
<td><strong>NaN</strong></td>
</tr>
<tr class="even">
<td><strong>-INF</strong></td>
<td>-inf</td>
<td>-inf</td>
<td>-inf</td>
<td>-inf</td>
<td>-inf</td>
<td>NaN</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td><strong>-F</strong></td>
<td>-inf</td>
<td>-F</td>
<td>src0</td>
<td>src0</td>
<td>+-F oder +-0</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="even">
<td><strong>-0</strong></td>
<td>-inf</td>
<td>src1</td>
<td>-0</td>
<td>+0</td>
<td>src1</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td><strong>+0</strong></td>
<td>-inf</td>
<td>src1</td>
<td>+0</td>
<td>+0</td>
<td>src1</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="even">
<td><strong>+ F</strong></td>
<td>-inf</td>
<td>+-F oder +-0</td>
<td>src0</td>
<td>src0</td>
<td>+ F</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td><strong>+ INF</strong></td>
<td>NaN</td>
<td>+inf</td>
<td>+inf</td>
<td>+inf</td>
<td>+inf</td>
<td>+inf</td>
<td>NaN</td>
</tr>
<tr class="even">
<td><strong>NaN</strong></td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
</tr>
</tbody>
</table>



 

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

 

 





