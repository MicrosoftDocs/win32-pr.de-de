---
title: VML bwnormal-Attribut
description: VML bwnormal-Attribut
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2fd14a50fc28c47154611b9a996fe0ef035f70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039198"
---
# <a name="vml-bwnormal-attribute"></a>VML bwnormal-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den schwarz-und weiß-Modus für normale schwarze und weiße Ausgabegeräte. Lese-/Schreibzugriff. [Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md).

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:bwnormal = " *Ausdruck* " >

**Anmerkungen**

Wenn [bwmode](msdn-online-vml-bwmode-attribute.md) auf **Auto** festgelegt ist, wird dieses Attribut verwendet, um zu bestimmen, wie die Form in normalem schwarz und weiß dargestellt werden soll.

Weitere Informationen zu den Werten dieses Attributs finden Sie im Thema [vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md) . Der Standardwert ist " **Auto**".

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form wird als Graustufenbild für die normale schwarze und weiße Ausgabe verarbeitet.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 