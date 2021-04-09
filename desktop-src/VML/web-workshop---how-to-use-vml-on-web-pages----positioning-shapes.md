---
title: Positionieren von Formen
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Webworkshop, Positionieren von Formen
- Entwerfen von Webseiten, Positionieren von Formen
- Vector Markup Language (VML), Positionieren von Formen
- VML (Vector Markup Language), Positionieren von Formen
- Vektorgrafiken, Positionierungs Formen
- VML-Formen, positionieren
- Positionieren von Formen
- Vector Markup Language (VML), statischer Positions Stil
- VML (Vector Markup Language), statischer Positions Stil
- Vektorgrafiken, statischer Positions Stil
- statischer Positions Stil
- Vector Markup Language (VML), relativer Positions Stil
- VML (Vector Markup Language), relativer Positions Stil
- Vektorgrafiken, relativer Positions Stil
- relativer Positions Stil
- Vector Markup Language (VML), absoluter Positions Stil
- VML (Vector Markup Language), absoluter Positions Stil
- Vektorgrafiken, absoluter Positions Stil
- absoluter Positions Stil
- Vector Markup Language (VML), z-Index-Positions Stil
- VML (Vector Markup Language), z-Index-Positions Stil
- Vektorgrafiken, z-Index Positions Stil
- z-Index-Positions Stil
- Vector Markup Language (VML), Drehungs Positions Stil
- VML (Vector Markup Language), Drehungs Positions Stil
- Vektorgrafiken, Drehungs Positions Stil
- Stil der Drehungs Position
- Vector Markup Language (VML), drehpositions Stil
- VML (Vector Markup Language), Flip-Positions Stil
- Vektorgrafiken, drehpositions Stil
- Positions Stil kippen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8e01d0c7962467b1894f0f4c2c6cd1f6b01509
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039147"
---
# <a name="positioning-shapes"></a>Positionieren von Formen

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Sie haben gelernt, wie Formen mithilfe von VML auf einer Webseite gezeichnet werden können. In diesem Thema verwenden Sie VML zum genauen Positionieren von Grafiken auf einer Webseite.

VML verwendet dieselbe Syntax, die in den Abschnitten " [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) " und " [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) " von [CSS2](https://www.w3.org/TR/PR-CSS2/) definiert ist, um Formen auf einer Webseite zu positionieren. Sie können " [static](#static)", " [relative](#relative)" oder " [absolute](#absolute) " verwenden, um zu bestimmen, wo sich der Basispunkt auf einer Webseite befindet. Anschließend können Sie die Attribute **Top** und **left** Style verwenden, um den Offset von dem Basispunkt anzugeben, an dem das enthaltende Feld für die Form positioniert wird.

Sie können [z-Index](#z-index) auch verwenden, um die z-Reihenfolge von Formen auf einer Webseite anzugeben.

Außerdem bietet VML [Drehung](#rotation) und [kippen](#flip) zum Drehen und Kippen von Formen.

In diesem Thema:

-   [static](#static)
-   [relative](#relative)
-   [absolute](#absolute)
-   [z-index](#z-index)
-   [Rotations](#rotation)
-   [flip](#flip)
-   [Zusammenfassung](#summary)

## <a name="static"></a>static

Der Standard Positions Stil ist statisch, wodurch Browser angewiesen werden, die Form am aktuellen Punkt (dem Basispunkt) im Text Fluss zu positionieren und die Einstellungen in den Attributen **Top** und **left** Style zu ignorieren.

In der folgenden VML-Darstellung wird das rote Oval z. b. unmittelbar nach dem Text "Anfang der Form:" positioniert, wie in der folgenden Abbildung dargestellt:

![shape1 \-ps.gif (2123 Bytes)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="relative"></a>relative

Wenn Sie das Positions Stil Attribut auf "relative" festlegen, können Sie das enthaltende Feld mit einem Offset vom aktuellen Punkt (dem Basispunkt) im Text Fluss platzieren. Der Offset wird durch die Einstellungen in den Attributen **Top** und **left** Style festgelegt. Beachten Sie, dass das als relativ positionierte enthaltende Feld Speicherplatz im Text Fluss einnimmt.

Beispielsweise wird in der folgenden VML-Darstellung das rote Oval 20 Punkte von Links und 10 Punkte vom oberen Rand bis zum aktuellen Punkt im Text Fluss positioniert, wie in der folgenden Abbildung dargestellt:

![shape3.gif (2048 Bytes)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="absolute"></a>absolute

Wenn Sie das Positions Format Attribut auf "absolute" festlegen, können Sie das enthaltende Feld mit einer exakten Entfernung von der oberen linken Ecke (dem Basispunkt) des übergeordneten Elements (dem positionierten Element, das die Form enthält) platzieren. Beachten Sie, dass das als absolut positionierte enthaltende Feld keinen Speicherplatz im Text Fluss belegt.

In der folgenden VML-Darstellung ist das rote Oval z. b. im- `<body>` Element (der gesamten Webseite) enthalten. Daher befindet sich der Basispunkt in der linken oberen Ecke der Webseite. Das enthaltende Feld für das Oval ist genau 20 Punkte von der linken Seite und 10 Punkte von oben, relativ zur oberen linken Ecke der Webseite positioniert, wie in der folgenden Abbildung dargestellt:

![shape2.gif (2006 Bytes)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="z-index"></a>z-index

Es ist möglich, eine Form zu positionieren, die eine andere Form überlappt. Normalerweise wird die im HTML-Code zuletzt aufgeführte Grafik im oberen Bereich angezeigt.

In VML können Sie die z-Reihenfolge steuern, indem Sie das **z-Index-** Format Attribut verwenden. Der Wert dieses Attributs kann 0 (null), eine positive Ganzzahl oder eine negative Ganzzahl sein. Die Grafik mit einem größeren z-index-Wert wird auf der Grafik mit einem kleineren z-index-Wert angezeigt. Wenn beide Grafiken denselben z-index-Wert aufweisen, wird die Grafik, die zuletzt im HTML-Code aufgeführt ist, oben angezeigt.

In der folgenden VML-Darstellung wird das rote Oval beispielsweise oberhalb des blauen Rechtecks angezeigt. Dies liegt daran, dass der z-index-Wert des roten Oval größer ist als der z-index-Wert des blauen Rechtecks.

![shape4.gif (572 Bytes)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





Wenn Sie den z-Index ändern, wie in der folgenden VML-Darstellung gezeigt, würde sich das rote Oval hinter das blaue Rechteck bewegen.

![shape5.gif (469 bytes)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





Wenn Sie eine negative ganze Zahl angeben, können Sie z-Index verwenden, um Grafiken hinter dem normalen Text Fluss zu positionieren, wie in der folgenden VML-Darstellung gezeigt.

![shape6.gif (2125 Bytes)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="rotation"></a>Drehung

Mithilfe des Attributs " **Rotation** " können Sie angeben, wie viele Grad eine Form auf der Achse aktiviert werden soll. Ein positiver Wert weist auf eine Drehung im Uhrzeigersinn hin. ein negativer Wert gibt eine Drehung gegen den Uhrzeigersinn an.

Wenn Sie z. b. **Style**= '... Rotation: 90 ' Sie können die Form 90 Grad im Uhrzeigersinn drehen.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="flip"></a>flip

Sie können das Attribut " **Flip** Style" verwenden, um eine Form auf der x-oder y-Achse entsprechend der folgenden Tabelle zu kippen:



| Wert | BESCHREIBUNG                                                  |
|-------|--------------------------------------------------------------|
| x     | Drehen der gedrehten Form um die y-Achse (Umkehrung der x-Ordinate) |
| Y     | Drehen der gedrehten Form um die x-Achse (y-Ordinate umkehren) |



 

In der Flip-Eigenschaft können sowohl x als auch y angegeben werden.

Wenn Sie z. b. **Style**= '... Flip: x y ", Sie kippen die Form auf der x-und der y-Achse.

[![zurück ](images/top.gif) zum Anfang](#top)

## <a name="summary"></a>Zusammenfassung

Je nachdem, was Sie gelernt haben, können Sie eine Form genau auf einer Webseite positionieren, indem Sie die folgenden Schritte ausführen:

1.  Legen Sie fest, wo die Form auf einer Webseite angezeigt werden soll, und wählen Sie die Größe der Form aus.
2.  Geben Sie **Style**= ' Position: relative (oder relative) ' an, um den Basispunkt zu bestimmen.
3.  Verwenden Sie **Links** und **oben** , um den Offset vom Basispunkt anzugeben.
4.  Verwenden Sie **Width** und **height** , um die Größe des enthaltenden Felds für die Form anzugeben.
5.  Verwenden Sie **z-Index** , um die z-Reihenfolge der Form anzugeben.

 

 