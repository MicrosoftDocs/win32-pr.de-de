---
title: Color2-Attribut (Fill)(VML)
description: Color2-Attribut (Fill)(VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e651245ddf9fb2a3669c3529038b5d0d8cbb3922b8a112c201858d2efd786a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007890"
---
# <a name="color2-attribute-fillvml"></a>Color2-Attribut (Fill)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert eine zweite Farbe für Füllungen. Lese-/Schreibzugriff. [VgColor](msdn-online-vml-ivgcolor.md) .

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *element* color2=" *ausdruck* ">

**Skriptsyntax**

*element* .color2="*expression*"

*expression* = *Element*.color2

**Anmerkungen**

Eine zweite Farbe wird verwendet, wenn ein Fülltyp ein Muster oder ein Farbverlauf ist. Der Standardwert ist **Weiß.**

*VML-Standardattribut*

**Beispiel**

Der Fülltyp der Form ist ein Muster, bei dem die Vordergrundfüllung durch das Quellbild definiert wird, während der transparente Hintergrund durch die zweite Farbe definiert wird.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 