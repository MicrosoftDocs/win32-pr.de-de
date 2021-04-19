---
description: Weitere Informationen finden Sie in der jetstopbackup-Funktion.
title: Jetstopbackup-Funktion
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c47a1454e5846fae510a7b91c197d4b180fd14a7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106369348"
---
# <a name="jetstopbackup-function"></a><span data-ttu-id="0a80b-103">Jetstopbackup-Funktion</span><span class="sxs-lookup"><span data-stu-id="0a80b-103">JetStopBackup Function</span></span>


<span data-ttu-id="0a80b-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0a80b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopbackup-function"></a><span data-ttu-id="0a80b-105">Jetstopbackup-Funktion</span><span class="sxs-lookup"><span data-stu-id="0a80b-105">JetStopBackup Function</span></span>

<span data-ttu-id="0a80b-106">Die **jetstopbackup** -Funktion verhindert, dass alle streamingsicherungsbezogenen Aktivitäten auf einer bestimmten laufenden Instanz fortgesetzt werden, sodass die Streamingsicherung auf vorhersagbare Weise beendet wird.</span><span class="sxs-lookup"><span data-stu-id="0a80b-106">The **JetStopBackup** function prevents any streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="0a80b-107">**Windows XP:**  Diese Funktion wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0a80b-107">**Windows XP:**  This function is introduced in Windows XP.</span></span>

<span data-ttu-id="0a80b-108">[Jetstopservice](./jetstopservice-function.md) ist der Legacy-Befehl, wenn nur eine Instanz zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="0a80b-108">[JetStopService](./jetstopservice-function.md) is the legacy call when only one instance is allowed.</span></span> <span data-ttu-id="0a80b-109">In diesem Fall ist die einzige aktive Instanz die, die für die Beendigung vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="0a80b-109">In this case, the only active instance is the one being prepared for termination.</span></span>

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="0a80b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a80b-110">Parameters</span></span>

<span data-ttu-id="0a80b-111">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0a80b-111">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="0a80b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a80b-112">Return Value</span></span>

<span data-ttu-id="0a80b-113">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="0a80b-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0a80b-114">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0a80b-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a80b-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0a80b-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="0a80b-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a80b-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a80b-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0a80b-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0a80b-118">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0a80b-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a80b-119">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="0a80b-119">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="0a80b-120">Es ist nicht klar, welche Instanz für die Beendigung vorbereitet werden soll, wenn <a href="gg269240(v=exchg.10).md">jetstopservice</a> im Modus für mehrere Instanzen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0a80b-120">It is not clear which instance to prepare for termination when using <a href="gg269240(v=exchg.10).md">JetStopService</a> with multiple instance mode.</span></span></p>
<p><span data-ttu-id="0a80b-121"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0a80b-121"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0a80b-122">Wenn diese Funktion erfolgreich ausgeführt wird, startet die Instanz alle neuen Streamingsicherungs-APIs.</span><span class="sxs-lookup"><span data-stu-id="0a80b-122">If this function succeeds, the instance will start failing any new streaming backup APIs.</span></span>

<span data-ttu-id="0a80b-123">Wenn diese Funktion fehlschlägt, werden keine Schritte zur Vorbereitung der Sicherung auf der-Instanz ausgeführt, und es wird keine Änderung am Instanzzustand vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="0a80b-123">If this function fails, no steps to prepare for the backup termination on the instance will be taken and no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0a80b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a80b-124">Remarks</span></span>

<span data-ttu-id="0a80b-125">Die Sicherung wird in der Regel durch ein Ereignis außerhalb des Prozess Mechanismus ausgelöst. durch die Verwendung dieser API führt die ESENT-Anwendung selbst weitere Aufrufe an die Streamingsicherungs-APIs aus.</span><span class="sxs-lookup"><span data-stu-id="0a80b-125">Backup is usually triggered by an event outside the process mechanism and by using this API, the ESENT application itself will make any further calls to the streaming backup APIs to fail.</span></span> <span data-ttu-id="0a80b-126">Der Großteil der APIs für die Streaming-Sicherung beginnt mit dem JET_errBackupAbortByServer.</span><span class="sxs-lookup"><span data-stu-id="0a80b-126">The majority of streaming backup APIs will start failing with JET_errBackupAbortByServer.</span></span> <span data-ttu-id="0a80b-127">Daher wird bei jedem Fortschritt der Streamingsicherung (z.b. [jetreadfilanstance](./jetreadfileinstance-function.md)) ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0a80b-127">As such, any streaming backup progress (like [JetReadFileInstance](./jetreadfileinstance-function.md)) will return an error.</span></span> <span data-ttu-id="0a80b-128">Sicherungs Vorgänge, die Teil der Sicherungs Beendigung sind (z. b. [jetendexternalbackupinstance](./jetendexternalbackupinstance-function.md)), sind weiterhin zulässig.</span><span class="sxs-lookup"><span data-stu-id="0a80b-128">Backup operations which are part of the backup termination (such as [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) will still be allowed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0a80b-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a80b-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a80b-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0a80b-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0a80b-131">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0a80b-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a80b-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0a80b-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0a80b-133">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0a80b-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a80b-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0a80b-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0a80b-135">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="0a80b-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a80b-136"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="0a80b-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0a80b-137">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0a80b-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a80b-138"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0a80b-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0a80b-139">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0a80b-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0a80b-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0a80b-140">See Also</span></span>

[<span data-ttu-id="0a80b-141">Jetendexternalbackupinstance</span><span class="sxs-lookup"><span data-stu-id="0a80b-141">JetEndExternalBackupInstance</span></span>](./jetendexternalbackupinstance-function.md)  
[<span data-ttu-id="0a80b-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0a80b-142">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0a80b-143">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="0a80b-143">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="0a80b-144">Jetreadfilinput Stance</span><span class="sxs-lookup"><span data-stu-id="0a80b-144">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="0a80b-145">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="0a80b-145">JetStopService</span></span>](./jetstopservice-function.md)
