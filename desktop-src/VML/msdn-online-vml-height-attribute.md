---
title: VML Height-Attribut
description: VML Height-Attribut
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41751e4863fdb128dbbedf2e3abf8e7f0a6736d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101839"
---
# <a name="vml-height-attribute"></a>VML Height-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt die Höhe der Form an. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "height: *Expression* " >

**Skript Syntax**

*Element* . Style. Height = "*Ausdruck*"

*Ausdruck* = *Element*. Style. Height

**Anmerkungen**

Das **height** -Attribut ähnelt dem standardmäßigen HTML- **height** -Attribut für Stile.

Einheiten können dem übergeordneten Element zugeordnet werden, oder Sie können sich in absoluten Einheiten befinden.

Mögliche Werte:



| Wert      | BESCHREIBUNG                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Die Standardposition eines Elements im Fluss der Seite.                                                                                                          |
| units      | Eine Zahl mit einem absoluten Einheiten Kenn Zeichner (cm, mm, in, PT, PC oder px) oder einem relativen Einheiten Kenn Zeichner (em oder Ex). Wenn keine Einheiten angegeben werden, wird die Pixel (px) angenommen. |
| Prozentwert | Wert, ausgedrückt als Prozentsatz der Höhe des übergeordneten Objekts.                                                                                                   |



 

*VML-Standard Attribut*

**Siehe auch**

[Einheiten](msdn-online-vml-units.md)

**Beispiel**

Die Höhe der Form ist auf 30 festgelegt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



[Beispiel für Höhen Attribut](/previous-versions/bb229671(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 