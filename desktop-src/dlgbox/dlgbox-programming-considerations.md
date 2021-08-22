---
title: Erwägungen zur Dialogfeldprogrammierung
description: In dieser Übersicht werden einige Überlegungen zur Programmierung in Bezug auf Dialogfelder erläutert.
ms.assetid: 49024a0f-ea92-4d56-b063-8e5fcdbd884a
keywords:
- Windows Benutzeroberfläche,Windowing
- Windows Benutzeroberfläche,Dialogfelder
- Windowing, Dialogfelder
- Dialogfelder, Informationen
- Dialogfeldprozesen
- Dialogfelder, Prozeduren
- WM_INITDIALOG Meldung
- WM_COMMAND Meldung
- WM_PARENTNOTIFY Meldung
- Meldungen zu Steuerelementfarben
- Dialogfelder, Nachrichtenverarbeitung
- Dialogfelder, Tastaturschnittstelle
- Dialogfelder,mnemonics
- Dialogfelder, benutzerdefiniert
- Benutzerdefinierte Dialogfelder
- Dialogfelder, Einstellungen
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 956f700841b0a3d76b7e071f0232382507394879a0253bc4cbcea533fdbb23bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456250"
---
# <a name="dialog-box-programming-considerations"></a>Erwägungen zur Dialogfeldprogrammierung

In dieser Übersicht werden einige Überlegungen zur Programmierung in Bezug auf Dialogfelder erläutert.

Die Übersicht enthält die folgenden Themen.

-   [Dialogfeldprozessen](#dialog-box-procedures)
    -   [\_WM-INITDIALOG-Nachricht](wm-initdialog.md)
    -   [DIE \_ WM-BEFEHLSMELDUNG](/windows/desktop/menurc/wm-command)
    -   [DIE WM \_ PARENTNOTIFY-Nachricht](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)
    -   [Meldungen zu Steuerelementfarben](#control-color-messages)
    -   [Standardnachrichtenverarbeitung im Dialogfeld](#dialog-box-default-message-processing)
-   [Tastaturschnittstelle des Dialogfelds](#dialog-box-keyboard-interface)
    -   [Der \_ WS-TABSTOP-Stil](/windows/desktop/winmsg/window-styles)
    -   [Der WS \_ GROUP-Stil](/windows/desktop/winmsg/window-styles)
    -   [Mnemotechnik](#mnemonics)
-   [Dialogfeld Einstellungen](#dialog-box-settings)
    -   [Optionsfelder und Kontrollkästchen](#radio-buttons-and-check-boxes)
    -   [Steuerelemente zum Bearbeiten des Dialogfelds](#dialog-box-edit-controls)
    -   [Listenfelder, Kombinationsfelder und Verzeichnisauflistungen](#list-boxes-combo-boxes-and-directory-listings)
    -   [Dialogfeld-Steuerelementmeldungen](#dialog-box-control-messages)
-   [Benutzerdefinierte Dialogfelder](#custom-dialog-boxes)

## <a name="dialog-box-procedures"></a>Dialogfeldprozessen

Eine Dialogfeldprozedur ähnelt einer Fensterprozedur darin, dass das System Nachrichten an die Prozedur sendet, wenn sie Informationen zum Erteilen oder Ausführen von Aufgaben enthält. Im Gegensatz zu einer Fensterprozedur ruft eine Dialogfeldprozedur nie die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) auf. Stattdessen wird **TRUE** zurückgegeben, wenn eine Nachricht verarbeitet wird, oder **FALSE,** wenn dies nicht der Fall ist.

Jede Dialogfeldprozedur weist das folgende Format auf:

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

Die Prozedurparameter erfüllen den gleichen Zweck wie in einer Fensterprozedur, wobei der *Parameter hwndDlg* das Fensterhandle des Dialogfelds empfängt.

Die meisten Dialogfeldprozessen verarbeiten die [**WM \_ INITDIALOG-Nachricht**](wm-initdialog.md) und die [**WM \_ COMMAND-Meldungen,**](/windows/desktop/menurc/wm-command) die von den Steuerelementen gesendet werden, verarbeiten jedoch nur wenige, wenn auch nur andere Nachrichten. Wenn eine Dialogfeldprozedur keine Nachricht verarbeitet, muss sie **FALSE** zurückgeben, um das System anzuweisen, die Nachrichten intern zu verarbeiten. Die einzige Ausnahme von dieser Regel ist die **WM \_ INITDIALOG-Nachricht.** Die Dialogfeldprozedur muss **TRUE** zurückgeben, um das System anzuweisen, die **WM \_ INITDIALOG-Nachricht** weiter zu verarbeiten. In jedem Fall darf die Prozedur [**defWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)nicht aufrufen.

- [\_WM-INITDIALOG-Nachricht](#the-wm_initdialog-message)
- [DIE \_ WM-BEFEHLSMELDUNG](#the-wm_command-message)
- [DIE WM \_ PARENTNOTIFY-Nachricht](#the-wm_parentnotify-message)
- [Meldungen zu Steuerelementfarben](#control-color-messages)
- [Standardnachrichtenverarbeitung im Dialogfeld](#dialog-box-default-message-processing)

### <a name="the-wm_initdialog-message"></a>\_WM-INITDIALOG-Nachricht

Das System sendet keine [**WM \_ CREATE-Nachricht**](/windows/desktop/winmsg/wm-create) an die Dialogfeldprozedur. Stattdessen wird eine [**\_ WM-INITDIALOG-Nachricht**](wm-initdialog.md) gesendet, wenn das Dialogfeld und alle zugehörigen Steuerelemente erstellt werden, aber bevor das Dialogfeld angezeigt wird. Die Prozedur sollte alle erforderlichen Initialisierungen ausführen, um sicherzustellen, dass im Dialogfeld die aktuellen Einstellungen angezeigt werden, die dem Task zugeordnet sind. Wenn z. B. ein Dialogfeld ein Steuerelement zum Anzeigen des aktuellen Laufwerks und Verzeichnisses enthält, muss die Prozedur das aktuelle Laufwerk und verzeichnis bestimmen und das Steuerelement auf diesen Wert festlegen.

Die Prozedur kann Steuerelemente mithilfe von Funktionen wie [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) und [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx)initialisieren. Da Steuerelemente Fenster sind, kann die Prozedur sie auch mithilfe von Fensterverwaltungsfunktionen wie [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) und [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)bearbeiten. Die Prozedur kann das Fensterhandle mithilfe der [**GetDlgItem-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) an ein Steuerelement abrufen.

Die Dialogfeldprozedur kann den Inhalt, den Zustand und die Position eines beliebigen Steuerelements nach Bedarf ändern. Beispielsweise kann die Prozedur in einem Dialogfeld, das ein Listenfeld mit Dateinamen und eine Schaltfläche **Öffnen** enthält, die Schaltfläche **Öffnen** deaktivieren, bis der Benutzer eine Datei aus der Liste auswählt. In diesem Beispiel gibt die Dialogfeldvorlage den [**WS \_ DISABLED-Stil**](/windows/desktop/winmsg/window-styles) für die Schaltfläche **Öffnen** an, und das System deaktiviert die Schaltfläche beim Erstellen automatisch. Wenn die Dialogfeldprozedur eine Benachrichtigung aus dem Listenfeld empfängt, die angibt, dass der Benutzer eine Datei ausgewählt hat, ruft die Prozedur die [**EnableWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-enablewindow) auf, um die Schaltfläche **Öffnen** zu aktivieren.

Um ein benutzerdefiniertes Symbol auf der Beschriftungsleiste des Dialogfelds anzuzeigen, kann Ihr [**WM \_ INITDIALOG-Handler**](wm-initdialog.md) die [**WM \_ SETICON-Nachricht**](/windows/desktop/winmsg/wm-seticon) an das Dialogfeld senden.

Wenn die Anwendung das Dialogfeld mithilfe einer der Funktionen [**DialogBoxParam,**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) [**DialogBoxIndirectParam,**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)oder [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)erstellt, enthält der *lParam-Parameter* für die [**WM \_ INITDIALOG-Nachricht**](wm-initdialog.md) den zusätzlichen Parameter, der an die Funktion übergeben wird. Anwendungen verwenden diesen zusätzlichen Parameter in der Regel, um einen Zeiger auf zusätzliche Initialisierungsinformationen an die Dialogfeldprozedur zu übergeben, aber die Dialogfeldprozedur muss die Bedeutung des Parameters bestimmen. Wenn die Anwendung eine andere Funktion zum Erstellen des Dialogfelds verwendet, legt das System den *lParam-Parameter* auf **NULL** fest.

Vor der Rückgabe aus der [**WM \_ INITDIALOG-Nachricht**](wm-initdialog.md) sollte die Prozedur bestimmen, ob der Eingabefokus auf ein angegebenes Steuerelement festgelegt werden soll. Wenn die Dialogfeldprozedur **TRUE** zurückgibt, legt das System den Eingabefokus automatisch auf das Steuerelement fest, dessen Fensterhandle sich im *wParam-Parameter* befindet. Wenn das Steuerelement, das den Standardfokus erhält, nicht geeignet ist, kann es den Fokus mithilfe der [**SetFocus-Funktion**](/windows/desktop/api/winuser/nf-winuser-setfocus) auf das entsprechende Steuerelement festlegen. Wenn die Prozedur den Eingabefokus festlegt, muss sie **FALSE** zurückgeben, um zu verhindern, dass das System den Standardfokus festlegt. Das Steuerelement, das den Standardeingabefokus empfängt, ist immer das erste in der Vorlage angegebene Steuerelement, das sichtbar und nicht deaktiviert ist und über den [WS \_ TABSTOP-Stil](/windows/desktop/winmsg/window-styles) verfügt. Wenn kein solches Steuerelement vorhanden ist, legt das System den Standardeingabefokus auf das erste Steuerelement in der Vorlage fest.

### <a name="the-wm_command-message"></a>DIE \_ WM-BEFEHLSMELDUNG

Ein Steuerelement kann eine [**WM \_ COMMAND-Nachricht**](/windows/desktop/menurc/wm-command) an die Dialogfeldprozedur senden, wenn der Benutzer eine Aktion im Steuerelement ausführt. Diese Nachrichten, als Benachrichtigungsmeldungen bezeichnet, informieren das Verfahren über Benutzereingaben und ermöglichen es ihm, entsprechende Antworten auszuführen.

Alle vordefinierten Steuerelemente, außer statische Steuerelemente, senden Benachrichtigungsmeldungen für ausgewählte Benutzeraktionen. Beispielsweise sendet eine Pushschaltfläche die [**BN CLICKED-Benachrichtigungsmeldung, \_**](../controls/bn-clicked.md) wenn der Benutzer auf die Schaltfläche klickt. In allen Fällen enthält das Wort mit niedriger Reihenfolge des *wParam-Parameters* den Steuerelementbezeichner, das Wort in hoher Reihenfolge von *wParam* den Benachrichtigungscode und der *lParam-Parameter* das Steuerelementfensterhandle.

Die Dialogfeldprozedur sollte Benachrichtigungsmeldungen überwachen und verarbeiten. Insbesondere muss die Prozedur Nachrichten verarbeiten, die die IDOK- oder IDCANCEL-Bezeichner aufweisen. Diese Meldungen stellen eine Anforderung des Benutzers dar, das Dialogfeld zu schließen. Die Prozedur sollte das Dialogfeld mithilfe der [**EndDialog-Funktion**](/windows/desktop/api/Winuser/nf-winuser-enddialog) für modale Dialogfelder und der [**DestroyWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-destroywindow) für moduslose Dialogfelder schließen.

Das System sendet wm [**\_ command-Meldungen**](/windows/desktop/menurc/wm-command) auch an die Dialogfeldprozedur, wenn das Dialogfeld über ein Menü wie das **Fenstermenü** verfügt und der Benutzer auf ein Menüelement klickt. Insbesondere sendet das System eine **WM \_ COMMAND-Nachricht,** bei der der *wParam-Parameter* auf **IDCANCEL** festgelegt ist, wenn der Benutzer im Fenstermenü des Dialogfelds auf **Schließen** klickt. Die Nachricht ist nahezu identisch mit der Benachrichtigungsnachricht, die von der Schaltfläche **Abbrechen** gesendet wird, und sollte auf die gleiche Weise verarbeitet werden.

### <a name="the-wm_parentnotify-message"></a>DIE WM \_ PARENTNOTIFY-Nachricht

Ein Steuerelement sendet immer dann eine [**WM \_ PARENTNOTIFY-Nachricht,**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) wenn der Benutzer eine Maustaste drückt, während er auf das Steuerelement verweist. Einige Anwendungen interpretieren diese Nachricht als Signal, um eine Aktion im Zusammenhang mit dem Steuerelement auszuführen, z. B. das Anzeigen einer Textzeile, die den Zweck des Steuerelements beschreibt.

Das System sendet auch [**WM \_ PARENTNOTIFY-Meldungen,**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) wenn es ein Fenster erstellt und zerstört, jedoch nicht für Steuerelemente, die aus einer Dialogfeldvorlage erstellt wurden. Das System verhindert diese Meldungen, indem das **WS \_ EX \_ NOPARENTNOTIFY-Format** beim Erstellen der Steuerelemente angegeben wird. Eine Anwendung kann dieses Standardverhalten nur überschreiben, wenn sie eigene Steuerelemente für das Dialogfeld erstellt.

### <a name="control-color-messages"></a>Control-Color-Meldungen

Steuerelemente und das System können Meldungen zu Steuerelementfarben senden, wenn die Dialogfeldprozedur den Hintergrund eines Steuerelements oder eines anderen Fensters mit einem bestimmten Pinsel und farben zeichnen soll. Dies kann nützlich sein, wenn Anwendungen die standardfarben überschreiben, die in Dialogfeldern und ihren Steuerelementen verwendet werden. Im Folgenden sind die Meldungen zur Steuerelementfarbe angegeben, die die **WM \_ CTLCOLOR-Nachricht** ersetzt haben.

-   [**WM \_ CTLCOLORBTN**](../controls/wm-ctlcolorbtn.md)
-   [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md)
-   [**WM \_ CTLCOLOREDIT**](../controls/wm-ctlcoloredit.md)
-   [**WM \_ CTLCOLORLISTBOX**](../controls/wm-ctlcolorlistbox.md)
-   [**WM \_ CTLCOLORSCROLLBAR**](../controls/wm-ctlcolorscrollbar.md)
-   [**WM \_ CTLCOLORSTATIC**](../controls/wm-ctlcolorstatic.md)

Ein Steuerelement sendet eine Farbmeldung an die Dialogfeldprozedur, bevor es seinen eigenen Hintergrund zeichnet. Die Meldung ermöglicht es der Prozedur, anzugeben, welcher Pinsel verwendet werden soll, und die Hintergrund- und Vordergrundfarben festzulegen. Die Prozedur gibt einen Pinsel durch Rückgabe des Pinselhandpunkts an. Zum Festlegen der Hintergrund- und Vordergrundfarben verwendet die Prozedur die [**Funktionen SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) und [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) mit dem Anzeigegerätekontext des Steuerelements. Die Farbmeldung des Steuerelements übergibt ein Handle an den Anzeigegerätekontext an die Prozedur im *wParam-Parameter der* Nachricht.

Das System sendet eine [**WM \_ CTLCOLORDLG-Nachricht**](wm-ctlcolordlg.md) an das Dialogfeldprozedur, wenn die Prozedur die [**WM \_ ERASEBKGND-Nachricht nicht verarbeiten**](/windows/desktop/winmsg/wm-erasebkgnd) kann. Die vordefinierte Dialogfeldklasse verfügt nicht über einen Klassenhintergrundpinsel, sodass die Prozedur mit dieser Meldung ihren eigenen Hintergrund definieren kann, ohne den Code zur Durchführung der Arbeit einfügen zu müssen.

Wenn eine Dialogfeldprozedur keine Steuerelementfarbmeldung verarbeiten kann, verwendet das System in jedem Fall einen Pinsel mit der Standardfensterfarbe, um den Hintergrund für alle Steuerelemente und Fenster mit Ausnahme von Bildlaufleisten zu zeichnen. Eine Anwendung kann die Standardfensterfarbe abrufen, indem der **COLOR \_ WINDOW-Wert** an die [**GetSysColor-Funktion übergeben**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) wird. Während der Hintergrund gestrichen wird, wird die Vordergrundfarbe für den Anzeigegerätekontext auf die Standardtextfarbe (**COLOR \_ WINDOWTEXT ) festgelegt.** Für Bildlaufleisten verwendet das System einen Pinsel mit der Standardmäßigen Bildlaufleistenfarbe (**COLOR \_ SCROLLBAR**). In diesem Fall werden die Hintergrund- und Vordergrundfarben für den Anzeigegerätekontext auf Weiß bzw. Schwarz festgelegt.

### <a name="dialog-box-default-message-processing"></a>Standardnachrichtenverarbeitung im Dialogfeld

Die Fensterprozedur für die vordefinierte Dialogfeldklasse führt die Standardverarbeitung für alle Nachrichten durch, die von der Dialogfeldprozedur nicht verarbeitet werden. Wenn die Dialogfeldprozedur **FALSE für** jede Nachricht zurückgibt, überprüft die vordefinierte Fensterprozedur die Nachrichten und führt die folgenden Standardaktionen aus:



| `Message`                                            | Standardaktion                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DM \_ GETDEFID**](dm-getdefid.md)                | Sie können diese Nachricht an ein Dialogfeld senden. Das Dialogfeld gibt den Steuerelementbezeichner der Standardschaltfläche zurück, wenn das Dialogfeld über eine schaltfläche verfügt. andernfalls wird 0 (null) zurückgegeben.                                                                                                                                                                                                                                                                                                                      |
| [**DM \_ REPOSITION**](dm-reposition.md)            | Sie können diese Nachricht an ein Dialogfeld der obersten Ebene senden. Das Dialogfeld positioniert sich selbst neu, sodass es in den Desktopbereich passt.                                                                                                                                                                                                                                                                                                                                                                       |
| [**DM \_ SETDEFID**](dm-setdefid.md)                | Sie können diese Nachricht an ein Dialogfeld senden. Im Dialogfeld wird die Standardschaltfläche auf das Steuerelement festgelegt, das durch den Steuerelementbezeichner im *wParam-Parameter angegeben* wird.                                                                                                                                                                                                                                                                                                                             |
| [**WM \_ ACTIVATE**](/windows/desktop/inputdev/wm-activate)           | Stellt den Eingabefokus auf dem Steuerelement wieder wieder auf, das vom zuvor gespeicherten Handle identifiziert wird, wenn das Dialogfeld aktiviert ist. Andernfalls speichert die Prozedur das Handle im Steuerelement mit dem Eingabefokus.                                                                                                                                                                                                                                                                                               |
| [**WM \_ CHARTOITEM**](../controls/wm-chartoitem.md)         | Gibt 0 (null) zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close)                   | Veröffentlicht die [**BN \_ CLICKED-Benachrichtigungsmeldung**](../controls/bn-clicked.md) im Dialogfeld und gibt **IDCANCEL** als Steuerelementbezeichner an. Wenn das Dialogfeld über einen IDCANCEL-Steuerelementbezeichner verfügt und das Steuerelement derzeit deaktiviert ist, wird von der Prozedur eine Warnung angezeigt, und die Meldung wird nicht gesendet.                                                                                                                                                                                              |
| [**WM \_ COMPAREITEM**](../controls/wm-compareitem.md)       | Gibt 0 (null) zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)         | Füllt den Clientbereich des Dialogfelds entweder mithilfe des Pinsels, der von der [**WM \_ CTLCOLORDLG-Meldung**](wm-ctlcolordlg.md) zurückgegeben wird, oder mit der Standardfensterfarbe.                                                                                                                                                                                                                                                                                                                                 |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Gibt ein Handle für die anwendungsdefinierte Dialogfeldschriftart zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ INITDIALOG**](wm-initdialog.md)            | Gibt 0 (null) zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | Sendet eine [**CB \_ SHOWDROPDOWN-Nachricht**](../controls/cb-showdropdown.md) an das Kombinationsfeld mit dem Eingabefokus und leitet das Steuerelement an, das Dropdownlistenfeld auszublenden. Die Prozedur ruft [**DefWindowProc auf,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) um die Standardaktion fertig zu machen.                                                                                                                                                                                                                                      |
| [**WM \_ NCDESTROY**](/windows/desktop/winmsg/wm-ncdestroy)           | Gibt globalen Arbeitsspeicher frei, der für Bearbeitungssteuerelemente im Dialogfeld zugeordnet ist (gilt für Dialogfelder, die den [**DS \_ LOCALEDIT-Stil**](dialog-box-styles.md) angeben) und gibt jede anwendungsdefinierte Schriftart frei (gilt für Dialogfelder, die den [**DS \_ SETFONT-**](dialog-box-styles.md) oder [**DS \_ SHELLFONT-Stil**](dialog-box-styles.md) angeben). Die Prozedur ruft die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) auf, um die Standardaktion fertig zu machen. |
| [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) | Sendet eine [**CB \_ SHOWDROPDOWN-Nachricht**](../controls/cb-showdropdown.md) an das Kombinationsfeld mit dem Eingabefokus und leitet das Steuerelement an, das Dropdownlistenfeld auszublenden. Die Prozedur ruft [**DefWindowProc auf,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) um die Standardaktion fertig zu machen.                                                                                                                                                                                                                                      |
| [**WM \_ NEXTDLGCTL**](wm-nextdlgctl.md)            | Legt den Eingabefokus auf das nächste oder vorherige Steuerelement im Dialogfeld, auf das Steuerelement fest, das durch das Handle im *wParam-Parameter* identifiziert wird, oder auf das erste Steuerelement im Dialogfeld, das sichtbar, nicht deaktiviert ist und über das [**WS \_ TABSTOP-Format**](/windows/desktop/winmsg/window-styles) verfügt. Die Prozedur ignoriert diese Meldung, wenn das aktuelle Fenster mit dem Eingabefokus kein Steuerelement ist.                                                                                                                  |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)           | Legt den Eingabefokus auf das Steuerelement fest, das von einem zuvor gespeicherten Steuerelementfensterhand handle identifiziert wird. Wenn kein solches Handle vorhanden ist, legt die Prozedur den Eingabefokus auf das erste Steuerelement in der Dialogfeldvorlage fest, das sichtbar und nicht deaktiviert ist und über das [**Format WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) verfügt. Wenn kein solches Steuerelement vorhanden ist, legt die Prozedur den Eingabefokus auf das erste Steuerelement in der Vorlage fest.                                                                                          |
| [**WM \_ SHOWWINDOW**](/windows/desktop/winmsg/wm-showwindow)         | Speichert ein Handle im Steuerelement mit dem Eingabefokus, wenn das Dialogfeld ausgeblendet wird, und ruft [**dann DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) auf, um die Standardaktion zu vervollständigen.                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)         | Speichert ein Handle im Steuerelement mit dem Eingabefokus, wenn das Dialogfeld minimiert wird, und ruft [**dann DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) auf, um die Standardaktion zu vervollständigen.                                                                                                                                                                                                                                                                                                                  |
| [**WM \_ VKEYTOITEM**](../controls/wm-vkeytoitem.md)         | Gibt 0 (null) zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

Die vordefinierte Fensterprozedur übergibt alle anderen Nachrichten zur Standardverarbeitung [**an DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

## <a name="dialog-box-keyboard-interface"></a>Dialogfeldtastaturschnittstelle

Das System stellt eine spezielle Tastaturschnittstelle für Dialogfelder bereit, die eine spezielle Verarbeitung für mehrere Tasten übernimmt. Die Schnittstelle generiert Meldungen, die bestimmten Schaltflächen im Dialogfeld entsprechen, oder ändert den Eingabefokus von einem Steuerelement in ein anderes. Im Folgenden finden Sie die Schlüssel, die in dieser Schnittstelle verwendet werden, und ihre jeweiligen Aktionen.


| Schlüssel            | Aktion                                                                                                                                                                    |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALT+*mnemonisch* | Verschiebt den Eingabefokus auf das erste Steuerelement (mit [**dem WS \_ TABSTOP-Stil)**](/windows/desktop/winmsg/window-styles) nach dem statischen Steuerelement, das das angegebene mnemonische Steuerelement enthält.        |
| DOWN           | Verschiebt den Eingabefokus auf das nächste Steuerelement in der Gruppe.                                                                                                                   |
| EINGABETASTE          | Sendet eine [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) an die Dialogfeldprozedur. Der *wParam-Parameter* ist auf IDOK oder steuerelementbezeichner der Standardschaltfläche festgelegt. |
| ESC            | Sendet eine [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) an die Dialogfeldprozedur. Der *wParam-Parameter* ist auf IDCANCEL festgelegt.                                              |
| LEFT           | Verschiebt den Eingabefokus auf das vorherige Steuerelement in der Gruppe.                                                                                                               |
| *Mnemonische*     | Verschiebt den Eingabefokus auf das erste Steuerelement (mit [**dem WS \_ TABSTOP-Stil)**](/windows/desktop/winmsg/window-styles) nach dem statischen Steuerelement, das das angegebene mnemonische Steuerelement enthält.        |
| RIGHT          | Verschiebt den Eingabefokus auf das nächste Steuerelement in der Gruppe.                                                                                                                   |
| UMSCHALT+TAB      | Verschiebt den Eingabefokus auf das vorherige Steuerelement mit dem [**WS \_ TABSTOP-Stil.**](/windows/desktop/winmsg/window-styles)                                                                |
| TAB            | Verschiebt den Eingabefokus auf das nächste Steuerelement mit dem [**WS \_ TABSTOP-Stil.**](/windows/desktop/winmsg/window-styles)                                                                    |
| UP             | Verschiebt den Eingabefokus auf das vorherige Steuerelement in der Gruppe.                                                                                                               |

Das System stellt automatisch die Tastaturschnittstelle für alle modalen Dialogfelder bereit. Sie stellt die Schnittstelle für nicht moduslose Dialogfelder nur dann bereit, wenn die Anwendung die [**IsDialogMessage-Funktion**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) aufruft, um Nachrichten in der Hauptnachrichtenschleife zu filtern. Dies bedeutet, dass die Anwendung die Nachricht unmittelbar nach dem Abrufen der Nachricht aus der Nachrichtenwarteschlange an **IsDialogMessage** übergeben muss. Die Funktion verarbeitet die Nachrichten, wenn sie für das Dialogfeld gilt, und gibt einen Wert ungleich 0 (null) zurück, um anzugeben, dass die Nachricht verarbeitet wurde und nicht an die [**TranslateMessage-**](/windows/desktop/api/winuser/nf-winuser-translatemessage) oder [**DispatchMessage-Funktion übergeben werden**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) darf.

Da die Tastaturschnittstelle des Dialogfelds Richtungstasten verwendet, um zwischen Steuerelementen in einem Dialogfeld zu wechseln, kann eine Anwendung diese Tasten nicht zum Scrollen des Inhalts eines modalen Dialogfelds oder eines moduslosen Dialogfelds verwenden, für das [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) aufgerufen wird. Wenn ein Dialogfeld Bildlaufleisten hat, muss die Anwendung eine alternative Tastaturschnittstelle für die Bildlaufleisten bereitstellen. Beachten Sie, dass die Mausschnittstelle zum Scrollen verfügbar ist, wenn das System eine Maus enthält.

### <a name="the-ws_tabstop-style"></a>Das \_ WS-TABSTOP-Format

Der [**WS \_ TABSTOP-Stil**](/windows/desktop/winmsg/window-styles) gibt die Steuerelemente an, zu denen der Benutzer wechseln kann, indem er die TAB-TASTE oder UMSCHALT+TAB-TASTE drückt.

Wenn der Benutzer TAB oder UMSCHALT+TAB drückt, bestimmt das System zuerst, ob diese Tasten von dem Steuerelement verarbeitet werden, das derzeit den Eingabefokus besitzt. Es sendet dem Steuerelement eine [**WM \_ GETDLGCODE-Nachricht,**](wm-getdlgcode.md) und wenn das Steuerelement DLGC WANTTAB zurückgibt, übergibt das System die Schlüssel \_ an das Steuerelement. Andernfalls verwendet das System die [**GetNextDlgTabItem-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) um das nächste Steuerelement zu suchen, das sichtbar und nicht deaktiviert ist und das [**das Format WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) aufweise. Die Suche beginnt mit dem Steuerelement, das derzeit den Eingabefokus hat, und wird in der Reihenfolge fortgesetzt, in der die Steuerelemente erstellt wurden, d.&a0;b. in der Reihenfolge, in der sie in der Dialogfeldvorlage definiert sind. Wenn das System ein Steuerelement mit den erforderlichen Merkmalen findet, verschiebt das System den Eingabefokus darauf.

Wenn bei der Suche nach dem nächsten Steuerelement mit dem [**WS \_ TABSTOP-Stil**](/windows/desktop/winmsg/window-styles) ein Fenster mit dem **WS \_ EX \_ CONTROLPARENT-Stil** auftritt, durchsucht das System rekursiv die unteren Fenster.

Eine Anwendung kann auch [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) verwenden, um Steuerelemente mit [**dem WS \_ TABSTOP-Stil zu**](/windows/desktop/winmsg/window-styles) suchen. Die Funktion ruft das Fensterhand handle des nächsten oder vorherigen Steuerelements mit dem **WS \_ TABSTOP-Format** ab, ohne den Eingabefokus zu verschieben.

### <a name="the-ws_group-style"></a>Der WS \_ GROUP-Stil

Standardmäßig verschiebt das System den Eingabefokus auf das nächste oder vorherige Steuerelement, wenn der Benutzer eine Richtungstaste drückt. Solange das aktuelle Steuerelement mit dem Eingabefokus diese Schlüssel nicht verarbeiten und das nächste oder vorherige Steuerelement kein statisches Steuerelement ist, bewegt das System den Eingabefokus weiterhin durch alle Steuerelemente im Dialogfeld, während der Benutzer weiterhin die Richtungstasten drückt.

Eine Anwendung kann das [**WS \_ GROUP-Format**](/windows/desktop/winmsg/window-styles) verwenden, um dieses Standardverhalten zu ändern. Der Stil markiert den Anfang einer Gruppe von Steuerelementen. Wenn ein Steuerelement in der Gruppe den Eingabefokus hat, wenn der Benutzer mit dem Drücken der Richtungstasten beginnt, verbleibt der Fokus in der Gruppe. Im Allgemeinen muss das erste Steuerelement in einer Gruppe den **WS \_ GROUP-Stil** haben, und alle anderen Steuerelemente in der Gruppe dürfen diesen Stil nicht haben. Alle Steuerelemente in der Gruppe müssen zusammenhängend sein. Das heißt, sie müssen nacheinander ohne intervenende Steuerelemente erstellt worden sein.

Wenn der Benutzer eine Richtungstaste drückt, bestimmt das System zuerst, ob das aktuelle Steuerelement mit dem Eingabefokus die Richtungsschlüssel verarbeitet. Das System sendet eine [**WM \_ GETDLGCODE-Nachricht**](wm-getdlgcode.md) an das Steuerelement, und wenn das Steuerelement den **WERT VON DLGC \_ WANTLGWS** zurückgibt, übergibt den Schlüssel an das Steuerelement. Andernfalls verwendet das System die [**GetNextDlgGroupItem-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) um das nächste Steuerelement in der Gruppe zu bestimmen.

[**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) durchsucht Steuerelemente in der Reihenfolge (oder umgekehrten Reihenfolge), in der sie erstellt wurden. Wenn der Benutzer die TASTE RIGHT oder DOWN drückt, gibt **GetNextDlgGroupItem** das nächste Steuerelement zurück, wenn dieses Steuerelement nicht über den [**WS \_ GROUP-Stil**](/windows/desktop/winmsg/window-styles) verfügt. Andernfalls kehrt die Funktion die Reihenfolge der Suche um und gibt das erste Steuerelement mit dem **WS \_ GROUP-Stil** zurück. Wenn der Benutzer die LEFT- oder UP-Taste drückt, gibt die Funktion das vorherige Steuerelement zurück, es sei denn, das aktuelle Steuerelement verfügt bereits über den **WS \_ GROUP-Stil.** Wenn das aktuelle Steuerelement über diesen Stil verfügt, kehrt die Funktion die Reihenfolge der Suche um, sucht das erste Steuerelement mit dem **WS \_ GROUP-Stil** und gibt das Steuerelement zurück, das unmittelbar vor dem gesuchten Steuerelement steht.

Wenn bei der Suche nach dem nächsten Steuerelement in der Gruppe ein Fenster mit dem **Format WS \_ EX \_ CONTROLPARENT** auftritt, durchsucht das System rekursiv die unteren Fenster.

Nachdem das System über das nächste oder vorherige Steuerelement verfügt, sendet es eine [**WM \_ GETDLGCODE-Nachricht**](wm-getdlgcode.md) an das Steuerelement, um den Steuerelementtyp zu bestimmen. Das System verschiebt dann den Eingabefokus, um zu steuern, ob es sich nicht um ein statisches Steuerelement handelt. Wenn es sich bei dem Steuerelement um ein automatisches Optionsfeld handelt, sendet das System eine [**BM \_ CLICK-Nachricht**](../controls/bm-click.md) an das Steuerelement. Eine Anwendung kann auch [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) verwenden, um Steuerelemente in einer Gruppe zu suchen.

Im Allgemeinen kombiniert das erste Steuerelement in der Gruppe die [**Stile WS \_ GROUP**](/windows/desktop/winmsg/window-styles) und [**WS \_ TABSTOP,**](/windows/desktop/winmsg/window-styles) sodass der Benutzer mithilfe der TAB-TASTE von Gruppe zu Gruppe wechseln kann. Wenn die Gruppe Optionsfelder enthält, sollte die Anwendung den **WS \_ TABSTOP-Stil** nur auf das erste Steuerelement in der Gruppe anwenden. Das System verschiebt den Stil automatisch, wenn der Benutzer zwischen Steuerelementen in der Gruppe wechselt. Dadurch wird sichergestellt, dass der Eingabefokus immer auf dem zuletzt ausgewählten Steuerelement liegt, wenn der Benutzer mithilfe der TAB-TASTE in die Gruppe wechselt.

### <a name="mnemonics"></a>Mnemotechnik

Ein mnemonisches Element ist ein ausgewählter Buchstabe oder eine ziffer in der Bezeichnung einer Schaltfläche oder im Text eines statischen Steuerelements. Das System verschiebt den Eingabefokus auf das Steuerelement, das dem mnemonischen -Steuerelement zugeordnet ist, wenn der Benutzer entweder die Taste drückt, die dem mnemonischen Schlüssel entspricht, oder diese Taste und die ALT-Taste in Kombination drückt. Mnemonische Daten bieten dem Benutzer eine schnelle Möglichkeit, mithilfe der Tastatur zu einem angegebenen Steuerelement zu wechseln.

Eine Anwendung erstellt ein mnemonisches Zeichen für ein Steuerelement, indem das ampersand (&) unmittelbar vor dem ausgewählten Buchstaben oder der ausgewählten Ziffer in der Bezeichnung oder im Text für das Steuerelement eingefügt wird. In den meisten Fällen enthält die mit NULL beendete Zeichenfolge, die mit dem -Steuerelement in der Dialogfeldvorlage bereitgestellt wird, das ampersand-Objekt. Eine Anwendung kann jedoch jederzeit ein mnemonisches -Steuerelement erstellen, indem die vorhandene Bezeichnung oder der Text eines Steuerelements durch die [**SetDlgItemText-Funktion ersetzt**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) wird. Für jedes Steuerelement kann nur ein mnemonisches -Steuerelement angegeben werden. Obwohl dies empfohlen wird, müssen mnemonische Daten in einem Dialogfeld nicht eindeutig sein.

Wenn der Benutzer einen Buchstaben oder eine Zifferntaste drückt, bestimmt das System zuerst, ob das aktuelle Steuerelement mit dem Eingabefokus die Taste verarbeitet. Das System sendet eine [**WM \_ GETDLGCODE-Nachricht**](wm-getdlgcode.md) an das Steuerelement, und wenn das Steuerelement den **DLGC \_ WANTALLKEYS-** oder **DLG \_ WANTMESSAGE-Wert** zurückgibt, übergibt das System den Schlüssel an das Steuerelement. Andernfalls wird nach einem Steuerelement gesucht, dessen mnemonisches Ergebnis dem angegebenen Buchstaben oder der angegebenen Ziffer entspricht. Die Suche wird fortgesetzt, bis ein Steuerelement gefunden oder alle Steuerelemente untersucht wurden. Während der Suche werden alle statischen Steuerelemente übersprungen, die das [**SS \_ NOPREFIX-Format**](../controls/static-control-styles.md) haben.

Wenn die Suche nach einem Steuerelement mit einem entsprechenden mnemonischen -Steuerelement auf ein Fenster mit dem **WS \_ EX \_ CONTROLPARENT-Stil** trifft, durchsucht das System rekursiv die unteren Fenster.

Wenn das System ein statisches Steuerelement findet und das Steuerelement nicht deaktiviert ist, verschiebt das System den Eingabefokus auf das erste Steuerelement nach dem statischen Steuerelement, das sichtbar und nicht deaktiviert ist und über das [**WS \_ TABSTOP-Format**](/windows/desktop/winmsg/window-styles) verfügt. Wenn das System ein anderes Steuerelement findet, das über ein entsprechendes mnemonisches Steuerelement verfügt, verschiebt es den Eingabefokus auf dieses Steuerelement. Wenn es sich bei dem Steuerelement um eine Standardschaltfläche handelt, sendet das System eine [**BN CLICKED-Benachrichtigungsmeldung \_**](../controls/bn-clicked.md) an die Dialogfeldprozedur. Wenn es sich bei dem Steuerelement um ein anderes Schaltflächenformat handelt und im Dialogfeld kein anderes Steuerelement mit dem gleichen mnemonischen Steuerelement angezeigt wird, sendet das System die [**BM \_ CLICK-Nachricht**](../controls/bm-click.md) an das Steuerelement.

## <a name="dialog-box-settings"></a>Dialogfeld-Einstellungen

Die Dialogfeldeinstellungen sind die aktuellen Auswahlen und Werte für die Steuerelemente im Dialogfeld. Die Dialogfeldprozedur ist für das Initialisieren der Steuerelemente auf diese Einstellungen beim Erstellen des Dialogfelds verantwortlich. Sie ist auch für das Abrufen der aktuellen Einstellungen aus den Steuerelementen verantwortlich, bevor das Dialogfeld zerstört wird. Welche Methoden zum Initialisieren und Abrufen von Einstellungen verwendet werden, hängt vom Typ des Steuerelements ab.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Optionsfelder und Kontrollkästchen](#radio-buttons-and-check-boxes)
-   [Dialogfeld "Steuerelemente bearbeiten"](#dialog-box-edit-controls)
-   [Listenfelder, Kombinationsfelder und Verzeichnisauflistungen](#list-boxes-combo-boxes-and-directory-listings)
-   [Dialogfeld-Steuerungsmeldungen](#dialog-box-control-messages)

### <a name="radio-buttons-and-check-boxes"></a>Optionsfelder und Kontrollkästchen

Dialogfelder verwenden Optionsfelder und Kontrollkästchen, damit der Benutzer aus einer Liste von Optionen auswählen kann. Mit Optionsfeldern kann der Benutzer aus optionen auswählen, die sich gegenseitig ausschließen. Mit Kontrollkästchen kann der Benutzer eine Kombination von Optionen auswählen.

Die Dialogfeldprozedur kann den Anfangszustand eines Kontrollkästchens mithilfe der [**CheckDlgButton-Funktion**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx) festlegen, die das Kontrollkästchen ein- oder auscheckt. Für Optionsfelder in einer Gruppe von Optionsfeldern, die sich gegenseitig ausschließen, kann die Dialogfeldprozedur die [**CheckSchachtelButton-Funktion**](https://msdn.microsoft.com/library/Cc410654(v=MSDN.10).aspx) verwenden, um das entsprechende Optionsfeld zu setzen und jedes andere Optionsfeld automatisch zu löschen.

Bevor ein Dialogfeld beendet wird, kann die Dialogfeldprozedur den Status jedes Optionsfelds und Kontrollkästchens mithilfe der [**IsDlgButtonChecked-Funktion**](https://msdn.microsoft.com/library/Cc364806(v=MSDN.10).aspx) überprüfen, die den aktuellen Zustand der Schaltfläche zurückgibt. Ein Dialogfeld speichert diese Informationen in der Regel, um die Schaltflächen beim nächsten Erstellen des Dialogfelds zu initialisieren.

### <a name="dialog-box-edit-controls"></a>Dialogfeld "Steuerelemente bearbeiten"

Viele Dialogfelder verfügen über Bearbeitungssteuerelemente, mit denen der Benutzer Text als Eingabe eingeben kann. Die meisten Dialogfeld-Prozeduren initialisieren ein Bearbeitungssteuerfeld, wenn das Dialogfeld zum ersten Mal gestartet wird. Beispielsweise kann die Dialogfeldprozedur einen vorgeschlagenen Dateinamen in das Steuerelement einfügen, den der Benutzer dann auswählen, ändern oder ersetzen kann. Die Dialogfeldprozedur kann den Text in einem Bearbeitungssteuerfeld mithilfe der [**SetDlgItemText-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) festlegen, die Text aus einem angegebenen Puffer in das Bearbeitungssteuerfeld kopiert. Wenn das Bearbeitungssteuerfeld den Eingabefokus erhält, wählt es automatisch den vollständigen Text für die Bearbeitung aus.

Da Bearbeitungssteuerelemente ihren Text nicht automatisch an das Dialogfeld zurückgeben, muss die Dialogfeldprozedur den Text abrufen, bevor er beendet wird. Der Text kann mithilfe der [**GetDlgItemText-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) abgerufen werden, die den Bearbeitungssteuertext in einen Puffer kopiert. Die Dialogfeldprozedur speichert diesen Text in der Regel, um das Bearbeitungssteuerfeld später zu initialisieren, oder übergibt ihn zur Verarbeitung an das übergeordnete Fenster.

Einige Dialogfelder verwenden Bearbeitungssteuerelemente, mit denen der Benutzer Zahlen eingeben kann. Die Dialogfeldprozedur kann mithilfe der [**GetDlgItemInt-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) eine Zahl aus einem Bearbeitungssteuerfeld abrufen, die den Text aus dem Bearbeitungssteuerfeld abruft und den Text in einen Dezimalwert konvertiert. Der Benutzer gibt die Zahl in Dezimalstellen ein. Sie kann entweder signiert oder unsigniert sein. Die Dialogfeldprozedur kann mithilfe der [**SetDlgItemInt-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemint) eine ganze Zahl anzeigen. **SetDlgItemInt konvertiert** eine ganze Zahl mit oder ohne Vorzeichen in eine Zeichenfolge mit Dezimalstellen.

### <a name="list-boxes-combo-boxes-and-directory-listings"></a>Listenfelder, Kombinationsfelder und Verzeichnisauflistungen

In einigen Dialogfeldern werden Listen mit Namen angezeigt, aus denen der Benutzer einen oder mehrere Namen auswählen kann. Um eine Liste von Dateinamen anzuzeigen, z. B. verwendet ein Dialogfeld in der Regel ein Listenfeld und die [**Funktionen DlgDirList**](https://msdn.microsoft.com/library/Cc410788(v=MSDN.10).aspx) und [**DlgDirSelectEx.**](https://msdn.microsoft.com/library/Cc410769(v=MSDN.10).aspx) Die **DlgDirList-Funktion** füllt automatisch ein Listenfeld mit den Dateinamen im aktuellen Verzeichnis aus. Die **DlgDirSelect-Funktion** ruft den ausgewählten Dateinamen aus dem Listenfeld ab. Zusammen bieten diese beiden Funktionen eine praktische Möglichkeit für ein Dialogfeld, eine Verzeichnisauflistung anzuzeigen, damit der Benutzer eine Datei auswählen kann, ohne ihren Namen und Speicherort eingeben zu müssen.

Ein Dialogfeld kann auch ein Kombinationsfeld verwenden, um eine Liste von Dateinamen anzuzeigen. Die [**DlgDirListComboBox-Funktion**](https://msdn.microsoft.com/library/Cc410798(v=MSDN.10).aspx) füllt automatisch einen Listenfeldteil des Kombinationsfelds mit den Dateinamen im aktuellen Verzeichnis aus. Die [**DlgDirSelectComboBoxEx-Funktion**](https://msdn.microsoft.com/library/Cc410768(v=MSDN.10).aspx) ruft einen ausgewählten Dateinamen aus dem Listenfeldteil ab.

### <a name="dialog-box-control-messages"></a>Dialogfeld-Steuerungsmeldungen

Viele Steuerelemente erkennen vordefinierte Meldungen, die beim Empfangen durch Steuerelemente dazu führen, dass sie eine Aktion durchführen. Die BM [**\_ SETCHECK-Nachricht**](../controls/bm-setcheck.md) legt z. B. das Einchecken in einem Kontrollkästchen fest, und die [**EM \_ GETSEL-Nachricht**](../controls/em-getsel.md) ruft den derzeit ausgewählten Teil des Steuerelementtexts ab. Die Steuermeldungen bieten einer Dialogprozedur einen größeren und flexibleren Zugriff auf die Steuerelemente als die Standardfunktionen, sodass sie häufig verwendet werden, wenn das Dialogfeld komplexe Interaktionen mit dem Benutzer erfordert.

Eine Dialogfeldprozedur kann eine Nachricht an ein Steuerelement senden, indem sie den Steuerelementbezeichner angibt und die [**SendDlgItemMessage-Funktion**](/windows/desktop/api/Winuser/nf-winuser-senddlgitemmessagea) verwendet, die mit der [**SendMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-sendmessage) identisch ist. Es wird jedoch ein Steuerelementbezeichner anstelle eines Fensterhandle verwendet, um das Steuerelement zu identifizieren, das die Nachricht empfangen soll. Eine angegebene Nachricht erfordert möglicherweise, dass die Dialogprozedur Parameter mit der Nachricht sendet, und die Nachricht kann über entsprechende Rückgabewerte verfügen. Der Vorgang und die Anforderungen jeder Steuernachricht hängen vom Zweck der Nachricht und dem Steuerelement ab, das sie verarbeitet.

Weitere Informationen zu den Steuerelementmeldungen finden Sie unter [Windows Controls](../controls/window-controls.md).

## <a name="custom-dialog-boxes"></a>Benutzerdefinierte Dialogfelder

Eine Anwendung kann benutzerdefinierte Dialogfelder erstellen, indem sie eine anwendungsdefinierte Fensterklasse für die Dialogfelder anstelle der vordefinierten Dialogfeldklasse verwendet. Anwendungen verwenden diese Methode in der Regel, wenn ein Dialogfeld das Hauptfenster ist. Es ist aber auch nützlich, um modale und moduslose Dialogfelder für Anwendungen zu erstellen, die überlappende Standardfenster aufweisen.

Mit der von der Anwendung definierten Fensterklasse kann die Anwendung eine Fensterprozedur für das Dialogfeld definieren und Nachrichten verarbeiten, bevor sie an die Dialogfeldprozedur gesendet werden. Außerdem kann die Anwendung ein Klassensymbol, einen Klassenhintergrundpinsel und ein Klassenmenü für das Dialogfeld definieren. Die Anwendung muss die Fensterklasse registrieren, bevor sie versucht, ein Dialogfeld zu erstellen, und muss die Dialogfeldvorlage mit dem Atomwert oder Namen der Fensterklasse bereitstellen.

Viele Anwendungen erstellen eine neue Dialogfeldklasse, indem sie zuerst die Klasseninformationen für die vordefinierte Dialogfeldklasse abrufen und an die [**GetClassInfo-Funktion**](/windows/desktop/api/winuser/nf-winuser-getclassinfoa) übergeben, die eine [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) mit den Informationen füllt. Die Anwendung ändert einzelne Member der -Struktur, z. B. den Klassennamen, den Pinsel und das Symbol, und registriert dann die neue Klasse mithilfe der [**RegisterClass-Funktion.**](/windows/desktop/api/winuser/nf-winuser-registerclassa) Wenn eine Anwendung die **WNDCLASS-Struktur** eigenständig ausfüllt, muss sie den **cbWndExtra-Member** auf **DLGWINDOWEXTRA** festlegen. Dies ist die Anzahl zusätzlicher Bytes, die das System für jedes Dialogfeld benötigt. Wenn eine Anwendung auch zusätzliche Bytes für jedes Dialogfeld verwendet, müssen sie über die zusätzlichen Bytes hinausgehen, die vom System benötigt werden.

Die Fensterprozedur für das benutzerdefinierte Dialogfeld verfügt über die gleichen Parameter und Anforderungen wie jede andere Fensterprozedur. Im Gegensatz zu anderen Fensterprozeduren sollte die Fensterprozedur für dieses Dialogfeld jedoch die [**DefDlgProc-Funktion**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) anstelle der [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) für alle Nachrichten aufrufen, die nicht verarbeitet werden. **DefDlgProc** führt die gleiche Standardnachrichtenverarbeitung durch wie die Fensterprozedur für das vordefinierte Dialogfeld, einschließlich des Aufrufs der Dialogfeldprozedur.

Eine Anwendung kann auch benutzerdefinierte Dialogfelder erstellen, indem sie die Fensterprozedur des vordefinierten Dialogfelds untergliedert. Mit der [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) kann eine Anwendung die Fensterprozedur für ein angegebenes Fenster angeben. Die Anwendung versucht möglicherweise auch, eine Unterklasse mithilfe der [**SetClassLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) zu erstellen. Dies wirkt sich jedoch auf alle Dialogfelder im System aus, nicht nur auf diejenigen, die zur Anwendung gehören.

Anwendungen, die benutzerdefinierte Dialogfelder erstellen, stellen manchmal eine alternative Tastaturschnittstelle für die Dialogfelder bereit. Bei dialogfeldern ohne Modus kann dies bedeuten, dass die Anwendung die [**IsDialogMessage-Funktion**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) nicht aufruft und stattdessen alle Tastatureingaben in der benutzerdefinierten Fensterprozedur verarbeitet. In solchen Fällen kann die Anwendung die [**WM \_ NEXTDLGCTL-Nachricht**](wm-nextdlgctl.md) verwenden, um den Code zu minimieren, der erforderlich ist, um den Eingabefokus von einem Steuerelement in ein anderes zu verschieben. Wenn diese Meldung an [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)übergeben wird, verschiebt sie den Eingabefokus auf ein angegebenes Steuerelement und aktualisiert die Darstellung der Steuerelemente, z.B. das Verschieben des Standardrahmens für Diebstaste oder das Festlegen eines automatischen Optionsfelds.
