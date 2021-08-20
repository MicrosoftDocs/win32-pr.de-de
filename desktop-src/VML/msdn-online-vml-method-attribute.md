---
title: VML-Methodenattribut
description: VML-Methodenattribut
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d6b5ae67f94a2fc6e27451fb1a947c8341d1f77c08a721ca7946250cee3b7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124763"
---
# <a name="vml-method-attribute"></a>VML-Methodenattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Methode, die zum Generieren einer Farbverlaufsfüllung verwendet wird. Lese-/Schreibzugriff. **VgSigmaType**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *element* method=" *ausdruck* ">

**Skriptsyntax**

*element* .method="*expression*"

*expression* = *.method-Element*

**Anmerkungen**

Mögliche Werte:



| Wert  | Beschreibung          |
|--------|----------------------|
| Keine   | Keine Sigmafüllung.       |
| Linear | Lineares Sigmafüllen.   |
| Sigma  | Sigmafüllen. Standard. |
| Beliebig    | Beliebige Sigmafüllung.      |



 

*VML-Standardattribut*

**Beispiel**

Die Form hat eine rote lineare Farbverlaufsfüllung.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 