---
description: 'Weitere Informationen zu: jetescrowupdate-Funktion'
title: JetEscrowUpdate-Funktion
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb49d50ee7c529174fe4c5546efd7de1727892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369753"
---
# <a name="jetescrowupdate-function"></a><span data-ttu-id="ff430-103">JetEscrowUpdate-Funktion</span><span class="sxs-lookup"><span data-stu-id="ff430-103">JetEscrowUpdate Function</span></span>


<span data-ttu-id="ff430-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ff430-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetescrowupdate-function"></a><span data-ttu-id="ff430-105">JetEscrowUpdate-Funktion</span><span class="sxs-lookup"><span data-stu-id="ff430-105">JetEscrowUpdate Function</span></span>

<span data-ttu-id="ff430-106">Die **jetescrowupdate** -Funktion führt eine atomarische Additions Operation für eine Spalte aus.</span><span class="sxs-lookup"><span data-stu-id="ff430-106">The **JetEscrowUpdate** function performs an atomic addition operation on one column.</span></span> <span data-ttu-id="ff430-107">Diese Funktion ermöglicht es mehreren Sitzungen, denselben Datensatz gleichzeitig zu aktualisieren, ohne dass Konflikte auftreten.</span><span class="sxs-lookup"><span data-stu-id="ff430-107">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="ff430-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff430-108">Parameters</span></span>

<span data-ttu-id="ff430-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="ff430-109">*sesid*</span></span>

<span data-ttu-id="ff430-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff430-110">The session to use for this call.</span></span>

<span data-ttu-id="ff430-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="ff430-111">*tableid*</span></span>

<span data-ttu-id="ff430-112">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff430-112">The cursor to use for this call.</span></span>

<span data-ttu-id="ff430-113">*ColumnID*</span><span class="sxs-lookup"><span data-stu-id="ff430-113">*columnid*</span></span>

<span data-ttu-id="ff430-114">Das *ColumnID* der zu aktualisierenden Spalte.</span><span class="sxs-lookup"><span data-stu-id="ff430-114">The *columnid* of the column to be updated.</span></span>

<span data-ttu-id="ff430-115">*teuren*</span><span class="sxs-lookup"><span data-stu-id="ff430-115">*pv*</span></span>

<span data-ttu-id="ff430-116">Ein Zeiger auf einen Puffer, der den Addend für die Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="ff430-116">A pointer to a buffer containing the addend for the column.</span></span>

<span data-ttu-id="ff430-117">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="ff430-117">*cbMax*</span></span>

<span data-ttu-id="ff430-118">Die Größe des Puffers, der den Addend enthält.</span><span class="sxs-lookup"><span data-stu-id="ff430-118">The size of the buffer containing the addend.</span></span>

<span data-ttu-id="ff430-119">*pvold*</span><span class="sxs-lookup"><span data-stu-id="ff430-119">*pvOld*</span></span>

<span data-ttu-id="ff430-120">Der Ausgabepuffer, der den aktuellen Wert der Spalte erhält, wie er in der Datenbank gespeichert wird (die Versionsverwaltung wird ignoriert).</span><span class="sxs-lookup"><span data-stu-id="ff430-120">The output buffer that will receive the current value of the column as stored in the database (versioning is ignored).</span></span>

<span data-ttu-id="ff430-121">*cboldmax*</span><span class="sxs-lookup"><span data-stu-id="ff430-121">*cbOldMax*</span></span>

<span data-ttu-id="ff430-122">Die maximale Größe des Ausgabepuffers, der den aktuellen Wert der Spalte empfängt.</span><span class="sxs-lookup"><span data-stu-id="ff430-122">The maximum size of the output buffer that will receive the current value of the column.</span></span> <span data-ttu-id="ff430-123">Derzeit wird nur JET_coltypLong unterstützt, daher muss der Puffer entweder 4 Bytes oder 0 Byte lang sein.</span><span class="sxs-lookup"><span data-stu-id="ff430-123">Currently only JET_coltypLong is supported, so the buffer must either be 4 bytes or 0 bytes in length.</span></span> <span data-ttu-id="ff430-124">Wenn *pvold* NULL ist, sollte *cboldmax* den Wert 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ff430-124">If *pvOld* is NULL then *cbOldMax* should be 0.</span></span>

<span data-ttu-id="ff430-125">*pcboldactual*</span><span class="sxs-lookup"><span data-stu-id="ff430-125">*pcbOldActual*</span></span>

<span data-ttu-id="ff430-126">Empfängt die tatsächliche Menge an rohwertdaten, die im Ausgabepuffer empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="ff430-126">Receives the actual amount of raw value data received in the output buffer.</span></span>

<span data-ttu-id="ff430-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="ff430-127">*grbit*</span></span>

<span data-ttu-id="ff430-128">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="ff430-128">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff430-129">Wert</span><span class="sxs-lookup"><span data-stu-id="ff430-129">Value</span></span></p></th>
<th><p><span data-ttu-id="ff430-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ff430-130">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff430-131">JET_bitEscrowNoRollback</span><span class="sxs-lookup"><span data-stu-id="ff430-131">JET_bitEscrowNoRollback</span></span></p></td>
<td><p><span data-ttu-id="ff430-132">Auch wenn für die Sitzung, die das hinterlegter-Update ausführt, ein Rollback der Transaktion ausgeführt wird, wird dieses Update nicht rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="ff430-132">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="ff430-133">Beachten Sie, dass die Protokolldaten Sätze möglicherweise nicht auf den Datenträger geleert werden, wenn ein Absturz vorliegt.</span><span class="sxs-lookup"><span data-stu-id="ff430-133">Note that as the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ff430-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff430-134">Return Value</span></span>

<span data-ttu-id="ff430-135">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="ff430-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ff430-136">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ff430-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff430-137">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ff430-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="ff430-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff430-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff430-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ff430-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ff430-140">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ff430-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-141">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="ff430-141">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="ff430-142">Der Cursor verfügt über ein Update, das mit <a href="gg269339(v=exchg.10).md">jetprepareupdate</a>vorbereitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ff430-142">The cursor has an update prepared with <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ff430-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ff430-144">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="ff430-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-145">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ff430-145">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ff430-146">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="ff430-146">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="ff430-147">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ff430-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-148">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="ff430-148">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="ff430-149">Es wurde eine ungültige Puffergröße übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ff430-149">An invalid buffer size has been passed in.</span></span> <span data-ttu-id="ff430-150">Derzeit wird nur JET_coltypLong unterstützt, daher muss der Puffer 4 Bytes groß sein.</span><span class="sxs-lookup"><span data-stu-id="ff430-150">Currently only JET_coltypLong is supported, so the buffer must be 4 bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="ff430-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="ff430-152">Es wurde eine ungültige Spalte angegeben.</span><span class="sxs-lookup"><span data-stu-id="ff430-152">An invalid column has been specified.</span></span> <span data-ttu-id="ff430-153">Die Spalte muss mit JET_bitColumnEscrowUpdate angegebenen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ff430-153">The column must be created with JET_bitColumnEscrowUpdate specified.</span></span> <span data-ttu-id="ff430-154">Nur festgelegte Spalten von JET_coltypLong können als zu aktualisierbare Hinterlegungs Möglichkeiten angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ff430-154">Only fixed columns of JET_coltypLong can be specified as escrow updateable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="ff430-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="ff430-156">Der Cursor muss sich in einem Datensatz befinden, um eine Spalte zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ff430-156">Cursor must be on a record in order to update a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-157">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="ff430-157">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="ff430-158">Hinterlegte Updates können nur von Sitzungen in einer Transaktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ff430-158">Escrow updates can only be performed by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ff430-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ff430-160">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ff430-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-161">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="ff430-161">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="ff430-162">Der Cursor kann nicht schreibgeschützt sein und einen Datensatz aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ff430-162">Cursor cannot be read only and update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-163">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ff430-163">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ff430-164">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff430-164">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-165">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="ff430-165">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="ff430-166">Dieselbe Sitzung kann nicht gleichzeitig von mehreren Threads verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff430-166">The same session cannot be used from more than one thread at the same time.</span></span> <span data-ttu-id="ff430-167">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ff430-167">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-168">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ff430-168">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ff430-169">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="ff430-169">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-170">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="ff430-170">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="ff430-171">Die Sitzung muss über Schreibberechtigungen zum Aktualisieren eines Datensatzes verfügen.</span><span class="sxs-lookup"><span data-stu-id="ff430-171">Session must have write permissions to update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-172">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="ff430-172">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="ff430-173">Der zurückgegebene Fehler, wenn ein in Konflikt stehender Update angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="ff430-173">The error returned when a conflicting update is requested.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="ff430-174">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff430-174">Remarks</span></span>

<span data-ttu-id="ff430-175">Wenn zwei Sitzungen versuchen, einen Datensatz gleichzeitig zu aktualisieren, empfängt die zweite Sitzung normalerweise einen JET_errWriteConflict Fehler, es sei denn, die Sitzungen werden vollständig serialisiert.</span><span class="sxs-lookup"><span data-stu-id="ff430-175">Normally, if two sessions attempt to update a record simultaneously, the second session will receive a JET_errWriteConflict error unless the sessions are completely serialized.</span></span> <span data-ttu-id="ff430-176">Zum Serialisieren von zwei Sitzungen, die denselben Datensatz aktualisieren, muss die zweite Sitzung die Transaktion starten, nachdem die erste Transaktion einen Commit für die Transaktion ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="ff430-176">To serialize two sessions that update the same record, the second session must start its transaction after the first transaction commits its transaction.</span></span> <span data-ttu-id="ff430-177">Weitere Informationen finden Sie unter [jetbegintransaction](./jetbegintransaction-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ff430-177">See [JetBeginTransaction](./jetbegintransaction-function.md) for more information.</span></span>

<span data-ttu-id="ff430-178">Mehrere Spalten im gleichen Datensatz können mit einem Hinterlegungs Wert aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ff430-178">Multiple columns in the same record can be escrow updated.</span></span> <span data-ttu-id="ff430-179">Die Updates wirken sich nicht gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="ff430-179">The updates do not affect each other.</span></span>

<span data-ttu-id="ff430-180">Nur **jetescrowupdate** -Vorgänge sind miteinander kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ff430-180">Only **JetEscrowUpdate** operations are compatible with each other.</span></span> <span data-ttu-id="ff430-181">Wenn zwei verschiedene Sitzungen versuchen, Updates vorzubereiten oder denselben Datensatz zu löschen, wird ein Schreib Konflikt generiert.</span><span class="sxs-lookup"><span data-stu-id="ff430-181">If two different sessions try to prepare updates or delete the same record, a write conflict will be generated.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p></p></th>
<th><p><span data-ttu-id="ff430-182">Sitzung B</span><span class="sxs-lookup"><span data-stu-id="ff430-182">Session B</span></span><br /><span data-ttu-id="ff430-183">
<strong>Jetescrowupdate</strong></span><span class="sxs-lookup"><span data-stu-id="ff430-183">
<strong>JetEscrowUpdate</strong></span></span></p></th>
<th><p><span data-ttu-id="ff430-184"><a href="gg269339(v=exchg.10).md">Jetprepareupdate</a></span><span class="sxs-lookup"><span data-stu-id="ff430-184"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></span></span></p></th>
<th><p><span data-ttu-id="ff430-185"><a href="gg269315(v=exchg.10).md">Jetdelete</a></span><span class="sxs-lookup"><span data-stu-id="ff430-185"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ff430-186"><strong>Jetescrowupdate</strong></span><span class="sxs-lookup"><span data-stu-id="ff430-186"><strong>JetEscrowUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="ff430-187">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ff430-187">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ff430-188">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="ff430-188">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="ff430-189">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="ff430-189">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="ff430-190"><a href="gg269288(v=exchg.10).md">Jetupdate</a></span><span class="sxs-lookup"><span data-stu-id="ff430-190"><a href="gg269288(v=exchg.10).md">JetUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="ff430-191">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="ff430-191">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="ff430-192">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="ff430-192">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="ff430-193">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="ff430-193">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-194">Sitzung A</span><span class="sxs-lookup"><span data-stu-id="ff430-194">Session A</span></span></p></td>
<td><p><span data-ttu-id="ff430-195"><a href="gg269315(v=exchg.10).md">Jetdelete</a></span><span class="sxs-lookup"><span data-stu-id="ff430-195"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></td>
<td><p><span data-ttu-id="ff430-196">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="ff430-196">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="ff430-197">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="ff430-197">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="ff430-198">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="ff430-198">JET_errWriteConflict</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ff430-199">Hinterlegte Vorgänge werden mit einer Versions Angabe versehen und mit [jetrollback Rück](./jetrollback-function.md) gängig gemacht (es sei denn, JET_bitEscrowNoRollback wurde angegeben).</span><span class="sxs-lookup"><span data-stu-id="ff430-199">Escrow operations are versioned and are undone using [JetRollback](./jetrollback-function.md) (unless JET_bitEscrowNoRollback was specified).</span></span> <span data-ttu-id="ff430-200">**Jetescrowupdate** gibt den Rohwert der in der Datenbank gespeicherten Spalte zurück, weil eine Anwendung möglicherweise eine spezielle Aktion ausführt, wenn ein Sentinelwert getroffen wird.</span><span class="sxs-lookup"><span data-stu-id="ff430-200">**JetEscrowUpdate** returns the raw value of the column stored in the database, because an application may want to perform a special action when a sentinel value is hit.</span></span> <span data-ttu-id="ff430-201">[Jetretrievecolumn](./jetretrievecolumn-function.md) gibt die korrekt versionierte Sicht der Spalte zurück, wobei Updates von gleichzeitigen Sitzungen ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="ff430-201">[JetRetrieveColumn](./jetretrievecolumn-function.md) returns the correctly versioned view of the column, ignoring updates made by concurrent sessions.</span></span>

<span data-ttu-id="ff430-202">Wenn zwei Sitzungen in derselben Spalte desselben Datensatzes ausgeführt werden, können wir sehen, wie dies funktioniert.</span><span class="sxs-lookup"><span data-stu-id="ff430-202">Given two sessions operating on the same column of the same record, we can see how this works.</span></span> <span data-ttu-id="ff430-203">Angenommen, die Spalte beginnt mit einem Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="ff430-203">Assume the column starts with a value of 0.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff430-204">Sitzung</span><span class="sxs-lookup"><span data-stu-id="ff430-204">Session</span></span></p></th>
<th><p><span data-ttu-id="ff430-205">Vorgang</span><span class="sxs-lookup"><span data-stu-id="ff430-205">Operation</span></span></p></th>
<th><p><span data-ttu-id="ff430-206">Gespeicherter Wert</span><span class="sxs-lookup"><span data-stu-id="ff430-206">Stored value</span></span></p></th>
<th><p><span data-ttu-id="ff430-207">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff430-207">Returned value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff430-208">A</span><span class="sxs-lookup"><span data-stu-id="ff430-208">A</span></span></p></td>
<td><p><span data-ttu-id="ff430-209"><a href="gg294083(v=exchg.10).md">Jetbegintransations</a></span><span class="sxs-lookup"><span data-stu-id="ff430-209"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-210">A</span><span class="sxs-lookup"><span data-stu-id="ff430-210">A</span></span></p></td>
<td><p><span data-ttu-id="ff430-211"><a href="gg294083(v=exchg.10).md">Jetbegintransations</a></span><span class="sxs-lookup"><span data-stu-id="ff430-211"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ff430-212">0</span><span class="sxs-lookup"><span data-stu-id="ff430-212">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-213">A</span><span class="sxs-lookup"><span data-stu-id="ff430-213">A</span></span></p></td>
<td><p><span data-ttu-id="ff430-214"><strong>Jetescrowupdate</strong> (4)</span><span class="sxs-lookup"><span data-stu-id="ff430-214"><strong>JetEscrowUpdate</strong> (4)</span></span></p></td>
<td><p><span data-ttu-id="ff430-215">4</span><span class="sxs-lookup"><span data-stu-id="ff430-215">4</span></span></p></td>
<td><p><span data-ttu-id="ff430-216">0</span><span class="sxs-lookup"><span data-stu-id="ff430-216">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-217">A</span><span class="sxs-lookup"><span data-stu-id="ff430-217">A</span></span></p></td>
<td><p><span data-ttu-id="ff430-218"><a href="gg269198(v=exchg.10).md">Jetretrievecolumschlag</a></span><span class="sxs-lookup"><span data-stu-id="ff430-218"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ff430-219">4</span><span class="sxs-lookup"><span data-stu-id="ff430-219">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-220">B</span><span class="sxs-lookup"><span data-stu-id="ff430-220">B</span></span></p></td>
<td><p><span data-ttu-id="ff430-221"><a href="gg294083(v=exchg.10).md">Jetbegintransaction</a></span><span class="sxs-lookup"><span data-stu-id="ff430-221"><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-222">B</span><span class="sxs-lookup"><span data-stu-id="ff430-222">B</span></span></p></td>
<td><p><span data-ttu-id="ff430-223"><a href="gg269198(v=exchg.10).md">Jetretrievecolumschlag</a></span><span class="sxs-lookup"><span data-stu-id="ff430-223"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ff430-224">0</span><span class="sxs-lookup"><span data-stu-id="ff430-224">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-225">B</span><span class="sxs-lookup"><span data-stu-id="ff430-225">B</span></span></p></td>
<td><p><span data-ttu-id="ff430-226"><strong>Jetescrowupdate</strong> (3)</span><span class="sxs-lookup"><span data-stu-id="ff430-226"><strong>JetEscrowUpdate</strong> (3)</span></span></p></td>
<td><p><span data-ttu-id="ff430-227">7</span><span class="sxs-lookup"><span data-stu-id="ff430-227">7</span></span></p></td>
<td><p><span data-ttu-id="ff430-228">4</span><span class="sxs-lookup"><span data-stu-id="ff430-228">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-229">B</span><span class="sxs-lookup"><span data-stu-id="ff430-229">B</span></span></p></td>
<td><p><span data-ttu-id="ff430-230"><a href="gg269198(v=exchg.10).md">Jetretrievecolumschlag</a></span><span class="sxs-lookup"><span data-stu-id="ff430-230"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ff430-231">3</span><span class="sxs-lookup"><span data-stu-id="ff430-231">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-232">A</span><span class="sxs-lookup"><span data-stu-id="ff430-232">A</span></span></p></td>
<td><p><span data-ttu-id="ff430-233"><strong>Jetescrowupdate</strong> (2)</span><span class="sxs-lookup"><span data-stu-id="ff430-233"><strong>JetEscrowUpdate</strong> (2)</span></span></p></td>
<td><p><span data-ttu-id="ff430-234">9</span><span class="sxs-lookup"><span data-stu-id="ff430-234">9</span></span></p></td>
<td><p><span data-ttu-id="ff430-235">7</span><span class="sxs-lookup"><span data-stu-id="ff430-235">7</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-236">A</span><span class="sxs-lookup"><span data-stu-id="ff430-236">A</span></span></p></td>
<td><p><span data-ttu-id="ff430-237"><strong>Jetescrowupdate</strong> (-7)</span><span class="sxs-lookup"><span data-stu-id="ff430-237"><strong>JetEscrowUpdate</strong> (-7)</span></span></p></td>
<td><p><span data-ttu-id="ff430-238">2</span><span class="sxs-lookup"><span data-stu-id="ff430-238">2</span></span></p></td>
<td><p><span data-ttu-id="ff430-239">9</span><span class="sxs-lookup"><span data-stu-id="ff430-239">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-240">B</span><span class="sxs-lookup"><span data-stu-id="ff430-240">B</span></span></p></td>
<td><p><span data-ttu-id="ff430-241"><a href="gg269198(v=exchg.10).md">Jetretrievecolumschlag</a></span><span class="sxs-lookup"><span data-stu-id="ff430-241"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ff430-242">3</span><span class="sxs-lookup"><span data-stu-id="ff430-242">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-243">A</span><span class="sxs-lookup"><span data-stu-id="ff430-243">A</span></span></p></td>
<td><p><span data-ttu-id="ff430-244"><a href="gg269198(v=exchg.10).md">Jetretrievecolumschlag</a></span><span class="sxs-lookup"><span data-stu-id="ff430-244"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ff430-245">-1</span><span class="sxs-lookup"><span data-stu-id="ff430-245">-1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-246">B</span><span class="sxs-lookup"><span data-stu-id="ff430-246">B</span></span></p></td>
<td><p><span data-ttu-id="ff430-247"><a href="gg269273(v=exchg.10).md">Jetrollback</a></span><span class="sxs-lookup"><span data-stu-id="ff430-247"><a href="gg269273(v=exchg.10).md">JetRollback</a></span></span></p></td>
<td><p><span data-ttu-id="ff430-248">-1</span><span class="sxs-lookup"><span data-stu-id="ff430-248">-1</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-249">A</span><span class="sxs-lookup"><span data-stu-id="ff430-249">A</span></span></p></td>
<td><p><span data-ttu-id="ff430-250"><a href="gg269198(v=exchg.10).md">Jetretrievecolumschlag</a></span><span class="sxs-lookup"><span data-stu-id="ff430-250"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ff430-251">-1</span><span class="sxs-lookup"><span data-stu-id="ff430-251">-1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ff430-252">Es wird nicht empfohlen, einen Datensatz in der gleichen Transaktion zu ersetzen, der Änderungen an einem Datensatz ausführt.</span><span class="sxs-lookup"><span data-stu-id="ff430-252">Replacing a record in the same transaction that performs escrow updates to a record is not recommended.</span></span> <span data-ttu-id="ff430-253">Insbesondere, wenn ein Update für einen Datensatz mit einem [JET_TABLEID](./jet-tableid.md) vorbereitet wird und ein anderer [JET_TABLEID](./jet-tableid.md) verwendet wird, um die Aktualisierung des Datensatzes zu übernehmen, geht der aktualisierte hinterlegter-Wert verloren, wenn [jetupdate](./jetupdate-function.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ff430-253">In particular, if an update on a record is prepared with one [JET_TABLEID](./jet-tableid.md) and a different [JET_TABLEID](./jet-tableid.md) is used to escrow update the record then the escrow updated will be lost when [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="ff430-254">Dies geschieht auch, wenn die hinterlegte Spalte während des Updates nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ff430-254">This happens even if the escrow column was not set during the update.</span></span>

<span data-ttu-id="ff430-255">Wenn für eine aktualisierbare Hinterlegungs Spalte der Wert 0 (null) festgelegt ist, kann ein spezielles Verhalten ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="ff430-255">When an escrow updateable column has a value of zero, special behavior can be triggered.</span></span> <span data-ttu-id="ff430-256">Dieses Verhalten tritt nur auf, wenn ein **jetescrowupdate** -Vorgang bewirkt, dass die Spalte den Wert 0 (null) aufweist.</span><span class="sxs-lookup"><span data-stu-id="ff430-256">This behavior only happens if a **JetEscrowUpdate** operation causes the column to have a value of zero.</span></span> <span data-ttu-id="ff430-257">Die Aktion wird nicht sofort ausgeführt. Sie tritt jedoch irgendwann nach der Transaktion auf, die bewirkt hat, dass die Spalte einen Wert von 0 (null) hat.</span><span class="sxs-lookup"><span data-stu-id="ff430-257">The action does not happen immediately, but occurs sometime after the transaction which caused the column to have a value of zero commits.</span></span> <span data-ttu-id="ff430-258">Die Spalte muss weiterhin den Wert 0 (null) aufweisen (d. h., wenn keine anderen Sitzungen die Spalte geändert haben).</span><span class="sxs-lookup"><span data-stu-id="ff430-258">The column must still have a value of zero (that is, if no other sessions have modified the column).</span></span> <span data-ttu-id="ff430-259">Wenn die Spalte mit JET_bitColumnDeleteOnZero erstellt wurde, wird der Datensatz, der die Spalte enthält, gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ff430-259">If the column was created with JET_bitColumnDeleteOnZero, the record containing the column will be deleted.</span></span> <span data-ttu-id="ff430-260">Wenn die Spalte mit JET_bitColumnFinalize erstellt wurde, wird ein Rückruf ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="ff430-260">If the column was created with JET_bitColumnFinalize then a callback will be issued.</span></span> <span data-ttu-id="ff430-261">Ein Absturz kann dazu führen, dass diese Aktionen nicht ausgeführt werden, aber die Online Wartung (mithilfe der [jetdefragment](./jetdefragment-function.md) -Funktion) führt zu einer ordnungsgemäßen Wiederholung der Aktionen.</span><span class="sxs-lookup"><span data-stu-id="ff430-261">A crash may cause these actions not to happen, but online maintenance (using the [JetDefragment](./jetdefragment-function.md) function) will correctly redo the actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ff430-262">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff430-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff430-263"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ff430-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ff430-264">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ff430-264">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-265"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ff430-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ff430-266">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ff430-266">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-267"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ff430-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ff430-268">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="ff430-268">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff430-269"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="ff430-269"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ff430-270">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ff430-270">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff430-271"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ff430-271"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ff430-272">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ff430-272">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ff430-273">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ff430-273">See Also</span></span>

[<span data-ttu-id="ff430-274">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="ff430-274">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="ff430-275">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ff430-275">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ff430-276">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ff430-276">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ff430-277">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ff430-277">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ff430-278">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ff430-278">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ff430-279">Jetbegintransaction</span><span class="sxs-lookup"><span data-stu-id="ff430-279">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="ff430-280">Jetdebug</span><span class="sxs-lookup"><span data-stu-id="ff430-280">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="ff430-281">Jetprepareupdate</span><span class="sxs-lookup"><span data-stu-id="ff430-281">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="ff430-282">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="ff430-282">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="ff430-283">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="ff430-283">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="ff430-284">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="ff430-284">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="ff430-285">Jetupdate</span><span class="sxs-lookup"><span data-stu-id="ff430-285">JetUpdate</span></span>](./jetupdate-function.md)
