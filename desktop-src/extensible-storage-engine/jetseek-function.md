---
description: 'Weitere Informationen zu: JetSeek-Funktion'
title: JetSeek-Funktion
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c386ae3af5353b95d9d1d3c67df4d680c52bff68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360827"
---
# <a name="jetseek-function"></a><span data-ttu-id="5f119-103">JetSeek-Funktion</span><span class="sxs-lookup"><span data-stu-id="5f119-103">JetSeek Function</span></span>


<span data-ttu-id="5f119-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5f119-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetseek-function"></a><span data-ttu-id="5f119-105">JetSeek-Funktion</span><span class="sxs-lookup"><span data-stu-id="5f119-105">JetSeek Function</span></span>

<span data-ttu-id="5f119-106">Die **JetSeek** -Funktion positioniert einen Cursor effizient auf einen Index Eintrag, der mit den Suchkriterien übereinstimmt, die durch den Suchschlüssel in diesem Cursor und die angegebene Ungleichheit festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="5f119-106">The **JetSeek** function efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="5f119-107">Ein Suchschlüssel muss zuvor mithilfe von [jetmakekey](./jetmakekey-function.md)erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="5f119-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="5f119-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f119-108">Parameters</span></span>

<span data-ttu-id="5f119-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="5f119-109">*sesid*</span></span>

<span data-ttu-id="5f119-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f119-110">The session to use for this call.</span></span>

<span data-ttu-id="5f119-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="5f119-111">*tableid*</span></span>

<span data-ttu-id="5f119-112">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f119-112">The cursor to use for this call.</span></span>

<span data-ttu-id="5f119-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="5f119-113">*grbit*</span></span>

<span data-ttu-id="5f119-114">Eine Gruppe von Bits, die die Optionen enthalten, die für diesen-Befehl verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5f119-114">A group of bits that contain the options to be used for this call.</span></span> <span data-ttu-id="5f119-115">*Grbit* darf nicht NULL sein und muss mindestens einen der Werte enthalten, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5f119-115">*Grbit* must be nonzero and must include one or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f119-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5f119-116">Value</span></span></p></th>
<th><p><span data-ttu-id="5f119-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5f119-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f119-118">JET_bitCheckUniqueness</span><span class="sxs-lookup"><span data-stu-id="5f119-118">JET_bitCheckUniqueness</span></span></p></td>
<td><p><span data-ttu-id="5f119-119">Ein spezieller Fehlercode, der JET_wrnUniqueKey, wird zurückgegeben, wenn er mit einer kostengünstigen Bestimmung feststellen kann, dass es genau einen Index Eintrag gibt, der mit dem Suchschlüssel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5f119-119">A special error code, JET_wrnUniqueKey, will be returned if it can be cheaply determined that there is exactly one index entry that matches the search key.</span></span></p>
<p><span data-ttu-id="5f119-120">Diese Option wird ignoriert, es sei denn, JET_bitSeekEQ ebenfalls angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5f119-120">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p>
<p><span data-ttu-id="5f119-121">Diese Option ist nur für Windows Server 2003 und spätere Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5f119-121">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f119-122">JET_bitSeekEQ</span><span class="sxs-lookup"><span data-stu-id="5f119-122">JET_bitSeekEQ</span></span></p></td>
<td><p><span data-ttu-id="5f119-123">Der Cursor wird am Index Eintrag positioniert, der am nächsten am Anfang des Indexes liegt, der exakt mit dem Suchschlüssel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5f119-123">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span> <span data-ttu-id="5f119-124">Der Index Anfang ist der Index Eintrag, der beim Verschieben in den ersten Datensatz in diesem Index gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="5f119-124">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="5f119-125">Der Index Anfang ist nicht mit dem unteren Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</span><span class="sxs-lookup"><span data-stu-id="5f119-125">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="5f119-126">Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe einer Platzhalter Option mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5f119-126">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f119-127">JET_bitSeekGE</span><span class="sxs-lookup"><span data-stu-id="5f119-127">JET_bitSeekGE</span></span></p></td>
<td><p><span data-ttu-id="5f119-128">Der Cursor wird am Index Eintrag positioniert, der dem Anfang des Indexes am nächsten liegt, der größer als oder gleich einem Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5f119-128">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="5f119-129">Der Index Anfang ist der Index Eintrag, der beim Verschieben in den ersten Datensatz in diesem Index gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="5f119-129">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="5f119-130">Der Index Anfang ist nicht mit dem unteren Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</span><span class="sxs-lookup"><span data-stu-id="5f119-130">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="5f119-131">Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde, indem eine Platzhalter Option verwendet wurde, um Indexeinträge zu suchen, die dem Ende des Indexes am nächsten sind.</span><span class="sxs-lookup"><span data-stu-id="5f119-131">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f119-132">JET_bitSeekGT</span><span class="sxs-lookup"><span data-stu-id="5f119-132">JET_bitSeekGT</span></span></p></td>
<td><p><span data-ttu-id="5f119-133">Der Cursor wird am Index Eintrag positioniert, der dem Anfang des Indexes am nächsten liegt, der größer als ein Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5f119-133">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="5f119-134">Der Index Anfang ist der Index Eintrag, der beim Verschieben in den ersten Datensatz in diesem Index gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="5f119-134">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="5f119-135">Der Index Anfang ist nicht mit dem unteren Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</span><span class="sxs-lookup"><span data-stu-id="5f119-135">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="5f119-136">Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde, indem eine Platzhalter Option verwendet wurde, um Indexeinträge zu suchen, die dem Anfang des Indexes am nächsten liegen.</span><span class="sxs-lookup"><span data-stu-id="5f119-136">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f119-137">JET_bitSeekLE</span><span class="sxs-lookup"><span data-stu-id="5f119-137">JET_bitSeekLE</span></span></p></td>
<td><p><span data-ttu-id="5f119-138">Der Cursor wird am Index Eintrag positioniert, der am nächsten am Ende des Indexes liegt, der kleiner oder gleich einem Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5f119-138">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="5f119-139">Das Ende des Indexes ist der Index Eintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="5f119-139">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="5f119-140">Das Ende des Indexes ist nicht mit dem hohen Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</span><span class="sxs-lookup"><span data-stu-id="5f119-140">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="5f119-141">Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde, indem eine Platzhalter Option verwendet wurde, um Indexeinträge zu suchen, die dem Anfang des Indexes am nächsten liegen.</span><span class="sxs-lookup"><span data-stu-id="5f119-141">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f119-142">JET_bitSeekLT</span><span class="sxs-lookup"><span data-stu-id="5f119-142">JET_bitSeekLT</span></span></p></td>
<td><p><span data-ttu-id="5f119-143">Der Cursor wird am Index Eintrag positioniert, der am nächsten am Ende des Indexes liegt, der kleiner als ein Index Eintrag ist, der genau mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5f119-143">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="5f119-144">Das Ende des Indexes ist der Index Eintrag, der beim Verschieben zum letzten Datensatz in diesem Index gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="5f119-144">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="5f119-145">Das Ende des Indexes ist nicht mit dem hohen Ende des Indexes identisch, was sich je nach Sortierreihenfolge der Schlüssel Spalten im Index ändern kann.</span><span class="sxs-lookup"><span data-stu-id="5f119-145">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="5f119-146">Es ist nicht sinnvoll, diese Option mit einem Suchschlüssel zu verwenden, der mithilfe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt wurde, indem eine Platzhalter Option verwendet wurde, um Indexeinträge zu suchen, die dem Ende des Indexes am nächsten sind.</span><span class="sxs-lookup"><span data-stu-id="5f119-146">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f119-147">JET_bitSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="5f119-147">JET_bitSetIndexRange</span></span></p></td>
<td><p><span data-ttu-id="5f119-148">Ein Index Bereich wird automatisch für alle Schlüssel eingerichtet, die exakt mit dem Suchschlüssel übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5f119-148">An index range will automatically be setup for all keys that exactly match the search key.</span></span> <span data-ttu-id="5f119-149">Der resultierende Index Bereich ist identisch mit einem Index Bereich, der andernfalls durch einen Aufrufen von <a href="gg294112(v=exchg.10).md">jetsetindexrange</a> mit den Optionen JET_bitRangeInclusive und JET_bitRangeUpperLimit erstellt worden wäre.</span><span class="sxs-lookup"><span data-stu-id="5f119-149">The resulting index range is identical to one that would have otherwise been created by a call to <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> with the JET_bitRangeInclusive and JET_bitRangeUpperLimit options.</span></span> <span data-ttu-id="5f119-150">Weitere Informationen finden Sie unter <a href="gg294112(v=exchg.10).md">jetsetindexrange</a> .</span><span class="sxs-lookup"><span data-stu-id="5f119-150">See <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> for more information.</span></span></p>
<p><span data-ttu-id="5f119-151">Dies ist eine bequeme Methode zum Ermitteln aller Indexeinträge, die denselben Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5f119-151">This is a convenient method for discovering all the index entries that match the same search criteria.</span></span></p>
<p><span data-ttu-id="5f119-152">Diese Option wird ignoriert, es sei denn, JET_bitSeekEQ ebenfalls angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5f119-152">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="5f119-153">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f119-153">Return Value</span></span>

<span data-ttu-id="5f119-154">Diese Funktion ermöglicht die Rückgabe von [JET_ERRs](./jet-err.md) , die in dieser API definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5f119-154">This function allows for the return of any [JET_ERRs](./jet-err.md) that are defined in this API.</span></span> <span data-ttu-id="5f119-155">Weitere Informationen zu Jet-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5f119-155">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f119-156">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5f119-156">Return code</span></span></p></th>
<th><p><span data-ttu-id="5f119-157">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f119-157">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f119-158">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5f119-158">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5f119-159">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="5f119-159">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="5f119-160">Für <strong>JetSeek</strong>bedeutet dies, dass ein Index Eintrag gefunden wurde, der genau mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5f119-160">For <strong>JetSeek</strong>, this means that an index entry was found that exactly matched the search criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f119-161">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5f119-161">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5f119-162">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="5f119-162">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f119-163">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5f119-163">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5f119-164">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="5f119-164">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5f119-165">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f119-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f119-166">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="5f119-166">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="5f119-167">Es ist kein aktueller Suchschlüssel für den Cursor vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5f119-167">There is no current search key for the cursor.</span></span> <span data-ttu-id="5f119-168"><strong>JetSeek</strong> erfordert, dass der Cursor über einen gültigen Suchschlüssel verfügt, da er diesen für die Suchkriterien verwendet, die zum Suchen von Indexeinträgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f119-168"><strong>JetSeek</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f119-169">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5f119-169">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5f119-170">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5f119-170">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f119-171">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="5f119-171">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="5f119-172">Es wurde kein Index Eintrag gefunden, der mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5f119-172">No index entry was found that matched the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f119-173">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5f119-173">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5f119-174">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f119-174">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f119-175">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="5f119-175">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="5f119-176">Es wurde ein Index Eintrag gefunden, der mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5f119-176">An index entry was found that matched the search criteria.</span></span> <span data-ttu-id="5f119-177">Dieser Index Eintrag war jedoch keine genaue Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="5f119-177">However, that index entry was not an exact match.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f119-178">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="5f119-178">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="5f119-179">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f119-179">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="5f119-180">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f119-180">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f119-181">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5f119-181">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5f119-182">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="5f119-182">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f119-183">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="5f119-183">JET_wrnUniqueKey</span></span></p></td>
<td><p><span data-ttu-id="5f119-184">Es wurde genau ein Index Eintrag gefunden, der genau mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5f119-184">Exactly one index entry was found that exactly matched the search criteria.</span></span> <span data-ttu-id="5f119-185">Dieser Fehler wird nur zurückgegeben, wenn JET_bitSeekCheckUniqueness angegeben wurde, und es war sehr billig, zu ermitteln, ob der übereinstimmende Index Eintrag der einzige Index Eintrag war, der genau mit den Suchkriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5f119-185">This error will only be returned if JET_bitSeekCheckUniqueness was specified and it was cheap to determine that the matching index entry was the only index entry that exactly matches the search criteria.</span></span></p>
<p><span data-ttu-id="5f119-186">Dieser Fehler wird nur von Windows Server 2003 und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f119-186">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f119-187">Bei Erfolg wird der Cursor an einem Index Eintrag positioniert, der den Suchkriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="5f119-187">On success, the cursor will be positioned at an index entry that matches the search criteria.</span></span> <span data-ttu-id="5f119-188">Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="5f119-188">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="5f119-189">Wenn ein Index Bereich wirksam ist, wird dieser Index Bereich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="5f119-189">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="5f119-190">Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5f119-190">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="5f119-191">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="5f119-191">No change to the database state will occur.</span></span> <span data-ttu-id="5f119-192">Wenn mehrere Indexeinträge denselben Wert aufweisen, wird der am Anfang des Indexes am nächsten liegenden Eintrag immer ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="5f119-192">When multiple index entries have the same value, the entry closest to the start of the index is always selected.</span></span>

<span data-ttu-id="5f119-193">Bei einem Fehler bleibt die Position des Cursors unverändert, es sei denn, JET_errRecordNotFound zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5f119-193">On failure, the position of the cursor will remain unchanged unless JET_errRecordNotFound was returned.</span></span> <span data-ttu-id="5f119-194">In diesem Fall wird der Cursor positioniert, wo der Index Eintrag, der mit den Suchkriterien übereinstimmt, die durch den Suchschlüssel in diesem Cursor und der angegebenen Ungleichheit angegeben wurden, wäre.</span><span class="sxs-lookup"><span data-stu-id="5f119-194">In that case, the cursor will be positioned where the index entry that matched the search criteria specified by the search key in that cursor and the specified inequality would have been.</span></span> <span data-ttu-id="5f119-195">Der Cursor kann relativ zu dieser Position verschoben werden, befindet sich jedoch noch nicht in einem gültigen Index Eintrag.</span><span class="sxs-lookup"><span data-stu-id="5f119-195">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="5f119-196">Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="5f119-196">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="5f119-197">Wenn ein Index Bereich wirksam ist, wird dieser Index Bereich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="5f119-197">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="5f119-198">Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5f119-198">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="5f119-199">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="5f119-199">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5f119-200">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f119-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f119-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5f119-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5f119-202">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5f119-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f119-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5f119-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5f119-204">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5f119-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f119-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5f119-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5f119-206">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="5f119-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f119-207"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="5f119-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5f119-208">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5f119-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f119-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5f119-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5f119-210">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5f119-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5f119-211">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5f119-211">See Also</span></span>

[<span data-ttu-id="5f119-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5f119-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5f119-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5f119-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5f119-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5f119-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5f119-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5f119-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5f119-216">Jetmakekey</span><span class="sxs-lookup"><span data-stu-id="5f119-216">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="5f119-217">Jetsetindexrange</span><span class="sxs-lookup"><span data-stu-id="5f119-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="5f119-218">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="5f119-218">JetStopService</span></span>](./jetstopservice-function.md)
