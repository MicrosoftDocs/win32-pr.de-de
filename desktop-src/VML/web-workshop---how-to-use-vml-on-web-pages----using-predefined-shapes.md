---
title: Verwenden von vordefinierten Formen
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Webworkshop, vordefinierte Formen
- Entwerfen von Webseiten, vordefinierte Formen
- Vector Markup Language (VML), vordefinierte Formen
- VML (Vector Markup Language), vordefinierte Formen
- Vektorgrafiken, vordefinierte Formen
- VML-Formen, vordefiniert
- vordefinierte Formen
- Vector Markup Language (VML), Rect-Element
- VML (Vector Markup Language), Rect-Element
- Vektorgrafiken, Rect-Element
- Rect-Element
- VML-Elemente, Rect
- Vector Markup Language (VML), roundRect-Element
- VML (Vector Markup Language), roundRect-Element
- Vektorgrafiken, roundRect-Element
- roundRect-Element
- VML-Elemente, roundRect
- Vector Markup Language (VML), Zeilen Element
- VML (Vector Markup Language), Zeilen Element
- Vektorgrafiken, Zeilen Element
- Line-Element
- VML-Elemente, Zeile
- Vector Markup Language (VML), polylinienelement
- VML (Vector Markup Language), polylinienelement
- Vektorgrafiken, polylinienelement
- Polylinie-Element
- VML-Elemente, Polyline
- Vector Markup Language (VML), Kurven Element
- VML (Vector Markup Language), Kurven Element
- Vektorgrafiken, Kurven Element
- Kurven Element
- VML-Elemente, Kurve
- Vector Markup Language (VML), Bogen Element
- VML (Vector Markup Language), Bogen Element
- Vektorgrafiken, Bogen Element
- Arc-Element
- VML-Elemente, Bogen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c1cafacf00f6f3f9129c29c56837f3f485aa3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516883"
---
# <a name="using-predefined-shapes"></a>Verwenden von vordefinierten Formen

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Wie Sie gelernt haben, können Sie das- `<oval>` Element von VML verwenden, um ein einfaches Oval zu erstellen. VML bietet mehrere weitere vordefinierte Elemente. In diesem Thema wird veranschaulicht, wie Grafiken mithilfe dieser Elemente gezeichnet werden.

In diesem Thema:

-   [Rect](#roundrect)
-   [roundRect](#roundrect)
-   [line](#polyline)
-   [Polylinie](#polyline)
-   [Kurve](#curve)
-   [Bogen](#arc)
-   [Zusammenfassung](#summary)

## <a name="rect"></a>rect

Sie können das- `<rect>` Element verwenden, um ein Rechteck zu zeichnen. Anschließend können Sie das Rechteck anpassen, indem Sie unterschiedliche Eigenschafts Attribute angeben.

Beispielsweise können Sie ein Rechteck zeichnen, das mit blau gefüllt ist, indem Sie **FillColor**= "Blue" angeben und ihm eine rote Gliederung mit 3,5 Punkten geben, indem Sie " **strokeColor**=" Red " **strokeweight**=" 3.5 pt "angeben, wie in der folgenden VML-Darstellung gezeigt:

![rect1.gif (485 bytes)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) . (Hinweis: die VML-Spezifikation weist kein Lesezeichen für das `<rect>` Element auf.)

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="roundrect"></a>roundRect

Sie können das- `<roundrect>` Element verwenden, um ein Rechteck mit abgerundeten Ecken zu zeichnen. Anschließend können Sie das abgerundete Rechteck anpassen, indem Sie unterschiedliche Eigenschafts Attribute angeben.

Sie können z. b. ein Rechteck mit gerundeten Ecken von 30% der Hälfte der kleineren Dimension des Rechtecks zeichnen, indem Sie **arcsize**= "0,3" angeben, geben Sie den Wert gelb durch Angabe von **FillColor**= "Yellow" ein, und weisen Sie ihm einen zwei-Punkt-roten Umriss zu, indem Sie " **strokeColor**=" Red " **strokeweight**=" 2pt "angeben, wie in der folgenden VML-Darstellung gezeigt:

![roundrect1.gif (622 Bytes)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="line"></a>line

Sie können das- `<line>` Element verwenden, um eine gerade Linie zu erstellen. Anschließend können Sie die Zeile anpassen, indem Sie unterschiedliche Eigenschafts Attribute angeben.

Sie können z. b. eine horizontale Linie zeichnen, indem Sie **from**= "20pt, 20pt" **to**= "100pt, 20pt" angeben und Sie durch Angabe von " **strokeColor**=" Red " **strokeweight**=" 2pt "in der folgenden VML-Darstellung als 2-Punkt und Rot festlegen

![line1.gif (88 Bytes)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





Sie können eine vertikale oder diagonal Linie zeichnen, indem Sie einfach unterschiedliche Werte für die Attribute **from** und **to** Property angeben, wie in der folgenden VML-Darstellung dargestellt:

![line2.gif (86 Bytes)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="polyline"></a>Polylinie

Sie können das- `<polyline>` Element verwenden, um Formen zu definieren, die aus verbundenen Liniensegmenten erstellt werden. Anschließend können Sie die Form anpassen, indem Sie verschiedene Eigenschafts Attribute angeben.

Wenn Sie z. b. die in der folgenden Abbildung gezeigte Form zeichnen möchten, können Sie die folgende VML-Darstellung eingeben:

![polyline1.gif (957 bytes)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="curve"></a>Kurve

Sie können das- `<curve>` Element verwenden, um eine kubische Bézier-Kurve zu zeichnen. Sie können dann die Kurve anpassen, indem Sie verschiedene Eigenschafts Attribute angeben.

Wenn Sie z. b. eine Kurve zeichnen möchten, wie in der folgenden Abbildung dargestellt, können Sie die folgende VML-Darstellung eingeben:

![curve1.gif (992 bytes)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="arc"></a>Bogen

Sie können das- `<arc>` Element verwenden, um einen Bogen zu zeichnen, der als Segment eines Oval definiert ist. Der Bogen wird durch die Schnittmenge des Oval mit den Anfangs-und EndRadius-Vektoren definiert, die von den Winkeln angegeben werden. Die Winkel werden mithilfe der Eigenschaften eines Kreises (Breite gleich Höhe) berechnet und dann auf die gewünschte Breite und Höhe zentral skaliert.

Beispielsweise können Sie einen Bogen zeichnen, der bei 0 Grad beginnt und um 90 Grad endet, indem Sie **Start Angle**= "0" **EndAngle**= "90" angeben, wie in der folgenden VML-Darstellung dargestellt:

![arc1.gif (410 Bytes)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





Sie können den Bogen ändern, indem Sie unterschiedliche **Start Angle** **-und** -Werte angeben, wie in der folgenden VML-Darstellung dargestellt:

![arc2.gif (608 bytes)](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 bytes)](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="summary"></a>Zusammenfassung

Sie können vordefinierte VML-Elemente, wie z. b. `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` und verwenden `<arc>` , um auf einfache Weise Grafiken auf einer Webseite zu zeichnen und diese Grafiken dann anzupassen, indem Sie einfach Ihre Eigenschafts Attribute ändern.

 

 