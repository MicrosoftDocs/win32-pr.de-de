---
title: Interagieren mit der aktuellen Auswahl
description: Der Benutzer kann Text in einem Rich-Edit-Steuerelement mit der Maus oder der Tastatur auswählen.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec776ab0c8e07bb61dcc0e12d13af46b17d094a
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724281"
---
# <a name="how-to-interact-with-the-current-selection"></a><span data-ttu-id="aed57-103">Interagieren mit der aktuellen Auswahl</span><span class="sxs-lookup"><span data-stu-id="aed57-103">How to Interact with the Current Selection</span></span>

<span data-ttu-id="aed57-104">Der Benutzer kann Text in einem Rich-Edit-Steuerelement mit der Maus oder der Tastatur auswählen.</span><span class="sxs-lookup"><span data-stu-id="aed57-104">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="aed57-105">Bei der *aktuellen Auswahl* handelt es sich um den Bereich der ausgewählten Zeichen oder um die Position der Einfügemarke, wenn keine Zeichen ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="aed57-105">The *current selection* is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="aed57-106">Eine Anwendung kann Informationen über die aktuelle Auswahl, die Festlegung, den Zeitpunkt der Änderung und das Anzeigen oder Ausblenden der Auswahl Markierung erhalten.</span><span class="sxs-lookup"><span data-stu-id="aed57-106">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="aed57-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="aed57-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="aed57-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="aed57-108">Technologies</span></span>

-   [<span data-ttu-id="aed57-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="aed57-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="aed57-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="aed57-110">Prerequisites</span></span>

-   <span data-ttu-id="aed57-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="aed57-111">C/C++</span></span>
-   <span data-ttu-id="aed57-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="aed57-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="aed57-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="aed57-113">Instructions</span></span>

### <a name="interact-with-the-current-selection"></a><span data-ttu-id="aed57-114">Mit der aktuellen Auswahl interagieren</span><span class="sxs-lookup"><span data-stu-id="aed57-114">Interact with the Current Selection</span></span>

<span data-ttu-id="aed57-115">Um die aktuelle Auswahl in einem Rich-Edit-Steuerelement zu ermitteln, verwenden Sie die [**EM \_ exgetsel**](em-exgetsel.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="aed57-115">To determine the current selection in a rich edit control, use the [**EM\_EXGETSEL**](em-exgetsel.md) message.</span></span> <span data-ttu-id="aed57-116">Um die aktuelle Auswahl festzulegen, verwenden Sie die Nachricht [**EM \_ exsetsel**](em-exsetsel.md) .</span><span class="sxs-lookup"><span data-stu-id="aed57-116">To set the current selection, use the [**EM\_EXSETSEL**](em-exsetsel.md) message.</span></span> <span data-ttu-id="aed57-117">Die [**charrange**](/windows/desktop/api/Richedit/ns-richedit-charrange) -Struktur wird mit beiden Nachrichten verwendet und gibt einen Bereich von Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="aed57-117">The [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure is used with both messages and specifies a range of characters.</span></span> <span data-ttu-id="aed57-118">Zum Abrufen von Informationen über den Inhalt der aktuellen Auswahl können Sie die Nachricht [**EM \_ SelectionType**](em-selectiontype.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="aed57-118">To retrieve information about the contents of the current selection, you can use the [**EM\_SELECTIONTYPE**](em-selectiontype.md) message.</span></span>

<span data-ttu-id="aed57-119">Eine Anwendung kann erkennen, wenn sich die aktuelle Auswahl ändert, indem Sie den [en \_ selChange](en-selchange.md) -Benachrichtigungs Code verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="aed57-119">An application can detect when the current selection changes by processing the [EN\_SELCHANGE](en-selchange.md) notification code.</span></span> <span data-ttu-id="aed57-120">Der Benachrichtigungs Code gibt eine [**selChange**](/windows/desktop/api/Richedit/ns-richedit-selchange) -Struktur an, die Informationen über die neue Auswahl enthält.</span><span class="sxs-lookup"><span data-stu-id="aed57-120">The notification code specifies a [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that contains information about the new selection.</span></span> <span data-ttu-id="aed57-121">Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code nur dann, wenn Sie ihn mithilfe der Nachricht [**EM \_ SetEventMask**](em-seteventmask.md) aktivieren.</span><span class="sxs-lookup"><span data-stu-id="aed57-121">A rich edit control sends this notification code only if you enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="aed57-122">Standardmäßig wird ein Rich-Edit-Steuerelement angezeigt und ausgeblendet, wenn es den Fokus erhält und den Fokus verliert.</span><span class="sxs-lookup"><span data-stu-id="aed57-122">By default, a rich edit control shows and hides the selection highlight when it gains and loses the focus.</span></span> <span data-ttu-id="aed57-123">Sie können die Auswahl Markierung jederzeit anzeigen oder ausblenden, indem Sie die " [**EM \_ HideSelection**](em-hideselection.md) "-Meldung verwenden.</span><span class="sxs-lookup"><span data-stu-id="aed57-123">You can show or hide the selection highlight at any time by using the [**EM\_HIDESELECTION**](em-hideselection.md) message.</span></span> <span data-ttu-id="aed57-124">Beispielsweise kann eine Anwendung ein Such Dialogfeld bereitstellen, um Text in einem Rich-Edit-Steuerelement zu finden.</span><span class="sxs-lookup"><span data-stu-id="aed57-124">For example, an application might provide a Search dialog box to find text in a rich edit control.</span></span> <span data-ttu-id="aed57-125">Die Anwendung wählt den übereinstimmenden Text aus, ohne das Dialogfeld zu schließen. in diesem Fall muss Sie die " **EM \_ HideSelection** "-Meldung verwenden, um die Auswahl hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="aed57-125">The application might select matching text without closing the dialog box, in which case it must use the **EM\_HIDESELECTION** message to highlight the selection.</span></span>

<span data-ttu-id="aed57-126">Wie bei den Bearbeitungs Steuerelementen können Sie auch den Fenster Stil " [**es \_ nohidesel**](edit-control-styles.md) " angeben, um zu verhindern, dass ein Rich Edit-Steuerelement die Auswahl Markierung ausblenden kann, wenn es den Fokus verliert.</span><span class="sxs-lookup"><span data-stu-id="aed57-126">As with edit controls, you can specify the [**ES\_NOHIDESEL**](edit-control-styles.md) window style to prevent a rich edit control from hiding the selection highlight when it loses the focus.</span></span>

<span data-ttu-id="aed57-127">Als Alternative zur Verwendung der Nachrichten " [**EM \_ exgetsel**](em-exgetsel.md) " und " [**EM \_ exsetsel**](em-exsetsel.md) " können Sie die aktuelle Auswahl mithilfe der Nachrichten " [**EM \_ GetSEL**](em-getsel.md) " und " [**EM \_ SetSel**](em-setsel.md) Edit Control" abrufen und festlegen.</span><span class="sxs-lookup"><span data-stu-id="aed57-127">As an alternative to using the [**EM\_EXGETSEL**](em-exgetsel.md) and [**EM\_EXSETSEL**](em-exsetsel.md) messages, you can retrieve and set the current selection by using the [**EM\_GETSEL**](em-getsel.md) and [**EM\_SETSEL**](em-setsel.md) edit control messages.</span></span> <span data-ttu-id="aed57-128">Die **\_ GetSEL-GetSEL** -Nachricht verpackt 2 16-Bit-Zeichen Indizes in ihren 32-Bit-Rückgabewert und funktioniert daher nur für die Auswahl, die vollständig innerhalb des ersten 64K liegen.</span><span class="sxs-lookup"><span data-stu-id="aed57-128">The **EM\_GETSEL** message packs two 16-bit character indexes into its 32-bit return value and therefore, works only for selections that fall entirely within the first 64K.</span></span> <span data-ttu-id="aed57-129">Ein Rich Edit-Steuerelement enthält jedoch nie mehr als 32 KB Text, es sei denn, Sie erweitern diesen Grenzwert mithilfe der [**EM- \_ Begrenzungs Text**](em-limittext.md) -oder der [**EM \_ exlimittext**](em-exlimittext.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="aed57-129">However, a rich edit control will never contain more than 32K characters of text, unless you extend this limit by using the [**EM\_LIMITTEXT**](em-limittext.md) or [**EM\_EXLIMITTEXT**](em-exlimittext.md) message.</span></span> <span data-ttu-id="aed57-130">Für eine Auswahl, die über den ersten 64 KB-Text hinausgeht, gibt die **EM \_ GetSEL** -Nachricht – 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="aed57-130">For selections that extend beyond the first 64 KB of text, the **EM\_GETSEL** message returns –1.</span></span> <span data-ttu-id="aed57-131">In einem solchen Fall können Sie weiterhin die Werte verwenden, die in *wParam* und *LPARAM* zurückgegeben werden, um die Start-und Endzeichen der Auswahl zu suchen.</span><span class="sxs-lookup"><span data-stu-id="aed57-131">In such a case you can still use the values that are returned in *wParam* and *lParam* to find the start and end characters of the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aed57-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aed57-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aed57-133">Verwenden von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="aed57-133">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="aed57-134">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="aed57-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




