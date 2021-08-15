---
title: On-Attribut (Schatten)(VML)
description: On-Attribut (Schatten)(VML)
ms.assetid: 234fe63e-8a4a-4067-9d05-a8990d1cee5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda4d33fbd22d2a7913f13ae8ad874ba3240944f06303f020888aeaafaee88f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345851"
---
# <a name="on-attribute-shadowvml"></a>On-Attribut (Schatten)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob ein Schatten angezeigt wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *element* on="-Ausdruck "> 

**Skriptsyntax**

*element* .on="*expression*"

*expression* = *.on-Element*

**Anmerkungen**

True **gibt an,** dass der Schatten angezeigt wird. Der Standardwert ist **False**.

*VML-Standardattribut*

**Beispiel**

Der Schatten wird angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True"/>
   </v:shape>
```





 

 