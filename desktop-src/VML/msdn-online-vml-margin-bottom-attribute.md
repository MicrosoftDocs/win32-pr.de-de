---
title: VML-Margin-Bottom Attribut
description: VML-Margin-Bottom Attribut
ms.assetid: c1101430-f4fc-4fa5-8e02-7cee126c2c1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35712733179a3c03dc291c4d5efcf4fee68c2865
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728824"
---
# <a name="vml-margin-bottom-attribute"></a>VML-Margin-Bottom Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt den unteren Rand des enthaltenden Rechtecks der Form an, das relativ zum Shape-Anker ist. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* margin-bottom = " *Ausdruck* " >

**Skript Syntax**

*Element* . MarginBottom = "*Ausdruck*"

*Ausdruck* = *Element*. MarginBottom

**Anmerkungen**

Das Attribut " **margin-bottom** " ähnelt dem standardmäßigen HTML-Attribut " **margin-bottom** ", das mit Stylesheets verwendet wird.

Beachten Sie, dass **MarginBottom** anstelle von **margin-bottom** für die Skripterstellung verwendet wird. Beachten Sie auch, dass der Rand nicht geändert werden kann, wenn die **Position** **absolut** ist.

Mögliche Werte:



| Wert      | BESCHREIBUNG                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Die Standardposition eines Elements im Fluss der Seite.                                                                                                                                           |
| units      | Standard. Eine Zahl mit einem absoluten Einheiten Kenn Zeichner (cm, mm, in, PT, PC oder px) oder einem relativen Einheiten Kenn Zeichner (em oder Ex). Wenn keine Einheiten angegeben werden, wird die Pixel (px) angenommen. Der Standardwert ist 0. |
| Prozentwert | Wert, ausgedrückt als Prozentsatz der Höhe des übergeordneten Objekts.                                                                                                                                    |



 

*VML-Standard Attribut*

**Siehe auch**

[Einheiten](msdn-online-vml-units.md)

**Beispiel**

Der untere Rand ist auf 25 Pixel festgelegt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-bottom:25px">
   </v:rect>
```



[Beispiel für das margin-bottom-Attribut](/previous-versions/bb229675(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 