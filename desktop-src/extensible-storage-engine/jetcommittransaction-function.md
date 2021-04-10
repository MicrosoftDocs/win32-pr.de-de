---
description: Weitere Informationen finden Sie in der jetcommittransaction-Funktion.
title: JetCommitTransaction-Funktion
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2fe42891aa916a428d63fb68c99f42f38e78993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960681"
---
# <a name="jetcommittransaction-function"></a><span data-ttu-id="81fc1-103">JetCommitTransaction-Funktion</span><span class="sxs-lookup"><span data-stu-id="81fc1-103">JetCommitTransaction Function</span></span>


<span data-ttu-id="81fc1-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="81fc1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcommittransaction-function"></a><span data-ttu-id="81fc1-105">JetCommitTransaction-Funktion</span><span class="sxs-lookup"><span data-stu-id="81fc1-105">JetCommitTransaction Function</span></span>

<span data-ttu-id="81fc1-106">Die **jetcommittransaction** -Funktion führt einen Commit für die Änderungen aus, die an den Zustand der Datenbank während des aktuellen Speicher Punkts vorgenommen werden, und migriert Sie zum vorherigen Sicherungspunkt.</span><span class="sxs-lookup"><span data-stu-id="81fc1-106">The **JetCommitTransaction** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="81fc1-107">Wenn für den äußersten Speicherpunkt ein Commit ausgeführt wird, werden die während dieses Speicher Punkts vorgenommenen Änderungen in den Zustand der Datenbank übertragen, und die Sitzung wird beendet.</span><span class="sxs-lookup"><span data-stu-id="81fc1-107">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="81fc1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="81fc1-108">Parameters</span></span>

<span data-ttu-id="81fc1-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="81fc1-109">*sesid*</span></span>

<span data-ttu-id="81fc1-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="81fc1-110">The session to use for this call.</span></span>

<span data-ttu-id="81fc1-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="81fc1-111">*grbit*</span></span>

<span data-ttu-id="81fc1-112">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="81fc1-112">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81fc1-113">Wert</span><span class="sxs-lookup"><span data-stu-id="81fc1-113">Value</span></span></p></th>
<th><p><span data-ttu-id="81fc1-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="81fc1-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81fc1-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="81fc1-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="81fc1-116">Die Transaktion wird normal ausgeführt, aber diese API wartet nicht, bis die Transaktion in die Transaktionsprotokoll Datei geleert wurde, bevor Sie an den Aufrufer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="81fc1-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="81fc1-117">Dadurch wird die Dauer eines Commitvorgangs drastisch reduziert und die Dauerhaftigkeit beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="81fc1-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="81fc1-118">Alle Transaktionen, die vor einem Absturz nicht in das Protokoll geschrieben werden, werden während des nächsten Aufrufens von <a href="gg294068(v=exchg.10).md">jetinit</a>automatisch abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="81fc1-118">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to <a href="gg294068(v=exchg.10).md">JetInit</a>.</span></span></p>
<p><span data-ttu-id="81fc1-119">Wenn JET_bitWaitLastLevel0Commit oder JET_bitWaitAllLevel0Commit angegeben werden, wird diese Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="81fc1-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="81fc1-120">Wenn dieser Befehl von <strong>jetcommittransaction</strong> nicht mit dem ersten Befehl von <a href="gg294083(v=exchg.10).md">jetbegintransaction</a> für diese Sitzung identisch ist, wird diese Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="81fc1-120">If this call to <strong>JetCommitTransaction</strong> does not match the first call to <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> for this session, this option is ignored.</span></span> <span data-ttu-id="81fc1-121">Dies liegt daran, dass die letzte Aktion, die auf dem äußersten Speicherpunkt auftritt, der bestimmende Faktor ist, der angibt, ob die gesamte Transaktion tatsächlich auf den Datenträger übertragen wird</span><span class="sxs-lookup"><span data-stu-id="81fc1-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81fc1-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="81fc1-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="81fc1-123">Alle Transaktionen, für die zuvor von einer Sitzung ein Commit ausgeführt wurde und die noch nicht in die Transaktionsprotokoll Datei geleert wurden, werden sofort geleert.</span><span class="sxs-lookup"><span data-stu-id="81fc1-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="81fc1-124">Diese API wartet, bis die Transaktionen geleert wurden, bevor Sie an den Aufrufer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="81fc1-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="81fc1-125">Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</span><span class="sxs-lookup"><span data-stu-id="81fc1-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="81fc1-126">Diese Option kann nicht in Kombination mit anderen Optionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81fc1-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="81fc1-127">Diese Option ist nur ab Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="81fc1-127">This option is only available as of Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81fc1-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="81fc1-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="81fc1-129">Wenn für die Sitzung bereits ein Commit für Transaktionen ausgeführt wurde und diese noch nicht in die Transaktionsprotokoll Datei geleert wurden, sollten Sie sofort geleert werden.</span><span class="sxs-lookup"><span data-stu-id="81fc1-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="81fc1-130">Diese API wartet, bis die Transaktionen geleert wurden, bevor Sie an den Aufrufer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="81fc1-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="81fc1-131">Dies ist nützlich, wenn die Anwendung zuvor mehrere Transaktionen mit JET_bitCommitLazyFlush committet hat und diese nun auf den Datenträger leeren möchte.</span><span class="sxs-lookup"><span data-stu-id="81fc1-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="81fc1-132">Diese Option kann auch verwendet werden, wenn sich die Sitzung derzeit nicht in einer Transaktion befindet.</span><span class="sxs-lookup"><span data-stu-id="81fc1-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="81fc1-133">Diese Option kann nicht in Kombination mit anderen Optionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81fc1-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="81fc1-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81fc1-134">Return Value</span></span>

<span data-ttu-id="81fc1-135">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="81fc1-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="81fc1-136">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="81fc1-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="81fc1-137">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="81fc1-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="81fc1-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81fc1-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81fc1-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="81fc1-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="81fc1-140">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="81fc1-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81fc1-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="81fc1-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="81fc1-142">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="81fc1-142">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81fc1-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="81fc1-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="81fc1-144">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="81fc1-144">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="81fc1-145">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81fc1-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81fc1-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="81fc1-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="81fc1-147">Eine der angeforderten Optionen war ungültig oder nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="81fc1-147">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="81fc1-148">Dieser Fehler wird von <strong>jetcommittransaction</strong> zurückgegeben, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="81fc1-148">This error will be returned by <strong>JetCommitTransaction</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="81fc1-149">Es wurde ein ungültiges <em>grbit</em> angegeben.</span><span class="sxs-lookup"><span data-stu-id="81fc1-149">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="81fc1-150">JET_bitWaitLastLevel0Commit wurde in Kombination mit einem anderen <em>grbit</em>angegeben.</span><span class="sxs-lookup"><span data-stu-id="81fc1-150">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="81fc1-151">JET_bitWaitAllLevel0Commit wurde in Kombination mit einem anderen <em>grbit</em>angegeben.</span><span class="sxs-lookup"><span data-stu-id="81fc1-151">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81fc1-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="81fc1-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="81fc1-153">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="81fc1-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81fc1-154">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="81fc1-154">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="81fc1-155">Der Vorgang ist fehlgeschlagen, da die angegebene Sitzung nicht in einer Transaktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81fc1-155">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81fc1-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="81fc1-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="81fc1-157">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81fc1-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81fc1-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="81fc1-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="81fc1-159">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81fc1-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="81fc1-160">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81fc1-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81fc1-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="81fc1-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="81fc1-162">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="81fc1-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="81fc1-163">Bei Erfolg werden alle Änderungen, die während des aktuellen Speicher Punkts für die jeweilige Sitzung an der Datenbank vorgenommen wurden, committet, und der Sicherungspunkt wird beendet.</span><span class="sxs-lookup"><span data-stu-id="81fc1-163">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="81fc1-164">Wenn der letzte Sicherungspunkt für die Sitzung beendet wurde, wird die Transaktion optional in die Transaktionsprotokoll Datei geleert, und die Sitzung wird beendet.</span><span class="sxs-lookup"><span data-stu-id="81fc1-164">If the last save point for the session was ended then the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="81fc1-165">Bei einem Fehler bleibt der Transaktionsstatus der Sitzung unverändert.</span><span class="sxs-lookup"><span data-stu-id="81fc1-165">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="81fc1-166">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="81fc1-166">No change to the database state will occur.</span></span> <span data-ttu-id="81fc1-167">Die Anwendung sollte [jetrollback](./jetrollback-function.md) anrufen, um die Transaktion abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="81fc1-167">The application should call [JetRollback](./jetrollback-function.md) to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="81fc1-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81fc1-168">Remarks</span></span>

<span data-ttu-id="81fc1-169">Es muss ein Aufrufen von **jetcommittransaction** oder [jetrollback](./jetrollback-function.md) vorhanden sein, um jeden beliebigen [jetbegintransaction](./jetbegintransaction-function.md) -Befehl für eine bestimmte Sitzung abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="81fc1-169">There must be one call to **JetCommitTransaction** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="81fc1-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81fc1-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="81fc1-171"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="81fc1-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="81fc1-172">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="81fc1-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81fc1-173"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="81fc1-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="81fc1-174">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="81fc1-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81fc1-175"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="81fc1-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="81fc1-176">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="81fc1-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="81fc1-177"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="81fc1-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="81fc1-178">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="81fc1-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="81fc1-179"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="81fc1-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="81fc1-180">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="81fc1-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="81fc1-181">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="81fc1-181">See Also</span></span>

[<span data-ttu-id="81fc1-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="81fc1-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="81fc1-183">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="81fc1-183">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="81fc1-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="81fc1-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="81fc1-185">Jetbegintransaction</span><span class="sxs-lookup"><span data-stu-id="81fc1-185">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="81fc1-186">Jetcommittransaction</span><span class="sxs-lookup"><span data-stu-id="81fc1-186">JetCommitTransaction</span></span>]()  
[<span data-ttu-id="81fc1-187">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="81fc1-187">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="81fc1-188">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="81fc1-188">JetStopService</span></span>](./jetstopservice-function.md)
