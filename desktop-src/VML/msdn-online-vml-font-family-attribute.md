---
title: VML-Font-Family Attribut
description: VML-Font-Family Attribut
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29aa72775e8f00e195462cf3df06097d267b908
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039584"
---
# <a name="vml-font-family-attribute"></a>VML-Font-Family Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Familie der TextPath-Schriftart. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* Style = "Font-Family: *Expression* " >

**Skript Syntax**

*Element* . Style. FontFamily = "*Ausdruck*"

*Ausdruck* = *Element*. Style. FontFamily

**Anmerkungen**

Definiert den Schriftart Namen. Bestimmte Namen wie z. b. Arial können verwendet werden oder generische Typen wie Serif, Sans-Serif, currsive, Fantasy oder Monospace. Die Werte sind identisch mit den standardmäßigen HTML-Format Attributen.

*VML-Standard Attribut*

**Beispiel**

Die Schriftfamilie des Texts ist Arial.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 