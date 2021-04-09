---
title: Size-Attribut (vmlframe)
description: Size-Attribut (vmlframe)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b0401c414a3536e22bdb7328b2b08b2fbcf45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039054"
---
# <a name="size-attribute-vmlframe"></a>Size-Attribut (vmlframe)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Größe des Clippingbereichs des Frames. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Vmlframe](msdn-online-vml-vmlframe-element.md)

**Tagsyntax**

<v: *Element* size = " *Expression* " >

**Skript Syntax**

*Element* . Size = "*Ausdruck*"

*Ausdruck* = *Element*. Size

**Anmerkungen**

Der Standardwert ist 0,0. Beachten Sie, dass **size** nur funktioniert, wenn [Clip](msdn-online-vml-clip-attribute.md) den Wert **true** hat. In diesem Attribut wird die Größe als Breite und Höhe des Frames definiert.

*VML-Standard Attribut*

**Beispiel**

Die Größe des Clippingbereichs beträgt 50 PT, 50pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 