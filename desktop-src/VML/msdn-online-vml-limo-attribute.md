---
title: VML-Limo-Attribut
description: VML-Limo-Attribut
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa99325f396a3e4709fcd7ca1ee6ee82df1b653dff50df56df2df06ef2d513ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598310"
---
# <a name="vml-limo-attribute"></a>VML-Limo-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert einen Streckungspunkt auf dem Pfad. Lese-/Schreibzugriff. **Vector2D**.

**Gilt für**

[Path](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *element* limo="-Ausdruck "> 

**Skriptsyntax**

*element* .limo="*expression*"

*expression* = *Limo-Element*

**Anmerkungen**

Der Standardwert ist "0 0". Limostreckungen sind Punkte am Rand einer Form, die definieren, wo und wie eine Form von einem Benutzer in einem grafischen Editor gestreckt werden kann.

*VML-Standardattribut*

**Beispiel**

Ein Limo-Streckpunkt wird in der Mitte der horizontalen Linie definiert.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 