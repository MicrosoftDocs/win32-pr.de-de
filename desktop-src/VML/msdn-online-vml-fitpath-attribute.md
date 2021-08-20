---
title: VML-FitPath-Attribut
description: VML-FitPath-Attribut
ms.assetid: f15775ed-f7b7-45d9-83ed-e307daf7451b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8863fb4d8a382ac9ccddaf7cc55fe5e8ceeff221dc1f816e340fa0a78cf9d7b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124783"
---
# <a name="vml-fitpath-attribute"></a>VML-FitPath-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert, ob der Text in den Pfad einer Form passt. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* fitpath=" *ausdruck* ">

**Skriptsyntax**

*element* .fitpath="*expression*"

*expression* = *Element*.fitpath

**Anmerkungen**

True **gibt an,** dass der Text so groß ist, dass er den Pfad ausfüllt, auf dem er sich befindet. Der Standardwert ist **False**.

*VML-Standardattribut*

**Beispiel**

Der Text passt zum Pfad.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitpath="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 