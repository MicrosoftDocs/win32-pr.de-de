---
title: VML-XScale-Attribut
description: VML-XScale-Attribut
ms.assetid: b876201d-87d1-4795-8f7f-33712a8bf493
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3221ab44cad9eb9f422ce451f618eb8eeba55bcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315303"
---
# <a name="vml-xscale-attribute"></a>VML-XScale-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob anstelle des Shape-Pfads ein geradliniger Textpfad verwendet wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* Style = "XScale: *Expression* " >

**Skript Syntax**

*Element* . Style. XScale = "*Ausdruck*"

*Ausdruck* = *Element*. Style. XScale

**Anmerkungen**

Wenn der Wert **true** ist, wird der Text entlang von links nach rechts entlang des x-Werts der unteren Grenze der Form ausgeführt. Der Standardwert ist **False**.

*VML-Standard Attribut*

**Beispiel**

Der Text wird so angezeigt, als ob er in einer horizontalen Linie gezeichnet würde, auch wenn der Shape-Pfad diagonal ist.


```HTML
   <v:line from="100 100" to="400 400">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="xscale:true;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 