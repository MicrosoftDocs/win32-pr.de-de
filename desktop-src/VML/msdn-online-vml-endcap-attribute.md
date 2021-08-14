---
title: VML-EndCap-Attribut
description: VML-EndCap-Attribut
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b2d36eb76b840ca8f89aebf3dadefaa68093394a07bd78db0e8fa0b18ed555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346715"
---
# <a name="vml-endcap-attribute"></a>VML-EndCap-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Strichobergrenze für das Ende eines Strichs. Lese-/Schreibzugriff. **VgLineEndCapStyle**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: endcap="-Elementausdruck ">  

**Skriptsyntax**

*element* .endcap="*expression*"

*expression* = *Element*.endcap

**Anmerkungen**

Mögliche Werte:

-   Flach (Standard)
-   Square
-   Round

*VML-Standardattribut*

**Beispiel**

Eine Linie wird mit einem flachen Ende des Strichs gezeichnet.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 