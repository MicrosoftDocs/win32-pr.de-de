---
title: VML V-Text-align-Attribut
description: VML V-Text-align-Attribut
ms.assetid: ca2cbbf6-ddbb-4f2b-942c-3fe0033bd649
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6efb96bde980a4831f400ada7032f9ee37f1d976
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948860"
---
# <a name="vml-v-text-align-attribute"></a>VML V-Text-align-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Textausrichtung. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* Style = "v-Text-align: *Expression* " >

**Skript Syntax**

*Element* . Style. v-Text-align = "*Ausdruck*"

*Ausdruck* = *Element*. Style. v-Text-align

**Anmerkungen**

Mögliche Werte:

-   **left** (Standard)
-   **Richting**
-   **Tagesstätte**
-   **fertigte**
-   **Brief: rechtfertigen**
-   **Stretch-rechtfertigen**

*VML-Standard Attribut*

**Beispiel**

Der Text wird so gestreckt, dass er dem Pfad entspricht, aber der zusätzliche Leerraum wird zwischen den einzelnen Buchstaben eingefügt.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-align:letter-justify;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 