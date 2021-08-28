---
title: dcl_sampler (sm4 - asm)
description: dcl \_ sampler (sm4 - asm)
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cb3835e1c0e2cfb5ffbb49523617b9d233810494
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627096"
---
# <a name="dcl_sampler-sm4---asm"></a>dcl \_ sampler (sm4 - asm)

Deklariert ein Samplerregister.



| dcl \_ sampler sN, mode |
|-----------------------|



 



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em><br/></td>
<td>[in] Ein Samplerregister, wobei <em>N</em> eine ganze Zahl ist, die die Registernummer angibt.<br/></td>
</tr>
<tr class="even">
<td><span id="mode"></span><span id="MODE"></span><em>Modus</em><br/></td>
<td>[in] Ein Samplermodus, der einschränkt, welche Samplerzustände (in den Membern D3D10_SAMPLER_DESC <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>aufgeführt)</strong></a>werden. Die Modi und Zustände sind in der folgenden Tabelle aufgeführt.<br/> 
<table>
<thead>
<tr class="header">
<th>Mode</th>
<th>"Sampler States Honored" (Zustände von Samplern)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>default</td>
<td><em>Filter</em> (verwendet nicht die werte _COMPARISON oder _TEXT), <em>AddressU/V/W,</em> <em>MinLOD/MaxLOD,</em> <em>MipLODBias,</em> <em>MaxAnisotropy,</em> <em>BorderColor[4]</em></td>
</tr>
<tr class="even">
<td>Vergleich</td>
<td><em>Filter</em>, <em>ComparisonFunction</em>, <em>AddressU/V/W</em>, <em>MinLOD, MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></td>
</tr>
<tr class="odd">
<td>Mono</td>
<td><em>Filter</em> (muss einer der _TEXT-Werte sein), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (diese beiden Zustände sind globaler Gerätestatus), <em>MinLOD,</em> <em>MipLODBias,</em> <em>MaxAnisotropy</em></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

Der Modus schränkt die Beispielanweisungen ein, die verwendet werden können. In dieser Tabelle sind die Texturobjektmethoden aufgeführt, die für jeden Modus unterstützt werden.



| Ein Sampler, der in diesem Modus ausgeführt wird | Kann diese Texture-Object verwenden                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| default                          | [Beispiel](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md) |
| Vergleich                       | [SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                               |
| Mono                             | [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | X\*          |



 

\* – Die Verwendung eines Samplers im Monomodus wird nur in einem Pixel-Shader unterstützt.

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu erleichtern. Sie können mit shader Model 4 keinen Shader in der Assemblysprache erstellen.

## <a name="example"></a>Beispiel

Beispiel:


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a>Minimales Shadermodell

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

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

