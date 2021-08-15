---
title: VMLMargin-Bottom Attribut
description: VMLMargin-Bottom Attribut
ms.assetid: c1101430-f4fc-4fa5-8e02-7cee126c2c1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551cf9cba00901e07998f2de38465cba1cb45bb8f563c04d1adf25f75d1852bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057818"
---
# <a name="vml-margin-bottom-attribute"></a>VMLMargin-Bottom Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt den unteren Rand des Rechtecks der Form an, das relativ zum Formanker enthält. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* margin-bottom="-Ausdruck "> 

**Skriptsyntax**

*element* .marginbottom="*expression*"

*expression* = *Element*.marginbottom

**Anmerkungen**

Das **Margin-Bottom-Attribut** ähnelt dem html-Standardattribut **Margin-Bottom,** das mit Stylesheets verwendet wird.

Beachten Sie, **dass marginbottom** anstelle von **margin-bottom für skriptbasierte** Skripts verwendet wird. Beachten Sie auch, dass **sich der Rand** nicht zu ändern scheint, wenn die Position **absolut** ist.

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

Der untere Rand ist auf 25 Pixel festgelegt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-bottom:25px">
   </v:rect>
```



[Beispiel für das Margin-Bottom-Attribut.](/previous-versions/bb229675(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 