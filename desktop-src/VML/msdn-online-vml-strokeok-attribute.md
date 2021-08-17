---
title: VML StrokeOK-Attribut
description: VML StrokeOK-Attribut
ms.assetid: f150f87b-1ed9-4c53-bf7f-ebe1e81642fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5051f3a2d5e7ac8e4d509d8b8f65182f86799db41bbd8a4d71741961c3a1e406
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475220"
---
# <a name="vml-strokeok-attribute"></a>VML StrokeOK-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob ein Strich angezeigt wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Path](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *element* strokeok=" *ausdruck* ">

**Skriptsyntax**

*element* .strokeok="*expression*"

*expression* = *Element*.strokeok

**Anmerkungen**

False gibt an, dass der Pfad nicht strichen kann. Der Standardwert ist **True**. Dieses Attribut überschreibt alle anderen Strichattribute im übergeordneten Oder **Stroke-Element.**

*VML-Standardattribut*

**Beispiel**

Der Pfad wird nicht mit Strichen strichen.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" strokeok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 