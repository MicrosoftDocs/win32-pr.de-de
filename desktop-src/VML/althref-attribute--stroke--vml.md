---
title: Althref-Attribut (Strich) (VML)
description: Althref-Attribut (Strich) (VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021e89e87f70910561e55406e282920cdbed2963
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339291"
---
# <a name="althref-attribute-strokevml"></a>Althref-Attribut (Strich) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt einen alternativen Verweis für ein Bild an. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* o:althref = " *Ausdruck* " >

**Skript Syntax**

*Element* . althref = "*Ausdruck*"

*Ausdruck* = *Element*. althref

**Anmerkungen**

Unterstützt die Beibehaltung von Daten mithilfe von HTML-Roundtripping. Bei HTML-Schreibzugriff die alternative Darstellung (d. h. die ursprünglichen PICT-Daten, wenn die Datei vom Macintosh stammt) gespeichert wird. Beim Lesen von HTML wird **althref** gegenüber **src** bevorzugt.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Der Strich der Form hat eine **althref** , die auf eine Datei mit dem Namen "myimage.gif" zeigt.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 