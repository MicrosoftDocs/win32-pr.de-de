---
title: Texturobjekt
description: In Direct3D 10 geben Sie die Sampler und Texturen unabhängig voneinander an. Textursstichproben werden mithilfe eines Texturobjekts mit Vorlagen implementiert. Dieses Templated-Texture-Objekt hat ein bestimmtes Format, gibt einen bestimmten Typ zurück und implementiert mehrere Methoden.
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
ms.openlocfilehash: 4d1881ba4a88e97e978e2646c92d276bb9763ffd
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825770"
---
# <a name="texture-object"></a>Texturobjekt

In Direct3D 10 geben Sie die Sampler und Texturen unabhängig voneinander an. Textursstichproben werden mithilfe eines Texturobjekts mit Vorlagen implementiert. Dieses Templated-Texture-Objekt hat ein bestimmtes Format, gibt einen bestimmten Typ zurück und implementiert mehrere Methoden.

Unterschiede zwischen Direct3D9 und Direct3D10:

- In Direct3D 9 sind Sampler an bestimmte Texturen gebunden.
- In Direct3D 10 sind Texturen und Sampler unabhängige Objekte. Jedes Templated-Texture-Objekt implementiert Textur-Samplingmethoden, die sowohl die Textur als auch den Sampler als Eingabeparameter verwenden.



 

Hier ist die Syntax zum Erstellen aller Texturobjekte (mit Ausnahme von Objekten mit mehrerenAmpeln).



| \[ < *Object1-Typname;* > \]  |
|------------------------------------|



 

Für Mehrfachbeispielobjekte (Texture2DMS und Texture2DMSArray) muss die Texturgröße explizit angegeben und als Anzahl von Stichproben ausgedrückt werden.



| \[ < *Object2-Typ, Name der* > \] *Beispiele;* |
|---------------------------------------------|



 

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
<li>Der Puffertyp unterstützt die meisten Texturobjektmethoden außer GetDimensions.</li>
<li>TextureCubeArray ist im Shadermodell 4.1 oder höher verfügbar.</li>
<li>Shadermodell 4.1 ist in Direct3D 10.1 oder höher verfügbar.</li>
</ol></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Typ</em></p></td>
<td><p>Dies ist optional. Jeder <a href="dx-graphics-hlsl-scalar.md">skalare HLSL-Typ oder</a> <a href="dx-graphics-hlsl-vector.md"><strong>Vektor-HLSL-Typ,</strong></a>umgeben von eckigen Klammern. Der Standardtyp ist <strong>float4.</strong></p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Namen</em></p></td>
<td><p>Eine ASCII-Zeichenfolge, die den Texturobjektnamen angibt.</p></td>
</tr>
<tr class="even">
<td><p><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Proben</em></p></td>
<td><p>Die Anzahl der Stichproben (bereiche zwischen 1 und 128).</p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a>Beispiel 1

Hier ist ein Beispiel für das Deklarieren eines Texturobjekts.


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a>Texturobjektmethoden

Jedes Texturobjekt implementiert bestimmte Methoden. Hier ist die Tabelle, in der alle Methoden aufgeführt sind. Informationen dazu, welche Objekte diese Methode verwenden können, finden Sie auf der Referenzseite für die einzelnen Methoden.



| Texturmethode                                                                     | Beschreibung                                                                                                       | vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [CalculateLevelOfDetail](dx-graphics-hlsl-to-calculate-lod.md)                    | Berechnen Sie die LOD, und geben Sie ein geklammertes Ergebnis zurück.                                                                       |          |           |          | x         |          |           |
| [CalculateLevelOfDetailUnclamped](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | Berechnen Sie die LOD, und geben Sie ein ergebnislos zurück.                                                                    |          |           |          | x         |          |           |
| [versammeln](dx-graphics-hlsl-to-gather.md)                                           | Ruft die vier Stichproben (nur rote Komponente) ab, die für die bilineare Interpolation beim Sampling einer Textur verwendet werden. |          | x         |          | x         |          | x         |
| [GetDimensions](dx-graphics-hlsl-to-getdimensions.md)                             | Gibt die Texturdimension für eine angegebene Mipmapebene an.                                                           | x        | x         | x        | x         | x        | x         |
| [GetDimensions (MultiSample)](dx-graphics-hlsl-to-getdimensions.md)               | Gibt die Texturdimension für eine angegebene Mipmapebene an.                                                           |          | x         |          | x         |          | x         |
| [GetSamplePosition](dx-graphics-hlsl-to-get-sample-position.md)                   | Gibt die Position des angegebenen Beispiels an.                                                                         |          | x         |          | x         |          | x         |
| [Load](dx-graphics-hlsl-to-load.md)                                               | Laden von Daten ohne Filterung oder Stichprobenentnahme.                                                                      | x        | x         | x        | x         | x        | x         |
| [Laden (Multisample)](dx-graphics-hlsl-to-load.md)                                 | Laden von Daten ohne Filterung oder Stichprobenentnahme.                                                                      |          | x         | x        | x         |          | x         |
| [Beispiel](dx-graphics-hlsl-to-sample.md)                                           | Beispiel für eine Textur.                                                                                                 |          |           | x        | x         |          |           |
| [SampleBias](dx-graphics-hlsl-to-samplebias.md)                                   | Sample a texture, after applying the bias value to the mipmap level.                                              |          |           | x        | x         |          |           |
| [SampleCmp](dx-graphics-hlsl-to-samplecmp.md)                                     | Beispiel für eine Textur mithilfe eines Vergleichswerts zum Ablehnen von Stichproben.                                                     |          |           | x        | x         |          |           |
| [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | Beispiel für eine Textur (nur Mipmap-Ebene 0) mithilfe eines Vergleichswerts zum Ablehnen von Stichproben.                               | x        | x         | x        | x         | x        | x         |
| [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)                                   | Beispiel für eine Textur mithilfe eines Farbverlaufs, um die Berechnung der Stichprobenposition zu beeinflussen.                         | x        | x         | x        | x         | x        | x         |
| [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                 | Beispiel für eine Textur auf der angegebenen Mipmapebene.                                                                   | x        | x         | x        | x         | x        | x         |



 

### <a name="return-type"></a>Rückgabetyp

Der Rückgabetyp einer Texturobjektmethode ist float4, sofern nicht anders angegeben, mit Ausnahme der Multisampled-Texturobjekte mit Antialiasing, die immer den angegebenen Typ und die angegebene Stichprobenanzahl benötigen. Der Rückgabetyp ist identisch mit dem Texturressourcentyp ([**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). Anders ausgedrückt: Dies kann einer der folgenden Typen sein.



| Typ                       | BESCHREIBUNG                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| float                      | 32-Bit-Gleitkommazahl (siehe [Gleitkommaregeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) für Unterschiede zu IEEE float)                            |
| INT                        | 32-Bit-Ganzzahl mit Vorzeichen                                                                                                                                                   |
| unsigned int               | 32-Bit-Ganzzahl ohne Vorzeichen                                                                                                                                                 |
| snorm                      | 32-Bit-Gleitkommazahl im Bereich -1 bis einschließlich 1 (siehe [Gleitkommaregeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) für Unterschiede zu IEEE float) |
| unorm                      | 32-Bit-Gleitkommazahl im Bereich von 0 bis einschließlich 1 (siehe [Gleitkommaregeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) für Unterschiede zu IEEE float)  |
| beliebiger Texturtyp oder Struktur | Die Anzahl der zurückgegebenen Komponenten muss zwischen 1 und 3 (einschließlich) liegen.                                                                                                    |



 

Darüber hinaus kann der Rückgabetyp ein beliebiger Texturtyp sein, einschließlich einer -Struktur, aber er muss kleiner als 4 Komponenten sein, z. B. ein float1-Typ, der eine Komponente zurückgibt.

## <a name="default-values-for-missing-components-in-a-texture"></a>Standardwerte für fehlende Komponenten in einer Textur

Der Standardwert für fehlende Komponenten in einem Texturressourcentyp ist 0 (null) für jede Komponente mit Ausnahme der Alphakomponente (A). Der Standardwert für das fehlende A ist 1. Die Art und Weise, wie diese im Shader angezeigt wird, hängt vom Texturressourcentyp ab. Sie hat die Form der ersten typierten Komponente, die tatsächlich im Texturressourcentyp vorhanden ist (beginnend von links in RGBA-Reihenfolge). Wenn dieses Formular UNORM oder FLOAT ist, ist der Standardwert für das fehlende A 1,0f. Wenn das Formular SINT oder UINT ist, wird der Standardwert für das fehlende A 0x1.

Wenn ein Shader beispielsweise den [**Ressourcentyp DXGI \_ FORMAT \_ R24 \_ UNORM \_ X8 \_ TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) liest, Die Standardwerte für G und B sind 0 (null), und der Standardwert für A ist 1,0f. Wenn ein Shader den [**DXGI FORMAT \_ \_ R16G16 \_ UINT-Texturressourcentyp**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) liest, ist der Standardwert für B 0 (null), und der Standardwert für A ist 0x00000001. Wenn ein Shader den [**DXGI FORMAT \_ \_ R16 \_ SINT-Texturressourcentyp**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) liest, sind die Standardwerte für G und B null, und der Standardwert für A ist 0x00000001.

## <a name="example-2"></a>Beispiel 2

Im Folgenden finden Sie ein Beispiel für texturiertes Sampling mithilfe einer Texturmethode.


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a>Minimales Shadermodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höher– Shadermodelle | ja       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

