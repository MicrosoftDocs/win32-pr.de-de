---
description: Windows unterstützt Formate zum Komprimieren von Bitmaps, die ihre Farben mit 8 oder 4 Bits pro Pixel definieren. Durch die Komprimierung wird der für die Bitmap erforderliche Datenträger-und Speicher Speicher reduziert.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Bitmapkomprimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38739f0e33f095b8eff567fc63b57db96b8cdc66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130853"
---
# <a name="bitmap-compression"></a>Bitmapkomprimierung

Windows unterstützt Formate zum Komprimieren von Bitmaps, die ihre Farben mit 8 oder 4 Bits pro Pixel definieren. Durch die Komprimierung wird der für die Bitmap erforderliche Datenträger-und Speicher Speicher reduziert.

Wenn das **Komprimierungs** Element der Bitmap-Informations Header Struktur BI \_ RLE8 ist, wird ein RLE-Format (Run-Length Encoding) zum Komprimieren einer 8-Bit-Bitmap verwendet. Dieses Format kann im codierten oder absoluten Modus komprimiert werden. Beide Modi können an beliebiger Stelle in der gleichen Bitmap vorkommen:

-   Der *codierte Modus* besteht aus zwei Bytes: mit dem ersten Byte wird die Anzahl der aufeinander folgenden Pixel angegeben, die mit dem im zweiten Byte enthaltenen Farb Index gezeichnet werden. Außerdem kann das erste Byte des Paars auf 0 (null) festgelegt werden, um ein Escapezeichen anzugeben, das das Ende einer Zeile, das Ende einer Bitmap oder ein Delta angibt, abhängig vom Wert des zweiten bytes. Die Interpretation der Escapesequenz hängt vom Wert des zweiten Bytes des Paars ab, bei dem es sich um einen der folgenden Werte handeln kann.



| Wert | Bedeutung                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Zeilenende.                                                                                                                                                |
| 1     | Ende der Bitmap.                                                                                                                                              |
| 2     | SS. Die 2 Bytes nach dem Escapezeichen enthalten nicht signierte Werte, die die horizontale und vertikale Offsets des nächsten Pixels von der aktuellen Position angeben. |



 

-   Im *absoluten Modus* ist das erste Byte 0 (null), und das zweite Byte ist ein Wert im Bereich 03h bis FFH. Das zweite Byte stellt die Anzahl der folgenden Bytes dar, von denen jeder den Farbindex eines einzelnen Pixels enthält. Wenn das zweite Byte zwei oder weniger ist, hat der Escape die gleiche Bedeutung wie der codierte Modus. Im absoluten Modus muss jede ausführen an einer Wort Grenze ausgerichtet werden.

Das folgende Beispiel zeigt die hexadezimalen Werte einer komprimierten 8-Bit-Bitmap:


```C++
[03 04] [05 06] [00 03 45 56 67] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



Die Bitmap wird wie folgt erweitert (zweistellige Werte stellen einen Farbindex für ein einzelnes Pixel dar):


```C++
04 04 04 
06 06 06 06 06 
45 56 67 
78 78 
move current position 5 right and 1 down 
78 78 
end of line 
1E 1E 1E 1E 1E 1E 1E 1E 1E 
end of RLE bitmap 
```



Wenn das **Komprimierungs** Element "BI RLE4" ist \_ , wird die Bitmap mithilfe eines Codierungs Formats der Laufzeit für eine 4-Bit-Bitmap komprimiert, das auch codierte und absolute Modi verwendet:

-   Im codierten Modus enthält das erste Byte des Paars die Anzahl der Pixel, die mit den Farbindizes im zweiten Byte gezeichnet werden. Das zweite Byte enthält zwei Farbindizes, eine in den hochwertigen 4 Bits und eine in den nieder wertigen 4 Bits. Der erste der Pixel wird mit der Farbe gezeichnet, die von den vier Bits mit hoher Reihenfolge angegeben wird, die zweite wird mit der Farbe in den niedriger Reihenfolge 4 Bits gezeichnet, die dritte mit der Farbe in den vier Bits mit hoher Reihenfolge usw., bis alle durch das erste Byte angegebenen Pixel gezeichnet wurden.
-   Im absoluten Modus ist das erste Byte gleich 0 (null). Das zweite Byte enthält die Anzahl der folgenden Farbindizes. Nachfolgende Bytes enthalten Farbindizes in ihren High-und Low-Order 4-Bits, einen Farbindex für jedes Pixel. Im absoluten Modus muss jede ausführen an einer Wort Grenze ausgerichtet werden. Die für BI-RLE8 beschriebenen End-of-Line-, End-of-Bitmap-und Delta-Escapezeichen \_ gelten auch für die BI \_ RLE4-Komprimierung.

Das folgende Beispiel zeigt die hexadezimalen Werte einer komprimierten 4-Bit-Bitmap:


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



Die Bitmap wird wie folgt erweitert (einstellige Werte stellen einen Farbindex für ein einzelnes Pixel dar):


```C++
0 4 0 
0 6 0 6 0 
4 5 5 6 6 7 
7 8 7 8 
move current position 5 right and 1 down 
7 8 7 8 
end of line 
1 E 1 E 1 E 1 E 1 
end of RLE bitmap 
```



 

 



