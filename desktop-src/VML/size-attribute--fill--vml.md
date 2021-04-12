---
title: Size-Attribut (Fill) (VML)
description: Size-Attribut (Fill) (VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eea5638d619853857499cc317517dfc5ffc762
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948804"
---
# <a name="size-attribute-fillvml"></a>Size-Attribut (Fill) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Größe des Bilds für die Füllung. Lese-/Schreibzugriff. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* size = " *Expression* " >

**Skript Syntax**

*Element* . Size = "*Ausdruck * * *"**

*Ausdruck* = *Element*. Size

**Anmerkungen**

Der Standardwert ist die Größe des ursprünglichen Bilds. Größen, die größer als der shapewert sind, zeigen eine vergrößerte, aber abgeschnittene Version des Bilds an.

*VML-Standard Attribut*

**Beispiel**

Obwohl die ursprüngliche Größe des Bilds 50-bis-50 Punkte beträgt, wird das Bild als 10-bis-10-Bild in der Mitte der Füllung angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 