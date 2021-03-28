---
title: Beispiel (DirectX HLSL-Strukturobjekt)
description: Stichproben eine Textur. | Sample (DirectX HLSL-Textur Objekt)
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ec80d296025684c1bb67642661a31d8cdc119a53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995295"
---
# <a name="sample-directx-hlsl-texture-object"></a>Beispiel (DirectX HLSL-Strukturobjekt)

Stichproben eine Textur.

|                                                                                  |
|----------------------------------------------------------------------------------|
| &lt;Template Type &gt; Object. Sample (Sampler \_ State S, float Location \[ , int Offset \] ); |

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

<p> </p></td>
</tr>
<tr class="even">
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
|          |           | x        | x         |          |           |

1.  Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.
2.  Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.

## <a name="example"></a>Beispiel

Dieses partielle Codebeispiel basiert auf der Datei BasicHLSL11. fx im [BasicHLSL11](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11)-Beispiel.

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

Bei der Textur Stichprobe wird die texusposition verwendet, um einen Texttyp zu suchen Ein Offset kann vor der Suche auf die Position angewendet werden. Der samplerstatus enthält die Optionen für Sampling und Filterung. Diese Methode kann in einem Pixelshader aufgerufen werden, wird jedoch in einem Vertexshader oder einem Geometry-Shader nicht unterstützt.

Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie abhängig von der Hardware Implementierung oder den Treibereinstellungen möglicherweise unterschiedliche Ergebnisse.

### <a name="calculating-texel-positions"></a>Berechnen von textabpositionen

Texturkoordinaten sind Gleit Komma Werte, die auf Textur Daten verweisen, die auch als normalisierter Textur Raum bezeichnet werden. Adress Umbruch Modi werden in dieser Reihenfolge (Texturkoordinaten + Offsets + Wrap-Modus) angewendet, um die Texturkoordinaten außerhalb des \[ Bereichs 0... 1 zu ändern \] .

Bei Textur Arrays gibt ein zusätzlicher Wert im Location-Parameter einen Index in ein Textur Array an. Dieser Index wird als skalierter float-Wert (anstelle des normalisierten Raums für standardmäßige Texturkoordinaten) behandelt. Die Konvertierung in einen ganzzahligen Index erfolgt in der folgenden Reihenfolge (float + Round-to-Next-even Integer + Klammer zum Array Bereich).

### <a name="applying-texture-coordinate-offsets"></a>Anwenden von Texturkoordinaten Offsets

Der Offset-Parameter ändert die Texturkoordinaten in texesbereich. Obwohl Texturkoordinaten normalisierte Gleit Komma Zahlen sind, wendet der Offset einen ganzzahligen Offset an. Beachten Sie auch, dass die Textur Offsets statisch sein müssen.

Das zurückgegebene Datenformat wird durch das Textur Format bestimmt. Wenn die Textur Ressource z. b. mit dem DXGI- \_ Format \_ A8B8G8R8 \_ unorm \_ sRGB-Format definiert wurde, konvertiert der Samplingvorgang Sampling-texeln von Gamma 2,0 in 1,0, filtert und schreibt das Ergebnis als Gleit Komma Wert im Bereich \[ 0.. 1 \] .

## <a name="related-topics"></a>Zugehörige Themen

[Texture-Objekt](dx-graphics-hlsl-to-type.md)
