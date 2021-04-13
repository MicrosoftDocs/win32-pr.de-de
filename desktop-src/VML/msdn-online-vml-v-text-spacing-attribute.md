---
title: VML-Attribut "V-Text-Spacing"
description: VML-Attribut "V-Text-Spacing"
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390667"
---
# <a name="vml-v-text-spacing-attribute"></a>VML-Attribut "V-Text-Spacing"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Größe des Abstands für Text. Lese-/Schreibzugriff. **Vgnumber**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* Style = "v-Text-Spacing: *Expression* " >

**Skript Syntax**

*Element* . Style. v-Text-Spacing = "*Ausdruck*"

*Ausdruck* = *Element*. Style. v-Text-Abstand

**Anmerkungen**

Der Standardwert ist 100. Weitere Informationen zum Text Abstand finden Sie im [V-Text-Spacing-Mode-](msdn-online-vml-v-text-spacing-mode-attribute.md) Attribut.

*VML-Standard Attribut*

**Beispiel**

Der Brief Abstand zwischen den einzelnen Buchstaben wird um 200 Einheiten gestrafft.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 