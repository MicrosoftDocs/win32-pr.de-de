---
title: Grundlegende VML-Typen
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Migrieren Sie Webseiten und Anwendungen, die auf VML basieren, auf SVG oder andere allgemein unterstützte Standards.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Vector Markup Language (VML), Basis Typen
- VML (Vector Markup Language), grundlegende Typen
- Vektorgrafiken, grundlegende VML-Typen
- Vector Markup Language (VML), Typen
- VML (Vector Markup Language), Typen
- Vektorgrafiken, VML-Typen
- grundlegende VML-Typen
- boolescher Typ
- Bruchtyp
- ordinentyp
- length-Typ
- Messtyp
- Angle-Typ
- Farbtyp
- Schrifttyp
- Bitmaptyp
- Vektortyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f05b058c919496b608b875f96e6c03bbeb0d50e8
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104557494"
---
# <a name="basic-vml-types"></a>Grundlegende VML-Typen

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

**Contents**

-   [Introduction (Einführung)](#introduction)
-   [boolean](#boolean)
-   [fraction](#fraction)
-   [g](#ordinate)
-   [length](#length)
    -   [Alternative Darstellungen](#alternative-representations)
-   [gemessen](#measure)
    -   [Alternative Darstellungen](#alternative-representations)
-   [angle](#angle)
    -   [Alternative Darstellungen](#alternative-representations)
-   [color](#color)
    -   [Farbeinheiten](#color-units)
    -   [HTML-Farben](#html-colors)
    -   [Schema Farben](#scheme-colors)
    -   [System Farben](#system-colors)
    -   [Reine Farben](#pure-colors)
    -   [Farbanpassungen](#color-adjustments)
-   [Raster](#font)
-   [Bitmap](#bitmap)
    -   [Bild Dateiformate](#picture-file-formats)
-   [ve](#vector)

## <a name="introduction"></a>Einführung

In diesem Vorschlag wird eine kleine Anzahl grundlegender Typen verwendet, die in der folgenden Tabelle aufgeführt sind.



| type                  | Element           | Grundlegende Darstellung | BESCHREIBUNG                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [boolean](#boolean)   |                   | 1 Bit                      | Ein boolescher Wert: true oder false.                                                                      |
| [fraction](#fraction) |                   | Nummer 2 6                 | Ein numerischer Wert, der um 2 6 (65536) skaliert und als ganze Zahl mit Vorzeichen gespeichert wird.                               |
| [g](#ordinate) |                   | 30-Bit-Ganzzahl Plus Vorzeichen   | Teil einer Koordinate (z. b. in einem Pfad), die durch den Koord definierten Werte.                                |
| [length](#length)     |                   | [Emu](#length)             | Eine physische Länge, z. b. die Breite einer Zeile oder die Größe einer Schriftart.                                |
| [gemessen](#measure)   |                   | EWU oder Nummer 2 6          | Entweder eine physische Länge, einschließlich einer Anzahl von Geräte Pixeln, oder ein Bruchteil einer anderen Menge. |
| [angle](#angle)       |                   | Grad 2 6                | Ein Winkel. positiv ist der Uhrzeigersinn.                                                                     |
| [color](#color)       | [c](#color)       | complex                    | Ein Element, mit dem eine Farbe abgeleitet werden kann.                                                        |
| [Raster](#font)         | [Raster](#font)     | complex                    | Eine Beschreibung einer Schriftart.                                                                             |
| [Bitmap](#bitmap)     | [Bitmap](#bitmap) | href                       | Ein Verweis auf eine externe Bilddatei.                                                             |
| [ve](#vector)     | [Ramelow](#vector)      | complex                    | Eine Beschreibung eines Vektor Pfads.                                                                       |



 

Die "grundlegende Darstellung" ist die höchste Genauigkeits Darstellung, die für den Vorschlag eine konforme Implementierung erfordert. Daten gehen verloren, wenn die-Implementierung nicht in der Lage ist, die Daten für die erforderliche Genauigkeit darzustellen. Die Farb-, Schriftart-und Vektor Typen entsprechen Elementen, die selbst über eine Struktur verfügen. in gewisser Hinsicht sind Sie keine grundlegenden Typen. Es ist jedoch praktisch, Sie in diesem Vorschlag als solche zu behandeln.

Jedem nicht komplexen Basistyp ist ein Element mit demselben Namen zugeordnet. Diese Elementnamen sind reserviert und können nicht für andere Zwecke innerhalb von Erweiterungen verwendet werden, auch wenn die Verwendung in einem onview = "Skip"-Erweiterungs Element erfolgt. Aus diesem Grund ist es möglich, dass eine Implementierung, bei der Unbekannter XML-Code gefunden wird, eine effiziente interne Speicherung des unbekannten XML-Codes ermöglicht, solange die Werte in die "Type"-Elemente eingeschlossen werden.


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



Im ersten vorangehenden Beispiel muss die Zeichenfolge "1,578" als Sequenz von Zeichen gespeichert werden (die-Implementierung weiß nicht, ob es sich um eine Zeichenfolge oder eine Zahl handelt); im zweiten Beispiel gibt das Bruch Element an, dass der Inhalt eine Zahl ist, sodass es in die Bruchteil-Darstellung mit hoher Genauigkeit konvertiert werden kann.

Komplexe Typen (einschließlich Bitmap) weisen verknüpfte Elementnamen auf, die zum Begrenzen des Werts verwendet werden. Dies vereinfacht die-Verarbeitung, indem sichergestellt wird, dass die komplexeren-Element Tags mit eindeutigen Element Tags verknüpft sind.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="boolean"></a>boolean


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



Ein boolescher Wert wird als Schlüsselwort dargestellt, das den Zustand des Flags angibt. Die folgenden Schlüsselwörter sind definiert.



| Wert für true | Wert für false |
|----------------|-----------------|
| true           | false           |
| ja            | nein              |
| on             | aus             |
| t              | f               |
| 1              | 0               |



 

Eine-Implementierung kann einen beliebigen Wert schreiben und alle Werte erkennen. Eine-Implementierung ist kostenlos, um Werte von einer Darstellung in eine andere zu ändern.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="fraction"></a>fraction


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



Alle numerischen Werte (d. h. Werte der dimensionlosen Mengen) in diesem Vorschlag können als ganze Zahlen gespeichert werden, indem Sie um 2 6 (65536) skaliert werden. Eine Zahl kann entweder in diesem Formular mit dem Suffix f oder als Dezimalzahl ohne Suffix angegeben werden. Folglich stellen die folgenden hypothetischen Elemente denselben Wert dar.


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



Eine Menge mit dem f-Suffix muss eine ganze Zahl sein. Bruchzahlen sind nicht zulässig. Die resultierende Ganzzahl muss als Komplement-signierte Zahl von 32 Bit 2 dargestellt werden. Folglich ist der Gültigkeitsbereich der Darstellung 32768 (tatsächlich kleiner als 32768 und größer oder gleich-32768).

Eine konforme Implementierung ist erforderlich, um Werte beizubehalten, die als f-Werte ausgedrückt werden. Werte, die als Dezimalzahlen dargestellt werden, können in einen f-Wert konvertiert und auf diese Weise gespeichert werden. Eine Anwendung ist berechtigt, intern generierte Werte in einer beliebigen entsprechenden Einheit aufzuzeichnen. ein Wert, der aus einem vorhandenen Dokument gelesen wird, muss jedoch entweder in der vollständigen ursprünglichen Genauigkeit beibehalten werden oder in einen f-Wert konvertiert werden.

Wenn die Implementierung dies nicht tun kann, muss Sie den Benutzer warnen, dass Daten verloren gehen. (Es ist zulässig, eine solche Warnung einmalig auszugeben, wenn extern generierte Daten zum ersten Mal gefunden werden.)

Wenn ein Dezimalwert in das f-Format konvertiert wird, kann die Implementierung einen beliebigen arithmetischen Rundungs Modus verwenden. Allerdings muss eine ganze Zahl genau in das f-Format konvertiert werden. Es wird empfohlen, dass Implementierungen durch Runden auf minus unendlich konvertiert werden und dass die konvertion immer exakt ist.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="ordinate"></a>g


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



Die Einheiten des Koordinatensystems, das durch den Koord festgelegt wird, haben einen nominalen Typ, der als "Ordini" bezeichnet wird. Dies ist ein Measure der Länge, wird jedoch nur in Bezug auf das Rechteck verwendet, das von coord festgelegt wird. Jeder Wert des Typs "Ordinalwert" wird durch die Werte " *w* " und " *h* " des Koord und das resultierende Verhältnis skaliert, das verwendet wird, um eine tatsächliche Messung auf dem Ausgabegerät herzustellen.

Eine konforme Implementierung muss in der Lage sein, Ordinalwerte von bis zu 30 Bits Pluszeichen (d. h. eine 31-Bit-Ganzzahl mit Vorzeichen, keine 32-Bit-Ganzzahl mit Vorzeichen) zu verarbeiten. Es wird jedoch empfohlen, dass Implementierungen versuchen, Koordinaten für path-und ähnliche Elemente zu entwickeln, die ungefähr 16 Bits Genauigkeit aufweisen. Dadurch wird die Wahrscheinlichkeit eines Unterlaufs oder eines Überlaufs in einer nicht konformen Implementierung minimiert.

Ordinalwerte sind immer ganzzahlige Werte. Ein Dezimaltrennzeichen darf nicht in einem Wert vom Typ "ordinalpunkt" vorkommen. An Werte vom Typ "Ordini" können keine Einheits spezifiatoren angehängt werden.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="length"></a>length


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



Eine Länge ist eine reale Messung oder manchmal eine Messung in Geräte Pixeln. Es wird empfohlen, dass-Implementierungen die Verwendung von Geräte Pixeln (px) vermeiden.

Alle Standard Qualifizierer für [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) -Einheiten sind für eine Länge zulässig. Außerdem kann die Qualifizierer-Emu verwendet werden. Dieser Qualifizierer bezieht sich auf eine Einheit, d. h. auf die EWU (englische Metrik Unit). Hierbei handelt es sich um einen gemeinsamen Nenner der Mess Mengen in den Computergrafiken. Der EMU ist <sup>Zoll</sup> /914400, d. h., es gibt 914400 Emu pro Zoll. In der folgenden Tabelle ist die Anzahl der Emus in einer kleinen Anzahl von häufig auftretenden Einheiten aufgeführt.



| Anzahl von Emus | Anzahl pro Zoll | Anzahl pro Millimeter | BESCHREIBUNG             |
|----------------|-----------------|-----------------------|-------------------------|
| 360            |                 | 0,01                  | Win32-HIMETRIC          |
| 12700          | 72              |                       | Punkt                 |
| 635            | 1440            |                       | Win32-Twip              |
| 762            | 1200            |                       | Drucker mit hoher Auflösung |



 

Bruchzahlen von Emus sind nicht zulässig. Jede Messung muss als eine ganzzahlige 32-Bit-Zahl von Emus dargestellt werden. Dadurch wird die Größe eines Mess Werts auf 2348 Zoll--ungefähr 59 Meter oder 65 Meter beschränkt. Da die Messungen immer auf die Größe eines Renderings auf einem nominell Bildschirm-oder Seitengröße-Ausgabegerät verweisen, liegen Sie immer innerhalb dieses Bereichs.

Beachten Sie jedoch, dass die Darstellung für reale Messungen ungeeignet ist und dass Sie aufgezeichnet werden (z. b. zum Aufzeichnen der realen Größe eines Pfades), dass eine andere Darstellung verwendet werden muss.

Eine konforme Implementierung ist erforderlich, um Werte beizubehalten, die genaue Anzahl von Emus sind. Werte, die auf andere Weise dargestellt werden, können in einen Emu-Wert konvertiert und auf diese Weise gespeichert werden. Eine Anwendung ist berechtigt, intern generierte Werte in einer beliebigen entsprechenden Einheit aufzuzeichnen. ein Wert, der aus einem vorhandenen Dokument gelesen wird, muss jedoch entweder in der vollständigen ursprünglichen Genauigkeit beibehalten werden oder in einen Emu-Wert konvertiert werden.

Wenn die Implementierung dies nicht tun kann, muss Sie den Benutzer warnen, dass Daten verloren gehen. (Es ist zulässig, eine solche Warnung einmalig auszugeben, wenn extern generierte Daten zum ersten Mal gefunden werden.)

In der Praxis werden für relativ wenige Messungen in diesem Vorschlag physische Längen verwendet. Bei den Daten, die normalerweise am wichtigsten sind, handelt es sich um die Pfaddaten, die in dem Koordinatensystem codiert sind, das auf der Grundlage der Form von coord definiert ist.

### <a name="alternative-representations"></a>Alternative Darstellungen

Die Standardlängen Darstellungen von HTML werden durch [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) definiert. Relative Einheiten, mit Ausnahme des Pixels, sind in dem Kontext, in dem Längen in diesem Vorschlag verwendet werden, nicht aussagekräftig und dürfen nicht verwendet werden. Wenn das Dokument die beabsichtigte (Ziel-) Pixelgröße aufzeichnet, wird die Übersetzung von Pixel in EMU definiert. Andernfalls sollte der von [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) definierte Standardwert 90 dpi verwendet werden.

Mit Ausnahme von "EMU" kann jeder Wert als Dezimal Bruch angegeben werden. Wenn ein Dezimalwert in den Emu-Wert konvertiert wird, kann die Implementierung einen beliebigen arithmetischen Rundungs Modus verwenden. (Die einzige Möglichkeit für eine Erstellungs Anwendung, ein bestimmtes Ergebnis zu gewährleisten, besteht darin, Sie in der EWU anzugeben.)

Wenn kein Einheits Spezifizierer in einem Längen Wert angegeben wird, muss die Implementierung die EWU annehmen.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="measure"></a>Kennzahl


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



Ein Measure ist eine Menge, die entweder eine [Länge](#length) oder ein [Bruchteil](#fraction)aufweisen kann. Dies ähnelt den HTML-und CSS-Längenmessungen, bei denen es sich in vielen Fällen entweder um physische Messungen oder Prozentsätze einer anderen Menge handeln kann. Wenn kein Einheits Spezifizierer angegeben wird, muss der Wert als Dezimal Bruch angenommen werden (daher wird dieses Verhalten vom Bruchteil geerbt, nicht von der Länge).

Anders als bei der Länge hat ein Pixelwert eine Kontext definierte Bedeutung, sodass die Konvertierung in die EWU normalerweise ungeeignet ist. Es gibt drei mögliche grundlegende Darstellungen, die die Implementierung beibehalten muss (d. h., eine Darstellung kann ohne Informationsverlust nicht in eine andere konvertiert werden).

1.  Ein Bruchteil muss im [Bruchteil](#fraction) -Format (einem "f"-Wert) beibehalten werden.
2.  Eine physische Länge sollte in der EWU beibehalten werden.
3.  Ein Pixelwert sollte als ganze Anzahl von Pixeln beibehalten werden.

Bruchzahlen von Pixeln sind nicht zulässig.

### <a name="alternative-representations"></a>Alternative Darstellungen

Alle alternativen Darstellungen von [Bruchteil](#fraction) und [Länge](#length) sind zulässig.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="angle"></a>angle


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



Die grundlegende Darstellung eines Winkels ist eine Anzahl von Grad, der um 2 6 (65536) multiheftet und als ganze Zahl gespeichert wird. Da der Koordinatenraum invertiert wird (positive y-Achse ist nicht mehr), ist ein Winkel im Uhrzeigersinn positiv. Eine konforme Implementierung ist erforderlich, um die vollständige Genauigkeit eines solchen Werts beizubehalten.

Eine Implementierung darf einen beliebigen Bereich für Winkel verwenden und einen Winkel normalisieren (z. b. auf-180 bis + 180 oder 0 bis 360). Implementierungen müssen nicht konsistent sein. die ganzzahlige Darstellung eines Winkels darf den Bereich einer 32-Bit-Ganzzahl mit Vorzeichen jedoch nicht überschreiten.

Das Suffix FD wird verwendet, um diese Darstellung eines Winkels (Bruch Komma) zu identifizieren. Beachten Sie, dass dies vom f-Suffix für einen dimensionlosen Bruchteil unterschieden wird, obwohl identische Arithmetik zur Unterstützung verwendet werden kann. Der Standardwert für einen Angular-Wert ist einfache Grad, d. h. ein nicht skalierter Wert. Dies kann auch mit dem Suffix "" (dem Grad Symbol) signalisiert werden. Diese Verwendung hängt jedoch davon ab, dass eine geeignete Dokument Codierung vorhanden ist. Folglich wird das Suffix "deg" auch als Mittelwert definiert. Der vollständige Satz möglicher mögliche genügt ist wie folgt.



| Suffix       | Konvertierungsfaktor | Kommentare                               |
|--------------|-------------------|----------------------------------------|
| FD           | 1                 | Interne Darstellung mit hoher Genauigkeit |
| keine, DEG,   | 65536             | Grad                                |
| rad          | 65536pi/180       | Radians                                |



 

### <a name="alternative-representations"></a>Alternative Darstellungen

Die Skalierungs Transformation weist Diskontinuitäten bei ungeraden Vielfachen von 45 auf. Daher ist es äußerst wichtig für die Konvertierung von ungenauer Menge, um genau definiert zu werden. Aus diesem Grund wird die Arithmetik der Konvertierung für die Rundung auf minus unendlich definiert.

Da dies in einigen Implementierungen schwierig oder unmöglich sein kann, ist die Verwendung des folgenden als ein Feature der Ebene 3 definiert:

1.  Ein beliebiger Grad Wert.
2.  Beliebiger Bogenmaß Wert-Wert

Folglich werden Werte mit den qualifizierten FD-Werten, nicht qualifizierten ganzzahligen Werten oder ganzzahligen Werten, die für die deg qualifiziert sind oder genau durch eine konforme Implementierung der Ebene andere Werte sind nicht erforderlich. Es wird dringend empfohlen, dass jede Implementierung die Konvertierung von einem Bruchteil eines Bruch Werts in einen skalierten (FD-) Grad Wert genau verarbeitet. Dies kann ohne Gleit Komma Unterstützung erfolgen.

Die anspruchsvolleren Anforderungen für die Konvertierung unterscheiden FD von f.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="color"></a>color


```HTML
c
<!element c  %color;>
```



Farben sind ein wesentlicher Bestandteil moderner Computergrafiken. Der Vorschlag verwendet die etablierten Methoden zum Angeben fester Farben. Farben in Diagrammen sind jedoch selten einfache statische Farben. Sie werden oft von anderen Elementen im Diagramm abgeleitet. Viele dieser Informationen sind anwendungsspezifisch, sodass dieser Vorschlag zwei grundlegende Mechanismen zur Angabe eines solchen Verhaltens bietet:

1.  Eine Farbe kann aus einer anderen Farbe in derselben Form abgeleitet werden.
2.  Eine kleine Anzahl von arithmetischen Vorgängen wird für das ableiten oder Ändern einer Farbe definiert.

Der Prototype-Shape-Mechanismus ergänzt dies, indem es das Definieren von Prototypen ermöglicht, von welchen Farben geerbt werden können.


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



Ein Farbwert ist eine supermenge der [CSS1-Farbdefinition](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) . Mithilfe der Erweiterungen kann der RGB-Farbwert aus anderen Farben innerhalb der Form oder aus einem mit CSS1 definierten Gesamt Farbschema ermittelt werden.

Wenn der Wert eines Elements als Farbe definiert ist, definiert der *Inhalt* eines Elements den Farbwert mithilfe eines einzelnen farbtokens, das optional durch eine arithmetische Operation in der entsprechenden RGB-Farbe geändert wird.

[![zurück ](images/top.gif) zum Anfang](#top)

### <a name="color-units"></a>Farbeinheiten

Der vollständige Satz von farbtoken stammt aus einer Vielzahl von Quellen: HTML, CSS1 und diesem Vorschlag. Sie werden wie folgt definiert, indem Notation aus [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) oder die für XML-Verknüpfungen definierte XPointer-Notation verwendet wird.

In den XPointer-Definitionen ist die Speicherort Quelle das Element, das den Farbwert enthält, und der Ausdruck verweist auf den gesamten Element Satz der Form, so als ob alle Base Prototype-Elemente mit der Form zusammengeführt worden wären. Wenn das entsprechende Element nicht vorhanden ist, wird an seiner Stelle der Standardwert für dieses Element verwendet.



| Color            | Definition                                                                                                  | Ebene | BESCHREIBUNG                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name             | Siehe unten                                                                                                   | 0     | HTML-Farbname, wie in der folgenden Tabelle aufgeführt.                                                                                                                            |
| \#rr' gg' g '      | \#rr' gg' g '                                                                                                 | 0     | Standard mäßige CSS1/sRGB-Farbdarstellung mit Werten im Bereich 0.. 255, die mit zwei hexadezimal Ziffern dargestellt werden.                                                     |
| \#Set            | \#RRGGBB                                                                                                    | 1     | Verkürztes CSS1-Formular mit nur drei hexadezimalen Ziffern.                                                                                                                   |
| RGB (r, g, b)       | \#r selbst b                                                                                                 | 1     | CSS1 RGB-Formular; die Elemente des RGB-Werts werden entsprechend der Definition in [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) konvertiert.                                      |
| fill             | Vorgänger (1, Form)<br/> Child (1, Fill)<br/> Child (1, Farbe)<br/>                           | 1     | Die Vorder grundfüllfarbe der Form.                                                                                                                                   |
| fillback         | Vorgänger (1, Form)<br/> Child (1, Fill)<br/> Child (1, zurück)<br/> Child (1, Farbe)<br/> | 1     | Die Hintergrundfarbe der Form Füllung.                                                                                                                                   |
| line             | Vorgänger (1, Form)<br/> Child (1, Zeile)<br/> Child (1, Farbe)<br/>                           | 1     | Die Vorder Grundlinien Farbe der Form.                                                                                                                                   |
| Lineback         | Vorgänger (1, Form)<br/> Child (1, Zeile)<br/> Child (1, zurück) <br/> Child (1, Farbe)<br/> | 1     | Die Hintergrund Linien Farbe der Form.                                                                                                                                   |
| lineorfill       | Zeile, ausfüllen                                                                                                  | 1     | Der Zeilen Wert, wenn kein Standardwert ist, andernfalls der Füllwert. Dadurch wird die Farbe an der Kante der Form zurückgegeben.                                           |
| fillthenline     | ausfüllen, Zeile                                                                                                  | 1     | Der Füllwert, wenn nicht der Standardwert, andernfalls der Zeilen Wert. Dadurch wird die Haupt Form Farbe zurückgegeben (wenn die Form nicht aufgefüllt ist, ist das Ergebnis die Linien Farbe).   |
| shadow           | Vorgänger (1, Form)<br/> Child (1, Shadow)<br/> Child (1, Farbe)<br/>                         | 2     | Die Farbe des Schattens (Hierbei handelt es sich um eine Funktion auf Ebene 2).                                                                                                                      |
| scheme           | Siehe unten                                                                                                   | 1     | Eine Schema Farbe aus dem Schema, das für das Dokument definiert ist. siehe unten.                                                                                                       |
| Schema (*Index*)  | Siehe unten                                                                                                   | 1     | Schema Farb *Index*, beginnend bei 0; siehe unten.                                                                                                                         |
| this             | Impliziert                                                                                                     | 2     | Der Vorgang (Ausfüllen eines Pfads oder zeichnen) wird auf andere Weise definiert (z. b. als Bitmap), und die Farbe gibt eine "Änderung" für die Farben an, die so impliziert sind. |
| Palette (*Index*) | Impliziert                                                                                                     | 3     | Verhält sich auf dieselbe Weise wie diese, mit der Ausnahme, dass genau ein Eintrag in einer Bitmap-Farbtabelle identifiziert wird. Nur zulässig, wenn explizit angegeben ist.                             |
| none             | \-                                                                                                          | 2     | Gibt an, dass keine Farbe vorhanden ist. kann verwendet werden, um einen Zeichnungs Vorgang abzubrechen, der die Farbe verwendet.                                                                          |
| System           | Siehe unten                                                                                                   | 3     | Eine von der Systembenutzer Oberfläche definierte Farbe.                                                                                                                             |



 

Mit dieser Farbe kann ein Farbwert eine Änderung an einer Farbe angeben, die auf andere Weise abgeleitet ist. insbesondere kann ein einzelner Vorgang für alle Farben in einer Bitmap angegeben werden. Die Farbe der Palette (*Index*) identifiziert einen bestimmten Eintrag in einer Palette zugeordneten Bitmap. Die Verwendung dieser wird nur zum Aufzeichnen eines Farbtabellen Eintrags definiert, der in einer solchen Bitmap als transparent angesehen werden sollte.

Die Definition eines Farbwerts darf weder direkt noch indirekt auf sich selbst verweisen. Wenn eine solche Definition fest steht, wird empfohlen, aber nicht erforderlich, dass die Implementierung den nicht definierten Wert als schwarz behandelt.

[![zurück ](images/top.gif) zum Anfang](#top)

### <a name="html-colors"></a>HTML-Farben

[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) definiert die folgenden 16 Farbnamen:



Farbnamen und sRGB-Werte

![Beispiel für schwarze Farbe.](images/black.gif)

Schwarz = " \# 000000"

![Beispiel für grüne Farbe.](images/green.gif)

Grün = " \# 008000"

![Beispiel für Silver-Farbe.](images/silver.gif)

Silver = " \# C0C0C0"

![Beispiel für eine Kalk Farbe.](images/lime.gif)

Kalk = " \# 00FF00"

![Beispiel für graue Farbe.](images/gray.gif)

Grau = " \# 808080"

![Beispiel für eine Oliven Farbe.](images/olive.gif)

Olive = " \# 808000"

![Beispiel für weiß Farbe.](images/white.gif)

Weiß = " \# FFFFFF"

![Beispiel für ywllow Color.](images/yellow.gif)

Gelb = " \# FFFF00"

![Beispiel für eine kastanienbraun-Farbe.](images/maroon.gif)

Maroon = " \# 800000"

![Beispiel für die Farbe der Marine.](images/navy.gif)

Navy = " \# 000080"

![Beispiel für rote Farbe.](images/red.gif)

Rot = " \# FF0000"

![Beispiel für blaue Farbe.](images/blue.gif)

Blue = " \# 0000FF"

![Beispiel für lila Farbe.](images/purple.gif)

Lila = " \# 800080"

![Beispiel für eine blaugrün-Farbe.](images/teal.gif)

Teal = " \# 008080"

![Beispiel für die Fuchsia-Farbe.](images/fuchsia.gif)

Fuchsia = " \# FF00FF"

![Beispiel für eine Aqua-Farbe.](images/aqua.gif)

Aqua = " \# 00ffff"



 

[![zurück ](images/top.gif) zum Anfang](#top)

### <a name="scheme-colors"></a>Schema Farben

Die Schema Farben, auf die durch das Schema verwiesen wird, werden auf Dokument Ebene mithilfe des Meta-Tags mit dem Namensattribut "Design Color Scheme" definiert.


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



Dieses Tag ermöglicht das Definieren von bis zu acht Schema Farben. Nicht definierte Farben sollten standardmäßig auf Schwarz eingestellt werden. Die Schema Farben ermöglichen das Ändern des Farbschemas, das für ein ganzes Dokument verwendet wird, indem Sie den Inhalt des Design Farbschemas ändern. Um sicherzustellen, dass die aus anderen Erstellungs Anwendungen importierten Grafiken eine konsistente Verwendung der Schema Farben machen, werden die folgenden Interpretationen definiert. Die "Verwendung" ist eine kurze Beschreibung des Zwecks, und in der Spalte "Beschreibung" finden Sie weitere Details.



| Index | Name              | Verwendung                         | BESCHREIBUNG                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| 0     | Schema. Hintergrund | Hintergrund                    | Die Farbe, die für den Hintergrund einer Grafik verwendet wird (und häufig für die gesamte Seite).                                    |
| 1     | Schema. Text       | Text und Zeilen                | Die Farbe für Text, der an eine Form und die Standardlinien Farbe angefügt ist.                                                      |
| 2     | Schema. Shadow     | Shadows                       | Standard Schatten Farbe: die Farbe, die normalerweise für Form Schatten verwendet wird.                                                     |
| 3     | Schema. Title      | Titeltext                    | Die Farbe, die für Überschriften-oder Titeltext verwendet werden soll.                                                                              |
| 4     | Schema. Fill       | Füllt                         | Standard Füllfarbe: die Farbe, die normalerweise zum Auffüllen von Formen verwendet wird.                                                          |
| 5     | Schema. Akzent     | Betont                        | Normale Hervorhebungs Farbe, die verwendet wird, um ein wichtiges Element einer Grafik hervorzuheben.                                             |
| 6     | Schema. Hyperlink  | Akzent und Hyperlink          | Hervorhebungs Farbe für Hyperlinks. Kann für andere Zwecke verwendet werden, in denen die Farbe einen Link zu anderen Informationen bezeichnet. |
| 7     | Schema. gefolgt   | Link zu Akzent und gefolgt | Hervorhebungs Farbe für verfolgte Hyperlinks; auch für "rückwärts"-Links geeignet.                                         |



 

Auf eine Schema Farbe kann entweder anhand des Namens oder des Indexes verwiesen werden. Daher weisen "Schema. Fill" und "Schema (4)" dieselbe Farbe auf.

Schema Farben werden nicht am Standardschema beteiligt, wenn keine Farbe angegeben ist. Eine nicht angegebene Füll Farbe muss immer als weiß interpretiert werden, unabhängig von der Farbe der Schema Farbe 4. Die "Akzent"-Farben sollten sowohl mit dem Hintergrund (0) als auch mit den Füll Farben (4) im Gegensatz zu Text-und Titel Textfarben die gleiche Eigenschaft aufweisen. Ein Standardverfahren besteht darin, die Akzente zu färben und den Standardtext (in der Regel Schwarz oder weiß) zu färben.

[![zurück ](images/top.gif) zum Anfang](#top)

### <a name="system-colors"></a>System Farben

Anwendungen zeichnen manchmal Farben auf der Grundlage von Betriebs Systemeinstellungen innerhalb von Grafiken auf. Diese sind normalerweise flüchtig und müssen nicht ausgeschrieben werden. die thesystemcolor-Definitionen sind nur zur Unterstützung dieser Funktion vorhanden. Eine System Farbe wird eingeführt, indem ein entsprechendes Tag in einem neuen Namespace definiert und die entsprechenden Informationen in den Element Inhalt eingefügt werden.

Dieser Vorschlag definiert ein derartiges Tag, um die Windows-Benutzeroberflächen Farben zu codieren, die in der Header Datei "Winuser. h" definiert sind.


```HTML
win.color
<!element win.color #pcdata>
```



Der Inhalt des-Elements ist eine einzelne ganze Zahl, die den Wert der relevanten Farb \_ Definition aus Winuser. h enthält. Eine ähnliche Technik kann für jede System-oder anwendungsspezifische Farbspezifikation übernommen werden. Es wird dringend empfohlen, dieses Feature nur aus Gründen der Abwärtskompatibilität zu verwenden.

[![zurück ](images/top.gif) zum Anfang](#top)

### <a name="pure-colors"></a>Reine Farben


```HTML
pure
<!elementpure empty>
```



Wenn das Element <pure/> in einem Farbwert angezeigt wird, ist dies ein Hinweis darauf, dass die Farbe nicht durch ein Dithering-Muster angeblendet werden sollte. Dies ist eine Funktion der Ebene 1, und eine konforme Implementierung muss Sie nicht berücksichtigen. Die Bezeichnung ist wichtig für Grafiken, die auf Geräten mit mittlerer Auflösung angezeigt werden, wie z. b. Video anzeigen, bei denen kleine Features (z. b. Zeilen) ein ungültiges Aliasing mit Dithering-Farben verursachen können Auf Geräten wie Druckern, die normalerweise alle Farben außer den wenigen vollständig übersättigten Farben unterscheiden, ist das Dithering normalerweise ausreichend gut, um dieses Problem zu vermeiden.

[![zurück ](images/top.gif) zum Anfang](#top)

### <a name="color-adjustments"></a>Farbanpassungen

Die Basis Farbe kann durch arithmetische Operationen für den RGB-Wert angepasst werden. Diese Vorgänge werden mithilfe zusätzlicher Elemente innerhalb des Farbwerts definiert. Solche Anpassungen sind nur hilfreich, wenn Sie auf von anderen Elementen abgeleitete Farben angewendet werden. Es ist zulässig, eine solche Anpassung für einen Wert mit fester Farbe anzugeben. Allerdings ist es für eine Implementierung zulässig, dies auf den entsprechenden RGB-Wert zu reduzieren und anstelle des Originals zu speichern.

Alle in diesem Abschnitt beschriebenen Farb Anpassungs Features sind Features der Ebene 1.


```HTML
color.adjustment
<!entity % color.adjustment  -- change to make to a color --
  "( %color.op; )?, ( %color.adj; )*"
>

color.op
<!entity % color.op          -- arithmetic operation --
  "( darken | lighten | add | subtract | reverseSubtract |
  blackWhite )"
>
<!element   darken           %color.parameter;>
<!element   lighten          %color.parameter;>
<!element   add              %color.parameter;>
<!element   subtract         %color.parameter;>
<!element   reversesubtract  %color.parameter;>
<!element   blackwhite       %color.parameter;>

color.parameter
<!entity % color.parameter  "#pcdata" >

color.adj
<!entity % color.adj          -- additional adjustment to color --
  "invert | invert128 | gray"
>
<!element   invert       empty>
<!element   INVERT128    empty>
<!element   gray         empty>
```



Der-Parameter der ersten sechs Vorgänge ist ein einzelner ganzzahliger numerischer Wert im Bereich von 0 bis 255. Die Anpassung wird wie folgt für den 3x8bit-RGB-Wert durchgeführt:

1.  Wenn <gray/> angegeben wird, wird der RGB-Wert durch yyy ersetzt, wobei y der Wert für die Leuchtkraft (y) ist, der aus dem sRGB-Wert in folgendem Wert von "ITU-r BT. 709" berechnet wird. Diese Berechnung lautet:
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  Wenn eine Color. op-Änderung angegeben wird, wird jede Komponente entsprechend der nachfolgenden Tabelle separat angepasst. c ist der Komponenten Wert, und p ist der Color. Parameter-Wert.

    | Vorgang       | Formel                            |
    |-----------------|------------------------------------|
    | Abdunkeln          | c: = CXP/255                       |
    | aufgehellt         | c: = 255-(255-c) XP/255           |
    | add             | c: = c + p                         |
    | Subtrahieren        | c: = c-p                         |
    | reversesubtract | c: = p-c                         |
    | BlackWhite      | Wenn c < p thenc: = 0elsec: = 255 |

    

     

    In jedem Fall, wenn der berechnete Komponenten Wert c den Wert 255 überschreitet, wird 255 verwendet, und wenn der Wert kleiner als 0 ist, wird 0 verwendet.

3.  Wenn <INVERT128/> angegeben wird, wird der Wert 128 subtrahiert oder jeder Komponente hinzugefügt, je nachdem, ob die Komponente kleiner als 128 ist oder nicht.
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  Wenn <invert/> angegeben wird, wird jede Komponente durch 255 abzüglich des Werts der Komponente ersetzt.
    ```HTML
    c := 255-c
    ```

    

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="font"></a>font


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



Eine Schriftart wird mithilfe eines style-Attributs identifiziert, wie in [CSS1 section 5,2 (Schriftart Eigenschaften)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) definiert. Der Text des Schriftart Elements ist derzeit nicht definiert, kann aber in Zukunft verwendet werden, um Standard Schriftart Informationen zu codieren. Anfängliche Implementierungen dieses Vorschlags sollten die Informationen beibehalten, aber nicht interpretieren.

Es ist zu beachten, dass in der Zukunft Unterstützung für Out-of-Line-Schriftart Informationen (herunterladbare Schriftarten oder freigegebene Schriftart Ressourcen) hinzugefügt wird. Dies erfolgt durch ein XML-Link-Element innerhalb des Inhalts des Font-Elements, wodurch die Abwärtskompatibilität mit anfänglichen Implementierungen sichergestellt wird.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="bitmap"></a>Bitmap


```HTML
bitmap
<!element   bitmap   empty>
<!attlist   bitmap
   XML-link    cdata               #fixed "simple"
   href        cdata               #REQUIRED
   title       cdata               #implied
   behavior    cdata               #implied
   show        (embed|replace|new) #fixed "embed"
   inline      (true|false)        #fixed "true"
   actuate     (auto|user)         #fixed "auto"
>
```



Das Bitmap-Element ermöglicht einen Verweis auf eine Out-of-Line-Bildressource (normalerweise eine Bitmap), die in einer Grafik enthalten sein soll.

Bitmap ist eine Funktion der Ebene 1.

Das Behavior-Attribut kann verwendet werden, um anzugeben, wie die Bitmap von einer Bearbeitungs Anwendung behandelt werden soll. Der Wert kann eines oder beide der folgenden Token sein.



| Token    | BESCHREIBUNG                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| gesondert | Markiert die Bitmap als separate Entität, die nicht als integraler Bestandteil des Dokuments angesehen werden sollte. Die Bitmap sollte nicht im Dokument aufbewahrt werden. Wenn das Dokument kopiert wird, sollte die Bitmap nicht kopiert werden. Wenn das Dokument verschoben wird, sollte die Bitmap nicht mit dem Dokument verschoben werden. |
| original | Das Title-Attribut identifiziert den ursprünglichen Speicherort der Bitmap als URL. Andernfalls wird die Bedeutung von Title nicht angegeben.                                                                                                                                                          |



 

Diese Werte sind beide Hinweise zum erwarteten Verhalten. Die separate Option bezieht sich auf das Verhalten der Daten, auf die von href verwiesen wird. Wenn sowohl "separat" als auch "Original" angegeben sind, wird erwartet, dass die Anwendung den href-URI ignoriert und die Bitmap aus den ursprünglichen Daten neu generiert. Wenn nur "Original" angegeben wird, wird davon ausgegangen, dass die Anwendung den href-URI verwendet, um die Bitmap zu suchen, aber dem Benutzer die Möglichkeit gibt, Sie erneut zu generieren.

Es ist zulässig, dass der href-URI und das Title-Attribut denselben (lexikalischen) Wert haben. Dies ist angemessen, wenn die referenzierte Bitmap nicht "gespeichert mit" dem Dokument ist. Es ist (obwohl nicht erforderlich), dass href für die eigene Kopie der Bitmap des Dokuments verwendet wird. diese kann gelöscht werden, wenn die verweisenden Formen gelöscht werden, und dieser Titel wird verwendet, um eine freigegebene Kopie anzugeben. Wenn beide denselben Wert enthalten, gibt es daher keine Dokument spezifische Kopie.

Anwendungen ignorieren den Hinweis möglicherweise, wenn er nicht in das tatsächliche Speichermodell der XML-Daten passt.

[![zurück ](images/top.gif) zum Anfang](#top)

### <a name="picture-file-formats"></a>Bild Dateiformate

Im Zusammenhang mit diesem Vorschlag sind externe Daten entweder eine Bitmap oder eine Datei, die zum Herstellen einer Bitmap verwendet wird. Auf renderebene 0 muss kein externes Bitmap-Format unterstützt werden--Pfade können nur mit voll Tonfarben gefüllt werden. Bitmaps müssen unterstützt werden, um den vollständigen Satz von Füllungen der Rendering-Ebene 1 zu erzeugen. Renderstufe 1 umfasst nur die folgenden Formate:

1.  Jff, d. h. ISO/IEC 10918 Formatierungsdaten, die in eine Datei mit dem JFI-Header eingebettet sind (die nach dem Soi-Ersteller als bestimmter APP0 Marker angesehen werden können) und einschließen (nur) den Bereich von JPEG-Formaten, die vom IJG V6-Code unterstützt werden.
2.  PNG, gemäß der Spezifikation der PNG-Version 1,0.

Die Rendering-Ebene 2 bietet auch Unterstützung für Folgendes:

-   GIF, wie von der von Compuserv in 1987 veröffentlichten GIF-Spezifikation (normalerweise als "GIF87a" bezeichnet) definiert. GIF89a muss auch auf dieser Ebene unterstützt werden, unterliegt der Einschränkung, dass die Daten keine Erweiterungs Blöcke enthalten dürfen, die eine Interpretation benötigen, um die Bitmap außer der Grafik Steuerelement-extensionswithouta-Anforderung für eine Benutzereingabe oder eine Verzögerungszeit anzuzeigen. Dies ermöglicht das Einschließen von Kommentaren, jedoch nicht die nur-Text-Erweiterung. Eine Anwendung kann Anwendungs Erweiterungen (0x21, 0xFF) einfügen, aber mit der Terminologie dieses Vorschlags dürfen diese nur die Bearbeitung, nicht das Rendering und Daten enthalten.

Jedes andere Datenformat, das in der Grafik verwendet wird, erzwingt, dass diese Grafik mindestens die Bearbeitungs Ebene 3 und möglicherweise die Renderingebene Ebene 3 (wenn die Daten zum Rendern der Grafik erforderlich sind). Es wird empfohlen, die unterstützten Formate zu veröffentlichen. Microsoft Office unterstützt z. b. die folgenden zusätzlichen Formate nativ und kann daher Bearbeitungsdaten in dieser Form schreiben:

1.  WMF--Windows-Metadatei (Win 3,1-Format)
2.  EMF--Windows "Enhanced"-Metadatei (Win32-Format)
3.  PICT-Mac OS QuickDraw-PICT-Datei (alle Versionen, aber ohne QuickTime-Einträge oder andere Erweiterungen)
4.  BMP--Windows-Bitmap-Dateiformat, "OS/2" (bitmapcore), BitmapInfo, BITMAPV4 und BITMAPV5 Formate

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="vector"></a>Vektor


```HTML
v
<!element v "( #pcdata | p )*">
```



Ein Vektorgrafik Pfad wird als "pcdata" codiert. Der Inhalt des v-Elements wird gemischt und enthält eine Vektor Pfad Beschreibung, die optional mit p-Elementen parametrisiert wird.

[Zurück zur VML-Übersicht](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

