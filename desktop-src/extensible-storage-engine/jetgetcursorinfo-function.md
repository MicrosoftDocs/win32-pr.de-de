---
description: Weitere Informationen finden Sie in der jetgetcurrsorinfo-Funktion
title: Jetgetcurrsorinfo-Funktion
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7201c37f79f68deead837cdcdd90402e4b2bf1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366506"
---
# <a name="jetgetcursorinfo-function"></a><span data-ttu-id="c7260-103">Jetgetcurrsorinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="c7260-103">JetGetCursorInfo Function</span></span>


<span data-ttu-id="c7260-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c7260-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcursorinfo-function"></a><span data-ttu-id="c7260-105">Jetgetcurrsorinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="c7260-105">JetGetCursorInfo Function</span></span>

<span data-ttu-id="c7260-106">Die **jetgetcursorinfo** -Funktion wird verwendet, um zu bestimmen, ob ein Update des aktuellen Datensatzes eines Cursors basierend auf dem aktuellen Update Status des Datensatzes zu einem Schreib Konflikt führt.</span><span class="sxs-lookup"><span data-stu-id="c7260-106">The **JetGetCursorInfo** function is used to determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="c7260-107">Es ist möglich, dass ein Schreib Konflikt letztendlich zurückgegeben wird, auch wenn **jetgetcurrsorinfo** JET_errSuccess zurückgibt, da eine andere Sitzung den Datensatz aktualisieren kann, bevor die aktuelle Sitzung denselben Datensatz aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="c7260-107">It is possible that a write conflict will ultimately be returned even if **JetGetCursorInfo** returns JET_errSuccess, because another session may update the record before the current session is able to update the same record.</span></span>

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="c7260-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7260-108">Parameters</span></span>

<span data-ttu-id="c7260-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="c7260-109">*sesid*</span></span>

<span data-ttu-id="c7260-110">Die Sitzung, die für diesen-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7260-110">The session that will be used for this call.</span></span>

<span data-ttu-id="c7260-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="c7260-111">*tableid*</span></span>

<span data-ttu-id="c7260-112">Der Cursor, der für diesen-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7260-112">The cursor that will be used for this call.</span></span>

<span data-ttu-id="c7260-113">*pvresult*</span><span class="sxs-lookup"><span data-stu-id="c7260-113">*pvResult*</span></span>

<span data-ttu-id="c7260-114">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="c7260-114">Reserved for future use.</span></span>

<span data-ttu-id="c7260-115">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="c7260-115">*cbMax*</span></span>

<span data-ttu-id="c7260-116">Muss auf 0 (null) festgelegt werden, andernfalls nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7260-116">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="c7260-117">Es ist für zukünftige Funktionen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7260-117">It is present for future functionality.</span></span>

<span data-ttu-id="c7260-118">*Infolevel*</span><span class="sxs-lookup"><span data-stu-id="c7260-118">*InfoLevel*</span></span>

<span data-ttu-id="c7260-119">Muss auf 0 (null) festgelegt werden, andernfalls nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7260-119">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="c7260-120">Es ist für zukünftige Funktionen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7260-120">It is present for future functionality.</span></span>

### <a name="return-value"></a><span data-ttu-id="c7260-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7260-121">Return Value</span></span>

<span data-ttu-id="c7260-122">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="c7260-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c7260-123">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c7260-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7260-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c7260-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="c7260-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7260-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7260-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c7260-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c7260-127">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c7260-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7260-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c7260-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c7260-129">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="c7260-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7260-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c7260-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c7260-131">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="c7260-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c7260-132">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c7260-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7260-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c7260-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c7260-134"><em>Cbmax</em> ist nicht 0 (null), oder <em>infolevel</em> ist nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c7260-134">Either <em>cbMax</em> is not 0 (zero) or <em>InfoLevel</em> is not 0 (zero).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7260-135">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="c7260-135">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="c7260-136">Der Cursor befindet sich derzeit nicht in einem Datensatz, und die Informationen zu einem logischen Datensatz können nicht als Ergebnis zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c7260-136">The cursor is not currently on a record and information on a logical record cannot be returned as a result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7260-137">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c7260-137">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c7260-138">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c7260-138">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7260-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c7260-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c7260-140">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7260-140">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7260-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c7260-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c7260-142">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7260-142">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="c7260-143">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c7260-143">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7260-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c7260-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c7260-145">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="c7260-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7260-146">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="c7260-146">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="c7260-147">Der aktuelle Datensatz des Cursors wurde von einer anderen Sitzung aktualisiert, und ein Update dieses Datensatzes durch diese Sitzung führt zu einem Schreib Konflikt.</span><span class="sxs-lookup"><span data-stu-id="c7260-147">The current record of the cursor has been updated by another session and an update of this record by this session will result in a write conflict.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c7260-148">Bei Erfolg hat dieser Vorgang keine Auswirkung auf die Position des Cursors, sondern gibt nur an, dass dieser Datensatz zurzeit von keiner anderen Sitzung aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c7260-148">On success, this operation has no effect on the location of the cursor but only indicates that no other session has currently updated this record.</span></span>

<span data-ttu-id="c7260-149">Bei einem Fehler gibt es keine Auswirkung auf den Cursor oder die Datenbank, wenn ein negativer Fehlercode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c7260-149">On failure, if a negative error code is returned there are no effects to the cursor or the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c7260-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7260-150">Remarks</span></span>

<span data-ttu-id="c7260-151">Dieser Vorgang wirkt sich nicht auf den Status des Cursors oder der Daten aus.</span><span class="sxs-lookup"><span data-stu-id="c7260-151">This operation does not affect the state of the cursor or the data.</span></span> <span data-ttu-id="c7260-152">Es wird nur ein Fehlercode zurückgegeben, der beschreibt, ob ein Update des aktuellen Datensatzes durch die aufrufende Sitzung bekanntermaßen zu einer JET_errWriteConflict führt oder unbekannt ist, JET_errWriteConflict zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c7260-152">It only returns an error code describing whether an update to the current record by the calling session is known to result in a JET_errWriteConflict, or is unknown to return JET_errWriteConflict.</span></span> <span data-ttu-id="c7260-153">Wenn dieser Datensatz bereits von einer anderen Sitzung aktualisiert wurde, um ihn zu verwenden, ist sicherzustellen, dass ein Update dieses Datensatzes durch diese Sitzung zu einem Schreib Konflikt führt.</span><span class="sxs-lookup"><span data-stu-id="c7260-153">If another session has already updated this record to use it is certain that an update of this record by this session will result in a write conflict.</span></span> <span data-ttu-id="c7260-154">Dies gilt, bis diese Sitzung einen Commit oder Rollback der Transaktionen auf die Transaktionsebene 0 (null) ausführt.</span><span class="sxs-lookup"><span data-stu-id="c7260-154">This will be true until this session commits or rolls back its transactions to transaction level 0 (zero).</span></span> <span data-ttu-id="c7260-155">Wenn **jetgetcursor Info** jedoch JET_errSuccess zurückgibt, ist es weiterhin möglich, dass eine andere Sitzung diesen Datensatz vor der aktuellen Sitzung aktualisiert. Folglich ist es weiterhin möglich, dass ein Update des aktuellen Datensatzes durch diese Sitzung in der aktuellen Transaktion zu einem Schreib Konflikt führt.</span><span class="sxs-lookup"><span data-stu-id="c7260-155">However, if **JetGetCursorInfo** returns JET_errSuccess, it is still possible for another session to update this record before the current session and thus it is still possible that an update of the current record by this session in its current transaction will result in a write conflict.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c7260-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7260-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7260-157"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c7260-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c7260-158">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c7260-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7260-159"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c7260-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c7260-160">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c7260-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7260-161"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c7260-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c7260-162">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="c7260-162">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7260-163"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="c7260-163"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c7260-164">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c7260-164">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7260-165"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c7260-165"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c7260-166">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c7260-166">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c7260-167">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c7260-167">See Also</span></span>

[<span data-ttu-id="c7260-168">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c7260-168">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c7260-169">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c7260-169">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c7260-170">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c7260-170">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c7260-171">Jetgetlock</span><span class="sxs-lookup"><span data-stu-id="c7260-171">JetGetLock</span></span>](./jetgetlock-function.md)  
[<span data-ttu-id="c7260-172">Jetprepareupdate</span><span class="sxs-lookup"><span data-stu-id="c7260-172">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="c7260-173">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="c7260-173">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="c7260-174">Jetupdate</span><span class="sxs-lookup"><span data-stu-id="c7260-174">JetUpdate</span></span>](./jetupdate-function.md)
