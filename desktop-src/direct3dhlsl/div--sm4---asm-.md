---
title: div (SM4-ASM)
description: Komponenten Weise Aufteilung.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 332d494adc2cc9bebe2e714b47ff2c5a6b299966
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038328"
---
# <a name="div-sm4---asm"></a>div (SM4-ASM)

Komponenten Weise Aufteilung.



| div \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] \[ - \] Quelle1 \[ \_ ABS \] \[ . Swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[im \] Ergebnis des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der Dividende.<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[im \] Divisor.<br/>                 |



 

## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle werden die Ergebnisse angezeigt, die bei der Ausführung der Anweisung mit verschiedenen Klassen von Zahlen erzielt wurden, vorausgesetzt, dass weder ein Überlauf noch ein Unterlauf auftritt

Beachten Sie die beiden zulässigen Implementierungen von dividieren: a/b und a \* (1/b).

Ein Ergebnis hierfür ist, dass für große nennenwerte (größer als 8.5070592 e + 37) Ausnahmen von der folgenden Tabelle vorliegen, wobei 1/Nenner ein denorm ist. Da Implementierungen möglicherweise eine Teilung als \* (1/b) statt direkt a/b ausführen, und 1/ \[ großer Wert \] ein denorm ist, das geleert werden könnte, würden einige Fälle in der Tabelle zu unterschiedlichen Ergebnissen führen. Beispiel: (+/-) inf/(+/-)- \[ Wert > 8.5070592 e + 37 \] kann Nan für einige Implementierungen, aber (+/-) inf für andere Implementierungen verursachen.

In dieser Tabelle steht F für eine endliche reelle Zahl.



|                     |          |            |             |        |        |             |            |          |         |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| **src0 Quelle1->** | **-INF** | **-F**     | **-denorm** | **-0** | **+0** | **+ denorm** | **+ F**     | **+ INF** | **Ji** |
| **-INF**            | -inf     | -inf       | -inf        | -inf   | -inf   | -inf        | -inf       | NaN      | NaN     |
| **-F**              | -inf     | -F         | src0        | src0   | src0   | src0        | +-F oder +-0 | +inf     | NaN     |
| **-denorm**         | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **-0**              | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **+0**              | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+ denorm**         | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+ F**              | -inf     | +-F oder +-0 | src0        | src0   | src0   | src0        | + F         | +inf     | NaN     |
| **+ INF**            | NaN      | +inf       | +inf        | +inf   | +inf   | +inf        | +inf       | +inf     | NaN     |
| **NaN**             | NaN      | NaN        | NaN         | NaN    | NaN    | NaN         | NaN        | NaN      | NaN     |



 

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





