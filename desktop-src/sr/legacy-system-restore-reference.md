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
# <a name="legacy-system-restore-reference"></a><span data-ttu-id="f7913-104">Ältere System Wiederherstellungs Referenz</span><span class="sxs-lookup"><span data-stu-id="f7913-104">Legacy System Restore Reference</span></span>

<span data-ttu-id="f7913-105">\[Diese Informationen gelten nur für Windows XP mit Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="f7913-105">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="f7913-106">In dieser Dokumentation werden die Implementierungsdetails des von einer Legacy Version der System Wiederherstellung verwendeten Repository beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f7913-106">This documentation describes implementation details of the repository used by a legacy version of System Restore.</span></span> <span data-ttu-id="f7913-107">Dies gilt nicht für die Implementierung der System Wiederherstellung in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f7913-107">It does not apply to the implementation of System Restore on Windows Vista.</span></span>

## <a name="system-restore-repository-structure"></a><span data-ttu-id="f7913-108">Systemwiederherstellungsrepository-Struktur</span><span class="sxs-lookup"><span data-stu-id="f7913-108">System Restore Repository Structure</span></span>

<span data-ttu-id="f7913-109">Windows XP mit SP2 enthält ein Repository für die Systemwiederherstellung im folgenden Ordner:% System Drive% \\ systemvolumeinformationen.</span><span class="sxs-lookup"><span data-stu-id="f7913-109">Windows XP with SP2 contains a repository for System Restore in the following folder: %SYSTEMDRIVE%\\System Volume Information.</span></span> <span data-ttu-id="f7913-110">Dieses Repository enthält Informationen zu Wiederherstellungs Punkten, bei denen es sich im Wesentlichen um eine Momentaufnahme des Systems zu einem bestimmten Zeitpunkt handelt.</span><span class="sxs-lookup"><span data-stu-id="f7913-110">This repository contains information for restore points, which are essentially a snapshot of the system at a moment in time.</span></span>

<span data-ttu-id="f7913-111">Das Repository ist wie folgt strukturiert:</span><span class="sxs-lookup"><span data-stu-id="f7913-111">The repository is structured as follows:</span></span>

<span data-ttu-id="f7913-112">**Systemvolumeinformationen**    \*\* \_ Restore *{GUID*}\*\*       **WP1**       **WP2**       **RP *n*-1**       **RP \* n** \*     \*\* \_ Restore {*GUID*}\*\*       **WP1**       **WP2**       **RP *n*-1**       **RP \* n**\*</span><span class="sxs-lookup"><span data-stu-id="f7913-112">**System Volume Information**    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*</span></span>

<span data-ttu-id="f7913-113">Um zu ermitteln, welcher \_ Ordner "{*GUID*}" wieder hergestellt werden soll, lesen Sie die in der folgenden Datei angegebene **GUID** : systemroot% \\ system32 \\ Restore \\MachineGUID.txt.</span><span class="sxs-lookup"><span data-stu-id="f7913-113">To determine which \_restore{*GUID*} folder to use, read the **GUID** specified in the following file: SYSTEMROOT%\\System32\\Restore\\MachineGUID.txt.</span></span>

<span data-ttu-id="f7913-114">In jedem \_ Restore {*GUID*}-Ordner \_ enthält die Datei "Driver. cfg" Informationen aus einer **permanenten SR- \_ \_ Konfigurations** Struktur, die wie folgt definiert wird:</span><span class="sxs-lookup"><span data-stu-id="f7913-114">Within each \_restore{*GUID*} folder, the \_driver.cfg file contains information from a **SR\_PERSISTENT\_CONFIG** structure defined as follows:</span></span>

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

## <a name="files-contained-in-each-rpnfolder"></a><span data-ttu-id="f7913-115">In jedem RP *n*-Ordner enthaltene Dateien</span><span class="sxs-lookup"><span data-stu-id="f7913-115">Files Contained in Each RP *n* Folder</span></span>

<span data-ttu-id="f7913-116">Jeder RP *n* -Ordner enthält einen Momentaufnahme Ordner, der Folgendes enthält:</span><span class="sxs-lookup"><span data-stu-id="f7913-116">Each RP *n* folder contains a Snapshot folder that contains the following:</span></span>

-   <span data-ttu-id="f7913-117">Eine Momentaufnahme der Registrierungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="f7913-117">A snapshot of the registry hives</span></span>
-   <span data-ttu-id="f7913-118">Ein Repository-Ordner, der eine Momentaufnahme des WMI-Repository enthält.</span><span class="sxs-lookup"><span data-stu-id="f7913-118">A Repository folder that contains a snapshot of the WMI repository</span></span>
-   <span data-ttu-id="f7913-119">Eine Momentaufnahme der com+-Datenbank</span><span class="sxs-lookup"><span data-stu-id="f7913-119">A snapshot of the COM+ database</span></span>
-   <span data-ttu-id="f7913-120">Eine Momentaufnahme der IIS-Datenbank</span><span class="sxs-lookup"><span data-stu-id="f7913-120">A snapshot of the IIS database</span></span>

<span data-ttu-id="f7913-121">Jeder RP *n* -Ordner enthält eine Datei RP. log, die allgemeine Informationen zum Wiederherstellungspunkt aus der [**restorepointinfow**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="f7913-121">Each RP *n* folder contains an RP.log file that contains general information about the restore point from the [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) structure.</span></span>

<span data-ttu-id="f7913-122">Jeder RP *n* -Ordner kann Dateien enthalten, die zum Nachverfolgen von Änderungen für einen Wiederherstellungspunkt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7913-122">Each RP *n* folder may contain files used to track changes for a restore point.</span></span> <span data-ttu-id="f7913-123">Die erste Datei hat den Namen "Change. log", die nächste Datei hat den Namen "Change. log. 1" usw.</span><span class="sxs-lookup"><span data-stu-id="f7913-123">The first file is named change.log, the next file is named change.log.1, and so on.</span></span> <span data-ttu-id="f7913-124">Jede Änderungsprotokoll Datei enthält die folgenden Strukturen:</span><span class="sxs-lookup"><span data-stu-id="f7913-124">Each change log file contains the following structures:</span></span>

-   [<span data-ttu-id="f7913-125">**\_Protokoll \_ Header ändern**</span><span class="sxs-lookup"><span data-stu-id="f7913-125">**CHANGE\_LOG\_HEADER**</span></span>](change-log-header.md)
-   <span data-ttu-id="f7913-126">[**Ändern \_ Protokoll \_ Eintrag**](change-log-entry.md)1</span><span class="sxs-lookup"><span data-stu-id="f7913-126">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)1</span></span>
-   <span data-ttu-id="f7913-127">[**Ändern \_ Protokoll \_ Eintrag**](change-log-entry.md)2</span><span class="sxs-lookup"><span data-stu-id="f7913-127">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)2</span></span>
-   <span data-ttu-id="f7913-128">...</span><span class="sxs-lookup"><span data-stu-id="f7913-128">...</span></span>
-   <span data-ttu-id="f7913-129">[**Ändern \_ Protokoll \_ Eintrag**](change-log-entry.md)*n*</span><span class="sxs-lookup"><span data-stu-id="f7913-129">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)*n*</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7913-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f7913-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7913-131">Legacy-System Wiederherstellungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="f7913-131">Legacy System Restore Structures</span></span>](legacy-system-restore-structures.md)
</dt> </dl>

 

 




