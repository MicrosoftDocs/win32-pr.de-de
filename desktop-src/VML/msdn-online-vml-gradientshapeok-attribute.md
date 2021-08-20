---
title: VML GradientShapeOK-Attribut
description: VML GradientShapeOK-Attribut
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c25620f8ebc05905b83f3abab7b52f7a206b6bafb522b0104f06fd8f46d6bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124773"
---
# <a name="vml-gradientshapeok-attribute"></a>VML GradientShapeOK-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob ein Farbverlaufspfad aus wiederholten konzentrischen Pfaden besteht. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Path](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *element* gradientshapeok=" *expression* ">

**Skriptsyntax**

*element* .gradientshapeok="*expression*"

*expression* = *Element*.gradientshapeok

**Anmerkungen**

**True** gibt an, dass der Pfad mit einer konzentrischen Farbverlaufsfüllung gefüllt wird, wobei der Pfad als wiederholte Form des Farbverlaufs verwendet wird. Der Standardwert ist **False.**

*VML-Standardattribut*

**Beispiel**

Der Pfad wird mit einer konzentrischen Farbverlaufsfüllung gefüllt, die aus wiederholten Rechtecke besteht.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 