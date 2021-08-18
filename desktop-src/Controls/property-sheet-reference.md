---
title: -Eigenschaftenblatt
description: Dieser Abschnitt enthält Informationen zu Programmierelementen, die mit Eigenschaftenblättern verwendet werden.
ms.assetid: f4fa9815-eab8-4b0b-ae5f-0bce4374223a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50661ece6985c16f299b514fa59068bf06f115b49c0f0bbea783cf637c2c921
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826030"
---
# <a name="property-sheet"></a>-Eigenschaftenblatt

Dieser Abschnitt enthält Informationen zu Programmierelementen, die mit Eigenschaftenblättern verwendet werden.

### <a name="overviews"></a>Übersichten



| Thema                                              | Inhalte                                                                                                                    |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Informationen über Eigenschaftenblätter](property-sheets.md)       | Ein *Eigenschaftenblatt ist* ein Fenster, in dem der Benutzer die Eigenschaften eines Elements anzeigen und bearbeiten kann.<br/>                  |
| [Erstellen von Assistenten](wizards.md)                    | Ein Assistent ist ein Eigenschaftenblatttyp, der eine einfache und leistungsstarke Möglichkeit bietet, Benutzer durch eine Prozedur zu führen.<br/> |
| [Verwenden von Eigenschaftenblättern](using-property-sheets.md) | Dieser Abschnitt enthält Implementierungsdetails und Beispielcode für die Arbeit mit Eigenschaftenblättern.<br/>                     |



 

### <a name="functions"></a>Funktionen



| Thema                                                        | Inhalte                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*AddPropSheetPageProc*](/windows/desktop/api/Prsht/nc-prsht-lpfnaddpropsheetpage)           | Gibt eine anwendungsdefinierte Rückruffunktion an, die eine Eigenschaftenblatterweiterung verwendet, um einem Eigenschaftenblatt eine Seite hinzuzufügen.<br/>                                                                                                                      |
| [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)   | Erstellt eine neue Seite für ein Eigenschaftenblatt.<br/>                                                                                                                                                                                                        |
| [**DestroyPropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) | Zerstört eine Eigenschaftenblattseite. Eine Anwendung muss diese Funktion für Seiten aufrufen, die nicht an die [**PropertySheet-Funktion übergeben**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) wurden.<br/>                                                                              |
| [**Propertysheet.showdialog**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)                       | Erstellt ein Eigenschaftenblatt und fügt die in der angegebenen Eigenschaftenblatt-Headerstruktur definierten Seiten hinzu.<br/>                                                                                                                                           |
| [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)                 | Gibt eine anwendungsdefinierte Rückruffunktion an, die ein Eigenschaftenblatt aufruft, wenn eine Seite erstellt und zerstört wird. Eine Anwendung kann diese Funktion verwenden, um Initialisierungs- und Bereinigungsvorgänge für die Seite durchzuführen.<br/> |
| [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback)                         | Eine anwendungsdefinierte Rückruffunktion, die das System aufruft, wenn das Eigenschaftenblatt erstellt und initialisiert wird.<br/>                                                                                                                        |



 

### <a name="messages"></a>Meldungen



| Thema                                                               | Inhalte                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PSM \_ ADDPAGE**](psm-addpage.md)                                 | Fügt am Ende eines vorhandenen Eigenschaftenblatts eine neue Seite hinzu. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ AddPage-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) senden.<br/>                                                                                                |
| [**PSM \_ APPLY**](psm-apply.md)                                     | Simuliert die Auswahl  der Schaltfläche Anwenden, die angibt, dass sich eine oder mehrere Seiten geändert haben und die Änderungen überprüft und aufgezeichnet werden müssen.<br/>                                                                                                                   |
| [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md)                     | Wird von einer Anwendung gesendet, wenn seit der letzten [PSN \_ APPLY-Benachrichtigung](psn-apply.md) Änderungen vorgenommen wurden, die nicht abgebrochen werden können. Sie können diese Nachricht explizit oder mithilfe des [**Makros PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) senden.<br/> |
| [**PSM \_ GEÄNDERT**](psm-changed.md)                                 | Informiert ein Eigenschaftenblatt darüber, dass sich die Informationen auf einer Seite geändert haben. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ Changed-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) senden.<br/>                                                                                         |
| [**PSM \_ ENABLEWIZBUTTONS**](psm-enablewizbuttons.md)               | Aktiviert oder deaktiviert alle Standardschaltflächen in einem Assistenten für Assistenten. Sie können diese Nachricht explizit senden oder das [**\_ PropSheet-Makro EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) verwenden.<br/>                                                                          |
| [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md)           | Ruft ein Handle für das Fenster der aktuellen Seite eines Eigenschaftenblatts ab. Sie können diese Nachricht explizit oder mithilfe des [**\_ PropSheet-Makros GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) senden.<br/>                                                          |
| [**PSM \_ GETRESULT**](psm-getresult.md)                             | Wird von moduslosen Eigenschaftenblättern verwendet, um die Informationen abzurufen, die von PropertySheet an modale [**Eigenschaftenblätter zurückgegeben werden.**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) Sie können diese Nachricht explizit senden oder das [**PropSheet \_ GetResult-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) verwenden.<br/>                 |
| [**PSM \_ GETTABCONTROL**](psm-gettabcontrol.md)                     | Ruft das Handle für das Registerkarten-Steuerelement eines Eigenschaftenblatts ab. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ GetTabControl-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) senden.<br/>                                                                                 |
| [**PSM \_ HWNDTOINDEX**](psm-hwndtoindex.md)                         | Übernimmt das Fensterhand handle der Eigenschaftenblattseite und gibt den nullbasierten Index zurück. Sie können diese Nachricht explizit senden oder das [**PropSheet \_ HwndToIndex-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) verwenden.<br/>                                                                  |
| [**PSM \_ IDTOINDEX**](psm-idtoindex.md)                             | Verwendet die Ressourcen-ID einer Eigenschaftenblattseite und gibt ihren nullbasierten Index zurück. Sie können diese Nachricht explizit senden oder das [**PropSheet \_ IdToIndex-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) verwenden.<br/>                                                                          |
| [**PSM \_ INDEXTOHWND**](psm-indextohwnd.md)                         | Verwendet den Index einer Eigenschaftenblattseite und gibt dessen Fensterhandpunkt zurück. Sie können diese Nachricht explizit senden oder das [**PropSheet \_ IndexToHwnd-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) verwenden.<br/>                                                                               |
| [**PSM \_ INDEXTOID**](psm-indextoid.md)                             | Verwendet den Index einer Eigenschaftenblattseite und gibt die Ressourcen-ID zurück. Sie können diese Nachricht explizit senden oder das [**PropSheet \_ IndexToId-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) verwenden.<br/>                                                                                     |
| [**PSM \_ INDEXTOPAGE**](psm-indextopage.md)                         | Verwendet den Index einer Eigenschaftenblattseite und gibt das HPROPSHEETPAGE-Handle zurück. Sie können diese Nachricht explizit senden oder das [**PropSheet \_ IndexToPage-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) verwenden.<br/>                                                                       |
| [**PSM \_ INSERTPAGE**](psm-insertpage.md)                           | Fügt eine neue Seite in ein vorhandenes Eigenschaftenblatt ein. Die Seite kann entweder an einem angegebenen Index oder nach einer angegebenen Seite eingefügt werden. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ InsertPage-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) senden.<br/>                |
| [**PSM \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md)                 | Übergibt eine Meldung an ein Eigenschaftenblattdialogfeld und gibt an, ob die Nachricht vom Dialogfeld verarbeitet wurde. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ IsDialogMessage-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) senden.<br/>                              |
| [**PSM \_ PAGETOINDEX**](psm-pagetoindex.md)                         | Übernimmt das HPROPSHEETPAGE-Handle der Eigenschaftenblattseite und gibt seinen nullbasierten Index zurück. Sie können diese Nachricht explizit senden oder das [**PropSheet \_ PageToIndex-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) verwenden.<br/>                                                          |
| [**PSM \_ PRESSBUTTON**](psm-pressbutton.md)                         | Simuliert die Auswahl einer Eigenschaftenblattschaltfläche. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ PressButton-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) senden.<br/>                                                                                              |
| [**\_PSM-ABFRAGESIBLINGS**](psm-querysiblings.md)                     | Wird an ein Eigenschaftenblatt gesendet, das die Nachricht dann an die einzelnen Seiten weitersandt. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ QuerySiblings-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) senden.<br/>                                                              |
| [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md)                       | Gibt an, dass das System neu gestartet werden muss, damit die Änderungen wirksam werden. Sie können die [**PSM \_ REBOOTSYSTEM-Nachricht**](psm-rebootsystem.md) explizit oder mithilfe des [**PropSheet \_ RebootSystem-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) senden.<br/>                        |
| [**NEUBERECHNUNG VON \_ PSM-SEITEN**](psm-recalcpagesizes.md)                 | Berechnet die Seitengröße eines Standard- oder Assistenten-Eigenschaftenblatts neu, nachdem Seiten hinzugefügt oder entfernt wurden. Sie können diese Nachricht explizit senden oder das [**PropSheet \_ RecalcPageSizes-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) verwenden.<br/>                                     |
| [**PSM \_ REMOVEPAGE**](psm-removepage.md)                           | Entfernt eine Seite aus einem Eigenschaftenblatt. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ RemovePage-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) senden.<br/>                                                                                                              |
| [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md)                   | Gibt an Windows dass die Änderungen neu gestartet werden müssen, damit die Änderungen wirksam werden.<br/>                                                                                                                                                                                         |
| [**PSM \_ SETBUTTONTEXT**](psm-setbuttontext.md)                     | Legt den Text auf einer Schaltfläche in einem Assistenten fest. Sie können diese Nachricht explizit oder mithilfe des [**\_ PropSheet-Makros SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) senden.<br/>                                                                                                 |
| [**PSM \_ SETCURSEL**](psm-setcursel.md)                             | Aktiviert die angegebene Seite in einem Eigenschaftenblatt. Sie können diese Nachricht explizit oder mithilfe des [**\_ PropSheet-Makros SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) senden.<br/>                                                                                                    |
| [**PSM \_ SETCURSELID**](psm-setcurselid.md)                         | Aktiviert die angegebene Seite in einem Eigenschaftenblatt basierend auf dem Ressourcenbezeichner der Seite. Sie können diese Nachricht explizit oder mithilfe des [**\_ PropSheet-Makros SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) senden.<br/>                                                   |
| [**PSM \_ SETFINISHTEXT**](psm-setfinishtext.md)                     | Legt den Text der Schaltfläche **Fertig stellen** in einem Assistenten fest, zeigt die Schaltfläche an und aktiviert sie und blendet die Schaltflächen **Weiter** und **Zurück** aus. Sie können diese Nachricht explizit oder mithilfe des [**\_ PropSheet-Makros SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) senden.<br/>               |
| [**PSM \_ SETHEADERBITMAP**](psm-setheaderbitmap.md)                 | Diese Meldung ist nicht implementiert.<br/>                                                                                                                                                                                                                                     |
| [**PSM \_ SETHEADERBITMAPRESOURCE**](psm-setheaderbitmapresource.md) | Diese Meldung ist nicht implementiert.<br/>                                                                                                                                                                                                                                     |
| [**PSM \_ SETHEADERSUBTITLE**](psm-setheadersubtitle.md)             | Legt den Untertiteltext für den Header der inneren Seite eines Assistenten fest. Sie können diese Nachricht explizit senden oder das [**\_ PropSheet-Makro SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) verwenden.<br/>                                                                        |
| [**PSM \_ SETHEADERTITLE**](psm-setheadertitle.md)                   | Legt den Titeltext für den Header der inneren Seite eines Assistenten fest. Sie können diese Nachricht explizit senden oder das [**\_ PropSheet-Makro SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) verwenden.<br/>                                                                                 |
| [**PSM \_ SETNEXTTEXT**](psm-setnexttext.md)                         | Legt den Text der Schaltfläche **Weiter** in einem Assistenten fest. Sie können diese Nachricht explizit oder mithilfe des [**\_ PropSheet-Makros SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) senden.<br/>                                                                                                |
| [**PSM \_ SETTITLE**](psm-settitle.md)                               | Legt den Titel eines Eigenschaftenblatts fest. Sie können diese Nachricht explizit oder mit dem [**PropSheet \_ SetTitle-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) senden.<br/>                                                                                                                    |
| [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md)                     | Aktiviert oder deaktiviert die Schaltflächen **Zurück,** **Weiter** und **Fertig stellen** in einem Assistenten. Sie können auch das [**\_ PropSheet-Makro SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) verwenden, um die Nachricht zu veröffentlichen.<br/>                                                                          |
| [**PSM \_ SHOWWIZBUTTONS**](psm-showwizbuttons.md)                   | Zeigt Schaltflächen in einem Assistenten an oder blendet sie aus. Sie können diese Nachricht explizit oder mithilfe des [**\_ PropSheet-Makros ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) senden.<br/>                                                                                                        |
| [**PSM \_ UNVERÄNDERT**](psm-unchanged.md)                             | Informiert ein Eigenschaftenblatt darüber, dass die Informationen auf einer Seite in den zuvor gespeicherten Zustand zurückgesetzt wurden. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ UnChanged-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) senden.<br/>                                                      |



 

### <a name="notifications"></a>Benachrichtigungen



| Thema                                                     | Inhalte                                                                                                                                                                                                                                                |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PSN \_ APPLY](psn-apply.md)                               | Wird an jede Seite im Eigenschaftenblatt gesendet, um anzugeben, dass der Benutzer auf die Schaltfläche OK, Schließen oder Übernehmen geklickt hat und alle Änderungen wirksam werden soll. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>      |
| [PSN \_ GETOBJECT](psn-getobject.md)                       | Wird von einem Eigenschaftenblatt gesendet, um ein Ablagezielobjekt anzufordern, wenn der Cursor eine der Schaltflächen des Registerkartensteuerelements übergibt.<br/>                                                                                                                       |
| [\_PSN-HILFE](psn-help.md)                                 | Benachrichtigt eine Seite, dass der Benutzer auf die Schaltfläche Hilfe geklickt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>                                                                                          |
| [PSN \_ KILLACTIVE](psn-killactive.md)                     | Benachrichtigt eine Seite, dass sie die Aktivierung verlieren wird, weil entweder eine andere Seite aktiviert wird oder der Benutzer auf die Schaltfläche **OK** geklickt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>       |
| [PSN \_ QUERYCANCEL](psn-querycancel.md)                   | Gibt an, dass der Benutzer das Eigenschaftenblatt abgebrochen hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>                                                                                            |
| [PSN \_ QUERYINITIALFOCUS](psn-queryinitialfocus.md)       | Wird von einem Eigenschaftenblatt gesendet, um einer Eigenschaftenblattseite die Möglichkeit bereitzustellen, anzugeben, welches Dialogfeld-Steuerelement den anfänglichen Fokus erhalten soll. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>           |
| [\_PSN-ZURÜCKSETZUNG](psn-reset.md)                               | Benachrichtigt eine Seite, dass das Eigenschaftenblatt zerstört werden soll. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>                                                                                   |
| [PSN \_ SETACTIVE](psn-setactive.md)                       | Benachrichtigt eine Seite, dass sie aktiviert werden soll. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>                                                                                                   |
| [PSN \_ TRANSLATEACCELERATOR](psn-translateaccelerator.md) | Benachrichtigt ein Eigenschaftenblatt, dass eine Tastaturmeldung empfangen wurde. Sie bietet der Seite die Möglichkeit, eine private Tastaturbeschleunigungsübersetzung zu erstellen. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/> |
| [PSN \_ WIZBACK](psn-wizback.md)                           | Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die Schaltfläche **Zurück** geklickt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>                                                                          |
| [PSN \_ WIZFINISH](psn-wizfinish.md)                       | Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die Schaltfläche **Fertig stellen** geklickt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>                                                                        |
| [PSN \_ WIZNEXT](psn-wiznext.md)                           | Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die Schaltfläche **Weiter** geklickt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.<br/>                                                                          |



 

### <a name="structures"></a>Strukturen



| Thema                                      | Inhalte                                                                   |
|--------------------------------------------|----------------------------------------------------------------------------|
| [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) | Definiert den Rahmen und die Seiten eines Eigenschaftenblatts.<br/>                |
| [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2)     | Definiert eine Seite in einem Eigenschaftenblatt.<br/>                             |
| [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)             | Enthält Informationen für die Benachrichtigungscodes des Eigenschaftenblatts.<br/> |



 

 

