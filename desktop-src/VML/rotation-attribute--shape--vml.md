---
title: Rotationsattribut (Shape)(VML)
description: Rotationsattribut (Shape)(VML)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f73b55b57a7b9d9d7f14cdae4ec71a38a1e38246a4430339db23f35a339430
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754135"
---
# <a name="rotation-attribute-shapevml"></a>Rotationsattribut (Shape)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Winkel, in dem eine Form gedreht wird. Lese-/Schreibzugriff. [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* style="rotation: *ausdruck* ">

**Skriptsyntax**

*element* .rotation="*expression*"

*expression* = *Elementrotation*

**Anmerkungen**

Der Wert in Grad kann positiv oder negativ sein, und Werte größer als 360 werden in einen 360-Grad-Kreis modularisiert. Positive Winkel sind im Uhrzeigersinn. Der Standardwert ist 0.

Beachten Sie, dass die Form nach der Drehung neu positioniert wird, um die neuen Begrenzungsfeldkoordinaten widerzuspiegeln.

Beachten Sie außerdem, dass  für die Skripterstellung das Formatattribut nicht verwendet wird und **rotation** als direktes Attribut der Form behandelt wird.

Das **Rotation-Attribut** ähnelt dem Standardmäßigen **HTML-Rotationsattribut** für Stile.

*VML-Standardattribut*

**Siehe auch**

**Beispiel**

Das Rechteck wird um 45 Grad geneigt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



[Rotationsattribut – Beispiel.](/previous-versions/bb264091(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 