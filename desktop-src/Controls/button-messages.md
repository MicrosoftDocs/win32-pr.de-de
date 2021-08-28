---
title: Schaltflächenmeldungen
description: Eine Schaltfläche kann Nachrichten an das übergeordnete Fenster senden, und ein übergeordnetes Fenster kann Nachrichten an eine Schaltfläche senden.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136310a3718f17900f604287bf78186f7c927259
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625716"
---
# <a name="button-messages"></a>Schaltflächenmeldungen

Eine Schaltfläche kann Nachrichten an das übergeordnete Fenster senden, und ein übergeordnetes Fenster kann Nachrichten an eine Schaltfläche senden.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Senden von Nachrichten an Schaltflächen](#sending-messages-to-buttons)
-   [Verarbeiten von Nachrichten über eine Schaltfläche](#handling-messages-from-a-button)
-   [Benachrichtigungsmeldungen von Schaltflächen](#notification-messages-from-buttons)
-   [Schaltflächenfarbmeldungen](#button-color-messages)
-   [Standardnachrichtenverarbeitung für Schaltflächen](#button-default-message-processing)
-   [Zugehörige Themen](#related-topics)

## <a name="sending-messages-to-buttons"></a>Senden von Nachrichten an Schaltflächen

Ein übergeordnetes Fenster kann Mithilfe der [**SendMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-sendmessage) Nachrichten an eine Schaltfläche in einem überlappenden oder untergeordneten Fenster senden, oder es kann Nachrichten an eine Schaltfläche in einem Dialogfeld senden, indem die Funktionen [**SendDlgItemMessage,**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) [**CheckDlgButton,**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)und [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) verwendet werden.

Eine Anwendung kann die [**BM \_ GETCHECK-Nachricht**](bm-getcheck.md) verwenden, um den Prüfzustand eines Kontrollkästchens oder Optionsfelds abzurufen. Eine Anwendung kann auch die [**BM \_ GETSTATE-Nachricht**](bm-getstate.md) verwenden, um die aktuellen Zustände der Schaltfläche abzurufen (Überprüfungsstatus, Pushzustand und Fokuszustand). Um Informationen zu einem bestimmten Zustand abzurufen, verwenden Sie eine Bitmaske für den zurückgegebenen Zustandswert.

Die [**BM \_ SETCHECK-Nachricht**](bm-setcheck.md) legt den Prüfzustand eines Kontrollkästchens oder Optionsfelds fest. Die Meldung gibt 0 (null) zurück. Die [**BM \_ SETSTATE-Nachricht**](bm-setstate.md) legt den Pushzustand einer Schaltfläche fest. Diese Nachricht gibt auch 0 (null) zurück. Die [**BM \_ SETSTYLE-Nachricht**](bm-setstyle.md) ändert den Stil einer Schaltfläche. Sie ist für das Ändern von Schaltflächenstilen innerhalb eines Typs konzipiert (z. B. das Ändern eines Kontrollkästchens in ein automatisches Kontrollkästchen). Sie ist nicht für das Ändern zwischen Typen konzipiert (z. B. das Ändern eines Kontrollkästchens in ein Optionsfeld). Eine Anwendung sollte eine Schaltfläche nicht von einem Typ in einen anderen ändern.

Eine Schaltfläche im [**\_ BS-BITMAP-**](button-styles.md) oder [**\_ BS-SYMBOLformat**](button-styles.md) zeigt eine Bitmap oder ein Symbol anstelle von Text an. Die [**BM \_ SETIMAGE-Nachricht**](bm-setimage.md) ordnet ein Handle einer Bitmap oder einem Symbol einer Schaltfläche zu. Die [**BM \_ GETIMAGE-Nachricht**](bm-getimage.md) ruft ein Handle für die Bitmap oder das Symbol ab, das einer Schaltfläche zugeordnet ist.

Eine Anwendung kann auch die [**DM \_ GETDEFID-Nachricht**](/windows/desktop/dlgbox/dm-getdefid) verwenden, um den Bezeichner des standardgesteuerten Schaltflächensteuerelements in einem Dialogfeld abzurufen. Eine Anwendung kann die [**DM \_ SETDEFID-Nachricht**](/windows/desktop/dlgbox/dm-setdefid) verwenden, um die Standard-Pushschaltfläche für ein Dialogfeld festzulegen.

Das Aufrufen der [**CheckDlgButton-**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) oder [**CheckRadioButton-Funktion**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) entspricht dem Senden einer [**BM \_ SETCHECK-Nachricht.**](bm-setcheck.md) Das Aufrufen der [**IsDlgButtonChecked-Funktion**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) entspricht dem Senden einer [**BM \_ GETCHECK-Nachricht.**](bm-getcheck.md)

## <a name="handling-messages-from-a-button"></a>Verarbeiten von Nachrichten über eine Schaltfläche

Benachrichtigungen von einer Schaltfläche werden entweder als [**WM \_ COMMAND-**](/windows/desktop/menurc/wm-command) oder [**WM \_ NOTIFY-Nachrichten**](wm-notify.md) gesendet. Informationen dazu, welche Nachricht verwendet wird, finden Sie auf der Referenzseite für jede Benachrichtigung.

Weitere Informationen zum Behandeln von Nachrichten finden Sie unter Steuern von [Nachrichten.](control-messages.md) Siehe auch Schaltflächenmeldungen.

## <a name="notification-messages-from-buttons"></a>Benachrichtigungsmeldungen von Schaltflächen

Wenn der Benutzer auf eine Schaltfläche klickt, ändert sich der Status, und die Schaltfläche sendet Benachrichtigungscodes in Form von [**WM \_ COMMAND-Nachrichten**](/windows/desktop/menurc/wm-command) an das übergeordnete Fenster. Beispielsweise sendet ein Schaltflächen-Steuerelement den [BN CLICKED-Benachrichtigungscode, \_ ](bn-clicked.md) wenn der Benutzer die Schaltfläche ausgibt. In allen Fällen (mit Ausnahme von [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)) enthält das Wort mit niedriger Reihenfolge des *wParam-Parameters* den Steuerelementbezeichner, das Wort in hoher Reihenfolge von *wParam* den Benachrichtigungscode, und der *lParam-Parameter* enthält das Steuerelementfensterhandle.

Sowohl die Nachricht als auch die Antwort des übergeordneten Fensters hängen vom Typ, Stil und aktuellen Zustand der Schaltfläche ab. Im Folgenden werden die Schaltflächenbenachrichtigungscodes angezeigt, die eine Anwendung überwachen und verarbeiten soll.



| Benachrichtigungscode                                                        | Beschreibung                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)                              | Die Maus hat den Clientbereich einer Schaltfläche eingegeben oder verlassen. |
| [BN \_ GEKLICKT](bn-clicked.md)                                            | Der Benutzer hat auf eine Schaltfläche geklickt.                             |
| [BN \_ DBLCLK](bn-dblclk.md) oder [BN \_ DOUBLECLICKED](bn-doubleclicked.md) | Der Benutzer hat auf eine Schaltfläche doppelklicken können.                      |
| [BN \_ DISABLE](bn-disable.md)                                            | Eine Schaltfläche ist deaktiviert.                                  |
| [BN \_ PUSHED](bn-pushed.md) oder [BN \_ HILITE](bn-hilite.md)               | Der Benutzer hat eine Schaltfläche gedrückt.                              |
| [BN \_ KILLFOCUS](bn-killfocus.md)                                        | Die Schaltfläche hat den Tastaturfokus verloren.                    |
| [BN \_ PAINT](bn-paint.md)                                                | Die Schaltfläche sollte gezeichnet werden.                          |
| [BN \_ SETFOCUS](bn-setfocus.md)                                          | Die Schaltfläche hat den Tastaturfokus erhalten.                  |
| [BN \_ UNPUSHED](bn-unpushed.md) oder [BN \_ UNHILITE](bn-unhilite.md)       | Die Schaltfläche wird nicht mehr gepusht.                        |



 

Eine Schaltfläche sendet die Benachrichtigungscodes [BN \_ DISABLE,](bn-disable.md) [BN \_ PUSHED,](bn-pushed.md) [BN \_ KILLFOCUS,](bn-killfocus.md) [BN \_ PAINT,](bn-paint.md) [BN \_ SETFOCUS](bn-setfocus.md)und [BN \_ UNPUSHED](bn-unpushed.md) nur dann, wenn sie den [**BS \_ NOTIFY-Stil**](button-styles.md) haben. [BN \_ DBLCLK-Benachrichtigungscodes](bn-dblclk.md) werden automatisch für die Schaltflächen [**BS \_ USERBUTTON,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)und [**BS \_ OWNERDRAW**](button-styles.md) gesendet. Andere Schaltflächentypen senden BN \_ DBLCLK nur, wenn sie den **BS \_ NOTIFY-Stil** aufweisen. Alle Schaltflächen senden den [BN CLICKED-Benachrichtigungscode \_ ](bn-clicked.md) unabhängig von ihren Schaltflächenstilen.

Bei automatischen Schaltflächen ändert das System den Pushzustand und zeichnet die Schaltfläche. In diesem Fall verarbeitet die Anwendung in der Regel nur die Benachrichtigungscodes [BN \_ CLICKED](bn-clicked.md) und [BN \_ DBLCLK.](bn-dblclk.md) Bei Schaltflächen, die nicht automatisch sind, antwortet die Anwendung in der Regel auf den Benachrichtigungscode, indem sie eine Nachricht sendet, um den Zustand der Schaltfläche zu ändern. Informationen zum Senden von Nachrichten an Schaltflächen finden Sie unter [Senden von Nachrichten an Schaltflächen.](#sending-messages-to-buttons)

Wenn der Benutzer eine vom Besitzer gezeichnete Schaltfläche auswählt, sendet die Schaltfläche dem übergeordneten Fenster eine [**WM \_ DRAWITEM-Meldung,**](wm-drawitem.md) die den Bezeichner des zu zeichnenden Steuerelements und Informationen zu dessen Dimensionen und Zustand enthält.

## <a name="button-color-messages"></a>Schaltflächenfarbmeldungen

Das System stellt Standardfarbwerte für Schaltflächen bereit. Eine Anwendung kann die Standardwerte für diese Farben abrufen, indem sie die [**GetSysColor-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) aufruft, oder die Werte durch Aufrufen der [**SetSysColors-Funktion**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) festlegen. In der folgenden Tabelle sind die Standardwerte für Schaltflächenfarben aufgeführt.



| Wert               | Elementfarbe                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| COLOR \_ BTNFACE      | Schaltflächenflächen.                                                                                                              |
| COLOR \_ BTNHIGHLIGHT | Hervorhebungsbereich (oberer und linker Rand) einer Schaltfläche.                                                                       |
| COLOR \_ BTNSHADOW    | Schattenbereich (der untere und rechte Rand) einer Schaltfläche.                                                                      |
| COLOR \_ BTNTEXT      | Regulärer (nicht grayed) Text in Schaltflächen.                                                                                       |
| COLOR \_ GRAYTEXT     | Deaktivierter (grauer) Text in Schaltflächen. Diese Farbe wird auf 0 festgelegt, wenn der aktuelle Anzeigetreiber keine vollgraue Farbe unterstützt. |
| \_FARBFENSTER       | Fensterhintergrund.                                                                                                        |
| COLOR \_ WINDOWFRAME  | Fensterrahmen.                                                                                                             |
| COLOR \_ WINDOWTEXT   | Text in Fenstern.                                                                                                           |



 

Das Aufrufen von [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) wirkt sich jedoch auf alle Anwendungen aus, daher sollten Sie diese Funktion nicht aufrufen, um Schaltflächen für Ihre Anwendung anzupassen.

Das System sendet eine [**\_ WM-CTLCOLORBTN-Nachricht**](wm-ctlcolorbtn.md) an das übergeordnete Fenster einer Schaltfläche, bevor eine Schaltfläche gezeichnet wird. Diese Meldung enthält ein Handle für den Gerätekontext der Schaltfläche und ein Handle für das untergeordnete Fenster. Das übergeordnete Fenster kann diese Handles verwenden, um den Text und die Hintergrundfarben der Schaltfläche zu ändern. Allerdings reagieren nur vom Besitzer gezeichnete Schaltflächen auf das übergeordnete Fenster, das die Nachricht verarbeitet.

## <a name="button-default-message-processing"></a>Standardnachrichtenverarbeitung für Schaltflächen

Die Fensterprozedur für die vordefinierte Schaltflächen-Steuerelementfensterklasse führt die Standardverarbeitung für alle Nachrichten durch, die von der Schaltflächensteuerelementprozedur nicht verarbeitet werden. Wenn die Schaltflächensteuerelementprozedur **FALSE** für eine Nachricht zurückgibt, überprüft die vordefinierte Fensterprozedur die Meldungen und führt die in der folgenden Tabelle aufgeführten Standardaktionen aus.



<table>
<colgroup>
<col  />
<col  />
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
<td>Sendet der Schaltfläche eine <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> und <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>eine</strong></a> WM_LBUTTONUP und sendet dem übergeordneten Fenster einen BN_CLICKED Benachrichtigungscode. <a href="bn-clicked.md"></a></td>
</tr>
<tr class="even">
<td><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></td>
<td>Gibt den Überprüfungszustand der Schaltfläche zurück.</td>
</tr>
<tr class="odd">
<td><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></td>
<td>Gibt ein Handle für die Bitmap oder das Symbol zurück, die der Schaltfläche zugeordnet ist, oder <strong>NULL,</strong> wenn die Schaltfläche keine Bitmap oder kein Symbol enthält.</td>
</tr>
<tr class="even">
<td><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></td>
<td>Gibt den aktuellen Überprüfungs-, Push- und Fokuszustand der Schaltfläche zurück.</td>
</tr>
<tr class="odd">
<td><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></td>
<td>Legt den Überprüfungszustand für alle Stile von Optionsfeldern und Kontrollkästchen fest. Wenn der <em>wParam-Parameter</em> für Optionsfelder größer als 0 (null) ist, erhält die Schaltfläche die <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> Format.</td>
</tr>
<tr class="even">
<td><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></td>
<td>Ordnet der Schaltfläche das angegebene Bitmap- oder Symbolhand handle zu und gibt ein Handle zur vorherigen Bitmap oder dem vorherigen Symbol zurück.</td>
</tr>
<tr class="odd">
<td><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></td>
<td>Legt den Pushzustand der Schaltfläche fest. Bei vom Besitzer gezeichneten Schaltflächen <a href="wm-drawitem.md"><strong>wird WM_DRAWITEM</strong></a> nachricht an das übergeordnete Fenster gesendet, wenn sich der Zustand der Schaltfläche geändert hat.</td>
</tr>
<tr class="even">
<td><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></td>
<td>Legt das Schaltflächenformat fest. Wenn das niedrige Wort des <em>lParam-Parameters</em> <strong>TRUE</strong>ist, wird die Schaltfläche neu gezeichnet.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></td>
<td>Überprüft ein Kontrollkästchen oder automatisches Kontrollkästchen, wenn der Benutzer die Plustasten (+) oder gleich (=) drückt. Setzt ein Kontrollkästchen oder automatisches Kontrollkästchen frei, wenn der Benutzer die Minustaste (–) drückt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></td>
<td>Zeichnet die Schaltfläche.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></td>
<td>Löscht den Hintergrund für vom Besitzer gezeichnete Schaltflächen. Die Hintergründe anderer Schaltflächen werden im Rahmen der WM_PAINT <a href="/windows/desktop/gdi/wm-paint"><strong>und</strong></a> <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> gelöscht.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></td>
<td>Gibt Werte zurück, die den Typ der Eingabe angeben, die von der Standardschaltfläche verarbeitet wird, wie in der folgenden Tabelle gezeigt. 
<table>
<thead>
<tr class="header">
<th>Schaltflächenformat</th>
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

<p> </p></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></td>
<td>Gibt ein Handle für die aktuelle Schriftart zurück.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></td>
<td>Drückt die Schaltfläche, wenn der Benutzer die SPACEBAR drückt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></td>
<td>Gibt die Mauserfassung für alle Fälle außer der TAB-TASTE frei.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></td>
<td>Entfernt das Fokusrechteck aus einer Schaltfläche. Bei Pushschaltflächen und Standardtasten wird das Fokusrechteck ungültig. Wenn die Schaltfläche über die Mausaufnahme verfügt, wird die Aufnahme freigegeben, auf die Schaltfläche wird nicht geklickt, und ein Pushzustand wird entfernt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></td>
<td>Sendet einen <a href="bn-dblclk.md">BN_DBLCLK</a> Benachrichtigungscode an das übergeordnete Fenster für Optionsfelder und vom Besitzer gezeichnete Schaltflächen. Bei anderen Schaltflächen wird ein Doppelklick als WM_LBUTTONDOWN <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>verarbeitet.</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></td>
<td>Hebt die Schaltfläche hervor, wenn sich die Position des Mauscursors innerhalb des Clientrechtecks der Schaltfläche befindet.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></td>
<td>Gibt die Mausaufnahme frei, wenn die Schaltfläche die Mausaufnahme hatte.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></td>
<td>Führt die gleiche Aktion wie <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>aus, wenn die Schaltfläche über die Mausaufnahme verfügt. Andernfalls wird keine Aktion ausgeführt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></td>
<td>Diese Schaltfläche <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> schaltfläche in <a href="button-styles.md"><strong>eine</strong></a> BS_PUSHBUTTON Schaltfläche.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></td>
<td>Gibt HTTRANSPARENT zurück, wenn das Schaltflächen-Steuerelement ein Gruppenfeld ist.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></td>
<td>Zeichnet die Schaltfläche entsprechend ihrem Stil und dem aktuellen Zustand.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></td>
<td>Zeichnet ein Fokusrechteck auf der Schaltfläche, um den Fokus zu erhalten. Für Optionsfelder und automatische Optionsfelder wird dem übergeordneten Fenster ein <a href="bn-clicked.md">Benachrichtigungscode BN_CLICKED</a> gesendet.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></td>
<td>Legt eine neue Schriftart fest und aktualisiert optional das Fenster.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></td>
<td>Legt den Text der Schaltfläche fest. Im Fall eines Gruppenfelds zeichnet die Meldung den bereits vorhandene Text, bevor das Gruppenfeld mit dem neuen Text neu gestrichen wird.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></td>
<td>Gibt die Mauserfassung für alle Fälle außer der TAB-TASTE frei.</td>
</tr>
</tbody>
</table>



 

Die vordefinierte Fensterprozedur übergibt alle anderen Nachrichten zur Standardverarbeitung an die [**DefWindowProc-Funktion.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern von Nachrichten](control-messages.md)
</dt> </dl>

 

 
