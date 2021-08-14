---
title: VML-Margin-Right-Attribut
description: VML-Margin-Right-Attribut
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5569f4f89cbe5320cfc348f2e2929b986736412f4cb864a62dd4584bde43a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346458"
---
# <a name="vml-margin-right-attribute"></a>VML-Margin-Right-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt den rechten Rand des enthaltenden Rechtecks der Form relativ zum Formanker an. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* style="margin-right: *ausdruck* ">

**Skriptsyntax**

*element* .style.marginright="*expression*"

*expression* = *.style.marginright-Element*

**Anmerkungen**

Das **Margin-Right-Attribut** ähnelt dem standardmäßigen **HTML-Margin-Right-Attribut,** das mit Stylesheets verwendet wird.

Beachten Sie, dass **marginright** anstelle von **margin-right** für die Skripterstellung verwendet wird. Beachten Sie außerdem, dass sich der Rand nicht zu ändern scheint, wenn die **Position** **absolut** ist.

Mögliche Werte:



| Wert      | BESCHREIBUNG                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automatisch       | Standardposition eines Elements im Seitenfluss.                                                                                                                                           |
| units      | Standard. Eine Zahl mit einem absoluten Einheiten-Kennzeichner (cm, mm, in, pt, pc oder px) oder einem bezeichner für relative Einheiten (em oder ex). Wenn keine Einheiten angegeben werden, wird von Pixeln (px) ausgegangen. Der Standardwert ist 0. |
| Prozentwert | Der Als Prozentsatz der Höhe des übergeordneten Objekts ausgedrückte Wert.                                                                                                                                    |



 

*VML-Standardattribut*

**Siehe auch**

[Einheiten](msdn-online-vml-units.md)

**Beispiel**

Der rechte Rand ist auf 25 Pixel festgelegt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



[Beispiel für ein Margin-Right-Attribut.](/previous-versions/bb229677(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 