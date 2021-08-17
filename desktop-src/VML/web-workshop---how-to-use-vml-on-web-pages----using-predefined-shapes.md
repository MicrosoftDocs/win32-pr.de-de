---
title: Verwenden vordefinierter Formen
description: In diesem Artikel wird die Verwendung vordefinierter Formen in VML beschrieben, einem Feature, das ab Windows Internet Explorer 9 veraltet ist.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Web-Workshop, vordefinierte Formen
- Entwerfen von Webseiten, vordefinierte Formen
- Vector Markup Language (VML), vordefinierte Formen
- VML (Vector Markup Language), vordefinierte Formen
- Vektorgrafiken, vordefinierte Formen
- VML-Formen, vordefiniert
- Vordefinierte Formen
- Vector Markup Language (VML),rect-Element
- VML (Vector Markup Language),rect-Element
- Vektorgrafik, rect-Element
- rect-Element
- VML-Elemente, rect
- Vector Markup Language (VML),Roundrect-Element
- VML (Vector Markup Language),Roundrect-Element
- Vektorgrafik, Roundrect-Element
- roundrect-Element
- VML-Elemente, roundrect
- Vector Markup Language (VML),Line-Element
- VML (Vector Markup Language),Line-Element
- Vektorgrafik, Linienelement
- line-Element
- VML-Elemente, Zeile
- Vector Markup Language (VML),Polylinienelement
- VML (Vector Markup Language),Polylinienelement
- Vektorgrafik, Polylinienelement
- Polylinienelement
- VML-Elemente, Polylinie
- Vector Markup Language (VML),Curve-Element
- VML (Vector Markup Language),Curve-Element
- Vektorgrafik, Curve-Element
- curve-Element
- VML-Elemente, Kurve
- Vector Markup Language (VML),Arc-Element
- VML (Vector Markup Language),Arc-Element
- Vektorgrafik, Arc-Element
- Arc-Element
- VML-Elemente, Arc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f389a3a2670bd487799063df6bfcec59f28945ed09cad119fccd88e40f01b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753866"
---
# <a name="using-predefined-shapes"></a>Verwenden vordefinierter Formen

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Wie Sie gelernt haben, können Sie das `<oval>` -Element von VML verwenden, um ein einfaches Oval zu erstellen. VML stellt mehrere andere vordefinierte Elemente bereit. In diesem Thema wird veranschaulicht, wie Mithilfe dieser Elemente Grafiken gezeichnet werden.

In diesem Thema:

-   [Rect](#roundrect)
-   [roundrect](#roundrect)
-   [Linie](#polyline)
-   [Polylinie](#polyline)
-   [Kurve](#curve)
-   [Arc](#arc)
-   [Zusammenfassung](#summary)

## <a name="rect"></a>rect

Sie können das `<rect>` -Element verwenden, um ein Rechteck zu zeichnen. Anschließend können Sie das Rechteck anpassen, indem Sie verschiedene Eigenschaftsattribute angeben.

Sie können z. B. ein Rechteck zeichnen, das mit Blau gefüllt ist, indem Sie **fillcolor**="blue" angeben und ihm eine rote 3,5-Punkt-Kontur geben, indem Sie **strokecolor**="red" **strokeweight**="3.5pt" angeben, wie in der folgenden VML-Darstellung gezeigt:

![rect1.gif (485 Byte)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) (Hinweis: Die VML-Spezifikation enthält kein Lesezeichen für das `<rect>` Element.)

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="roundrect"></a>roundrect

Sie können das `<roundrect>` -Element verwenden, um ein Rechteck mit abgerundeten Ecken zu zeichnen. Anschließend können Sie das abgerundete Rechteck anpassen, indem Sie verschiedene Eigenschaftsattribute angeben.

Sie können z. B. ein Rechteck zeichnen, das 30 % der Hälfte der kleineren Dimension des Rechtecks abgerundete Ecken aufweist, indem Sie **arcsize**="0.3" angeben, es mit Gelb füllen, indem Sie **fillcolor**="yellow" angeben, und ihm eine rote 2-Punkt-Kontur geben, indem Sie **strokecolor**="red" **strokeweight**="2pt" angeben, wie in der folgenden VML-Darstellung gezeigt:

![roundrect1.gif (622 Bytes)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://WWW.w3.org/TR/NOTE-VML#-toc416858405)

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="line"></a>line

Sie können das `<line>` -Element verwenden, um eine gerade Linie zu erstellen. Anschließend können Sie die Zeile anpassen, indem Sie verschiedene Eigenschaftsattribute angeben.

Sie können z. B. eine horizontale Linie zeichnen, indem Sie **von**="20pt,20pt" **bis**="100pt,20pt" angeben und sie 2-Punkt und rot machen, indem Sie **strokecolor**="red" **strokeweight**="2pt" angeben, wie in der folgenden VML-Darstellung gezeigt:

![line1.gif (88 Byte)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





Sie können eine vertikale oder diagonale Linie zeichnen, indem Sie einfach unterschiedliche Werte für die Eigenschaftenattribute **from** und **to** angeben, wie in der folgenden VML-Darstellung gezeigt:

![line2.gif (86 Byte)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://WWW.w3.org/TR/NOTE-VML#-toc416858402)

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="polyline"></a>Polylinie

Sie können das `<polyline>` -Element verwenden, um Formen zu definieren, die aus verbundenen Liniensegmenten erstellt werden. Anschließend können Sie die Form anpassen, indem Sie verschiedene Eigenschaftsattribute angeben.

Um beispielsweise die in der folgenden Abbildung dargestellte Form zu zeichnen, können Sie die folgende VML-Darstellung eingeben:

![polyline1.gif (957 Bytes)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://WWW.w3.org/TR/NOTE-VML#-toc416858403)

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="curve"></a>Kurve

Sie können das `<curve>` -Element verwenden, um eine kubische Bézierkurve zu zeichnen. Anschließend können Sie die Kurve anpassen, indem Sie verschiedene Eigenschaftsattribute angeben.

Um z. B. eine Kurve wie in der folgenden Abbildung zu zeichnen, können Sie die folgende VML-Darstellung eingeben:

![curve1.gif (992 Bytes)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://WWW.w3.org/TR/NOTE-VML#-toc416858404)

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="arc"></a>Bogen

Sie können das `<arc>` -Element verwenden, um einen Bogen zu zeichnen, der als Segment eines Ovals definiert ist. Der Bogen wird durch die Schnittmenge des Ovals mit den Durchlauf- und Endradiusvektoren definiert, die von den Winkeln angegeben werden. Die Winkel werden mithilfe der Eigenschaften eines Kreises (Breite gleich Höhe) berechnet und dann anisotrop auf die gewünschte Breite und Höhe skaliert.

Beispielsweise können Sie einen Bogen zeichnen, der bei 0 Grad beginnt und bei 90 Grad endet, indem Sie **startangle**="0" **endangle**="90" angeben, wie in der folgenden VML-Darstellung gezeigt:

![arc1.gif (410 Bytes)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





Sie können den Bogen ändern, indem Sie verschiedene **Startangle-** und **Endangle-Werte** angeben, wie in der folgenden VML-Darstellung gezeigt:

![arc2.gif (608 Bytes)](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 Bytes)](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://WWW.w3.org/TR/NOTE-VML#-toc416858407)

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="summary"></a>Zusammenfassung

Sie können vordefinierte VML-Elemente wie , , , , , und verwenden, um grafiken einfach auf einer Webseite zu zeichnen, und diese Grafiken dann anpassen, indem Sie einfach deren Eigenschaftenattribute `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` ändern.

 

 