---
title: Origin Attribute (Fill)(VML)
description: Origin Attribute (Fill)(VML)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc33ae1f4cf7c588ae9b3f40ff8c445be88192bae1dfc86a3593eea931befb25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959220"
---
# <a name="origin-attribute-fillvml"></a>Origin Attribute (Fill)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Mitte eines Füllbilds. Lese-/Schreibzugriff. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *element* origin=" *ausdruck* ">

**Skriptsyntax**

*element* .origin="*expression*"

*expression* = *Element*.origin

**Anmerkungen**

Gibt einen Punkt relativ zur oberen linken Ecke des Bilds an. dieser Punkt wird als Ursprung des Bilds behandelt. Der Standardwert ist die Mitte des Bilds. Der Vektor ist ein Bruchteil der Breite und Höhe des Bilds.

*VML-Standardattribut*

**Beispiel**

Das Bild der Füllung wird nach links zu einem Punkt 50 % der Breite der Form verschoben.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 