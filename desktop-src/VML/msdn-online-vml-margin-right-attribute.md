---
title: VML-Margin-Right Attribut
description: VML-Margin-Right Attribut
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5529257a0e21c8a8f8c7a1a2f8381c10a6e3b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039582"
---
# <a name="vml-margin-right-attribute"></a>VML-Margin-Right Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt den rechten Rand des enthaltenden Rechtecks der Form an, das relativ zum Shape-Anker ist. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "margin-right: *Expression* " >

**Skript Syntax**

*Element* . Style. MarginRight = "*Ausdruck*"

*Ausdruck* = *Element*. Style. MarginRight

**Anmerkungen**

Das Attribut " **margin-right** " ähnelt dem standardmäßigen HTML-Attribut " **margin-right** ", das mit Stylesheets verwendet wird.

Beachten Sie, dass **MarginRight** anstelle von **margin-right** für die Skripterstellung verwendet wird. Beachten Sie auch, dass der Rand nicht geändert werden kann, wenn die **Position** **absolut** ist.

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

Der Rechte Rand ist auf 25 Pixel festgelegt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



[Beispiel für das margin-right-Attribut](/previous-versions/bb229677(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 