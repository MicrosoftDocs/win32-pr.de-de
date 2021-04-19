---
description: Listet die in Windows Vista eingeführten Druck-APIs (Application Programming Interface) auf.
ms.assetid: 7a4eb5d7-b37d-4090-aea4-7274daa1e15c
title: Neues beim Drucken in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8648d57f48623e6db0f6311bb07ae24ac15d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362555"
---
# <a name="whats-new-for-printing-in-windows-vista"></a>Neues beim Drucken in Windows Vista

Listet die in Windows Vista eingeführten Druck-APIs (Application Programming Interface) auf.

Die folgenden Funktionen und Enumerationen werden zum Verwalten von Druck Tickets verwendet.



| Funktion                                                               | BESCHREIBUNG                                                                                                                                   | Header    | Bibliothek     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-----------|-------------|
| [**Ptconvertprintticketdedevmode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) | Konvertiert ein Druck Ticket in eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur.                                                                            | Prntvpt. h | "Prntvpt. lib" |
| [**Ptconvertdevmodetoprintticket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) | Konvertiert einen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) in ein Druck Ticket.                                                                                      | Prntvpt. h | "Prntvpt. lib" |
| [**Ptreleasememory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)                             | Gibt Puffer frei, die von bestimmten Funktionen der Druck Ticket Verwaltung erstellt wurden.                                                                        | Prntvpt. h | "Prntvpt. lib" |
| [**Ptmergeandvalidateprintticket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) | Überprüft zwei Druck Tickets und führt Sie zu einem funktionierenden Druck Ticket zusammen.                                                                            | Prntvpt. h | "Prntvpt. lib" |
| [**Ptgetprint-Funktionen**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)               | Ruft ein Konto für die Funktionen des Druckers ab.                                                                                                | Prntvpt. h | "Prntvpt. lib" |
| [**Ptopenprovider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)                               | Öffnet einen Druck ticketanbieter.                                                                                                                | Prntvpt. h | "Prntvpt. lib" |
| [**Ptopzuproviderex**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)                           | Öffnet einen Druck ticketanbieter, auch wenn er die bevorzugte Version des [Druck Schemas](./print-schema.md)nicht unterstützt. | Prntvpt. h | "Prntvpt. lib" |
| [**Ptcloseprovider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)                             | Schließt einen Druck ticketanbieter.                                                                                                               | Prntvpt. h | "Prntvpt. lib" |
| [**Ptqueryschemaversionsupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)     | Ruft die neueste Version des [Druck Schemas](./print-schema.md) ab, das ein angegebener Drucker unterstützt.                        | Prntvpt. h | "Prntvpt. lib" |



 



| Enumeration                                        | BESCHREIBUNG                                                                                                                                                                               | Header    |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**Edefaultdevmodetype**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) | Ermöglicht es Aufrufern, anzugeben, welcher [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) als Quelle von Standardwerten verwendet wird, wenn ein Druck Ticket nicht alle Einstellungen angibt, die sich möglicherweise in einem **DEVMODE-Modus** befinden. | Prntvpt. h |
| [**Eprintticketscope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope)     | Gibt den Bereich eines Druck Tickets an.                                                                                                                                                    | Prntvpt. h |



 

Die folgenden Funktionen werden verwendet, um Druckertreiber zu installieren.



| Funktion                                                                   | BESCHREIBUNG                                                                                                                                                                 | Header     | Bibliothek      |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**Coreprinterdriverinstalliert**](coreprinterdriverinstalled.md)           | Meldet, ob ein Kern Druckertreiber mit angegebener GUID, Datum und Version installiert ist.                                                                                | Winspool. h | Winspool. lib |
| [**Deleteprinterdriverpackage**](deleteprinterdriverpackage.md)           | Löscht ein Druckertreiber Paket aus dem Treiber Speicher.                                                                                                                     | Winspool. h | Winspool. lib |
| [**Getcoreprinterdrivers**](getcoreprinterdrivers.md)                     | Ruft die GUID, Version und das Datum der angegebenen Haupt Druckertreiber und den Pfad zu ihren Paketen ab.                                                                      | Winspool. h | Winspool. lib |
| [**GetPrinterDriverPackagePath**](getprinterdriverpackagepath.md)         | Ruft den Pfad zum angegebenen Druckertreiber Paket auf einem Druckserver ab.                                                                                                    | Winspool. h | Winspool. lib |
| [**Installprinterdriverfrompackage**](installprinterdriverfrompackage.md) | Installiert einen Druckertreiber aus einem Treiber Paket im Treiber Speicher des Druck Servers.                                                                                         | Winspool. h | Winspool. lib |
| [**Uploadprinterdriverpackage**](uploadprinterdriverpackage.md)           | Lädt einen Druckertreiber in den Treiber Speicher eines Druck Servers hoch, damit er mit [**installprinterdriverfrompackage**](installprinterdriverfrompackage.md)installiert werden kann. | Winspool. h | Winspool. lib |



 

Die folgenden Funktionen, Enumerationen und Strukturen werden zum Drucken und zum Verwalten von Druckern und Drucker Verbindungen verwendet.



| Funktion                                               | BESCHREIBUNG                                                                                                                                              | Header     | Bibliothek      |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**AddPrinterConnection2**](addprinterconnection2.md) | Fügt dem angegebenen Drucker eine Verbindung für den aktuellen Benutzer hinzu.                                                                                         | Winspool. h | Winspool. lib |
| [**OpenPrinter2**](openprinter2.md)                   | Ruft ein Handle für den angegebenen Drucker oder Druckserver oder andere Typen von Handles im Druck Subsystem ab, während einige der Druckeroptionen festgelegt werden. | Winspool. h | Winspool. lib |



 



| Enumeration                                            | BESCHREIBUNG                                                                                       | Header     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------|------------|
| [**\_druckeroptionsflags \_**](printer-option-flags.md) | Gibt das Caching eines Handles für einen mit [**OpenPrinter2**](openprinter2.md)geöffneten Drucker an. | Winspool. h |



 



| Struktur                                                         | BESCHREIBUNG                                                                            | Header     |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------|
| [**Kern \_ Drucker \_ Treiber**](core-printer-driver.md)              | Stellt einen Druckertreiber dar, von dem andere Druckertreiber abhängig sind.              | Winspool. h |
| [**Treiber \_ Informationen \_ 8**](driver-info-8.md)                          | Stellt einen Druckertreiber dar.                                                           | Winspool. h |
| [**Formular \_ Informationen \_ 2**](form-info-2.md)                              | Stellt Informationen über ein Lokalisier bares Druckformular dar.                                 | Winspool. h |
| [**Auftrags \_ Informationen \_ 4**](job-info-4.md)                                | Stellt einen vollständigen Satz von Werten dar, die einem Auftrag zugeordnet sind und 64-Bit-Spooldateien unterstützt | Winspool. h |
| [**Drucker \_ Verbindungs \_ Informationen \_ 1**](printer-connection-info-1.md) | Stellt Informationen zu einer Verbindung mit einem Drucker dar.                                | Winspool. h |
| [**Drucker \_ Optionen**](printer-options.md)                       | Stellt Druckeroptionen dar.                                                            | Winspool. h |
| [**PrintProcessor- \_ Caps \_ 2**](printprocessor-caps-2.md)          | Stellt Drucker Funktions Informationen dar.                                             | Winspool. h |



 

Die folgenden Funktionen, Enumerationen und Schnittstellen werden verwendet, um ein neues asynchrones Druck Benachrichtigungssystem zu implementieren.



| Funktion                                                                             | BESCHREIBUNG                                                                                                                                                                                       | Header     | Bibliothek      |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**"Kreateprintasyncnotifychannel"**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)               | Erstellt einen Kommunikationskanal zwischen der Druckkomponente des Spoolers, wie z. b. einen Druckertreiber oder einen Port Monitor, und eine Anwendung, die Benachrichtigungen von der Komponente empfangen muss. | Prnasnot. h | Winspool. lib |
| [**Registerforprintasyncbenachrichtigungen**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)     | Registriert eine Anwendung zum Empfangen von Benachrichtigungen von Spooler-gehosteten Komponenten, z. b. Druckertreibern, Druck Prozessoren und Port Monitoren.                                                    | Prnasnot. h | Winspool. lib |
| [**Unregisterforprintasyncnotification**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications) | Ermöglicht es einer Anwendung, die registriert hat, Benachrichtigungen von Spooler-gehosteten Druckkomponenten zu empfangen, um das Abonnement der Benachrichtigungen zu beenden.                                         | Prnasnot. h | Winspool. lib |



 



| Enumeration                                                                    | BESCHREIBUNG                                                                                                                                                                                                          | Header     |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| [**Printasyncnotifyconversation-Stil**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle) | Gibt an, ob die Kommunikation zwischen Anwendungen und Druck Spoolern, die gehostet werden, z. b. Druckertreiber, Druck Prozessoren und Port Monitore, bidirektional oder unidirektional ist.                          | Prnasnot. h |
| [**Printasyncnotifyerror**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)                         | Gibt einen Fehler in einer asynchronen Benachrichtigungs Transaktion an.                                                                                                                                                      | Prnasnot. h |
| [**Printasyncnotif yuserfilter**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)               | Gibt an, ob Benachrichtigungen nur an Abhör Anwendungen gesendet werden, die dem gleichen Benutzer wie der vom Druck Spooler gehostete Absender zugeordnet sind, oder ob Sie zu einem umfassenderen Satz von lauschenden Anwendungen wechseln. | Prnasnot. h |



 



| Schnittstelle und Methode                                                                                                      | BESCHREIBUNG                                                                                                                                                   | Header     | Bibliothek      |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**Iprintasyncnotifycallback:: channelclosed**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-channelclosed)    | Wird von einem Member eines Kommunikationskanals verwendet, um das andere Mitglied zu informieren, dass der Kanal geschlossen wird.                                                    | Prnasnot. h | Winspool. lib |
| [**Iprintasyncnotifycallback:: oneventnotify**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-oneventnotify)    | Wird vom Druck Spooler aufgerufen, um einen Listener zu warnen, dass eine Benachrichtigung auf einem angegebenen Kanal verfügbar ist.                                                      | Prnasnot. h | Winspool. lib |
| [**Iprintasyncnotifychannel:: closechannel**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-closechannel)         | Schließt einen Kommunikationskanal.                                                                                                                               | Prnasnot. h | Winspool. lib |
| [**Iprintasyncnotifychannel:: SendNotification**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-sendnotification) | Sendet eine Benachrichtigung von einer-Druck Spooler-gehosteten Komponente an eine oder mehrere abzurufende Anwendungen oder sendet eine Antwort von einer Anwendung zurück an eine-Komponente. | Prnasnot. h | Winspool. lib |
| [**Iprintasyncnotifydataobject:: acquiredata**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-acquiredata)  | Verweist auf die Benachrichtigungs Daten sowie auf die Größe und den Typ der Daten.                                                                   | Prnasnot. h | Winspool. lib |
| [**Iprintasyncnotifydataobject:: ReleaseData**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-releasedata)  | Gibt den Speicher frei, der von den Daten verwendet wird, die in [**iprintasyncnotifydataobject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)gekapselt sind.                                  | Prnasnot. h | Winspool. lib |



 

Die folgenden Enumerationen und Strukturen werden zum Aufrufen von Microsoft XPS Document Converter (mxdc) verwendet, der XML Paper Specification (XPS)-Dokumente in ein Gerät oder eine Datei schreibt.



| Enumeration                                | BESCHREIBUNG                                                            | Header |
|--------------------------------------------|------------------------------------------------------------------------|--------|
| [**MxdcS0PageEnums**](mxdcs0pageenums.md) | Gibt Typen von Ressourcen, z. b. Schriftarten oder Bilder, auf einer XPS-Seite an. | Mxdc. h |



 



| Struktur                                                          | BESCHREIBUNG                                                                                                                                    | Header |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| [**Mxdcescapeheader**](mxdcescapeheader.md)                       | Stellt eine Anweisung für den mxdc dar.                                                                                                         | Mxdc. h |
| [**Mxdcgetdateinamedata**](mxdcgetfilenamedata.md)                 | Stellt den vollständigen Pfad und Namen für eine mxdc-Ausgabedatei dar.                                                                                     | Mxdc. h |
| [**Mxdcprintticketescape**](mxdcprintticketescape.md)             | Stellt eine Kombination aus [**mxdcescapeheader**](mxdcescapeheader.md) und [**mxdcprintticketpassthrough**](mxdcprintticketpassthrough.md)dar. | Mxdc. h |
| [**Mxdcprintticketpassthrough**](mxdcprintticketpassthrough.md)   | Stellt ein Druck Ticket dar, das einem XPS-Dokument zugeordnet wird.                                                                        | Mxdc. h |
| [**MxdcS0PageData**](mxdcs0pagedata.md)                           | Stellt eine XPS-formatierte Seite dar, die ohne Verarbeitung an die mxdc-Ausgabedatei übermittelt werden soll.                                                  | Mxdc. h |
| [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) | Stellt eine Kombination aus [**mxdcescapeheader**](mxdcescapeheader.md) und [**MxdcS0PageData**](mxdcs0pagedata.md)dar.                         | Mxdc. h |
| [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md)       | Stellt eine Kombination aus [**mxdcescapeheader**](mxdcescapeheader.md) und [**MxdcS0PageResource**](mxdcs0pageresourceescape.md)dar.           | Mxdc. h |
| [**MxdcS0PageResource**](mxdcs0pageresourceescape.md)             | Stellt eine Ressource, z. b. eine Schriftart oder ein Bild, dar, die von mxdc auf einer XPS-Seite enthalten ist.                                                   | Mxdc. h |



 

 

 
