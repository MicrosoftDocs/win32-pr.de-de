---
title: VML bwpure-Attribut
description: VML bwpure-Attribut
ms.assetid: a68e8197-bfd6-4b8e-8d4c-598590addff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e39c658265a5ab8c617fc8856db362a80d1ea8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858330"
---
# <a name="vml-bwpure-attribute"></a>VML bwpure-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den schwarz-und weißen Modus für reine schwarze und weiße Ausgabegeräte. Lese-/Schreibzugriff. [Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md).

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:bwpure = " *Ausdruck* " >

**Anmerkungen**

Wenn [bwmode](msdn-online-vml-bwmode-attribute.md) auf **Auto** festgelegt ist, wird dieses Attribut verwendet, um zu bestimmen, wie die Form in rein schwarz und weiß dargestellt werden soll.

Weitere Informationen zu den Werten dieses Attributs finden Sie im Thema [vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md) . Der Standardwert ist " **Auto**".

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form wird als Bild mit hohem Kontrast für reine schwarze und weiße Ausgabe verarbeitet.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwpure="highcontrast" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 