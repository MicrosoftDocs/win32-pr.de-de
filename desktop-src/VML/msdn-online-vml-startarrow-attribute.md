---
title: VML-Attribut "startarrow"
description: VML-Attribut "startarrow"
ms.assetid: 484dfcdb-f68d-40f9-9a83-18abb054d1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2c17569750c1e655a5538ca5bf233e49f827e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948918"
---
# <a name="vml-startarrow-attribute"></a>VML-Attribut "startarrow"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Pfeilspitze für den Anfang einer Linie. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* startarrow = " *Expression* " >

**Skript Syntax**

*Element* . startarrow = "*Ausdruck*"

*Ausdruck* = *Element*. startarrow

**Anmerkungen**

Mögliche Werte:

-   Keine (Standard)
-   Blockieren
-   Klassisch
-   Diamond
-   Oval
-   Öffnen

VML-Standard Attribut

**Beispiel**

Eine Linie wird mit einer klassischen Pfeilspitze am Anfang des Strichs gezeichnet.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke StartArrow="classic"/>
   </v:line>
```



 

 