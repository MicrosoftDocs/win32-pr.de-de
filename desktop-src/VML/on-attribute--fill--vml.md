---
title: On-Attribut (Fill) (VML)
description: On-Attribut (Fill) (VML)
ms.assetid: 9b7d42e5-4fd9-402d-8d1f-af01f6577475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e25e805be23b4678b1be828b711365a8624f10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339512"
---
# <a name="on-attribute-fillvml"></a>On-Attribut (Fill) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob die Füllung angezeigt wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* on = " *Expression* " >

**Skript Syntax**

*Element* . on = "*Ausdruck*"

*Ausdruck* = *Element*. on

**Anmerkungen**

Wenn der Wert **false** ist, wird die Füllung nicht angezeigt. Der Standardwert ist **True**.

*VML-Standard Attribut*

**Beispiel**

Obwohl die Füllung als rot definiert ist, wird Sie nicht angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" on="False"/>
   </v:shape>
```



 

 