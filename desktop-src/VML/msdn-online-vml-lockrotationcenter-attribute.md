---
title: VML-lockrotationcenter-Attribut
description: VML-lockrotationcenter-Attribut
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338487"
---
# <a name="vml-lockrotationcenter-attribute"></a>VML-lockrotationcenter-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob die Drehung des extrudierten Objekts durch das [RotationAngle](msdn-online-vml-rotationangle-attribute.md) -Attribut angegeben wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Schläuche](msdn-online-vml-extrusion-element.md)

**Tagsyntax**

<o: *Element* lockrotationcenter = " *Expression* " >

**Skript Syntax**

*Element* . lockrotationcenter = "*Ausdruck*"

*Ausdruck* = *Element*. lockrotationcenter

**Anmerkungen**

Wenn der Wert **false** ist, wird die Drehung durch das [Orientation](msdn-online-vml-orientation-attribute.md) -Attribut angegeben. Der Standardwert ist **True**.

Beachten Sie dabei Folgendes:


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



der gleiche wie:


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



*Microsoft Office Extensions-Attribut*

 

 