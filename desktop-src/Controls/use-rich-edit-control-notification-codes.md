---
title: Verwenden von Benachrichtigungs Codes für Rich-Edit-Steuerelemente
description: Das übergeordnete Fenster eines Rich-Edit-Steuer Elements kann Benachrichtigungs Codes verarbeiten, um Ereignisse zu überwachen, die das Steuerelement Rich Edit-Steuerelemente unterstützen alle Benachrichtigungs Codes, die mit Bearbeitungs Steuerelementen verwendet werden, sowie mehrere zusätzliche.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68e510bf7c5abe6109862a01d8926c8956736f9
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103948531"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a><span data-ttu-id="d820e-104">Verwenden von Benachrichtigungs Codes für Rich-Edit-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d820e-104">How to Use Rich Edit Control Notification Codes</span></span>

<span data-ttu-id="d820e-105">Das übergeordnete Fenster eines Rich-Edit-Steuer Elements kann Benachrichtigungs Codes verarbeiten, um Ereignisse zu überwachen, die das Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d820e-105">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="d820e-106">Rich Edit-Steuerelemente unterstützen alle Benachrichtigungs Codes, die mit Bearbeitungs Steuerelementen verwendet werden, sowie mehrere zusätzliche.</span><span class="sxs-lookup"><span data-stu-id="d820e-106">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d820e-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="d820e-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d820e-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="d820e-108">Technologies</span></span>

-   [<span data-ttu-id="d820e-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d820e-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d820e-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d820e-110">Prerequisites</span></span>

-   <span data-ttu-id="d820e-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="d820e-111">C/C++</span></span>
-   <span data-ttu-id="d820e-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d820e-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d820e-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="d820e-113">Instructions</span></span>

### <a name="use-a-rich-edit-control-notification-code"></a><span data-ttu-id="d820e-114">Verwenden eines Rich-Edit-Steuerelement-Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="d820e-114">Use a Rich Edit Control Notification Code</span></span>

<span data-ttu-id="d820e-115">Sie können bestimmen, welche Benachrichtigungs Codes von einem Rich Edit-Steuerelement durch Festlegen seiner Ereignis Maske an das übergeordnete Fenster gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d820e-115">You can determine which notification codes a rich edit control sends its parent window by setting its event mask.</span></span> <span data-ttu-id="d820e-116">Um die Ereignis Maske für ein Rich-Edit-Steuerelement festzulegen, verwenden Sie die Nachricht [**EM \_ SetEventMask**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="d820e-116">To set the event mask for a rich edit control, use the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="d820e-117">Sie können die aktuelle Ereignis Maske für ein Rich Edit-Steuerelement mithilfe der [**EM \_ GetEventMask**](em-geteventmask.md) -Nachricht abrufen.</span><span class="sxs-lookup"><span data-stu-id="d820e-117">You can retrieve the current event mask for a rich edit control by using the [**EM\_GETEVENTMASK**](em-geteventmask.md) message.</span></span> <span data-ttu-id="d820e-118">Eine Liste der Ereignismasken-Flags finden Sie unter [Rich Edit Control Event Mask Flags](rich-edit-control-event-mask-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d820e-118">For a list of event mask flags, see [Rich Edit Control Event Mask Flags](rich-edit-control-event-mask-flags.md).</span></span>

<span data-ttu-id="d820e-119">Das übergeordnete Fenster eines Rich-Edit-Steuer Elements kann alle Tastatur-und Maus Eingaben für das Steuerelement filtern, indem der [en \_ msgfilter](en-msgfilter.md) -Benachrichtigungs Code verarbeitet wird</span><span class="sxs-lookup"><span data-stu-id="d820e-119">A rich edit control's parent window can filter all keyboard and mouse input to the control by processing the [EN\_MSGFILTER](en-msgfilter.md) notification code.</span></span> <span data-ttu-id="d820e-120">Das übergeordnete Fenster kann die Verarbeitung der Tastatur-oder Maus Meldung verhindern oder die Meldung ändern, indem die angegebene [**msgfilter**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) -Struktur geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d820e-120">The parent window can prevent the keyboard or mouse message from being processed or can change the message by modifying the specified [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure.</span></span>

<span data-ttu-id="d820e-121">Eine Anwendung kann den von [en \_ geschützten](en-protected.md) Benachrichtigungs Code verarbeiten, um zu erkennen, wann der Benutzer versucht, geschützten Text zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d820e-121">An application can process the [EN\_PROTECTED](en-protected.md) notification code to detect when the user attempts to modify protected text.</span></span> <span data-ttu-id="d820e-122">Um einen Textbereich als geschützt zu markieren, können Sie den Effekt geschützter Zeichen festlegen.</span><span class="sxs-lookup"><span data-stu-id="d820e-122">To mark a range of text as protected, you can set the protected character effect.</span></span>

<span data-ttu-id="d820e-123">Sie können es Benutzern ermöglichen, Dateien in einem Rich-Edit-Steuerelement zu löschen, indem Sie den [en \_ dropfiles](en-dropfiles.md) -Benachrichtigungs Code verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d820e-123">You can enable the user to drop files in a rich edit control by processing the [EN\_DROPFILES](en-dropfiles.md) notification code.</span></span> <span data-ttu-id="d820e-124">Die angegebene [**endropfiles**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) -Struktur enthält Informationen zu den Dateien, die gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="d820e-124">The specified [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure contains information about the files that are being dropped.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d820e-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d820e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d820e-126">Verwenden von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="d820e-126">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="d820e-127">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="d820e-127">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




