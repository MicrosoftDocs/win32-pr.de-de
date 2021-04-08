---
title: VML-Attribut "tdarrowwidth"
description: VML-Attribut "tdarrowwidth"
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108d65fc1a06ace3d318d54a6416e0d98c0a4652
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730153"
---
# <a name="vml-endarrowwidth-attribute"></a>VML-Attribut "tdarrowwidth"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert eine Pfeilspitzen Breite für das Ende einer Linie. Lese-/Schreibzugriff. **Vgarrowheadwidth**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* endarrowwidth = " *Ausdruck* " >

**Skript Syntax**

*Element* . endarrowwidth = "*Ausdruck*"

*Ausdruck* = *Element*. endarrowwidth

**Anmerkungen**

Mögliche Werte:

-   Verringern
-   Mittel (Standard)
-   Breite

*VML-Standard Attribut*

**Beispiel**

Eine Linie wird mit einer breiten klassischen Pfeilspitze am Ende des Strichs gezeichnet.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 