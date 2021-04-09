---
title: Verwenden des Formeln-Elements
description: Verwenden des Formeln-Elements
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Webworkshop, Formeln-Element
- Entwerfen von Webseiten, Formeln-Element
- Vector Markup Language (VML), Formeln-Element
- VML (Vector Markup Language), Formeln-Element
- Vektorgrafiken, Formeln-Element
- Formeln-Element
- VML-Elemente, Formeln
- VML-Formen, Formeln-Element
- Vector Markup Language (VML), Definieren von Pfaden für Formen
- VML (Vector Markup Language), Definieren von Pfaden für Formen
- Vektorgrafiken, Definieren von Pfaden für Formen
- VML-Formen, Definieren von Pfaden
- Definieren von Pfaden für Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85ce4ebb6eea05895edf974e3ca86b1fa2ad923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039049"
---
# <a name="using-the-formulas-element"></a>Verwenden des Formeln-Elements

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

In diesem Thema wird veranschaulicht, wie Sie mit dem `<formulas>` untergeordneten Element einen anpassbaren Pfad für eine Form definieren.

Sie können das <formulas> untergeordnete Element innerhalb `<shape>` von oder platzieren `<shapetype>` , um Formeln zu definieren, die den Pfad einer Form variieren können. Innerhalb des `<formulas>` untergeordneten Elements definiert ein **f** -Unterelement eine Formel, sodass ein Wert basierend auf dieser Formel ausgewertet wird. Die Formel definiert z. b `<v:f eqn="prod 10 4 5"/>` . einen Wert, der "10 x 4/5" entspricht.

Sie können viele **f** -unter Elemente in einem `<formulas>` Unterelement platzieren. Formeln können auf die Werte verweisen, die zuvor in anderen Formeln innerhalb desselben `<formulas>` unter Elements definiert wurden. Der in der ersten Formel definierte Wert kann als bezeichnet werden @0 . der in der zweiten Formel definierte Wert kann als bezeichnet werden @1 usw.

Außerdem können Sie das **ADJ** -Eigenschafts Attribut des- `<shape>` Elements angeben, z. b. adj = "100, 200, 150". Innerhalb des- `<formulas>` Elements können Sie auf diese Werte in der **ADJ** -Liste verweisen. Der erste Wert (100) in der **ADJ** -Liste kann auf 0 (NULL \# ), auf den zweiten Wert (200) als \# 1 usw. verwiesen werden.

Wenn Sie z. b. ein lächelndes Gesicht zeichnen möchten, können Sie die folgende VML-Darstellung eingeben:

![shape1.gif (735 bytes)](images/shape1f.gif)


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





-   `adj="17520"` definiert einen Wert (= 17520). Auf diesen Wert kann als 0 verwiesen werden \# .
-   Die erste Formel, `<v:f eqn="sum 33030 0 #0"/>` , definiert den Wert (= 33030 + 0- \# 0). Auf diesen Wert kann als verwiesen werden @0 .
-   Die zweite Formel `<v:f eqn="prod #0 4 3"/>` definiert den Wert (= \# 0 \* 4/3). Auf diesen Wert kann als verwiesen werden @1 .
-   Die dritte Formel `<v:f eqn="prod @0 1 3"/>` definiert den Wert (= @0 \* 1/3). Auf diesen Wert kann als verwiesen werden @2 .
-   Die vierte Formel, `<v:f eqn="sum @1 0 @2"/>` , definiert den Wert (= @1 + 0 -@2 ). Auf diesen Wert kann als verwiesen werden @3 .
-   Innerhalb des- `<path>` Elements werden die Werte, die in der ersten ( @0 ) und vierten ( @3 )-Formel definiert sind, verwendet, um die Kontur der Form zu bestimmen.

Wenn Sie die **ADJ** -Liste ändern (z. b.), werden `adj="20000"` die Werte der Formeln, die auf die **ADJ** -Liste verweisen, ebenfalls geändert. Dies wirkt sich auf das lächelnde Gesicht wie folgt aus:

![shape2.gif (765 bytes)](images/shape2f.gif)


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





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858392) .

 

 