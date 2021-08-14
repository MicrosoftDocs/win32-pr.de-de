---
title: VML-Margin-Top Attribut
description: VML-Margin-Top Attribut
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e42d86ba6e0fe05c2b0dff1f6d8bdabba0100fffee97d489fd59360cb8e13bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346396"
---
# <a name="vml-margin-top-attribute"></a>VML-Margin-Top Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt den oberen Rand des Rechtecks der Form an, das relativ zum Formanker enthält. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* margin-top="-Ausdruck "> 

**Skriptsyntax**

*element* .margin-top="*expression*"

*expression* = *Element*.margin-top

**Anmerkungen**

Das **Margin-Top-Attribut** ähnelt dem standardmäßigen HTML **Margin-Top-Attribut,** das mit Stylesheets verwendet wird.

Beachten **Sie, dass margintop** anstelle von **margin-top für Skripts** verwendet wird. Beachten Sie auch, dass **sich der Rand** nicht zu ändern scheint, wenn die Position **absolut** ist.

Diese Eigenschaft wird anstelle von **Top** für Formen in Microsoft Word und Microsoft Excel verwendet, die an einer Position relativ zu einem Ankerpunkt gleiten.

Mögliche Werte:



| Wert      | BESCHREIBUNG                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automatisch       | Standardposition eines Elements im Fluss der Seite.                                                                                                                                           |
| units      | Standard. Eine Zahl mit einem absoluten Einheiten-Designator (cm, mm, in, pt, pc oder px) oder einem relativen Einheiten-Designator (em oder ex). Wenn keine Einheiten angegeben werden, wird von Pixeln (px) ausgegangen. Der Standardwert ist 0. |
| Prozentwert | Wert, der als Prozentsatz der Höhe des übergeordneten Objekts ausgedrückt wird.                                                                                                                                    |



 

*VML-Standardattribut*

**Siehe auch**

[Einheiten](msdn-online-vml-units.md)

**Beispiel**

Der obere Rand ist auf 25 Pixel festgelegt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



[Margin-Top-Attribut – Beispiel.](/previous-versions/bb264087(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 