---
title: Sample Grad (DirectX HLSL-Textur Objekt)
description: Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird | Sample Grad (DirectX HLSL-Textur Objekt)
ms.assetid: f3d73296-23c4-4178-b89e-6f84cfcb48a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 236c453f3636452cbba8ed6000b2416e5187898d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219180"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a>Sample Grad (DirectX HLSL-Textur Objekt)

Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird



|                                                                                                            |
|------------------------------------------------------------------------------------------------------------|
| &lt;Template Type &gt; Object. samplegrad (Sampler \_ State S, float Location, float DDX, float DDY \[ , int Offset \] ); |



 

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
<td>Ein beliebiger <a href="dx-graphics-hlsl-to-type.md">Textur Objekttyp</a> (mit Ausnahme von Texture2DMS und Texture2DMSArray).<br/></td>
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
<td>Texture1D</td>
<td>float</td>
</tr>
<tr class="even">
<td>Texture1DArray, Texture2D</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture2DArray, Texture3D, texturecube</td>
<td>float3</td>
</tr>
<tr class="even">
<td>Texturecubearray </td>
<td>float4</td>
</tr>
<tr class="odd">
<td>Texture2DMS, Texture2DMSArray</td>
<td>Nicht unterstützt</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="DDX"></span><span id="ddx"></span><em>DDX</em></p></td>
<td><p>in Die Änderungs Rate der Oberflächengeometrie in der x-Richtung. Der Argumenttyp ist vom Textur Objekttyp abhängig.</p>

<table>
<thead>
<tr class="header">
<th>Texture-Object-Typ</th>
<th>Parametertyp</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>float</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, texturecube, texturecubearray </td>
<td>float3</td>
</tr>
<tr class="even">
<td>Texture2DMS, Texture2DMSArray</td>
<td>Nicht unterstützt</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span id="DDY"></span><span id="ddy"></span><em>Tziger</em></p></td>
<td><p>in Die Änderungs Rate der Oberflächengeometrie in der y-Richtung. Der Argumenttyp ist vom Textur Objekttyp abhängig.</p>

<table>
<thead>
<tr class="header">
<th>Texture-Object-Typ</th>
<th>Parametertyp</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>float</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, texturecube, texturecubearray </td>
<td>float3</td>
</tr>
<tr class="even">
<td>Texture2DMS, Texture2DMSArray</td>
<td>Nicht unterstützt</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Kompensieren</em></p></td>
<td><p>in Ein optionaler Offset der Textur Koordinate, der für beliebige Textur Objekttypen verwendet werden kann. Der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet. Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden. Der Argumenttyp ist vom Textur Objekttyp abhängig. Weitere Informationen finden Sie unter<a href="dx-graphics-hlsl-to-sample.md">Anwenden von ganzzahligen Offsets</a>.</p>

<table>
<thead>
<tr class="header">
<th>Texture-Object-Typ</th>
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
<td>Texturecube, texturecubearray </td>
<td>Nicht unterstützt</td>
</tr>
<tr class="odd">
<td>Texture2DMS, Texture2DMSArray</td>
<td>Nicht unterstützt</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Rückgabewert

Der Vorlagentyp der Textur, bei dem es sich um einen Vektor mit einer einzelnen oder mehreren Komponenten handeln kann. Das Format basiert auf dem [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)der Textur.

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.
2.  Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.

## <a name="example"></a>Beispiel

Dieses partielle Codebeispiel wird aus der Datei "" in der Datei "" in der Datei " [MotionBlur10](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx)" aus dem Beispiel


```
// Object Declarations
Texture2D g_txDiffuse;

SamplerState g_samLinear
{
    Filter = ANISOTROPIC;
    MaxAnisotropy = 8;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VSSceneOut
{
    float4 Pos : SV_POSITION;
    float4 Color : COLOR0;
    float2 Tex : TEXCOORD;
    float2 Aniso : ANISOTROPY;
};

float4 PSSceneMain( VSSceneOut Input ) : SV_TARGET
{
    float2 ddx = Input.Aniso;
    float2 ddy = Input.Aniso;
    
    // Shader body calling the intrinsic function
    float4 diff = g_txDiffuse.SampleGrad( g_samLinear, Input.Tex, ddx, ddy);
    
    ...
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texture-Objekt](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

