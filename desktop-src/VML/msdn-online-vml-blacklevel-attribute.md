---
title: VML-Attribut "Blacklevel"
description: VML-Attribut "Blacklevel"
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5394f8b218f2eb577aa63ead5ae940fe2a49029f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039201"
---
# <a name="vml-blacklevel-attribute"></a>VML-Attribut "Blacklevel"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Intensität von schwarz in einem Bild. Lese-/Schreibzugriff. **Vgnumber**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *Element* Blacklevel = " *Expression* " >

**Skript Syntax**

*Element* . Blacklevel = "*Ausdruck*"

*Ausdruck* = *Element*. Blacklevel

**Anmerkungen**

Ermöglicht das Ändern der Farb Ebene, sodass schwarze als echte schwarze angezeigt werden und alle anderen Farben als Schattierungen über schwarz sichtbar sind. Der Standardwert ist 0. Obwohl eine beliebige Zahl zwischen positivem und negativem unendlich zulässig ist, werden Werte kleiner als-0,5 als "alle schwarz" angezeigt, und Werte größer als 0,5 werden als "weiß" angezeigt.

*VML-Standard Attribut*

**Beispiel**

Das Bild wird mit sehr dunklen Tönen angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 