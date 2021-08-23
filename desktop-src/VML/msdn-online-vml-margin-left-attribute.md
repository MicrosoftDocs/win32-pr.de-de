---
title: VML Margin-Left-Attribut
description: VML Margin-Left-Attribut
ms.assetid: 65488c47-06c2-4a8f-8d29-4837865465f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f403c19e617f8131886d3f4a862ff1ac0b878edbd2acf2fd0e27cb17b3406c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680821"
---
# <a name="vml-margin-left-attribute"></a>VML Margin-Left-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt den linken Rand des enthaltenden Rechtecks der Form relativ zum Formanker an. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *element* style="margin-left: *expression* ">

**Skriptsyntax**

*element* .style.marginleft="*expression*"

*expression* = *.style.marginleft-Element*

**Anmerkungen**

Das **Margin-Left-Attribut** ähnelt dem html-Standardattribut **Margin-Left,** das mit Stylesheets verwendet wird.

Beachten Sie, dass **marginleft** anstelle von **margin-left** für die Skripterstellung verwendet wird. Beachten Sie außerdem, dass sich der Rand nicht zu ändern scheint, wenn die **Position** **absolut** ist.

Diese Eigenschaft wird anstelle von **Left** für Formen in Microsoft Word und Microsoft Excel verwendet, die an einer Position relativ zu einem Ankerpunkt gleitend sind.

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

Der linke Rand ist auf 25 Pixel festgelegt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-left:25px">
   </v:rect>
```



[Beispiel für ein Margin-Left-Attribut.](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 