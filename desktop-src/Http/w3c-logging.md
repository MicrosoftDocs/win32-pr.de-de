---
title: W3C-Protokollierung
description: Die erweiterte W3C-Protokollierung ist der Typ der serverseitigen Protokollierung, die für die Server Sitzung oder URL-Gruppe aktiviert werden kann.
ms.assetid: a08b8f9e-2247-43c6-b253-81f72001d8d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b253daebae22a2b99e152451cff360c7b633ca64
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724832"
---
# <a name="w3c-logging"></a>W3C-Protokollierung

Die erweiterte W3C-Protokollierung ist der Typ der serverseitigen Protokollierung, die für die Server Sitzung oder URL-Gruppe aktiviert werden kann. Wenn die W3C-Protokollierung für eine URL-Gruppe aktiviert ist, wird die Protokollierung nur bei Anforderungen ausgeführt, die an die URL-Gruppe weitergeleitet werden. Es wird eine separate Protokolldatei für jede URL-Gruppe erstellt, die für die W3C-Protokollierung konfiguriert ist.

Wenn die W3C-Protokollierung für die Server Sitzung aktiviert ist, fungiert sie als zentralisierte Form der Protokollierung für alle URL-Gruppen in der Server Sitzung. Für alle URL-Gruppen in der Server Sitzung wird eine einzelne Protokolldatei verwaltet.

In der folgenden Tabelle sind die Felder aufgeführt, die von der HTTP-Server-API protokolliert werden können. Die Tabelle enthält eine Teilmenge der [**http- \_ Protokoll \_ Feld**](http-log-field--constants.md) Konstanten. Einige der unten aufgeführten Felder werden intern automatisch von der HTTP-Server-API generiert und sind daher nicht in der Datenstruktur der [**http- \_ Protokoll \_ Felder \_**](/windows/desktop/api/Http/ns-http-http_log_fields_data) enthalten. Die Spalte "wird als" enthält den Text, der in der Protokolldatei angezeigt wird. Die Daten in der Tabelle befinden sich in der Reihenfolge der Vorkommen im Protokolldatei Daten Satz.

Felder, die nicht als "http-Server-API generiert" gekennzeichnet sind, müssen in der [**http- \_ Protokoll \_ Felder- \_ Daten**](/windows/desktop/api/Http/ns-http-http_log_fields_data) Struktur nach Anwendung übermittelt werden. Die Anwendung könnte diese Felder aus der [**http- \_ Anforderungs**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) Struktur generieren, die an Sie übermittelt wird.



| Feld                            | Angezeigt als      | BESCHREIBUNG                                                                                                                                | HTTP- \_ Protokoll \_ Felder- \_ Datenmember | HTTP- \_ Protokoll \_ Felder Konstanten      |
|----------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|----------------------------------|
| Datum                             | Datum            | Das Datum, an dem die Aktivität aufgetreten ist.                                                                                                   | Die HTTP Server-API wurde generiert.     | \_ \_ Feld \_ Datum des HTTP-Protokolls           |
| Time                             | time            | Die Uhrzeit in koordinierter Weltzeit (UTC), zu der die Aktivität aufgetreten ist.                                                             | Die HTTP Server-API wurde generiert.     | \_ \_ Feld \_ Zeit für HTTP-Protokoll           |
| Dienst Name und Instanznummer | s-Sitename      | Der Internet Dienst Name und die Instanznummer, die auf dem Client ausgeführt wurden.                                                              | Dienstname                    | HTTP- \_ Protokoll \_ Feld- \_ Website \_ Name     |
| Servername                      | s-Computername  | Der Name des Servers, auf dem der Protokolldatei Eintrag generiert wurde.                                                                          | ServerName                     | Computer Name für HTTP- \_ Protokoll \_ Feld \_ \_ |
| Server-IP-Adresse                | s-IP            | Die IP-Adresse des Servers, auf dem der Protokolldatei Eintrag generiert wurde.                                                                    | ServerIp                       | HTTP \_ \_ -Protokollfeld \_ Server \_ -IP     |
| Methode                           | CS-Methode       | Das angeforderte Verb, z. b. eine Get-Methode.                                                                                             | Methode                         | HTTP- \_ Protokoll \_ Feld \_ Methode         |
| URI-Stamm                         | CS-URI-stem     | Das Ziel des Verbs, z. b. Default.htm.                                                                                          | UriStem                        | URI-Stamm des HTTP- \_ Protokoll \_ Felds \_ \_      |
| URI-Abfrage                        | CS-URI-Query    | Die Abfrage, die der Client auszuführen versucht hat, falls vorhanden. Eine Abfrage-URI (Universal Resource Identifier) ist nur für dynamische Seiten erforderlich. | UriQuery                       | URI-Abfrage für HTTP- \_ Protokoll \_ Feld \_ \_     |
| Serverport                      | s-Port          | Die für den Dienst konfigurierte Server Portnummer.                                                                                 | ServerPort                     | HTTP- \_ Protokoll \_ Feld- \_ \_ Serverport   |
| Benutzername                        | cs-username     | Der Name des authentifizierten Benutzers, der auf den Server zugegriffen hat. Anonyme Benutzer werden durch einen Bindestrich gekennzeichnet.                                    | UserName                       | Benutzer Name für das HTTP- \_ Protokoll \_ Feld \_ \_     |
| Client IP Address                | c-ip            | Die IP-Adresse des Clients, der die Anforderung gestellt hat.                                                                                        | ClientIp                       | HTTP \_ \_ -Protokollfeld \_ Client \_ -IP     |
| Protokoll Version                 | CS-Version      | Die vom Client verwendete HTTP-Protokollversion.                                                                                            | Die HTTP Server-API wurde generiert.     | HTTP- \_ Protokoll \_ Feld \_ Version        |
| Benutzer-Agent                       | CS (Benutzer-Agent)  | Der vom Client verwendete Browsertyp                                                                                                     | UserAgent                      | HTTP- \_ Protokoll \_ Feld Benutzer- \_ \_ Agent    |
| Cookie                           | CS (Cookie)      | Der Inhalt des gesendeten oder empfangenen Cookies, sofern vorhanden.                                                                                        | Cookie                         | HTTP- \_ Protokoll \_ Feld \_ Cookie         |
| Referrer                         | CS (Referrer)    | Die Website, die der Benutzer zuletzt besucht hat. Diese Website stellte eine Verknüpfung zur aktuellen Website her.                                                        | Referrer                       | Verweis auf http- \_ Protokoll \_ Feld \_       |
| Host                             | CS-Host         | Der Host Header Name (sofern vorhanden).                                                                                                              | Host                           | HTTP- \_ Protokoll \_ Feld \_ Host           |
| HTTP-Status                      | SC-Status       | Der HTTP-Statuscode.                                                                                                                      | ProtocolStatus                 | Status des HTTP- \_ Protokoll \_ Felds \_         |
| Protokoll unter Status               | SC-unter Status    | Der unter Status-Fehlercode.                                                                                                                  | SubStatus                      | unter Status des HTTP- \_ Protokoll \_ Felds \_ \_    |
| Win32-Status                     | SC-Win32-Status | Der Windows-Statuscode.                                                                                                                   | Win32Status                    | Win32-Status des HTTP- \_ Protokoll \_ Felds \_ \_  |
| Gesendete Bytes                       | SC-bytes        | Die Anzahl der vom Server gesendeten Bytes.                                                                                                    | Die HTTP Server-API wurde generiert.     | \_gesendete HTTP-Protokoll \_ Feld \_ Bytes \_    |
| Empfangene Bytes                   | CS-bytes        | Die Anzahl von Bytes, die vom Server empfangen und verarbeitet wurden.                                                                                  | Die HTTP Server-API wurde generiert.     | HTTP- \_ Protokoll \_ Feld ( \_ Bytes \_ )    |
| Benötigte Zeit                       | Zeit      | Die Dauer der Aktion in Millisekunden.                                                                                  | Die HTTP Server-API wurde generiert.     | Zeit für das HTTP- \_ Protokoll \_ Feld \_ \_    |
| Stream-ID                      | streamid          | Die Datenstrom-ID.                                                                                  | Die HTTP Server-API wurde generiert.     | HTTP- \_ Protokoll \_ Feld-Stream- \_ \_ ID       |



 

Die Protokolldatei ist ein anpassbares, textbasiertes ASCII-Format. Die Feld Präfixe in der Datei werden wie folgt definiert:

|     |                           |
|-----|---------------------------|
| s   | Server Aktionen.           |
| c   | Client Aktionen.           |
| SC  | Server-zu-Client-Aktionen. |
| cs  | Client-zu-Server-Aktionen. |



 

Die Anwendung kann eine oder mehrere der erweiterten W3C-Protokolldatei Felder auswählen, aber nicht alle Felder enthalten Informationen. Für Felder, die ausgewählt wurden, für die jedoch keine Informationen vorhanden sind, wird ein Bindestrich (-) als Platzhalter angezeigt. Wenn ein Feld ein nicht druckbares Zeichen enthält, wird es von der HTTP-Server-API durch ein Pluszeichen (+) ersetzt, um das Protokolldatei Format beizubehalten. Dies tritt in der Regel bei Virenangriffen auf, wenn z. b. ein böswilliger Benutzer Wagen Rückläufe und Zeilen Feeds sendet, die, wenn Sie nicht durch das Pluszeichen (+) ersetzt werden, das Protokolldatei Format sprengen würden. Felder werden durch Leerzeichen voneinander getrennt.

Wenn ein Feld von der URL-Gruppe oder der Server Sitzung aktiviert ist, aber nicht für die Anforderung ausgewählt ist, wird es in der Protokolldatei mit einem Bindestrich (-) als Platzhalter angezeigt.

Protokolldateien werden erstellt, wenn die erste Anforderung in der URL-Gruppe oder der Server Sitzung eingeht. Sie werden bei der Konfiguration der Protokollierung nicht erstellt. Im folgenden Beispiel wird der erste Eintrag der Protokolldatei für eine W3C-Protokolldatei mit den Feldern Client-IP, Benutzername, Server-IP, Serverport, Methode, URI-Stamm, URI-Abfrage, Status und Benutzer-Agent angezeigt:

``` syntax
#Software: Microsoft HTTP Server API 2.0  
#Version: 1.0   // the log file version as it's described by "https://www.w3.org/TR/WD-logfile".
#Date: 2002-05-02 17:42:15  // when the first log file entry was recorded, which is when the entire log file was created.
#Fields: date time c-ip cs-username s-ip s-port cs-method cs-uri-stem cs-uri-query sc-status cs(User-Agent)
2002-05-02 17:42:15 172.22.255.255 - 172.30.255.255 80 GET /images/picture.jpg - 200 Mozilla/4.0+(compatible;MSIE+5.5;+Windows+2000+Server)
```

Das Zeit Erfassungs Feld wird initialisiert, wenn die HTTP-Server-API das erste Byte empfängt, bevor die Anforderung analysiert wird. Der Zeitstempel des Zeitrahmens wird beendet, wenn der letzte Sendevorgang abgeschlossen ist. Die Zeit wird nicht über das Netzwerk hinweg berücksichtigt. Die erste Anforderung an die Site wird etwas länger als andere ähnliche Anforderungen angezeigt, da die HTTP-Server-API die Protokolldatei mit der ersten Anforderung öffnet.

 

 