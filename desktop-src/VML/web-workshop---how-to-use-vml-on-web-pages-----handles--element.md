---
title: Verwenden des Handles-Elements
description: Verwenden des Handles-Elements
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Web-Workshop,Handles-Element
- Entwerfen von Webseiten,Handles-Element
- Vector Markup Language (VML),handles-Element
- VML (Vector Markup Language),handles-Element
- Vektorgrafik,Handles-Element
- handles-Element
- VML-Elemente,Handles
- VML-Formen,Handles-Element
- Vector Markup Language (VML), Anfügen von Text an Formen
- VML (Vector Markup Language),Anfügen von Text an Formen
- Vektorgrafiken,Anfügen von Text an Formen
- VML-Formen,Anfügen von Text
- Anfügen von Text an Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d504024a3d5c42caf8af116a08e5bd8787905991f14c4181fe3a75b10f4814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057207"
---
# <a name="using-the-handles-element"></a>Verwenden des Handles-Elements

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

In diesem Thema wird veranschaulicht, wie Das -Element verwendet wird, `<handles>` um Text an eine Form anfügen.

Sie können das Unterelement in oder platzieren, um Benutzeroberflächenelemente zu definieren, die die `<handles>` `<shape>` `<shapetype>` **AdJ-Werte** in der Form variieren können.

Beispielsweise können Sie, wie in der folgenden VML-Darstellung gezeigt, ein Anpassungshandl (gelbes Feld) bereitstellen, das Benutzer einfach ziehen können, um die Form anzupassen.

Hinweis: Die Handles sind verfügbar, wenn diese VML-Form in Microsoft Office-Anwendungen angezeigt wird, in denen die Form manipulierbar sein soll.

![shape1.gif (564 Bytes)](images/shape1h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="16200,5400"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





Beachten Sie, dass der einzige Unterschied zwischen der vorherigen VML-Darstellung und der folgenden der **adj-Wert** ist.

![shape2.gif (1361 Bytes)](images/shape2h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="11304,6600"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation.](https://www.w3.org/TR/NOTE-VML#-toc416858393)

 

 