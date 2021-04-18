---
title: VML Width-Attribut
description: VML Width-Attribut
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b3d4917d76b3c8820186b04b2e77537e6a6ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337851"
---
# <a name="vml-width-attribute"></a>VML Width-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Breite der Form. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "width: *Expression* " >

**Skript Syntax**

*Element* . Style. Width = "*Ausdruck*"

*Ausdruck* = *Element*. Style. Width

**Anmerkungen**

Das **Width** -Attribut ähnelt dem standardmäßigen HTML- **Width** -Attribut für Stile.

Einheiten können dem übergeordneten Element zugeordnet werden, oder Sie können sich in absoluten Einheiten befinden.

Mögliche Werte:



| Wert      | BESCHREIBUNG                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Die Standardposition eines Elements im Fluss der Seite.                                                                                                          |
| units      | Eine Zahl mit einem absoluten Einheiten Kenn Zeichner (cm, mm, in, PT, PC oder px) oder einem relativen Einheiten Kenn Zeichner (em oder Ex). Wenn keine Einheiten angegeben werden, wird die Pixel (px) angenommen. |
| Prozentwert | Wert, ausgedrückt als Prozentsatz der Breite des übergeordneten Objekts.                                                                                                    |



 

*VML-Standard Attribut*

**Siehe auch**

[Einheiten](msdn-online-vml-units.md)

**Beispiel**

Die Breite der Form ist 25.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:25;height:20">
   </v:rect>
```



[Beispiel](/previous-versions/bb264101(v=vs.85))für das width-Attribut. (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 