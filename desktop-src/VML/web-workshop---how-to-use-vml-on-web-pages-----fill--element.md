---
title: Verwenden des Fill-Elements
description: In diesem Artikel wird die Verwendung des Fill-Elements von VML beschrieben, einem Feature, das ab Windows Internet Explorer 9 veraltet ist.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Web workshop,fill-Element
- Entwerfen von Webseiten, Fill-Element
- Vector Markup Language (VML), Fill-Element
- VML (Vector Markup Language),Füllelement
- Vektorgrafiken, Fill-Element
- fill-Element
- VML-Elemente, auffüllen
- VML-Formen, Fill-Element
- Vector Markup Language (VML), Farbverlaufsfüllung
- VML (Vector Markup Language),Farbverlaufsfüllung
- Vektorgrafik, Farbverlaufsfüllung
- VML-Formen, Farbverlaufsfüllung
- Mit Farbverlauf gefüllte Formen
- Vector Markup Language (VML), Musterfüllung
- VML (Vector Markup Language),Musterfüllung
- Vektorgrafiken, Musterfüllung
- VML-Formen, Musterfüllung
- Mit Mustern gefüllte Formen
- Vector Markup Language (VML), Bildfüllung
- VML (Vector Markup Language),Bildfüllung
- Vektorgrafiken, Bildfüllung
- VML-Formen, Bildfüllung
- Mit Bildern gefüllte Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f6b3e0c92989e037ebf9b95b7bd726134b9099dd5d3755ff4588f7e970586c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057264"
---
# <a name="using-the-fill-element"></a>Verwenden des Fill-Elements

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Wie Sie gelernt haben, können  Sie das fillcolor-Eigenschaftsattribut eines vordefinierten Formelements wie `<oval>` , , , , , , `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` verwenden, um die Farbe anzugeben, die zum Füllen der Form verwendet wird. In diesem Thema wird veranschaulicht, wie eine Form gezeichnet wird, die mit erweiterten Effekten gefüllt ist.

Sie können das `<fill>` Unterelement innerhalb von `<shape>` oder oder in einem `<shapetype>` beliebigen vordefinierten Shape-Element platzieren, um zu beschreiben, wie die Form gefüllt werden soll. Anschließend können Sie die Eigenschaftenattribute des `<fill>` Unterelements verwenden, um den Fülleffekt anzupassen, z. B. [Farbverlaufsfüllung,](#gradient-fill) [Musterfüllung,](#pattern-fill) [Bildfüllung.](#picture-fill)

In diesem Thema:

-   [Farbverlaufsfüllung](#gradient-fill)
-   [Musterfüllung](#pattern-fill)
-   [Bildfüllung](#picture-fill)

## <a name="gradient-fill"></a>Farbverlaufsfüllung

Um eine mit Farbverlauf gefüllte  Form zu zeichnen, können Sie das Type-Eigenschaftsattribut des `<fill>` Unterelements auf "gradient" oder "gradientRadial" festlegen und dann andere Eigenschaftsattribute des `<fill>` Unterelements angeben, z. B. **methode**, **color2,** **focus** und **angle**.

**Beispiele:**

Um eine Form zu erstellen, die horizontal mit  Farbverlauf gefüllt ist, können Sie das type-Eigenschaftsattribut auf "gradient" festlegen, wie in der folgenden VML-Darstellung gezeigt:

![horizontal1.gif (3055 Bytes)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




Wenn Sie  das Fillcolor-Eigenschaftsattribut der Form ändern, wird die Form mit einer anderen Farbe farbverlaufsgefüllt. Sie können eine zweite Farbe  hinzufügen, indem Sie das color2-Eigenschaftsattribut des `<fill>` Unterelements angeben. Wenn Sie z. B. eine Form erstellen möchten, die in zwei Farben  mit Farbverläufen gefüllt ist, können Sie eine zweite Farbe hinzufügen, indem Sie das color2-Eigenschaftsattribut des `<fill>` Unterelements angeben, wie in der folgenden VML-Darstellung gezeigt:

![horizontal2.gif (3127 Bytes)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




Sie können  das Methodeneigenschaftsattribut auf "linear" oder "sigma" oder "any" oder "none" festlegen. Die Auswirkung des Farbverlaufs unterscheidet sich geringfügig. Darüber hinaus können Sie das Eigenschaftenattribut **angle**,**focus**,**focussize** oder **focusposition** verwenden, um zu ändern, wie der Farbverlauf verläuft.

**Beispiele:**

 

Um eine vertikal mit Farbverlauf gefüllte Form zu erstellen, können Sie das Angle-Eigenschaftsattribut auf angle="-90" festlegen, wie in der folgenden VML-Darstellung gezeigt:

![vertical1.gif (3836 Bytes)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




Um eine Form zu erstellen, die vom Diagonalen  nach oben mit Farbverläufen gefüllt wird, können Sie das Angle-Eigenschaftsattribut auf angle="-135" festlegen, wie in der folgenden VML-Darstellung gezeigt:

![dialgonalup1.gif (5816 Bytes)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




Um eine Form zu erstellen, die vom Diagonalen  nach unten mit Farbverläufen gefüllt wird, können Sie das Angle-Eigenschaftsattribut auf angle="-45" festlegen, wie in der folgenden VML-Darstellung gezeigt:

![diagonaldown1.gif (5753 Bytes)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




Um eine Form zu erstellen, die von der Mitte aus mit Farbverläufen gefüllt ist, können Sie `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` angeben, wie in der folgenden VML-Darstellung gezeigt:

![fromcenter1.gif (4.598 Byte)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="pattern-fill"></a>Musterfüllung

Um eine mit Mustern gefüllte  Form zu zeichnen, können Sie das type-Eigenschaftsattribut des `<fill>` Unterelements auf "pattern" festlegen und dann andere Eigenschaftsattribute des `<fill>` Unterelements angeben, z. B. **src** und **color2.**

**Beispiele:**

Um eine Form zu erstellen, die mit einem  Musterbild gefüllt ist, können Sie das type-Eigenschaftsattribut auf "pattern" angeben und das src-Eigenschaftsattribut auf den Speicherort der Musterbilddatei verweisen, wie in der folgenden VML-Darstellung gezeigt: 

![pattern1.gif (872 Bytes)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




Wenn Sie  das src-Eigenschaftsattribut auf eine andere Musterdatei verweisen, können Sie eine Form erstellen, die mit einem anderen Muster gefüllt ist. Außerdem können Sie die Farbe ändern, indem Sie einen anderen Wert für das **fillcolor-** oder color2-Eigenschaftsattribut angeben, wie in der folgenden VML-Darstellung gezeigt: 

![pattern2.gif (831 Bytes)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="picture-fill"></a>Bildfüllung

Um eine mit Bildern gefüllte Form  zu zeichnen, können Sie das type-Eigenschaftsattribut des `<fill>` Unterelements auf "frame" festlegen und dann andere Eigenschaftsattribute des `<fill>` Unterelements angeben, z. B. **src** und **color2.**

**Beispiele:**

Um eine Form zu erstellen, die mit einer  Bilddatei gefüllt ist, können Sie das type-Eigenschaftsattribut auf "frame" angeben und dann das src-Eigenschaftsattribut auf den Speicherort der Bilddatei verweisen, wie in der folgenden VML-Darstellung gezeigt: 

![picture1.gif (8496 Bytes)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




Sie können ganz einfach eine Form erstellen, die  mit einem anderen Bild gefüllt ist, indem Sie das src-Eigenschaftsattribut auf eine andere Datei verweisen.

Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://www.w3.org/TR/NOTE-VML#-toc416858394)

 

 