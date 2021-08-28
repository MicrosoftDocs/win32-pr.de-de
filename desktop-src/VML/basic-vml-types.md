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
ms.openlocfilehash: a640dbacf875284008714ae404ba462b61652067
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883272"
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
| [length](#length)     |                   | [WWU](#length)             | Eine physische Länge, z. B. die Breite einer Linie oder die Größe einer Schriftart.                                |
| [Messen](#measure)   |                   | EMU oder Nummer 2 6          | Entweder eine physische Länge, einschließlich einer Anzahl von Gerätepixeln, oder ein Bruchteil einer anderen Menge. |
| [angle](#angle)       |                   | Grad 2 6                | Ein Winkel; Positiv ist im Uhrzeigersinn.                                                                     |
| [color](#color)       | [c](#color)       | complex                    | Ein Element, mit dem eine Farbe abgeleitet werden kann.                                                        |
| [Schriftart](#font)         | [Schriftart](#font)     | complex                    | Eine Beschreibung einer Schriftart.                                                                             |
| [Bitmap](#bitmap)     | [Bitmap](#bitmap) | href                       | Ein Verweis auf eine externe Bilddatei.                                                             |
| [Vektor](#vector)     | [V](#vector)      | complex                    | Eine Beschreibung eines Vektorpfads                                                                       |



 

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



| Wert für TRUE | Wert für FALSE |
|----------------|-----------------|
| true           | false           |
| ja            | Nein              |
| on             | aus             |
| t              | f               |
| 1              | 0               |



 

Eine Implementierung kann einen beliebigen Wert schreiben und muss alle Werte erkennen. Eine Implementierung kann Werte von einer Darstellung in eine andere ändern.

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="fraction"></a>fraction


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



Alle numerischen Werte (d. h. Werte dimensionsloser Mengen) in diesem Vorschlag können als ganze Zahlen gespeichert werden, indem sie um 2 6 (65536) skaliert werden. Eine Zahl kann entweder in dieser Form mit dem Suffix f oder als Dezimalzahl ohne Suffix angegeben werden. Daher stellen die folgenden hypothetischen Elemente den gleichen Wert dar.


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



Eine Menge mit dem Suffix f muss eine ganze Zahl sein. Bruchzahlen sind nicht zulässig. Die resultierende ganze Zahl muss als Komplement mit Vorzeichen einer 32-Bit-2-Zahl darstellbar sein. daher ist der effektive Bereich der Darstellung 32768 (tatsächlich kleiner als 32768 und größer oder gleich -32768).)

Eine konforme Implementierung ist erforderlich, um Werte beizubehalten, die als f-Werte ausgedrückt werden. Werte, die als Dezimalzahlen dargestellt werden, können in einen f-Wert konvertiert und auf diese Weise gespeichert werden. Eine Anwendung ist berechtigt, intern generierte Werte in jeder geeigneten Einheit aufzuzeichnen. ein aus einem vorhandenen Dokument eingelesener Wert muss jedoch entweder mit der vollständigen ursprünglichen Genauigkeit beibehalten oder in einen f-Wert konvertiert werden.

Wenn die Implementierung dies nicht kann, muss sie den Benutzer warnen, dass Daten verloren gehen können. (Es ist akzeptabel, eine solche Warnung einmal auszugeben, wenn extern generierte Daten zum ersten Mal gefunden werden.)

Wenn ein Dezimalwert in das f-Format konvertiert wird, kann die Implementierung einen beliebigen arithmetischen Rundungsmodus verwenden. eine ganze Zahl muss jedoch genau in das f-Format konvertiert werden. Es wird empfohlen, dass Implementierungen konvertiert werden, indem sie auf minus unendlich gerundet werden, und dass die Konvertierung immer genau ist.

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="ordinate"></a>Koordinieren


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



Die Einheiten des Koordinatensystems, die von coord eingerichtet werden, sind von einem nominalen Typ, der als "15" bezeichnet wird. Dies ist ein Maß für die Länge, wird jedoch nur in Bezug auf das Rechteck verwendet, das durch das Coord eingerichtet wird. Jeder Wert vom Typ "ordinate" wird anhand der *w-* und *h-Werte* des Koords und des resultierenden Verhältnisses skaliert, das verwendet wird, um eine echte Messung auf dem Ausgabegerät einzurichten.

Eine konforme Implementierung muss in der Lage sein, Werte von bis zu 30 Bit plus Vorzeichen (d.h. eine 31-Bit-Ganzzahl mit Vorzeichen, keine 32-Bit-Ganzzahl mit Vorzeichen) zu verarbeiten. Es wird jedoch empfohlen, dass Implementierungen versuchen, Koordinaten für Pfad- und ähnliche Elemente mit einer Genauigkeit von etwa 16 Bits zu erzeugen. Dadurch wird die Wahrscheinlichkeit eines Unterlaufs oder Überlaufs in einer nicht konformen Implementierung minimiert.

-Werte sind immer integral. Ein Dezimaltrennzeichen wird möglicherweise nicht in einem Wert vom Typ "vererkt" angezeigt. Es dürfen keine Einheitenspezifizierer an Werte vom Typ "Spezifizierer" angefügt werden.

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="length"></a>length


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



Eine Länge ist eine reale Messung oder manchmal eine Messung in Gerätepixeln. Es wird empfohlen, dass Implementierungen die Verwendung von Gerätepixeln (px) vermeiden.

Alle [STANDARDMÄßIGEN CSS1-Einheitenqualifizierer](https://www.w3.org/pub/WWW/TR/REC-CSS1) sind mit einer Länge zulässig. Darüber hinaus kann die Qualifiziereremulator-Emulator verwendet werden. Dieser Qualifizierer bezieht sich auf eine Einheit , die EWU (English Metric Unit), die ein gemeinsamer Nenner der Maßmengen ist, die in Computergrafiken weit verbreitet sind. Die EMU ist inch/914400, d.h. es gibt 914400 EMU pro Zoll. <sup></sup> In der folgenden Tabelle ist die Anzahl der EMUs in einer kleinen Anzahl häufig auftretender Einheiten aufgeführt.



| Anzahl der EMUs | Anzahl pro Zoll | Number per Millimeter | Beschreibung             |
|----------------|-----------------|-----------------------|-------------------------|
| 360            |                 | 0.01                  | Win32 HIMETRIC          |
| 12700          | 72              |                       | "point"                 |
| 635            | 1440            |                       | Win32 TWIP              |
| 762            | 1200            |                       | Drucker mit hoher Auflösung |



 

Bruchteile von EMUs sind nicht zulässig. Jede Messung muss als 32-Bit-Ganzzahl von EMUs mit Vorzeichen darstellbar sein – dies schränkt die Größe einer Messung auf 2348 Zoll ein – etwa 59 Meter oder 65 Meter. Da sich die Messungen immer auf die Größe eines Renderings auf einem Ausgabegerät mit nominaler Bildschirm- oder Seitengröße beziehen, liegen sie immer innerhalb dieses Bereichs.

Beachten Sie jedoch, dass die Darstellung für reale Messungen ungeeignet ist und dass an dem Ort, an dem diese aufgezeichnet werden (z. B. um die tatsächliche Größe eines Pfads aufzuzeichnen), eine andere Darstellung verwendet werden muss.

Eine konforme Implementierung ist erforderlich, um Werte beizubehalten, bei denen es sich um die genaue Anzahl von EMUs handelt. Auf andere Weise dargestellte Werte können in einen EMU-Wert konvertiert und auf diese Weise gespeichert werden. Eine Anwendung ist berechtigt, intern generierte Werte in jeder geeigneten Einheit aufzuzeichnen. Ein aus einem vorhandenen Dokument eingelesener Wert muss jedoch entweder mit voller ursprünglicher Genauigkeit beibehalten oder in einen EMU-Wert konvertiert werden.

Wenn die Implementierung dies nicht kann, muss sie den Benutzer warnen, dass Daten verloren gehen können. (Es ist akzeptabel, eine solche Warnung einmal auszugeben, wenn extern generierte Daten zum ersten Mal gefunden werden.)

In der Praxis werden physische Längen für relativ wenige Messungen in diesem Vorschlag verwendet. Die normalerweise wichtigsten Daten sind die Pfaddaten, die im Koordinatensystem codiert werden, das auf Formbasis durch Coord definiert wird.

### <a name="alternative-representations"></a>Alternative Darstellungen

Die Standardlängendarstellungen von HTML werden von [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) definiert. Relative Einheiten, mit Ausnahme des Pixels, sind in dem Kontext, in dem Längen in diesem Vorschlag verwendet werden, nicht sinnvoll und dürfen nicht verwendet werden. Wenn das Dokument die beabsichtigte Pixelgröße (Ziel) aufzeichnet, definiert dies die Übersetzung von Pixeln in EMU. Andernfalls sollte der von [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) definierte Standardwert von 90 dpi verwendet werden.

Mit Ausnahme von emu kann jeder Wert als Dezimalbruch angegeben werden. Wenn ein Dezimalwert in EMU konvertiert wird, kann die Implementierung einen beliebigen arithmetischen Rundungsmodus verwenden. (Die einzige Möglichkeit für eine Erstellungsanwendung, ein bestimmtes Ergebnis zu gewährleisten, besteht darin, sie in emu anzugeben.)

Wenn kein Einheitenspezifizierer in einem Längenwert angegeben wird, muss die Implementierung von emu ausgehen.

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="measure"></a>Kennzahl


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



Ein Measure ist eine Menge, die entweder eine [Länge](#length) oder ein [Bruchteil](#fraction)sein kann. Dies ähnelt den HTML- und CSS-Längenmessungen, die in vielen Fällen entweder physische Messungen oder Prozentsätze einer anderen Menge sein können. Wenn kein Einheitenspezifizierer angegeben wird, muss davon ausgegangen werden, dass es sich bei dem Wert um einen Dezimalbruch handelt (daher wird dieses Verhalten von fraction und nicht von length geerbt.)

Im Gegensatz zur Länge hat ein Pixelwert eine kontextdefinierte Bedeutung, sodass die Konvertierung in die Emulierung normalerweise ungeeignet ist. Es gibt drei mögliche grundlegende Darstellungen, die von der Implementierung verwaltet werden müssen (d. h., eine Darstellung kann nicht ohne Informationsverlust in eine andere konvertiert werden).

1.  Ein Bruchwert sollte im [Bruchformat](#fraction) beibehalten werden (ein "f"-Wert).
2.  Eine physische Länge sollte in EMU beibehalten werden.
3.  Ein Pixelwert sollte als ganze Anzahl von Pixeln beibehalten werden.

Bruchzahlen von Pixeln sind nicht zulässig.

### <a name="alternative-representations"></a>Alternative Darstellungen

Alle alternativen Darstellungen von [Bruch](#fraction) und [Länge](#length) sind zulässig.

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="angle"></a>angle


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



Die grundlegende Darstellung eines Winkels ist eine Anzahl von Grad, die um 2 6 (65536) multipliziert und als ganze Zahl gespeichert werden. Da der Koordinatenraum invertiert ist (die positive y-Achse ist herunter), ist ein Winkel im Uhrzeigersinn positiv. Eine konforme Implementierung ist erforderlich, um die vollständige Genauigkeit eines solchen Werts zu erhalten.

Eine Implementierung darf einen beliebigen Bereich für Winkel verwenden und darf einen Winkel normalisieren (z. B. bis -180 bis +180 oder 0 bis 360). Implementierungen müssen nicht konsistent sein. die integrale Darstellung eines Winkels darf jedoch den Bereich einer 32-Bit-Ganzzahl mit Vorzeichen nicht überschreiten.

Das Suffix fd wird verwendet, um diese Darstellung eines Winkels (Bruchgrad) zu identifizieren. Beachten Sie, dass sich dies von dem f-Suffix für einen dimensionslosen Bruch unterscheidet, obwohl identische arithmetische Brüche zur Unterstützung verwendet werden können. Der Standardwert für einen Winkelwert ist einfacher Grad, d. h. ein nicht skaliertes Wert. Dies kann auch mit dem Suffix " " (dem Gradsymbol) signalisiert werden. Die Verwendung dieses Codierungstyps hängt jedoch davon ab, dass eine geeignete Dokumentcodierung verwendet wird. Folglich wird das Suffix deg auch als Mittelwerte definiert. Der vollständige Satz möglicher Ausreichender ist wie folgt.



| Suffix       | Konvertierungsfaktor | Kommentare                               |
|--------------|-------------------|----------------------------------------|
| Fd           | 1                 | Interne Darstellung mit hoher Genauigkeit |
| none, deg,   | 65536             | Grad                                |
| rad          | 65536pi/180       | Radians                                |



 

### <a name="alternative-representations"></a>Alternative Darstellungen

Die Skalierungstransformation verfügt über Diskontinuitäten bei ungeraden Vielfachen von 45 . Daher ist es äußerst wichtig, dass die Konvertierung einer beliebigen unexact-Menge klar definiert ist. Aus diesem Grund wird die Arithmetik der Konvertierung so definiert, dass sie in Richtung Minus unendlich gerundet wird.

Da dies in einigen Implementierungen schwierig oder unmöglich garantiert werden kann, wird die Verwendung des folgenden Features als Level 3-Feature definiert:

1.  Ein beliebiger Bruchgradwert.
2.  Beliebiger Radianwert

Daher müssen werte qualifizierte fd- und nicht qualifizierte integrale Werte oder integrale Werte deg oder genau von einer konformen Implementierung der Ebene 0 behandelt werden. Andere Werte müssen dies nicht. Es wird dringend empfohlen, dass jede Implementierung die Konvertierung von einem Bruchgradwert in einen skalierten Gradwert (fd) genau verarbeitet. Dies kann ohne Gleitkommaunterstützung erfolgen.

Die genaueren Anforderungen für die Konvertierung unterscheiden fd von f.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="color"></a>color


```HTML
c
<!element c  %color;>
```



Farben sind ein wesentlicher Bestandteil moderner Computergrafiken. Der Vorschlag verwendet die festgelegten Methoden zum Angeben fester Farben. Farben in Diagrammen sind jedoch selten einfache statische Farben. sie werden häufig von anderen Elementen im Diagramm abgeleitet. Viele dieser Informationen sind sehr anwendungsspezifisch, daher bietet dieser Vorschlag zwei sehr grundlegende Mechanismen, um ein solches Verhalten anzugeben:

1.  Eine Farbe kann von einer anderen Farbe in derselben Form abgeleitet werden.
2.  Eine kleine Anzahl arithmetischer Operationen wird zum Ableiten oder Ändern einer Farbe definiert.

Der Prototyp-Formmechanismus ergänzt dies, indem Prototypen definiert werden können, von denen Farben geerbt werden können.


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



Ein Farbwert ist eine Obermenge der [CSS1-Farbdefinition.](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) Die Erweiterungen ermöglichen es, den RGB-Farbwert aus anderen Farben innerhalb der Form oder aus einem mit CSS1 definierten Gesamtfarbschema zu bestimmen.

Wenn der Wert eines Elements als Farbe  definiert ist, definiert der Inhalt eines Elements den Farbwert mit einem einzelnen Farbtoken, das optional durch eine arithmetische Operation für die entsprechende RGB-Farbe geändert wird.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

### <a name="color-units"></a>Farbeinheiten

Der vollständige Satz von Farbtoken stammt aus einer Vielzahl von Quellen: HTML, CSS1 und dieser Vorschlag. Sie werden wie folgt mithilfe der Notation von [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) oder der XPointer-Notation definiert, die für die XML-Verknüpfung definiert ist.

In den XPointer-Definitionen ist die Speicherortquelle das Element, das den Farbwert enthält, und der Ausdruck bezieht sich auf den gesamten Elementsatz der Form, als ob alle Basisprototypelemente mit der Form zusammengeführt worden wäre. Wenn das entsprechende Element nicht vorhanden ist, wird der Standardwert für dieses Element an seiner Stelle verwendet.



| Color            | Definition                                                                                                  | Ebene | Beschreibung                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name             | Siehe unten                                                                                                   | 0     | HTML-Farbname, wie in der folgenden Tabelle aufgeführt.                                                                                                                            |
| \#rr'gg'bb'      | \#rr'gg'bb'                                                                                                 | 0     | Standardmäßige CSS1/sRGB-Farbdarstellung mit Werten im Bereich 0,255, dargestellt mit jeweils zwei Hexadezimalziffern.                                                     |
| \#Rgb            | \#rrggbb                                                                                                    | 1     | Das CSS1-Formular wurde mit nur drei Hexadezimalziffern verkürzt.                                                                                                                   |
| rgb(r,g,b)       | \#(r) (g) (b)                                                                                                 | 1     | CSS1 rgb form; Die Elemente des rgb-Werts werden wie in [CSS1 definiert konvertiert.](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units)                                      |
| fill             | ancestor(1,shape)<br/> child(1, fill)<br/> child(1, color)<br/>                           | 1     | Die Vordergrundfüllfarbe der Form.                                                                                                                                   |
| fillBack         | ancestor(1,shape)<br/> child(1, fill)<br/> child(1, back)<br/> child(1, color)<br/> | 1     | Die Hintergrundfarbe der Formfüllung.                                                                                                                                   |
| line             | ancestor(1,shape)<br/> child(1, line)<br/> child(1, color)<br/>                           | 1     | Die Vordergrundlinienfarbe der Form.                                                                                                                                   |
| lineBack         | ancestor(1,shape)<br/> child(1, line)<br/> child(1,back) <br/> child(1, color)<br/> | 1     | Die Hintergrundlinienfarbe der Form.                                                                                                                                   |
| lineOrFill       | Zeile, Füllung                                                                                                  | 1     | Der Zeilenwert, wenn kein Standardwert festgelegt ist, andernfalls der Füllwert. Dadurch wird effektiv die Farbe zurückgegeben, die sich am Rand der Form befindet.                                           |
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



Wenn das Element pure/ in einem Farbwert angezeigt wird, ist dies ein Hinweis darauf, dass die Farbe nicht durch ein &lt; &gt; Dithermuster angedeutet werden sollte. Dies ist ein Feature der Ebene 1, das von einer konformen Implementierung nicht erfüllt werden muss. Die Bezeichnung ist wichtig für Grafiken, die auf Geräten mit mittlerer Auflösung angezeigt werden, z. B. Videoanzeigen, bei denen kleine Features (z. B. Linien) schlechte Aliase mit ditherierten Farben verursachen können. Auf Geräten wie Druckern, die normalerweise alle Farben mit Ausnahme der wenigen vollständigen Farben dithern, ist das Dithering normalerweise ausreichend, um dieses Problem zu vermeiden.

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

1.  Wenn gray/ angegeben ist, wird der RGB-Wert durch yyy ersetzt, wobei y der Luminanzwert (y) ist, der anhand des sRGB-Werts im Anschluss an &lt; &gt; ITU-r BT.709 berechnet wird. Diese Berechnung ist:
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
    | Schwarzweiss      | wenn c < p thenc := 0elsec := 255 |

    

     

    Wenn der berechnete Komponentenwert c 255 überschreitet, wird in jedem Fall 255 verwendet, und wenn er kleiner als 0 ist, wird 0 verwendet.

3.  Wenn INVERT128/ angegeben wird, wird der Wert 128 subtrahiert oder jeder Komponente hinzugefügt, je danach, ob die Komponente kleiner als &lt; &gt; 128 ist oder nicht.
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  Wenn invert/ angegeben wird, wird jede Komponente &lt; &gt; durch 255 abzüglich des Werts der Komponente ersetzt.
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

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

### <a name="picture-file-formats"></a>Bilddateiformate

Im Kontext dieses Vorschlags sind externe Daten immer entweder eine Bitmap oder eine Datei, die zum Erstellen einer Bitmap verwendet wird. Auf Renderebene 0 muss kein externes Bitmapformat unterstützt werden. Pfade können nur mit Volltonfarben gefüllt werden. Zum Rendern des vollständigen Satzes von Füllungen auf Renderebene 1 müssen Bitmaps unterstützt werden. Renderebene 1 enthält (nur) die folgenden Formate:

1.  JFIF, d.h. daten im ISO/IEC 10918-Format, die in eine Datei mit dem JFIF-Header eingebettet sind (die nach dem SOI-Maker als bestimmter APP0-Marker betrachtet werden können) und einschließlich (nur) des Bereichs der JPEG-Formate, die vom IJG v6-Code unterstützt werden.
2.  PNG, wie in der PNG-Version 1.0-Spezifikation definiert.

Renderebene 2 bietet auch Unterstützung für Folgendes:

-   GIF, wie durch die GIF-Spezifikation definiert, die von CompuServ im Jahr 1987 veröffentlicht wurde (normalerweise als "GIF87a" bezeichnet). GIF89a muss auch auf dieser Ebene unterstützt werden. Dies unterliegt der Einschränkung, dass die Daten keine Erweiterungsblöcke enthalten dürfen, die interpretiert werden müssen, um die Bitmap anzuzeigen, außer Grafiksteuerelementerweiterungenmitouta-Anforderung für Benutzereingaben oder eine Verzögerungszeit. Dadurch können Kommentare eingeschlossen werden, aber nicht die Nur-Text-Erweiterung. Eine Anwendung kann Anwendungserweiterungen (0x21, 0xFF) einfügen, aber gemäß der Terminologie dieses Vorschlags dürfen diese nur Bearbeitungs- und nicht Renderingdaten enthalten.

Jedes andere datenformat, das in der Grafik verwendet wird, erzwingt, dass diese Grafik mindestens die Bearbeitungsebene 3 und möglicherweise die Ebene 3 rendert (wenn die Daten zum Rendern der Grafik erforderlich sind). Einer Anwendung wird empfohlen, die unterstützten Formate zu veröffentlichen. beispielsweise unterstützt Microsoft Office die folgenden zusätzlichen Formate nativ und kann daher Bearbeitungsdaten in dieser Form schreiben:

1.  WMF – Windows Metadatei (Win 3.1-Format)
2.  EMF – Windows "erweiterte" Metadatei (Win32-Format)
3.  PICT – Mac OS QuickDraw PICT-Datei (alle Versionen, jedoch ohne QuickTime-Datensätze oder andere Erweiterungen)
4.  BMP : Windows Bitmapdateiformat, "os/2" (BITMAPCORE), BITMAPINFO, BITMAPV4 und BITMAPV5

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="vector"></a>Vektor


```HTML
v
<!element v "( #pcdata | p )*">
```



Ein Vektorgrafikpfad wird als pcdata codiert. Der Inhalt des v-Elements wird gemischt und enthält optional eine Vektorpfadbeschreibung, die mit p-Elementen parametrisiert wird.

[Zurück zur VML-Übersicht](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

