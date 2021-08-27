---
title: Texturobjekt
description: In Direct3D 10 geben Sie die Sampler und Texturen unabhängig an. Textursampling wird mithilfe eines Objekts mit Vorlagentextur implementiert. Dieses Vorlagentexturobjekt hat ein bestimmtes Format, gibt einen bestimmten Typ zurück und implementiert mehrere Methoden.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- Texturobjekt HLSL
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ac22ba8c9da7d69784d977e2b78b8f0b52a6a3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628116"
---
# <a name="texture-object"></a>Texturobjekt

In Direct3D 10 geben Sie die Sampler und Texturen unabhängig an. Textursampling wird mithilfe eines Objekts mit Vorlagentextur implementiert. Dieses Vorlagentexturobjekt hat ein bestimmtes Format, gibt einen bestimmten Typ zurück und implementiert mehrere Methoden.

Unterschiede zwischen Direct3D9 und Direct3D10:

- In Direct3D 9 sind Sampler an bestimmte Texturen gebunden.
- In Direct3D 10 sind Texturen und Sampler unabhängige Objekte. Jedes Vorlagentexturobjekt implementiert Textursamplingmethoden, die sowohl die Textur als auch den Sampler als Eingabeparameter verwenden.



 

Hier ist die Syntax zum Erstellen aller Texturobjekte (mit Ausnahme von Multisampled-Objekten).



| \[ < *Object1-Typname* > \] ; |
|------------------------------------|



 

Für Multisampled-Objekte (Texture2DMS und Texture2DMSArray) muss die Texturgröße explizit angegeben und als Anzahl von Stichproben ausgedrückt werden.



| \[ < *Object2-Typ,* > \] *Beispielname*; |
|---------------------------------------------|



 

## <a name="parameters"></a>Parameter



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
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em><br/></td>
<td>Ein Texturobjekt. Muss einer der folgenden Typen sein. <br/> 
<table>
<thead>
<tr class="header">
<th>Object1-Typ</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Buffer</td>
<td>Buffer </td>
</tr>
<tr class="even">
<td>Texture1D</td>
<td>1D-Textur</td>
</tr>
<tr class="odd">
<td>Texture1DArray</td>
<td>Array von 1D-Texturen</td>
</tr>
<tr class="even">
<td>Texture2D</td>
<td>2D-Textur</td>
</tr>
<tr class="odd">
<td>Texture2DArray</td>
<td>Array von 2D-Texturen</td>
</tr>
<tr class="even">
<td>Texture3D</td>
<td>3D-Textur</td>
</tr>
<tr class="odd">
<td>TextureCube</td>
<td>Cubetextur</td>
</tr>
<tr class="even">
<td>TextureCubeArray  </td>
<td>Array von Cubetexturen</td>
</tr>
<tr class="odd">
<td>Object2-Typ</td>
<td>Beschreibung</td>
</tr>
<tr class="even">
<td>Texture2DMS</td>
<td>2D-Textur mit mehrerenAmpeln</td>
</tr>
<tr class="odd">
<td>Texture2DMSArray</td>
<td>Array von 2D-Texturen mit mehrerenAmpeln</td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li>Der Puffertyp unterstützt die meisten Texturobjektmethoden mit Ausnahme von GetDimensions.</li>
<li>TextureCubeArray ist im Shadermodell 4.1 oder höher verfügbar.</li>
<li>Shadermodell 4.1 ist in Direct3D 10.1 oder höher verfügbar.</li>
</ol></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Typ</em></p></td>
<td><p>Optional. Beliebiger <a href="dx-graphics-hlsl-scalar.md">HLSL-Skalartyp</a> oder <a href="dx-graphics-hlsl-vector.md"><strong>HLSL-Vektortyp,</strong></a>umschlossen von spitzen Klammern. Der Standardtyp ist <strong>float4.</strong></p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Namen</em></p></td>
<td><p>Eine ASCII-Zeichenfolge, die den Namen des Texturobjekts angibt.</p></td>
</tr>
<tr class="even">
<td><p><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Proben</em></p></td>
<td><p>Die Anzahl der Stichproben (liegt zwischen 1 und 128).</p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a>Beispiel 1

Hier ist ein Beispiel für das Deklarieren eines Texturobjekts.


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a>Texturobjektmethoden

Jedes Texturobjekt implementiert bestimmte Methoden. Hier ist die Tabelle, in der alle Methoden aufgelistet sind. Auf der Referenzseite für jede Methode können Sie sehen, welche Objekte diese Methode verwenden können.



| Texturmethode                                                                     | Beschreibung                                                                                                       | Vs \_ 4 \_ 0 | Vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [CalculateLevelOfDetail](dx-graphics-hlsl-to-calculate-lod.md)                    | Berechnen Sie die LOD, und geben Sie ein klammertes Ergebnis zurück.                                                                       |          |           |          | x         |          |           |
| [CalculateLevelOfDetailUnclamped](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | Berechnen Sie die LOD, und geben Sie ein ergebnisloses Ergebnis zurück.                                                                    |          |           |          | x         |          |           |
| [Versammeln](dx-graphics-hlsl-to-gather.md)                                           | Ruft die vier Stichproben (nur rote Komponente) ab, die beim Sampling einer Textur für die bilineare Interpolation verwendet werden. |          | x         |          | x         |          | x         |
| [GetDimensions](dx-graphics-hlsl-to-getdimensions.md)                             | Abrufen der Texturdimension für eine angegebene Mipmapebene.                                                           | x        | x         | x        | x         | x        | x         |
| [GetDimensions (MultiSample)](dx-graphics-hlsl-to-getdimensions.md)               | Abrufen der Texturdimension für eine angegebene Mipmapebene.                                                           |          | x         |          | x         |          | x         |
| [GetSamplePosition](dx-graphics-hlsl-to-get-sample-position.md)                   | Abrufen der Position des angegebenen Beispiels.                                                                         |          | x         |          | x         |          | x         |
| [Load](dx-graphics-hlsl-to-load.md)                                               | Laden von Daten ohne Filterung oder Stichproben.                                                                      | x        | x         | x        | x         | x        | x         |
| [Laden (Multisample)](dx-graphics-hlsl-to-load.md)                                 | Laden von Daten ohne Filterung oder Stichproben.                                                                      |          | x         | x        | x         |          | x         |
| [Beispiel](dx-graphics-hlsl-to-sample.md)                                           | Probieren Sie eine Textur aus.                                                                                                 |          |           | x        | x         |          |           |
| [SampleBias](dx-graphics-hlsl-to-samplebias.md)                                   | Probieren Sie eine Textur aus, nachdem Sie den Biaswert auf die Mipmapebene angewendet haben.                                              |          |           | x        | x         |          |           |
| [SampleCmp](dx-graphics-hlsl-to-samplecmp.md)                                     | Probieren Sie eine Textur mithilfe eines Vergleichswerts aus, um Stichproben abzulehnen.                                                     |          |           | x        | x         |          |           |
| [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | Probieren Sie eine Textur (nur Mipmapebene 0) mithilfe eines Vergleichswerts aus, um Stichproben abzulehnen.                               | x        | x         | x        | x         | x        | x         |
| [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)                                   | Probieren Sie eine Textur mithilfe eines Farbverlaufs aus, um die Art und Weise zu beeinflussen, wie die Stichprobenposition berechnet wird.                         | x        | x         | x        | x         | x        | x         |
| [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                 | Probieren Sie eine Textur auf der angegebenen Mipmapebene aus.                                                                   | x        | x         | x        | x         | x        | x         |



 

### <a name="return-type"></a>Rückgabetyp

Der Rückgabetyp einer Texturobjektmethode ist float4, sofern nichts anderes angegeben ist, mit Ausnahme der Multisampling-Texturobjekte mit Antialiasing, für die immer der angegebene Typ und die Stichprobenanzahl erforderlich sind. Der Rückgabetyp entspricht dem Texturressourcentyp ([**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). Mit anderen Worten: Es kann sich um einen der folgenden Typen ausdingen.



| Typ                       | BESCHREIBUNG                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| float                      | 32-Bit-Gleitkommawert (Unterschiede zu IEEE float finden Sie unter [Gleitkommaregeln)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules)                            |
| INT                        | 32-Bit-Ganzzahl mit Vorzeichen                                                                                                                                                   |
| unsigned int               | 32-Bit-Ganzzahl ohne Vorzeichen                                                                                                                                                 |
| snorm                      | 32-Bit-Gleitkommawert im Bereich von -1 bis einschließlich 1 (Unterschiede zu IEEE float finden Sie unter [Gleitkommaregeln).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) |
| unorm                      | 32-Bit-Gleitkommawert im Bereich von 0 bis einschließlich 1 (Unterschiede zu IEEE float finden Sie unter [Gleitkommaregeln)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules)  |
| beliebiger Texturtyp oder -struktur | Die Anzahl der zurückgegebenen Komponenten muss zwischen 1 und 3 einschließlich liegen.                                                                                                    |



 

Darüber hinaus kann der Rückgabetyp ein beliebiger Texturtyp sein, einschließlich einer -Struktur, aber er muss weniger als 4 Komponenten sein, z. B. ein float1-Typ, der eine Komponente zurückgibt.

## <a name="default-values-for-missing-components-in-a-texture"></a>Standardwerte für fehlende Komponenten in einer Textur

Der Standardwert für fehlende Komponenten in einem Texturressourcentyp ist für alle Komponenten mit Ausnahme der Alphakomponente (A) 0 (null). Der Standardwert für das fehlende A ist 1. Die Art und Weise, wie diese dem Shader angezeigt wird, hängt vom Texturressourcentyp ab. Sie hat die Form der ersten typisierten Komponente, die tatsächlich im Texturressourcentyp vorhanden ist (beginnend von links in RGBA-Reihenfolge). Wenn dieses Formular UNORM oder FLOAT ist, ist der Standardwert für das fehlende A 1,0f. Wenn das Formular SINT oder UINT ist, ist der Standardwert für das fehlende A 0x1.

Wenn ein Shader beispielsweise den Texturressourcentyp [**DXGI \_ FORMAT \_ R24 \_ UNORM \_ X8 \_ TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) liest, Die Standardwerte für G und B sind null, und der Standardwert für A ist 1,0f. Wenn ein Shader den [**Texturressourcentyp DXGI FORMAT \_ \_ R16G16 \_ UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) liest, ist der Standardwert für B 0 und der Standardwert für A 0x00000001. Wenn ein Shader den [**TEXTURressourcentyp DXGI FORMAT \_ \_ R16 \_ SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) liest, sind die Standardwerte für G und B 0 und der Standardwert für A 0x00000001.

## <a name="example-2"></a>Beispiel 2

Hier sehen Sie ein Beispiel für die Textursampling mithilfe einer Texturmethode.


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höhere Shadermodelle | Ja       |



 

## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

