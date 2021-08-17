---
title: VML BWNormal-Attribut
description: VML BWNormal-Attribut
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2811a9cd734e0f2ca6ca2f707b6313d7434ac756a1f9cd8982d7179c75748bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754955"
---
# <a name="vml-bwnormal-attribute"></a>VML BWNormal-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Schwarz-Weiß-Modus für normale Schwarz-Weiß-Ausgabegeräte. Lese-/Schreibzugriff. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:bwnormal=" *Ausdruck* ">

**Anmerkungen**

Wenn [BWMode](msdn-online-vml-bwmode-attribute.md) auf auto festgelegt **ist,** wird dieses Attribut verwendet, um zu bestimmen, wie die Form in normalem Schwarz/Weiß gerendert wird.

Weitere Informationen zu den Werten dieses Attributs finden Sie im [Thema VgBlackWhiteMode.](msdn-online-vml-vgblackwhitemode.md) Der Standardwert ist **auto.**

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form wird als Graustufenbild für die normale Schwarz-Weiß-Ausgabe verarbeitet.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 