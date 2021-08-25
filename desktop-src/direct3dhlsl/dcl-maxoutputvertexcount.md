---
title: dcl_maxOutputVertexCount (sm4 – asm)
description: dcl \_ maxOutputVertexCount (sm4 - asm)
ms.assetid: 91eb2dfc-f4ff-4f23-9cb4-ec5fdb676157
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ba7783575ac5782c63bc1ec3ca5f56f6ffe9a1bc7483f3f01ccbcf8adac5e23f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068520"
---
# <a name="dcl_maxoutputvertexcount-sm4---asm"></a>dcl \_ maxOutputVertexCount (sm4 - asm)

Deklariert die maximale Anzahl von Scheitelpunkten, die von einem Geometrie-Shader ausgegeben werden können.



| dcl \_ maxOutputVertexCount *count* |
|-----------------------------------|



 



| Element                                                               | BESCHREIBUNG                                                             |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="count"></span><span id="COUNT"></span>*Count*<br/> | \[in \] einer 32-Bit-Ganzzahl ohne Vorzeichen zwischen 1 und n (einschließlich).<br/> |



 

Ein geometriebasierter Shader kann maximal 1024 32-Bit-Werte ausgeben. Dieses Maximum schließt die Größe der Eingabedaten und die Größe der vom Shader erstellten Daten ein.

Hier sind einige Einschränkungen:

-   Wenn die Anzahl der Scheitelpunkte erreicht ist, bevor die Ausführung des Geometry-Shaders abgeschlossen ist, wird der Shader beendet.
-   Ein geometry-shader kann das Ende des Programms erreichen, bevor er Scheitelpunkte ausgibt. dies ist völlig zulässig.
-   Wenn Sie einen Geometrie-Shader debuggen, können Sie die Anzahl der generierten Scheitelpunkte angeben, indem Sie die Anzahl der generierten Emit-Anweisungen zählen.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               | x               |              |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Sie können keinen Shader in der Assemblysprache mit shader Model 4 erstellen.

## <a name="example"></a>Beispiel

Beispiele:

Angenommen, Eingabedaten bestehen aus Position (.xyzw) und Farbe (.rgb). Jede Komponente verbraucht ein Byte. bei 7 Bytes beträgt die maximale Anzahl von Scheitelpunkten, die der Shader generieren kann, 1024 / (4 + 3) = 146.


```
dcl_maxOutputVertexCount 146
```



Angenommen, Ihr Geometrie-Shader erstellt 32 Vektoren mit vier Komponenten. Die maximale Anzahl von Scheitelpunkten, die der Shader generieren kann, wäre 1024 / (32 \* 4) = 8.


```
dcl_maxOutputVertexCount 8
```



## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





