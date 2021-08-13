---
title: Src-Attribut (ImageData)(VML)
description: Src-Attribut (ImageData)(VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688bc1e82afbaf0747a03465c93feb1d760cc60eb441792654ef11ec59cee749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596682"
---
# <a name="src-attribute-imagedatavml"></a>Src-Attribut (ImageData)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert eine Quelle für das Image. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *element* src=" *ausdruck* ">

**Skriptsyntax**

*element* .src="*expression*"

*expression* = *.src-Element*

**Anmerkungen**

Dieses Attribut muss immer mit dem [ImageData-Element](msdn-online-vml-imagedata-element.md) verwendet werden und auf gültige Bilddaten verweisen, damit ein Bild angezeigt wird. Wenn dieses Attribut ohne [HRef](https://www.bing.com/search?q=HRef) oder [Title](title-attribute--imagedata--vml.md)angezeigt wird, wird das Bild verknüpft.

*VML-Standardattribut*

**Beispiel**

Die Quelle des Images ist eine Datei mit dem Namen "kids.jpg".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 