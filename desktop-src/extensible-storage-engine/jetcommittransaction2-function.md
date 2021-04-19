---
description: 'Weitere Informationen finden Sie hier: JetCommitTransaction2-Funktion'
title: JetCommitTransaction2-Funktion
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24dfecd091de027f51ed8f69c0441fbc7cbd57af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373318"
---
# <a name="jetcommittransaction2-function"></a><span data-ttu-id="5460b-103">JetCommitTransaction2-Funktion</span><span class="sxs-lookup"><span data-stu-id="5460b-103">JetCommitTransaction2 Function</span></span>


<span data-ttu-id="5460b-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5460b-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="5460b-105">Die **JetCommitTransaction2** -Funktion führt einen Commit für die Änderungen aus, die an den Zustand der Datenbank während des aktuellen Speicher Punkts vorgenommen werden, und migriert Sie zum vorherigen Sicherungspunkt.</span><span class="sxs-lookup"><span data-stu-id="5460b-105">The **JetCommitTransaction2** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="5460b-106">Wenn für den äußersten Speicherpunkt ein Commit ausgeführt wird, werden die während dieses Speicher Punkts vorgenommenen Änderungen an den Status der Datenbank übertragen, und die Sitzung wird beendet.</span><span class="sxs-lookup"><span data-stu-id="5460b-106">If the outermost save point is committed, the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="5460b-107">Die **JetCommitTransaction2** -Funktion wurde im Windows 8-Betriebssystem eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5460b-107">The **JetCommitTransaction2** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a><span data-ttu-id="5460b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5460b-108">Parameters</span></span>

<span data-ttu-id="5460b-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="5460b-109">*sesid*</span></span>

<span data-ttu-id="5460b-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5460b-110">The session to use for this call.</span></span>

<span data-ttu-id="5460b-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="5460b-111">*grbit*</span></span>

<span data-ttu-id="5460b-112">Eine Gruppe von Bits, die NULL oder mehr der in der folgenden Tabelle aufgeführten Werte angeben.</span><span class="sxs-lookup"><span data-stu-id="5460b-112">A group of bits that specify zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5460b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="5460b-113">Value</span></span></p></th>
<th><p><span data-ttu-id="5460b-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5460b-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5460b-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="5460b-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="5460b-116">Die Transaktion wird normal ausgeführt, aber diese API wartet nicht, bis die Transaktion in die Transaktionsprotokoll Datei geleert wurde, bevor Sie an den Aufrufer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5460b-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="5460b-117">Dadurch wird die Dauer eines Commitvorgangs drastisch reduziert und die Dauerhaftigkeit beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="5460b-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="5460b-118">Alle Transaktionen, die vor einem Absturz nicht in das Protokoll geschrieben werden, werden während des nächsten Aufrufens der <a href="gg294068(v=exchg.10).md">jetinit</a> -Funktion automatisch abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="5460b-118">Any transaction that is not flushed to the log before a crash will automatically be aborted during crash recovery during the next call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function.</span></span></p>
<p><span data-ttu-id="5460b-119">Wenn JET_bitWaitLastLevel0Commit oder JET_bitWaitAllLevel0Commit angegeben werden, wird diese Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5460b-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="5460b-120">Wenn dieser <strong>JetCommitTransaction2</strong> -Aufrufvorgang nicht mit dem ersten Aufrufen der <a href="gg294083(v=exchg.10).md">jetbegintransaction</a> -Funktion für diese Sitzung identisch ist, wird diese Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5460b-120">If this call to <strong>JetCommitTransaction2</strong> does not match the first call to the <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> function for this session, this option is ignored.</span></span> <span data-ttu-id="5460b-121">Dies liegt daran, dass die letzte Aktion, die auf dem äußersten Speicherpunkt auftritt, der bestimmende Faktor ist, der angibt, ob die gesamte Transaktion tatsächlich auf den Datenträger übertragen wird</span><span class="sxs-lookup"><span data-stu-id="5460b-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5460b-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="5460b-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="5460b-123">Alle Transaktionen, für die zuvor von einer Sitzung ein Commit ausgeführt wurde und die noch nicht in die Transaktionsprotokoll Datei geleert wurden, werden sofort geleert.</span><span class="sxs-lookup"><span data-stu-id="5460b-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="5460b-124">Diese API wartet, bis die Transaktionen geleert wurden, bevor Sie an den Aufrufer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5460b-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="5460b-125">Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</span><span class="sxs-lookup"><span data-stu-id="5460b-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="5460b-126">Diese Option kann nicht in Kombination mit anderen Optionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5460b-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="5460b-127">Diese Option ist ab Windows Server 2003 in Versionen des Windows Server-Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5460b-127">This option is available in versions of the Windows Server operating system starting with Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5460b-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="5460b-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="5460b-129">Wenn für die Sitzung bereits ein Commit für Transaktionen ausgeführt wurde und diese noch nicht in die Transaktionsprotokoll Datei geleert wurden, sollten Sie sofort geleert werden.</span><span class="sxs-lookup"><span data-stu-id="5460b-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="5460b-130">Diese API wartet, bis die Transaktionen geleert wurden, bevor Sie an den Aufrufer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5460b-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="5460b-131">Dies ist nützlich, wenn die Anwendung zuvor mehrere Transaktionen mit JET_bitCommitLazyFlush committet hat und diese nun auf den Datenträger leeren möchte.</span><span class="sxs-lookup"><span data-stu-id="5460b-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="5460b-132">Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</span><span class="sxs-lookup"><span data-stu-id="5460b-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="5460b-133">Diese Option kann nicht in Kombination mit anderen Optionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5460b-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5460b-134">*cmsecdurablecommit*</span><span class="sxs-lookup"><span data-stu-id="5460b-134">*cmsecDurableCommit*</span></span>

<span data-ttu-id="5460b-135">Die Dauer für das Commit einer verzögerten Transaktion.</span><span class="sxs-lookup"><span data-stu-id="5460b-135">The duration to commit a lazy transaction.</span></span>

<span data-ttu-id="5460b-136">*pcomentschärd*</span><span class="sxs-lookup"><span data-stu-id="5460b-136">*pCommitID*</span></span>

<span data-ttu-id="5460b-137">Die Commit-ID, die diesem Commitdatensatz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5460b-137">The Commit-ID associated with this commit record.</span></span>

### <a name="return-value"></a><span data-ttu-id="5460b-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5460b-138">Return value</span></span>

<span data-ttu-id="5460b-139">Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="5460b-139">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="5460b-140">Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Engine) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Fehler Behandlungsparameter](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5460b-140">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5460b-141">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5460b-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="5460b-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5460b-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5460b-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5460b-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5460b-144">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5460b-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5460b-145">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5460b-145">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5460b-146">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens der <a href="gg269240(v=exchg.10).md">jetstopservice</a> -Funktion beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="5460b-146">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5460b-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5460b-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5460b-148">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="5460b-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5460b-149">Dieser Fehler wird nur von Versionen des Windows-Betriebssystems ab Windows XP zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5460b-149">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5460b-150">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="5460b-150">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="5460b-151">Eine der angeforderten Optionen war ungültig oder nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="5460b-151">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="5460b-152">Dieser Fehler wird von der <strong>JetCommitTransaction2</strong> -Funktion zurückgegeben, wenn Folgendes geschieht:</span><span class="sxs-lookup"><span data-stu-id="5460b-152">This error will be returned by the <strong>JetCommitTransaction2</strong> function when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="5460b-153">Es wurde ein ungültiges <em>grbit</em> angegeben.</span><span class="sxs-lookup"><span data-stu-id="5460b-153">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="5460b-154">JET_bitWaitLastLevel0Commit wurde in Kombination mit einem anderen <em>grbit</em>angegeben.</span><span class="sxs-lookup"><span data-stu-id="5460b-154">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="5460b-155">JET_bitWaitAllLevel0Commit wurde in Kombination mit einem anderen <em>grbit</em>angegeben.</span><span class="sxs-lookup"><span data-stu-id="5460b-155">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5460b-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5460b-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5460b-157">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5460b-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5460b-158">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="5460b-158">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="5460b-159">Der Vorgang ist fehlgeschlagen, da die angegebene Sitzung nicht in einer Transaktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5460b-159">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5460b-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5460b-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5460b-161">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5460b-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5460b-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="5460b-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="5460b-163">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5460b-163">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="5460b-164">Dieser Fehler wird nur von Versionen des Windows-Betriebssystems ab Windows XP zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5460b-164">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5460b-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5460b-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5460b-166">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="5460b-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5460b-167">Bei Erfolg werden alle Änderungen, die während des aktuellen Speicher Punkts für die jeweilige Sitzung an der Datenbank vorgenommen wurden, committet, und der Sicherungspunkt wird beendet.</span><span class="sxs-lookup"><span data-stu-id="5460b-167">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="5460b-168">Wenn der letzte Sicherungspunkt für die Sitzung beendet wurde, wird die Transaktion optional in die Transaktionsprotokoll Datei geleert, und die Sitzung wird beendet.</span><span class="sxs-lookup"><span data-stu-id="5460b-168">If the last save point for the session was ended, the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="5460b-169">Bei einem Fehler bleibt der Transaktionsstatus der Sitzung unverändert.</span><span class="sxs-lookup"><span data-stu-id="5460b-169">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="5460b-170">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="5460b-170">No change to the database state will occur.</span></span> <span data-ttu-id="5460b-171">Die Anwendung sollte die [jetrollback](./jetrollback-function.md) -Funktion anrufen, um die Transaktion abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="5460b-171">The application should call the [JetRollback](./jetrollback-function.md) function to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5460b-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5460b-172">Remarks</span></span>

<span data-ttu-id="5460b-173">Es muss ein **JetCommitTransaction2** -oder [jetrollback](./jetrollback-function.md) -Rückruf vorhanden sein, um jeden Aufrufen von [jetbegintransaction](./jetbegintransaction-function.md) für eine bestimmte Sitzung abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="5460b-173">There must be one call to **JetCommitTransaction2** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5460b-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5460b-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5460b-175"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5460b-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5460b-176">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5460b-176">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5460b-177"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5460b-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5460b-178">Erfordert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5460b-178">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5460b-179"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5460b-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5460b-180">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="5460b-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5460b-181"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="5460b-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5460b-182">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5460b-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5460b-183"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5460b-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5460b-184">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5460b-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5460b-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5460b-185">See also</span></span>

[<span data-ttu-id="5460b-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5460b-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5460b-187">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5460b-187">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5460b-188">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5460b-188">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5460b-189">Jetbegintransaction</span><span class="sxs-lookup"><span data-stu-id="5460b-189">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="5460b-190">Jetcommittransaction</span><span class="sxs-lookup"><span data-stu-id="5460b-190">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="5460b-191">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="5460b-191">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="5460b-192">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="5460b-192">JetStopService</span></span>](./jetstopservice-function.md)
