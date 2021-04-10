---
title: Angle-Attribut (Fill) (VML)
description: Angle-Attribut (Fill) (VML)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039518"
---
# <a name="angle-attribute-fillvml"></a>Angle-Attribut (Fill) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Winkel einer Farbverlaufsfüllung. Lese-/Schreibzugriff. [Vgangle](msdn-online-vml-vgangleindegrees-data-type.md) .

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* Winkel = " *Ausdruck* " >

**Skript Syntax**

*Element* . Angle = "*Ausdruck*"

*Ausdruck* = *Element*. Angle

**Anmerkungen**

Der Vektor eines Farbverlaufs ist senkrecht zum Vektor der Blend-Richtung von einer Farbe zu einer anderen. Der Standardwert ist 0 (null) Grad, bei dem es sich um einen horizontalen Vektor von links nach rechts handelt. Positive Winkel drehen den Farbverlauf gegen den Uhrzeigersinn.

*VML-Standard Attribut*

**Beispiel**

Die Füllung der Form besteht aus einem Farbverlauf von zwei Farben und wird von blau zu rot mit einem Winkel von 45 Grad ausgeführt. Rot wird in der oberen linken Ecke angezeigt, und blau befindet sich in der unteren rechten Ecke.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 