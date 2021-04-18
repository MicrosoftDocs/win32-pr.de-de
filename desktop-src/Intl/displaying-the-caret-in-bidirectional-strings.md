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
# <a name="displaying-the-caret-in-bidirectional-strings"></a><span data-ttu-id="59e22-103">Anzeigen des Caretzeichen in bidirektionalen Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="59e22-103">Displaying the Caret in Bidirectional Strings</span></span>

<span data-ttu-id="59e22-104">In unidirektionalem Text hat die Position der Einfügemarke keine Mehrdeutigkeit, da sich der führende Rand eines Zeichens an derselben Stelle wie der nachfolgende Rand des vorherigen Zeichens befindet.</span><span class="sxs-lookup"><span data-stu-id="59e22-104">In unidirectional text, the caret position has no ambiguity because the leading edge of a character is at the same place as the trailing edge of the previous character.</span></span> <span data-ttu-id="59e22-105">In bidirektionalem Text ist die Position der Einfügemarke zwischen den Ausführungen der entgegengesetzten Richtung mehrdeutig.</span><span class="sxs-lookup"><span data-stu-id="59e22-105">However, in bidirectional text, the caret position between runs of opposing direction is ambiguous.</span></span> <span data-ttu-id="59e22-106">Beispielsweise wird im "hellosalaam"-Absatz von links nach rechts der letzte Buchstabe von "Hello" unmittelbar vor dem ersten Buchstaben von "Salaam" vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="59e22-106">For example, in the left-to-right paragraph "hellosalaam", the last letter of "hello" immediately precedes the first letter of "salaam".</span></span> <span data-ttu-id="59e22-107">Die beste Position, an der die Einfügemarke angezeigt wird, hängt davon ab, ob Sie der "o" von "Hello" oder der "s" von "Salaam" vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="59e22-107">The best position in which to display the caret depends on whether it is considered to follow the "o" of "hello" or to precede the "s" of "salaam".</span></span>

<span data-ttu-id="59e22-108">Uniscriverwendet die in der nächsten Tabelle dargestellten Positions Konventionen für Caretzeichen.</span><span class="sxs-lookup"><span data-stu-id="59e22-108">Uniscribe uses the caret positioning conventions shown in the next table.</span></span>



| <span data-ttu-id="59e22-109">Situation</span><span class="sxs-lookup"><span data-stu-id="59e22-109">Situation</span></span>       | <span data-ttu-id="59e22-110">Platzierung von visuellen Caretzeichen</span><span class="sxs-lookup"><span data-stu-id="59e22-110">Visual caret placement</span></span>                       |
|-----------------|----------------------------------------------|
| <span data-ttu-id="59e22-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59e22-111">Typing</span></span>          | <span data-ttu-id="59e22-112">Der nachfolgende Rand des letzten Zeichens, das eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="59e22-112">Trailing edge of last character typed.</span></span>       |
| <span data-ttu-id="59e22-113">Einfügen</span><span class="sxs-lookup"><span data-stu-id="59e22-113">Pasting</span></span>         | <span data-ttu-id="59e22-114">Der nachfolgende Rand des letzten eingefügten Zeichens.</span><span class="sxs-lookup"><span data-stu-id="59e22-114">Trailing edge of last character pasted.</span></span>      |
| <span data-ttu-id="59e22-115">Einfügevordringen</span><span class="sxs-lookup"><span data-stu-id="59e22-115">Caret advancing</span></span> | <span data-ttu-id="59e22-116">Der nachfolgende Rand des letzten Zeichens, das übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="59e22-116">Trailing edge of last character passed over.</span></span> |
| <span data-ttu-id="59e22-117">Einfügemarke</span><span class="sxs-lookup"><span data-stu-id="59e22-117">Caret retiring</span></span>  | <span data-ttu-id="59e22-118">Führender Rand des letzten übergebenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="59e22-118">Leading edge of last character passed over.</span></span>  |
| <span data-ttu-id="59e22-119">Startseite</span><span class="sxs-lookup"><span data-stu-id="59e22-119">Home</span></span>            | <span data-ttu-id="59e22-120">Führender Zeilen Rand.</span><span class="sxs-lookup"><span data-stu-id="59e22-120">Leading edge of line.</span></span>                        |
| <span data-ttu-id="59e22-121">Ende</span><span class="sxs-lookup"><span data-stu-id="59e22-121">End</span></span>             | <span data-ttu-id="59e22-122">Der nachfolgende Zeilen Rand.</span><span class="sxs-lookup"><span data-stu-id="59e22-122">Trailing edge of line.</span></span>                       |



 

<span data-ttu-id="59e22-123">Die Einfügemarke kann wie im folgenden Beispiel gezeigt positioniert werden:</span><span class="sxs-lookup"><span data-stu-id="59e22-123">The caret can be positioned as shown in the following example:</span></span>


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



<span data-ttu-id="59e22-124">Die Positionierung der Einfügemarke kann einfacher sein, wie unten gezeigt, wenn ein *fimportwert* auf " **true** " oder " **false**" beschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="59e22-124">Positioning of the caret can be simpler, as shown below, given an *fAdvancing* value restricted to **TRUE** or **FALSE**:</span></span>


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



<span data-ttu-id="59e22-125">[**Scriptcptox**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) verarbeitet logische Positionen außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="59e22-125">[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) handles out-of-range positions logically.</span></span> <span data-ttu-id="59e22-126">Er gibt den führenden Rand des Testlaufs für *icharpos* <0 und den nachfolgenden Rand des Testlaufs für *icharpos* >= length zurück.</span><span class="sxs-lookup"><span data-stu-id="59e22-126">It returns the leading edge of the run for *iCharPos* <0, and the trailing edge of the run for *iCharPos* >= length.</span></span> <span data-ttu-id="59e22-127">Weitere Informationen finden Sie unter [Verwalten der Platzierung von Caretzeichen und Treffer Tests](managing-caret-placement-and-hit-testing.md) .</span><span class="sxs-lookup"><span data-stu-id="59e22-127">For more information, see [Managing Caret Placement and Hit Testing](managing-caret-placement-and-hit-testing.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="59e22-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59e22-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59e22-129">Verwenden von uniscri</span><span class="sxs-lookup"><span data-stu-id="59e22-129">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



