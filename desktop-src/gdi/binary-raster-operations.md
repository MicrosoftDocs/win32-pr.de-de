---
description: In diesem Abschnitt werden die binären Rastervorgangscodes aufgelistet, die von den Funktionen GetROP2 und SetROP2 verwendet werden. Rasteroperationscodes definieren, wie GDI die Bits aus dem ausgewählten Stift mit den Bits in der Zielbitmap kombiniert.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Binäre Rastervorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462c07165d7f377f2a536722bf2f728446c308503108474cbb6a585cee6f68e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105809"
---
# <a name="binary-raster-operations"></a>Binäre Rastervorgänge

In diesem Abschnitt werden die binären Rastervorgangscodes aufgelistet, die von den Funktionen [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) und [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) verwendet werden. Rasteroperationscodes definieren, wie GDI die Bits aus dem ausgewählten Stift mit den Bits in der Zielbitmap kombiniert.

Jeder Rastervorgangscode stellt einen booleschen Vorgang dar, bei dem die Werte der Pixel im ausgewählten Stift und der Zielbitmap kombiniert werden. Im Folgenden sind die beiden Operanden, die in diesen Vorgängen verwendet werden.



| Operand | Bedeutung            |
|---------|--------------------|
| P       | Ausgewählter Stift       |
| D       | Zielbitmap |



 

Die booleschen Operatoren, die in diesen Vorgängen verwendet werden, folgen.



| Operator | Bedeutung                    |
|----------|----------------------------|
| a        | Bitweises AND                |
| n        | Bitweises NOT (umgekehrt)      |
| o        | Bitweises OR                 |
| x        | Bitweises exklusives OR (XOR) |



 

Alle booleschen Vorgänge werden in umgekehrter polnischer Notation dargestellt. Der folgende Vorgang ersetzt beispielsweise die Werte der Pixel in der Zielbitmap durch eine Kombination der Pixelwerte des Stifts und des ausgewählten Pinsels:


```C++
DPo 
```



Jeder Rastervorgangscode ist eine 32-Bit-Ganzzahl, deren Wort in hoher Reihenfolge ein boolescher Vorgangsindex ist und dessen Wort mit niedriger Reihenfolge der Vorgangscode ist. Der 16-Bit-Vorgangsindex ist ein null erweiterter 8-Bit-Wert, der alle möglichen Ergebnisse darstellt, die sich aus der booleschen Operation für zwei Parameter ergeben (in diesem Fall der Stift und die Zielwerte). Beispielsweise werden die Vorgangsindizes für die DPo- und DPan-Vorgänge in der folgenden Liste angezeigt.



| P   | D   | Dsb | Dpan |
|-----|-----|-----|------|
| 0   | 0   | 0   | 1    |
| 0   | 1   | 1   | 1    |
| 1   | 0   | 1   | 1    |
| 1   | 1   | 1   | 0    |



 

In der folgenden Liste werden die Zeichnungsmodi und die booleschen Vorgänge beschrieben, die sie darstellen.



| Rastervorgang | Boolescher Vorgang |
|------------------|-------------------|
| R2 \_ BLACK        | 0                 |
| R2 \_ COPYPEN      | P                 |
| R2 \_ MASKNOTPEN   | DPna              |
| R2 \_ MASKPEN      | Dpa               |
| R2 \_ MASKPENNOT   | PDna              |
| R2 \_ MERGENOTPEN  | DPno              |
| R2 \_ MERGEPEN     | Dsb               |
| R2 \_ MERGEPENNOT  | PDno              |
| R2 \_ NOP          | D                 |
| R2 \_ NOT          | Dn                |
| R2 \_ NOTCOPYPEN   | Pn                |
| R2 \_ NOTMASKPEN   | DPan              |
| R2 \_ NOTMERGEPEN  | DPon              |
| R2 \_ NOTXORPEN    | DPxn              |
| R2 \_ WHITE        | 1                 |
| R2 \_ XORPEN       | Dpx               |



 

Für ein monocolores Gerät ordnet GDI den Wert 0 (null) schwarz und den Wert 1 weiß zu. Wenn eine Anwendung versucht, mit einem schwarzen Stift auf einem weißen Ziel mithilfe der verfügbaren binären Rastervorgänge zu zeichnen, treten die folgenden Ergebnisse auf.



| Rastervorgang | Ergebnis             |
|------------------|--------------------|
| R2 \_ BLACK        | Sichtbare schwarze Linie |
| R2 \_ COPYPEN      | Sichtbare schwarze Linie |
| R2 \_ MASKNOTPEN   | Keine sichtbare Zeile    |
| R2 \_ MASKPEN      | Sichtbare schwarze Linie |
| R2 \_ MASKPENNOT   | Sichtbare schwarze Linie |
| R2 \_ MERGENOTPEN  | Keine sichtbare Zeile    |
| R2 \_ MERGEPEN     | Sichtbare schwarze Linie |
| R2 \_ MERGEPENNOT  | Sichtbare schwarze Linie |
| R2 \_ NOP          | Keine sichtbare Zeile    |
| R2 \_ NOT          | Sichtbare schwarze Linie |
| R2 \_ NOTCOPYPEN   | Keine sichtbare Zeile    |
| R2 \_ NOTMASKPEN   | Keine sichtbare Zeile    |
| R2 \_ NOTMERGEPEN  | Sichtbare schwarze Linie |
| R2 \_ NOTXORPEN    | Sichtbare schwarze Linie |
| R2 \_ WHITE        | Keine sichtbare Zeile    |
| R2 \_ XORPEN       | Keine sichtbare Zeile    |



 

Für ein Farbgerät verwendet GDI RGB-Werte, um die Farben des Stifts und des Ziels darzustellen. Ein RGB-Farbwert ist eine lange ganze Zahl, die ein rotes, ein grünes und ein blaues Farbfeld enthält, die jeweils die Intensität der angegebenen Farbe angeben. Die Intensitäten reichen von 0 bis 255. Die Werte werden in die drei Bytes der langen ganzen Zahl in niedriger Reihenfolge gepackt. Die Farbe eines Stifts ist immer eine Volltonfarbe, aber die Farbe des Ziels kann eine Mischung aus zwei oder drei Farben sein. Wenn eine Anwendung versucht, mit einem weißen Stift auf einem blauen Ziel mithilfe der verfügbaren binären Rastervorgänge zu zeichnen, treten die folgenden Ergebnisse auf.



| Rastervorgang | Ergebnis                 |
|------------------|------------------------|
| R2 \_ BLACK        | Sichtbare schwarze Linie     |
| R2 \_ COPYPEN      | Sichtbare weiße Linie     |
| R2 \_ MASKNOTPEN   | Sichtbare schwarze Linie     |
| R2 \_ MASKPEN      | Unsichtbare blaue Linie    |
| R2 \_ MASKPENNOT   | Sichtbare rote/grüne Linie |
| R2 \_ MERGENOTPEN  | Unsichtbare blaue Linie    |
| R2 \_ MERGEPEN     | Sichtbare weiße Linie     |
| R2 \_ MERGEPENNOT  | Sichtbare weiße Linie     |
| R2 \_ NOP          | Unsichtbare blaue Linie    |
| R2 \_ NOT          | Sichtbare rote/grüne Linie |
| R2 \_ NOTCOPYPEN   | Sichtbare schwarze Linie     |
| R2 \_ NOTMASKPEN   | Sichtbare rote/grüne Linie |
| R2 \_ NOTMERGEPEN  | Sichtbare schwarze Linie     |
| R2 \_ NOTXORPEN    | Unsichtbare blaue Linie    |
| R2 \_ WHITE        | Sichtbare weiße Linie     |
| R2 \_ XORPEN       | Sichtbare rote/grüne Linie |



 

 

 



