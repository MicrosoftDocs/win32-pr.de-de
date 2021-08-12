---
title: VML FillColor-Attribut
description: VML FillColor-Attribut
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e626e017437d14cf1088c188e659e1099dc38c7ba88215438a6c9a45166c7732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601360"
---
# <a name="vml-fillcolor-attribute"></a>VML FillColor-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Pinselfarbe, die den geschlossenen Pfad einer Form ausfüllt. Lese-/Schreibzugriff. [IVgColor](msdn-online-vml-ivgcolor.md) .

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* fillcolor="-Ausdruck "> 

**Skriptsyntax**

*element* .fillcolor="*expression*"

*expression* = *Element*.fillcolor

**Anmerkungen**

Der **FillColor-Wert** wird aus dem **Color-Attribut** des **Fill-Elements dupliziert.**

*VML-Standardattribut*

**Siehe auch**

[Form,](shape-element--vml.md) [Füllen,](msdn-online-vml-fill-element.md) [IVgColor](msdn-online-vml-ivgcolor.md)

**Beispiel**

Die Füllfarbe des Rechtecks ist rot.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[FillColor-Attribut – Beispiel.](/previous-versions/bb229668(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 