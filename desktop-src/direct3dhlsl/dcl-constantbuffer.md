---
title: dcl_constantBuffer (SM4-ASM)
description: DCL \_ constantbuffer (SM4-ASM)
ms.assetid: 164fb2a4-8782-42f0-b4ba-1f87d9c7255d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2eeb9368af0121ee61fde5d106eb0f3b08e5acb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101094"
---
# <a name="dcl_constantbuffer-sm4---asm"></a>DCL \_ constantbuffer (SM4-ASM)

Deklariert einen Shader-Konstantenpuffer.



| DCL \_ constantbuffer *CBN \[ - \] Größe*, *accesspattern* |
|----------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>CB<em>N [Größe]</em><br/></td>
<td>in Ein Shader-Konstantenpuffer, bei dem N eine ganze Zahl ist, die die Anzahl und Größe des Konstanten Puffers angibt, ist eine ganze Zahl, die die Anzahl der Elemente im Puffer angibt.<br/></td>
</tr>
<tr class="even">
<td><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>Accesspattern</em><br/></td>
<td>in Der Zugriff auf den Puffer erfolgt über den Shader-Code, der eines der folgenden ist: <br/> 
<table>
<thead>
<tr class="header">
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>sofort eingepackt</td>
<td>Indizieren Sie den Puffer mit einem Literalwert.</td>
</tr>
<tr class="even">
<td>dynamic_indexed</td>
<td>Indizieren Sie den Puffer mit dem Ergebnis eines ausgewerteten Ausdrucks.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.

## <a name="example"></a>Beispiel

In diesem Beispiel wird ein konstanter Puffer für Register CB0 mit 19 Elementen deklariert. Auf diese Elemente wird mit einem literalen Index zugegriffen.


```
dcl_constantbuffer  cb0[19], immediateIndexed
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

 

 





