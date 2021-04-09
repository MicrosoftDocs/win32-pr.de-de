---
title: Aufgaben Dialogfeld
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit einem Aufgaben Dialogfeld verwendet werden. Ein Aufgaben Dialogfeld ähnelt, aber viel flexibler als ein einfaches Meldungs Feld.
ms.assetid: vs|controls|~\controls\taskdialogs\taskdialogs.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f115531b9f872c824e9d1822be07777b2bc439
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2020
ms.locfileid: "103858548"
---
# <a name="task-dialog"></a>Aufgaben Dialogfeld

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit einem Aufgaben Dialogfeld verwendet werden. Ein *Aufgaben Dialogfeld* ähnelt, aber viel flexibler als ein einfaches Meldungs Feld.

### <a name="overviews"></a>Übersichten



| Thema                                           | Inhalte                                            |
|-------------------------------------------------|-----------------------------------------------------|
| [Informationen über Aufgaben Dialoge](task-dialogs-overview.md) | Beschreibt die Elemente eines Aufgaben Dialogfelds.<br/> |



 

### <a name="functions"></a>Functions



| Thema                                                  | Inhalte                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nenne**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog)                       | Erstellt ein Aufgaben Dialogfeld, zeigt es an und führt es aus. Das Aufgaben Dialogfeld enthält Anwendungs definierten Meldungs Text und Titel, Symbole und eine beliebige Kombination von vordefinierten Push-Schaltflächen. Diese Funktion unterstützt nicht die Registrierung einer Rückruffunktion, um Benachrichtigungen zu empfangen.<br/>                                                                                                                |
| [*Taskdialogcallbackproc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) | Eine Anwendungs definierte Funktion, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Funktion verwendet wird. Er empfängt Nachrichten aus dem Aufgaben Dialogfeld, wenn verschiedene Ereignisse auftreten.<br/> Der **pftaskdialogcallback** -Typ definiert einen Zeiger auf diese Rückruffunktion. [*Taskdialogcallbackproc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.<br/> |
| [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)       | Erstellt ein Aufgaben Dialogfeld, zeigt es an und führt es aus. Das Aufgaben Dialogfeld enthält Anwendungs definierte Symbole, Meldungen, Titel, Überprüfung, Kontrollkästchen, Befehls Verknüpfungen, Schaltflächen und Options Felder. Diese Funktion kann eine Rückruffunktion registrieren, um Benachrichtigungs Meldungen zu empfangen.<br/>                                                                                                               |



 

### <a name="messages"></a>Meldungen



| Thema                                                                                           | Inhalte                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TDM- \_ Click- \_ Schaltfläche**](tdm-click-button.md)                                                  | Simuliert die Aktion eines Schaltflächen-Click in einem Aufgaben Dialogfeld.<br/>                                                                                                                                  |
| [**Optionsfeld "TDM \_ Click" \_ \_**](tdm-click-radio-button.md)                                     | Simuliert die Aktion eines Options Felds in einem Aufgaben Dialogfeld.<br/>                                                                                                                            |
| [**TDM- \_ Klick \_ Überprüfung**](tdm-click-verification.md)                                      | Simuliert die Aktion eines Überprüfungs Kontrollkästchens in einem Aufgaben Dialogfeld.<br/>                                                                                                                   |
| [**\_Schaltfläche zum Aktivieren von TDM \_**](tdm-enable-button.md)                                                | Aktiviert oder deaktiviert eine Schaltfläche "Push" in einem Aufgaben Dialogfeld.<br/>                                                                                                                                       |
| [**Optionsfeld zum Aktivieren von TDM \_ \_ \_**](tdm-enable-radio-button.md)                                   | Aktiviert oder deaktiviert ein Optionsfeld in einem Aufgaben Dialogfeld.<br/>                                                                                                                                      |
| [**TDM- \_ Navigations \_ Seite**](tdm-navigate-page.md)                                                | Erstellt ein Aufgaben Dialogfeld mit neuen Inhalten neu und simuliert die Funktionalität eines Assistenten für mehrere Seiten.<br/>                                                                                           |
| [**Status der TDM- \_ Schaltflächen Erweiterung \_ \_ \_ erforderlich \_**](tdm-set-button-elevation-required-state.md) | Gibt an, ob eine angegebene Aufgaben Dialogfeld-oder Befehls Verknüpfung über ein Schild Symbol der Benutzerkontensteuerung (UAC) verfügen soll. Das heißt, ob für die von der Schaltfläche aufgerufene Aktion eine Erhöhung erforderlich ist. <br/> |
| [**TDM \_ - \_ Element \_ Text festlegen**](tdm-set-element-text.md)                                         | Aktualisiert ein Textelement in einem Aufgaben Dialogfeld.<br/>                                                                                                                                                  |
| [**TDM \_ Set \_ Marquee \_ Progress \_ Bar**](tdm-set-marquee-progress-bar.md)                        | Gibt an, ob die gehostete Statusanzeige im Marquee-Modus angezeigt werden soll.<br/>                                                                                                            |
| [**TDM-Statusanzeige- \_ \_ \_ \_ Marquee festlegen**](tdm-set-progress-bar-marquee.md)                        | Startet und beendet die Marquee-Anzeige der Statusanzeige und legt die Geschwindigkeit des Marquee fest.<br/>                                                                                              |
| [**TDM-Statusanzeige- \_ \_ \_ \_ POS festlegen**](tdm-set-progress-bar-pos.md)                                | Legt die aktuelle Position für eine Statusanzeige fest.<br/>                                                                                                                                             |
| [**TDM \_ - \_ \_ Statusanzeige \_ Bereich festlegen**](tdm-set-progress-bar-range.md)                            | Legt die minimalen und maximalen Werte für die gehostete Statusanzeige fest.<br/>                                                                                                                          |
| [**Statusanzeige \_ \_ \_ \_ Status in TDM festlegen**](tdm-set-progress-bar-state.md)                            | Legt den aktuellen Status der Statusanzeige fest.<br/>                                                                                                                                               |
| [**TDM- \_ Aktualisierungs \_ Element \_ Text**](tdm-update-element-text.md)                                   | Aktualisiert ein Textelement in einem Aufgaben Dialogfeld. <br/>                                                                                                                                                 |
| [**Symbol für TDM- \_ Update \_**](tdm-update-icon.md)                                                    | Aktualisiert das Symbol eines Aufgaben Dialogfelds. <br/>                                                                                                                                                     |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                           | Inhalte                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TDN- \_ Schaltfläche \_ geklickt](tdn-button-clicked.md)                  | Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer eine Schaltfläche oder einen Befehls Link im Aufgaben Dialogfeld auswählt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.<br/>                                                                                                                                                                                                   |
| [TDN \_ erstellt](tdn-created.md)                                 | Wird von einem Aufgaben Dialogfeld gesendet, nachdem das Aufgaben Dialogfeld erstellt wurde und bevor es angezeigt wird. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann. <br/>                                                                                                                                                                                                  |
| [TDN \_ zerstört](tdn-destroyed.md)                             | Wird von einem Aufgaben Dialogfeld gesendet, wenn es zerstört wird und sein Fenster Handle nicht mehr gültig ist. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.<br/>                                                                                                                                                                                                       |
| [TDN- \_ Dialog \_ erstellt](tdn-dialog-constructed.md)          | Wird von einem Aufgaben Dialogfeld gesendet, nachdem das Aufgaben Dialogfeld erstellt wurde und bevor es angezeigt wird. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann. <br/>                                                                                                                                                                                                  |
| [auf TDN- \_ expando- \_ Schaltfläche \_ geklickt](tdn-expando-button-clicked.md) | Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer auf die Schaltfläche "expando" des Aufgaben Dialogs klickt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.<br/>                                                                                                                                                                                                            |
| [TDN- \_ Hilfe](tdn-help.md)                                       | Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer F1 auf der Tastatur drückt, während das Aufgaben Dialogfeld den Fokus besitzt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.<br/>                                                                                                                                                                                            |
| [TDN- \_ Link \_ geklickt](tdn-hyperlink-clicked.md)            | Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer auf einen Link im Inhalt des Aufgaben Dialogfelds klickt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann. <br/>                                                                                                                                                                                                        |
| [TDN \_ navigiert](tdn-navigated.md)                             | Wird von einem Aufgaben Dialogfeld gesendet, wenn eine Navigation aufgetreten ist. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann. <br/>                                                                                                                                                                                                                                     |
| [Schaltfläche "TDN" \_ \_ \_ geklickt](tdn-radio-button-clicked.md)     | Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer eine Schaltfläche oder einen Befehls Link im Aufgaben Dialogfeld auswählt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann. <br/>                                                                                                                                                                                                  |
| [TDN- \_ Timer](tdn-timer.md)                                     | Wird von einem Aufgaben Dialogfeld ungefähr alle 200 Millisekunden gesendet. Dieser Benachrichtigungs Code wird gesendet, wenn das TDF- \_ Rückruf- \_ Timer-Flag im **dwFlags** -Member der [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur festgelegt wurde, die an die [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Funktion übergeben wurde. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der **TaskDialogIndirect** -Methode registriert werden kann.<br/> |
| [TDN-über \_ Prüfung \_ geklickt](tdn-verification-clicked.md)      | Wird durch das Aufgaben Dialogfeld gesendet, wenn der Benutzer auf das Kontrollkästchen Aufgaben Dialogfeld Überprüfung klickt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.<br/>                                                                                                                                                                                                       |



 

### <a name="structures"></a>Strukturen



| Thema                                           | Inhalte                                                                                                                                                   |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**taskdialog- \_ Schaltfläche**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialog_button) | Enthält Informationen, die zum Anzeigen einer Schaltfläche in einem Aufgaben Dialogfeld verwendet werden. Die [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur verwendet diese-Struktur.<br/> |
| [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)    | Enthält Informationen, die zum Anzeigen eines Aufgaben Dialogfelds verwendet werden. Die [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Funktion verwendet diese-Struktur.<br/>          |



 

 

