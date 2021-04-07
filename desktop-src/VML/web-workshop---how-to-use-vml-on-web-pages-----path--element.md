---
title: Verwenden des Path-Elements
description: Verwenden des Path-Elements
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Webworkshop, Pfad Element
- Entwerfen von Webseiten, Path-Element
- Vector Markup Language (VML), Pfad Element
- VML (Vector Markup Language), Pfad Element
- Vektorgrafiken, Pfad Element
- Path-Element
- VML-Elemente, Pfad
- VML-Formen, Pfad Element
- Vector Markup Language (VML), Anpassen von Form umrissen
- VML (Vector Markup Language), Anpassen von Form umrissen
- Vektorgrafiken, Anpassen von Form umrissen
- VML-Formen, Anpassen von umrissen
- Anpassen von Form umrissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba82d0ab946ef8937b68b4934f9c4d928bd25225
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729752"
---
# <a name="using-the-path-element"></a>Verwenden des Path-Elements

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Sie haben gelernt, dass Sie die vordefinierten VML-Shape-Elemente, wie z `<oval>` . b., `<line>` ,, `<polyline>` `<curve>` , `<rect>` , `<roundrect>` und--verwenden können `<arc>` , um eine Form zu zeichnen. In diesem Thema wird veranschaulicht, wie das `<path>` -Unterelement verwendet wird, um die Kontur einer Form anzupassen.

Sie können das `<path>` untergeordnete Element innerhalb des- `<shape>` Elements oder des- `<shapetype>` Elements platzieren. Anschließend können Sie die Eigenschafts Attribute des `<path>` unter Elements verwenden, um die Kontur der Form anzupassen.

Um z. b. die in der folgenden Abbildung gezeigte angepasste Form zu zeichnen, können Sie mit dem `<path>` -Unterelement die Gliederung der Form definieren, wie in der folgenden VML-Darstellung dargestellt:

![shape1.gif (1301 Bytes)](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   Die Werte `m 8,65` geben an, dass die Zeichnung am Punkt (8, 65) beginnt.
-   Die Werte `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` geben an, dass eine gerade Linie an der aktuellen Stelle beginnt (8, 65) und am angegebenen Punkt (72, 65) endet, der zum neuen aktuellen Punkt wird. Eine neue Zeile beginnt am aktuellen Punkt (72, 65) und endet am angegebenen Punkt, der zum neuen aktuellen Punkt wird usw., bis zum letzten Punkt (60, 100).
-   `x` Gibt an, dass der Pfad mit einer geraden Linie geschlossen wird, die am aktuellen Punkt (60, 100) beginnt und am ursprünglichen Punkt endet (8, 65).
-   `e` Gibt die Zeichnung zum Ende an.

Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858391) .

 

 