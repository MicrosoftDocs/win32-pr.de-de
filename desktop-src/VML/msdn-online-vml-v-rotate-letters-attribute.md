---
title: VML-Attribut "V-Rotation-Letters"
description: VML-Attribut "V-Rotation-Letters"
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9397fe8a819e9f4c8b517e1ac92e0094ad8e4458
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101710"
---
# <a name="vml-v-rotate-letters-attribute"></a>VML-Attribut "V-Rotation-Letters"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob die Buchstaben des Texts gedreht werden. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* Style = "v-Rotation-Letters: *Expression* " >

**Skript Syntax**

*Element* . Style. v-Rotation-Letters = "*Ausdruck*"

*Ausdruck* = *Element*. Style. v-Rotation-Buchstaben

**Anmerkungen**

**True** gibt an, dass die Buchstaben des Texts um 90 Grad gedreht werden. Der Standardwert ist **False**.

*VML-Standard Attribut*

**Beispiel**

Die Buchstaben werden um 90 Grad gedreht.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 