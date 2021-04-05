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
# <a name="how-to-interact-with-the-current-selection"></a>Interagieren mit der aktuellen Auswahl

Der Benutzer kann Text in einem Rich-Edit-Steuerelement mit der Maus oder der Tastatur auswählen. Bei der *aktuellen Auswahl* handelt es sich um den Bereich der ausgewählten Zeichen oder um die Position der Einfügemarke, wenn keine Zeichen ausgewählt sind. Eine Anwendung kann Informationen über die aktuelle Auswahl, die Festlegung, den Zeitpunkt der Änderung und das Anzeigen oder Ausblenden der Auswahl Markierung erhalten.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="interact-with-the-current-selection"></a>Mit der aktuellen Auswahl interagieren

Um die aktuelle Auswahl in einem Rich-Edit-Steuerelement zu ermitteln, verwenden Sie die [**EM \_ exgetsel**](em-exgetsel.md) -Nachricht. Um die aktuelle Auswahl festzulegen, verwenden Sie die Nachricht [**EM \_ exsetsel**](em-exsetsel.md) . Die [**charrange**](/windows/desktop/api/Richedit/ns-richedit-charrange) -Struktur wird mit beiden Nachrichten verwendet und gibt einen Bereich von Zeichen an. Zum Abrufen von Informationen über den Inhalt der aktuellen Auswahl können Sie die Nachricht [**EM \_ SelectionType**](em-selectiontype.md) verwenden.

Eine Anwendung kann erkennen, wenn sich die aktuelle Auswahl ändert, indem Sie den [en \_ selChange](en-selchange.md) -Benachrichtigungs Code verarbeitet. Der Benachrichtigungs Code gibt eine [**selChange**](/windows/desktop/api/Richedit/ns-richedit-selchange) -Struktur an, die Informationen über die neue Auswahl enthält. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code nur dann, wenn Sie ihn mithilfe der Nachricht [**EM \_ SetEventMask**](em-seteventmask.md) aktivieren.

Standardmäßig wird ein Rich-Edit-Steuerelement angezeigt und ausgeblendet, wenn es den Fokus erhält und den Fokus verliert. Sie können die Auswahl Markierung jederzeit anzeigen oder ausblenden, indem Sie die " [**EM \_ HideSelection**](em-hideselection.md) "-Meldung verwenden. Beispielsweise kann eine Anwendung ein Such Dialogfeld bereitstellen, um Text in einem Rich-Edit-Steuerelement zu finden. Die Anwendung wählt den übereinstimmenden Text aus, ohne das Dialogfeld zu schließen. in diesem Fall muss Sie die " **EM \_ HideSelection** "-Meldung verwenden, um die Auswahl hervorzuheben.

Wie bei den Bearbeitungs Steuerelementen können Sie auch den Fenster Stil " [**es \_ nohidesel**](edit-control-styles.md) " angeben, um zu verhindern, dass ein Rich Edit-Steuerelement die Auswahl Markierung ausblenden kann, wenn es den Fokus verliert.

Als Alternative zur Verwendung der Nachrichten " [**EM \_ exgetsel**](em-exgetsel.md) " und " [**EM \_ exsetsel**](em-exsetsel.md) " können Sie die aktuelle Auswahl mithilfe der Nachrichten " [**EM \_ GetSEL**](em-getsel.md) " und " [**EM \_ SetSel**](em-setsel.md) Edit Control" abrufen und festlegen. Die **\_ GetSEL-GetSEL** -Nachricht verpackt 2 16-Bit-Zeichen Indizes in ihren 32-Bit-Rückgabewert und funktioniert daher nur für die Auswahl, die vollständig innerhalb des ersten 64K liegen. Ein Rich Edit-Steuerelement enthält jedoch nie mehr als 32 KB Text, es sei denn, Sie erweitern diesen Grenzwert mithilfe der [**EM- \_ Begrenzungs Text**](em-limittext.md) -oder der [**EM \_ exlimittext**](em-exlimittext.md) -Nachricht. Für eine Auswahl, die über den ersten 64 KB-Text hinausgeht, gibt die **EM \_ GetSEL** -Nachricht – 1 zurück. In einem solchen Fall können Sie weiterhin die Werte verwenden, die in *wParam* und *LPARAM* zurückgegeben werden, um die Start-und Endzeichen der Auswahl zu suchen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




