---
title: VMLFont-Weight Attribut
description: VMLFont-Weight Attribut
ms.assetid: d7b2b0c5-b5cf-4e7d-bbca-c554d12bf97e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14dd5edb3fed869390edeff514471359162ee39fd1d78796af3d2a260c96bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754641"
---
# <a name="vml-font-weight-attribute"></a>VMLFont-Weight Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Stärke der Buchstaben der Schriftart. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* style="font-weight: *expression* ">

**Skriptsyntax**

*element* .style.fontweight="*expression*"

*expression* = *Element*.style.fontweight

**Anmerkungen**

Die Werte sind identisch mit den Standardattributen im HTML-Format. Mögliche Werte:



| Wert   | BESCHREIBUNG                                                                 |
|---------|-----------------------------------------------------------------------------|
| normal  | Normal. Standard.                                                            |
| fett    | Fettdruck                                                                       |
| bolder  | Größer als normal.                                                        |
| lighter | Leichter als normal.                                                        |
| 100     | Mindestens so hell wie das Gewicht von 200.                                        |
| 200     | Mindestens so fett wie das 100-Gewicht und mindestens so hell wie das 300-Gewicht. |
| 300     | Mindestens so fett wie das 200-Gewicht und mindestens so hell wie das 400-Gewicht. |
| 400     | Normal.                                                                     |
| 500     | Mindestens so fett wie das 400-Gewicht und mindestens so hell wie das 600-Gewicht. |
| 600     | Mindestens so fett wie das 500-Gewicht und mindestens so hell wie das 700-Gewicht. |
| 700     | Fettdruck                                                                       |
| 800     | Mindestens so fett wie das 700-Gewicht und mindestens so hell wie das 900-Gewicht. |
| 900     | Mindestens so fett wie die 800-Gewichtung.                                         |



 

*VML-Standardattribut*

**Beispiel**

Die Schriftgewichtung ist fett.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal bold 36pt Arial"/>
   </v:line>
```



 

 