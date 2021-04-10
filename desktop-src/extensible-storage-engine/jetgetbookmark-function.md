---
description: 'Weitere Informationen: jetgetbookmark-Funktion'
title: Jetgetbookmark-Funktion
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a27ce474a8f021ff9039a07d7542b194e72e262a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131961"
---
# <a name="jetgetbookmark-function"></a><span data-ttu-id="d06ad-103">Jetgetbookmark-Funktion</span><span class="sxs-lookup"><span data-stu-id="d06ad-103">JetGetBookmark Function</span></span>


<span data-ttu-id="d06ad-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d06ad-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetbookmark-function"></a><span data-ttu-id="d06ad-105">Jetgetbookmark-Funktion</span><span class="sxs-lookup"><span data-stu-id="d06ad-105">JetGetBookmark Function</span></span>

<span data-ttu-id="d06ad-106">Die **jetgetbookmark** -Funktion Ruft das Lesezeichen für den Datensatz ab, der mit dem Index Eintrag an der aktuellen Position eines Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="d06ad-106">The **JetGetBookmark** function retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="d06ad-107">Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von [jetgobackbookmark](./jetgotobookmark-function.md)wieder in denselben Datensatz zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="d06ad-107">This bookmark can then be used to reposition that cursor back to the same record using [JetGoToBookmark](./jetgotobookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="d06ad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d06ad-108">Parameters</span></span>

<span data-ttu-id="d06ad-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="d06ad-109">*sesid*</span></span>

<span data-ttu-id="d06ad-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d06ad-110">The session to use for this call.</span></span>

<span data-ttu-id="d06ad-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d06ad-111">*tableid*</span></span>

<span data-ttu-id="d06ad-112">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d06ad-112">The cursor to use for this call.</span></span>

<span data-ttu-id="d06ad-113">*pvbookmark*</span><span class="sxs-lookup"><span data-stu-id="d06ad-113">*pvBookmark*</span></span>

<span data-ttu-id="d06ad-114">Der Ausgabepuffer, der das Lesezeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="d06ad-114">The output buffer that receives the bookmark.</span></span>

<span data-ttu-id="d06ad-115">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="d06ad-115">*cbMax*</span></span>

<span data-ttu-id="d06ad-116">Die maximale Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d06ad-116">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="d06ad-117">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="d06ad-117">*pcbActual*</span></span>

<span data-ttu-id="d06ad-118">Die tatsächliche Größe (in Bytes) des Lesezeichens.</span><span class="sxs-lookup"><span data-stu-id="d06ad-118">The actual size, in bytes, of the bookmark.</span></span>

<span data-ttu-id="d06ad-119">Wenn dieser Parameter **null** ist, wird die tatsächliche Größe des Lesezeichens nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d06ad-119">If this parameter is **NULL** then the actual size of the bookmark will not be returned.</span></span>

<span data-ttu-id="d06ad-120">Wenn der Ausgabepuffer zu klein ist, wird die tatsächliche Größe des Lesezeichens weiterhin zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d06ad-120">If the output buffer is too small, the actual size of the bookmark will still be returned.</span></span> <span data-ttu-id="d06ad-121">Dies bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.</span><span class="sxs-lookup"><span data-stu-id="d06ad-121">That means that this number will be larger than the size of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="d06ad-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d06ad-122">Return Value</span></span>

<span data-ttu-id="d06ad-123">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="d06ad-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d06ad-124">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d06ad-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d06ad-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d06ad-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="d06ad-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d06ad-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d06ad-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d06ad-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d06ad-128">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d06ad-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d06ad-129">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="d06ad-129">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="d06ad-130">Der Vorgang wurde erfolgreich abgeschlossen, aber der Ausgabepuffer war zu klein, um das ganze Lesezeichen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d06ad-130">The operation completed successfully, but the output buffer was too small to receive the entire bookmark.</span></span> <span data-ttu-id="d06ad-131">Der Ausgabepuffer wurde mit dem Umfang des Lesezeichens aufgefüllt, das passt.</span><span class="sxs-lookup"><span data-stu-id="d06ad-131">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="d06ad-132">Die tatsächliche Größe des Lesezeichens wurde auch zurückgegeben, wenn dies angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="d06ad-132">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d06ad-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d06ad-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d06ad-134">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d06ad-134">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d06ad-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d06ad-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d06ad-136">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</span><span class="sxs-lookup"><span data-stu-id="d06ad-136">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="d06ad-137"><strong>Windows XP:  </strong> Diese Rückgabewerte werden in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d06ad-137"><strong>Windows XP:  </strong>This return values is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d06ad-138">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="d06ad-138">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="d06ad-139">Der Cursor ist nicht in einem Datensatz positioniert.</span><span class="sxs-lookup"><span data-stu-id="d06ad-139">The cursor is not positioned on a record.</span></span> <span data-ttu-id="d06ad-140">Dafür sind viele verschiedene Gründe möglich.</span><span class="sxs-lookup"><span data-stu-id="d06ad-140">This can happen for many different reasons.</span></span> <span data-ttu-id="d06ad-141">Dies ist beispielsweise der Fall, wenn der Cursor nach dem letzten Datensatz im aktuellen Index positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="d06ad-141">For example, this will happen if the cursor is positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d06ad-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d06ad-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d06ad-143">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d06ad-143">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d06ad-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d06ad-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d06ad-145">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d06ad-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d06ad-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d06ad-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d06ad-147">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d06ad-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="d06ad-148"><strong>Windows XP:  </strong> Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d06ad-148"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d06ad-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d06ad-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d06ad-150">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="d06ad-150">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d06ad-151">Wenn diese Funktion erfolgreich ausgeführt wird, wird das Lesezeichen für den Datensatz, der dem Index Eintrag an der aktuellen Position eines Cursors zugeordnet ist, im Ausgabepuffer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d06ad-151">If this function succeeds, the bookmark for the record that is associated with the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="d06ad-152">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="d06ad-152">No change to the database state will occur.</span></span>

<span data-ttu-id="d06ad-153">Wenn diese Funktion fehlschlägt, werden der Status des Ausgabepuffers und die tatsächliche Größe des Lesezeichens nur dann definiert, wenn JET_errBufferTooSmall zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d06ad-153">If this function fails, the state of the output buffer and the actual size of the bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="d06ad-154">Wenn JET_errBufferTooSmall zurückgegeben wird, enthält der Ausgabepuffer den Teil des Lesezeichens, der in den bereitgestellten Bereich passt, und die tatsächliche Größe des Lesezeichens ist genau.</span><span class="sxs-lookup"><span data-stu-id="d06ad-154">In the event that JET_errBufferTooSmall is returned, the output buffer will contain as much of the bookmark as will fit in the space provided and the actual size of the bookmark will be accurate.</span></span> <span data-ttu-id="d06ad-155">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="d06ad-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d06ad-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d06ad-156">Remarks</span></span>

<span data-ttu-id="d06ad-157">Lesezeichen sollten im Allgemeinen als nicht transparente Datenblöcke behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="d06ad-157">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="d06ad-158">Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen.</span><span class="sxs-lookup"><span data-stu-id="d06ad-158">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="d06ad-159">Allerdings gelten für alle ESENT-Lesezeichen die folgenden Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="d06ad-159">However, the following conditions are true of all ESENT bookmarks:</span></span>

  - <span data-ttu-id="d06ad-160">Ein Lesezeichen identifiziert eindeutig einen Datensatz in einer bestimmten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d06ad-160">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="d06ad-161">Das Lesezeichen eines Datensatzes ändert sich nicht für die Lebensdauer dieses Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="d06ad-161">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="d06ad-162">Das Lesezeichen eines Datensatzes entspricht dem Schlüssel dieses Datensatzes auf dem primären Index für die Tabelle, die diesen Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="d06ad-162">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="d06ad-163">Wenn kein primärer Index für diese Tabelle definiert wird, erstellt die Datenbank-Engine ein eigenes Lesezeichen für den Datensatz.</span><span class="sxs-lookup"><span data-stu-id="d06ad-163">If no primary index is defined over that table the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="d06ad-164">Lesezeichen können miteinander verglichen werden, indem die [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) -Funktion verwendet wird, um ihre relative Reihenfolge im primären Index für die Tabelle der Quelldaten Sätze festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d06ad-164">Bookmarks can be compared against each other using the [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) function to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="d06ad-165">Wenn kein primärer Index für diese Tabelle definiert ist, ist es nicht sinnvoll, die relative Reihenfolge von Lesezeichen aus dieser Tabelle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d06ad-165">If no primary index is defined over that table, it is not meaningful to use the relative ordering of bookmarks from that table.</span></span>

  - <span data-ttu-id="d06ad-166">Es ist bedeutungslos, Lesezeichen von Datensätzen aus unterschiedlichen Tabellen miteinander zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="d06ad-166">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="d06ad-167">Ein Lesezeichen ist vor Windows Vista immer kleiner oder gleich JET_cbBookmarkMost (256) Bytes.</span><span class="sxs-lookup"><span data-stu-id="d06ad-167">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length, prior to Windows Vista.</span></span>
    
<span data-ttu-id="d06ad-168">**Windows Vista:** In Windows Vista und späteren Versionen können Lesezeichen größer als JET_cbBookmarkMost (256) Bytes sein.</span><span class="sxs-lookup"><span data-stu-id="d06ad-168">**Windows Vista:** On Windows Vista and later releases, bookmarks can be larger than JET_cbBookmarkMost (256) bytes.</span></span> <span data-ttu-id="d06ad-169">Die maximale Größe eines Lesezeichens ist gleich dem aktuellen Wert von JET_paramKeyMost + 1.</span><span class="sxs-lookup"><span data-stu-id="d06ad-169">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d06ad-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d06ad-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d06ad-171"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d06ad-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d06ad-172">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d06ad-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d06ad-173"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d06ad-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d06ad-174">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d06ad-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d06ad-175"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d06ad-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d06ad-176">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="d06ad-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d06ad-177"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="d06ad-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d06ad-178">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d06ad-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d06ad-179"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d06ad-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d06ad-180">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d06ad-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d06ad-181">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d06ad-181">See Also</span></span>

[<span data-ttu-id="d06ad-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d06ad-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d06ad-183">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d06ad-183">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d06ad-184">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d06ad-184">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d06ad-185">Jetgojebookmark</span><span class="sxs-lookup"><span data-stu-id="d06ad-185">JetGoToBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="d06ad-186">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="d06ad-186">JetStopService</span></span>](./jetstopservice-function.md)  
<span data-ttu-id="d06ad-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="d06ad-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>
