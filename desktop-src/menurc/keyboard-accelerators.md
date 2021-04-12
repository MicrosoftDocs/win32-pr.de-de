---
title: Tastaturkürzel
description: In diesem Abschnitt werden Tastaturbeschleuniger erläutert. Eine Tastenkombination ist eine Tastenkombination oder eine Kombination von Tastatureingaben, die eine Befehls Meldung für eine Anwendung generiert.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators.htm
keywords:
- Benutzereingabe, Tastaturbeschleuniger
- Erfassen von Benutzereingaben, Tastatur Accelerators
- Tastaturbeschleuniger
- Accelerators
- WM_COMMAND Meldung
- WM_SYS Befehls Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cd8cecd2fc1273750c75b8e5f33106d22343a14
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390283"
---
# <a name="keyboard-accelerators"></a>Tastaturkürzel

Eine *Tastatur* EINGABETASTE (oder einfach, Zugriffstaste) ist eine Tastenkombination oder eine Kombination von Tastatureingaben, mit der ein [**WM- \_ Befehl**](wm-command.md) oder eine [**WM- \_ syscommand**](wm-syscommand.md) -Nachricht für eine Anwendung generiert wird.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                                                 | BESCHREIBUNG                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Informationen zu Tastatur Accelerators](about-keyboard-accelerators.md)       | Erläutert Tastaturbeschleuniger.<br/>                                |
| [Verwenden von Tastatur Accelerators](using-keyboard-accelerators.md)       | Erläutert Aufgaben, die mit Tastatur Accelerators verknüpft sind.<br/> |
| [Referenz zur Tastatur Beschleunigung](keyboard-accelerator-reference.md) | Enthält die API-Referenz.<br/>                                     |



 

### <a name="keyboard-accelerator-functions"></a>Funktionen der Tastatur Beschleunigung



| Name                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Copyacceleratortable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea)       | Kopiert die angegebene Zugriffstasten Tabelle. Diese Funktion wird verwendet, um die Zugriffstasten Tabellendaten zu erhalten, die einem Zugriffstasten-Tabellen handle entsprechen, oder um die Größe der Datenzugriffs Tabellen-Daten zu ermitteln. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**"Kreateacceleratortable"**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)   | Erstellt eine Zugriffstasten Tabelle. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) | Zerstört eine Zugriffstasten Tabelle.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa)               | Lädt die angegebene Zugriffstasten Tabelle. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)       | Verarbeitet Zugriffstasten für Menübefehle. Die Funktion übersetzt eine [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -oder [**WM- \_ syskeydown**](/windows/desktop/inputdev/wm-syskeydown) -Nachricht in einen [**WM- \_ Befehl**](wm-command.md) oder eine [**WM- \_ syscommand**](wm-syscommand.md) -Nachricht (wenn ein Eintrag für den Schlüssel in der angegebenen Zugriffstasten Tabelle vorhanden ist) und sendet dann den **WM- \_ Befehl** oder die **WM- \_ syscommand** -Nachricht direkt an die angegebene Fenster Prozedur. [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) gibt erst zurück, wenn die Fenster Prozedur die Meldung verarbeitet hat. <br/> |



 

### <a name="keyboard-accelerator-messages"></a>Tastaturbeschleuniger-Meldungen



| Name                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ changeuistate**](wm-changeuistate.md) | Wird gesendet, um anzugeben, dass der Benutzeroberflächen Zustand geändert werden soll.<br/>                                                                                                                                                                                                                                                  |
| [**WM \_ InitMenu**](wm-initmenu.md)           | Wird gesendet, wenn ein Menü aktiv wird. Sie tritt auf, wenn der Benutzer auf ein Element in der Menüleiste klickt oder eine Menü Taste drückt. Dadurch kann die Anwendung das Menü ändern, bevor es angezeigt wird. <br/> Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion. <br/> |
| [**WM \_ queryuistate**](wm-queryuistate.md)   | Wird gesendet, um den Benutzeroberflächen Zustand für ein Fenster abzurufen.<br/>                                                                                                                                                                                                                                                            |
| [**WM \_ updateuistate**](wm-updateuistate.md) | Wird gesendet, um den Benutzeroberflächen Status für das angegebene Fenster und alle untergeordneten Fenster zu ändern.<br/>                                                                                                                                                                                                                        |



 

### <a name="keyboard-accelerator-notifications"></a>Benachrichtigungen über Tastaturbeschleuniger



| Name                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ initmenupopup**](wm-initmenupopup.md) | Wird gesendet, wenn ein Dropdown Menü oder ein Untermenü aktiv werden soll. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern. <br/>                                                                                                                                              |
| [**WM- \_ menuchar**](wm-menuchar.md)           | Wird gesendet, wenn ein Menü aktiv ist und der Benutzer eine Taste drückt, die keiner mnetmonischen oder Zugriffstaste entspricht. Diese Meldung wird an das Fenster gesendet, das das Menü besitzt. <br/>                                                                                                                                             |
| [**WM- \_ MenuSelect**](wm-menuselect.md)       | Wird an das Besitzer Fenster eines Menüs gesendet, wenn der Benutzer ein Menü Element auswählt. <br/>                                                                                                                                                                                                                                                      |
| [**WM- \_ syschar**](wm-syschar.md)             | Wird im Fenster mit dem Tastaturfokus gepostet, wenn eine [**WM- \_ syskeydown**](/windows/desktop/inputdev/wm-syskeydown) -Meldung von der [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion übersetzt wird. Er gibt den Zeichencode eines System Zeichen Schlüssels an, bei dem es sich um einen Zeichen Schlüssel handelt, der gedrückt wird, während die Alt-Taste gedrückt ist. <br/> |
| [**WM ( \_ syscommand)**](wm-syscommand.md)       | Ein Fenster empfängt diese Meldung, wenn der Benutzer einen Befehl im Menü **Fenster** auswählt oder wenn der Benutzer die Schaltfläche maximieren, die Schaltfläche Minimieren, die Schaltfläche Wiederherstellen oder die Schaltfläche Schließen auswählt.<br/>                                                                                                                                |



 

### <a name="keyboard-accelerator-structures"></a>Tastatur Zugriffstasten



| Name                   | BESCHREIBUNG                                                          |
|------------------------|----------------------------------------------------------------------|
| [**Acceleration**](/windows/win32/api/winuser/ns-winuser-accel) | Definiert eine Zugriffstaste, die in einer Zugriffstasten Tabelle verwendet wird. <br/> |



 

 

