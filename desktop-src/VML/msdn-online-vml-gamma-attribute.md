---
title: VML-Gammaattribut
description: VML-Gammaattribut
ms.assetid: 47a4d10e-f5ef-457b-92dd-bce5dae59b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c333bcb30a66aa9a87bc8402d64734e40504a0c49a38a8543c7fa97acfee7e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118845403"
---
# <a name="vml-gamma-attribute"></a>VML-Gammaattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Kontrast für ein Bild. Lese-/Schreibzugriff. **VgNumber**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *element* gamma="-Ausdruck "> 

**Skriptsyntax**

*element* .gamma="*expression*"

*expression* = *Element*.gamma

**Anmerkungen**

Durch verringern des Gammawerts unter 1 wird ein Bild verändert, um den Kontrast zu erhöhen, während Werte größer als 1 den Kontrast verringern. Nützliche Werte liegen zwischen 0,3 und etwa 3. Der Standardwert ist 0.

*VML-Standardattribut*

**Beispiel**


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gamma=".7" src="gamera.jpg"/>
   </v:shape>
```



 

 