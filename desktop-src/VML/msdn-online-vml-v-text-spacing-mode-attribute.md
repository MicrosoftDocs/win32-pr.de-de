---
title: VML-Attribut "V-Text-Spacing-Mode"
description: VML-Attribut "V-Text-Spacing-Mode"
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42137e8c8ec401548c4e0b027a50f34813fc7b45b04c4568011617906ac8e1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057658"
---
# <a name="vml-v-text-spacing-mode-attribute"></a>VML-Attribut "V-Text-Spacing-Mode"

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Modus für Letterspacing. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* style="v-text-spacing-mode: *expression* ">

**Skriptsyntax**

*element* .style.v-text-spacing-mode="*expression*"

*expression* = *Element*.style.v-text-spacing-mode

**Anmerkungen**

Zu den Werten zählen

-   **Tightening** (Standard)
-   **Tracking**

Dieses Attribut bestimmt, ob Zwischenraum zwischen den einzelnen Buchstaben entfernt (Verkraffung) oder zwischen jedem Buchstaben (Nachverfolgung) hinzugefügt wird. Der Umfang der Änderung des Letterpacings wird durch das [V-Text-Spacing-Attribut](msdn-online-vml-v-text-spacing-attribute.md) definiert.

*VML-Standardattribut*

**Beispiel**

Die Buchstabenpashierung zwischen den einzelnen Buchstaben wird um 200 Einheiten erhöht.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 