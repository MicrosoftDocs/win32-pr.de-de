---
title: Referenz zur Legacysystemwiederherstellung
description: In dieser Dokumentation werden Implementierungsdetails des Repositorys beschrieben, das von einer Legacyversion der Systemwiederherstellung verwendet wird. Dies gilt nicht für die Implementierung der Systemwiederherstellung auf Windows Vista.
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9fe01ab076d598a4fcc8ac9c46706142d761aec6d903f3c626e792cfaa60e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047332"
---
# <a name="legacy-system-restore-reference"></a>Referenz zur Legacysystemwiederherstellung

\[Diese Informationen gelten nur für Windows XP mit Service Pack 2 (SP2).\]

In dieser Dokumentation werden Implementierungsdetails des Repositorys beschrieben, das von einer Legacyversion der Systemwiederherstellung verwendet wird. Dies gilt nicht für die Implementierung der Systemwiederherstellung auf Windows Vista.

## <a name="system-restore-repository-structure"></a>Struktur des Systemwiederherstellungs-Repositorys

Windows XP mit SP2 enthält ein Repository für die Systemwiederherstellung im folgenden Ordner: %SYSTEMDRIVE% \\ Systemvolumeinformationen. Dieses Repository enthält Informationen zu Wiederherstellungspunkten, bei denen es sich im Wesentlichen um eine Momentaufnahme des Systems zu einem zeitpunktigen Zeitpunkt handelt.

Das Repository ist wie folgt strukturiert:

**Wiederherstellung von Systemvolumeinformationen{****\_ *GUID*}****RP1****RP2** RP ***n*-1****RP*n** *     **\_ restore{*GUID*}****RP1****RP2** RP ***n*-1****RP*n**                                                            *

Um zu bestimmen, welcher \_ Ordner restore{*GUID*} verwendet werden soll, lesen Sie die **GUID,** die in der folgenden Datei angegeben ist: SYSTEMROOT% \\ System32 \\ Restore \\MachineGUID.txt.

In jedem \_ Ordner restore{*GUID*} enthält die \_ Datei driver.cfg Informationen aus einer **SR PERSISTENT \_ \_ CONFIG-Struktur,** die wie folgt definiert ist:

``` syntax
typedef struct _SR_PERSISTENT_CONFIG
 {      
  ULONG Signature;            // Set to CPrs
  ULONG FileNameNumber;       // Number for next temp file 
                              // For example, A0000001 would be 1  
  INT64 FileSeqNumber;        // Next sequence number
  ULONG CurrentRestoreNumber; // For example, RP5 would be 5
 } SR_PERSISTENT_CONFIG, * PSR_PERSISTENT_CONFIG;
```

## <a name="files-contained-in-each-rpnfolder"></a>In jedem RP *n-Ordner* enthaltene Dateien

Jeder RP *n-Ordner* enthält einen Momentaufnahmeordner, der Folgendes enthält:

-   Eine Momentaufnahme der Registrierungsstrukturen
-   Ein Repositoryordner, der eine Momentaufnahme des WMI-Repositorys enthält
-   Eine Momentaufnahme der COM+-Datenbank
-   Eine Momentaufnahme der IIS-Datenbank

Jeder RP *n-Ordner* enthält eine RP.log-Datei, die allgemeine Informationen zum Wiederherstellungspunkt aus der [**RESTOREPOINTINFOW-Struktur**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) enthält.

Jeder RP *n-Ordner* kann Dateien enthalten, mit denen Änderungen für einen Wiederherstellungspunkt nachverfolgt werden. Die erste Datei heißt change.log, die nächste Datei heißt change.log.1 usw. Jede Änderungsprotokolldatei enthält die folgenden Strukturen:

-   [**CHANGE \_ LOG \_ HEADER**](change-log-header.md)
-   [**CHANGE \_ \_PROTOKOLLEINTRAG**](change-log-entry.md)1
-   [**CHANGE \_ \_PROTOKOLLEINTRAG**](change-log-entry.md)2
-   ...
-   [**CHANGE \_ LOG \_ ENTRY**](change-log-entry.md)*n*

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Legacysystemwiederherstellungsstrukturen](legacy-system-restore-structures.md)
</dt> </dl>

 

 




