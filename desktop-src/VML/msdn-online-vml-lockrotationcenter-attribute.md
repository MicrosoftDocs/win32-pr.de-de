---
title: VML LockRotationCenter-Attribut
description: VML LockRotationCenter-Attribut
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ef0cfee24998cfa343265569274ace688a05f90a270b721317394e59589a51e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598058"
---
# <a name="vml-lockrotationcenter-attribute"></a>VML LockRotationCenter-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob die Drehung des gekergten Objekts durch das [RotationAngle-Attribut](msdn-online-vml-rotationangle-attribute.md) angegeben wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Tagsyntax**

<o: *element* lockrotationcenter=" *ausdruck* ">

**Skriptsyntax**

*element* .lockrotationcenter="*expression*"

*expression* = *Element*.lockrotationcenter

**Anmerkungen**

**False** gibt an, dass die Drehung durch das [Orientation-Attribut](msdn-online-vml-orientation-attribute.md) angegeben wird. Der Standardwert ist **True**.

Beachten Sie dabei Folgendes:


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



der gleiche wie:


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



*Microsoft Office Extensions-Attribut*

 

 