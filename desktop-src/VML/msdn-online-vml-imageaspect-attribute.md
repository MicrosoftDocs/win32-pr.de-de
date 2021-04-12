---
title: VML imageaspect-Attribut
description: VML imageaspect-Attribut
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b873f7577907acb6d8f88f0290117651077b3c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315615"
---
# <a name="vml-imageaspect-attribute"></a>VML imageaspect-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert, wie das Seitenverhältnis des Strich Bilds beibehalten wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v:

Element *imageaspect = "* Expression *" #b0*

**Skript Syntax**

Element *. imageaspect = "* Ausdruck *"*

Expression- *=* Element *. imageaspect*

**Anmerkungen**

Mögliche Werte:



| Wert   | BESCHREIBUNG                                |
|---------|--------------------------------------------|
| Ignorieren  | Ignoriert Aspekte von Aspekten.                      |
| Mindestens | Image ist mindestens so groß wie **ImageSize**. |
| Höchstens  | Image ist nicht größer als **ImageSize**.     |



 

In jedem Fall wird das **ImageSize** -Attribut angepasst, um den Aspekt des Bilds zu erhalten.

*VML-Standard Attribut*

**Beispiel**

Das Strich Bild ist mindestens so groß wie die Bildgröße.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 