---
description: 'Weitere Informationen zu: jetendexternalbackup-Funktion'
title: JetEndExternalBackup-Funktion
TOCTitle: JetEndExternalBackup Function
ms:assetid: 058f903b-14b7-44b3-9ec7-7c05c9ec6363
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269176(v=EXCHG.10)
ms:contentKeyID: 32765479
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 91f3db40fef483114313bbaa5f01e592d860bde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354015"
---
# <a name="jetendexternalbackup-function"></a><span data-ttu-id="a4365-103">JetEndExternalBackup-Funktion</span><span class="sxs-lookup"><span data-stu-id="a4365-103">JetEndExternalBackup Function</span></span>


<span data-ttu-id="a4365-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a4365-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackup-function"></a><span data-ttu-id="a4365-105">JetEndExternalBackup-Funktion</span><span class="sxs-lookup"><span data-stu-id="a4365-105">JetEndExternalBackup Function</span></span>

<span data-ttu-id="a4365-106">Die **jetendexternalbackup** -Funktion beendet eine externe Sicherungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a4365-106">The **JetEndExternalBackup** function ends an external backup session.</span></span> <span data-ttu-id="a4365-107">Diese Funktion ist das letzte API-Element in einer Reihe von API-Elementen, die aufgerufen werden müssen, um eine erfolgreiche Online Sicherung (nicht VSS-basiert) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a4365-107">This function is the last API element in a series of API elements that must be called to execute a successful online (non-VSS based) backup.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="a4365-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4365-108">Parameters</span></span>

<span data-ttu-id="a4365-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a4365-109">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="a4365-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4365-110">Return Value</span></span>

<span data-ttu-id="a4365-111">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="a4365-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a4365-112">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a4365-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4365-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a4365-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="a4365-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4365-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4365-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a4365-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a4365-116">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a4365-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4365-117">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a4365-117">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a4365-118">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a4365-118">The operation cannot complete because the instance that is associated with the session has not been yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4365-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a4365-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a4365-120">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a4365-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4365-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a4365-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a4365-122"><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a4365-122"><strong>Windows XP:  </strong>This return value is introduced in Windows XP</span></span></p>
<p><span data-ttu-id="a4365-123">Der Vorgang kann nicht ausgeführt werden, da der-Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der den Zugriff auf alle Daten widerrufen muss, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="a4365-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4365-124">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a4365-124">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a4365-125">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="a4365-125">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4365-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a4365-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a4365-127">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4365-127">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4365-128">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="a4365-128">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="a4365-129">Der Vorgang ist fehlgeschlagen, da keine externe Sicherung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4365-129">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4365-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="a4365-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="a4365-131"><strong>Windows Server 2003:  </strong> Dieser Rückgabewert wird in Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a4365-131"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="a4365-132">Der Vorgang ist fehlgeschlagen, da die aktuelle externe Sicherung durch einen <a href="gg294067(v=exchg.10).md">jetstopbackup</a>-Befehl abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="a4365-132">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4365-133">errbackupabortbycaller</span><span class="sxs-lookup"><span data-stu-id="a4365-133">errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="a4365-134"><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a4365-134"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="a4365-135">Der Aufrufer hat eine Sicherung in der Mitte der Sicherungs Sequenz beendet, ohne die Absicht mit <a href="gg294067(v=exchg.10).md">jetstopbackup</a>zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="a4365-135">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="a4365-136">Dieser Fehler ist auf einen Fehler im Sicherungs Client in Windows Server 2003 und höher zurückzuführen.</span><span class="sxs-lookup"><span data-stu-id="a4365-136">This error is a result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="a4365-137">Unter Windows XP wird dieser Fehler für eine absichtliche Beendigung der externen Sicherungs Sequenz zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a4365-137">On Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4365-138">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="a4365-138">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="a4365-139">Der Vorgang ist fehlgeschlagen, weil versucht wurde, die Engine im Legacy Modus (Windows 2000-Kompatibilitätsmodus) zu verwenden, in dem nur eine Instanz unterstützt wird, wenn in der Tat mehrere Instanzen bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a4365-139">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a4365-140">Wenn diese Funktion erfolgreich ausgeführt wird, war die externe Sicherung erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a4365-140">If this function succeeds, the external backup was a success.</span></span> <span data-ttu-id="a4365-141">Erfolg gibt an, dass alle Dateien (z. b. Datenbanken und Protokolle), die für den Sicherungstyp (in [jetbeginexternalbackup](./jetbeginexternalbackup-function.md)angegeben) geeignet sind, von der Sicherungs-Engine abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="a4365-141">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="a4365-142">Die gesicherten Dateien können mit Hard Recovery ([jetexternalrestore](./jetexternalrestore-function.md)) wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a4365-142">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="a4365-143">Wenn diese Funktion fehlschlägt, wird die externe Sicherung normalerweise beendet.</span><span class="sxs-lookup"><span data-stu-id="a4365-143">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="a4365-144">"Fehler" bedeutet, dass die Sicherung aufgrund eines Fehlers bei der Client-oder Anwendungs Verwendung ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="a4365-144">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="a4365-145">Es ist wichtig, den Rückgabecode für diese API zu überprüfen, um zu überprüfen, ob die Sicherungs Sequenz erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a4365-145">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a4365-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4365-146">Remarks</span></span>

<span data-ttu-id="a4365-147">Wenn die Engine zum Protokollieren von Ereignissen konfiguriert ist, wird ein Ereignis protokolliert, um die Auflösung der externen Sicherung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a4365-147">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="a4365-148">Wenn die Sicherungs Sequenz nicht in der richtigen Reihenfolge und mit einem erfolgreichen Rückruf von **jetendexternalbackup** abgeschlossen ist, können nachfolgende inkrementelle Sicherungen mehr Daten enthalten, als die Anwendung erwartet hat.</span><span class="sxs-lookup"><span data-stu-id="a4365-148">If the backup sequence is not completed in order and with a successful call to **JetEndExternalBackup**, subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="a4365-149">Weitere Informationen zur API-Sequenz für die externe Sicherung finden Sie unter [jetbeginexternalbackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="a4365-149">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="a4365-150">Vor Windows Vista hat die Engine, wenn die Protokoll Verkürzung nicht durchgeführt wurde, die Sicherung als Kopier Sicherung angesehen.</span><span class="sxs-lookup"><span data-stu-id="a4365-150">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="a4365-151">Allerdings kann es sich bei der Sicherung um eine normale Sicherung handeln, bei der die abkürzen nicht durchgeführt wurde (z. b. Wenn separate Datenbanken vorhanden sind).</span><span class="sxs-lookup"><span data-stu-id="a4365-151">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="a4365-152">Mithilfe der Option JET_bitBackupTruncateDone können Sie die Engine über diese Informationen informieren und entsprechende Daten Bank Header Änderungen zulassen.</span><span class="sxs-lookup"><span data-stu-id="a4365-152">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow appropriate database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a4365-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4365-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4365-154"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a4365-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a4365-155">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a4365-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4365-156"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a4365-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a4365-157">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a4365-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4365-158"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a4365-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a4365-159">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a4365-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4365-160"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="a4365-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a4365-161">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a4365-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4365-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a4365-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a4365-163">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a4365-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a4365-164">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a4365-164">See Also</span></span>

[<span data-ttu-id="a4365-165">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="a4365-165">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="a4365-166">Erweiterbare Speicher-Engine-Fehler</span><span class="sxs-lookup"><span data-stu-id="a4365-166">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="a4365-167">Jetattachdatabase</span><span class="sxs-lookup"><span data-stu-id="a4365-167">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="a4365-168">Jetbeginexternalbackup</span><span class="sxs-lookup"><span data-stu-id="a4365-168">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="a4365-169">Jetclosefile</span><span class="sxs-lookup"><span data-stu-id="a4365-169">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="a4365-170">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a4365-170">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a4365-171">Jetexternalrestore</span><span class="sxs-lookup"><span data-stu-id="a4365-171">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="a4365-172">Jetgetattachinfo</span><span class="sxs-lookup"><span data-stu-id="a4365-172">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="a4365-173">Jetgetloginfo</span><span class="sxs-lookup"><span data-stu-id="a4365-173">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="a4365-174">Jetopumfile</span><span class="sxs-lookup"><span data-stu-id="a4365-174">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="a4365-175">Jetreadfile</span><span class="sxs-lookup"><span data-stu-id="a4365-175">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="a4365-176">Jetstopbackup</span><span class="sxs-lookup"><span data-stu-id="a4365-176">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="a4365-177">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="a4365-177">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="a4365-178">Jettruneurelog</span><span class="sxs-lookup"><span data-stu-id="a4365-178">JetTruncateLog</span></span>](./jettruncatelog-function.md)
