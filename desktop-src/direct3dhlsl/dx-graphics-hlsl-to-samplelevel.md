---
title: SampleLevel (DirectX HLSL-Texturobjekt)
description: Probieren Sie eine Textur mithilfe eines Offsets auf Mipmapebene aus.
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bc3a074641ce5b15a3d837e8bd91dfdae09fe627
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826684"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a>SampleLevel (DirectX HLSL-Texturobjekt)

Probieren Sie eine Textur mithilfe eines Offsets auf Mipmapebene aus.

&lt;Vorlagentyp &gt; Object.SampleLevel( sampler \_ state S, float Location, float LOD \[ , int Offset \] );



 

Diese Funktion ähnelt [Sample,](dx-graphics-hlsl-to-sample.md) mit der Ausnahme, dass sie die LOD-Ebene (in der letzten Komponente des Location-Parameters) verwendet, um die Mipmapebene auszuwählen. Beispielsweise verwendet eine 2D-Textur die ersten beiden Komponenten für UV-Koordinaten und die dritte Komponente für die Mipmapebene.

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
<td>Jeder <a href="dx-graphics-hlsl-to-type.md">Texturobjekttyp</a> (mit Ausnahme von Texture2DMS und Texture2DMSArray).<br/></td>
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
<td>Texture2DArray, Texture3D, TextureCube</td>
<td>float3</td>
</tr>
<tr class="even">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Wenn das Texturobjekt ein Array ist, ist die letzte Komponente der Arrayindex.</p></td>
</tr>
<tr class="even">
<td><p><span id="LOD"></span><span id="lod"></span><em>Lod</em></p></td>
<td><p>[in] Eine Zahl, die die Mipmapebene angibt. Wenn der Wert = 0 ist, wird der Nullth (größte Karte) verwendet. Der Bruchwert (sofern angegeben) wird verwendet, um zwischen zwei Mipmapebenen zu interpolieren.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></p></td>
<td><p>[in] Ein optionaler Texturkoordinatenoffset, der für jeden Texturobjekttyp verwendet werden kann. Der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet. Die Texturoffsets müssen statisch sein. Der Argumenttyp ist vom Texturobjekttyp abhängig. Weitere Informationen finden Sie unter <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Anwenden von Texturkoordinatenoffsets.</a></p>

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

Der Vorlagentyp der Textur, bei dem es sich um einen Ein- oder Mehrkomponentenvektor aussetzen kann. Das Format basiert auf dem [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)der Textur.

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Vs \_ 4 \_ 0 | Vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  TextureCubeArray ist im Shadermodell 4.1 oder höher verfügbar.
2.  Shadermodell 4.1 ist in Direct3D 10.1 oder höher verfügbar.

## <a name="example"></a>Beispiel

Dieses Teilcodebeispiel stammt aus der Datei Instancing.fx im [Beispiel Instancing10.](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx)


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

[Texturobjekt](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

