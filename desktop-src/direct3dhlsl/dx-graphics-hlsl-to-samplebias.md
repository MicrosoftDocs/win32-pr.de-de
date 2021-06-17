---
title: SampleBias (DirectX HLSL-Texturobjekt)
description: Samples a texture, after applying the input bias to the mipmap level.
ms.assetid: 1bc03ad8-7b69-4001-81c7-64d8c631d68d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01087ab36bdbe90ff73643899229c7ec6ccfbdbe
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826795"
---
# <a name="samplebias-directx-hlsl-texture-object"></a>SampleBias (DirectX HLSL-Texturobjekt)

Samples a texture, after applying the input bias to the mipmap level.

&lt;Vorlagentyp &gt; Object.SampleBias( \_ Samplerzustand S, float Location, float Bias \[ , int Offset \] );



 

## <a name="parameters"></a>Parameter



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em><br/></td>
<td>Beliebiger <a href="dx-graphics-hlsl-to-type.md">Texturobjekttyp</a> (außer Texture2DMS und Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>S</em><br/></td>
<td>[in] Ein <a href="dx-graphics-hlsl-sampler.md">Samplerzustand.</a> Dies ist ein Objekt, das in einer Effektdatei deklariert ist, die Zustandszuweisungen enthält.<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Lage</em><br/></td>
<td>[in] Die Texturkoordinaten. Der Argumenttyp ist vom Texturobjekttyp abhängig. <br/> 
<table>
<thead>
<tr class="header">
<th>Texture-Object Typ</th>
<th>Parametertyp</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D</td>
<td>float</td>
</tr>
<tr class="even">
<td>Texture1DArray, Texture2D</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture2DArray, Texture3D, TextureCube</td>
<td>float3</td>
</tr>
<tr class="even">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Vorurteil</em></p></td>
<td><p>[in] Der Biaswert, bei dem es sich um eine Gleitkommazahl zwischen -16,0 und 15,99 handelt, wird vor der Stichprobenentnahme auf eine MIP-Ebene angewendet.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></p></td>
<td><p>[in] Ein optionaler Texturkoordinatenoffset, der für jeden Texturobjekttyp verwendet werden kann. Der Offset wird vor der Stichprobenentnahme auf die Position angewendet. Die Texturoffsets müssen statisch sein. Der Argumenttyp ist vom Texturobjekttyp abhängig. Weitere Informationen finden Sie unter <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Anwenden von Texturkoordinatenoffsets.</a></p>

<table>
<thead>
<tr class="header">
<th>Texture-Object Typ</th>
<th>Parametertyp</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>INT</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
</tr>
<tr class="odd">
<td>Texture3D</td>
<td>int3</td>
</tr>
<tr class="even">
<td>TextureCube, TextureCubeArray </td>
<td>Nicht unterstützt</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Rückgabewert

Der Vorlagentyp der Textur, der ein Vektor mit einer oder mehreren Komponenten sein kann. Das Format basiert auf dem DXGI FORMAT der [**\_ Textur.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x        | x         |          |           |



 

1.  TextureCubeArray ist in Shader Model 4.1 oder höher verfügbar.
2.  ShaderModell 4.1 ist in Direct3D 10.1 oder höher verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texture-Object](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

