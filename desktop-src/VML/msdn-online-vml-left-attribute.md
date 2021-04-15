---
title: VML Left-Attribut
description: VML Left-Attribut
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17810d7635d4b8194f2bd2df258a900cb534581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474028"
---
# <a name="vml-left-attribute"></a>VML Left-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt die Position der Form relativ zum Element, das im Dokument Fluss links davon liegt. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "left: *Expression* " >

**Skript Syntax**

*Element* . Style. Left = "*Ausdruck*"

*Ausdruck* = *Element*. Style. Left

**Anmerkungen**

Das **left** -Attribut ähnelt dem standardmäßigen HTML-Attribut **left** für Stile.

Einheiten können dem übergeordneten Element zugeordnet werden, oder Sie können sich in absoluten Einheiten befinden. Dieses Attribut wird nicht für Formen geschrieben, die Inline verankert sind.

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

Der linke Wert der Form wird im folgenden Beispiel auf 1 festgelegt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Beispiel für das linke Attribut](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 