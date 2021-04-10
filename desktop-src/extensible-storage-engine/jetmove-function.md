---
description: 'Weitere Informationen: jetmove-Funktion'
title: JetMove-Funktion
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e42cb2258d373f8c4edb96309c6db0853eab4fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214383"
---
# <a name="jetmove-function"></a><span data-ttu-id="705fa-103">JetMove-Funktion</span><span class="sxs-lookup"><span data-stu-id="705fa-103">JetMove Function</span></span>


<span data-ttu-id="705fa-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="705fa-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetmove-function"></a><span data-ttu-id="705fa-105">JetMove-Funktion</span><span class="sxs-lookup"><span data-stu-id="705fa-105">JetMove Function</span></span>

<span data-ttu-id="705fa-106">Die **jetmove** -Funktion positioniert einen Cursor am Anfang oder Ende eines Indexes und durchläuft die Einträge in diesem Index entweder vorwärts oder rückwärts.</span><span class="sxs-lookup"><span data-stu-id="705fa-106">The **JetMove** function positions a cursor at the start or end of an index and traverses the entries in that index either forward or backward.</span></span> <span data-ttu-id="705fa-107">Es ist auch möglich, den Cursor auf dem aktuellen Index um eine angegebene Anzahl von Indexeinträgen vorwärts oder rückwärts zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="705fa-107">It is also possible to move the cursor forward or backward on the current index by a specified number of index entries.</span></span> <span data-ttu-id="705fa-108">Ein anderer Ansatz besteht darin, die Indexeinträge, die mithilfe von **jetmove** aufgezählt werden können, durch das Einrichten eines Index Bereichs auf dem Cursor mithilfe von [jetsetindexrange](./jetsetindexrange-function.md)künstlich einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="705fa-108">Another approach is to artificially limit the index entries that can be enumerated using **JetMove** by setting up an index range on the cursor using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="705fa-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="705fa-109">Parameters</span></span>

<span data-ttu-id="705fa-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="705fa-110">*sesid*</span></span>

<span data-ttu-id="705fa-111">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="705fa-111">The session to use for this call.</span></span>

<span data-ttu-id="705fa-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="705fa-112">*tableid*</span></span>

<span data-ttu-id="705fa-113">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="705fa-113">The cursor to use for this call.</span></span>

<span data-ttu-id="705fa-114">*beschäftigen*</span><span class="sxs-lookup"><span data-stu-id="705fa-114">*cRow*</span></span>

<span data-ttu-id="705fa-115">Ein beliebiger Offset, der die gewünschte Bewegung des Cursors des aktuellen Indexes angibt.</span><span class="sxs-lookup"><span data-stu-id="705fa-115">An arbitrary offset that indicates the desired movement of the cursor on the current index.</span></span>

<span data-ttu-id="705fa-116">Zusätzlich zu Standard Offsets kann dieser Parameter auch mit einer der folgenden Optionen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="705fa-116">In addition to standard offsets, this parameter can also be set with one of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="705fa-117">Wert</span><span class="sxs-lookup"><span data-stu-id="705fa-117">Value</span></span></p></th>
<th><p><span data-ttu-id="705fa-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="705fa-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="705fa-119">JET_MoveFirst</span><span class="sxs-lookup"><span data-stu-id="705fa-119">JET_MoveFirst</span></span></p></td>
<td><p><span data-ttu-id="705fa-120">Verschiebt den Cursor zum ersten Index Eintrag im Index (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="705fa-120">Moves the cursor to the first index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="705fa-121"><strong>Hinweis</strong>   Der Literalwert "-2147483648" wird verwendet, um diese Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="705fa-121"><strong>Note</strong>   The literal value of -2147483648 is used to denote this option.</span></span> <span data-ttu-id="705fa-122">Verwenden Sie diesen Wert nicht als normalen Offset oder unbeabsichtigtes Verhalten.</span><span class="sxs-lookup"><span data-stu-id="705fa-122">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705fa-123">JET_MoveLast</span><span class="sxs-lookup"><span data-stu-id="705fa-123">JET_MoveLast</span></span></p></td>
<td><p><span data-ttu-id="705fa-124">Verschiebt den Cursor auf den letzten Index Eintrag im Index (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="705fa-124">Moves the cursor to the last index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="705fa-125"><strong>Hinweis</strong>   Der Literalwert 2147483647 wird verwendet, um diese Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="705fa-125"><strong>Note</strong>   The literal value of 2147483647 is used to denote this option.</span></span> <span data-ttu-id="705fa-126">Verwenden Sie diesen Wert nicht als normalen Offset oder unbeabsichtigtes Verhalten.</span><span class="sxs-lookup"><span data-stu-id="705fa-126">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705fa-127">JET_MoveNext</span><span class="sxs-lookup"><span data-stu-id="705fa-127">JET_MoveNext</span></span></p></td>
<td><p><span data-ttu-id="705fa-128">Verschiebt den Cursor zum nächsten Index Eintrag im Index (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="705fa-128">Moves the cursor to the next index entry in the index (if one exists).</span></span> <span data-ttu-id="705fa-129">Dieser Wert ist genau gleich dem normalen Offset von + 1.</span><span class="sxs-lookup"><span data-stu-id="705fa-129">This value is exactly equal to an ordinary offset of +1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705fa-130">JET_MovePrevious</span><span class="sxs-lookup"><span data-stu-id="705fa-130">JET_MovePrevious</span></span></p></td>
<td><p><span data-ttu-id="705fa-131">Verschiebt den Cursor zum vorherigen Index Eintrag im Index (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="705fa-131">Moves the cursor to the previous index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="705fa-132">Dieser Wert ist genau gleich dem normalen Offset von-1 oder 0 (null).</span><span class="sxs-lookup"><span data-stu-id="705fa-132">This value is exactly equal to an ordinary offset of -1, or 0 (Zero).</span></span></p>
<p><span data-ttu-id="705fa-133">Der Cursor bleibt an der aktuellen logischen Position, und das vorhanden sein des Index Eintrags, der dieser logischen Position entspricht, wird getestet.</span><span class="sxs-lookup"><span data-stu-id="705fa-133">The cursor remains at the current logical position and the existence of the index entry that corresponds to that logical position will be tested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="705fa-134">*grbit*</span><span class="sxs-lookup"><span data-stu-id="705fa-134">*grbit*</span></span>

<span data-ttu-id="705fa-135">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angeben.</span><span class="sxs-lookup"><span data-stu-id="705fa-135">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="705fa-136">Wert</span><span class="sxs-lookup"><span data-stu-id="705fa-136">Value</span></span></p></th>
<th><p><span data-ttu-id="705fa-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="705fa-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="705fa-138">JET_bitMoveKeyNE</span><span class="sxs-lookup"><span data-stu-id="705fa-138">JET_bitMoveKeyNE</span></span></p></td>
<td><p><span data-ttu-id="705fa-139">Verschiebt den Cursor um die Anzahl der Indexeinträge, die erforderlich sind, um die angeforderte Anzahl von Index Schlüsselwerten im Index zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="705fa-139">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="705fa-140">Dies hat den Effekt, dass Indexeinträge mit doppelten Schlüsselwerten in einem einzelnen Index Eintrag reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="705fa-140">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span> <span data-ttu-id="705fa-141">Normalerweise verschiebt ein Offset den Cursor um die angegebene Anzahl von Indexeinträgen, unabhängig von den Schlüsselwerten.</span><span class="sxs-lookup"><span data-stu-id="705fa-141">Ordinarily, an offset will move the cursor by the specified number of index entries regardless of their key values.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="705fa-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="705fa-142">Return Value</span></span>

<span data-ttu-id="705fa-143">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="705fa-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="705fa-144">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="705fa-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="705fa-145">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="705fa-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="705fa-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="705fa-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="705fa-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="705fa-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="705fa-148">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="705fa-148">The operation completed successfully.</span></span> <span data-ttu-id="705fa-149">Für <strong>jetmove</strong>bedeutet dies, dass ein Index Eintrag am angeforderten Speicherort oder Offset des aktuellen Indexes gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="705fa-149">For <strong>JetMove</strong>, this means that an index entry was found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705fa-150">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="705fa-150">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="705fa-151">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="705fa-151">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705fa-152">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="705fa-152">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="705fa-153">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</span><span class="sxs-lookup"><span data-stu-id="705fa-153">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="705fa-154"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="705fa-154"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705fa-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="705fa-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="705fa-156">Der Cursor befindet sich derzeit nicht auf einem Index Eintrag.</span><span class="sxs-lookup"><span data-stu-id="705fa-156">The cursor is not currently positioned on an index entry.</span></span> <span data-ttu-id="705fa-157">Für <strong>jetmove</strong>bedeutet dies, dass am angeforderten Speicherort oder Offset des aktuellen Indexes kein Index Eintrag gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="705fa-157">For <strong>JetMove</strong>, this means that an index entry was not found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705fa-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="705fa-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="705fa-159">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="705fa-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705fa-160">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="705fa-160">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="705fa-161">Der Cursor ist zurzeit logisch auf einem Index Eintrag positioniert, der einem Datensatz entspricht, der gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="705fa-161">The cursor is currently logically positioned on an index entry that corresponds to a record that has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705fa-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="705fa-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="705fa-163">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="705fa-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705fa-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="705fa-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="705fa-165">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="705fa-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="705fa-166"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="705fa-166"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705fa-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="705fa-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="705fa-168">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="705fa-168">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="705fa-169">Wenn diese Funktion erfolgreich ausgeführt wird, wird der Cursor an einem Index Eintrag positioniert, der mit dem angeforderten Speicherort oder Offset übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="705fa-169">If this function succeeds, the cursor will be positioned at an index entry that matches the requested location or offset.</span></span> <span data-ttu-id="705fa-170">Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="705fa-170">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="705fa-171">Wenn ein Index Bereich wirksam ist und JET_MoveFirst oder JET_MoveLast angegeben wurde, wird dieser Index Bereich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="705fa-171">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="705fa-172">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="705fa-172">No change to the database state will occur.</span></span>

<span data-ttu-id="705fa-173">Wenn diese Funktion fehlschlägt, bleibt die Position des Cursors unverändert, es sei denn, JET_errNoCurrentRecord zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="705fa-173">If this function fails, the position of the cursor will remain unchanged unless JET_errNoCurrentRecord was returned.</span></span> <span data-ttu-id="705fa-174">In diesem Fall wird der Cursor positioniert, wo der Index Eintrag, der mit dem angeforderten Speicherort oder Offset übereinstimmt, wäre.</span><span class="sxs-lookup"><span data-stu-id="705fa-174">In that case, the cursor will be positioned where the index entry that matches the requested location or offset would have been.</span></span> <span data-ttu-id="705fa-175">Der Cursor kann relativ zu dieser Position verschoben werden, befindet sich jedoch noch nicht in einem gültigen Index Eintrag.</span><span class="sxs-lookup"><span data-stu-id="705fa-175">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="705fa-176">Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="705fa-176">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="705fa-177">Wenn ein Index Bereich wirksam ist und JET_MoveFirst oder JET_MoveLast angegeben wurde, wird dieser Index Bereich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="705fa-177">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="705fa-178">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="705fa-178">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="705fa-179">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="705fa-179">Remarks</span></span>

<span data-ttu-id="705fa-180">Ein Cursor kann mithilfe von **jetmove**, vor der ersten und nach der letzten, an zwei Sonderpositionen verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="705fa-180">A cursor can be moved to two special positions using **JetMove**, Before First and After Last.</span></span> <span data-ttu-id="705fa-181">Wenn sich der Cursor auf dem ersten Index Eintrag in der Tabelle befindet und **jetmove** mit JET_MovePrevious aufgerufen wird, schlägt der Aufruf mit JET_errNoCurrentRecord fehl, und der Cursor wird logisch vor dem ersten Eintrag im Index positioniert.</span><span class="sxs-lookup"><span data-stu-id="705fa-181">If the cursor is on the first index entry in the table and **JetMove** is called with JET_MovePrevious, the call will fail with JET_errNoCurrentRecord and the cursor will be logically positioned before the first entry in the index.</span></span> <span data-ttu-id="705fa-182">Diese logische Position wird auch dann beibehalten, wenn vor dem ersten Eintrag im Index ein anderer Index Eintrag eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="705fa-182">This logical position is maintained even if another index entry is inserted prior to the first entry in the index.</span></span> <span data-ttu-id="705fa-183">Eine analoge Situation tritt für den letzten relativ zum Ende des Indexes ein.</span><span class="sxs-lookup"><span data-stu-id="705fa-183">An analogous situation occurs for After Last relative to the end of the index.</span></span> <span data-ttu-id="705fa-184">Vor der ersten und nach der letzten sind besonders nützlich, wenn Sie einen Bereich von Indexeinträgen einrichten, die mithilfe von **jetmove** durchlaufen werden sollen. dabei wird ein iteratormodell verwendet, das erwartet, dass immer zum nächsten (oder vorherigen) Element wechselt, bevor dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="705fa-184">Before First and After Last are most useful when setting up a range of index entries to be iterated using **JetMove**, using an iterator model that expects to always move to the next (or previous) element prior to using that element.</span></span>

<span data-ttu-id="705fa-185">Der Satz von Indexeinträgen, der von **jetmove** besucht werden kann, kann durch das Einrichten eines Index Bereichs auf dem Cursor eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="705fa-185">The set of index entries that can be visited by **JetMove** can be limited by setting up an index range on the cursor.</span></span> <span data-ttu-id="705fa-186">Dies ist nützlich für Anwendungen, die einen Satz von Indexeinträgen auflisten, die einfache Kriterien erfüllen, die über ein paar von Suchschlüsseln ausgedrückt werden können, die für diesen Index erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="705fa-186">This is useful for applications that enumerate a set of index entries that match simple criteria that can be expressed through a pair of search keys built for that index.</span></span> <span data-ttu-id="705fa-187">Weitere Informationen finden Sie unter [jetsetindexrange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="705fa-187">For more information, see [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="705fa-188">In Releases vor Windows Server 2003 SP1 liegt ein Problem in **jetmove** vor, das in einigen bestimmten Fällen auftritt, das sich auf die korrekte Durchsetzung eines Index Bereichs auswirkt, wie von der [jetsetindexrange](./jetsetindexrange-function.md) -Funktion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="705fa-188">On releases prior to Windows Server 2003 SP1, there is a problem in **JetMove** that occurs in some specific cases, that affects the correct enforcement of an index range as set up by the [JetSetIndexRange](./jetsetindexrange-function.md) function.</span></span> <span data-ttu-id="705fa-189">Wenn sich der Cursor derzeit vor dem ersten Index Eintrag befindet und ein Index Bereich mit einer Obergrenze festgelegt ist, die kleiner als der erste Index Eintrag ist, wird der nächste **jetmove** -Befehl fälschlicherweise zu diesem Index Eintrag gewechselt, anstatt wie erwartet mit JET_errNoCurrentRecord.</span><span class="sxs-lookup"><span data-stu-id="705fa-189">If the cursor is currently before the first index entry and an index range is set with an upper limit that is less than the first index entry, the next call to **JetMove** will erroneously go to that index entry instead of failing with JET_errNoCurrentRecord, as expected.</span></span> <span data-ttu-id="705fa-190">Der gleiche Fehler tritt für die analoge Situation auf, beginnend ab dem Index Ende.</span><span class="sxs-lookup"><span data-stu-id="705fa-190">The same error will happen for the analogous situation starting from the end of the index.</span></span> <span data-ttu-id="705fa-191">Diese Situation kann in einer Anwendung auftreten, die einen Index Bereich einrichtet und mithilfe eines Iterators navigiert, der erwartet, dass vor dem ersten Index Eintrag begonnen wird, der ein Member der aufzuzählenden Menge von Einträgen ist, anstatt mit dem ersten Index Eintrag dieses Satzes zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="705fa-191">This situation can occur in an application that sets up an index range and navigates it using an iterator that expects to start before the first index entry that is a member of the set of entries to enumerate, rather than starting on the first index entry of that set.</span></span> <span data-ttu-id="705fa-192">Diese Situation tritt auch in dem analogen Fall auf, beginnend ab dem Ende des Indexes.</span><span class="sxs-lookup"><span data-stu-id="705fa-192">This situation also occurs on the analogous case starting from the end of the index.</span></span> <span data-ttu-id="705fa-193">Die Problem Umgehung besteht darin, dass die Anwendung manuell prüft, ob sich der erfassten Index Eintrag innerhalb des Index Bereichs befindet, indem der Schlüssel für den aktuellen Index Eintrag (abgerufen mit [jetretrievekey](./jetretrievekey-function.md)) mit dem Schlüssel verglichen wird, der das Ende des aktuellen Index Bereichs darstellt (abgerufen mit [jetretrievekey](./jetretrievekey-function.md) mithilfe JET_bitRetrieveCopy).</span><span class="sxs-lookup"><span data-stu-id="705fa-193">The workaround is for the application to manually verify that the index entry acquired is inside the index range by comparing the key for the current index entry (retrieved using [JetRetrieveKey](./jetretrievekey-function.md)) with the key representing the end of the current index range (retrieved using [JetRetrieveKey](./jetretrievekey-function.md) using JET_bitRetrieveCopy).</span></span>

<span data-ttu-id="705fa-194">Es ist wichtig, bei der Übergabe berechneter Offsets an **jetmove** vorsichtig zu sein.</span><span class="sxs-lookup"><span data-stu-id="705fa-194">It is important to be careful when passing computed offsets to **JetMove**.</span></span> <span data-ttu-id="705fa-195">Wenn der berechnete Offset kleiner als oder gleich JET_MoveFirst ist, muss dieser Offset in mehrere Teile aufgeteilt werden, von denen jeder separat an **jetmove** übermittelt wird, aber innerhalb einer einzelnen Transaktion, um den gewünschten Effekt zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="705fa-195">If the computed offset is less than or equal to JET_MoveFirst, that offset must be broken up into multiple pieces, each of which is passed to **JetMove** separately but within a single transaction to get the desired effect.</span></span> <span data-ttu-id="705fa-196">Das gleiche gilt für Offsets, die größer oder gleich JET_MoveNext sind.</span><span class="sxs-lookup"><span data-stu-id="705fa-196">The same is true for offsets greater than or equal to JET_MoveNext.</span></span> <span data-ttu-id="705fa-197">Es ist unwahrscheinlich, dass eine Anwendung diese in der realen Welt durchlaufen würde, aber es ist gut, bei der unterschiedlichen Semantik von JET_MoveFirst und JET_MoveLast von einem normalen Offset eine Verteidigung gegen diesen Fall zu haben.</span><span class="sxs-lookup"><span data-stu-id="705fa-197">It is unlikely that an application would undergo this in the real world, but it is good to have a defense against this case given the very different semantics of JET_MoveFirst and JET_MoveLast from an ordinary offset.</span></span>

<span data-ttu-id="705fa-198">Wenn **jetmove** mit einem sehr großen Offset aufgerufen wird, z. b. wenn der Parameter "cRow" auf 1000 festgelegt ist, durchläuft **jetmove** alle 1000-Indexeinträge, um die endgültige Position zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="705fa-198">When **JetMove** is called with a very large offset, such as when the cRow parameter is set to 1000, **JetMove** traverses all 1000 index entries to reach the final position.</span></span> <span data-ttu-id="705fa-199">Derzeit bietet die ESE-API keine effiziente Möglichkeit, direkt zu einem bestimmten Index Eintrag zu wechseln, ohne jeden Index Eintrag durchlaufen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="705fa-199">Currently, the ESE API does not provide an efficient way to move directly to a given index entry by offset without traversing each index entry.</span></span>

#### <a name="requirements"></a><span data-ttu-id="705fa-200">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="705fa-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="705fa-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="705fa-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="705fa-202">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="705fa-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705fa-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="705fa-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="705fa-204">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="705fa-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705fa-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="705fa-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="705fa-206">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="705fa-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="705fa-207"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="705fa-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="705fa-208">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="705fa-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="705fa-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="705fa-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="705fa-210">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="705fa-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="705fa-211">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="705fa-211">See Also</span></span>

[<span data-ttu-id="705fa-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="705fa-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="705fa-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="705fa-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="705fa-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="705fa-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="705fa-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="705fa-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="705fa-216">Jetretrievekey</span><span class="sxs-lookup"><span data-stu-id="705fa-216">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="705fa-217">Jetsetindexrange</span><span class="sxs-lookup"><span data-stu-id="705fa-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
