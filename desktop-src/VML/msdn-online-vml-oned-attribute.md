---
title: VML-Attribut mit Anmerkungen
description: VML-Attribut mit Anmerkungen
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1892d5ed185358c4abc5fa6fdaf6448ac5b6317c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316292"
---
# <a name="vml-oned-attribute"></a>VML-Attribut mit Anmerkungen

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob die zusätzlichen Handles einer Form ausgeblendet sind. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* ' o:oning = ' *Ausdruck* ' >

**Anmerkungen**

Blendet alle Shape-Handles außer der oberen linken und der unteren rechten Ecke aus. Das heißt, die gleichen Handles, die für ein gerades Liniensegment verwendet werden. Der Standardwert ist **False**.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Alle außer den linken oberen und unteren rechten Zieh Punkten der Form werden ausgeblendet.


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 