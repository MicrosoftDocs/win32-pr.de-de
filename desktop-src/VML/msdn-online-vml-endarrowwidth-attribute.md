---
title: VML-EndArrowWidth-Attribut
description: VML-EndArrowWidth-Attribut
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90270cfc554d7e2dea70b313507fd7f61bf3a073c0e27c03c82d8a696f2939a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119396080"
---
# <a name="vml-endarrowwidth-attribute"></a>VML-EndArrowWidth-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert eine Pfeilspitzenbreite für das Ende einer Linie. Lese-/Schreibzugriff. **VgArrowheadWidth**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* endarrowwidth="-Ausdruck "> 

**Skriptsyntax**

*element* .endarrowwidth="*expression*"

*expression* = *Element*.endarrowwidth

**Anmerkungen**

Mögliche Werte:

-   Schmalen
-   Mittel (Standard)
-   Breite

*VML-Standardattribut*

**Beispiel**

Eine Linie wird mit einer breiten klassischen Pfeilspitze am Ende des Strichs gezeichnet.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 