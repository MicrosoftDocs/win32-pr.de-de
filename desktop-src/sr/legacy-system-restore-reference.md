---
title: Ältere System Wiederherstellungs Referenz
description: In dieser Dokumentation werden die Implementierungsdetails des von einer Legacy Version der System Wiederherstellung verwendeten Repository beschrieben. Dies gilt nicht für die Implementierung der System Wiederherstellung in Windows Vista.
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8703cbf88b97458f07c616d48405708e25acec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855459"
---
# <a name="legacy-system-restore-reference"></a>Ältere System Wiederherstellungs Referenz

\[Diese Informationen gelten nur für Windows XP mit Service Pack 2 (SP2).\]

In dieser Dokumentation werden die Implementierungsdetails des von einer Legacy Version der System Wiederherstellung verwendeten Repository beschrieben. Dies gilt nicht für die Implementierung der System Wiederherstellung in Windows Vista.

## <a name="system-restore-repository-structure"></a>Systemwiederherstellungsrepository-Struktur

Windows XP mit SP2 enthält ein Repository für die Systemwiederherstellung im folgenden Ordner:% System Drive% \\ systemvolumeinformationen. Dieses Repository enthält Informationen zu Wiederherstellungs Punkten, bei denen es sich im Wesentlichen um eine Momentaufnahme des Systems zu einem bestimmten Zeitpunkt handelt.

Das Repository ist wie folgt strukturiert:

**Systemvolumeinformationen**    ** \_ Restore *{GUID*}**       **WP1**       **WP2**       **RP *n*-1**       **RP * n** *     ** \_ Restore {*GUID*}**       **WP1**       **WP2**       **RP *n*-1**       **RP * n***

Um zu ermitteln, welcher \_ Ordner "{*GUID*}" wieder hergestellt werden soll, lesen Sie die in der folgenden Datei angegebene **GUID** : systemroot% \\ system32 \\ Restore \\MachineGUID.txt.

In jedem \_ Restore {*GUID*}-Ordner \_ enthält die Datei "Driver. cfg" Informationen aus einer **permanenten SR- \_ \_ Konfigurations** Struktur, die wie folgt definiert wird:

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

## <a name="files-contained-in-each-rpnfolder"></a>In jedem RP *n*-Ordner enthaltene Dateien

Jeder RP *n* -Ordner enthält einen Momentaufnahme Ordner, der Folgendes enthält:

-   Eine Momentaufnahme der Registrierungs Strukturen
-   Ein Repository-Ordner, der eine Momentaufnahme des WMI-Repository enthält.
-   Eine Momentaufnahme der com+-Datenbank
-   Eine Momentaufnahme der IIS-Datenbank

Jeder RP *n* -Ordner enthält eine Datei RP. log, die allgemeine Informationen zum Wiederherstellungspunkt aus der [**restorepointinfow**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) -Struktur enthält.

Jeder RP *n* -Ordner kann Dateien enthalten, die zum Nachverfolgen von Änderungen für einen Wiederherstellungspunkt verwendet werden. Die erste Datei hat den Namen "Change. log", die nächste Datei hat den Namen "Change. log. 1" usw. Jede Änderungsprotokoll Datei enthält die folgenden Strukturen:

-   [**\_Protokoll \_ Header ändern**](change-log-header.md)
-   [**Ändern \_ Protokoll \_ Eintrag**](change-log-entry.md)1
-   [**Ändern \_ Protokoll \_ Eintrag**](change-log-entry.md)2
-   ...
-   [**Ändern \_ Protokoll \_ Eintrag**](change-log-entry.md)*n*

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Legacy-System Wiederherstellungs Strukturen](legacy-system-restore-structures.md)
</dt> </dl>

 

 




