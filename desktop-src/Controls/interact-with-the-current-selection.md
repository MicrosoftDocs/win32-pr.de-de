---
title: Interagieren mit der aktuellen Auswahl
description: Der Benutzer kann Text in einem Rich-Edit-Steuerelement auswählen, indem er die Maus oder die Tastatur verwendet.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6e60ef0ba4aa9a8034256c8c272950f4983d16c0195737065563b378e14202
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434640"
---
# <a name="how-to-interact-with-the-current-selection"></a>Interagieren mit der aktuellen Auswahl

Der Benutzer kann Text in einem Rich-Edit-Steuerelement auswählen, indem er die Maus oder die Tastatur verwendet. Die *aktuelle Auswahl* ist der Bereich der ausgewählten Zeichen oder die Position der Einfügemarke, wenn keine Zeichen ausgewählt sind. Eine Anwendung kann Informationen über die aktuelle Auswahl erhalten, sie festlegen, bestimmen, wann sie sich ändert, und die Markierung der Auswahl ein- oder ausblenden.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="interact-with-the-current-selection"></a>Interagieren mit der aktuellen Auswahl

Um die aktuelle Auswahl in einem Rich-Edit-Steuerelement zu bestimmen, verwenden Sie die [**EM \_ EXGETSEL-Meldung.**](em-exgetsel.md) Verwenden Sie zum Festlegen der aktuellen Auswahl die [**EM \_ EXSETSEL-Meldung.**](em-exsetsel.md) Die [**CHARRANGE-Struktur**](/windows/desktop/api/Richedit/ns-richedit-charrange) wird mit beiden Meldungen verwendet und gibt einen Zeichenbereich an. Um Informationen über den Inhalt der aktuellen Auswahl abzurufen, können Sie die [**EM \_ SELECTIONTYPE-Meldung**](em-selectiontype.md) verwenden.

Eine Anwendung kann erkennen, wenn sich die aktuelle Auswahl ändert, indem sie den [EN \_ SELCHANGE-Benachrichtigungscode](en-selchange.md) verarbeitet. Der Benachrichtigungscode gibt eine [**SELCHANGE-Struktur**](/windows/desktop/api/Richedit/ns-richedit-selchange) an, die Informationen über die neue Auswahl enthält. Ein rich-Edit-Steuerelement sendet diesen Benachrichtigungscode nur, wenn Sie ihn mithilfe der [**EM \_ SETEVENTMASK-Nachricht**](em-seteventmask.md) aktivieren.

Standardmäßig wird die Hervorhebung der Auswahl in einem Rich-Edit-Steuerelement angezeigt und ausblendet, wenn sie an Bedeutung gewinnt und den Fokus verliert. Sie können die Hervorhebung der Auswahl jederzeit mithilfe der [**MELDUNG EM \_ HIDESELECTION**](em-hideselection.md) ein- oder ausblenden. Beispielsweise kann eine Anwendung ein Suchdialogfeld bereitstellen, um Text in einem Rich-Edit-Steuerelement zu suchen. Die Anwendung kann übereinstimmenden Text auswählen, ohne das Dialogfeld zu schließen. In diesem Fall muss sie die **EM \_ HIDESELECTION-Meldung** verwenden, um die Auswahl hervorzuheben.

Wie bei Bearbeitungssteuerelementen können Sie den [**ES \_ NOHIDESEL-Fensterstil**](edit-control-styles.md) angeben, um zu verhindern, dass ein umfangreiches Bearbeitungssteuerelemente die Auswahl hervorheben, wenn es den Fokus verliert.

Als Alternative zur Verwendung der [**EM \_ EXGETSEL-**](em-exgetsel.md) und [**EM \_ EXSETSEL-Meldungen**](em-exsetsel.md) können Sie die aktuelle Auswahl mithilfe der Bearbeitungssteuerungsmeldungen [**EM \_ GETSEL**](em-getsel.md) und [**EM \_ SETSEL**](em-setsel.md) abrufen und festlegen. Die **EM \_ GETSEL-Nachricht** packt zwei 16-Bit-Zeichenindizes in ihren 32-Bit-Rückgabewert und funktioniert daher nur für Auswahlen, die vollständig innerhalb des ersten 64K fallen. Ein umfangreiches Bearbeitungssteuerfeld enthält jedoch nie mehr als 32.000 Zeichen Text, es sei denn, Sie erweitern diesen Grenzwert mithilfe der [**EM \_ LIMITTEXT-**](em-limittext.md) oder [**EM \_ EXLIMITTEXT-Nachricht.**](em-exlimittext.md) Für Auswahlen, die über die ersten 64 KB text hinausgehen, gibt die **EM \_ GETSEL-Nachricht** –1 zurück. In diesem Fall können Sie weiterhin die in *wParam* und *lParam* zurückgegebenen Werte verwenden, um die Start- und Endzeichen der Auswahl zu finden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




