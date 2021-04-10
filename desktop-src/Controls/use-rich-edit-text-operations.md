---
title: Verwenden von Rich-Text-Bearbeitungsvorgängen
description: Eine Anwendung kann Nachrichten senden, um Text in einem Rich-Edit-Steuerelement abzurufen oder zu suchen. Sie können entweder den ausgewählten Text oder einen angegebenen Textbereich abrufen.
ms.assetid: 95D88F9A-3DD1-48E4-B6FF-3168F2D25846
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b54619e1ce5952b7c0d06527c6aca2402a4e714
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949162"
---
# <a name="how-to-use-rich-edit-text-operations"></a><span data-ttu-id="fc04b-104">Verwenden von Rich-Text-Bearbeitungsvorgängen</span><span class="sxs-lookup"><span data-stu-id="fc04b-104">How to Use Rich Edit Text Operations</span></span>

<span data-ttu-id="fc04b-105">Eine Anwendung kann Nachrichten senden, um Text in einem Rich-Edit-Steuerelement abzurufen oder zu suchen.</span><span class="sxs-lookup"><span data-stu-id="fc04b-105">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="fc04b-106">Sie können entweder den ausgewählten Text oder einen angegebenen Textbereich abrufen.</span><span class="sxs-lookup"><span data-stu-id="fc04b-106">You can retrieve either the selected text or a specified range of text.</span></span>

<span data-ttu-id="fc04b-107">Um den ausgewählten Text in einem Rich-Edit-Steuerelement zu erhalten, verwenden Sie die [**\_ GetSelText**](em-getseltext.md) -Nachricht von EM.</span><span class="sxs-lookup"><span data-stu-id="fc04b-107">To get the selected text in a rich edit control, use the [**EM\_GETSELTEXT**](em-getseltext.md) message.</span></span> <span data-ttu-id="fc04b-108">Der Text wird in das angegebene Zeichen Array kopiert.</span><span class="sxs-lookup"><span data-stu-id="fc04b-108">The text is copied to the specified character array.</span></span> <span data-ttu-id="fc04b-109">Sie müssen sicherstellen, dass das Array groß genug ist, um den ausgewählten Text und ein abschließendes NULL-Zeichen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fc04b-109">You must ensure that the array is large enough to hold the selected text plus a terminating null character.</span></span>

<span data-ttu-id="fc04b-110">Um einen angegebenen Textbereich abzurufen, verwenden Sie die Nachricht [**EM \_ GetTextRange**](em-gettextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="fc04b-110">To retrieve a specified range of text, use the [**EM\_GETTEXTRANGE**](em-gettextrange.md) message.</span></span> <span data-ttu-id="fc04b-111">Die [**TextRange**](/windows/win32/api/richedit/ns-richedit-textrangea) -Struktur, die mit dieser Meldung verwendet wird, gibt den abzurufenden Textbereich an und verweist auf ein Zeichen Array, das den Text empfängt.</span><span class="sxs-lookup"><span data-stu-id="fc04b-111">The [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure used with this message specifies the text range to retrieve and points to a character array that receives the text.</span></span> <span data-ttu-id="fc04b-112">Hier muss die Anwendung sicherstellen, dass das Array für den angegebenen Text und ein abschließendes NULL-Zeichen groß genug ist.</span><span class="sxs-lookup"><span data-stu-id="fc04b-112">Here again, the application must ensure that the array is large enough for the specified text plus a terminating null character.</span></span>

<span data-ttu-id="fc04b-113">Sie können in einem Rich-Edit-Steuerelement nach einer Zeichenfolge suchen, indem Sie die Nachrichten [**EM \_ FindText**](em-findtext.md) oder [**EM \_ FINDTEXTEX**](em-findtextex.md) oder ihre Unicode-Entsprechungen [**EM \_ findtextw**](em-findtextw.md) und [**EM \_ findtextexw**](em-findtextexw.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc04b-113">You can search for a string in a rich edit control by using the [**EM\_FINDTEXT**](em-findtext.md) or [**EM\_FINDTEXTEX**](em-findtextex.md) messages, or their Unicode equivalents, [**EM\_FINDTEXTW**](em-findtextw.md) and [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span> <span data-ttu-id="fc04b-114">Die [**FindText**](/windows/win32/api/richedit/ns-richedit-findtexta) -Struktur, die mit den nicht erweiterten Versionen verwendet wird, gibt den zu suchenden Textbereich und die zu suchende Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="fc04b-114">The [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure that is used with the nonextended versions specifies the text range to search and the string to search for.</span></span> <span data-ttu-id="fc04b-115">Die erweiterten Versionen verwenden eine [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur, die die gleichen Informationen angibt und auch die Start-und Endpunkte des Zeichen Bereichs des gefundenen Texts empfängt.</span><span class="sxs-lookup"><span data-stu-id="fc04b-115">The extended versions use a [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, which specifies the same information and also receives the start and end points of the character range of the found text.</span></span> <span data-ttu-id="fc04b-116">Sie können diese Optionen auch angeben, ob bei der Suche die Groß-/Kleinschreibung beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="fc04b-116">You can also specify such options as whether the search is case sensitive.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="fc04b-117">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="fc04b-117">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="fc04b-118">Technologien</span><span class="sxs-lookup"><span data-stu-id="fc04b-118">Technologies</span></span>

-   [<span data-ttu-id="fc04b-119">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="fc04b-119">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="fc04b-120">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="fc04b-120">Prerequisites</span></span>

-   <span data-ttu-id="fc04b-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="fc04b-121">C/C++</span></span>
-   <span data-ttu-id="fc04b-122">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="fc04b-122">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="fc04b-123">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="fc04b-123">Instructions</span></span>

### <a name="use-a-rich-edit-text-operation"></a><span data-ttu-id="fc04b-124">Verwenden eines Rich-Edit-Text Vorgangs</span><span class="sxs-lookup"><span data-stu-id="fc04b-124">Use a Rich Edit Text Operation</span></span>

<span data-ttu-id="fc04b-125">Die folgende Beispiel Funktion sucht den angegebenen Text in dem ausgewählten Text in einem Rich-Edit-Steuerelement, das Unicode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fc04b-125">The following example function finds the specified text within the selected text in a rich edit control that supports Unicode.</span></span> <span data-ttu-id="fc04b-126">Wenn das Ziel gefunden wird, wird es zur neuen Auswahl.</span><span class="sxs-lookup"><span data-stu-id="fc04b-126">If the target is found, it becomes the new selection.</span></span>


```C++
BOOL FindTextInSelection(HWND hRich, WCHAR* target)
{
    CHARRANGE selectionRange;
    
    SendMessage(hRich, EM_EXGETSEL, 0, (LPARAM)&selectionRange);
    
    FINDTEXTEX ftex;
    
    ftex.lpstrText  = target;
    ftex.chrg.cpMin = selectionRange.cpMin;
    ftex.chrg.cpMax = selectionRange.cpMax;
    
    LRESULT lr = SendMessage(hRich, EM_FINDTEXTEXW, (WPARAM)FR_DOWN, (LPARAM) &ftex);
    
    if (lr >= 0)
    {
        LRESULT lr1 = SendMessage(hRich, EM_EXSETSEL, 0, (LPARAM)&ftex.chrgText);
        
        SendMessage(hRich, EM_HIDESELECTION, (LPARAM)FALSE, 0);
        
        return TRUE;
    }
    
    return FALSE;
    
}
```



## <a name="remarks"></a><span data-ttu-id="fc04b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc04b-127">Remarks</span></span>

<span data-ttu-id="fc04b-128">Microsoft Rich Edit 3,0 unterstützt auch die Funktion "hexadeunicode Input Method Editor (IME)", die es einem Benutzer ermöglicht, mithilfe von "Hot Keys" zwischen hexadezimal und Unicode zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="fc04b-128">Microsoft Rich Edit 3.0 also supports the HexToUnicode Input Method Editor (IME) function, which allows a user to convert between hexadecimal and Unicode by using hot keys.</span></span> <span data-ttu-id="fc04b-129">Weitere Informationen finden Sie unter [hexyunicode-IME](/windows/desktop/Intl/hextounicode-ime).</span><span class="sxs-lookup"><span data-stu-id="fc04b-129">For more information, see [HexToUnicode IME](/windows/desktop/Intl/hextounicode-ime).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc04b-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fc04b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc04b-131">Verwenden von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="fc04b-131">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="fc04b-132">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="fc04b-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 