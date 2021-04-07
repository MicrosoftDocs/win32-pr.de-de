---
title: VML-aspektattribut
description: VML-aspektattribut
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f7cf666e9bb8d4bf3cfe0e47190a8127415ac1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728336"
---
# <a name="vml-aspect-attribute"></a>VML-aspektattribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt an, wie das Seitenverhältnis des Füll Bilds beibehalten wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* Aspekt = " *Ausdruck* " >

**Skript Syntax**

*Element* . Aspect = "*Ausdruck*"

*Ausdruck* = *Element*. Aspekt

**Anmerkungen**

Mögliche Werte:



| Wert   | BESCHREIBUNG                           |
|---------|---------------------------------------|
| ignore  | Ignoriert Aspekte von Aspekten. Standard.        |
| mindestens | Image ist mindestens so groß wie die **Größe**. |
| höchstens  | Das Bild ist nicht größer als die **Größe**.     |



 

*VML-Standard Attribut*

**Beispiel**

Das Bild, das die Füllung bildet, ist größer als oder gleich einer Größe von 10 Punkten um 10 Punkte.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 