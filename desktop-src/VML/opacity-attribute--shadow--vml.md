---
title: Opacity-Attribut (Schatten)(VML)
description: Opacity-Attribut (Schatten)(VML)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43287a4bb6de9f2dd0d9d2b0af97d971314ab7e93ab2c4fae58b666ee1a94124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680620"
---
# <a name="opacity-attribute-shadowvml"></a>Opacity-Attribut (Schatten)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt die Transparenz eines Schattens. Lese-/Schreibzugriff. [VgFraction](msdn-online-vml-vgfraction-data-type.md) .

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *element* opacity=" *ausdruck* ">

**Skriptsyntax**

*element* .opacity="*expression*"

*expression* = *Element*.opacity

**Anmerkungen**

Der Standardwert ist 1. Der Wert 0 macht einen vollständig transparenten Schatten.

*VML-Standardattribut*

**Beispiel**

Die Form hat einen Schatten, der zu 50 % transparent ist.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 