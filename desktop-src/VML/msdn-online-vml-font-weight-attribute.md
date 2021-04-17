---
title: VML-Font-Weight Attribut
description: VML-Font-Weight Attribut
ms.assetid: d7b2b0c5-b5cf-4e7d-bbca-c554d12bf97e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e4de8a1bb4132c75d4520dcacc661fbbc97eef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390530"
---
# <a name="vml-font-weight-attribute"></a>VML-Font-Weight Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Stärke der Buchstaben der Schriftart. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* Style = "Font-Weight: *Expression* " >

**Skript Syntax**

*Element* . Style. FontWeight = "*Ausdruck*"

*Ausdruck* = *Element*. Style. FontWeight

**Anmerkungen**

Die Werte sind identisch mit den standardmäßigen HTML-Format Attributen. Mögliche Werte:



| Wert   | BESCHREIBUNG                                                                 |
|---------|-----------------------------------------------------------------------------|
| normal  | Normal. Standard.                                                            |
| fett    | Fettdruck                                                                       |
| bolder  | Schwerer als normal.                                                        |
| lighter | Heller als normal.                                                        |
| 100     | Mindestens so hell wie die 200-Gewichtung.                                        |
| 200     | Mindestens so fett wie die 100-Gewichtung und mindestens so leicht wie die 300-Gewichtung. |
| 300     | Mindestens so fett wie die 200-Gewichtung und mindestens so leicht wie die 400-Gewichtung. |
| 400     | Normal.                                                                     |
| 500     | Mindestens so fett wie die 400-Gewichtung und mindestens so leicht wie die 600-Gewichtung. |
| 600     | Mindestens so fett wie die 500-Gewichtung und mindestens so leicht wie die 700-Gewichtung. |
| 700     | Fettdruck                                                                       |
| 800     | Mindestens so fett wie die 700-Gewichtung und mindestens so leicht wie die 900-Gewichtung. |
| 900     | Mindestens so fett wie die 800-Gewichtung.                                         |



 

*VML-Standard Attribut*

**Beispiel**

Die Schrift Breite ist fett formatiert.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal bold 36pt Arial"/>
   </v:line>
```



 

 