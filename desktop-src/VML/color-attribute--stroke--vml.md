---
title: Farbattribut (Stroke)(VML)
description: Farbattribut (Stroke)(VML)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17b3dd30d95765c98ec754526349b2bdc274696112043065fa7ddc7d894b582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125370"
---
# <a name="color-attribute-strokevml"></a>Farbattribut (Stroke)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Farbe eines Strichs. Lese-/Schreibzugriff. **VgColor**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* color=" *ausdruck* ">

**Skriptsyntax**

*element* .color="*expression*"

*expression* = *Element*.color

**Anmerkungen**

Überschreibt das **StrokeColor-Attribut** einer Form. Der Standardwert ist **schwarz.**

*VML-Standardattribut*

**Beispiel**

Die Form hat eine Strichfarbe von **grün** und nicht **rot.**


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 