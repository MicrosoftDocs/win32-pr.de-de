---
title: Tastaturkürzel
description: In diesem Abschnitt werden Tastenkombinationen erläutert. Eine Tastaturbeschleunigung ist eine Tastatureingabe oder eine Kombination von Tastatureingaben, die eine Befehlsmeldung für eine Anwendung generiert.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators.htm
keywords:
- Benutzereingabe, Zugriffstasten
- Erfassen von Benutzereingaben, Tastaturbeschleunigungen
- Tastenkombinationen
- Beschleuniger
- WM_COMMAND Meldung
- WM_SYS COMMAND-Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df67f4879edc2e0e81a8715155bf2edfac05f1e5ce9d3557f9b051ae682a6afa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734468"
---
# <a name="keyboard-accelerators"></a>Tastaturkürzel

Eine *Tastaturbeschleunigung* (oder einfach eine Zugriffstaste) ist eine Tastatureingabe oder eine Kombination von Tastatureingaben, die eine [**WM \_ COMMAND-**](wm-command.md) oder [**WM \_ SYSCOMMAND-Nachricht**](wm-syscommand.md) für eine Anwendung generiert.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                                                 | Beschreibung                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Informationen zu Tastaturbeschleunigungen](about-keyboard-accelerators.md)       | Erläutert Tastenkombinationen.<br/>                                |
| [Verwenden von Tastenkombinationen](using-keyboard-accelerators.md)       | Erläutert Aufgaben, die Tastenkombinationen zugeordnet sind.<br/> |
| [Referenz zur Tastaturbeschleunigung](keyboard-accelerator-reference.md) | Enthält den API-Verweis.<br/>                                     |



 

### <a name="keyboard-accelerator-functions"></a>Tastaturbeschleunigungsfunktionen



| Name                                                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea)       | Kopiert die angegebene Zugriffstastentabelle. Diese Funktion wird verwendet, um die Acceleratortabellendaten abzurufen, die einem Accelerator-Tabellenhandle entsprechen, oder um die Größe der Acceleratortabellendaten zu bestimmen. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)   | Erstellt eine Zugriffstastentabelle. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) | Zerstört eine Zugriffstastentabelle.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa)               | Lädt die angegebene Zugriffstastentabelle. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**Translateaccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)       | Verarbeitet Zugriffstasten für Menübefehle. Die Funktion übersetzt eine [**WM \_ KEYDOWN-**](/windows/desktop/inputdev/wm-keydown) oder [**WM \_ SYSKEYDOWN-Nachricht**](/windows/desktop/inputdev/wm-syskeydown) in eine [**WM \_ COMMAND-**](wm-command.md) oder [**WM \_ SYSCOMMAND-Nachricht**](wm-syscommand.md) (wenn ein Eintrag für den Schlüssel in der angegebenen Zugriffstastentabelle vorhanden ist) und sendet dann die **WM \_ COMMAND-** oder **WM \_ SYSCOMMAND-Nachricht** direkt an die angegebene Fensterprozedur. [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) gibt erst dann zurück, wenn die Fensterprozedur die Nachricht verarbeitet hat. <br/> |



 

### <a name="keyboard-accelerator-messages"></a>Tastaturbeschleunigungsmeldungen



| Name                                          | Beschreibung                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) | Wird gesendet, um anzugeben, dass der Benutzeroberflächenzustand geändert werden soll.<br/>                                                                                                                                                                                                                                                  |
| [**WM \_ INITMENU**](wm-initmenu.md)           | Wird gesendet, wenn ein Menü aktiv wird. Er tritt auf, wenn der Benutzer auf ein Element in der Menüleiste klickt oder eine Menütaste drückt. Dadurch kann die Anwendung das Menü ändern, bevor es angezeigt wird. <br/> Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) <br/> |
| [**WM \_ QUERYUISTATE**](wm-queryuistate.md)   | Wird gesendet, um den Benutzeroberflächenzustand für ein Fenster abzurufen.<br/>                                                                                                                                                                                                                                                            |
| [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) | Wird gesendet, um den Benutzeroberflächenzustand für das angegebene Fenster und alle untergeordneten Fenster zu ändern.<br/>                                                                                                                                                                                                                        |



 

### <a name="keyboard-accelerator-notifications"></a>Tastaturbeschleunigungsbenachrichtigungen



| Name                                          | Beschreibung                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) | Wird gesendet, wenn ein Dropdownmenü oder Untermenü aktiv wird. Dadurch kann eine Anwendung das Menü ändern, bevor es angezeigt wird, ohne das gesamte Menü zu ändern. <br/>                                                                                                                                              |
| [**WM \_ MENUCHAR**](wm-menuchar.md)           | Wird gesendet, wenn ein Menü aktiv ist und der Benutzer eine Taste drückt, die keiner mnemonic- oder accelerator-Taste entspricht. Diese Meldung wird an das Fenster gesendet, das das Menü besitzt. <br/>                                                                                                                                             |
| [**\_WM-MENÜAUSWAHL**](wm-menuselect.md)       | Wird an das Besitzerfenster eines Menüs gesendet, wenn der Benutzer ein Menüelement auswählt. <br/>                                                                                                                                                                                                                                                      |
| [**WM \_ SYSCHAR**](wm-syschar.md)             | Wird mit dem Tastaturfokus an das Fenster gesendet, wenn eine [**\_ WM-SYSKEYDOWN-Nachricht**](/windows/desktop/inputdev/wm-syskeydown) von der [**TranslateMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-translatemessage) übersetzt wird. Sie gibt den Zeichencode einer Systemzeichentaste an, d. h. eine Zeichentaste, die gedrückt wird, während die ALT-Taste gedrückt ist. <br/> |
| [**WM \_ SYSCOMMAND**](wm-syscommand.md)       | Ein Fenster empfängt diese Meldung, wenn der Benutzer im Menü **Fenster** einen Befehl ausgibt oder wenn der Benutzer die Schaltfläche "Maximieren", "Minimieren", "Wiederherstellen" oder "Schließen" ausgibt.<br/>                                                                                                                                |



 

### <a name="keyboard-accelerator-structures"></a>Tastaturbeschleunigungsstrukturen



| Name                   | Beschreibung                                                          |
|------------------------|----------------------------------------------------------------------|
| [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) | Definiert einen Zugriffstastenschlüssel, der in einer Zugriffstastentabelle verwendet wird. <br/> |



 

 

