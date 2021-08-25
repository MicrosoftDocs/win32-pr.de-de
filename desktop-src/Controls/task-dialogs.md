---
title: Aufgabendialogfeld
description: Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit einem Aufgabendialogfeld verwendet werden. Ein Aufgabendialogfeld ähnelt einem einfachen Meldungsfeld, ist jedoch viel flexibler als ein einfaches Meldungsfeld.
ms.assetid: vs|controls|~\controls\taskdialogs\taskdialogs.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6797314b75fff46ddf8a4f64638fefb5ea0181d2353bd1a1d3caa57325d28e7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168550"
---
# <a name="task-dialog"></a>Aufgabendialogfeld

Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit einem Aufgabendialogfeld verwendet werden. Ein *Aufgabendialogfeld* ähnelt einem einfachen Meldungsfeld, ist jedoch viel flexibler als ein einfaches Meldungsfeld.

### <a name="overviews"></a>Übersichten



| Thema                                           | Inhalte                                            |
|-------------------------------------------------|-----------------------------------------------------|
| [Informationen zu Taskdialogfeldern](task-dialogs-overview.md) | Beschreibt die Elemente eines Aufgabendialogfelds.<br/> |



 

### <a name="functions"></a>Functions



| Thema                                                  | Inhalte                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog)                       | Erstellt, zeigt ein Aufgabendialogfeld an und führt es aus. Das Aufgabendialogfeld enthält anwendungsdefinierten Meldungstext und -titel, Symbole und eine beliebige Kombination vordefinierter Pushschaltflächen. Diese Funktion unterstützt nicht die Registrierung einer Rückruffunktion zum Empfangen von Benachrichtigungen.<br/>                                                                                                                |
| [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) | Eine anwendungsdefinierte Funktion, die mit der [**TaskDialogIndirect-Funktion verwendet**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) wird. Sie empfängt Nachrichten aus dem Aufgabendialogfeld, wenn verschiedene Ereignisse auftreten.<br/> Der **PFTASKDIALOGCALLBACK-Typ** definiert einen Zeiger auf diese Rückruffunktion. [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) ist ein Platzhalter für den anwendungsdefinierten Funktionsnamen.<br/> |
| [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)       | Erstellt, zeigt ein Aufgabendialogfeld an und führt es aus. Das Aufgabendialogfeld enthält anwendungsdefinierte Symbole, Meldungen, Titel, Überprüfungskontrollkästchen, Befehlslinks, Pushschaltflächen und Optionsfelder. Diese Funktion kann eine Rückruffunktion registrieren, um Benachrichtigungsmeldungen zu empfangen.<br/>                                                                                                               |



 

### <a name="messages"></a>Nachrichten



| Thema                                                                                           | Inhalte                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_TDM-KLICKSCHALTFLÄCHE \_**](tdm-click-button.md)                                                  | Simuliert die Aktion eines Schaltflächenklicks in einem Aufgabendialogfeld.<br/>                                                                                                                                  |
| [**OPTIONSFELD "TDM \_ \_ \_ KLICKEN"**](tdm-click-radio-button.md)                                     | Simuliert die Aktion eines Optionsfeldklicks in einem Aufgabendialogfeld.<br/>                                                                                                                            |
| [**TDM KLICK \_ AUF \_ ÜBERPRÜFUNG**](tdm-click-verification.md)                                      | Simuliert die Aktion eines Überprüfungskontrollkästchens, indem in einem Aufgabendialogfeld geklickt wird.<br/>                                                                                                                   |
| [**TDM-SCHALTFLÄCHE \_ \_ "AKTIVIEREN"**](tdm-enable-button.md)                                                | Aktiviert oder deaktiviert eine Pushschaltfläche in einem Aufgabendialogfeld.<br/>                                                                                                                                       |
| [**OPTIONSFELD "TDM \_ \_ \_ AKTIVIEREN"**](tdm-enable-radio-button.md)                                   | Aktiviert oder deaktiviert ein Optionsfeld in einem Aufgabendialogfeld.<br/>                                                                                                                                      |
| [**TDM \_ NAVIGATE \_ PAGE**](tdm-navigate-page.md)                                                | Erstellt ein Aufgabendialogfeld mit neuen Inhalten neu und simuliert die Funktionalität eines mehrseitigen Assistenten.<br/>                                                                                           |
| [**TDM \_ SET \_ BUTTON \_ ELEVATION \_ REQUIRED \_ STATE**](tdm-set-button-elevation-required-state.md) | Gibt an, ob ein bestimmtes Aufgabendialogfeld oder ein Befehlslink ein Schildsymbol für die Benutzerkontensteuerung (User Account Control, UAC) haben soll. Das heißt, ob für die von der Schaltfläche aufgerufene Aktion eine Erhöhung erforderlich ist. <br/> |
| [**TDM \_ SET \_ ELEMENT \_ TEXT**](tdm-set-element-text.md)                                         | Aktualisiert ein Textelement in einem Aufgabendialogfeld.<br/>                                                                                                                                                  |
| [**TDM \_ SET \_ MARQUEE \_ PROGRESS \_ BAR**](tdm-set-marquee-progress-bar.md)                        | Gibt an, ob die gehostete Statusanzeige im Festzeltmodus angezeigt werden soll.<br/>                                                                                                            |
| [**TDM \_ SET \_ PROGRESS \_ BAR \_ MARQUEE**](tdm-set-progress-bar-marquee.md)                        | Startet und beendet die Anzeige der Statusanzeige im Festzelt und legt die Geschwindigkeit des Festzelt fest.<br/>                                                                                              |
| [**TDM \_ SET \_ PROGRESS \_ BAR \_ POS**](tdm-set-progress-bar-pos.md)                                | Legt die aktuelle Position für eine Statusleiste fest.<br/>                                                                                                                                             |
| [**TDM– \_ \_ STATUSLEISTENBEREICH \_ \_ FESTLEGEN**](tdm-set-progress-bar-range.md)                            | Legt die minimalen und maximalen Werte für die gehostete Statusleiste fest.<br/>                                                                                                                          |
| [**STATUS DER \_ \_ TDM-STATUSLEISTE \_ \_ FESTLEGEN**](tdm-set-progress-bar-state.md)                            | Legt den aktuellen Status der Statusleiste fest.<br/>                                                                                                                                               |
| [**TDM \_ UPDATE \_ ELEMENT \_ TEXT**](tdm-update-element-text.md)                                   | Aktualisiert ein Textelement in einem Aufgabendialogfeld. <br/>                                                                                                                                                 |
| [**\_TDM-UPDATESYMBOL \_**](tdm-update-icon.md)                                                    | Aktualisiert das Symbol eines Aufgabendialogfelds. <br/>                                                                                                                                                     |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                           | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AUF DIE SCHALTFLÄCHE "TDN" \_ \_ GEKLICKT](tdn-button-clicked.md)                  | Wird von einem Aufgabendialogfeld gesendet, wenn der Benutzer eine Schaltfläche oder einen Befehlslink im Aufgabendialogfeld auswählt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode registriert werden**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) kann.<br/>                                                                                                                                                                                                   |
| [TDN \_ CREATED](tdn-created.md)                                 | Wird von einem Aufgabendialogfeld gesendet, nachdem das Aufgabendialogfeld erstellt wurde und bevor es angezeigt wird. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode registriert werden**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) kann. <br/>                                                                                                                                                                                                  |
| [TDN \_ ZERSTÖRT](tdn-destroyed.md)                             | Wird von einem Aufgabendialogfeld gesendet, wenn es zerstört wird und sein Fensterhandpunkt nicht mehr gültig ist. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode registriert werden**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) kann.<br/>                                                                                                                                                                                                       |
| [\_TDN-DIALOGFELD \_ ERSTELLT](tdn-dialog-constructed.md)          | Wird von einem Aufgabendialogfeld gesendet, nachdem das Aufgabendialogfeld erstellt wurde und bevor es angezeigt wird. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode registriert werden**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) kann. <br/>                                                                                                                                                                                                  |
| [AUF DIE SCHALTFLÄCHE "TDN \_ \_ EXPANDO" \_ GEKLICKT](tdn-expando-button-clicked.md) | Wird von einem Aufgabendialogfeld gesendet, wenn der Benutzer auf die Expando-Schaltfläche des Aufgabendialogfelds klickt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode registriert werden**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) kann.<br/>                                                                                                                                                                                                            |
| [TDN-HILFE \_](tdn-help.md)                                       | Wird von einem Aufgabendialogfeld gesendet, wenn der Benutzer F1 auf der Tastatur drückt, während das Aufgabendialogfeld den Fokus besitzt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode registriert werden**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) kann.<br/>                                                                                                                                                                                            |
| [TDN-LINK \_ \_ GEKLICKT](tdn-hyperlink-clicked.md)            | Wird von einem Aufgabendialogfeld gesendet, wenn der Benutzer auf einen Link im Inhalt des Aufgabendialogfelds klickt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode registriert werden**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) kann. <br/>                                                                                                                                                                                                        |
| [TDN \_ NAVIGATED](tdn-navigated.md)                             | Wird von einem Aufgabendialogfeld gesendet, wenn eine Navigation erfolgt ist. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode registriert werden**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) kann. <br/>                                                                                                                                                                                                                                     |
| [OPTIONSFELD "TDN" \_ \_ \_ GEKLICKT](tdn-radio-button-clicked.md)     | Wird von einem Aufgabendialogfeld gesendet, wenn der Benutzer eine Schaltfläche oder einen Befehlslink im Aufgabendialogfeld auswählt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode registriert werden**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) kann. <br/>                                                                                                                                                                                                  |
| [\_TDN-TIMER](tdn-timer.md)                                     | Wird von einem Aufgabendialogfeld ungefähr alle 200 Millisekunden gesendet. Dieser Benachrichtigungscode wird gesendet, wenn das TDF \_ CALLBACK \_ TIMER-Flag im **dwFlags-Member** der [**TASKDIALOGCONFIG-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) festgelegt wurde, der an die [**TaskDialogIndirect-Funktion übergeben**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) wurde. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der **TaskDialogIndirect-Methode registriert werden** kann.<br/> |
| [AUF \_ TDN-ÜBERPRÜFUNG \_ GEKLICKT](tdn-verification-clicked.md)      | Wird vom Aufgabendialogfeld gesendet, wenn der Benutzer auf das Kontrollkästchen Überprüfung des Aufgabendialogfelds klickt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode registriert werden**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) kann.<br/>                                                                                                                                                                                                       |



 

### <a name="structures"></a>Strukturen



| Thema                                           | Inhalte                                                                                                                                                   |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCHALTFLÄCHE \_ "TASKDIALOG"**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialog_button) | Enthält Informationen zum Anzeigen einer Schaltfläche in einem Aufgabendialogfeld. Die [**TASKDIALOGCONFIG-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) verwendet diese Struktur.<br/> |
| [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)    | Enthält Informationen zum Anzeigen eines Aufgabendialogfelds. Die [**TaskDialogIndirect-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) verwendet diese Struktur.<br/>          |



 

 

