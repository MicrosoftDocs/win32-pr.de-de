---
title: VML-Trim-Attribut
description: VML-Trim-Attribut
ms.assetid: c8038361-00bd-4787-9759-506a8a47b19a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05f7463465c10abb4f4f01267a7ebeac878cbf36c41f1effde6ec218bad1088
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974611"
---
# <a name="vml-trim-attribute"></a>VML-Trim-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob oberhalb und unterhalb des Texts zusätzlicher Platz entfernt wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* style="trim: *expression* ">

**Skriptsyntax**

*element* .style.trim="*expression*"

*expression* = *Element*.style.trim

**Anmerkungen**

True **gibt an,** dass für aufsteigende und absteigende Daten reservierter Speicherplatz entfernt wird. Der Standardwert ist **False**.

*VML-Standardattribut*

**Beispiel**

Der zusätzliche Platz über und darunter wird gekürzt.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="trim:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 