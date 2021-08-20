---
title: VML DoubleClickNotify-Attribut
description: VML DoubleClickNotify-Attribut
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9945f4391890f33d3569d1c1aed39a8ec5bbe4b0be29258da1cca4b7caf895da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124830"
---
# <a name="vml-doubleclicknotify-attribute"></a>VML DoubleClickNotify-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Sendet eine Ereignismeldung, wenn auf eine Form doppelklickt. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *element* o:doubleclicknotify=" *expression* ">

**Anmerkungen**

Der Standardwert ist **False** und gibt an, dass das Ereignis nicht ausgelöst wird.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form löst beim Doppelklicken ein Doppelklickereignis aus.


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 