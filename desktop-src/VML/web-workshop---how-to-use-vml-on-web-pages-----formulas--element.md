---
title: Verwenden des Formulas-Elements
description: Verwenden des Formulas-Elements
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Web workshop,formulas-Element
- Entwerfen von Webseiten, Formulas-Element
- Vector Markup Language (VML),formulas-Element
- VML (Vector Markup Language),formulas-Element
- Vektorgrafik, Formulas-Element
- formulas-Element
- VML-Elemente, Formeln
- VML-Formen, Formulas-Element
- Vector Markup Language (VML), Definieren von Pfaden für Formen
- VML (Vector Markup Language),Definieren von Pfaden für Formen
- Vektorgrafiken, Definieren von Pfaden für Formen
- VML-Formen, Definieren von Pfaden
- Definieren von Pfaden für Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23810ae6612e18132566c7d546db7f1f3a569871050b7919cbd8512f3d832808
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512799"
---
# <a name="using-the-formulas-element"></a>Verwenden des Formulas-Elements

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

In diesem Thema wird veranschaulicht, wie das `<formulas>` Unterelement verwendet wird, um einen anpassbaren Pfad für eine Form zu definieren.

Sie können das <formulas> Unterelement in `<shape>` oder `<shapetype>` platzieren, um Formeln zu definieren, die den Pfad einer Form variieren können. Innerhalb des `<formulas>` Unterelements definiert ein **f-Unterelement** eine Formel, sodass ein Wert basierend auf dieser Formel ausgewertet wird. Beispielsweise definiert die Formel einen Wert, der `<v:f eqn="prod 10 4 5"/>` "10 x 4 /5" entspricht.

Sie können  viele f-Unterelemente in einem `<formulas>` Unterelement platzieren. Formeln können auf die Werte verweisen, die zuvor in anderen Formeln innerhalb desselben `<formulas>` Unterelements definiert wurden. Der Wert, der in der ersten Formel definiert ist, kann als bezeichnet @0 werden, der Wert, der in der zweiten Formel definiert ist, kann als usw. bezeichnet @1 werden.

Darüber hinaus können Sie das adj-Eigenschaftsattribut des Elements  `<shape>` angeben, z.B. adj="100, 200, 150". Innerhalb des `<formulas>` -Elements können Sie dann auf diese Werte in der **AdJ-Liste** verweisen. Der erste Wert (100) in der **AdJ-Liste** kann als 0 bezeichnet \# werden, der zweite Wert (200) kann als \# 1 usw. bezeichnet werden.

Um beispielsweise ein lächelndes Gesicht zu zeichnen, können Sie die folgende VML-Darstellung eingeben:

![shape1.gif (735 Bytes)](images/shape1f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="17520"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





-   `adj="17520"` definiert einen Wert (= 17520). Auf diesen Wert kann als 0 verwiesen \# werden.
-   Die erste Formel, `<v:f eqn="sum 33030 0 #0"/>` , definiert den Wert (= 33030 + 0 - \# 0). Auf diesen Wert kann als verwiesen @0 werden.
-   Die zweite Formel, `<v:f eqn="prod #0 4 3"/>` , definiert den Wert (= \# 0 \* 4/3). Auf diesen Wert kann als verwiesen @1 werden.
-   Die dritte Formel, `<v:f eqn="prod @0 1 3"/>` , definiert den Wert (= @0 \* 1/3). Auf diesen Wert kann als verwiesen @2 werden.
-   Die vierte Formel, `<v:f eqn="sum @1 0 @2"/>` , definiert den Wert (= + @1 0 -@2 ). Auf diesen Wert kann als verwiesen @3 werden.
-   Innerhalb des `<path>` -Elements werden die Werte, die in der ersten Formel ( ) und der vierten Formel ( ) definiert @0 @3 sind, verwendet, um die Kontur der Form zu bestimmen.

Wenn Sie die **AdJ-Liste** ändern, z. B. `adj="20000"` , werden die Werte der Formeln, die auf die **AdJ-Liste** verweisen, ebenfalls geändert, was sich wie folgt auf das lächelnde Gesicht auswirkt:

![shape2.gif (765 Bytes)](images/shape2f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="20000"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://www.w3.org/TR/NOTE-VML#-toc416858392)

 

 