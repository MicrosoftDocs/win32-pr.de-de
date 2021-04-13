---
description: Weitere Informationen finden Sie in der jeto ssnapshotfreeze-Funktion
title: JetOSSnapshotFreeze-Funktion
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb6ea9a4a3145c0c4b3c3caeb3214b299ea1be85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217235"
---
# <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="85201-103">JetOSSnapshotFreeze-Funktion</span><span class="sxs-lookup"><span data-stu-id="85201-103">JetOSSnapshotFreeze Function</span></span>


<span data-ttu-id="85201-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="85201-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="85201-105">JetOSSnapshotFreeze-Funktion</span><span class="sxs-lookup"><span data-stu-id="85201-105">JetOSSnapshotFreeze Function</span></span>

<span data-ttu-id="85201-106">Die **jeesssnapshotfreeze** -Funktion startet eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="85201-106">The **JetOSSnapshotFreeze** function starts a snapshot.</span></span> <span data-ttu-id="85201-107">Während der Momentaufnahme kann keine Aktivität zum Schreiben von Datenträgern durch die Engine durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="85201-107">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span>

<span data-ttu-id="85201-108">**Windows XP:**  **jedessnapshotfreeze** wurde in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="85201-108">**Windows XP:**  **JetOSSnapshotFreeze** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="85201-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="85201-109">Parameters</span></span>

<span data-ttu-id="85201-110">*snapid*</span><span class="sxs-lookup"><span data-stu-id="85201-110">*snapId*</span></span>

<span data-ttu-id="85201-111">Der Bezeichner der Momentaufnahme Sitzung.</span><span class="sxs-lookup"><span data-stu-id="85201-111">The identifier of the snapshot session.</span></span>

<span data-ttu-id="85201-112">*pcinstanceingefo*</span><span class="sxs-lookup"><span data-stu-id="85201-112">*pcInstanceInfo*</span></span>

<span data-ttu-id="85201-113">Die Anzahl der Instanzen, die zurzeit in der-Engine ausgeführt werden und Teil der Momentaufnahme Sitzung sind.</span><span class="sxs-lookup"><span data-stu-id="85201-113">The number of instances currently running in the engine that are part of the snapshot session.</span></span>

<span data-ttu-id="85201-114">*painstanceingefo*</span><span class="sxs-lookup"><span data-stu-id="85201-114">*paInstanceInfo*</span></span>

<span data-ttu-id="85201-115">Ein Array von-Strukturen, eines für jede laufende Instanz, die Teil der Momentaufnahme Sitzung ist, und beschreibt die Instanz und die Datenbanken, die Teil davon sind.</span><span class="sxs-lookup"><span data-stu-id="85201-115">An array of structures, one for each running instance that is part of the snapshot session, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="85201-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="85201-116">*grbit*</span></span>

<span data-ttu-id="85201-117">Die Optionen für diesen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="85201-117">The options for this call.</span></span> <span data-ttu-id="85201-118">Dieser Parameter ist für die zukünftige Verwendung reserviert, und der einzige gültige Wert ist 0.</span><span class="sxs-lookup"><span data-stu-id="85201-118">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="85201-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85201-119">Return Value</span></span>

<span data-ttu-id="85201-120">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="85201-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="85201-121">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="85201-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85201-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="85201-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="85201-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85201-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85201-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="85201-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="85201-125">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="85201-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85201-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="85201-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="85201-127">Die Zeiger, die für die Ausgabeparameter bereitgestellt werden, sind NULL, die Momentaufnahme Sitzung ist ungültig, oder der <em>grbit</em> -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="85201-127">The pointers provided for the output parameters are NULL, the snapshot session is invalid, or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85201-128">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="85201-128">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="85201-129">Die Momentaufnahme Sitzung befindet sich nicht im entsprechenden Zustand, um ein Einfrieren zu starten (z. b. ist ein vorheriger Einfrieren für diese Sitzung zuvor fehlgeschlagen).</span><span class="sxs-lookup"><span data-stu-id="85201-129">The snapshot session is not in the appropriate state to start a freeze (for example, a previous freeze failed on this session before).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85201-130">JET_errOSSnapshotNotAllowed</span><span class="sxs-lookup"><span data-stu-id="85201-130">JET_errOSSnapshotNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="85201-131">Die Engine befindet sich nicht in einem Zustand, in dem eine Momentaufnahme ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="85201-131">The engine is not in a state in which a snapshot can be performed.</span></span> <span data-ttu-id="85201-132">Mindestens eine Streamingsicherung wird bereits ausgeführt, oder eine oder mehrere Instanzen durchlaufen Wiederherstellungsschritte oder beenden.</span><span class="sxs-lookup"><span data-stu-id="85201-132">Either one or more streaming backups is already in progress, or one or more instances are going through recovery steps or terminating.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85201-133">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="85201-133">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="85201-134">Der Bezeichner für die Momentaufnahme Sitzung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="85201-134">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85201-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="85201-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="85201-136">Die Funktion konnte aufgrund einer nicht genügend Arbeitsspeicher Bedingung nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="85201-136">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85201-137">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="85201-137">JET_errOutOfThreads</span></span></p></td>
<td><p><span data-ttu-id="85201-138">Die Funktion ist fehlgeschlagen, da ein neuer Thread, der die Sperrung durchgeführt hat, nicht gestartet</span><span class="sxs-lookup"><span data-stu-id="85201-138">The function failed because a new thread doing the freeze failed to start.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="85201-139">Wenn diese Funktion erfolgreich ausgeführt wird, werden keine Schreibvorgänge für die Datenbankdateien oder die Protokolldateien ausgeführt, die Bestandteil der fixierten Instanzen sind.</span><span class="sxs-lookup"><span data-stu-id="85201-139">If this function succeeds, there will not be any write IOs issued for the database files or for the log files that are part of instances that are frozen.</span></span> <span data-ttu-id="85201-140">Außerdem werden die Instanzinformationen ordnungsgemäß ausgefüllt und müssen später freigegeben werden, indem [jetfrebuffer](./jetfreebuffer-function.md) mit dem Zeiger auf das zurückgegebene instanzinformationsarray aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="85201-140">Also, the instance information will be properly filled and it must be freed later on by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="85201-141">Wenn diese Funktion fehlschlägt, wird die Engine weiterhin normal ausgeführt, und die IOS-Funktion wird wie gewohnt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85201-141">If this function fails, the engine will keep running normally with the IOs occurring as usual.</span></span> <span data-ttu-id="85201-142">Wenn das Einfrieren fehlschlägt, muss [jedessnapshotthaw](./jetossnapshotthaw-function.md) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="85201-142">There is no need to call [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) if the freeze fails.</span></span> <span data-ttu-id="85201-143">Außerdem werden die Instanzinformationen nicht aufgefüllt, sodass es nicht erforderlich ist, diese Ressource freizugeben.</span><span class="sxs-lookup"><span data-stu-id="85201-143">Also, the instance information will not be filled so there is no need to free this resource.</span></span>

#### <a name="remarks"></a><span data-ttu-id="85201-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85201-144">Remarks</span></span>

<span data-ttu-id="85201-145">Während des Sperr Zeitraums werden keinerlei Schreib-e/a-Vorgänge für die angefügten Datenbanken oder die Transaktionsprotokolle ausgegeben, es kann jedoch sein, dass für die temporären Datenbanken oder Streamingdateien Schreibvorgänge für IOS ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="85201-145">During the freeze period, there will not be any write IOs issued to the attached databases or the transaction logs, although there might be write IOs issued to the temporary databases or streaming files.</span></span>

<span data-ttu-id="85201-146">Der Zustand, in dem sich die Datenbanken und die Protokolldateien während des Fixierens befinden (der Zustand, in dem sich die Dateien in einem Volumesnapshot-Image befinden) so, dass eine normale Wiederherstellung möglich ist, wenn diese Dateien später wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="85201-146">The state in which the databases and the log files will be during the freeze (the state in which the files would be in a Volume Snapshot image) will be such that a normal recovery will be possible if those files are restored later.</span></span>

<span data-ttu-id="85201-147">Da während des Sperr Zeitraums keine Schreibvorgänge vorhanden sind, können normale API-Aufrufe in der Engine für dieses Intervall angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="85201-147">Because there are no write operations during the freeze period, normal API calls into the engine might be stalled for that interval.</span></span> <span data-ttu-id="85201-148">Die Client Anwendung muss in der Lage sein, API-Aufrufe zu verarbeiten, die möglicherweise länger dauern, wenn ein Einfrieren auftritt.</span><span class="sxs-lookup"><span data-stu-id="85201-148">The client application must be able to handle API calls that might take longer then normal if a freeze occurs.</span></span>

<span data-ttu-id="85201-149">Aufgrund der oben beschriebenen möglichen Auswirkungen gibt es einen internen Timeout, nach dem die Momentaufnahme Sitzung die Freeze-Phase beendet, auch wenn die APIs, die den reaktivieren oder Abbruch durchgeführt haben, nicht aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="85201-149">Due to the possible effects described above, there is an internal timeout after which the snapshot session will stop the freeze phase even if the APIs doing the thaw or abort were not called.</span></span> <span data-ttu-id="85201-150">Der Wert des Timeouts kann mit dem [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) System-Parameter geändert werden.</span><span class="sxs-lookup"><span data-stu-id="85201-150">The value of the timeout can be changed using the [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) system parameter.</span></span> <span data-ttu-id="85201-151">Beachten Sie, dass sich das typische Sperr Intervall im Bereich von 10 Sekunden mit dem Standard Timeout von ungefähr 60 Sekunden befindet.</span><span class="sxs-lookup"><span data-stu-id="85201-151">Note that the typical freeze interval is in the range of 10 seconds with the default timeout somewhere around 60 seconds.</span></span>

#### <a name="requirements"></a><span data-ttu-id="85201-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85201-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85201-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="85201-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="85201-154">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="85201-154">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85201-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="85201-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="85201-156">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="85201-156">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85201-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="85201-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="85201-158">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="85201-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85201-159"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="85201-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="85201-160">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="85201-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85201-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="85201-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="85201-162">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="85201-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85201-163"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="85201-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="85201-164">Implementiert als <strong>jeumssnapshotfrezew</strong> (Unicode) und <strong>jeto ssnapshotfrezea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="85201-164">Implemented as <strong>JetOSSnapshotFreezeW</strong> (Unicode) and <strong>JetOSSnapshotFreezeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="85201-165">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="85201-165">See Also</span></span>

[<span data-ttu-id="85201-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="85201-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="85201-167">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="85201-167">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="85201-168">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="85201-168">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="85201-169">Jejessnapshotabort</span><span class="sxs-lookup"><span data-stu-id="85201-169">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="85201-170">Jejessnapshotprepare</span><span class="sxs-lookup"><span data-stu-id="85201-170">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="85201-171">Jejessnapshotprepareingestance</span><span class="sxs-lookup"><span data-stu-id="85201-171">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="85201-172">Jejessnapshotthaw</span><span class="sxs-lookup"><span data-stu-id="85201-172">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
