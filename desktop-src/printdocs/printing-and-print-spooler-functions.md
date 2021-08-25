---
description: Die Druckspooler-API enthält die Funktionen und Datenstrukturen, die Anwendungen verwenden, um den Windows-Druckspooler und die drucker- und druckaufträge zu verwalten, die er steuert.
ms.assetid: d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39
title: Druckspooler-API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cab0a23afcfa95c4acb427437c72758356ee9771182301111f9660455d2081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824890"
---
# <a name="print-spooler-api-functions"></a>Druckspooler-API-Funktionen

Die Druckspooler-API enthält die Funktionen und Datenstrukturen, die Anwendungen verwenden, um den Windows-Druckspooler und die drucker- und druckaufträge zu verwalten, die er steuert.

Die Funktionen der Druckspooler-API sind in die folgenden Gruppen unterteilt:

-   [Druckauftragsfunktionen](#print-job-functions)
-   [Drucker Benutzeroberfläche Funktionen](#printer-user-interface-functions)
-   [Druckerfunktionen](#printer-functions)
-   [Benachrichtigungsfunktionen für Druckeränderung](#printer-change-notification-functions)
-   [Druckerformularfunktionen](#printer-form-functions)
-   [Druckspoolerfunktionen](#print-spooler-api-functions)

## <a name="print-job-functions"></a>Druckauftragsfunktionen

Diese Funktionen senden Druckaufträge an einen Drucker und verfolgen und steuern die Druckaufträge im Druckspooler.



| Funktion                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addjob**](addjob.md)<br/>                                           | Die [**AddJob-Funktion**](/windows/desktop/printdocs/addjob) fügt der Liste der Druckaufträge, die vom Druckspooler geplant werden können, einen Druckauftrag hinzu. Die Funktion ruft den Namen der Datei ab, die Sie zum Speichern des Auftrags verwenden können. <br/>                                      |
| [**ClosePrinter**](closeprinter.md)<br/>                               | Die [**ClosePrinter-Funktion**](/windows/desktop/printdocs/closeprinter) schließt das angegebene Druckerobjekt. <br/>                                                                                                                                                      |
| [**DocumentEvent**](documentevent.md)<br/>                             | Die [**DocumentEvent-Funktion**](/windows/desktop/printdocs/documentevent) ist ein Ereignishandler für Ereignisse, die dem Drucken eines Dokuments zugeordnet sind. <br/>                                                                                                                     |
| [**Documentproperties**](documentproperties.md)<br/>                   | Die [**DocumentProperties-Funktion**](/windows/desktop/printdocs/documentproperties) ruft Druckerin initialisierungsinformationen ab oder ändert sie oder zeigt ein Eigenschaftenblatt für die Druckerkonfiguration für den angegebenen Drucker an. <br/>                                        |
| [**EndDocPrinter**](enddocprinter.md)<br/>                             | Die [**EndDocPrinter-Funktion**](/windows/desktop/printdocs/enddocprinter) beendet einen Druckauftrag für den angegebenen Drucker. <br/>                                                                                                                                             |
| [**EndPagePrinter**](endpageprinter.md)<br/>                           | Die [**EndPagePrinter-Funktion**](/windows/desktop/printdocs/endpageprinter) benachrichtigt den Druckspooler, dass sich die Anwendung am Ende einer Seite in einem Druckauftrag befindet. <br/>                                                                                               |
| [**EnumJobs**](enumjobs.md)<br/>                                       | Die [**EnumJobs-Funktion**](/windows/desktop/printdocs/enumjobs) ruft Informationen zu einem angegebenen Satz von Druckaufträgen für einen angegebenen Drucker ab. <br/>                                                                                                                |
| [**GetJob**](getjob.md)<br/>                                           | Die [**GetJob-Funktion**](/windows/desktop/printdocs/getjob) ruft Informationen zu einem angegebenen Druckauftrag ab. <br/>                                                                                                                                                    |
| [**OpenPrinter**](openprinter.md)<br/>                                 | Die [**OpenPrinter-Funktion**](/windows/desktop/printdocs/openprinter) ruft ein Handle für den angegebenen Drucker oder Druckerserver oder andere Handles im Drucksubsystem ab. <br/>                                                                               |
| [**OpenPrinter2**](openprinter2.md)<br/>                               | Ruft ein Handle für den angegebenen Drucker, Druckerserver oder andere Handles im Drucksubsystem ab, während einige der Druckeroptionen festgelegt werden.<br/>                                                                                      |
| [**ReportJobProcessingProgress**](reportjobprocessingprogress.md)<br/> | Meldet dem Druckspoolerdienst, ob sich ein XPS-Druckauftrag in der Spooling- oder Renderingphase befindet und welcher Teil der Verarbeitung gerade ausgeführt wird.<br/>                                                                               |
| [**ScheduleJob**](schedulejob.md)<br/>                                 | Die [**ScheduleJob-Funktion**](/windows/desktop/printdocs/schedulejob) fordert an, dass der Druckspooler einen angegebenen Druckauftrag für das Drucken geplant. <br/>                                                                                                                |
| [**SetJob**](setjob.md)<br/>                                           | Die [**SetJob-Funktion**](/windows/desktop/printdocs/setjob) hält einen Druckauftrag auf einem angegebenen Drucker an, setzt ihn wieder auf, bricht ihn ab oder startet ihn neu. Sie können auch die **SetJob-Funktion** verwenden, um Druckauftragsparameter wie die Druckauftragspriorität und den Dokumentnamen zu festlegen. <br/> |
| [**StartDocPrinter**](startdocprinter.md)<br/>                         | Die [**StartDocPrinter-Funktion**](/windows/desktop/printdocs/startdocprinter) benachrichtigt den Druckspooler, dass ein Dokument zum Drucken spoolt werden soll. <br/>                                                                                                           |
| [**StartPagePrinter**](startpageprinter.md)<br/>                       | Die [**StartPagePrinter-Funktion**](/windows/desktop/printdocs/startpageprinter) benachrichtigt den Spooler, dass eine Seite auf dem angegebenen Drucker gedruckt werden soll. <br/>                                                                                                 |



 

## <a name="printer-user-interface-functions"></a>Drucker Benutzeroberfläche Funktionen

Diese Funktionen zeigen eine Benutzeroberfläche an, die es dem Benutzer ermöglicht, einen Drucker auszuwählen oder zu konfigurieren.



| Funktion                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedDocumentProperties**](advanceddocumentproperties.md)<br/> | Die [**AdvancedDocumentProperties-Funktion**](/windows/desktop/printdocs/advanceddocumentproperties) zeigt ein Dialogfeld für die Druckerkonfiguration für den angegebenen Drucker an, sodass der Benutzer diesen Drucker konfigurieren kann. <br/>                                                                                                                                                      |
| [**ConfigurePort**](configureport.md)<br/>                           | Die [**ConfigurePort-Funktion**](/windows/desktop/printdocs/configureport) zeigt das Dialogfeld "Portkonfiguration" für einen Port auf dem angegebenen Server an. <br/>                                                                                                                                                                                                                     |
| [**ConnectToPrinterDlg**](connecttoprinterdlg.md)<br/>               | Die [**ConnectToPrinterDlg-Funktion**](/windows/desktop/printdocs/connecttoprinterdlg) zeigt ein Dialogfeld an, in dem Benutzer Drucker in einem Netzwerk durchsuchen und eine Verbindung mit ihnen herstellen können. Wenn der Benutzer einen Drucker auswählt, versucht die Funktion, eine Verbindung mit ihm herzustellen. Wenn kein geeigneter Treiber auf dem Server installiert ist, erhält der Benutzer die Möglichkeit, einen Drucker lokal zu erstellen. <br/> |
| [**PrinterProperties**](printerproperties.md)<br/>                   | Die [**PrinterProperties-Funktion**](/windows/desktop/printdocs/printerproperties) zeigt ein Eigenschaftenblatt für Druckereigenschaften für den angegebenen Drucker an. <br/>                                                                                                                                                                                                                    |



 

## <a name="printer-functions"></a>Druckerfunktionen

Diese Funktionen fügen die Drucker hinzu und konfigurieren sie, die der Druckspooler verwendet.



| Funktion                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPrinter**](abortprinter.md)<br/>                       | Die [**AbortPrinter-Funktion**](/windows/desktop/printdocs/abortprinter) löscht die Spooldatei eines Druckers, wenn der Drucker für das Spooling konfiguriert ist. <br/>                                                                                                                                                                                                                                                                  |
| [**AddPrinter**](addprinter.md)<br/>                           | Die [**AddPrinter-Funktion**](/windows/desktop/printdocs/addprinter) fügt der Liste der unterstützten Drucker für einen angegebenen Server einen Drucker hinzu. <br/>                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection**](addprinterconnection.md)<br/>       | Die **AddPrinterConnection-Funktion** fügt dem angegebenen Drucker für den aktuellen Benutzer eine Verbindung hinzu. <br/>                                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection2**](addprinterconnection2.md)<br/>     | Fügt dem angegebenen Drucker für den aktuellen Benutzer eine Verbindung hinzu und gibt Verbindungsdetails an.<br/>                                                                                                                                                                                                                                                                                             |
| [**DeletePrinter**](deleteprinter.md)<br/>                     | Die [**DeletePrinter-Funktion**](/windows/desktop/printdocs/deleteprinter) löscht das angegebene Druckerobjekt. <br/>                                                                                                                                                                                                                                                                                                    |
| [**DeletePrinterConnection**](deleteprinterconnection.md)<br/> | Die [**DeletePrinterConnection-Funktion**](/windows/desktop/printdocs/deleteprinterconnection) löscht eine Verbindung mit einem Drucker, der durch einen Aufruf von [**AddPrinterConnection**](addprinterconnection.md) oder [**ConnectToPrinterDlg hergestellt wurde.**](connecttoprinterdlg.md) <br/>                                                                                                                                      |
| [**DeletePrinterData**](deleteprinterdata.md)<br/>             | Die [**DeletePrinterData-Funktion**](/windows/desktop/printdocs/deleteprinterdata) löscht die angegebenen Konfigurationsdaten für einen Drucker. Die Konfigurationsdaten eines Druckers bestehen aus einem Satz von benannten und typierten Werten. Die **DeletePrinterData-Funktion** löscht einen dieser Werte, der durch ihren Wertnamen angegeben wird. <br/>                                                                                                     |
| [**DeletePrinterDataEx**](deleteprinterdataex.md)<br/>         | Die [**DeletePrinterDataEx-Funktion**](/windows/desktop/printdocs/deleteprinterdataex) löscht einen angegebenen Wert aus den Konfigurationsdaten für einen Drucker. Die Konfigurationsdaten eines Druckers bestehen aus einem Satz von benannten und typierten Werten, die in einer Hierarchie von Registrierungsschlüsseln gespeichert sind. Die Funktion löscht einen angegebenen Wert unter einem angegebenen Schlüssel. <br/>                                                                        |
| [**DeletePrinterKey**](deleteprinterkey.md)<br/>               | Die [**DeletePrinterKey-Funktion**](/windows/desktop/printdocs/deleteprinterkey) löscht einen angegebenen Schlüssel und alle seine Unterschlüssel für einen angegebenen Drucker. <br/>                                                                                                                                                                                                                                                               |
| [**EnumPrinterData**](enumprinterdata.md)<br/>                 | Die [**EnumPrinterData-Funktion**](/windows/desktop/printdocs/enumprinterdata) aufzählt Konfigurationsdaten für einen angegebenen Drucker. <br/>                                                                                                                                                                                                                                                                               |
| [**EnumPrinterDataEx**](enumprinterdataex.md)<br/>             | Die [**EnumPrinterDataEx-Funktion**](/windows/desktop/printdocs/enumprinterdataex) auflistet alle Wertnamen und Daten für einen angegebenen Drucker und Schlüssel. <br/>                                                                                                                                                                                                                                                             |
| [**EnumPrinterKey**](enumprinterkey.md)<br/>                   | Die [**EnumPrinterKey-Funktion**](/windows/desktop/printdocs/enumprinterkey) aufzählt die Unterschlüssel eines angegebenen Schlüssels für einen angegebenen Drucker. <br/>                                                                                                                                                                                                                                                                     |
| [**EnumPrinters**](enumprinters.md)<br/>                       | Die [**EnumPrinters-Funktion**](/windows/desktop/printdocs/enumprinters) aufzählt verfügbare Drucker, Druckerserver, Domänen oder Druckanbieter. <br/>                                                                                                                                                                                                                                                                 |
| [**FlushPrinter**](flushprinter.md)<br/>                       | Die [**FlushPrinter-Funktion**](/windows/desktop/printdocs/flushprinter) sendet einen Puffer an den Drucker, um ihn aus einem vorübergehenden Zustand zu löschen. <br/>                                                                                                                                                                                                                                                                 |
| [**GetDefaultPrinter**](getdefaultprinter.md)<br/>             | Die [**GetDefaultPrinter-Funktion**](/windows/desktop/printdocs/getdefaultprinter) ruft den Druckernamen des Standarddruckers für den aktuellen Benutzer auf dem lokalen Computer ab. <br/>                                                                                                                                                                                                                                    |
| [**GetPrinter**](getprinter.md)<br/>                           | Die [**GetPrinter-Funktion**](/windows/desktop/printdocs/getprinter) ruft Informationen zu einem angegebenen Drucker ab. <br/>                                                                                                                                                                                                                                                                                               |
| [**GetPrinterData**](getprinterdata.md)<br/>                   | Die [**GetPrinterData-Funktion**](/windows/desktop/printdocs/getprinterdata) ruft Konfigurationsdaten für den angegebenen Drucker oder Druckerserver ab. <br/>                                                                                                                                                                                                                                                                |
| [**GetPrinterDataEx**](getprinterdataex.md)<br/>               | Die [**GetPrinterDataEx-Funktion**](/windows/desktop/printdocs/getprinterdataex) ruft Konfigurationsdaten für den angegebenen Drucker oder Druckerserver ab. **GetPrinterDataEx** kann werte abrufen, die von der [**SetPrinterData-Funktion**](setprinterdata.md) gespeichert werden. Darüber hinaus kann **GetPrinterDataEx** Werte abrufen, die unter einem angegebenen Schlüssel von der [**SetPrinterDataEx-Funktion**](setprinterdataex.md) gespeichert sind. <br/> |
| [**IsValidDevmode**](isvaliddevmode.md)<br/>                   | Die [**IsValidDevmode-Funktion**](isvaliddevmode.md) überprüft, ob der Inhalt einer DEVMODE-Struktur gültig ist. <br/>                                                                                                                                                                                                                                                                           |
| [**ReadPrinter**](readprinter.md)<br/>                         | Die [**ReadPrinter-Funktion**](/windows/desktop/printdocs/readprinter) ruft Daten vom angegebenen Drucker ab. <br/>                                                                                                                                                                                                                                                                                                   |
| [**ResetPrinter**](resetprinter.md)<br/>                       | Die [**ResetPrinter-Funktion**](/windows/desktop/printdocs/resetprinter) gibt die Datentyp- und Gerätemoduswerte an, die zum Drucken von Dokumenten verwendet werden sollen, die von der [**StartDocPrinter-Funktion**](startdocprinter.md) übermittelt werden. Diese Werte können mithilfe der [**SetJob-Funktion**](setjob.md) überschrieben werden, nachdem der Dokumentdruck gestartet wurde. <br/>                                                                  |
| [**SetDefaultPrinter**](setdefaultprinter.md)<br/>             | Die [**SetDefaultPrinter-Funktion**](/windows/desktop/printdocs/setdefaultprinter) legt den Druckernamen des Standarddruckers für den aktuellen Benutzer auf dem lokalen Computer fest. <br/>                                                                                                                                                                                                                                         |
| [**SetPort**](setport.md)<br/>                                 | Die [**SetPort-Funktion**](/windows/desktop/printdocs/setport) legt den Status fest, der einem Druckerport zugeordnet ist. <br/>                                                                                                                                                                                                                                                                                                      |
| [**SetPrinter**](setprinter.md)<br/>                           | Die [**SetPrinter-Funktion**](/windows/desktop/printdocs/setprinter) legt die Daten für einen angegebenen Drucker fest oder legt den Zustand des angegebenen Druckers fest, indem der Druck angehalten, der Druckvorgang fortsetzen oder alle Druckaufträge löscht werden. <br/>                                                                                                                                                                                           |
| [**SetPrinterData**](setprinterdata.md)<br/>                   | Die [**SetPrinterData-Funktion**](/windows/desktop/printdocs/setprinterdata) legt die Konfigurationsdaten für einen Drucker oder Druckerserver fest. <br/>                                                                                                                                                                                                                                                                             |
| [**SetPrinterDataEx**](setprinterdataex.md)<br/>               | Die [**SetPrinterDataEx-Funktion**](/windows/desktop/printdocs/setprinterdataex) legt die Konfigurationsdaten für einen Drucker oder Druckerserver fest. Die Funktion speichert die Konfigurationsdaten unter dem Registrierungsschlüssel des Druckers. <br/>                                                                                                                                                                                            |
| [**WritePrinter**](writeprinter.md)<br/>                       | Die [**WritePrinter-Funktion**](writeprinter.md) benachrichtigt den Druckspooler, dass Daten in den angegebenen Drucker geschrieben werden sollen. <br/>                                                                                                                                                                                                                                                           |



 

## <a name="printer-change-notification-functions"></a>Benachrichtigungsfunktionen für Druckeränderungen

Diese Funktionen ermöglichen es einer Anwendung, über Änderungen am Status eines Druckers benachrichtigt zu werden.



| Funktion                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)<br/> | Die [**Funktion FindClosePrinterChangeNotification**](/windows/desktop/printdocs/findcloseprinterchangenotification) schließt ein Änderungsbenachrichtigungsobjekt, das durch Aufrufen der [**FindFirstPrinterChangeNotification-Funktion**](findfirstprinterchangenotification.md) erstellt wurde. Der drucker- oder druckserver, der dem Änderungsbenachrichtigungsobjekt zugeordnet ist, wird von diesem Objekt nicht mehr überwacht. <br/> |
| [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)<br/> | Die [**FindFirstPrinterChangeNotification-Funktion**](/windows/desktop/printdocs/findfirstprinterchangenotification) erstellt ein Änderungsbenachrichtigungsobjekt und gibt ein Handle für das Objekt zurück. Sie können dieses Handle dann in einem Aufruf einer der Wartefunktionen verwenden, um Änderungen am Drucker oder Druckerserver zu überwachen. <br/>                                                                              |
| [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)<br/>   | Die [**Funktion FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) ruft Informationen zur letzten Änderungsbenachrichtigung für ein Änderungsbenachrichtigungsobjekt ab, das einem Drucker oder Druckerserver zugeordnet ist. Rufen Sie diese Funktion auf, wenn ein Wartevorgang für das Änderungsbenachrichtigungsobjekt erfüllt ist. <br/>                                           |
| [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md)<br/>                           | Die [**FreePrinterNotifyInfo-Funktion**](/windows/desktop/printdocs/freeprinternotifyinfo) gibt einen vom System zugeordneten Puffer frei, der von der [**FindNextPrinterChangeNotification-Funktion**](findnextprinterchangenotification.md) erstellt wurde. <br/>                                                                                                                                                                |



 

## <a name="printer-form-functions"></a>Druckerformularfunktionen

Diese Funktionen verwalten die von einem Drucker verwendeten Formulare.



| Funktion                                    | BESCHREIBUNG                                                                                                                                    |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddForm**](addform.md)<br/>       | Die [**Funktion AddForm**](/windows/desktop/printdocs/addform) fügt der Liste der verfügbaren Formulare ein Formular hinzu, das für den angegebenen Drucker ausgewählt werden kann. <br/> |
| [**DeleteForm**](deleteform.md)<br/> | Die [**DeleteForm-Funktion**](/windows/desktop/printdocs/deleteform) entfernt einen Formularnamen aus der Liste der unterstützten Formulare. <br/>                                |
| [**EnumForms**](enumforms.md)<br/>   | Die [**EnumForms-Funktion**](/windows/desktop/printdocs/enumforms) listet die vom angegebenen Drucker unterstützten Formulare auf. <br/>                               |
| [**GetForm**](getform.md)<br/>       | Die [**GetForm-Funktion**](/windows/desktop/printdocs/getform) ruft Informationen zu einem angegebenen Formular ab. <br/>                                              |
| [**SetForm**](setform.md)<br/>       | Die [**SetForm-Funktion**](/windows/desktop/printdocs/setform) legt die Formularinformationen für den angegebenen Drucker fest. <br/>                                       |



 

## <a name="print-spooler-functions"></a>Druckspoolerfunktionen

Diese Funktionen interagieren auf niedriger Ebene mit dem Druckspooler.



| Funktion                                                          | BESCHREIBUNG                                                                                                                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseSpoolFileHandle**](closespoolfilehandle.md)<br/>   | Die [**CloseSpoolFileHandle-Funktion**](/windows/desktop/printdocs/closespoolfilehandle) schließt ein Handle für eine Spooldatei, die dem druckauftrag zugeordnet ist, der derzeit von der Anwendung übermittelt wird. <br/>                    |
| [**CommitSpoolData**](commitspooldata.md)<br/>             | Die [**CommitSpoolData-Funktion**](/windows/desktop/printdocs/commitspooldata) benachrichtigt den Druckspooler, dass eine angegebene Datenmenge in eine angegebene Spooldatei geschrieben wurde und gerendert werden kann. <br/> |
| [**GetPrintExecutionData**](getprintexecutiondata.md)<br/> | [**GetPrintExecutionData**](getprintexecutiondata.md) ruft den aktuellen Druckkontext ab.<br/>                                                                                             |
| [**GetSpoolFileHandle**](getspoolfilehandle.md)<br/>       | Die [**GetSpoolFileHandle-Funktion**](/windows/desktop/printdocs/getspoolfilehandle) ruft ein Handle für die Spooldatei ab, die dem derzeit von der Anwendung übermittelten Auftrag zugeordnet ist. <br/>                        |



 

 

