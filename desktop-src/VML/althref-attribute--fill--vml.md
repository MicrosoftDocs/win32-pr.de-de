---
title: Althref-Attribut (Fill) (VML)
description: Althref-Attribut (Fill) (VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0679e5aa01b934092c21bfa5d0504b056f620f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473445"
---
# <a name="althref-attribute-fillvml"></a>Althref-Attribut (Fill) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert einen alternativen Verweis für ein Bild. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Ausfüllen](msdn-online-vml-fill-element.md)

**Tagsyntax**

<v: *Element* o:althref = " *Ausdruck* " >

**Skript Syntax**

*Element* . althref = "*Ausdruck*"

*Ausdruck* = *Element*. althref

**Anmerkungen**

Unterstützt die Beibehaltung von Daten mithilfe von HTML-Roundtripping. Beim HTML-Schreibvorgang wird die alternative Darstellung (die ursprünglichen Daten, wenn die Datei aus dem Apple Macintosh stammt) gespeichert. Beim Lesen von HTML wird **althref** gegenüber **src** bevorzugt.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Füllung der Form hat eine **althref** , die auf eine Datei mit dem Namen "myimage.gif" zeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 