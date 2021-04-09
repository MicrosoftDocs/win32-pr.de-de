---
title: VML-Attribut "V-Text-Reverse"
description: VML-Attribut "V-Text-Reverse"
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2625439d4b7a767a21de3578a7b15d3115a8f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039295"
---
# <a name="vml-v-text-reverse-attribute"></a>VML-Attribut "V-Text-Reverse"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob die layoutreihenfolge der Zeilen umgekehrt wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* Style = "v-Text-Reverse: *Expression* " >

**Skript Syntax**

*Element* . Style. v-Text-Reverse = "*Ausdruck*"

*Ausdruck* = *Element*. Style. v-Text-Reverse

**Anmerkungen**

**True** gibt an, dass die layoutreihenfolge der Zeilen umgekehrt wird. Dieses Attribut wird für das vertikale Text Layout verwendet. Der Standardwert ist **False**.

*VML-Standard Attribut*

**Beispiel**

Die layoutreihenfolge wird umgekehrt.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 