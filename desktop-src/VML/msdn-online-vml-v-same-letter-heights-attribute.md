---
title: VML-Attribut "V-gleich-Letter-Heights"
description: VML-Attribut "V-gleich-Letter-Heights"
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d155c3c72eb67718edd33ae601d22f8e5d074a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727761"
---
# <a name="vml-v-same-letter-heights-attribute"></a>VML-Attribut "V-gleich-Letter-Heights"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob alle Buchstaben unabhängig vom ursprünglichen Fall dieselbe Höhe aufweisen. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* Style = "v-same-Letter-Heights: *Expression* " >

**Skript Syntax**

*Element* . Style. v-same-Letter-Höhen = "*Ausdruck*"

*Ausdruck* = *Element*. Style. v-Höhe-Letter-Höhen

**Anmerkungen**

**True** gibt an, dass die Kleinbuchstaben auf die Höhe der Großbuchstaben gestreckt werden. Der Standardwert ist **False**.

*VML-Standard Attribut*

**Beispiel**

Alle Buchstaben haben unabhängig von der Groß-/Kleinschreibung dieselbe Höhe.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 