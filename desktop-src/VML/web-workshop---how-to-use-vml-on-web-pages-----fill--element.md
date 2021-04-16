---
title: Verwenden des Fill-Elements
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Webworkshop, Fill-Element
- Entwerfen von Webseiten, Fill-Element
- Vector Markup Language (VML), Fill-Element
- VML (Vector Markup Language), Fill-Element
- Vektorgrafiken, Fill-Element
- Fill-Element
- VML-Elemente, ausfüllen
- VML-Formen, Fill-Element
- Vector Markup Language (VML), Farbverlaufsfüllung
- VML (Vector Markup Language), Farbverlaufsfüllung
- Vektorgrafiken, Farbverlaufsfüllung
- VML-Formen, Farbverlaufsfüllung
- durch Farbverlauf gefüllte Formen
- Vector Markup Language (VML), Musterfüllung
- VML (Vector Markup Language), Musterfüllung
- Vektorgrafiken, Musterfüllung
- VML-Formen, Musterfüllung
- Muster gefüllte Formen
- Vector Markup Language (VML), Bild Füllung
- VML (Vector Markup Language), Bild Füllung
- Vektorgrafiken, bildfüll
- VML-Formen, Bild Füllung
- Bild gefüllte Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf497a3120f53e24f1cff2bf7084469754bbaf7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104555357"
---
# <a name="using-the-fill-element"></a>Verwenden des Fill-Elements

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Wie Sie gelernt haben, können Sie das **FillColor** -Eigenschafts Attribut eines vordefinierten Shape-Elements verwenden, z. b.,,,, `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` , `<roundrect>` , `<arc>` --, um die Farbe anzugeben, die zum Ausfüllen der Form verwendet wird. In diesem Thema wird veranschaulicht, wie eine Form gezeichnet wird, die mit erweiterten Effekten gefüllt ist.

Sie können das `<fill>` untergeordnete Element innerhalb des- `<shape>` ,-oder-Elements `<shapetype>` oder eines beliebigen vordefinierten Shape-Elements platzieren, um das Ausfüllen der Form zu beschreiben. Anschließend können Sie die Eigenschafts Attribute des `<fill>` unter Elements verwenden, um den Fülleffekt anzupassen, z. b. [Farbverlaufsfüllung](#gradient-fill), [Musterfüllung](#pattern-fill), [Bild Füllung](#picture-fill).

In diesem Thema:

-   [Farbverlaufsfüllung](#gradient-fill)
-   [Musterfüllung](#pattern-fill)
-   [Bild Füllung](#picture-fill)

## <a name="gradient-fill"></a>Farbverlaufsfüllung

Um eine Form vom **Typ** "Gradient" zu zeichnen, können Sie das Type-Eigenschafts Attribut des `<fill>` unter Elements auf "Gradient" oder "gradientradi" festlegen und dann andere Eigenschafts Attribute des `<fill>` unter Elements angeben, z. b. **Methode**, **color2**, **Fokus** und **Winkel**.

**Beispiele:**

Zum Erstellen einer Form, die horizontal mit einem Farbverlauf gefüllt ist, können Sie das Attribut **Type** Property auf "Gradient" festlegen, wie in der folgenden VML-Darstellung gezeigt:

![horizontal1.gif (3055 Bytes)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




Wenn Sie das **FillColor** -Eigenschafts Attribut der Form ändern, wird die Form dann mit einer anderen Farbe aufgefüllt. Sie können eine zweite Farbe hinzufügen, indem Sie das **color2** -Eigenschafts Attribut des `<fill>` unter Elements angeben. Um z. b. eine Form zu erstellen, die in zwei Farben mit einem Farbverlauf gefüllt ist, können Sie eine zweite Farbe hinzufügen, indem Sie das **color2** -Eigenschafts Attribut des `<fill>` unter Elements angeben, wie in der folgenden VML-Darstellung dargestellt:

![horizontal2.gif (3127 Bytes)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




Sie können das **method** -Eigenschaften Attribut auf "Linear" oder "Sigma" oder "Any" oder "None" festlegen. Die Auswirkung des Farbverlaufs unterscheidet sich geringfügig. Außerdem können Sie mit dem **Angle**-,**Fokus**-,**focussize**-oder **focusposition** -Eigenschafts Attribut ändern, wie der Farbverlauf verläuft.

**Beispiele:**

 

Zum Erstellen einer Form, die mit einem vertikalen Farbverlauf aufgefüllt ist, können Sie das Angle-Eigenschafts Attribut auf Angle = "-90" festlegen, wie in der folgenden VML-Darstellung gezeigt:

![vertical1.gif (3836 Bytes)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




Um eine Form zu erstellen, die von diagonalem bewegen mit einem Farbverlauf gefüllt ist, können Sie das **Angle** -Eigenschafts Attribut auf Angle = "-135" festlegen, wie in der folgenden VML-Darstellung gezeigt:

![dialgonalup1.gif (5816 Bytes)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




Um eine Form zu erstellen, die von einem diagonalen, nach unten ausgefüllten Farbverlauf gefüllt ist, können Sie das **Angle** -Eigenschafts Attribut auf Angle = "-45" festlegen, wie in der folgenden VML-Darstellung gezeigt:

![diagonaldown1.gif (5753 Bytes)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




Um eine Form zu erstellen, die aus dem Mittelpunkt aufgefüllt wird, können Sie angeben `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , wie in der folgenden VML-Darstellung gezeigt:

![fromcenter1.gif (4598 Bytes)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="pattern-fill"></a>Musterfüllung

Um eine Muster gefüllte Form zu zeichnen, können Sie das **Type** -Eigenschafts Attribut des `<fill>` unter Elements auf "Pattern" festlegen und anschließend andere Eigenschafts Attribute des `<fill>` unter Elements angeben, z. b. **src** und **color2**.

**Beispiele:**

Zum Erstellen einer Form, die mit einem Musterbild gefüllt ist, können Sie das **Type** -Eigenschafts Attribut auf "Pattern" festlegen und das **src** -Eigenschafts Attribut auf den Speicherort der Pattern-Bilddatei verweisen, wie in der folgenden VML-Darstellung gezeigt:

![pattern1.gif (872 bytes)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




Wenn Sie das **src** -Eigenschafts Attribut auf eine andere Musterdatei verweisen, können Sie eine Form erstellen, die mit einem anderen Muster gefüllt ist. Außerdem können Sie die Farbe ändern, indem Sie einen anderen Wert für das **FillColor** -oder **color2** -Eigenschafts Attribut angeben, wie in der folgenden VML-Darstellung dargestellt:

![pattern2.gif (831 Bytes)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="picture-fill"></a>Bild Füllung

Zum Zeichnen eines Bilds können Sie das **Type** -Eigenschafts Attribut des `<fill>` unter Elements auf "Frame" festlegen und anschließend andere Eigenschafts Attribute des `<fill>` unter Elements angeben, z. b. **src** und **color2**.

**Beispiele:**

Um eine Form zu erstellen, die mit einer Bilddatei gefüllt ist, können Sie das **Type** -Eigenschafts Attribut auf "Frame" festlegen und dann das **src** -Eigenschafts Attribut auf den Speicherort der Bilddatei verweisen, wie in der folgenden VML-Darstellung gezeigt:

![picture1.gif (8496 Bytes)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




Sie können problemlos eine Form erstellen, die mit einem anderen Bild gefüllt ist, indem Sie das **src** -Eigenschafts Attribut auf eine andere Datei zeigen.

Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858394) .

 

 