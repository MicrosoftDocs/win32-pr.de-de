---
title: Fehler Protokollierung in Windows Server 2003 SP1
description: Fehler Protokollierung in Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Fehler Protokollierung in Windows Server 2003 mit Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b82c816dab39877f700973de3c0c7798034d124
ms.sourcegitcommit: 7bdca1558c21be976be950a213c5a072c449f111
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/14/2019
ms.locfileid: "103719338"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a>Fehler Protokollierung in Windows Server 2003 SP1

## <a name="addition-of-w3c-style-headers"></a>Hinzufügen von W3C-Stil Headern

Ab Windows Server 2003 mit Service Pack 1 (SP1) umfasst das HTTP-Server-API-Fehlerprotokoll W3C-Stil Header, die die Analyse von Protokolldateien mithilfe von Standardprotokoll-Parser ermöglichen. Die unten gezeigte Vorlage listet alle Felder auf, die in der http-Fehlerprotokoll Datei protokolliert werden können.

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a>Protokollieren zusätzlicher Felder

Das http-Fehlerprotokoll wurde erweitert und enthält neun weitere Felder zum Protokollieren von Daten zu Fehlern, die auftreten. Die neuen Fehler Felder sind unten aufgeführt:

-   Server Computer Name \[ S-Computername\]
-   Benutzer-Agent- \[ cs (Benutzer- \_ Agent)\]
-   Cookie- \[ cs (Cookie)\]
-   referenrer- \[ cs (Verweiser)\]
-   Hostname \[ : cs-Host\]
-   Vom Server empfangene Bytes ( \[ SC-Bytes)\]
-   Von der Server-cs-Bytes empfangene und verarbeitete Bytes \[ -Bytes\]
-   Benötigte Zeit für die Verarbeitung der Anforderungs \[ Zeit.\]
-   Queue-Name (reserviert für IIS) \[ S-QueueName\]

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a>Auswählen von "fLEDs" zum Protokollieren in der http-Fehlerprotokoll Datei

Der Registrierungsschlüssel **errorloggingfields** wurde hinzugefügt, um die Felder zu steuern, die im http-Fehlerprotokoll protokolliert wurden. Diese Registrierungs Werte befinden sich unter einem HTTP- \\ Parameter Schlüssel unter:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

Der **errorloggingfields** -Registrierungs Wert ist ein DWORD-Wert, der Bitwerte für jedes der Felder enthält, die protokolliert werden können. Legen Sie zum Aktivieren der Protokollierung eines bestimmten Felds den entsprechenden Bitwert auf 1 fest, und starten Sie den HTTP-Dienst neu. Legen Sie den Bitwert auf 0 fest, um die Protokollierung zu deaktivieren. Verwenden Sie zum Konfigurieren mehrerer Felder ein bitweises OR der einzelnen Werte. Wenn Sie z. b. die Protokollierungs Felder Cookie und Referrer aktivieren möchten, sollte der Wert 0x00020000 \| 0x00040000 = 0x00060000 lauten. Wenn der Registrierungsschlüssel **errorloggingfields** nicht vorhanden ist, werden die Standard Felder protokolliert. Der Wert von **errorloggingfields** zum Protokollieren der Standard Felder lautet 0x7c884c7. Um die Protokollierung für alle Felder zu aktivieren, die in der folgenden Tabelle angezeigt werden, legen Sie den Wert auf 0x7dff4e7 fest.

Die Felder für die Fehler Protokollierung sind in der folgenden Tabelle aufgeführt:



| Protokollfeld            | Standardmäßig protokolliert | Bitwert  |
|----------------------|-------------------|------------|
| Date                 | Ja               | 0x00000001 |
| Time                 | Ja               | 0x00000002 |
| Server Computer Name | Nein                | 0x00000020 |
| Client IP Address    | Ja               | 0x00000004 |
| ClientPort          | Ja               | 0x00400000 |
| Server-IP-Adresse    | Ja               | 0x00000040 |
| Serverport          | Ja               | 0x00008000 |
| Protokoll Version     | Ja               | 0x00080000 |
| Methode               | Ja               | 0x00000080 |
| URI                  | Ja               | 0x00800000 |
| Benutzer-Agent           | Nein                | 0x00010000 |
| Cookie               | Nein                | 0x00020000 |
| Verweiser             | Nein                | 0x00040000 |
| Host                 | Nein                | 0x00100000 |
| Protokoll Status      | Ja               | 0x00000400 |
| SC-Bytes             | Nein                | 0x00001000 |
| CS-Bytes             | Nein                | 0x00002000 |
| Benötigte Zeit           | Nein                | 0x00004000 |
| SiteId               | Ja               | 0x01000000 |
| Reason-Ausdruck        | Ja               | 0x02000000 |
| Warteschlangenname           | Nein                | 0x04000000 |
| Stream-ID            | Nein                | 0x???????? |



 

## <a name="time-and-date-rollover"></a>Zeit-und Datums-Rollover

Standardmäßig wird eine neue http-Fehlerprotokoll Datei erstellt (als Dateirollover bezeichnet), wenn die aktuelle Protokolldatei eine bestimmte Größe erreicht. Ab Windows Server 2003 mit SP1 können neue Fehlerprotokoll Dateien basierend auf Datum und Uhrzeit erstellt werden. Zeit-und Datums-Rollover werden von zwei neuen Registrierungs Werten gesteuert: **errorloggingrollovertype** und **errorlogginglocaltimerollover**. Diese Registrierungs Werte müssen der Registrierung hinzugefügt werden, um Zeit-und Datums-Rollover zu aktivieren. Der HTTP-Dienst muss neu gestartet werden, wenn diese Schlüssel der Registrierung hinzugefügt werden. Die Registrierungsschlüssel für das Rollover der Protokolldatei werden unter folgendem Schlüssel erstellt:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

Der Registrierungsschlüssel **errorloggingrollovertype** gibt den Typ des gewünschten Rollovers an und ist standardmäßig auf Größen basiertes Rollover festgelegt. Rollover kann auch täglich, wöchentlich, monatlich oder stündlich erfolgen. Wenn der Dateirollover auf der Zeit basiert, gibt ein **errorlogginglocaltimerollover** -Wert von 0 an, dass die rolloverzeit in GMT ausgedrückt wird, und der Wert 1 gibt an, dass die rolloverzeit in Ortszeit ausgedrückt wird. Der **errorloggingrollovertype** -Schlüssel kann einen Wert von 0 bis 4 annehmen, wie in der folgenden Tabelle aufgeführt.



| Wert des Rollover-Typs | BESCHREIBUNG                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 0                   | Größen basierter Rollover. Für Protokolldateien wird ein Rollover durchgeführt, wenn die Datei die Größe erreicht, die im Registrierungsschlüssel **errorlogfiletrungateesize** definiert ist. |
| 1                   | Der Protokoll Dateirollover erfolgt täglich.                                                                                                         |
| 2                   | Der Protokoll Dateirollover erfolgt wöchentlich.                                                                                                        |
| 3                   | Der Protokoll Dateirollover erfolgt monatlich.                                                                                                       |
| 4                   | Der Protokoll Dateirollover erfolgt stündlich.                                                                                                        |



 

Die Benennungs Konventionen für Dateien, in denen die Fehlerprotokolle gespeichert werden, unterscheiden sich für die Größen-, Datums-und zeitbasierten Rollover. In der folgenden Tabelle werden die Benennungs Konventionen für http-Protokolldateien aufgelistet.



| Tollovertyp | Protokolldateiname  | BESCHREIBUNG                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Size          | Httperrn. log   | Die Protokolldatei wird wieder verwendet, wenn Sie eine bestimmte Größe erreicht. n ist die Dateinummer und wird erhöht, wenn für die Protokolldatei ein Rollover durchgeführt wird. |
| Täglich         | "htyymmdd. log"   | Die Protokolldatei wird täglich wieder verwendet.                                                                                                     |
| Wöchentlich        | "htyymmww. log"   | Die Protokolldatei wird wöchentlich wieder verwendet, wobei WW die Woche des Monats ist.                                                                 |
| Monatlich       | "htyymm. log"     | Die Protokolldatei wird monatlich wieder verwendet.                                                                                               |
| Stündlich        | htyymmddhh. log | Die Protokolldatei wird stündlich wieder verwendet, wobei HH die Stunde des Tages ist, die in 0-24-Stunden-Notation ausgedrückt wird.                                   |



 

 

 




