---
title: VML-Attribut "onmouseover"
description: VML-Attribut "onmouseover"
ms.assetid: 68f0fa7a-0d22-4ede-8404-e007296960e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8318235b660f92f3d82b2dd8dd15e2192e97a84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039511"
---
# <a name="vml-onmouseover-attribute"></a>VML-Attribut "onmouseover"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Löst ein Maus Ereignis für eine Form aus. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* onmouseover = " *Expression* " >

**Anmerkungen**

Ein "MouseOver"-Ereignis wird generiert, wenn sich der Mauszeiger auf der Form befindet. Der Wert wird mithilfe des-Schlüssel Worts **this** (als Verweis auf das-Objekt) gefolgt von der-Objektmodell Syntax generiert. Wenn Sie z. b. die Füllfarbe in Rot ändern möchten, verwenden Sie Folgendes:

onmouseover = "this. FillColor = ' red '"

Beachten Sie, dass einfache und doppelte Anführungszeichen verwendet werden, um den Ausdruck festzulegen.

*VML-Standard Attribut*

**Beispiel**

Wenn sich der Mauszeiger auf der Form befindet, wird die Füllfarbe von rot in grün umgewandelt.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20"
   onmouseover='this.fillcolor="green"'>
   </v:rect>
```



[Beispiel für das onMouseOver-Attribut](/previous-versions/bb264088(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 