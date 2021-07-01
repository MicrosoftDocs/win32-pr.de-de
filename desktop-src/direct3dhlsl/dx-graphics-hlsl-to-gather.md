---
title: Gather (DirectX HLSL-Texturobjekt)
description: Ruft die vier Stichproben (nur rote Komponente) ab, die für die bilineare Interpolation beim Sampling einer Textur verwendet werden.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4659ba19e9fa950a659969f2491533858f4658fb
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120545"
---
# <a name="gather-directx-hlsl-texture-object"></a>Gather (DirectX HLSL-Texturobjekt)

Ruft die vier Stichproben (nur rote Komponente) ab, die für die bilineare Interpolation beim Sampling einer Textur verwendet werden.

&lt;Vorlagentyp &gt; 4 Object.Gather( \_ Samplerzustand S, float2 \| 3 \| 4 Location , \[ int2 Offset \] );



 

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
<td>Die folgenden <a href="dx-graphics-hlsl-to-type.md">Texturobjekttypen</a> werden unterstützt: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.<br/></td>
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
<td>Texture2D</td>
<td>float2</td>
</tr>
<tr class="even">
<td>Texture2DArray, TextureCube</td>
<td>float3</td>
</tr>
<tr class="odd">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></p></td>
<td><p>[in] Ein optionaler Texturkoordinatenoffset, der für jeden Texturobjekttyp verwendet werden kann. Der Offset wird vor der Stichprobenentnahme auf die Position angewendet. Der Argumenttyp ist vom Texturobjekttyp abhängig. Bei Shadern, die auf ShaderModell 5.0 und höher abzielen, werden die 6 am wenigsten signifikanten Bits jedes Offsetwerts als Wert mit Vorsignierung verwendet, was einen Bereich von [-32...31] ergibt. Bei vorherigen Shadermodell-Shadern müssen Offsets direkte ganze Zahlen zwischen -8 und 7 sein.</p>

<table>
<thead>
<tr class="header">
<th>Texture-Object Typ</th>
<th>Parametertyp</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
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

Ein Vektor mit vier Komponenten mit vier Komponenten roter Daten, dessen Typ mit dem Vorlagentyp der Textur identisch ist.

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

1.  TextureCubeArray ist in Shader Model 4.1 oder höher verfügbar.
2.  ShaderModell 4.1 ist in Direct3D 10.1 oder höher verfügbar.

## <a name="example"></a>Beispiel


```
Texture2D<int1> Tex2d;
Texture2DArray<int2> Tex2dArray;
TextureCube<int3> TexCube;
TextureCubeArray<float2> TexCubeArray;

SamplerState s;

int4 main (float4 f : SV_Position) : SV_Target
{
    int2 iOffset = int2(2,3);

    int4 i1 = Tex2d.Gather(s, f.xy);
    int4 i2 = Tex2d.Gather(s, f.xy, iOffset);

    int4 i3 = Tex2dArray.Gather(s, f.xyz);
    int4 i4 = Tex2dArray.Gather(s, f.xyz, iOffset);

    int4 i5 = TexCube.Gather(s, f.xyzw);

    float4 f6 = TexCubeArray.Gather(s, f.xyzw);

    return i1+i2+i3+i4+i5+int4(i6);
}
  
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texture-Object](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





