---
title: Verborgenes VML-Attribut
description: Verborgenes VML-Attribut
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9122b3a9828fde816684cb20035949628ef25e38d06fb188d8271f0d5384f1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308280"
---
# <a name="vml-obscured-attribute"></a>Verborgenes VML-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob ein Schatten transparent ist. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *element* obscured=" *ausdruck* ">

**Skriptsyntax**

*element* .obscured="*expression*"

*expression* = *.obscured-Element*

**Anmerkungen**

**True** gibt an, dass Sie durch den Schatten sehen können, ob keine Füllung auf der Form vorhanden ist. Der Standardwert ist **False**.

*VML-Standardattribut*

**Beispiel**

Der Hintergrund wird durch den Schatten angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 