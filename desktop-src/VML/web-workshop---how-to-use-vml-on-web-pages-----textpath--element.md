---
title: Verwenden des TextPath-Elements
description: Verwenden des TextPath-Elements
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- Webworkshop, TextPath-Element
- Entwerfen von Webseiten, TextPath-Element
- Vector Markup Language (VML), TextPath-Element
- VML (Vector Markup Language), TextPath-Element
- Vektorgrafiken, TextPath-Element
- TextPath-Element
- VML-Elemente, TextPath
- VML-Formen, TextPath-Element
- Vector Markup Language (VML), Zeichnen von Text
- VML (Vector Markup Language), Zeichnen von Text
- Vektorgrafiken, Zeichnen von VML-Text
- Zeichnen von Text
- VML-Formen, Zeichnen von Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148c032d14307dc07ec56911f4c5cc45a4c69664
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102263"
---
# <a name="using-the-textpath-element"></a>Verwenden des TextPath-Elements

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

In diesem Thema wird veranschaulicht, wie das-Element verwendet wird, `<textpath>` um Text mit verschiedenen Stilen zu zeichnen.

Sie können das `<textpath>` untergeordnete Element innerhalb `<shape>` von oder platzieren `<shapetype>` , um Text zu zeichnen. Sie können dann die Eigenschafts Attribute des `<textpath>` unter Elements verwenden, um den Text anzupassen. Sie können auch das `<formulas>` untergeordnete-Element verwenden, um die Kontur des Texts zu definieren.

Wenn Sie z. b. den in der folgenden Abbildung gezeigten Text erstellen möchten, können Sie die VML-Darstellung unten eingeben. Beachten Sie, dass wir das- `<shapetype>` Element verwenden, um einen Prototyp für den Text Umriss zu definieren. Anschließend werden zwei Formen aus dem gleichen ShapeType instanziiert. Sie können einfach das Attribut der **Zeichen** folgen Eigenschaft ändern, um anderen Text anzuzeigen.

![shape1 \-1.gif (4898 Bytes)](images/shape1-1t.gif)

![shape1 \-2.gif (2789 Bytes)](images/shape1-2t.gif)


```HTML
<v:shapetype id="MyShape"
coordsize="21600,21600" adj="9931"
path="m0@0c7200@2,14400@1,21600,0m0@5c7200@6,14400@6,21600@5e">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="prod #0 3 4"/>
<v:f eqn="prod #0 5 4"/>
<v:f eqn="prod #0 3 8"/>
<v:f eqn="prod #0 1 8"/>
<v:f eqn="sum 21600 0 @3"/>
<v:f eqn="sum @4 21600 0"/>
<v:f eqn="prod #0 1 2"/>
<v:f eqn="prod @5 1 2"/>
<v:f eqn="sum @7 @8 0"/>
<v:f eqn="prod #0 7 8"/>
<v:f eqn="prod @5 1 3"/>
<v:f eqn="sum @1 @2 0"/>
<v:f eqn="sum @12 @0 0"/>
<v:f eqn="prod @13 1 4"/>
<v:f eqn="sum @11 14400 @14"/>
</v:formulas>
<v:path textpathok="t" />
<v:textpath on="t" fitshape="t" xscale="t"/>
</v:shapetype>

<v:shape type="#MyShape" style='position:relative; top:5; left:5;
width:261.6pt;height:71.45pt;' adj="8717" fillcolor="red" strokeweight="1pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/> <v:textpath
style='font-family:"Arial Black";v-text-kern:t' trim="t"
fitpath="t" xscale="f" string="Hello World !"/>
</v:shape>

<v:shape type="#MyShape" style='position:relative; top:120; left:5; width:207pt;
height:63pt;' adj="8717" fillcolor="blue" strokeweight="2pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/>
<v:textpath style='font-family:"Times New Roman";v-text-kern:t'
trim="t" fitpath="t" xscale="f" string="VML"/>
</v:shape>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858398) .

 

 