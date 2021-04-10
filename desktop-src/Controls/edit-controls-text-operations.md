---
title: Bearbeiten von Steuerelement Text Vorgängen
description: Das System verarbeitet automatisch alle vom Benutzer initiierten Text Vorgänge und benachrichtigt die Anwendung, wenn die Vorgänge abgeschlossen sind.
ms.assetid: 9af3a1bc-4c87-4cc9-966d-50742be7c811
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9640616cf70b9a2933ef9d4c3fdb2accbfdcabf0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039669"
---
# <a name="edit-control-text-operations"></a>Bearbeiten von Steuerelement Text Vorgängen

Das System verarbeitet automatisch alle vom Benutzer initiierten Text Vorgänge und benachrichtigt die Anwendung, wenn die Vorgänge abgeschlossen sind.

In den folgenden Themen werden vom Benutzer initiierte Text Vorgänge und die Antwort der Anwendung erläutert:

-   [Auswählen eines Bearbeitungs Steuer Elements](#selecting-an-edit-control)
-   [Festlegen und Abrufen von Text](#setting-and-retrieving-text)
-   [Auswählen von Text](#selecting-text)
-   [Ersetzen von Text](#replacing-text)
-   [Ändern der Schriftart, die von einem Bearbeitungs Steuerelement verwendet wird](#changing-the-font-used-by-an-edit-control)
-   [Kopierfüge-und Löschvorgänge Ausschneiden](#cut-copy-paste-and-clear-operations)
-   [Ändern von Text](#modifying-text)
-   [Einschränken des eingegebenen Texts für Benutzer](#limiting-user-entered-text)
-   [Zeichen-und Zeilen Vorgänge](#character-and-line-operations)
-   [Scrollen von Text in einem Bearbeitungs Steuerelement](#scrolling-text-in-an-edit-control)
-   [Festlegen von Tabstopps und Rändern](#setting-tab-stops-and-margins)
-   [Verbergen von Benutzereingaben](#concealing-user-input)
-   [Verwenden von Ganzzahlen](#using-integers)
-   [Machen von Text Vorgängen](#undoing-text-operations)
-   [Behandeln von WordWrap und Zeilenumbrüchen](#handling-wordwrap-and-line-breaks)
-   [Abrufen von Punkten und Zeichen](#retrieving-points-and-characters)
-   [Automatische Vervollständigung von Zeichen folgen](#autocompletion-of-strings)
-   [Komplexes Skript in Bearbeitungs Steuerelementen](#complex-script-in-edit-controls)

## <a name="selecting-an-edit-control"></a>Auswählen eines Bearbeitungs Steuer Elements

Der Benutzer kann ein Bearbeitungs Steuerelement auswählen, indem er mit der Maus darauf klickt oder die Tab-Taste drückt, um dorthin zu wechseln. Die tabhe-Methode ist Teil einer vordefinierten Tastaturschnittstelle, die das System bereitstellt. Eine umfassende Beschreibung dieser Schnittstelle finden Sie unter [Dialog Felder](/windows/desktop/dlgbox/dialog-boxes). Wenn der Benutzer ein Bearbeitungs Steuerelement auswählt, übergibt das System dem Steuerelement den Tastaturfokus (siehe "Tastaturfokus und-Aktivierung" in [Informationen zu Tastatureingaben](/windows/desktop/inputdev/about-keyboard-input)) und hebt den Text mit umgekehrtem Video hervor.

## <a name="setting-and-retrieving-text"></a>Festlegen und Abrufen von Text

Eine Anwendung kann den Text eines Bearbeitungs Steuer Elements mithilfe der [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) -Funktion, der [**SetDlgItemText**](/windows/desktop/DevNotes/-setdlgitemtext) -Funktion oder durch Senden des Steuer Elements an eine [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht festlegen.

Um den gesamten Text aus einem Bearbeitungs Steuerelement abzurufen, verwenden Sie zuerst die [**getwindowtextlength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) -Funktion oder die [**WM \_ getTextLength**](/windows/desktop/winmsg/wm-gettextlength) -Nachricht, um die Größe des Puffers zu bestimmen, der zum enthalten des Texts erforderlich ist. Rufen Sie anschließend den Text mithilfe der [**GetWindowText**](/windows/desktop/DevNotes/-getwindowtext) -Funktion, der [**getdlgitemtext**](/windows/desktop/api/winuser/nf-winuser-getdlgitemtexta) -Funktion oder der [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext) -Nachricht ab.

## <a name="selecting-text"></a>Auswählen von Text

Nachdem Sie ein Bearbeitungs Steuerelement ausgewählt haben, kann der Benutzer mithilfe der Maus oder der Tastatur Text im Steuerelement auswählen. Eine Anwendung kann die Position des Anfangs-und Endzeichens der aktuellen Auswahl in einem Bearbeitungs Steuerelement abrufen, indem das Steuerelement eine [**EM \_ GetSEL**](em-getsel.md) -Nachricht sendet. Der Rückgabewert für die Endposition ist ein Wert größer als das letzte Zeichen in der Auswahl (d. h. die Position des ersten Zeichens nach dem letzten ausgewählten Zeichen).

Eine Anwendung kann auch Text in einem Bearbeitungs Steuerelement auswählen, indem das Steuerelement eine [**EM- \_ SetSel**](em-setsel.md) -Nachricht mit den Index Start-und Endzeichen für die Auswahl sendet. Die Anwendung kann z. b. **EM \_ SetSel** mit [**EM \_ replacesel**](em-replacesel.md) verwenden, um Text aus einem Bearbeitungs Steuerelement zu löschen.

Diese drei Nachrichten gelten sowohl für einzeilige als auch für mehrzeilige Bearbeitungs Steuerelemente.

## <a name="replacing-text"></a>Ersetzen von Text

Eine Anwendung kann den markierten Text in einem Bearbeitungs Steuerelement ersetzen, indem das Steuerelement eine [**EM \_ replacesel**](em-replacesel.md) -Nachricht mit einem Zeiger auf den Ersetzungstext sendet. Wenn keine aktuelle Auswahl vorhanden ist, fügt **EM \_ replacesel den Ersetzungs** Text an der Einfügemarke ein. Die Anwendung empfängt möglicherweise einen [en \_ errspace](en-errspace.md) -Benachrichtigungs Code, wenn der Ersetzungstext den verfügbaren Arbeitsspeicher überschreitet. Diese Meldung gilt sowohl für einzeilige als auch für mehrzeilige Bearbeitungs Steuerelemente.

Eine Anwendung kann den " [**EM \_ replacesel**](em-replacesel.md) " verwenden, um einen Teil des Texts eines Bearbeitungs Steuer Elements oder die Funktion " [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) " zu ersetzen, um alle Elemente zu ersetzen.

## <a name="changing-the-font-used-by-an-edit-control"></a>Ändern der Schriftart, die von einem Bearbeitungs Steuerelement verwendet wird

Eine Anwendung kann die von einem Bearbeitungs Steuerelement verwendete Schriftart ändern, indem die [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont) -Nachricht gesendet wird. Bei der Verarbeitung der " [**WM \_ InitDialog**](/windows/desktop/dlgbox/wm-initdialog) "-Meldung werden die meisten Anwendungen dies tun. Durch Ändern der Schriftart wird die Größe des Bearbeitungs Steuer Elements nicht geändert. Anwendungen, die die **WM- \_ setFont** -Nachricht senden, müssen möglicherweise die Schriftart Metrik für den Text abrufen und die Größe des Bearbeitungs Steuer Elements neu berechnen. Weitere Informationen zu Schriftarten und Schriftart Metriken finden Sie unter [Schriftarten und Text](/windows/desktop/gdi/fonts-and-text).

## <a name="cut-copy-paste-and-clear-operations"></a>Kopierfüge-und Löschvorgänge Ausschneiden

Es gibt vier Meldungen zum Verschieben von Text zwischen einem Bearbeitungs Steuerelement und der Zwischenablage. Die Option zum Senden der WM-Nachricht kopiert die aktuelle Auswahl (sofern vorhanden) aus einem Bearbeitungs Steuerelement in die Zwischenablage, ohne Sie aus dem Bearbeitungs Steuerelement zu löschen. [**\_**](/windows/desktop/dataxchg/wm-copy) Die [**WM- \_ Ausschneide**](/windows/desktop/dataxchg/wm-cut) Nachricht löscht die aktuelle Auswahl (sofern vorhanden) im Bearbeitungs Steuerelement und kopiert den gelöschten Text in die Zwischenablage. Die " [**WM \_ Clear**](/windows/desktop/dataxchg/wm-clear) "-Meldung löscht die aktuelle Auswahl (sofern vorhanden) aus einem Bearbeitungs Steuerelement, kopiert sie jedoch nicht in die Zwischenablage (es sei denn, der Benutzer hat die UMSCHALTTASTE gedrückt). Die [**WM \_**](/windows/desktop/dataxchg/wm-paste) -einfügenachricht kopiert Text aus der Zwischenablage an der Einfügemarke in ein Bearbeitungs Steuerelement. Diese vier Nachrichten gelten sowohl für einzeilige als auch für mehrzeilige Bearbeitungs Steuerelemente.

Microsoft Windows NT 4,0 und höher: ein Bearbeitungs Steuerelement enthält ein integriertes Kontextmenü, das es dem Benutzer leicht macht, Text zwischen dem Bearbeitungs Steuerelement und der Zwischenablage zu verschieben. Das Kontextmenü wird angezeigt, wenn der Benutzer mit der rechten Maustaste auf das Steuerelement klickt. Die Befehle im Kontextmenü umfassen **Rückgängig**, **Ausschneiden**, **Kopieren**, **Einfügen**, **Löschen** und **Alles auswählen**.

## <a name="modifying-text"></a>Ändern von Text

Der Benutzer kann Text in einem Bearbeitungs Steuerelement auswählen, löschen oder verschieben. Das System behält ein internes Flag für jedes Bearbeitungs Steuerelement bei, das angibt, ob der Inhalt des Steuer Elements geändert wurde. Das System löscht dieses Flag, wenn es das Steuerelement erstellt, und legt das Flag fest, wenn der Text im Steuerelement geändert wird. Eine Anwendung kann das Änderungsflag abrufen, indem das Steuerelement eine [**EM \_ getmodify**](em-getmodify.md) -Nachricht sendet. Die Anwendung kann dann das Änderungsflag festlegen oder löschen, indem das Steuerelement an eine [**EM- \_ setmodify**](em-setmodify.md) -Meldung gesendet wird. Diese Nachrichten gelten sowohl für einzeilige als auch für mehrzeilige Bearbeitungs Steuerelemente.

## <a name="limiting-user-entered-text"></a>Einschränken des eingegebenen Texts für Benutzer

Der Standard Grenzwert für die Text Menge, die ein Benutzer in einem Bearbeitungs Steuerelement eingeben kann, ist 32 KB. Eine Anwendung kann das Standard Limit ändern, indem das Steuerelement eine [**EM- \_ SetLimitText**](em-setlimittext.md) -Nachricht sendet. In dieser Meldung wird die Anzahl der Bytes, die der Benutzer in ein Bearbeitungs Steuerelement eingeben kann, festgelegt, aber es wirkt sich nicht auf den Text aus, der sich bereits im Steuerelement befindet, wenn die Nachricht gesendet wurde, und der Text, der von der [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) -Funktion oder der [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht kopiert Nehmen wir beispielsweise an, dass die Anwendung die **SetDlgItemText** -Funktion verwendet, um 500 Bytes in einem Bearbeitungs Steuerelement zu platzieren, und der Benutzer gibt auch 500 bytes (insgesamt 1.000 Bytes) ein. Wenn die Anwendung dann eine **EM- \_ SetLimitText** -Nachricht sendet, die vom Benutzer eingegebenen Text auf 300 bytes einschränkt, bleiben die 1.000 Bytes, die sich bereits im Bearbeitungs Steuerelement befinden, dort, und der Benutzer kann keinen weiteren Text hinzufügen. Wenn die Anwendung dagegen eine **EM- \_ SetLimitText** -Nachricht sendet, die vom Benutzer eingegebenen Text auf 1.300 bytes einschränkt, verbleiben die 1.000 Bytes, aber der Benutzer kann 300 weitere Bytes hinzufügen.

Wenn der Benutzer das Zeichenlimit eines Bearbeitungs Steuer Elements erreicht, sendet das System der Anwendung eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht, die einen [en \_ maxtext](en-maxtext.md) -Benachrichtigungs Code enthält. Dieser Benachrichtigungs Code bedeutet nicht, dass der Arbeitsspeicher erschöpft ist, aber dass das Limit für den Benutzer eingegebenen Text erreicht wurde. der Benutzer kann keinen weiteren Text eingeben. Um diese Beschränkung zu ändern, muss eine Anwendung dem Steuerelement eine neue [**EM- \_ SetLimitText**](em-setlimittext.md) -Nachricht mit einer höheren Grenze senden.

Nehmen Sie als Beispiel für die Verwendung von [**EM \_ SetLimitText**](em-setlimittext.md) und [en \_ maxtext](en-maxtext.md)an, dass die Anwendung den Benutzer auf höchstens vier Zeichen in einem Bearbeitungs Steuerelement begrenzen muss. Die Anwendung verwendet **EM \_ SetLimitText** , um ein Limit von vier Zeichen anzugeben. Wenn der Benutzer versucht hat, ein fünftes Zeichen einzugeben, sendet das System einen en \_ maxtext-Benachrichtigungs Code an die Anwendung.

## <a name="character-and-line-operations"></a>Zeichen-und Zeilen Vorgänge

Es gibt mehrere Nachrichten, die Informationen über die Zeichen und Zeilen in einem Bearbeitungs Steuerelement zurückgeben. Die meisten Meldungen geben einen Index, normalerweise eine Null basierte Zahl, zurück, um auf ein Zeichen oder eine Zeile zu verweisen. Beispielsweise ist in einem einzeiligen Bearbeitungs Steuerelement, das n Zeichen enthält, der Zeilen Index 0 (null), und die Zeichen werden von 0 (null) bis n-1 indiziert. In einem mehrzeiligen Bearbeitungs Steuerelement, das m Linien und n Zeichen enthält, werden die Zeilen von 0 bis m-1 indiziert, und die Zeichen werden von 0 bis n-1 indiziert. Beachten Sie, dass Zeichen Indizierung Zeilenumbrüche ignoriert.

Eine Anwendung kann die Anzahl von Zeichen in einem Bearbeitungs Steuerelement ermitteln, indem die [**WM- \_ getTextLength**](/windows/desktop/winmsg/wm-gettextlength) -Nachricht an das Bearbeitungs Steuerelement gesendet wird. Diese Meldung gibt die Länge des Texts in einem einzeiligen oder mehrzeiligen Bearbeitungs Steuerelement in Zeichen (ohne das abschließende Null Zeichen) zurück. Die [**EM \_ LineLength**](em-linelength.md) -Nachricht gibt die Länge in Zeichen einer Zeile zurück, die durch den Zeichen Index eines Zeichens in der Zeile angegeben wird. Die zurückgegebene Länge enthält keine ausgewählten Zeichen. Eine Anwendung kann diese Nachrichten in einem einzeiligen oder mehrzeiligen Bearbeitungs Steuerelement verwenden.

Die [**EM \_ getfirstvisibleline**](em-getfirstvisibleline.md) -Meldung gibt den NULL basierten Index der obersten sichtbaren Zeile in einem mehrzeiligen Bearbeitungs Steuerelement oder den NULL basierten Index des ersten sichtbaren Zeichens in einem einzeiligen Bearbeitungs Steuerelement zurück. Eine Anwendung kann eine Zeile aus einem Bearbeitungs Steuerelement in einen Puffer kopieren, indem die [**EM \_ getline**](em-getline.md) -Nachricht an das Bearbeitungs Steuerelement gesendet wird. Die Zeile wird durch den Zeilen Index angegeben, und das erste Wort des empfangenden Puffers enthält die maximale Anzahl von Bytes, die in den Puffer kopiert werden sollen. Der Rückgabewert ist die Anzahl der kopierten Bytes. Diese Meldung kann auch in einem einzeiligen oder mehrzeiligen Bearbeitungs Steuerelement verwendet werden.

Es sind eindeutige Meldungen verfügbar, um die Informationen zu einer Zeile in einem mehrzeiligen Bearbeitungs Steuerelement zurückzugeben. Die [**EM \_ getLineCount**](em-getlinecount.md) -Meldung gibt die Anzahl der Zeilen in einem Bearbeitungs Steuerelement zurück. Die [**EM \_ linefromchar**](em-linefromchar.md) -Meldung gibt den Index der Zeile zurück, die einen angegebenen Zeichen Index enthält. Die [**EM \_ lineindex**](em-lineindex.md) -Meldung gibt den Index des ersten Zeichens in einer angegebenen Zeile zurück.

## <a name="scrolling-text-in-an-edit-control"></a>Scrollen von Text in einem Bearbeitungs Steuerelement

Um einen Bildlauf in einem Bearbeitungs Steuerelement zu implementieren, können Sie die in [Edit Control Types und Styles](about-edit-controls.md)beschriebenen automatischen scrollstile verwenden, oder Sie können dem Bearbeitungs Steuerelement explizit Schiebe leisten hinzufügen. Verwenden Sie zum Hinzufügen einer horizontalen Schiebe Leiste den Stil WS \_ HScroll; um eine vertikale Schiebe Leiste hinzuzufügen, verwenden Sie den Stil [**WS \_ VScroll**](/windows/desktop/winmsg/window-styles). Ein Bearbeitungs Steuerelement mit Scrollleisten verarbeitet seine eigenen Bild Lauf leisten Meldungen. Ausführliche Informationen zum Hinzufügen von Schiebe leisten zum Bearbeiten von Steuerelementen finden Sie unter [Scrollleisten](scroll-bars.md).

Das System stellt drei Nachrichten bereit, die eine Anwendung mit Schiebe leisten an ein Bearbeitungs Steuerelement senden kann. Die [**\_ gelinescroll**](em-linescroll.md) -Nachricht kann ein mehrzeilige Bearbeitungs Steuerelement sowohl vertikal als auch horizontal scrollen. Der *LPARAM* -Parameter gibt die Anzahl der Zeilen an, für die ein vertikaler Bildlauf beginnend mit der aktuellen Zeile durchführen soll, und der *wParam* -Parameter gibt die Anzahl der Zeichen an, die horizontal durchlaufen werden sollen Das Bearbeitungs Steuerelement gibt keine horizontalen [**\_ Bildlauf**](edit-control-styles.md) -Meldungen an, wenn es über [**das \_ Rechte**](edit-control-styles.md) Center oder den es-Kontext Stil verfügt. Die **EM \_ linescroll** -Nachricht gilt nur für mehrzeilige Bearbeitungs Steuerelemente.

Die [**EM- \_ scrollnachricht**](em-scroll.md) führt einen vertikalen Bildlauf in einem mehrzeiligen Bearbeitungs Steuerelement Der *wParam* -Parameter gibt die scrollaktion an. Die **EM- \_ scrollnachricht** gilt nur für mehrzeilige Bearbeitungs Steuerelemente. **EM \_** Der Bildlauf hat denselben Effekt wie die [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht.

Die [**EM \_ scrollcaret**](em-scrollcaret.md) -Meldung führt einen Bildlauf in der Einfügemarke in einem Bearbeitungs Steuerelement durch.

## <a name="setting-tab-stops-and-margins"></a>Festlegen von Tabstopps und Rändern

Eine Anwendung kann Tabstopps in einem mehrzeiligen Bearbeitungs Steuerelement mithilfe der [**EM \_ settabstopps**](em-settabstops.md) -Meldung festlegen. (Die Standardeinstellung für einen Tabstopp beträgt acht Zeichen.) Wenn eine Anwendung dem Bearbeitungs Steuerelement Text hinzufügt, generieren Tabstopp Zeichen im Text automatisch bis zum nächsten Tabstopp Zeichen. Die **EM \_ SetTabStops** -Meldung bewirkt nicht automatisch, dass das System den Text neu zeichnet. Zu diesem Zweck kann eine Anwendung die [**invalidatup**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) -Funktion aufzurufen. Die **EM \_ settabstopps** -Meldung gilt nur für mehrzeilige Bearbeitungs Steuerelemente.

Eine Anwendung kann die Breite des linken und rechten Rands für ein Bearbeitungs Steuerelement mithilfe der [**EM- \_ setMargin**](em-setmargins.md) -Nachricht festlegen. Nachdem diese Nachricht gesendet wurde, zeichnet das System das Bearbeitungs Steuerelement neu, um die neuen Rand Einstellungen widerzuspiegeln. Eine Anwendung kann die Breite des linken oder rechten Rands abrufen, indem Sie die [**EM \_ getMargin**](em-getmargins.md) -Nachricht sendet. Standardmäßig sind die Ränder des Bearbeitungs Steuer Elements so festgelegt, dass das größte horizontale überschreiten des Zeichens (negative ABC-breiten) für die aktuelle Schriftart, die im Bearbeitungs Steuerelement verwendet wird, berücksichtigt wird.

## <a name="concealing-user-input"></a>Verbergen von Benutzereingaben

Eine Anwendung kann ein Kenn Wort Zeichen in einem Bearbeitungs Steuerelement verwenden, um Benutzereingaben zu verbergen. Wenn ein Kenn Wort Zeichen festgelegt ist, wird es anstelle der einzelnen Zeichen angezeigt, die der Benutzer eingibt. Wenn ein Kenn Wort Zeichen entfernt wird, zeigt das Steuerelement die Zeichen an, die der Benutzer eingibt. Wenn die Anwendung ein einzeitiges Bearbeitungs Steuerelement mit dem Style [**es \_ Password**](edit-control-styles.md)erstellt, ist das Standard Kennwort ein Sternchen ( \* ). Eine Anwendung kann die Nachricht " [**EM \_ setpasswordchar**](em-setpasswordchar.md) " verwenden, um ein anderes Kenn Wort Zeichen zu entfernen oder zu definieren, und die Nachricht " [**EM \_ getpasswordchar**](em-getpasswordchar.md) " zum Abrufen des aktuellen Kenn Wort Zeichens. Diese Nachrichten gelten nur für einzeilige Bearbeitungs Steuerelemente.

## <a name="using-integers"></a>Verwenden von Ganzzahlen

Es gibt zwei ganzzahlige Konvertierungs Funktionen für Bearbeitungs Steuerelemente, die nur Zahlen enthalten sollen. Die [**setdlgitemint**](/windows/desktop/api/winuser/nf-winuser-setdlgitemint) -Funktion erstellt die Zeichen folgen Darstellung einer angegebenen Ganzzahl (mit oder ohne Vorzeichen) und sendet die Zeichenfolge an ein Bearbeitungs Steuerelement. **Setdlgitemint** gibt keinen Wert zurück. Die [**getdlgitemint**](/windows/desktop/api/winuser/nf-winuser-getdlgitemint) -Funktion erstellt eine Ganzzahl (mit oder ohne Vorzeichen) aus der Zeichen folgen Darstellung in einem Bearbeitungs Steuerelement. **Getdlgitemint** gibt die ganze Zahl (oder einen Fehlerwert) zurück.

## <a name="undoing-text-operations"></a>Machen von Text Vorgängen

Jedes Bearbeitungs Steuerelement behält ein rückgängig-Flag bei, das angibt, ob eine Anwendung den letzten Vorgang auf dem Bearbeitungs Steuerelement umkehren oder rückgängig machen kann (z. b. durch das rückgängig machen eines Textes). Das Bearbeitungs Steuerelement legt das rückgängig-Flag fest, um anzugeben, dass der Vorgang rückgängig gemacht werden kann, und setzt ihn zurück, um anzugeben, dass der Vorgang nicht rückgängig gemacht werden Eine Anwendung kann die Einstellung des rückgängigflag ermitteln, indem das Steuerelement eine [**EM \_ CanUndo**](em-canundo.md) -Nachricht sendet.

Eine Anwendung kann den letzten Vorgang rückgängig machen, indem das Steuerelement eine [**EM- \_ Rückgängig**](em-undo.md) Meldung sendet. Ein Vorgang kann rückgängig gemacht werden, sofern kein anderer Bearbeitungs Steuerungs Vorgang zuerst ausgeführt wird. Der Benutzer kann z. b. Text löschen, den Text ersetzen (den Löschvorgang rückgängig machen) und den Text dann erneut löschen (die Ersetzung rückgängig machen). Die **EM- \_ Rückgängig** Meldung gilt sowohl für einzeilige als auch für mehrzeilige Bearbeitungs Steuerelemente und funktioniert immer für einzeilige Bearbeitungs Steuerelemente.

Eine Anwendung kann das rückgängig-Flag eines Bearbeitungs Steuer Elements zurücksetzen, indem das Steuerelement eine [**EM \_ emptyundobuffer**](em-emptyundobuffer.md) -Meldung sendet. Das System setzt das rückgängig-Flag automatisch zurück, wenn ein Bearbeitungs Steuerelement eine [**EM \_ SetHandle**](em-sethandle.md) -oder [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht empfängt. Die [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) -Funktion sendet eine **WM- \_ SetText** -Nachricht.

## <a name="handling-wordwrap-and-line-breaks"></a>Behandeln von WordWrap und Zeilenumbrüchen

Eine Anwendung kann WordWrap-Funktionen mit mehrzeiligen Bearbeitungs Steuerelementen verwenden, um das Wort oder Word-Fragment zu suchen, das in die nächste Zeile umschlossen werden soll. Bei Verwendung der vom System bereitgestellten standardmäßigen WordWrap-Funktion enden Zeilen immer an den Leerzeichen zwischen Wörtern. Eine Anwendung kann Ihre eigene WordWrap-Funktion angeben, indem Sie eine [*editwordbreakproc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) -WordWrap-Funktion bereitstellt und das Bearbeitungs Steuerelement an eine [**EM \_ setwordbreakproc**](em-setwordbreakproc.md) -Nachricht sendet. Eine Anwendung kann die Adresse der aktuellen WordWrap-Funktion abrufen, indem das Steuerelement eine [**EM \_ getwordbreakproc**](em-getwordbreakproc.md) -Nachricht sendet.

Eine Anwendung kann ein mehr zeitiges Bearbeitungs Steuerelement zum Hinzufügen oder Entfernen eines weiche Zeilenumbruch Zeichens (zwei Wagen Rückläufe und ein Zeilenvorschub) am Ende von umschließenden Textzeilen hinzufügen oder entfernen. Eine Anwendung kann diese Funktion aktivieren oder deaktivieren, indem das Bearbeitungs Steuerelement eine [**EM- \_ fmtlines**](em-fmtlines.md) -Meldung sendet. Diese Meldung gilt nur für mehrzeilige Bearbeitungs Steuerelemente und wirkt sich nicht auf eine Zeile aus, die mit einem harten Zeilenumbruch endet (ein Wagen Rücklauf und ein Zeilenvorschub, den der Benutzer eingegeben hat). In mehrzeiligen Bearbeitungs Steuerelementen kann eine Anwendung auch den [**es \_ wantreturn**](edit-control-styles.md) -Stil angeben, um anzufordern, dass das System einen Wagen Rücklauf einfügt, wenn der Benutzer die EINGABETASTE im Bearbeitungs Steuerelement drückt.

## <a name="retrieving-points-and-characters"></a>Abrufen von Punkten und Zeichen

Um das Zeichen zu bestimmen, das einem bestimmten Punkt im Client Bereich eines Bearbeitungs Steuer Elements am nächsten liegt, senden Sie die [**EM \_ charfrompos**](em-charfrompos.md) -Nachricht an das-Steuerelement. Die Meldung gibt den Zeichen Index und den Zeilen Index des Zeichens zurück, das dem Punkt am nächsten liegt. Auf ähnliche Weise können Sie die Client Bereichs Koordinaten eines angegebenen Zeichens abrufen, indem Sie die [**EM \_ posfromchar**](em-posfromchar.md) -Nachricht senden. Die Meldung gibt die x-und y-Koordinaten der linken oberen Ecke des angegebenen Zeichens zurück.

## <a name="autocompletion-of-strings"></a>Automatische Vervollständigung von Zeichen folgen

Die automatische Vervollständigung erweitert Zeichen folgen, die teilweise in einem Bearbeitungs Steuerelement eingegeben wurden, in vollständige Zeichen folgen. Wenn ein Benutzer beispielsweise mit der Eingabe einer URL im Adress Bearbeitungs Steuerelement beginnt, das in der Windows Internet Explorer-Symbolleiste eingebettet ist, erweitert die automatische Vervollständigung die Zeichenfolge in eine oder mehrere vollständige URLs, die mit der vorhandenen partiellen Zeichenfolge konsistent sind. Eine partielle URL-Zeichenfolge, z. b. "MIC", kann auf " https://www.microsoft.com " oder "" erweitert werden https://www.microsoft.com/windows . Die automatische Vervollständigung wird normalerweise mit Bearbeitungs Steuerelementen oder mit Steuerelementen verwendet, die ein eingebettetes Bearbeitungs Steuerelement aufweisen

Weitere Informationen finden Sie in der Dokumentation zur [**iautocomplete**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete) -und [**IAutoComplete2**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete2) -Schnittstelle.

## <a name="complex-script-in-edit-controls"></a>Komplexes Skript in Bearbeitungs Steuerelementen

Ein *komplexes Skript* ist eine Sprache, deren gedruckte Form nicht auf einfache Weise angelegt ist. Ein komplexes Skript kann z. b. ein bidirektionales Rendering, eine kontextabhängige Strukturierung von Symbolen oder das Kombinieren von Zeichen ermöglichen. Die standardmäßigen Bearbeitungs Steuerelemente wurden erweitert, um mehrsprachigen Text und komplexe Skripts zu unterstützen. Dies umfasst nicht nur die Eingabe und Anzeige, sondern auch die korrekte Cursor Bewegung über Zeichen Cluster (z. b. in einem Thai-und Devanagari-Skript).

Eine gut geschriebene Anwendung empfängt diese Unterstützung automatisch, ohne Änderungen. Auch hier sollten Sie die Unterstützung für die Lesefolge und die Rechte Ausrichtung von rechts nach Links hinzufügen. Schalten Sie in diesem Fall die erweiterten stilflags des Fensters Bearbeitungs Steuerelement ein, um diese Attribute zu steuern, wie im folgenden Beispiel gezeigt.


```
// ID_EDITCONTROL is the control ID in the resource file.
HANDLE hWndEdit = GetDlgItem(hDlg, ID_EDITCONTROL);
LONG lAlign = GetWindowLong(hWndEdit, GWL_EXSTYLE) ;

// To toggle alignment
lAlign ^= WS_EX_RIGHT ;

// To toggle reading order
lAlign ^= WS_EX_RTLREADING ;
```



Nachdem Sie den **lalign** -Wert festgelegt haben, aktivieren Sie die neue Anzeige, indem Sie den erweiterten Stil des Fensters Bearbeitungs Steuerelement wie folgt festlegen.


```
// This assumes your edit control is in a dialog box. If not, 
// get the edit control handle from another source.

SetWindowLong(hWndEdit, GWL_EXSTYLE, lAlign);
InvalidateRect(hWndEdit, NULL, FALSE);
```



Uniscriist ein weiterer Satz von Funktionen, die eine Feinsteuerung der Verarbeitung komplexer Skripts ermöglichen. Weitere Informationen finden Sie unter [uniscri.](/windows/desktop/Intl/uniscribe)

 

 