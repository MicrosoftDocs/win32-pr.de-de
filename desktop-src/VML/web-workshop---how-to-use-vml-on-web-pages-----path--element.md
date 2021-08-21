---
title: Verwenden des Path-Elements
description: Verwenden des Path-Elements
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Web-Workshop,Path-Element
- Entwerfen von Webseiten, Path-Element
- Vector Markup Language (VML),Path-Element
- VML (Vector Markup Language),Path-Element
- Vektorgrafik,Path-Element
- path-Element
- VML-Elemente,Pfad
- VML-Formen, Path-Element
- Vector Markup Language (VML), Anpassen von Formgliederungen
- VML (Vector Markup Language), Anpassen von Formgliederungen
- Vektorgrafiken,Anpassen von Formgliederungen
- VML-Formen, Anpassen von Konturen
- Anpassen von Formgliederungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cbb27dbc2b039478903f697b02cefb14464b71a96ab2165db124d0a0053a400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057183"
---
# <a name="using-the-path-element"></a>Verwenden des Path-Elements

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Sie haben gelernt, dass Sie die vordefinierten VML-Formelemente wie , , , , , , und verwenden können, um `<oval>` `<line>` eine Form zu `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` zeichnen. In diesem Thema wird veranschaulicht, wie sie das Unterelement verwenden, um die `<path>` Kontur einer Form anzupassen.

Sie können das `<path>` Unterelement innerhalb des - oder `<shape>` -Elements `<shapetype>` platzieren. Anschließend können Sie die Eigenschaftenattribute des Unterelements verwenden, um `<path>` die Kontur der Form anzupassen.

Um beispielsweise die benutzerdefinierte Form zu zeichnen, die in der folgenden Abbildung dargestellt ist, können Sie das Unterelement verwenden, um die Kontur der Form zu definieren, wie in der folgenden `<path>` VML-Darstellung gezeigt:

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





-   Die Werte `m 8,65` geben an, dass die Zeichnung an der Stelle beginnt (8,65).
-   Die Werte geben an, dass eine gerade Linie am aktuellen Punkt (8, 65) beginnt und am angegebenen Punkt `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` (72, 65) endet, der zum neuen aktuellen Punkt wird. Eine neue Zeile beginnt am aktuellen Punkt (72, 65) und endet am angegebenen Punkt, der zum neuen aktuellen Punkt wird, und so weiter, bis zum letzten Punkt (60, 100).
-   `x` gibt an, dass der Pfad um eine gerade Linie geschlossen wird, die am aktuellen Punkt (60, 100) beginnt und am ursprünglichen Punkt (8, 65) endet.
-   `e` gibt an, dass das Zeichnen nicht mehr angezeigt wird.

Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://www.w3.org/TR/NOTE-VML#-toc416858391)

 

 