---
title: Beispiel (DirectX HLSL-Strukturobjekt)
description: Stichproben einer Textur. | Beispiel (DirectX HLSL-Texturobjekt)
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2374063d222d06576f720fed2aa7fb714bcccf04
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825747"
---
# <a name="sample-directx-hlsl-texture-object"></a>Beispiel (DirectX HLSL-Strukturobjekt)

Stichproben einer Textur.

&lt;Vorlagentyp &gt; Object.Sample( \_ Samplerzustand S, float Location \[ , int Offset \] );

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

## <a name="example"></a>Beispiel

Dieses Teilcodebeispiel basiert auf der Datei BasicHLSL11.fx im [BasicHLSL11-Beispiel](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).

```
// Object Declarations
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color (note that COLOR0 is clamped from 0..1)
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT In;

// Shader body calling the intrinsic function
   ...
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
```

## <a name="remarks"></a>Bemerkungen

Bei der Texturstichprobe wird die Texelposition verwendet, um einen Texelwert zu suchen. Ein Offset kann vor der Suche auf die Position angewendet werden. Der Samplerzustand enthält die Sampling- und Filteroptionen. Diese Methode kann innerhalb eines Pixel-Shaders aufgerufen werden, wird jedoch in einem Vertex-Shader oder geometrie-Shader nicht unterstützt.

Verwenden Sie einen Offset nur bei einer ganzzahligen MIP-Ebene. Andernfalls erhalten Sie je nach Hardwareimplementierung oder Treibereinstellungen möglicherweise unterschiedliche Ergebnisse.

### <a name="calculating-texel-positions"></a>Berechnen von Texelpositionen

Texturkoordinaten sind Gleitkommawerte, die auf Texturdaten verweisen, die auch als normalisierter Texturraum bezeichnet werden. Adressumbruchmodi werden in dieser Reihenfolge (Texturkoordinaten + Offsets + Umbruchmodus) angewendet, um Texturkoordinaten außerhalb des \[ Bereichs 0...1 zu \] ändern.

Bei Texturarrays gibt ein zusätzlicher Wert im location-Parameter einen Index in einem Texturarray an. Dieser Index wird als skalierte Gleitkommawerte behandelt (anstelle des normalisierten Platzes für Standardtexturkoordinaten). Die Konvertierung in einen ganzzahligen Index erfolgt in der folgenden Reihenfolge (float + round-to-nearest-even integer + clamp to the array range).

### <a name="applying-texture-coordinate-offsets"></a>Anwenden von Texturkoordinatenoffsets

Der offset-Parameter ändert die Texturkoordinaten im Texelraum. Obwohl Texturkoordinaten normalisierte Gleitkommazahlen sind, wendet der Offset einen ganzzahligen Offset an. Beachten Sie auch, dass die Texturoffsets statisch sein müssen.

Das zurückgegebene Datenformat wird durch das Texturformat bestimmt. Wenn die Texturressource z. B. mit dem DXGI \_ FORMAT \_ A8B8G8R8 UNORM SRGB-Format definiert wurde, konvertiert der Samplingvorgang \_ sampled texels von gamma 2.0 in 1.0, filtert das Ergebnis und schreibt das Ergebnis als Gleitkommawert im Bereich \_ \[ 0..1 \] .

## <a name="related-topics"></a>Zugehörige Themen

[Texture-Object](dx-graphics-hlsl-to-type.md)
