---
title: Informationen zu Hot Key-Steuerelementen
description: Ein Hot Key-Steuerelement ist ein Fenster, in dem der Benutzer eine Kombination von Tastatureingaben eingeben kann, die als hot-Taste verwendet werden sollen.
ms.assetid: 5f011459-4c30-45d4-9668-19f575b041ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256fcfde87a1fb6603f90e8a2a41cb4f2cc9356f9f45d861efdc6836aa5344fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672243"
---
# <a name="about-hot-key-controls"></a>Informationen zu Hot Key-Steuerelementen

Ein Hot Key-Steuerelement ist ein Fenster, in dem der Benutzer eine Kombination von Tastatureingaben eingeben kann, die als hot-Taste verwendet werden sollen. Eine hot-Taste ist eine Tastenkombination, die der Benutzer drücken kann, um schnell eine Aktion durchzuführen. Beispielsweise kann ein Benutzer einen hot-Schlüssel erstellen, der ein bestimmtes Fenster aktiviert und an den Anfang der Z-Reihenfolge bringt. Das Hot Key-Steuerelement zeigt die Auswahlmöglichkeiten des Benutzers an und stellt sicher, dass der Benutzer eine gültige Tastenkombination auswählt. Der folgende Screenshot zeigt, wie ein Hot-Key-Steuerelement in einem Dialogfeld angezeigt wird, nachdem der Benutzer die ALT-TASTE gedrückt hat.

![Screenshot eines Dialogfelds, das ein Hot-Key-Steuerelement enthält](images/hotkey.png)

## <a name="using-hot-key-controls"></a>Verwenden von Hot Key-Steuerelementen

Wenn der Benutzer eine Tastenkombination ein gibt, die als Hot Key verwendet werden soll, werden die Namen der Schlüssel im Hot Key-Steuerelement angezeigt. Eine Tastenkombination kann aus einer Modifizierertaste (z. B. STRG, ALT oder UMSCHALT) und einer zugehörigen Taste (z. B. einer Zeichentaste, einer Pfeiltaste, einer Funktionstaste und so weiter) bestehen.

Nachdem der Benutzer eine Tastenkombination ausgewählt hat, ruft die Anwendung die Tastenkombination aus dem Hot Key-Steuerelement ab und verwendet sie zum Einrichten eines hot-Schlüssels im System. Die vom Hot Key-Steuerelement abgerufenen Informationen enthalten ein Flag, das den Modifiziererschlüssel und den virtuellen Schlüsselcode des zugehörigen Schlüssels angibt.

Die Anwendung kann die Von einem Hot Key-Steuerelement bereitgestellten Informationen verwenden, um einen globalen hot-Schlüssel oder einen threadspezifischen hot-Schlüssel zu einrichten. Ein globaler Hot Key ist einem bestimmten Fenster zugeordnet. Sie ermöglicht es dem Benutzer, das Fenster in einem beliebigen Teil des Systems zu aktivieren. Eine Anwendung legt mithilfe der [**WM \_ SETHOTKEY-Nachricht**](/windows/desktop/inputdev/wm-sethotkey) einen globalen Hot Key fest. Wenn der Benutzer einen globalen hot-Schlüssel drückt, empfängt das in **WM \_ SETHOTKEY** angegebene Fenster eine [**WM \_ SYSCOMMAND-Meldung,**](/windows/desktop/menurc/wm-syscommand) die den [**SC \_ HOTKEY-Wert angibt.**](/windows/desktop/inputdev/wm-sethotkey) Diese Meldung aktiviert das Fenster, das sie empfängt. Der hot-Schlüssel bleibt gültig, bis die Anwendung, die **WM \_ SETHOTKEY aufgerufen** hat, beendet wird.

Ein threadspezifischer hot-Schlüssel generiert eine [**WM \_ HOTKEY-Nachricht,**](/windows/desktop/inputdev/wm-hotkey) die an den Anfang eines bestimmten Threads gesendet wird, sodass sie bei der nächsten Iteration der Nachrichtenschleife entfernt wird. Eine Anwendung legt einen threadspezifischen hot-Schlüssel mithilfe der [**RegisterHotKey-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerhotkey) fest.

### <a name="hot-key-control-messages"></a>Hot Key-Steuerungsmeldungen

Nach dem Erstellen eines Hot Key-Steuerelements interagiert eine Anwendung mit drei Nachrichten: [**HKM \_ SETRULES,**](hkm-setrules.md) [**HKM \_ SETHOTKEY**](hkm-sethotkey.md)und [**HKM \_ GETHOTKEY**](hkm-gethotkey.md).

Eine Anwendung kann die [**HKM \_ SETRULES-Nachricht**](hkm-setrules.md) senden, um eine Reihe von TASTENKOMBINATIONEN (STRG, ALT und UMSCHALT) anzugeben, die als ungültige Hot-Tasten betrachtet werden. Wenn die Anwendung eine ungültige Tastenkombination angibt, sollte sie auch eine Standardmodifiziererkombination angeben, die verwendet werden soll, wenn der Benutzer die ungültige Kombination auswählt. Wenn der Benutzer die ungültige Kombination ein gibt, führt das System einen logischen OR-Vorgang für die ungültige Kombination und die Standardkombination aus. Das Ergebnis wird als gültige Kombination betrachtet. es wird in eine Zeichenfolge konvertiert und im -Steuerelement angezeigt.

Die [**HKM \_ SETHOTKEY-Nachricht**](hkm-sethotkey.md) ermöglicht einer Anwendung das Festlegen der Hot Key-Kombination für ein Hot Key-Steuerelement. Diese Meldung wird in der Regel auch verwendet, wenn das Hot Key-Steuerelement erstellt wird.

Anwendungen verwenden die [**HKM \_ GETHOTKEY-Nachricht,**](hkm-gethotkey.md) um den virtuellen Schlüsselcode und die Modifiziererflags des vom Benutzer ausgewählten hot-Schlüssels abzurufen.

### <a name="hot-key-control-notifications"></a>Benachrichtigungen zur Hot Key-Steuerung

Das Hot Key-Steuerelement sendet keine Benachrichtigungscodes über die [**WM \_ NOTIFY-Nachricht.**](wm-notify.md) Die [EN CHANGE-Benachrichtigung \_](en-change.md) wird jedoch über die [**WM \_ COMMAND-Nachricht**](/windows/desktop/menurc/wm-command) gesendet, wenn der Benutzer den Inhalt des Steuerelements ändert.

### <a name="default-hot-key-message-processing"></a>Standardmäßige Verarbeitung von Hot Key-Nachrichten

In diesem Abschnitt werden die Fenstermeldungen beschrieben, die von der Fensterprozedur für die vordefinierte HOTKEY CLASS-Fensterklasse verarbeitet werden, die mit [**HotKey-Steuerelementen \_**](common-control-window-classes.md) verwendet wird.

|    `Message`                                            |    Verarbeitung ausgeführt                               |
|------------------------------------------------|--------------------------------------------------------------|
| [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)               | Ruft den Code des virtuellen Schlüssels ab.             |
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)             | Initialisiert das Hot Key-Steuerelement, clears any hot key rules und verwendet die Systemschriftart.   |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)     | Blendet den Caretpunkt aus, ruft die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) auf und zeigt den Caretpunkt erneut an.   |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)     | Gibt eine Kombination der [**DLGC \_ WANTCHARS- und**](/windows/desktop/dlgbox/wm-getdlgcode) [**DLGC \_ WANTWS-Werte**](/windows/desktop/dlgbox/wm-getdlgcode) zurück.   |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)           | Ruft die Schriftart ab.                         |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)         | Ruft die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) auf, wenn der Schlüssel ENTER, TAB, SPACE BAR, DEL, ESC oder BACKSPACE ist. Wenn die Taste UMSCHALT, STRG oder ALT ist, überprüft sie, ob die Kombination gültig ist, und legt die heiße Taste mithilfe der Kombination fest. Alle anderen Schlüssel werden als Hot Keys festgelegt, ohne dass ihre Gültigkeit zuerst überprüft wird. |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)             | Ruft den Code des virtuellen Schlüssels ab.             |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)     | Zerstört das Caret-Caret-                         |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) | Legt den Fokus auf das Fenster fest.               |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)         | Legt den [**WS \_ EX \_ CLIENTEDGE-Fensterstil**](/windows/desktop/winmsg/extended-window-styles) fest.        |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                  | Zeichnet das Hot Key-Steuerelement.                 |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)       | Erstellt das Caret-Caret- und zeigt es an.                |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)           | Legt die Schriftart fest.                              |
| [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar)           | Ruft den Code des virtuellen Schlüssels ab.             |
| [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)   | Ruft die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) auf, wenn der Schlüssel ENTER, TAB, SPACE BAR, DEL, ESC oder BACKSPACE ist. Wenn die Taste UMSCHALT, STRG oder ALT ist, überprüft sie, ob die Kombination gültig ist, und legt die heiße Taste mithilfe der Kombination fest. Alle anderen Schlüssel werden als Hot Keys festgelegt, ohne dass ihre Gültigkeit zuerst überprüft wird. |
| [**WM \_ SYSKEYUP**](/windows/desktop/inputdev/wm-syskeyup)       | Ruft den Code des virtuellen Schlüssels ab.             |
