---
description: Blockkomprimierung ist eine Texturkomprimierungstechnik zum Reduzieren der Texturgröße.
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: Blockkomprimierung (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edf93a9d475b21b54baa59f9324a7f69b043bb0c21787c0c2892bfdbe2f6c66d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101256"
---
# <a name="block-compression-direct3d-10"></a>Blockkomprimierung (Direct3D 10)

Blockkomprimierung ist eine Texturkomprimierungstechnik zum Reduzieren der Texturgröße. Im Vergleich zu einer Textur mit 32 Bits pro Farbe kann eine blockkomprimierte Textur bis zu 75 Prozent kleiner sein. Anwendungen sehen in der Regel eine Leistungssteigerung, wenn die Blockkomprimierung aufgrund des geringeren Speicherbedarfs verwendet wird.

Die Blockkomprimierung funktioniert zwar verlustbeend, funktioniert aber gut und wird für alle Texturen empfohlen, die von der Pipeline transformiert und gefiltert werden. Texturen, die direkt dem Bildschirm zugeordnet sind (Benutzeroberflächenelemente wie Symbole und Text), sind keine gute Wahl für die Komprimierung, da Artefakte merklicher sind.

Eine blockkomprimierte Textur muss in allen Dimensionen als Vielfaches der Größe 4 erstellt werden und kann nicht als Ausgabe der Pipeline verwendet werden.

-   [Wie funktioniert die Blockkomprimierung?](#how-does-block-compression-work)
    -   [Speichern von nicht komprimierten Daten](#storing-uncompressed-data)
    -   [Speichern komprimierter Daten](#storing-compressed-data)
-   [Verwenden der Blockkomprimierung](#using-block-compression)
    -   [Virtuelle Größe im Vergleich zur physischen Größe](#virtual-size-versus-physical-size)
-   [Komprimierungsalgorithmen](#compression-algorithms)
    -   [BC1](#bc1)
    -   [BU2](#bc2)
    -   [BC3](#bc3)
    -   [BC4](#bc4)
    -   [BC5](#bc5)
-   [Formatkonvertierung mit Direct3D 10.1](#format-conversion-using-direct3d-101)
-   [Zugehörige Themen](#related-topics)

## <a name="how-does-block-compression-work"></a>Wie funktioniert die Blockkomprimierung?

Die Blockkomprimierung ist eine Technik, mit der die Menge an Arbeitsspeicher reduziert wird, die zum Speichern von Farbdaten erforderlich ist. Indem Sie einige Farben in ihrer ursprünglichen Größe und andere Farben mithilfe eines Codierungsschemas speichern, können Sie den zum Speichern des Bilds erforderlichen Arbeitsspeicher erheblich reduzieren. Da die Hardware komprimierte Daten automatisch decodiert, gibt es keine Leistungseinbußen bei der Verwendung komprimierter Texturen.

Sehen Sie sich die folgenden beiden Beispiele an, um zu sehen, wie die Komprimierung funktioniert. Im ersten Beispiel wird die Menge an Arbeitsspeicher beschrieben, die beim Speichern von nicht komprimierten Daten verwendet wird. Im zweiten Beispiel wird die Menge an Arbeitsspeicher beschrieben, die beim Speichern komprimierter Daten verwendet wird.

### <a name="storing-uncompressed-data"></a>Speichern von nicht komprimierten Daten

Die folgende Abbildung stellt eine unkomprimierte 4×4-Textur dar. Angenommen, jede Farbe enthält eine einzelne Farbkomponente (z.B. Rot) und wird in einem Byte Arbeitsspeicher gespeichert.

![Abbildung einer unkomprimierten 4x4-Textur](images/d3d10-block-compress-1.png)

Die nicht komprimierten Daten werden sequenziell im Arbeitsspeicher angeordnet und erfordern 16 Bytes, wie in der folgenden Abbildung dargestellt.

![Abbildung von nicht komprimierten Daten im sequenziellen Speicher](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a>Speichern komprimierter Daten

Nachdem Sie nun gesehen haben, wie viel Arbeitsspeicher ein nicht komprimiertes Bild verwendet, sehen Sie sich an, wie viel Arbeitsspeicher ein komprimiertes Image speichert. Das [](#bc4) BC4-Komprimierungsformat speichert 2 Farben (jeweils 1 Byte) und 16 3-Bit-Indizes (48 Bits oder 6 Bytes), die zum Interpolieren der ursprünglichen Farben in der Textur verwendet werden, wie in der folgenden Abbildung dargestellt.

![Abbildung des bc4-Komprimierungsformats](images/d3d10-block-compress-3.png)

Der zum Speichern der komprimierten Daten insgesamt erforderliche Speicherplatz beträgt 8 Byte, was gegenüber dem nicht komprimierten Beispiel eine Speichereinsparung von 50 Prozent darstellt. Die Einsparungen sind sogar noch größer, wenn mehr als eine Farbkomponente verwendet wird.

Die erheblichen Speichereinsparungen durch die Blockkomprimierung können zu einer Leistungssteigerung führen. Diese Leistung geht auf Kosten der Imagequalität (aufgrund der Farbinterpolation). die niedrigere Qualität ist jedoch häufig nicht wahrnehmbar.

Im nächsten Abschnitt erfahren Sie, wie Sie mit Direct3D 10 die Blockkomprimierung in Ihrer Anwendung ganz einfach verwenden können.

## <a name="using-block-compression"></a>Verwenden der Blockkomprimierung

Erstellen Sie eine blockkomprimierte Textur genau wie eine unkomprimierte Textur (siehe [Erstellen einer Textur aus einer Datei),](d3d10-graphics-programming-guide-resources-creating-textures.md)mit der Ausnahme, dass Sie ein blockkomprimiertes Format angeben.


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



Erstellen Sie als Nächstes eine Ansicht, um die Textur an die Pipeline zu binden. Da eine blockkomprimierte Textur nur als Eingabe für eine Shaderphase verwendet werden kann, möchten Sie eine Shaderressourcenansicht erstellen, indem [**Sie CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview)aufrufen.

Verwenden Sie eine komprimierte Blocktextur auf die gleiche Weise wie eine unkomprimierte Textur. Wenn Ihre Anwendung einen Arbeitsspeicherzeiger auf blockkomprimierte Daten erhält, müssen Sie die Speicherauffüllung in einer Mipmap berücksichtigen, die bewirkt, dass sich die deklarierte Größe von der tatsächlichen Größe unterscheidet.

### <a name="virtual-size-versus-physical-size"></a>Virtuelle Größe im Vergleich zur physischen Größe

Wenn Sie über Anwendungscode verfügen, der einen Speicherzeiger verwendet, um den Speicher einer komprimierten Blocktextur zu durchgehen, gibt es einen wichtigen Aspekt, der möglicherweise eine Änderung im Anwendungscode erfordert. Eine blockkomprimierte Textur muss ein Vielfaches von 4 in allen Dimensionen sein, da die Blockkomprimierungsalgorithmen für 4x4-Texelblöcke ausgeführt werden. Dies ist ein Problem bei einer Mipmap, deren Anfangsdimensionen durch 4 teilbar sind, aber nicht durch unterteilte Ebenen. Das folgende Diagramm zeigt den Unterschied im Bereich zwischen der virtuellen (deklarierten) Größe und der physischen (tatsächlichen) Größe der einzelnen Mipmapebenen.

![Diagramm der nicht komprimierten und komprimierten Mipmap-Ebenen](images/d3d10-block-compress-pad.png)

Die linke Seite des Diagramms zeigt die Mipmapebenengrößen, die für eine nicht komprimierte Textur mit 60×40 generiert werden. Die Größe der obersten Ebene wird aus dem API-Aufruf übernommen, der die Textur generiert. jede nachfolgende Ebene ist halb so groß wie die vorherige Ebene. Bei einer nicht komprimierten Textur besteht kein Unterschied zwischen der virtuellen (deklarierten) Größe und der physischen (tatsächlichen) Größe.

Auf der rechten Seite des Diagramms werden die Mipmapebenengrößen angezeigt, die für dieselbe 60×40-Textur mit Komprimierung generiert werden. Beachten Sie, dass sowohl die zweite als auch die dritte Ebene über Speicherauffüllung verfügen, um die Größenfaktoren auf jeder Ebene auf 4 zu setzen. Dies ist erforderlich, damit die Algorithmen mit 4×4 Texelblöcken arbeiten können. Dies ist besonders offensichtlich, wenn Sie Mipmap-Ebenen berücksichtigen, die kleiner als 4 sind×4; Die Größe dieser sehr kleinen Mipmapebenen wird auf den nächsten Faktor von 4 aufgerundet, wenn Texturspeicher zugeordnet wird.

Die Stichprobenhardware verwendet die virtuelle Größe. Wenn die Textur entnommen wird, wird die Speicherauffüllung ignoriert. Bei Mipmapebenen, die kleiner als 4×4 sind, werden nur die ersten vier Texel für eine 2×2-Karte verwendet, und nur das erste Texel wird von einem 1×1-Block verwendet. Es gibt jedoch keine API-Struktur, die die physische Größe (einschließlich der Speicherabstand) verfügbar macht.

Achten Sie zusammenfassend darauf, dass Sie beim Kopieren von Bereichen, die blockkomprimierte Daten enthalten, ausgerichtete Speicherblöcke verwenden. Um dies in einer Anwendung zu tun, die einen Speicherzeiger erhält, stellen Sie sicher, dass der Zeiger die Oberflächenhöhe verwendet, um die größe des physischen Arbeitsspeichers zu berücksichtigen.

## <a name="compression-algorithms"></a>Komprimierungsalgorithmen

Blockkomprimierungstechniken in Direct3D untergliedern unkomprimierte Texturdaten in 4×4-Blöcke, komprimieren jeden Block und speichern dann die Daten. Aus diesem Grund muss die Komprimierung von Texturen texturdimensionen aufweisen, die ein Vielfaches von 4 sind.

![Diagramm der Blockkomprimierung](images/d3d10-compression-1.png)

Das obige Diagramm zeigt eine Textur, die in Texelblöcke partitioniert ist. Der erste Block zeigt das Layout der 16 Texel mit der Bezeichnung a-p, aber jeder Block weist die gleiche Datenorganisation auf.

Direct3D implementiert mehrere Komprimierungsschemas, von denen jedes einen anderen Kompromiss zwischen der Anzahl der gespeicherten Komponenten, der Anzahl der Bits pro Komponente und der verbrauchten Arbeitsspeichermenge implementiert. Verwenden Sie diese Tabelle, um das Format auszuwählen, das am besten mit dem Datentyp und der Datenauflösung funktioniert, die am besten zu Ihrer Anwendung passt.



| Quelldaten                     | Datenkomprimierungsauflösung (in Bits) | Wählen Sie dieses Komprimierungsformat aus. |
|---------------------------------|---------------------------------------|--------------------------------|
| Farbe und Alpha aus drei Komponenten | Farbe (5:6:5), Alpha (1) oder kein Alpha  | BC1                            |
| Farbe und Alpha aus drei Komponenten | Farbe (5:6:5), Alpha (4)              | [BU2](#bc2)                    |
| Farbe und Alpha aus drei Komponenten | Farbe (5:6:5), Alpha (8)              | [BC3](#bc3)                    |
| Einkomponentenfarbe             | Eine Komponente (8)                     | [BC4](#bc4)                    |
| Farbe mit zwei Komponenten             | Zwei Komponenten (8:8)                  | [BC5](#bc5)                    |



 

### <a name="bc1"></a>BC1

Verwenden Sie das erste Blockkomprimierungsformat (BC1) (DXGI \_ FORMAT \_ BC1 \_ TYPELESS, DXGI \_ FORMAT \_ BC1 \_ UNORM oder DXGI \_ BC1 \_ UNORM \_ SRGB), um Dreikomponentenfarbdaten mit einer 5:6:5-Farbe (5 Bits Rot, 6 Bits Grün, 5 Bits Blau) zu speichern. Dies gilt auch, wenn die Daten auch 1-Bit-Alpha enthalten. Bei einer 4×4-Textur mit dem größtmöglichen Datenformat reduziert das BC1-Format den erforderlichen Arbeitsspeicher von 48 Byte (16 Farben × 3 Komponenten/Farbe × 1 Byte/Komponente) auf 8 Byte Arbeitsspeicher.

Der Algorithmus funktioniert mit 4×4 Blöcken von Texeln. Anstatt 16 Farben zu speichern, speichert der Algorithmus 2 Referenzfarben (Farbe \_ 0 und Farbe \_ 1) und 16 2-Bit-Farbindizes (blockiert a–p), wie im folgenden Diagramm dargestellt.

![Diagramm des Layouts für die bc1-Komprimierung](images/d3d10-compression-bc1.png)

Die Farbindizes (a–p) werden verwendet, um die ursprünglichen Farben aus einer Farbtabelle nachzuschlagen. Die Farbtabelle enthält 4 Farben. Die ersten beiden Farben – Farbe \_ 0 und Farbe \_ 1 – sind die minimalen und maximalen Farben. Die anderen beiden Farben, Farbe \_ 2 und Farbe \_ 3, sind Zwischenfarben, die mit linearer Interpolation berechnet werden.


```
color_2 = 2/3*color_0 + 1/3*color_1
color_3 = 1/3*color_0 + 2/3*color_1
```



Den vier Farben werden 2-Bit-Indexwerte zugewiesen, die in den Blöcken a–p gespeichert werden.


```
color_0 = 00
color_1 = 01
color_2 = 10
color_3 = 11
```



Schließlich werden alle Farben in den Blöcken a–p mit den vier Farben in der Farbtabelle verglichen, und der Index für die nächstgelegene Farbe wird in den 2-Bit-Blöcken gespeichert.

Dieser Algorithmus eignet sich auch für Daten, die ebenfalls 1-Bit-Alpha enthalten. Der einzige Unterschied besteht darin, dass Farbe \_ 3 auf 0 (was eine transparente Farbe darstellt) und Farbe \_ 2 eine lineare Mischung aus Farbe \_ 0 und Farbe \_ 1 ist.


```
color_2 = 1/2*color_0 + 1/2*color_1;
color_3 = 0;
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> Dieses Format ist sowohl in Direct3D 9 als auch in 10 vorhanden.<br/>
<ul>
<li>In Direct3D 9 wird das BC1-Format als D3DFMT_DXT1 bezeichnet.</li>
<li>In Direct3D 10 wird das BC1-Format durch DXGI_FORMAT_BC1_UNORM oder DXGI_FORMAT_BC1_UNORM_SRGB dargestellt.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc2"></a>BU2

Verwenden Sie das BC2-Format (DXGI \_ FORMAT \_ BC2 \_ TYPELESS, DXGI \_ FORMAT \_ BC2 \_ UNORM oder DXGI \_ BC2 \_ UNORM \_ SRGB), um Daten zu speichern, die Farb- und Alphadaten mit geringer Koherität enthalten (verwenden Sie [BC3](#bc3) für hochgradig konsistente Alphadaten). Im BC2-Format werden RGB-Daten als 5:6:5-Farbe (5 Bits Rot, 6 Bits Grün, 5 Bits Blau) und Alpha als separater 4-Bit-Wert gespeichert. Bei einer 4×4-Textur mit dem größtmöglichen Datenformat reduziert diese Komprimierungstechnik den erforderlichen Arbeitsspeicher von 64 Bytes (16 Farben × 4 Komponenten/Farbe × 1 Byte/Komponente) auf 16 Bytes Arbeitsspeicher.

Im BC2-Format werden Farben mit der gleichen Anzahl von Bits und Datenlayout wie das [BC1-Format](#bc1) gespeichert. BC2 benötigt jedoch zusätzliche 64 Bit Arbeitsspeicher, um die Alphadaten zu speichern, wie im folgenden Diagramm dargestellt.

![Diagramm des Layouts für die bc2-Komprimierung](images/d3d10-compression-bc2.png)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> Dieses Format ist sowohl in Direct3D 9 als auch in 10 vorhanden.<br/>
<ul>
<li>In Direct3D 9 wird das BC2-Format als D3DFMT_DXT2 und D3DFMT_DXT3 bezeichnet.</li>
<li>In Direct3D 10 wird das BC2-Format durch DXGI_FORMAT_BC2_UNORM oder DXGI_FORMAT_BC2_UNORM_SRGB dargestellt.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc3"></a>BC3

Verwenden Sie das BC3-Format (DXGI \_ FORMAT \_ BC3 \_ TYPELESS, DXGI \_ FORMAT \_ BC3 \_ UNORM oder DXGI \_ BC3 \_ UNORM \_ SRGB), um hochgradig konsistente Farbdaten zu speichern (verwenden Sie [BC2](#bc2) mit weniger konsistenten Alphadaten). Im BC3-Format werden Farbdaten mit 5:6:5 Farben (5 Bits Rot, 6 Bits Grün, 5 Bits Blau) und Alphadaten mit einem Byte gespeichert. Bei einer 4×4-Textur mit dem größtmöglichen Datenformat reduziert diese Komprimierungstechnik den erforderlichen Arbeitsspeicher von 64 Bytes (16 Farben × 4 Komponenten/Farbe × 1 Byte/Komponente) auf 16 Bytes Arbeitsspeicher.

Im BC3-Format werden Farben mit der gleichen Anzahl von Bits und Datenlayout wie das [BC1-Format](#bc1) gespeichert. BC3 benötigt jedoch zusätzliche 64 Bit Arbeitsspeicher, um die Alphadaten zu speichern. Das BC3-Format verarbeitet Alpha, indem zwei Verweiswerte gespeichert und zwischen diesen interpoliert werden (ähnlich wie BC1 RGB-Farben speichert).

Der Algorithmus funktioniert mit 4×4 Blöcken von Texeln. Anstatt 16 Alphawerte zu speichern, speichert der Algorithmus 2 Verweis alphas (alpha \_ 0 und alpha \_ 1) und 16 3-Bit-Farbindizes (Alpha a bis p), wie im folgenden Diagramm dargestellt.

![Diagramm des Layouts für die bc3-Komprimierung](images/d3d10-compression-bc3.png)

Das BC3-Format verwendet die Alphaindizes (a–p), um die ursprünglichen Farben aus einer Nachschlagetabelle nachzuschlagen, die 8 Werte enthält. Die ersten beiden Werte – Alpha \_ 0 und Alpha \_ 1 – sind die Minimal- und Höchstwerte. Die anderen sechs Zwischenwerte werden mithilfe der linearen Interpolation berechnet.

Der Algorithmus bestimmt die Anzahl der interpolierten Alphawerte, indem die beiden Alpha-Verweiswerte untersucht werden. Wenn Alpha \_ 0 größer als Alpha \_ 1 ist, interpoliert BC3 sechs Alphawerte, andernfalls 4. Wenn BC3 nur vier Alphawerte interpoliert, werden zwei zusätzliche Alphawerte festgelegt (0 für vollständig transparent und 255 für vollständig deckende Alphawerte). BC3 komprimiert die Alphawerte im Texelbereich 4×4, indem der Bitcode gespeichert wird, der den interpolierten Alphawerten entspricht, die am besten mit dem ursprünglichen Alpha für ein bestimmtes Texel übereinstimmen.


```
if( alpha_0 > alpha_1 )
{
  // 6 interpolated alpha values.
  alpha_2 = 6/7*alpha_0 + 1/7*alpha_1; // bit code 010
  alpha_3 = 5/7*alpha_0 + 2/7*alpha_1; // bit code 011
  alpha_4 = 4/7*alpha_0 + 3/7*alpha_1; // bit code 100
  alpha_5 = 3/7*alpha_0 + 4/7*alpha_1; // bit code 101
  alpha_6 = 2/7*alpha_0 + 5/7*alpha_1; // bit code 110
  alpha_7 = 1/7*alpha_0 + 6/7*alpha_1; // bit code 111
}
else
{
  // 4 interpolated alpha values.
  alpha_2 = 4/5*alpha_0 + 1/5*alpha_1; // bit code 010
  alpha_3 = 3/5*alpha_0 + 2/5*alpha_1; // bit code 011
  alpha_4 = 2/5*alpha_0 + 3/5*alpha_1; // bit code 100
  alpha_5 = 1/5*alpha_0 + 4/5*alpha_1; // bit code 101
  alpha_6 = 0;                         // bit code 110
  alpha_7 = 255;                       // bit code 111
}
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/>
<ul>
<li>In Direct3D 9 wird das BC3-Format als D3DFMT_DXT4 und D3DFMT_DXT5 bezeichnet.</li>
<li>In Direct3D 10 wird das BC3-Format durch DXGI_FORMAT_BC3_UNORM oder DXGI_FORMAT_BC3_UNORM_SRGB dargestellt.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc4"></a>BC4

Verwenden Sie das BC4-Format, um Einkomponentenfarbdaten mit 8 Bits für jede Farbe zu speichern. Aufgrund der erhöhten Genauigkeit (im Vergleich zu [BC1)](#bc1)eignet sich BC4 ideal zum Speichern von Gleitkommadaten im Bereich von \[ 0 bis 1 \] im \_ DXGI FORMAT \_ BC4 \_ UNORM-Format und \[ -1 bis +1 \] im DXGI FORMAT \_ \_ BC4 \_ SNORM-Format. Bei einer 4×4-Textur, die das größtmögliche Datenformat verwendet, reduziert diese Komprimierungstechnik den erforderlichen Arbeitsspeicher von 16 Bytes (16 Farben × 1 Komponenten/Farbe × 1 Byte/Komponente) auf 8 Bytes.

Der Algorithmus funktioniert mit 4×4 Blöcken von Texeln. Anstatt 16 Farben zu speichern, speichert der Algorithmus 2 Referenzfarben (rot \_ 0 und rot \_ 1) und 16 3-Bit-Farbindizes (rot a bis rot p), wie im folgenden Diagramm dargestellt.

![Diagramm des Layouts für die bc4-Komprimierung](images/d3d10-compression-bc4.png)

Der Algorithmus verwendet die 3-Bit-Indizes, um Farben aus einer Farbtabelle nachzuschlagen, die acht Farben enthält. Die ersten beiden Farben – Rot \_ 0 und Rot \_ 1 – sind die minimalen und maximalen Farben. Der Algorithmus berechnet die verbleibenden Farben mithilfe der linearen Interpolation.

Der Algorithmus bestimmt die Anzahl der interpolierten Farbwerte, indem die beiden Verweiswerte untersucht werden. Wenn rot \_ 0 größer als rot \_ 1 ist, interpoliert BC4 sechs Farbwerte, andernfalls 4. Wenn BC4 nur vier Farbwerte interpoliert, werden zwei zusätzliche Farbwerte festgelegt (0,0f für vollständig transparent und 1,0f für vollständig deckend). BC4 komprimiert die Alphawerte im 4×4-Texelbereich, indem der Bitcode gespeichert wird, der den interpolierten Alphawerten entspricht, die dem ursprünglichen Alpha für ein bestimmtes Texel am besten entsprechen.

-   [BC4 \_ UNORM](/windows)
-   [BC4 \_ SNORM](/windows)

### <a name="bc4_unorm"></a>BC4 \_ UNORM

Die Interpolation der Einzelkomponentendaten erfolgt wie im folgenden Codebeispiel.


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



Den Referenzfarben werden 3-Bit-Indizes (000–111, da es 8 Werte gibt) zugewiesen, die während der Komprimierung in Blöcken rot a bis rot p gespeichert werden.

### <a name="bc4_snorm"></a>BC4 \_ SNORM

Das DXGI \_ FORMAT \_ BC4 \_ SNORM ist genau identisch, mit der Ausnahme, dass die Daten im SNORM-Bereich codiert sind und 4 Farbwerte interpoliert werden. Die Interpolation der Einzelkomponentendaten erfolgt wie im folgenden Codebeispiel.


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                     // bit code 110
  red_7 =  1.0f;                     // bit code 111
}
```



Den Referenzfarben werden 3-Bit-Indizes (000–111, da es 8 Werte gibt) zugewiesen, die während der Komprimierung in Blöcken rot a bis rot p gespeichert werden.

### <a name="bc5"></a>BC5

Verwenden Sie das BC5-Format, um Zweikomponentenfarbdaten mit 8 Bits für jede Farbe zu speichern. Aufgrund der erhöhten Genauigkeit (im Vergleich zu [BC1)](#bc1)eignet sich BC5 ideal zum Speichern von Gleitkommadaten im Bereich von \[ 0 bis 1 \] im \_ DXGI FORMAT \_ BC5 \_ UNORM-Format und \[ -1 bis +1 \] im DXGI FORMAT \_ \_ BC5 \_ SNORM-Format. Bei einer 4×4-Textur mit dem größtmöglichen Datenformat reduziert diese Komprimierungstechnik den erforderlichen Arbeitsspeicher von 32 Byte (16 Farben × 2 Komponenten/Farbe × 1 Byte/Komponente) auf 16 Bytes.

Der Algorithmus funktioniert mit 4×4 Blöcken von Texeln. Anstatt 16 Farben für beide Komponenten zu speichern, speichert der Algorithmus zwei Referenzfarben für jede Komponente (rot \_ 0, rot \_ 1, grün \_ 0 und grün \_ 1) und 16 3-Bit-Farbindizes für jede Komponente (rot a bis rot p und grün a bis grün p), wie im folgenden Diagramm dargestellt.

![Diagramm des Layouts für die bc5-Komprimierung](images/d3d10-compression-bc5.png)

Der Algorithmus verwendet die 3-Bit-Indizes, um Farben aus einer Farbtabelle nachzuschlagen, die acht Farben enthält. Die ersten beiden Farben – Rot \_ 0 und Rot \_ 1 (oder Grün \_ 0 und Grün \_ 1) – sind die minimalen und maximalen Farben. Der Algorithmus berechnet die verbleibenden Farben mithilfe der linearen Interpolation.

Der Algorithmus bestimmt die Anzahl der interpolierten Farbwerte, indem die beiden Verweiswerte untersucht werden. Wenn rot \_ 0 größer als rot \_ 1 ist, interpoliert BC5 sechs Farbwerte, andernfalls 4. Wenn BC5 nur vier Farbwerte interpoliert, werden die verbleibenden beiden Farbwerte auf 0,0f und 1,0f festgelegt.

-   [BC5 \_ UNORM](/windows)
-   [BC5 \_ SNORM](/windows)

### <a name="bc5_unorm"></a>BC5 \_ UNORM

Die Interpolation der Einzelkomponentendaten erfolgt wie im folgenden Codebeispiel. Die Berechnungen für die grünen Komponenten sind ähnlich.


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



Den Referenzfarben werden 3-Bit-Indizes (000–111, da es 8 Werte gibt) zugewiesen, die während der Komprimierung in Blöcken rot a bis rot p gespeichert werden.

### <a name="bc5_snorm"></a>BC5 \_ SNORM

Das DXGI \_ FORMAT \_ BC5 \_ SNORM ist genau gleich, mit der Ausnahme, dass die Daten im SNORM-Bereich codiert sind und wenn 4 Datenwerte interpoliert werden, sind die beiden zusätzlichen Werte -1,0f und 1,0f. Die Interpolation der Einzelkomponentendaten erfolgt wie im folgenden Codebeispiel. Die Berechnungen für die grünen Komponenten sind ähnlich.


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                    // bit code 110
  red_7 =  1.0f;                    // bit code 111
}
```



Den Referenzfarben werden 3-Bit-Indizes (000–111, da es 8 Werte gibt) zugewiesen, die während der Komprimierung in Blöcken rot a bis rot p gespeichert werden.

## <a name="format-conversion-using-direct3d-101"></a>Formatkonvertierung mit Direct3D 10.1

Direct3D 10.1 ermöglicht Kopien zwischen vorstrukturierten Texturen und blockkomprimierten Texturen der gleichen Bitbreite. Die Funktionen, die dies erreichen können, sind [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) und [**CopySubresourceRegion.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)

Ab Direct3D 10.1 können Sie [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) und [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) verwenden, um zwischen einigen Formattypen zu kopieren. Dieser Kopiervorgang führt eine Formatkonvertierung durch, die Ressourcendaten als anderen Formattyp neu interpretiert. Betrachten Sie dieses Beispiel, das den Unterschied zwischen der Neuinterpretation von Daten und dem Verhalten eines typischeren Konvertierungstyps zeigt:


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



Um "f" als Typ von "u" neu zu interpretieren, verwenden Sie [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



In der vorherigen Neuinterpretation ändert sich der zugrunde liegende Wert der Daten nicht. [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) interpretiert float als ganze Zahl ohne Vorzeichen neu.

Verwenden Sie die Zuweisung, um den typischeren Konvertierungstyp auszuführen:


```
    u = f; // ‘u’ becomes 1.
```



In der vorherigen Konvertierung ändert sich der zugrunde liegende Wert der Daten.

In der folgenden Tabelle sind die zulässigen Quell- und Zielformate aufgeführt, die Sie bei dieser Neuinterpretationsart der Formatkonvertierung verwenden können. Sie müssen die Werte ordnungsgemäß codieren, damit die Neuinterpretation wie erwartet funktioniert.



| Bitbreite | Unkomprimierte Ressource                                                                                                                                               | Block-Compressed Ressource                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 32        | DXGI \_ FORMAT \_ R32 \_ UINT<br/> DXGI \_ FORMAT \_ R32 \_ SINT<br/>                                                                                               | DXGI \_ FORMAT \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                   |
| 64        | DXGI \_ FORMAT \_ R16G16B16A16 \_ UINT<br/> DXGI \_ FORMAT \_ R16G16B16A16 \_ SINT<br/> \_DXGI-FORMAT \_ R32G32 \_ UINT<br/> DXGI \_ FORMAT \_ R32G32 \_ SINT<br/> | DXGI \_ FORMAT \_ BC1 \_ UNORM \[ \_ SRGB\]<br/> DXGI \_ FORMAT \_ BC4 \_ UNORM<br/> DXGI \_ FORMAT \_ BC4 \_ SNORM<br/>                                               |
| 128       | DXGI \_ FORMAT \_ R32G32B32A32 \_ UINT<br/> DXGI \_ FORMAT \_ R32G32B32A32 \_ SINT<br/>                                                                             | DXGI \_ FORMAT \_ BC2 \_ UNORM \[ \_ SRGB\]<br/> DXGI \_ FORMAT \_ BC3 \_ UNORM \[ \_ SRGB\]<br/> DXGI \_ FORMAT \_ BC5 \_ UNORM<br/> DXGI \_ FORMAT \_ BC5 \_ SNORM<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
