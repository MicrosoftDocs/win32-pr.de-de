---
title: VML-V-Text-Reverse-Attribut
description: VML-V-Text-Reverse-Attribut
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f1535620c1fefe98ac23e2f842ef9a97e13b9cb39c65ec6b97f6f7d12b1998
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654620"
---
# <a name="vml-v-text-reverse-attribute"></a>VML-V-Text-Reverse-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob die Layoutreihenfolge von Zeilen umgekehrt wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* style="v-text-reverse: *expression* ">

**Skriptsyntax**

*element* .style.v-text-reverse="*expression*"

*expression* = *Element*.style.v-text-reverse

**Anmerkungen**

**True** gibt an, dass die Layoutreihenfolge der Zeilen umgekehrt wird. Dieses Attribut wird für das vertikale Textlayout verwendet. Der Standardwert ist **False**.

*VML-Standardattribut*

**Beispiel**

Die Layoutreihenfolge wird umgekehrt.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 