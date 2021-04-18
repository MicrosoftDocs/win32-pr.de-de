---
title: VML-Farben (Attribut)
description: VML-Farben (Attribut)
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c5df5b2dc97c19441d6abaf6cd6c03d949c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516964"
---
# <a name="vml-colors-attribute"></a>VML-Farben (Attribut)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert mehrere Farben für eine Farbverlaufsfüllung. Lese-/Schreibzugriff. **Ivggradientcolorarray**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* Farben = " *Ausdruck* " >

**Skript Syntax**

*Element* . Colors = "*Ausdruck*"

*Ausdruck* = *Element*. Colors

**Anmerkungen**

Wird verwendet, um ein Array zu definieren, das aus paarweise zugeordneten Werten von Prozentsätzen ([vgbruch](msdn-online-vml-vgfraction-data-type.md)) und Color ([vgcolor](msdn-online-vml-ivgcolor.md)) besteht. Das Array erstellt eine gemischte Füllung mithilfe der einzelnen Punkte im Array, beginnend bei 0% (durch **Farbe** definiert) und endet bei 100% (durch **color2** definiert). Zwischen Farben können definiert werden, indem ein Farbwert einem Prozentsatz zugewiesen wird. Das Prozent-und Farbpaar ist nicht durch ein Komma getrennt, aber Paare werden durch Kommas voneinander getrennt.

VML-Standard Attribut

**Beispiel**

Die Form hat eine Farbverlaufsfüllung, die aus vier Farben besteht, beginnend mit rot, mit gelb, dann grün und finallyblue.


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



 

 