---
title: VML FitShape-Attribut
description: VML FitShape-Attribut
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0adbb6fd92f296156cf2f95cf2b714cfacd2f193f8e1e1b912e6637b9e8d5cd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099250"
---
# <a name="vml-fitshape-attribute"></a>VML FitShape-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert, ob der Text in das umgebende Feld einer Form passt. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* fitshape=" *ausdruck* ">

**Skriptsyntax**

*element* .fitshape="*expression*"

*expression* = *Element*.fitshape

**Anmerkungen**

**True** gibt an, dass der Text an die Ränder des Felds gestreckt wird, das die gesamte Form definiert. Der Standardwert ist **False**.

*VML-Standardattribut*

**Beispiel**

Der Text wird gestreckt, um die Form anzupassen.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 