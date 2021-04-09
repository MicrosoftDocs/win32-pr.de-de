---
title: VML-Layout-Flow Attribut
description: VML-Layout-Flow Attribut
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e437e31043afcf7fba4967076a861c9bca86477
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948903"
---
# <a name="vml-layout-flow-attribute"></a>VML-Layout-Flow Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt den Fluss des Textlayouts in einem Textfeld. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[TextBox](msdn-online-vml-textbox-element.md)

**Tagsyntax**

<v: *Element* Style = "Layout-Flow: *Ausdruck* " >

**Anmerkungen**

Mögliche Werte:



| Wert                  | BESCHREIBUNG                                 |
|------------------------|---------------------------------------------|
| Horizontal             | Der Text wird horizontal angezeigt. Standard.    |
| Rechtes               | Der Text wird vertikal angezeigt.               |
| vertikal-ideografisch   | Ideografischer Text wird vertikal angezeigt.   |
| horizontal-ideografisch | Ideografischer Text wird horizontal angezeigt. |



 

*VML-Standard Attribut*

**Beispiel**

Der Text Fluss im Textfeld wird vertikal weitergeleitet.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 