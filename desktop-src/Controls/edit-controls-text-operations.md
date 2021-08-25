---
title: Bearbeiten von Steuerelementtextvorgängen
description: Das System verarbeitet automatisch alle vom Benutzer initiierten Textvorgänge und benachrichtigt die Anwendung, wenn die Vorgänge abgeschlossen sind.
ms.assetid: 9af3a1bc-4c87-4cc9-966d-50742be7c811
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8698fbd38241a0e5c3f40e69f7ab401fc22e3982e2bc70001733bc71daf49689
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826370"
---
# <a name="edit-control-text-operations"></a>Bearbeiten von Steuerelementtextvorgängen

Das System verarbeitet automatisch alle vom Benutzer initiierten Textvorgänge und benachrichtigt die Anwendung, wenn die Vorgänge abgeschlossen sind.

In den folgenden Themen werden vom Benutzer initiierte Textvorgänge und die Antwort der Anwendung behandelt:

-   [Auswählen eines Edit-Steuerelements](#selecting-an-edit-control)
-   [Festlegen und Abrufen von Text](#setting-and-retrieving-text)
-   [Auswählen von Text](#selecting-text)
-   [Ersetzen von Text](#replacing-text)
-   [Ändern der schriftart, die von einem Bearbeitungssteuer steuerelement verwendet wird](#changing-the-font-used-by-an-edit-control)
-   [Ausschneiden von Vorgängen zum Einfügen und Löschen von Kopiervorgängen](#cut-copy-paste-and-clear-operations)
-   [Ändern von Text](#modifying-text)
-   [Einschränken des vom Benutzer eingegebenen Texts](#limiting-user-entered-text)
-   [Zeichen- und Zeilenoperationen](#character-and-line-operations)
-   [Scrollen von Text in einem Bearbeitungssteuerfeld](#scrolling-text-in-an-edit-control)
-   [Festlegen von Tabstopps und Rändern](#setting-tab-stops-and-margins)
-   [Verbergen von Benutzereingaben](#concealing-user-input)
-   [Verwenden von ganzen Zahlen](#using-integers)
-   [Rückgängig machen von Textvorgängen](#undoing-text-operations)
-   [Behandeln von Wordwrap und Zeilenumbrüchen](#handling-wordwrap-and-line-breaks)
-   [Abrufen von Punkten und Zeichen](#retrieving-points-and-characters)
-   [Automatische Vervollstierung von Zeichenfolgen](#autocompletion-of-strings)
-   [Komplexes Skript in Bearbeitungssteuerelementen](#complex-script-in-edit-controls)

## <a name="selecting-an-edit-control"></a>Auswählen eines Edit-Steuerelements

Der Benutzer kann ein Bearbeitungssteuer steuerelement auswählen, indem er mit der Maus darauf klickt oder indem er die TAB-TASTE drückt, um zu ihm zu wechseln. Die Tabulatormethode ist Teil einer vordefinierten Tastaturschnittstelle, die das System bietet. Eine vollständige Beschreibung dieser Schnittstelle finden Sie unter [Dialogfelder](/windows/desktop/dlgbox/dialog-boxes). Wenn der Benutzer ein Bearbeitungssteuerfeld auswählt, erhält das Steuerelement den Tastaturfokus (siehe "Tastaturfokus und -aktivierung" [in](/windows/desktop/inputdev/about-keyboard-input)Informationen zur Tastatureingabe) und hebt seinen Text mithilfe von umgekehrten Videos hervor.

## <a name="setting-and-retrieving-text"></a>Festlegen und Abrufen von Text

Eine Anwendung kann den Text eines Bearbeitungssteuerfelds mithilfe der [**SetWindowText-Funktion,**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) der [**SetDlgItemText-Funktion**](/windows/desktop/DevNotes/-setdlgitemtext) oder durch Senden einer [**WM \_ SETTEXT-Nachricht**](/windows/desktop/winmsg/wm-settext) an das Steuerelement festlegen.

Um den ganzen Text aus einem Bearbeitungssteuerfeld abzurufen, verwenden Sie zuerst die [**GetWindowTextLength-Funktion**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) oder die [**WM \_ GETTEXTLENGTH-Nachricht,**](/windows/desktop/winmsg/wm-gettextlength) um die Größe des Puffers zu bestimmen, der zum Enthalten des Texts erforderlich ist. Rufen Sie als Nächstes den Text mithilfe der [**GetWindowText-Funktion,**](/windows/desktop/DevNotes/-getwindowtext) der [**GetDlgItemText-Funktion**](/windows/desktop/api/winuser/nf-winuser-getdlgitemtexta) oder der [**WM \_ GETTEXT-Nachricht**](/windows/desktop/winmsg/wm-gettext) ab.

## <a name="selecting-text"></a>Auswählen von Text

Nach dem Auswählen eines Bearbeitungssteuerfelds kann der Benutzer Text im Steuerelement mit der Maus oder der Tastatur auswählen. Eine Anwendung kann die Anfangs- und Endzeichenpositionen der aktuellen Auswahl in einem Bearbeitungssteuerzeichen abrufen, indem sie dem Steuerelement eine [**EM \_ GETSEL-Nachricht**](em-getsel.md) sendet. Der Rückgabewert für die Endposition ist eins größer als das letzte Zeichen in der Auswahl (d. h. die Position des ersten Zeichens nach dem zuletzt ausgewählten Zeichen).

Eine Anwendung kann text auch in einem Bearbeitungssteuerfeld auswählen, indem sie dem Steuerelement eine [**EM \_ SETSEL-Nachricht**](em-setsel.md) mit den Anfangs- und Endzeichenindizes für die Auswahl sendet. Beispielsweise kann die Anwendung **EM \_ SETSEL** mit [**EM \_ REPLACESEL**](em-replacesel.md) verwenden, um Text aus einem Bearbeitungssteuerfeld zu löschen.

Diese drei Meldungen gelten sowohl für einzeilen- als auch für mehrzeilenbasierte Bearbeitungssteuerelemente.

## <a name="replacing-text"></a>Ersetzen von Text

Eine Anwendung kann ausgewählten Text in einem Bearbeitungssteuerfeld ersetzen, indem sie dem Steuerelement eine [**EM \_ REPLACESEL-Nachricht**](em-replacesel.md) mit einem Zeiger auf den Ersetzungstext sendet. Wenn keine aktuelle Auswahl angezeigt wird, fügt **EM \_ REPLACESEL** den Ersetzungstext an der Einfügemarke ein. Die Anwendung erhält möglicherweise einen [EN ERRSPACE-Benachrichtigungscode, \_ ](en-errspace.md) wenn der Ersetzungstext den verfügbaren Arbeitsspeicher überschreitet. Diese Meldung gilt sowohl für einzeilenbasierte als auch für mehrzeilenbasierte Bearbeitungssteuerelemente.

Eine Anwendung kann [**EM \_ REPLACESEL**](em-replacesel.md) verwenden, um einen Teil des Texts eines Bearbeitungssteuerfelds oder die [**SetDlgItemText-Funktion**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) zu ersetzen.

## <a name="changing-the-font-used-by-an-edit-control"></a>Ändern der schriftart, die von einem Bearbeitungssteuer steuerelement verwendet wird

Eine Anwendung kann die Schriftart ändern, die ein Bearbeitungssteuer steuerelement verwendet, indem die [**WM \_ SETFONT-Nachricht gesendet**](/windows/desktop/winmsg/wm-setfont) wird. Die meisten Anwendungen tun dies während der Verarbeitung der [**WM \_ INITDIALOG-Nachricht.**](/windows/desktop/dlgbox/wm-initdialog) Das Ändern der Schriftart ändert nicht die Größe des Bearbeitungssteuer steuerelements. -Anwendungen, die die **WM \_ SETFONT-Nachricht** senden, müssen möglicherweise die Schriftartmetriken für den Text abrufen und die Größe des Bearbeitungssteuerfelds neu berechnen. Weitere Informationen zu Schriftarten und Schriftartmetriken finden Sie unter [Schriftarten und Text.](/windows/desktop/gdi/fonts-and-text)

## <a name="cut-copy-paste-and-clear-operations"></a>Ausschneiden von Vorgängen zum Einfügen und Löschen von Kopiervorgängen

Es gibt vier Meldungen zum Verschieben von Text zwischen einem Bearbeitungssteuerfeld und der Zwischenablage. Die [**WM \_ COPY-Meldung**](/windows/desktop/dataxchg/wm-copy) kopiert die aktuelle Auswahl (sofern vorhanden) aus einem Bearbeitungssteuerteil in die Zwischenablage, ohne sie aus dem Bearbeitungssteuerteil zu löschen. Die [**WM \_ CUT-Meldung**](/windows/desktop/dataxchg/wm-cut) löscht die aktuelle Auswahl (sofern enthalten) im Bearbeitungssteuerfeld und kopiert den gelöschten Text in die Zwischenablage. In [**der WM \_ CLEAR-Meldung**](/windows/desktop/dataxchg/wm-clear) wird die aktuelle Auswahl (sofern bereits vorhandene) aus einem Bearbeitungssteuerteil gelöscht, aber nicht in die Zwischenablage kopiert (es sei denn, der Benutzer hat die UMSCHALTTASTE gedrückt). Die [**WM \_ PASTE-Meldung**](/windows/desktop/dataxchg/wm-paste) kopiert Text aus der Zwischenablage in ein Bearbeitungssteuerfeld an der Einfügemarke. Diese vier Meldungen gelten sowohl für einzeilenbasierte als auch für mehrzeilenbasierte Bearbeitungssteuerelemente.

Microsoft Windows NT 4.0 und höher: Ein Bearbeitungssteuerelement enthält ein integriertes Kontextmenü, das dem Benutzer das Verschieben von Text zwischen dem Bearbeitungssteuerelement und der Zwischenablage erleichtert. Das Kontextmenü wird angezeigt, wenn der Benutzer mit der rechten Maustaste auf das Steuerelement klickt. Zu den Befehlen im Kontextmenü gehören **Rückgängig**, **Ausschneiden,** **Kopieren,** **Einfügen,** **Löschen** und **Alle auswählen.**

## <a name="modifying-text"></a>Ändern von Text

Der Benutzer kann Text in einem Bearbeitungssteuerfeld auswählen, löschen oder verschieben. Das System verwaltet ein internes Flag für jedes Bearbeitungssteuerzeichen, das angibt, ob der Inhalt des Steuerelements geändert wurde. Das System gibt dieses Flag beim Erstellen des Steuerelements frei und legt das Flag fest, wenn der Text im Steuerelement geändert wird. Eine Anwendung kann das Änderungsflag abrufen, indem sie dem Steuerelement eine [**EM \_ GETMODIFY-Nachricht**](em-getmodify.md) sendet. Die Anwendung kann dann das Änderungsflag festlegen oder löschen, indem sie dem Steuerelement eine [**EM \_ SETMODIFY-Nachricht**](em-setmodify.md) sendet. Diese Meldungen gelten sowohl für einzeilenbasierte als auch für mehrzeilenbasierte Bearbeitungssteuerelemente.

## <a name="limiting-user-entered-text"></a>Einschränken des vom Benutzer eingegebenen Texts

Der Standardgrenzwert für die Textmenge, die ein Benutzer in ein Bearbeitungssteuerfeld eingeben kann, beträgt 32 KB. Eine Anwendung kann den Standardgrenzwert ändern, indem sie dem Steuerelement eine [**EM \_ SETLIMITTEXT-Nachricht**](em-setlimittext.md) sendet. Diese Meldung legt eine harte Grenze für die Anzahl von Bytes fest, die der Benutzer in ein Bearbeitungssteuerfeld eingeben kann, wirkt sich jedoch weder auf Text aus, der sich bereits im Steuerelement befindet, als die Nachricht gesendet wurde, noch auf Text, der von der [**SetDlgItemText-Funktion**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) oder der [**WM \_ SETTEXT-Nachricht**](/windows/desktop/winmsg/wm-settext) in das Steuerelement kopiert wurde. Angenommen, die Anwendung verwendet die **SetDlgItemText-Funktion,** um 500 Bytes in einem Bearbeitungssteuersatz zu platzieren, und der Benutzer gibt auch 500 Bytes (insgesamt 1.000 Bytes) ein. Wenn die Anwendung dann eine **EM \_ SETLIMITTEXT-Nachricht** sendet, die den vom Benutzer eingegebenen Text auf 300 Byte beschränkt, bleiben die 1.000 Bytes, die sich bereits im Bearbeitungssteuerfeld enthalten haben, dort, und der Benutzer kann keinen text mehr hinzufügen. Wenn die Anwendung dagegen eine **EM \_ SETLIMITTEXT-Nachricht** sendet, die den vom Benutzer eingegebenen Text auf 1.300 Byte beschränkt, bleiben die 1.000 Bytes erhalten, aber der Benutzer kann 300 weitere Bytes hinzufügen.

Wenn der Benutzer die Zeichengrenze eines Bearbeitungssteuerzeichens erreicht, sendet das System der Anwendung eine [**WM \_ COMMAND-Nachricht**](/windows/desktop/menurc/wm-command) mit einem [EN \_ MAXTEXT-Benachrichtigungscode.](en-maxtext.md) Dieser Benachrichtigungscode bedeutet nicht, dass der Arbeitsspeicher erschöpft ist, sondern dass der Grenzwert für vom Benutzer eingegebenen Text erreicht wurde. der Benutzer kann keinen text mehr eingeben. Um diesen Grenzwert zu ändern, muss eine Anwendung dem Steuerelement eine neue [**EM \_ SETLIMITTEXT-Nachricht**](em-setlimittext.md) mit einem höheren Grenzwert senden.

Nehmen wir als Beispiel für die Verwendung von [**EM \_ SETLIMITTEXT**](em-setlimittext.md) und [EN \_ MAXTEXT](en-maxtext.md)an, dass die Anwendung den Benutzer auf maximal vier Zeichen in einem Bearbeitungssteuerzeichen beschränken muss. Die Anwendung verwendet **EM \_ SETLIMITTEXT,** um einen Grenzwert von vier Zeichen anzugeben. Wenn der Benutzer versucht hat, ein fünftes Zeichen ein eingaben, sendet das System einen EN \_ MAXTEXT-Benachrichtigungscode an die Anwendung.

## <a name="character-and-line-operations"></a>Zeichen- und Zeilenoperationen

Es gibt mehrere Meldungen, die Informationen zu den Zeichen und Zeilen in einem Bearbeitungssteuerzeichen zurückgeben. Die meisten Nachrichten geben einen Index zurück, in der Regel eine nullbasierte Zahl, um auf ein Zeichen oder eine Zeile zu verweisen. In einem einzeilenbasierten Bearbeitungssteuerzeichen, das n Zeichen enthält, ist der Zeilenindex beispielsweise 0 (null), und die Zeichen werden von 0 bis n-1 indiziert. In einem mehrzeilenbasierten Bearbeitungssteuerzeichen, das m Zeilen und n Zeichen enthält, werden die Zeilen von 0 bis m-1 indiziert, und die Zeichen werden von 0 bis n-1 indiziert. Beachten Sie, dass bei der Zeichenindizierung Zeilenumbrüche ignoriert werden.

Eine Anwendung kann die Anzahl der Zeichen in einem Bearbeitungssteuerzeichen bestimmen, indem sie die [**WM \_ GETTEXTLENGTH-Nachricht**](/windows/desktop/winmsg/wm-gettextlength) an das Bearbeitungssteuerzeichen sendet. Diese Meldung gibt die Länge des Texts in einem ein- oder mehrzeilenbasierten Bearbeitungssteuerfeld in Zeichen (ohne das beendende NULL-Zeichen) zurück. Die [**EM \_ LINELENGTH-Nachricht**](em-linelength.md) gibt die Länge einer Zeile in Zeichen zurück, die durch den Zeichenindex eines Zeichens in der Zeile angegeben wird. Die zurückgegebene Länge enthält keine ausgewählten Zeichen. Eine Anwendung kann diese Nachrichten in einem ein- oder mehrzeilenbasierten Bearbeitungssteuerteil verwenden.

Die [**EM \_ GETFIRSTVISIBLELINE-Nachricht**](em-getfirstvisibleline.md) gibt den nullbasierten Index der obersten sichtbaren Zeile in einem mehrzeilenbasierten Bearbeitungssteuerzeichen oder den nullbasierten Index des ersten sichtbaren Zeichens in einem einzeilenbasierten Bearbeitungssteuerzeichen zurück. Eine Anwendung kann eine Zeile aus einem Bearbeitungssteuer steuerelement in einen Puffer kopieren, indem sie die [**EM \_ GETLINE-Nachricht**](em-getline.md) an das Bearbeitungssteuer steuerelement sendet. Die Zeile wird durch ihren Zeilenindex angegeben, und das erste Wort des empfangenden Puffers enthält die maximale Anzahl von Bytes, die in den Puffer kopiert werden sollen. Der Rückgabewert ist die Anzahl der kopierten Bytes. Diese Meldung kann auch in einem ein- oder mehrzeilenbasierten Bearbeitungssteuerteil verwendet werden.

Es sind eindeutige Meldungen verfügbar, um die Informationen zu einer Zeile in einem mehrzeilenigen Bearbeitungssteuerteil zurück zu geben. Die [**EM \_ GETLINECOUNT-Nachricht**](em-getlinecount.md) gibt die Anzahl der Zeilen in einem Bearbeitungssteuerzeichen zurück. Die [**EM \_ LINEFROMCHAR-Meldung**](em-linefromchar.md) gibt den Index der Zeile zurück, die einen angegebenen Zeichenindex enthält. Die [**EM \_ LINEINDEX-Nachricht**](em-lineindex.md) gibt den Index des ersten Zeichens in einer angegebenen Zeile zurück.

## <a name="scrolling-text-in-an-edit-control"></a>Scrollen von Text in einem Bearbeitungssteuerelement

Zum Implementieren des Scrollens in einem Bearbeitungssteuerelement können Sie die in Bearbeiten von [Steuerelementtypen und Stilen](about-edit-controls.md)erläuterten automatischen Bildlaufstile verwenden oder dem Bearbeitungssteuerelement explizit Scrollleisten hinzufügen. Verwenden Sie zum Hinzufügen einer horizontalen Bildlaufleiste den Stil WS \_ HSCROLL. Verwenden Sie zum Hinzufügen einer vertikalen Bildlaufleiste den Stil [**WS \_ VSCROLL.**](/windows/desktop/winmsg/window-styles) Ein Bearbeitungssteuerelement mit Bildlaufleisten verarbeitet seine eigenen Scrollleistennachrichten. Ausführliche Informationen zum Hinzufügen von Bildlaufleisten zum Bearbeiten von Steuerelementen finden Sie unter [Scrollleisten.](scroll-bars.md)

Das System stellt drei Nachrichten bereit, die eine Anwendung an ein Bearbeitungssteuerelement mit Bildlaufleisten senden kann. Die [**EM \_ LINESCROLL-Nachricht**](em-linescroll.md) kann ein mehrzeiliges Bearbeitungssteuerelement vertikal und horizontal scrollen. Der *lParam-Parameter* gibt die Anzahl der Zeilen an, die vertikal ab der aktuellen Zeile gescrollt werden sollen, und der *wParam-Parameter* gibt die Anzahl der Zeichen an, die horizontal gescrollt werden sollen, beginnend mit dem aktuellen Zeichen. Das Bearbeitungssteuerelement bestätigt keine horizontalen Bildlaufmeldungen, wenn es den [**STIL ES \_ CENTER**](edit-control-styles.md) oder [**ES \_ RIGHT**](edit-control-styles.md) auf hat. Die **EM \_ LINESCROLL-Meldung** gilt nur für Mehrzeilen-Bearbeitungssteuerelemente.

Die [**EM \_ SCROLL-Nachricht**](em-scroll.md) führt einen vertikalen Bildlauf für ein mehrzeiliges Bearbeitungssteuerelement durch. Der *wParam-Parameter* gibt die Scrollaktion an. Die **EM \_ SCROLL-Meldung** gilt nur für Steuerelemente zur mehrzeiligen Bearbeitung. **EM \_ SCROLL** hat die gleiche Auswirkung wie die [**\_ WM-VSCROLL-Nachricht.**](wm-vscroll.md)

Die [**EM \_ SCROLLCARET-Nachricht**](em-scrollcaret.md) scrollt das Caretzeichen in einem Bearbeitungssteuerelement in die Ansicht.

## <a name="setting-tab-stops-and-margins"></a>Festlegen von Tabstopps und Rändern

Eine Anwendung kann Tabstopps in einem mehrzeiligen Bearbeitungssteuerelement mithilfe der [**EM \_ SETTABSTOPS-Meldung**](em-settabstops.md) festlegen. (Der Standardwert für einen Tabstopp beträgt acht Zeichen.) Wenn eine Anwendung dem Bearbeitungssteuerelement Text hinzufügt, generieren Tabstoppzeichen im Text automatisch Speicherplatz bis zum nächsten Tabstopp. Die **EM \_ SETTABSTOPS-Meldung** bewirkt nicht automatisch, dass das System den Text neu gezeichnet. Zu diesem Zweck kann eine Anwendung die [**InvalidateRect-Funktion**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) aufrufen. Die **EM \_ SETTABSTOPS-Meldung** gilt nur für Steuerelemente zur mehrzeiligen Bearbeitung.

Eine Anwendung kann die Breite des linken und rechten Rands für ein Bearbeitungssteuerelement mithilfe der [**EM \_ SETMARGINS-Nachricht**](em-setmargins.md) festlegen. Nach dem Senden dieser Nachricht wird das Bearbeitungssteuerelement neu gezeichnet, um die neuen Randeinstellungen widerzuspiegeln. Eine Anwendung kann die Breite des linken oder rechten Rands abrufen, indem sie die [**EM \_ GETMARGINS-Nachricht**](em-getmargins.md) sendet. Standardmäßig sind die Ränder des Bearbeitungssteuerelements so weit festgelegt, dass sie den größten horizontalen Überhänge (negative ABC-Breite) für die aktuelle Schriftart aufnehmen, die im Bearbeitungssteuerelement verwendet wird.

## <a name="concealing-user-input"></a>Verbergen von Benutzereingaben

Eine Anwendung kann ein Kennwortzeichen in einem Bearbeitungssteuerelement verwenden, um Benutzereingaben zu verbergen. Wenn ein Kennwortzeichen festgelegt wird, wird es anstelle jedes Zeichens angezeigt, das der Benutzer eingibt. Wenn ein Kennwortzeichen entfernt wird, zeigt das Steuerelement die Zeichen an, die der Benutzer eingibt. Wenn die Anwendung ein einzeiliges Bearbeitungssteuerelement mit dem Format [**ES \_ PASSWORD**](edit-control-styles.md)erstellt, ist das Standardkennwortzeichen ein Sternchen ( \* ). Eine Anwendung kann die [**EM \_ SETPASSWORDCHAR-Nachricht**](em-setpasswordchar.md) verwenden, um ein anderes Kennwortzeichen zu entfernen oder zu definieren, und die [**EM \_ GETPASSWORDCHAR-Nachricht**](em-getpasswordchar.md) zum Abrufen des aktuellen Kennwortzeichens. Diese Meldungen gelten nur für einzeilige Bearbeitungssteuerelemente.

## <a name="using-integers"></a>Verwenden von ganzen Zahlen

Es gibt zwei Ganzzahlkonvertierungsfunktionen für Bearbeitungssteuerelemente, die nur Zahlen enthalten sollen. Die [**SetDlgItemInt-Funktion**](/windows/desktop/api/winuser/nf-winuser-setdlgitemint) erstellt die Zeichenfolgendarstellung einer angegebenen ganzen Zahl (mit oder ohne Vorzeichen) und sendet die Zeichenfolge an ein Bearbeitungssteuerelement. **SetDlgItemInt** gibt keinen Wert zurück. Die [**GetDlgItemInt-Funktion**](/windows/desktop/api/winuser/nf-winuser-getdlgitemint) erstellt eine ganze Zahl (mit oder ohne Vorzeichen) aus ihrer Zeichenfolgendarstellung in einem Bearbeitungssteuerelement. **GetDlgItemInt** gibt die ganze Zahl (oder einen Fehlerwert) zurück.

## <a name="undoing-text-operations"></a>Rückgängigmieren von Textvorgängen

Jedes Bearbeitungssteuerelement behält ein Rückgängigflag bei, das angibt, ob eine Anwendung den letzten Vorgang des Bearbeitungssteuerelements umkehren oder rückgängig machen kann (z. B. das Rückgängig machen eines Textlöschvorgangs). Das Bearbeitungssteuerelement legt das Rückgängig-Flag fest, um anzugeben, dass der Vorgang rückgängig machen kann, und setzt es zurück, um anzugeben, dass der Vorgang nicht rückgängig machen kann. Eine Anwendung kann die Einstellung des Rückgängig-Flags bestimmen, indem sie dem Steuerelement eine [**EM \_ CANUNDO-Nachricht**](em-canundo.md) sendet.

Eine Anwendung kann den letzten Vorgang rückgängig setzen, indem sie dem Steuerelement eine [**\_ EM-UNDO-Nachricht**](em-undo.md) sendet. Ein Vorgang kann rückgängig gemacht werden, sofern zuerst kein anderer Bearbeitungssteuerelementvorgang erfolgt. Beispielsweise kann der Benutzer Text löschen, den Text ersetzen (den Löschvorgang rückgängig machen) und den Text dann erneut löschen (ersetzung rückgängig machen). Die **EM \_ UNDO-Meldung** gilt sowohl für einzeilige als auch für mehrzeilige Bearbeitungssteuerelemente und funktioniert immer für einzeilige Bearbeitungssteuerelemente.

Eine Anwendung kann das Rückgängig-Flag eines Bearbeitungssteuerelements zurücksetzen, indem sie dem Steuerelement eine [**EM \_ EMPTYUNDOBUFFER-Nachricht**](em-emptyundobuffer.md) sendet. Das Rückgängig-Flag wird vom System automatisch zurückgesetzt, sobald ein Bearbeitungssteuerelement eine [**EM \_ SETHANDLE-**](em-sethandle.md) oder [**WM \_ SETTEXT-Nachricht**](/windows/desktop/winmsg/wm-settext) empfängt. Die [**SetDlgItemText-Funktion**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) sendet eine **WM \_ SETTEXT-Nachricht.**

## <a name="handling-wordwrap-and-line-breaks"></a>Behandeln von Zeilenumbrüchen und Zeilenumbrüchen

Eine Anwendung kann Wordwrap-Funktionen mit mehrzeiligen Bearbeitungssteuerelementen verwenden, um das Wort oder Wortfragment zu suchen, das von der nächsten Zeile umschlossen werden soll. Mithilfe der vom System bereitgestellten Wordwrap-Standardfunktion enden Zeilen immer an den Leerzeichen zwischen Wörtern. Eine Anwendung kann ihre eigene Wordwrap-Funktion angeben, indem sie eine [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) Wordwrap-Funktion angibt und dem Bearbeitungssteuerelement eine [**EM \_ SETWORDBREAKPROC-Nachricht**](em-setwordbreakproc.md) sendet. Eine Anwendung kann die Adresse der aktuellen Wordwrap-Funktion abrufen, indem sie dem Steuerelement eine [**EM \_ GETWORDBREAKPROC-Nachricht**](em-getwordbreakproc.md) sendet.

Eine Anwendung kann ein mehrzeiliges Bearbeitungssteuerelement anweisen, am Ende von umschlossenen Textzeilen automatisch ein weiches Zeilenumbruchzeichen (zwei Wagenrückläufe und einen Zeilenvorschub) hinzuzufügen oder zu entfernen. Eine Anwendung kann dieses Feature aktivieren oder deaktivieren, indem sie dem Bearbeitungssteuerelement eine [**EM \_ FMTLINES-Nachricht**](em-fmtlines.md) sendet. Diese Meldung gilt nur für Mehrzeilen-Bearbeitungssteuerelemente und wirkt sich nicht auf eine Zeile aus, die mit einem hartzeiligen Umbruch endet (ein Wagenrücklauf und ein vom Benutzer eingegebener Zeilenvorschub). Außerdem kann eine Anwendung in mehrzeiligen Bearbeitungssteuerelementen den [**ES \_ WANTRETURN-Stil**](edit-control-styles.md) angeben, um anzufordern, dass das System einen Wagenrücklauf einfügt, wenn der Benutzer die EINGABETASTE im Bearbeitungssteuerelement drückt.

## <a name="retrieving-points-and-characters"></a>Abrufen von Punkten und Zeichen

Um das Zeichen zu bestimmen, das einem angegebenen Punkt im Clientbereich eines Bearbeitungssteuerelements am nächsten liegt, senden Sie die [**EM \_ CHARFROMPOS-Nachricht**](em-charfrompos.md) an das Steuerelement. Die Nachricht gibt den Zeichenindex und den Zeilenindex des Zeichens zurück, das dem Punkt am nächsten ist. Auf ähnliche Weise können Sie die Clientbereichskoordinaten eines angegebenen Zeichens abrufen, indem Sie die [**EM \_ POSFROMCHAR-Nachricht**](em-posfromchar.md) senden. Die Nachricht gibt die x- und y-Koordinaten der oberen linken Ecke des angegebenen Zeichens zurück.

## <a name="autocompletion-of-strings"></a>Automatische Vervollständigung von Zeichenfolgen

Die automatische Vervollständigung erweitert Zeichenfolgen, die teilweise in ein Bearbeitungssteuerelement eingegeben wurden, in vollständige Zeichenfolgen. Wenn ein Benutzer beispielsweise beginnt, eine URL in das Adressbearbeitungssteuerelement einzugeben, das in die symbolleiste Windows Internet Explorer eingebettet ist, erweitert die automatische Vervollständigung die Zeichenfolge in mindestens eine vollständige URLs, die mit der vorhandenen Teilzeichenfolge konsistent sind. Eine partielle URL-Zeichenfolge wie "mic" kann auf " " oder " " erweitert https://www.microsoft.com https://www.microsoft.com/windows werden. Die automatische Vervollständigung wird in der Regel mit Bearbeitungssteuerelementen oder mit Steuerelementen verwendet, die über ein eingebettetes Bearbeitungssteuerelement verfügen.

Weitere Informationen finden Sie in der Dokumentation zur [**IAutoComplete-**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete) und [**IAutoComplete2-Schnittstelle.**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete2)

## <a name="complex-script-in-edit-controls"></a>Komplexes Skript in Steuerelementen bearbeiten

Ein *komplexes Skript* ist eine Sprache, deren gedrucktes Formular nicht einfach angeordnet ist. Ein komplexes Skript kann z. B. bidirektionales Rendering, kontextbezogene Strukturierung von Glyphen oder kombinierende Zeichen ermöglichen. Die standardmäßigen Bearbeitungssteuerelemente wurden erweitert, um mehrsprachigen Text und komplexe Skripts zu unterstützen. Dies schließt nicht nur eingabe- und display-, sondern auch eine korrekte Cursorbewegung über Zeichencluster ein (z.B. in thailändischen und Devanagari-Skripts).

Eine gut geschriebene Anwendung erhält diese Unterstützung automatisch und ohne Änderungen. Auch hier sollten Sie erwägen, Unterstützung für die Lesereihenfolge von rechts nach links und die Ausrichtung nach rechts hinzuzufügen. Schalten Sie in diesem Fall die erweiterten Stilflags des Bearbeitungssteuerelementfensters um, um diese Attribute zu steuern, wie im folgenden Beispiel gezeigt.


```
// ID_EDITCONTROL is the control ID in the resource file.
HANDLE hWndEdit = GetDlgItem(hDlg, ID_EDITCONTROL);
LONG lAlign = GetWindowLong(hWndEdit, GWL_EXSTYLE) ;

// To toggle alignment
lAlign ^= WS_EX_RIGHT ;

// To toggle reading order
lAlign ^= WS_EX_RTLREADING ;
```



Aktivieren Sie nach dem Festlegen des **lAlign-Werts** die neue Anzeige, indem Sie den erweiterten Stil des Bearbeitungssteuerelementfensters wie folgt festlegen.


```
// This assumes your edit control is in a dialog box. If not, 
// get the edit control handle from another source.

SetWindowLong(hWndEdit, GWL_EXSTYLE, lAlign);
InvalidateRect(hWndEdit, NULL, FALSE);
```



Uniscribe ist ein weiterer Satz von Funktionen, die eine fein kontrollierte Verarbeitung komplexer Skripts ermöglichen. Weitere Informationen finden Sie unter [Uniscribe.](/windows/desktop/Intl/uniscribe)

 

 