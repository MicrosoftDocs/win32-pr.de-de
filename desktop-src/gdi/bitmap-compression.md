---
description: Windows unterstützt Formate zum Komprimieren von Bitmaps, die ihre Farben mit 8 oder 4 Bits pro Pixel definieren. Die Komprimierung reduziert den Datenträger- und Arbeitsspeicherspeicher, der für die Bitmap erforderlich ist.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Bitmapkomprimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcefec93bb5583ba066e35d5143410d1c249bb09
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812846"
---
# <a name="bitmap-compression"></a>Bitmapkomprimierung

Windows unterstützt Formate zum Komprimieren von Bitmaps, die ihre Farben mit 8 oder 4 Bits pro Pixel definieren. Die Komprimierung reduziert den Datenträger- und Arbeitsspeicherspeicher, der für die Bitmap erforderlich ist.

Wenn der **Komprimierungsmember** der Bitmapinformationsheaderstruktur BI \_ RLE8 ist, wird ein RLE-Format (Run-Length Encoding) verwendet, um eine 8-Bit-Bitmap zu komprimieren. Dieses Format kann im codierten oder absoluten Modus komprimiert werden. Beide Modi können überall in derselben Bitmap auftreten:

-   *Der codierte Modus* besteht aus zwei Bytes: Das erste Byte gibt die Anzahl der aufeinanderfolgenden Pixel an, die mit dem im zweiten Byte enthaltenen Farbindex gezeichnet werden sollen. Darüber hinaus kann das erste Byte des Paars auf 0 (null) festgelegt werden, um ein Escapezeichen anzugeben, das das Ende einer Zeile, das Ende einer Bitmap oder ein Delta angibt, abhängig vom Wert des zweiten Byte. Die Interpretation des Escapewerts hängt vom Wert des zweiten Byte des Paars ab. Dies kann einer der folgenden Werte sein.



| Wert | Bedeutung                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Zeilenende.                                                                                                                                                |
| 1     | Ende der Bitmap.                                                                                                                                              |
| 2     | Delta. Die 2 Bytes nach dem Escapezeichen enthalten Werte ohne Vorzeichen, die die horizontalen und vertikalen Offsets des nächsten Pixels von der aktuellen Position angeben. |



 

-   Im *absoluten Modus* ist das erste Byte 0 (null), und das zweite Byte ist ein Wert im Bereich von 03H bis FFH. Das zweite Byte stellt die Anzahl der folgenden Bytes dar, von denen jedes den Farbindex eines einzelnen Pixels enthält. Wenn das zweite Byte zwei oder weniger ist, hat das Escapeobjekt die gleiche Bedeutung wie der codierte Modus. Im absoluten Modus muss jede Ausführung nullaufgefüllt werden, um an einer 16-Bit-Wortgrenze zu enden.

Das folgende Beispiel zeigt die Hexadezimalwerte einer 8-Bit-komprimierten Bitmap:


```C++
[03 04] [05 06] [00 03 45 56 67 00] [02 78] [00 02 05 01] 
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



Wenn der **Komprimierungsmember** BI \_ RLE4 ist, wird die Bitmap mithilfe eines Codierungsformats der Laufzeit für eine 4-Bit-Bitmap komprimiert, die auch codierte und absolute Modi verwendet:

-   Im codierten Modus enthält das erste Byte des Paars die Anzahl der Pixel, die mithilfe der Farbindizes im zweiten Byte gezeichnet werden sollen. Das zweite Byte enthält zwei Farbindizes, einen in seinen 4 Bits in hoher Reihenfolge und einen in seinen niedrigen 4 Bits. Das erste der Pixel wird mit der von den 4 Bits in hoher Reihenfolge angegebenen Farbe gezeichnet, das zweite mithilfe der Farbe in den niedrigen 4 Bits, das dritte mithilfe der Farbe in den 4 Bits in hoher Reihenfolge usw., bis alle durch das erste Byte angegebenen Pixel gezeichnet wurden.
-   Im absoluten Modus ist das erste Byte 0 (null). Das zweite Byte enthält die Anzahl der folgenden Farbindizes. Nachfolgende Bytes enthalten Farbindizes in ihren 4 Bits mit hoher und niedriger Reihenfolge, einen Farbindex für jedes Pixel. Im absoluten Modus muss jede Ausführung an einer Wortgrenze ausgerichtet werden. Die für BI RLE8 beschriebenen Zeilenende-, Bitmapende- und Delta-Escapes \_ gelten auch für die BI \_ RLE4-Komprimierung.

Das folgende Beispiel zeigt die Hexadezimalwerte einer 4-Bit-komprimierten Bitmap:


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



 

 



