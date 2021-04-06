---
description: Text erkenungen teilen ein Ink-Beispiel in Segmente und übersetzen die frei Hand Segmente in Text.
ms.assetid: 9fbdde0e-5312-48ec-9273-ded6703b99a9
title: Text erkenzer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8372af61d45bb1cc8bcd8377202149073c3decc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759511"
---
# <a name="text-recognizers"></a>Text erkenzer

Text erkenungen teilen ein Ink-Beispiel in Segmente und übersetzen die frei Hand Segmente in Text. Dies ist nützlich für das Erkennen von Handschrift. Dies ist auch in komplexen Schreib Szenarien nützlich, wie z. b. das erkennen einzelner Kanji-Glyphen und die automatische Vervollständigung eines Zeichens beim Schreiben.

Eine Texterkennung gibt für jedes frei Hand Erkennungs Segment eine Unicode-Zeichenfolge zurück. Die Zeichenfolge ist der Vertrauensgrad, den die Erkennung dem Ergebnis zuweist, und eine Zuordnung des Ergebnisses zurück zum ursprünglichen frei Hand Eingaben. Diese Zuordnung zeigt, welches Segment in der ursprünglichen frei Hand Eingabe der Unicode-Code Zeichenfolge entspricht. Die Zeichenfolge, die die Ausgabe der Texterkennung darstellt, wird immer in der linearen Reihenfolge und nicht in der räumlichen Reihenfolge oder in chronologischer Reihenfolge dargestellt, in der die Segmente eingegeben wurden.

In der folgenden Tabelle werden die Sprachen aufgelistet, die von den Handschrift Erkennungsprogrammen von Microsoft unterstützt werden, sowie die Windows-Versionen, in denen diese Sprachen erstmals Beachten Sie, dass einige sprach erkenzer möglicherweise nicht in einer bestimmten Version von Windows verfügbar sind und separat heruntergeladen werden müssen. Erkennungs Tools von Drittanbietern sind möglicherweise auch für zusätzliche Sprachen verfügbar, werden aber nicht unbedingt von Microsoft unterstützt.



| Sprache                                   | Windows XP Tablet PC Edition | Windows XP Tablet PC Edition 2005 | Windows Vista | Windows 7 |
|--------------------------------------------|------------------------------|-----------------------------------|---------------|-----------|
| Chinesisch (vereinfacht und traditionell)       | X                            |                                   |               |           |
| Englisch (USA, Vereinigtes Königreich, Kanada und Australien)    | X                            |                                   |               |           |
| Französisch                                     | X                            |                                   |               |           |
| Deutsch                                     | X                            |                                   |               |           |
| Japanisch                                   | X                            |                                   |               |           |
| Koreanisch                                     | X                            |                                   |               |           |
| Spanisch                                    | X                            |                                   |               |           |
| Italienisch                                    |                              | X                                 |               |           |
| Niederländisch (Niederlande und Belgien)            |                              |                                   | X             |           |
| Portugiesisch (Brasilien und Portugiesisch/neutral) |                              |                                   | X             |           |
| Katalanisch                                    |                              |                                   |               | X         |
| Kroatisch                                   |                              |                                   |               | X         |
| Tschechisch                                      |                              |                                   |               | X         |
| Dänisch                                     |                              |                                   |               | X         |
| Finnisch                                    |                              |                                   |               | X         |
| Deutsch (Schweiz)                       |                              |                                   |               | X         |
| Norwegisch (Bokmal und Nynorsk)             |                              |                                   |               | X         |
| Polnisch                                     |                              |                                   |               | X         |
| Portugiesisch (Portugal)                      |                              |                                   |               | X         |
| Rumänisch                                   |                              |                                   |               | X         |
| Russisch                                    |                              |                                   |               | X         |
| Serbisch (Kyrillisch und lateinisch)               |                              |                                   |               | X         |
| Spanisch (Argentinien und Mexiko)             |                              |                                   |               | X         |
| Schwedisch                                    |                              |                                   |               | X         |



 

 

 



