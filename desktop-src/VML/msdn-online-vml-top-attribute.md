---
title: Top-Attribut von VML
description: Top-Attribut von VML
ms.assetid: faad0c76-3566-4a51-962b-971667df2025
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c76a39035bc3dd3f0ae348280561e614d7dab4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728241"
---
# <a name="vml-top-attribute"></a>Top-Attribut von VML

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Position der Form relativ zum übergeordneten Element im Fluss der Seite. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "Top: *Expression* " >

**Skript Syntax**

*Element* . Style.Top = "*Ausdruck*"

*Ausdruck* = *Element*. Style.Top

**Anmerkungen**

Das **Top** -Attribut ähnelt dem standardmäßigen HTML- **Top** -Attribut für Stile.

Einheiten können dem übergeordneten Element zugeordnet werden, oder Sie können sich in absoluten Einheiten befinden. Dieses Attribut kann nicht für Formen geschrieben werden, die Inline verankert sind.

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

Der obere Rand der Form ist 5 Pixel unterhalb des Objekts, das ihm im Fluss der Seite vorangestellt ist.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:5;left:1;width:20;height:20">
   </v:rect>
```



[Beispiel](/previous-versions/bb264098(v=vs.85))für das Top-Attribut. (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 