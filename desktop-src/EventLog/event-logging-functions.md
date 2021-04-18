---
description: Die folgenden Funktionen werden bei der Ereignisprotokollierung verwendet.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Funktionen zur Ereignisprotokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437899684861c5fc7ddbfe98c2499dc07bd9da8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347538"
---
# <a name="event-logging-functions"></a><span data-ttu-id="aa171-103">Funktionen zur Ereignisprotokollierung</span><span class="sxs-lookup"><span data-stu-id="aa171-103">Event Logging Functions</span></span>

<span data-ttu-id="aa171-104">Die folgenden Funktionen werden bei der Ereignisprotokollierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="aa171-104">The following functions are used with event logging.</span></span>



| <span data-ttu-id="aa171-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="aa171-105">Function</span></span>                                                         | <span data-ttu-id="aa171-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa171-106">Description</span></span>                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa171-107">**Backupeer-Protokoll**</span><span class="sxs-lookup"><span data-stu-id="aa171-107">**BackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | <span data-ttu-id="aa171-108">Speichert das angegebene Ereignisprotokoll in einer Sicherungsdatei.</span><span class="sxs-lookup"><span data-stu-id="aa171-108">Saves the specified event log to a backup file.</span></span>                                                     |
| [<span data-ttu-id="aa171-109">**Cleareventlog**</span><span class="sxs-lookup"><span data-stu-id="aa171-109">**ClearEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | <span data-ttu-id="aa171-110">Löscht das angegebene Ereignisprotokoll und speichert optional die aktuelle Kopie des Protokolls in einer Sicherungsdatei.</span><span class="sxs-lookup"><span data-stu-id="aa171-110">Clears the specified event log, and optionally saves the current copy of the log to a backup file.</span></span>  |
| [<span data-ttu-id="aa171-111">**Closeeventlog**</span><span class="sxs-lookup"><span data-stu-id="aa171-111">**CloseEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | <span data-ttu-id="aa171-112">Schließt ein Lese Handle in das angegebene Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="aa171-112">Closes a read handle to the specified event log.</span></span>                                                    |
| [<span data-ttu-id="aa171-113">**Deregistereventsource**</span><span class="sxs-lookup"><span data-stu-id="aa171-113">**DeregisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | <span data-ttu-id="aa171-114">Schließt ein Schreib Handle in das angegebene Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="aa171-114">Closes a write handle to the specified event log.</span></span>                                                   |
| [<span data-ttu-id="aa171-115">**Geteventloginformation**</span><span class="sxs-lookup"><span data-stu-id="aa171-115">**GetEventLogInformation**</span></span>](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | <span data-ttu-id="aa171-116">Ruft Informationen zum angegebenen Ereignisprotokoll ab.</span><span class="sxs-lookup"><span data-stu-id="aa171-116">Retrieves information about the specified event log.</span></span>                                                |
| [<span data-ttu-id="aa171-117">**Getnumofeventlogrecords**</span><span class="sxs-lookup"><span data-stu-id="aa171-117">**GetNumberOfEventLogRecords**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | <span data-ttu-id="aa171-118">Ruft die Anzahl der Datensätze im angegebenen Ereignisprotokoll ab.</span><span class="sxs-lookup"><span data-stu-id="aa171-118">Retrieves the number of records in the specified event log.</span></span>                                         |
| [<span data-ttu-id="aa171-119">**Getoldesteventlogrecord**</span><span class="sxs-lookup"><span data-stu-id="aa171-119">**GetOldestEventLogRecord**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | <span data-ttu-id="aa171-120">Ruft die absolute Datensatznummer des ältesten Datensatzes im angegebenen Ereignisprotokoll ab.</span><span class="sxs-lookup"><span data-stu-id="aa171-120">Retrieves the absolute record number of the oldest record in the specified event log.</span></span>               |
| [<span data-ttu-id="aa171-121">**Notifychangeeventlog**</span><span class="sxs-lookup"><span data-stu-id="aa171-121">**NotifyChangeEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | <span data-ttu-id="aa171-122">Ermöglicht es einer Anwendung, Benachrichtigungen zu empfangen, wenn ein Ereignis in das angegebene Ereignisprotokoll geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="aa171-122">Enables an application to receive notification when an event is written to the specified event log.</span></span> |
| [<span data-ttu-id="aa171-123">**Openbackupeer ventlog**</span><span class="sxs-lookup"><span data-stu-id="aa171-123">**OpenBackupEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | <span data-ttu-id="aa171-124">Öffnet ein Handle für ein Sicherungs Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="aa171-124">Opens a handle to a backup event log.</span></span>                                                               |
| [<span data-ttu-id="aa171-125">**OpenEventLog**</span><span class="sxs-lookup"><span data-stu-id="aa171-125">**OpenEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | <span data-ttu-id="aa171-126">Öffnet ein Handle für das angegebene Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="aa171-126">Opens a handle to the specified event log.</span></span>                                                          |
| [<span data-ttu-id="aa171-127">**ReadEventLog**</span><span class="sxs-lookup"><span data-stu-id="aa171-127">**ReadEventLog**</span></span>](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | <span data-ttu-id="aa171-128">Liest eine ganze Anzahl von Einträgen aus dem angegebenen Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="aa171-128">Reads a whole number of entries from the specified event log.</span></span>                                       |
| [<span data-ttu-id="aa171-129">**Registereventsource**</span><span class="sxs-lookup"><span data-stu-id="aa171-129">**RegisterEventSource**</span></span>](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | <span data-ttu-id="aa171-130">Ruft ein registriertes Handle für das angegebene Ereignisprotokoll ab.</span><span class="sxs-lookup"><span data-stu-id="aa171-130">Retrieves a registered handle to the specified event log.</span></span>                                           |
| [<span data-ttu-id="aa171-131">**ReportEvent**</span><span class="sxs-lookup"><span data-stu-id="aa171-131">**ReportEvent**</span></span>](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | <span data-ttu-id="aa171-132">Schreibt einen Eintrag am Ende des angegebenen Ereignis Protokolls.</span><span class="sxs-lookup"><span data-stu-id="aa171-132">Writes an entry at the end of the specified event log.</span></span>                                              |



 

 

 



