---
title: Color2-Attribut (Fill) (VML)
description: Color2-Attribut (Fill) (VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5689bba52277b4056f57a171f3ffc1e197aa4c8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339085"
---
# <a name="color2-attribute-fillvml"></a>Color2-Attribut (Fill) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert eine zweite Farbe für Füllungen. Lese-/Schreibzugriff. [Vgcolor](msdn-online-vml-ivgcolor.md) .

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* color2 = " *Ausdruck* " >

**Skript Syntax**

*Element* . color2 = "*Ausdruck*"

*Ausdruck* = *Element*. color2

**Anmerkungen**

Eine zweite Farbe wird verwendet, wenn ein Fülltyp ein Muster oder ein Farbverlauf ist. Der Standardwert ist **weiß**.

*VML-Standard Attribut*

**Beispiel**

Der Fülltyp der Form ist ein Muster, bei dem die Vordergrundfarbe durch das Quell Bild definiert wird, der transparente Hintergrund jedoch durch die zweite Farbe definiert ist.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 