---
title: VML-Attribut "StartArrowWidth"
description: VML-Attribut "StartArrowWidth"
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d427db8e504fca57fc77b24b7b5fa1360ed7716276cd67b43c55ee8d0552d8f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513240"
---
# <a name="vml-startarrowwidth-attribute"></a>VML-Attribut "StartArrowWidth"

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Pfeilspitzenbreite für den Anfang einer Linie. Lese-/Schreibzugriff. **VgArrowheadWidth**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* startarrowwidth=" *expression* ">

**Skriptsyntax**

*element* .startarrowwidth="*expression*"

*expression* = *Element*.startarrowwidth

**Anmerkungen**

Mögliche Werte:

-   Schmalen
-   Mittel (Standard)
-   Breite

VML-Standardattribut

**Beispiel**

Eine Linie wird mit einer breiten klassischen Pfeilspitze am Anfang des Strichs gezeichnet.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 