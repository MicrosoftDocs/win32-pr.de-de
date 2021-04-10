---
description: 'Weitere Informationen zu: jetsetindexrange-Funktion'
title: JetSetIndexRange-Funktion
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 883085633bebf25180c82f0f8917f6fa31fe7304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214755"
---
# <a name="jetsetindexrange-function"></a><span data-ttu-id="cfcf0-103">JetSetIndexRange-Funktion</span><span class="sxs-lookup"><span data-stu-id="cfcf0-103">JetSetIndexRange Function</span></span>


<span data-ttu-id="cfcf0-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cfcf0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetindexrange-function"></a><span data-ttu-id="cfcf0-105">JetSetIndexRange-Funktion</span><span class="sxs-lookup"><span data-stu-id="cfcf0-105">JetSetIndexRange Function</span></span>

<span data-ttu-id="cfcf0-106">Die **jetsetindexrange** -Funktion schränkt vorübergehend den Satz von Indexeinträgen ein, den der Cursor mithilfe von [jetmove](./jetmove-function.md) durchlaufen kann, beginnend mit dem aktuellen Index Eintrag und endet mit dem Index Eintrag, der mit den Suchkriterien übereinstimmt, die durch den Suchschlüssel in diesem Cursor und den angegebenen gebundenen Kriterien festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-106">The **JetSetIndexRange** function temporarily limits the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="cfcf0-107">Ein Suchschlüssel muss zuvor mithilfe von [jetmakekey](./jetmakekey-function.md)erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="cfcf0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfcf0-108">Parameters</span></span>

<span data-ttu-id="cfcf0-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="cfcf0-109">*sesid*</span></span>

<span data-ttu-id="cfcf0-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-110">The session to use for this call.</span></span>

<span data-ttu-id="cfcf0-111">*tableidsrc*</span><span class="sxs-lookup"><span data-stu-id="cfcf0-111">*tableidSrc*</span></span>

<span data-ttu-id="cfcf0-112">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-112">The cursor to use for this call.</span></span>

<span data-ttu-id="cfcf0-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="cfcf0-113">*grbit*</span></span>

<span data-ttu-id="cfcf0-114">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="cfcf0-114">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cfcf0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="cfcf0-115">Value</span></span></p></th>
<th><p><span data-ttu-id="cfcf0-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cfcf0-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfcf0-117">JET_bitRangeInclusive</span><span class="sxs-lookup"><span data-stu-id="cfcf0-117">JET_bitRangeInclusive</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-118">Diese Option gibt die Begrenzungs Kriterien des Index Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-118">This presence or absence of this option indicates the boundary criteria of the index range.</span></span> <span data-ttu-id="cfcf0-119">Wenn diese Option vorhanden ist, gibt diese Option an, dass die Beschränkung des Index Bereichs inklusiv ist.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-119">When present, this option indicates that the limit of the index range is inclusive.</span></span> <span data-ttu-id="cfcf0-120">Wenn diese Option nicht vorhanden ist, gibt diese Option an, dass die Beschränkung des Index Bereichs exklusiv ist.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-120">When absent, this option indicates that the limit of the index range is exclusive.</span></span> <span data-ttu-id="cfcf0-121">Wenn das Limit des Index Bereichs inklusiv ist, werden alle Indexeinträge, die genau mit den Suchkriterien übereinstimmen, in den Bereich eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-121">When the limit of the index range is inclusive then any index entries exactly matching the search criteria are included in the range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfcf0-122">JET_bitRangeInstantDuration</span><span class="sxs-lookup"><span data-stu-id="cfcf0-122">JET_bitRangeInstantDuration</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-123">Mit dieser Option wird angefordert, dass der Index Bereich entfernt wird, sobald er erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-123">This option requests that the index range be removed as soon as it has been established.</span></span> <span data-ttu-id="cfcf0-124">Alle anderen Aspekte des Vorgangs bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-124">All other aspects of the operation remain unchanged.</span></span> <span data-ttu-id="cfcf0-125">Dies ist hilfreich, um zu testen, ob Indexeinträge vorhanden sind, die mit den Suchkriterien übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-125">This is useful for testing for the existence of index entries that match the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfcf0-126">JET_bitRangeRemove</span><span class="sxs-lookup"><span data-stu-id="cfcf0-126">JET_bitRangeRemove</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-127">Mit dieser Option wird angefordert, dass ein vorhandener Index Bereich im Cursor abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-127">This option requests that an existing index range on the cursor be canceled.</span></span> <span data-ttu-id="cfcf0-128">Nachdem der Index Bereich abgebrochen wurde, kann er über das Ende des Index Bereichs mithilfe von <a href="gg294117(v=exchg.10).md">jetmove</a>verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-128">Once the index range is canceled, it will be possible to move beyond the end of the index range using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span> <span data-ttu-id="cfcf0-129">Wenn ein Index Bereich nicht bereits in Kraft ist, schlägt <strong>jetsetindexrange</strong> mit JET_errInvalidOperation fehl.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-129">If an index range is not already in effect, then <strong>JetSetIndexRange</strong> will fail with JET_errInvalidOperation.</span></span></p>
<p><span data-ttu-id="cfcf0-130">Wenn diese Option angegeben wird, werden alle anderen Optionen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-130">When this option is specified, all other options are ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfcf0-131">JET_bitRangeUpperLimit</span><span class="sxs-lookup"><span data-stu-id="cfcf0-131">JET_bitRangeUpperLimit</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-132">Wenn diese Option verwendet wird, stellt der Suchschlüssel im Cursor die Suchkriterien für den Index Eintrag dar, der am Ende des Indexes liegt, der mit dem Index Bereich übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-132">If this option is used, then the search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span> <span data-ttu-id="cfcf0-133">Der Index Bereich wird zwischen der aktuellen Position des Cursors und diesem Index Eintrag festgelegt, sodass alle Übereinstimmungen gefunden werden können, indem Sie den Index mithilfe von <a href="gg294117(v=exchg.10).md">jetmove</a> mit JET_MoveNext oder einem positiven Offset durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-133">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking forward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MoveNext or a positive offset.</span></span></p>
<p><span data-ttu-id="cfcf0-134">Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde, indem eine Platzhalter Option verwendet wurde, um Indexeinträge zu suchen, die dem Anfang des Indexes am nächsten liegen.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-134">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p>
<p><span data-ttu-id="cfcf0-135">Wenn diese Option weggelassen wird, stellt der Suchschlüssel im Cursor die Suchkriterien für den Index Eintrag dar, der am Anfang des Indexes liegt, der mit dem Index Bereich übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-135">If this option is omitted, then the search key in the cursor represents the search criteria for the index entry closest to the start of the index that will match the index range.</span></span> <span data-ttu-id="cfcf0-136">Der Index Bereich wird zwischen der aktuellen Position des Cursors und diesem Index Eintrag festgelegt, sodass alle Übereinstimmungen gefunden werden können, indem Sie mithilfe von <a href="gg294117(v=exchg.10).md">jetmove</a> mit JET_MovePrevious oder einem negativen Offset auf den Index zurückgehen.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-136">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking backward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MovePrevious or a negative offset.</span></span></p>
<p><span data-ttu-id="cfcf0-137">Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel auszulassen, der mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde, indem eine Platzhalter Option verwendet wurde, um Indexeinträge zu suchen, die dem Ende des Indexes am nächsten sind.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-137">It is not meaningful to omit this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="cfcf0-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfcf0-138">Return Value</span></span>

<span data-ttu-id="cfcf0-139">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cfcf0-140">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cfcf0-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cfcf0-141">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cfcf0-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="cfcf0-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cfcf0-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfcf0-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cfcf0-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-144">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-144">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="cfcf0-145">Für <strong>jetsetindexrange</strong>bedeutet dies, dass entweder ein vorhandener Index Bereich abgebrochen wurde oder dass mindestens ein Index Eintrag innerhalb des Index Bereichs vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-145">For <strong>JetSetIndexRange</strong>, this means that either an existing index range was canceled or that there is at least one index entry inside of the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfcf0-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="cfcf0-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-147">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfcf0-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="cfcf0-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-149">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="cfcf0-150">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfcf0-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="cfcf0-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-152">Dieser Fehler wird von <strong>jetsetindexrange</strong> zurückgegeben, wenn JET_bitRangeRemove angegeben wurde und kein Index Bereich in Kraft war.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-152">This error will be returned by <strong>JetSetIndexRange</strong> when JET_bitRangeRemove was specified and no index range was in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfcf0-153">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="cfcf0-153">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-154">Es ist kein aktueller Suchschlüssel für den Cursor vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-154">There is no current search key for the cursor.</span></span> <span data-ttu-id="cfcf0-155"><strong>Jetsetindexrange</strong> erfordert, dass der Cursor über einen gültigen Suchschlüssel verfügt, da er diesen für die Suchkriterien verwendet, die zum Suchen von Indexeinträgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-155"><strong>JetSetIndexRange</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfcf0-156">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="cfcf0-156">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-157">Es ist kein aktueller Index für den Cursor vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-157">There is no current index for the cursor.</span></span> <span data-ttu-id="cfcf0-158">Dies geschieht für <strong>jetsetindexrange</strong> , wenn sich der Cursor auf dem gruppierten Index einer Tabelle befindet. es wurde kein primärer Index definiert.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-158">This will happen for <strong>JetSetIndexRange</strong> if the cursor is on the clustered index of a table, a primary index has not been defined.</span></span> <span data-ttu-id="cfcf0-159">Das Festlegen eines Index Bereichs über einen solchen Index wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-159">Setting an index range over such an index is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfcf0-160">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="cfcf0-160">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-161">Dieser Fehler wird von <strong>jetsetindexrange</strong> zurückgegeben, um anzugeben, dass innerhalb des Index Bereichs keine Indexeinträge vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-161">This error will be returned by <strong>JetSetIndexRange</strong> to indicate that there are no index entries inside the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfcf0-162">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="cfcf0-162">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-163">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-163">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfcf0-164">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="cfcf0-164">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-165">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-165">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfcf0-166">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="cfcf0-166">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-167">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-167">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="cfcf0-168">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-168">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfcf0-169">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="cfcf0-169">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="cfcf0-170">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-170">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cfcf0-171">Wenn JET_bitRangeRemove angegeben wird, wird der derzeit in Kraft gelegte Index Bereich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-171">On success, if JET_bitRangeRemove is specified, then the index range that is currently in effect is canceled.</span></span> <span data-ttu-id="cfcf0-172">Wenn JET_bitRangeRemove nicht angegeben ist und JET_bitRangeInstantDuration angegeben ist, ist kein Index Bereich in Kraft.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-172">If JET_bitRangeRemove is not specified and JET_bitRangeInstantDuration is specified, then no index range is in effect.</span></span> <span data-ttu-id="cfcf0-173">Wenn weder JET_bitRangeRemove noch JET_bitRangeInstantDuration angegeben ist, ist ein neuer Index Bereich in Kraft.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-173">If neither JET_bitRangeRemove nor JET_bitRangeInstantDuration is specified, then a new index range is in effect.</span></span> <span data-ttu-id="cfcf0-174">Dieser Index Bereich schränkt temporär den Satz der Indexeinträge ein, die der Cursor mithilfe von [jetmove](./jetmove-function.md) durchlaufen kann, beginnend mit dem aktuellen Index Eintrag und endet mit dem Index Eintrag, der mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-174">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="cfcf0-175">Die Position des Cursors bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-175">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="cfcf0-176">Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-176">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="cfcf0-177">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-177">No change to the database state will occur.</span></span>

<span data-ttu-id="cfcf0-178">Bei einem Fehler wird kein Index Bereich wirksam, wenn JET_errNoCurrentRecord nicht zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-178">On failure, if JET_errNoCurrentRecord is not returned, then no index range is in effect.</span></span> <span data-ttu-id="cfcf0-179">Wenn JET_errNoCurrentRecord zurückgegeben wird, ist ein neuer Index Bereich wirksam.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-179">If JET_errNoCurrentRecord is returned, then a new index range is in effect.</span></span> <span data-ttu-id="cfcf0-180">Dieser Index Bereich schränkt temporär den Satz der Indexeinträge ein, die der Cursor mithilfe von [jetmove](./jetmove-function.md) durchlaufen kann, beginnend mit dem aktuellen Index Eintrag und endet mit dem Index Eintrag, der mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-180">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="cfcf0-181">Die Position des Cursors bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-181">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="cfcf0-182">Wenn JET_errNoCurrentRecord zurückgegeben wurde und ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-182">If JET_errNoCurrentRecord was returned and a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="cfcf0-183">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-183">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cfcf0-184">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfcf0-184">Remarks</span></span>

<span data-ttu-id="cfcf0-185">Ein Index Bereich ist flüchtig und wird automatisch abgebrochen, wenn eine andere Navigation als [jetmove](./jetmove-function.md) für den Cursor ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-185">An index range is volatile and will automatically be canceled if any navigation other than [JetMove](./jetmove-function.md) is performed on the cursor.</span></span>

<span data-ttu-id="cfcf0-186">Index Bereiche funktionieren nur in einer Richtung.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-186">Index ranges only work in one direction.</span></span> <span data-ttu-id="cfcf0-187">Wenn eine Obergrenze festgelegt wird, wird nur Vorwärtsbewegung mithilfe von [jetmove](./jetmove-function.md) mit JET_MoveNext oder ein positiver Offset verhindert, sobald das Ende des Index Bereichs erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-187">If an upper limit is established then only forward motion using [JetMove](./jetmove-function.md) with JET_MoveNext or a positive offset will be prevented once the end of the index range has been reached.</span></span> <span data-ttu-id="cfcf0-188">Es ist weiterhin möglich, den Index Bereich in diesem Fall mithilfe von [jetmove](./jetmove-function.md) mit JET_MovePrevious oder einem negativen Offset zu belassen.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-188">It is still possible to leave the index range in this case using [JetMove](./jetmove-function.md) with JET_MovePrevious or a negative offset.</span></span> <span data-ttu-id="cfcf0-189">Eine analoge Situation tritt bei einer niedrigeren Grenze auf.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-189">An analogous situation occurs for a lower limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="cfcf0-190">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfcf0-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfcf0-191"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cfcf0-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cfcf0-192">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfcf0-193"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cfcf0-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cfcf0-194">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfcf0-195"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="cfcf0-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cfcf0-196">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfcf0-197"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="cfcf0-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cfcf0-198">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfcf0-199"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cfcf0-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cfcf0-200">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cfcf0-200">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cfcf0-201">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cfcf0-201">See Also</span></span>

[<span data-ttu-id="cfcf0-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cfcf0-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cfcf0-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="cfcf0-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="cfcf0-204">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="cfcf0-204">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="cfcf0-205">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="cfcf0-205">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="cfcf0-206">Jetmakekey</span><span class="sxs-lookup"><span data-stu-id="cfcf0-206">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="cfcf0-207">Jetmove</span><span class="sxs-lookup"><span data-stu-id="cfcf0-207">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="cfcf0-208">Jetsetindexrange</span><span class="sxs-lookup"><span data-stu-id="cfcf0-208">JetSetIndexRange</span></span>]()  
[<span data-ttu-id="cfcf0-209">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="cfcf0-209">JetStopService</span></span>](./jetstopservice-function.md)
