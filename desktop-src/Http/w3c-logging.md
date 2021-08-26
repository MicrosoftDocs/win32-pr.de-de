---
title: W3C-Protokollierung
description: Die erweiterte W3C-Protokollierung ist eine Art der serverseitigen Protokollierung, die für die Serversitzung oder URL-Gruppe aktiviert werden kann.
ms.assetid: a08b8f9e-2247-43c6-b253-81f72001d8d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa67d2e0141dfb936ea44070479560ca90e9c3720db8ffebedf5af20b0442dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078300"
---
# <a name="w3c-logging"></a>W3C-Protokollierung

Die erweiterte W3C-Protokollierung ist eine Art der serverseitigen Protokollierung, die für die Serversitzung oder URL-Gruppe aktiviert werden kann. Wenn die W3C-Protokollierung für eine URL-Gruppe aktiviert ist, wird die Protokollierung nur für Anforderungen ausgeführt, die an die URL-Gruppe weitergeleitet werden. Für jede URL-Gruppe, die für die Aktivierung der W3C-Protokollierung konfiguriert ist, wird eine separate Protokolldatei erstellt.

Wenn die W3C-Protokollierung in der Serversitzung aktiviert ist, fungiert sie als zentralisierte Form der Protokollierung für alle URL-Gruppen unter der Serversitzung. Eine einzelne Protokolldatei wird für alle URL-Gruppen in der Serversitzung verwaltet.

In der folgenden Tabelle sind die Felder aufgeführt, die von der HTTP-Server-API protokolliert werden können. Die Tabelle enthält eine Teilmenge der [**HTTP \_ LOG FIELD-Konstanten. \_**](http-log-field--constants.md) Einige der unten aufgeführten Felder werden von der HTTP-Server-API intern automatisch generiert und sind daher nicht in der [**HTTP \_ LOG FIELDS \_ \_ DATA-Struktur**](/windows/desktop/api/Http/ns-http-http_log_fields_data) enthalten. Die Spalte "Wird angezeigt als" enthält den Text, der in der Protokolldatei angezeigt wird. Die Daten in der Tabelle werden in der Reihenfolge des Auftretens im Protokolldateidatensatz angezeigt.

Felder, die nicht als "HTTP-Server-API generiert" gekennzeichnet sind, müssen innerhalb der [**HTTP \_ LOG FIELDS \_ \_ DATA-Struktur**](/windows/desktop/api/Http/ns-http-http_log_fields_data) nach Anwendung übergeben werden. Die Anwendung könnte diese Felder aus der [**HTTP \_ REQUEST-Struktur**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) generieren, die an sie übergeben wird.



| Feld                            | Wird als angezeigt.      | Beschreibung                                                                                                                                | HTTP \_ LOG \_ FIELDS \_ DATA Member | HTTP \_ LOG \_ FIELDS-Konstanten      |
|----------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|----------------------------------|
| Datum                             | Datum            | Das Datum, an dem die Aktivität aufgetreten ist.                                                                                                   | HTTP-Server-API generiert.     | \_DATUM DES HTTP-PROTOKOLLFELDS \_ \_           |
| Zeit                             | time            | Die Zeit in koordinierter Weltzeit (UTC), zu der die Aktivität aufgetreten ist.                                                             | HTTP-Server-API generiert.     | FELDZEIT \_ DES HTTP-PROTOKOLLS \_ \_           |
| Dienstname und Instanznummer | s-sitename      | Der Internetdienstname und die Instanznummer, die auf dem Client ausgeführt wurden.                                                              | Dienstname                    | WEBSITENAME \_ DES HTTP-PROTOKOLLFELDS \_ \_ \_     |
| Servername                      | s-computername  | Der Name des Servers, auf dem der Protokolldateieintrag generiert wurde.                                                                          | ServerName                     | COMPUTERNAME \_ DES HTTP-PROTOKOLLFELDS \_ \_ \_ |
| Server-IP-Adresse                | s-ip            | Die IP-Adresse des Servers, auf dem der Protokolldateieintrag generiert wurde.                                                                    | ServerIp                       | \_IP DES HTTP-PROTOKOLLFELDSERVERS \_ \_ \_     |
| Methode                           | cs-method       | Das angeforderte Verb, z. B. eine GET-Methode.                                                                                             | Methode                         | HTTP \_ LOG \_ \_ FIELD-METHODE         |
| URI-Stamm                         | cs-uri-stem     | Das Ziel des Verbs, z. B. Default.htm.                                                                                          | UriStem                        | HTTP \_ LOG \_ FIELD \_ URI \_ STEM      |
| URI-Abfrage                        | cs-uri-query    | Die Abfrage, sofern vorhanden, die der Client ausführen wollte. Eine Abfrage-URI (Universal Resource Identifier) ist nur für dynamische Seiten erforderlich. | UriQuery                       | HTTP \_ LOG \_ FIELD \_ URI \_ QUERY     |
| Serverport                      | s-port          | Die Serverportnummer, die für den Dienst konfiguriert ist.                                                                                 | ServerPort                     | HTTP \_ LOG \_ FIELD \_ SERVER \_ PORT   |
| Benutzername                        | cs-username     | Der Name des authentifizierten Benutzers, der auf den Server zugegriffen hat. Anonyme Benutzer werden durch einen Bindestrich gekennzeichnet.                                    | UserName                       | \_BENUTZERNAME DES HTTP-PROTOKOLLFELDS \_ \_ \_     |
| Client IP Address                | c-ip            | Die IP-Adresse des Clients, der die Anforderung gestellt hat.                                                                                        | ClientIp                       | CLIENT-IP DES \_ HTTP-PROTOKOLLFELDS \_ \_ \_     |
| Protokollversion                 | cs-version      | Die vom Client verwendete HTTP-Protokollversion.                                                                                            | HTTP-Server-API generiert.     | VERSION \_ DES HTTP-PROTOKOLLFELDS \_ \_        |
| Benutzer-Agent                       | cs(User-Agent)  | Der vom Client verwendete Browsertyp                                                                                                     | UserAgent                      | HTTP \_ LOG \_ FIELD \_ USER \_ AGENT    |
| Cookie                           | cs(Cookie)      | Der Inhalt des gesendeten oder empfangenen Cookies, sofern vorhanden.                                                                                        | Cookie                         | HTTP \_ LOG \_ FIELD \_ COOKIE         |
| Referrer                         | cs(Referrer)    | Die Website, die der Benutzer zuletzt besucht hat. Diese Website stellte eine Verknüpfung zur aktuellen Website her.                                                        | Referrer                       | HTTP \_ LOG \_ FIELD \_ REFERRER       |
| Host                             | cs-host         | Der Hostheadername, sofern dieser enthalten ist.                                                                                                              | Host                           | \_ \_ HTTP-PROTOKOLLFELDHOST \_           |
| HTTP-Status                      | sc-status       | Der HTTP-Statuscode.                                                                                                                      | ProtocolStatus                 | \_ \_ HTTP-PROTOKOLLFELDSTATUS \_         |
| Protokollunterstatus               | sc-substatus    | Der Unterstatusfehlercode.                                                                                                                  | SubStatus                      | UNTERSTATUS \_ DES \_ \_ HTTP-PROTOKOLLFELDS \_    |
| Win32-Status                     | sc-win32-status | Der Windows Statuscode.                                                                                                                   | Win32Status                    | STATUS DES \_ \_ \_ HTTP-PROTOKOLLFELDS WIN32 \_  |
| Gesendete Bytes                       | sc-bytes        | Die Anzahl der vom Server gesendeten Bytes.                                                                                                    | HTTP-Server-API generiert.     | GESENDETE \_ \_ HTTP-PROTOKOLLFELDBYTES \_ \_    |
| Empfangene Bytes                   | cs-bytes        | Die Anzahl der vom Server empfangenen und verarbeiteten Bytes.                                                                                  | HTTP-Server-API generiert.     | HTTP \_ LOG \_ FIELD \_ BYTES \_ RECV    |
| Benötigte Zeit                       | Zeit in Rechnung      | Die Dauer der Aktion in Millisekunden.                                                                                  | HTTP-Server-API generiert.     | HTTP \_ LOG \_ FIELD \_ TIME \_ TAKEN    |
| Stream-ID                      | streamid          | Die Stream-ID.                                                                                  | HTTP-Server-API generiert.     | \_ \_ \_ HTTP-PROTOKOLLFELD-STREAM-ID \_       |



 

Die Protokolldatei ist ein anpassbares textbasiertes ASCII-Format. Die Feldpräfixe in der Datei sind wie folgt definiert:

| Präfix    | BESCHREIBUNG                          |
|-----|---------------------------|
| s   | Serveraktionen.           |
| c   | Clientaktionen.           |
| Sc  | Server-zu-Client-Aktionen. |
| cs  | Client-zu-Server-Aktionen. |



 

Die Anwendung kann eines oder mehrere der Felder der erweiterten W3C-Protokolldatei auswählen, aber nicht alle Felder enthalten Informationen. Bei Feldern, die ausgewählt sind, für die jedoch keine Informationen enthalten sind, wird ein Bindestrich (-) als Platzhalter angezeigt. Wenn ein Feld ein nicht druckbares Zeichen enthält, ersetzt die HTTP-Server-API es durch ein Pluszeichen (+), um das Protokolldateiformat zu erhalten. Dies tritt in der Regel bei Virenangriffen auf, wenn beispielsweise ein böswilliger Benutzer Wagenrücklauf- und Zeilenfeeds sendet, die das Protokolldateiformat nicht durch das Pluszeichen (+) ersetzen würden. Felder werden durch Leerzeichen getrennt.

Wenn ein Feld von der URL-Gruppe oder Serversitzung aktiviert, aber nicht für die Anforderung ausgewählt wurde, wird es in der Protokolldatei mit einem Bindestrich (-) als Platzhalter angezeigt.

Protokolldateien werden erstellt, wenn die erste Anforderung in der URL-Gruppe oder Serversitzung eintrifft. Sie werden bei der Konfiguration der Protokollierung nicht erstellt. Das folgende Beispiel zeigt den ersten Protokolldateieintrag für eine W3C-Protokolldatei mit aktivierten Feldern "Client-IP", "Benutzername", "Server-IP", "Serverport", "Methode", "URI-Stamm", "URI-Abfrage", "Status" und "Benutzer-Agent":

``` syntax
#Software: Microsoft HTTP Server API 2.0  
#Version: 1.0   // the log file version as it's described by "https://www.w3.org/TR/WD-logfile".
#Date: 2002-05-02 17:42:15  // when the first log file entry was recorded, which is when the entire log file was created.
#Fields: date time c-ip cs-username s-ip s-port cs-method cs-uri-stem cs-uri-query sc-status cs(User-Agent)
2002-05-02 17:42:15 172.22.255.255 - 172.30.255.255 80 GET /images/picture.jpg - 200 Mozilla/4.0+(compatible;MSIE+5.5;+Windows+2000+Server)
```

Das Zeitfeld wird initialisiert, wenn die HTTP-Server-API das erste Byte empfängt, bevor die Anforderung analysiert wird. Der zeitbasierte Zeitstempel wird beendet, wenn der letzte Sendeabschluss erfolgt. Die zeitbasierte Zeit spiegelt nicht die Zeit im gesamten Netzwerk wider. Die erste Anforderung an die Website zeigt eine etwas längere Zeit als andere ähnliche Anforderungen an, da die HTTP-Server-API die Protokolldatei mit der ersten Anforderung öffnet.

 

 