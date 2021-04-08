---
title: Src-Attribut (imagedata) (VML)
description: Src-Attribut (imagedata) (VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039053"
---
# <a name="src-attribute-imagedatavml"></a>Src-Attribut (imagedata) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert eine Quelle für das Bild. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *Element* src = " *Expression* " >

**Skript Syntax**

*Element* . src = "*Ausdruck*"

*Ausdruck* = *Element*. src

**Anmerkungen**

Dieses Attribut muss immer mit dem [imagedata](msdn-online-vml-imagedata-element.md) -Element verwendet werden und auf gültige Bilddaten zeigen, damit ein Bild angezeigt wird. Wenn dieses Attribut ohne [href](https://www.bing.com/search?q=HRef) oder [Title](title-attribute--imagedata--vml.md)angezeigt wird, wird das Bild verknüpft.

*VML-Standard Attribut*

**Beispiel**

Die Quelle des Bilds ist eine Datei mit dem Namen "kids.jpg".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 