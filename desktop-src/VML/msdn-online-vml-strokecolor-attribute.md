---
title: VML-Attribut "strokeColor"
description: VML-Attribut "strokeColor"
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d379f41f3d2c1f03349beae8d0420a7c1a26429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039150"
---
# <a name="vml-strokecolor-attribute"></a>VML-Attribut "strokeColor"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Pinsel Farbe, mit der der Pfad einer Form festgelegt wird. Lese-/Schreibzugriff. [Ivgcolor](msdn-online-vml-ivgcolor.md).

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* strokeColor = " *Expression* " >

**Skript Syntax**

*Element* . strokeColor = "*Ausdruck*"

*Ausdruck* = *Element*. strokeColor

**Anmerkungen**

Der Wert wird aus dem **Color** -Attribut des [Stroke](msdn-online-vml-stroke-element.md) -Elements dupliziert.

*VML-Standard Attribut*

**Beispiel**

Die Farbe des Strichs des Rechtecks ist rot.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Beispiel für ein strokeColor-Attribut](/previous-versions/bb264093(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 