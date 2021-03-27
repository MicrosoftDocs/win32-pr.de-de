---
title: verwerfen (SM4-ASM)
description: Markieren Sie die Ergebnisse des Pixel-Shaders bedingt, damit Sie verworfen werden, wenn das Ende des Programms erreicht ist.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d98365ae6d80710f15cf7204f98d810be30a13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948315"
---
# <a name="discard-sm4---asm"></a>verwerfen (SM4-ASM)

Markieren Sie die Ergebnisse des Pixel-Shaders bedingt, damit Sie verworfen werden, wenn das Ende des Programms erreicht ist.



| { \_ z \ verwerfen|\_NZ} src0. Select- \_ Komponente |
|-------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[\]der Wert, der bestimmt, ob das aktuelle Pixel, das verarbeitet wird, verworfen werden soll.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung gibt das aktuelle Pixel als beendet an, während die Ausführung fortgesetzt wird, sodass andere gleichzeitig ausgeführte Pixel ggf. Ableitungen erhalten können. Obwohl die Ausführung fortgesetzt wird, werden alle Pixel-Shader-Ausgaben geschrieben, bevor oder nachdem die **Verwerfungs** Anweisung verworfen wurde.

Bei **Verwerfen von \_ z**, wenn alle Bits in *src0. Select \_ Component* gleich 0 (null) sind, wird das Pixel verworfen.

Bei **Verwerfen von \_ NZ** wird das Pixel verworfen, wenn Bits in *src0. Select- \_ Komponente* ungleich NULL sind.

Außerdem kann die **Verwerfungs** Anweisung in jedem Fluss Steuerungs Konstrukt vorhanden sein.

In einem Shader sind möglicherweise mehrere **Verwerfungs** Anweisungen vorhanden, und wenn eine ausgeführt wird, wird das Pixel beendet.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





