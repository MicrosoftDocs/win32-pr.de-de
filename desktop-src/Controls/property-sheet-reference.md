---
title: -Eigenschaftenblatt
description: Dieser Abschnitt enthält Informationen zu Programmier Elementen, die mit Eigenschafts Blättern verwendet werden.
ms.assetid: f4fa9815-eab8-4b0b-ae5f-0bce4374223a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c42b7b4c1be7d0dc11613da36f78abbad847d6e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949137"
---
# <a name="property-sheet"></a>-Eigenschaftenblatt

Dieser Abschnitt enthält Informationen zu Programmier Elementen, die mit Eigenschafts Blättern verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                              | Inhalte                                                                                                                    |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Eigenschaften Blättern](property-sheets.md)       | Ein Eigenschaften *Blatt* ist ein Fenster, das es dem Benutzer ermöglicht, die Eigenschaften eines Elements anzuzeigen und zu bearbeiten.<br/>                  |
| [Erstellen von Assistenten](wizards.md)                    | Ein Assistent ist eine Art von Eigenschaften Blatt, das eine einfache und leistungsstarke Möglichkeit bietet, Benutzer durch eine Prozedur zu leiten.<br/> |
| [Verwenden von Eigenschaften Blättern](using-property-sheets.md) | Dieser Abschnitt enthält Implementierungsdetails und Beispielcode zum Arbeiten mit Eigenschaften Blättern.<br/>                     |



 

### <a name="functions"></a>Functions



| Thema                                                        | Inhalte                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Addpropsheetpageproc*](/windows/desktop/api/Prsht/nc-prsht-lpfnaddpropsheetpage)           | Gibt eine Anwendungs definierte Rückruffunktion an, die eine Eigenschaften Blatt Erweiterung zum Hinzufügen einer Seite zu einem Eigenschaften Blatt verwendet.<br/>                                                                                                                      |
| [**"Kreatepropertysheetpage"**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)   | Erstellt eine neue Seite für ein Eigenschaften Blatt.<br/>                                                                                                                                                                                                        |
| [**Destroypropertysheetpage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) | Zerstört eine Eigenschaften Blattseite. Eine Anwendung muss diese Funktion für Seitenaufrufen, die nicht an die [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) -Funktion übermittelt wurden.<br/>                                                                              |
| [**Eigenschaften Blatt**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)                       | Erstellt ein Eigenschaften Blatt und fügt die Seiten hinzu, die in der angegebenen Eigenschaften Blatt-Header Struktur definiert sind.<br/>                                                                                                                                           |
| [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)                 | Gibt eine Anwendungs definierte Rückruffunktion an, die von einem Eigenschaften Blatt aufgerufen wird, wenn eine Seite erstellt wird, und wenn es im Begriff ist, zerstört zu werden. Eine Anwendung kann diese Funktion verwenden, um Initialisierungs-und Bereinigungs Vorgänge für die Seite auszuführen.<br/> |
| [*Propsheetproc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback)                         | Eine von der Anwendung definierte Rückruffunktion, die vom System aufgerufen wird, wenn das Eigenschaften Blatt erstellt und initialisiert wird.<br/>                                                                                                                        |



 

### <a name="messages"></a>Meldungen



| Thema                                                               | Inhalte                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PSM \_ addPage**](psm-addpage.md)                                 | Fügt am Ende eines vorhandenen Eigenschaften Blatts eine neue Seite hinzu. Sie können diese Nachricht explizit oder mithilfe des [**propsheet- \_ addPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) -Makros senden.<br/>                                                                                                |
| [**PSM \_ anwenden**](psm-apply.md)                                     | Simuliert die Auswahl der Schaltfläche **anwenden** und gibt an, dass sich mindestens eine Seite geändert hat und die Änderungen überprüft und aufgezeichnet werden müssen.<br/>                                                                                                                   |
| [**PSM \_ cancelumclose**](psm-canceltoclose.md)                     | Wird von einer Anwendung gesendet, wenn Sie Änderungen seit der letzten Überprüfung von [PSN \_ ](psn-apply.md) -Benachrichtigungen durchgeführt hat, die nicht abgebrochen werden können. Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ canceldeclose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) -Makros senden.<br/> |
| [**PSM \_ geändert**](psm-changed.md)                                 | Teilt einem Eigenschaften Blatt mit, dass sich die Informationen in einer Seite geändert haben. Sie können diese Nachricht explizit oder mithilfe des von [**propsheet \_ geänderten**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) Makros senden.<br/>                                                                                         |
| [**PSM- \_ enablewizbuttons**](psm-enablewizbuttons.md)               | Aktiviert oder deaktiviert alle Standard Schaltflächen in einem Aero-Assistenten. Sie können diese Nachricht explizit senden oder das [**propsheet \_ enablewizbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) -Makro verwenden.<br/>                                                                          |
| [**PSM \_ getcurrentpagehwnd**](psm-getcurrentpagehwnd.md)           | Ruft ein Handle für das Fenster der aktuellen Seite eines Eigenschaften Blatts ab. Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ getcurrentpgehwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) -Makros senden.<br/>                                                          |
| [**PSM \_ GetResult**](psm-getresult.md)                             | Wird von nicht modalen Eigenschaften Blättern zum Abrufen der Informationen verwendet, die von [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)an modale Eigenschaften Blätter zurückgegeben werden. Sie können diese Nachricht explizit senden oder das [**propsheet \_ GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) -Makro verwenden.<br/>                 |
| [**PSM \_ gettabcontrol**](psm-gettabcontrol.md)                     | Ruft das Handle für das Registerkarten-Steuerelement eines Eigenschaften Blatts ab. Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ gettabcontrol**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) -Makros senden.<br/>                                                                                 |
| [**PSM \_ hwndumindex**](psm-hwndtoindex.md)                         | Nimmt das Fenster Handle der Eigenschaften Blattseite an und gibt dessen Null basierten Index zurück. Sie können diese Nachricht explizit senden oder das [**propsheet- \_ hwnddeindex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) -Makro verwenden.<br/>                                                                  |
| [**PSM \_ idumindex**](psm-idtoindex.md)                             | Übernimmt die Ressourcen-ID einer Eigenschaften Blattseite und gibt ihren Null basierten Index zurück. Sie können diese Nachricht explizit senden oder das [**propsheet- \_ iddeindex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) -Makro verwenden.<br/>                                                                          |
| [**PSM- \_ Indexverzeichnis**](psm-indextohwnd.md)                         | Nimmt den Index einer Eigenschaften Blattseite an und gibt das Fenster Handle zurück. Sie können diese Nachricht explizit senden oder das [**propsheet- \_ indexdehwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) -Makro verwenden.<br/>                                                                               |
| [**PSM- \_ indextoid**](psm-indextoid.md)                             | Nimmt den Index einer Eigenschaften Blattseite an und gibt die zugehörige Ressourcen-ID zurück. Sie können diese Nachricht explizit senden oder das [**propsheet- \_ indextoid**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) -Makro verwenden.<br/>                                                                                     |
| [**PSM- \_ indextopage**](psm-indextopage.md)                         | Nimmt den Index einer Eigenschaften Blattseite an und gibt das hpropsheetpage-Handle zurück. Sie können diese Nachricht explizit senden oder das [**propsheet \_ indextopage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) -Makro verwenden.<br/>                                                                       |
| [**PSM \_ insertpage**](psm-insertpage.md)                           | Fügt eine neue Seite in ein vorhandenes Eigenschaften Blatt ein. Die Seite kann entweder an einem angegebenen Index oder nach einer angegebenen Seite eingefügt werden. Sie können diese Nachricht explizit oder mithilfe des " [**propsheet \_ insertpage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) "-Makros senden.<br/>                |
| [**PSM \_ IsDialogMessage**](psm-isdialogmessage.md)                 | Übergibt eine Meldung an ein Eigenschaften Blatt und gibt an, ob das Dialogfeld die Nachricht verarbeitet hat. Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) -Makros senden.<br/>                              |
| [**PSM- \_ pageumindex**](psm-pagetoindex.md)                         | Nimmt das hpropsheetpage-Handle der Eigenschaften Blattseite an und gibt dessen Null basierten Index zurück. Sie können diese Nachricht explizit senden oder das " [**propsheet \_ Page$ Index**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) "-Makro verwenden.<br/>                                                          |
| [**PSM- \_ Drucktaste**](psm-pressbutton.md)                         | Simuliert die Auswahl einer Eigenschaften Blatt Schaltfläche. Sie können diese Nachricht explizit oder mithilfe des- [**propsheet- \_ pressbutton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) -Makros senden.<br/>                                                                                              |
| [**PSM- \_ querysiblings**](psm-querysiblings.md)                     | Wird an ein Eigenschaften Blatt gesendet, das die Nachricht dann an jede Ihrer Seiten weiterleitet. Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ querysiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) -Makros senden.<br/>                                                              |
| [**PSM- \_ rebootsystem**](psm-rebootsystem.md)                       | Gibt an, dass das System neu gestartet werden muss, damit die Änderungen wirksam werden. Sie können die [**PSM- \_ rebootsystem**](psm-rebootsystem.md) -Nachricht explizit oder mithilfe des [**propsheet \_ rebootsystem**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) -Makros senden.<br/>                        |
| [**PSM- \_ recalcpagesizes**](psm-recalcpagesizes.md)                 | Berechnet die Seitengröße eines Standard-oder Assistenten-Eigenschaften Blatts neu, nachdem Seiten hinzugefügt oder entfernt wurden. Sie können diese Nachricht explizit senden oder das [**propsheet \_ recalcpagesizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) -Makro verwenden.<br/>                                     |
| [**PSM- \_ RemovePage**](psm-removepage.md)                           | Entfernt eine Seite aus einem Eigenschaftenblatt. Sie können diese Nachricht explizit oder mithilfe des [**propsheet- \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) -Makros senden.<br/>                                                                                                              |
| [**PSM- \_ restartfenster**](psm-restartwindows.md)                   | Gibt an, dass Windows neu gestartet werden muss, damit die Änderungen wirksam werden.<br/>                                                                                                                                                                                         |
| [**PSM \_ SetButtonText**](psm-setbuttontext.md)                     | Legt den Text auf einer Schaltfläche in einem Aero-Assistenten fest. Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) senden.<br/>                                                                                                 |
| [**PSM \_ setcurrsel**](psm-setcursel.md)                             | Aktiviert die angegebene Seite in einem Eigenschaften Blatt. Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ setcurrsel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) senden.<br/>                                                                                                    |
| [**PSM \_ setcurrselid**](psm-setcurselid.md)                         | Aktiviert die angegebene Seite in einem Eigenschaften Blatt basierend auf dem Ressourcen Bezeichner der Seite. Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ setcurrselbyid**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) senden.<br/>                                                   |
| [**PSM \_ setfinishtext**](psm-setfinishtext.md)                     | Legt den Text der Schaltfläche **Fertig** stellen in einem Assistenten fest, zeigt die Schaltfläche an und aktiviert Sie und blendet die Schaltflächen **weiter** und **zurück** aus. Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ setfinishtext**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) senden.<br/>               |
| [**PSM-Einstellungs \_ Bitmap**](psm-setheaderbitmap.md)                 | Diese Meldung ist nicht implementiert.<br/>                                                                                                                                                                                                                                     |
| [**PSM-Einstellungs \_ bitmapresource**](psm-setheaderbitmapresource.md) | Diese Meldung ist nicht implementiert.<br/>                                                                                                                                                                                                                                     |
| [**PSM- \_ abadertitel**](psm-setheadersubtitle.md)             | Legt den Untertitel Text für den Header der inneren Seite eines Assistenten fest. Sie können diese Nachricht explizit senden oder das [**propsheet-unter \_ Titel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) -Makro verwenden.<br/>                                                                        |
| [**PSM-Einstellungs \_ Titel**](psm-setheadertitle.md)                   | Legt den Titeltext für den Header der inneren Seite eines Assistenten fest. Sie können diese Nachricht explizit senden oder das [**propsheet- \_**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) ".<br/>                                                                                 |
| [**PSM \_ setnexttext**](psm-setnexttext.md)                         | Legt den Text der Schaltfläche **weiter** in einem Assistenten fest. Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ setnexttext**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) senden.<br/>                                                                                                |
| [**PSM- \_ SetTitle**](psm-settitle.md)                               | Legt den Titel eines Eigenschaften Blatts fest. Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) senden.<br/>                                                                                                                    |
| [**PSM-Einstellungs Schaltflächen \_**](psm-setwizbuttons.md)                     | Aktiviert oder deaktiviert die Schaltflächen " **zurück**", " **weiter**" und " **Fertig** stellen" in einem Assistenten. Sie können die Nachricht auch mit dem propsheet-Makro für das ""- [**\_ /twizbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) -Makro veröffentlichen.<br/>                                                                          |
| [**PSM- \_ showwizbuttons**](psm-showwizbuttons.md)                   | Blendet Schaltflächen in einem Assistenten ein oder aus. Sie können diese Nachricht explizit oder mithilfe des [**propsheet- \_ showwitzbuttons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) -Makros senden.<br/>                                                                                                        |
| [**PSM \_ unverändert**](psm-unchanged.md)                             | Teilt einem Eigenschaften Blatt mit, dass die Informationen in einer Seite in den zuvor gespeicherten Zustand zurückversetzt wurden. Sie können diese Nachricht explizit oder mithilfe des [**\_ unveränderten propsheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) -Makros senden.<br/>                                                      |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                     | Inhalte                                                                                                                                                                                                                                                |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PSN- \_ Anwendung](psn-apply.md)                               | Wird an jede Seite im Eigenschaften Blatt gesendet, um anzugeben, dass der Benutzer auf die Schaltfläche "OK", "Schließen" oder "übernehmen" geklickt hat und alle Änderungen wirksam werden sollen. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)<br/>      |
| [PSN- \_ GetObject](psn-getobject.md)                       | Wird von einem Eigenschaften Blatt gesendet, um ein Ablage Zielobjekt anzufordern, wenn der Cursor über eine der Schaltflächen des Registerkarten-Steuer Elements weitergeleitet wird.<br/>                                                                                                                       |
| [\_Hilfe zu PSN](psn-help.md)                                 | Benachrichtigt eine Seite, dass der Benutzer auf die Schaltfläche "Hilfe" geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                          |
| [PSN- \_ killactive](psn-killactive.md)                     | Benachrichtigt eine Seite, dass Sie im Begriff ist, die Aktivierung zu verlieren, weil eine andere Seite aktiviert oder der Benutzer auf die Schaltfläche " **OK** " geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>       |
| [PSN \_ querycancel](psn-querycancel.md)                   | Gibt an, dass der Benutzer das Eigenschaften Blatt abgebrochen hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                            |
| [PSN \_ queryinitialfocus](psn-queryinitialfocus.md)       | Wird von einem Eigenschaften Blatt gesendet, um der Seite eines Eigenschaften Blatts anzugeben, welches Dialogfeld-Steuerelement den Anfangs Fokus erhalten soll. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)<br/>           |
| [PSN- \_ zurück Setzung](psn-reset.md)                               | Benachrichtigt eine Seite, dass das Eigenschaften Blatt zerstört werden soll. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                   |
| [PSN- \_ SETACTIVE](psn-setactive.md)                       | Benachrichtigt eine Seite, dass Sie im Begriff ist, aktiviert zu werden. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                                                   |
| [PSN \_ TranslateAccelerator](psn-translateaccelerator.md) | Benachrichtigt ein Eigenschaften Blatt, dass eine Tastatur Meldung empfangen wurde. Die Seite bietet die Möglichkeit, eine private Tastatur Zugriffstaste zu übersetzen. Diese Benachrichtigung wird in Form einer WM-Benachrichtigungs Meldung gesendet. [**\_**](wm-notify.md)<br/> |
| [PSN- \_ witzback](psn-wizback.md)                           | Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die Schaltfläche " **zurück** " geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                          |
| [PSN- \_ witzschluss](psn-wizfinish.md)                       | Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die Schaltfläche **Fertig** stellen geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                        |
| [PSN- \_ nächstes](psn-wiznext.md)                           | Benachrichtigt eine Seite, dass der Benutzer auf die Schaltfläche **weiter** in einem Assistenten geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.<br/>                                                                          |



 

### <a name="structures"></a>Strukturen



| Thema                                      | Inhalte                                                                   |
|--------------------------------------------|----------------------------------------------------------------------------|
| [**Propsheetheiader**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) | Definiert den Frame und die Seiten eines Eigenschaften Blatts.<br/>                |
| [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2)     | Definiert eine Seite in einem Eigenschaften Blatt.<br/>                             |
| [**Pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)             | Enthält Informationen für die Eigenschaften Blatt-Benachrichtigungs Codes.<br/> |



 

 

