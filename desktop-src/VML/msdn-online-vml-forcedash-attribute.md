---
title: VML forcedash-Attribut
description: VML forcedash-Attribut
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bcec4a694a6449412aa07ec69aa9a817aa917c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039300"
---
# <a name="vml-forcedash-attribute"></a>VML forcedash-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob ein gestrichelter Umriss verwendet wird, um eine Form zu zeichnen, wenn eine Form keine Zeile oder Füllung aufweist. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:forcedash = " *Ausdruck* " >

**Anmerkungen**

Wird von Microsoft PowerPoint-Platzhaltern zum Zeichnen einer gestrichelten Kontur verwendet, wenn keine Zeile und keine Füllung für eine Form vorhanden ist. Der Standardwert ist **False**. Wenn der Wert **true** ist, wird ein gestrichelter Umriss verwendet, um einen Platzhalter anzugeben.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Eine gestrichelte Linie wird verwendet, um die Form zu Rendering, wenn keine Zeile oder Füllung vorhanden ist.


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 