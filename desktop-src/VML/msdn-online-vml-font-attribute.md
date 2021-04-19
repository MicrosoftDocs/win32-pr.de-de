---
title: VML-Schriftart Attribut
description: VML-Schriftart Attribut
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bace73b90cac7519ea6abacb73c80506c655e133
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342158"
---
# <a name="vml-font-attribute"></a>VML-Schriftart Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt einen zusammengesetzten Wert für Schriftart Attribute an. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* Style = "Font: *Expression* " >

**Skript Syntax**

*Element* . Style. Font = "*Ausdruck*"

*Ausdruck* = *Element*. Style. Font

**Anmerkungen**

Definiert die Attribute einer Schriftart, einschließlich Familie, Stil, Gewichtung, Größe und Variant. Die Reihenfolge der Definitionen in der Zeichenfolge lautet: **Schriftart**, **Schriftart, Schriftart, Schrift** **Grad,** Schrift **Grad,** **Zeilenhöhe** und **Schriftfamilie**. Die Werte sind identisch mit den standardmäßigen HTML-Format Attributen.

*VML-Standard Attribut*

**Beispiel**

Die Schriftart des TextPath-Texts ist kursiv, Small-Caps, Bold, 36 Punkt Arial.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 