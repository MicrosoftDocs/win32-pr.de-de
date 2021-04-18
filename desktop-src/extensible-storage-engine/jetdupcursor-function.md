---
description: 'Weitere Informationen über: jetdupcursor-Funktion'
title: JetDupCursor-Funktion
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 590b9b08c5386aaf1cd2dd541ac496a5fa0871d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366148"
---
# <a name="jetdupcursor-function"></a><span data-ttu-id="0196b-103">JetDupCursor-Funktion</span><span class="sxs-lookup"><span data-stu-id="0196b-103">JetDupCursor Function</span></span>


<span data-ttu-id="0196b-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0196b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupcursor-function"></a><span data-ttu-id="0196b-105">JetDupCursor-Funktion</span><span class="sxs-lookup"><span data-stu-id="0196b-105">JetDupCursor Function</span></span>

<span data-ttu-id="0196b-106">Die **jetdupcursor** -Funktion dupliziert einen geöffneten Cursor und gibt ein Handle für den duplizierten Cursor zurück.</span><span class="sxs-lookup"><span data-stu-id="0196b-106">The **JetDupCursor** function duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="0196b-107">Wenn der duplizierte Cursor ein Schreib geschützter Cursor war, ist der duplizierte Cursor ebenfalls ein Schreib geschützter Cursor.</span><span class="sxs-lookup"><span data-stu-id="0196b-107">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="0196b-108">Jeder Status im Zusammenhang mit dem Erstellen eines Suchschlüssels oder dem Aktualisieren eines Datensatzes wird nicht in den doppelten Cursor kopiert.</span><span class="sxs-lookup"><span data-stu-id="0196b-108">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="0196b-109">Außerdem wird der Speicherort des ursprünglichen Cursors nicht in den doppelten Cursor dupliziert.</span><span class="sxs-lookup"><span data-stu-id="0196b-109">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="0196b-110">Der doppelte Cursor wird immer auf dem gruppierten Index geöffnet, und sein Speicherort ist immer in der ersten Zeile der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0196b-110">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="0196b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0196b-111">Parameters</span></span>

<span data-ttu-id="0196b-112">*-sid*</span><span class="sxs-lookup"><span data-stu-id="0196b-112">*sesid*</span></span>

<span data-ttu-id="0196b-113">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0196b-113">The session to use for this call.</span></span>

<span data-ttu-id="0196b-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="0196b-114">*tableid*</span></span>

<span data-ttu-id="0196b-115">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0196b-115">The cursor to use for this call.</span></span>

<span data-ttu-id="0196b-116">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="0196b-116">*ptableid*</span></span>

<span data-ttu-id="0196b-117">Zeiger auf *TableID*.</span><span class="sxs-lookup"><span data-stu-id="0196b-117">Pointer to *tableid*.</span></span>

<span data-ttu-id="0196b-118">*grbit*</span><span class="sxs-lookup"><span data-stu-id="0196b-118">*grbit*</span></span>

<span data-ttu-id="0196b-119">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="0196b-119">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="0196b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0196b-120">Return Value</span></span>

<span data-ttu-id="0196b-121">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="0196b-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0196b-122">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0196b-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0196b-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0196b-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="0196b-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0196b-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0196b-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0196b-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0196b-126">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0196b-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0196b-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="0196b-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="0196b-128">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="0196b-128">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0196b-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="0196b-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="0196b-130">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="0196b-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="0196b-131">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0196b-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0196b-132">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="0196b-132">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="0196b-133">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0196b-133">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0196b-134">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="0196b-134">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="0196b-135">Es sind keine verfügbaren Cursor Ressourcen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0196b-135">No available cursor resources exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0196b-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="0196b-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="0196b-137">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0196b-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0196b-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="0196b-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="0196b-139">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0196b-139">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="0196b-140">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0196b-140">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0196b-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="0196b-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="0196b-142">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="0196b-142">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0196b-143">Bei Erfolg wird *pTableID* auf einen doppelten Cursor festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0196b-143">On success, *ptableid* is set to a duplicated cursor.</span></span>

<span data-ttu-id="0196b-144">Bei einem Fehler werden keine Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="0196b-144">On failure, no changes are made.</span></span> <span data-ttu-id="0196b-145">Der Status von *TableID* ist unverändert.</span><span class="sxs-lookup"><span data-stu-id="0196b-145">The state of *tableid* is unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0196b-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0196b-146">Remarks</span></span>

<span data-ttu-id="0196b-147">Beim duplizierten Cursor ist nicht der gesamte Cursor Zustand kopiert.</span><span class="sxs-lookup"><span data-stu-id="0196b-147">The duplicated cursor does not have the entire cursor state copied.</span></span> <span data-ttu-id="0196b-148">Der Speicherort des duplizierten Cursors, einschließlich des aktuellen Indexes, unterscheidet sich in der Regel vom angegebenen Cursor.</span><span class="sxs-lookup"><span data-stu-id="0196b-148">The location of the duplicated cursor, including the current index, is usually different from the given cursor.</span></span> <span data-ttu-id="0196b-149">Der doppelte Cursor wird immer für den gruppierten Index und für die erste Zeile in der Tabelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0196b-149">The duplicated cursor is always returned on the clustered index and on the first row in the table.</span></span> <span data-ttu-id="0196b-150">Wenn die Tabelle leer ist, befindet sich der duplizierte Cursor nicht in einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="0196b-150">If the table is empty, the duplicated cursor is not on any row.</span></span>

<span data-ttu-id="0196b-151">Tabellen, die mit **jetdupcursor** geöffnet werden, sollten normalerweise mit [jetclosetable](./jetclosetable-function.md)geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="0196b-151">Tables opened with **JetDupCursor** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="0196b-152">Die Ausnahme von dieser Regel tritt auf, wenn **jetdupcursor** in einer Transaktion aufgerufen wird und für die Transaktion ein Rollback ausgeführt wird (mit [jetrollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="0196b-152">The exception to this rule happens when **JetDupCursor** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="0196b-153">Beim Rollback einer Transaktion wird der Cursor automatisch geschlossen.</span><span class="sxs-lookup"><span data-stu-id="0196b-153">When rolling back a transaction, the cursor is automatically closed.</span></span> <span data-ttu-id="0196b-154">In diesem Fall ist es ein Fehler, die Tabelle mit [jetclosetable](./jetclosetable-function.md)zu schließen.</span><span class="sxs-lookup"><span data-stu-id="0196b-154">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="0196b-155">Die Anzahl der Tabellen, die gleichzeitig geöffnet werden können, wird von [JET_paramMaxOpenTables](./resource-parameters.md)direkt beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="0196b-155">The number of tables that can be opened simultaneously is affected directly by [JET_paramMaxOpenTables](./resource-parameters.md).</span></span> <span data-ttu-id="0196b-156">Weitere Informationen finden Sie unter [System Parameter](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="0196b-156">See [System Parameters](./extensible-storage-engine-system-parameters.md) for details.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0196b-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0196b-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0196b-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0196b-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0196b-159">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0196b-159">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0196b-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0196b-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0196b-161">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0196b-161">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0196b-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0196b-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0196b-163">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="0196b-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0196b-164"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="0196b-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0196b-165">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0196b-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0196b-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0196b-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0196b-167">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0196b-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0196b-168">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0196b-168">See Also</span></span>

[<span data-ttu-id="0196b-169">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0196b-169">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0196b-170">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0196b-170">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0196b-171">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0196b-171">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0196b-172">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="0196b-172">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="0196b-173">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="0196b-173">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="0196b-174">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="0196b-174">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="0196b-175">System Parameter</span><span class="sxs-lookup"><span data-stu-id="0196b-175">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
