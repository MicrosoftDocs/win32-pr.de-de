---
title: VML-Objektmodell Referenz
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889c977260548c26bbfd8196160e4537ccb8895d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039513"
---
# <a name="vml-object-model-reference"></a>VML-Objektmodell Referenz

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

In diesem Thema:

-   [Introduction (Einführung)](#introduction)
-   [Beispiel](#example)
-   [Einrichten von VML](#setting-up-vml)
-   [VML-OM-Referenz](#vml-om-reference)
    -   [Shape-Element](#shape-element)
-   [Unter Elemente des Shape-Elements](#subelements-of-the-shape-element)
    -   [Background-Element](#background-element)
    -   [Extrusion-Element](#extrusion-element)
    -   [Fill-Element](#fill-element)
    -   [Group-Element](#group-element)
    -   [Imagedata-Element](#imagedata-element)
    -   [Path-Element](#path-element)
    -   [Shadow-Element](#shadow-element)
    -   [Verzerrt-Element](#skew-element)
    -   [Stroke-Element](#stroke-element)
    -   [TextPath-Element](#textpath-element)
-   [Im VML-Objektmodell verwendete Datentypen](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a>Einführung

[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) ist eine textbasierte Sprache, die [XML](https://www.w3.org/TR/REC-xml.mdl) verwendet, um HTML zu erweitern, um Vektorgrafik Informationen anzuzeigen. Der VML-Dokumentobjektmodell (DOM) definiert eine programmgesteuerte Schnittstelle für die Bearbeitung der Dokument Elemente. Dies ermöglicht dem Benutzer das dynamische Erstellen und Ändern von Vektorgrafiken über eine Plattform-und sprachneutrale Schnittstelle. Das VML-DOM entspricht der [Dokumentobjektmodell](https://www.w3.org/TR/REC-DOM-Level-1/) Spezifikation.

VML verwendet das [Shape](#shape-element) -Element als grundlegenden Baustein für Vektorgrafik Bilder. Nachdem eine Form erstellt wurde, können Sie die Form durch Attribute oder angefügte unter Elemente ändern. Um z. b. die Farbe einer Form zu ändern, weisen Sie dem **FillColor** -Attribut einen Farbwert zu.


```HTML
myshape.fillcolor = "red"
```



Einige der Attribute einer Form [sind auch unter](/windows) Elemente und verfügen über eigene Attribute, einschließlich der folgenden:

-   [Hintergrund](#background-element)
-   [Schläuche](#extrusion-element)
-   [Ausfüllen](#fill-element)
-   [Gruppieren](#group-element)
-   [Imagedata](#imagedata-element)
-   [Pfad](#path-element)
-   [Shadow](#shadow-element)
-   [Neigen](#skew-element)
-   [Stellung](#stroke-element)
-   [TextPath](#textpath-element)

Das VML-OM verwendet mehrere [Datentypen](/windows) , um Parameter zu definieren. Datatypes, die "VG" als Präfix haben, sind Enumerationen, und die mit dem Präfix "IVG" sind Objekte. Klicken Sie hier, um eine Liste zu finden. Kleinere Datentypen sind mit bestimmten Parametern aufgelistet.

## <a name="example"></a>Beispiel

Der folgende VBScript-Code zeigt, wie eine einfache Form erstellt wird:


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



Im obigen Beispiel wird eine Form mithilfe der Dokumentobjektmodell-Methode " **kreateelement**" erstellt. Die Form ist eine vordefinierte VML-Form "Rect". Obwohl das Objekt vorhanden ist, kann es nicht Teil des Dokuments sein, bis es an das Dokument angefügt wird. Mithilfe der **AppendChild** -Methode wird das Rect als untergeordnetes Element eines **div** -Elements mit dem Namen mydiv festgestellt. Einige minimale Stil Attribute (**Position**, **Breite**, **Höhe**, **oben**, **Links**) werden festgelegt, um der Form eine bestimmte Größe zuzuweisen. Schließlich wird eine Farbe mit dem **FillColor** -Attribut zugewiesen. Beachten Sie, dass jede Skriptsprache oder jede beliebige Sprache verwendet werden kann, die mit Dokumentobjektmodell-Schnittstellen verwendet werden kann.

## <a name="setting-up-vml"></a>Einrichten von VML

Eine Implementierung von VML erfolgt über Microsoft Internet Explorer 5,0 oder höher. Zum ordnungsgemäßen Einrichten des renderingobjekts auf einer Webseite müssen folgende Ergänzungen vorgenommen werden:

1.  Das Schema muss im ersten <HTML> Markieren Sie Folgendes:
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  Das Renderingverhalten muss Teil des Dokument Stils sein:
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

Im folgenden sehen Sie eine Beispiel-HTML-Webseite, die für VML ordnungsgemäß eingerichtet wurde und die dynamische Erstellung einer Form anzeigt.


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



Beachten Sie, dass in Beta Versionen ein ActiveX-Objekttag und ein anderes Verhaltens Format erforderlich sind.

## <a name="vml-om-reference"></a>VML-OM-Referenz

Dieser Verweis definiert die [Shape](#shape-element) -Elemente [, unter](/windows)Elemente und [Datentypen](/windows) , die vom Objektmodell von VML verwendet werden.

### <a name="shape-element"></a>Shape-Element

Formen sind die Bausteine grafischer Bilder, die durch Vector Markup Language (VML) definiert werden. Die Form ist das Element der obersten Ebene, und verschiedene unter Elemente helfen dabei, die Art der einzelnen Formen zu definieren.

VML bietet vordefinierte Formen:

**Shape-Attribute**

-   **Arc**
-   **FF**
-   **Line**
-   **Polylinie**
-   **Rect**
-   **RoundRect**



|              |                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADJ          | [Ivganpassungen](msdn-online-vml-ivgadjustments-data-type.md). Eine durch Trennzeichen getrennte Liste von Zahlen, die die Parameter für die Führungs Formeln sind, die den Pfad der Form definieren. Werte werden möglicherweise weggelassen, um die Verwendung von Standardwerten zuzulassen. Es können bis zu 8 Anpassungs Werte vorhanden sein.                                                                                                   |
| ALT          | Eine Zeichenfolge. Alternativer Text, der Shape zugeordnet ist. Wird für nicht-grafische Browser verwendet.                                                                                                                                                                                                                                                                                                 |
| Schaltfläche       | [Vgder State](msdn-online-vml-vgtristate.md). Zeigt das Schaltflächen Verhalten beim Klicken an.                                                                                                                                                                                                                                                                                                 |
| Bwmode       | [Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md). Bestimmt, wie die Form in der schwarz-und weiß-Ansicht in-Apps oder bei der Druck auf schwarze und weiße Drucker dargestellt wird. Folgende Werte sind enthalten: **Color**, **Auto**, **Grayscale**, **lightgrayscale**, **inversgray**, **grayoutline**, **blacktextandlines**, **HighContrast**, **Black**, **White**, **undrawn**. Standardwert: **Auto**. |
| Bwnormal     | Vgblackwhitemode. Wenn bwmode auf Auto fest steht, wird diese Eigenschaft für die Art und Weise, wie die Form in normalem schwarz und weiß dargestellt wird, untersucht. Folgende Werte sind enthalten: **Color**, **Auto**, **Grayscale**, **lightgrayscale**, **inversgray**, **grayoutline**, **blacktextandlines**, **HighContrast**, **Black**, **White**, **undrawn**. Standardwert: **Auto**.                                                |
| Bwpure       | Vgblackwhitemode. Wenn bwmode auf Auto fest steht, wird diese Eigenschaft für das Renderingformat in reiner B/W. Folgende Werte sind enthalten: **Color**, **Auto**, **Grayscale**, **lightgrayscale**, **inversgray**, **grayoutline**, **blacktextandlines**, **HighContrast**, **Black**, **White**, **undrawn**. Standardwert: **Auto**.                                                              |
| Childshapes  | Ivggroupshapes. Eine Auflistung anderer Formen in dieser Gruppe. Diese Auflistung unterstützt die standardmäßigen length-und Item-Methoden.                                                                                                                                                                                                                                                       |
| Chromakey    | [Ivgcolor](msdn-online-vml-ivgcolor.md). Ein Farbwert, der transparent ist und alles hinter der Form anzeigt.                                                                                                                                                                                                                                                             |
| Control1     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Der Kontrollpunkt für die Kurve.                                                                                                                                                                                                                                                                                                  |
| Control2     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Der Kontrollpunkt für die Kurve.                                                                                                                                                                                                                                                                                                  |
| Coordorigin  | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Die Koordinaten in der oberen linken Ecke des Container Rechtecks. Bereich von 0 bis unendlich.                                                                                                                                                                                                                               |
| Coordsize    | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Die Breite und Höhe des Koordinaten Raums innerhalb des Bezugs Rechtecks dieser Form. Wenn Sie nicht angegeben ist, entspricht Sie der Breite und Höhe des Rechtecks. Bereich von 0 bis unendlich. Standardwert: "1000, 1000".                                                                                               |
| Umschließen     | [Vganglin Grad](msdn-online-vml-vgangleindegrees-data-type.md). Endwinkel der Form.                                                                                                                                                                                                                                                                                          |
| Schläuche    | Ivgextrusion. Gibt den Wert des extrusionsobjekt für diese Form an. Weitere Informationen finden Sie unter dem-Element " [Extrusion](msdn-online-vml-extrusion-element.md) ".                                                                                                                                                                                                                               |
| Ausfüllen         | Vgfillformat. Gibt den Füll Wert für diese Form an. Weitere Informationen finden [Sie im Fill](msdn-online-vml-fill-element.md) -Element.                                                                                                                                                                                                                                                |
| FillColor    | [Ivgcolor](msdn-online-vml-ivgcolor.md). Die Primärfarbe des Pinsels, der zum Ausfüllen des Pfads dieser Form verwendet werden soll.                                                                                                                                                                                                                                                                  |
| Füllen       | [Vgder State](msdn-online-vml-vgtristate.md). True gibt an, dass der Pfad, der die Form definiert, ausgefüllt wird. Standardmäßig wird Sie mit einer voll Tonfarbe aufgefüllt, es sei denn, es gibt ein Füll Teilelement, das komplexere Fülleigenschaften angibt. Wenn der Wert false ist, ist die Füllung transparent.                                                                                                           |
| Kippen         | Vgfliporientation. Werte: X Y XY YX                                                                                                                                                                                                                                                                                                                                         |
| Forcedash    | [Vgder State](msdn-online-vml-vgtristate.md). Gibt an, dass ein gestrichelter Umriss gerendert werden soll, wenn keine Zeile und keine Füllung für eine Form vorhanden ist. Dieses Verhalten ist in der Regel hilfreich, um unsichtbare Formen in der Bearbeitung von Anwendungen sichtbar zu machen, sodass Sie ausgewählt und verarbeitet werden können, z. b. in einer ImageMap.                                                                 |
| Formeln     | Ivgformeln. Ein Array von Formeln, das eine Form definiert.                                                                                                                                                                                                                                                                                                                          |
| From         | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Anfangspunkt der Zeile.                                                                                                                                                                                                                                                                                                   |
| HRef         | [Zeichenfolge](#data-types-used-in-the-vml-object-model). Die URL, zu der gewechselt werden soll, wenn auf diese Form geklickt wird.                                                                                                                                                                                                                                                                                 |
| ImageData    | Ivgimagedata. Bild Informationen, wenn die Form ein Bild ist. Weitere Informationen finden Sie unter dem imagedata-Element.                                                                                                                                                                                                                                                                       |
| Geplant         | [Vgder State](msdn-online-vml-vgtristate.md). Blendet alle Handles außer der oberen linken und unteren rechten Ecke aus, wie in den Handles für ein gerades Liniensegment.                                                                                                                                                                                                                             |
| Opacity      | [Vgbruchteile](msdn-online-vml-vgfraction-data-type.md). Die Deckkraft der gesamten Form. Eine Zahl zwischen 0,0 und 1,0.                                                                                                                                                                                                                                                           |
| Pfad         | Ivgpath. Eine Zeichenfolge, die die Befehle enthält, die den Pfad definieren.                                                                                                                                                                                                                                                                                                                  |
| Punkte       | [Ivgpoints](msdn-online-vml-ivgpoints-data-type.md). Eine Auflistung von Punkten, die eine Form definieren.                                                                                                                                                                                                                                                                                   |
| Drucken        | [Vgder State](msdn-online-vml-vgtristate.md). True gibt an, dass diese Form gedruckt werden soll.                                                                                                                                                                                                                                                                                        |
| Drehung     | [Vganglin Grad](msdn-online-vml-vgangleindegrees-data-type.md). Legt die Drehung der Form fest. Der Wert wird an den Shape-Stil weitergegeben.                                                                                                                                                                                                                                              |
| Skalieren        | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Skalierung der Form.                                                                                                                                                                                                                                                                                                           |
| Shadow       | Ivgshadow. Gibt den Schatten für diese Form an. Weitere Informationen finden Sie im [Schatten](msdn-online-vml-shadow-element.md) Element.                                                                                                                                                                                                                                                        |
| SPT          | Reserviert.                                                                                                                                                                                                                                                                                                                                                                        |
| Start Angle   | [Vganglin Grad](msdn-online-vml-vgangleindegrees-data-type.md). Der Start Winkel der Form.                                                                                                                                                                                                                                                                                        |
| Stroke       | Vgstrokeformat. Weitere Informationen finden Sie unter Stroke-Element.                                                                                                                                                                                                                                                                                                                                  |
| StrokeColor  | [Ivgcolor](msdn-online-vml-ivgcolor.md). Die Primärfarbe des Pinsels, der zum Zeichnen des Pfads dieser Form verwendet werden soll.                                                                                                                                                                                                                                                                |
| Strichen gezeichnet      | [Vgder State](msdn-online-vml-vgtristate.md). Wenn der Wert true ist, wird der Pfad, der die Form definiert, mit Strichen gezeichnet.                                                                                                                                                                                                                                                                              |
| Strokeweight | [Vglength](msdn-online-vml-vglength.md). Die Breite des Pinsels, der zum Zeichnen des Pfads verwendet werden soll. Zwischen 0 und 1584.                                                                                                                                                                                                                                                           |
| TextPath     | Ivgtextpath. Gibt das TextPath-Objekt der Form an. Weitere Informationen finden Sie im [TextPath](msdn-online-vml-textpath-element.md) -Element.                                                                                                                                                                                                                                  |
| Beschreibung           | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Endpunkt Ende.                                                                                                                                                                                                                                                                                                        |
| type         | Eine Zeichenfolge. Der Typ der Form.                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a>Unter Elemente des Shape-Elements

Die folgenden unter Elemente sind Teil des VML-Objektmodells.

-   [Hintergrund](#background-element)
-   [Schläuche](#extrusion-element)
-   [Ausfüllen](#fill-element)
-   [Gruppieren](#group-element)
-   [Imagedata](#imagedata-element)
-   [Pfad](#path-element)
-   [Shadow](#shadow-element)
-   [Neigen](#skew-element)
-   [Stellung](#stroke-element)
-   [TextPath](#textpath-element)

### <a name="background-element"></a>Background-Element

Beschreibt die Füllung des Hintergrunds einer Seite mithilfe von VML-Füllungen.

**Attribute**



|           |                                                                                                                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bwmode    | [Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md). Bestimmt, wie die Form in der schwarzen und weißen Ansicht in Anwendungen oder gedruckt wird.                                     |
| Bwnormal  | [Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md). Wenn bwmode auf Auto fest steht, wird diese Eigenschaft für die Art und Weise, wie die Form in normalem schwarz und weiß dargestellt wird, untersucht.                        |
| Bwpure    | [Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md). Wenn bwmode auf Auto fest steht, wird diese Eigenschaft für das Renderingformat in reiner Schwarz-und weiß-Form abgefragt.                          |
| Ausfüllen      | Vgfillformat. Gibt die Füllung für diese Form an. Weitere Informationen finden [Sie unter Fill](msdn-online-vml-fill-element.md) -Element.                                                             |
| FillColor | [Ivgcolor](msdn-online-vml-ivgcolor.md). Die Primärfarbe des Pinsels, der zum Ausfüllen des Pfads dieser Form verwendet werden soll. Duplikat des Farbwerts im Fill-Element. Der Standardwert ist Weiß. |



 

### <a name="extrusion-element"></a>Extrusion-Element

Beschreibt eine 3D-Extrusion der Form.

**Attribute**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Autorotationcenter</td>
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. True gibt an, dass der Mittelpunkt der Drehung der Gruppe von 3D-Objekten (tatsächlich ist nur ein Objekt in der Gruppe vorhanden) automatisch als Mittelpunkt der Gruppe festgelegt wird. Andernfalls wird Sie durch die rotationCenter-Parameter bestimmt, bei denen es sich um einen Bruchteil der Form handelt, bei dem 0, 0, 0 die Mitte ist.</td>
</tr>
<tr class="even">
<td>Backtiefe</td>
<td><a href="msdn-online-vml-vglength.md"><strong>Vglength</strong></a>. Menge der abwärts Extrusion. Liegt zwischen 0 und 32767.</td>
</tr>
<tr class="odd">
<td>Brightness</td>
<td><a href="#data-types-used-in-the-vml-object-model">Vgpositivenumschlag</a>. Allgemeine Helligkeit der Szene. Der Standardwert ist &quot; 20.000 &quot; .</td>
</tr>
<tr class="even">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">Ivgcolor</a>. Die Farbe der-Extrusion. Wird nur verwendet, wenn ColorMode Benutzer definiert ist. Andernfalls wird die Farbe des Bild-und-Effekts automatisch auf den gleichen Wert wie FillColor festgelegt.</td>
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
<td><a href="#data-types-used-in-the-vml-object-model">Vgpositivenumschlag</a>. Das Verhältnis zwischen Incident und diffus reflektiertem Licht. Werte, die kleiner als 1,0 sind, sind normal, aber Werte, die größer als 1 sind, können interessante Effekte</td>
</tr>
<tr class="odd">
<td>Edge</td>
<td><a href="msdn-online-vml-vglength.md">Vglength</a>. Legt die Größe eines simulierten, gerundeten gepufferten Edge fest. Reicht zwischen 0 und 32767 in Gleit Komma-pts. Der Standardwert ist &quot; 1 pt &quot; .</td>
</tr>
<tr class="even">
<td>Facet</td>
<td><a href="#data-types-used-in-the-vml-object-model">Vgpositivenumschlag</a>. Legt die Facette der Szene fest. Der Standardwert ist &quot; 30.000 &quot; .</td>
</tr>
<tr class="odd">
<td>Foretiefe</td>
<td><a href="msdn-online-vml-vglength.md">Vglength</a>. Menge der vorwärts-Extrusion. Liegt zwischen 0 und 32767.</td>
</tr>
<tr class="even">
<td>Lightface</td>
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. Determinimt, ob die Vorderseite des Objekts auf Änderungen in der 3D-Beleuchtung antwortet, z. b. Wenn ein Objekt rotiert.</td>
</tr>
<tr class="odd">
<td>Lightharsh</td>
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. Harte Beleuchtung für die primäre Light-Quelle. Der Standardwert lautet False.</td>
</tr>
<tr class="even">
<td>LightHarsh2</td>
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. Harte Beleuchtung der sekundären Lichtquelle. Der Standardwert lautet False.</td>
</tr>
<tr class="odd">
<td>Lightlevel</td>
<td><a href="#data-types-used-in-the-vml-object-model">Vgnumber</a>. Intensität der primären Lichtquelle. Der Standardwert ist &quot; 38000 &quot; .</td>
</tr>
<tr class="even">
<td>LightLevel2</td>
<td><a href="#data-types-used-in-the-vml-object-model">Vgnumber</a>. Intensität der sekundären Lichtquelle. Der Standardwert ist &quot; 38000 &quot; .</td>
</tr>
<tr class="odd">
<td>Lightposition</td>
<td>Vector3D. Die Position der primären Lichtquelle. Der Standardwert ist &quot; 50000, 0, 10000 &quot; .</td>
</tr>
<tr class="even">
<td>LightPosition2</td>
<td>Vector3D. Die Position der sekundären Lichtquelle. Der Standardwert ist &quot; -50000, 0, 10000 &quot; .</td>
</tr>
<tr class="odd">
<td>Lockrotationcenter</td>
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. &quot;Lockrotationcenter &quot; bedeutet, dass die Rotation der Gruppe so definiert ist, dass Sie durch den Drehwinkel [1] Grad um die y-Achse auf der Seite folgt, gefolgt von einem Drehwinkel [0] Grad zur x-Achse. Wenn lockrotationcenter auf false festgelegt ist, wird die Drehung so definiert, dass Sie durch die Ausrichtung auf den durch Ausrichtung definierten Vektor festgelegt wird. Beispielsweise entspricht lockrotationcenter = false orientationangle = 45 Orientation = (0, 1, 0) dem lockrotationcenter = true RotationAngle = (0,0).</td>
</tr>
<tr class="even">
<td>Metallisch</td>
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. Bewirkt, dass das Licht mit dem reflektierten Licht anstelle der hellen Quellfarbe die Material Farbe ist, sodass das Objekt mehr Metallic erscheint.</td>
</tr>
<tr class="odd">
<td>Ein</td>
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. Schaltet die Anzeige des extrusioneffekts ein bzw. aus.</td>
</tr>
<tr class="even">
<td>Orientation</td>
<td>Vector3D. Die Ausrichtung der Kamera.</td>
</tr>
<tr class="odd">
<td>Orientationangle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">Vganglin Grad</a>. Der Winkel zwischen der Ausrichtung der Kamera und der XY-Ebene.</td>
</tr>
<tr class="even">
<td>Wasser</td>
<td>Vg3DExtrudePlane. Ermöglicht die-Extrusion zwischen orthogonaler Ebene und der Bildschirm Ebene. Erfordert, dass foretiefe und backtiefe in Zeichnungs Einheiten anstelle von Emus angegeben werden. Gültige Werte:
<ul>
<li>D</li>
<li>ZX</li>
<li>YZ</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rendern</td>
<td>Vg3DRenderMode. Gültige Werte:
<ul>
<li>Solid (Standard)</li>
<li>Draht Modell</li>
<li>Boundingcube</li>
</ul></td>
</tr>
<tr class="even">
<td>RotationAngle</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. AngleX, AngleY oder anglez wird durch das shaperotations-Attribut gesteuert.</td>
</tr>
<tr class="odd">
<td>RotationCenter</td>
<td>Vector3D. Mittelpunkt der Drehung.</td>
</tr>
<tr class="even">
<td>Glanz</td>
<td><a href="#data-types-used-in-the-vml-object-model">Vgpositivenumschlag</a>. Bestimmt, wie sich die Glanz Reflektion konzentriert oder verteilt. Ein hoher Wert wäre 8 bis 10 und würde eine Spiegelung angleichen, und ein niedriger Wert wäre 2 bis 3 und würde eine ungefähre Reihenfolge von Bekleidung aufweisen. Werte von 3 bis 7 werden empfohlen. Hohe Werte werden PinPoint-Lichtquellen widerspiegeln.</td>
</tr>
<tr class="odd">
<td>Schief</td>
<td><a href="#data-types-used-in-the-vml-object-model">Vgprozentsatz</a>. Wenn der Typ parallel ist, bestimmt das Attribut die Menge der Schiefe. Liegt zwischen 0 und 100.</td>
</tr>
<tr class="even">
<td>Schief legen</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">Vganglin Grad</a>. Wenn der Typ parallel ist, bestimmt das Attribut den Grad der Schiefe. Der Standardwert ist &quot; -45 &quot; .</td>
</tr>
<tr class="odd">
<td>Spiegelung</td>
<td><a href="#data-types-used-in-the-vml-object-model">Vgpositivenumschlag</a>. Das Verhältnis zwischen Incident und spekulativ reflektiertem Licht. Werte, die kleiner als 1,0 sind, sind normal, aber Werte, die größer als 1 sind, können interessante Effekte</td>
</tr>
<tr class="even">
<td>type</td>
<td>Vgextrusiontype. Gültige Werte:
<ul>
<li>Parallel (Standard)</li>
<li>Perspektive</li>
</ul></td>
</tr>
<tr class="odd">
<td>Standpunkt</td>
<td>Vector3D. Der Punkt, von dem aus die Szene angezeigt wird.</td>
</tr>
<tr class="even">
<td>Viewpointorigin</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Kann über Werte von 0,5 bis-0,5 verfügen, um den Ursprung des Standpunkts innerhalb des umgebenden Felds der Form zu positionieren.</td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a>Fill-Element

Beschreibt, wie ein Pfad für Füllungen komplexer ist als eine voll Tonfarbe.

**Attribute**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Alignshape</td>
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. Richten Sie das Bild mit der Form aus. Wenn false, wird das Bild mit dem Fenster ausgerichtet.</td>
</tr>
<tr class="even">
<td>Angle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">Vganglin Grad</a>. Der Winkel, in dem der Farbverlauf verläuft. 0 Grad liegt entlang der horizontalen Achse von links nach rechts.</td>
</tr>
<tr class="odd">
<td>Aspekt</td>
<td><strong>Vgaspecttype</strong>. Das ImageSize-Attribut wird angepasst, um den Aspekt des Bilds zu erhalten. Mögliche Werte:
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignorieren</td>
<td>Ignoriert Aspekte von Aspekten.</td>
</tr>
<tr class="even">
<td>Mindestens</td>
<td>Image ist mindestens so groß wie die Bildgröße.</td>
</tr>
<tr class="odd">
<td>Höchstens</td>
<td>Das Bild ist nicht größer als die Bildgröße.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">Ivgcolor</a> Die Haupt Füllfarbe. Identisch mit FillColor-Attribut in Form.</td>
</tr>
<tr class="odd">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">Ivgcolor</a>. Die sekundäre Farbe für eine Füllung, wenn der Bildtyp ein Muster oder eine Farbverlaufsfüllung ist.</td>
</tr>
<tr class="even">
<td>Farben</td>
<td><a href="#data-types-used-in-the-vml-object-model">Ivggradientcolorarray</a>. Zwischen Farben im Farbverlauf und ihre relativen Positionen entlang des Farbverlaufs, z. b. &quot; 30% rot, 70% blau, 90% grün &quot; . Die primäre Farbe (Farb Attribut in Form) ist 0%, und die sekundäre Farbe (color2-Attribut) ist 100%.</td>
</tr>
<tr class="odd">
<td>Fokus</td>
<td><a href="#data-types-used-in-the-vml-object-model">Vgsignedprozentsatz</a>. Der Fokuspunkt für die lineare Verlaufs Füllung. Werte werden von-100 bis + 100.</td>
</tr>
<tr class="even">
<td>Focusposition</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Die Position des innersten Rechtecks für radiale Farbverläufe. Der Vektor ist ein Bruchteil (0,0-1,0) der Breite und Höhe der Form.</td>
</tr>
<tr class="odd">
<td>Focussize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Größe des innersten Rechtecks für radiale Farbverläufe. Der Vektor ist ein Bruchteil (0,0 bis 1,0) der Breite und Höhe der Form.</td>
</tr>
<tr class="even">
<td>Methode</td>
<td>Vgsigmatype. Mögliche Werte:
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
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. Schaltet die Füll Anzeige ein. Identisch mit Fill-Attribut in Form.</td>
</tr>
<tr class="even">
<td>Opacity</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">Vgbruchteile</a>. Deckkraft der Füllung.</td>
</tr>
<tr class="odd">
<td>Opacity2</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">Vgbruchteile</a>. Die sekundäre Deckkraft für Farbverläufe.</td>
</tr>
<tr class="even">
<td>Origin</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Der Punkt ist relativ zur oberen linken Ecke des Bilds, das als Ursprung des Bilds behandelt wird. Der Standardwert ist der Mittelpunkt des Bilds. Der Vektor ist ein Bruchteil (zwischen 0,0 und 1,0) der Breite und Höhe des Bilds.</td>
</tr>
<tr class="odd">
<td>Position</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Zeigen Sie im Verweis Rechteck der Form, um den Ursprung des Bilds zu positionieren. Der Standardwert ist die Mitte des Container Rechtecks. Der Vektor ist ein Bruchteil (0,0-1,0) der Breite und Höhe des Bilds.</td>
</tr>
<tr class="even">
<td>Size</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Die Größe des Bilds. Der Standardwert ist die Pixelgröße des Bilds. Kann in absoluten Koordinaten oder in Prozent angegeben werden.</td>
</tr>
<tr class="odd">
<td>Src</td>
<td><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>. Die URL zu einem Bild, das für Bild-und Muster Füllungen geladen werden soll. Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird.</td>
</tr>
<tr class="even">
<td>type</td>
<td>Vgfilltype. Es kann sich um einen der folgenden Typen handeln:
<ul>
<li>Hintergrund</li>
<li>Frame</li>
<li>Farbverlauf</li>
<li>Gradientcenter</li>
<li>Gradientradiale</li>
<li>Gradienttitle</li>
<li>Gradientunskaliert</li>
<li>Muster</li>
<li>Basis</li>
<li>Tile</li>
</ul>
Kachel, Muster und Rahmen erfordern, dass die Bildattribute bereitgestellt werden. Gradient und gradientradiale erfordern, dass die Farbverlaufs Attribute bereitgestellt werden.</td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a>Group-Element

Eine Gruppe ist eine Sammlung einzelner Formen, die als Einheit positioniert und transformiert werden kann.



|        |                                                                                              |
|--------|----------------------------------------------------------------------------------------------|
| Element   | [Ivgshape](#data-types-used-in-the-vml-object-model). Das angegebene Element im Array von Formen. |
| Länge | [Integer](#data-types-used-in-the-vml-object-model). Anzahl der Formen in dieser Gruppe.         |



 

### <a name="imagedata-element"></a>Imagedata-Element

Beschreibt ein Bild, das oberhalb einer Form gerendert werden soll.



|             |                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BiLevel     | [Vgder State](msdn-online-vml-vgtristate.md). Zeigt das Bild nur in zwei Farben an (normalerweise schwarz und weiß).                                                                                                                                                                                                                                                     |
| Blacklevel  | [Vgbruchteile](msdn-online-vml-vgfraction-data-type.md). Ermöglicht die Anpassung, um die Ebene so festzulegen, dass schwarze als echte schwarze angezeigt werden und alle anderen Farben als Schattierungen über schwarz sichtbar sind.                                                                                                                                                                        |
| Chromakey   | [Ivgcolor](msdn-online-vml-ivgcolor.md). Transparente Farbe des Bilds.                                                                                                                                                                                                                                                                                         |
| CropBottom  | [Vgnumber](#data-types-used-in-the-vml-object-model). Der Abstand von der unteren Seite des Bilds wird als Prozentsatz der Bildgröße ausgedrückt.                                                                                                                                                                                                                           |
| Durchforsten    | [Vgnumber](#data-types-used-in-the-vml-object-model). Die Entfernung von der linken Kante des Bilds wird als Bruchteil der Bildgröße ausgedrückt (von 0,0 bis 1,0). "Out-Zuschneiden" wird jedoch unterstützt. Daher werden Werte kleiner als 0 und größer als 1 unterstützt. Beispielsweise würde-5, 20 die Begrenzungen 25 x der Bildgröße mit 4/5 auf einer Seite des Bilds überschneiden. |
| Durchschnitt   | [Vgnumber](#data-types-used-in-the-vml-object-model). Der Entfernungs Abstand von der rechten Seite des Bilds, ausgedrückt als Prozentsatz der Bildgröße.                                                                                                                                                                                                                            |
| CropTop     | [Vgnumber](#data-types-used-in-the-vml-object-model). Die Entfernung von der Oberkante des Bilds wird als Prozentsatz der Bildgröße ausgedrückt.                                                                                                                                                                                                                              |
| Embosscolor | [Ivgcolor](msdn-online-vml-ivgcolor.md). Dies wird auf einen Prozentsatz der Schatten Farbe festgelegt, um einen geprägten Bildeffekt zu erstellen.                                                                                                                                                                                                                                 |
| Erzielen        | [Vgpositivenumschlag](#data-types-used-in-the-vml-object-model). Passt die Intensität aller Farben an. Legt im Grunde fest, wie hell weiß sein wird. Liegt zwischen 0 und 32767.                                                                                                                                                                                           |
| Gamma       | [Vgbruchteile](msdn-online-vml-vgfraction-data-type.md). Gamma Korrektur. Das Erhöhen des Bilds bietet einem Bild einen größeren Kontrast.                                                                                                                                                                                                                                           |
| GrayScale   | [Vgder State](msdn-online-vml-vgtristate.md). Bild in Graustufen Farben anzeigen.                                                                                                                                                                                                                                                                              |
| Src         | [Zeichenfolge](#data-types-used-in-the-vml-object-model). Die URL zu einem Bild, das für Bild-und Muster Füllungen geladen werden soll. Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird.                                                                                                                                                           |



 

### <a name="path-element"></a>Path-Element

Definiert den Pfad, der die Form bildet, mithilfe einer Zeichenfolge, die einen umfangreichen Satz von "Pen Movement"-Befehlen enthält.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Limo</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>. Definiert den Punkt, an dem die Form gestreckt wird. Beispielsweise würde sich der Limo-Punkt für eine Giraffen-Form auf dem Hals befinden, sodass bei der Größenänderung der Form der Hals gestreckt wird und der Rest der Form seine Dimensionen beibehält.</td>
</tr>
<tr class="even">
<td>Textboxrect</td>
<td><a href="#data-types-used-in-the-vml-object-model">Ivgfixedrechglearray</a>. Ein Array mit den Rechtecke, die definieren, wohin Text wechseln soll.</td>
</tr>
<tr class="odd">
<td>V</td>
<td><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>. Entspricht dem v-Attribut des Path-Tags. Beachten Sie, dass path möglicherweise dem Pfad Attribut oder dem Element entspricht.</td>
</tr>
<tr class="even">
<td>Wert</td>
<td><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>. Eine Textdarstellung der Befehle, die den Pfad definieren. X-oder y-Koordinaten Werte können ein Verweis auf eine Formel in der Form sein &quot; @# &quot; , wobei # die Ordinalzahl der Formel (z. b.) ist &quot; @2 &quot; . Diese Attribut Zeichenfolge besteht aus einem umfangreichen Satz von Befehlen, einschließlich der folgenden: <br/> 
<table>
<thead>
<tr class="header">
<th>Get-Help</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AE (angleelliponto)</td>
<td><strong>Mittelpunkt</strong>(x, y) <strong>Größe</strong>(w, h) <strong>anfangs Winkel</strong>, <strong>Endwinkel</strong><br/> Zeichnen Sie ein Segment einer Ellipse. Eine gerade Linie wird vom aktuellen Punkt bis zum Startpunkt des Segments gezeichnet.<br/></td>
</tr>
<tr class="even">
<td>Al (angleelipse)</td>
<td>Identisch mit AE, mit dem Unterschied, dass es ein implizites m bis zum Ausgangspunkt des Segments gibt.</td>
</tr>
<tr class="odd">
<td>AR (Bogen)</td>
<td>Identisch mit. Ein neuer Unterpfad wird jedoch von einem impliziten m bis zum Anfangspunkt des Bogens gestartet.</td>
</tr>
<tr class="even">
<td>at (ArcTo)</td>
<td><strong>left</strong>, <strong>Top</strong>, <strong>right</strong>, <strong>Bottom</strong>, <strong>Start</strong>(x, y) <strong>End</strong>(x, y) <br/> Die ersten vier Werte definieren das umgebende Feld einer Ellipse. Die letzten vier definieren zwei radiale Vektoren. Ein Segment der Ellipse wird gezeichnet, das mit dem durch den Start RADIUS-Vektor definierten Winkel beginnt und mit dem durch den endvektor definierten Winkel endet. Eine gerade Linie wird vom aktuellen Punkt bis zum Anfang des Bogens gezeichnet. Der Bogen wird immer in der Richtung gegen den Uhrzeigersinn gezeichnet. <br/></td>
</tr>
<tr class="odd">
<td>c (Cursor)</td>
<td><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>bis</strong>(x, y) <br/> Zeichnen Sie eine kubische Bézier-Kurve vom aktuellen Punkt bis zur Koordinate, die von den letzten beiden Parametern angegeben wird, und die von den ersten vier Parametern angegebenen Steuerungs Punkte. Der aktuelle Punkt wird zum Endpunkt des bezierers.<br/></td>
</tr>
<tr class="even">
<td>e (Ende)</td>
<td>Beendet den aktuellen Satz von unter Pfaden. Ein angegebener Satz von unter Pfaden (wie durch Ende getrennt) wird mithilfe von eofill gefüllt. Nachfolgende Sätze von unter Pfaden werden unabhängig voneinander aufgefüllt und für vorhandene festgelegt.</td>
</tr>
<tr class="odd">
<td>l (LineTo)</td>
<td>x, y<br/> Zeichnen Sie eine Linie vom aktuellen Punkt bis zur angegebenen x-, y-Koordinate, die zum neuen aktuellen Punkt wird. Es können zusätzliche Koordinatenpaare angegeben werden, um eine Polylinie zu bilden, z. b. &quot; l 10, 13, 45, 27, 89,-12 &quot; .<br/></td>
</tr>
<tr class="even">
<td>m (muveto)</td>
<td>x, y<br/> Startet einen neuen unter Pfad an der angegebenen x-, y-Koordinate.<br/></td>
</tr>
<tr class="odd">
<td>NF (nofill)</td>
<td>Der aktuelle Satz von unter Pfaden (durch Ende getrennt) wird nicht ausgefüllt.</td>
</tr>
<tr class="even">
<td>NS (noStroke)</td>
<td>Der aktuelle Satz von unter Pfaden (durch Ende getrennt) wird nicht mit Strichen gezeichnet.</td>
</tr>
<tr class="odd">
<td>QB (quadraticbezier)</td>
<td>(<strong>ControlPoint</strong>(x, y)) *,<strong>Ende</strong>(x, y) <br/> Definiert eine oder mehrere Quadratische Bézier-Kurven mithilfe von Steuerungs Punkten und einem Endpunkt. Intermediate (On-Curve)-Punkte werden durch Interpolationen zwischen aufeinander folgenden Steuerungs Punkten abgerufen, ähnlich wie TrueType-Schriftarten. Der Unterpfad muss kein Start sein. in diesem Fall wird der Unterpfad geschlossen, und der letzte Punkt definiert den Startpunkt.<br/></td>
</tr>
<tr class="even">
<td>QX (ellipticalquadrantx)</td>
<td><strong>Ende</strong>(x, y) <br/> Eine Quartals Ellipse wird vom aktuellen Punkt zum angegebenen Endpunkt gezeichnet. Das elliptische Segment ist anfänglich tangential zu einer Zeile parallel zur x-Achse. Das Segment wird also horizontal gestartet.<br/></td>
</tr>
<tr class="odd">
<td>Qy (ellipticalquadranty)</td>
<td><strong>Ende</strong>(x, y) <br/> Identisch mit QX, mit dem Unterschied, dass das elliptische Segment anfänglich tangential zu einer Zeile parallel zur y-Achse ist. Dies bedeutet, dass das Segment vertikal beginnt.<br/></td>
</tr>
<tr class="even">
<td>r (rlineto)</td>
<td>x, y <br/> Zeichnen Sie eine Linie vom aktuellen Punkt bis zur relativen Koordinate (CPX + x, cpy + y). Wenn zusätzliche Koordinatenpaare angegeben werden, wird jeder neue Punkt relativ zum letzten Wert berechnet.<br/></td>
</tr>
<tr class="odd">
<td>t (rmuveto)</td>
<td>x, y<br/> Starten Sie einen neuen untergeordneten Pfad an den relativen Koordinaten (CPX + x, cpy + y), wobei CPX, cpy die aktuelle Position ist. <br/></td>
</tr>
<tr class="even">
<td>v (Cursor)</td>
<td><strong>Control1</strong>(x, y) <strong>Control2</strong>(x, y) <strong>bis</strong> (x, y) <br/> Eine kubische Bézier-Kurve, die die angegebenen Koordinaten relativ zum aktuellen Punkt verwendet. Alle Punkte werden relativ zum gleichen Ausgangspunkt berechnet.<br/></td>
</tr>
<tr class="odd">
<td>WA (clockwisearcto)</td>
<td>Identisch mit, aber der Bogen wird in Richtung im Uhrzeigersinn gezeichnet.</td>
</tr>
<tr class="even">
<td>WR (clockwisearc)</td>
<td>Identisch mit AR, wird aber in Richtung des Uhrzeigersinn gezeichnet.</td>
</tr>
<tr class="odd">
<td>x (schließen)</td>
<td>Schließen Sie den aktuellen untergeordneten Pfad, indem Sie eine gerade Linie von der aktuellen Punkt-zum ursprünglichen muvepoint zeichnen.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a>Shadow-Element

Beschreibt einen Schatteneffekt für eine Form.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">Ivgcolor</a>. Farbe des primär Schattens. Der Standardwert ist RGB (128128128).</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">Ivgcolor</a>. Farbe des zweiten Schattens oder hervorheben in einem geprägten oder einschenden Schatten. Der Standardwert ist RGB (203203203).</td>
</tr>
<tr class="odd">
<td>Matrix</td>
<td><a href="#data-types-used-in-the-vml-object-model">Ivgskewmatrix</a>. Eine perspektivische Transformationsmatrix in Form von &quot; Sxx, sxy, syx, SYY, px, PY &quot; [s = Scale, p = Perspective]. Die s-Elemente geben an, wie der Schatten in Bezug auf die Form skaliert werden soll, und die p-Elemente geben an, wie der Schatten in Bezug auf die Form verzerrt werden soll. In der folgenden Matrix wird z. b. die Form um den Faktor 2 angepasst und um den Faktor 4 in alle Richtungen geneigt: <br/> &quot;2, 2, 2, 4, 4&quot;<br/> Diese Matrix wird nur verwendet, wenn der Typ des Schattens auf Perspective festgelegt ist.<br/></td>
</tr>
<tr class="even">
<td>Verdeckt</td>
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. Der Schatten kann durchsucht werden, wenn die Form nicht ausgefüllt ist. Der Standardwert lautet False.</td>
</tr>
<tr class="odd">
<td>Offset</td>
<td><a href="#data-types-used-in-the-vml-object-model">Ivgskewoffset</a>. Die Menge des x-, y-Offsets vom Speicherort der Form. Der Standardwert ist &quot; 2pt, 2pt &quot; .</td>
</tr>
<tr class="even">
<td>Offset2</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Die Menge des x, y Sekunden Offsets von der Form? s. Werte sind entweder eine absolute Messung oder ein Bruchteil der Form (-0,5 bis + 0,5).</td>
</tr>
<tr class="odd">
<td>Ein</td>
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. Schaltet die Anzeige des Schattens ein und aus.</td>
</tr>
<tr class="even">
<td>Opacity</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">Vgbruchteile</a>. Deckkraft des Schatten Effekts.</td>
</tr>
<tr class="odd">
<td>Origin</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Ein paar von Bruchteil-Werten von-0,5 bis + 0,5.</td>
</tr>
<tr class="even">
<td>type</td>
<td><a href="#data-types-used-in-the-vml-object-model">Vgshadowtype</a>. Gültige Werte:
<ul>
<li>Single (Standard)</li>
<li>Double</li>
<li>Perspektive</li>
<li>Shaperelative</li>
<li>Drawingrelative</li>
<li>Emboss</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a>Verzerrt-Element

Beschreibt einen perspektivischen perspektivischen Effekt auf eine Form. Die Schiefe wird auf Vektorgrafik Daten, nicht auf Bilddaten angewendet.



|        |                                                                                                                                                                                                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Matrix | [Ivgskewmatrix](#data-types-used-in-the-vml-object-model). Eine perspektivische Transformationsmatrix in der Form "Sxx, sxy, syx, SYY, px, py" \[ s = Scale, p = Perspective \] . Wenn Offset in absoluten Einheiten ist, befinden sich px und py in den Einheiten "EMU ^-1". andernfalls handelt es sich um einen umgekehrten Bruchteil der Shape-Größe. |
| Offset | [Ivgskewoffset](#data-types-used-in-the-vml-object-model). Die Menge des x-, y-Offsets vom Speicherort der Form. Der Standardwert ist "2pt, 2pt".                                                                                                                                                   |
| Ein     | [Vgder State](msdn-online-vml-vgtristate.md). Schaltet die Anzeige der Schiefe ein bzw. aus.                                                                                                                                                                                             |
| Origin | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Ein paar von Bruchteil-Werten von-0,5 bis + 0,5.                                                                                                                                                                     |



 

### <a name="stroke-element"></a>Stroke-Element

Beschreibt das Zeichnen des Pfads, wenn etwas über eine voll tonlinie hinaus mit einer voll Tonfarbe gewünscht ist.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Color</td>
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. Die Farbe der Linie. Identisch mit dem Attribut "strokeColor" in Form, überschreibt es jedoch.</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">Ivgcolor</a>. Sekundärfarbe. Wird verwendet, wenn FillType den Wert Pattern hat.</td>
</tr>
<tr class="odd">
<td>DashStyle</td>
<td><strong>Vglinedashstyle</strong>. Stil Format für Strich. Kann ein bestimmter Wert oder eine Sequenz von Zahlen mit einem benutzerdefinierten Bindestrich Muster sein. Gültige Werte:
<ul>
<li>Solid (Standard)</li>
<li>Shortdash</li>
<li>Kurzpunkt</li>
<li>Shortdashdot</li>
<li>Shortdashdotdot</li>
<li>Punkt</li>
<li>Strich</li>
<li>DashDot</li>
<li>Longdash</li>
<li>Longdashdot</li>
<li>Longdashdotdot</li>
</ul></td>
</tr>
<tr class="even">
<td>Umdarrow</td>
<td><strong>Vgarrowheadstyle</strong>. Arrowhead für das Ende der Zeile. Gültige Werte:
<ul>
<li>Keine (Standard)</li>
<li>Blockieren</li>
<li>Klassisch</li>
<li>Diamond</li>
<li>Oval</li>
<li>Öffnen</li>
<li>Chevron</li>
<li>Doublechevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>"Tdarrowlength"</td>
<td><strong>Vgarrowheadlength</strong>. Pfeilspitzen Länge für das Ende der Zeile. Gültige Werte:
<ul>
<li>Short</li>
<li>Mittel (Standard)</li>
<li>Long</li>
</ul></td>
</tr>
<tr class="even">
<td>"-Rowwidth"</td>
<td><strong>Vgarrowheadwidth</strong>. Pfeilspitze Breite für das Ende der Zeile. Gültige Werte:
<ul>
<li>Verringern</li>
<li>Mittel (Standard)</li>
<li>Breite</li>
</ul></td>
</tr>
<tr class="odd">
<td>EndCap</td>
<td><strong>Vglineendcapstyle</strong>. Gültige Werte:
<ul>
<li>Flach</li>
<li>Square</li>
<li>Round</li>
</ul></td>
</tr>
<tr class="even">
<td>FillType</td>
<td><strong>Vglinefilltype</strong>. Gültige Werte:
<ul>
<li>Solid (Standard)</li>
<li>Tile</li>
<li>Muster</li>
<li>Frame</li>
</ul></td>
</tr>
<tr class="odd">
<td>Imagealignshape</td>
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. Richten Sie das Bild mit der Form aus. Wenn false, wird das Bild mit dem Fenster ausgerichtet.</td>
</tr>
<tr class="even">
<td>Imageaspekt</td>
<td><strong>Vgaspecttype</strong>. Das ImageSize-Attribut wird angepasst, um den Aspekt des Bilds zu erhalten. Mögliche Werte:
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignorieren</td>
<td>Ignoriert Aspekte von Aspekten.</td>
</tr>
<tr class="even">
<td>Mindestens</td>
<td>Image ist mindestens so groß wie die Bildgröße.</td>
</tr>
<tr class="odd">
<td>Höchstens</td>
<td>Das Bild ist nicht größer als die Bildgröße.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>ImageSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Größe des Bilds, mit dem der Pinsel gebildet werden soll. Der Standardwert ist die Größe des Bilds.</td>
</tr>
<tr class="even">
<td>JOINSTYLE</td>
<td><strong>Vglinejoinstyle</strong>. Gültige Werte:
<ul>
<li>Round (abgerundetes gemeinsames)</li>
<li>Abgeschrägte (abgeschrägte Verbindung)</li>
<li>Miter (Miter Joint)</li>
</ul></td>
</tr>
<tr class="odd">
<td>LineStyle</td>
<td><strong>Vglinestyle</strong>. Gültige Werte:
<ul>
<li>Single</li>
<li>Thin Thin (1:1:1)</li>
<li>Thin Thick (1:1:2)</li>
<li>Dickdünn (2:1:1)</li>
<li>Thickbetweenthin (1:1:2:1:1)</li>
</ul></td>
</tr>
<tr class="even">
<td>MiterLimit</td>
<td><a href="msdn-online-vml-vglength.md">Länge</a>. Der maximale Abstand zwischen dem inneren und dem äußeren Punkt eines gemeinsamen Punkts. Diese Zahl ist ein Vielfaches der Linienstärke. Liegt zwischen 0 und 32.767.</td>
</tr>
<tr class="odd">
<td>Ein</td>
<td><a href="msdn-online-vml-vgtristate.md">Vgder State</a>. Schaltet die Anzeige der Zeile ein und aus. Identisch mit dem Stroke-Attribut in Form, überschreibt es jedoch.</td>
</tr>
<tr class="even">
<td>Opacity</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">Vgbruchteile</a>. Deckkraft des Strichs.</td>
</tr>
<tr class="odd">
<td>Src</td>
<td>Eine Zeichenfolge. Die URL zu einem Bild, das für Bild-und Muster Füllungen geladen werden soll. Dieses Attribut muss immer vorhanden sein und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird.</td>
</tr>
<tr class="even">
<td>Startarrow</td>
<td><strong>Vgarrowheadstyle</strong>. Pfeilspitze für den Anfang der Zeile. Gültige Werte:
<ul>
<li>Keine (Standard)</li>
<li>Blockieren</li>
<li>Klassisch</li>
<li>Diamond</li>
<li>Oval</li>
<li>Öffnen</li>
<li>Chevron</li>
<li>Doublechevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>Startarrowlength</td>
<td>Vgarrowheadlength. Pfeilspitzen Länge für den Anfang der Zeile. Gültige Werte:
<ul>
<li>Short</li>
<li>Mittel (Standard)</li>
<li>Long</li>
</ul></td>
</tr>
<tr class="even">
<td>Startarrowwidth</td>
<td>Vgarrowheadwidth. Pfeilspitzen Breite für den Anfang der Zeile. Gültige Werte:
<ul>
<li>Schmale mittlere Breite (Standard)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Weight</td>
<td><a href="msdn-online-vml-vglength.md">Vglength</a>. Breite der Zeile. Liegt zwischen 0 und 1584.
<div class="alert">
<blockquote>
[!Note]<br />
Mit dem Attribut "Dashboard" kann der Benutzer ein benutzerdefiniertes Bindestrich Muster angeben. Dies erfolgt mithilfe einer Reihe von Zahlen. Dash-Stile werden in Bezug auf die Länge des Bindestrichs (der gezeichnete Teil des Strichs) und die Länge des leer Zeichens zwischen den Bindestrichen definiert. Die Längen sind relativ zur Linienstärke. &quot;die Länge 1 &quot; ist gleich der Linienstärke. Der EndCap-Stil wird auf jeden Bindestrich angewendet, Pfeil Stile nicht. Die Zeichenfolge definiert zuerst die Länge des Bindestrichs und dann die Länge des Leerraums. Dies wird möglicherweise wiederholt, um komplexe Dash-Stile zu bilden. Die Zeichenfolge sollte immer ein Zahlenpaar enthalten. Wenn Sie eine ungerade Anzahl von Zahlen enthält, werden die letzten möglicherweise ignoriert. In der folgenden Tabelle sind einige typische Werte und eine Beschreibung des beabsichtigten Effekts aufgeführt. &quot;0 &quot; impliziert einen Punkt, der vierfache symmetrisch sein sollte (bei roundendpunkten sollte er ein Kreis sein). Wenn das Zeilen endlimit flach ist, sollte ein Viewer, sofern möglich, einen integrierten Betriebssystem-Dash auswählen (d.h. etwas, das schnell gezeichnet werden kann). Im folgenden finden Sie einige Beispiele.
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td>&quot;2 2&quot;</td>
<td>kurzstriche (jeder Bindestrich und der zwischen Raum in der Zwischenzeit ist die doppelte Breite der Linie)</td>
</tr>
<tr class="even">
<td>&quot;1 2&quot;</td>
<td>Punkt (jeder Bindestrich ist die Breite der Linie, während jeder Leerraum doppelt so breit ist wie die Linie)</td>
</tr>
<tr class="odd">
<td>&quot;4 2&quot;</td>
<td>Dash (jeder Bindestrich ist viermal so breit wie die Breite der Linie)</td>
</tr>
<tr class="even">
<td>&quot;8 2&quot;</td>
<td>langer Bindestrich</td>
</tr>
<tr class="odd">
<td>&quot;4 2 1 2&quot;</td>
<td>Bindestrich Punkt</td>
</tr>
<tr class="even">
<td>&quot;8 2 1 2&quot;</td>
<td>Long-Dash-Punkt</td>
</tr>
<tr class="odd">
<td>&quot;8 2 1 2 1 2&quot;</td>
<td>Long-Dash-Punkt Punkt</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a>TextPath-Element

Beschreibt einen Vektor Pfad basierend auf den angegebenen Textdaten, Schriftart und Stilen. Wenn ein Pfad Element angegeben wird, wird der Textpfad nach der Angabe an ein **Pfad** Element geleitet.



|          |                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| Fitpath  | [Vgder State](msdn-online-vml-vgtristate.md). Gibt den Text an, um den Pfad auszufüllen, in dem er sich befindet.                                 |
| Fitshape | [Vgder State](msdn-online-vml-vgtristate.md). Streckt den Textpfad auf die Ränder des Form Felds.                      |
| Ein       | [Vgder State](msdn-online-vml-vgtristate.md). Bestimmt, ob die Zeichen Pfade angezeigt werden.                    |
| String   | Eine Zeichenfolge. Der Text, der als Textpfad dargestellt werden soll.                                                                                    |
| Glätten     | [Vgder State](msdn-online-vml-vgtristate.md). Entfernt alle zusätzlichen Speicherplatz, die für Vorgänger und Nachfolger reserviert sind, wenn Sie nicht verwendet werden. |
| XScale   | [Vgder State](msdn-online-vml-vgtristate.md). Verwenden Sie die gerade x-Messung anstelle des Pfads.                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a>Im VML-Objektmodell verwendete Datentypen

Die folgenden Datentypen werden vom VML-Objektmodell verwendet.

-   [Double](/windows)
-   [Fest](/windows)
-   [Integer](/windows)
-   [Ivganpassungen](/windows)
-   [Ivgcolor](/windows)
-   [Ivgequation](/windows)
-   [Ivgfixedrechteck](/windows)
-   [Ivgfixedrechglearray](/windows)
-   [Ivgformula](/windows)
-   [Ivgformeln](/windows)
-   [Ivggradientcolorarray](/windows)
-   [Ivgpoints](/windows)
-   [Ivgskewmatrix](/windows)
-   [Ivgskewoffset](/windows)
-   [IVgVector2D](/windows)
-   [IVgVector3D](/windows)
-   [Länge](/windows)
-   [Measure](/windows)
-   [String](/windows)
-   [Vgblackwhitemode](/windows)
-   [Vgbruchteile](/windows)
-   [Vgvstate](/windows)

**Double-Datentyp**

Eine ganze Zahl mit doppelter Genauigkeit mit einem Bereich von-unendlich bis unendlich.

**Fester Datentyp**

Gleit Komma Zahl mit einem Bereich von-32.766,0 bis 32.766,0.

**Integer-Datentyp**

Eine ganze Zahl mit einem Bereich von-unendlich bis unendlich.

**Ivganpassungen-Datentyp**

Sammlung von Anpassungen einer Form, die zum Ändern der Abmessungen einer Form verwendet werden kann. Anpassungen können als temporäre Platzhalter verwendet werden, oder Sie können aus irgendeinem Grund Variablen verwenden. Es gibt nur 8 Anpassungen in der Sammlung.



| Attribute | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exists     | [Ivgtrstate](msdn-online-vml-vgtristate.md). Bestimmt, ob eine angegebene Anpassung vorhanden ist. Beachten Sie, dass ein Index verwendet werden muss. Das heißt, "vorhanden" (Element) muss verwendet werden, um das vorhanden sein eines Elements abzurufen.                                                                                                                                                                   |
| Element       | [Long](#data-types-used-in-the-vml-object-model). Ein Array von Anpassungen, die von 0 bis 7 indiziert wurden. Beachten Sie, dass die Anpassungen möglicherweise sparsam angegeben werden. Das heißt, zwischen Array Werte können nicht immer ausgefüllt werden. Beispielsweise können Element 1, 3 und 5 Werte für eine Länge von 3 aufweisen, wobei Item (0), Item (2) und Item (4) angegeben sind. Um festzustellen, ob ein Element vorhanden ist, verwenden Sie das vorhanden sein-Attribut. |
| Länge     | [Integer](#data-types-used-in-the-vml-object-model). Anzahl der Anpassungen. Darf nicht größer als 8 sein.                                                                                                                                                                                                                                                                          |
| Wert      | [Zeichenfolge](#data-types-used-in-the-vml-object-model). Text Darstellung numerischer Werte mit Kommas zwischen den einzelnen Zahlen.                                                                                                                                                                                                                                                    |



 

**Ivgcolor**

Gibt eine Farbe an.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>RGB</td>
<td><strong>Vgrgbtype</strong>. RGB-Wert (Long) der Farbe. Nur gültig, wenn der Typ RGB ist.</td>
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
<td><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>. Text Darstellung der Farbe. Die folgenden benannten Farb Typen werden unterstützt:
<ul>
<li>Schwarz (#000000)</li>
<li>Silber (#C0C0C0)</li>
<li>Grau (#808080)</li>
<li>Weiß (#FFFFFF)</li>
<li>Maroon (#800000)</li>
<li>Rot (#FF0000)</li>
<li>Lila (#800080)</li>
<li>Fuchsia (#FF00FF)</li>
<li>Grün (#008000)</li>
<li>Kalk (#00FF00)</li>
<li>Oliv (#808000)</li>
<li>Gelb (#FFFF00)</li>
<li>Navy (#000080)</li>
<li>Blau (#0000FF)</li>
<li>Teal (#008080)</li>
<li>Aqua (#00FFFF)</li>
</ul></td>
</tr>
<tr class="even">
<td>type</td>
<td><strong>Vgcolortype</strong>. Der Typ der Farbe. Einer der folgenden Typen:
<ul>
<li>Mixed</li>
<li>benannt</li>
<li>RGB</li>
<li>Schema</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Ivgequation**

Für Formeln verwendete Gleichungen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Vorgang</td>
<td><strong>Vgequationoperationtype</strong> Der Name des Vorgangs, der für die Parameter durchgeführt werden soll. Die folgenden Vorgänge können in einer Gleichung verwendet werden:
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
<td>Absoluter Wert. <br/> <strong>ABS</strong>(v) <br/></td>
</tr>
<tr class="even">
<td>Atan2</td>
<td>Polar Arithmetik: führt zu FD-Einheiten (Grad multipliziert mit 65536).<br/> <strong>atan2</strong>(P1, v) <br/></td>
</tr>
<tr class="odd">
<td>Cos</td>
<td>Kosinus, Argument in FD-Einheiten (Grad multipliziert mit 65536).<br/> v * <strong>cos</strong>(P1) <br/></td>
</tr>
<tr class="even">
<td>Cosatan2</td>
<td>Behält die vollständige Genauigkeit in der zwischen Berechnung bei.<br/> v * <strong>cos (atan2 (</strong> P2, P1 <strong>))</strong><br/></td>
</tr>
<tr class="odd">
<td>Ellipse</td>
<td>Ellipse</td>
</tr>
<tr class="even">
<td>Wenn</td>
<td>Bei Bedingungs Test. v > 0 <strong>?</strong> P1: P2</td>
</tr>
<tr class="odd">
<td>Max.</td>
<td>Der größere von zwei-Werten. <br/> <strong>Max</strong>(v, P1) <br/></td>
</tr>
<tr class="even">
<td>Mid</td>
<td>Durchschnitt (v + P1)/2</td>
</tr>
<tr class="odd">
<td>Min</td>
<td>Der kleinere von zwei-Werten. <strong>Min</strong>(v, P1)</td>
</tr>
<tr class="even">
<td>Mod</td>
<td>Modulo</td>
</tr>
<tr class="odd">
<td>Produkt</td>
<td>Wird für Multiplikation und Division verwendet. v * P1/P2</td>
</tr>
<tr class="even">
<td>Sin</td>
<td>Sinus, Argument in FD-Einheiten (Grad multipliziert mit 65536). <br/> v * <strong>Sin</strong>(P1) <br/></td>
</tr>
<tr class="odd">
<td>Sinatan2</td>
<td>Behält die vollständige Genauigkeit in der zwischen Berechnung bei. v * <strong>Sin</strong>(<strong>atan2</strong>(P2, P1))</td>
</tr>
<tr class="even">
<td>Sqrt</td>
<td>Das Ergebnis ist positiv und wird abgerundet. <br/> <strong>sqrt</strong>(v) <br/></td>
</tr>
<tr class="odd">
<td>SUM</td>
<td>Wird für Addition und Subtraktion verwendet.<br/> v + P1 P2<br/></td>
</tr>
<tr class="even">
<td>Sumangle</td>
<td>Vorhandener Winkel (skaliert durch 65536), wobei P1 und P2 in Grad liegen.<br/> v + P1 * 65536 + P2 * 65536<br/></td>
</tr>
<tr class="odd">
<td>Tan</td>
<td>Tangens, Argument in FD-Einheiten (Grad multipliziert mit 65536). <br/> v * Tan (P1)<br/></td>
</tr>
<tr class="even">
<td>Val</td>
<td>Definiert einen Führungs Wert aus einem anderen Wert.</td>
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
<td><strong>Vgformulaparamtype</strong>. Der Typ des ersten Parameters. Die folgenden Werte werden unterstützt:
<table>
<thead>
<tr class="header">
<th>type</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Wert</td>
<td>Der Parameter ist ein einfacher Wert.</td>
</tr>
<tr class="even">
<td>"Anpassungen Reference"</td>
<td>Der-Parameter ist ein Verweis auf eine-Anpassung. Wenn der erste Parameter z. b. 1 ist, wird der Wert der ersten Anpassung verwendet.</td>
</tr>
<tr class="odd">
<td>Formulareferenzierung</td>
<td>Der-Parameter ist das Ergebnis eines Verweises auf das Ergebnis einer vorherigen Formel. Wenn der erste Parameter z. b. 2 ist, wird das Ergebnis von Formel 2 verwendet.</td>
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
<td><strong>Vgformulaparamtype</strong> Der Typ des Parameters 2.</td>
</tr>
<tr class="even">
<td>Val</td>
<td><strong>Integer</strong>. Das Ergebnis.</td>
</tr>
<tr class="odd">
<td>Valtype2</td>
<td><strong>Vgformulaparamtype</strong>. Der Typ des Ergebnisses.</td>
</tr>
</tbody>
</table>



 

**Ivgfixedrechteck**

Gibt ein festes Rechteck an.



| Attribute | BESCHREIBUNG                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Wert      | [Zeichenfolge](#data-types-used-in-the-vml-object-model). Textwert, der den Pfad angibt.         |
| Links       | [Double](#data-types-used-in-the-vml-object-model). Ganz links-Koordinate des Rechtecks.   |
| Oben        | [Double](#data-types-used-in-the-vml-object-model). Oberste Koordinate des Rechtecks.    |
| Rechts      | [Double](#data-types-used-in-the-vml-object-model). Rechte Koordinate des Rechtecks.  |
| bottom     | [Double](#data-types-used-in-the-vml-object-model). Die untersten Koordinaten des Rechtecks. |



 

**Ivgfixedrechglearray**

Array fester Rechtecke.



| Attribute | BESCHREIBUNG                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| Wert      | [Zeichenfolge](#data-types-used-in-the-vml-object-model). Text Darstellung des Arrays.                           |
| Länge     | [Integer](#data-types-used-in-the-vml-object-model). Anzahl der Rechtecke in diesem Array.                    |
| Element       | [Ivgfixedrechteck](#data-types-used-in-the-vml-object-model). Das Rechteck Objekt am angegebenen Index. |



 

**Ivgformula-** Datentyp

Definitionen für Formeln, die den Pfad einer Form variieren oder zu anderen Berechnungs Zwecken verwendet werden können. Formeln können auf dem **ADJ** -Attribut einer Form basieren, die sich ändern kann. Formeln können auch auf andere Formeln verweisen.



| Attribute | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                          |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eqn        | [Ivgequation.](#data-types-used-in-the-vml-object-model) Jede Formel definiert einen einzelnen Wert als Ergebnis der Auswertung des Ausdrucks. Der Ausdruck wird durch dieses Attribut definiert und verfügt über die allgemeine Form eines Vorgangs, gefolgt von bis zu drei Argumenten, bei denen es sich um Anpassungs Werte (z. b. \# 2), die Ergebnisse früherer Formeln (z. b. @2 ), festgelegte Zahlen oder vordefinierte Werte handeln kann. |



 

**Ivgformeln-Datentyp**

Eine Auflistung von Formel Objekten.



| Attribute | BESCHREIBUNG                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Länge     | [Integer](#data-types-used-in-the-vml-object-model). Anzahl der Formel Objekte in der Sammlung.                                                |
| Element       | [Ivgformula](#data-types-used-in-the-vml-object-model). Eine bestimmte Formel. Beachten Sie, dass das Formel Array den Shape-Typ als Abbildung vererbt werden kann. |



 

**Ivggradientcolorarray**

Ein Array von Farben, die einen Farbverlauf (gemischter Bereich von Farben) definieren.



| Attribute | BESCHREIBUNG                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| Wert      | [Zeichenfolge](#data-types-used-in-the-vml-object-model). Gibt das Array von Farben an. Beispiel: "Red. 2; grün. 4; schwarz. 7 " |
| Länge     | [Integer](#data-types-used-in-the-vml-object-model). Anzahl der Farben im Array.                                          |



 



| Methoden     | BESCHREIBUNG                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Addcolor    | [Vgbruchteile](msdn-online-vml-vgfraction-data-type.md). Fügt eine neue Farbe an dem Durchbruch angegebenen Endpunkt hinzu. Die neue Farbe ist standardmäßig weiß und ist der Rückgabewert. Die Farbe kann dann als Verweis geändert werden. |
| Removecolor | [Vgbruchteile](msdn-online-vml-vgfraction-data-type.md). Entfernt eine Farbe an einem Endpunkt, der durch einen Bruchteil angegeben wird. Hinweis: Wenn 0,0 oder 1,0 nicht vorhanden ist, wird dies impliziert und die Farbe weiß an diesem Punkt verwendet.          |



 

**Ivgpoints-Datentyp**

Ein Array von Punkten, die eine Form definieren.



| Attribute | BESCHREIBUNG                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Wert      | [Zeichenfolge](#data-types-used-in-the-vml-object-model). Text Darstellung des Arrays.           |
| Länge     | [Integer](#data-types-used-in-the-vml-object-model). Anzahl der Punkte in diesem Array.        |
| Element       | [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md). Der Punkt am angegebenen Index. |



 

**Ivgskewmatrix-Datentyp**

Eine Matrix, die für verzerrende Formen verwendet wird, eine perspektivische Transformationsmatrix in der Form "*Sxx, sxy, syx, SYY, px, PY* " \[ *s* = Scale, *p* = Perspective \] . Wenn Offset in absoluten Einheiten ist, befinden sich *px und py* in den Einheiten "EMU ^-1". andernfalls handelt es sich um einen umgekehrten Bruchteil der Shape-Größe.



| Attribute   | BESCHREIBUNG                                         |
|--------------|-----------------------------------------------------|
| Xtox         | [Double](#data-types-used-in-the-vml-object-model). |
| Ytox         | [Double](#data-types-used-in-the-vml-object-model). |
| Xtoy         | [Double](#data-types-used-in-the-vml-object-model). |
| Ytoy         | [Double](#data-types-used-in-the-vml-object-model). |
| Perspectivex | [Double](#data-types-used-in-the-vml-object-model). |
| Perspectivey | [Double](#data-types-used-in-the-vml-object-model). |



 

**Ivgskewoffset**

Gibt den Offset der Schiefe an.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Wert</td>
<td><a href="#data-types-used-in-the-vml-object-model">Zeichenfolge</a>. Text Darstellung des Offsets.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. X-Komponente. Prozentsatz oder Measure. Wenn keine Einheiten enthalten sind, wird der shaperelative Typ impliziert. Andernfalls wird der absolute Typ impliziert.</td>
</tr>
<tr class="odd">
<td>J</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Y-Komponente.</td>
</tr>
<tr class="even">
<td>type</td>
<td><strong>Vgskewtransformtype</strong>. Gibt den Typ der Transformation an. Gültige Werte sind ganzzahlige Punkte im Bereich von-unendlich und unendlich. 
<table>
<thead>
<tr class="header">
<th>type</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Shaperelative</td>
<td>Die Werte des Offsets sind Prozentsätze (Verhältnisse) der Größe der ursprünglichen Form. der Wert 0,5 bedeutet z. b. einen Offset der Hälfte der Form.</td>
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

Gibt einen zweidimensionalen Vektor an, der aus zwei **doppelten** Zahlen besteht.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Wert</td>
<td><strong>Zeichenfolge</strong>. Eine Text Darstellung beider Vektor Zahlen, die durch ein Leerzeichen voneinander getrennt sind.</td>
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
<td>type</td>
<td><strong>Vgvector Type</strong>. Erwartete Einheiten für diesen Vektor. Gültige Werte:
<ul>
<li>Measure</li>
<li>Länge</li>
<li>Angler</li>
<li>Fraction</li>
<li>Ganzzahl in Prozent</li>
</ul></td>
</tr>
</tbody>
</table>



 

**IVgVector3D-Datentyp**

Gibt einen dreidimensionalen Vektor an, der aus drei **doppelten** Zahlen besteht.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Wert</td>
<td><strong>Zeichenfolge</strong>. Text Darstellung von drei Vektor Zahlen, die durch ein Leerzeichen voneinander getrennt sind.</td>
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
<td>type</td>
<td><strong>Vgvector Type</strong>. Erwartete Einheiten für diesen Vektor. Gültige Werte:
<ul>
<li>Measure</li>
<li>Länge</li>
<li>Angler</li>
<li>Fraction</li>
<li>Zahl</li>
<li>Prozentsatz</li>
<li>Integer</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Length-Datentyp**

Eine Gleit Komma Zahl mit einem Bereich von 0 bis unendlich.

**Measure-Datentyp**

Eine Gleit Komma Zahl von-unendlich bis unendlich.

**String-Datentyp**

Zeichendaten beliebiger Länge.

**Vgblackwhitemode**

Renderingmodus für schwarz und weiß. Dabei sind folgende Werte möglich:

-   **Farbe**
-   **Automatisch**
-   **Graustufen**
-   **Lightgrayscale**
-   **Inverton**
-   **Grayoutline**
-   **Blacktextandlines**
-   **HighContrast**
-   **Schwarz**
-   **Weiß**
-   **Rückgängig machen**

**Vgbruchdatentyp**

Gleit Komma Zahl mit einem Bereich von 0,0 bis 1,0. Bruchzahlen können auch als Prozentsatz angegeben werden. z. b. "50%".

**Vgvstate-Datentyp**

Enumeration, die für Werte verwendet wird, die einen von drei Zuständen haben können:

-   **TRUE**
-   **FALSE**
-   **GEMISCHT**