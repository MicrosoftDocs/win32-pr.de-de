---
title: VML-Attribut "verdeckt"
description: VML-Attribut "verdeckt"
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e383061d3210c9c52dc8c89322bd617257555e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039194"
---
# <a name="vml-obscured-attribute"></a>VML-Attribut "verdeckt"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob ein Schatten transparent ist. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *Element* verdeckt = " *Ausdruck* " >

**Skript Syntax**

*Element* . verdeckt = "*Ausdruck*"

*Ausdruck* = *Element*. verdeckt

**Anmerkungen**

Wenn der Wert **true** ist, wird der Schatten angezeigt, wenn die Form nicht ausgefüllt ist. Der Standardwert ist **False**.

*VML-Standard Attribut*

**Beispiel**

Der Hintergrund wird durch den Schatten angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 