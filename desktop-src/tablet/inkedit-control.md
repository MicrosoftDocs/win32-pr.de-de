---
description: Das InkEdit-Steuerelement bietet eine einfache Möglichkeit, frei Hand Eingaben zu erfassen, zu erkennen und anzuzeigen.
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: InkEdit-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6d5441506ee791eefddba05b9b1f3ddb8a8ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866139"
---
# <a name="inkedit-control"></a><span data-ttu-id="a79b0-103">InkEdit-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="a79b0-103">InkEdit Control</span></span>

<span data-ttu-id="a79b0-104">Das [InkEdit](inkedit-control-reference.md) -Steuerelement bietet eine einfache Möglichkeit, frei Hand Eingaben zu erfassen, zu erkennen und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a79b0-104">The [InkEdit](inkedit-control-reference.md) control provides an easy way to capture, recognize, and display ink.</span></span>

<span data-ttu-id="a79b0-105">Diese Implementierung des [InkEdit](inkedit-control-reference.md) -Steuer Elements basiert auf dem [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) -Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a79b0-105">This implementation of the [InkEdit](inkedit-control-reference.md) control is based on the [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) control.</span></span> <span data-ttu-id="a79b0-106">Die verwaltete (.NET Framework)-Implementierung von [InkEdit](/previous-versions/ms835842(v=msdn.10)) basiert auf dem [**RichTextBox**](/previous-versions/windows/) -Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a79b0-106">The managed (.NET Framework) implementation of [InkEdit](/previous-versions/ms835842(v=msdn.10)) is based on the [**RichTextBox**](/previous-versions/windows/) control.</span></span>

<span data-ttu-id="a79b0-107">Der Hauptzweck des [InkEdit](inkedit-control-reference.md) -Steuer Elements besteht darin, frei Hand Eingaben zu erfassen, zu erkennen und in Textform anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a79b0-107">The primary purpose of the [InkEdit](inkedit-control-reference.md) control is to collect ink, recognize it, and display it in text form.</span></span> <span data-ttu-id="a79b0-108">Außerdem wird die Anzeige von frei Hand Eingaben als eingebettetes Objekt mit Text Formatierungsfunktionen unterstützt, z. b. Fett und unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="a79b0-108">Additionally, it supports displaying ink as an embedded object with text formatting capabilities, such as bold and underline.</span></span>

## <a name="gestures-and-correction"></a><span data-ttu-id="a79b0-109">Gesten und Korrektur</span><span class="sxs-lookup"><span data-stu-id="a79b0-109">Gestures and Correction</span></span>

<span data-ttu-id="a79b0-110">[InkEdit](inkedit-control-reference.md) unterstützt die folgenden Gesten.</span><span class="sxs-lookup"><span data-stu-id="a79b0-110">[InkEdit](inkedit-control-reference.md) supports the following gestures.</span></span>



| <span data-ttu-id="a79b0-111">Geste</span><span class="sxs-lookup"><span data-stu-id="a79b0-111">Gesture</span></span>                                                                    | <span data-ttu-id="a79b0-112">Gesten Name</span><span class="sxs-lookup"><span data-stu-id="a79b0-112">Gesture Name</span></span>              | <span data-ttu-id="a79b0-113">Aktion</span><span class="sxs-lookup"><span data-stu-id="a79b0-113">Action</span></span>               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![nach-links-Geste](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | <span data-ttu-id="a79b0-115">Nach unten links</span><span class="sxs-lookup"><span data-stu-id="a79b0-115">Down-left</span></span><br/>      | <span data-ttu-id="a79b0-116">EINGABETASTE</span><span class="sxs-lookup"><span data-stu-id="a79b0-116">Enter</span></span><br/>     |
| ![Bewegung nach unten links](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | <span data-ttu-id="a79b0-118">Nach unten links</span><span class="sxs-lookup"><span data-stu-id="a79b0-118">Down-left-long</span></span><br/> | <span data-ttu-id="a79b0-119">EINGABETASTE</span><span class="sxs-lookup"><span data-stu-id="a79b0-119">Enter</span></span><br/>     |
| ![Rechte Bewegung](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | <span data-ttu-id="a79b0-121">Rechts oben</span><span class="sxs-lookup"><span data-stu-id="a79b0-121">Up-right</span></span><br/>       | <span data-ttu-id="a79b0-122">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="a79b0-122">Tab</span></span><br/>       |
| ![Bewegung nach oben rechts](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | <span data-ttu-id="a79b0-124">Oben rechts</span><span class="sxs-lookup"><span data-stu-id="a79b0-124">Up-right-long</span></span><br/>  | <span data-ttu-id="a79b0-125">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="a79b0-125">Tab</span></span><br/>       |
| ![Rechte Bewegung](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | <span data-ttu-id="a79b0-127">Rechts</span><span class="sxs-lookup"><span data-stu-id="a79b0-127">Right</span></span><br/>          | <span data-ttu-id="a79b0-128">LeerZchn</span><span class="sxs-lookup"><span data-stu-id="a79b0-128">Space</span></span><br/>     |
| ![linke Bewegung](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | <span data-ttu-id="a79b0-130">Links</span><span class="sxs-lookup"><span data-stu-id="a79b0-130">Left</span></span><br/>           | <span data-ttu-id="a79b0-131">Rücktaste</span><span class="sxs-lookup"><span data-stu-id="a79b0-131">Backspace</span></span><br/> |



 

<span data-ttu-id="a79b0-132">Gesten Ereignisse, die Sie behandeln können, enthalten Gesten-, Strich-und Cursor Informationen, die Sie zum Senden von Text an [InkEdit](inkedit-control-reference.md) oder zum Platzieren von Daten in der Zwischenablage verwenden können.</span><span class="sxs-lookup"><span data-stu-id="a79b0-132">Gesture events that you can handle contain gesture, stroke, and cursor information you can use to send text to [InkEdit](inkedit-control-reference.md) or place data on the clipboard.</span></span>

<span data-ttu-id="a79b0-133">[InkEdit](inkedit-control-reference.md) bietet auch eine Korrektur Benutzeroberfläche, die es Benutzern ermöglicht, Alternativen anzuzeigen und aus Ihnen auszuwählen, die Bildschirmtastatur zu verwenden und Zeichen-/Schreib-/blockerkenzer zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a79b0-133">[InkEdit](inkedit-control-reference.md) also provides a correction user interface that enables users to view and select from alternates, use the on-screen keyboard, and character/letter/block recognizers.</span></span>

## <a name="other-details"></a><span data-ttu-id="a79b0-134">Weitere Details</span><span class="sxs-lookup"><span data-stu-id="a79b0-134">Other Details</span></span>

<span data-ttu-id="a79b0-135">[InkEdit](inkedit-control-reference.md) ist so konzipiert, dass es in einem Formular Szenario für eine einzelne Zeile sowie für die mehrzeilige Texteingabe und-Bearbeitung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="a79b0-135">[InkEdit](inkedit-control-reference.md) is designed to work well in a form scenario for single line as well as multiline text entry and editing.</span></span> <span data-ttu-id="a79b0-136">Der primäre Verwendungszweck für InkEdit besteht darin, Texteingaben von einem Benutzer in Form von Handschrift zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a79b0-136">The primary intended use for InkEdit is to get text input from a user in the form of handwriting.</span></span> <span data-ttu-id="a79b0-137">Standardmäßig wird die frei Hand Eingabe erkannt, und der Text wird an seiner Stelle eingefügt.</span><span class="sxs-lookup"><span data-stu-id="a79b0-137">By default, ink input is recognized and text is inserted in its place.</span></span> <span data-ttu-id="a79b0-138">Die Standardbenutzer Oberfläche für InkEdit ähnelt der des [**RichTextBox**](/previous-versions/windows/) -Steuer Elements, es sei denn, der Benutzer legt frei Hand Eingaben fest.</span><span class="sxs-lookup"><span data-stu-id="a79b0-138">The default user interface for InkEdit resembles that of the [**RichTextBox**](/previous-versions/windows/) control, except when the user is laying down ink.</span></span> <span data-ttu-id="a79b0-139">Sie können ursprüngliches frei Hand Eingaben anstelle von Text anzeigen. die frei Hand Eingabe wird jedoch auf die aktuelle Eingabe Schriftgröße des InkEdit-Steuer Elements skaliert und Inline mit anderem Text angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a79b0-139">You can display original ink rather than text; however, the ink is scaled to the current input font size of the InkEdit control and is displayed inline with other text.</span></span>

> [!Note]  
> <span data-ttu-id="a79b0-140">Aus Sicherheitsgründen müssen Sie Standard Prozeduren verwenden, um eine Datei zu öffnen oder zu schließen, die Eingabe/Ausgabe zu streamen und die [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) -oder [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) -Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a79b0-140">For security reasons, you must use standard procedures to open or close a file, stream the input/output, and set the [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) or [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) property.</span></span>

 

<span data-ttu-id="a79b0-141">Das [InkEdit](inkedit-control-reference.md) -Steuerelement ist so festgelegt, dass Freihand als Text standardmäßig erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="a79b0-141">The [InkEdit](inkedit-control-reference.md) control is set to recognize ink as text by default.</span></span> <span data-ttu-id="a79b0-142">Legen Sie die [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) -Eigenschaft auf **InsertAsInk** fest, damit Benutzer frei Hand Eingaben als frei Hand Eingaben hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="a79b0-142">To enable users to add ink as ink, set the [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) property to **InsertAsInk**.</span></span>

<span data-ttu-id="a79b0-143">Ausführliche Referenzinformationen zum [InkEdit](inkedit-control-reference.md) -Steuerelement finden Sie unter InkEdit.</span><span class="sxs-lookup"><span data-stu-id="a79b0-143">For detailed reference information about the [InkEdit](inkedit-control-reference.md) control, see InkEdit.</span></span>

> [!Note]  
> <span data-ttu-id="a79b0-144">Wenn Sie das Win32 [InkEdit](inkedit-control-reference.md) -Steuerelement verwenden und es in einem Gruppenfeld platzieren, stellen Sie sicher, dass das Feld einen transparenten Stil hat. Andernfalls kann InkEdit keine Freihand sammeln.</span><span class="sxs-lookup"><span data-stu-id="a79b0-144">If you use the Win32 [InkEdit](inkedit-control-reference.md) control and place it inside a group box, make sure the box has a transparent style; otherwise, InkEdit is not able to collect ink.</span></span>

 

> [!Note]  
> <span data-ttu-id="a79b0-145">Um sicherzustellen, dass frei Hand Eingaben ordnungsgemäß angezeigt werden, wenden Sie die Methode zum [**Aktualisieren**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) des [InkEdit](inkedit-control-reference.md) -Steuer Elements an, wenn es ein [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) [**-oder**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1)</span><span class="sxs-lookup"><span data-stu-id="a79b0-145">To ensure ink is displayed properly, call the [InkEdit](inkedit-control-reference.md) control [**Refresh**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) method when it receives an [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) or [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) event.</span></span>

 

<span data-ttu-id="a79b0-146">In den folgenden Abschnitten wird die Verwendung des [InkEdit](inkedit-control-reference.md) -Steuer Elements ausführlich erläutert:</span><span class="sxs-lookup"><span data-stu-id="a79b0-146">The following sections detail the use of the [InkEdit](inkedit-control-reference.md) control:</span></span>

-   [<span data-ttu-id="a79b0-147">Instanziieren von InkEdit</span><span class="sxs-lookup"><span data-stu-id="a79b0-147">Instantiating InkEdit</span></span>](instantiating-inkedit.md)
-   [<span data-ttu-id="a79b0-148">Wort und Zeichenerkennung</span><span class="sxs-lookup"><span data-stu-id="a79b0-148">Word vs. Character Recognition</span></span>](word-vs--character-recognition.md)
-   [<span data-ttu-id="a79b0-149">Anzeigen von frei Hand Eingaben</span><span class="sxs-lookup"><span data-stu-id="a79b0-149">Displaying Ink as Ink</span></span>](displaying-ink-as-ink.md)
-   [<span data-ttu-id="a79b0-150">Verwenden von InkEdit unter früheren Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="a79b0-150">Using InkEdit on Earlier Versions of Windows</span></span>](using-inkedit-on-earlier-versions-of-windows.md)
-   [<span data-ttu-id="a79b0-151">Verwenden eines Anwendungs Wörterbuchs mit InkEdit</span><span class="sxs-lookup"><span data-stu-id="a79b0-151">Using an Application Dictionary with InkEdit</span></span>](using-an-application-dictionary-with-inkedit.md)

 

