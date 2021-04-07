---
title: Formatieren von Text in Rich Edit-Steuerelementen
description: Eine Anwendung kann Nachrichten an ein Rich Edit-Steuerelement senden, um Zeichen und Absätze zu formatieren und Formatierungsinformationen abzurufen.
ms.assetid: 19A4F0D1-88C5-407D-A70F-CB486DAD352E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246c6309dec94538f47ed9ca7e464f1d6d17f240
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724284"
---
# <a name="how-to-format-text-in-rich-edit-controls"></a><span data-ttu-id="1f499-103">Formatieren von Text in Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="1f499-103">How to Format Text in Rich Edit Controls</span></span>

<span data-ttu-id="1f499-104">Eine Anwendung kann Nachrichten an ein Rich Edit-Steuerelement senden, um Zeichen und Absätze zu formatieren und Formatierungsinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1f499-104">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="1f499-105">Die Attribute für die Absatz Formatierung umfassen Ausrichtung, Tabstopps, Einzüge, Nummerierungen und einfache Tabellen.</span><span class="sxs-lookup"><span data-stu-id="1f499-105">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="1f499-106">Für Zeichen können Sie Schriftart Name, Größe, Farbe und Effekte angeben, z. b. Fett, kursiv und geschützt.</span><span class="sxs-lookup"><span data-stu-id="1f499-106">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1f499-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="1f499-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1f499-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="1f499-108">Technologies</span></span>

-   [<span data-ttu-id="1f499-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="1f499-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1f499-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1f499-110">Prerequisites</span></span>

-   <span data-ttu-id="1f499-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="1f499-111">C/C++</span></span>
-   <span data-ttu-id="1f499-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="1f499-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1f499-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="1f499-113">Instructions</span></span>

### <a name="format-text-in-a-rich-edit-control"></a><span data-ttu-id="1f499-114">Formatieren von Text in einem Rich-Edit-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="1f499-114">Format Text in a Rich Edit Control</span></span>

<span data-ttu-id="1f499-115">Sie können die Absatz Formatierung mithilfe der [**EM- \_ SetParaFormat**](em-setparaformat.md) -Meldung anwenden.</span><span class="sxs-lookup"><span data-stu-id="1f499-115">You can apply paragraph formatting by using the [**EM\_SETPARAFORMAT**](em-setparaformat.md) message.</span></span> <span data-ttu-id="1f499-116">Um die aktuelle Absatz Formatierung für den ausgewählten Text zu ermitteln, verwenden Sie die [**EM \_ GetParaFormat**](em-getparaformat.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1f499-116">To determine the current paragraph formatting for the selected text, use the [**EM\_GETPARAFORMAT**](em-getparaformat.md) message.</span></span> <span data-ttu-id="1f499-117">Die [**paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) -oder [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) -Struktur wird mit beiden Nachrichten verwendet, um Absatz Formatierungs Attribute anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1f499-117">The [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) or [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) structure is used with both messages to specify paragraph formatting attributes.</span></span>

<span data-ttu-id="1f499-118">Sie können die Zeichen Formatierung mithilfe der [**EM- \_ setcharformat**](em-setcharformat.md) -Meldung anwenden.</span><span class="sxs-lookup"><span data-stu-id="1f499-118">You can apply character formatting by using the [**EM\_SETCHARFORMAT**](em-setcharformat.md) message.</span></span> <span data-ttu-id="1f499-119">Zum Bestimmen der aktuellen Zeichen Formatierung für den ausgewählten Text können Sie die [**EM \_ getcharformat**](em-getcharformat.md) -Meldung verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f499-119">To determine the current character formatting for the selected text, you can use the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span> <span data-ttu-id="1f499-120">Die [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) -oder [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) -Struktur wird mit beiden Nachrichten zum Angeben von Zeichen Attributen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f499-120">The [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) or [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure is used with both messages to specify character attributes.</span></span>

<span data-ttu-id="1f499-121">Sie können auch die Nachrichten [**EM \_ setcharformat**](em-setcharformat.md) und [**EM \_ getcharformat**](em-getcharformat.md) verwenden, um die Zeichen Formatierung der Einfügemarke festzulegen und abzurufen. Hierbei handelt es sich um die Formatierung, die auf alle nachträglich eingefügten Zeichen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f499-121">You can also use [**EM\_SETCHARFORMAT**](em-setcharformat.md) and [**EM\_GETCHARFORMAT**](em-getcharformat.md) messages to set and retrieve the character formatting of the insertion point, which is the formatting that is applied to any subsequently inserted characters.</span></span> <span data-ttu-id="1f499-122">Wenn eine Anwendung z. b. die Standard Zeichenformatierung auf "Fett" festlegt und der Benutzer dann ein Zeichen eingibt, ist dieses Zeichen fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="1f499-122">For example, if an application sets the default character formatting to bold and the user then types a character, that character is bold.</span></span>

<span data-ttu-id="1f499-123">Die Zeichen Formatierung der Einfügemarke wird nur dann auf den neu eingefügten Text angewendet, wenn die aktuelle Auswahl leer ist (wenn die aktuelle Auswahl eine Einfügemarke ist).</span><span class="sxs-lookup"><span data-stu-id="1f499-123">The character formatting of the insertion point is applied to newly inserted text only if the current selection is empty (if the current selection is an insertion point).</span></span> <span data-ttu-id="1f499-124">Andernfalls geht der neue Text von der Zeichen Formatierung des Texts aus, den er ersetzt.</span><span class="sxs-lookup"><span data-stu-id="1f499-124">Otherwise, the new text assumes the character formatting of the text it replaces.</span></span> <span data-ttu-id="1f499-125">Wenn sich die Auswahl ändert, ändert sich die Standard Zeichen Formatierung so, dass Sie dem ersten Zeichen in der neuen Auswahl entspricht.</span><span class="sxs-lookup"><span data-stu-id="1f499-125">If the selection changes, the default character formatting changes to match the first character in the new selection.</span></span>

<span data-ttu-id="1f499-126">Der geschützte Zeichen Effekt ist insofern eindeutig, als er die Darstellung von Text nicht ändert.</span><span class="sxs-lookup"><span data-stu-id="1f499-126">The protected character effect is unique in that it does not change the appearance of text.</span></span> <span data-ttu-id="1f499-127">Wenn der Benutzer versucht, geschützten Text zu ändern, sendet ein Rich Edit-Steuerelement sein übergeordnetes Fenster an den [ \_ geschützten](en-protected.md) Benachrichtigungs Code, sodass das übergeordnete Fenster die Änderung zulassen oder verhindern kann.</span><span class="sxs-lookup"><span data-stu-id="1f499-127">If the user attempts to modify protected text, a rich edit control sends its parent window an [EN\_PROTECTED](en-protected.md) notification code, allowing the parent window to allow or prevent the change.</span></span> <span data-ttu-id="1f499-128">Zum Empfangen dieses Benachrichtigungs Codes müssen Sie ihn mithilfe der Nachricht [**EM \_ SetEventMask**](em-seteventmask.md) aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1f499-128">To receive this notification code, you must enable it by using the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="1f499-129">Die Vordergrundfarbe ist immer ein Zeichen Attribut.</span><span class="sxs-lookup"><span data-stu-id="1f499-129">Foreground color is always a character attribute.</span></span> <span data-ttu-id="1f499-130">In Microsoft Rich Edit 1,0 ist die Hintergrundfarbe nur eine Eigenschaft des Rich Edit-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="1f499-130">In Microsoft Rich Edit 1.0, background color is only a property of the rich edit control.</span></span> <span data-ttu-id="1f499-131">Um die Standard Hintergrundfarbe festzulegen, verwenden Sie die Nachricht [**EM \_ setbkgndcolor**](em-setbkgndcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="1f499-131">To set the default background color, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span> <span data-ttu-id="1f499-132">Beachten Sie, dass Rich Edit die " [**WM \_ ctlcoloredit**](wm-ctlcoloredit.md) "-Meldung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1f499-132">Note that Rich Edit does not support the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f499-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1f499-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f499-134">Verwenden von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="1f499-134">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="1f499-135">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="1f499-135">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




