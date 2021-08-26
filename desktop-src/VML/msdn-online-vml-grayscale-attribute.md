---
title: VML GrayScale-Attribut
description: VML GrayScale-Attribut
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683371e2441ffa93f96dc8f727e4eed293954b1897267db8848aa39ffa497af8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099210"
---
# <a name="vml-grayscale-attribute"></a>VML GrayScale-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob ein Bild im Graustufenmodus angezeigt wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *element* grayscale=" *ausdruck* ">

**Skriptsyntax**

*element* .grayscale="*expression*"

*expression* = *.grayscale-Element*

**Anmerkungen**

**True** gibt an, dass das Bild in Graustufen statt in Farbe angezeigt wird. Der Standardwert ist **False**.

Der Wert basiert auf der CCIR-Empfehlung 709, die ein größeres grünes Gewicht bevorzugt und mehr ansprechende Ergebnisse für natürliche Farbe erzeugt.

*VML-Standardattribut*

**Beispiel**

Das Bild wird in Graustufen statt in Farbe angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 