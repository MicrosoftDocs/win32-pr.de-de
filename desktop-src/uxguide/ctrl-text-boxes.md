---
title: Text Felder
description: Mit einem Textfeld können Benutzer einen Text oder einen numerischen Wert anzeigen, eingeben oder bearbeiten.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2b5257e9772465f26815abb0f6ecbe0ff357ba4b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104530434"
---
# <a name="text-boxes"></a><span data-ttu-id="89fc5-103">Text Felder</span><span class="sxs-lookup"><span data-stu-id="89fc5-103">Text Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="89fc5-104">Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="89fc5-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="89fc5-105">Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="89fc5-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="89fc5-106">Mit einem Textfeld können Benutzer einen Text oder einen numerischen Wert anzeigen, eingeben oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="89fc5-106">With a text box, users can display, enter, or edit a text or numeric value.</span></span>

![<span data-ttu-id="89fc5-107">Screenshot eines typischen Textfelds und einer Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="89fc5-107">screen shot of a typical text box and label</span></span> ](images/ctrl-text-boxes-image1.png)

<span data-ttu-id="89fc5-108">Ein typisches Textfeld.</span><span class="sxs-lookup"><span data-stu-id="89fc5-108">A typical text box.</span></span>

> [!Note]  
> <span data-ttu-id="89fc5-109">Richtlinien im Zusammenhang mit [Layout](vis-layout.md), [Schriftarten](vis-fonts.md)und [Luftballons](ctrl-balloons.md) werden in separaten Artikeln dargestellt.</span><span class="sxs-lookup"><span data-stu-id="89fc5-109">Guidelines related to [layout](vis-layout.md), [fonts](vis-fonts.md), and [balloons](ctrl-balloons.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="89fc5-110">Ist dies das richtige Steuerelement?</span><span class="sxs-lookup"><span data-stu-id="89fc5-110">Is this the right control?</span></span>

<span data-ttu-id="89fc5-111">Orientieren Sie sich an folgenden Fragen:</span><span class="sxs-lookup"><span data-stu-id="89fc5-111">To decide, consider these questions:</span></span>

-   <span data-ttu-id="89fc5-112">**Ist es praktikabel, alle gültigen Werte effizient aufzuzählen?**</span><span class="sxs-lookup"><span data-stu-id="89fc5-112">**Is it practical to enumerate all the valid values efficiently?**</span></span> <span data-ttu-id="89fc5-113">Wenn dies der Fall ist, sollten Sie stattdessen eine [Auswahlliste](ctrl-list-boxes.md), eine [Listenansicht](ctrl-list-views.md), eine [Dropdown Liste](/windows/desktop/uxguide/ctrl-drop), eine bearbeitbare Dropdown Liste oder einen [Schieberegler](ctrl-sliders.md) in Erwägung ziehen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-113">If so, consider a [single-selection list](ctrl-list-boxes.md), [list view](ctrl-list-views.md), [drop-down list](/windows/desktop/uxguide/ctrl-drop), editable drop-down list, or [slider](ctrl-sliders.md) instead.</span></span>
-   <span data-ttu-id="89fc5-114">**Sind die gültigen Daten vollständig uneingeschränkt eingeschränkt? Oder ist die gültige Daten nur durch das Format eingeschränkt (eingeschränkte Länge oder Zeichen Typen)?**</span><span class="sxs-lookup"><span data-stu-id="89fc5-114">**Is the valid data completely unconstrained? Or is the valid data constrained only by format (constrained length or character types)?**</span></span> <span data-ttu-id="89fc5-115">Wenn dies der Fall ist, verwenden Sie ein Textfeld.</span><span class="sxs-lookup"><span data-stu-id="89fc5-115">If so, use a text box.</span></span>
-   <span data-ttu-id="89fc5-116">**Stellt der Wert einen Datentyp dar, der über ein spezielles allgemeines Steuerelement verfügt?**</span><span class="sxs-lookup"><span data-stu-id="89fc5-116">**Does the value represent a data type that has a specialized common control?**</span></span> <span data-ttu-id="89fc5-117">Beispiele hierfür sind Datums-, Uhrzeit-oder IPv4-oder IPv6-Adressen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-117">Examples include date, time, or IPv4 or IPv6 address.</span></span> <span data-ttu-id="89fc5-118">Wenn dies der Fall ist, verwenden Sie das entsprechende Steuerelement, z. b. ein Datums Steuerelement anstelle eines Textfelds.</span><span class="sxs-lookup"><span data-stu-id="89fc5-118">If so, use the appropriate control, such as a date control rather than a text box.</span></span>
-   <span data-ttu-id="89fc5-119">Wenn die Daten numerisch sind:</span><span class="sxs-lookup"><span data-stu-id="89fc5-119">If the data is numeric:</span></span>
    -   <span data-ttu-id="89fc5-120">**Wird die Einstellung von Benutzern als relative Menge wahrgenommen?**</span><span class="sxs-lookup"><span data-stu-id="89fc5-120">**Do users perceive the setting as a relative quantity?**</span></span> <span data-ttu-id="89fc5-121">Wenn ja, verwenden Sie einen Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="89fc5-121">If so, use a slider.</span></span>
    -   <span data-ttu-id="89fc5-122">**Wäre es für Benutzer hilfreich, sofort Feedback zur Auswirkung von Einstellungsänderungen zu erhalten?**</span><span class="sxs-lookup"><span data-stu-id="89fc5-122">**Would the user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="89fc5-123">Wenn dies der Fall ist, verwenden Sie einen Schieberegler, möglicherweise zusammen mit einem Textfeld.</span><span class="sxs-lookup"><span data-stu-id="89fc5-123">If so, use a slider, possibly along with a text box.</span></span> <span data-ttu-id="89fc5-124">Beispielsweise können Benutzer mithilfe eines Schiebereglers problemlos eine Farbe auswählen, da Sie sofort die Auswirkungen von Änderungen auf die Werte für Farbton, Sättigung und Helligkeit sehen können.</span><span class="sxs-lookup"><span data-stu-id="89fc5-124">For example, users can easily choose a color using a slider because they can immediately see the effect of changes to hue, saturation, or luminosity values.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="89fc5-125">Entwurfskonzepte</span><span class="sxs-lookup"><span data-stu-id="89fc5-125">Design concepts</span></span>

<span data-ttu-id="89fc5-126">Obwohl Textfelder den Vorteil haben, dass Sie sehr flexibel sind, haben Sie den Nachteil, dass Sie über minimale Einschränkungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-126">While text boxes have the benefit of being very flexible, they have the drawback of having minimal constraints.</span></span> <span data-ttu-id="89fc5-127">Für ein bearbeitbares Textfeld gelten die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="89fc5-127">The only constraints on an editable text box are:</span></span>

-   <span data-ttu-id="89fc5-128">Optional können Sie die maximale Anzahl von Zeichen festlegen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-128">You can optionally set the maximum number of characters.</span></span>
-   <span data-ttu-id="89fc5-129">Sie können die Eingabe optional nur auf numerische Zeichen (0 9) beschränken.</span><span class="sxs-lookup"><span data-stu-id="89fc5-129">You can optionally restrict input to numeric characters (0   9) only.</span></span>
-   <span data-ttu-id="89fc5-130">Wenn Sie ein [Drehfeld-Steuer](ctrl-spin-controls.md)Element verwenden, können Sie die Optionen für die Drehfeld Steuerung auf gültige Werte beschränken.</span><span class="sxs-lookup"><span data-stu-id="89fc5-130">If you use a [spin control](ctrl-spin-controls.md), you can limit spin control choices to valid values.</span></span>

<span data-ttu-id="89fc5-131">Abgesehen von der Länge und der optionalen Anwesenheit eines Spin-Steuer Elements haben Textfelder keine visuellen Hinweise, die die gültigen Werte oder deren Format vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-131">Aside from their length and the optional presence of a spin control, text boxes don't have any visual clues that suggest the valid values or their format.</span></span> <span data-ttu-id="89fc5-132">Dies bedeutet, dass Sie sich auf Bezeichnungen verlassen, um diese Informationen Benutzern zu vermitteln.</span><span class="sxs-lookup"><span data-stu-id="89fc5-132">This means relying on labels to convey this information to users.</span></span> <span data-ttu-id="89fc5-133">Wenn Benutzer Text eingeben, der nicht gültig ist, müssen Sie den Fehler mit einer Fehlermeldung behandeln.</span><span class="sxs-lookup"><span data-stu-id="89fc5-133">If users enter text that's not valid, you must handle the error with an error message.</span></span>

<span data-ttu-id="89fc5-134">Als allgemeine Regel **sollten Sie die am meisten eingeschränkte Steuerung verwenden**.</span><span class="sxs-lookup"><span data-stu-id="89fc5-134">As a general rule, **you should use the most constrained control that you can**.</span></span> <span data-ttu-id="89fc5-135">Verwenden Sie als letztes Mittel nicht eingeschränkte Steuerelemente wie Textfelder.</span><span class="sxs-lookup"><span data-stu-id="89fc5-135">Use unconstrained controls like text boxes as a last resort.</span></span> <span data-ttu-id="89fc5-136">Wenn Sie Einschränkungen in Erwägung ziehen, sollten Sie die Anforderungen von globalen Benutzern berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-136">That said, when you are considering constraints, bear in mind the needs of global users.</span></span> <span data-ttu-id="89fc5-137">Beispielsweise ist ein Steuerelement, das auf die USA von Postleitzahlen beschränkt ist, nicht globalisiert, aber ein nicht eingeschränktes Textfeld, das beliebige Postleitzahl annimmt, ist.</span><span class="sxs-lookup"><span data-stu-id="89fc5-137">For example, a control that is constrained to United States ZIP Codes isn't globalized, but an unconstrained text box that accepts any postal code format is.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="89fc5-138">Verwendungsmuster</span><span class="sxs-lookup"><span data-stu-id="89fc5-138">Usage patterns</span></span>

<span data-ttu-id="89fc5-139">Ein Textfeld ist ein flexibles Steuerelement mit mehreren möglichen Verwendungsmöglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="89fc5-139">A text box is a flexible control with several possible uses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89fc5-140"><strong>Dateneingabe</strong></span><span class="sxs-lookup"><span data-stu-id="89fc5-140"><strong>Data input</strong></span></span><br/> <span data-ttu-id="89fc5-141">Ein einzeilige, nicht eingeschränktes Textfeld, das zum eingeben oder bearbeiten kurzer Zeichen folgen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="89fc5-141">A single-line, unconstrained text box used to enter or edit short strings.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br/> <span data-ttu-id="89fc5-142">Ein einzeilige, nicht eingeschränktes Textfeld.</span><span class="sxs-lookup"><span data-stu-id="89fc5-142">A single-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89fc5-143"><strong>Formatierte Dateneingabe</strong></span><span class="sxs-lookup"><span data-stu-id="89fc5-143"><strong>Formatted data input</strong></span></span><br/> <span data-ttu-id="89fc5-144">Ein Satz kurzer, einzeilige Textfelder mit fester Größe, mit denen Daten in einem bestimmten Format eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-144">A set of short, fixed-sized, single-line text boxes used to enter data with a specific format.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br/> <span data-ttu-id="89fc5-145">Ein Textfeld, das für formatierte Dateneingaben verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="89fc5-145">A text box used for formatted data input.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89fc5-146">Die Funktion zum <a href="glossary.md">automatischen Beenden</a> verschiebt den Eingabefokus automatisch von einem Textfeld auf das nächste.</span><span class="sxs-lookup"><span data-stu-id="89fc5-146">The <a href="glossary.md">auto-exit</a> feature automatically advances the input focus from one text box to the next.</span></span> <span data-ttu-id="89fc5-147">Ein Nachteil dieses Ansatzes besteht darin, dass die Daten nicht als einzelne Einheit kopiert oder eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="89fc5-147">One disadvantage to this approach is that the data can't be copied or pasted as a single unit.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89fc5-148"><strong>Unterstützte Dateneingabe</strong></span><span class="sxs-lookup"><span data-stu-id="89fc5-148"><strong>Assisted data input</strong></span></span><br/> <span data-ttu-id="89fc5-149">Ein einzeitiges, nicht eingeschränktes Textfeld zum eingeben oder Bearbeiten von Zeichen folgen in Kombination mit einer Befehls Schaltfläche, die Benutzern hilft, gültige Werte auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-149">A single-line, unconstrained text box used to enter or edit strings, combined with a command button that helps users select valid values.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br/> <span data-ttu-id="89fc5-150">In diesem Beispiel hilft der Befehl "Durchsuchen" Benutzern dabei, gültige Werte auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-150">In this example, the Browse command helps users select valid values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89fc5-151"><strong>Texteingabe</strong></span><span class="sxs-lookup"><span data-stu-id="89fc5-151"><strong>Textual input</strong></span></span><br/> <span data-ttu-id="89fc5-152">Ein mehrzeilige, nicht eingeschränktes Textfeld, das verwendet wird, um lange Zeichen folgen einzugeben oder zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="89fc5-152">A multi-line, unconstrained text box used to enter or edit long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br/> <span data-ttu-id="89fc5-153">Ein mehrzeilige, nicht eingeschränktes Textfeld.</span><span class="sxs-lookup"><span data-stu-id="89fc5-153">A multi-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89fc5-154"><strong>Numerische Eingabe</strong></span><span class="sxs-lookup"><span data-stu-id="89fc5-154"><strong>Numeric input</strong></span></span><br/> <span data-ttu-id="89fc5-155">Ein einzeilige, numerisch formatierendes Textfeld zum eingeben oder Bearbeiten von Zahlen mit einem optionalen <a href="ctrl-spin-controls.md">Spin-Steuer</a> Element, um die Maus basierte Eingabe zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-155">A single-line, numeric-only text box used to enter or edit numbers, with an optional <a href="ctrl-spin-controls.md">spin control</a> to facilitate mouse-based input.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br/> <span data-ttu-id="89fc5-156">Ein für numerische Eingaben verwendetes Textfeld.</span><span class="sxs-lookup"><span data-stu-id="89fc5-156">A text box used for numeric input.</span></span><br/> <span data-ttu-id="89fc5-157">Die Kombination aus einem Textfeld und dem zugehörigen Drehfeld-Steuerelement wird als <a href="ctrl-spin-controls.md">Drehfeld</a>bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="89fc5-157">The combination of a text box and its associated spin control is called a <a href="ctrl-spin-controls.md">spin box</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89fc5-158"><strong>Kennwort und PIN-Eingabe</strong></span><span class="sxs-lookup"><span data-stu-id="89fc5-158"><strong>Password and PIN input</strong></span></span><br/> <span data-ttu-id="89fc5-159">Ein einzeilige, nicht eingeschränktes Textfeld, mit dem Kenn Wörter und Pins sicher eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-159">A single-line, unconstrained text box used to enter passwords and PINs securely.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br/> <span data-ttu-id="89fc5-160">Ein Textfeld, mit dem Kenn Wörter eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-160">A text box used to enter passwords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89fc5-161"><strong>Datenausgabe</strong></span><span class="sxs-lookup"><span data-stu-id="89fc5-161"><strong>Data output</strong></span></span><br/> <span data-ttu-id="89fc5-162">Ein einzeilige, Schreib geschütztes Textfeld, das immer ohne Rahmen angezeigt wird, um kurze Zeichen folgen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-162">A single-line, read-only text box, always displayed without a border, used to display short strings.</span></span> <br/></td>
<td><span data-ttu-id="89fc5-163">Im Gegensatz zu statischem Text können mit einem Textfeld angezeigte Daten mittels Bildlauf (nützlich, wenn die Daten breiter als das Steuerelement sind), ausgewählt und kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-163">Unlike static text, data displayed using a text box can be scrolled (useful if the data is wider than the control), selected, and copied.</span></span><br/> <img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br/> <span data-ttu-id="89fc5-164">Ein einzeilige, Schreib geschütztes Textfeld, das zum Anzeigen von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="89fc5-164">A single-line, read-only text box used to display data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89fc5-165"><strong>Textausgabe</strong></span><span class="sxs-lookup"><span data-stu-id="89fc5-165"><strong>Textual output</strong></span></span><br/> <span data-ttu-id="89fc5-166">Ein mehrzeilige Schreib geschütztes Textfeld, in dem lange Zeichen folgen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-166">A multi-line, read-only text box used to display long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br/> <span data-ttu-id="89fc5-167">Ein Schreib geschütztes Textfeld, das zum Anzeigen von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="89fc5-167">A read-only text box used to display data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="89fc5-168">Richtlinien</span><span class="sxs-lookup"><span data-stu-id="89fc5-168">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="89fc5-169">Allgemein</span><span class="sxs-lookup"><span data-stu-id="89fc5-169">General</span></span>

-   <span data-ttu-id="89fc5-170">**Wenn Sie ein Textfeld deaktivieren, deaktivieren Sie auch alle zugeordneten Bezeichnungen, Anweisungs Bezeichnungen, Dreh Steuerelemente und Befehls Schaltflächen.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-170">**When disabling a text box, also disable any associated labels, instruction labels, spin controls, and command buttons.**</span></span>
-   <span data-ttu-id="89fc5-171">**Verwenden Sie die automatische Vervollständigung, um Benutzern zu helfen, Daten einzugeben, die wahrscheinlich wiederholt verwendet werden**.</span><span class="sxs-lookup"><span data-stu-id="89fc5-171">**Use auto-complete to help users enter data that is likely to be used repeatedly**.</span></span> <span data-ttu-id="89fc5-172">Beispiele hierfür sind Benutzernamen, Adressen und Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-172">Examples include user names, addresses, and file names.</span></span> <span data-ttu-id="89fc5-173">Verwenden Sie jedoch nicht die automatische Vervollständigung für Textfelder, die vertrauliche Informationen enthalten können, z. b. Kenn Wörter, Pins, Kreditkartennummern oder medizinische Informationen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-173">However, don't use auto-complete for text boxes that may contain sensitive information, such as passwords, PINs, credit card numbers, or medical information.</span></span>
-   <span data-ttu-id="89fc5-174">**Sorgen Sie dafür, dass Benutzer nicht unnötig scrollen.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-174">**Don't make users scroll unnecessarily.**</span></span> <span data-ttu-id="89fc5-175">Wenn Sie davon ausgehen, dass Daten größer als das Textfeld sind, und Sie das Textfeld problemlos vergrößern können, ohne dass das Layout beeinträchtigt wird, können Sie das Feld vergrößern, um einen Bildlauf zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-175">If you expect data to be larger than the text box and you can readily make the text box larger without harming the layout, size the box to eliminate the need for scrolling.</span></span>

    <span data-ttu-id="89fc5-176">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-176">**Incorrect:**</span></span>

    ![<span data-ttu-id="89fc5-177">Screenshot des Textfelds "Computername"</span><span class="sxs-lookup"><span data-stu-id="89fc5-177">screen shot of a computer name text box</span></span> ](images/ctrl-text-boxes-image10.png)

    <span data-ttu-id="89fc5-178">In diesem Beispiel sollte das Textfeld viel länger zum Verarbeiten der Daten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-178">In this example, the text box should be made much longer to handle its data.</span></span>

-   <span data-ttu-id="89fc5-179">Scrollleisten:</span><span class="sxs-lookup"><span data-stu-id="89fc5-179">Scroll bars:</span></span>
    -   <span data-ttu-id="89fc5-180">**Fügen Sie keine horizontalen Schiebe leisten in mehrzeiligen Textfeldern ein.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-180">**Don't put horizontal scroll bars on multi-line text boxes.**</span></span> <span data-ttu-id="89fc5-181">Verwenden Sie stattdessen vertikales Scrollen und Zeilenumbrüchen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-181">Use vertical scrolling and line wrapping instead.</span></span>
    -   <span data-ttu-id="89fc5-182">**Legen Sie keine Schiebe leisten in einzeiligen Textfeldern ab.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-182">**Don't put any scroll bars on single-line text boxes.**</span></span>
-   <span data-ttu-id="89fc5-183">**Für numerische Eingaben können Sie ein Drehfeld-Steuerelement verwenden.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-183">**For numeric input, you may use a spin control.**</span></span> <span data-ttu-id="89fc5-184">Verwenden Sie für Texteingaben stattdessen eine Dropdown Liste oder eine bearbeitbare Dropdown Liste.</span><span class="sxs-lookup"><span data-stu-id="89fc5-184">For textual input, use a drop-down list or editable drop-down list instead.</span></span>
-   <span data-ttu-id="89fc5-185">**Verwenden Sie die Funktion zum automatischen Beenden nicht mit Ausnahme der formatierten Dateneingabe.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-185">**Don't use the auto-exit feature except for formatted data input.**</span></span> <span data-ttu-id="89fc5-186">Die automatische Verschiebung des Fokus kann die Benutzer überraschen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-186">The automatic shift of focus can surprise users.</span></span>

### <a name="editable-text-boxes"></a><span data-ttu-id="89fc5-187">Bearbeitbare Textfelder</span><span class="sxs-lookup"><span data-stu-id="89fc5-187">Editable text boxes</span></span>

-   <span data-ttu-id="89fc5-188">**Beschränken Sie die Länge des Eingabe Texts, wenn dies möglich ist.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-188">**Limit the length of the input text when you can.**</span></span> <span data-ttu-id="89fc5-189">Wenn die gültige Eingabe z. b. eine Zahl zwischen 0 und 999 ist, verwenden Sie ein numerisches Textfeld, das auf drei Zeichen begrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="89fc5-189">For example, if the valid input is a number between 0 and 999, use a numeric text box that is limited to three characters.</span></span> <span data-ttu-id="89fc5-190">Alle Teile von Textfeldern, in denen formatierte Dateneingaben verwendet werden, müssen eine kurze, festgelegte Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-190">All parts of text boxes that use formatted data input must have a short, fixed length.</span></span>
-   <span data-ttu-id="89fc5-191">**Seien Sie flexibel mit Datenformaten.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-191">**Be flexible with data formats.**</span></span> <span data-ttu-id="89fc5-192">Wenn Benutzer wahrscheinlich Text in einer Vielzahl von Formaten eingeben, versuchen Sie, alle häufigsten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="89fc5-192">If users are likely to enter text using a wide variety of formats, try to handle all the most common ones.</span></span> <span data-ttu-id="89fc5-193">Beispielsweise können viele Namen, Zahlen und Bezeichner mit optionalen Leerzeichen und Interpunktions Zeichen eingegeben werden, und die Groß-und Kleinschreibung ist oft unerheblich.</span><span class="sxs-lookup"><span data-stu-id="89fc5-193">For example, many names, numbers, and identifiers can be entered with optional spaces and punctuation, and the capitalization often doesn't matter.</span></span>
-   <span data-ttu-id="89fc5-194">Wenn Sie die wahrscheinlichen Formate nicht verarbeiten können, benötigen Sie ein bestimmtes Format, indem Sie formatierte Dateneingaben verwenden, oder geben Sie die gültigen Formate in der Bezeichnung an.</span><span class="sxs-lookup"><span data-stu-id="89fc5-194">If you can't handle the likely formats, require a specific format by using formatted data input or indicate the valid formats in the label.</span></span>

    <span data-ttu-id="89fc5-195">**Annehmbar:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-195">**Acceptable:**</span></span>

    ![<span data-ttu-id="89fc5-196">Screenshot eines Textfelds für numerische Eingabe</span><span class="sxs-lookup"><span data-stu-id="89fc5-196">screen shot of a text box for numeric input</span></span> ](images/ctrl-text-boxes-image11.png)

    <span data-ttu-id="89fc5-197">In diesem Beispiel erfordert ein Textfeld Eingaben in einem bestimmten Format.</span><span class="sxs-lookup"><span data-stu-id="89fc5-197">In this example, a text box requires input in a specific format.</span></span>

    <span data-ttu-id="89fc5-198">**Besserer**</span><span class="sxs-lookup"><span data-stu-id="89fc5-198">**Better:**</span></span>

    ![<span data-ttu-id="89fc5-199">Screenshot des Eingabe Textfelds für formatierte Daten</span><span class="sxs-lookup"><span data-stu-id="89fc5-199">screen shot of formatted data input text box</span></span> ](images/ctrl-text-boxes-image12.png)

    <span data-ttu-id="89fc5-200">In diesem Beispiel wird das formatierte Dateneingabe Muster verwendet, um ein bestimmtes Format anzufordern.</span><span class="sxs-lookup"><span data-stu-id="89fc5-200">In this example, the formatted data input pattern is used to require a specific format.</span></span>

    <span data-ttu-id="89fc5-201">**Best**</span><span class="sxs-lookup"><span data-stu-id="89fc5-201">**Best:**</span></span>

    ![<span data-ttu-id="89fc5-202">Screenshot eines nicht eingeschränkten Textfelds</span><span class="sxs-lookup"><span data-stu-id="89fc5-202">screen shot of an unconstrained text box</span></span> ](images/ctrl-text-boxes-image13.png)

    <span data-ttu-id="89fc5-203">In diesem Beispiel werden in einem Textfeld alle wahrscheinlichen Formate behandelt.</span><span class="sxs-lookup"><span data-stu-id="89fc5-203">In this example, a text box handles all likely formats.</span></span>

-   <span data-ttu-id="89fc5-204">Bei der Auswahl der maximalen Eingabe Länge sollten Sie die Formatflexibilität in Erwägung gezogen</span><span class="sxs-lookup"><span data-stu-id="89fc5-204">Consider format flexibility when choosing the maximum input length.</span></span> <span data-ttu-id="89fc5-205">Eine gültige Kreditkartennummer kann z. b. bis zu 19 Zeichen lang sein. durch das Einschränken der Länge auf einen kürzeren Wert wird die Eingabe von Zahlen in den längeren Formaten erschwert.</span><span class="sxs-lookup"><span data-stu-id="89fc5-205">For example, a valid credit card number can use up to 19 characters so limiting the length to anything shorter would make it difficult to enter numbers using the longer formats.</span></span>
-   <span data-ttu-id="89fc5-206">**Verwenden Sie das Format für formatierte Dateneingaben nicht, wenn Benutzer mit höherer Wahrscheinlichkeit in lange, komplexe Daten eingefügt werden.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-206">**Don't use the formatted data input pattern if users are more likely to paste in long, complex data.**</span></span> <span data-ttu-id="89fc5-207">Reservieren Sie stattdessen das formatierte Dateneingabe Muster für Situationen, in denen Benutzer die Daten wahrscheinlicher eingeben.</span><span class="sxs-lookup"><span data-stu-id="89fc5-207">Rather, reserve the formatted data input pattern for situations where users are more likely to type the data.</span></span>

    ![<span data-ttu-id="89fc5-208">Screenshot eines Textfelds mit der Bezeichnung: IPv6-Adresse</span><span class="sxs-lookup"><span data-stu-id="89fc5-208">screen shot of a text box with label: ipv6 address</span></span> ](images/ctrl-text-boxes-image14.png)

    <span data-ttu-id="89fc5-209">In diesem Beispiel wird das formatierte Dateneingabe Muster nicht verwendet, sodass Benutzer IPv6-Adressen einfügen können.</span><span class="sxs-lookup"><span data-stu-id="89fc5-209">In this example, the formatted data input pattern isn't used, so that users can to paste IPv6 addresses.</span></span>

-   <span data-ttu-id="89fc5-210">**Wenn Benutzer wahrscheinlicher werden, dass Sie den gesamten Wert erneut eingeben, wählen Sie den gesamten Text im Eingabefokus aus.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-210">**If users are more likely going to reenter the entire value, select all the text on input focus.**</span></span> <span data-ttu-id="89fc5-211">Wenn Benutzer die Wahrscheinlichkeit haben, dass Sie bearbeitet werden, platzieren Sie die Einfügemarke am Ende des Texts.</span><span class="sxs-lookup"><span data-stu-id="89fc5-211">If users are more likely to edit, place the caret at the end of the text.</span></span>

    ![<span data-ttu-id="89fc5-212">Screenshot eines Kennwort-Textfelds</span><span class="sxs-lookup"><span data-stu-id="89fc5-212">screen shot of a password text box</span></span> ](images/ctrl-text-boxes-image15.png)

    <span data-ttu-id="89fc5-213">In diesem Beispiel ist es wahrscheinlicher, dass Benutzer als "Edit" ersetzt werden, sodass der gesamte Wert im Eingabefokus ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="89fc5-213">In this example, users are more likely to replace than edit, so the entire value is selected on input focus.</span></span>

    ![<span data-ttu-id="89fc5-214">Screenshot eines Textfelds zum Eingeben von Schlüsselwörtern</span><span class="sxs-lookup"><span data-stu-id="89fc5-214">screen shot of a text box for entering keywords</span></span> ](images/ctrl-text-boxes-image16.png)

    <span data-ttu-id="89fc5-215">In diesem Beispiel ist es wahrscheinlicher, dass Benutzerschlüssel Wörter hinzufügen, als den Text zu ersetzen, sodass die Einfügemarke am Ende des Texts platziert wird.</span><span class="sxs-lookup"><span data-stu-id="89fc5-215">In this example, users are more likely to add keywords than replace the text, so the caret is placed at the end of the text.</span></span>

-   <span data-ttu-id="89fc5-216">**Verwenden Sie immer ein mehr zeitiges Textfeld, wenn neue Zeilenzeichen gültige Eingaben sind.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-216">**Always use a multi-line text box if new-line characters are valid input.**</span></span>
-   <span data-ttu-id="89fc5-217">**Wenn das Textfeld für eine Datei oder einen Pfad steht, stellen Sie immer eine Schaltfläche zum Durchsuchen bereit.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-217">**When the text box is for a file or path, always provide a Browse button.**</span></span>

### <a name="numeric-text-boxes"></a><span data-ttu-id="89fc5-218">Numerische Textfelder</span><span class="sxs-lookup"><span data-stu-id="89fc5-218">Numeric text boxes</span></span>

-   <span data-ttu-id="89fc5-219">**Wählen Sie die am einfachsten geeignete Einheit aus, und bezeichnen Sie die Einheiten.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-219">**Choose the most convenient unit and label the units.**</span></span> <span data-ttu-id="89fc5-220">Verwenden Sie z. b. die Verwendung von Millilitern anstelle von Litern (oder umgekehrt), Prozentsätzen anstelle direkter Werte (oder umgekehrt) usw.</span><span class="sxs-lookup"><span data-stu-id="89fc5-220">For example, consider using milliliters instead of liters (or vice versa), percentages instead of direct values (or vice versa), and so on.</span></span>

    <span data-ttu-id="89fc5-221">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-221">**Correct:**</span></span>

    ![<span data-ttu-id="89fc5-222">Screenshot des Textfelds mit "Litern als Einheit"</span><span class="sxs-lookup"><span data-stu-id="89fc5-222">screen shot of text box with liters as unit</span></span> ](images/ctrl-text-boxes-image17.png)

    <span data-ttu-id="89fc5-223">In diesem Beispiel wird die-Einheit als bezeichnet, erfordert jedoch, dass Benutzer Dezimalzahlen eingeben.</span><span class="sxs-lookup"><span data-stu-id="89fc5-223">In this example, the unit is labeled, but it requires users to enter decimal numbers.</span></span>

    <span data-ttu-id="89fc5-224">**Besserer**</span><span class="sxs-lookup"><span data-stu-id="89fc5-224">**Better:**</span></span>

    ![<span data-ttu-id="89fc5-225">Screenshot des Textfelds mit Millilitern als Einheit</span><span class="sxs-lookup"><span data-stu-id="89fc5-225">screen shot of text box with milliliters as unit</span></span> ](images/ctrl-text-boxes-image18.png)

    <span data-ttu-id="89fc5-226">In diesem Beispiel verwendet das Textfeld eine komfortablere Einheit.</span><span class="sxs-lookup"><span data-stu-id="89fc5-226">In this example, the text box uses a more convenient unit.</span></span>

-   <span data-ttu-id="89fc5-227">**Verwenden Sie ein Drehfeld-Steuerelement, wenn es hilfreich ist.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-227">**Use a spin control whenever it is helpful.**</span></span> <span data-ttu-id="89fc5-228">Manchmal sind Dreh Steuerelemente jedoch nicht praktikabel, z. b. Wenn Benutzer viele große Zahlen eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-228">However, sometimes spin controls aren't practical, such as when users need to enter many large numbers.</span></span> <span data-ttu-id="89fc5-229">Dreh Steuerelemente verwenden, wenn:</span><span class="sxs-lookup"><span data-stu-id="89fc5-229">Use spin controls when:</span></span>
    -   <span data-ttu-id="89fc5-230">Die Eingabe ist wahrscheinlich eine kleine Zahl, in der Regel unter 100.</span><span class="sxs-lookup"><span data-stu-id="89fc5-230">The input is likely to be a small number, typically under 100.</span></span>
    -   <span data-ttu-id="89fc5-231">Benutzer nehmen wahrscheinlich eine kleine Änderung an einer vorhandenen Zahl vor.</span><span class="sxs-lookup"><span data-stu-id="89fc5-231">Users are likely to make a small change to an existing number.</span></span>
    -   <span data-ttu-id="89fc5-232">Es ist wahrscheinlicher, dass Benutzer die Maus verwenden, als die Tastatur zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-232">Users are more likely to be using the mouse than the keyboard.</span></span>
-   <span data-ttu-id="89fc5-233">**Numerischen Text rechtsbündig ausrichten:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-233">**Right-align numeric text whenever:**</span></span>

    -   <span data-ttu-id="89fc5-234">Es ist mehr als ein numerisches Textfeld vorhanden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-234">There is more than one numeric text box.</span></span>
    -   <span data-ttu-id="89fc5-235">Die Textfelder sind vertikal ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="89fc5-235">The text boxes are vertically aligned.</span></span>
    -   <span data-ttu-id="89fc5-236">Benutzer können die Werte wahrscheinlich hinzufügen oder vergleichen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-236">Users are likely to add or compare the values.</span></span>

    <span data-ttu-id="89fc5-237">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-237">**Correct:**</span></span>

    ![<span data-ttu-id="89fc5-238">Screenshot der Ausgaben Textfelder (Hotel usw.)</span><span class="sxs-lookup"><span data-stu-id="89fc5-238">screen shot of expenses text boxes (hotel, etc.)</span></span> ](images/ctrl-text-boxes-image19.png)

    <span data-ttu-id="89fc5-239">In diesem Beispiel wird der numerische Text rechtsbündig ausgerichtet, um das Vergleichen von Werten zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="89fc5-239">In this example, the numeric text is right-aligned to make it easy to compare values.</span></span>

    <span data-ttu-id="89fc5-240">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-240">**Incorrect:**</span></span>

    ![<span data-ttu-id="89fc5-241">Screenshot von Textfeldern für RGB-Werte</span><span class="sxs-lookup"><span data-stu-id="89fc5-241">screen shot of text boxes for rgb values</span></span> ](images/ctrl-text-boxes-image20.png)

    <span data-ttu-id="89fc5-242">In diesem Beispiel ist der numerische Text falsch linksbündig ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="89fc5-242">In this example, the numeric text is incorrectly left-aligned.</span></span>

-   <span data-ttu-id="89fc5-243">**Sie sollten Währungswerte immer rechtsbündig ausrichten.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-243">**Always right-align monetary values.**</span></span>
-   <span data-ttu-id="89fc5-244">**Weisen Sie bestimmten numerischen Werten keine besondere Bedeutungen zu**, selbst wenn diese besondere Bedeutungen intern von Ihrer Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-244">**Don't assign special meanings to specific numeric values**, even if those special meanings are used internally by your application.</span></span> <span data-ttu-id="89fc5-245">Verwenden Sie stattdessen Kontrollkästchen oder Options Felder für eine explizite Benutzer Auswahl.</span><span class="sxs-lookup"><span data-stu-id="89fc5-245">Instead, use check boxes or radio buttons for an explicit user selection.</span></span>

    <span data-ttu-id="89fc5-246">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-246">**Incorrect:**</span></span>

    ![<span data-ttu-id="89fc5-247">Screenshot der Bezeichnung: Verwenden von "-1" zum Deaktivieren der Zwischenspeicherung</span><span class="sxs-lookup"><span data-stu-id="89fc5-247">screen shot of label: use -1 to disable caching</span></span> ](images/ctrl-text-boxes-image21.png)

    <span data-ttu-id="89fc5-248">In diesem Beispiel hat der Wert-1 eine besondere Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="89fc5-248">In this example, the value -1 has a special meaning.</span></span>

    <span data-ttu-id="89fc5-249">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-249">**Correct:**</span></span>

    ![<span data-ttu-id="89fc5-250">Screenshot der Kontrollkästchen Bezeichnung: Caching</span><span class="sxs-lookup"><span data-stu-id="89fc5-250">screen shot of check box label: caching</span></span> ](images/ctrl-text-boxes-image22.png)

    <span data-ttu-id="89fc5-251">In diesem Beispiel wird die-Option durch ein Kontrollkästchen explizit.</span><span class="sxs-lookup"><span data-stu-id="89fc5-251">In this example, a check box makes the option explicit.</span></span>

### <a name="password-and-pin-input"></a><span data-ttu-id="89fc5-252">Kennwort und PIN-Eingabe</span><span class="sxs-lookup"><span data-stu-id="89fc5-252">Password and PIN input</span></span>

-   <span data-ttu-id="89fc5-253">**Verwenden Sie immer das allgemeine Kennwort, anstatt ein eigenes Kennwort zu erstellen.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-253">**Always use the password common control instead of creating your own.**</span></span> <span data-ttu-id="89fc5-254">Kenn Wörter und Pins erfordern eine besondere Behandlung, damit Sie sicher verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-254">Passwords and PINs require special treatment to be handled securely.</span></span>

<span data-ttu-id="89fc5-255">Weitere Richtlinien und Beispiele finden Sie unter [Luftballons](ctrl-balloons.md).</span><span class="sxs-lookup"><span data-stu-id="89fc5-255">For more guidelines and examples, see [Balloons](ctrl-balloons.md).</span></span>

### <a name="textual-output"></a><span data-ttu-id="89fc5-256">Textausgabe</span><span class="sxs-lookup"><span data-stu-id="89fc5-256">Textual output</span></span>

-   <span data-ttu-id="89fc5-257">**Verwenden Sie ggf. die Farbe des weißen hintergrundsystems für großen, mehrzeiligen schreibgeschützten Text.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-257">**Consider using the white background system color for large, multi-line read-only text.**</span></span> <span data-ttu-id="89fc5-258">Durch einen weißen Hintergrund wird der Text leichter lesbar.</span><span class="sxs-lookup"><span data-stu-id="89fc5-258">A white background makes the text easier to read.</span></span> <span data-ttu-id="89fc5-259">Viel Text in einem grauen Hintergrund verhindert das lesen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-259">Lots of text on a gray background discourages reading.</span></span>

<span data-ttu-id="89fc5-260">Weitere Informationen zu Hintergrundfarben finden Sie unter [Schriftarten](vis-fonts.md).</span><span class="sxs-lookup"><span data-stu-id="89fc5-260">For more information on background colors, see [Fonts](vis-fonts.md).</span></span>

### <a name="data-output"></a><span data-ttu-id="89fc5-261">Datenausgabe</span><span class="sxs-lookup"><span data-stu-id="89fc5-261">Data output</span></span>

-   <span data-ttu-id="89fc5-262">**Verwenden Sie keinen Rahmen für einzeilige schreibgeschützte Textfelder.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-262">**Don't use a border for single-line, read-only text boxes.**</span></span> <span data-ttu-id="89fc5-263">Der Rahmen ist ein visueller Hinweis darauf, dass der Text bearbeitbar ist.</span><span class="sxs-lookup"><span data-stu-id="89fc5-263">The border is a visual clue that the text is editable.</span></span>
-   <span data-ttu-id="89fc5-264">**Deaktivieren Sie nicht schreibgeschützte einzeilige Textfelder.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-264">**Don't disable single-line, read-only text boxes.**</span></span> <span data-ttu-id="89fc5-265">Dadurch wird verhindert, dass Benutzer den Text in die Zwischenablage auswählen und kopieren.</span><span class="sxs-lookup"><span data-stu-id="89fc5-265">This prevents users from selecting and copying the text to the clipboard.</span></span> <span data-ttu-id="89fc5-266">Außerdem wird verhindert, dass Benutzer einen Bildlauf durchführen, wenn Sie die Größe ihrer Grenzen überschreiten.</span><span class="sxs-lookup"><span data-stu-id="89fc5-266">It also prevents users from scrolling the data if it exceeds the size of its boundaries.</span></span>
-   <span data-ttu-id="89fc5-267">**Legen Sie einen Tabstopp nicht in einem schreibgeschützten einzeiligen Textfeld fest, wenn der Benutzer wahrscheinlich keinen Bildlauf durchführen oder den Text kopieren muss.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-267">**Don't set a tab stop on single-line, read-only text box unless the user is likely to need to scroll or copy the text.**</span></span>

## <a name="input-validation-and-error-handling"></a><span data-ttu-id="89fc5-268">Eingabevalidierung und Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="89fc5-268">Input validation and error handling</span></span>

<span data-ttu-id="89fc5-269">Da Textfelder in der Regel nicht darauf beschränkt sind, nur gültige Eingaben zu akzeptieren, müssen Sie möglicherweise die Eingabe validieren und Probleme behandeln.</span><span class="sxs-lookup"><span data-stu-id="89fc5-269">Because text boxes are usually not constrained to accept only valid input, you may need to validate the input and handle any problems.</span></span> <span data-ttu-id="89fc5-270">Überprüfen Sie die verschiedenen Arten von Eingabe Problemen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="89fc5-270">Validate the various types of input problems as follows:</span></span>

-   <span data-ttu-id="89fc5-271">Wenn der Benutzer ein ungültiges Zeichen eingibt, ignorieren Sie das Zeichen und zeigen eine [Eingabeproblem](ctrl-balloons.md) Sprechblase an, in der die gültigen Zeichen erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-271">If the user enters a character that isn't valid, ignore the character and display an [input problem balloon](ctrl-balloons.md) that explains the valid characters.</span></span>

    ![Screenshot des Product Key Textfelds](images/ctrl-text-boxes-image23.png)

    <span data-ttu-id="89fc5-273">In diesem Beispiel meldet eine Sprechblase ein falsches Eingabezeichen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-273">In this example, a balloon reports an incorrect input character.</span></span>

-   <span data-ttu-id="89fc5-274">Wenn die Eingabedaten einen ungültigen Wert oder ein ungültiges Format aufweisen, zeigen Sie eine Sprechblase für Eingabe Probleme an, wenn das Textfeld den Eingabefokus verliert.</span><span class="sxs-lookup"><span data-stu-id="89fc5-274">If the input data has a value or format that isn't valid, display an input problem balloon when the text box loses input focus.</span></span>
-   <span data-ttu-id="89fc5-275">Wenn die Eingabedaten mit anderen Steuerelementen im Fenster inkonsistent sind, geben Sie eine Fehlermeldung an, wenn die gesamte Eingabe vollständig ist, z. b. Wenn Benutzer in einem modalen Dialogfeld auf OK klicken.</span><span class="sxs-lookup"><span data-stu-id="89fc5-275">If the input data is inconsistent with other controls on the window, give an error message when the entire input is complete, such as when users click OK for a modal dialog box.</span></span>

<span data-ttu-id="89fc5-276">**Löschen Sie keine ungültigen Eingabedaten, es sei denn, die Benutzer können Fehler problemlos beheben.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-276">**Don't clear invalid input data unless users aren't able to correct errors easily.**</span></span> <span data-ttu-id="89fc5-277">Dies ermöglicht es Benutzern, Fehler zu beheben, ohne zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-277">Doing so allows users to correct mistakes without starting over.</span></span> <span data-ttu-id="89fc5-278">Sie sollten z. b. falsche Kenn Wörter und Pins löschen, da Sie nicht auf einfache Weise korrigiert werden können.</span><span class="sxs-lookup"><span data-stu-id="89fc5-278">For example, you should clear incorrect passwords and PINs because users can't correct them easily.</span></span>

<span data-ttu-id="89fc5-279">Weitere Richtlinien und Beispiele finden Sie unter [Fehlermeldungen](mess-error.md) und [Luftballons](ctrl-balloons.md).</span><span class="sxs-lookup"><span data-stu-id="89fc5-279">For more guidelines and examples, see [Error Messages](mess-error.md) and [Balloons](ctrl-balloons.md).</span></span>

## <a name="prompts"></a><span data-ttu-id="89fc5-280">Eingabeaufforderungen</span><span class="sxs-lookup"><span data-stu-id="89fc5-280">Prompts</span></span>

<span data-ttu-id="89fc5-281">Eine Eingabeaufforderung ist eine Bezeichnung oder eine kurze Anweisung in einem Textfeld als Standardwert.</span><span class="sxs-lookup"><span data-stu-id="89fc5-281">A prompt is a label or short instruction placed inside a text box as its default value.</span></span> <span data-ttu-id="89fc5-282">Im Gegensatz zu statischem Text werden Aufforderungen auf dem Bildschirm ausgeblendet, sobald Benutzer etwas in das Textfeld eingeben oder den Eingabefokus erhalten.</span><span class="sxs-lookup"><span data-stu-id="89fc5-282">Unlike static text, prompts disappear from the screen once users type something into the text box or it gets input focus.</span></span>

![<span data-ttu-id="89fc5-283">Screenshot des Eingabe Aufforderungs-Textfelds mit Bezeichnung: Suchen</span><span class="sxs-lookup"><span data-stu-id="89fc5-283">screen shot of prompt text box with label: search</span></span> ](images/ctrl-text-boxes-image24.png)

<span data-ttu-id="89fc5-284">Eine typische Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="89fc5-284">A typical prompt.</span></span>

<span data-ttu-id="89fc5-285">Verwenden Sie eine Eingabeaufforderung, wenn:</span><span class="sxs-lookup"><span data-stu-id="89fc5-285">Use a prompt when:</span></span>

-   <span data-ttu-id="89fc5-286">Der Bildschirmbereich ist so hoch, dass die Verwendung einer Bezeichnung oder Anweisung nicht erwünscht ist, z. b. auf einer Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="89fc5-286">Screen space is at such a premium that using a label or instruction is undesirable, such as on a toolbar.</span></span>
-   <span data-ttu-id="89fc5-287">Bei der Eingabeaufforderung wird in erster Linie der Zweck des Textfelds auf kompakte Weise identifiziert.</span><span class="sxs-lookup"><span data-stu-id="89fc5-287">The prompt is primarily for identifying the purpose of the text box in a compact way.</span></span> <span data-ttu-id="89fc5-288">Dabei darf es sich nicht um wichtige Informationen handeln, die der Benutzer während der Verwendung des Textfelds sehen muss.</span><span class="sxs-lookup"><span data-stu-id="89fc5-288">It must not be crucial information that the user needs to see while using the text box.</span></span>

<span data-ttu-id="89fc5-289">Verwenden Sie keine Aufforderungen, um Benutzer zur Eingabe von etwas oder zum Klicken auf Schaltflächen zu leiten.</span><span class="sxs-lookup"><span data-stu-id="89fc5-289">Don't use prompts just to direct users to type something or to click buttons.</span></span> <span data-ttu-id="89fc5-290">Schreiben Sie z. b. nicht den Text der Eingabeaufforderung, und klicken Sie dann auf senden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-290">For example, don't write prompt text that says Enter a filename and then click Send.</span></span>

<span data-ttu-id="89fc5-291">Bei Verwendung von Eingabe Aufforderungen:</span><span class="sxs-lookup"><span data-stu-id="89fc5-291">When using prompts:</span></span>

-   <span data-ttu-id="89fc5-292">Zeichnen Sie den Eingabe Aufforderungs Text in kursiv grau und den eigentlichen Eingabetext in normaler schwarz.</span><span class="sxs-lookup"><span data-stu-id="89fc5-292">Draw the prompt text in italic gray and the actual input text in normal black.</span></span> <span data-ttu-id="89fc5-293">Der Eingabe Aufforderungs Text darf nicht mit echtem Text verwechselt werden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-293">The prompt text must not be confused with real text.</span></span>
-   <span data-ttu-id="89fc5-294">Halten Sie den Text der Eingabeaufforderung kurz.</span><span class="sxs-lookup"><span data-stu-id="89fc5-294">Keep the prompt text concise.</span></span> <span data-ttu-id="89fc5-295">Sie können Fragmente anstelle von vollständigen Sätzen verwenden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-295">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="89fc5-296">Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="89fc5-296">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="89fc5-297">Verwenden Sie keine endinterpunktions Zeichen oder Ellipsen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-297">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="89fc5-298">Der Eingabe Aufforderungs Text sollte nicht bearbeitbar sein und sollte ausgeblendet werden, wenn Benutzer in das Textfeld oder die Tab-Taste klicken.</span><span class="sxs-lookup"><span data-stu-id="89fc5-298">The prompt text should not be editable and should disappear once users click in or tab into the text box.</span></span>
    -   <span data-ttu-id="89fc5-299">**Ausnahme:** Wenn das Textfeld den Standardeingabe Fokus besitzt, wird die Eingabeaufforderung angezeigt, und Sie verschwindet, sobald der Benutzer mit der Eingabe beginnt.</span><span class="sxs-lookup"><span data-stu-id="89fc5-299">**Exception:** If the text box has default input focus, the prompt is displayed, and it disappears once the user starts typing.</span></span>
-   <span data-ttu-id="89fc5-300">Der Text der Eingabeaufforderung wird wieder hergestellt, wenn das Textfeld noch leer ist, wenn es den Eingabefokus verliert.</span><span class="sxs-lookup"><span data-stu-id="89fc5-300">The prompt text is restored if the text box is still empty when it loses input focus.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="89fc5-301">Empfohlene Größe und Abstände</span><span class="sxs-lookup"><span data-stu-id="89fc5-301">Recommended sizing and spacing</span></span>

![<span data-ttu-id="89fc5-302">Abbildung von einzeiligen und zweizeiligen Textfeldern</span><span class="sxs-lookup"><span data-stu-id="89fc5-302">figure of one-line and two-line text boxes</span></span> ](images/ctrl-text-boxes-image25.png)

<span data-ttu-id="89fc5-303">Empfohlene Größe und Abstände für Textfelder.</span><span class="sxs-lookup"><span data-stu-id="89fc5-303">Recommended sizing and spacing for text boxes.</span></span>

<span data-ttu-id="89fc5-304">Die Breite eines Textfelds ist ein visueller Hinweis auf die erwartete Eingabe Größe.</span><span class="sxs-lookup"><span data-stu-id="89fc5-304">The width of a text box is a visual clue of the expected input size.</span></span> <span data-ttu-id="89fc5-305">Beim Anpassen von Textfeldern:</span><span class="sxs-lookup"><span data-stu-id="89fc5-305">When sizing text boxes:</span></span>

-   <span data-ttu-id="89fc5-306">**Wählen Sie eine Breite aus, die für die längsten gültigen Daten geeignet ist.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-306">**Choose a width appropriate for the longest valid data.**</span></span> <span data-ttu-id="89fc5-307">In den meisten Fällen sollten Benutzer keinen Bildlauf der längsten wahrscheinlichen Zeichenfolge durchführen, die Sie eingeben oder anzeigen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-307">In most situations, users shouldn't have to scroll the longest likely string they'll enter or view.</span></span>
-   <span data-ttu-id="89fc5-308">**Fügen Sie zusätzliche 30 Prozent** (bis zu 200 Prozent für kürzerer Text) für Text (aber nicht zahlen) ein, der lokalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="89fc5-308">**Include an additional 30 percent** (up to 200 percent for shorter text) for any text (but not numbers) that will be localized.</span></span>
-   <span data-ttu-id="89fc5-309">**Wenn die erwartete Eingabe keine bestimmte Größe hat, wählen Sie eine Breite aus, die mit den anderen Textfeldern oder Steuerelementen im Fenster konsistent ist.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-309">**If the expected input has no particular size, choose a width that is consistent with the other text boxes or controls on the window.**</span></span>
-   <span data-ttu-id="89fc5-310">**Größe für mehrzeilige Textfelder, um eine ganzzahlige Anzahl von Textzeilen anzuzeigen.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-310">**Size multi-line text boxes to display an integral number of lines of text.**</span></span>

## <a name="labels"></a><span data-ttu-id="89fc5-311">Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="89fc5-311">Labels</span></span>

### <a name="text-box-labels"></a><span data-ttu-id="89fc5-312">Text Feld Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="89fc5-312">Text box labels</span></span>

-   <span data-ttu-id="89fc5-313">Alle Textfelder benötigen Bezeichnungen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-313">All text boxes need labels.</span></span> <span data-ttu-id="89fc5-314">Schreiben Sie die Bezeichnung als Wort oder Ausdruck, nicht als Satz, enden Sie mit einem Doppelpunkt, und verwenden Sie [statischen Text](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="89fc5-314">Write the label as a word or phrase, not as a sentence, ending with a colon, and using [static text](glossary.md).</span></span>

    <span data-ttu-id="89fc5-315">**Ausnahmen:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-315">**Exceptions:**</span></span>

    -   <span data-ttu-id="89fc5-316">Text Felder mit Eingabe Aufforderungen, die sich in einem Premium-Bereich befinden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-316">Text boxes with prompts located where space is at a premium.</span></span>
    -   <span data-ttu-id="89fc5-317">Bei der Bezeichnung sollte eine Gruppe von Textfeldern, die für **formatierte Dateneingaben** verwendet werden, als einzelnes Textfeld behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-317">For labeling, a group of text boxes used for **formatted data input** should be treated as a single text box.</span></span>
    -   <span data-ttu-id="89fc5-318">Wenn ein Textfeld einem Optionsfeld oder Kontrollkästchen untergeordnet ist und durch seine Bezeichnung mit einem Doppelpunkt vorangestellt wird, sollten Sie keine zusätzliche Bezeichnung für das Textfeld einfügen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-318">If a text box is subordinate to a radio button or check box, and is introduced by its label ending with a colon, don't put an additional label on the text box.</span></span>
    -   <span data-ttu-id="89fc5-319">**Lassen Sie Steuerelement Bezeichnungen aus, die die main-Anweisung wiedergeben.**</span><span class="sxs-lookup"><span data-stu-id="89fc5-319">**Omit control labels that restate the main instruction.**</span></span> <span data-ttu-id="89fc5-320">In diesem Fall nimmt die main-Anweisung den Doppelpunkt (es sei denn, es handelt sich um eine Frage) und den Zugriffsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="89fc5-320">In this case, the main instruction takes the colon (unless it's a question) and access key.</span></span>

        <span data-ttu-id="89fc5-321">**Annehmbar:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-321">**Acceptable:**</span></span>

        ![Screenshot des Textfelds mit wiederhollicher Bezeichnung](images/ctrl-text-boxes-image26.png)

        <span data-ttu-id="89fc5-323">In diesem Beispiel ist die Textfeld-Bezeichnung lediglich eine erneute Anweisung der Main-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="89fc5-323">In this example, the text box label is just a restatement of the main instruction.</span></span>

        <span data-ttu-id="89fc5-324">**Besserer**</span><span class="sxs-lookup"><span data-stu-id="89fc5-324">**Better:**</span></span>

        ![<span data-ttu-id="89fc5-325">Screenshot des Textfelds mit Haupt Anweisung</span><span class="sxs-lookup"><span data-stu-id="89fc5-325">screen shot of text box with main instruction only</span></span> ](images/ctrl-text-boxes-image27.png)

        <span data-ttu-id="89fc5-326">In diesem Beispiel wird die redundante Bezeichnung entfernt, sodass die Haupt Anweisung den Doppelpunkt und die Zugriffstaste übernimmt.</span><span class="sxs-lookup"><span data-stu-id="89fc5-326">In this example, the redundant label is removed, so the main instruction takes the colon and access key.</span></span>

-   <span data-ttu-id="89fc5-327">Weisen Sie einen eindeutigen Zugriffsschlüssel zu.</span><span class="sxs-lookup"><span data-stu-id="89fc5-327">Assign a unique access key.</span></span> <span data-ttu-id="89fc5-328">Richtlinien für die Zugriffsschlüssel Zuweisung finden Sie unter [Tastatur](inter-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="89fc5-328">For access key assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="89fc5-329">Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="89fc5-329">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="89fc5-330">Positionieren Sie die Bezeichnung entweder links neben dem Textfeld, und richten Sie die Bezeichnung am linken Rand des Textfelds aus.</span><span class="sxs-lookup"><span data-stu-id="89fc5-330">Position the label either to the left of or above the text box, and align the label with the left edge of the text box.</span></span> <span data-ttu-id="89fc5-331">Wenn sich die Bezeichnung auf der linken Seite befindet, richten Sie den Beschriftungs Text vertikal mit dem Text Feld Text aus.</span><span class="sxs-lookup"><span data-stu-id="89fc5-331">If the label is on the left, vertically align the label text with the text box text.</span></span>

    <span data-ttu-id="89fc5-332">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-332">**Correct:**</span></span>

    ![<span data-ttu-id="89fc5-333">Screenshot der linksbündig ausgerichteten Bezeichnung oberhalb des Textfelds</span><span class="sxs-lookup"><span data-stu-id="89fc5-333">screen shot of left-aligned label above text box</span></span> ](images/ctrl-text-boxes-image28.png)

    ![<span data-ttu-id="89fc5-334">Screenshot der Text ausgerichteten Bezeichnung links vom Textfeld</span><span class="sxs-lookup"><span data-stu-id="89fc5-334">screen shot of text-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image29.png)

    <span data-ttu-id="89fc5-335">In diesen Beispielen richtet sich die Bezeichnung am oberen Rand am linken Rand des Textfelds, und die Bezeichnung auf der linken Seite richtet sich nach dem Text im Textfeld.</span><span class="sxs-lookup"><span data-stu-id="89fc5-335">In these examples, the label on top aligns with the left edge of the text box, and the label on the left aligns with the text in the text box.</span></span>

    <span data-ttu-id="89fc5-336">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-336">**Incorrect:**</span></span>

    ![<span data-ttu-id="89fc5-337">Screenshot der Text ausgerichteten Bezeichnung oberhalb des Textfelds</span><span class="sxs-lookup"><span data-stu-id="89fc5-337">screen shot of text-aligned label above text box</span></span> ](images/ctrl-text-boxes-image30.png)

    ![<span data-ttu-id="89fc5-338">Screenshot der oben ausgerichteten Bezeichnung links vom Textfeld</span><span class="sxs-lookup"><span data-stu-id="89fc5-338">screen shot of top-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image31.png)

    <span data-ttu-id="89fc5-339">In diesen falschen Beispielen richtet sich die Bezeichnung oben mit dem Text im Textfeld, und die Bezeichnung auf der linken Seite richtet sich nach dem oberen Rand des Textfelds.</span><span class="sxs-lookup"><span data-stu-id="89fc5-339">In these incorrect examples, the label on top aligns with the text in the text box, and the label on the left aligns with the top of the text box.</span></span>

-   <span data-ttu-id="89fc5-340">Sie können Einheiten (z. b. Sekunden oder Verbindungen) in Klammern hinter der Bezeichnung angeben.</span><span class="sxs-lookup"><span data-stu-id="89fc5-340">You may specify units (for example, seconds or connections) in parentheses after the label.</span></span>
-   <span data-ttu-id="89fc5-341">Wenn ein Textfeld eine beliebig kleine maximale Anzahl von Zeichen akzeptiert, können Sie die maximale Eingabe in der Bezeichnung angeben.</span><span class="sxs-lookup"><span data-stu-id="89fc5-341">If a text box accepts an arbitrarily small maximum number of characters, you can state the maximum input in the label.</span></span> <span data-ttu-id="89fc5-342">Die Breite des Textfelds sollte außerdem die maximale Größe vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-342">The text box width should also suggest the maximum size.</span></span>

    ![<span data-ttu-id="89fc5-343">Screenshot des Kennworts (Textfeld)</span><span class="sxs-lookup"><span data-stu-id="89fc5-343">screen shot of password text box</span></span> ](images/ctrl-text-boxes-image32.png)

    <span data-ttu-id="89fc5-344">In diesem Beispiel gibt die Bezeichnung die maximale Anzahl von Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="89fc5-344">In this example, the label gives the maximum number of characters.</span></span>

-   <span data-ttu-id="89fc5-345">Machen Sie den Inhalt des Textfelds (oder seiner Einheiten Bezeichnung) nicht Teil eines Satzes, da dies nicht lokalisierbar ist.</span><span class="sxs-lookup"><span data-stu-id="89fc5-345">Don't make the content of the text box (or its units label) part of a sentence, because this is not localizable.</span></span>
-   <span data-ttu-id="89fc5-346">Wenn das Textfeld verwendet werden kann, um mehrere Elemente einzugeben, legen Sie fest, wie die Elemente in der Bezeichnung getrennt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-346">If the text box can be used to enter several items, make it clear how to separate the items in the label.</span></span>

    ![<span data-ttu-id="89fc5-347">Screenshot der Bezeichnung von separaten Namen mit Semikolon</span><span class="sxs-lookup"><span data-stu-id="89fc5-347">screen shot of label separate names with semicolon</span></span> ](images/ctrl-text-boxes-image33.png)

    <span data-ttu-id="89fc5-348">In diesem Beispiel wird das Element Trennzeichen in der Bezeichnung angegeben.</span><span class="sxs-lookup"><span data-stu-id="89fc5-348">In this example, the item separator is given in the label.</span></span>

-   <span data-ttu-id="89fc5-349">Richtlinien zum Angeben der erforderlichen Eingabe finden Sie unter erforderliche Eingabe in [Dialog Feldern](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="89fc5-349">For guidelines on indicating required input, see Required input in [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="instruction-labels"></a><span data-ttu-id="89fc5-350">Anweisungs Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="89fc5-350">Instruction labels</span></span>

-   <span data-ttu-id="89fc5-351">Wenn Sie Anweisungs Text über ein Textfeld hinzufügen müssen, fügen Sie ihn oberhalb der Bezeichnung hinzu.</span><span class="sxs-lookup"><span data-stu-id="89fc5-351">If you need to add instructional text about a text box, add it above the label.</span></span> <span data-ttu-id="89fc5-352">Verwenden Sie vollständige Sätze mit endinterpunktions Zeichen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-352">Use complete sentences with ending punctuation.</span></span>
-   <span data-ttu-id="89fc5-353">Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="89fc5-353">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="89fc5-354">Zusätzliche Informationen, die hilfreich, aber nicht erforderlich sind, sollten kurz gehalten werden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-354">Additional information that is helpful but not necessary should be kept short.</span></span> <span data-ttu-id="89fc5-355">Legen Sie diese Informationen entweder in Klammern zwischen der Bezeichnung und dem Doppelpunkt oder ohne Klammern unterhalb des Textfelds ab.</span><span class="sxs-lookup"><span data-stu-id="89fc5-355">Place this information either in parentheses between the label and colon, or without parentheses below the text box.</span></span>

    ![<span data-ttu-id="89fc5-356">Screenshot der hinzugefügten Informationen unten im Textfeld</span><span class="sxs-lookup"><span data-stu-id="89fc5-356">screen shot of added information below text box</span></span> ](images/ctrl-text-boxes-image34.png)

    <span data-ttu-id="89fc5-357">In diesem Beispiel werden unter dem Textfeld zusätzliche Informationen eingefügt.</span><span class="sxs-lookup"><span data-stu-id="89fc5-357">In this example, additional information is placed below the text box.</span></span>

### <a name="prompt-labels"></a><span data-ttu-id="89fc5-358">Bezeichnungen Aufforderungs Zeichen</span><span class="sxs-lookup"><span data-stu-id="89fc5-358">Prompt labels</span></span>

-   <span data-ttu-id="89fc5-359">Halten Sie den Text der Eingabeaufforderung kurz.</span><span class="sxs-lookup"><span data-stu-id="89fc5-359">Keep the prompt text concise.</span></span> <span data-ttu-id="89fc5-360">Sie können Fragmente anstelle von vollständigen Sätzen verwenden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-360">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="89fc5-361">Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="89fc5-361">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="89fc5-362">Verwenden Sie keine endinterpunktions Zeichen oder Ellipsen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-362">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="89fc5-363">Wenn die Eingabeaufforderung Benutzer zur Eingabe von Informationen auffordert, die durch eine Schaltfläche neben dem Textfeld bearbeitet werden, platzieren Sie einfach die Schaltfläche neben dem Textfeld.</span><span class="sxs-lookup"><span data-stu-id="89fc5-363">If the prompt directs users to enter information that will be acted upon by a button next to the text box, simply place the button next to the text box.</span></span> <span data-ttu-id="89fc5-364">Verwenden Sie die Eingabeaufforderung nicht, um Benutzer zum Klicken auf die Schaltfläche zu leiten (schreiben Sie z. b. keinen Eingabe Aufforderungs Text, und klicken Sie dann auf Senden).</span><span class="sxs-lookup"><span data-stu-id="89fc5-364">Don't use the prompt to direct users to click the button (for example, don't write prompt text that says, Drag a file and then click Send).</span></span>

## <a name="documentation"></a><span data-ttu-id="89fc5-365">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="89fc5-365">Documentation</span></span>

<span data-ttu-id="89fc5-366">Beim Verweisen auf Textfelder:</span><span class="sxs-lookup"><span data-stu-id="89fc5-366">When referring to text boxes:</span></span>

-   <span data-ttu-id="89fc5-367">Verwenden Sie den Typ, um auf Benutzerinteraktionen zu verweisen, die eine Typisierung oder Einfügen erfordern. Andernfalls verwenden Sie die EINGABETASTE, wenn Benutzer mithilfe anderer Methoden Informationen in das Textfeld einfügen können, z. b. das Auswählen des Werts aus einer Liste oder das Verwenden einer Schaltfläche Durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-367">Use type to refer to user interactions that require typing or pasting; otherwise use enter if users can put information into the text box using other means, such as selecting the value from a list or using a Browse button.</span></span>
-   <span data-ttu-id="89fc5-368">Verwenden Sie SELECT, um auf einen Eintrag in einem schreibgeschützten Textfeld zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-368">Use select to refer to an entry in a read-only text box.</span></span>
-   <span data-ttu-id="89fc5-369">Verwenden Sie den genauen Bezeichnungs Text einschließlich der Groß-und Kleinschreibung, und schließen Sie das Textfeld ein.</span><span class="sxs-lookup"><span data-stu-id="89fc5-369">Use the exact label text, including its capitalization, and include the word box.</span></span> <span data-ttu-id="89fc5-370">Fügen Sie den Unterstrich oder Doppelpunkt des Zugriffsschlüssels nicht ein.</span><span class="sxs-lookup"><span data-stu-id="89fc5-370">Don't include the access key underscore or colon.</span></span> <span data-ttu-id="89fc5-371">Verweisen Sie nicht auf ein Textfeld als Textfeld oder Feld.</span><span class="sxs-lookup"><span data-stu-id="89fc5-371">Don't refer to a text box as a text box or a field.</span></span>
-   <span data-ttu-id="89fc5-372">Formatieren Sie nach Möglichkeit die Bezeichnung mit fettem Text.</span><span class="sxs-lookup"><span data-stu-id="89fc5-372">When possible, format the label using bold text.</span></span> <span data-ttu-id="89fc5-373">Andernfalls sollten Sie die Bezeichnung nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="89fc5-373">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

    <span data-ttu-id="89fc5-374">Beispiel: Geben Sie Ihr Kennwort in das Feld **Kennwort ein** , und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="89fc5-374">Example: Type your password into the **Password** box, and then click **OK**.</span></span>

-   <span data-ttu-id="89fc5-375">Wenn für das Textfeld ein bestimmtes Format erforderlich ist, sollten Sie nur das am häufigsten verwendete akzeptable Format dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="89fc5-375">If the text box requires a specific format, document only the most commonly used acceptable format.</span></span> <span data-ttu-id="89fc5-376">Ermöglichen Sie Benutzern, beliebige andere Formate selbst zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-376">Let users discover any other formats on their own.</span></span> <span data-ttu-id="89fc5-377">Sie möchten mit Datenformaten flexibel sein, aber dies sollte nicht zu einer komplexen Dokumentation führen.</span><span class="sxs-lookup"><span data-stu-id="89fc5-377">You want to be flexible with data formats, but doing so should not result in complex documentation.</span></span>

    <span data-ttu-id="89fc5-378">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-378">**Correct:**</span></span>

    <span data-ttu-id="89fc5-379">Geben Sie die Seriennummer des Teils mit dem 1234-56-7890-Format ein.</span><span class="sxs-lookup"><span data-stu-id="89fc5-379">Enter the part's serial number using the 1234-56-7890 format.</span></span>

    <span data-ttu-id="89fc5-380">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="89fc5-380">**Incorrect:**</span></span>

    <span data-ttu-id="89fc5-381">Geben Sie die Seriennummer des Teils in einem der folgenden Formate ein:</span><span class="sxs-lookup"><span data-stu-id="89fc5-381">Enter the part's serial number using any of the following formats:</span></span>

    <span data-ttu-id="89fc5-382">1234567890</span><span class="sxs-lookup"><span data-stu-id="89fc5-382">1234567890</span></span>

    <span data-ttu-id="89fc5-383">1234-56-7890</span><span class="sxs-lookup"><span data-stu-id="89fc5-383">1234-56-7890</span></span>

    <span data-ttu-id="89fc5-384">1234 56 7890</span><span class="sxs-lookup"><span data-stu-id="89fc5-384">1234 56 7890</span></span>

