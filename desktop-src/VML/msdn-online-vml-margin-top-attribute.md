---
title: VML-Margin-Top Attribut
description: VML-Margin-Top Attribut
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14b6f4743f04740fe3fdbac4cc1d03f7bbe0282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316406"
---
# <a name="vml-margin-top-attribute"></a>VML-Margin-Top Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt den oberen Rand des enthaltenden Rechtecks der Form an, das relativ zum Shape-Anker ist. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Margin-Top = " *Ausdruck* " >

**Skript Syntax**

*Element* . Margin-Top = "*Ausdruck*"

*Ausdruck* = *Element*. Margin-Top

**Anmerkungen**

Das Attribut " **Margin-Top** " ähnelt dem standardmäßigen HTML-Attribut " **Margin-Top** ", das mit Stylesheets verwendet wird.

Beachten Sie, dass **MarginBottom** anstelle von **Margin-Top** für die Skripterstellung verwendet wird. Beachten Sie auch, dass der Rand nicht geändert werden kann, wenn die **Position** **absolut** ist.

Diese Eigenschaft wird anstelle von **Top** für Formen in Microsoft Word und Microsoft Excel verwendet, die in einer Position relativ zu einem Ankerpunkt schweben.

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

Der obere Rand ist auf 25 Pixel festgelegt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



[Beispiel für das margin-top-Attribut](/previous-versions/bb264087(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 