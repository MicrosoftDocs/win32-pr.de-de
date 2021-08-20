---
title: Fehlerprotokollierung in Windows Server 2003 SP1
description: Fehlerprotokollierung in Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Fehlerprotokollierung in Windows Server 2003 mit Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d5a84dfba8ecb9a78ed38d3ad112f0820e6b578bce77e189e5047a25f458b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014808"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a>Fehlerprotokollierung in Windows Server 2003 SP1

## <a name="addition-of-w3c-style-headers"></a>Hinzufügen von W3C-Stilheadern

Ab Windows Server 2003 mit Service Pack 1 (SP1) enthält das HTTP-Server-API-Fehlerprotokoll W3C-Formatheader, mit denen Protokolldateien mithilfe von Standardprotokollparsern analysiert werden können. Die unten gezeigte Vorlage listet alle Felder auf, die in der HTTP-Fehlerprotokolldatei protokolliert werden können.

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

Das HTTP-Fehlerprotokoll wurde um neun weitere Felder erweitert, um Daten zu auftretenden Fehlern zu protokollieren. Die neuen Fehlerfelder sind unten aufgeführt:

-   Servercomputername \[ S-COMPUTERNAME\]
-   Benutzer-Agent \[ \_ CS(BENUTZER-AGENT)\]
-   Cookie \[ CS(COOKIE)\]
-   referrer \[ CS(referrer)\]
-   Hostname \[ CS-HOST\]
-   Vom Server empfangene Bytes \[ SC-BYTES\]
-   Vom Server empfangene und verarbeitete Bytes \[ CS-BYTES\]
-   Time Taken to process the request \[ TIME-TAKEN\]
-   Queue-Name (für IIS reserviert) \[ S-QUEUENAME\]

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a>Auswählen von "Zu protokollierende Dateien" in der HTTP-Fehlerprotokolldatei

Der **Registrierungsschlüssel ErrorLoggingFields** wurde hinzugefügt, um die im HTTP-Fehlerprotokoll protokollierten Felder zu steuern. Diese Registrierungswerte befinden sich unter einem \\ HTTP-Parameterschlüssel unter:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

Der **ErrorLoggingFields-Registrierungswert** ist ein DWORD-Wert, der Bitwerte für jedes der Felder enthält, die protokolliert werden können. Um die Protokollierung eines bestimmten Felds zu aktivieren, legen Sie den entsprechenden Bitwert auf 1 fest, und starten Sie den HTTP-Dienst neu. Legen Sie den Bitwert auf 0 fest, um die Protokollierung zu deaktivieren. Um mehrere Felder zu konfigurieren, verwenden Sie ein bitweises OR der einzelnen Werte. Um beispielsweise die Felder Cookie- und Referrer-Protokollierung zu aktivieren, sollte der Wert 0x00020000 \| 0x00040000 = 0x00060000 sein. Wenn der **ErrorLoggingFields-Registrierungsschlüssel** nicht vorhanden ist, werden die Standardfelder protokolliert. Der **ErrorLoggingFields-Wert** zum Protokollieren der Standardfelder ist 0x7c884c7. Legen Sie den Wert auf 0x7dff4e7 fest, um die Protokollierung für alle felder in der folgenden Tabelle zu aktivieren.

Die Fehlerprotokollierungsfelder sind in der folgenden Tabelle aufgeführt:



| Protokollfeld            | Standardmäßig protokolliert | Bitwert  |
|----------------------|-------------------|------------|
| Date                 | Ja               | 0x00000001 |
| Time                 | Ja               | 0x00000002 |
| Servercomputername | Nein                | 0x00000020 |
| Client IP Address    | Ja               | 0x00000004 |
| Clientport          | Ja               | 0x00400000 |
| Server-IP-Adresse    | Ja               | 0x00000040 |
| Serverport          | Ja               | 0x00008000 |
| Protokollversion     | Ja               | 0x00080000 |
| Methode               | Ja               | 0x00000080 |
| URI                  | Ja               | 0x00800000 |
| Benutzer-Agent           | Nein                | 0x00010000 |
| Cookie               | Nein                | 0x00020000 |
| Referrer             | Nein                | 0x00040000 |
| Host                 | Nein                | 0x00100000 |
| Protokollstatus      | Ja               | 0x00000400 |
| SC-Bytes             | Nein                | 0x00001000 |
| CS-Bytes             | Nein                | 0x00002000 |
| Benötigte Zeit           | Nein                | 0x00004000 |
| Siteid               | Ja               | 0x01000000 |
| Grundphrase        | Ja               | 0x02000000 |
| Warteschlangenname           | Nein                | 0x04000000 |
| Stream-ID            | Nein                | 0x???????? |



 

## <a name="time-and-date-rollover"></a>Zeit- und Datumsrollover

Standardmäßig wird eine neue HTTP-Fehlerprotokolldatei erstellt (als Dateirollover bezeichnet), wenn die aktuelle Protokolldatei eine angegebene Größe erreicht. Ab Windows Server 2003 mit SP1 können neue Fehlerprotokolldateien basierend auf Datum und Uhrzeit erstellt werden. Zeit- und Datumsrollover werden durch zwei neue Registrierungswerte gesteuert: **ErrorLoggingRolloverType** und **ErrorLoggingLocaltimeRollover.** Zum Aktivieren des Zeit- und Datumsrollovers müssen diese Registrierungswerte der Registrierung hinzugefügt werden. Der HTTP-Dienst muss neu gestartet werden, wenn diese Schlüssel der Registrierung hinzugefügt werden. Die Registrierungsschlüssel für den Rollover der Protokolldatei werden unter dem folgenden Schlüssel erstellt:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

Der **Registrierungsschlüssel ErrorLoggingRolloverType** gibt den gewünschten Rollovertyp an und ist standardmäßig auf größenbasiertes Rollover festgelegt. Ein Rollover kann auch auf täglicher, wöchentlicher, monatlicher oder stündlicher Basis festgelegt werden. Wenn der Dateirollover auf der Zeit basiert, gibt der **ErrorLoggingLocaltimeRollover-Wert** 0 an, dass die Rolloverzeit in GMT ausgedrückt wird, und der Wert 1 gibt an, dass die Rolloverzeit in Ortszeit ausgedrückt wird. Der **ErrorLoggingRolloverType-Schlüssel** kann einen Wert von 0 bis 4 verwenden, wie in der folgenden Tabelle aufgeführt.



| Rollovertypwert | BESCHREIBUNG                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 0                   | Größenbasierter Rollover. Protokolldateien werden gerollt, wenn die Datei die im **Registrierungsschlüssel ErrorLogFileTruncateSize definierte Größe** erreicht. |
| 1                   | Das Rollover der Protokolldatei erfolgt täglich.                                                                                                         |
| 2                   | Der Rollover der Protokolldatei erfolgt wöchentlich.                                                                                                        |
| 3                   | Das Rollover der Protokolldatei erfolgt monatlich.                                                                                                       |
| 4                   | Der Rollover der Protokolldatei erfolgt stündlich.                                                                                                        |



 

Die Namenskonventionen für Dateien, in denen die Fehlerprotokolle gespeichert werden, unterscheiden sich je nach Größe, Datum und Uhrzeit. In der folgenden Tabelle sind die Namenskonventionen für HTTP-Protokolldateien aufgeführt.



| Tollovertyp | Protokolldateiname  | BESCHREIBUNG                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Size          | HTTPERRn.LOG   | Die Protokolldatei wird wiederverwendet, wenn sie eine bestimmte Größe erreicht. n ist die Dateinummer und wird inkrementiert, wenn ein Rollback für die Protokolldatei besteht. |
| Täglich         | htYYMMDD.log   | Die Protokolldatei wird täglich wiederverwendet.                                                                                                     |
| Wöchentlich        | htYYMMww.log   | Die Protokolldatei wird wöchentlich wiederverwendet, wobei ww die Woche des Monats ist.                                                                 |
| Monatlich       | htYYMM.log     | Die Protokolldatei wird jeden Monat wiederverwendet.                                                                                               |
| Stündlich        | htYYMMDDhh.log | Die Protokolldatei wird stündlich wiederverwendet, wobei hh die Stunde des Tages ist, ausgedrückt in 0-24-Stunden-Notation.                                   |



 

 

 




