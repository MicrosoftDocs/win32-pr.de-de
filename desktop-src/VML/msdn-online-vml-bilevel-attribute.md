---
title: VML-Attribut mit BiLevel
description: VML-Attribut mit BiLevel
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263a9d538a76ba0c9b203cbcf04f8413d4286c34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728312"
---
# <a name="vml-bilevel-attribute"></a>VML-Attribut mit BiLevel

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob ein Bild in schwarz und weiß angezeigt wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *Element* BiLevel = " *Expression* " >

**Skript Syntax**

*Element* . BiLevel = "*Ausdruck*"

*Ausdruck* = *Element*. BiLevel

**Anmerkungen**

**True** gibt an, dass das Bild mit zwei Farben (schwarz und weiß) angezeigt wird. Der Standardwert ist **False**. Dadurch wird eine ähnliche Wirkung wie bei der Nachlässigkeit erzielt.

*VML-Standard Attribut*

**Beispiel**

Das Bild wird nur in schwarz und weiß angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 