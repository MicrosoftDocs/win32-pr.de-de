---
title: VML Offset2-Attribut
description: VML Offset2-Attribut
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b5253e1a27ce8292ee5fc4ce49259db9512a5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517051"
---
# <a name="vml-offset2-attribute"></a>VML Offset2-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt einen zweiten Offset. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *Element* offset2 = " *Ausdruck* " >

**Skript Syntax**

*Element* . offset2 = "*Ausdruck*"

*Ausdruck* = *Element*. offset2

**Anmerkungen**

Der Standardwert für einen zweiten Offset für den x-Wert ist 0, und der Standardwert für den y-Wert ist 0. Werte sind entweder eine absolute Messung oder ein Bruchteil der Form. Bei einem Bruchteil liegen die Werte zwischen 50% und-50%.

Verwenden Sie einen zweiten Offset, um besondere Schatteneffekte zu erstellen. Weitere Informationen zu zweiten Offsets finden Sie unter dem [Type](type-attribute--shadow--vml.md) -Attribut.

*VML-Standard Attribut*

**Beispiel**

Für die Form wird ein doppelter Schatten erstellt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 