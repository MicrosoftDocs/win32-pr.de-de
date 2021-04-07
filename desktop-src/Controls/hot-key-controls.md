---
title: Informationen zu Hot Key-Steuerelementen
description: Ein Hot Key-Steuerelement ist ein Fenster, das es dem Benutzer ermöglicht, eine Kombination von Tastatureingaben einzugeben, die als heiße Taste verwendet werden sollen.
ms.assetid: 5f011459-4c30-45d4-9668-19f575b041ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec45d61df535025cff00fee6428f604aa670bf3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730481"
---
# <a name="about-hot-key-controls"></a>Informationen zu Hot Key-Steuerelementen

Ein Hot Key-Steuerelement ist ein Fenster, das es dem Benutzer ermöglicht, eine Kombination von Tastatureingaben einzugeben, die als heiße Taste verwendet werden sollen. Eine heiße Taste ist eine Tastenkombination, die der Benutzer zum schnellen Ausführen einer Aktion drücken kann. Beispielsweise kann ein Benutzer einen Hot-Schlüssel erstellen, der ein bestimmtes Fenster aktiviert und an den Anfang der z-Reihenfolge bringt. Das Steuerelement "Hot Key" zeigt die Auswahl des Benutzers an und stellt sicher, dass der Benutzer eine gültige Tastenkombination auswählt. Der folgende Screenshot zeigt, wie ein Steuerelement für den Abkürzungs Schlüssel in einem Dialogfeld angezeigt wird, nachdem der Benutzer die Alt-Taste gedrückt hat.

![Screenshot eines Dialog Felds, das ein Hot Key-Steuerelement enthält](images/hotkey.png)

## <a name="using-hot-key-controls"></a>Verwenden von Hot Key-Steuerelementen

Wenn der Benutzer eine Tastenkombination eingibt, die als heiße Taste verwendet werden soll, werden die Namen der Schlüssel im Steuerelement "Hot Key" angezeigt. Eine Tastenkombination kann aus einer Modifizierertaste (z. b. STRG, alt oder UMSCHALT) und einem begleitenden Schlüssel (z. b. eine Zeichen Taste, eine Pfeiltaste, eine Funktionstaste usw.) bestehen.

Nachdem der Benutzer eine Tastenkombination ausgewählt hat, ruft die Anwendung die Tastenkombination aus dem Steuerelement "Hot Key" ab und verwendet Sie, um eine systemeigene Taste im System einzurichten. Die aus dem Hot Key-Steuerelement abgerufenen Informationen enthalten ein Flag, das die Modifizierertaste und den virtuellen Schlüsselcode des zugehörigen Schlüssels angibt.

Die Anwendung kann die Informationen, die von einem Steuerelement für heiße Schlüssel bereitgestellt werden, verwenden, um einen globalen Hot Key oder eine Thread spezifische Hot Key-Taste einzurichten. Eine globale Hot-Taste ist einem bestimmten Fenster zugeordnet. Es ermöglicht dem Benutzer, das Fenster in jedem Teil des Systems zu aktivieren. Eine Anwendung legt mithilfe der [**WM \_ SetHotKey**](/windows/desktop/inputdev/wm-sethotkey) -Nachricht eine globale Taste für den Schlüssel fest. Jedes Mal, wenn der Benutzer eine globale Hotkey-Taste drückt, empfängt das in " **WM \_** " angegebene Fenster eine " [**WM \_ syscommand**](/windows/desktop/menurc/wm-syscommand) "-Meldung, die den [**SC- \_ Hotkey**](/windows/desktop/inputdev/wm-sethotkey) -Wert angibt. Diese Meldung aktiviert das Fenster, in dem Sie empfangen wird. Die Hot-Taste bleibt gültig, bis die Anwendung, die **WM \_ SetHotKey** aufgerufen hat, beendet wird.

Ein Thread spezifischer [**Hotkey generiert eine WM- \_ Hotkey**](/windows/desktop/inputdev/wm-hotkey) -Nachricht, die an den Anfang eines bestimmten Threads gesendet wird, sodass Sie von der nächsten Iterationen der Nachrichten Schleife entfernt wird. Eine Anwendung legt mithilfe der [**RegisterHotKey**](/windows/desktop/api/winuser/nf-winuser-registerhotkey) -Funktion einen Thread spezifischen Hotkey fest.

### <a name="hot-key-control-messages"></a>Hot Key Control-Meldungen

Nachdem Sie ein Hot Key-Steuerelement erstellt haben, interagiert eine Anwendung mithilfe von drei Nachrichten: [**HKM \_ setrules**](hkm-setrules.md), [**HKM \_ SetHotKey**](hkm-sethotkey.md)und [**HKM \_ GetHotKey**](hkm-gethotkey.md).

Eine Anwendung kann die [**HKM \_ setrules**](hkm-setrules.md) -Nachricht senden, um einen Satz von Tastenkombinationen für STRG, alt und UMSCHALT anzugeben, die als ungültige Abkürzungs Tasten angesehen werden. Wenn die Anwendung eine ungültige Tastenkombination angibt, sollte auch eine standardmodifiziererkombination angegeben werden, die verwendet werden soll, wenn der Benutzer die ungültige Kombination auswählt. Wenn der Benutzer die ungültige Kombination eingibt, führt das System eine logische OR-Operation für die ungültige Kombination und die Standardkombination aus. Das Ergebnis wird als gültige Kombination betrachtet. Sie wird in eine Zeichenfolge konvertiert und im-Steuerelement angezeigt.

Die [**HKM \_ SetHotKey**](hkm-sethotkey.md) -Nachricht ermöglicht einer Anwendung die Festlegung der Tastenkombination für ein Hot Key-Steuerelement. Diese Meldung wird normalerweise auch verwendet, wenn das Steuerelement für die Hot-Taste erstellt wird.

Anwendungen verwenden die [**HKM \_ GetHotKey**](hkm-gethotkey.md) -Nachricht, um den Code und die Modifiziererflags des virtuellen Schlüssels abzurufen, der vom Benutzer ausgewählt wurde.

### <a name="hot-key-control-notifications"></a>Benachrichtigungen über die Hot Key-Steuerung

Das Hot Key-Steuerelement sendet keine Benachrichtigungs Codes über die WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md) Wenn der Benutzer den Inhalt des Steuer Elements ändert, sendet er jedoch die [ \_ Änderungs](en-change.md) Benachrichtigung "en" über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.

### <a name="default-hot-key-message-processing"></a>Standard Nachrichtenverarbeitung für heiße Schlüssel

In diesem Abschnitt werden die Fenster Meldungen beschrieben, die von der Fenster Prozedur für die vordefinierte [**Hotkey- \_ Klassen**](common-control-window-classes.md) Fenster-Klasse behandelt werden, die mit Hot Key-Steuerelementen



|                                                |                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Meldung**                                    | **Verarbeitung wird ausgeführt**                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ -Zeichen**](/windows/desktop/inputdev/wm-char)               | Ruft den Code des virtuellen Schlüssels ab.                                                                                                                                                                                                                                                                                                               |
| [**WM \_ Erstellen**](/windows/desktop/winmsg/wm-create)             | Initialisiert das Hot Key-Steuerelement, löscht alle Regeln für den Abkürzungs Schlüssel und verwendet die System Schriftart.                                                                                                                                                                                                                                                          |
| [**WM- \_ erasebkgnd**](/windows/desktop/winmsg/wm-erasebkgnd)     | Blendet die Einfügemarke aus, ruft die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion auf und zeigt die Einfügemarke erneut an.                                                                                                                                                                                                                                     |
| [**WM \_ getdlgcode**](/windows/desktop/dlgbox/wm-getdlgcode)     | Gibt eine Kombination der [**dlgc- \_ wantchars**](/windows/desktop/dlgbox/wm-getdlgcode) -und [**dlgc- \_ wantpfeile**](/windows/desktop/dlgbox/wm-getdlgcode) -Werte zurück.                                                                                                                                               |
| [**WM- \_ getFont**](/windows/desktop/winmsg/wm-getfont)           | Ruft die Schriftart ab.                                                                                                                                                                                                                                                                                                                           |
| [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown)         | Ruft die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion auf, wenn die Taste eingegeben, Tab, Leertaste, del, ESC oder RÜCKTASTE ist. Wenn der Schlüssel Shift, STRG oder alt ist, wird überprüft, ob die Kombination gültig ist. wenn dies der Fall ist, wird die Taste mit der Kombination aus festgelegt. Alle anderen Schlüssel werden als heiße Schlüssel festgelegt, ohne dass deren Gültigkeit zuerst überprüft wird. |
| [**WM- \_ KeyUp**](/windows/desktop/inputdev/wm-keyup)             | Ruft den Code des virtuellen Schlüssels ab.                                                                                                                                                                                                                                                                                                               |
| [**WM- \_ killfokus**](/windows/desktop/inputdev/wm-killfocus)     | Zerstört das Caretzeichen.                                                                                                                                                                                                                                                                                                                           |
| [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) | Legt den Fokus auf das Fenster fest.                                                                                                                                                                                                                                                                                                                 |
| [**WM- \_ nccreate**](/windows/desktop/winmsg/wm-nccreate)         | Legt den Stil des [**WS \_ Ex \_ clientedge**](/windows/desktop/winmsg/extended-window-styles) -Fensters fest.                                                                                                                                                                                                                              |
| [**WM- \_ Paint**](/windows/desktop/gdi/wm-paint)                  | Zeichnet das Hot Key-Steuerelement.                                                                                                                                                                                                                                                                                                                   |
| [**WM- \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus)       | Erstellt das Caretzeichen und zeigt es an.                                                                                                                                                                                                                                                                                                                  |
| [**WM- \_ setFont**](/windows/desktop/winmsg/wm-setfont)           | Legt die Schriftart fest.                                                                                                                                                                                                                                                                                                                                |
| [**WM- \_ syschar**](/windows/desktop/menurc/wm-syschar)           | Ruft den Code des virtuellen Schlüssels ab.                                                                                                                                                                                                                                                                                                               |
| [**WM \_ syskeydown**](/windows/desktop/inputdev/wm-syskeydown)   | Ruft die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion auf, wenn die Taste eingegeben, Tab, Leertaste, del, ESC oder RÜCKTASTE ist. Wenn der Schlüssel Shift, STRG oder alt ist, wird überprüft, ob die Kombination gültig ist. wenn dies der Fall ist, wird die Taste mit der Kombination aus festgelegt. Alle anderen Schlüssel werden als heiße Schlüssel festgelegt, ohne dass deren Gültigkeit zuerst überprüft wird. |
| [**WM- \_ syskeyup**](/windows/desktop/inputdev/wm-syskeyup)       | Ruft den Code des virtuellen Schlüssels ab.                                                                                                                                                                                                                                                                                                               |



 

 

 