---
description: Bei einem komplexen Skript handelt es sich um ein Skript, für das der fcomplex-Member der Skript \_ Eigenschaften auf true festgelegt ist. In diesem Thema werden die Eigenschaften erläutert, die möglicherweise in einem komplexen Skript vorhanden sind.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: Informationen zu komplexen Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb1929a58e7810fb51bcb2b7a6bf9d5a762282e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042545"
---
# <a name="about-complex-scripts"></a><span data-ttu-id="c31d3-104">Informationen zu komplexen Skripts</span><span class="sxs-lookup"><span data-stu-id="c31d3-104">About Complex Scripts</span></span>

<span data-ttu-id="c31d3-105">Bei einem [komplexen Skript](uniscribe-glossary.md) handelt es sich um ein Skript, für das der **fcomplex** -Member der [**Skript \_ Eigenschaften**](/windows/desktop/api/Usp10/ns-usp10-script_properties) auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c31d3-105">A [complex script](uniscribe-glossary.md) is a script for which the **fComplex** member of [**SCRIPT\_PROPERTIES**](/windows/desktop/api/Usp10/ns-usp10-script_properties) is set to **TRUE**.</span></span> <span data-ttu-id="c31d3-106">In diesem Thema werden die Eigenschaften erläutert, die möglicherweise in einem komplexen Skript vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c31d3-106">This topic details the properties that a complex script might have.</span></span>

## <a name="bidirectional-rendering"></a><span data-ttu-id="c31d3-107">Bidirektionales Rendering</span><span class="sxs-lookup"><span data-stu-id="c31d3-107">Bidirectional Rendering</span></span>

<span data-ttu-id="c31d3-108">Bidirektionales Rendering ist die Behandlung von Text, der sowohl von links nach rechts und von rechts nach links liest.</span><span class="sxs-lookup"><span data-stu-id="c31d3-108">Bidirectional rendering is handling of text that reads both left-to-right and right-to-left.</span></span> <span data-ttu-id="c31d3-109">Bei der bidirektionalen Darstellung von Arabisch ist die Standard Leserichtung für Text z. b. von rechts nach links, aber für einige Zahlen von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="c31d3-109">For example, in the bidirectional rendering of Arabic, the default reading direction for text is right-to-left, but it is left-to-right for some numbers.</span></span> <span data-ttu-id="c31d3-110">Die Verarbeitung eines komplexen Skripts muss den Unterschied zwischen der logischen Reihenfolge (Keystroke) und der visuellen Reihenfolge der Symbole berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="c31d3-110">Processing a complex script must account for the difference between the logical (keystroke) order and the visual order of the glyphs.</span></span> <span data-ttu-id="c31d3-111">Außerdem muss bei der Verarbeitung der Caretzeichen und Treffer Tests ordnungsgemäß behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="c31d3-111">In addition, processing must properly deal with caret movement and hit testing.</span></span> <span data-ttu-id="c31d3-112">Die Zuordnung zwischen Bildschirmposition und Zeichen Index erfordert ein Verständnis der Layoutalgorithmen für die jeweilige Anzeige, z. b. die Auswahl von Text-oder Caretzeichen.</span><span class="sxs-lookup"><span data-stu-id="c31d3-112">The mapping between screen position and a character index requires an understanding of the layout algorithms for the particular display, for example, selection of text or caret display.</span></span>

## <a name="contextual-shaping"></a><span data-ttu-id="c31d3-113">Kontextabhängige Strukturierung</span><span class="sxs-lookup"><span data-stu-id="c31d3-113">Contextual Shaping</span></span>

<span data-ttu-id="c31d3-114">In der kontextbezogenen Strukturierung ändern Skript Zeichen die Form abhängig von den Zeichen, die Sie umschließen.</span><span class="sxs-lookup"><span data-stu-id="c31d3-114">In contextual shaping, script characters change shape depending on the characters that surround them.</span></span> <span data-ttu-id="c31d3-115">Eine solche Strukturierung findet in einem englischen, kursiven schreiben statt, wenn eine Form vom Typ "l" vom Typ "l" abhängig von dem vorangestellenden Zeichen geändert wird, z. b. "a" (mit niedriger Verbindung mit "l") oder "o" (mit hoher Verbindung).</span><span class="sxs-lookup"><span data-stu-id="c31d3-115">Such shaping occurs in English cursive writing when a lowercase "l" changes shape depending on the character that precedes it, such as an "a" (connects low to the "l") or an "o" (connects high).</span></span> <span data-ttu-id="c31d3-116">Arabisch ist beispielsweise ein Skript, das die Kontext Bildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c31d3-116">For example, Arabic is a script that exhibits contextual shaping.</span></span>

## <a name="combining-characters"></a><span data-ttu-id="c31d3-117">Kombinieren von Zeichen</span><span class="sxs-lookup"><span data-stu-id="c31d3-117">Combining Characters</span></span>

<span data-ttu-id="c31d3-118">Das Kombinieren von Zeichen, auch als "Ligaturen" bezeichnet, sind Zeichen, die beim Platzieren in ein Zeichen eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="c31d3-118">Combining characters, also called "ligatures," are characters that join into one character when placed together.</span></span> <span data-ttu-id="c31d3-119">Arabisch ist ein Skript, das viele kombinierte Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="c31d3-119">Arabic is a script that has many combining characters.</span></span> <span data-ttu-id="c31d3-120">Ein Beispiel für die Kombination von Zeichen ist "a", gefolgt von "Kombinieren von Grab", bei dem die gerenderte Darstellung "a" ist.</span><span class="sxs-lookup"><span data-stu-id="c31d3-120">One example of the use of combining characters is the "a" followed by "combining grave", for which the rendered representation is "à".</span></span> <span data-ttu-id="c31d3-121">Der Unicode-Stream "U + 0061 U + 0300" erfordert einige Verarbeitungsschritte, um sicherzustellen, dass das "kombinierte Grab" ordnungsgemäß über "a" positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="c31d3-121">The Unicode stream "U+0061 U+0300" requires some processing to make sure the "combining grave" is correctly positioned above the "a".</span></span>

## <a name="specialized-word-break-and-justification"></a><span data-ttu-id="c31d3-122">Spezialisierte Wort Umbruch und-Begründung</span><span class="sxs-lookup"><span data-stu-id="c31d3-122">Specialized Word Break and Justification</span></span>

<span data-ttu-id="c31d3-123">Einige Skripts, z. b. Thai, haben komplexe Regeln für das Aufteilen von Wörtern zwischen Zeilen oder das rechtfertigen von Text in einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="c31d3-123">Some scripts, for example, Thai, have complex rules for dividing words between lines or justifying text on a line.</span></span>

## <a name="filtering-for-illegal-character-combinations"></a><span data-ttu-id="c31d3-124">Filtern nach unzulässigen Zeichenkombinationen</span><span class="sxs-lookup"><span data-stu-id="c31d3-124">Filtering for Illegal Character Combinations</span></span>

<span data-ttu-id="c31d3-125">Ein komplexes Skript, z. b. Thai, kann unzulässige Zeichenkombinationen herausfiltern, wenn eine Sprache bestimmte Zeichenkombinationen nicht zulässt.</span><span class="sxs-lookup"><span data-stu-id="c31d3-125">A complex script, for example, Thai, can filter out illegal character combinations when a language does not allow certain character combinations.</span></span>

## <a name="font-fallback"></a><span data-ttu-id="c31d3-126">Schriftart-Fallback</span><span class="sxs-lookup"><span data-stu-id="c31d3-126">Font Fallback</span></span>

<span data-ttu-id="c31d3-127">Bei einem Schriftart Fall Back handelt es sich um die automatisierte Auswahl einer anderen Schriftart als der vom Benutzer ausgewählten Schriftart.</span><span class="sxs-lookup"><span data-stu-id="c31d3-127">Font fallback is the automated selection of a font other than the font selected by the user.</span></span> <span data-ttu-id="c31d3-128">In uniwriter wird das Schriftart-Fall Back von der [**scriptstringanalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) -Funktion angewendet, wenn sich der gesamte Text oder ein Teil des Texts in einem Skript befindet, das von der vom Benutzer ausgewählten Schriftart nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c31d3-128">In Uniscribe, font fallback is applied by the [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) function when all or part of the text is in a script that the user-selected font does not support.</span></span> <span data-ttu-id="c31d3-129">Weitere Informationen finden Sie unter [using Font Fallback](using-font-fallback.md).</span><span class="sxs-lookup"><span data-stu-id="c31d3-129">For more information, see [Using Font Fallback](using-font-fallback.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c31d3-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c31d3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c31d3-131">Informationen zu uniscri</span><span class="sxs-lookup"><span data-stu-id="c31d3-131">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 



