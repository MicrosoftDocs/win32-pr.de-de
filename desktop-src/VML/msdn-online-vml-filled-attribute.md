---
title: Ausgefülltes VML-Attribut
description: Ausgefülltes VML-Attribut
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 232d8b36b6d272c3a1ee8c17f3ddeca023ab4708
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474188"
---
# <a name="vml-filled-attribute"></a>Ausgefülltes VML-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob der geschlossene Pfad ausgefüllt wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* ausgefüllt = " *Ausdruck* " >

**Skript Syntax**

*Element* . Fill = "*Ausdruck*"

*Ausdruck* = *Element*. ausgefüllt

**Anmerkungen**

Der Wert wird aus dem **on** -Attribut des [Fill](msdn-online-vml-fill-element.md) -Elements dupliziert.

*VML-Standard Attribut*

**Beispiel**

Der Shape-Pfad ist ausgefüllt.


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Beispiel für ausgefülltes Attribut](/previous-versions/bb229669(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 