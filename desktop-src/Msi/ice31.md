---
description: ICE31 überprüft alle vordefinierten Schriftart Stile, die in Steuerelementen verwendet werden, die Text anzeigen. Außerdem wird überprüft, ob die defaultuifont-Eigenschaft auf einen gültigen Schrift Schnitt verweist.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d577ceaa2a2b7838f1f03a8577d9a633fb65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216742"
---
# <a name="ice31"></a><span data-ttu-id="e4071-104">ICE31</span><span class="sxs-lookup"><span data-stu-id="e4071-104">ICE31</span></span>

<span data-ttu-id="e4071-105">ICE31 überprüft alle vordefinierten Schriftart Stile, die in Steuer [Elementen](controls.md) verwendet werden, die Text anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e4071-105">ICE31 validates any predefined font styles used in [controls](controls.md) that display text.</span></span> <span data-ttu-id="e4071-106">Außerdem wird überprüft, ob die [**defaultuifont**](defaultuifont.md) -Eigenschaft auf einen gültigen Schrift Schnitt verweist.</span><span class="sxs-lookup"><span data-stu-id="e4071-106">It also validates that the [**DefaultUIFont**](defaultuifont.md) property refers to a valid font style.</span></span>

<span data-ttu-id="e4071-107">Steuerelemente können ein vordefiniertes Schriftformat aufweisen, wie unter [Hinzufügen von Steuerelementen und Text](adding-controls-and-text.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e4071-107">Controls can have a predefined font style as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="e4071-108">Um die Schriftart und den Schrift Schnitt einer Text Zeichenfolge festzulegen, stellen Sie die Zeichenfolge der angezeigten Zeichen mit "{ \\ Style}" oder "{&*Style*}" vor.</span><span class="sxs-lookup"><span data-stu-id="e4071-108">To set the font and font style of a text string, prefix the string of displayed characters with {\\style} or {&*style*}.</span></span> <span data-ttu-id="e4071-109">Dabei ist Style ein Bezeichner, der in der TextStyle-Spalte der [TextStyle-Tabelle](textstyle-table.md)aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="e4071-109">Where style is an identifier listed in the TextStyle column of the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="e4071-110">Wenn keines dieser beiden vorhanden ist, die [**defaultuifont**](defaultuifont.md) -Eigenschaft jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4071-110">If neither of these are present, but the [**DefaultUIFont**](defaultuifont.md) property is defined as a valid text style, that font will be used.</span></span>

<span data-ttu-id="e4071-111">ICE31 überprüft die Text Spalte für jedes Steuerelement in der [Steuerelement Tabelle](control-table.md) , um zu überprüfen, ob ein gültiger Eintrag in der [TextStyle-Tabelle](textstyle-table.md)vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e4071-111">ICE31 checks the Text column for each control in the [Control Table](control-table.md) to verifies that a valid entry exist in the [TextStyle table](textstyle-table.md).</span></span>

<span data-ttu-id="e4071-112">ICE31 ignoriert das [scrollabletext-Steuer](scrollabletext-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="e4071-112">ICE31 ignores the [ScrollableText Control](scrollabletext-control.md).</span></span>

## <a name="results"></a><span data-ttu-id="e4071-113">Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="e4071-113">Results</span></span>

<span data-ttu-id="e4071-114">ICE31 gibt eine Fehlermeldung für nicht definierte Stile, Formatvorlagen Namen, die zu lang sind, eine fehlende TextStyle-Tabelle und stiltags ohne schließende geschweifte Klammer an.</span><span class="sxs-lookup"><span data-stu-id="e4071-114">ICE31 posts an error message for undefined styles, style names that are too long, a missing TextStyle table, and style tags with no closing brace.</span></span>

<span data-ttu-id="e4071-115">ICE31 gibt eine Warnung aus, wenn sich das Stiltag nicht am Anfang der Zeile befindet, oder wenn ein Steuerelement über mehrere Style-Tags verfügt.</span><span class="sxs-lookup"><span data-stu-id="e4071-115">ICE31 posts a warning if the style tag is not at the beginning of the line, or if a control has multiple style tags.</span></span>

## <a name="example"></a><span data-ttu-id="e4071-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e4071-116">Example</span></span>

<span data-ttu-id="e4071-117">ICE31 gibt die folgenden Fehler für das gezeigte Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="e4071-117">ICE31 posts the following errors for the example shown:</span></span>

-   <span data-ttu-id="e4071-118">Steuerelement dialogb. Control1 verwendet nicht definierte TextStyle-badstyle-Elemente.</span><span class="sxs-lookup"><span data-stu-id="e4071-118">Control DialogB.Control1 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="e4071-119">Steuerelement dialogb. Control2 verwendet nicht definierte TextStyle-badstyle-Elemente.</span><span class="sxs-lookup"><span data-stu-id="e4071-119">Control DialogB.Control2 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="e4071-120">Im Steuerelement dialogb. Control6 fehlt die schließende geschweifte Klammer im Textstil.</span><span class="sxs-lookup"><span data-stu-id="e4071-120">Control DialogB.Control6 is missing closing brace in text style.</span></span>
-   <span data-ttu-id="e4071-121">Steuerelement dialogb. Control3 gibt einen Text Stil an, der zu lang ist, um gültig zu sein.</span><span class="sxs-lookup"><span data-stu-id="e4071-121">Control DialogB.Control3 specifies a text style that is too long to be valid.</span></span>

<span data-ttu-id="e4071-122">ICE31 gibt die folgende Warnung für das folgende Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="e4071-122">ICE31 posts the following warning for the example shown:</span></span>

-   <span data-ttu-id="e4071-123">Das textstiltag in dialogb. Control4 hat keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="e4071-123">Text Style tag in DialogB.Control4 has no effect.</span></span> <span data-ttu-id="e4071-124">Möchten Sie, dass Sie als Text angezeigt werden?</span><span class="sxs-lookup"><span data-stu-id="e4071-124">Do you really want it to appear as text?</span></span>

<span data-ttu-id="e4071-125">[Control-Tabelle](control-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="e4071-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="e4071-126">Dialog</span><span class="sxs-lookup"><span data-stu-id="e4071-126">Dialog</span></span>  | <span data-ttu-id="e4071-127">Control</span><span class="sxs-lookup"><span data-stu-id="e4071-127">Control</span></span>  | <span data-ttu-id="e4071-128">Text</span><span class="sxs-lookup"><span data-stu-id="e4071-128">Text</span></span>                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4071-129">Dialoga</span><span class="sxs-lookup"><span data-stu-id="e4071-129">DialogA</span></span> | <span data-ttu-id="e4071-130">Control0</span><span class="sxs-lookup"><span data-stu-id="e4071-130">Control0</span></span> | <span data-ttu-id="e4071-131">{ \\ Okstyle} Dies ist der anzuzeigende Text.</span><span class="sxs-lookup"><span data-stu-id="e4071-131">{\\OKStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="e4071-132">Dialoga</span><span class="sxs-lookup"><span data-stu-id="e4071-132">DialogA</span></span> | <span data-ttu-id="e4071-133">Control1</span><span class="sxs-lookup"><span data-stu-id="e4071-133">Control1</span></span> | <span data-ttu-id="e4071-134">{&okstyle} Dies ist der anzuzeigende Text.</span><span class="sxs-lookup"><span data-stu-id="e4071-134">{&OKStyle}This is the text to display.</span></span>                                                                                                                              |
| <span data-ttu-id="e4071-135">Dialog GB</span><span class="sxs-lookup"><span data-stu-id="e4071-135">DialogB</span></span> | <span data-ttu-id="e4071-136">Control1</span><span class="sxs-lookup"><span data-stu-id="e4071-136">Control1</span></span> | <span data-ttu-id="e4071-137">{&badstyle} Dies ist der anzuzeigende Text.</span><span class="sxs-lookup"><span data-stu-id="e4071-137">{&BadStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="e4071-138">Dialog GB</span><span class="sxs-lookup"><span data-stu-id="e4071-138">DialogB</span></span> | <span data-ttu-id="e4071-139">Control2</span><span class="sxs-lookup"><span data-stu-id="e4071-139">Control2</span></span> | <span data-ttu-id="e4071-140">{ \\ Badstyle} Dies ist der anzuzeigende Text.</span><span class="sxs-lookup"><span data-stu-id="e4071-140">{\\BadStyle}This is the text to display.</span></span>                                                                                                                            |
| <span data-ttu-id="e4071-141">Dialog GB</span><span class="sxs-lookup"><span data-stu-id="e4071-141">DialogB</span></span> | <span data-ttu-id="e4071-142">Control3</span><span class="sxs-lookup"><span data-stu-id="e4071-142">Control3</span></span> | <span data-ttu-id="e4071-143">{&Stil, der mehr als 72 Zeichen hat und daher nicht möglicherweise ein Stil ist, auch wenn Sie es irgendwie geschafft haben, ihn in der TextStyle-Tabelle zu erhalten} Dies ist der anzuzeigende Text.</span><span class="sxs-lookup"><span data-stu-id="e4071-143">{&Style that is over 72 chars and therefore cannot possibly be a style even if somehow you did manage to get it in the TextStyle table}This is the text to display.</span></span> |
| <span data-ttu-id="e4071-144">Dialog GB</span><span class="sxs-lookup"><span data-stu-id="e4071-144">DialogB</span></span> | <span data-ttu-id="e4071-145">Control4</span><span class="sxs-lookup"><span data-stu-id="e4071-145">Control4</span></span> | <span data-ttu-id="e4071-146">Warnung { \\ okstyle} Dies ist der anzuzeigende Text.</span><span class="sxs-lookup"><span data-stu-id="e4071-146">Warning {\\OKStyle}This is the text to display.</span></span>                                                                                                                     |
| <span data-ttu-id="e4071-147">Dialog GB</span><span class="sxs-lookup"><span data-stu-id="e4071-147">DialogB</span></span> | <span data-ttu-id="e4071-148">Control5</span><span class="sxs-lookup"><span data-stu-id="e4071-148">Control5</span></span> | <span data-ttu-id="e4071-149">{ \\ Okstyle} {&okstyle}. Dies ist der anzuzeigende Text.</span><span class="sxs-lookup"><span data-stu-id="e4071-149">{\\OKStyle}{&OKStyle}This is the text to display.</span></span>                                                                                                                   |
| <span data-ttu-id="e4071-150">Dialog GB</span><span class="sxs-lookup"><span data-stu-id="e4071-150">DialogB</span></span> | <span data-ttu-id="e4071-151">Control6</span><span class="sxs-lookup"><span data-stu-id="e4071-151">Control6</span></span> | <span data-ttu-id="e4071-152">{ \\ Okstyle Dies ist der anzuzeigende Text.</span><span class="sxs-lookup"><span data-stu-id="e4071-152">{\\OKStyle This is the text to display.</span></span>                                                                                                                             |



 

<span data-ttu-id="e4071-153">[TextStyle-Tabelle](textstyle-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="e4071-153">[TextStyle table](textstyle-table.md) (partial)</span></span>



| <span data-ttu-id="e4071-154">Textart</span><span class="sxs-lookup"><span data-stu-id="e4071-154">TextStyle</span></span> |
|-----------|
| <span data-ttu-id="e4071-155">Okstyle</span><span class="sxs-lookup"><span data-stu-id="e4071-155">OkStyle</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="e4071-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4071-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4071-157">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="e4071-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



