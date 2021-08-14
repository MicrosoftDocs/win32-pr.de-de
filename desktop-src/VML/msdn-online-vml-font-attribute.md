---
title: VML-Schriftartattribut
description: VML-Schriftartattribut
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 074aa0672002dcbbac55d21ed27383d5a3fd6e3b9ccfe9125ad89c2c43ac71ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986660"
---
# <a name="vml-font-attribute"></a>VML-Schriftartattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt einen Verbundwert von Schriftartattributen an. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* style="font: *expression* ">

**Skriptsyntax**

*element* .style.font="*expression*"

*expression* = *Element*.style.font

**Anmerkungen**

Definiert die Attribute einer Schriftart, einschließlich Familie, Stil, Gewichtung, Größe und Variante. Die Reihenfolge der Definitionen in der Zeichenfolge ist: **font-style**, **font-variant**, **font-weight**, **font-size**, **line-height** und **font-family**. Die Werte sind identisch mit den Standardattributen im HTML-Format.

*VML-Standardattribut*

**Beispiel**

Die Schriftart des Textpfadtexts ist italisch, klein, fett, arial mit 36 Punkt.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 