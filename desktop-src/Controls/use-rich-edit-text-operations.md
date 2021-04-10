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
# <a name="how-to-use-rich-edit-text-operations"></a>Verwenden von Rich-Text-Bearbeitungsvorgängen

Eine Anwendung kann Nachrichten senden, um Text in einem Rich-Edit-Steuerelement abzurufen oder zu suchen. Sie können entweder den ausgewählten Text oder einen angegebenen Textbereich abrufen.

Um den ausgewählten Text in einem Rich-Edit-Steuerelement zu erhalten, verwenden Sie die [**\_ GetSelText**](em-getseltext.md) -Nachricht von EM. Der Text wird in das angegebene Zeichen Array kopiert. Sie müssen sicherstellen, dass das Array groß genug ist, um den ausgewählten Text und ein abschließendes NULL-Zeichen zu speichern.

Um einen angegebenen Textbereich abzurufen, verwenden Sie die Nachricht [**EM \_ GetTextRange**](em-gettextrange.md) . Die [**TextRange**](/windows/win32/api/richedit/ns-richedit-textrangea) -Struktur, die mit dieser Meldung verwendet wird, gibt den abzurufenden Textbereich an und verweist auf ein Zeichen Array, das den Text empfängt. Hier muss die Anwendung sicherstellen, dass das Array für den angegebenen Text und ein abschließendes NULL-Zeichen groß genug ist.

Sie können in einem Rich-Edit-Steuerelement nach einer Zeichenfolge suchen, indem Sie die Nachrichten [**EM \_ FindText**](em-findtext.md) oder [**EM \_ FINDTEXTEX**](em-findtextex.md) oder ihre Unicode-Entsprechungen [**EM \_ findtextw**](em-findtextw.md) und [**EM \_ findtextexw**](em-findtextexw.md)verwenden. Die [**FindText**](/windows/win32/api/richedit/ns-richedit-findtexta) -Struktur, die mit den nicht erweiterten Versionen verwendet wird, gibt den zu suchenden Textbereich und die zu suchende Zeichenfolge an. Die erweiterten Versionen verwenden eine [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur, die die gleichen Informationen angibt und auch die Start-und Endpunkte des Zeichen Bereichs des gefundenen Texts empfängt. Sie können diese Optionen auch angeben, ob bei der Suche die Groß-/Kleinschreibung beachtet wird.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-a-rich-edit-text-operation"></a>Verwenden eines Rich-Edit-Text Vorgangs

Die folgende Beispiel Funktion sucht den angegebenen Text in dem ausgewählten Text in einem Rich-Edit-Steuerelement, das Unicode unterstützt. Wenn das Ziel gefunden wird, wird es zur neuen Auswahl.


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



## <a name="remarks"></a>Bemerkungen

Microsoft Rich Edit 3,0 unterstützt auch die Funktion "hexadeunicode Input Method Editor (IME)", die es einem Benutzer ermöglicht, mithilfe von "Hot Keys" zwischen hexadezimal und Unicode zu konvertieren. Weitere Informationen finden Sie unter [hexyunicode-IME](/windows/desktop/Intl/hextounicode-ime).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 