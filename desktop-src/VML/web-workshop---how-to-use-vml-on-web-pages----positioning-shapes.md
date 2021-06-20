---
title: Positionieren von Formen
description: In diesem Artikel wird die Positionierung von Formen in VML beschrieben, einem Feature, das seit Windows Internet Explorer 9 veraltet ist.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Web-Workshop,Positionieren von Formen
- Entwerfen von Webseiten, Positionieren von Formen
- Vector Markup Language (VML), Positionieren von Formen
- VML (Vector Markup Language),Positionieren von Formen
- Vektorgrafiken,Positionieren von Formen
- VML-Formen, Positionierung
- Positionieren von Formen
- Vector Markup Language (VML), statischer Positionsstil
- VML (Vector Markup Language), statischer Positionsstil
- Vektorgrafiken, statischer Positionsstil
- Statischer Positionsstil
- Vector Markup Language (VML), relative Position
- VML (Vector Markup Language),relative Position
- Vektorgrafik, relative Position
- Relative Position
- Vector Markup Language (VML), absolute Position
- VML (Vector Markup Language),absoluter Positionsstil
- Vektorgrafiken, absolute Position
- Absoluter Positionsstil
- Vector Markup Language (VML), Z-Indexpositionsstil
- VML (Vector Markup Language),Z-Indexpositionsstil
- Vektorgrafiken, Z-Indexpositionsstil
- z-index position style
- Vector Markup Language (VML), Drehpositionsstil
- VML (Vector Markup Language), Drehpositionsstil
- Vektorgrafik, Drehpositionsstil
- Drehpositionsstil
- Vector Markup Language (VML), Kipppositionsstil
- VML (Vector Markup Language),FlipPosition Style
- Vektorgrafiken, Kipppositionsstil
- Kipppositionsstil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c96a8de891ed1bbd1b9bfee9eff52ede946247b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407713"
---
# <a name="positioning-shapes"></a>Positionieren von Formen

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Sie haben gelernt, wie Sie mithilfe von VML Formen auf einer Webseite zeichnen und färben. In diesem Thema verwenden Sie VML, um Grafiken genau auf einer Webseite zu positionieren.

VML verwendet dieselbe Syntax, die in den Abschnitten [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) und Visual [Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) von [CSS2](https://www.w3.org/TR/PR-CSS2/) definiert ist, um Formen auf einer Webseite zu positionieren. Sie können [statische](#static), [relative oder](#relative) [absolute](#absolute) Verwenden, um zu bestimmen, wo sich der Basispunkt auf einer Webseite befindet. Sie können dann  die  Attribute oben und links verwenden, um den Offset von dem Basispunkt anzugeben, an dem das enthaltende Feld für die Form positioniert wird.

Sie können [z-index auch verwenden,](#z-index) um die Z-Reihenfolge von Formen auf einer Webseite anzugeben.

Darüber hinaus bietet VML [Drehung und](#rotation) Kippen, um Formen zu drehen oder zu kippen. [](#flip)

In diesem Thema:

-   [static](#static)
-   [relative](#relative)
-   [absolute](#absolute)
-   [z-index](#z-index)
-   [Drehung](#rotation)
-   [flip](#flip)
-   [Zusammenfassung](#summary)

## <a name="static"></a>static

Der Standardpositionsstil ist statisch, wodurch Browser angewiesen werden, die Form am aktuellen Punkt (dem  Basispunkt) im Textfluss zu positionieren und die Einstellungen in den Formatattributen oben und links zu ignorieren. 

In der folgenden VML-Darstellung wird das rote Oval beispielsweise direkt nach dem Text "Anfang der Form:" positioniert, wie in der folgenden Abbildung dargestellt:

![shape1 \-ps.gif (2123 Bytes)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="relative"></a>relative

Wenn Sie das Positionsformatattribut auf "relative" festlegen, können Sie das enthaltende Feld mit einem Offset vom aktuellen Punkt (dem Basispunkt) im Textfluss platzieren. Der Offset wird durch die Einstellungen in den **Formatattributen oben** und **links** bestimmt. Beachten Sie, dass das enthaltende Feld, das als relativ positioniert ist, Platz im Textfluss benötigt.

In der folgenden VML-Darstellung ist das rote Oval z. B. 20 Punkte von links und 10 Punkte von oben relativ zum aktuellen Punkt im Textfluss positioniert, wie in der folgenden Abbildung dargestellt:

![shape3.gif (2048 Bytes)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="absolute"></a>absolute

Wenn Sie das Positionsformatattribut auf "absolut" festlegen, können Sie den enthaltenden Feld genau in einen Abstand von der oberen linken Ecke (dem Basispunkt) des übergeordneten Elements (dem positionierten Element, das die Form enthält) platzieren. Beachten Sie, dass das enthaltende Feld, das als absolut positioniert ist, keinen Platz im Textfluss an sich nimmt.

In der folgenden VML-Darstellung ist das rote Oval beispielsweise im -Element (die gesamte Webseite) enthalten. Daher befindet sich der Basispunkt in der oberen linken Ecke `<body>` der Webseite. Das enthaltende Feld für das Oval ist genau 20 Punkte von links und 10 Punkte von oben relativ zur oberen linken Ecke der Webseite positioniert, wie in der folgenden Abbildung gezeigt:

![shape2.gif (2006 Bytes)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="z-index"></a>z-index

Es ist möglich, eine Form zu positionieren, die eine andere Form überlappt. Normalerweise wird die Grafik, die zuletzt im HTML-Code aufgeführt ist, oben angezeigt.

In VML können Sie die Z-Reihenfolge mithilfe des **Z-Index-Formatattributs** steuern. Der Wert dieses Attributs kann 0 (null), eine positive ganze Zahl oder eine negative ganze Zahl sein. Die Grafik mit einem größeren Z-Index-Wert wird oben in der Grafik mit einem kleineren Z-Index-Wert angezeigt. Wenn beide Grafiken denselben Z-Index-Wert haben, wird oben die Grafik angezeigt, die zuletzt im HTML-Code aufgeführt ist.

In der folgenden VML-Darstellung wird beispielsweise das rote Oval über dem blauen Rechteck angezeigt. Dies liegt daran, dass der Z-Index-Wert des roten Ovals größer als der Z-Index-Wert des blauen Rechtecks ist.

![shape4.gif (572 Bytes)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





Wenn Sie den Z-Index ändern, wie in der folgenden VML-Darstellung gezeigt, würde sich das rote Oval hinter dem blauen Rechteck bewegen.

![shape5.gif (469 Bytes)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





Wenn Sie eine negative ganze Zahl bereitstellen, können Sie z-index verwenden, um Grafiken hinter dem normalen Textfluss zu positionieren, wie in der folgenden VML-Darstellung gezeigt.

![shape6.gif (2125 Bytes)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="rotation"></a>Drehung

Sie können  das Rotationsformatattribut verwenden, um anzugeben, wie viele Grad eine Form auf der Achse drehen soll. Ein positiver Wert gibt eine Drehung im Uhrzeigersinn an. Ein negativer Wert gibt eine Drehung gegen den Uhrzeigersinn an.

Wenn Sie z. B. **style**='... angeben rotation:90' können Sie die Form um 90 Grad im Uhrzeigersinn drehen.

[![zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="flip"></a>flip

Sie können das **Flip-Stilattribut** verwenden, um eine Form auf der x- oder y-Achse gemäß der folgenden Tabelle zu kippen:



| Wert | Beschreibung                                                  |
|-------|--------------------------------------------------------------|
| x     | Drehen der gedrehten Form um die y-Achse (X-Ordinate umkehren) |
| j     | Drehen Sie die gedrehte Form um die x-Achse (invertierte y-Koordinaten). |



 

Sowohl x als auch y können in der Flip-Eigenschaft angegeben werden.

Wenn Sie z. B. **style**='... eingeben, flip:x y' wird die Form sowohl auf der x- als auch auf der y-Achse gekippt.

[![Zurück zum Anfang ](images/top.gif) Zurück zum Anfang](#top)

## <a name="summary"></a>Zusammenfassung

Je nachdem, was Sie gelernt haben, können Sie eine Form auf einer Webseite genau positionieren, indem Sie die folgenden Schritte ausführen:

1.  Entscheiden Sie, wo die Form auf einer Webseite angezeigt werden soll, und legen Sie die Größe der Form fest.
2.  Geben Sie **style**='position:relative (or relative)' an, um den Basispunkt zu bestimmen.
3.  Verwenden Sie **links** und **oben,** um den Offset vom Basispunkt anzugeben.
4.  Verwenden Sie **Breite** und **Höhe,** um die Größe des enthaltenden Felds für die Form anzugeben.
5.  Verwenden Sie **z-index,** um die Z-Reihenfolge der Form anzugeben.

 

 