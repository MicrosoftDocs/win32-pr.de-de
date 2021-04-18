---
title: Erwägungen zur Dialogfeldprogrammierung
description: In dieser Übersicht werden einige Überlegungen zur Programmierung von Dialogfeldern erläutert.
ms.assetid: 49024a0f-ea92-4d56-b063-8e5fcdbd884a
keywords:
- Windows-Benutzeroberfläche, Fenster
- Windows-Benutzeroberfläche, Dialogfelder
- Fenster, Dialogfelder
- Dialogfelder, Info
- Dialogfeld Prozeduren
- Dialogfelder, Prozeduren
- WM_INITDIALOG Meldung
- WM_COMMAND Meldung
- WM_PARENTNOTIFY Meldung
- Steuerelement-Farb Meldungen
- Dialogfelder, Nachrichtenverarbeitung
- Dialogfelder, Tastaturschnittstelle
- Dialogfelder, mnetmonics
- Dialogfelder, Benutzer definiert
- benutzerdefinierte Dialogfelder
- Dialogfelder, Einstellungen
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 790abe7c76cdb99f86b2a90a133b15faae721e0e
ms.sourcegitcommit: f7cf41ffc79d1ffead9de2fc61677201f94b423a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2020
ms.locfileid: "106340945"
---
# <a name="dialog-box-programming-considerations"></a>Erwägungen zur Dialogfeldprogrammierung

In dieser Übersicht werden einige Überlegungen zur Programmierung von Dialogfeldern erläutert.

Die Übersicht umfasst die folgenden Themen.

-   [Dialog Feld Prozeduren](#dialog-box-procedures)
    -   [Die "WM \_ InitDialog"-Meldung](wm-initdialog.md)
    -   [Die WM- \_ Befehls Meldung](/windows/desktop/menurc/wm-command)
    -   [Die WM- \_ Nachricht "Parser"](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)
    -   [Steuerelement-Farb Meldungen](#control-color-messages)
    -   [Dialog Feld-Standard Nachrichtenverarbeitung](#dialog-box-default-message-processing)
-   [Tastaturschnittstelle des Dialog Felds](#dialog-box-keyboard-interface)
    -   [Der WS- \_ Tabstopps-Stil](/windows/desktop/winmsg/window-styles)
    -   [Der WS- \_ Gruppen Stil](/windows/desktop/winmsg/window-styles)
    -   [Mnemonik](#mnemonics)
-   [Dialog Feld Einstellungen](#dialog-box-settings)
    -   [Options Felder und Kontrollkästchen](#radio-buttons-and-check-boxes)
    -   [Dialog Feld zum Bearbeiten von Steuerelementen](#dialog-box-edit-controls)
    -   [Listenfelder, Kombinations Felder und Verzeichnislisten](#list-boxes-combo-boxes-and-directory-listings)
    -   [Dialog Feld-Steuerelement Meldungen](#dialog-box-control-messages)
-   [Benutzerdefinierte Dialogfelder](#custom-dialog-boxes)

## <a name="dialog-box-procedures"></a>Dialog Feld Prozeduren

Eine Dialogfeld Prozedur ähnelt einer Fenster Prozedur, in der das System Nachrichten an die Prozedur sendet, wenn Sie Informationen zur Ausführung oder zu auszuführenden Aufgaben enthält. Anders als bei einer Fenster Prozedur ruft eine Dialogfeld Prozedur nie die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion auf. Stattdessen wird " **true** " zurückgegeben, wenn eine Nachricht verarbeitet wird, andernfalls " **false** ".

Jede Dialogfeld Prozedur weist die folgende Form auf:

```cpp
BOOL CALLBACK DlgProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    switch (message) 
    { 
 
        // Place message cases here. 
 
        default: 
            return FALSE; 
    } 
}
```

Die Prozedur Parameter dienen dem gleichen Zweck wie in einer Fenster Prozedur, und der *hwnddlg* -Parameter empfängt das Fenster Handle des Dialog Felds.

In den meisten Dialogfeld Prozeduren werden die " [**WM \_ InitDialog**](wm-initdialog.md) "-Meldung und die von den Steuerelementen gesendeten [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldungen verarbeitet, aber einige andere Nachrichten verarbeiten. Wenn eine Dialogfeld Prozedur eine Nachricht nicht verarbeitet, muss Sie **false** zurückgeben, um das System zur internen Verarbeitung der Nachrichten zu leiten. Die einzige Ausnahme von dieser Regel ist die **WM- \_ InitDialog** -Nachricht. Die Dialogfeld Prozedur muss " **true** " zurückgeben, um das System zur weiteren Verarbeitung der " **WM \_ InitDialog** "-Meldung zu leiten. In jedem Fall muss die Prozedur " [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)" nicht aufzurufen.

- [Die "WM \_ InitDialog"-Meldung](#the-wm_initdialog-message)
- [Die WM- \_ Befehls Meldung](#the-wm_command-message)
- [Die WM- \_ Nachricht "Parser"](#the-wm_parentnotify-message)
- [Steuerelement-Farb Meldungen](#control-color-messages)
- [Dialog Feld-Standard Nachrichtenverarbeitung](#dialog-box-default-message-processing)

### <a name="the-wm_initdialog-message"></a>Die "WM \_ InitDialog"-Meldung

Das System sendet eine [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Meldung nicht an die Dialogfeld Prozedur. Stattdessen wird eine WM- [**\_ InitDialog**](wm-initdialog.md) -Nachricht gesendet, wenn das Dialogfeld und alle zugehörigen Steuerelemente erstellt werden, aber bevor das Dialogfeld angezeigt wird. Die Prozedur muss jede Initialisierung durchführen, die erforderlich ist, um sicherzustellen, dass im Dialogfeld die aktuellen Einstellungen angezeigt werden, die dem Task zugeordnet sind. Wenn ein Dialogfeld z. b. ein Steuerelement enthält, das das aktuelle Laufwerk und Verzeichnis anzeigt, muss die Prozedur das aktuelle Laufwerk und Verzeichnis ermitteln und das Steuerelement auf diesen Wert festlegen.

Die Prozedur kann Steuerelemente mithilfe von Funktionen wie z. b. [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) und [**checkdlgbutton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx)initialisieren. Da es sich bei den Steuerelementen um Fenster handelt, kann die Prozedur Sie auch mithilfe von Fenster Verwaltungsfunktionen wie [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) und [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)manipulieren. Die Prozedur kann das Fenster Handle für ein Steuerelement mithilfe der [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) -Funktion abrufen.

Die Dialogfeld Prozedur kann den Inhalt, den Zustand und die Position eines beliebigen Steuer Elements nach Bedarf ändern. Beispielsweise kann die Prozedur in einem Dialogfeld, das ein Listenfeld von Dateinamen und eine Schaltfläche **Öffnen** enthält, die Schaltfläche **Öffnen** deaktivieren, bis der Benutzer eine Datei aus der Liste auswählt. In diesem Beispiel gibt die Dialogfeld Vorlage den [**\_ deaktivierten WS**](/windows/desktop/winmsg/window-styles) -Stil für die Schaltfläche **Öffnen** an, und das System deaktiviert die Schaltfläche automatisch, wenn Sie erstellt wird. Wenn die Dialogfeld Prozedur eine Benachrichtigungs Meldung aus dem Listenfeld empfängt, die anzeigt, dass der Benutzer eine Datei ausgewählt hat, ruft die Prozedur die [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) -Funktion auf, um die Schaltfläche **Öffnen** zu aktivieren.

Wenn Sie ein benutzerdefiniertes Symbol auf der Titelleiste des Dialog Felds anzeigen möchten, kann der [**WM \_ InitDialog**](wm-initdialog.md) -Handler die [**WM \_**](/windows/desktop/winmsg/wm-seticon) -Nachricht an das Dialogfeld senden.

Wenn die Anwendung das Dialogfeld mithilfe einer der Funktionen [**Dialogbox param**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama), [**dialogboxderetparam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), anitdialogparam oder [**kreatedialogindirectparam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)erstellt, enthält der *LPARAM* -Parameter für die [**WM- \_ InitDialog**](wm-initdialog.md) -Nachricht den zusätzlichen Parameter, der an die Funktion übergeben wird. [](/windows/desktop/api/Winuser/nf-winuser-createdialogparama) Anwendungen verwenden diesen zusätzlichen Parameter in der Regel, um einen Zeiger auf zusätzliche Initialisierungs Informationen an die Dialogfeld Prozedur zu übergeben, aber die Dialogfeld Prozedur muss die Bedeutung des Parameters bestimmen. Wenn die Anwendung eine andere Funktion verwendet, um das Dialogfeld zu erstellen, legt das System den *LPARAM* -Parameter auf **null** fest.

Vor der Rückgabe aus der [**WM- \_ InitDialog**](wm-initdialog.md) -Nachricht sollte die Prozedur bestimmen, ob der Eingabefokus auf ein angegebenes Steuerelement festgelegt werden soll. Wenn die Dialogfeld Prozedur **true** zurückgibt, legt das System den Eingabefokus automatisch auf das Steuerelement fest, dessen Fenster Handle im *wParam* -Parameter ist. Wenn das Steuerelement, das den Standard Fokus erhält, nicht geeignet ist, kann der Fokus mithilfe der [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) -Funktion auf das entsprechende Steuerelement festgelegt werden. Wenn die Prozedur den Eingabefokus festlegt, muss Sie **false** zurückgeben, um zu verhindern, dass vom System der Standard Fokus festgelegt wird. Das Steuerelement, das den Standardeingabe Fokus empfängt, ist immer das erste Steuerelement, das in der Vorlage angegeben ist, die sichtbar und nicht deaktiviert ist und die den [WS \_ tabstoppstil](/windows/desktop/winmsg/window-styles) hat. Wenn kein solches Steuerelement vorhanden ist, legt das System den Standardeingabe Fokus auf das erste Steuerelement in der Vorlage fest.

### <a name="the-wm_command-message"></a>Die WM- \_ Befehls Meldung

Ein-Steuerelement kann eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung an die Dialogfeld Prozedur senden, wenn der Benutzer eine Aktion im-Steuerelement ausführt. Diese Nachrichten, die als Benachrichtigungs Meldungen bezeichnet werden, informieren das Verfahren über Benutzereingaben und ermöglichen es, entsprechende Antworten auszuführen.

Alle vordefinierten Steuerelemente, mit Ausnahme von statischen Steuerelementen, senden Benachrichtigungs Meldungen für ausgewählte Benutzeraktionen. Beispielsweise sendet eine pushschaltfläche die per e-Mail [**\_ angeklickte**](../controls/bn-clicked.md) Benachrichtigungs Meldung, wenn der Benutzer auf die Schaltfläche klickt. In allen Fällen enthält das nieder wertige Wort des *wParam* -Parameters den Steuerelement Bezeichner, das hochwertige Wort von *wParam* enthält den Benachrichtigungs Code, und der *LPARAM* -Parameter enthält das Steuerelement Fenster handle.

Die Dialogfeld Prozedur sollte Benachrichtigungs Meldungen überwachen und verarbeiten. Insbesondere muss die Prozedur Nachrichten verarbeiten, die über die IDOK-oder IDCANCEL-IDs verfügen. Diese Nachrichten stellen eine Anforderung des Benutzers dar, das Dialogfeld zu schließen. Die Prozedur sollte das Dialogfeld mit der Funktion [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) für modale Dialogfelder und der [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) -Funktion für nicht modale Dialogfelder schließen.

Das System sendet auch [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldungen an die Dialogfeld Prozedur, wenn das Dialogfeld über ein Menü verfügt, z. b. das Menü **Fenster** , und der Benutzer auf ein Menü Element klickt. Insbesondere sendet das System eine WM- **\_ Befehls** Nachricht, bei der der *wParam* -Parameter auf **IDCANCEL** festgelegt ist, wenn der Benutzer im Menü Fenster des Dialog Felds auf **Schließen** klickt. Die Nachricht ist nahezu identisch mit der Benachrichtigungs Meldung, die von der Schaltfläche **Abbrechen** gesendet wurde, und sollte auf die gleiche Weise verarbeitet werden.

### <a name="the-wm_parentnotify-message"></a>Die WM- \_ Nachricht "Parser"

Ein Steuerelement sendet immer dann eine [**WM \_**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) -Nachricht, wenn der Benutzer eine Maustaste drückt, während er auf das Steuerelement zeigt. Einige Anwendungen interpretieren diese Nachricht als Signal zum Ausführen einer Aktion, die mit dem Steuerelement verknüpft ist, z. b. zum Anzeigen einer Textzeile, die den Zweck des Steuer Elements beschreibt.

Das System sendet auch beim Erstellen und zerstören eines Fensters [**WM- \_ Parser**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) , jedoch nicht für Steuerelemente, die aus einer Dialogfeld Vorlage erstellt werden. Das System verhindert diese Nachrichten durch Angeben des **WS \_ Ex \_ noparentnotify** -Stils, wenn die Steuerelemente erstellt werden. Eine Anwendung kann dieses Standardverhalten nicht außer Kraft setzen, es sei denn, Sie erstellt eigene Steuerelemente für das Dialogfeld.

### <a name="control-color-messages"></a>Control-Color Meldungen

Steuerelemente und das System können Steuerelement-Farb Meldungen senden, wenn die Dialogfeld Prozedur den Hintergrund eines Steuer Elements oder eines anderen Fensters mit einem bestimmten Pinsel und Farben zeichnen soll. Dies kann hilfreich sein, wenn Anwendungen die Standardfarben überschreiben, die in Dialogfeldern und deren Steuerelementen verwendet werden. Im folgenden finden Sie die Steuerelement-Farb Meldungen, die die **WM \_ CtlColor** -Meldung ersetzt haben.

-   [**WM \_ ctlcolorbtn**](../controls/wm-ctlcolorbtn.md)
-   [**WM \_ ctlcolordlg**](wm-ctlcolordlg.md)
-   [**WM \_ ctlcoloredit**](../controls/wm-ctlcoloredit.md)
-   [**WM \_ ctlcolorlistbox**](../controls/wm-ctlcolorlistbox.md)
-   [**WM \_ ctlcolorscrollbar**](../controls/wm-ctlcolorscrollbar.md)
-   [**WM \_ ctlcolorstatic**](../controls/wm-ctlcolorstatic.md)

Ein-Steuerelement sendet eine Steuerelement Farbe an die Dialogfeld Prozedur, kurz bevor es seinen eigenen Hintergrund zeichnet. Die Meldung ermöglicht dem Verfahren, anzugeben, welcher Pinsel verwendet werden soll, und die Hintergrund-und Vordergrundfarbe festzulegen. Die Prozedur gibt einen Pinsel an, indem das Pinsel Handle zurückgegeben wird. Zum Festlegen der Hintergrund-und Vorder Grundfarben verwendet die Prozedur die Funktionen [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) und [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) mit dem Anzeigegeräte Kontext des Steuer Elements. Die Kontroll Farben Meldung übergibt ein Handle an den Anzeigegeräte Kontext an die Prozedur im *wParam* -Parameter der Nachricht.

Das System sendet eine [**WM \_ ctlcolordlg**](wm-ctlcolordlg.md) -Meldung an die Dialogfeld Prozedur, wenn die Prozedur die [**WM \_ erasebkgnd**](/windows/desktop/winmsg/wm-erasebkgnd) -Nachricht nicht verarbeitet. Die vordefinierte Dialogfeld Klasse verfügt nicht über einen klassenhintergrund Pinsel. Daher kann die Prozedur mit dieser Meldung Ihren eigenen Hintergrund definieren, ohne den Code zum Ausführen der Arbeit einschließen zu müssen.

In jedem Fall verwendet das System einen Pinsel mit der Standardfenster Farbe, um den Hintergrund für alle Steuerelemente und Fenster außer Bild Lauf leisten zu zeichnen, wenn eine Dialogfeld Prozedur keine Kontroll Farb Meldung verarbeitet. Eine Anwendung kann die Standardfenster Farbe abrufen, indem der Wert des **Farb \_ Fensters** an die [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) -Funktion übergeben wird. Während der Hintergrund gezeichnet wird, wird die Vordergrundfarbe für die Anzeige des Geräte Kontexts auf die Standard Textfarbe (**Color \_ WindowText**) festgelegt. Für Bild Lauf leisten verwendet das System einen Pinsel mit der Standardfarbe der Scrollleiste (**Farb \_ Scrollleiste**). In diesem Fall werden die Hintergrund-und Vorder Grundfarben für den Anzeigegeräte Kontext auf White bzw. Black festgelegt.

### <a name="dialog-box-default-message-processing"></a>Dialog Feld-Standard Nachrichtenverarbeitung

Die Fenster Prozedur für die vordefinierte Dialogfeld Klasse führt die Standard Verarbeitung für alle Nachrichten aus, die von der Dialogfeld Prozedur nicht verarbeitet werden. Wenn die Dialogfeld Prozedur für jede Nachricht **false** zurückgibt, prüft die vordefinierte Fenster Prozedur die Nachrichten und führt die folgenden Standard Aktionen aus:



| `Message`                                            | Standardaktion                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DM \_ getdefid**](dm-getdefid.md)                | Sie können diese Meldung an ein Dialogfeld senden. Im Dialogfeld wird der Steuerelement Bezeichner der standardmäßigen Schaltfläche "Push" zurückgegeben, wenn das Dialogfeld einen enthält. Andernfalls wird 0 (null) zurückgegeben.                                                                                                                                                                                                                                                                                                                      |
| [**DM- \_ Neupositionierung**](dm-reposition.md)            | Sie können diese Meldung an ein Dialogfeld der obersten Ebene senden. Das Dialogfeld wird automatisch neu positioniert, sodass es in den Desktop Bereich passt.                                                                                                                                                                                                                                                                                                                                                                       |
| [**DM \_ -setdefid**](dm-setdefid.md)                | Sie können diese Meldung an ein Dialogfeld senden. Im Dialogfeld wird die standardmäßige pushtaste auf das Steuerelement festgelegt, das von der Steuerelement-ID im *wParam* -Parameter angegeben wird.                                                                                                                                                                                                                                                                                                                             |
| [**WM \_ aktivieren**](/windows/desktop/inputdev/wm-activate)           | Stellt den Eingabefokus auf das Steuerelement wieder her, das durch das zuvor gespeicherte Handle identifiziert wird, wenn das Dialogfeld aktiviert ist. Andernfalls speichert die Prozedur das Handle für das Steuerelement, das den Eingabefokus besitzt.                                                                                                                                                                                                                                                                                               |
| [**WM- \_ Diagramm**](../controls/wm-chartoitem.md)         | Gibt 0 (null) zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ Schließen**](/windows/desktop/winmsg/wm-close)                   | Sendet die per e-Mail [**\_ angeklickte**](../controls/bn-clicked.md) Benachrichtigungs Meldung an das Dialogfeld, wobei **IDCANCEL** als Steuerelement Bezeichner angegeben wird. Wenn das Dialogfeld über einen IDCANCEL-Steuerelement Bezeichner verfügt und das Steuerelement zurzeit deaktiviert ist, wird eine Warnung durch die Prozedur ausgegeben, und die Nachricht wird nicht gepostet.                                                                                                                                                                                              |
| [**WM- \_ compareitem**](../controls/wm-compareitem.md)       | Gibt 0 (null) zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM- \_ erasebkgnd**](/windows/desktop/winmsg/wm-erasebkgnd)         | Füllt den Client Bereich des Dialog Felds entweder mithilfe des von der WM- [**\_ ctlcolordlg**](wm-ctlcolordlg.md) -Nachricht zurückgegebenen Pinsels oder mit der Standardfenster Farbe aus.                                                                                                                                                                                                                                                                                                                                 |
| [**WM- \_ getFont**](/windows/desktop/winmsg/wm-getfont)               | Gibt ein Handle für die von der Anwendung definierte Dialogfeld Schriftart zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ InitDialog**](wm-initdialog.md)            | Gibt 0 (null) zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown)     | Sendet eine [**CB- \_ ShowDropDown**](../controls/cb-showdropdown.md) -Meldung an das Kombinations Feld mit dem Eingabefokus und leitet das Steuerelement, um das Dropdown-Listenfeld auszublenden. Die Prozedur ruft [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) auf, um die Standardaktion abzuschließen.                                                                                                                                                                                                                                      |
| [**WM \_ ncdestroy**](/windows/desktop/winmsg/wm-ncdestroy)           | Gibt den im Dialogfeld für Bearbeitungs Steuerelemente zugewiesenen globalen Speicher frei (gilt für Dialogfelder, in denen der " [**DS \_ localedit**](dialog-box-styles.md) "-Stil angegeben ist) und gibt alle Anwendungs definierten Schriftart frei (gilt für Dialogfelder, die den [**DS- \_ setFont**](dialog-box-styles.md) -oder [**DS- \_ shellfont**](dialog-box-styles.md) -Stil angeben). Die Prozedur ruft die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion auf, um die Standardaktion abzuschließen. |
| [**WM- \_ nclbuttondown**](/windows/desktop/inputdev/wm-nclbuttondown) | Sendet eine [**CB- \_ ShowDropDown**](../controls/cb-showdropdown.md) -Meldung an das Kombinations Feld mit dem Eingabefokus und leitet das Steuerelement, um das Dropdown-Listenfeld auszublenden. Die Prozedur ruft [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) auf, um die Standardaktion abzuschließen.                                                                                                                                                                                                                                      |
| [**WM \_ nextdlgctl**](wm-nextdlgctl.md)            | Legt den Eingabefokus auf das nächste oder vorherige Steuerelement im Dialogfeld, auf das Steuerelement fest, das durch das Handle im *wParam* -Parameter identifiziert wird, oder auf das erste Steuerelement im Dialogfeld, das sichtbar und nicht deaktiviert ist und die den [**WS- \_ Tabstopps**](/windows/desktop/winmsg/window-styles) -Stil aufweist. Die Prozedur ignoriert diese Meldung, wenn das aktuelle Fenster mit dem Eingabefokus kein Steuerelement ist.                                                                                                                  |
| [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus)           | Legt den Eingabefokus auf das Steuerelement fest, das von einem zuvor gespeicherten Steuerelement Fenster Handle identifiziert wurde. Wenn kein solcher handle vorhanden ist, legt die Prozedur den Eingabefokus auf das erste Steuerelement in der Dialogfeld Vorlage fest, das sichtbar und nicht deaktiviert ist und die den [**WS- \_ Tabstopps**](/windows/desktop/winmsg/window-styles) -Stil aufweist. Wenn kein solches Steuerelement vorhanden ist, legt die Prozedur den Eingabefokus auf das erste Steuerelement in der Vorlage fest.                                                                                          |
| [**WM- \_ ShowWindow**](/windows/desktop/winmsg/wm-showwindow)         | Speichert ein Handle für das Steuerelement mit dem Eingabefokus, wenn das Dialogfeld ausgeblendet wird, und ruft dann [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) auf, um die Standardaktion abzuschließen.                                                                                                                                                                                                                                                                                                                     |
| [**WM ( \_ syscommand)**](/windows/desktop/menurc/wm-syscommand)         | Speichert ein Handle für das Steuerelement mit dem Eingabefokus, wenn das Dialogfeld minimiert wird, und ruft dann [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) auf, um die Standardaktion abzuschließen.                                                                                                                                                                                                                                                                                                                  |
| [**WM \_ vkeytoitem**](../controls/wm-vkeytoitem.md)         | Gibt 0 (null) zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

Die vordefinierte Fenster Prozedur übergibt alle anderen Nachrichten zur Standard Verarbeitung an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

## <a name="dialog-box-keyboard-interface"></a>Tastaturschnittstelle des Dialog Felds

Das System stellt eine spezielle Tastaturschnittstelle für Dialogfelder bereit, die eine spezielle Verarbeitung für mehrere Schlüssel durchführt. Die-Schnittstelle generiert Nachrichten, die bestimmten Schaltflächen im Dialogfeld entsprechen, oder ändert den Eingabefokus von einem Steuerelement zu einem anderen. Im folgenden werden die Schlüssel verwendet, die in dieser Schnittstelle verwendet werden.


| Schlüssel            | Aktion                                                                                                                                                                    |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALT +*mnetmonisch* | Verschiebt den Eingabefokus auf das erste Steuerelement (mit dem [**WS- \_ Tabstopps**](/windows/desktop/winmsg/window-styles) -Stil) nach dem statischen Steuerelement, das den angegebenen mnetmonischen enthält.        |
| DOWN           | Verschiebt den Eingabefokus auf das nächste Steuerelement in der Gruppe.                                                                                                                   |
| EINGABETASTE          | Sendet eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung an die Dialogfeld Prozedur. Der *wParam* -Parameter ist auf IDOK oder den Steuerelement Bezeichner der standardmäßigen Schaltfläche Push festgelegt. |
| ESC            | Sendet eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung an die Dialogfeld Prozedur. Der *wParam* -Parameter ist auf IDCANCEL festgelegt.                                              |
| LEFT           | Verschiebt den Eingabefokus auf das vorherige Steuerelement in der Gruppe.                                                                                                               |
| *mnemonische*     | Verschiebt den Eingabefokus auf das erste Steuerelement (mit dem [**WS- \_ Tabstopps**](/windows/desktop/winmsg/window-styles) -Stil) nach dem statischen Steuerelement, das den angegebenen mnetmonischen enthält.        |
| RIGHT          | Verschiebt den Eingabefokus auf das nächste Steuerelement in der Gruppe.                                                                                                                   |
| UMSCHALT+TAB      | Verschiebt den Eingabefokus auf das vorherige Steuerelement, das die [**WS \_ Tabstoppart**](/windows/desktop/winmsg/window-styles) aufweist.                                                                |
| TAB            | Verschiebt den Eingabefokus auf das nächste Steuerelement, das die [**WS \_ Tabstoppart**](/windows/desktop/winmsg/window-styles) aufweist.                                                                    |
| UP             | Verschiebt den Eingabefokus auf das vorherige Steuerelement in der Gruppe.                                                                                                               |

Das System stellt automatisch die Tastaturschnittstelle für alle modalen Dialogfelder bereit. Sie stellt nicht die Schnittstelle für Dialogfelder ohne Modus bereit, es sei denn, die Anwendung ruft die [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) -Funktion auf, um Nachrichten in der Hauptnachrichten Schleife zu filtern. Dies bedeutet, dass die Anwendung die Nachricht direkt nach dem Abrufen der Nachricht aus der Nachrichten Warteschlange an **IsDialogMessage** übergeben muss. Die-Funktion verarbeitet die Nachrichten, wenn Sie für das Dialogfeld vorgesehen ist, und gibt einen Wert ungleich 0 (null) zurück, um anzugeben, dass die Nachricht verarbeitet wurde und nicht an die Funktion [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) oder [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) weitergegeben werden darf.

Da die Tastaturschnittstelle des Dialog Felds Richtungs Tasten zum Wechseln zwischen Steuerelementen in einem Dialogfeld verwendet, kann eine Anwendung diese Schlüssel nicht verwenden, um den Inhalt eines modalen Dialog Felds oder eines nicht modalen Dialog Felds auszuscrollen, für das [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) aufgerufen wird. Wenn ein Dialogfeld Scrollleisten enthält, muss die Anwendung eine Alternative Tastaturschnittstelle für die Bild Lauf leisten bereitstellen. Beachten Sie, dass die Maus Oberfläche zum Scrollen verfügbar ist, wenn das System eine Maus enthält.

### <a name="the-ws_tabstop-style"></a>Der WS- \_ Tabstopps-Stil

Der [**WS \_ Tabstopp**](/windows/desktop/winmsg/window-styles) -Stil gibt die Steuerelemente an, die der Benutzer durch Drücken der Tab-Taste oder UMSCHALT + TAB-Taste verschieben kann.

Wenn der Benutzer Tab oder UMSCHALT + TAB drückt, bestimmt das System zunächst, ob diese Schlüssel von dem Steuerelement verarbeitet werden, das derzeit den Eingabefokus besitzt. Das Steuerelement sendet eine [**WM \_ getdlgcode**](wm-getdlgcode.md) -Nachricht, und wenn das Steuerelement dlgc \_ wanttab zurückgibt, übergibt das System die Schlüssel an das Steuerelement. Andernfalls verwendet das System die [**getnextdlgtabitem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) -Funktion, um das nächste Steuerelement zu suchen, das sichtbar und nicht deaktiviert ist und das die [**WS \_ Tabstoppart**](/windows/desktop/winmsg/window-styles) hat. Die Suche beginnt mit dem Steuerelement, das derzeit den Eingabefokus besitzt, und wird in der Reihenfolge fortgesetzt, in der die Steuerelemente erstellt wurden – d. h. die Reihenfolge, in der Sie in der Dialogfeld Vorlage definiert sind. Wenn das System ein Steuerelement mit den erforderlichen Merkmalen lokalisiert, verschiebt das System den Eingabefokus darauf.

Wenn bei der Suche nach dem nächsten Steuerelement mit der [**WS- \_ Tabstopps**](/windows/desktop/winmsg/window-styles) -Formatvorlage ein Fenster mit dem **WS \_ Ex \_ controlparent** -Stil gefunden wird, durchsucht das System die untergeordneten Elemente des Fensters rekursiv.

Eine Anwendung kann auch " [**getnextdlgtabitem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) " verwenden, um Steuerelemente zu finden, die die [**WS \_ Tabstoppart**](/windows/desktop/winmsg/window-styles) aufweisen. Die-Funktion Ruft das Fenster Handle für das nächste oder vorherige Steuerelement ab, das die **WS \_ Tabstoppart** hat, ohne den Eingabefokus zu verschieben.

### <a name="the-ws_group-style"></a>Der WS- \_ Gruppen Stil

Standardmäßig verschiebt das System den Eingabefokus immer dann auf das nächste oder vorherige Steuerelement, wenn der Benutzer eine Richtungs Taste drückt. Solange das aktuelle Steuerelement mit dem Eingabefokus diese Schlüssel nicht verarbeitet und das nächste oder vorherige Steuerelement kein statisches Steuerelement ist, verschiebt das System den Eingabefokus weiterhin über alle Steuerelemente im Dialogfeld, da der Benutzer weiterhin die Richtung Taste drückt.

Eine Anwendung kann das [**WS- \_ Gruppen**](/windows/desktop/winmsg/window-styles) Format verwenden, um dieses Standardverhalten zu ändern. Der Stil markiert den Anfang einer Gruppe von Steuerelementen. Wenn ein Steuerelement in der Gruppe den Eingabefokus besitzt, wenn der Benutzer mit dem Drücken von Richtungs Schlüsseln beginnt, bleibt der Fokus in der Gruppe. Im Allgemeinen muss das erste Steuerelement in einer Gruppe den **WS- \_ Gruppen** Stil aufweisen, und alle anderen Steuerelemente in der Gruppe dürfen nicht über diesen Stil verfügen. Alle Steuerelemente in der Gruppe müssen zusammenhängend sein, d. –., Sie müssen in einer Folge ohne dazwischenliegende Steuerelemente erstellt werden.

Wenn der Benutzer eine Richtungs Taste drückt, bestimmt das System zunächst, ob das aktuelle Steuerelement, das über den Eingabefokus verfügt, die Richtungs Tasten verarbeitet. Das System sendet eine [**WM \_ getdlgcode**](wm-getdlgcode.md) -Meldung an das Steuerelement, und wenn das Steuerelement den **dlgc- \_ wantpfeile** -Wert zurückgibt, übergibt er den Schlüssel an das-Steuerelement. Andernfalls verwendet das System die [**getnextdlggroupitem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) -Funktion, um das nächste Steuerelement in der Gruppe zu bestimmen.

[**Getnextdlggroupitem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) sucht Steuerelemente in der Reihenfolge (oder in umgekehrter Reihenfolge), in der Sie erstellt wurden. Wenn der Benutzer die nach-rechts-oder nach-unten-Taste drückt, gibt **getnextdlggroupitem** das nächste Steuerelement zurück, wenn dieses Steuerelement nicht über den [**WS- \_ Gruppen**](/windows/desktop/winmsg/window-styles) Stil verfügt. Andernfalls kehrt die Funktion die Reihenfolge der Suche um und gibt das erste Steuerelement zurück, das den **WS- \_ Gruppen** Stil hat. Wenn der Benutzer die nach-links-oder nach-oben-Taste drückt, gibt die Funktion das vorherige Steuerelement zurück, es sei denn **, das aktuelle \_** Steuerelement hat bereits das Wenn das aktuelle Steuerelement diesen Stil hat, kehrt die Funktion die Reihenfolge der Suche um, sucht das erste Steuerelement mit dem **WS- \_ Gruppen** Stil und gibt das Steuerelement zurück, das unmittelbar vor dem gefundenen Steuerelement liegt.

Wenn bei der Suche nach dem nächsten Steuerelement in der Gruppe ein Fenster mit dem **WS \_ Ex \_ controlparent** -Stil gefunden wird, durchsucht das System die untergeordneten Elemente des Fensters rekursiv.

Nachdem das System über das nächste oder vorherige Steuerelement verfügt, sendet es eine [**WM \_ getdlgcode**](wm-getdlgcode.md) -Meldung an das Steuerelement, um den Steuer ungstyp zu bestimmen. Anschließend verschiebt das System den Eingabefokus, um zu steuern, ob es sich nicht um ein statisches Steuerelement handelt. Wenn das Steuerelement ein automatisches Optionsfeld ist, sendet das System eine [**BM- \_ Click**](../controls/bm-click.md) -Nachricht an das Steuerelement. Eine Anwendung kann auch [**getnextdlggroupitem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) verwenden, um Steuerelemente in einer Gruppe zu suchen.

Im allgemeinen kombiniert das erste Steuerelement in der Gruppe die [**WS- \_ Gruppen**](/windows/desktop/winmsg/window-styles) -und [**WS \_ Tabstopp**](/windows/desktop/winmsg/window-styles) -Stile, sodass der Benutzer mithilfe der Tab-Taste von der Gruppe zur Gruppe wechseln kann. Wenn die Gruppe Options Felder enthält, sollte die Anwendung die **WS \_ Tabstoppart** nur auf das erste Steuerelement in der Gruppe anwenden. Das System verschiebt den Stil automatisch, wenn der Benutzer zwischen den Steuerelementen in der Gruppe bewegt wird. Dadurch wird sichergestellt, dass der Eingabefokus immer auf dem zuletzt ausgewählten Steuerelement liegt, wenn der Benutzer mithilfe der Tab-Taste zur Gruppe wechselt.

### <a name="mnemonics"></a>Mnemonik

Ein mnetmonisches ist ein ausgewählter Buchstabe oder eine Ziffer in der Bezeichnung einer Schaltfläche oder im Text eines statischen Steuer Elements. Das System verschiebt den Eingabefokus immer dann auf das Steuerelement, das mit dem mnetmonischen verknüpft ist, wenn der Benutzer entweder den Schlüssel drückt, der der mnetmonischen entspricht, oder diese Taste und die Alt-Taste in Kombination drückt. Mnetmonics bieten dem Benutzer eine schnelle Möglichkeit, mit der Tastatur zu einem angegebenen Steuerelement zu wechseln.

Eine Anwendung erstellt ein mmamonisches Element für ein Steuerelement, indem das kaufmännische und-Zeichen (&) direkt vor dem ausgewählten Buchstaben oder der Ziffer in der Bezeichnung oder im Text für das Steuerelement eingefügt werden. In den meisten Fällen enthält die mit dem Steuerelement in der Dialogfeld Vorlage bereitgestellte NULL-abschließende Zeichenfolge das kaufmännische und-Zeichen. Allerdings kann eine Anwendung jederzeit einen mnetmonischen erstellen, indem Sie die vorhandene Bezeichnung oder den Text eines Steuer Elements durch die Funktion [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) ersetzt. Für jedes Steuerelement kann nur ein mnetmonisches angegeben werden. Obwohl es empfohlen wird, muss mnetmonics in einem Dialogfeld nicht eindeutig sein.

Wenn der Benutzer einen Buchstaben oder Ziffern Schlüssel drückt, bestimmt das System zunächst, ob das aktuelle Steuerelement, das über den Eingabefokus verfügt, den Schlüssel verarbeitet. Das System sendet eine [**WM- \_ getdlgcode**](wm-getdlgcode.md) -Meldung an das Steuerelement, und wenn das Steuerelement den **dlgc- \_ wantallkeys** -oder den **DLG \_ wantmessage** -Wert zurückgibt, übergibt das System den Schlüssel an das Steuerelement. Andernfalls sucht Sie nach einem Steuerelement, dessen mnetmonic dem angegebenen Buchstaben oder der angegebenen Ziffer entspricht. Die Suche wird fortgesetzt, bis ein Steuerelement gesucht wird oder alle Steuerelemente untersucht wurden. Während der Suche werden alle statischen Steuerelemente, die den [**SS \_ NoPrefix**](../controls/static-control-styles.md) -Stil aufweisen, ausgelassen.

Wenn bei der Suche nach einem Steuerelement mit einem übereinstimmenden mnetmonischen ein Fenster mit dem **WS- \_ Ex- \_ controlparent** -Stil gefunden wird, durchsucht das System die untergeordneten Elemente des Fensters rekursiv

Wenn das System ein statisches-Steuerelement sucht und das-Steuerelement nicht deaktiviert ist, verschiebt das System den Eingabefokus auf das erste Steuerelement, nachdem das statische Steuerelement sichtbar, nicht deaktiviert und das [**WS- \_ Tabstopps**](/windows/desktop/winmsg/window-styles) -Format aufweist. Wenn das System ein anderes Steuerelement mit einem übereinstimmenden mnetmonischen-Element eingibt, wird der Eingabefokus in dieses Steuerelement verschoben. Wenn es sich bei dem Steuerelement um eine Standard-pushtaste handelt, sendet das System eine mit einem e-Mail [**\_ angeklickte**](../controls/bn-clicked.md) Benachrichtigung an die Dialogfeld Prozedur. Wenn das Steuerelement eine andere Art von Schaltfläche ist und kein anderes Steuerelement im Dialogfeld mit demselben mnetmonischen vorhanden ist, sendet das System die [**BM- \_ Click**](../controls/bm-click.md) -Nachricht an das Steuerelement.

## <a name="dialog-box-settings"></a>Dialog Feld Einstellungen

Bei den Dialogfeld Einstellungen handelt es sich um die aktuelle Auswahl und die Werte für die Steuerelemente im Dialogfeld. Die Dialogfeld Prozedur ist für die Initialisierung der Steuerelemente mit diesen Einstellungen beim Erstellen des Dialog Felds verantwortlich. Außerdem ist es für das Abrufen der aktuellen Einstellungen aus den Steuerelementen zuständig, bevor das Dialogfeld zerstört wird. Welche Methoden zum Initialisieren und Abrufen von Einstellungen verwendet werden, hängt vom Typ des Steuer Elements ab.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Options Felder und Kontrollkästchen](#radio-buttons-and-check-boxes)
-   [Dialog Feld zum Bearbeiten von Steuerelementen](#dialog-box-edit-controls)
-   [Listenfelder, Kombinations Felder und Verzeichnislisten](#list-boxes-combo-boxes-and-directory-listings)
-   [Dialog Feld-Steuerelement Meldungen](#dialog-box-control-messages)

### <a name="radio-buttons-and-check-boxes"></a>Options Felder und Kontrollkästchen

In Dialog Feldern können Sie mithilfe von Options Feldern und Kontrollkästchen den Benutzer aus einer Liste von Optionen auswählen. Mithilfe von Options Feldern können Benutzer aus sich gegenseitig ausschließende Optionen auswählen. mit Kontrollkästchen können Benutzer eine Kombination von Optionen auswählen.

Mit der-Dialogfeld Prozedur kann der anfängliche Zustand eines Kontrollkästchens mithilfe der [**checkdlgbutton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx) -Funktion festgelegt werden, mit der das Kontrollkästchen festgelegt oder deaktiviert wird. Für options Felder in einer Gruppe von sich gegenseitig ausschließenden Options Feldern kann die Dialogfeld Prozedur die [**checkradiobutton**](https://msdn.microsoft.com/library/Cc410654(v=MSDN.10).aspx) -Funktion verwenden, um das entsprechende Optionsfeld festzulegen und alle anderen Options Felder automatisch zu löschen.

Bevor ein Dialogfeld beendet wird, kann die Dialogfeld Prozedur den Status der einzelnen Options Felder und Kontrollkästchen mithilfe der [**isdlgbuttoncheckfunktion**](https://msdn.microsoft.com/library/Cc364806(v=MSDN.10).aspx) überprüfen, die den aktuellen Zustand der Schaltfläche zurückgibt. In einem Dialogfeld werden diese Informationen normalerweise gespeichert, um die Schaltflächen beim nächsten Erstellen des Dialog Felds zu initialisieren.

### <a name="dialog-box-edit-controls"></a>Dialog Feld zum Bearbeiten von Steuerelementen

In vielen Dialogfeldern sind Bearbeitungs Steuerelemente enthalten, mit denen der Benutzer Text als Eingabe angeben können. Die meisten Dialogfeld Prozeduren initialisieren beim ersten Starten des Dialog Felds ein Bearbeitungs Steuerelement. Beispielsweise kann die Dialogfeld Prozedur einen vorgeschlagenen Dateinamen im Steuerelement platzieren, den der Benutzer dann auswählen, ändern oder ersetzen kann. Die Dialogfeld Prozedur kann den Text in einem Bearbeitungs Steuerelement mithilfe der [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) -Funktion festlegen, die Text aus einem angegebenen Puffer in das Bearbeitungs Steuerelement kopiert. Wenn das Bearbeitungs Steuerelement den Eingabefokus erhält, wählt es automatisch den vollständigen Text zum Bearbeiten aus.

Da Bearbeitungs Steuerelemente Ihren Text nicht automatisch an das Dialogfeld zurückgeben, muss die Dialogfeld Prozedur den Text vor dem Beenden abrufen. Der Text kann mithilfe der [**getdlgitemtext**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) -Funktion abgerufen werden, die den Bearbeitungs Steuerelement Text in einen Puffer kopiert. Die Dialogfeld Prozedur speichert diesen Text in der Regel, um das Bearbeitungs Steuerelement zu einem späteren Zeitpunkt zu initialisieren, oder übergibt es zur Verarbeitung an das übergeordnete Fenster.

In einigen Dialogfeldern werden Bearbeitungs Steuerelemente verwendet, mit denen der Benutzer Zahlen eingeben können. Die Dialogfeld Prozedur kann eine Zahl aus einem Bearbeitungs Steuerelement mithilfe der [**getdlgitemint**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) -Funktion abrufen, die den Text aus dem Bearbeitungs Steuerelement abruft und den Text in einen Dezimalwert konvertiert. Der Benutzer gibt die Zahl in Dezimalstellen ein. Sie kann entweder signiert oder unsigniert sein. In der Dialogfeld Prozedur kann eine ganze Zahl mithilfe der Funktion [**setdlgitemint**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemint) angezeigt werden. **Setdlgitemint** konvertiert eine Ganzzahl mit oder ohne Vorzeichen in eine Zeichenfolge von Dezimalziffern.

### <a name="list-boxes-combo-boxes-and-directory-listings"></a>Listenfelder, Kombinations Felder und Verzeichnislisten

In einigen Dialogfeldern werden Listen von Namen angezeigt, aus denen der Benutzer einen oder mehrere Namen auswählen kann. Zum Anzeigen einer Liste von Dateinamen werden z. b. in einem Dialogfeld in der Regel ein Listenfeld und die [**dlgdirlist**](https://msdn.microsoft.com/library/Cc410788(v=MSDN.10).aspx) -und [**DlgDirSelectEx**](https://msdn.microsoft.com/library/Cc410769(v=MSDN.10).aspx) -Funktionen verwendet. Die **dlgdirlist** -Funktion füllt automatisch ein Listenfeld mit den Dateinamen im aktuellen Verzeichnis aus. Die **dlgdirselect** -Funktion Ruft den ausgewählten Dateinamen aus dem Listenfeld ab. Zusammen bieten diese beiden Funktionen eine bequeme Möglichkeit für ein Dialogfeld, eine Verzeichnis Auflistung anzuzeigen, damit der Benutzer eine Datei auswählen kann, ohne seinen Namen und Speicherort eingeben zu müssen.

Ein Dialogfeld kann auch ein Kombinations Feld verwenden, um eine Liste von Dateinamen anzuzeigen. Die [**dlgdirlistcombobox**](https://msdn.microsoft.com/library/Cc410798(v=MSDN.10).aspx) -Funktion füllt automatisch einen Listenfeld Bereich des Kombinations Felds mit den Dateinamen im aktuellen Verzeichnis aus. Die [**dlgdirselectcomboboxex**](https://msdn.microsoft.com/library/Cc410768(v=MSDN.10).aspx) -Funktion Ruft einen ausgewählten Dateinamen aus dem Listenfeld Teil ab.

### <a name="dialog-box-control-messages"></a>Dialog Feld-Steuerelement Meldungen

Viele Steuerelemente erkennen vordefinierte Meldungen, die beim Empfang durch Steuerelemente bewirken, dass Sie eine Aktion ausführen. Beispielsweise legt die [**BM- \_ setcheck**](../controls/bm-setcheck.md) -Nachricht das Kontrollkästchen Check in a fest, und die [**\_ GetSEL**](../controls/em-getsel.md) -Nachricht des Steuer Elements Ruft den Teil des aktuell ausgewählten Text des Steuer Elements ab. Die Steuer Meldungen weisen einem Dialogfeld eine größere und flexiblere Zugriffs Steuerung als die Standardfunktionen zu, sodass Sie häufig verwendet werden, wenn das Dialogfeld komplexe Interaktionen mit dem Benutzer erfordert.

Eine Dialogfeld Prozedur kann eine Nachricht an ein Steuerelement senden, indem Sie den Steuerelement Bezeichner bereitstellt und die [**SendDlgItemMess**](/windows/desktop/api/Winuser/nf-winuser-senddlgitemmessagea) -Funktion verwendet, die mit der [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion identisch ist, mit der Ausnahme, dass ein Steuerelement Bezeichner anstelle eines Fenster Handles verwendet wird, um das Steuerelement zu identifizieren, das die Nachricht empfangen soll. Eine angegebene Meldung erfordert möglicherweise, dass die Dialog Prozedur Parameter mit der Nachricht sendet, und die Nachricht kann entsprechende Rückgabewerte aufweisen. Der Vorgang und die Anforderungen der einzelnen Steuerungs Meldungen richten sich nach dem Zweck der Nachricht und dem Steuerelement, von dem die Nachricht verarbeitet wird.

Weitere Informationen zu den Steuerelement Meldungen finden Sie unter Windows-Steuer [Elemente](../controls/window-controls.md).

## <a name="custom-dialog-boxes"></a>Benutzerdefinierte Dialogfelder

Eine Anwendung kann benutzerdefinierte Dialogfelder erstellen, indem Sie eine von der Anwendung definierte Fenster Klasse für die Dialogfelder verwendet, anstatt die vordefinierte Dialogfeld Klasse zu verwenden. Anwendungen verwenden diese Methode in der Regel, wenn ein Dialogfeld das Hauptfenster ist, aber es ist auch nützlich, wenn Sie modale und nicht modale Dialogfelder für Anwendungen erstellen, die überlappende Standardfenster verfügen.

Die von der Anwendung definierte Fenster Klasse ermöglicht es der Anwendung, eine Fenster Prozedur für das Dialogfeld zu definieren und Nachrichten zu verarbeiten, bevor Sie an die Dialogfeld Prozedur gesendet werden. Außerdem ermöglicht es der Anwendung, ein Klassen Symbol, einen klassenhintergrund Pinsel und ein Klassen Menü für das Dialogfeld zu definieren. Die Anwendung muss die Fenster Klasse registrieren, bevor versucht wird, ein Dialogfeld zu erstellen, und die Dialogfeld Vorlage mit dem Atom-Wert oder dem Namen der Fenster Klasse bereitstellen.

Viele Anwendungen erstellen eine neue Dialogfeld Klasse, indem zuerst die Klassen Informationen für die vordefinierte Dialogfeld Klasse abgerufen und an die [**GetClassInfo**](/windows/desktop/api/winuser/nf-winuser-getclassinfoa) -Funktion übergeben wird, die eine [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur mit den Informationen füllt. Die Anwendung ändert einzelne Member der Struktur, z. b. den Klassennamen, den Pinsel und das Symbol, und registriert dann die neue Klasse mithilfe der [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) -Funktion. Wenn eine Anwendung die **WNDCLASS** -Struktur allein füllt, muss Sie das **CbWndExtra** -Member auf **dlgwindowextra** festlegen. Dies ist die Anzahl zusätzlicher bytes, die das System für jedes Dialogfeld benötigt. Wenn eine Anwendung auch zusätzliche Bytes für jedes Dialogfeld verwendet, müssen Sie über die für das System benötigten zusätzlichen Bytes hinausgehen.

Die Fenster Prozedur für das benutzerdefinierte Dialogfeld verfügt über dieselben Parameter und Anforderungen wie jede andere Fenster Prozedur. Anders als bei anderen Fenster Prozeduren sollte die Fenster Prozedur für dieses Dialogfeld jedoch die [**defdlgproc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) -Funktion anstelle der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion für alle Nachrichten, die nicht verarbeitet werden, aufruft. **Defdlgproc** führt dieselbe Standard Nachrichtenverarbeitung durch wie die Fenster Prozedur für das vordefinierte Dialogfeld, das den Aufruf der Dialogfeld Prozedur einschließt.

Eine Anwendung kann auch benutzerdefinierte Dialogfelder erstellen, indem Sie die Fenster Prozedur des vordefinierten Dialog Felds Unterklassen. Mit der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion kann eine Anwendung die Fenster Prozedur für ein angegebenes Fenster angeben. Die Anwendung kann auch versuchen, mithilfe der [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) -Funktion eine Unterklasse zu verwenden. Dies wirkt sich jedoch auf alle Dialogfelder im System aus, nicht nur auf die, die der Anwendung angehören.

Anwendungen, die benutzerdefinierte Dialogfelder erstellen, stellen manchmal eine Alternative Tastaturschnittstelle für die Dialogfelder bereit. Bei nicht modalem Dialogfeldern kann dies bedeuten, dass die Anwendung die [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) -Funktion nicht aufruft und stattdessen alle Tastatureingaben in der benutzerdefinierten Fenster Prozedur verarbeitet. In solchen Fällen kann die Anwendung die WM- [**\_ nextdlgctl**](wm-nextdlgctl.md) -Nachricht verwenden, um den Code zu minimieren, der erforderlich ist, um den Eingabefokus von einem Steuerelement zu einem anderen zu verschieben. Diese Meldung verschiebt den Eingabefokus bei der Übergabe an [**defdlgproc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)in ein angegebenes Steuerelement und aktualisiert die Darstellung der Steuerelemente, z. b. das Verschieben des Standardrahmens für die pushschaltfläche oder das Festlegen eines automatischen Options Felds.
