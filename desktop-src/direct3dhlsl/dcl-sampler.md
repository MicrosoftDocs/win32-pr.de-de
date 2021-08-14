---
title: dcl_sampler (sm4 – asm)
description: dcl \_ sampler (sm4 – asm)
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e0e04558c9ca1c10f89e924605c8999a7f7346d2278850d7cd6449968fd13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515539"
---
# <a name="dcl_sampler-sm4---asm"></a>dcl \_ sampler (sm4 – asm)

Deklariert ein Samplerregister.



| dcl \_ sampler sN, mode |
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
<td>[in] Ein Samplerregister, wobei <em>N</em> eine ganze Zahl ist, die die Registernummer angibt.<br/></td>
</tr>
<tr class="even">
<td><span id="mode"></span><span id="MODE"></span><em>Modus</em><br/></td>
<td>[in] Ein Samplermodus, der einschränkt, welche Samplerzustände (in den Membern von <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>aufgeführt) berücksichtigt werden. Die Modi und Zustände sind in der folgenden Tabelle aufgeführt.<br/> 
<table>
<thead>
<tr class="header">
<th>Mode</th>
<th>Samplerzustände berücksichtigt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>default</td>
<td><em>Filter</em> (darf nicht die werte _COMPARISON oder _TEXT), <em>AddressU/V/W,</em> <em>MinLOD/MaxLOD,</em> <em>MipLODBias,</em> <em>MaxAnisotropy,</em> <em>BorderColor[4]</em></td>
</tr>
<tr class="even">
<td>Vergleich</td>
<td><em>Filter,</em> <em>ComparisonFunction,</em> <em>AddressU/V/W,</em> <em>MinLOD, MaxLOD,</em> <em>MipLODBias,</em> <em>MaxAnisotropy,</em> <em>BorderColor[4]</em></td>
</tr>
<tr class="odd">
<td>Mono</td>
<td><em>Filter</em> (muss einer der _TEXT-Werte sein), <em>MonoFilterWidth,</em> <em>MonoFilterHeight</em> (diese beiden Zustände sind der globale Gerätestatus), <em>MinLOD,</em> <em>MipLODBias,</em> <em>MaxAnisotropy</em></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

Der Modus schränkt die Beispielanweisungen ein, die verwendet werden können. In dieser Tabelle sind die Texturenobjektmethoden aufgeführt, die für jeden Modus unterstützt werden.



| Ein Sampler, der in diesem Modus ausgeführt wird | Kann diese Texture-Object Methoden verwenden                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| default                          | [Beispiel,](dx-graphics-hlsl-to-sample.md) [SampleLevel,](dx-graphics-hlsl-to-samplelevel.md) [SampleGrad](dx-graphics-hlsl-to-samplegrad.md) |
| Vergleich                       | [SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                               |
| Mono                             | [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x\*          |



 

\* – Die Verwendung eines Samplers im Mono-Modus wird nur in einem Pixel-Shader unterstützt.

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Sie können keinen Shader in der Assemblysprache mit shader Model 4 erstellen.

## <a name="example"></a>Beispiel

Beispiel:


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

