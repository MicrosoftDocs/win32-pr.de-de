---
title: VML-Attribut "gewinnen"
description: VML-Attribut "gewinnen"
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5675503def2f48d4c5fbf7154f0d0d05b2fe417d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390671"
---
# <a name="vml-gain-attribute"></a>VML-Attribut "gewinnen"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Intensität aller Farben in einem Bild. Lese-/Schreibzugriff. **Vgnumber**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *Element* Gewinn = " *Ausdruck* " >

**Skript Syntax**

*Element* . Gewinn = "*Ausdruck*"

*Ausdruck* = *Element*. Gewinn

**Anmerkungen**

Dieses Attribut definiert, wie hell die Farbe weiß ist, was sich auf alle anderen Farben auswirkt. Die Werte reichen von 0 bis unendlich. Der Standardwert ist 1,0. Der Wert 0 zeigt kein Bild an. Werte, die größer als 1 sind, erleichtern das Bild, und Werte kleiner als 1 machen das Bild grau.

Dieses Attribut kann verwendet werden, um interessante Effekte zu erstellen.

*VML-Standard Attribut*

**Beispiel**

Das Bild wird mit allen Farben angezeigt, die in der grau Richtung angezeigt werden.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 