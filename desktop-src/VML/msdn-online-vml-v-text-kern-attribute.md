---
title: VML-V-Text-Kern-Attribut
description: VML-V-Text-Kern-Attribut
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b20eab11cc24cd7580b68de8acf86468fb1d16a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948950"
---
# <a name="vml-v-text-kern-attribute"></a>VML-V-Text-Kern-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob die kernung aktiviert ist. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* Style = "v-Text-Kern: *Expression* " >

**Skript Syntax**

*Element* . Style. v-Text-Kern = "*Ausdruck*"

*Ausdruck* = *Element*. Style. v-Text-Kern

**Anmerkungen**

**True** gibt an, dass die kernung aktiviert ist. Der Standardwert ist **False**. Die kernung ist das Entfernen von Leerzeichen zwischen bestimmten Brief Paaren, um ungleichmäßige letterforms auszugleichen. Wenn z. b. die kerif-Aktivierung aktiviert ist, wird zusätzlicher Speicherplatz zwischen dem Großbuchstaben "T" und dem Kleinbuchstaben "i" entfernt.

*VML-Standard Attribut*

**Beispiel**

Die kernung ist aktiviert.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 