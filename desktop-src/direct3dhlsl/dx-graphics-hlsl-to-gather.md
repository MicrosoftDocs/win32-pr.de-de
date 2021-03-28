---
title: Gather (DirectX-HLSL-Textur Objekt)
description: Ruft die vier Stichproben (nur rote Komponente) ab, die bei der Stichprobenentnahme einer Textur für die bilineare interpolung verwendet werden.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16c568afc3cfdc0d26472d50599abdf3dbd08301
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "104976928"
---
# <a name="gather-directx-hlsl-texture-object"></a>Gather (DirectX-HLSL-Textur Objekt)

Ruft die vier Stichproben (nur rote Komponente) ab, die bei der Stichprobenentnahme einer Textur für die bilineare interpolung verwendet werden.



|                                                                                                    |
|----------------------------------------------------------------------------------------------------|
| &lt;Template Type &gt; 4 Object. Gather (Sampler \_ State S, float2 \| 3 \| 4 Location \[ , int2 Offset \] ); |



 

## <a name="parameters"></a>Parameter



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
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em><br/></td>
<td>Die folgenden <a href="dx-graphics-hlsl-to-type.md">Textur Objekt</a> Typen werden unterstützt: Texture2D, Texture2DArray, texturecube, texturecubearray.<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>Hymnen</em><br/></td>
<td>in Ein <a href="dx-graphics-hlsl-sampler.md">samplerzustand</a>. Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Hotels</em><br/></td>
<td>in Die Texturkoordinaten. Der Argumenttyp ist vom Textur Objekttyp abhängig. <br/> 
<table>
<thead>
<tr class="header">
<th>Texture-Object-Typ</th>
<th>Parametertyp</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture2D</td>
<td>float2</td>
</tr>
<tr class="even">
<td>Texture2DArray, texturecube</td>
<td>float3</td>
</tr>
<tr class="odd">
<td>Texturecubearray </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Kompensieren</em></p></td>
<td><p>in Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet. Die Textur Offsets müssen statisch sein. Der Argumenttyp ist vom Textur Objekttyp abhängig. Weitere Informationen finden Sie unter <a href="dx-graphics-hlsl-to-sample.md">Anwenden von Texturkoordinaten Offsets</a>.</p>

<table>
<thead>
<tr class="header">
<th>Texture-Object-Typ</th>
<th>Parametertyp</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
</tr>
<tr class="even">
<td>Texturecube, texturecubearray </td>
<td>Nicht unterstützt</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Rückgabewert

Ein Vektor mit vier Komponenten mit vier Komponenten von roten Daten, deren Typ mit dem Vorlagentyp der Textur identisch ist.

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

1.  Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.
2.  Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.

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

[Texture-Objekt](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





