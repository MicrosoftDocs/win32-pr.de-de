---
title: Title-Attribut (Form)(VML)
description: Title-Attribut (Form)(VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ec2a16df6740bca64357dae039f4222de956300604198b2d199977970c526d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596508"
---
# <a name="title-attribute-shapevml"></a>Title-Attribut (Form)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Text, der angezeigt wird, wenn der Mauszeiger über die Form bewegt wird. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* title=" *ausdruck* ">

**Skriptsyntax**

*element* .title="*expression*"

*expression* = *Element*.title

**Anmerkungen**

Das **Title-Attribut** ähnelt dem **HTML-Standardtitelattribut.** Das Verhalten eines Titels ähnelt einer Microsoft Windows QuickInfo.

**VML-Standardattribut**

**Beispiel**

Der Titel der Form ist "QuickInfo-Anzeige" und wird angezeigt, wenn der Mauszeiger über die Form bewegt wird.


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Title-Attribut – Beispiel.](/previous-versions/bb264097(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 