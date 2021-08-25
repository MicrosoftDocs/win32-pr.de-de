---
title: Origin Attribute (Shadow)(VML)
description: Origin Attribute (Shadow)(VML)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1776b0d8a857a3247543eae13d280d023585229d27c04a576420003ea53920
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959180"
---
# <a name="origin-attribute-shadowvml"></a>Origin Attribute (Shadow)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Mitte des Schattens. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *element* origin=" *ausdruck* ">

**Skriptsyntax**

*element* .origin="*expression*"

*expression* = *Element*.origin

**Anmerkungen**

Ein Paar von Bruchwerten der Form im Bereich von 50 % bis -50 %. Der Standardwert ist 0,0.

*VML-Standardattribut*

**Beispiel**

Der Schatten weist einen Ursprung auf, der 20 % nach unten und 20 % rechts neben dem Ursprung der Form liegt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 