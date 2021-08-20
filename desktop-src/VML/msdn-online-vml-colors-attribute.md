---
title: VML-Farbattribut
description: VML-Farbattribut
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a699b0ab8da898dd82fa4e1bf4823c0f9fdd443eb8275e25dbfaac6d2f039a6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999280"
---
# <a name="vml-colors-attribute"></a>VML-Farbattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert mehrere Farben für eine Farbverlaufsfüllung. Lese-/Schreibzugriff. **IVgGradientColorArray**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *element* colors=" *ausdruck* ">

**Skriptsyntax**

*element* .colors="*expression*"

*expression* = *Element*.colors

**Anmerkungen**

Wird verwendet, um ein Array zu definieren, das aus paarweise Werten von Prozentsätzen ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) und Farbe ([VgColor](msdn-online-vml-ivgcolor.md)) besteht. Das Array erstellt mithilfe jedes Punkts im Array eine gemischte Füllung, beginnend bei 0 % (definiert durch **Color)** und endet bei 100 % (definiert durch **Color2).** Zwischenfarben entlang des Wegs können definiert werden, indem einem Prozentsatz ein Farbwert zugewiesen wird. Das Prozent- und Das Farbpaar werden nicht durch ein Komma getrennt, sondern durch Kommas voneinander getrennt.

VML-Standardattribut

**Beispiel**

Die Form verfügt über eine Farbverlaufsfüllung, die aus vier Farben besteht, beginnend mit Rot, überblenden zu Gelb, dann grün und schließlich blau.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 