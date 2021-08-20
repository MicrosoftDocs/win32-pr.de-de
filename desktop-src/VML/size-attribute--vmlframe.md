---
title: Size-Attribut (VMLFrame)
description: Size-Attribut (VMLFrame)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32d496bc40b5b84b7a8a16bf6b84a2926010d56dcc311659dd63300363a7067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754125"
---
# <a name="size-attribute-vmlframe"></a>Size-Attribut (VMLFrame)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Größe des Ausschneidebereichs des Frames. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Tagsyntax**

<v: *element* size="-Ausdruck "> 

**Skriptsyntax**

*element* .size="*expression*"

*expression* = *Element*.size

**Anmerkungen**

Der Standardwert ist 0,0. Beachten Sie, **dass Größe** nur funktioniert, wenn [Clip](msdn-online-vml-clip-attribute.md) true **ist.** In diesem Attribut wird die Größe als Breite und Höhe des Frames definiert.

*VML-Standardattribut*

**Beispiel**

Die Größe des Ausschneidebereichs beträgt 50pt, 50pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 