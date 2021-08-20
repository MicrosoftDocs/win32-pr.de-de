---
title: VML StrokeColor-Attribut
description: VML StrokeColor-Attribut
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a419813c5bd9db4370320f9f181477013136c70265f4ba1d8572a38ae9e3c473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124233"
---
# <a name="vml-strokecolor-attribute"></a>VML StrokeColor-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Pinselfarbe, die den Pfad einer Form stricht. Lese-/Schreibzugriff. [IVgColor](msdn-online-vml-ivgcolor.md).

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *element* strokecolor=" *ausdruck* ">

**Skriptsyntax**

*element* .strokecolor="*expression*"

*expression* = *Element*.strokecolor

**Anmerkungen**

Der Wert wird aus dem **Color-Attribut** des [Stroke-Elements](msdn-online-vml-stroke-element.md) dupliziert.

*VML-Standardattribut*

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



[StrokeColor-Attribut – Beispiel.](/previous-versions/bb264093(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 