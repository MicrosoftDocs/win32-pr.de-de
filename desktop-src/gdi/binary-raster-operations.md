---
description: In diesem Abschnitt werden die binären Raster Vorgangs Codes aufgelistet, die von den GetROP2-und SetROP2-Funktionen verwendet werden. Raster-Vorgangs Codes definieren, wie GDI die Bits aus dem ausgewählten Stift mit den Bits in der Ziel Bitmap kombiniert.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Binäre Raster Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8a70030b1940c31d036505a80a6b1868aececd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130856"
---
# <a name="binary-raster-operations"></a>Binäre Raster Vorgänge

In diesem Abschnitt werden die binären Raster Vorgangs Codes aufgelistet, die von den [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) -und [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) -Funktionen verwendet werden. Raster-Vorgangs Codes definieren, wie GDI die Bits aus dem ausgewählten Stift mit den Bits in der Ziel Bitmap kombiniert.

Jeder Raster Vorgangs Code stellt einen booleschen Vorgang dar, in dem die Werte der Pixel im ausgewählten Stift und die Ziel Bitmap kombiniert werden. Die folgenden beiden Operanden werden in diesen Vorgängen verwendet.



| Operand | Bedeutung            |
|---------|--------------------|
| P       | Ausgewählter Stift       |
| D       | Ziel Bitmap |



 

Die in diesen Vorgängen verwendeten booleschen Operatoren folgen.



| Operator | Bedeutung                    |
|----------|----------------------------|
| a        | Bitweises AND                |
| n        | Bitweises NOT (inversen)      |
| o        | Bitweises OR                 |
| x        | Bitweises exklusives OR (XOR) |



 

Alle booleschen Vorgänge werden in umgekehrter polnischer Schreibweise dargestellt. Der folgende Vorgang ersetzt z. b. die Werte der Pixel in der Ziel Bitmap durch eine Kombination der Pixelwerte des Stifts und des ausgewählten Pinsels:


```C++
DPo 
```



Jeder Raster Vorgangs Code ist eine 32-Bit-Ganzzahl, deren hohes Wort ein boolescher Vorgangs Index ist und dessen niedriges Wort der Vorgangs Code ist. Bei dem 16-Bit-Vorgangs Index handelt es sich um einen 8-Bit-Wert mit 0 (null), der alle möglichen Ergebnisse darstellt, die sich aus der booleschen Operation für zwei Parameter ergeben (in diesem Fall der Stift-und Zielwert). Die Vorgangs Indizes für die DPO-und DPAN-Vorgänge werden z. b. in der folgenden Liste angezeigt.



| P   | D   | DPO | DPAN |
|-----|-----|-----|------|
| 0   | 0   | 0   | 1    |
| 0   | 1   | 1   | 1    |
| 1   | 0   | 1   | 1    |
| 1   | 1   | 1   | 0    |



 

In der folgenden Liste werden die Zeichnungs Modi und die booleschen Operationen beschrieben, die Sie darstellen.



| Raster Vorgang | Boolescher Vorgang |
|------------------|-------------------|
| R2 \_ schwarz        | 0                 |
| R2- \_ CopyPen      | P                 |
| R2 \_ masklotpen   | DPNA              |
| R2- \_ MaskPen      | DPa               |
| R2 \_ maskpnot   | Pdna              |
| R2 \_ mergenotpen  | Dpno              |
| R2- \_ MergePen     | DPO               |
| R2 \_ mergepnot  | Pdno              |
| R2 \_ NOP          | D                 |
| R2 \_ nicht          | Dn                |
| R2- \_ notcopypen   | PN                |
| R2 \_ notmaskpen   | DPAN              |
| R2 \_ NotMergePen  | Dpon              |
| R2- \_ NotXorPen    | Dpxn              |
| R2 \_ weiß        | 1                 |
| R2- \_ XOrPen       | DPX               |



 

Bei einem monochrome Gerät ordnet GDI den Wert 0 (null) und den Wert 1 weiß zu. Wenn eine Anwendung versucht, mit einem schwarzen Stift auf einem weißen Ziel mithilfe der verfügbaren binären Raster Vorgänge zu zeichnen, treten die folgenden Ergebnisse auf.



| Raster Vorgang | Ergebnis             |
|------------------|--------------------|
| R2 \_ schwarz        | Sichtbare schwarze Linie |
| R2- \_ CopyPen      | Sichtbare schwarze Linie |
| R2 \_ masklotpen   | Keine sichtbare Zeile    |
| R2- \_ MaskPen      | Sichtbare schwarze Linie |
| R2 \_ maskpnot   | Sichtbare schwarze Linie |
| R2 \_ mergenotpen  | Keine sichtbare Zeile    |
| R2- \_ MergePen     | Sichtbare schwarze Linie |
| R2 \_ mergepnot  | Sichtbare schwarze Linie |
| R2 \_ NOP          | Keine sichtbare Zeile    |
| R2 \_ nicht          | Sichtbare schwarze Linie |
| R2- \_ notcopypen   | Keine sichtbare Zeile    |
| R2 \_ notmaskpen   | Keine sichtbare Zeile    |
| R2 \_ NotMergePen  | Sichtbare schwarze Linie |
| R2- \_ NotXorPen    | Sichtbare schwarze Linie |
| R2 \_ weiß        | Keine sichtbare Zeile    |
| R2- \_ XOrPen       | Keine sichtbare Zeile    |



 

Bei einem Farbgerät verwendet GDI RGB-Werte, um die Farben des Stifts und des Ziels darzustellen. Ein RGB-Farbwert ist eine lange ganze Zahl, die ein rotes, grünes und blaues Farbfeld enthält, das jeweils die Intensität der angegebenen Farbe angibt. Die Intensitäten liegen zwischen 0 und 255. Die Werte werden in die drei nieder wertigen Bytes der Long-Ganzzahl gepackt. Die Farbe eines Stifts ist immer eine voll Tonfarbe, aber die Farbe des Ziels kann eine Mischung aus zwei oder drei Farben sein. Wenn eine Anwendung versucht, mit einem weißen Stift auf einem blauen Ziel mithilfe der verfügbaren binären Raster Vorgänge zu zeichnen, treten die folgenden Ergebnisse auf.



| Raster Vorgang | Ergebnis                 |
|------------------|------------------------|
| R2 \_ schwarz        | Sichtbare schwarze Linie     |
| R2- \_ CopyPen      | Sichtbare weiße Linie     |
| R2 \_ masklotpen   | Sichtbare schwarze Linie     |
| R2- \_ MaskPen      | Unsichtbare blaue Linie    |
| R2 \_ maskpnot   | Sichtbare rote/grüne Linie |
| R2 \_ mergenotpen  | Unsichtbare blaue Linie    |
| R2- \_ MergePen     | Sichtbare weiße Linie     |
| R2 \_ mergepnot  | Sichtbare weiße Linie     |
| R2 \_ NOP          | Unsichtbare blaue Linie    |
| R2 \_ nicht          | Sichtbare rote/grüne Linie |
| R2- \_ notcopypen   | Sichtbare schwarze Linie     |
| R2 \_ notmaskpen   | Sichtbare rote/grüne Linie |
| R2 \_ NotMergePen  | Sichtbare schwarze Linie     |
| R2- \_ NotXorPen    | Unsichtbare blaue Linie    |
| R2 \_ weiß        | Sichtbare weiße Linie     |
| R2- \_ XOrPen       | Sichtbare rote/grüne Linie |



 

 

 



