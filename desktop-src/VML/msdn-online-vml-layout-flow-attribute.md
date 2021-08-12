---
title: VML-Layout-Flow-Attribut
description: VML-Layout-Flow-Attribut
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde6937a3f93ff2a462cfc5950c13b7f3910573c54d82449ef705bca4afbb068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599354"
---
# <a name="vml-layout-flow-attribute"></a>VML-Layout-Flow-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt den Fluss des Textlayouts in einem Textfeld. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[TextBox](msdn-online-vml-textbox-element.md)

**Tagsyntax**

<v: *element* style="layout-flow: *ausdruck* ">

**Anmerkungen**

Mögliche Werte:



| Wert                  | BESCHREIBUNG                                 |
|------------------------|---------------------------------------------|
| Horizontal             | Text wird horizontal angezeigt. Standard.    |
| Vertikale               | Text wird vertikal angezeigt.               |
| vertikal-ideografische Darstellung   | Ideografischer Text wird vertikal angezeigt.   |
| horizontal-ideographic | Ideografischer Text wird horizontal angezeigt. |



 

*VML-Standardattribut*

**Beispiel**

Der Textfluss im Textfeld wird vertikal fließen.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 