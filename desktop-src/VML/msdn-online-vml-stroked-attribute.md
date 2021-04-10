---
title: In VML gestreichelt Attribut
description: In VML gestreichelt Attribut
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9578027f305f9c720b42ae50befe8abd7e18a949
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102274"
---
# <a name="vml-stroked-attribute"></a>In VML gestreichelt Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert, ob der Pfad gestreichelt wird. Lese-/Schreibzugriff. [Vgder State](msdn-online-vml-vgtristate.md) .

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* gestreichelt = " *Ausdruck* " >

**Skript Syntax**

*Element* . stroked = "*Ausdruck*"

*Ausdruck* = *Element*. stroked

**Anmerkungen**

Der Wert wird aus dem **on** -Attribut des [Stroke](msdn-online-vml-stroke-element.md) -Elements dupliziert.

*VML-Standard Attribut*

**Beispiel**

Der Shape-Pfad ist gestreichelt.


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Beispiel](/previous-versions/bb264094(v=vs.85))für einen Strich mit Strichen. (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 