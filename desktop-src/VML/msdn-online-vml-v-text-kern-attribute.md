---
title: VML V-Text-Kern-Attribut
description: VML V-Text-Kern-Attribut
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5ca41b66c05af673839ccbc8ba9eb95cf652eb223cd4dd3915799e91ff6c69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974630"
---
# <a name="vml-v-text-kern-attribute"></a>VML V-Text-Kern-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob Kerning aktiviert ist. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* style="v-text-kern: *expression* ">

**Skriptsyntax**

*element* .style.v-text-kern="*expression*"

*expression* = *Element*.style.v-text-kern

**Anmerkungen**

True **gibt an,** dass das Kerning aktiviert ist. Der Standardwert ist **False**. Kerning ist das Entfernen von Leerzeichen zwischen bestimmten Buchstabenpaaren, um ungleiche Buchstabenform zu kompensieren. Wenn z. B. Kerning aktiviert ist, wird zusätzlicher Platz zwischen einem groß geschriebenen "T" und einem Kleinbuchstaben "i" entfernt.

*VML-Standardattribut*

**Beispiel**

Kerning ist aktiviert.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 