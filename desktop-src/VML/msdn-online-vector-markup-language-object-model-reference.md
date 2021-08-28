---
title: VML-Objektmodellreferenz
description: In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa8c608a60cbdb5af0fa5699fb1d458a5f18552
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884168"
---
# <a name="vml-object-model-reference"></a>VML-Objektmodellreferenz

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

In diesem Thema:

-   [Introduction (Einführung)](#introduction)
-   [Beispiel](#example)
-   [Einrichten von VML](#setting-up-vml)
-   [VML OM-Referenz](#vml-om-reference)
    -   [Shape-Element](#shape-element)
-   [Unterelemente des Shape-Elements](#subelements-of-the-shape-element)
    -   [Background-Element](#background-element)
    -   [Element "Extrusion"](#extrusion-element)
    -   [Fill-Element](#fill-element)
    -   [Group-Element](#group-element)
    -   [Imagedata-Element](#imagedata-element)
    -   [Path-Element](#path-element)
    -   [Shadow-Element](#shadow-element)
    -   [Skew-Element](#skew-element)
    -   [Stroke-Element](#stroke-element)
    -   [TextPath-Element](#textpath-element)
-   [Im VML-Objektmodell verwendete Datentypen](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a>Einführung

[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) ist eine textbasierte Sprache, die [XML](https://www.w3.org/TR/REC-xml.mdl) verwendet, um HTML zum Anzeigen von Vektorgrafikinformationen zu erweitern. Der VML-Dokumentobjektmodell (DOM) definiert eine programmgesteuerte Schnittstelle für die Bearbeitung der Dokumentelemente. Dadurch kann der Benutzer Vektorgrafiken dynamisch über eine plattform- und sprachneutrale Schnittstelle erstellen und ändern. Das VML-DOM entspricht der [Dokumentobjektmodell](https://www.w3.org/TR/REC-DOM-Level-1/) Spezifikation.

VML verwendet das [Shape-Element](#shape-element) als grundlegenden Baustein für Vektorgrafikbilder. Nachdem eine Form erstellt wurde, können Sie die Form über Attribute oder angefügte Unterelemente ändern. Um beispielsweise die Farbe einer Form zu ändern, weisen Sie dem **FillColor-Attribut** einen Farbwert zu.


```HTML
myshape.fillcolor = "red"
```



Einige der Attribute einer Form sind ebenfalls [Unterelemente](/windows) und verfügen über eigene Attribute, einschließlich der folgenden:

-   [Hintergrund](#background-element)
-   [Extrusion](#extrusion-element)
-   [Ausfüllen](#fill-element)
-   [Gruppe](#group-element)
-   [Imagedata](#imagedata-element)
-   [Path](#path-element)
-   [Shadow](#shadow-element)
-   [Neigen](#skew-element)
-   [Takt](#stroke-element)
-   [Textpath](#textpath-element)

Die VML OM verwendet mehrere [Datentypen,](/windows) um Parameter zu definieren. Datentypen mit dem Präfix "Vg" sind Enumerationen, und solche mit dem Präfix "IVg" sind Objekte. Klicken Sie hier, um eine Liste anzuzeigen. Kleinere Datentypen werden mit bestimmten Parametern aufgelistet.

## <a name="example"></a>Beispiel

Der folgende VBScript-Code zeigt, wie Sie eine einfache Form erstellen:


```HTML
        Set MyRect = Document.CreateElement("v:Rect")
        Set R = MyDiv.AppendChild(MyRect)
        R.Style.Position = "absolute"
        R.Style.Width = 20
        R.Style.Height = 20
        R.Style.Top = 50
        R.Style.Left = 50
        R.FillColor = "red"
```



Im obigen Beispiel wird eine Form mithilfe der Dokumentobjektmodell Methode **CreateElement** erstellt. Die Form ist eine vordefinierte VML-Rect-Form. Obwohl das Objekt vorhanden ist, kann es nicht Teil des Dokuments sein, bis es an das Dokument angefügt ist. Mithilfe der **AppendChild-Methode** wird rect zu einem untergeordneten Element eines **DIV-Elements** namens MyDiv. Einige minimale Stilattribute (**Position**, **Breite**, **Höhe**, **Top**, **Links**) werden festgelegt, um der Form eine bestimmte Größe zu geben. Schließlich wird eine Farbe mit dem **FillColor-Attribut** zugewiesen. Beachten Sie, dass jede Skriptsprache oder jede Sprache verwendet werden kann, die mit Dokumentobjektmodell Schnittstellen verwendet werden kann.

## <a name="setting-up-vml"></a>Einrichten von VML

Eine Implementierung von VML erfolgt über Microsoft Internet Explorer 5.0 oder höher. Um das Renderingobjekt ordnungsgemäß auf einer Webseite einzurichten, müssen die folgenden Ergänzungen vorgenommen werden:

1.  Das Schema muss im anfänglichen &lt; HTML-Tag wie folgt eingerichtet &gt; werden:
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  Das Renderingverhalten muss Teil des Dokumentstils sein:
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

Das folgende Beispiel zeigt eine HTML-Beispielwebseite, die ordnungsgemäß für VML eingerichtet wurde und die dynamische Erstellung einer Form zeigt.


```HTML
<HTML xmlns:v="urn:schemas-microsoft-com:vml">
<HEAD>
<STYLE>
v\:* { behavior: url(#default#VML); display:inline-block}
</STYLE>
<TITLE>VML Sample</TITLE>
</HEAD>
<BODY>
<DIV id="MyDiv"></DIV>
<SCRIPT ID="MYSCRIPT" LANGUAGE="VBScript">
<!--
Set MyRect = Document.CreateElement("v:Rect")
Set R = MyDiv.AppendChild(MyRect)
R.Style.Position = "absolute"
R.Style.Width = 20
R.Style.Height = 20
R.Style.Top = 50
R.Style.Left = 50
R.FillColor = "red"
-->
</SCRIPT>
</BODY>
</HTML>
```



Beachten Sie, dass in Betaversionen ein ActiveX-Objekttag und ein anderes Verhalten erforderlich waren.

## <a name="vml-om-reference"></a>VML OM-Referenz

Dieser Verweis definiert das [Shape-Element,](#shape-element) die Unterelemente und [die](/windows) [Datentypen,](/windows)die vom Objektmodell von VML verwendet werden.

### <a name="shape-element"></a>Shape-Element

Formen sind die Bausteine grafischer Bilder, die durch Vector Markup Language (VML) definiert werden. Die Form ist das Element der obersten Ebene, und mehrere Unterelemente helfen dabei, die Art der einzelnen Formen zu definieren.

VML stellt vordefinierte Formen bereit:

**Shape-Attribute**

-   **Arc**
-   **Kurve**
-   **Linie**
-   **Polylinie**
-   **Rect**
-   **RoundRect**



|   Unterelement           |    Beschreibung                                                                                                                                                                                                                                                                                                                                                                              |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Adj          | [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md). Eine durch Trennzeichen getrennte Liste von Zahlen, die die Parameter für die Führungsformeln sind, die den Pfad der Form definieren. Werte können weggelassen werden, um die Verwendung von Standardwerten zu ermöglichen. Es können bis zu 8 Anpassungswerte vorhanden sein.                                                                                                   |
| ALT          | Eine Zeichenfolge. Alternativer Text, der der Form zugeordnet ist. Wird für das nicht grafische Durchsuchen verwendet.                                                                                                                                                                                                                                                                                                 |
| Schaltfläche       | [VgTriState](msdn-online-vml-vgtristate.md). Zeigt das Schaltflächenverhalten beim Klicken an.                                                                                                                                                                                                                                                                                                 |
| BWMode       | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Bestimmt, wie Die Form in der Schwarz-Weiß-Ansicht in Apps oder beim Drucken auf Schwarz-Weiß-Druckern gerendert wird. Zu den Werten gehören: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**. Standard: **Automatisch.** |
| BWNormal     | VgBlackWhiteMode. Wenn BWMode auf Auto festgelegt ist, wird diese Eigenschaft zum Rendern der Form in normalem Schwarz-Weiß-Modus herangezogen. Zu den Werten gehören: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**. Standard: **Automatisch.**                                                |
| BWPure       | VgBlackWhiteMode. Wenn BWMode auf Auto festgelegt ist, wird diese Eigenschaft zum Rendern der Form in reinem B/W herangezogen. Zu den Werten gehören: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**. Standard: **Automatisch.**                                                              |
| ChildShapes  | IVgGroupShapes. Eine Auflistung anderer Formen in dieser Gruppe. Diese Auflistung unterstützt die Standardmethoden Length und Item.                                                                                                                                                                                                                                                       |
| Key (Schlüssel)    | [IVgColor](msdn-online-vml-ivgcolor.md). Ein Farbwert, der transparent ist und alles hinter der Form zeigt.                                                                                                                                                                                                                                                             |
| Control1     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Steuerungspunkt für Kurve.                                                                                                                                                                                                                                                                                                  |
| Control2     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Steuerungspunkt für Kurve.                                                                                                                                                                                                                                                                                                  |
| CoordOrigin  | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Die Koordinaten in der oberen linken Ecke des Containerrechtecks. Bereich von 0 bis unendlich.                                                                                                                                                                                                                               |
| CoordSize    | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Die Breite und Höhe des Koordinatenraums innerhalb des Referenzrechtecks dieser Form. Wenn sie nicht angegeben ist, entspricht sie der Breite und Höhe des Rechtecks. Bereich von 0 bis unendlich. Standardwert: "1000,1000".                                                                                               |
| EndAngle     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Endwinkel der Form.                                                                                                                                                                                                                                                                                          |
| Extrusion    | IVgExtrusion. Gibt den Objektwert derExtrusion für diese Form an. Weitere Informationen finden Sie im [Element "Extrusion".](msdn-online-vml-extrusion-element.md)                                                                                                                                                                                                                               |
| Füllung         | VgFillFormat. Gibt den Füllwert für diese Form an. Weitere [](msdn-online-vml-fill-element.md) Informationen finden Sie unter Fill-Element.                                                                                                                                                                                                                                                |
| Fillcolor    | [IVgColor](msdn-online-vml-ivgcolor.md). Die Primäre Farbe des Pinsels, der zum Ausfüllen des Pfads dieser Form verwendet werden soll.                                                                                                                                                                                                                                                                  |
| Gefüllt       | [VgTriState](msdn-online-vml-vgtristate.md). True gibt an, dass der Pfad, der die Form definiert, ausgefüllt wird. Standardmäßig wird es mit einer Volltonfarbe gefüllt, es sei denn, es gibt ein Fill-Unterelement, das komplexere Fülleigenschaften angibt. False gibt an, dass die Füllung transparent ist.                                                                                                           |
| Kippen         | VgFlipOrientation. Werte sind: X Y XY YX                                                                                                                                                                                                                                                                                                                                         |
| ForceDash    | [VgTriState](msdn-online-vml-vgtristate.md). Hinweis darauf, dass eine gestrichelte Kontur gerendert werden soll, wenn keine Linie und keine Füllung für eine Form vorhanden ist. Dieses Verhalten ist im Allgemeinen nützlich, um unsichtbare Formen in Bearbeitungsanwendungen sichtbar zu machen, sodass sie ausgewählt und bearbeitet werden können, z. B. in einer Bildkarte.                                                                 |
| Formeln     | IVgFormulas. Ein Array von Formeln, das eine Form definiert.                                                                                                                                                                                                                                                                                                                          |
| From         | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Startpunkt der Zeile.                                                                                                                                                                                                                                                                                                   |
| Href         | [Zeichenfolge](#data-types-used-in-the-vml-object-model). Die URL, zu der sie springen soll, wenn auf diese Form geklickt wird.                                                                                                                                                                                                                                                                                 |
| ImageData    | IVgImageData. Bildinformationen, wenn die Form ein Bild ist. Weitere Informationen finden Sie im ImageData-Element.                                                                                                                                                                                                                                                                       |
| OnEd         | [VgTriState](msdn-online-vml-vgtristate.md). Blendet alle Handles mit Ausnahme der oberen linken und unteren rechten Seite aus, wie in den Handles für ein gerades Segment.                                                                                                                                                                                                                             |
| Opacity      | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Die Deckkraft der gesamten Form. Eine Zahl zwischen 0,0 und 1,0.                                                                                                                                                                                                                                                           |
| Pfad         | IVgPath. Eine Zeichenfolge, die die Befehle enthält, die den Pfad definieren.                                                                                                                                                                                                                                                                                                                  |
| Punkte       | [IVgPoints](msdn-online-vml-ivgpoints-data-type.md). Eine Auflistung von Punkten, die eine Form definieren.                                                                                                                                                                                                                                                                                   |
| Drucken        | [VgTriState](msdn-online-vml-vgtristate.md). True gibt an, dass diese Form gedruckt werden soll.                                                                                                                                                                                                                                                                                        |
| Drehung     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Legt die Drehung der Form fest. Der Wert wird an den Formstil weitergegeben.                                                                                                                                                                                                                                              |
| Skalieren        | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Skalierung der Form.                                                                                                                                                                                                                                                                                                           |
| Shadow       | IVgShadow. Gibt den Schatten für diese Form an. Weitere [](msdn-online-vml-shadow-element.md) Informationen finden Sie im Shadow-Element.                                                                                                                                                                                                                                                        |
| Spt          | Reserviert.                                                                                                                                                                                                                                                                                                                                                                        |
| Startangle   | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Startwinkel der Form.                                                                                                                                                                                                                                                                                        |
| Stroke       | VgStrokeFormat. Weitere Informationen finden Sie unter Stroke-Element.                                                                                                                                                                                                                                                                                                                                  |
| StrokeColor  | [IVgColor](msdn-online-vml-ivgcolor.md). Die Primäre Farbe des Pinsels, der zum Strichen des Pfads dieser Form verwendet werden soll.                                                                                                                                                                                                                                                                |
| Streichelte      | [VgTriState](msdn-online-vml-vgtristate.md). True gibt an, dass der Pfad, der die Form definiert, gestrichelt wird.                                                                                                                                                                                                                                                                              |
| StrokeWeight | [VGLength](msdn-online-vml-vglength.md). Die Breite des Pinsels, der zum Strichen des Pfads verwendet werden soll. Liegt zwischen 0 und 1584.                                                                                                                                                                                                                                                           |
| Textpath     | IVgTextPath. Gibt das TextPath-Objekt der Form an. Weitere Informationen [finden Sie im TextPath-Element.](msdn-online-vml-textpath-element.md)                                                                                                                                                                                                                                  |
| To           | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Der Endpunkt der Zeile.                                                                                                                                                                                                                                                                                                        |
| Typ         | Eine Zeichenfolge. Typ der Form.                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a>Unterelemente des Shape-Elements

Die folgenden Unterelemente sind Teil des VML-Objektmodells.

-   [Hintergrund](#background-element)
-   [Extrusion](#extrusion-element)
-   [Ausfüllen](#fill-element)
-   [Gruppe](#group-element)
-   [Imagedata](#imagedata-element)
-   [Path](#path-element)
-   [Shadow](#shadow-element)
-   [Neigen](#skew-element)
-   [Takt](#stroke-element)
-   [Textpath](#textpath-element)

### <a name="background-element"></a>Background-Element

Beschreibt die Füllung des Hintergrunds einer Seite mithilfe von VML-Füllungen.


|   attribute        |   Beschreibung                                                                                                                                                                                      |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BWMode    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Bestimmt, wie Form in der Schwarz-Weiß-Ansicht in Anwendungen oder beim Drucken gerendert wird.                                     |
| BWNormal  | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Wenn BWMode auf Auto festgelegt ist, wird diese Eigenschaft zum Rendern der Form in normalem Schwarz/Weiß verwendet.                        |
| BWPure    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Wenn BWMode auf Auto festgelegt ist, wird diese Eigenschaft zum Rendern der Form in rein schwarz und weiß verwendet.                          |
| Füllung      | VgFillFormat. Gibt die Füllung für diese Form an. Weitere [Informationen finden](msdn-online-vml-fill-element.md) Sie unter Fill-Element.                                                             |
| Fillcolor | [IVgColor](msdn-online-vml-ivgcolor.md). Die Primäre Farbe des Pinsels, der zum Ausfüllen des Pfads dieser Form verwendet werden soll. Duplikat des Color-Werts im Fill-Element. Der Standardwert ist Weiß. |



 

### <a name="extrusion-element"></a>Extrusionselement

Beschreibt eine 3D-Extrusion der Form.

**Attribute**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>AutoRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. True gibt an, dass der Mittelpunkt der Drehung der Gruppe von 3D-Objekten (tatsächlich ist immer nur ein Objekt in der Gruppe) automatisch als Mittelpunkt der Gruppe bestimmt wird. Andernfalls wird sie durch die RotationCenter-Parameter bestimmt, die einen Bruchteil der Form mit 0,0,0 als Mittelpunkt sind.</td>
</tr>
<tr class="even">
<td>BackDepth</td>
<td><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>. Umfang der Abwärtsextrusion. Liegt zwischen 0 und 32767.</td>
</tr>
<tr class="odd">
<td>Brightness</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Gesamtstärke der Szene. Der Standardwert &quot; ist 20.000 &quot; .</td>
</tr>
<tr class="even">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Die Farbe derExtrusion. Wird nur verwendet, wenn ColorMode auf Benutzerdefiniert festgelegt ist. Andernfalls legt Auto die Farbe desExtrusionseffekts auf die gleiche wie FillColor fest.</td>
</tr>
<tr class="odd">
<td>ColorMode</td>
<td>Vg3DColorMode. Gültige Werte:
<ul>
<li>Auto (Standard)</li>
<li>Benutzerdefiniert</li>
</ul></td>
</tr>
<tr class="even">
<td>Diffusity</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Das Verhältnis von Incident zu diffus reflektierten Licht. Werte kleiner als 1,0 sind normal, aber Werte, die höher als 1 sind, können interessante Effekte erzeugen.</td>
</tr>
<tr class="odd">
<td>Microsoft Edge</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Legt die Größe einer simulierten gerundeten Kante fest. Liegt zwischen 0 und 32767 in Gleitkomma pts. Der Standardwert ist &quot; &quot; 1pt.</td>
</tr>
<tr class="even">
<td>Facet</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Legt das Facet der Szene fest. Der Standardwert &quot; ist 30.000. &quot;</td>
</tr>
<tr class="odd">
<td>ForeDepth</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Menge der Forwardextrusion. Liegt zwischen 0 und 32767.</td>
</tr>
<tr class="even">
<td>LightFace</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Gibt an, ob die Vorderseite des Objekts auf Änderungen in der 3D-Beleuchtung reagiert, z. B. wenn sich ein Objekt dreht.</td>
</tr>
<tr class="odd">
<td>LightHarsh</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Beleuchten der Beleuchtung für die primäre Lichtquelle. Der Standardwert lautet False.</td>
</tr>
<tr class="even">
<td>LightHarsh2</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Glühbirnenlicht für die sekundäre Lichtquelle. Der Standardwert lautet False.</td>
</tr>
<tr class="odd">
<td>LightLevel</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>. Intensität der primären Lichtquelle. Der Standardwert ist &quot; 38000. &quot;</td>
</tr>
<tr class="even">
<td>LightLevel2</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>. Intensität der sekundären Lichtquelle. Der Standardwert ist &quot; 38000. &quot;</td>
</tr>
<tr class="odd">
<td>LightPosition</td>
<td>Vector3d. Position der primären Lichtquelle. Der Standardwert &quot; ist 50000,0,10000 &quot; .</td>
</tr>
<tr class="even">
<td>LightPosition2</td>
<td>Vector3d. Position der sekundären Lichtquelle. Der Standardwert &quot; ist -50000,0,10000 &quot; .</td>
</tr>
<tr class="odd">
<td>LockRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. &quot;Lockrotationcenter bedeutet, dass die Drehung der Gruppe durch Drehwinkel[1] Grad um die y-Achse auf der Seite definiert ist, gefolgt von Drehwinkel[0] Grad um die &quot; x-Achse. Wenn LockRotationCenter false ist, wird die Drehung als Ausrichtungswinkel grad um den durch die Ausrichtung definierten Vektor definiert. Beispielsweise entspricht lockrotationcenter=false orientationangle=45 orientation=(0,1,0) lockrotationcenter=true rotationangle=(0,45).</td>
</tr>
<tr class="even">
<td>Metallisch</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Bewirkt, dass das spiegelnde Licht die Materialfarbe und nicht die Lichtquellenfarbe ist, wodurch das Objekt farbig erscheint.</td>
</tr>
<tr class="odd">
<td>Ein</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Schaltet die Anzeige desExtrusionseffekts ein und aus.</td>
</tr>
<tr class="even">
<td>Orientation</td>
<td>Vector3d. Ausrichtung der Kamera.</td>
</tr>
<tr class="odd">
<td>OrientationAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Winkel zwischen der Ausrichtung der Kamera und der XY-Ebene.</td>
</tr>
<tr class="even">
<td>Ebene</td>
<td>Vg3DExtrudePlane. Ermöglicht dieExtrusion von orthogonalen Ebenen zur Bildschirmebene. Erfordert, dass ForeDepth und BackDepth in Zeicheneinheiten anstelle von Emus angegeben werden. Gültige Werte:
<ul>
<li>XY</li>
<li>ZX</li>
<li>YZ</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rendern</td>
<td>Vg3DRenderMode. Gültige Werte:
<ul>
<li>Solid (Standard)</li>
<li>Drahtmodell</li>
<li>BoundingCube</li>
</ul></td>
</tr>
<tr class="even">
<td>RotationAngle</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. AngleX, AngleY oder AngleZ wird durch das ShapeRotation-Attribut gesteuert.</td>
</tr>
<tr class="odd">
<td>RotationCenter</td>
<td>Vector3d. Mittelpunkt der Drehung.</td>
</tr>
<tr class="even">
<td>Glanz</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Bestimmt, wie konzentriert oder verteilt die spiegelförmige Reflektion ist. Ein hoher Wert wäre 8 bis 10 und würde einem Spiegel ungefähren, und ein niedriger Wert wäre 2 bis 3 und würde der Verhedung von Bekleidung ungefähren. Werte von 3 bis 7 werden empfohlen. Hohe Werte spiegeln punktgenaue Lichtquellen wider.</td>
</tr>
<tr class="odd">
<td>SkewAmt</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>. Wenn Type auf Parallel festgelegt ist, bestimmt das Attribut die Menge der Schiefe. Liegt zwischen 0 und 100.</td>
</tr>
<tr class="even">
<td>SkewAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Wenn Type auf Parallel festgelegt ist, bestimmt das Attribut den Grad der Schiefe. Der Standardwert ist &quot; -45. &quot;</td>
</tr>
<tr class="odd">
<td>Specularity</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Das Verhältnis zwischen Vorfall und spiegelnd reflektierten Lichten. Werte kleiner als 1,0 sind normal, aber Werte, die höher als 1 sind, können interessante Effekte erzeugen.</td>
</tr>
<tr class="even">
<td>Typ</td>
<td>VgExtrusionType. Gültige Werte:
<ul>
<li>Parallel (Standard)</li>
<li>Perspektive</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sicht</td>
<td>Vector3d. Der Punkt, von dem aus die Szene angezeigt wird.</td>
</tr>
<tr class="even">
<td>ViewpointOrigin</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Kann Werte von 0,5 bis -0,5 haben, um den Ursprung des Blickpunkts innerhalb des Umrandungsfelds der Form zu positionieren.</td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a>Fill-Element

Beschreibt, wie ein Pfad für Füllungen ausgefüllt werden soll, die komplexer als eine Volltonfarbe sind.

**Attribute**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>AlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Richten Sie das Bild an der Form aus. False gibt an, dass das Bild mit dem Fenster ausgerichtet wird.</td>
</tr>
<tr class="even">
<td>Angle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Der Winkel, entlang dem der Farbverlauf verläuft. 0 Grad liegt entlang der horizontalen Achse von links nach rechts.</td>
</tr>
<tr class="odd">
<td>Aspekt</td>
<td><strong>VgAspectType</strong>. Das ImageSize-Attribut wird angepasst, um den Aspekt des Bilds zu erhalten. Mögliche Werte:
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignorieren</td>
<td>Ignorieren von Aspektproblemen.</td>
</tr>
<tr class="even">
<td>Atleast</td>
<td>Das Bild ist mindestens so groß wie die Bildgröße.</td>
</tr>
<tr class="odd">
<td>AtMost</td>
<td>Das Bild ist nicht größer als die Bildgröße.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> Die Hauptfüllfarbe. Identisch mit dem FillColor-Attribut in Form.</td>
</tr>
<tr class="odd">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Die sekundäre Farbe für eine Füllung, wenn der Bildtyp Muster oder eine Farbverlaufsfüllung ist.</td>
</tr>
<tr class="even">
<td>Farben</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>. Zwischenfarben im Farbverlauf und ihre relativen Positionen entlang des Farbverlaufs, z. B. &quot; 30 % Rot, 70 % Blau, 90 % &quot; Grün. Primäre Farbe (Farbattribut in Form) ist 0 % und sekundäre Farbe (Color2-Attribut) 100 %.</td>
</tr>
<tr class="odd">
<td>Fokus</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>. Fokuspunkt für lineare Farbverlaufsfüllung. Die Werte liegen zwischen -100 und +100.</td>
</tr>
<tr class="even">
<td>FocusPosition</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Position des innersten Rechtecks für radiale Farbverläufe. Der Vektor ist ein Bruchteil (0,0 bis 1,0) der Breite und Höhe der Form.</td>
</tr>
<tr class="odd">
<td>FocusSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Größe des innersten Rechtecks für radiale Farbverläufe. Der Vektor ist ein Bruchteil (0,0 bis 1,0) der Breite und Höhe der Form.</td>
</tr>
<tr class="even">
<td>Methode</td>
<td>VgSigmaType. Mögliche Werte:
<ul>
<li>Keine</li>
<li>Linear</li>
<li>Sigma</li>
<li>Any</li>
</ul>
<p>Der Standardwert ist Sigma.</p></td>
</tr>
<tr class="odd">
<td>Ein</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Aktiviert die Füllanzeige. Identisch mit dem Fill-Attribut in Form.</td>
</tr>
<tr class="even">
<td>Opacity</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Deckkraft der Füllung.</td>
</tr>
<tr class="odd">
<td>Deckkraft2</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Die sekundäre Deckkraft für Farbverläufe.</td>
</tr>
<tr class="even">
<td>Origin</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Zeigen Sie relativ zur oberen linken Ecke des Bilds, das als Ursprung des Bilds behandelt wird. Der Standardwert ist die Mitte des Images. Der Vektor ist ein Bruchteil (von 0,0 bis 1,0) der Breite und Höhe des Bilds.</td>
</tr>
<tr class="odd">
<td>Position</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Zeigen Sie auf das Verweisrechteck der Form, um den Ursprung des Bilds zu positionieren. Der Standardwert ist die Mitte des Containerrechtecks. Der Vektor ist ein Bruchteil (0,0 bis 1,0) der Breite und Höhe des Bilds.</td>
</tr>
<tr class="even">
<td>Size</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Die Größe des Bilds. Der Standardwert ist die Pixelgröße des Bilds. Kann in absoluten Koordinaten oder in Prozent angegeben werden.</td>
</tr>
<tr class="odd">
<td>Src</td>
<td><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge.</a> URL zu einem Bild, das für Bild- und Musterfüllungen geladen werden soll. Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird.</td>
</tr>
<tr class="even">
<td>Typ</td>
<td>VgFillType. Es kann sich um einen der folgenden Typen handeln:
<ul>
<li>Hintergrund</li>
<li>Frame</li>
<li>Farbverlauf</li>
<li>GradientCenter</li>
<li>GradientRadial</li>
<li>GradientTitle</li>
<li>GradientUnscaled</li>
<li>Muster</li>
<li>Basis</li>
<li>Tile</li>
</ul>
Für Kachel, Muster und Frame müssen die Bildattribute angegeben werden. Gradient und GradientRadial erfordern, dass die Farbverlaufsattribute bereitgestellt werden.</td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a>Group-Element

Eine Gruppe ist eine Sammlung einzelner Formen, die als Einheit positioniert und transformiert werden können.



|   attribute        |   BESCHREIBUNG                                                                                                                                                                                      |
|--------|----------------------------------------------------------------------------------------------|
| Element   | [IVgShape](#data-types-used-in-the-vml-object-model). Angegebenes Element im Array von Formen. |
| Länge | [Integer](#data-types-used-in-the-vml-object-model). Anzahl der Formen in dieser Gruppe.         |



 

### <a name="imagedata-element"></a>Imagedata-Element

Beschreibt ein Bild, das über einer Form gerendert werden soll.



|   attribute        |   Beschreibung                                                                                                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BiLevel     | [VgTriState](msdn-online-vml-vgtristate.md). Bild nur in zwei Farben anzeigen (in der Regel Schwarz und Weiß).                                                                                                                                                                                                                                                     |
| BlackLevel  | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Ermöglicht die Anpassung, die Ebene so festzulegen, dass Schwarz als echtes Schwarz angezeigt wird und alle anderen Farben als Schattierungen oberhalb von Schwarz sichtbar sind.                                                                                                                                                                        |
| Keykey   | [IVgColor](msdn-online-vml-ivgcolor.md). Transparente Farbe des Bilds.                                                                                                                                                                                                                                                                                         |
| CropBottom  | [VgNumber](#data-types-used-in-the-vml-object-model). Zuschneiden des Abstands vom unteren Rand des Bilds als Prozentsatz der Bildgröße.                                                                                                                                                                                                                           |
| CropLeft    | [VgNumber](#data-types-used-in-the-vml-object-model). Zuschneiden des Abstands vom linken Bildrand als Bruchteil der Bildgröße (von 0,0 bis 1,0). "Out-Cropping" wird jedoch unterstützt, und daher werden Werte von kleiner als 0 und größer als 1 unterstützt. Beispielsweise würde -5, 20 die Begrenzungen um das 25-fache der Bildgröße mit 4/5 auf einer Seite des Bilds ausschneiden. |
| CropRight   | [VgNumber](#data-types-used-in-the-vml-object-model). Zuschneiden des Abstands von der rechten Seite des Bilds als Prozentsatz der Bildgröße.                                                                                                                                                                                                                            |
| CropTop     | [VgNumber](#data-types-used-in-the-vml-object-model). Zuschneiden des Abstands vom oberen Rand des Bilds als Prozentsatz der Bildgröße.                                                                                                                                                                                                                              |
| EmbossColor | [IVgColor](msdn-online-vml-ivgcolor.md). Dies wird auf einen Prozentsatz der Schattenfarbe festgelegt, um einen einprägten Bildeffekt zu erstellen.                                                                                                                                                                                                                                 |
| Gewinnen        | [VgPositiveNumber](#data-types-used-in-the-vml-object-model). Passt die Intensität aller Farben an. Legt im Wesentlichen fest, wie hell weiß sein wird. Liegt zwischen 0 und 32767.                                                                                                                                                                                           |
| Gamma       | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Gammakorrektur. Durch erhöhen des Bilds erhalten Sie mehr Kontrast.                                                                                                                                                                                                                                           |
| GrayScale   | [VgTriState](msdn-online-vml-vgtristate.md). Bild in Graustufenfarben anzeigen.                                                                                                                                                                                                                                                                              |
| Src         | [Zeichenfolge](#data-types-used-in-the-vml-object-model). URL zu einem Bild, das für Bild- und Musterfüllungen geladen werden soll. Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten verweisen, damit ein Bild angezeigt wird.                                                                                                                                                           |



 

### <a name="path-element"></a>Path-Element

Definiert den Pfad, aus dem die Form besteht, mithilfe einer Zeichenfolge, die einen umfangreichen Satz von "Stiftbewegungsbefehlen" enthält.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Limo</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>. Definiert den Punkt, an dem die Form gestreckt wird. Beispielsweise würde sich der Strichpunkt für eine Form des Strichs auf dem Hängen befindet, sodass sich bei einer Größenänderung der Strich gestreckt wird und der Rest der Form seine Abmessungen beibehält.</td>
</tr>
<tr class="even">
<td>TextBoxRect</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>. Array, das die Rechtecke enthält, die definieren, wohin Text gehen soll.</td>
</tr>
<tr class="odd">
<td>V</td>
<td><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>. Entspricht dem v-Attribut im Path-Tag. Beachten Sie, dass der Pfad dem Path-Attribut oder -Element entsprechen kann.</td>
</tr>
<tr class="even">
<td>Wert</td>
<td><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>. Eine Textdarstellung der Befehle, die den Pfad definieren. X- oder y-Koordinatenwerte können ein Verweis auf eine Formel in der Form &quot; @# &quot; sein, wobei # die Ordnungszahl der Formel ist, z. &quot; @2 &quot; B. . Diese Attributzeichenfolge besteht aus einem umfangreichen Satz von Befehlen, einschließlich der folgenden: <br/> 
<table>
<thead>
<tr class="header">
<th>Befehl</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ae (angleellipseto)</td>
<td><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong><br/> Zeichnen eines Segments einer Ellipse. Eine gerade Linie wird vom aktuellen Punkt bis zum Anfangspunkt des Segments gezeichnet.<br/></td>
</tr>
<tr class="even">
<td>al (angleelipse)</td>
<td>Identisch mit ae, außer dass ein implizites m zum Anfangspunkt des Segments vorhanden ist.</td>
</tr>
<tr class="odd">
<td>ar (arc)</td>
<td>Identisch mit at. Ein neuer Unterpfad wird jedoch durch ein impliziertes m bis zum Anfangspunkt des Bogens gestartet.</td>
</tr>
<tr class="even">
<td>at (arcto)</td>
<td><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y) <br/> Die ersten vier Werte definieren den Begrenzungsfeld einer Ellipse. Die letzten vier definieren zwei radiale Vektoren. Ein Segment der Ellipse wird gezeichnet, das mit dem durch den Startradiusvektor definierten Winkel beginnt und am durch den Endvektor definierten Winkel endet. Eine gerade Linie wird vom aktuellen Punkt bis zum Anfang des Bogens gezeichnet. Der Bogen wird immer gegen den Uhrzeigersinn gezeichnet. <br/></td>
</tr>
<tr class="odd">
<td>c (curveto)</td>
<td><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>bis</strong>(x,y) <br/> Zeichnen Sie eine kubische Bézierkurve vom aktuellen Punkt bis zur Koordinate, die von den letzten beiden Parametern angegeben wird, den Kontrollpunkten, die von den ersten vier Parametern angegeben werden. Der aktuelle Punkt wird zum Endpunkt des Bézierers.<br/></td>
</tr>
<tr class="even">
<td>e (ende)</td>
<td>Beenden Sie den aktuellen Satz von Unterpfaden. Eine bestimmte Gruppe von Unterpfaden (durch Ende getrennt) wird mit eofill aufgefüllt. Nachfolgende Gruppen von Unterpfaden werden unabhängig aufgefüllt und vorhandenen überlagert.</td>
</tr>
<tr class="odd">
<td>l (lineto)</td>
<td>x,y<br/> Zeichnen Sie eine Linie vom aktuellen Punkt zur angegebenen x,y-Koordinate, die zum neuen aktuellen Punkt wird. Zusätzliche Koordinatenpaare können angegeben werden, um eine Polylinie zu bilden, z.B. &quot; l 10,13,45,27,89,-12 &quot; .<br/></td>
</tr>
<tr class="even">
<td>m (moveto)</td>
<td>x,y<br/> Starten Sie einen neuen Unterpfad an der angegebenen x,y-Koordinate.<br/></td>
</tr>
<tr class="odd">
<td>nf (nofill)</td>
<td>Der aktuelle Satz von Unterpfaden (durch Ende getrennt) wird nicht ausgefüllt.</td>
</tr>
<tr class="even">
<td>ns (nostroke)</td>
<td>Der aktuelle Satz von Unterpfaden (durch Ende getrennt) wird nicht strichen.</td>
</tr>
<tr class="odd">
<td>qb (quadraticbezier)</td>
<td>(<strong>Kontrollpunkt</strong>(x, y))*,<strong>end</strong>(x,y) <br/> Definiert eine oder mehrere quadratische Bézierkurven mithilfe von Kontrollpunkten und einem Endpunkt. Zwischenpunkte (on-curve) werden durch Interpolation zwischen aufeinander folgenden Kontrollpunkten abgerufen, ähnlich wie TrueType-Schriftarten. Der Unterpfad muss kein Startpfad sein. In diesem Fall wird der Unterpfad geschlossen, und der letzte Punkt definiert den Startpunkt.<br/></td>
</tr>
<tr class="even">
<td>qx (ellipticalquadrantx)</td>
<td><strong>end</strong>(x,y) <br/> Eine Quartalsellipse wird vom aktuellen Punkt zum angegebenen Endpunkt gezeichnet. Das elliptische Segment ist anfänglich tangential zu einer Linie parallel zur x-Achse; Das heißt, das Segment beginnt horizontal.<br/></td>
</tr>
<tr class="odd">
<td>qy (ellipticalquadranty)</td>
<td><strong>end</strong>(x,y) <br/> Identisch mit qx, außer dass das elliptische Segment anfänglich tangential zu einer Linie parallel zur y-Achse ist; Das heißt, das Segment beginnt vertikal.<br/></td>
</tr>
<tr class="even">
<td>r (rlineto)</td>
<td>x,y <br/> Zeichnen Sie eine Linie vom aktuellen Punkt zur relativen Koordinate (cpx + x, cpy + y). Wenn zusätzliche Koordinatenpaare angegeben werden, wird jeder neue Punkt relativ zum letzten berechnet.<br/></td>
</tr>
<tr class="odd">
<td>t (rmoveto)</td>
<td>x,y<br/> Starten Sie einen neuen Unterpfad an den relativen Koordinaten ( cpx + x, cpy + y), wobei cpx, cpy die aktuelle Position ist. <br/></td>
</tr>
<tr class="even">
<td>v (curveto)</td>
<td><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>bis</strong> (x,y) <br/> Kubische Bézierkurve mit den angegebenen Koordinaten relativ zum aktuellen Punkt. Alle Punkte werden relativ zum gleichen Ausgangspunkt berechnet.<br/></td>
</tr>
<tr class="odd">
<td>wa (clockwisearcto)</td>
<td>Identisch mit at, aber der Bogen wird im Uhrzeigersinn gezeichnet.</td>
</tr>
<tr class="even">
<td>wr (clockwisearc)</td>
<td>Entspricht ar, wird aber im Uhrzeigersinn gezeichnet.</td>
</tr>
<tr class="odd">
<td>x (schließen)</td>
<td>Schließen Sie den aktuellen Unterpfad, indem Sie eine gerade Linie vom aktuellen Punkt zum ursprünglichen Moveto-Punkt zeichnen.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a>Shadow-Element

Beschreibt einen Schatteneffekt auf eine Form.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Farbe des primären Schattens. Der Standardwert ist RGB(128,128,128)</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Farbe des zweiten Schattens oder Hervorhebung in einem eingeblendeten oder eingeblendeten Schatten. Der Standardwert ist RGB(203,203,203).</td>
</tr>
<tr class="odd">
<td>Matrix</td>
<td><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>. Eine perspektivische Transformationsmatrix im Format &quot; sxx,sxy,syx,syy,px,py &quot; [s=scale, p=perspective]. Die Elemente s geben an, wie der Schatten in Bezug auf die Form skaliert werden soll, und die p-Elemente geben an, wie der Schatten in Bezug auf die Form schief werden soll. Beispielsweise wird die Größe der Form durch die folgende Matrix um den Faktor 2 geändert und um den Faktor 4 in alle Richtungen verzerrt: <br/> &quot;2,2,2,2,4,4&quot;<br/> Diese Matrix wird nur verwendet, wenn der Typ des Schattens auf perspective festgelegt ist.<br/></td>
</tr>
<tr class="even">
<td>Verdeckt</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Der Schatten kann über sichtbar sein, wenn keine Füllung auf der Form vorhanden ist. Der Standardwert lautet False.</td>
</tr>
<tr class="odd">
<td>Offset</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>. Die Menge des x,y-Offsets von der Position der Form. Der Standardwert ist &quot; 2pt,2pt. &quot;</td>
</tr>
<tr class="even">
<td>Offset2</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Menge des x,y-Sekundenoffsets von der Position der Form. Werte sind entweder eine absolute Messung oder ein Bruchteilwert der Form (-0,5 bis +0,5).</td>
</tr>
<tr class="odd">
<td>Ein</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Aktiviert und deaktiviert die Anzeige des Schattens.</td>
</tr>
<tr class="even">
<td>Opacity</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Deckkraft des Schatteneffekts.</td>
</tr>
<tr class="odd">
<td>Origin</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Ein Paar von Bruchwerten der Form von -0,5 bis +0,5.</td>
</tr>
<tr class="even">
<td>Typ</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>. Gültige Werte:
<ul>
<li>Single (Standard)</li>
<li>Double</li>
<li>Perspektive</li>
<li>ShapeRelative</li>
<li>DrawingRelative</li>
<li>Emboss</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a>Skew-Element

Beschreibt einen perspektivische Schiefe-Effekt auf eine Form. Die Schiefe wird auf Vektorgrafikdaten angewendet, nicht auf Bilddaten.



|   attribute        |   Beschreibung                                                                                                                                                                                      |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Matrix | [IVgSkewMatrix](#data-types-used-in-the-vml-object-model). Eine perspektivische Transformationsmatrix im Format "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective \] . Wenn offset in absoluten Einheiten vorliegt, sind px,py in emul ^ -1 Einheiten; andernfalls sind sie ein umgekehrter Bruchteil der Formgröße. |
| Offset | [IvgSkewOffset](#data-types-used-in-the-vml-object-model). Die Menge des x,y-Offsets von der Position der Form. Der Standardwert ist "2pt,2pt".                                                                                                                                                   |
| Ein     | [VgTriState](msdn-online-vml-vgtristate.md). Aktiviert oder deaktiviert die Anzeige der Schiefe.                                                                                                                                                                                             |
| Origin | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Ein Paar von Bruchwerten der Form von -0,5 bis +0,5.                                                                                                                                                                     |



 

### <a name="stroke-element"></a>Stroke-Element

Beschreibt, wie der Pfad gezeichnet wird, wenn etwas außerhalb einer durchgezogenen Linie mit einer Volltonfarbe gewünscht wird.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Color</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Die Farbe der Linie. Entspricht dem StrokeColor-Attribut in Shape, überschreibt es jedoch.</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Sekundäre Farbe. Wird verwendet, wenn FillType pattern ist.</td>
</tr>
<tr class="odd">
<td>Dashstyle</td>
<td><strong>VgLineDashStyle</strong>. Format des Bindestrichformats. Kann ein bestimmter Wert oder eine Sequenz von Zahlen mit einem benutzerdefinierten Bindestrichmuster sein. Gültige Werte:
<ul>
<li>Solid (Standard)</li>
<li>ShortDash</li>
<li>ShortDot</li>
<li>ShortDashDot</li>
<li>ShortDashDotDot</li>
<li>Punkt</li>
<li>Strich</li>
<li>DashDot</li>
<li>LongDash</li>
<li>LongDashDot</li>
<li>LongDashDotDot</li>
</ul></td>
</tr>
<tr class="even">
<td>EndArrow</td>
<td><strong>VgArrowheadStyle</strong>. Pfeilspitze für das Ende der Zeile. Gültige Werte:
<ul>
<li>Keine (Standard)</li>
<li>Blockieren</li>
<li>Klassisch</li>
<li>Diamond</li>
<li>Oval</li>
<li>Öffnen</li>
<li>Chevron</li>
<li>DoubleChevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>EndArrowLength</td>
<td><strong>VgArrowHeadLength</strong>. Pfeilkopflänge für das Ende der Zeile. Gültige Werte:
<ul>
<li>Short</li>
<li>Mittel (Standard)</li>
<li>Long</li>
</ul></td>
</tr>
<tr class="even">
<td>EndArrowWidth</td>
<td><strong>VgArrowheadWidth</strong>. Pfeilkopfbreite für das Ende der Zeile. Gültige Werte:
<ul>
<li>Schmalen</li>
<li>Mittel (Standard)</li>
<li>Breite</li>
</ul></td>
</tr>
<tr class="odd">
<td>Endcap</td>
<td><strong>VgLineEndCapStyle</strong>. Gültige Werte:
<ul>
<li>Flach</li>
<li>Square</li>
<li>Round</li>
</ul></td>
</tr>
<tr class="even">
<td>FillType</td>
<td><strong>VgLineFillType</strong>. Gültige Werte:
<ul>
<li>Solid (Standard)</li>
<li>Tile</li>
<li>Muster</li>
<li>Frame</li>
</ul></td>
</tr>
<tr class="odd">
<td>ImageAlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Richten Sie das Bild an der Form aus. Wenn false, richten Sie das Bild am Fenster aus.</td>
</tr>
<tr class="even">
<td>ImageAspect</td>
<td><strong>VgAspectType</strong>. Das ImageSize-Attribut wird angepasst, um den Aspekt des Bilds beizubehalten. Mögliche Werte:
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignorieren</td>
<td>Ignorieren sie Aspektprobleme.</td>
</tr>
<tr class="even">
<td>Atleast</td>
<td>Das Bild ist mindestens so groß wie die Bildgröße.</td>
</tr>
<tr class="odd">
<td>AtMost</td>
<td>Das Bild ist nicht größer als die Bildgröße.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>Imagesize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Größe des Bilds, mit dem der Pinsel formt werden soll. Der Standardwert ist die Größe des Bilds.</td>
</tr>
<tr class="even">
<td>JoinStyle</td>
<td><strong>VgLineJoinStyle</strong>. Gültige Werte:
<ul>
<li>Rund (abgerundetes Fugen)</li>
<li>Abrägung (Abrägung)</li>
<li>Miter (Miter-Joint)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Linestyle</td>
<td><strong>VgLineStyle</strong>. Gültige Werte:
<ul>
<li>Eine</li>
<li>ThinThin (1:1:1)</li>
<li>ThinThick (1:1:2)</li>
<li>ThickThin (2:1:1)</li>
<li>ThickBetweenThin (1:1:2:1:1)</li>
</ul></td>
</tr>
<tr class="even">
<td>MiterLimit</td>
<td><a href="msdn-online-vml-vglength.md">Länge</a>. Der maximale Abstand zwischen dem inneren punkt und dem äußeren Punkt eines Fugens. Diese Zahl ist ein Vielfaches der Linienstärke. Reicht von 0 bis 32.767.</td>
</tr>
<tr class="odd">
<td>Ein</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Aktiviert und deaktiviert die Anzeige der Zeile. Entspricht dem Stroke-Attribut in Shape, überschreibt es jedoch.</td>
</tr>
<tr class="even">
<td>Opacity</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Deckkraft des Strichs.</td>
</tr>
<tr class="odd">
<td>Src</td>
<td>Eine Zeichenfolge. URL zu einem Bild, das für Bild- und Musterfüllungen geladen werden soll. Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird.</td>
</tr>
<tr class="even">
<td>StartArrow</td>
<td><strong>VgArrowheadStyle</strong>. Pfeilspitze für den Anfang der Zeile. Gültige Werte:
<ul>
<li>Keine (Standard)</li>
<li>Blockieren</li>
<li>Klassisch</li>
<li>Diamond</li>
<li>Oval</li>
<li>Öffnen</li>
<li>Chevron</li>
<li>DoubleChevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>StartArrowLength</td>
<td>VgArrowHeadLength. Pfeilspitzenlänge für den Anfang der Zeile. Gültige Werte:
<ul>
<li>Short</li>
<li>Mittel (Standard)</li>
<li>Long</li>
</ul></td>
</tr>
<tr class="even">
<td>StartArrowWidth</td>
<td>VgArrowheadWidth. Die Pfeilspitzenbreite für den Anfang der Linie. Gültige Werte:
<ul>
<li>Schmales Mittel (Standard) Breit</li>
</ul></td>
</tr>
<tr class="odd">
<td>Weight</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Breite der Linie. Liegt zwischen 0 und 1584.
<div class="alert">
<blockquote>
[!Note]<br />
Mit dem DashStyle-Attribut kann der Benutzer ein benutzerdefiniertes Bindestrichmuster angeben. Dies erfolgt mithilfe einer Reihe von Zahlen. Bindestrichformate werden in Bezug auf die Länge des Bindestrichs (den gezeichneten Teil des Strichs) und die Länge des Leerzeichens zwischen den Bindestrichen definiert. Die Längen sind relativ zur Linienbreite. eine Länge von &quot; 1 &quot; entspricht der Linienbreite. Der EndCap-Stil wird auf jeden Bindestrich angewendet, Pfeilstile nicht. Die Zeichenfolge definiert zuerst die Länge des Bindestrichs und dann die Länge des Leerzeichens. Dies kann wiederholt werden, um komplexe Bindestrichformate zu bilden. Die Zeichenfolge sollte immer ein Zahlenpaar enthalten. , wenn sie eine ungerade Anzahl von Zahlen enthält, kann die letzte ignoriert werden. In der folgenden Tabelle sind einige typische Werte und eine Beschreibung des beabsichtigten Effekts aufgeführt. &quot;0 impliziert einen Punkt, der vierfach symmetrisch sein sollte (mit runden &quot; Endcaps sollte er ein Kreis sein). Wenn das Zeilenendcap Flat ist, sollte ein Viewer nach Möglichkeit einen integrierten Betriebssystemstrich auswählen (d.h. etwas, das schnell gestrichelt werden kann). Im Folgenden finden Sie einige Beispiele.
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td>&quot;2 2&quot;</td>
<td>kurze Bindestriche (jeder Bindestrich und der Abstand dazwischen ist doppelt so breit wie die Linie)</td>
</tr>
<tr class="even">
<td>&quot;1 2&quot;</td>
<td>Punkt (jeder Bindestrich ist die Breite der Linie, während jedes Leerzeichen doppelt so breit wie die Linie ist)</td>
</tr>
<tr class="odd">
<td>&quot;4 2&quot;</td>
<td>Bindestrich (jeder Bindestrich ist viermal so breit wie die Linie, während jedes Leerzeichen doppelt so breit wie die Linie ist)</td>
</tr>
<tr class="even">
<td>&quot;8 2&quot;</td>
<td>long-dash</td>
</tr>
<tr class="odd">
<td>&quot;4 2 1 2&quot;</td>
<td>Bindestrichpunkt</td>
</tr>
<tr class="even">
<td>&quot;8 2 1 2&quot;</td>
<td>Long-Dash-Punkt</td>
</tr>
<tr class="odd">
<td>&quot;8 2 1 2 1 2&quot;</td>
<td>Punkt mit langem Strich</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a>TextPath-Element

Beschreibt einen Vektorpfad basierend auf den bereitgestellten Textdaten, Schriftarten und Stilen. Der Textpfad wird getauscht, damit er einem **Path-Element entspricht,** sofern angegeben.



|   attribute        |   Beschreibung                                                                                                                                                                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| FitPath  | [VgTriState](msdn-online-vml-vgtristate.md). Größe des Texts, um den Pfad zu füllen, auf dem er sich befindet.                                 |
| FitShape | [VgTriState](msdn-online-vml-vgtristate.md). Streckt den Textpfad bis zu den Rändern des Formfelds.                      |
| Ein       | [VgTriState](msdn-online-vml-vgtristate.md). Bestimmt, ob die Zeichenpfade angezeigt werden oder nicht.                    |
| String   | Eine Zeichenfolge. Der Text, der als Textpfad gerendert werden soll.                                                                                    |
| Glätten     | [VgTriState](msdn-online-vml-vgtristate.md). Entfernt zusätzlichen Speicherplatz, der für Aufsteigende und Absteigende reserviert ist, wenn er nicht verwendet wird. |
| Xscale   | [VgTriState](msdn-online-vml-vgtristate.md). Verwenden Sie eine gerade x-Messung, anstatt entlang des Pfads zu messen.                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a>Im VML-Objektmodell verwendete Datentypen

Die folgenden Datentypen werden vom VML-Objektmodell verwendet.

-   [Double](/windows)
-   [Fest](/windows)
-   [Integer](/windows)
-   [IVgAdjustments](/windows)
-   [IVgColor](/windows)
-   [IVgEquation](/windows)
-   [IVgFixedRectangle](/windows)
-   [IVgFixedRectangleArray](/windows)
-   [IVgFormula](/windows)
-   [IVgFormulas](/windows)
-   [IVgGradientColorArray](/windows)
-   [IVgPoints](/windows)
-   [IVgSkewMatrix](/windows)
-   [IVgSkewOffset](/windows)
-   [IVgVector2D](/windows)
-   [IVgVector3D](/windows)
-   [Länge](/windows)
-   [Measure](/windows)
-   [String](/windows)
-   [VgBlackWhiteMode](/windows)
-   [VgFraction](/windows)
-   [VgTriState](/windows)

**Double-Datentyp**

Eine ganze Zahl mit doppelter Genauigkeit mit einem Bereich von -infinity bis unendlich.

**Korrigierter Datentyp**

Gleitkommazahl im Bereich von -32.766,0 bis 32.766,0.

**Integer-Datentyp**

Eine ganze Zahl mit einem Bereich von -infinity bis unendlich.

**IVgAdjustments-Datentyp**

Auflistung von Anpassungen an einer Form, die verwendet werden können, um die Dimensionen einer Form zu ändern. Anpassungen können als temporäre Platzhalter oder aus einem beliebigen Grund verwendet werden, aus dem Sie Variablen verwenden würden. Es gibt nur 8 Anpassungen in der Auflistung.



| attribute | Beschreibung                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exists     | [IVgTriState](msdn-online-vml-vgtristate.md). Bestimmt, ob eine angegebene Anpassung vorhanden ist. Beachten Sie, dass ein Index verwendet werden muss. das heißt, exists( item ) muss verwendet werden, um das Vorhandensein eines Elements abzurufen.                                                                                                                                                                   |
| Element       | [Long](#data-types-used-in-the-vml-object-model). Array von Anpassungen, indiziert von 0 bis 7. Beachten Sie, dass Anpassungen möglicherweise nur selten angegeben werden. Das heißt, zwischengeschaltete Arraywerte werden möglicherweise nicht immer ausgefüllt. Beispielsweise können die Elemente 1, 3 und 5 Werte für die Länge 3 aufweisen, wobei item(0), item(2) und item(4) angegeben sind. Um festzustellen, ob ein Element vorhanden ist, verwenden Sie das Exists-Attribut. |
| Länge     | [Integer](#data-types-used-in-the-vml-object-model). Anzahl der Anpassungen. Darf nicht größer als 8 sein.                                                                                                                                                                                                                                                                          |
| Wert      | [Zeichenfolge](#data-types-used-in-the-vml-object-model). Textdarstellung numerischer Werte mit Kommas zwischen den einzelnen Zahlen.                                                                                                                                                                                                                                                    |



 

**IVgColor**

Gibt eine Farbe an.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>RGB</td>
<td><strong>VgRGBType</strong>. RGB-Wert (Lang) der Farbe. Nur gültig, wenn Type RGB ist.</td>
</tr>
<tr class="even">
<td>R</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Rote Komponente der Farbe. Kann zwischen 0 und 255 liegen.</td>
</tr>
<tr class="odd">
<td>G</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Grüne Komponente der Farbe. Kann zwischen 0 und 255 liegen.</td>
</tr>
<tr class="even">
<td>B</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Blaue Komponente der Farbe. Kann zwischen 0 und 255 liegen.</td>
</tr>
<tr class="odd">
<td>String</td>
<td><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>. Textdarstellung der Farbe. Die folgenden benannten Farbtypen werden unterstützt:
<ul>
<li>Schwarz (#000000)</li>
<li>Silber (#C0C0C0)</li>
<li>Gray (#808080)</li>
<li>Weiß (#FFFFFF)</li>
<li>Maroon (#800000)</li>
<li>Rot (#FF0000)</li>
<li>Violett (#800080)</li>
<li>Sollia (#FF00FF)</li>
<li>Grün (#008000)</li>
<li>Limon (#00FF00)</li>
<li>Oliv (#808000)</li>
<li>Gelb (#FFFF00)</li>
<li>#000080</li>
<li>Blau (#0000FF)</li>
<li>Teal (#008080)</li>
<li>Aqua (#00FFFF)</li>
</ul></td>
</tr>
<tr class="even">
<td>Typ</td>
<td><strong>VgColorType</strong>. Typ der Farbe. Einer der folgenden Typen:
<ul>
<li>Mixed</li>
<li>benannt</li>
<li>RGB</li>
<li>Schema</li>
</ul></td>
</tr>
</tbody>
</table>



 

**IVgEquation**

Formeln, die für Formeln verwendet werden.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Vorgang</td>
<td><strong>VgEquationOperationType</strong> Name des Vorgangs, der für die Parameter ausgeführt werden soll. Die folgenden Vorgänge können in einer Gleichung verwendet werden:
<table>
<thead>
<tr class="header">
<th>Vorgang</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Abs</td>
<td>Absoluter Wert. <br/> <strong>abs</strong>(v) <br/></td>
</tr>
<tr class="even">
<td>Atan2</td>
<td>Polararithmetik: Führt zu fd-Einheiten (Grad multipliziert mit 65536).<br/> <strong>atan2</strong>(p1,v) <br/></td>
</tr>
<tr class="odd">
<td>Cos</td>
<td>Kosinus, Argument in fd-Einheiten (Grad multipliziert mit 65536).<br/> v * <strong>cos</strong>(p1) <br/></td>
</tr>
<tr class="even">
<td>Cosatan2</td>
<td>Behält die vollständige Genauigkeit bei der Zwischenberechnung bei.<br/> v * <strong>cos(atan2(</strong> p2,p1 <strong>))</strong><br/></td>
</tr>
<tr class="odd">
<td>Ellipse</td>
<td>Ellipse</td>
</tr>
<tr class="even">
<td>If</td>
<td>Wenn Bedingungstest. v > 0 <strong>?</strong> p1 : p2</td>
</tr>
<tr class="odd">
<td>Max.</td>
<td>Der größere von zwei Werten. <br/> <strong>max</strong>(v,p1) <br/></td>
</tr>
<tr class="even">
<td>Mid</td>
<td>Average ( v + p1)/2</td>
</tr>
<tr class="odd">
<td>Min</td>
<td>Der kleinere von zwei Werten. <strong>min</strong>(v,p1)</td>
</tr>
<tr class="even">
<td>Mod</td>
<td>Modulo</td>
</tr>
<tr class="odd">
<td>Produkt</td>
<td>Wird für Multiplikation und Division verwendet. v * p1 /p2</td>
</tr>
<tr class="even">
<td>Sin</td>
<td>Sinus, Argument in FD-Einheiten (Grad multipliziert mit 65536). <br/> v * <strong>sin</strong>(p1) <br/></td>
</tr>
<tr class="odd">
<td>Sinatan2</td>
<td>Behält die vollständige Genauigkeit bei der Zwischenberechnung bei. v * <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</td>
</tr>
<tr class="even">
<td>Sqrt</td>
<td>Das Ergebnis ist positiv und rundet ab. <br/> <strong>sqrt</strong>(v) <br/></td>
</tr>
<tr class="odd">
<td>Sum</td>
<td>Wird für Addition und Subtraktion verwendet.<br/> v + p1 p2<br/></td>
</tr>
<tr class="even">
<td>Sumangle</td>
<td>Vorhandener Winkel (skaliert um 65536), wobei p1 und p2 grad sind.<br/> v + p1 * 65536 + p2 * 65536<br/></td>
</tr>
<tr class="odd">
<td>Tan</td>
<td>Tangens, Argument ist in FD-Einheiten (Grad multipliziert mit 65536). <br/> v * tan( p1 )<br/></td>
</tr>
<tr class="even">
<td>Val</td>
<td>Definiert einen Leitfadenwert aus einem anderen Wert.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Param1</td>
<td><strong>Integer</strong>. Der erste Parameter.</td>
</tr>
<tr class="odd">
<td>Paramtype1</td>
<td><strong>VgFormulaParamType</strong>. Der Typ des ersten Parameters. Die folgenden Werte werden unterstützt:
<table>
<thead>
<tr class="header">
<th>Typ</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Wert</td>
<td>Parameter ist ein einfacher Wert.</td>
</tr>
<tr class="even">
<td>AdjustmentReference</td>
<td>Parameter ist ein Verweis auf eine Anpassung. Wenn der erste Parameter beispielsweise 1 ist, wird der Wert der ersten Anpassung verwendet.</td>
</tr>
<tr class="odd">
<td>FormulaReference</td>
<td>Parameter ist das Ergebnis eines Verweises auf das Ergebnis einer vorherigen Formel. Wenn der erste Parameter beispielsweise 2 ist, wird das Ergebnis von Formel 2 verwendet.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Param2</td>
<td><strong>Integer</strong>. Der zweite Parameter.</td>
</tr>
<tr class="odd">
<td>Paramtype2</td>
<td><strong>VgFormulaParamType</strong> Der Typ des Parameters 2.</td>
</tr>
<tr class="even">
<td>Val</td>
<td><strong>Integer</strong>. Das Ergebnis.</td>
</tr>
<tr class="odd">
<td>Valtype2</td>
<td><strong>VgFormulaParamType</strong>. Der Typ des Ergebnisses.</td>
</tr>
</tbody>
</table>



 

**IVgFixedRectangle**

Gibt ein festes Rechteck an.



| attribute | Beschreibung                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Wert      | [Zeichenfolge.](#data-types-used-in-the-vml-object-model) Textwert, der den Pfad an gibt.         |
| Left       | [Double](#data-types-used-in-the-vml-object-model). Die äußerste linke Koordinate des Rechtecks.   |
| Oben        | [Double](#data-types-used-in-the-vml-object-model). Oberste Koordinate des Rechtecks.    |
| Right      | [Double](#data-types-used-in-the-vml-object-model). Die oberste Koordinate des Rechtecks.  |
| Unten     | [Double](#data-types-used-in-the-vml-object-model). Die unterste Koordinate des Rechtecks. |



 

**IVgFixedRectangleArray**

Array fester Rechtecke.



| attribute | Beschreibung                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| Wert      | [Zeichenfolge.](#data-types-used-in-the-vml-object-model) Textdarstellung des Arrays.                           |
| Länge     | [Integer](#data-types-used-in-the-vml-object-model). Anzahl der Rechtecke in diesem Array.                    |
| Element       | [IVgFixedRectangle](#data-types-used-in-the-vml-object-model). Das Rechteckobjekt am angegebenen Index. |



 

**IVgFormula-Datentyp**

Definitionen für Formeln, die den Pfad einer Form variieren oder für andere Berechnungszwecke verwendet werden können. Formeln können auf dem **Adj-Attribut** einer Form basieren, das sich ändern kann. Formeln können auch auf andere Formeln verweisen.



| attribute| Beschreibung                                           |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eqn        | [IVgEquation](#data-types-used-in-the-vml-object-model). Jede Formel definiert einen einzelnen Wert als Ergebnis der Auswertung des Ausdrucks. Der Ausdruck wird durch dieses Attribut definiert und hat die allgemeine Form eines Vorgangs, gefolgt von bis zu drei Argumenten, die Anpassungswerte (z. B. 2), die Ergebnisse früherer Formeln (z. B. ), feste Zahlen oder vordefinierte Werte sein \# @2 können. |



 

**IVgFormulas-Datentyp**

Eine Auflistung von Formelobjekten.



| attribute | Beschreibung                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Länge     | [Integer](#data-types-used-in-the-vml-object-model). Anzahl von Formelobjekten in der Auflistung.                                                |
| Element       | [IVgFormula](#data-types-used-in-the-vml-object-model). Eine bestimmte Formel. Beachten Sie, dass das Formelarray vom Formtyp geerbt werden kann. |



 

**IVgGradientColorArray**

Ein Array von Farben, die einen Farbverlauf definieren (gemischter Farbbereich).



| attribute | Beschreibung                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| Wert      | [Zeichenfolge.](#data-types-used-in-the-vml-object-model) Gibt das Array von Farben an. Beispiel: "red .2; green .4; black .7" |
| Länge     | [Integer](#data-types-used-in-the-vml-object-model). Anzahl der Farben im Array.                                          |



 



| Methode     | Beschreibung                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AddColor    | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Fügt am durch fraction angegebenen Endpunkt eine neue Farbe hinzu. Die neue Farbe ist standardmäßig weiß und ist der Rückgabewert. Die Farbe kann dann als Verweis geändert werden. |
| RemoveColor | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Entfernt eine Farbe am Endpunkt, der durch fraction angegeben wird. Hinweis: Wenn 0.0 oder 1.0 nicht vorhanden ist, wird dies impliziert, und die Farbe Weiß wird an diesem Punkt verwendet.          |



 

**IVgPoints-Datentyp**

Array von Punkten, die eine Form definieren.



| attribute | Beschreibung                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Wert      | [Zeichenfolge.](#data-types-used-in-the-vml-object-model) Textdarstellung des Arrays.           |
| Länge     | [Integer](#data-types-used-in-the-vml-object-model). Anzahl der Punkte in diesem Array.        |
| Element       | [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md). Der Punkt am angegebenen Index. |



 

**IVgSkewMatrix-Datentyp**

Eine Matrix, die zum Erstellen von Formen verwendet wird, eine Perspektivtransformationsmatrix im Format "*sxx,sxy,syx,syy,px,py* " \[ *s* =scale, *p* =perspective \] . Wenn offset in absoluten Einheiten liegt, befinden *sich px,py* in emu ^-1 Einheiten; andernfalls sind sie ein umgekehrter Bruchteil der Formgröße.



| attribute   | Beschreibung                                         |
|--------------|-----------------------------------------------------|
| XtoX         | [Double](#data-types-used-in-the-vml-object-model). |
| YtoX         | [Double](#data-types-used-in-the-vml-object-model). |
| XtoY         | [Double](#data-types-used-in-the-vml-object-model). |
| YtoY         | [Double](#data-types-used-in-the-vml-object-model). |
| PerspectiveX | [Double](#data-types-used-in-the-vml-object-model). |
| Perspectivey | [Double](#data-types-used-in-the-vml-object-model). |



 

**IVgSkewOffset**

Gibt den Offset der Schiefe an.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Wert</td>
<td><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge.</a> Textdarstellung des Offsets.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. X-Komponente. Prozentsatz oder Measure. Wenn keine Einheiten verwendet werden, wird ShapeRelative-Typ impliziert. andernfalls wird absoluter Typ impliziert.</td>
</tr>
<tr class="odd">
<td>J</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Y-Komponente.</td>
</tr>
<tr class="even">
<td>Typ</td>
<td><strong>VgSkewTransformType</strong>. Gibt den Typ der Transformation an. Gültige Werte sind ganzzahlige Punkte, die zwischen -infinity und infinity liegen. 
<table>
<thead>
<tr class="header">
<th>Typ</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShapeRelative</td>
<td>Die Werte des Offsets sind Prozentsätze (Verhältnisse) der Größe der ursprünglichen Form. Ein Wert von 0,5 bedeutet z. B. einen Offset, der halb so groß wie die Form ist.</td>
</tr>
<tr class="even">
<td>Absolut</td>
<td>Die Werte sind absolute Einheiten.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

**IVgVector2D-Datentyp**

Gibt einen zweidimensionalen Vektor an, der aus zwei **Double-Zahlen** besteht.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Wert</td>
<td><strong>Zeichenfolge.</strong> Textdarstellung beider Vektorzahlen, die durch ein Leerzeichen getrennt sind.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. X-Komponente dieses Vektors.</td>
</tr>
<tr class="odd">
<td>J</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Y-Komponente dieses Vektors.</td>
</tr>
<tr class="even">
<td>Typ</td>
<td><strong>VgVectorType</strong>. Erwartete Einheiten für diesen Vektor. Gültige Werte:
<ul>
<li>"Measure"</li>
<li>Länge</li>
<li>AngleInDegrees</li>
<li>Fraction</li>
<li>Ganze Zahl in Prozent</li>
</ul></td>
</tr>
</tbody>
</table>



 

**IVgVector3D-Datentyp**

Gibt einen dreidimensionalen Vektor an, der aus drei **Double-Zahlen** besteht.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Wert</td>
<td><strong>Zeichenfolge.</strong> Textdarstellung von drei Vektorzahlen, die durch ein Leerzeichen getrennt sind.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. X-Komponente dieses Vektors.</td>
</tr>
<tr class="odd">
<td>J</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Y-Komponente dieses Vektors.</td>
</tr>
<tr class="even">
<td>Z</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Z-Komponente dieses Vektors.</td>
</tr>
<tr class="odd">
<td>Typ</td>
<td><strong>VgVectorType</strong>. Erwartete Einheiten für diesen Vektor. Gültige Werte:
<ul>
<li>"Measure"</li>
<li>Länge</li>
<li>AngleInDegrees</li>
<li>Fraction</li>
<li>Zahl</li>
<li>Prozentsatz</li>
<li>Integer</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Längendatentyp**

Eine Gleitkommazahl mit einem Bereich von 0 bis unendlich.

**Measuredatentyp**

Eine Gleitkommazahl von -infinity bis unendlich.

**String-Datentyp**

Zeichendaten beliebiger Länge.

**VgBlackWhiteMode**

Renderingmodus für Schwarz/Weiß. Mögliche Werte:

-   **Farbe**
-   **Automatisch**
-   **Graustufen**
-   **LightGrayScale**
-   **InverseGray**
-   **GrayOutline**
-   **BlackTextAndLines**
-   **HighContrast**
-   **Schwarz**
-   **Weiß**
-   **Undrawn**

**VgFraction-Datentyp**

Gleitkommazahl mit einem Bereich von 0,0 bis 1,0. Brüche können auch als Prozentsatz angegeben werden. z.B. "50%".

**VgTriState-Datentyp**

Enumeration, die für Werte verwendet wird, die einen von drei Zuzuständen haben können:

-   **TRUE**
-   **FALSE**
-   **GEMISCHT**
