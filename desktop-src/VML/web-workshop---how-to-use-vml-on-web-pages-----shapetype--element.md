---
title: Verwenden des ShapeType-Elements
description: Verwenden des ShapeType-Elements
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Webworkshop, ShapeType-Element
- Entwerfen von Webseiten, ShapeType-Element
- Vector Markup Language (VML), ShapeType-Element
- VML (Vector Markup Language), ShapeType-Element
- Vektorgrafiken, ShapeType-Element
- ShapeType-Element
- VML-Elemente, ShapeType
- VML-Formen, ShapeType-Element
- Vector Markup Language (VML), definieren häufig verwendeter Formen
- VML (Vector Markup Language), definieren häufig verwendeter Formen
- Vektorgrafiken, definieren häufig verwendeter Formen
- definieren häufig verwendeter Formen
- VML-Formen, häufig verwendete definieren
- Vector Markup Language (VML), Instanziieren von Kopien von Formen
- VML (Vector Markup Language), Instanziieren von Kopien von Formen
- Vektorgrafiken, Instanziieren von Kopien von Formen
- Instanziieren von Kopien von Formen
- VML-Formen, instanziieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa7ec47dde492231e8bcd54f68e4637454613b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474013"
---
# <a name="using-the-shapetype-element"></a>Verwenden des ShapeType-Elements

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

In diesem Thema wird veranschaulicht, wie `<shapetype>` Sie das-Element verwenden, um Ihre eigenen häufig verwendeten Formen zu definieren und dann Formen aus dem ShapeType zu instanziieren oder zu erstellen.

Wenn Sie viele Formen zeichnen möchten, die die gleichen oder ähnliche Eigenschaften aufweisen, wäre es mühsam, wenn Sie für jede Form wiederholt dieselben Eigenschafts Attribute eingeben müssten. VML stellt das- `<shapetype>` Element bereit, sodass Sie einen Prototyp einer Form definieren können. Anschließend können Sie das- `<shape>` Element verwenden, um viele Kopien von Formen aus demselben ShapeType zu instanziieren.

Sie können die drei Schritte ausführen, um einen ShapeType zu definieren, und dann eine Form aus dem ShapeType instanziieren:

1.  `<shapetype>`Geben Sie ein-Element ein, und benennen Sie es durch Angeben des ID-Attributs.
2.  Beschreiben Sie den ShapeType mithilfe der Eigenschafts Attribute oder untergeordneten Elemente.
3.  Instanziieren Sie eine Form, indem `<shape>` Sie ein-Element eingeben und das Type-Attribut der Form auf das ID-Attribut des ShapeType-Elements verweisen.

Beispielsweise geben Sie die folgenden Zeilen ein, um einen ShapeType mit dem Namen "myShape" zu erstellen:


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



Anschließend ändern Sie den ShapeType, indem Sie einige Eigenschafts Attribute festlegen, z `fillcolor="red" strokecolor="blue"` . b.. Oder Sie können unter Elemente innerhalb des ShapeType verwenden, z `<path>` . b., `<fill>` , `<stroke>` (wir werden diese unter Elemente in späteren Themen besprechen).


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



Dann Instanziieren Sie eine Form aus dem ShapeType "myShape", indem Sie angeben `type="#MyShape"` , wie in der folgenden VML-Darstellung gezeigt. Diese Form erbt alle Eigenschaften aus dem ShapeType "myShape" und wird in dem enthaltenden Feld mit einer Größe von 100 x 80 angezeigt.


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



Sie können eine andere Form aus dem ShapeType "myShape" instanziieren, indem Sie `type="#MyShape"` einige Eigenschaften wie in der folgenden VML-Darstellung angeben und überschreiben, wie `fillcolor="maroon"` in der folgenden VML-Darstellung gezeigt. Diese Form erbt alle Eigenschaften aus dem ShapeType "myShape" mit Ausnahme der FillColor-Eigenschaft und wird innerhalb des enthaltenden Felds mit einer Größe von 70 x 90 angezeigt.


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



Im folgenden finden Sie die komplette VML-Darstellung für das vorherige Beispiel:

![Typ1 \-1.gif (477 bytes)](images/type1-1.gif)![Typ1 \-2.gif (471 bytes)](images/type1-2.gif)


```HTML
<body>
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue" coordsize="21600,21600"
path="m10860,2187c10451,1746,9529,1018,9015,730,7865,152,6685,,5415,,4175,
152,2995,575,1967,1305,1150,2187,575,3222,242,4220,,5410,242,6560,575,7597l10860,
21600,20995,7597c21480,6560,21600,5410,21480,4220,21115,3222,20420,2187,19632,
1305,18575,575,17425,152,16275,,15005,,13735,152,12705,730,12176,1018,11254,1746,
10860,2187xe">
</v:shapetype>
<v:shape type="#MyShape" style='width:100;height:80;'/>
<v:shape type="#MyShape" style='width:70;height:90;' fillcolor="maroon"/>
</body>
```





Wenn eine Form von einem ShapeType-Objekt instanziiert wird, erbt Sie alle Eigenschafts Attribute aus dem ShapeType. Sie können einige oder alle geerbten Attribute überschreiben, indem Sie Attribute innerhalb des `<shape>` Elements neu definieren. Beachten Sie, dass die Vererbung nur eine Ebene ist. Dies liegt daran, dass nur ein- `<shape>` Element auf ein-Element verweisen kann `<shapetype>` . Ein- `<shapetype>` Element kann nicht auf ein anderes `<shapetype>` Element verweisen.

Außerdem gehört ein ShapeType keiner Gruppe an. Daher kann das- `<shapetype>` Element allein oder innerhalb eines-Elements angezeigt werden `<group>` . Sie können viele Formen innerhalb verschiedener Gruppen haben, die auf denselben ShapeType verweisen. Wenn ein ShapeType innerhalb einer Gruppe angezeigt wird, kann eine Form, die in einer anderen Gruppe lebt, weiterhin auf diesen ShapeType verweisen.

In der folgenden VML-Darstellung sind z. b. Rect1 und Rect2 in groupA und Rect3 in GroupB. Alle drei Rechtecke werden von myShape ShapeType instanziiert.


```HTML
<body>
...
<v:shapetype id="MyShape" fillcolor="blue" strokecolor="red"...>
</v:shapetype>

<v:group id="GroupA"...>
<v:shape id="Rect1" type="#MyShape" .../>
<v:shape id="Rect2" type="#MyShape" strokecolor="black".../>
</v:group>

<v:group id="GroupB"...>
<v:shape id="Rect3" type="#MyShape" fillcolor="green".../>
</v:group>
...
</body>
```



Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858387) .

 

 