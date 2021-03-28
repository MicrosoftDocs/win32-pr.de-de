---
title: dcl_maxOutputVertexCount (SM4-ASM)
description: DCL \_ maxoutputvertexcount (SM4-ASM)
ms.assetid: 91eb2dfc-f4ff-4f23-9cb4-ec5fdb676157
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31a09788b2f407673f57dad8a71792a5b02b7613
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993223"
---
# <a name="dcl_maxoutputvertexcount-sm4---asm"></a>DCL \_ maxoutputvertexcount (SM4-ASM)

Deklariert die maximale Anzahl von Vertices, die von einem Geometry-Shader ausgegeben werden können.



| DCL- \_ maxoutputvertexcount- *Anzahl* |
|-----------------------------------|



 



| Element                                                               | BESCHREIBUNG                                                             |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="count"></span><span id="COUNT"></span>*Countdown*<br/> | \[in \] einer 32-Bit-Ganzzahl ohne Vorzeichen zwischen 1 und n (einschließlich).<br/> |



 

Ein Geometry-Shader kann maximal 1024 32-Bit-Werte ausgeben. Diese maximale Größe schließt die Größe der Eingabedaten und die Größe der vom Shader erstellten Daten ein.

Es folgen einige Einschränkungen:

-   Wenn die Anzahl der Scheitel Punkte erreicht wird, bevor der Geometrie-Shader die Ausführung beendet, wird der Shader beendet.
-   Ein Geometry-Shader kann das Ende seines Programms erreichen, bevor er Vertices ausstellt. Dies ist absolut zulässig.
-   Wenn Sie einen Geometry-Shader Debuggen, können Sie die Anzahl der generierten Scheitel Punkte ermitteln, indem Sie die Anzahl der generierten ausgangsweisungen zählen.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               | x               |              |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.

## <a name="example"></a>Beispiel

Hier einige Beispiele.

Nehmen Sie an, dass die Eingabedaten aus der Position (. xyzw) und der Farbe (RGB) erstellt wurden. Jede Komponente verwendet ein Byte. bei 7 Bytes beträgt die maximale Anzahl von Vertices, die der Shader generieren kann, 1024/(4 + 3) = 146.


```
dcl_maxOutputVertexCount 146
```



Angenommen, Ihr Geometry-Shader erstellt 32 4-komponentenvektoren. Die maximale Anzahl der Scheitel Punkte, die der Shader generieren kann, ist 1024/(32 \* 4) = 8.


```
dcl_maxOutputVertexCount 8
```



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

 

 





