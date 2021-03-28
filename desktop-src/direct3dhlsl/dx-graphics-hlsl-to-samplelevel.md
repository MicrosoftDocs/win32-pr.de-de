---
title: Samplelevel (DirectX HLSL-Textur Objekt)
description: Gibt eine Textur mit einem Offset auf MipMap-Ebene aus.
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73cf7bc0c13987099540cecd49519de35b4b7de1
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "104102590"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a>Samplelevel (DirectX HLSL-Textur Objekt)

Gibt eine Textur mit einem Offset auf MipMap-Ebene aus.



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| &lt;Template Type &gt; Object. samplelevel (Sampler \_ State S, float Location, float Lod \[ , int Offset \] ); |



 

Diese Funktion ähnelt [Sample](dx-graphics-hlsl-to-sample.md) , mit der Ausnahme, dass Sie die Lod-Ebene (in der letzten Komponente des Location-Parameters) verwendet, um die MipMap-Ebene auszuwählen. Beispielsweise werden in einer 2D-Textur die ersten beiden Komponenten für UV-Koordinaten und die dritte Komponente für die MipMap-Ebene verwendet.

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
</tbody>
</table>

<p> </p>
<p>Wenn das Textur Objekt ein Array ist, ist die letzte Komponente der Array Index.</p></td>
</tr>
<tr class="even">
<td><p><span id="LOD"></span><span id="lod"></span><em>LOD</em></p></td>
<td><p>in Eine Zahl, die die MipMap-Ebene angibt. Wenn der Wert = 0 ist, wird die NULL-Werte (größte Karte) verwendet. Der Bruch Wert (falls angegeben) wird verwendet, um zwischen zwei MipMap-Ebenen zu interpolieren.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Kompensieren</em></p></td>
<td><p>in Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet. Die Textur Offsets müssen statisch sein. Der Argumenttyp ist vom Textur Objekttyp abhängig. Weitere Informationen finden Sie unter <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Anwenden von Texturkoordinaten Offsets</a>.</p>

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

Dieses partielle Codebeispiel wird aus der Datei "Instancing. FX" im [Instancing10](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx)-Beispiel entnommen.


```
// Object Declarations
Texture1D g_txRandom;

SamplerState g_samPoint
{
    Filter = MIN_MAG_MIP_POINT;
    AddressU = Wrap;
    AddressV = Wrap;
};

    
// Shader body calling the intrinsic function
float3 RandomDir(float fOffset)
{   
    float tCoord = (fOffset) / 300.0;
    return g_txRandom.SampleLevel( g_samPoint, tCoord, 0 );
   ...

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texture-Objekt](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

