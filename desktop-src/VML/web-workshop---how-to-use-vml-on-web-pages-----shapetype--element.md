---
title: Verwenden des Shapetype-Elements
description: Verwenden des Shapetype-Elements
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Web workshop,shapetype-Element
- Entwerfen von Webseiten, Shapetype-Element
- Vector Markup Language (VML),shapetype-Element
- VML (Vector Markup Language),shapetype-Element
- Vektorgrafik, Shapetype-Element
- shapetype-Element
- VML-Elemente, Shapetype
- VML-Formen, Shapetype-Element
- Vector Markup Language (VML), Definieren häufig verwendeter Formen
- VML (Vector Markup Language),Definieren häufig verwendeter Formen
- Vektorgrafiken, Definieren häufig verwendeter Formen
- Definieren häufig verwendeter Formen
- VML-Formen, definieren häufig verwendete Formen
- Vector Markup Language (VML), Instanziieren von Kopien von Formen
- VML (Vector Markup Language),Instanziieren von Kopien von Formen
- Vektorgrafiken, Instanziieren von Kopien von Formen
- Instanziieren von Kopien von Formen
- VML-Formen,Instanziieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d815d9f5f911e1a34d558496881ae606819d328a501c635ff463a84f2926ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512649"
---
# <a name="using-the-shapetype-element"></a>Verwenden des Shapetype-Elements

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

In diesem Thema wird veranschaulicht, wie Sie das -Element verwenden, `<shapetype>` um Ihre eigenen häufig verwendeten Formen zu definieren und dann Formen aus dem Shape-Typ zu instanziieren oder zu erstellen.

Wenn Sie viele Formen zeichnen möchten, die über die gleichen oder ähnliche Eigenschaften verfügen, wäre es mühsam, wenn Sie wiederholt die gleichen Eigenschaftsattribute für jede Form eingeben müssten. VML stellt das `<shapetype>` -Element bereit, damit Sie einen Prototyp einer Form definieren können. Anschließend können Sie das `<shape>` -Element verwenden, um viele Kopien von Formen aus dem gleichen Shape-Typ zu instanziieren.

Sie können die drei Schritte ausführen, um einen Shape-Typ zu definieren, und dann eine Form aus dem Shape-Typ instanziieren:

1.  Geben Sie ein `<shapetype>` Element ein, und geben Sie ihm einen Namen, indem Sie das ID-Attribut angeben.
2.  Beschreiben Sie den Shape-Typ mit seinen Eigenschaftsattributen oder Unterelementen.
3.  Instanziieren Sie eine Form, indem Sie ein `<shape>` Element eingeben, und verweisen Sie das Typattribut der Form auf das ID-Attribut des Shape-Typs.

Geben Sie beispielsweise die folgenden Zeilen ein, um einen Shape-Typ namens "MyShape" zu erstellen:


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



Anschließend ändern Sie den Shape-Typ, indem Sie einige Eigenschaftsattribute festlegen, `fillcolor="red" strokecolor="blue"` z. B. . Alternativ können Sie untergeordnete Elemente innerhalb des Shape-Datentyps verwenden, z. B. `<path>` `<fill>` , , `<stroke>` (diese Unterelemente werden in späteren Themen behandelt).


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



Anschließend instanziieren Sie eine Form aus dem Shape-Typ "MyShape", indem Sie `type="#MyShape"` angeben, wie in der folgenden VML-Darstellung gezeigt. Diese Form erbt alle Eigenschaften vom Shape-Typ "MyShape" und wird in ihrem enthaltenden Feld mit einer Größe von 100 x 80 angezeigt.


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



Sie können eine andere Form aus dem Shape-Typ "MyShape" instanziieren, indem Sie `type="#MyShape"` einige Eigenschaften angeben und überschreiben, z. B. , wie in der folgenden `fillcolor="maroon"` VML-Darstellung gezeigt. Diese Form erbt alle Eigenschaften vom Shape-Typ "MyShape" mit Ausnahme der fillcolor-Eigenschaft und wird in ihrem enthaltenden Feld mit einer Größe von 70 x 90 angezeigt.


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



Dies ist die vollständige VML-Darstellung für das vorherige Beispiel:

![type1 \-1.gif (477 Byte)](images/type1-1.gif)![type1 \-2.gif (471 Bytes)](images/type1-2.gif)


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





Wie Sie gelernt haben, erbt eine Form, wenn sie von einem Shape-Typ instanziiert wird, alle Eigenschaftsattribute vom Shape-Typ. Sie können einige oder alle geerbten Attribute überschreiben, indem Sie Attribute innerhalb des Elements neu `<shape>` definieren. Beachten Sie, dass die Vererbung nur eine Ebene ist. Dies liegt daran, dass nur ein `<shape>` -Element auf ein -Element verweisen `<shapetype>` kann. Ein `<shapetype>` -Element kann nicht auf ein anderes `<shapetype>` Element verweisen.

Außerdem gehört ein Shape-Typ keiner Gruppe an. Daher kann das `<shapetype>` Element allein oder innerhalb eines Elements angezeigt `<group>` werden. Sie können viele Formen in verschiedenen Gruppen haben, die auf denselben Shape-Typ verweisen. Wenn ein Shape-Typ innerhalb einer Gruppe angezeigt wird, kann eine Form, die in einer anderen Gruppe vorhanden ist, weiterhin auf diesen Shape-Typ verweisen.

In der folgenden VML-Darstellung befinden sich Rect1 und Rect2 beispielsweise in GroupA und Rect3 in GroupB. Alle drei Rechtecke werden über den Shape-Typ MyShape instanziiert.


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



Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://www.w3.org/TR/NOTE-VML#-toc416858387)

 

 