---
title: VML LineStyle-Attribut
description: VML LineStyle-Attribut
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90be9c2aceeb3663f55c92e1140eb6a12f66aa23dd8856d0da63f0a306d8cd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598283"
---
# <a name="vml-linestyle-attribute"></a>VML LineStyle-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Linienart des Strichs. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* linestyle="-Ausdruck "> 

**Skriptsyntax**

*element* .linestyle="*expression*"

*expression* = *Element*.linestyle

**Anmerkungen**

Mögliche Werte:

-   Single (Standard)
-   ThinThin
-   ThinThick
-   ThickThin
-   ThickBetweenThin

*VML-Standardattribut*

**Beispiel**

Eine doppelte Linie wird mit zwei dünnen Strichen gezeichnet.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 