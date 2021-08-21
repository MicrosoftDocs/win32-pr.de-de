---
title: Grundlegende VML-Typen
description: In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Migrieren Sie Webseiten und Anwendungen, die auf VML basieren, zu SVG oder anderen weit verbreiteten Standards.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Vector Markup Language (VML), grundlegende Typen
- VML (Vector Markup Language),Basistypen
- Vektorgrafiken,einfache VML-Typen
- Vector Markup Language (VML), Typen
- VML (Vector Markup Language),Typen
- Vektorgrafiken, VML-Typen
- Grundlegende VML-Typen
- Boolescher Typ
- Bruchtyp
- Ordinaltyp
- length-Typ
- Measuretyp
- Winkeltyp
- Farbtyp
- Schriftarttyp
- Bitmaptyp
- Vektortyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70dbb2e540e809b88b446cceda9973f8988c7241cae7f4f96402a0edc7906550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347819"
---
# <a name="basic-vml-types"></a>Grundlegende VML-Typen

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

**Contents**

-   [Introduction (Einführung)](#introduction)
-   [boolean](#boolean)
-   [fraction](#fraction)
-   [Koordinieren](#ordinate)
-   [length](#length)
    -   [Alternative Darstellungen](#alternative-representations)
-   [Messen](#measure)
    -   [Alternative Darstellungen](#alternative-representations)
-   [angle](#angle)
    -   [Alternative Darstellungen](#alternative-representations)
-   [color](#color)
    -   [Farbeinheiten](#color-units)
    -   [HTML-Farben](#html-colors)
    -   [Schemafarben](#scheme-colors)
    -   [Systemfarben](#system-colors)
    -   [Reine Farben](#pure-colors)
    -   [Farbanpassungen](#color-adjustments)
-   [Schriftart](#font)
-   [Bitmap](#bitmap)
    -   [Bilddateiformate](#picture-file-formats)
-   [Vektor](#vector)

## <a name="introduction"></a>Einführung

Dieser Vorschlag verwendet eine kleine Anzahl grundlegender Typen, die in der folgenden Tabelle aufgeführt sind.



| Typ                  | Element           | Grundlegende Darstellung | Beschreibung                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [boolean](#boolean)   |                   | 1 Bit                      | Ein boolescher Wert: true oder false.                                                                      |
| [fraction](#fraction) |                   | Zahl 2 6                 | Ein numerischer Wert, der um 2 6 (65536) skaliert und als ganze Zahl mit Vorzeichen gespeichert wird.                               |
| [Koordinieren](#ordinate) |                   | 30-Bit-Ganzzahl plus Vorzeichen   | Teil einer Koordinate (z. B. in einem Pfad) der durch coord definierten Werte.                                |
| [length](#length)     |                   | [Wwu](#length)             | Eine physische Länge, z. B. die Breite einer Linie oder die Größe einer Schriftart.                                |
| [Messen](#measure)   |                   | EMU oder Nummer 2 6          | Entweder eine physische Länge, einschließlich einer Anzahl von Gerätepixeln, oder ein Bruchteil einer anderen Menge. |
| [angle](#angle)       |                   | Grad 2 6                | Ein Winkel; Positiv ist im Uhrzeigersinn.                                                                     |
| [color](#color)       | [c](#color)       | complex                    | Ein Element, mit dem eine Farbe abgeleitet werden kann.                                                        |
| [Schriftart](#font)         | [Schriftart](#font)     | complex                    | Eine Beschreibung einer Schriftart.                                                                             |
| [Bitmap](#bitmap)     | [Bitmap](#bitmap) | href                       | Ein Verweis auf eine externe Bilddatei.                                                             |
| [Vektor](#vector)     | [v](#vector)      | complex                    | Eine Beschreibung eines Vektorpfads                                                                       |



 

Die "grundlegende Darstellung" ist die Darstellung mit der höchsten Genauigkeit, die der Vorschlag erfordert, um eine konforme Implementierung zu verwalten. -Daten gehen verloren, wenn die Implementierung die Daten nicht mit der erforderlichen Genauigkeit darstellen kann. Die Farb-, Schriftart- und Vektortypen entsprechen Elementen, die selbst strukturiert sind– in einem Sinne sind sie keine grundlegenden Typen; Es ist jedoch praktisch, sie in diesem Vorschlag als solche zu behandeln.

Jedem nicht komplexen Basistyp ist ein Element mit demselben Namen zugeordnet. Diese Elementnamen sind reserviert und dürfen nicht für andere Zwecke innerhalb von Erweiterungen verwendet werden, auch wenn die Verwendung innerhalb eines onview="skip"-Erweiterungselements liegt. Aus diesem Grund ist es möglich, dass eine Implementierung, die unbekanntes XML-Code trifft, eine effiziente interne Speicherung des unbekannten XML-Code ermöglicht, solange die Werte in die "Type"-Elemente eingeschlossen sind.


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



Im ersten Beispiel oben muss die Zeichenfolge "1.578" als Zeichensequenz gespeichert werden (die Implementierung weiß nicht, ob es sich um eine Zeichenfolge oder eine Zahl handelt). Im zweiten Beispiel gibt das Fraction-Element an, dass der Inhalt eine Zahl ist, daher kann er in die Bruchdarstellung mit hoher Genauigkeit konvertiert werden.

Komplexe Typen (einschließlich Bitmap) verfügen über zugeordnete Elementnamen, die zum Begrenzen des Werts verwendet werden. Dadurch wird die Analyse vereinfacht, indem sichergestellt wird, dass die komplexeren Analyseaufgaben eindeutigen Elementtags zugeordnet werden.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="boolean"></a>boolean


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



Ein boolescher Wert wird als Schlüsselwort dargestellt, das den Zustand des Flags angibt. Die folgenden Schlüsselwörter sind definiert.



| Wert für "true" | Wert für false |
|----------------|-----------------|
| true           | false           |
| Ja            | Nein              |
| on             | aus             |
| t              | f               |
| 1              | 0               |



 

Eine Implementierung kann einen beliebigen Wert schreiben und muss alle Werte erkennen. Eine Implementierung kann Werte von einer Darstellung in eine andere ändern.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="fraction"></a>fraction


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



Alle numerischen Werte (d. h. Werte dimensionsloser Mengen) in diesem Vorschlag können als ganze Zahlen gespeichert werden, indem sie um 2 6 (65536) skaliert werden. Eine Zahl kann entweder in dieser Form mit dem Suffix f oder als Dezimalzahl ohne Suffix angegeben werden. Daher stellen die folgenden hypothetischen Elemente denselben Wert dar.


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



Eine Menge mit dem Suffix f muss eine ganze Zahl sein. Bruchzahlen sind nicht zulässig. Die resultierende ganze Zahl muss als 32-Bit-2-Komplement mit Vorzeichen dargestellt werden können. Daher ist der effektive Bereich der Darstellung 32768 (tatsächlich kleiner als 32768 und größer oder gleich -32768).

Eine konforme Implementierung ist erforderlich, um Werte zu erhalten, die als f-Werte ausgedrückt werden. Werte, die als Dezimalzahlen dargestellt werden, können in einen f-Wert konvertiert und auf diese Weise gespeichert werden. Eine Anwendung darf intern generierte Werte in jeder geeigneten Einheit aufzeichnen. Ein aus einem vorhandenen Dokument gelesener Wert muss jedoch entweder bis zur vollständigen ursprünglichen Genauigkeit beibehalten oder in einen f-Wert konvertiert werden.

Wenn die Implementierung dies nicht tun kann, muss sie den Benutzer warnen, dass Möglicherweise Daten verloren gehen. (Es ist akzeptabel, eine solche Warnung einmal aus zu geben, wenn extern generierte Daten zum ersten Mal gefunden werden.)

Wenn ein Dezimalwert in das f-Format konvertiert wird, kann die Implementierung einen beliebigen arithmetischen Rundungsmodus verwenden. eine ganze Zahl muss jedoch genau in das Format f konvertiert werden. Es wird empfohlen, dass Implementierungen konvertiert werden, indem sie auf minus unendlich gerundet werden und dass die Konvertierung immer genau ist.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="ordinate"></a>Koordinieren


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



Die Einheiten des koordinatenkoordinaten Systems sind von einem nominalen Typ, der als Ordinalzahl bezeichnet wird. Dies ist ein Maß für die Länge, wird aber nur in Bezug auf das Rechteck verwendet, das coord eingibt. Jeder Wert vom Typ ordinte wird durch die *w-* und *h-Werte* des Coord und das resultierende Verhältnis skaliert, das verwendet wird, um eine echte Messung auf dem Ausgabegerät zu erstellen.

Eine konforme Implementierung muss ordinierte Werte von bis zu 30 Bits plus Vorzeichen verarbeiten können (d. h. eine 31-Bit-Ganzzahl mit Vorzeichen, keine 32-Bit-Ganzzahl mit Vorzeichen). Es wird jedoch empfohlen, dass Implementierungen versuchen, Koordinaten für Pfadelemente und ähnliche Elemente mit einer Genauigkeit von etwa 16 Bits zu erzeugen. Dadurch wird die Wahrscheinlichkeit eines Unterlaufs oder Überlaufs in einer nicht konformen Implementierung minimiert.

Ordinalwerte sind immer integral. Ein Dezimaltrennzeichen wird möglicherweise nicht in einem Wert vom Typ Ordinalzahl angezeigt. An Werte vom Typ ordinte dürfen keine Einheitenspezifizierer angefügt werden.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="length"></a>length


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



Eine Länge ist eine reale Messung oder manchmal eine Messung in Gerätepixeln. Es wird empfohlen, dass Implementierungen die Verwendung von Gerätepixeln (px) vermeiden.

Alle STANDARDMÄßIGEN CSS1-Einheitenqualifizierer sind für eine Länge zulässig. [](https://www.w3.org/pub/WWW/TR/REC-CSS1) Darüber hinaus kann der Qualifizierer Emu verwendet werden. Dieser Qualifizierer bezieht sich auf eine Einheit – die EMU (English Metric Unit) –, die ein gemeinsamer Nenner der Messmengen ist, die weit verbreitet in Computergrafiken verwendet werden. Die EMU ist "inch/914400", d. h., es gibt 914400 EMU pro Zoll. <sup></sup> In der folgenden Tabelle ist die Anzahl der EMUs in einer kleinen Anzahl häufig gefundener Einheiten aufgeführt.



| Anzahl der EMUs | Zahl pro Zoll | Zahl pro Millimeter | Beschreibung             |
|----------------|-----------------|-----------------------|-------------------------|
| 360            |                 | 0.01                  | Win32 HIMETRIC          |
| 12700          | 72              |                       | "Point"                 |
| 635            | 1440            |                       | Win32 TWIP              |
| 762            | 1200            |                       | Drucker mit hoher Auflösung |



 

Bruchzahlen von EMUs sind nicht zulässig. Jede Messung muss als 32-Bit-Ganzzahl mit Vorzeichen von EMUs darstellbar sein – dies beschränkt die Größe einer Messung auf 2348 Zoll – etwa 59 Meter oder 65 Meter. Da die Messungen immer auf die Größe eines Renderings auf einem nominalen Ausgabegerät mit Bildschirm- oder Seitengröße verweisen, liegen sie immer innerhalb dieses Bereichs.

Beachten Sie jedoch, dass die Darstellung für reale Messungen ungeeignet ist und dass dort, wo diese aufgezeichnet werden (z. B. um die reale Größe eines Pfads zu erfassen), eine andere Darstellung verwendet werden muss.

Eine konforme Implementierung ist erforderlich, um Werte zu erhalten, die eine genaue Anzahl von EMUs sind. Auf andere Weise dargestellte Werte können in einen EMU-Wert konvertiert und auf diese Weise gespeichert werden. Eine Anwendung darf intern generierte Werte in jeder geeigneten Einheit aufzeichnen. Ein aus einem vorhandenen Dokument gelesener Wert muss jedoch entweder bis zur vollständigen ursprünglichen Genauigkeit beibehalten oder in einen EMU-Wert konvertiert werden.

Wenn die Implementierung dies nicht tun kann, muss sie den Benutzer warnen, dass Möglicherweise Daten verloren gehen. (Es ist akzeptabel, eine solche Warnung einmal aus zu geben, wenn extern generierte Daten zum ersten Mal gefunden werden.)

In der Praxis werden physische Längen für relativ wenige Messungen in diesem Vorschlag verwendet. Die Daten, die normalerweise am wichtigsten sind, sind die Pfaddaten, die im Koordinatensystem codiert werden, das auf Formbasis durch Coord definiert wird.

### <a name="alternative-representations"></a>Alternative Darstellungen

Die Standardlängendarstellungen von HTML werden durch [CSS1 definiert.](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) Relative Einheiten, mit Ausnahme des Pixels, sind im Kontext, in dem Längen in diesem Vorschlag verwendet werden, nicht sinnvoll und dürfen nicht verwendet werden. Wenn das Dokument die beabsichtigte Pixelgröße (Ziel) auf zeichnet, wird die Übersetzung von Pixeln in EMU definiert. Andernfalls sollte der von [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) definierte Standardwert von 90 dpi verwendet werden.

Mit Ausnahme von Emu kann jeder Wert als Dezimalbruch angegeben werden. Wenn ein Dezimalwert in EMU konvertiert wird, kann die Implementierung einen beliebigen arithmetischen Rundungsmodus verwenden. (Die einzige Möglichkeit für eine Erstellungsanwendung, ein bestimmtes Ergebnis zu garantieren, besteht in der Angabe in emu.)

Wenn kein Einheitenspezifizierer in einem Längenwert angegeben wird, muss die Implementierung emu voraussetzungen.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="measure"></a>Kennzahl


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



Ein Measure ist eine Menge, die entweder eine Länge [oder](#length) einen Bruch [sein kann.](#fraction) Dies ähnelt den HTML- und CSS-Längenmessungen, die in vielen Fällen entweder physische Messungen oder Prozentsätze einer anderen Menge sein können. Wenn kein Einheitenspezifizierer angegeben wird, muss davon ausgegangen werden, dass der Wert ein Dezimalbruch ist (daher wird dieses Verhalten von fraction und nicht von length geerbt.)

Im Gegensatz zur Länge hat ein Pixelwert eine kontextdefinierte Bedeutung, sodass die Konvertierung in Emu normalerweise ungeeignet ist. Es gibt drei mögliche grundlegende Darstellungen, die von der Implementierung verwaltet werden müssen (d. h., eine Darstellung kann ohne Verlust von Informationen nicht in eine andere konvertiert werden).

1.  Ein Bruchwert sollte im Bruchformat beibehalten [werden](#fraction) (ein "f"-Wert).
2.  Eine physische Länge sollte in EMU beibehalten werden.
3.  Ein Pixelwert sollte als ganze Anzahl von Pixeln beibehalten werden.

Bruchzahlen von Pixeln sind nicht zulässig.

### <a name="alternative-representations"></a>Alternative Darstellungen

Alle alternativen Darstellungen von [Bruch und](#fraction) [Länge](#length) sind zulässig.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="angle"></a>angle


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



Die grundlegende Darstellung eines Winkels ist eine Anzahl von Graden, die durch 2 6 (65536) multiplet und als ganze Zahl gespeichert werden. Da der Koordinatenraum invertiert wird (die positive y-Achse ist nach unten), ist ein Winkel im Uhrzeigersinn positiv. Eine konforme Implementierung ist erforderlich, um die vollständige Genauigkeit eines solchen Werts beizubehalten.

Eine Implementierung darf einen beliebigen Bereich für Winkel verwenden und darf einen Winkel normalisieren (z. B. bis -180 bis +180 oder 0 bis 360 ). Implementierungen müssen nicht konsistent sein. die ganzzahlige Darstellung eines Winkels darf jedoch den Bereich einer 32-Bit-Ganzzahl mit Vorzeichen nicht überschreiten.

Das Suffix fd wird verwendet, um diese Darstellung eines Winkels (Bruchteil des Grads) zu identifizieren. Beachten Sie, dass dies vom f-Suffix für einen dimensionslosen Bruch unterschieden wird, obwohl eine identische Arithmetik zur Unterstützung verwendet werden kann. Der Standardwert für einen Winkelwert ist ein einfacher Grad, d. h. ein nicht skaliertes Wert. Dies kann auch mit dem Suffix " " (dem Gradsymbol) signalisiert werden. Die Verwendung dieser ist jedoch von einer geeigneten Dokumentcodierung abhängig. Folglich wird das Suffix deg auch als Mittelwert definiert. Der vollständige Satz der möglichen Ausreichenden ist wie folgt.



| Suffix       | Konvertierungsfaktor | Kommentare                               |
|--------------|-------------------|----------------------------------------|
| Fd           | 1                 | Interne Darstellung mit hoher Genauigkeit |
| none, deg,   | 65536             | Grad                                |
| rad          | 65536pi/180       | Radians                                |



 

### <a name="alternative-representations"></a>Alternative Darstellungen

Die Skalierungstransformation weist Diskontinuitäten bei ungeraden Vielfachen von 45 auf. Daher ist es äußerst wichtig, dass die Konvertierung einer ungenauen Menge klar definiert ist. Aus diesem Grund wird die Arithmetik der Konvertierung so definiert, dass sie auf minus unendlich gerundet wird.

Da dies in einigen Implementierungen schwierig oder unmöglich zu garantieren ist, wird die Verwendung von Folgendem als Feature der Stufe 3 definiert:

1.  Ein beliebiger Fractional Degree-Wert.
2.  Beliebiger Radianwert

Daher müssen werte qualifizierte fd- und nicht qualifizierte integrale Werte oder integrale Werte qualifizierte deg oder genau von einer konformen Implementierung der Ebene 0 verarbeitet werden. andere Werte benötigen dies nicht. Es wird dringend empfohlen, dass jede Implementierung die Konvertierung von einem Bruchteil des Werts in einen skalierten (fd)-Gradwert genau verarbeiten soll. Dies kann ohne Gleitkommaunterstützung erfolgen.

Die genaueren Anforderungen für die Konvertierung unterscheiden fd von f.

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="color"></a>color


```HTML
c
<!element c  %color;>
```



Farben sind ein wesentlicher Bestandteil moderner Computergrafiken. Der Vorschlag verwendet die bewährten Methoden zum Angeben fester Farben. Farben in Diagrammen sind jedoch selten einfache statische Farben. sie werden häufig von anderen Elementen im Diagramm abgeleitet. Da ein Großteil dieser Informationen sehr anwendungsspezifisch ist, bietet dieser Vorschlag zwei grundlegende Mechanismen, um ein solches Verhalten anzugeben:

1.  Eine Farbe kann von einer anderen Farbe in der gleichen Form abgeleitet werden.
2.  Eine kleine Anzahl arithmetischer Operationen wird zum Ableiten oder Ändern einer Farbe definiert.

Der Prototypformmechanismus ergänzt dies durch die Möglichkeit, Prototypen zu definieren, von denen Farben geerbt werden können.


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



Ein Farbwert ist eine Obermenge der [CSS1-Farbdefinition.](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) Die Erweiterungen ermöglichen es, den RGB-Farbwert aus anderen Farben innerhalb der Form oder aus einem mit CSS1 definierten Gesamtfarbschema zu bestimmen.

Wenn der Wert eines Elements als Farbe definiert ist, definiert der *Inhalt* eines Elements den Farbwert mithilfe eines einzelnen Farbtokens, das optional durch eine arithmetische Operation für die entsprechende RGB-Farbe geändert wird.

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

### <a name="color-units"></a>Farbeinheiten

Der vollständige Satz von Farbtoken stammt aus einer Vielzahl von Quellen: HTML, CSS1 und diesem Vorschlag. Sie werden wie folgt mithilfe der Notation aus [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) oder der für die XML-Verknüpfung definierten XPointer-Notation definiert.

In den XPointer-Definitionen ist die Speicherortquelle das Element, das den Farbwert enthält, und der Ausdruck bezieht sich auf den gesamten Elementsatz der Form, als ob alle Basisprototypelemente mit der Form zusammengeführt worden wären. Wenn das entsprechende Element nicht vorhanden ist, wird der Standardwert für dieses Element an seiner Stelle verwendet.



| Color            | Definition                                                                                                  | Ebene | Beschreibung                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name             | Siehe unten                                                                                                   | 0     | HTML-Farbname, wie in der folgenden Tabelle aufgeführt.                                                                                                                            |
| \#rr'gg'bb'      | \#rr'gg'bb'                                                                                                 | 0     | Standardmäßige CSS1/sRGB-Farbdarstellung mit Werten im Bereich 0,.255, dargestellt mit jeweils 2 Hexadezimalziffern.                                                     |
| \#Rgb            | \#rrggbb                                                                                                    | 1     | Verkürztes CSS1-Formular mit nur drei Hexadezimalziffern.                                                                                                                   |
| rgb(r,g,b)       | \#(r) (g) (b)                                                                                                 | 1     | CSS1 RGB-Formular; die Elemente des RGB-Werts werden wie in [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) definiert konvertiert.                                      |
| fill             | ancestor(1,shape)<br/> child(1, fill)<br/> child(1, color)<br/>                           | 1     | Die Vordergrundfüllfarbe der Form.                                                                                                                                   |
| fillBack         | ancestor(1,shape)<br/> child(1, fill)<br/> child(1, back)<br/> child(1, color)<br/> | 1     | Die Hintergrundfarbe der Formfüllung.                                                                                                                                   |
| line             | ancestor(1,shape)<br/> child(1, line)<br/> child(1, color)<br/>                           | 1     | Die Vordergrundlinienfarbe der Form.                                                                                                                                   |
| lineBack         | ancestor(1,shape)<br/> child(1, line)<br/> child(1,back) <br/> child(1, color)<br/> | 1     | Die Hintergrundlinienfarbe der Form.                                                                                                                                   |
| lineOrFill       | line, fill                                                                                                  | 1     | Der Zeilenwert, wenn kein Standardwert verwendet wird, andernfalls der Füllwert. Dadurch wird effektiv die Farbe zurückgegeben, die sich am Rand der Form befindet.                                           |
| fillThenLine     | fill, line                                                                                                  | 1     | Der Füllwert, wenn kein Standardwert verwendet wird, andernfalls der Zeilenwert. Dadurch wird effektiv die Hauptfarbe der Form zurückgegeben (wenn die Form nicht ausgefüllt ist, ist das Ergebnis die Linienfarbe).   |
| shadow           | ancestor(1,shape)<br/> child(1, shadow)<br/> child(1, color)<br/>                         | 2     | Die Farbe des Schattens (dies ist ein Feature der Ebene 2).                                                                                                                      |
| scheme           | Siehe unten                                                                                                   | 1     | Eine Schemafarbe aus dem für das Dokument definierten Schema. siehe unten.                                                                                                       |
| scheme(*index*)  | Siehe unten                                                                                                   | 1     | *Schemafarbindex,* beginnend mit 0; siehe unten.                                                                                                                         |
| this             | Impliziert                                                                                                     | 2     | Der Vorgang (Ausfüllen eines Pfads oder Zeichnen) wird auf andere Weise definiert (z. B. als Bitmap), und die Farbe gibt eine "Änderung" an den Farben an, die so impliziert sind. |
| palette(*index*) | Impliziert                                                                                                     | 3     | Verhält sich auf die gleiche Weise wie dies, mit dem Unterschied, dass genau ein Eintrag in einer Bitmapfarbtabelle identifiziert wird. Nur zulässig, wenn dies explizit angegeben ist.                             |
| Keine             | \-                                                                                                          | 2     | Gibt das Fehlen einer Farbe an. kann verwendet werden, um einen Zeichnungsvorgang abzubrechen, der die Farbe verwendet.                                                                          |
| System           | Siehe unten                                                                                                   | 3     | Eine von der Systembenutzerschnittstelle definierte Farbe.                                                                                                                             |



 

Mit dieser Farbe kann ein Farbwert eine Änderung an einer Farbe angeben, die auf andere Weise abgeleitet wird. insbesondere kann ein einzelner Vorgang für alle Farben in einer Bitmap angegeben werden. Die *Palette(Index)-Farbe* identifiziert einen bestimmten Eintrag in einer palettenzuordnungsbasierten Bitmap. Die Verwendung dieser Option ist nur für die Aufzeichnung eines Farbtabelleneintrags definiert, der in einer solchen Bitmap als transparent betrachtet werden sollte.

Die Definition eines Farbwerts darf weder direkt noch indirekt auf sich selbst verweisen. Wenn eine solche Definition gefunden wird, wird empfohlen, aber nicht erforderlich, dass die Implementierung den nicht definierten Wert als schwarz behandelt.

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

### <a name="html-colors"></a>HTML-Farben

[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) definiert die folgenden 16 Farbnamen:



Farbnamen und sRGB-Werte

![Beispiel für schwarze Farbe.](images/black.gif)

Black = " \# 000000"

![Beispiel für eine grüne Farbe.](images/green.gif)

Grün = " \# 008000"

![Beispiel für silberfarbene Farbe.](images/silver.gif)

Silver = " \# C0C0C0"

![Beispiel für Limonenfarbe.](images/lime.gif)

Lime = " \# 00FF00"

![Beispiel für graue Farbe.](images/gray.gif)

Gray = " \# 808080"

![Beispiel für olivfarbene Farbe.](images/olive.gif)

^ = " \# 808000"

![Beispiel für weißer Farbe.](images/white.gif)

White = " \# FFFFFF"

![Beispiel für ywllow-Farbe.](images/yellow.gif)

Gelb = " \# FFFF00"

![Beispiel für marunische Farbe.](images/maroon.gif)

Maroon = " \# 800000"

![Beispiel für farbgebungsfarbenes Farbschema.](images/navy.gif)

Unicode = " \# 000080"

![Beispiel für eine rote Farbe.](images/red.gif)

Red = " \# FF0000"

![Beispiel für blaue Farbe.](images/blue.gif)

Blue = " \# 0000FF"

![Beispiel für violette Farbe.](images/purple.gif)

Purple = " \# 800080"

![Beispiel für Tealfarbe.](images/teal.gif)

Teal = " \# 008080"

![Beispiel für farbgebungsfarbene Farben.](images/fuchsia.gif)

Sollia = " \# FF00FF"

![Beispiel für Aquafarbe.](images/aqua.gif)

Aqua = " \# 00FFFF"



 

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

### <a name="scheme-colors"></a>Schemafarben

Die Schemafarben, auf die vom Schema verwiesen wird, werden auf Dokumentebene mithilfe des Metatags mit dem Namensattribut "Designfarbschema" definiert.


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



Mit diesem Tag können bis zu acht Schemafarben definiert werden. Nicht definierte Farben sollten standardmäßig schwarz sein. Die Schemafarben ermöglichen das Ändern des Farbschemas, das für ein vollständiges Dokument verwendet wird, nur durch Ändern des Inhalts des Designfarbschemas. Um sicherzustellen, dass aus verschiedenen Erstellungsanwendungen importierte Grafiken die Schemafarben konsistent verwenden, werden die folgenden Interpretationen definiert. Die "Nutzung" ist eine kurze Beschreibung des Zwecks, und die Spalte "beschreibung" enthält zusätzliche Details.



| Index | Name              | Verwendung                         | BESCHREIBUNG                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| 0     | scheme.background | Hintergrund                    | Die Farbe, die für den Hintergrund einer Grafik (und häufig für die gesamte Seite) verwendet wird.                                    |
| 1     | scheme.text       | Text und Zeilen                | Die Farbe für Text, der an eine Form angefügt ist, und die Standardlinienfarbe.                                                      |
| 2     | scheme.shadow     | Shadows                       | Standardschattenfarbe– die Farbe, die normalerweise für Formschatten verwendet wird.                                                     |
| 3     | scheme.title      | Titeltext                    | Die Farbe, die für Überschriften- oder Titeltext verwendet werden soll.                                                                              |
| 4     | scheme.fill       | Füllt                         | Standardfüllfarbe– die Farbe, die normalerweise zum Füllen von Formen verwendet wird.                                                          |
| 5     | scheme.accent     | Akzent                        | Normale "Hervorhebungsfarbe", die verwendet wird, um ein wichtiges Element einer Grafik hervorzuheben.                                             |
| 6     | scheme.hyperlink  | Akzent und Link          | Hervorhebungsfarbe, die für Links verwendet wird. Kann für andere Zwecke verwendet werden, bei denen die Farbe einen Link zu anderen Informationen kennzeichnet. |
| 7     | scheme.followed   | Akzent und gefolgter Link | Hervorhebungsfarbe für gefolgte Links; ist auch für Rückwärtslinks geeignet.                                         |



 

Auf eine Schemafarbe kann entweder nach Name oder index verwiesen werden, daher haben scheme.fill und scheme(4) dieselbe Farbe.

Schemafarben sind nicht Teil des Standardschemas, wenn keine Farbe angegeben ist. Eine nicht angegebene Füllfarbe muss immer als weiß interpretiert werden, unabhängig von der Farbe der Schemafarbe 4. Die Akzentfarben sollten gegenüber den Hintergrundfarben (0) und den Füllfarben (4) sowie text- und title-Textfarben dieselbe Eigenschaft haben. Eine Standardtechnik besteht in der Farbfärbung der Akzente und des Standardtexts (in der Regel schwarz oder weiß).

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

### <a name="system-colors"></a>Systemfarben

Anwendungen zeichnen Farben manchmal basierend auf Betriebssystemeinstellungen in Grafiken auf. Normalerweise sind diese vorübergehend und müssen nicht geschrieben werden. Die Systemcolor-Definitionen sind ausschließlich zur Unterstützung vorhanden. Eine Systemfarbe wird eingeführt, indem ein entsprechendes Tag in einem neuen Namespace definiert und die entsprechenden Informationen in den Elementinhalt eingefügt werden.

Dieser Vorschlag definiert ein solches Tag, um die Windows in der Headerdatei winuser.h definierten Benutzeroberflächenfarben zu codieren.


```HTML
win.color
<!element win.color #pcdata>
```



Der Inhalt des Elements ist eine einzelne ganze Zahl, die den Wert der relevanten \_ COLOR-Definition aus winuser.h enthält. Eine ähnliche Technik kann für jede system- oder anwendungsspezifische Farbspezifikation übernommen werden. Es wird dringend empfohlen, dieses Feature nur aus Gründen der Abwärtskompatibilität zu verwenden.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

### <a name="pure-colors"></a>Reine Farben


```HTML
pure
<!elementpure empty>
```



Wenn das Element in einem Farbwert angezeigt wird, ist dies ein Hinweis darauf, dass die Farbe nicht durch ein <pure/> Dithermuster angedeutet werden sollte. Dies ist ein Feature der Ebene 1, das von einer konformen Implementierung nicht erfüllt werden muss. Die Bezeichnung ist wichtig für Grafiken, die auf Geräten mit mittlerer Auflösung angezeigt werden, z. B. Videoanzeigen, bei denen kleine Features (z. B. Linien) schlechte Aliase mit ditherierten Farben verursachen können. Auf Geräten wie Druckern, die normalerweise alle Farben mit Ausnahme der wenigen vollständigen Farben dithern, ist das Dithering normalerweise ausreichend, um dieses Problem zu vermeiden.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

### <a name="color-adjustments"></a>Farbanpassungen

Die Basisfarbe kann durch arithmetische Operationen für den RGB-Wert angepasst werden. Diese Vorgänge werden mit zusätzlichen Elementen innerhalb des Farbwerts definiert. Solche Anpassungen sind nur nützlich, wenn sie auf Farben angewendet werden, die von anderen Elementen abgeleitet wurden. Es ist gültig, eine solche Anpassung für einen festen Farbwert anzugeben. eine Implementierung kann dies jedoch auf den entsprechenden RGB-Wert reduzieren und anstelle des Originals speichern.

Alle in diesem Abschnitt beschriebenen Farbanpassungsfeatures sind Features der Ebene 1.


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



Der Parameter der ersten sechs Vorgänge ist ein einzelner integraler numerischer Wert im Bereich von 0 bis 255. Die Anpassung erfolgt für den RGB-Wert von 3 x 8 Bit wie folgt:

1.  Wenn angegeben wird, wird der RGB-Wert durch yyy ersetzt, wobei y der Ludomanzwert (y) ist, der anhand des sRGB-Werts im Anschluss an <gray/> ITU-r BT.709 berechnet wird. Diese Berechnung ist:
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  Wenn eine Color.op-Änderung angegeben wird, wird jede Komponente separat gemäß der folgenden Tabelle angepasst. c ist der Komponentenwert, und p ist der Color.Parameter-Wert.

    | Vorgang       | Formel                            |
    |-----------------|------------------------------------|
    | Verdunkeln          | c := cxp/255                       |
    | Aufhellen         | c := 255 - (255-c)xp/255           |
    | add             | c := c + p                         |
    | Subtrahieren        | c := c - p                         |
    | reversesubtract | c := p - c                         |
    | Schwarzweiss      | wenn c < p, dannc := 0elsec := 255 |

    

     

    Wenn der berechnete Komponentenwert c 255 überschreitet, wird in jedem Fall 255 verwendet, und wenn er kleiner als 0 ist, wird 0 verwendet.

3.  Wenn angegeben ist, wird der Wert 128 subtrahiert oder jeder Komponente hinzugefügt, je nach dem, ob die Komponente kleiner als <INVERT128/> 128 ist oder nicht.
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  Wenn <invert/> angegeben wird, wird jede Komponente durch 255 minus dem Wert der Komponente ersetzt.
    ```HTML
    c := 255-c
    ```

    

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="font"></a>font


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



Eine Schriftart wird mithilfe eines Formatattributs identifiziert, wie in [CSS1 Abschnitt 5.2 (Schriftarteigenschaften) definiert.](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) Der Text des Schriftartelements ist derzeit nicht definiert, kann aber in Zukunft zum Codieren von Standardschriftartinformationen verwendet werden. Die ersten Implementierungen dieses Vorschlags sollten die Informationen beibehalten, aber nicht interpretieren.

Es ist ratsam, dass in Zukunft Unterstützung für Out-of-Line-Schriftartinformationen (herunterladbare Schriftarten oder freigegebene Schriftartressourcen) hinzugefügt wird. Dies erfolgt durch ein XML-Link-Element innerhalb des Inhalts des Schriftartelements, um die Abwärtskompatibilität mit anfänglichen Implementierungen sicherzustellen.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

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



Mit dem Bitmapelement kann ein Verweis auf eine Out-of-Line-Bildressource (normalerweise eine Bitmap) in eine Grafik aufgenommen werden.

bitmap ist ein Feature der Ebene 1.

Das Behavior-Attribut kann verwendet werden, um anzugeben, wie die Bitmap von einer Bearbeitungsanwendung behandelt werden soll. Der Wert kann eines oder beide der folgenden Token sein.



| Token    | BESCHREIBUNG                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Separate | Markiert die Bitmap als separate Entität, die nicht als integraler Teil des Dokuments betrachtet werden sollte. Die Bitmap sollte nicht mit dem Dokument beibehalten werden. Wenn das Dokument kopiert wird, sollte die Bitmap nicht kopiert werden. Wenn das Dokument verschoben wird, sollte die Bitmap nicht damit verschoben werden. |
| original | Das Title-Attribut identifiziert die ursprüngliche Position der Bitmap als URL. andernfalls wird die Bedeutung des Titels nicht angegeben.                                                                                                                                                          |



 

Diese Werte sind hinweise auf das erwartete Verhalten. Die separate Option bezieht sich auf das Verhalten der Daten, auf die href verweist. Wenn sowohl separate als auch originale angegeben werden, wird erwartet, dass die Anwendung den href-URI ignoriert und die Bitmap aus den ursprünglichen Daten neu generiert. Wenn nur original angegeben wird, wird von der Anwendung erwartet, dass sie den href-URI verwendet, um die Bitmap zu finden, dem Benutzer jedoch die Möglichkeit gibt, sie erneut zu generieren.

Es ist zulässig, den href-URI und das Title-Attribut auf denselben (lexikalischen) Wert zu ändern. Dies ist geeignet, wenn die Bitmap, auf die verwiesen wird, nicht mit dem Dokument "gespeichert" wird. Es ist (wenn auch nicht erforderlich) vorgesehen, dass href für die eigene Kopie der Bitmap des Dokuments verwendet wird ( die gelöscht werden kann, wenn die verweisenden Formen gelöscht werden) und dieser Titel verwendet wird, um eine freigegebene Kopie anzugeben. Wenn beide den gleichen Wert enthalten, gibt es also keine dokumentspezifische Kopie.

Anwendungen ignorieren den Hinweis möglicherweise, wenn er nicht in das tatsächliche Speichermodell der XML-Daten passt.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

### <a name="picture-file-formats"></a>Bilddateiformate

Im Rahmen dieses Vorschlags sind externe Daten aus jeder Zeit entweder eine Bitmap oder eine Datei, die zum Erzeugen einer Bitmap verwendet wird. Auf Renderebene 0 muss kein externes Bitmapformat unterstützt werden. Pfade können nur mit Vollfarben gefüllt werden. Zum Rendern des vollständigen Füllstands der Renderebene 1 müssen Bitmaps unterstützt werden. Renderebene 1 enthält (nur) die folgenden Formate:

1.  JFIF, d. h. Iso/IEC 10918-Formatdaten, die in eine Datei mit dem JFIF-Header eingebettet sind (der nach dem SOI-Maker als bestimmter APP0-Marker angesehen werden kann) und (nur) den Bereich der JPEG-Formate enthalten, die vom IJG v6-Code unterstützt werden.
2.  PNG, wie in der PNG-Version 1.0-Spezifikation definiert.

Renderebene 2 bietet auch Unterstützung für Folgendes:

-   GIF, wie in der GIF-Spezifikation definiert, die 1987 von CompuServ veröffentlicht wurde (normalerweise als "GIF87a" bezeichnet). GIF89a muss auch auf dieser Ebene unterstützt werden, jedoch mit der Einschränkung, dass die Daten keine Erweiterungsblöcke enthalten dürfen, die interpretiert werden müssen, um die Bitmap als Grafiksteuersteuererweiterungen anzuzeigenmit einer Anforderung für Benutzereingaben oder einer Verzögerungszeit. Dadurch können Kommentare eingeschlossen werden, aber nicht die Nur-Text-Erweiterung. Eine Anwendung kann Anwendungserweiterungen (0x21, 0xFF) einfügen. Unter Verwendung der Terminologie dieses Vorschlags dürfen diese jedoch nur Bearbeitungs- und nicht Renderingdaten enthalten.

Jedes andere datenformat, das in der Grafik verwendet wird, erzwingt, dass diese Grafik mindestens Bearbeitungsebene 3 und möglicherweise Renderingebene 3 ist (wenn die Daten zum Rendern der Grafik erforderlich sind). Einer Anwendung wird empfohlen, die unterstützten Formate zu veröffentlichen. Beispielsweise unterstützt Microsoft Office die folgenden zusätzlichen Formate nativ und schreibt daher möglicherweise Bearbeitungsdaten in diesem Format:

1.  WMF – Windows Metadatei (Win 3.1-Format)
2.  EMF : Windows "erweiterte" Metadatei (Win32-Format)
3.  PICT : Mac OS QuickDraw PICT-Datei (alle Versionen, aber ohne QuickTime-Datensätze oder andere Erweiterungen)
4.  BMP: Windows Bitmapdateiformat, "os/2" (BITMAPCORE), BITMAPINFO, BITMAPV4 und BITMAPV5

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="vector"></a>Vektor


```HTML
v
<!element v "( #pcdata | p )*">
```



Ein Vektorgrafikpfad wird als pcdata codiert. Der Inhalt des v-Elements wird gemischt und enthält eine Vektorpfadbeschreibung, die optional mit p-Elementen parametrisiert wird.

[Zurück zur Übersicht über VML](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

