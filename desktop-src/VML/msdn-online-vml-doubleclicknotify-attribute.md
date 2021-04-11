---
title: VML-Attribut "doubleclicknotify"
description: VML-Attribut "doubleclicknotify"
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16be329952cfff23957f961fb6d29198ad173898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315236"
---
# <a name="vml-doubleclicknotify-attribute"></a>VML-Attribut "doubleclicknotify"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Sendet eine Ereignismeldung, wenn auf eine Form Doppel geklickt wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:doubleclicknotify = " *Ausdruck* " >

**Anmerkungen**

Der Standardwert ist **false**, was darauf hinweist, dass das Ereignis nicht ausgelöst wird.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Bei einem Doppelklick wird durch die Form ein Doppelklick Ereignis auslöst.


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 