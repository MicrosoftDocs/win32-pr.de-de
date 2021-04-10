---
title: VML-Attribut "startarrowwidth"
description: VML-Attribut "startarrowwidth"
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ba4f5adddc328d1791fa2beb570f59da826f83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728537"
---
# <a name="vml-startarrowwidth-attribute"></a>VML-Attribut "startarrowwidth"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Pfeilspitzen Breite für den Anfang einer Linie. Lese-/Schreibzugriff. **Vgarrowheadwidth**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* startarrowwidth = " *Expression* " >

**Skript Syntax**

*Element* . startarrowwidth = "*Ausdruck*"

*Ausdruck* = *Element*. startarrowwidth

**Anmerkungen**

Mögliche Werte:

-   Verringern
-   Mittel (Standard)
-   Breite

VML-Standard Attribut

**Beispiel**

Eine Linie wird mit einer breiten klassischen Pfeilspitze am Anfang des Strichs gezeichnet.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 