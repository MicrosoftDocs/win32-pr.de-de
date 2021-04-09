---
title: Schaltflächenmeldungen
description: Eine Schaltfläche kann Nachrichten an das übergeordnete Fenster senden, und ein übergeordnetes Fenster kann Nachrichten an eine Schaltfläche Senden.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1601f269ec1242a10579d2ace812723d3ead7f84
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103734041"
---
# <a name="button-messages"></a>Schaltflächenmeldungen

Eine Schaltfläche kann Nachrichten an das übergeordnete Fenster senden, und ein übergeordnetes Fenster kann Nachrichten an eine Schaltfläche Senden.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Senden von Nachrichten an Schaltflächen](#sending-messages-to-buttons)
-   [Verarbeiten von Nachrichten über eine Schaltfläche](#handling-messages-from-a-button)
-   [Benachrichtigungs Meldungen von Schaltflächen](#notification-messages-from-buttons)
-   [Schaltflächen-Farb Meldungen](#button-color-messages)
-   [Schaltfläche Standard Nachrichtenverarbeitung](#button-default-message-processing)
-   [Zugehörige Themen](#related-topics)

## <a name="sending-messages-to-buttons"></a>Senden von Nachrichten an Schaltflächen

Ein übergeordnetes Fenster kann mithilfe der [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion Meldungen an eine Schaltfläche in einem überlappenden oder untergeordneten Fenster senden oder Nachrichten mithilfe der Funktionen [**SendDlgItemMess**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**checkdlgbutton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**checkradio Button**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)und [**isdlgbuttoncheckan**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) eine Schaltfläche in einem Dialogfeld senden.

Eine Anwendung kann die [**BM \_ getcheck**](bm-getcheck.md) -Nachricht verwenden, um den Status der Überprüfung eines Kontrollkästchens oder Options Felds abzurufen. Eine Anwendung kann auch die [**BM \_ GetState**](bm-getstate.md) -Nachricht verwenden, um die aktuellen Status der Schaltfläche abzurufen (den Prüf Zustand, den pushzustand und den Fokus Zustand). Um Informationen zu einem bestimmten Zustand zu erhalten, verwenden Sie eine Bitmaske für den zurückgegebenen Statuswert.

Die [**BM- \_ setcheck**](bm-setcheck.md) -Nachricht legt den Kontrollzustand eines Kontrollkästchens oder Options Felds fest. die Meldung gibt 0 (null) zurück. Die [**BM- \_ SetState**](bm-setstate.md) -Meldung legt den pushzustand einer Schaltfläche fest. diese Meldung gibt auch 0 (null) zurück. Die [**BM- \_ SetStyle**](bm-setstyle.md) -Nachricht ändert den Stil einer Schaltfläche. Er dient zum Ändern von Schaltflächen Formaten innerhalb eines Typs (z. b. Ändern eines Kontrollkästchens in ein automatisches Kontrollkästchen). Sie ist nicht für die Änderung zwischen Typen (z. b. Ändern eines Kontrollkästchens in ein Optionsfeld) konzipiert. Eine Anwendung sollte keine Schaltfläche von einem Typ in einen anderen ändern.

Eine Schaltfläche mit dem [**\_ Symbol**](button-styles.md) Stil " [**SB \_ Bitmap**](button-styles.md) " oder "SB" zeigt anstelle von Text eine Bitmap oder ein Symbol an. Die [**BM \_**](bm-setimage.md) -abtader Nachricht verknüpft ein Handle mit einer Schaltfläche zu einer Bitmap oder einem Symbol. Die [**BM \_ GetImage**](bm-getimage.md) -Nachricht Ruft ein Handle für das Bitmap oder Symbol ab, das einer Schaltfläche zugeordnet ist.

Eine Anwendung kann auch die [**DM \_ getdefid-**](/windows/desktop/dlgbox/dm-getdefid) Nachricht verwenden, um den Bezeichner des Standard Steuer Elements der Push-Schaltfläche in einem Dialogfeld abzurufen. Eine Anwendung kann die " [**DM \_ setdefid"-**](/windows/desktop/dlgbox/dm-setdefid) Meldung verwenden, um die Standard-pushschaltfläche für ein Dialogfeld festzulegen.

Das Aufrufen der [**checkdlgbutton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) -oder [**checkradiobutton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) -Funktion entspricht dem Senden einer [**BM- \_ setcheck**](bm-setcheck.md) -Nachricht. Das Aufrufen der [**isdlgbuttoncheck-**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) Funktion entspricht dem Senden einer [**BM \_ getcheck**](bm-getcheck.md) -Nachricht.

## <a name="handling-messages-from-a-button"></a>Verarbeiten von Nachrichten über eine Schaltfläche

Benachrichtigungen von einer Schaltfläche werden entweder als [**WM- \_ Befehl**](/windows/desktop/menurc/wm-command) oder als [**WM- \_ Benachrichtigungs**](wm-notify.md) Nachrichten gesendet. Informationen dazu, welche Nachricht verwendet wird, finden Sie auf der Referenzseite für jede Benachrichtigung.

Weitere Informationen zum Verarbeiten von Nachrichten finden Sie unter [Control Messages](control-messages.md). Siehe auch Schaltflächen Meldungen.

## <a name="notification-messages-from-buttons"></a>Benachrichtigungs Meldungen von Schaltflächen

Wenn der Benutzer auf eine Schaltfläche klickt, wird der Status geändert, und die Schaltfläche sendet Benachrichtigungs Codes in Form von [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldungen an das übergeordnete Fenster. Beispielsweise sendet ein Push-Schaltflächen-Steuerelement den auf der Benutzer auf die Schaltfläche [ \_ angeklickten](bn-clicked.md) Wert der Milliarde. In allen Fällen (mit Ausnahme von [BCN- \_ betitemchange](bcn-hotitemchange.md)) enthält das nieder wertige Wort des *wParam* -Parameters den Steuerelement Bezeichner, das hochwertige Wort von *wParam* enthält den Benachrichtigungs Code, und der *LPARAM* -Parameter enthält das Steuerelement Fenster handle.

Sowohl die Nachricht als auch die Antwort des übergeordneten Fensters hängen vom Typ, Format und aktuellen Zustand der Schaltfläche ab. Im folgenden sind die Schaltflächen-Benachrichtigungs Codes, die eine Anwendung überwachen und verarbeiten soll



| Benachrichtigungs Code                                                        | BESCHREIBUNG                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [BCN- \_ hubänderung](bcn-hotitemchange.md)                              | Die Maus hat den Client Bereich einer Schaltfläche eingegeben oder verlassen. |
| [auf BN \_ geklickt](bn-clicked.md)                                            | Der Benutzer hat auf eine Schaltfläche geklickt.                             |
| [BN \_ Dblclk](bn-dblclk.md) oder [BN- \_ Doppel](bn-doubleclicked.md) Klick | Der Benutzer hat auf eine Schaltfläche Doppel geklickt.                      |
| [BN \_ Deaktivieren](bn-disable.md)                                            | Eine Schaltfläche ist deaktiviert.                                  |
| [BN \_ Per pushübertragung](bn-pushed.md) oder [Milliarde \_ Hilite](bn-hilite.md)               | Der Benutzer hat eine Schaltfläche gedrückt.                              |
| [BN- \_ killfokus](bn-killfocus.md)                                        | Die Schaltfläche hat den Tastaturfokus verloren.                    |
| [BN- \_ Paint](bn-paint.md)                                                | Die Schaltfläche sollte gezeichnet werden.                          |
| [BN- \_ SetFocus](bn-setfocus.md)                                          | Die Schaltfläche hat den Tastaturfokus erhalten.                  |
| [BN \_ Nicht per pushübertragung](bn-unpushed.md) oder [Milliarde \_ unhilite](bn-unhilite.md)       | Die Schaltfläche wird nicht mehr per pushübertragung übermittelt.                        |



 

Mit einer Schaltfläche werden die Benachrichtigungs Codes " [BN \_ deaktiviert](bn-disable.md)", " [BN \_ gepusht](bn-pushed.md)", " [BN- \_ killfocus](bn-killfocus.md)", "bn [ \_ Paint](bn-paint.md)", " [BN \_ SetFocus](bn-setfocus.md)" und " [BN \_](bn-unpushed.md) " nur dann gesendet, [**Wenn die \_**](button-styles.md) [BN \_ Dblclk](bn-dblclk.md) -Benachrichtigungs Codes werden automatisch für die Schaltflächen " [**\_ Benutzer Schaltfläche**](button-styles.md)", " [**SB- \_ RadioButton**](button-styles.md)" und " [**b \_**](button-styles.md) Andere Schaltflächen Typen senden \_ nur dann eine Milliarde dblclk, wenn Sie über das Format "Schriftarten **\_ Benachrichtigen** " verfügen Alle Schaltflächen senden den von der [Milliarde \_ angeklickten](bn-clicked.md) Benachrichtigungs Code unabhängig von den Schaltflächen Stilen

Für automatische Schaltflächen ändert das System den pushzustand und zeichnet die Schaltfläche. In diesem Fall [verarbeitet die Anwendung \_ ](bn-clicked.md) i. [d. d. \_ d](bn-dblclk.md) . a Für Schaltflächen, die nicht automatisch sind, antwortet die Anwendung in der Regel auf den Benachrichtigungs Code, indem eine Nachricht gesendet wird, um den Zustand der Schaltfläche zu ändern. Informationen zum Senden von Nachrichten an Schaltflächen finden Sie unter [Senden von Nachrichten an Schalt](#sending-messages-to-buttons)Flächen.

Wenn der Benutzer eine vom Besitzer gezeichnete Schaltfläche auswählt, sendet die Schaltfläche seinem übergeordneten Fenster eine [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht, die den Bezeichner des Steuer Elements enthält, das gezeichnet werden soll, sowie Informationen zu den Dimensionen und dem Zustand

## <a name="button-color-messages"></a>Schaltflächen-Farb Meldungen

Das System stellt Standard Farbwerte für Schaltflächen bereit. Eine Anwendung kann die Standardwerte für diese Farben abrufen, indem Sie die [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) -Funktion aufruft, oder die Werte durch Aufrufen der Funktion [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) festlegen. In der folgenden Tabelle werden die Standardwerte für die Schaltflächen Farbe angezeigt.



| Wert               | Farbiges Element                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| Farbe ( \_ btnface)      | Schaltflächen Flächen.                                                                                                              |
| Farbe \_ btnhervorhebung | Markieren Sie den Bereich (die oberen und linken Kanten) einer Schaltfläche.                                                                       |
| Farbe \_ btnshadow    | Der Schattenbereich (der untere und der Rechte Rand) einer Schaltfläche.                                                                      |
| Farbe \_ btntext      | Regulärer (nicht ausgegrauter) Text in Schaltflächen.                                                                                       |
| Farbe \_ grau Text     | Deaktivierter (grauer) Text in Schaltflächen. Diese Farbe wird auf 0 festgelegt, wenn der aktuelle Anzeigetreiber keine ausgefüllte graue Farbe unterstützt. |
| Farb \_ Fenster       | Fenster Hintergründe.                                                                                                        |
| Color \_ WindowFrame  | Fensterrahmen.                                                                                                             |
| \_WindowText-Farbe   | Text in Windows.                                                                                                           |



 

Allerdings wirkt sich das Aufrufen von [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) auf alle Anwendungen aus. Daher sollten Sie diese Funktion nicht aufrufen, um die Schaltflächen für die Anwendung anzupassen.

Das System sendet eine [**WM \_ ctlcolorbtn**](wm-ctlcolorbtn.md) -Meldung an das übergeordnete Fenster einer Schaltfläche, bevor eine Schaltfläche gezeichnet wird. Diese Meldung enthält ein Handle für den Gerätekontext der Schaltfläche und ein Handle für das untergeordnete Fenster. Das übergeordnete Fenster kann diese Handles verwenden, um die Text-und Hintergrundfarben der Schaltfläche zu ändern. Allerdings reagieren nur vom Besitzer gezeichnete Schaltflächen auf das übergeordnete Fenster, das die Nachricht verarbeitet.

## <a name="button-default-message-processing"></a>Schaltfläche Standard Nachrichtenverarbeitung

Die Fenster Prozedur für die vordefinierte Schaltflächen Steuerelement-Fenster Klasse führt die Standard Verarbeitung für alle Meldungen aus, die von der Schaltflächen-Steuerelement Prozedur nicht verarbeitet werden Wenn die Schaltflächen-Steuerelement Prozedur für jede Nachricht **false** zurückgibt, prüft die vordefinierte Fenster Prozedur die Nachrichten und führt die in der folgenden Tabelle aufgeführten Standard Aktionen aus.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>`Message`</th>
<th>Standardaktion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="bm-click.md"><strong>BM_CLICK</strong></a></td>
<td>Sendet die Schaltfläche a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> und eine <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> Meldung und sendet dem übergeordneten Fenster einen <a href="bn-clicked.md">BN_CLICKED</a> Benachrichtigungs Code.</td>
</tr>
<tr class="even">
<td><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></td>
<td>Gibt den Prüf Zustand der Schaltfläche zurück.</td>
</tr>
<tr class="odd">
<td><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></td>
<td>Gibt ein Handle für das Bitmap oder Symbol zurück, das der Schaltfläche zugeordnet ist, oder <strong>null</strong> , wenn die Schaltfläche keine Bitmap oder ein Symbol aufweist.</td>
</tr>
<tr class="even">
<td><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></td>
<td>Gibt den aktuellen Prüf Zustand, den pushzustand und den Fokus Zustand der Schaltfläche zurück.</td>
</tr>
<tr class="odd">
<td><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></td>
<td>Legt den Status der Überprüfung für alle Stile von Options Feldern und Kontrollkästchen fest. Wenn der <em>wParam</em> -Parameter für options Felder größer als 0 (null) ist, erhält die Schaltfläche den <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> Stil.</td>
</tr>
<tr class="even">
<td><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></td>
<td>Ordnet die angegebene Bitmap oder das angegebene Symbol Handle der Schaltfläche zu und gibt ein Handle für das vorherige Bitmap oder Symbol zurück.</td>
</tr>
<tr class="odd">
<td><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></td>
<td>Legt den pushzustand der Schaltfläche fest. Bei vom Besitzer gezeichneten Schaltflächen wird eine <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> Meldung an das übergeordnete Fenster gesendet, wenn sich der Zustand der Schaltfläche geändert hat.</td>
</tr>
<tr class="even">
<td><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></td>
<td>Legt den Schaltflächen Stil fest. Wenn das nieder wertige Wort des <em>LPARAM</em> -Parameters <strong>true</strong>ist, wird die Schaltfläche neu gezeichnet.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></td>
<td>Prüft ein Kontrollkästchen oder ein automatisches Kontrollkästchen, wenn der Benutzer die Plus-(+) oder gleich (=)-Taste drückt. Löscht ein Kontrollkästchen oder ein automatisches Kontrollkästchen, wenn der Benutzer die Minus Taste (–) drückt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></td>
<td>Zeichnet die Schaltfläche.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></td>
<td>Löscht den Hintergrund für vom Besitzer gezeichnete Schaltflächen. Die Hintergründe anderer Schaltflächen werden als Teil der <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> -und <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> Verarbeitung gelöscht.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></td>
<td>Gibt Werte zurück, die den Typ der Eingabe angeben, die von der Standard Schaltfläche Prozedur verarbeitet wird, wie in der folgenden Tabelle dargestellt. 
<table>
<thead>
<tr class="header">
<th>Schaltflächen Stil</th>
<th>Gibt zurück</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS | DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS | DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></td>
<td>DLGC_DEFPUSHBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></td>
<td>DLGC_STATIC</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></td>
<td>DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON | DLGC_BUTTON</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></td>
<td>Gibt ein Handle für die aktuelle Schriftart zurück.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></td>
<td>Drückt die Schaltfläche, wenn der Benutzer die LEERTASTE drückt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></td>
<td>Gibt die Maus Aufzeichnung für alle Fälle außer der Tab-Taste frei.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></td>
<td>Entfernt das Fokus Rechteck aus einer Schaltfläche. Für pushschaltflächen und Standard-Push-Schaltflächen wird das Fokus Rechteck ungültig. Wenn die Schaltfläche die Maus Aufzeichnung enthält, wird die Erfassung freigegeben, die Schaltfläche wird nicht geklickt, und jeder pushzustand wird entfernt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></td>
<td>Sendet eine <a href="bn-dblclk.md">BN_DBLCLK</a> Benachrichtigungs Codes an das übergeordnete Fenster für options Felder und vom Besitzer gezeichnete Schaltflächen. Bei anderen Schaltflächen wird ein Doppelklick als <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> Nachricht verarbeitet.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></td>
<td>Hebt die Schaltfläche hervor, wenn sich die Position des Mauszeigers innerhalb des Client Rechtecks der Schaltfläche befindet.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></td>
<td>Gibt die Maus Aufzeichnung frei, wenn die Schaltfläche die Maus Aufzeichnung aufwies.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></td>
<td>Führt dieselbe Aktion wie <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>aus, wenn die Schaltfläche die Maus Aufzeichnung aufweist. Andernfalls wird keine Aktion ausgeführt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></td>
<td>Schaltet eine beliebige <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> Schaltfläche in eine Schaltfläche <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></td>
<td>Gibt "httransparent" zurück, wenn das Schaltflächen-Steuerelement ein Gruppenfeld ist.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></td>
<td>Zeichnet die Schaltfläche nach Ihrem Stil und dem aktuellen Zustand.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></td>
<td>Zeichnet ein Fokus Rechteck auf der Schaltfläche, die den Fokus erhält. Für options Felder und automatische Options Felder wird das übergeordnete Fenster als <a href="bn-clicked.md">BN_CLICKED</a> Benachrichtigungs Code gesendet.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></td>
<td>Legt eine neue Schriftart fest und aktualisiert optional das Fenster.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></td>
<td>Legt den Text der Schaltfläche fest. Im Fall eines Gruppen Felds zeichnet die Meldung den bereits vorhandenen Text, bevor das Gruppenfeld mit dem neuen Text neu gezeichnet wird.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></td>
<td>Gibt die Maus Aufzeichnung für alle Fälle außer der Tab-Taste frei.</td>
</tr>
</tbody>
</table>



 

Die vordefinierte Fenster Prozedur übergibt alle anderen Nachrichten zur Standard Verarbeitung an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern von Meldungen](control-messages.md)
</dt> </dl>

 

 