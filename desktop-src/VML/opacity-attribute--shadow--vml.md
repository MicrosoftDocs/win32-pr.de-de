---
title: Opacity-Attribut (Schatten) (VML)
description: Opacity-Attribut (Schatten) (VML)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d09ca038a187c4a4ed1f914f5d05bcfd63e4a4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390449"
---
# <a name="opacity-attribute-shadowvml"></a>Opacity-Attribut (Schatten) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt die Transparenz eines Schattens. Lese-/Schreibzugriff. [Vgbruchteile](msdn-online-vml-vgfraction-data-type.md) .

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *Element* Deckkraft = " *Ausdruck* " >

**Skript Syntax**

*Element* . Opacity = "*Ausdruck*"

*Ausdruck* = *Element*. Deckkraft

**Anmerkungen**

Der Standardwert ist 1. Der Wert 0 (null) führt zu einem vollständig transparenten Schatten.

*VML-Standard Attribut*

**Beispiel**

Die Form hat einen Schatten, der 50% transparent ist.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 