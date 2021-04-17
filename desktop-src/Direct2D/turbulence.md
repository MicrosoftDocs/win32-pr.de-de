---
title: Turbulenzen Effekt
description: Verwenden Sie den Turbulenz Effekt, um eine Bitmap basierend auf der Perlin-Rausch Funktion zu generieren.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- Turbulenzen Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f67f615ec5b68ca285a048b68bc7bc8eab6e24
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104565902"
---
# <a name="turbulence-effect"></a>Turbulenzen Effekt

Verwenden Sie den Turbulenz Effekt, um eine Bitmap basierend auf der Perlin-Rausch Funktion zu generieren.

Der Turbulenz Effekt hat kein Eingabebild.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Turbulence.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Rausch Modi](#noise-modes)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

![ein Screenshot mit dem Effekt Beispiel zeigt die Ausgabe des Turbulenzen Effekts.](images/32-turbulence.png)

Der Turbulenz Effekt berechnet die Summe von einem oder mehreren Oktaven der Perlin-Rausch Funktion. Perlin-Rauschen ist eine pseudo zufällige Funktion, deren Wert von der Häufigkeit, der Position und dem Ausgangswert abhängig ist. Der Effekt generiert die RGBA-Werte mithilfe einer dieser Gleichungen.

Wenn Sie das D2D1- \_ Turbulenz Rauschen-Summen-Summen Füll Modus auswählen, wird \_ \_ \_ diese Gleichung verwendet.

![Screenshot, der die zum Generieren einer Bitmap verwendete "Turbulence"-Funktion anzeigt.](images/turbulence-equation1.png)

Wenn Sie den \_ Rausch Modus D2D1 Turbulenz Rauschen auswählen, wird \_ \_ diese Gleichung verwendet.

![die zum Generieren einer Bitmap verwendete "Turbulence"-Funktion.](images/turbulence-equation2.png)

> [!Note]  
> Die `PerlinNoise` -Funktion hat einen Bereich von \[ -1, 1 \] .

 

Dieser Effekt gibt Pixelwerte in einem prämultiplizierten Alpha aus.

## <a name="effect-properties"></a>Effekt Eigenschaften



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Anzeige Name und indexenumeration</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Offset<br/> D2D1_TURBULENCE_PROP_OFFSET<br/></td>
<td>Die Koordinaten, an denen die Turbulenzen ausgegeben werden.<br/> Der Algorithmus, der zum Generieren des Perlin-Rauschens verwendet wird, ist Positions abhängig, sodass ein anderer Offset eine andere Ausgabe ergibt. Diese Eigenschaft ist nicht gebunden, und die Einheiten werden in Dips angegeben. <br/>
<blockquote>
[!Note]<br />
Der Offset hat nicht denselben Effekt wie eine Übersetzung, weil die Rausch funktionsausgabe unendlich ist und die Funktion die Kachel umschließt.
</blockquote>
<br/> Der Typ ist D2D1_VECTOR_2F.<br/> Der Standardwert ist {0,0 f, 0,0 f}.<br/></td>
</tr>
<tr class="even">
<td>Size<br/> D2D1_TURBULENCE_PROP_SIZE<br/></td>
<td>Die Größe der Turbulenz Ausgabe.<br/> Diese Eigenschaft ist nicht gebunden, und die Einheiten werden in Dips angegeben. <br/>
<br/> Der Typ ist D2D1_VECTOR_2F.<br/> Der Standardwert ist {0,0 f, 0,0 f}.<br/></td>
</tr>
<tr class="odd">
<td>Basefrequency<br/> D2D1_TURBULENCE_PROP_BASE_FREQUENCY<br/></td>
<td>Die Basis Frequenzen in der X-und Y-Richtung. Diese Eigenschaft ist ein float-Wert und muss größer als 0 sein. Die Einheiten werden in 1/Dips angegeben. <br/> Der Wert 1 (1/Dips) für die Basisfrequenz führt dazu, dass der Perlin-Rausch einen gesamten Zeitraum zwischen zwei Pixeln vervollständigt. Die einfache Interpolation für diese Pixel ergibt vollständig zufällige Pixel, da es keine Korrelation zwischen den Pixeln gibt.<br/> Der Wert 0,1 (1/Dips) für die Basisfrequenz wiederholt die Perlin-Rausch Funktion alle 10 Dips. Dies führt zu einer Korrelation zwischen Pixeln, und der typische Turbulenz Effekt ist sichtbar.<br/> Der Typ ist D2D1_VECTOR_2F.<br/> Der Standardwert ist {0,01 f, 0,01 f}.<br/></td>
</tr>
<tr class="even">
<td>Numuctaves<br/> D2D1_TURBULENCE_PROP_NUM_OCTAVES<br/></td>
<td>Die Anzahl der Oktaven für die Rausch Funktion. Diese Eigenschaft ist ein UInt32 und muss größer als 0 sein.<br/> Der Typ ist "UInt32".<br/> Der Standardwert ist 1.<br/></td>
</tr>
<tr class="odd">
<td>Seed<br/> D2D1_TURBULENCE_PROP_SEED<br/></td>
<td>Der Seed für den Pseudo Zufallsgenerator. Diese Eigenschaft ist unbegrenzt.<br/> Der Typ ist "UInt32".<br/> Der Standardwert ist 0.<br/></td>
</tr>
<tr class="even">
<td>Stördatenverkehr<br/> D2D1_TURBULENCE_PROP_NOISE<br/></td>
<td>Der Turbulenz Füll Modus. Diese Eigenschaft kann entweder eine Dezimal-oder eine <em>Bruch</em> Zahl <em>sein.</em> Gibt an, ob eine Bitmap auf der Grundlage von Dezimal Geräuschen oder der Turbulence-Funktion generiert werden soll. Weitere Informationen finden Sie unter <a href="#noise-modes">Rausch Modi</a> . <br/> Der Typ ist D2D1_TURBULENCE_NOISE.<br/> Der Standardwert ist D2D1_TURBULENCE_NOISE_FRACTAL_SUM.<br/></td>
</tr>
<tr class="odd">
<td>Stitchable<br/> D2D1_TURBULENCE_PROP_STITCHABLE<br/></td>
<td>Schaltet die zusammen Fügung ein oder aus. Die Basisfrequenz wird so angepasst, dass die Ausgabe Bitmap angeheftet werden kann. Dies ist hilfreich, wenn Sie mehrere Kopien der Ausgabe des Turbulenz Effekts Kacheln möchten.
<ul>
<li>True: die Ausgabe Bitmap kann (mit dem Kachel Effekt) ohne das Aussehen von Nähten gekachelt werden. Die Basisfrequenz wird so angepasst, dass die Ausgabe Bitmap angeheftet werden kann.</li>
<li>False: die Basisfrequenz wird nicht angepasst, sodass die Nähte zwischen den Kacheln auftreten können, wenn die Bitmap gekachelt ist.</li>
</ul>
<br/> Der Typ ist "bool".<br/> Der Standardwert ist FALSE.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="noise-modes"></a>Rausch Modi



| Enumeration                           | Beschreibung                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| D2D1 \_ Turbulenz Rauschen-Dezimalstellen \_ \_ \_ Summe | Berechnet eine Summe der Oktaven und verschiebt den Ausgabebereich von \[ -1, 1 \] in \[ 0, 1 \] . |
| D2D1- \_ Turbulenzen \_ Rauschen- \_ Turbulenzen   | Berechnet eine Summe des absoluten Werts jeder Oktave.                                  |



 

> [!Note]  
> Keiner der Modi enthält eine explizite Klammer der Ausgabewerte.

 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Dieser Effekt generiert eine Bitmap mit logischer unbegrenzter groß.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Header                   | d2d1effects. h                                                                      |
| Bibliothek                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

