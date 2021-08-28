---
description: Text-Recognizer unterteilen ein Ink-Beispiel in Segmente und übersetzen die Ink-Segmente in Text.
ms.assetid: 9fbdde0e-5312-48ec-9273-ded6703b99a9
title: Text-Recognizers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2a579681fbd06c6b5dd27e5388f2c797e6be50433e11490fb5fe204d1c65d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842820"
---
# <a name="text-recognizers"></a>Text-Recognizers

Text-Recognizer unterteilen ein Ink-Beispiel in Segmente und übersetzen die Ink-Segmente in Text. Dies ist nützlich, um Handschriften zu erkennen. Dies ist auch in komplexen Schreibszenarien nützlich, z. B. beim Erkennen einzelner Kanji-Glyphen und beim Automatischen Vervollständigen eines Zeichens für Benutzer.

Eine Texterkennung gibt eine Unicode-Zeichenfolge für jedes Ink-Erkennungssegment zurück. Die Zeichenfolge ist der Vertrauensgrad, der dem Ergebnis von der -Erkannten zugewiesen wird, und eine Zuordnung des Ergebnisses zurück zur ursprünglichen Ink-Datei. Diese Zuordnung zeigt, welches Segment in der ursprünglichen Ink-Datei der Unicode-Codezeichenfolge entspricht. Die Zeichenfolge, die die Ausgabe der Text-Recognizer darstellt, wird immer in linearer Reihenfolge dargestellt, nicht in der räumlichen Reihenfolge oder chronologischen Reihenfolge, in der die Segmente eingegeben wurden.

In der folgenden Tabelle sind die Sprachen aufgeführt, die von den Handschrifterkennungen von Microsoft unterstützt werden, sowie die Windows Versionen, in denen diese Sprachen zum ersten Mal eingeführt wurden. Beachten Sie, dass einige Sprach erkennende Funktionen unter bestimmten Versionen von Windows möglicherweise nicht verfügbar sind und separat heruntergeladen werden müssen. Drittanbieter-Recognizer sind möglicherweise auch für zusätzliche Sprachen verfügbar, werden aber nicht unbedingt von Microsoft unterstützt.



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
| Niederländisch (Niederländisch und Norwegen)            |                              |                                   | X             |           |
| Portugiesisch (Brasilien und Portugiesisch/Neutral) |                              |                                   | X             |           |
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
| Serbisch (Kyrillisch und Lateinisch)               |                              |                                   |               | X         |
| Spanisch (Spanien und Mexiko)             |                              |                                   |               | X         |
| Schwedisch                                    |                              |                                   |               | X         |



 

 

 



