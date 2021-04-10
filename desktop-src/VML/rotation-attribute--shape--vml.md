---
title: Rotation-Attribut (Form) (VML)
description: Rotation-Attribut (Form) (VML)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03b114c885cbeaf5392068e79cd7f63bbc1fc52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039556"
---
# <a name="rotation-attribute-shapevml"></a>Rotation-Attribut (Form) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Winkel, in dem eine Form gedreht wird. Lese-/Schreibzugriff. [Vganglin Grad](msdn-online-vml-vgangleindegrees-data-type.md).

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "Rotation: *Expression* " >

**Skript Syntax**

*Element* . Rotation = "*Ausdruck*"

*Ausdruck* = *Element*. Drehung

**Anmerkungen**

Der Wert in Grad kann positiv oder negativ sein, und Werte, die größer als 360 sind, werden auf einen 360-Grad-Kreis modularisiert. Positive Winkel sind im Uhrzeigersinn. Der Standardwert ist 0.

Beachten Sie, dass die Form nach der Drehung neu positioniert wird, um die neuen Begrenzungsfeld Koordinaten widerzuspiegeln.

Beachten Sie außerdem, dass für die Skripterstellung das **Format Attribut nicht** verwendet wird und dass die **Drehung** als direktes Attribut der Form behandelt wird.

Das **Rotations** Attribut ähnelt dem Standard-HTML- **Rotations** Attribut für Stile.

*VML-Standard Attribut*

**Siehe auch**

**Beispiel**

Das Rechteck wird um 45 Grad gekippt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



[Beispiel für das Rotations Attribut](/previous-versions/bb264091(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 