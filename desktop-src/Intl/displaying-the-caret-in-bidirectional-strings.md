---
description: In unidirektionalem Text hat die Position der Einfügemarke keine Mehrdeutigkeit, da sich der führende Rand eines Zeichens an derselben Stelle wie der nachfolgende Rand des vorherigen Zeichens befindet.
ms.assetid: 3bebb329-3dd7-4b2e-8ff3-878aaf337a2c
title: Anzeigen des Caretzeichen in bidirektionalen Zeichen folgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76cce95362aa69564fd245ccad1da4a967dddc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352665"
---
# <a name="displaying-the-caret-in-bidirectional-strings"></a>Anzeigen des Caretzeichen in bidirektionalen Zeichen folgen

In unidirektionalem Text hat die Position der Einfügemarke keine Mehrdeutigkeit, da sich der führende Rand eines Zeichens an derselben Stelle wie der nachfolgende Rand des vorherigen Zeichens befindet. In bidirektionalem Text ist die Position der Einfügemarke zwischen den Ausführungen der entgegengesetzten Richtung mehrdeutig. Beispielsweise wird im "hellosalaam"-Absatz von links nach rechts der letzte Buchstabe von "Hello" unmittelbar vor dem ersten Buchstaben von "Salaam" vorangestellt. Die beste Position, an der die Einfügemarke angezeigt wird, hängt davon ab, ob Sie der "o" von "Hello" oder der "s" von "Salaam" vorangestellt ist.

Uniscriverwendet die in der nächsten Tabelle dargestellten Positions Konventionen für Caretzeichen.



| Situation       | Platzierung von visuellen Caretzeichen                       |
|-----------------|----------------------------------------------|
| Eingabe          | Der nachfolgende Rand des letzten Zeichens, das eingegeben wurde.       |
| Einfügen         | Der nachfolgende Rand des letzten eingefügten Zeichens.      |
| Einfügevordringen | Der nachfolgende Rand des letzten Zeichens, das übergeben wurde. |
| Einfügemarke  | Führender Rand des letzten übergebenen Zeichens.  |
| Startseite            | Führender Zeilen Rand.                        |
| Ende             | Der nachfolgende Zeilen Rand.                       |



 

Die Einfügemarke kann wie im folgenden Beispiel gezeigt positioniert werden:


```C++
if (fAdvancing) {
    ScriptCPtoX(
        iCharPos - 1, TRUE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
} else {
    ScriptCPtoX(
        iCharPos, FALSE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
}
```



Die Positionierung der Einfügemarke kann einfacher sein, wie unten gezeigt, wenn ein *fimportwert* auf " **true** " oder " **false**" beschränkt ist:


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



[**Scriptcptox**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) verarbeitet logische Positionen außerhalb des gültigen Bereichs. Er gibt den führenden Rand des Testlaufs für *icharpos* <0 und den nachfolgenden Rand des Testlaufs für *icharpos* >= length zurück. Weitere Informationen finden Sie unter [Verwalten der Platzierung von Caretzeichen und Treffer Tests](managing-caret-placement-and-hit-testing.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von uniscri](using-uniscribe.md)
</dt> </dl>

 

 



