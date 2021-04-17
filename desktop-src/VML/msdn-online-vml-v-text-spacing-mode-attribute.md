---
title: VML V-Text-Spacing-Mode-Attribut
description: VML V-Text-Spacing-Mode-Attribut
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a288f89a1405412ba8c582a5c52c7bfe56809c38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474172"
---
# <a name="vml-v-text-spacing-mode-attribute"></a>VML V-Text-Spacing-Mode-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Modus für Brief Abstände. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* Style = "v-Text-Spacing-Mode: *Expression* " >

**Skript Syntax**

*Element* . Style. v-Text-Spacing-Mode = "*Ausdruck*"

*Ausdruck* = *Element*. Style. v-Text-Abstände-Modus

**Anmerkungen**

Zu den Werten zählen

-   wird **verschärft** (Standard)
-   **Paletten**

Mit diesem Attribut wird festgelegt, ob zwischen den einzelnen Buchstaben (das Ende) oder zwischen den einzelnen Buchstaben (Nachverfolgung) ein Leerzeichen entfernt wird Die Menge der Änderungen im Buchstaben Abstand wird durch das [V-Text-Spacing-](msdn-online-vml-v-text-spacing-attribute.md) Attribut definiert.

*VML-Standard Attribut*

**Beispiel**

Der Brief Abstand zwischen den einzelnen Buchstaben wird um 200 Einheiten angehoben.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 