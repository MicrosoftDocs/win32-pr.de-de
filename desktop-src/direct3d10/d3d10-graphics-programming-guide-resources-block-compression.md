---
description: Die Block Komprimierung ist eine Textur Komprimierungs Methode zum Reduzieren der Textur Größe.
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: Block Komprimierung (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fcfb4bc91256415ab23686b7333df7d21df335d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568236"
---
# <a name="block-compression-direct3d-10"></a>Block Komprimierung (Direct3D 10)

Die Block Komprimierung ist eine Textur Komprimierungs Methode zum Reduzieren der Textur Größe. Im Vergleich zu einer Textur mit 32 Bit pro Farbe kann eine Block komprimierte Textur bis zu 75 Prozent kleiner sein. Anwendungen sehen in der Regel eine Leistungssteigerung bei der Verwendung der Block Komprimierung aufgrund der geringeren Speicher Beanspruchung.

Die Block Komprimierung funktioniert zwar gut, aber Sie wird für alle Texturen empfohlen, die von der Pipeline transformiert und gefiltert werden. Texturen, die direkt dem Bildschirm zugeordnet sind (UI-Elemente wie Symbole und Text), sind keine guten Auswahlmöglichkeiten für die Komprimierung, da Artefakte leichter erkennbar sind.

Eine Block komprimierte Textur muss als Vielfaches der Größe 4 in allen Dimensionen erstellt werden und kann nicht als Ausgabe der Pipeline verwendet werden.

-   [Wie funktioniert die Block Komprimierung?](#how-does-block-compression-work)
    -   [Speichern von nicht komprimierten Daten](#storing-uncompressed-data)
    -   [Speichern von komprimierten Daten](#storing-compressed-data)
-   [Verwenden von Block Komprimierung](#using-block-compression)
    -   [Virtuelle Größe im Vergleich zur physischen Größe](#virtual-size-versus-physical-size)
-   [Komprimierungs Algorithmen](#compression-algorithms)
    -   [BC1](#bc1)
    -   [BU2](#bc2)
    -   [BC3](#bc3)
    -   [BC4](#bc4)
    -   [BC5](#bc5)
-   [Format Konvertierung mit Direct3D 10,1](#format-conversion-using-direct3d-101)
-   [Zugehörige Themen](#related-topics)

## <a name="how-does-block-compression-work"></a>Wie funktioniert die Block Komprimierung?

Die Block Komprimierung ist eine Technik zum Reduzieren des Arbeitsspeichers, der zum Speichern von Farbdaten erforderlich ist. Wenn Sie einige Farben in ihrer ursprünglichen Größe und andere Farben mithilfe eines Codierungs Schemas speichern, können Sie die Menge an Arbeitsspeicher, die zum Speichern des Bilds erforderlich ist, erheblich reduzieren. Da komprimierte Daten von der Hardware automatisch decodiert werden, gibt es keine Leistungs Einbuße bei der Verwendung komprimierter Texturen.

Sehen Sie sich die folgenden beiden Beispiele an, um zu sehen, wie die Komprimierung funktioniert. Im ersten Beispiel wird die Menge an Arbeitsspeicher beschrieben, die beim Speichern von nicht komprimierten Daten verwendet wird. im zweiten Beispiel wird die Menge an Arbeitsspeicher beschrieben, die beim Speichern komprimierter Daten verwendet wird.

### <a name="storing-uncompressed-data"></a>Speichern von nicht komprimierten Daten

Die folgende Abbildung stellt eine unkomprimierte 4 × 4-Textur dar. Nehmen Sie an, dass jede Farbe eine einzelne Farbkomponente (z. h. rot) enthält und in einem Byte Arbeitsspeicher gespeichert wird.

![Abbildung einer unkomprimierten 4 x 4-Textur](images/d3d10-block-compress-1.png)

Die nicht komprimierten Daten werden sequenziell im Speicher angeordnet und erfordern 16 Bytes, wie in der folgenden Abbildung dargestellt.

![Abbildung von nicht komprimierten Daten in sequenzieller Arbeitsspeicher](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a>Speichern von komprimierten Daten

Nachdem Sie nun gesehen haben, wie viel Arbeitsspeicher ein nicht komprimiertes Image verwendet, sehen Sie sich an, wie viel Arbeitsspeicher ein komprimiertes Image speichert. Das [BC1](#bc1) -Komprimierungs Format speichert zwei Farben (jeweils 1 Byte) und 16 3-Bit-Indizes (48 Bits oder 6 Bytes), mit denen die ursprünglichen Farben in der Textur interpolieren werden, wie in der folgenden Abbildung dargestellt.

![Abbildung des BC1-Komprimierungs Formats](images/d3d10-block-compress-3.png)

Der Gesamt Speicherplatz, der zum Speichern der komprimierten Daten erforderlich ist, beträgt 8 50 Byte Die Einsparungen sind noch größer, wenn mehr als eine Farbkomponente verwendet wird.

Die beträchtlichen Speicher Einsparungen durch die Block Komprimierung können zu einer Leistungssteigerung führen. Diese Leistung ergibt sich aus den Kosten der Bildqualität (aufgrund der Farb interpolung). die niedrigere Qualität ist jedoch häufig nicht erkennbar.

Im nächsten Abschnitt erfahren Sie, wie Sie mit Direct3D 10 die Block Komprimierung in Ihrer Anwendung ganz einfach verwenden können.

## <a name="using-block-compression"></a>Verwenden von Block Komprimierung

Erstellen Sie eine Block komprimierte Textur wie eine nicht komprimierte Textur (siehe [Create a texture from a file](d3d10-graphics-programming-guide-resources-creating-textures.md)), mit dem Unterschied, dass Sie ein Block komprimiertes Format angeben.


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



Erstellen Sie als nächstes eine Ansicht, um die Textur an die Pipeline zu binden. Da eine Block komprimierte Textur nur als Eingabe für eine Shader-Phase verwendet werden kann, sollten Sie eine Shader-Ressourcen Ansicht erstellen, indem Sie [**createshaderresourceview**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview)aufrufen.

Verwenden Sie eine komprimierte-Struktur auf die gleiche Weise wie eine nicht komprimierte Textur. Wenn Ihre Anwendung einen Speicher Zeiger auf Block komprimierte Daten erhält, müssen Sie die Speicher Auffüll Zeichen in einer MipMap berücksichtigen, die bewirkt, dass die deklarierte Größe von der tatsächlichen Größe abweicht.

### <a name="virtual-size-versus-physical-size"></a>Virtuelle Größe im Vergleich zur physischen Größe

Wenn Sie über Anwendungscode verfügen, in dem ein Speicher Zeiger zum Durchlaufen des Speichers einer komprimierten Blocktextur verwendet wird, ist ein wichtiger Aspekt zu beachten, der möglicherweise eine Änderung des Anwendungs Codes erfordert. Eine Block komprimierte Textur muss ein Vielfaches von 4 in allen Dimensionen sein, da die Block Komprimierungs Algorithmen auf 4 x 4 texverblöcken angewendet werden. Dies stellt ein Problem für eine MipMap dar, deren anfängliche Dimensionen durch 4 teilbar sind, die unterteilten Ebenen jedoch nicht. Das folgende Diagramm zeigt den Unterschied zwischen der virtuellen (deklarierten) Größe und der physischen (tatsächlichen) Größe der einzelnen MipMap-Ebenen.

![Diagramm der nicht komprimierten und komprimierten MipMap-Ebenen](images/d3d10-block-compress-pad.png)

Die linke Seite des Diagramms zeigt die Größen der MipMap-Ebenen an, die für eine unkomprimierte 60 × 40-Textur generiert werden. Der API-Befehl, der die Textur generiert, wird auf oberster Ebene festgenommen. jede nachfolgende Ebene ist die Hälfte der Größe der vorherigen Ebene. Bei einer nicht komprimierten Textur besteht kein Unterschied zwischen der virtuellen (deklarierten) Größe und der physischen (tatsächlichen) Größe.

Auf der rechten Seite des Diagramms werden die Größen der MipMap-Ebene angezeigt, die für die gleiche 60 × 40-Textur mit Komprimierung generiert werden. Beachten Sie, dass die zweite und die dritte Ebene eine Speicher Auffüll Zeichen aufweisen, um die Größen Faktoren 4 auf jeder Ebene zu erhöhen. Dies ist erforderlich, damit die Algorithmen in 4 × 4 textexblöcken betrieben werden können. Dies ist besonders offensichtlich, wenn MipMap-Ebenen in Erwägung gezogen werden, die kleiner sind als 4 × 4. die Größe dieser sehr kleinen MipMap-Ebenen wird auf den nächstgelegenen Faktor 4 aufgerundet, wenn Texturspeicher zugeordnet wird.

Sampling der Hardware verwendet die virtuelle Größe. Beim Sampling der Textur wird die Arbeitsspeicher Auffüll Zeichen ignoriert. Bei MipMap-Ebenen, die kleiner als 4 × 4 sind, werden nur die ersten vier texeln für eine 2 × 2-Karte verwendet, und nur die ersten texeln werden von einem 1 × 1-Block verwendet. Es gibt jedoch keine API-Struktur, die die physische Größe (einschließlich des Speicher Paddings) verfügbar macht.

Beachten Sie bei der Zusammenfassung die Verwendung von ausgerichteten Speicherblöcken beim Kopieren von Regionen, die Block komprimierte Daten enthalten. Um dies in einer Anwendung zu erreichen, die einen Speicher Zeiger abruft, stellen Sie sicher, dass der Zeiger die Oberflächendarstellung verwendet, um die Größe des physischen Speichers zu berücksichtigen.

## <a name="compression-algorithms"></a>Komprimierungs Algorithmen

Die Verfahren zur Block Komprimierung in Direct3D unterbrechen unkomprimierte Textur Daten in 4 × 4-Blöcke, komprimieren jeden Block und speichern die Daten. Daher wird erwartet, dass Texturen komprimierte Textur Dimensionen aufweisen, die vielfachen von 4 sind.

![Diagramm der Block Komprimierung](images/d3d10-compression-1.png)

Das vorangehende Diagramm zeigt eine Textur, die in texblöcke partitioniert ist. Der erste Block zeigt das Layout der 16 texeln mit der Bezeichnung a-p an, aber jeder Block verfügt über dieselbe Organisation der Daten.

Direct3D implementiert mehrere Komprimierungs Schemas, von denen jedes einen anderen Kompromiss zwischen der Anzahl gespeicherter Komponenten, der Anzahl der Bits pro Komponente und dem verbrauchten Arbeitsspeicher implementiert. Verwenden Sie diese Tabelle, um das Format auszuwählen, das am besten mit dem Datentyp und der Datenauflösung funktioniert, die für Ihre Anwendung am besten geeignet ist.



| Quelldaten                     | Auflösung der Datenkomprimierung (in Bits) | Dieses Komprimierungs Format auswählen |
|---------------------------------|---------------------------------------|--------------------------------|
| Farbe und Alpha der drei Komponenten | Farbe (5:6:5), Alpha (1) oder kein Alpha  | BC1                            |
| Farbe und Alpha der drei Komponenten | Farbe (5:6:5), Alpha (4)              | [BU2](#bc2)                    |
| Farbe und Alpha der drei Komponenten | Farbe (5:6:5), Alpha (8)              | [BC3](#bc3)                    |
| Farbe mit einer Komponente             | Eine Komponente (8)                     | [BC4](#bc4)                    |
| Farbe mit zwei Komponenten             | Zwei Komponenten (8:8)                  | [BC5](#bc5)                    |



 

### <a name="bc1"></a>BC1

Verwenden Sie das erste Block Komprimierungs Format (BC1) (entweder DXGI- \_ Format \_ BC1 \_ typlose, DXGI- \_ Format \_ BC1 \_ unorm oder DXGI \_ BC1 \_ unorm \_ sRGB), um mithilfe einer 5:6:5-Farbe (5 Bits rot, 6 Bits grün, 5 Bits blau) Daten mit drei Komponenten zu speichern. Dies gilt auch, wenn die Daten auch 1-Bit-Alpha enthalten. Wenn eine 4 × 4-Textur mit dem größten möglichen Datenformat verwendet wird, verringert das BC1-Format den benötigten Arbeitsspeicher von 48 Byte (16 Farben × 3 Komponenten/Farbe × 1 Byte/Komponente) auf 8 Bytes Arbeitsspeicher.

Der-Algorithmus funktioniert an 4 × 4 Texels-Blöcken. Anstatt 16 Farben zu speichern, speichert der Algorithmus 2 Verweis Farben (Farbe \_ 0 und Farbe \_ 1) und 16 2-Bit-Farbindizes (blockiert ein – p), wie im folgenden Diagramm dargestellt.

![Diagramm des Layouts für die BC1-Komprimierung](images/d3d10-compression-bc1.png)

Die Farbindizes (a – p) werden verwendet, um die ursprünglichen Farben aus einer Farbtabelle zu suchen. Die Farbtabelle enthält 4 Farben. Die ersten beiden Farben – Color \_ 0 und Color \_ 1 – sind die Mindest-und höchst Farben. Bei den anderen beiden Farben (Farbe \_ 2 und Farbe \_ 3) handelt es sich um zwischen Farben, die mit linearer Interpolationen berechnet werden.


```
color_2 = 2/3*color_0 + 1/3*color_1
color_3 = 1/3*color_0 + 2/3*color_1
```



Die vier Farben sind 2-Bit-Indexwerte zugewiesen, die in Blocks a – p gespeichert werden.


```
color_0 = 00
color_1 = 01
color_2 = 10
color_3 = 11
```



Schließlich wird jede der Farben in Blocks a – p mit den vier Farben in der Farbtabelle verglichen, und der Index für die nächstgelegene Farbe wird in den 2-Bit-Blöcken gespeichert.

Dieser Algorithmus eignet sich für Daten, die auch 1-Bit-Alpha enthalten. Der einzige Unterschied besteht darin, dass Farbe \_ 3 auf 0 festgelegt ist (was eine transparente Farbe darstellt) und Farbe \_ 2 eine lineare Mischung aus Farbe \_ 0 und Farbe \_ 1 ist.


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

Verwenden Sie das BC2-Format (entweder DXGI- \_ Format \_ BC2 \_ typlose, DXGI- \_ Format \_ BC2 \_ unorm oder DXGI \_ BC2 \_ unorm \_ sRGB), um Daten zu speichern, die Farb-und Alpha Daten mit geringer Kohärenz enthalten (verwenden Sie [BC3](#bc3) für hochgradig kohärente Alpha-Daten). Das BC2-Format speichert RGB-Daten als 5:6:5-Farbe (5 Bits rot, 6 Bits grün, 5 Bits blau) und Alpha als separaten 4-Bit-Wert. Wenn eine 4 × 4-Textur mit dem größten möglichen Datenformat angenommen wird, reduziert dieses Komprimierungs Verfahren den von 64 bytes (16 Farben × 4 Komponenten/Farbe × 1 Byte/Komponente) benötigten Arbeitsspeicher auf 16 Bytes an Arbeitsspeicher.

Das Format BC2 speichert Farben mit der gleichen Anzahl von Bits und Datenlayout wie das [BC1](#bc1) -Format. für BC2 sind jedoch zusätzliche 64-Bits Arbeitsspeicher erforderlich, um die Alpha Daten zu speichern, wie im folgenden Diagramm dargestellt.

![Diagramm des Layouts für die BC2-Komprimierung](images/d3d10-compression-bc2.png)

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

Verwenden Sie das BC3-Format (entweder DXGI- \_ Format \_ BC3 \_ typlose, DXGI- \_ Format \_ BC3 \_ unorm oder DXGI \_ BC3 \_ unorm \_ sRGB), um hochgradig kohärente Farbdaten zu speichern (verwenden Sie [BC2](#bc2) mit weniger kohärenten Alpha Daten). Das Format BC3 speichert Farbdaten mit einer Farbe von 5:6:5 (5 Bits rot, 6 Bits grün, 5 Bits blau) und Alpha Daten mithilfe eines Bytes. Wenn eine 4 × 4-Textur mit dem größten möglichen Datenformat angenommen wird, reduziert dieses Komprimierungs Verfahren den von 64 bytes (16 Farben × 4 Komponenten/Farbe × 1 Byte/Komponente) benötigten Arbeitsspeicher auf 16 Bytes an Arbeitsspeicher.

Das Format BC3 speichert Farben mit der gleichen Anzahl von Bits und Datenlayout wie das [BC1](#bc1) -Format. für BC3 sind jedoch zusätzliche 64-Bits Arbeitsspeicher erforderlich, um die Alpha Daten zu speichern. Das BC3-Format verarbeitet Alpha durch die Speicherung zweier Verweis Werte und interpolieren zwischen Ihnen (ähnlich wie BC1 die RGB-Farbe speichert).

Der-Algorithmus funktioniert an 4 × 4 Texels-Blöcken. Anstatt 16 Alpha-Werte zu speichern, speichert der Algorithmus 2 Reference Premultiplied (Alpha \_ 0 und Alpha \_ 1) und 16 3-Bit-Farbindizes (Alpha a bis p), wie im folgenden Diagramm dargestellt.

![Diagramm des Layouts für die BC3-Komprimierung](images/d3d10-compression-bc3.png)

Das BC3-Format verwendet die Alpha Indizes (a – p), um die ursprünglichen Farben aus einer Nachschlage Tabelle zu suchen, die 8 Werte enthält. Die ersten beiden Werte – Alpha \_ 0 und Alpha \_ 1 – sind die Mindest-und Höchstwerte. die anderen sechs Zwischenwerte werden mithilfe von linearer Interpolationen berechnet.

Der Algorithmus bestimmt die Anzahl der interpoliert Alpha Werte durch Untersuchen der beiden Referenz-Alpha-Werte. Wenn Alpha \_ 0 größer als Alpha \_ 1 ist, interpoliert BC3 6 alpha Werte, andernfalls wird 4 interpoliert. Wenn BC3 nur 4 alpha-Werte interpoliert, werden zwei zusätzliche Alpha Werte festgelegt (0 für vollständig transparent und 255 für vollständig deckend). BC3 komprimiert die Alpha Werte im 4 × 4-texesbereich, indem der Bitcode gespeichert wird, der den interinterpolierten Alpha Werten entspricht, die am ehesten mit dem ursprünglichen Alpha für ein bestimmtes Texel übereinstimmen.


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

Verwenden Sie das BC4-Format, um Farbdaten mit einer Komponente in 8 Bits für jede Farbe zu speichern. Aufgrund der zunehmenden Genauigkeit (im Vergleich zu [BC1](#bc1)) ist BC4 ideal für das Speichern von Gleit Komma Daten im Bereich von \[ 0 bis 1 \] . dabei wird das DXGI \_ -Format \_ BC4 \_ unorm-Format und \[ -1 bis + 1 \] verwendet, wobei das DXGI- \_ Format \_ BC4 \_ snorm-Format verwendet wird. Wenn eine 4 × 4-Textur mit dem größten möglichen Datenformat angenommen wird, reduziert diese Komprimierungs Technik den benötigten Arbeitsspeicher von 16 Bytes (16 Farben × 1 Komponenten/Farbe × 1 Byte/Komponente) auf 8 Bytes.

Der-Algorithmus funktioniert an 4 × 4 Texels-Blöcken. Anstatt 16 Farben zu speichern, speichert der Algorithmus 2 Verweis Farben (rot \_ 0 und rot \_ 1) und 16 3-Bit-Farbindizes (rot a bis rot p), wie im folgenden Diagramm dargestellt.

![Diagramm des Layouts für die BC4-Komprimierung](images/d3d10-compression-bc4.png)

Der Algorithmus verwendet die 3-Bit-Indizes, um Farben aus einer Farbtabelle zu suchen, die 8 Farben enthält. Die ersten beiden Farben – rot \_ 0 und rot \_ 1 – sind die Mindest-und höchst Farben. Der Algorithmus berechnet die verbleibenden Farben mithilfe der linearen interpolung.

Der Algorithmus bestimmt die Anzahl der interpoliert Farbwerte durch Untersuchen der beiden Referenzwerte. Wenn rot \_ 0 größer als rot \_ 1 ist, interpoliert BC4 sechs Farbwerte, andernfalls wird 4 interpoliert. Wenn BC4 nur 4 Farbwerte interpoliert, werden zwei zusätzliche Farbwerte festgelegt (0,0 f für vollständig transparent und 1.0 f für vollständig nicht transparent). BC4 komprimiert die Alpha Werte im 4 × 4-texesbereich, indem der Bitcode gespeichert wird, der den interpoliert Alpha-Werten entspricht, die am ehesten mit dem ursprünglichen Alpha für eine bestimmte textexelle übereinstimmen.

-   [BC4 \_ unorm](/windows)
-   [BC4 \_ snorm](/windows)

### <a name="bc4_unorm"></a>BC4 \_ unorm

Die interpolung der Einzelkomponenten Daten erfolgt wie im folgenden Codebeispiel.


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



Den Verweis Farben werden 3-Bit-Indizes zugewiesen (000 – 111, da acht Werte vorhanden sind), die in Blöcken rot a bis rot p während der Komprimierung gespeichert werden.

### <a name="bc4_snorm"></a>BC4 \_ snorm

Das DXGI- \_ Format \_ BC4 \_ snorm ist exakt identisch, mit der Ausnahme, dass die Daten im snorm-Bereich codiert werden und wenn 4 Farbwerte interpoliert werden. Die interpolung der Einzelkomponenten Daten erfolgt wie im folgenden Codebeispiel.


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



Den Verweis Farben werden 3-Bit-Indizes zugewiesen (000 – 111, da acht Werte vorhanden sind), die in Blöcken rot a bis rot p während der Komprimierung gespeichert werden.

### <a name="bc5"></a>BC5

Verwenden Sie das BC5-Format, um Farbdaten mit zwei Komponenten zu speichern, wobei für jede Farbe 8 Bits verwendet werden. Aufgrund der zunehmenden Genauigkeit (im Vergleich zu [BC1](#bc1)) ist BC5 ideal für das Speichern von Gleit Komma Daten im Bereich von \[ 0 bis 1 \] . dabei wird das DXGI \_ -Format \_ BC5 \_ unorm-Format und \[ -1 bis + 1 \] verwendet, wobei das DXGI- \_ Format \_ BC5 \_ snorm-Format verwendet wird. Wenn eine 4 × 4-Textur mit dem größten möglichen Datenformat angenommen wird, reduziert diese Komprimierungs Technik den von 32 Bytes (16 Farben × 2 Komponenten/Farbe × 1 Byte/Komponente) benötigten Arbeitsspeicher auf 16 Bytes.

Der-Algorithmus funktioniert an 4 × 4 Texels-Blöcken. Anstatt für beide Komponenten 16 Farben zu speichern, speichert der Algorithmus zwei Verweis Farben für jede Komponente (rot \_ 0, rot \_ 1, grün \_ 0 und grün \_ 1) und 16 3-Bit-Farbindizes für jede Komponente (rot a bis rot und grün a durch grünes p), wie im folgenden Diagramm dargestellt.

![Diagramm des Layouts für die BC5-Komprimierung](images/d3d10-compression-bc5.png)

Der Algorithmus verwendet die 3-Bit-Indizes, um Farben aus einer Farbtabelle zu suchen, die 8 Farben enthält. Die ersten beiden Farben – rot \_ 0 und rot \_ 1 (oder grün \_ und grün \_ 1) – sind die Mindest-und höchst Farben. Der Algorithmus berechnet die verbleibenden Farben mithilfe der linearen interpolung.

Der Algorithmus bestimmt die Anzahl der interpoliert Farbwerte durch Untersuchen der beiden Referenzwerte. Wenn rot \_ 0 größer als rot \_ 1 ist, interpoliert BC5 sechs Farbwerte, andernfalls wird 4 interpoliert. Wenn BC5 nur 4 Farbwerte interpoliert, werden die verbleibenden beiden Farbwerte bei 0,0 f und 1.0 f festgelegt.

-   [BC5 \_ unorm](/windows)
-   [BC5 \_ snorm](/windows)

### <a name="bc5_unorm"></a>BC5 \_ unorm

Die interpolung der Einzelkomponenten Daten erfolgt wie im folgenden Codebeispiel. Die Berechnungen für die grünen Komponenten sind ähnlich.


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



Den Verweis Farben werden 3-Bit-Indizes zugewiesen (000 – 111, da acht Werte vorhanden sind), die in Blöcken rot a bis rot p während der Komprimierung gespeichert werden.

### <a name="bc5_snorm"></a>BC5 \_ snorm

Das DXGI- \_ Format \_ BC5 \_ snorm ist exakt identisch, mit der Ausnahme, dass die Daten im snorm-Bereich codiert werden und wenn 4 Datenwerte interpoliert werden, sind die beiden zusätzlichen Werte-1.0 f und 1.0 f. Die interpolung der Einzelkomponenten Daten erfolgt wie im folgenden Codebeispiel. Die Berechnungen für die grünen Komponenten sind ähnlich.


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



Den Verweis Farben werden 3-Bit-Indizes zugewiesen (000 – 111, da acht Werte vorhanden sind), die in Blöcken rot a bis rot p während der Komprimierung gespeichert werden.

## <a name="format-conversion-using-direct3d-101"></a>Format Konvertierung mit Direct3D 10,1

Direct3D 10,1 ermöglicht Kopien zwischen vorstrukturierten typisierten Texturen und Block komprimierten Texturen derselben Bitbreite. Die Funktionen, die dies erreichen können, sind [**copyresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) und [**copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).

Ab Direct3D 10,1 können Sie [**copyresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) und [**copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) zum Kopieren zwischen einigen Format Typen verwenden. Diese Art von Kopiervorgang führt einen Typ von Formatkonvertierung aus, bei dem Ressourcen Daten in einem anderen Formattyp neu interpretiert werden. Sehen Sie sich dieses Beispiel an, in dem der Unterschied zwischen dem erneuten interpretieren von Daten mit der Art und Weise dargestellt wird, in der sich die


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



Verwenden Sie [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy), um "f" als Typ von "u" neu zu interpretieren:


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



In der obigen Neuinterpretation ändert sich der zugrunde liegende Wert der Daten nicht. [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) interpretiert den float-Wert als ganze Zahl ohne Vorzeichen neu.

Verwenden Sie zum Ausführen der typischen Art der Konvertierung die Zuweisung:


```
    u = f; // ‘u’ becomes 1.
```



In der vorangehenden Konvertierung ändert sich der zugrunde liegende Wert der Daten.

In der folgenden Tabelle werden die zulässigen Quell-und Zielformate aufgelistet, die Sie in diesem neuinterpretertyp der Formatkonvertierung verwenden können. Sie müssen die Werte ordnungsgemäß codieren, damit die Neuinterpretation erwartungsgemäß funktioniert.



| Bitbreite | Nicht komprimierte Ressource                                                                                                                                               | Block-Compressed-Ressource                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 32        | DXGI- \_ Format \_ R32 \_ uint<br/> DXGI- \_ Format \_ R32 \_ Sint<br/>                                                                                               | DXGI- \_ Format \_ R9G9B9E5 \_ sharedexp                                                                                                                                   |
| 64        | DXGI- \_ Format \_ R16G16B16A16 \_ uint<br/> DXGI- \_ Format \_ R16G16B16A16 \_ Sint<br/> DXGI- \_ Format \_ R32G32 \_ uint<br/> DXGI- \_ Format \_ R32G32 \_ Sint<br/> | DXGI- \_ Format \_ BC1 \_ unorm \[ \_ sRGB\]<br/> DXGI- \_ Format \_ BC4 \_ unorm<br/> DXGI- \_ Format \_ BC4 \_ snorm<br/>                                               |
| 128       | DXGI- \_ Format \_ R32G32B32A32 \_ uint<br/> DXGI- \_ Format \_ R32G32B32A32 \_ Sint<br/>                                                                             | DXGI- \_ Format \_ BC2 \_ unorm \[ \_ sRGB\]<br/> DXGI- \_ Format \_ BC3 \_ unorm \[ \_ sRGB\]<br/> DXGI- \_ Format \_ BC5 \_ unorm<br/> DXGI- \_ Format \_ BC5 \_ snorm<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
