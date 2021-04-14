---
title: VML-Grayscale-Attribut
description: VML-Grayscale-Attribut
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c4b5da616ec5f96eeb226ecb2ba18202874f67
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390529"
---
# <a name="vml-grayscale-attribute"></a>VML-Grayscale-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob ein Bild im Graustufen Modus angezeigt wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *Element* Grayscale = " *Ausdruck* " >

**Skript Syntax**

*Element* . Grayscale = "*Ausdruck*"

*Ausdruck* = *Element*. Grayscale

**Anmerkungen**

Wenn der Wert **true** ist, wird das Bild in Graustufen anstelle der Farbe angezeigt. Der Standardwert ist **False**.

Der Wert basiert auf der CCIR-Empfehlung 709, die eine höhere grüne Gewichtung begünstigt und detailliertere Ergebnisse für die natürliche Farbe erzeugt.

*VML-Standard Attribut*

**Beispiel**

Das Bild wird in Graustufen anstelle der Farbe angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 