---
title: VML-Schaltflächenattribut
description: VML-Schaltflächenattribut
ms.assetid: 273024ac-683f-48d2-b6a0-574824f4c05d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c505feebbf4614f7e56c856fa2c757e93160823d8bcd2fd5d539da80c436f32b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754975"
---
# <a name="vml-button-attribute"></a>VML-Schaltflächenattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob eine Form als Schaltfläche verarbeitet wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:button=" *Ausdruck* ">

**Anmerkungen**

Der Standardwert ist **False**. True **gibt an,** dass die Form als Schaltfläche verarbeitet wird.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form ist eine Schaltfläche.


```HTML
   <v:rect id=myrect fillcolor="red" o:button="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 