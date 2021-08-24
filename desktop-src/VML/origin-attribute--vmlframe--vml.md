---
title: Origin-Attribut (VMLFrame)(VML)
description: Origin-Attribut (VMLFrame)(VML)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874b857a2408927e296f82f0f9aa0a5e15f6da69b1e2af6eaf6ebe2c5df746d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768260"
---
# <a name="origin-attribute-vmlframevml"></a>Origin-Attribut (VMLFrame)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Ursprung des Ausschneidebereichs des Frames. Lese-/Schreibzugriff. **VgVector2D**.

**Gilt für**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Tagsyntax**

<v: *element* origin="-Ausdruck "> 

**Skriptsyntax**

*element* .origin="*expression*"

*expression* = *Element*.origin

**Anmerkungen**

Der Standardwert ist 0,0. Beachten Sie, **dass Origin** nur funktioniert, wenn [Clip](msdn-online-vml-clip-attribute.md) true **ist.** In diesem Attribut wird der Ursprung als die obere linke Ecke des Frames definiert.

*VML-Standardattribut*

**Beispiel**

Der Ursprung des Clippingbereichs ist 100pt,100pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 