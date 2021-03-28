---
title: Texture-Objekt
description: In Direct3D 10 geben Sie die Samplern und Texturen unabhängig an. Textur Stichproben werden mithilfe eines Vorlagen basierten Textur Objekts implementiert. Dieses auf Vorlagen basierende Textur Objekt hat ein bestimmtes Format, gibt einen bestimmten Typ zurück und implementiert mehrere Methoden.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- Textur Objekt HLSL
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b075ddc1f659923efd03d9fe9d21ee3238e656e9
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104219411"
---
# <a name="texture-object"></a>Texture-Objekt

In Direct3D 10 geben Sie die Samplern und Texturen unabhängig an. Textur Stichproben werden mithilfe eines Vorlagen basierten Textur Objekts implementiert. Dieses auf Vorlagen basierende Textur Objekt hat ein bestimmtes Format, gibt einen bestimmten Typ zurück und implementiert mehrere Methoden.




|                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen von Direct3D9 und Direct3D10: in Direct3D 9 sind Samplern an bestimmte Texturen gebunden. in Direct3D 10 sind Texturen und Samplern unabhängige Objekte. Jedes Vorlagen Struktur Objekt implementiert Textur-Samplingmethoden, die sowohl die Textur als auch den Sampler als Eingabeparameter annehmen.<br/> |



 

Hier ist die Syntax zum Erstellen aller Textur Objekte (mit Ausnahme von Multisampling-Objekten).



| Objekt1 \[ <  > \] *Typname*; |
|------------------------------------|



 

Multisampling-Objekte (Texture2DMS und Texture2DMSArray) erfordern, dass die Textur Größe explizit angegeben und als Anzahl von Stichproben ausgedrückt wird.



| Objekt2 \[ < *Type, Samples* > \] *Name*; |
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
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em><br/></td>
<td>Ein Textur Objekt. Muss einer der folgenden Typen sein: <br/> 
<table>
<thead>
<tr class="header">
<th>Objekt1-Typ</th>
<th>BESCHREIBUNG</th>
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
<td>Cube-Textur</td>
</tr>
<tr class="even">
<td>Texturecubearray  </td>
<td>Array von Cube-Texturen</td>
</tr>
<tr class="odd">
<td>Objekt2-Typ</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>Texture2DMS</td>
<td>2D-Textur mit Multisampling</td>
</tr>
<tr class="odd">
<td>Texture2DMSArray</td>
<td>Array von 2D-Multisampling-Texturen</td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li>Der Puffertyp unterstützt die meisten Textur Objektmethoden außer GetDimensions.</li>
<li>Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.</li>
<li>Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.</li>
</ol></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Sorte</em></p></td>
<td><p>Optional. Alle <a href="dx-graphics-hlsl-scalar.md">skalaren HLSL-Typen</a> oder <a href="dx-graphics-hlsl-vector.md"><strong>Vektor-HLSL-Typen</strong></a>, umgeben von spitzen Klammern. Der Standardtyp ist <strong>float4</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Benennen</em></p></td>
<td><p>Eine ASCII-Zeichenfolge, die den Textur Objektnamen angibt.</p></td>
</tr>
<tr class="even">
<td><p><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Stich</em></p></td>
<td><p>Die Anzahl der Stichproben (Bereiche zwischen 1 und 128).</p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a>Beispiel 1

Im folgenden finden Sie ein Beispiel für das Deklarieren eines Textur Objekts.


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a>Textur Objektmethoden

Jedes Textur Objekt implementiert bestimmte Methoden. Hier ist die Tabelle, in der alle Methoden aufgelistet sind. Auf der Referenzseite für jede Methode finden Sie Informationen dazu, welche Objekte diese Methode verwenden können.



| Texture-Methode                                                                     | BESCHREIBUNG                                                                                                       | vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [Calculatelevelof-Detail](dx-graphics-hlsl-to-calculate-lod.md)                    | Berechnen Sie das Lod, und geben Sie ein gespanntes Ergebnis zurück.                                                                       |          |           |          | x         |          |           |
| [Calculatelevelof detailunklamed](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | Berechnen Sie das Lod, und geben Sie ein nicht angehaltene Ergebnis zurück.                                                                    |          |           |          | x         |          |           |
| [Informieren](dx-graphics-hlsl-to-gather.md)                                           | Ruft die vier Stichproben (nur rote Komponente) ab, die bei der Stichprobenentnahme einer Textur für die bilineare interpolung verwendet werden. |          | x         |          | x         |          | x         |
| [GetDimensions](dx-graphics-hlsl-to-getdimensions.md)                             | Die Textur Dimension für eine angegebene MipMap-Ebene wird abgerufen.                                                           | x        | x         | x        | x         | x        | x         |
| [GetDimensions (Multisample)](dx-graphics-hlsl-to-getdimensions.md)               | Die Textur Dimension für eine angegebene MipMap-Ebene wird abgerufen.                                                           |          | x         |          | x         |          | x         |
| [Getsampleposition](dx-graphics-hlsl-to-get-sample-position.md)                   | Gibt die Position des angegebenen Beispiels an.                                                                         |          | x         |          | x         |          | x         |
| [Load](dx-graphics-hlsl-to-load.md)                                               | Laden von Daten ohne filtern oder Sampling.                                                                      | x        | x         | x        | x         | x        | x         |
| [Load (Multisample)](dx-graphics-hlsl-to-load.md)                                 | Laden von Daten ohne filtern oder Sampling.                                                                      |          | x         | x        | x         |          | x         |
| [Beispiel](dx-graphics-hlsl-to-sample.md)                                           | Beispiel für eine Textur.                                                                                                 |          |           | x        | x         |          |           |
| [Samplebias](dx-graphics-hlsl-to-samplebias.md)                                   | Beispiel für eine Textur, nachdem der Wert "Bias" auf die MipMap-Ebene angewendet wurde.                                              |          |           | x        | x         |          |           |
| [Samplecmp](dx-graphics-hlsl-to-samplecmp.md)                                     | Beispiel für eine Textur mit einem Vergleichswert zum ablehnen von Beispielen.                                                     |          |           | x        | x         |          |           |
| [Samplecmplevelzero](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | Beispiel für eine Textur (nur MipMap-Ebene 0) unter Verwendung eines Vergleichs Werts zum ablehnen von Beispielen.                               | x        | x         | x        | x         | x        | x         |
| [Samplegrad](dx-graphics-hlsl-to-samplegrad.md)                                   | Beispiel für eine Textur mit einem Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet                         | x        | x         | x        | x         | x        | x         |
| [Samplelevel](dx-graphics-hlsl-to-samplelevel.md)                                 | Beispiel für eine Textur auf der angegebenen MipMap-Ebene.                                                                   | x        | x         | x        | x         | x        | x         |



 

### <a name="return-type"></a>Rückgabetyp

Der Rückgabetyp einer Textur Objektmethode ist float4, sofern nichts anderes angegeben wird, mit Ausnahme der Multisampling-Textur Objekte mit Antialiasing, für die immer der angegebene Typ und die angegebene Stichproben Anzahl benötigt werden. Der Rückgabetyp ist identisch mit dem Textur Ressourcentyp ([**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). Das heißt, es kann sich um einen der folgenden Typen handeln:



| type                       | BESCHREIBUNG                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| float                      | 32-Bit Float (siehe Gleit [Komma Regeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) für Unterschiede von IEEE Float)                            |
| INT                        | 32-Bit-Ganzzahl mit Vorzeichen                                                                                                                                                   |
| unsigned int               | 32-Bit-Ganzzahl ohne Vorzeichen                                                                                                                                                 |
| snorm                      | 32-Bit Float im Bereich von-1 bis 1 einschließlich (siehe Gleit [Komma Regeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) für Unterschiede von IEEE Float) |
| unorm                      | 32-Bit-Gleit Komma Zahl im Bereich von 0 bis 1 einschließlich (siehe Gleit [Komma Regeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) für Unterschiede von IEEE Float)  |
| beliebige Textur Typen oder-Struktur | Die Anzahl der zurückgegebenen Komponenten muss zwischen 1 und 3 liegen.                                                                                                    |



 

Außerdem kann der Rückgabetyp ein beliebiger Textur Typ sein, einschließlich einer Struktur, muss jedoch kleiner als vier Komponenten sein, z. b. ein float1-Typ, der eine Komponente zurückgibt.

## <a name="default-values-for-missing-components-in-a-texture"></a>Standardwerte für fehlende Komponenten in einer Textur

Der Standardwert für fehlende Komponenten in einem Textur Ressourcentyp ist für alle Komponenten mit Ausnahme der Alpha Komponente (a) 0 (null). der Standardwert für das fehlende A ist 1. Die Art und Weise, wie diese für den Shader angezeigt wird, hängt vom Textur Ressourcentyp ab. Sie nimmt die Form der ersten typisierten Komponente an, die tatsächlich im Textur Ressourcentyp vorhanden ist (beginnend von Links in RGBA-Reihenfolge). Wenn dieses Formular unorm oder float ist, ist der Standardwert für das fehlende A 1.0 f. Wenn das Formular "Sint" oder "uint" ist, ist der Standardwert für das fehlende "A" 0x1.

Wenn ein Shader z. b. den typlosen Textur Ressourcentyp " [**DXGI- \_ Format \_ R24 \_ unorm \_ X8 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) " liest, sind die Standardwerte für "G" und "B" 0 und der Standardwert für "1.0 f;". Wenn ein Shader den [**\_ \_ R16G16 \_ uint**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) -Textur Ressourcentyp im DXGI-Format liest, ist der Standardwert für b 0 (null), und der Standardwert für eine ist 0x00000001; wenn ein Shader den-Textur Ressourcentyp " [**DXGI- \_ Format \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

## <a name="example-2"></a>Beispiel 2

Im folgenden finden Sie ein Beispiel für die Textur Stichproben Verwendung einer Textur Methode.


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Dieses Objekt wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md) und höhere shadermodelle | ja       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

