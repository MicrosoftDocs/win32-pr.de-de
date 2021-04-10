---
title: Verwenden des Stroke-Elements
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Webworkshop, Stroke-Element
- Entwerfen von Webseiten, Stroke-Element
- Vector Markup Language (VML), Stroke-Element
- VML (Vector Markup Language), Stroke-Element
- Vektorgrafiken, Stroke-Element
- Stroke-Element
- VML-Elemente, Strich
- VML-Formen, Stroke-Element
- Vector Markup Language (VML), Eigenschafts Attribut für dashstile
- VML (Vector Markup Language), Eigenschafts Attribut für dashstile
- Vektorgrafiken, Eigenschafts Attribut für dashstile
- DashStyle-Eigenschafts Attribut
- Vector Markup Language (VML), Opacity-Eigenschafts Attribut
- VML (Vector Markup Language), Opacity-Eigenschafts Attribut
- Vektorgrafiken, Opacity-Eigenschafts Attribut
- Deck Kraft-Eigenschafts Attribut
- Vector Markup Language (VML), LineStyle-Eigenschafts Attribut
- VML (Vector Markup Language), LineStyle-Eigenschafts Attribut
- Vektorgrafiken, LineStyle-Eigenschafts Attribut
- LineStyle-Eigenschafts Attribut
- Vector Markup Language (VML), JOINSTYLE-Eigenschafts Attribut
- VML (Vector Markup Language), JOINSTYLE-Eigenschafts Attribut
- Vektorgrafiken, JOINSTYLE-Eigenschafts Attribut
- JOINSTYLE-Eigenschafts Attribut
- Vector Markup Language (VML), FillType-Eigenschafts Attribut
- VML (Vector Markup Language), FillType-Eigenschafts Attribut
- Vektorgrafiken, FillType-Eigenschafts Attribut
- FillType-Eigenschafts Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b58e02945884ea63ad1be01e67cfc156951cd5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316353"
---
# <a name="using-the-stroke-element"></a>Verwenden des Stroke-Elements

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Verwenden von `<stroke>`

Wie Sie gelernt haben, können Sie die Eigenschaften Attribute **strokeColor** und **strokeweight** einer vordefinierten Form (z. b. `<oval>` ,, `<line>` , `<polyline>` `<curve>` , `<rect>` ,,--) verwenden, `<roundrect>` `<arc>` um die Farbe und Gewichtung der Kontur einer Form anzugeben. In diesem Thema wird veranschaulicht, wie Sie eine Form mit einer erweiterten Gliederung zeichnen.

Sie können das `<stroke>` untergeordnete Element innerhalb des- `<shape>` ,-oder-Elements `<shapetype>` oder eines beliebigen vordefinierten Shape-Elements platzieren, um zu beschreiben, wie der Umriss der Form gezeichnet wird. Sie können dann die Eigenschafts Attribute (z. b. "Dashboard", " [Deck Kraft](#opacity)", " [LineStyle](#linestyle) [", "](#dashstyle) [JOINSTYLE](#joinstyle)", " [FillType](#filltype) ") des `<stroke>` unter Elements verwenden, um die Kontur anzupassen.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="dashstyle"></a>DashStyle

Sie können **das Eigenschafts** Attribut "Dashboard" des `<stroke>` unter Elements verwenden, um einen Umriss mit verschiedenen Bindestrichen zu zeichnen.

**Beispiele:**

Wenn Sie `<v:stroke dashstyle="solid" />` im- `<line>` Element angeben, können Sie eine vollständig erstellte Linie erstellen, wie in der folgenden VML-Darstellung gezeigt:

![solid.gif (96 Bytes)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





Wenn Sie das Eigenschafts Attribut "Dashboard" in "Punkt" ändern, können Sie eine gepunktete Linie erstellen, wie **in der folgenden** VML-Darstellung gezeigt:

![dot.gif (144 Bytes)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





Wenn Sie das Eigenschafts Attribut "Dashboard" in "Dash" ändern, können Sie wie **in der folgenden** VML-Darstellung gezeigt eine Bindestrich Linie erstellen:

![dash.gif (137 bytes)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





Wenn Sie das Eigenschafts Attribut " **DashStyle** " in "DashDot" ändern, können Sie eine Linie mit einem gestrichelten und gepunkteten Stil erstellen, wie in der folgenden VML-Darstellung dargestellt:

![dashdot.gif (145 bytes)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





Wenn Sie das Eigenschafts Attribut "Dashboard" in "longdash" ändern, können Sie eine Zeile mit einem langen gestrichelten Stil erstellen, wie **in der folgenden** VML-Darstellung dargestellt:

![longdash.gif (123 Bytes)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





Wenn **Sie das** Eigenschafts Attribut "Dashboard" in "longdashdot" ändern, können Sie eine Zeile mit einem langen gestrichelten und gepunkteten Stil erstellen, wie in der folgenden VML-Darstellung dargestellt:

![longdashdot.gif (135 bytes)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





Wenn Sie im- `<v:stroke dashstyle="dashdot" />` `<rect>` Element platzieren, können Sie ein Rechteck mit einem gestrichelten und gepunkteten Umriss erstellen, wie in der folgenden VML-Darstellung dargestellt:

![rect.gif (615 bytes)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="opacity"></a>Durchlässigkeit

Sie können das Attribut der **Deck Kraft** -Eigenschaft des `<stroke>` unter Elements verwenden, um eine Gliederung mit verschiedenen Deckkraft Stilen zu zeichnen. Der Wert für das Attribut für die **Deck Kraft** -Eigenschaft kann eine beliebige Zahl zwischen 0 und 1 sein. Standardmäßig ist der Wert 1, was eine vollständige Deckkraft angibt.

**Beispiele:**

In der folgenden VML-Darstellung wird eine Zeile mit vollständiger Deckkraft erstellt:

![line1.gif (96 Bytes)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





Wenn Sie `<v:stroke opacity="0.5" />` innerhalb des- `<line>` Elements hinzufügen, können Sie eine Zeile mit einer Deckkraft von 50% erstellen, wie in der folgenden VML-Darstellung dargestellt:

![line2.gif (108 bytes)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="linestyle"></a>LineStyle

Sie können das **LineStyle** -Eigenschafts Attribut des `<stroke>` untergeordneten-Elements verwenden, um eine Gliederung mit verschiedenen Linienstilen zu zeichnen.

**Beispiele:**

Wenn Sie `<v:stroke linestyle="single" />` im- `<rect>` Element angeben, können Sie ein Rechteck mit einem einzelnen Umriss erstellen, wie in der folgenden VML-Darstellung dargestellt:

![single.gif (537 Bytes)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





Wenn Sie das **LineStyle** -Eigenschafts Attribut in "Thin Thin" ändern, können Sie ein Rechteck mit der Kontur (1:1:1) erstellen, wie in der folgenden VML-Darstellung gezeigt:

![thinthin.gif (642 bytes)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





Wenn Sie das **LineStyle** -Eigenschafts Attribut in "Thin Thick" ändern, können Sie ein Rechteck mit der Kontur (1:1:2) erstellen, wie in der folgenden VML-Darstellung gezeigt:

![thinthick.gif (646 bytes)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





Wenn Sie das **LineStyle** -Eigenschafts Attribut in "Thick Thin" ändern, können Sie ein Rechteck mit der Kontur (2:1:1) erstellen, wie in der folgenden VML-Darstellung gezeigt:

![thickthin.gif (676 bytes)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





Wenn Sie das **LineStyle** -Eigenschafts Attribut in "thickbetweenthin" ändern, können Sie ein Rechteck mit der Kontur (1:1:2:1:1) erstellen, wie in der folgenden VML-Darstellung gezeigt:

![thickbthin.gif (669 bytes)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="joinstyle"></a>JOINSTYLE

Sie können das **JOINSTYLE** -Attribut des `<stroke>` untergeordneten-Elements verwenden, um zu definieren, wie Linien verknüpft werden.

Um z. b. eine Form zu erstellen, die die roundjoingliederung hat, wie in der folgenden Abbildung dargestellt, können Sie im- `<v:stroke joinstyle="round" />` `<polyline>` Element angeben, wie in der folgenden VML-Darstellung gezeigt:

![round.gif (660 bytes)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





Wenn Sie das Attribut " **JOINSTYLE** Property" in "abvel" ändern, können Sie eine Form erstellen, die die Kontur für den Abschrägungs Join enthält, wie in der folgenden VML-Darstellung dargestellt:

![bevel.gif (650 bytes)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





Wenn Sie das Attribut " **JOINSTYLE** Property" in "Miter" ändern, können Sie wie in der folgenden VML-Darstellung gezeigt eine Form erstellen, die die Beschreibung des Miter-Joins hat:

![miter.gif (702 bytes)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="filltype"></a>FillType

Sie können das **FillType** -Eigenschafts Attribut des `<stroke>` unter Elements verwenden, um einen Umriss mit verschiedenen Füll Effekten zu zeichnen.

**Beispiele:**

Wenn Sie `<v:stroke filltype="solid" />` im- `<roundrect>` Element angeben, können Sie ein abgerundetes Rechteck mit dem vollständig gefüllten Umriss erstellen, wie in der folgenden VML-Darstellung dargestellt:

![solid.gif (701 Bytes)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





Wenn Sie das **FillType** -Eigenschafts Attribut in "Pattern" ändern, das **src** -Eigenschafts Attribut auf den Speicherort der Pattern-Bilddatei verweisen und das **color2** -Eigenschafts Attribut auf die zweite Muster Farbe festlegen, können Sie ein abgerundetes Rechteck mit einem Muster Umriss erstellen, wie in der folgenden VML-Darstellung dargestellt:

![pattern.gif (1055 Bytes)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





Wenn Sie das **FillType** -Eigenschafts Attribut in "Tile" ändern und das **src** -Eigenschafts Attribut auf den Speicherort der Bilddatei verweisen, können Sie ein abgerundetes Rechteck mit einer gekachelten Gliederung erstellen, wie in der folgenden VML-Darstellung dargestellt:

![tile.gif (6617 Bytes)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





Wenn Sie das **FillType** -Eigenschafts Attribut in "Frame" ändern und das **src** -Eigenschafts Attribut auf den Speicherort der Bilddatei verweisen, können Sie ein abgerundetes Rechteck mit einer Bild Gliederung erstellen, wie in der folgenden VML-Darstellung dargestellt:

![frame.gif (6203 Bytes)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858395) .

 

 