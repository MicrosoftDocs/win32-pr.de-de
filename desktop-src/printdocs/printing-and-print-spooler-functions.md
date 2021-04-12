---
description: Die druckspoolerapi enthält die Funktionen und Datenstrukturen, mit denen Anwendungen den Druck Spooler von Windows und die von ihm kontrollierten Drucker und Druckaufträge verwalten.
ms.assetid: d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39
title: Druckspooler-API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df751b11206ebf26d2d0e8fd88f61ede8447dad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218105"
---
# <a name="print-spooler-api-functions"></a>Druckspooler-API-Funktionen

Die druckspoolerapi enthält die Funktionen und Datenstrukturen, mit denen Anwendungen den Druck Spooler von Windows und die von ihm kontrollierten Drucker und Druckaufträge verwalten.

Die Funktionen der druckspoolerapi sind in die folgenden Gruppen unterteilt:

-   [Druckauftrags Funktionen](#print-job-functions)
-   [Funktionen der druckerbenutzerschnittstelle](#printer-user-interface-functions)
-   [Druckerfunktionen](#printer-functions)
-   [Benachrichtigungsfunktionen für Drucker Änderungen](#printer-change-notification-functions)
-   [Druckerformular-Funktionen](#printer-form-functions)
-   [Druckspoolerfunktionen](#print-spooler-api-functions)

## <a name="print-job-functions"></a>Druckauftrags Funktionen

Diese Funktionen senden Druckaufträge an einen Drucker und verfolgen und steuern die Druckaufträge im Druck Spooler.



| Funktion                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddJob**](addjob.md)<br/>                                           | Die [**AddJob**](/windows/desktop/printdocs/addjob) -Funktion fügt der Liste der Druckaufträge, die vom Druck Spooler geplant werden können, einen Druckauftrag hinzu. Die-Funktion Ruft den Namen der Datei ab, die Sie verwenden können, um den Auftrag zu speichern. <br/>                                      |
| [**Closeprinter**](closeprinter.md)<br/>                               | Die [**closeprinter**](/windows/desktop/printdocs/closeprinter) -Funktion schließt das angegebene Drucker Objekt. <br/>                                                                                                                                                      |
| [**DocumentEvent**](documentevent.md)<br/>                             | Die [**DocumentEvent**](/windows/desktop/printdocs/documentevent) -Funktion ist ein Ereignishandler für Ereignisse, die dem Drucken eines Dokuments zugeordnet sind. <br/>                                                                                                                     |
| [**DocumentProperties**](documentproperties.md)<br/>                   | Die [**DocumentProperties**](/windows/desktop/printdocs/documentproperties) -Funktion ruft Drucker Initialisierungs Informationen ab oder ändert Sie oder zeigt ein Eigenschaften Blatt der Druckerkonfiguration für den angegebenen Drucker an. <br/>                                        |
| [**Enddocprinter**](enddocprinter.md)<br/>                             | Die [**enddocprinter**](/windows/desktop/printdocs/enddocprinter) -Funktion beendet einen Druckauftrag für den angegebenen Drucker. <br/>                                                                                                                                             |
| [**Endpageprinter**](endpageprinter.md)<br/>                           | Die [**endpageprinter**](/windows/desktop/printdocs/endpageprinter) -Funktion benachrichtigt den Druck Spooler, dass sich die Anwendung am Ende einer Seite in einem Druckauftrag befindet. <br/>                                                                                               |
| [**EnumJobs**](enumjobs.md)<br/>                                       | Die [**EnumJobs**](/windows/desktop/printdocs/enumjobs) -Funktion Ruft Informationen zu einem angegebenen Satz von Druckaufträgen für einen angegebenen Drucker ab. <br/>                                                                                                                |
| [**GetJob**](getjob.md)<br/>                                           | Die [**GetJob**](/windows/desktop/printdocs/getjob) -Funktion Ruft Informationen zu einem angegebenen Druckauftrag ab. <br/>                                                                                                                                                    |
| [**OpenPrinter**](openprinter.md)<br/>                                 | Die [**OpenPrinter**](/windows/desktop/printdocs/openprinter) -Funktion Ruft ein Handle für den angegebenen Drucker oder Druckserver oder andere Typen von Handles im Druck Subsystem ab. <br/>                                                                               |
| [**OpenPrinter2**](openprinter2.md)<br/>                               | Ruft ein Handle für den angegebenen Drucker, Druckserver oder andere Typen von Handles im Druck Subsystem ab, während einige der Druckeroptionen festgelegt werden.<br/>                                                                                      |
| [**Reportjobprocessingprogress**](reportjobprocessingprogress.md)<br/> | Meldet an den Druckspoolerdienst, ob sich ein XPS-Druckauftrag in der spoolingphase oder der Renderingphase befindet und welcher Teil der Verarbeitung derzeit ausgeführt wird.<br/>                                                                               |
| [**ScheduleJob**](schedulejob.md)<br/>                                 | Die [**schedulejob**](/windows/desktop/printdocs/schedulejob) -Funktion fordert an, dass der Druck Spooler einen angegebenen Druckauftrag zum Drucken plant. <br/>                                                                                                                |
| [**Setjob**](setjob.md)<br/>                                           | Mit der [**setjob**](/windows/desktop/printdocs/setjob) -Funktion wird ein Druckauftrag auf einem angegebenen Drucker angehalten, fortgesetzt, abgebrochen oder neu gestartet. Sie können auch die **setjob** -Funktion verwenden, um Druckauftrags Parameter festzulegen, z. b. die Druckauftrags Priorität und den Dokumentnamen. <br/> |
| [**StartDocPrinter**](startdocprinter.md)<br/>                         | Die Funktion [**StartDocPrinter**](/windows/desktop/printdocs/startdocprinter) benachrichtigt den Druck Spooler, dass ein Dokument zum Drucken gespoolt werden soll. <br/>                                                                                                           |
| [**Startpageprinter**](startpageprinter.md)<br/>                       | Die [**startpageprinter**](/windows/desktop/printdocs/startpageprinter) -Funktion benachrichtigt den Spooler, dass eine Seite auf dem angegebenen Drucker gedruckt werden soll. <br/>                                                                                                 |



 

## <a name="printer-user-interface-functions"></a>Funktionen der druckerbenutzerschnittstelle

Diese Funktionen zeigen eine Benutzeroberfläche an, die es dem Benutzer ermöglicht, einen Drucker auszuwählen oder zu konfigurieren.



| Funktion                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Advanceddocumentproperties**](advanceddocumentproperties.md)<br/> | Die [**advanceddocumentproperties**](/windows/desktop/printdocs/advanceddocumentproperties) -Funktion zeigt ein druckerkonfigurationsdialogfeld für den angegebenen Drucker an, sodass der Benutzer diesen Drucker konfigurieren kann. <br/>                                                                                                                                                      |
| [**Konfigurieren von Berichten**](configureport.md)<br/>                           | Die Funktion " [**Konfigurations Bericht**](/windows/desktop/printdocs/configureport) " zeigt das Dialogfeld Port-Konfiguration für einen Port auf dem angegebenen Server an. <br/>                                                                                                                                                                                                                     |
| [**Connecttoprinterdlg**](connecttoprinterdlg.md)<br/>               | Die [**connecttoprinterdlg**](/windows/desktop/printdocs/connecttoprinterdlg) -Funktion zeigt ein Dialogfeld an, mit dem Benutzer in einem Netzwerk nach Druckern suchen und eine Verbindung mit Ihnen herstellen können. Wenn der Benutzer einen Drucker auswählt, versucht die Funktion, eine Verbindung damit herzustellen. Wenn ein geeigneter Treiber nicht auf dem Server installiert ist, erhält der Benutzer die Möglichkeit, einen Drucker lokal zu erstellen. <br/> |
| [**Printerproperties**](printerproperties.md)<br/>                   | Die Funktion " [**printerproperties**](/windows/desktop/printdocs/printerproperties) " zeigt ein Eigenschaften Blatt "Druckereigenschaften" für den angegebenen Drucker an. <br/>                                                                                                                                                                                                                    |



 

## <a name="printer-functions"></a>Druckerfunktionen

Mit diesen Funktionen werden die Drucker, die der Druck Spooler verwendet, hinzugefügt und konfiguriert.



| Funktion                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abbruch Drucker**](abortprinter.md)<br/>                       | Die [**abortprinter**](/windows/desktop/printdocs/abortprinter) -Funktion löscht die Spooldatei eines Druckers, wenn der Drucker für das Spoolen konfiguriert ist. <br/>                                                                                                                                                                                                                                                                  |
| [**AddPrinter**](addprinter.md)<br/>                           | Die [**addprinter**](/windows/desktop/printdocs/addprinter) -Funktion fügt der Liste der unterstützten Drucker für einen angegebenen Server einen Drucker hinzu. <br/>                                                                                                                                                                                                                                                                       |
| [**"AddPrinterConnection"**](addprinterconnection.md)<br/>       | Die **addprconnection** -Funktion fügt dem angegebenen Drucker für den aktuellen Benutzer eine Verbindung hinzu. <br/>                                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection2**](addprinterconnection2.md)<br/>     | Fügt dem angegebenen Drucker eine Verbindung für den aktuellen Benutzer hinzu und gibt Verbindungsdetails an.<br/>                                                                                                                                                                                                                                                                                             |
| [**Deleteprinter**](deleteprinter.md)<br/>                     | Die [**deleteprinter**](/windows/desktop/printdocs/deleteprinter) -Funktion löscht das angegebene Drucker Objekt. <br/>                                                                                                                                                                                                                                                                                                    |
| [**Deleteprinterconnection**](deleteprinterconnection.md)<br/> | Die [**deleteprconnection**](/windows/desktop/printdocs/deleteprinterconnection) -Funktion löscht eine Verbindung zu einem Drucker, der durch einen [**AddPrinterConnection**](addprinterconnection.md) -oder [**connecttoprinterdlg**](connecttoprinterdlg.md)-Rückruf hergestellt wurde. <br/>                                                                                                                                      |
| [**Deleteprinterdata**](deleteprinterdata.md)<br/>             | Die [**deleteprinterdata**](/windows/desktop/printdocs/deleteprinterdata) -Funktion löscht die angegebenen Konfigurationsdaten für einen Drucker. Die Konfigurationsdaten eines Druckers bestehen aus einem Satz von benannten und typisierten Werten. Die **deleteprinterdata** -Funktion löscht einen dieser Werte, der durch den Wert Namen angegeben wird. <br/>                                                                                                     |
| [**Deleteprinterdataex**](deleteprinterdataex.md)<br/>         | Die [**deleteprinterdataex**](/windows/desktop/printdocs/deleteprinterdataex) -Funktion löscht einen angegebenen Wert aus den Konfigurationsdaten für einen Drucker. Die Konfigurationsdaten eines Druckers bestehen aus einem Satz benannter und typisierter Werte, die in einer Hierarchie von Registrierungs Schlüsseln gespeichert sind. Die-Funktion löscht einen angegebenen Wert unter einem angegebenen Schlüssel. <br/>                                                                        |
| [**Deleteprinterkey**](deleteprinterkey.md)<br/>               | Die [**deleteprinterkey**](/windows/desktop/printdocs/deleteprinterkey) -Funktion löscht einen angegebenen Schlüssel und alle zugehörigen Unterschlüssel für einen angegebenen Drucker. <br/>                                                                                                                                                                                                                                                               |
| [**Enumprinterdata**](enumprinterdata.md)<br/>                 | Die [**enumprinterdata**](/windows/desktop/printdocs/enumprinterdata) -Funktion Listet Konfigurationsdaten für einen angegebenen Drucker auf. <br/>                                                                                                                                                                                                                                                                               |
| [**Enumprinterdataex**](enumprinterdataex.md)<br/>             | Die [**enumprinterdataex**](/windows/desktop/printdocs/enumprinterdataex) -Funktion Listet alle Wertnamen und-Daten für einen angegebenen Drucker und Schlüssel auf. <br/>                                                                                                                                                                                                                                                             |
| [**Enumprinterkey**](enumprinterkey.md)<br/>                   | Die [**enumprinterkey**](/windows/desktop/printdocs/enumprinterkey) -Funktion Listet die Unterschlüssel eines angegebenen Schlüssels für einen angegebenen Drucker auf. <br/>                                                                                                                                                                                                                                                                     |
| [**Enumdrucker**](enumprinters.md)<br/>                       | Die [**enumprinter**](/windows/desktop/printdocs/enumprinters) -Funktion Listet verfügbare Drucker, Druckserver, Domänen oder Druckanbieter auf. <br/>                                                                                                                                                                                                                                                                 |
| [**Flushprinter**](flushprinter.md)<br/>                       | Die [**flushprinter**](/windows/desktop/printdocs/flushprinter) -Funktion sendet einen Puffer an den Drucker, um ihn aus einem vorübergehenden Zustand zu löschen. <br/>                                                                                                                                                                                                                                                                 |
| [**GetDefaultPrinter**](getdefaultprinter.md)<br/>             | Die [**GetDefaultPrinter**](/windows/desktop/printdocs/getdefaultprinter) -Funktion Ruft den Drucker Namen des Standard Druckers für den aktuellen Benutzer auf dem lokalen Computer ab. <br/>                                                                                                                                                                                                                                    |
| [**GetPrinter**](getprinter.md)<br/>                           | Die [**GetPrinter**](/windows/desktop/printdocs/getprinter) -Funktion Ruft Informationen zu einem angegebenen Drucker ab. <br/>                                                                                                                                                                                                                                                                                               |
| [**Getprinterdata**](getprinterdata.md)<br/>                   | Die [**getprinterdata**](/windows/desktop/printdocs/getprinterdata) -Funktion ruft Konfigurationsdaten für den angegebenen Drucker oder Druckserver ab. <br/>                                                                                                                                                                                                                                                                |
| [**Getprinterdataex**](getprinterdataex.md)<br/>               | Die [**getprinterdataex**](/windows/desktop/printdocs/getprinterdataex) -Funktion ruft Konfigurationsdaten für den angegebenen Drucker oder Druckserver ab. " **Getprinterdataex** " kann Werte abrufen, die von der Funktion " [**setprinterdata**](setprinterdata.md) " gespeichert werden. Außerdem kann **getprinterdataex** Werte abrufen, die unter einem angegebenen Schlüssel von der [**setprinterdataex**](setprinterdataex.md) -Funktion gespeichert sind. <br/> |
| [**Isvaliddevmode**](isvaliddevmode.md)<br/>                   | Die [**isvaliddevmode**](isvaliddevmode.md) -Funktion überprüft, ob der Inhalt einer DEVMODE-Struktur gültig ist. <br/>                                                                                                                                                                                                                                                                           |
| [**Lesen von Druckern**](readprinter.md)<br/>                         | Die Funktion "read [**Printer**](/windows/desktop/printdocs/readprinter) " Ruft Daten vom angegebenen Drucker ab. <br/>                                                                                                                                                                                                                                                                                                   |
| [**Resetprinter**](resetprinter.md)<br/>                       | Die [**resetprinter**](/windows/desktop/printdocs/resetprinter) -Funktion gibt die Werte für Datentyp und Geräte Modus an, die zum Drucken von Dokumenten verwendet werden, die von der [**StartDocPrinter**](startdocprinter.md) -Funktion gesendet werden. Diese Werte können überschrieben werden, indem die Funktion [**setjob**](setjob.md) verwendet wird, nachdem der Druck von Dokumenten begonnen wurde. <br/>                                                                  |
| [**Methode SetDefaultPrinter auf**](setdefaultprinter.md)<br/>             | Mit der Funktion " [**SetDefaultPrinter**](/windows/desktop/printdocs/setdefaultprinter) " wird der Druckername des Standard Druckers für den aktuellen Benutzer auf dem lokalen Computer festgelegt. <br/>                                                                                                                                                                                                                                         |
| [**SetPort**](setport.md)<br/>                                 | Die Funktion " [**setPort**](/windows/desktop/printdocs/setport) " legt den einem Druckerport zugeordneten Status fest. <br/>                                                                                                                                                                                                                                                                                                      |
| [**SetPrinter**](setprinter.md)<br/>                           | Die Funktion [**SetPrinter**](/windows/desktop/printdocs/setprinter) legt die Daten für einen angegebenen Drucker fest oder legt den Zustand des angegebenen Druckers fest, indem der Druckvorgang angehalten, der Druck fortgesetzt oder alle Druckaufträge gelöscht werden. <br/>                                                                                                                                                                                           |
| [**Setprinterdata**](setprinterdata.md)<br/>                   | Mit der [**setprinterdata**](/windows/desktop/printdocs/setprinterdata) -Funktion werden die Konfigurationsdaten für einen Drucker oder Druckserver festgelegt. <br/>                                                                                                                                                                                                                                                                             |
| [**Setprinterdataex**](setprinterdataex.md)<br/>               | Die Funktion [**setprinterdataex**](/windows/desktop/printdocs/setprinterdataex) legt die Konfigurationsdaten für einen Drucker oder Druckserver fest. Die-Funktion speichert die Konfigurationsdaten unter dem-Registrierungsschlüssel des Druckers. <br/>                                                                                                                                                                                            |
| [**"Write Printer"**](writeprinter.md)<br/>                       | Die Funktion " [**Write Printer**](writeprinter.md) " benachrichtigt den Druck Spooler, dass Daten in den angegebenen Drucker geschrieben werden sollen. <br/>                                                                                                                                                                                                                                                           |



 

## <a name="printer-change-notification-functions"></a>Benachrichtigungsfunktionen für Drucker Änderungen

Diese Funktionen ermöglichen es einer Anwendung, über Änderungen am Status eines Druckers benachrichtigt zu werden.



| Funktion                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Findcloseprinterchangenotifizierung**](findcloseprinterchangenotification.md)<br/> | Die Funktion [**findcloseprinterchangenotifischließt**](/windows/desktop/printdocs/findcloseprinterchangenotification) ein Änderungs Benachrichtigungs Objekt, das durch Aufrufen der [**findfirstprinterchangenotifizierungsfunktion**](findfirstprinterchangenotification.md) erstellt wurde. Der Drucker oder Druckserver, der dem Änderungs Benachrichtigungs Objekt zugeordnet ist, wird nicht mehr von diesem Objekt überwacht. <br/> |
| [**Findfirstprinterchangenotifizierung**](findfirstprinterchangenotification.md)<br/> | Die [**findfirstprinterchangenotifi-**](/windows/desktop/printdocs/findfirstprinterchangenotification) Funktion erstellt ein Änderungs Benachrichtigungs Objekt und gibt ein Handle für das-Objekt zurück. Anschließend können Sie dieses Handle in einem Rückruf einer der Wait-Funktionen verwenden, um Änderungen am Drucker oder Druckserver zu überwachen. <br/>                                                                              |
| [**Findnextprinterchangenotifizierung**](findnextprinterchangenotification.md)<br/>   | Die Funktion [**findnextprinterchangenotifiruft**](findnextprinterchangenotification.md) Informationen über die aktuellste Änderungs Benachrichtigung für ein Änderungs Benachrichtigungs Objekt ab, das einem Drucker oder Druckserver zugeordnet ist. Diese Funktion wird aufgerufen, wenn ein warte Vorgang für das Änderungs Benachrichtigungs Objekt erfüllt ist. <br/>                                           |
| [**Freiprinternotifyinfo**](freeprinternotifyinfo.md)<br/>                           | Die Funktion " [**freprinternotifyinfo**](/windows/desktop/printdocs/freeprinternotifyinfo) " gibt einen vom System zugewiesenen Puffer frei, der von der [**findnextprinterchangenotifi-**](findnextprinterchangenotification.md) Funktion erstellt wurde. <br/>                                                                                                                                                                |



 

## <a name="printer-form-functions"></a>Druckerformular-Funktionen

Diese Funktionen verwalten die von einem Drucker verwendeten Formulare.



| Funktion                                    | BESCHREIBUNG                                                                                                                                    |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddForm**](addform.md)<br/>       | Die [**AddForm**](/windows/desktop/printdocs/addform) -Funktion fügt der Liste der verfügbaren Formulare, die für den angegebenen Drucker ausgewählt werden können, ein Formular hinzu. <br/> |
| [**Deleteform**](deleteform.md)<br/> | Die [**deleteform**](/windows/desktop/printdocs/deleteform) -Funktion entfernt einen Formular Namen aus der Liste der unterstützten Formulare. <br/>                                |
| [**Enumforms**](enumforms.md)<br/>   | Die [**enumforms**](/windows/desktop/printdocs/enumforms) -Funktion Listet die Formulare auf, die vom angegebenen Drucker unterstützt werden. <br/>                               |
| [**GetForm**](getform.md)<br/>       | Die [**GetForm**](/windows/desktop/printdocs/getform) -Funktion Ruft Informationen zu einem angegebenen Formular ab. <br/>                                              |
| [**Setform**](setform.md)<br/>       | Die [**setform**](/windows/desktop/printdocs/setform) -Funktion legt die Formularinformationen für den angegebenen Drucker fest. <br/>                                       |



 

## <a name="print-spooler-functions"></a>Druckspoolerfunktionen

Diese Funktionen interagieren mit dem Druck Spooler auf niedriger Ebene.



| Funktion                                                          | BESCHREIBUNG                                                                                                                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Closespoolfilehandle**](closespoolfilehandle.md)<br/>   | Die [**closespoolfilehandle**](/windows/desktop/printdocs/closespoolfilehandle) -Funktion schließt ein Handle für eine Spooldatei, die dem gerade von der Anwendung übermittelten Druckauftrag zugeordnet ist. <br/>                    |
| [**Commitspooldata**](commitspooldata.md)<br/>             | Die [**commitspooldata**](/windows/desktop/printdocs/commitspooldata) -Funktion benachrichtigt den Druck Spooler, dass eine angegebene Datenmenge in eine angegebene Spooldatei geschrieben wurde und zum Rendern bereit ist. <br/> |
| [**Getprintexecutiondata**](getprintexecutiondata.md)<br/> | [**Getprintexecutiondata**](getprintexecutiondata.md) Ruft den aktuellen Druck Kontext ab.<br/>                                                                                             |
| [**Getspoolfilehandle**](getspoolfilehandle.md)<br/>       | Die [**getspoolfilehandle**](/windows/desktop/printdocs/getspoolfilehandle) -Funktion Ruft ein Handle für die Spooldatei ab, die dem derzeit von der Anwendung übermittelten Auftrag zugeordnet ist. <br/>                        |



 

 

