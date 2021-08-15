---
title: VML Gain-Attribut
description: VML Gain-Attribut
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7b72f1588608f4988731111583e758b0207080eb3e02768a45b58c39071b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057828"
---
# <a name="vml-gain-attribute"></a>VML Gain-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Intensität aller Farben in einem Bild. Lese-/Schreibzugriff. **VgNumber**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *element* gain=" *ausdruck* ">

**Skriptsyntax**

*element* .gain="*expression*"

*expression* = *.gain-Element*

**Anmerkungen**

Dieses Attribut definiert, wie hell die Farbe Weiß ist, was sich auf alle anderen Farben auswirkt. Werte liegen zwischen 0 und unendlich. Der Standardwert ist 1,0. Der Wert 0 zeigt kein Bild an. Werte größer als 1 erleichtern das Bild, und Werte kleiner als 1 machen das Bild grauer.

Dieses Attribut kann verwendet werden, um interessante Effekte zu erzeugen.

*VML-Standardattribut*

**Beispiel**

Das Bild wird mit allen Farben angezeigt, die in Richtung Grau tendieren.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 