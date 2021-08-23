---
title: VML-RotationAngle-Attribut
description: VML-RotationAngle-Attribut
ms.assetid: d5432512-1ac2-497b-a415-cec3c1217120
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78fa8414c0fd30adab9b5c1e21a11102c3b9ea6ad8a0d31cb25c0e88040c93d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573990"
---
# <a name="vml-rotationangle-attribute"></a>VML-RotationAngle-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt die Drehung des -Objekts um die x- und y-Achse an. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Tagsyntax**

<o: *element* rotationangle=" *ausdruck* ">

**Skriptsyntax**

*element* .rotationangle="*expression*"

*expression* = *Element*.rotationangle

**Anmerkungen**

Die Drehung des Objekts wird durch einen Drehwinkel um die y-Achse gefolgt vom Drehwinkel um die x-Achse definiert. Der Z-Achsenwinkel wird durch den Wert des Standardattributs **HTML-Formatrotation** der Form gesteuert. Der Standardwert ist 0,0.

*Microsoft Office Extensions-Attribut*

 

 