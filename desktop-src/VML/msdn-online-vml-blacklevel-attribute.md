---
title: VML BlackLevel-Attribut
description: VML BlackLevel-Attribut
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe31c9507468efd27aac9d9729a4f2ee3ddce449398b4a68bd7d79b2d029b8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057908"
---
# <a name="vml-blacklevel-attribute"></a>VML BlackLevel-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Intensität von Schwarz in einem Bild. Lese-/Schreibzugriff. **VgNumber**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *element* blacklevel=" *ausdruck* ">

**Skriptsyntax**

*element* .blacklevel="*expression*"

*expression* = *Element*.blacklevel

**Anmerkungen**

Ermöglicht es, die Farbebene so zu ändern, dass Schwarz als echte Schwarze und alle anderen Farben als Schattierungen über Schwarz angezeigt werden. Der Standardwert ist 0. Während eine beliebige Zahl zwischen positiv und negativ unendlich zulässig ist, werden Werte kleiner als -0,5 angezeigt, da alle Werte schwarz und Werte größer als 0,5 als alle weiß angezeigt werden.

*VML-Standardattribut*

**Beispiel**

Das Bild wird mit sehr dunklen Tönen angezeigt.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 