---
title: Opacity-Attribut (Stroke)(VML)
description: Opacity-Attribut (Stroke)(VML)
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f457ee73ffdccd589f5ab3b4d89c5ce4c05f871a71572c1f04b2ddef5de4a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596771"
---
# <a name="opacity-attribute-strokevml"></a>Opacity-Attribut (Stroke)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Transparenz eines Strichs. Lese-/Schreibzugriff. **VgFraction**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* opacity="-Ausdruck "> 

**Skriptsyntax**

*element* .opacity="*expression*"

*expression* = *Element*.opacity

**Anmerkungen**

Der Standardwert ist 1,0.

*VML-Standardattribut*

**Beispiel**

Der Strich ist zu 50 % transparent.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 