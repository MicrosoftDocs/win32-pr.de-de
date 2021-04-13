---
title: VML-Attribut "startarrowlength"
description: VML-Attribut "startarrowlength"
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a57e10c9cf7b9a8683f4b1856355232afc16be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390586"
---
# <a name="vml-startarrowlength-attribute"></a>VML-Attribut "startarrowlength"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Pfeilspitzen Länge für den Anfang einer Zeile. Lese-/Schreibzugriff. **Vgarrowheadlength**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* startarrowlength = " *Ausdruck* " >

**Skript Syntax**

*Element* . startarrowlength = "*Ausdruck*"

*Ausdruck* = *Element*. startarrowlength

**Anmerkungen**

Mögliche Werte:

-   Short
-   Mittel (Standard)
-   Long

VML-Standard Attribut

**Beispiel**

Eine Linie wird mit einer kurzen klassischen Pfeilspitze am Anfang des Strichs gezeichnet.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 