---
title: VML-Klassenattribut
description: VML-Klassenattribut
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ada95b56430dacd09801a9aaa200c92abab064bbbb5732b369372de63c34de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602182"
---
# <a name="vml-class-attribute"></a>VML-Klassenattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bezieht sich auf eine Definition eines CSS-Stils. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* class="-Ausdruck "> 

**Skriptsyntax**

*element* .classname="*expression*"

*expression* = *Element*.classname

**Anmerkungen**

Das **Klassenattribut** ähnelt dem HTML-Standardklassenattribut, das mit CSS-Stylesheets verwendet wird. 

Beachten **Sie, dass classname** anstelle der -Klasse **für Skripts** verwendet wird. Beachten Sie auch, dass der Klassenname für die **Skripterstellung** nur gelesen werden kann. Das Ändern des Werts **von Classname** ändert nicht das Rendering der Form.

*VML-Standardattribut*

**Siehe auch**

[Formen](shape-element--vml.md)

**Beispiel**

Eine Klasse für **breite wird** mit dem Stil erstellt.


```HTML
   .narrowstyle {width:50;height:100}
```



Anschließend wird auf die Breite verwiesen, indem der Stil ein- und aus dem Format besteht. Beachten Sie, dass width undheight  nicht im Formatattribut definiert sind, sondern durch den Stil definiert werden.


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



Beachten Sie, **dass Class** nur für CSS-Typattribute gilt.

 

 