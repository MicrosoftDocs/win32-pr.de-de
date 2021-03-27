---
title: dcl_sampler (SM4-ASM)
description: DCL \_ -Sampler (SM4-ASM)
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 45b6da3bcdb027a00edeb4f009773533424efeb8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104391115"
---
# <a name="dcl_sampler-sm4---asm"></a>DCL \_ -Sampler (SM4-ASM)

Deklariert ein Samplerregister.



| DCL- \_ samplersn, Modus |
|-----------------------|



 



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
<td><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em><br/></td>
<td>in Ein Samplerregister, wobei <em>N</em> eine ganze Zahl ist, die die Registernummer bezeichnet.<br/></td>
</tr>
<tr class="even">
<td><span id="mode"></span><span id="MODE"></span><em>Spar</em><br/></td>
<td>in Ein Samplingmodus, der einschränkt, welche samplerzustände (aufgelistet in den Mitgliedern von <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) berücksichtigt werden. Die Modi und Zustände werden in der folgenden Tabelle aufgeführt.<br/> 
<table>
<thead>
<tr class="header">
<th>Modus</th>
<th>Samplerzustände berücksichtigt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>default</td>
<td><em>Filter</em> (kann nicht die Werte _COMPARISON oder _TEXT verwenden), <em>adressssu/V/W</em>, <em>minlod/maxlod</em>, <em>miplodbias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></td>
</tr>
<tr class="even">
<td>Vergleich</td>
<td><em>Filter</em>, <em>comparisonfunction</em>, <em>adressssu/V/W</em>, <em>minlod, maxlod</em>, <em>miplodbias</em>, <em>MaxAnisotropy</em>, <em>BorderColor [4]</em></td>
</tr>
<tr class="odd">
<td>ein</td>
<td><em>Filter</em> (muss einer der _text Werte sein), <em>monofilterwidth</em>, <em>monofilterheight</em> (diese beiden Zustände sind Global Device State), <em>minlod</em>, <em>miplodbias</em>, <em>MaxAnisotropy</em></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

Der Modus schränkt die Beispiel Anweisungen ein, die verwendet werden können. in dieser Tabelle werden die Textur Objektmethoden aufgelistet, die für die einzelnen Modi unterstützt werden.



| Ein Sampler, der in diesem Modus ausgeführt wird. | Kann diese Texture-Object Methoden verwenden                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| default                          | [Sample](dx-graphics-hlsl-to-sample.md), [samplelevel](dx-graphics-hlsl-to-samplelevel.md), [samplegrad](dx-graphics-hlsl-to-samplegrad.md) |
| Vergleich                       | [Samplecmp](dx-graphics-hlsl-to-samplecmp.md), [samplecmplevelzero](dx-graphics-hlsl-to-samplecmplevelzero.md)                               |
| ein                             | [Samplelevel](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x\*          |



 

\* -Die Verwendung eines Samplers im Mono-Modus wird nur in einem Pixelshader unterstützt.

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.

## <a name="example"></a>Beispiel

Beispiel:


```
dcl_sampler s3, default
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

 

