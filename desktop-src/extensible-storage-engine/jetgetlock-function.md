---
description: 'Weitere Informationen: jetgetlock-Funktion'
title: Jetgetlock-Funktion
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5757616214336de25ce30ca49755ac229b10afbe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104132433"
---
# <a name="jetgetlock-function"></a><span data-ttu-id="0bec4-103">Jetgetlock-Funktion</span><span class="sxs-lookup"><span data-stu-id="0bec4-103">JetGetLock Function</span></span>


<span data-ttu-id="0bec4-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0bec4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetlock-function"></a><span data-ttu-id="0bec4-105">Jetgetlock-Funktion</span><span class="sxs-lookup"><span data-stu-id="0bec4-105">JetGetLock Function</span></span>

<span data-ttu-id="0bec4-106">Die **jetgetlock** -Funktion bietet die Möglichkeit, die Möglichkeit zum Aktualisieren von Zeilen, Schreiben einer Sperre oder explizit zu verhindern, dass eine Zeile von einer anderen Sitzung (Lesesperre) aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0bec4-106">The **JetGetLock** function provides a means to explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="0bec4-107">Normalerweise werden Zeilen Schreib Sperren implizit durch das Aktualisieren von Zeilen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0bec4-107">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="0bec4-108">Lese Sperren sind in der Regel aufgrund von Daten Satz Versionsverwaltung nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0bec4-108">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="0bec4-109">In einigen Fällen möchte eine Transaktion jedoch möglicherweise eine Zeile explizit sperren, um die Serialisierung zu erzwingen, oder um sicherzustellen, dass ein nachfolgender Vorgang erfolgreich ausgeführt wird, da die erforderlichen Sperren bereits übernommen wurden.</span><span class="sxs-lookup"><span data-stu-id="0bec4-109">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed by virtue that required locks have already been taken.</span></span>

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="0bec4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bec4-110">Parameters</span></span>

<span data-ttu-id="0bec4-111">*-sid*</span><span class="sxs-lookup"><span data-stu-id="0bec4-111">*sesid*</span></span>

<span data-ttu-id="0bec4-112">Die Sitzung, die für diesen-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0bec4-112">The session that will be used for this call.</span></span>

<span data-ttu-id="0bec4-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="0bec4-113">*tableid*</span></span>

<span data-ttu-id="0bec4-114">Der Cursor, der für diesen-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0bec4-114">The cursor that will be used for this call.</span></span>

<span data-ttu-id="0bec4-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="0bec4-115">*grbit*</span></span>

<span data-ttu-id="0bec4-116">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="0bec4-116">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bec4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0bec4-117">Value</span></span></p></th>
<th><p><span data-ttu-id="0bec4-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0bec4-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bec4-119">JET_bitReadLock</span><span class="sxs-lookup"><span data-stu-id="0bec4-119">JET_bitReadLock</span></span></p></td>
<td><p><span data-ttu-id="0bec4-120">Dieses Flag bewirkt, dass eine Lesesperre für den aktuellen Datensatz abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0bec4-120">This flag causes a read lock to be acquired on the current record.</span></span> <span data-ttu-id="0bec4-121">Lese Sperren sind nicht kompatibel mit Schreib sperren, die bereits von anderen Sitzungen gehalten wurden, aber mit Lese Sperren von anderen Sitzungen kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="0bec4-121">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bec4-122">JET_bitWriteLock</span><span class="sxs-lookup"><span data-stu-id="0bec4-122">JET_bitWriteLock</span></span></p></td>
<td><p><span data-ttu-id="0bec4-123">Dieses Flag bewirkt, dass eine Schreibsperre für den aktuellen Datensatz abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0bec4-123">This flag causes a write lock to be acquired on the current record.</span></span> <span data-ttu-id="0bec4-124">Schreib Sperren sind nicht kompatibel mit Schreib-oder Lese sperren, die von anderen Sitzungen aufrechterhalten werden, aber mit Lese Sperren in derselben Sitzung kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="0bec4-124">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0bec4-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0bec4-125">Return Value</span></span>

<span data-ttu-id="0bec4-126">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="0bec4-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0bec4-127">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0bec4-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bec4-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0bec4-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="0bec4-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0bec4-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bec4-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0bec4-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0bec4-131">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0bec4-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bec4-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="0bec4-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="0bec4-133">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="0bec4-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bec4-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="0bec4-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="0bec4-135">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="0bec4-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="0bec4-136">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0bec4-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bec4-137">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="0bec4-137">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="0bec4-138">Das angegebene <em>grbit</em> ist weder JET_bitReadLock noch JET_bitWriteLock.</span><span class="sxs-lookup"><span data-stu-id="0bec4-138">The given <em>grbit</em> is neither JET_bitReadLock or JET_bitWriteLock.</span></span> <span data-ttu-id="0bec4-139">Dabei muss es sich um eines dieser beiden Flags handeln.</span><span class="sxs-lookup"><span data-stu-id="0bec4-139">It must be one of these two flags.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bec4-140">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="0bec4-140">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="0bec4-141">Der Cursor muss sich in einem Datensatz befinden, um eine Sperre zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0bec4-141">Cursor must be on a record in order to acquire a lock.</span></span> <span data-ttu-id="0bec4-142">Sperren sind Always on-Datensätze.</span><span class="sxs-lookup"><span data-stu-id="0bec4-142">Locks are always on records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bec4-143">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="0bec4-143">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="0bec4-144">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0bec4-144">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bec4-145">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="0bec4-145">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="0bec4-146">Sperren können nur von Sitzungen in einer Transaktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0bec4-146">Locks can only be acquired by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bec4-147">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="0bec4-147">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="0bec4-148">Der Cursor kann nicht schreibgeschützt sein und eine Schreibsperre erhalten.</span><span class="sxs-lookup"><span data-stu-id="0bec4-148">Cursor cannot be read only and acquire a write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bec4-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="0bec4-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="0bec4-150">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0bec4-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bec4-151">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="0bec4-151">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="0bec4-152">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bec4-152">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="0bec4-153">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0bec4-153">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bec4-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="0bec4-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="0bec4-155">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="0bec4-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bec4-156">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="0bec4-156">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="0bec4-157">Die Sitzung muss über Schreibberechtigungen verfügen, um eine Schreibsperre zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0bec4-157">Session must have write permissions to acquire write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bec4-158">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="0bec4-158">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="0bec4-159">Der Fehler, der zurückgegeben wird, wenn eine widersprüchliche Sperre angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="0bec4-159">The error returned when a conflicting lock is requested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0bec4-160">Bei Erfolg hat die Sitzung die angeforderte Sperre erhalten.</span><span class="sxs-lookup"><span data-stu-id="0bec4-160">On success, session has acquired requested lock.</span></span>

<span data-ttu-id="0bec4-161">Bei einem Fehler hat die Sitzung die angeforderte Sperre nicht abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0bec4-161">On failure, session has not acquired requested lock.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0bec4-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bec4-162">Remarks</span></span>

<span data-ttu-id="0bec4-163">Schreib Sperren können nicht mit Sitzungen oder Cursorn mit schreibgeschützten Berechtigungen abgerufen werden, auch wenn die Sitzung und der Cursor letztendlich keinen Aktualisierungs Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="0bec4-163">Write locks cannot be acquired with sessions or cursors that have read-only permissions, even if the session and cursor ultimately do not perform an update operation.</span></span> <span data-ttu-id="0bec4-164">Sowohl die Sitzung als auch der Cursor müssen über Schreibberechtigungen verfügen, um eine Schreibsperre zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0bec4-164">Both the session and the cursor must have write privileges in order to acquire a write lock.</span></span>

<span data-ttu-id="0bec4-165">Lese-und Schreib Sperren sind eine Möglichkeit der pessimistischen Sperrung.</span><span class="sxs-lookup"><span data-stu-id="0bec4-165">Read and write locks are a means of pessimistic locking.</span></span> <span data-ttu-id="0bec4-166">Das pessimistische sperren erwartet, dass mehrere gleichzeitige Sitzungen in Konflikt stehen und Sperren im Voraus erhalten, um sicherzustellen, dass Ihre Vorgänge erfolgreich</span><span class="sxs-lookup"><span data-stu-id="0bec4-166">Pessimistic locking expects multiple concurrent sessions to conflict and acquire locks in advance to ensure that their operations succeed.</span></span>

<span data-ttu-id="0bec4-167">Die meisten Vorgänge werden aufgrund von implizit ergriffene Sperren serialisierbar sein.</span><span class="sxs-lookup"><span data-stu-id="0bec4-167">Most operations will be serializable by virtue of locks implicitly taken.</span></span> <span data-ttu-id="0bec4-168">Bei einigen Vorgängen wird dies jedoch nicht der Fall sein.</span><span class="sxs-lookup"><span data-stu-id="0bec4-168">However, some operations will not.</span></span> <span data-ttu-id="0bec4-169">Um dies zu veranschaulichen, sehen Sie sich die beiden Transaktionen an:</span><span class="sxs-lookup"><span data-stu-id="0bec4-169">To illustrate this, consider the two transactions,</span></span>

<span data-ttu-id="0bec4-170">T1: R (a), U (B)</span><span class="sxs-lookup"><span data-stu-id="0bec4-170">T1 : R(A), U(B)</span></span>

<span data-ttu-id="0bec4-171">T2: R (B), U (a)</span><span class="sxs-lookup"><span data-stu-id="0bec4-171">T2 : R(B), U(A)</span></span>

<span data-ttu-id="0bec4-172">Durch die Versionsverwaltung auf Datensatzebene wird sichergestellt, dass jede Transaktion bei gleichzeitiger Ausführung die ursprünglichen Werte für A und B angezeigt wird. Es gibt keine serielle Reihenfolge der Ausführung, die dieselben Ergebnisse für A und B erzielen kann, wenn die Ergebnisse von den gelesenen Daten abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="0bec4-172">Record level versioning will ensure that each transaction when executed concurrently will see the original values for A and B. There is no serial order of execution that could produce the same results for A and B in the case that the results are dependent upon the data read.</span></span> <span data-ttu-id="0bec4-173">Damit die Anwendung diese Transaktion serialisierbar macht, sollte Sie eine explizite Lesesperre für A und B in jeder Transaktion erhalten, wenn der Wert gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="0bec4-173">In order for the application to make this transaction serializable, it should acquire an explicit read lock on A and B in each transaction when the value is read.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0bec4-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bec4-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bec4-175"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0bec4-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0bec4-176">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0bec4-176">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bec4-177"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0bec4-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0bec4-178">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0bec4-178">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bec4-179"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0bec4-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0bec4-180">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="0bec4-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bec4-181"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="0bec4-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0bec4-182">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0bec4-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bec4-183"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0bec4-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0bec4-184">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0bec4-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0bec4-185">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0bec4-185">See Also</span></span>

[<span data-ttu-id="0bec4-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0bec4-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0bec4-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0bec4-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0bec4-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0bec4-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0bec4-189">Jetprepareupdate</span><span class="sxs-lookup"><span data-stu-id="0bec4-189">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="0bec4-190">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="0bec4-190">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="0bec4-191">Jetupdate</span><span class="sxs-lookup"><span data-stu-id="0bec4-191">JetUpdate</span></span>](./jetupdate-function.md)
