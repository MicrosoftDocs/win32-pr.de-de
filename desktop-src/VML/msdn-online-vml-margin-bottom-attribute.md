---
title: VML-Margin-Bottom-Attribut
description: VML-Margin-Bottom-Attribut
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
# <a name="vml-margin-bottom-attribute"></a>VML-Margin-Bottom-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt den unteren Rand des enthaltenden Rechtecks der Form relativ zum Formanker an. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *element* margin-bottom=" *ausdruck* ">

**Skriptsyntax**

*element* .marginbottom="*expression*"

*expression* = *.marginbottom-Element*

**Anmerkungen**

Das **Margin-Bottom-Attribut** ähnelt dem standardmäßigen **HTML-Margin-Bottom-Attribut,** das mit Stylesheets verwendet wird.

Beachten Sie, dass **marginbottom** anstelle von **margin-bottom** für die Skripterstellung verwendet wird. Beachten Sie außerdem, dass sich der Rand nicht zu ändern scheint, wenn die **Position** **absolut** ist.

Mögliche Werte:



| Wert      | Beschreibung                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automatisch       | Standardposition eines Elements im Seitenfluss.                                                                                                                                           |
| units      | Standard. Eine Zahl mit einem absoluten Einheiten-Kennzeichner (cm, mm, in, pt, pc oder px) oder einem bezeichner für relative Einheiten (em oder ex). Wenn keine Einheiten angegeben werden, wird von Pixeln (px) ausgegangen. Der Standardwert ist 0. |
| Prozentwert | Der Als Prozentsatz der Höhe des übergeordneten Objekts ausgedrückte Wert.                                                                                                                                    |



 

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



[Beispiel für ein Margin-Bottom-Attribut.](/previous-versions/bb229675(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 