---
title: Verwenden des Stroke-Elements
description: In diesem Artikel wird die Verwendung des Stroke-Elements von VML beschrieben, einem Feature, das ab Windows Internet Explorer 9 als veraltet gilt.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Web workshop,stroke-Element
- Entwerfen von Webseiten, Strichelement
- Vector Markup Language (VML),Strichelement
- VML (Vector Markup Language),Strichelement
- Vektorgrafik, Strichelement
- stroke-Element
- VML-Elemente, Strich
- VML-Formen, Strichelement
- Vector Markup Language (VML),Dashstyle-Eigenschaftsattribut
- VML (Vector Markup Language),Dashstyle-Eigenschaftsattribut
- Vektorgrafik, Dashstyle-Eigenschaftsattribut
- Dashstyle-Eigenschaftsattribut
- Vector Markup Language -Eigenschaftsattribut (VML), Deckkrafteigenschaft
- VML-Eigenschaftsattribut (Vector Markup Language),Deckkrafteigenschaft
- Vektorgrafik, Opacity-Eigenschaftsattribut
- Opacity-Eigenschaftsattribut
- Vector Markup Language (VML), Linestyle-Eigenschaftsattribut
- VML (Vector Markup Language),Linestyle-Eigenschaftsattribut
- Vektorgrafik, Eigenschaftenattribut "linestyle"
- linestyle-Eigenschaftsattribut
- Vector Markup Language (VML), Joinstyle-Eigenschaftsattribut
- VML (Vector Markup Language),Joinstyle-Eigenschaftsattribut
- Vektorgrafik, Joinstyle-Eigenschaftsattribut
- joinstyle-Eigenschaftsattribut
- Vector Markup Language (VML), Filltype-Eigenschaftsattribut
- VML (Vector Markup Language),Filltype-Eigenschaftsattribut
- Vektorgrafiken, Filltype-Eigenschaftsattribut
- filltype-Eigenschaftsattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cb69452abe5b3d743036f6a4db094da196281b575a6db65aa48535126fd917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057447"
---
# <a name="using-the-stroke-element"></a>Verwenden des Stroke-Elements

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Verwenden von `<stroke>`

Wie Sie gelernt haben, können Sie die **Strokecolor-** und **Strokeweight-Eigenschaftsattribute** einer vordefinierten Form wie , , , , , , `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` verwenden, um die Farbe und Gewichtung der Kontur einer Form anzugeben. In diesem Thema wird veranschaulicht, wie eine Form mit einer erweiterten Kontur gezeichnet wird.

Sie können das `<stroke>` Unterelement innerhalb von `<shape>` oder oder in `<shapetype>` einem beliebigen vordefinierten Formelement platzieren, um zu beschreiben, wie die Kontur der Form gezeichnet wird. Anschließend können Sie die Eigenschaftsattribute (z. [B. Dashstyle,](#dashstyle) [Deckkraft,](#opacity) [Linestyle,](#linestyle) [Joinstyle,](#joinstyle) [Filltype)](#filltype) des `<stroke>` Unterelements verwenden, um die Kontur anzupassen.

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="dashstyle"></a>Dashstyle

Sie können das **Dashstyle-Eigenschaftsattribut** des `<stroke>` Unterelements verwenden, um eine Kontur mit verschiedenen Bindestrichen zu zeichnen.

**Beispiele:**

Wenn Sie `<v:stroke dashstyle="solid" />` innerhalb des `<line>` -Elements angeben, können Sie eine durchgezogene Linie erstellen, wie in der folgenden VML-Darstellung gezeigt:

![solid.gif (96 Bytes)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





Wenn Sie das **Dashstyle-Eigenschaftsattribut** in "dot" ändern, können Sie eine gepunktete Linie erstellen, wie in der folgenden VML-Darstellung gezeigt:

![dot.gif (144 Bytes)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





Wenn Sie das **Dashstyle-Eigenschaftsattribut** in "Bindestrich" ändern, können Sie eine Bindestrichlinie erstellen, wie in der folgenden VML-Darstellung gezeigt:

![dash.gif (137 Byte)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





Wenn Sie das **Dashstyle-Eigenschaftsattribut** in "dashdot" ändern, können Sie eine Linie mit einem gestrichelten und gepunkteten Stil erstellen, wie in der folgenden VML-Darstellung gezeigt:

![dashdot.gif (145 Byte)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





Wenn Sie das **Dashstyle-Eigenschaftsattribut** in "longdash" ändern, können Sie eine Linie mit einem langen gestrichelten Stil erstellen, wie in der folgenden VML-Darstellung gezeigt:

![longdash.gif (123 Byte)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





Wenn Sie das **Dashstyle-Eigenschaftsattribut** in "longdashdot" ändern, können Sie eine Linie mit einem langen gestrichelten und gepunkteten Stil erstellen, wie in der folgenden VML-Darstellung gezeigt:

![longdashdot.gif (135 Bytes)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





Wenn Sie `<v:stroke dashstyle="dashdot" />` innerhalb des `<rect>` -Elements platzieren, können Sie ein Rechteck mit gestrichelter und gepunkteter Kontur erstellen, wie in der folgenden VML-Darstellung gezeigt:

![rect.gif (615 Bytes)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="opacity"></a>Durchlässigkeit

Sie können das **Opacity-Eigenschaftsattribut** des `<stroke>` Unterelements verwenden, um eine Kontur mit verschiedenen Deckkraftstilen zu zeichnen. Der Wert für das **Opacity-Eigenschaftsattribut** kann eine beliebige Zahl zwischen 0 und 1 sein. Standardmäßig ist es 1, was die vollständige Deckkraft angibt.

**Beispiele:**

Die folgende VML-Darstellung erstellt eine Linie mit vollständiger Deckkraft:

![line1.gif (96 Bytes)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





Wenn Sie `<v:stroke opacity="0.5" />` innerhalb des `<line>` -Elements hinzufügen, können Sie eine Linie mit einer Deckkraft von 50 % erstellen, wie in der folgenden VML-Darstellung gezeigt:

![line2.gif (108 Bytes)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="linestyle"></a>Linestyle

Sie können das Eigenschaftenattribut **linestyle** des `<stroke>` Unterelements verwenden, um eine Kontur mit verschiedenen Linienstilen zu zeichnen.

**Beispiele:**

Wenn Sie `<v:stroke linestyle="single" />` im `<rect>` -Element angeben, können Sie ein Rechteck mit einer einzelnen Kontur erstellen, wie in der folgenden VML-Darstellung gezeigt:

![single.gif (537 Bytes)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





Wenn Sie  das Linestyle-Eigenschaftsattribut in "thinthin" ändern, können Sie ein Rechteck mit der Kontur (1:1:1) erstellen, wie in der folgenden VML-Darstellung gezeigt:

![thinthin.gif (642 Bytes)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





Wenn Sie das Eigenschaftenattribut **linestyle** in "thinthick" ändern, können Sie ein Rechteck mit der Kontur (1:1:2) erstellen, wie in der folgenden VML-Darstellung gezeigt:

![thinthick.gif (646 Bytes)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





Wenn Sie das Eigenschaftenattribut **linestyle** in "thickthin" ändern, können Sie ein Rechteck mit der Kontur (2:1:1) erstellen, wie in der folgenden VML-Darstellung gezeigt:

![thickthin.gif (676 Bytes)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





Wenn Sie  das Linestyle-Eigenschaftsattribut in "thickbetweenthin" ändern, können Sie ein Rechteck mit der Kontur (1:1:2:1:1) erstellen, wie in der folgenden VML-Darstellung gezeigt:

![thickbthin.gif (669 Byte)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="joinstyle"></a>joinstyle

Sie können das **joinstyle-Attribut** des `<stroke>` Unterelements verwenden, um zu definieren, wie Zeilen miteinander verknüpft werden.

Um z. B. eine Form mit der Rundungsverknüpfungsgliederung zu erstellen, wie in der folgenden Abbildung gezeigt, können Sie `<v:stroke joinstyle="round" />` innerhalb des `<polyline>` -Elements angeben, wie in der folgenden VML-Darstellung gezeigt:

![round.gif (660 Bytes)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





Wenn Sie  das Joinstyle-Eigenschaftsattribut in "abschrägung" ändern, können Sie eine Form mit der Abschrägungsverknüpfungsgliederung erstellen, wie in der folgenden VML-Darstellung gezeigt:

![bevel.gif (650 Byte)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





Wenn Sie  das joinstyle-Eigenschaftsattribut in "miter" ändern, können Sie eine Form mit der Kontur miter-join erstellen, wie in der folgenden VML-Darstellung gezeigt:

![miter.gif (702 Bytes)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="filltype"></a>filltype

Sie können  das filltype-Eigenschaftsattribut des `<stroke>` Unterelements verwenden, um eine Kontur mit verschiedenen Fülleffekten zu zeichnen.

**Beispiele:**

Wenn Sie `<v:stroke filltype="solid" />` im `<roundrect>` -Element angeben, können Sie ein abgerundetes Rechteck mit der durchgezogenen Kontur erstellen, wie in der folgenden VML-Darstellung gezeigt:

![solid.gif (701 Byte)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





Wenn Sie  das Filltype-Eigenschaftsattribut in "pattern" ändern, das src-Eigenschaftsattribut auf den Speicherort der Musterbilddatei verweisen und das **Color2-Eigenschaftsattribut** auf die zweite Musterfarbe festlegen, können Sie ein abgerundetes Rechteck mit einer Mustergliederung erstellen, wie in der folgenden VML-Darstellung gezeigt: 

![pattern.gif (1055 Bytes)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





Wenn Sie  das filltype-Eigenschaftenattribut in "tile" ändern und das src-Eigenschaftsattribut auf den Speicherort der Bilddatei verweisen, können Sie ein abgerundetes Rechteck mit einer gekachelten Kontur erstellen, wie in der folgenden VML-Darstellung gezeigt: 

![tile.gif (6617 Bytes)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





Wenn Sie  das filltype-Eigenschaftenattribut in "frame" ändern und das src-Eigenschaftsattribut auf den Speicherort der Bilddatei verweisen, können Sie ein abgerundetes Rechteck mit einer Bildgliederung erstellen, wie in der folgenden VML-Darstellung gezeigt: 

![frame.gif (6203 Bytes)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://www.w3.org/TR/NOTE-VML#-toc416858395)

 

 