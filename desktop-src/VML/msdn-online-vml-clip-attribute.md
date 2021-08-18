---
title: VML-Clipattribut
description: VML-Clipattribut
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cab4afdef2a10c9c6f6a0561dedf5b4df3538a97152cb53181452b8ac531bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999290"
---
# <a name="vml-clip-attribute"></a>VML-Clipattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob die Beschneidung ein -Wert ist. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Tagsyntax**

<v: *element* clip="-Ausdruck "> 

**Skriptsyntax**

*element* .clip="*expression*"

*expression* = *Element*.clip

**Anmerkungen**

Wenn **Clip** auf **False festgelegt** ist, wird die Form an den Rahmen skaliert. True **gibt an,** dass teile der Form, die sich außerhalb des Rahmens befinden, nicht angezeigt werden.

Beachten [Sie, dass Ursprung](origin-attribute--vmlframe--vml.md) und [Größe](size-attribute--vmlframe.md) nur verwendet werden, wenn **Clip** true **ist.**

*VML-Standardattribut*

**Beispiel**

Das in der externen Datei definierte Bild wird abgeschnitten.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 