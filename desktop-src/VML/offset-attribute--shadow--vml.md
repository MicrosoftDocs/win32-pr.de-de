---
title: Offset-Attribut (Schatten)(VML)
description: Offset-Attribut (Schatten)(VML)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0683e9536e10bed141ecca56b4335d6221c5ced7e3d26220908aa388b453843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596905"
---
# <a name="offset-attribute-shadowvml"></a>Offset-Attribut (Schatten)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert, wie weit sich der Schatten über die Form erstreckt. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *element* offset=" *ausdruck* ">

**Skriptsyntax**

*element* .offset="*expression*"

*expression* = *Element*.offset

**Anmerkungen**

Der Standardoffset für den x-Wert ist 2pt, und der Standardwert für den y-Wert ist 2pt. Werte sind entweder eine absolute Messung oder ein Bruchteil der Form. Bei Bruch liegen sie zwischen 50 % und -50 %.

*VML-Standardattribut*

**Beispiel**

Die Form hat einen Schatten mit einem Offset von 5 Punkten nach unten und 10 Punkten rechts.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 