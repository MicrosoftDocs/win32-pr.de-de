---
title: VML-Font-Variant Attribut
description: VML-Font-Variant Attribut
ms.assetid: f58bf3e0-e285-474c-83b1-203fce4f3c3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 243f8b36d36d8bb9b210a916cef239cda6061e0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390384"
---
# <a name="vml-font-variant-attribute"></a>VML-Font-Variant Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Variant-Stil einer Schriftart. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* Style = "Font-Variant: *Expression* " >

**Skript Syntax**

*Element* . Style. fontVariant = "*Ausdruck*"

*Ausdruck* = *Element*. Style. fontVariant

**Anmerkungen**

Die Werte sind:

-   Normal (Standard)
-   kleine Obergrenzen

Die Werte sind identisch mit den standardmäßigen HTML-Format Attributen.

*VML-Standard Attribut*

**Beispiel**

Die Schriftart wird als kleine Großbuchstaben gerendert.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal small-caps normal 36pt Arial"/>
   </v:line>
```



 

 