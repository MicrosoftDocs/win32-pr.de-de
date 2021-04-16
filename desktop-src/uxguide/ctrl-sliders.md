---
title: Schieberegler (Entwurfs Grundlagen)
description: Mit einem Schieberegler können Benutzer aus einem kontinuierlichen Bereich von Werten auswählen.
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ff9791ab49c338e4c11e014a3e996771571add9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104558353"
---
# <a name="sliders-design-basics"></a><span data-ttu-id="f8027-103">Schieberegler (Entwurfs Grundlagen)</span><span class="sxs-lookup"><span data-stu-id="f8027-103">Sliders (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="f8027-104">Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f8027-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="f8027-105">Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="f8027-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="f8027-106">Mit einem Schieberegler können Benutzer aus einem kontinuierlichen Bereich von Werten auswählen.</span><span class="sxs-lookup"><span data-stu-id="f8027-106">With a slider, users can choose from a continuous range of values.</span></span> <span data-ttu-id="f8027-107">Ein Schieberegler verfügt über einen Balken, der den Bereich und einen Indikator mit dem aktuellen Wert anzeigt.</span><span class="sxs-lookup"><span data-stu-id="f8027-107">A slider has a bar that shows the range and an indicator that shows the current value.</span></span> <span data-ttu-id="f8027-108">Optionale Teil Striche zeigen Werte an.</span><span class="sxs-lookup"><span data-stu-id="f8027-108">Optional tick marks show values.</span></span>

![<span data-ttu-id="f8027-109">Darstellung von Balken, Schieberegler und Teil Strichen</span><span class="sxs-lookup"><span data-stu-id="f8027-109">figure showing bar, slider, and tick marks</span></span> ](images/ctrl-sliders-image1.png)

<span data-ttu-id="f8027-110">Ein typischer Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="f8027-110">A typical slider.</span></span>

> [!Note]  
> <span data-ttu-id="f8027-111">Richtlinien für das [Layout](vis-layout.md) werden in einem separaten Artikel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f8027-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="f8027-112">Ist dies das richtige Steuerelement?</span><span class="sxs-lookup"><span data-stu-id="f8027-112">Is this the right control?</span></span>

<span data-ttu-id="f8027-113">Verwenden Sie einen Schieberegler, wenn die Benutzer in der Lage sein sollen **, definierte, zusammenhängende Werte (z. b. Volume oder Helligkeit) oder einen Bereich diskreter Werte (z. b. Bildschirm Auflösungseinstellungen) festzulegen.**</span><span class="sxs-lookup"><span data-stu-id="f8027-113">Use a slider when you want your users to be able to **set defined, contiguous values (such as volume or brightness) or a range of discrete values (such as screen resolution settings).**</span></span>

<span data-ttu-id="f8027-114">Eine Schieberegler ist eine gute Wahl, wenn Sie wissen, dass Benutzer den Wert als relative Anzahl betrachten und nicht als numerischen Wert.</span><span class="sxs-lookup"><span data-stu-id="f8027-114">A slider is a good choice when you know that users think of the value as a relative quantity, not a numeric value.</span></span> <span data-ttu-id="f8027-115">So denken Benutzer beispielsweise beim Festlegen der Audiolautstärke an "niedrig" oder "mittel", aber nicht an Werte wie "2" oder "5".</span><span class="sxs-lookup"><span data-stu-id="f8027-115">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>

<span data-ttu-id="f8027-116">Orientieren Sie sich an folgenden Fragen:</span><span class="sxs-lookup"><span data-stu-id="f8027-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="f8027-117">**Handelt es sich bei der Einstellung um eine relative Anzahl?**</span><span class="sxs-lookup"><span data-stu-id="f8027-117">**Does the setting seem like a relative quantity?**</span></span> <span data-ttu-id="f8027-118">Wenn dies nicht der [Fall ist, verwenden Sie](ctrl-radio-buttons.md)Options Felder oder eine [Dropdown](/windows/desktop/uxguide/ctrl-drop) Liste oder eine [einzelne Auswahlliste](ctrl-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="f8027-118">If not, use [radio buttons](ctrl-radio-buttons.md), or a [drop-down](/windows/desktop/uxguide/ctrl-drop) or [single-selection list](ctrl-list-boxes.md).</span></span>
-   <span data-ttu-id="f8027-119">**Handelt es sich bei der Einstellung um einen exakten, bekannten numerischen Wert?**</span><span class="sxs-lookup"><span data-stu-id="f8027-119">**Is the setting an exact, known numeric value?**</span></span> <span data-ttu-id="f8027-120">Wenn dies der Fall ist, verwenden Sie [numerische Textfelder](ctrl-text-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="f8027-120">If so, use a [numeric text boxes](ctrl-text-boxes.md).</span></span>
-   <span data-ttu-id="f8027-121">**Wäre es für Benutzer hilfreich, sofort Feedback zur Auswirkung von Einstellungsänderungen zu erhalten?**</span><span class="sxs-lookup"><span data-stu-id="f8027-121">**Would a user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="f8027-122">Wenn ja, verwenden Sie einen Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="f8027-122">If so, use a slider.</span></span> <span data-ttu-id="f8027-123">Beispielsweise können Benutzer eine Farbe leichter auswählen, wenn sie sofort sehen, wie sich Änderungen an den Werten für Farbton, Sättigung oder Leuchtdichte auswirken.</span><span class="sxs-lookup"><span data-stu-id="f8027-123">For example, users can choose a color more easily by immediately seeing the effect of changes to hue, saturation, or luminosity values.</span></span>
-   <span data-ttu-id="f8027-124">**Weist die Einstellung einen Bereich aus vier oder mehr Werten auf?**</span><span class="sxs-lookup"><span data-stu-id="f8027-124">**Does the setting have a range of four or more values?**</span></span> <span data-ttu-id="f8027-125">Ist dies nicht der Fall, verwenden Sie stattdessen Optionsfelder.</span><span class="sxs-lookup"><span data-stu-id="f8027-125">If not, use radio buttons.</span></span>
-   <span data-ttu-id="f8027-126">**Können Benutzer den Wert ändern?**</span><span class="sxs-lookup"><span data-stu-id="f8027-126">**Can the user change the value?**</span></span> <span data-ttu-id="f8027-127">Schieberegler dienen zur Benutzerinteraktion.</span><span class="sxs-lookup"><span data-stu-id="f8027-127">Sliders are for user interaction.</span></span> <span data-ttu-id="f8027-128">Wenn ein Benutzer den Wert nicht jemals ändern kann, verwenden Sie stattdessen ein Schreib geschütztes [Textfeld](ctrl-text-boxes.md) .</span><span class="sxs-lookup"><span data-stu-id="f8027-128">If a user can't ever change the value, use a read-only [text box](ctrl-text-boxes.md) instead.</span></span>

<span data-ttu-id="f8027-129">Wenn ein Schieberegler oder ein numerisches Textfeld möglich ist, verwenden Sie ein numerisches Textfeld, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="f8027-129">If a slider or a numeric text box is possible, use a numeric text box if:</span></span>

-   <span data-ttu-id="f8027-130">Der auf dem Bildschirm verfügbare Platz ist knapp.</span><span class="sxs-lookup"><span data-stu-id="f8027-130">Screen space is tight.</span></span>
-   <span data-ttu-id="f8027-131">Ein Benutzer wird die Verwendung der Tastatur wahrscheinlich bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="f8027-131">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="f8027-132">Verwenden Sie in folgenden Fällen einen Schieberegler:</span><span class="sxs-lookup"><span data-stu-id="f8027-132">Use a slider if:</span></span>

-   <span data-ttu-id="f8027-133">Benutzer profitieren von sofortigem Feedback.</span><span class="sxs-lookup"><span data-stu-id="f8027-133">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="f8027-134">Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f8027-134">Guidelines</span></span>

-   <span data-ttu-id="f8027-135">**Verwenden Sie eine natürliche Ausrichtung.**</span><span class="sxs-lookup"><span data-stu-id="f8027-135">**Use a natural orientation.**</span></span> <span data-ttu-id="f8027-136">Wenn der Schieberegler beispielsweise einen echten Wert darstellt, der normalerweise vertikal angezeigt wird (z. B. eine Temperatur), verwenden Sie die vertikale Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="f8027-136">For example, if the slider represents a real-world value that is normally shown vertically (such as temperature), use a vertical orientation.</span></span>
-   <span data-ttu-id="f8027-137">**Orientieren Sie sich am Schieberegler, um die Kultur ihrer Benutzer widerzuspiegeln.**</span><span class="sxs-lookup"><span data-stu-id="f8027-137">**Orient the slider to reflect the culture of your users.**</span></span> <span data-ttu-id="f8027-138">Wenn z. b. westliche Kulturen von links nach rechts gelesen werden, legen Sie bei horizontalen Schiebereglern das niedrige Ende des Bereichs auf der linken Seite und das hohe Ende auf der rechten Seite ab.</span><span class="sxs-lookup"><span data-stu-id="f8027-138">For example, Western cultures read from left to right, so for horizontal sliders, put the low end of the range on the left and the high end on the right.</span></span> <span data-ttu-id="f8027-139">Führen Sie für Kulturen, die von rechts nach links gelesen werden, das Gegenteil aus.</span><span class="sxs-lookup"><span data-stu-id="f8027-139">For cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="f8027-140">**Legen Sie die Größe des Steuer Elements so fest, dass ein Benutzer leicht den gewünschten Wert festlegen kann.**</span><span class="sxs-lookup"><span data-stu-id="f8027-140">**Size the control so that a user can easily set the desired value.**</span></span> <span data-ttu-id="f8027-141">Stellen Sie für Einstellungen mit separaten Werten sicher, dass der Benutzer jeden Wert einfach mithilfe der Maus auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="f8027-141">For settings with discrete values, make sure the user can easily select any value using the mouse.</span></span>
-   <span data-ttu-id="f8027-142">**Es empfiehlt sich, eine nichtlineare Skala zu verwenden, wenn der Wertebereich groß ist und Benutzer wahrscheinlich Werte an einem Ende des Bereichs auswählen.**</span><span class="sxs-lookup"><span data-stu-id="f8027-142">**Consider using a non-linear scale if the range of values is large and users will likely select values at one end of the range.**</span></span> <span data-ttu-id="f8027-143">Der Uhrzeitwert kann z. b. 1 Minute, 1 Stunde, 1 Tag oder 1 Monat betragen.</span><span class="sxs-lookup"><span data-stu-id="f8027-143">For example, time value might be 1 minute, 1 hour, 1 day, or 1 month.</span></span>
-   <span data-ttu-id="f8027-144">**Jedes Mal, wenn ein Benutzer eine Auswahl getroffen hat, sollten Sie sofort Feedback abgeben.**</span><span class="sxs-lookup"><span data-stu-id="f8027-144">**Whenever practical, give immediate feedback while or after a user makes a selection.**</span></span> <span data-ttu-id="f8027-145">Beispielsweise wird mit der Microsoft Windows-volumesteuerung das resultierende audiovolume angegeben.</span><span class="sxs-lookup"><span data-stu-id="f8027-145">For example, the Microsoft Windows volume control beeps to indicate the resulting audio volume.</span></span>
-   <span data-ttu-id="f8027-146">**Verwenden Sie Bezeichnungen, um den Wertebereich anzuzeigen.**</span><span class="sxs-lookup"><span data-stu-id="f8027-146">**Use labels to show the range of values.**</span></span>

    <span data-ttu-id="f8027-147">**Ausnahme:** Wenn der Schieberegler vertikal ausgerichtet und die oberste Bezeichnung "Maximum", "High", "More" oder "äquivalente" ist, können Sie die anderen Bezeichnungen weglassen, da die Bedeutung "Clear" ist.</span><span class="sxs-lookup"><span data-stu-id="f8027-147">**Exception:** If the slider is vertically oriented and the top label is Maximum, High, More, or equivalent, you can omit the other labels since the meaning is clear.</span></span>

    ![<span data-ttu-id="f8027-148">Abbildung eines vertikalen Schiebereglers</span><span class="sxs-lookup"><span data-stu-id="f8027-148">figure of a vertical slider</span></span> ](images/ctrl-sliders-image2.png)

    <span data-ttu-id="f8027-149">In diesem Beispiel macht die vertikale Ausrichtung des Schiebereglers die Bereichs Bezeichnungen unnötig.</span><span class="sxs-lookup"><span data-stu-id="f8027-149">In this example, the slider's vertical orientation makes the range labels unnecessary.</span></span>

-   <span data-ttu-id="f8027-150">**Verwenden Sie Teil Striche, wenn Benutzer den ungefähren Wert der Einstellung kennen müssen.**</span><span class="sxs-lookup"><span data-stu-id="f8027-150">**Use tick marks when users need to know the approximate value of the setting.**</span></span>
-   <span data-ttu-id="f8027-151">**Verwenden Sie Teil Striche und eine Wert Bezeichnung, wenn Benutzer den genauen Wert der gewählten Einstellung kennen müssen.**</span><span class="sxs-lookup"><span data-stu-id="f8027-151">**Use tick marks and a value label when users need to know the exact value of the setting they choose.**</span></span> <span data-ttu-id="f8027-152">Verwenden Sie immer eine Wert Bezeichnung, wenn ein Benutzer die Einheiten kennen muss, damit die Einstellung sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="f8027-152">Always use a value label if a user needs to know the units to make sense of the setting.</span></span>

    ![<span data-ttu-id="f8027-153">Abbildung des Schiebereglers mit angezeigter Anzahl von Pixeln</span><span class="sxs-lookup"><span data-stu-id="f8027-153">figure of slider showing number of pixels selected</span></span> ](images/ctrl-sliders-image3.png)

    <span data-ttu-id="f8027-154">In diesem Beispiel wird eine Bezeichnung verwendet, um den ausgewählten Wert eindeutig anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f8027-154">In this example, a label is used to clearly indicate the selected value.</span></span>

-   <span data-ttu-id="f8027-155">**Platzieren Sie bei horizontal ausgerichteten Schiebereglern Teil Striche unter dem Schieberegler.**</span><span class="sxs-lookup"><span data-stu-id="f8027-155">**For horizontally-oriented sliders, place tick marks under the slider.**</span></span> <span data-ttu-id="f8027-156">Bei vertikal ausgerichteten Schiebereglern platzieren Sie Teil Striche für westliche Kulturen nach rechts. Führen Sie für Kulturen, die von rechts nach links gelesen werden, das Gegenteil aus.</span><span class="sxs-lookup"><span data-stu-id="f8027-156">For vertically-oriented sliders, place tick marks to the right for Western cultures; for cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="f8027-157">**Platzieren Sie die Wert Bezeichnung vollständig unter dem Schieberegler-Steuerelement, damit die Beziehung eindeutig ist.**</span><span class="sxs-lookup"><span data-stu-id="f8027-157">**Place the value label completely under the slider control so that the relationship is clear.**</span></span>

    <span data-ttu-id="f8027-158">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="f8027-158">**Incorrect:**</span></span>

    ![<span data-ttu-id="f8027-159">Abbildung einer Bezeichnung, die länger als der Schieberegler ist</span><span class="sxs-lookup"><span data-stu-id="f8027-159">figure of a label that is longer than its slider</span></span> ](images/ctrl-sliders-image4.png)

    <span data-ttu-id="f8027-160">In diesem Beispiel wird die Wert Bezeichnung nicht am Schieberegler ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="f8027-160">In this example, the value label isn't aligned under the slider.</span></span>

-   <span data-ttu-id="f8027-161">**Wenn Sie einen Schieberegler deaktivieren, deaktivieren Sie auch alle zugeordneten Bezeichnungen.**</span><span class="sxs-lookup"><span data-stu-id="f8027-161">**When disabling a slider, also disable any associated labels.**</span></span>
-   <span data-ttu-id="f8027-162">**Verwenden Sie für dieselbe Einstellung nicht sowohl einen Schieberegler als auch ein numerisches Textfeld.**</span><span class="sxs-lookup"><span data-stu-id="f8027-162">**Don't use both a slider and a numeric text box for the same setting.**</span></span> <span data-ttu-id="f8027-163">Verwenden Sie nur das geeignetere Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="f8027-163">Use only the more appropriate control.</span></span>

    <span data-ttu-id="f8027-164">**Ausnahme:** Verwenden Sie beide Steuerelemente, wenn der Benutzer sofortiges Feedback benötigt und einen exakten numerischen Wert festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="f8027-164">**Exception:** Use both controls when the user needs both immediate feedback and the ability to set an exact numeric value.</span></span>

-   <span data-ttu-id="f8027-165">**Verwenden Sie einen Schieberegler nicht als Statusanzeige.**</span><span class="sxs-lookup"><span data-stu-id="f8027-165">**Don't use a slider as a progress indicator.**</span></span>
-   <span data-ttu-id="f8027-166">**Ändern Sie nicht die Größe des Schieberegler-Indikators von der Standardgröße.**</span><span class="sxs-lookup"><span data-stu-id="f8027-166">**Don't change the size of the slider indicator from the default size.**</span></span>

    <span data-ttu-id="f8027-167">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="f8027-167">**Incorrect:**</span></span>

    ![<span data-ttu-id="f8027-168">Abbildung des Schiebereglers, der kleiner ist als der Standardwert</span><span class="sxs-lookup"><span data-stu-id="f8027-168">figure of slider that is smaller than the default</span></span> ](images/ctrl-sliders-image5.png)

    <span data-ttu-id="f8027-169">In diesem Beispiel wird eine Größe verwendet, die kleiner als der Standardwert ist.</span><span class="sxs-lookup"><span data-stu-id="f8027-169">In this example, a size smaller than the default is used.</span></span>

    <span data-ttu-id="f8027-170">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="f8027-170">**Correct:**</span></span>

    ![<span data-ttu-id="f8027-171">Abbildung mit dem Standard Schieberegler</span><span class="sxs-lookup"><span data-stu-id="f8027-171">figure showing the default slider</span></span> ](images/ctrl-sliders-image6.png)

    <span data-ttu-id="f8027-172">In diesem Beispiel wird die Standardgröße verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8027-172">In this example, the default size is used.</span></span>

-   <span data-ttu-id="f8027-173">**Markieren Sie nicht jeden Teil Strich.**</span><span class="sxs-lookup"><span data-stu-id="f8027-173">**Don't label every tick mark.**</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="f8027-174">Empfohlene Größe und Abstände</span><span class="sxs-lookup"><span data-stu-id="f8027-174">Recommended sizing and spacing</span></span>

![<span data-ttu-id="f8027-175">Abbildung der empfohlenen schiebereglergröße und des Abstands</span><span class="sxs-lookup"><span data-stu-id="f8027-175">figure of recommended slider sizing and spacing</span></span> ](images/ctrl-sliders-image7.png)

<span data-ttu-id="f8027-176">Empfohlene Größe und Abstände für Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="f8027-176">Recommended sizing and spacing for sliders.</span></span>

## <a name="labels"></a><span data-ttu-id="f8027-177">Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="f8027-177">Labels</span></span>

### <a name="slider-labels"></a><span data-ttu-id="f8027-178">Schiebereglerbeschriftungen</span><span class="sxs-lookup"><span data-stu-id="f8027-178">Slider labels</span></span>

-   <span data-ttu-id="f8027-179">Verwenden Sie eine statische Text Bezeichnung, die mit einem Doppelpunkt endet, oder eine Gruppenfeld Bezeichnung ohne endende Interpunktions Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f8027-179">Use a static text label ending with a colon, or a group box label with no ending punctuation.</span></span>
-   <span data-ttu-id="f8027-180">Weisen Sie jeder Bezeichnung einen eindeutigen Zugriffsschlüssel zu.</span><span class="sxs-lookup"><span data-stu-id="f8027-180">Assign a unique access key to each label.</span></span> <span data-ttu-id="f8027-181">Informationen zu Zuweisungs Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="f8027-181">For assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="f8027-182">Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="f8027-182">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="f8027-183">Positionieren Sie die Schieberegler-Bezeichnung entweder auf der linken Seite des Schiebereglers oder höher, und richten Sie am linken Rand des Schiebereglers (oder im linken Bereichs Bezeichner, falls vorhanden) an.</span><span class="sxs-lookup"><span data-stu-id="f8027-183">Position the slider label either to the left of the slider, or above and aligned with the left edge of the slider (or its left range identifier, if present).</span></span>

### <a name="range-labels"></a><span data-ttu-id="f8027-184">Bereichsbeschriftungen</span><span class="sxs-lookup"><span data-stu-id="f8027-184">Range labels</span></span>

-   <span data-ttu-id="f8027-185">Beschriften Sie die beiden Enden des Schiebereglerbereichs, sofern dies nicht aufgrund einer vertikalen Ausrichtung unnötig ist.</span><span class="sxs-lookup"><span data-stu-id="f8027-185">Label the two ends of the slider range, unless a vertical orientation makes this unnecessary.</span></span>
-   <span data-ttu-id="f8027-186">Verwenden Sie nach Möglichkeit nur Word für jede Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="f8027-186">Use only word, if possible, for each label.</span></span>
-   <span data-ttu-id="f8027-187">Verwenden Sie keine Interpunktion am Ende.</span><span class="sxs-lookup"><span data-stu-id="f8027-187">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="f8027-188">Stellen Sie sicher, dass die Beschriftungen aussagekräftig und parallel sind.</span><span class="sxs-lookup"><span data-stu-id="f8027-188">Make sure these labels are descriptive and parallel.</span></span> <span data-ttu-id="f8027-189">Beispiele: „Maximum/Minimum“, „Mehr/Weniger“, „Niedrig/Hoch“, „Leise/Laut“.</span><span class="sxs-lookup"><span data-stu-id="f8027-189">Examples: Maximum/Minimum, More/Less, Low/High, Soft/Loud.</span></span>
-   <span data-ttu-id="f8027-190">Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="f8027-190">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="f8027-191">Weisen Sie keine Zugriffsschlüssel zu.</span><span class="sxs-lookup"><span data-stu-id="f8027-191">Don't assign access keys.</span></span>

### <a name="value-labels"></a><span data-ttu-id="f8027-192">Wertbeschriftungen</span><span class="sxs-lookup"><span data-stu-id="f8027-192">Value labels</span></span>

-   <span data-ttu-id="f8027-193">Wenn Sie eine Wertbeschriftung benötigen, zeigen Sie sie unter dem Schieberegler an.</span><span class="sxs-lookup"><span data-stu-id="f8027-193">If you need a value label, display it below the slider.</span></span>
-   <span data-ttu-id="f8027-194">Zentrieren Sie den Text relativ zum Steuerelement, und schließen Sie die Einheiten ein (beispielsweise Pixel).</span><span class="sxs-lookup"><span data-stu-id="f8027-194">Center the text relative to the control and include the units (such as pixels).</span></span>

    ![<span data-ttu-id="f8027-195">Abbildung der Bezeichnung, zentriert mit dem Schieberegler</span><span class="sxs-lookup"><span data-stu-id="f8027-195">figure of label centered under the slider</span></span> ](images/ctrl-sliders-image8.png)

    <span data-ttu-id="f8027-196">In diesem Beispiel wird die Wert Bezeichnung unter dem Schieberegler zentriert und umfasst die Einheiten.</span><span class="sxs-lookup"><span data-stu-id="f8027-196">In this example, the value label is centered under the slider and includes the units.</span></span>

## <a name="documentation"></a><span data-ttu-id="f8027-197">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="f8027-197">Documentation</span></span>

<span data-ttu-id="f8027-198">Beim Verweisen auf Schieberegler:</span><span class="sxs-lookup"><span data-stu-id="f8027-198">When referring to sliders:</span></span>

-   <span data-ttu-id="f8027-199">Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, und schließen Sie den Schieberegler ein</span><span class="sxs-lookup"><span data-stu-id="f8027-199">Use the exact label text, including its capitalization, and include the word slider.</span></span> <span data-ttu-id="f8027-200">Fügen Sie den Unterstrich oder Doppelpunkt des Zugriffsschlüssels nicht ein.</span><span class="sxs-lookup"><span data-stu-id="f8027-200">Don't include the access key underscore or colon.</span></span>
-   <span data-ttu-id="f8027-201">Verwenden Sie Move, um die Benutzerinteraktion zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="f8027-201">To describe user interaction, use move.</span></span>
-   <span data-ttu-id="f8027-202">Formatieren Sie nach Möglichkeit die Bezeichnung mit fettem Text.</span><span class="sxs-lookup"><span data-stu-id="f8027-202">When possible, format the label using bold text.</span></span> <span data-ttu-id="f8027-203">Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="f8027-203">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="f8027-204">Beispiel: um die Bildschirmauflösung zu vergrößern, verschieben Sie den Schieberegler für die **Bildschirmauflösung** nach rechts.</span><span class="sxs-lookup"><span data-stu-id="f8027-204">Example: To increase your screen resolution, move the **Screen resolution** slider to the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8027-205">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8027-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8027-206">Glossar</span><span class="sxs-lookup"><span data-stu-id="f8027-206">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 