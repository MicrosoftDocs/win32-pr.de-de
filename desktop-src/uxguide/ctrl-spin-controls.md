---
title: Dreh Steuerelemente
description: Mit einem Drehfeld-Steuerelement können Benutzer auf Pfeil Schaltflächen klicken, um den Wert inkrementell im zugeordneten numerischen Textfeld zu ändern.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 54ce622983e52d65fa58ef05aca783ff67ebce66
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351099"
---
# <a name="spin-controls"></a><span data-ttu-id="7c3a9-103">Dreh Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="7c3a9-103">Spin Controls</span></span>

> [!NOTE]
> <span data-ttu-id="7c3a9-104">Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="7c3a9-105">Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="7c3a9-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="7c3a9-106">Mit einem Drehfeld-Steuerelement können Benutzer auf Pfeil Schaltflächen klicken, um den Wert inkrementell im zugeordneten [numerischen Textfeld](ctrl-text-boxes.md)zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-106">With a spin control, users can click arrow buttons to change incrementally the value within its associated [numeric text box](ctrl-text-boxes.md).</span></span> <span data-ttu-id="7c3a9-107">Der Begriff Drehfeld bezieht sich auf die Kombination aus einem Textfeld und dem zugehörigen Drehfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-107">The term spin box refers to the combination of a text box and its associated spin control.</span></span>

![<span data-ttu-id="7c3a9-108">Screenshot des Drehfeld-Steuer Elements und Textfelds</span><span class="sxs-lookup"><span data-stu-id="7c3a9-108">screen shot of spin control and text box</span></span> ](images/ctrl-spin-controls-image1.png)

<span data-ttu-id="7c3a9-109">Ein typisches Drehfeld.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-109">A typical spin box.</span></span>

<span data-ttu-id="7c3a9-110">Benutzer bevorzugen häufig Dreh Steuerelemente, da Sie Änderungen vornehmen können, ohne Ihre Hände von der Maus zu bewegen.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-110">Users often prefer spin controls because they can make changes without moving their hands from the mouse.</span></span> <span data-ttu-id="7c3a9-111">Wenn das Drehfeld Steuerelement mit einem Textfeld gekoppelt ist, können Benutzereingaben direkt in das Textfeld eingeben oder einfügen, sodass die Verwendung des Drehungs Steuer Elements optional ist.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-111">When the spin control is paired with a text box, users can type or paste input directly in the text box, so use of the spin control is optional.</span></span>

<span data-ttu-id="7c3a9-112">Während Dreh Steuerelemente für numerische Eingaben verwendet werden, muss die Eingabe keine reine ganze Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-112">While spin controls are used for numeric input, the input doesn't have to be a pure whole number.</span></span> <span data-ttu-id="7c3a9-113">Die Eingabe kann Dezimalzahlen sein und kann negative Vorzeichen, Trennzeichen (z. b. Doppelpunkte oder Bindestriche) und Einheits Modifizierer aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-113">The input can be decimal numbers and it can have negative signs, delimiters (such as colons or hyphens), and unit modifiers.</span></span>

> [!Note]  
> <span data-ttu-id="7c3a9-114">Richtlinien, die sich auf [Textfelder](ctrl-text-boxes.md) und [Layout](vis-layout.md) beziehen, werden in separaten Artikeln dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-114">Guidelines related to [text boxes](ctrl-text-boxes.md) and [layout](vis-layout.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="7c3a9-115">Ist dies das richtige Steuerelement?</span><span class="sxs-lookup"><span data-stu-id="7c3a9-115">Is this the right control?</span></span>

<span data-ttu-id="7c3a9-116">Orientieren Sie sich an folgenden Fragen:</span><span class="sxs-lookup"><span data-stu-id="7c3a9-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="7c3a9-117">**Wird das Steuerelement für numerische Eingaben verwendet?**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-117">**Is the control used for numeric input?**</span></span> <span data-ttu-id="7c3a9-118">Wenn dies nicht der Fall ist, verwenden Sie ein anderes Steuerelement, z. b. eine [Dropdown Liste](/windows/desktop/uxguide/ctrl-drop) oder einen [Schieberegler](ctrl-sliders.md), um einen festgelegten Satz von Werten auszuwählen</span><span class="sxs-lookup"><span data-stu-id="7c3a9-118">If not, use another control, such as a [drop-down list](/windows/desktop/uxguide/ctrl-drop) or [slider](ctrl-sliders.md), to select from a fixed set of values.</span></span> <span data-ttu-id="7c3a9-119">Verwenden Sie Scrollleisten für den Bildlauf.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-119">Use scroll bars for scrolling.</span></span>
-   <span data-ttu-id="7c3a9-120">**Betrachten die Benutzer den Wert als relative Menge, nicht als numerischen Wert?**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-120">**Do users think of the value as a relative quantity, not a numeric value?**</span></span> <span data-ttu-id="7c3a9-121">Wenn ja, verwenden Sie stattdessen einen Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-121">If so, use a slider instead.</span></span> <span data-ttu-id="7c3a9-122">Verwenden Sie Drehfelder nur für exakte, bekannte numerische Werte.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-122">Use spin boxes only for exact, known numeric values.</span></span> <span data-ttu-id="7c3a9-123">So denken Benutzer beispielsweise beim Festlegen der Audiolautstärke an "niedrig" oder "mittel", aber nicht an Werte wie "2" oder "5".</span><span class="sxs-lookup"><span data-stu-id="7c3a9-123">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>
-   <span data-ttu-id="7c3a9-124">**Ist das Steuerelement mit einem Textfeld gekoppelt?**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-124">**Is the control paired with a text box?**</span></span> <span data-ttu-id="7c3a9-125">Wenn nicht, verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-125">If not, don't use.</span></span> <span data-ttu-id="7c3a9-126">Drehfeld-Steuerelemente dürfen nicht allein oder mit anderen Steuerelement Typen außer einem Textfeld verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-126">Spin controls shouldn't be used alone or with other types of controls besides a text box.</span></span>

    <span data-ttu-id="7c3a9-127">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-127">**Incorrect:**</span></span>

    ![<span data-ttu-id="7c3a9-128">Screenshot des Drehfeld-Steuer Elements, Grafik, kein Textfeld</span><span class="sxs-lookup"><span data-stu-id="7c3a9-128">screen shot of spin control, graphic, no text box</span></span> ](images/ctrl-spin-controls-image2.png)

    <span data-ttu-id="7c3a9-129">In diesem Beispiel wird ein Drehfeld-Steuerelement verwendet, um eine dynamische Grafik zu steuern.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-129">In this example, a spin control is used to control a dynamic graphic.</span></span>

-   <span data-ttu-id="7c3a9-130">**Sind zusammenhängende Wertebereiche gültig?**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-130">**Are contiguous value ranges valid?**</span></span> <span data-ttu-id="7c3a9-131">Wenn dies nicht der Fall ist, verwenden Sie stattdessen eine Dropdown Liste mit gültigen Werten.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-131">If not, use a drop-down list of valid values instead.</span></span>

    ![<span data-ttu-id="7c3a9-132">Screenshot der Dropdown Liste</span><span class="sxs-lookup"><span data-stu-id="7c3a9-132">screen shot of drop-down list</span></span> ](images/ctrl-spin-controls-image3.png)

    <span data-ttu-id="7c3a9-133">In diesem Beispiel sind nicht alle laufwerksnummern gültig. eine Dropdown Liste ist daher eine bessere Wahl.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-133">In this example, not all disk drive numbers are valid, so a drop-down list is a better choice.</span></span>

-   <span data-ttu-id="7c3a9-134">**Verwendet das Dreh Steuerelement praktisch?**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-134">**Is using the spin control practical?**</span></span> <span data-ttu-id="7c3a9-135">Die Verwendung eines Drehfeld-Steuer Elements ist praktisch für:</span><span class="sxs-lookup"><span data-stu-id="7c3a9-135">Using a spin control is practical for:</span></span>

    -   <span data-ttu-id="7c3a9-136">Eingeben einer kleinen Zahl, normalerweise unter 100.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-136">Entering a small number, typically under 100.</span></span>
    -   <span data-ttu-id="7c3a9-137">Vornehmen kleiner Änderungen an einem vorhandenen oder Standardwert.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-137">Making small changes to an existing or default value.</span></span>

    <span data-ttu-id="7c3a9-138">Drehfeld-Steuerelemente können zwar für beliebige numerische Eingaben verwendet werden, Sie sind jedoch in anderen Situationen ineffizient.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-138">While spin controls can be used for any numeric input, they are inefficient in situations other than these.</span></span>

-   <span data-ttu-id="7c3a9-139">**Ist das Dreh Steuerelement hilfreich?**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-139">**Is the spin control helpful?**</span></span> <span data-ttu-id="7c3a9-140">Wird das Steuerelement in einem Kontext verwendet, in dem Benutzer wahrscheinlich Ihre Maus verwenden?</span><span class="sxs-lookup"><span data-stu-id="7c3a9-140">Is the control used in a context where users are likely to be using their mouse?</span></span> <span data-ttu-id="7c3a9-141">Wenn dies nicht der gibt, sollten Sie ein Spin-Steuerelement optional</span><span class="sxs-lookup"><span data-stu-id="7c3a9-141">If not, consider a spin control optional.</span></span>
-   <span data-ttu-id="7c3a9-142">**Sind die Dropdown Listen der gleich geordneten Steuerelemente?**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-142">**Are the sibling controls drop-down lists?**</span></span> <span data-ttu-id="7c3a9-143">Wenn andere Dropdown Listen vorhanden sind, sollten Sie in Erwägung ziehen, eine Dropdown Liste für die Konsistenz zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-143">If there are other drop-down lists, consider using a drop-down list for consistency.</span></span>

    ![<span data-ttu-id="7c3a9-144">Screenshot des Dialog Felds mit Dropdown Listen</span><span class="sxs-lookup"><span data-stu-id="7c3a9-144">screen shot of dialog box with drop-down lists</span></span> ](images/ctrl-spin-controls-image4.png)

    <span data-ttu-id="7c3a9-145">In diesem Beispiel könnte ein Drehfeld verwendet werden, aber eine Dropdown Liste wird aus Gründen der Konsistenz verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-145">In this example, a spin box could be used, but a drop-down list is used for consistency.</span></span>

-   <span data-ttu-id="7c3a9-146">**Handelt es sich bei Berührungs-oder Stift Benutzern um ein primäres Ziel**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-146">**Are touch or pen users a primary target?**</span></span> <span data-ttu-id="7c3a9-147">Wenn dies der Fall ist, sollten Sie stattdessen eine Dropdown Liste verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-147">If so, consider using a drop-down list instead.</span></span> <span data-ttu-id="7c3a9-148">Die Pfeil Schaltflächen in einem Drehfeld-Steuerelement sind zu klein, um effizient mit berühren oder einem Stift verwendet werden zu können.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-148">The arrow buttons in a spin control are too small to be used efficiently with touch or a pen.</span></span>

<span data-ttu-id="7c3a9-149">Wenn ein Schieberegler oder ein Drehfeld möglich ist, verwenden Sie ein Drehfeld, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="7c3a9-149">If a slider or a spin box is possible, use a spin box if:</span></span>

-   <span data-ttu-id="7c3a9-150">Der auf dem Bildschirm verfügbare Platz ist knapp.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-150">Screen space is tight.</span></span>
-   <span data-ttu-id="7c3a9-151">Ein Benutzer wird die Verwendung der Tastatur wahrscheinlich bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-151">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="7c3a9-152">Verwenden Sie in folgenden Fällen einen Schieberegler:</span><span class="sxs-lookup"><span data-stu-id="7c3a9-152">Use a slider if:</span></span>

-   <span data-ttu-id="7c3a9-153">Benutzer profitieren von sofortigem Feedback.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-153">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="7c3a9-154">Richtlinien</span><span class="sxs-lookup"><span data-stu-id="7c3a9-154">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="7c3a9-155">Allgemein</span><span class="sxs-lookup"><span data-stu-id="7c3a9-155">General</span></span>

-   <span data-ttu-id="7c3a9-156">**Verwenden Sie Dreh Steuerelemente, wenn Sie praktisch und hilfreich sind.**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-156">**Use spin controls whenever they are practical and helpful.**</span></span> <span data-ttu-id="7c3a9-157">Siehe [ist das richtige Steuerelement?](#is-this-the-right-control)</span><span class="sxs-lookup"><span data-stu-id="7c3a9-157">See [Is this the right control?](#is-this-the-right-control)</span></span>

    -   <span data-ttu-id="7c3a9-158">**Ausnahme:** Um mit anderen Textfeldern auf derselben Benutzeroberfläche konsistent zu sein, verwenden Sie die Drehfeld-Steuerelemente, auch wenn Sie nicht immer praktikabel sind.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-158">**Exception:** To be consistent with other text boxes on the same user interface (UI), use spin controls even if they aren't always practical.</span></span>

    <span data-ttu-id="7c3a9-159">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-159">**Correct:**</span></span>

    ![<span data-ttu-id="7c3a9-160">Screenshot der Drehfeld-Steuerelemente für Monat, Tag, Jahr</span><span class="sxs-lookup"><span data-stu-id="7c3a9-160">screen shot of month, day, year spin controls</span></span> ](images/ctrl-spin-controls-image5.png)

    <span data-ttu-id="7c3a9-161">In diesem Beispiel wird ein Drehfeld-Steuerelement für die Konsistenz mit dem Year-Steuerelement verwendet, auch wenn es nicht immer praktikabel ist.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-161">In this example, a spin control is used with the year control for consistency, even though it isn't always practical.</span></span>

    <span data-ttu-id="7c3a9-162">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-162">**Incorrect:**</span></span>

    ![<span data-ttu-id="7c3a9-163">Screenshot des Drehungs Steuer Elements für IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="7c3a9-163">screen shot of ip address spin control</span></span> ](images/ctrl-spin-controls-image6.png)

    <span data-ttu-id="7c3a9-164">In diesem Beispiel ist das Drehfeld-Steuerelement unbrauchbar.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-164">In this example, the spin control is unusable.</span></span>

-   <span data-ttu-id="7c3a9-165">**Legen Sie den "Kumpel" des Textfelds immer als Dreh Steuerelement ab.**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-165">**Always make a spin control the "buddy" of the text box.**</span></span> <span data-ttu-id="7c3a9-166">Dadurch wird das Drehfeld-Steuerelement in das Textfeld eingefügt.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-166">Doing so places the spin control inside the text box.</span></span>

    <span data-ttu-id="7c3a9-167">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-167">**Correct:**</span></span>

    ![<span data-ttu-id="7c3a9-168">Screenshot des Dreh Steuer Elements, das sich im Textfeld befindet</span><span class="sxs-lookup"><span data-stu-id="7c3a9-168">screen shot of spin control placed inside text box</span></span> ](images/ctrl-spin-controls-image7.png)

    <span data-ttu-id="7c3a9-169">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-169">**Incorrect:**</span></span>

    ![<span data-ttu-id="7c3a9-170">Screenshot des Drehfeld-Steuer Elements außerhalb des Textfelds</span><span class="sxs-lookup"><span data-stu-id="7c3a9-170">screen shot of spin control placed outside text box</span></span> ](images/ctrl-spin-controls-image8.png)

    <span data-ttu-id="7c3a9-171">Im richtigen Beispiel wird das Drehfeld-Steuerelement in das zugehörige Textfeld eingefügt.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-171">In the correct example, the spin control is placed inside its associated text box.</span></span>

-   <span data-ttu-id="7c3a9-172">**Deaktivieren Sie ein Drehfeld-Steuerelement, wenn das zugehörige Textfeld deaktiviert ist.**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-172">**Disable a spin control when its associated text box is disabled.**</span></span> <span data-ttu-id="7c3a9-173">Das Spin-Steuerelement ist eine ergänzende Eingabemethode – nie die einzige Eingabemethode.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-173">The spin control is a supplemental input method—never the only input method.</span></span>

### <a name="values"></a><span data-ttu-id="7c3a9-174">Werte</span><span class="sxs-lookup"><span data-stu-id="7c3a9-174">Values</span></span>

-   <span data-ttu-id="7c3a9-175">**Definieren Sie die oberste Schaltfläche, um den Wert um eine Einheit zu vergrößern, und die untere Schaltfläche, um um eine Einheit zu verringern.**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-175">**Define the top button to increase the value by one unit and the bottom button to decrease by one unit.**</span></span> <span data-ttu-id="7c3a9-176">In der Regel handelt es sich um eine Einheit, die jedoch die kleinste allgemeine Änderung des Werts sein sollte.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-176">Typically, the unit is one, but it should be the smallest common change in value.</span></span> <span data-ttu-id="7c3a9-177">Im Idealfall sollte das Drehfeld-Steuerelement alle gültigen Werte abdecken, und es sollte bequemer sein als das Eingeben des Texts.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-177">Ideally, the spin control should cover all valid values, and it should be more convenient than typing in the text.</span></span>

    ![<span data-ttu-id="7c3a9-178">Screenshot des Dreh Steuer Elements "Ränder"</span><span class="sxs-lookup"><span data-stu-id="7c3a9-178">screen shot of 'margins' spin control</span></span> ](images/ctrl-spin-controls-image9.png)

    <span data-ttu-id="7c3a9-179">Wenn Sie in diesem Beispiel auf ein Drehfeld-Steuerelement klicken, werden die Werte von 1 geändert. Dies ist die kleinste allgemeine Änderung des Werts.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-179">In this example, clicking a spin control changes the values by .1, which is the smallest common change in value.</span></span> <span data-ttu-id="7c3a9-180">Durch die Verwendung einer kleineren Einheit wird der Bereich gültiger Werte abgedeckt, aber die Dreh Steuerelemente können unbrauchbar werden.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-180">Using a smaller unit would cover the range of valid values but make the spin controls unusable.</span></span>

-   <span data-ttu-id="7c3a9-181">**Verwenden Sie das Drehfeld-Steuerelement, um Eingaben auf gültige Werte einzuschränken.**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-181">**Use the spin control to limit input to valid values.**</span></span> <span data-ttu-id="7c3a9-182">Die Verwendung eines Drehfeld-Steuer Elements sollte nie zu einem falschen Wert führen.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-182">Using a spin control should never result in an incorrect value.</span></span>
-   <span data-ttu-id="7c3a9-183">**Starten Sie den Bereich am Ende eines Bereichs gültiger Werte neu.**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-183">**At the end of a range of valid values, restart the range.**</span></span> <span data-ttu-id="7c3a9-184">Das Dreh Steuerelement-Metapher ist, dass der Benutzer ein Rad mit Werten spinnt, also dieses Rad-like-Verhalten.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-184">The spin control metaphor is that the user is spinning a wheel of values, hence this wheel-like behavior.</span></span>
    -   <span data-ttu-id="7c3a9-185">**Ausnahme:** Starten Sie den Bereich nicht neu, wenn der resultierende Wert nicht korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-185">**Exception:** Don't restart the range if the resulting value is certain to be incorrect.</span></span>

        ![<span data-ttu-id="7c3a9-186">Screenshot des Dreh Steuer Elements "Anzahl der Kopien"</span><span class="sxs-lookup"><span data-stu-id="7c3a9-186">screen shot of 'number of copies' spin control</span></span> ](images/ctrl-spin-controls-image10.png)

        <span data-ttu-id="7c3a9-187">Wenn Sie in diesem Beispiel auf die Schaltfläche mit dem Pfeil nach unten klicken, wird der Bereich nicht neu gestartet (durch den maximalen Wert), da dieser Wert sicher nicht korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-187">In this example, clicking the down arrow button doesn't restart the range (by going to the maximum value) because that value is certain to be incorrect.</span></span>

-   <span data-ttu-id="7c3a9-188">**Verwenden Sie anstelle von besonderen numerischen Werten Text.**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-188">**Use text instead of special numeric values.**</span></span> <span data-ttu-id="7c3a9-189">Ermöglichen Sie es Benutzern, diese besonderen Werte zu verwenden, anstatt Sie kennen zu müssen, und geben Sie Sie ein.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-189">Allow users to spin to these special values instead of having to know them and type them in.</span></span>

    ![<span data-ttu-id="7c3a9-190">Screenshot des "Standby after (Never)"-Drehfeld Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="7c3a9-190">screen shot of 'sleep after (never)' spin control</span></span> ](images/ctrl-spin-controls-image11.png)

    <span data-ttu-id="7c3a9-191">In diesem Beispiel ist nie ein spezieller Wert, aber Benutzer können darauf drehen.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-191">In this example, Never is a special value but users can spin to it.</span></span>

-   <span data-ttu-id="7c3a9-192">**Wenn der Wert Trennzeichen aufweist, sollte das zugehörige Textfeld über mehrere Eingabefokus Punkte verfügen.**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-192">**If the value has delimiters, the associated text box should have multiple input focus points.**</span></span> <span data-ttu-id="7c3a9-193">Auf diese Weise können die numerischen Segmente einzeln bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-193">Doing so allows the numeric segments to be manipulated individually.</span></span>

    ![<span data-ttu-id="7c3a9-194">Screenshot des Zeit drehenden Steuer Elements, Minuten ausgewählt</span><span class="sxs-lookup"><span data-stu-id="7c3a9-194">screen shot of time spin control, minutes selected</span></span> ](images/ctrl-spin-controls-image12.png)

    <span data-ttu-id="7c3a9-195">In diesem Beispiel wirkt sich das Spin-Steuerelement auf die Werte für Stunden, Minuten, Sekunden und Uhr/p.m.-Kennung –, je nachdem, welcher Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-195">In this example, the spin control affects the values for hours, minutes, seconds, and A.M./P.M.—whichever has the focus.</span></span>

-   <span data-ttu-id="7c3a9-196">**Wenn der Werteinheiten aufweist, verwenden Sie das Drehfeld-Steuerelement, um diese Einheiten ebenfalls zu ändern.**</span><span class="sxs-lookup"><span data-stu-id="7c3a9-196">**If the value has units, use the spin control to change those units as well.**</span></span>

    ![<span data-ttu-id="7c3a9-197">Screenshot des Time-Spin-Steuer Elements, "Uhr"</span><span class="sxs-lookup"><span data-stu-id="7c3a9-197">screen shot of time spin control, 'a.m.'</span></span> <span data-ttu-id="7c3a9-198">Ausgewählt</span><span class="sxs-lookup"><span data-stu-id="7c3a9-198">selected</span></span> ](images/ctrl-spin-controls-image13.png)

    <span data-ttu-id="7c3a9-199">In diesem Beispiel kann das Drehfeld-Steuerelement zum Ändern von Einheiten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-199">In this example, the spin control can be used to change units.</span></span>

## <a name="labels"></a><span data-ttu-id="7c3a9-200">Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="7c3a9-200">Labels</span></span>

-   <span data-ttu-id="7c3a9-201">Wenden Sie die [Textfeld-Beschriftungs](ctrl-text-boxes.md) Richtlinien an, um das zugehörige Textfeld zu bezeichnen</span><span class="sxs-lookup"><span data-stu-id="7c3a9-201">Apply the [text box labeling](ctrl-text-boxes.md) guidelines to label the associated text box.</span></span> <span data-ttu-id="7c3a9-202">Drehfeld-Steuerelemente werden niemals direkt bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-202">Spin controls are never labeled directly.</span></span>

## <a name="documentation"></a><span data-ttu-id="7c3a9-203">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7c3a9-203">Documentation</span></span>

<span data-ttu-id="7c3a9-204">Beim Verweisen auf Dreh Steuerelemente:</span><span class="sxs-lookup"><span data-stu-id="7c3a9-204">When referring to spin controls:</span></span>

-   <span data-ttu-id="7c3a9-205">In der Benutzerdokumentation finden Sie keine Informationen zu den Dreh Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-205">Don't refer to spin controls in user documentation.</span></span> <span data-ttu-id="7c3a9-206">Verweisen Sie stattdessen auf die Bezeichnung des zugeordneten Textfelds.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-206">Instead, refer to the label of the associated text box.</span></span>
-   <span data-ttu-id="7c3a9-207">Weitere Informationen finden Sie unter Dreh Steuerelemente und Drehfelder nur in der Programmierung und in anderen technischen Dokumentationen.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-207">Refer to spin controls and spin boxes only in programming and other technical documentation.</span></span>

<span data-ttu-id="7c3a9-208">Beispiel: Geben Sie im Feld **Datum** den Datums Abschnitt ein, den Sie ändern möchten, oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7c3a9-208">Example: In the **Date** box, type or select the part of the date you want to change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c3a9-209">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7c3a9-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c3a9-210">Glossar</span><span class="sxs-lookup"><span data-stu-id="7c3a9-210">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 