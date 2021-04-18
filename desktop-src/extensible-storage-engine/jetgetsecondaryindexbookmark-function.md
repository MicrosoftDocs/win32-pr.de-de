---
description: 'Weitere Informationen: jetgetsecondaryindexbookmark-Funktion'
title: Jetgetsecondaryindexbookmark-Funktion
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d86b875037982a18ebb9d488c3a05b3123002b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358509"
---
# <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="d625e-103">Jetgetsecondaryindexbookmark-Funktion</span><span class="sxs-lookup"><span data-stu-id="d625e-103">JetGetSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="d625e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d625e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="d625e-105">Jetgetsecondaryindexbookmark-Funktion</span><span class="sxs-lookup"><span data-stu-id="d625e-105">JetGetSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="d625e-106">Die **jetgetsecondaryindexbookmark** -Funktion Ruft ein spezielles Lesezeichen für den sekundären Index Eintrag an der aktuellen Position eines Cursors ab.</span><span class="sxs-lookup"><span data-stu-id="d625e-106">The **JetGetSecondaryIndexBookmark** function retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="d625e-107">Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von [jetgoysecondaryindexbookmark](./jetgotosecondaryindexbookmark-function.md)effizient wieder in denselben Index Eintrag zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="d625e-107">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md).</span></span> <span data-ttu-id="d625e-108">Dies ist besonders nützlich, wenn Sie einen sekundären Index neu positionieren, der doppelte Schlüssel enthält oder mehrere Indexeinträge für denselben Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="d625e-108">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="d625e-109">**Windows XP: jetgetsecondaryindexbookmark** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d625e-109">**Windows XP:  JetGetSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d625e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d625e-110">Parameters</span></span>

<span data-ttu-id="d625e-111">*-sid*</span><span class="sxs-lookup"><span data-stu-id="d625e-111">*sesid*</span></span>

<span data-ttu-id="d625e-112">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d625e-112">The session to use for this call.</span></span>

<span data-ttu-id="d625e-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d625e-113">*tableid*</span></span>

<span data-ttu-id="d625e-114">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d625e-114">The cursor to use for this call.</span></span>

<span data-ttu-id="d625e-115">*pvsecondarykey*</span><span class="sxs-lookup"><span data-stu-id="d625e-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="d625e-116">Der Ausgabepuffer, der den sekundären Schlüssel empfängt.</span><span class="sxs-lookup"><span data-stu-id="d625e-116">The output buffer that receives the secondary key.</span></span>

<span data-ttu-id="d625e-117">*cbsecondarykeymax*</span><span class="sxs-lookup"><span data-stu-id="d625e-117">*cbSecondaryKeyMax*</span></span>

<span data-ttu-id="d625e-118">Die maximale Größe (in Bytes) des Ausgabepuffers für den sekundären Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="d625e-118">The maximum size, in bytes, of the output buffer for the secondary key.</span></span>

<span data-ttu-id="d625e-119">*pcbsecondarykeyactual*</span><span class="sxs-lookup"><span data-stu-id="d625e-119">*pcbSecondaryKeyActual*</span></span>

<span data-ttu-id="d625e-120">Empfängt die tatsächliche Größe des sekundären Schlüssels in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d625e-120">Receives the actual size in bytes of the secondary key.</span></span>

<span data-ttu-id="d625e-121">Wenn dieser Parameter NULL ist, wird die tatsächliche Größe des sekundären Schlüssels nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d625e-121">If this parameter is NULL, the actual size of the secondary key will not be returned.</span></span>

<span data-ttu-id="d625e-122">Wenn der Ausgabepuffer zu klein ist, wird die tatsächliche Größe des sekundären Schlüssels weiterhin zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d625e-122">If the output buffer is too small, the actual size of the secondary key will still be returned.</span></span> <span data-ttu-id="d625e-123">Dies bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.</span><span class="sxs-lookup"><span data-stu-id="d625e-123">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="d625e-124">*pvprimarybookmark*</span><span class="sxs-lookup"><span data-stu-id="d625e-124">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="d625e-125">Der Ausgabepuffer, der das Primärschlüssel-Lesezeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="d625e-125">The output buffer that receives the primary key bookmark.</span></span>

<span data-ttu-id="d625e-126">*cbprimarybookmarkmax*</span><span class="sxs-lookup"><span data-stu-id="d625e-126">*cbPrimaryBookmarkMax*</span></span>

<span data-ttu-id="d625e-127">Die maximale Größe (in Bytes) des Ausgabepuffers für das Primärschlüssel-Lesezeichen.</span><span class="sxs-lookup"><span data-stu-id="d625e-127">The maximum size, in bytes, of the output buffer for the primary key bookmark.</span></span>

<span data-ttu-id="d625e-128">*pcbprimarykeyactual*</span><span class="sxs-lookup"><span data-stu-id="d625e-128">*pcbPrimaryKeyActual*</span></span>

<span data-ttu-id="d625e-129">Empfängt die tatsächliche Größe (in Bytes) des Primärschlüssel-Lesezeichens.</span><span class="sxs-lookup"><span data-stu-id="d625e-129">Receives the actual size, in bytes, of the primary key bookmark.</span></span>

<span data-ttu-id="d625e-130">Wenn dieser Parameter NULL ist, wird die tatsächliche Größe des Primärschlüssel-Lesezeichens nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d625e-130">If this parameter is NULL then the actual size of the primary key bookmark will not be returned.</span></span>

<span data-ttu-id="d625e-131">Wenn der Ausgabepuffer zu klein ist, wird die tatsächliche Größe des Primärschlüssel-Lesezeichens weiterhin zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d625e-131">If the output buffer is too small, the actual size of the primary key bookmark will still be returned.</span></span> <span data-ttu-id="d625e-132">Dies bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.</span><span class="sxs-lookup"><span data-stu-id="d625e-132">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="d625e-133">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d625e-133">*grbit*</span></span>

<span data-ttu-id="d625e-134">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="d625e-134">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="d625e-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d625e-135">Return Value</span></span>

<span data-ttu-id="d625e-136">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="d625e-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d625e-137">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d625e-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d625e-138">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d625e-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="d625e-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d625e-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d625e-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d625e-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d625e-141">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d625e-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d625e-142">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="d625e-142">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="d625e-143">Der Vorgang wurde erfolgreich abgeschlossen, aber einer der Ausgabepuffer war zu klein, um die angeforderten Daten zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d625e-143">The operation completed successfully, but one of the output buffers was too small to receive the requested data.</span></span></p>
<p><span data-ttu-id="d625e-144">Der Ausgabepuffer wurde mit dem Umfang des Lesezeichens aufgefüllt, das passt.</span><span class="sxs-lookup"><span data-stu-id="d625e-144">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="d625e-145">Die tatsächliche Größe des Lesezeichens wurde auch zurückgegeben, wenn dies angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="d625e-145">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d625e-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d625e-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d625e-147">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d625e-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d625e-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d625e-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d625e-149">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="d625e-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="d625e-150">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d625e-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d625e-151">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="d625e-151">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="d625e-152">Der Cursor befindet sich derzeit nicht auf einem sekundären Index.</span><span class="sxs-lookup"><span data-stu-id="d625e-152">The cursor is not currently on a secondary index.</span></span></p>
<p><span data-ttu-id="d625e-153">Das Abrufen eines sekundären Index Lesezeichens ist nicht sinnvoll, wenn der Cursor aktuell keinen sekundären Index verwendet.</span><span class="sxs-lookup"><span data-stu-id="d625e-153">It is not meaningful to retrieve a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="d625e-154"><a href="gg269221(v=exchg.10).md">Jetgetbookmark</a> sollte verwendet werden, wenn sich der Cursor nicht auf einem sekundären Index befindet.</span><span class="sxs-lookup"><span data-stu-id="d625e-154"><a href="gg269221(v=exchg.10).md">JetGetBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d625e-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="d625e-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="d625e-156">Der Cursor ist nicht in einem Datensatz positioniert.</span><span class="sxs-lookup"><span data-stu-id="d625e-156">The cursor is not positioned on a record.</span></span></p>
<p><span data-ttu-id="d625e-157">Dafür sind viele verschiedene Gründe möglich.</span><span class="sxs-lookup"><span data-stu-id="d625e-157">This can happen for many different reasons.</span></span> <span data-ttu-id="d625e-158">Dies ist beispielsweise der Fall, wenn der Cursor aktuell nach dem letzten Datensatz im aktuellen Index positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="d625e-158">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d625e-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d625e-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d625e-160">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d625e-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d625e-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d625e-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d625e-162">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d625e-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d625e-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d625e-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d625e-164">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d625e-164">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="d625e-165">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d625e-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d625e-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d625e-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d625e-167">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="d625e-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d625e-168">Bei Erfolg wird das sekundäre Index Lesezeichen für den Index Eintrag an der aktuellen Position eines Cursors in den Ausgabe Puffern zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d625e-168">On success, the secondary index bookmark for the index entry at the current position of a cursor will be returned in the output buffers.</span></span> <span data-ttu-id="d625e-169">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="d625e-169">No change to the database state will occur.</span></span>

<span data-ttu-id="d625e-170">Bei einem Fehler wird der Zustand der Ausgabepuffer und die tatsächliche Größe des sekundären Index Lesezeichens nur dann definiert, wenn JET_errBufferTooSmall zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d625e-170">On failure, the state of the output buffers and the actual size of the secondary index bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="d625e-171">Wenn JET_errBufferTooSmall zurückgegeben wird, enthalten die Ausgabepuffer so viel von dem sekundären Index Lesezeichen, das in den bereitgestellten Speicherplatz passt, und die tatsächliche Größe des sekundären Index Lesezeichens ist genau.</span><span class="sxs-lookup"><span data-stu-id="d625e-171">In the event that JET_errBufferTooSmall is returned, the output buffers will contain as much of the secondary index bookmark as will fit in the space provided and the actual size of the secondary index bookmark will be accurate.</span></span> <span data-ttu-id="d625e-172">In jedem Fall erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="d625e-172">In any case, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d625e-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d625e-173">Remarks</span></span>

<span data-ttu-id="d625e-174">Lesezeichen sollten im Allgemeinen als nicht transparente Datenblöcke behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="d625e-174">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="d625e-175">Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen.</span><span class="sxs-lookup"><span data-stu-id="d625e-175">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="d625e-176">Allerdings können die folgenden Eigenschaften für alle ESENT-Lesezeichen bekannt sein:</span><span class="sxs-lookup"><span data-stu-id="d625e-176">However, the following properties can be known about all ESENT bookmarks:</span></span>

  - <span data-ttu-id="d625e-177">Ein Lesezeichen identifiziert eindeutig einen Datensatz in einer bestimmten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d625e-177">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="d625e-178">Das Lesezeichen eines Datensatzes ändert sich nicht für die Lebensdauer dieses Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="d625e-178">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="d625e-179">Das Lesezeichen eines Datensatzes entspricht dem Schlüssel dieses Datensatzes auf dem primären Index für die Tabelle, die diesen Datensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="d625e-179">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="d625e-180">Wenn kein primärer Index für diese Tabelle definiert ist, erstellt die Datenbank-Engine ein eigenes Lesezeichen für den Datensatz.</span><span class="sxs-lookup"><span data-stu-id="d625e-180">If no primary index is defined over that table, the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="d625e-181">Lesezeichen können mithilfe von [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) miteinander verglichen werden, um ihre relative Reihenfolge im primären Index für die Tabelle der Quelldaten Sätze festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d625e-181">Bookmarks may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="d625e-182">Wenn kein primärer Index für diese Tabelle definiert ist, ist die relative Reihenfolge von Lesezeichen aus dieser Tabelle nicht sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="d625e-182">If no primary index is defined over that table, the relative ordering of bookmarks from that table is not meaningful.</span></span>

  - <span data-ttu-id="d625e-183">Es ist bedeutungslos, Lesezeichen von Datensätzen aus unterschiedlichen Tabellen miteinander zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="d625e-183">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="d625e-184">Ein Lesezeichen ist immer kleiner oder gleich JET_cbBookmarkMost (256) Bytes in der Länge vor Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d625e-184">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="d625e-185">In Windows Vista und späteren Versionen können Lesezeichen größer sein.</span><span class="sxs-lookup"><span data-stu-id="d625e-185">On Windows Vista and later releases, bookmarks can be larger.</span></span> <span data-ttu-id="d625e-186">Die maximale Größe eines Lesezeichens ist gleich dem aktuellen Wert von JET_paramKeyMost + 1.</span><span class="sxs-lookup"><span data-stu-id="d625e-186">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

<span data-ttu-id="d625e-187">Schlüssel sollten im Allgemeinen als nicht transparente Datenblöcke behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="d625e-187">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="d625e-188">Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen.</span><span class="sxs-lookup"><span data-stu-id="d625e-188">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="d625e-189">Allerdings können die folgenden Eigenschaften für alle ESENT-Schlüssel bekannt sein:</span><span class="sxs-lookup"><span data-stu-id="d625e-189">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="d625e-190">Schlüssel können mit [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) miteinander verglichen werden, um ihre relative Reihenfolge im Ursprungs Index für die Tabelle der Quell Indexeinträge festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d625e-190">Keys may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="d625e-191">Es ist bedeutungslos, Schlüssel von Indexeinträgen aus verschiedenen Indizes miteinander zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="d625e-191">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="d625e-192">Ein Schlüssel ist immer kleiner oder gleich JET_cbKeyMost (255) Bytes in der Länge vor Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d625e-192">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="d625e-193">Unter Windows Vista und späteren Versionen können Schlüssel größer sein.</span><span class="sxs-lookup"><span data-stu-id="d625e-193">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="d625e-194">Die maximale Größe eines Schlüssels ist gleich dem aktuellen Wert JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="d625e-194">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d625e-195">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d625e-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d625e-196"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d625e-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d625e-197">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d625e-197">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d625e-198"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d625e-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d625e-199">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d625e-199">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d625e-200"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d625e-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d625e-201">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="d625e-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d625e-202"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="d625e-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d625e-203">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d625e-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d625e-204"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d625e-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d625e-205">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d625e-205">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d625e-206">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d625e-206">See Also</span></span>

[<span data-ttu-id="d625e-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d625e-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d625e-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d625e-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d625e-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d625e-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d625e-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d625e-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d625e-211">Jetgetbookmark</span><span class="sxs-lookup"><span data-stu-id="d625e-211">JetGetBookmark</span></span>](./jetgetbookmark-function.md)  
[<span data-ttu-id="d625e-212">Jetgoysecondaryindexbookmark</span><span class="sxs-lookup"><span data-stu-id="d625e-212">JetGotoSecondaryIndexBookmark</span></span>](./jetgotosecondaryindexbookmark-function.md)  
[<span data-ttu-id="d625e-213">Jetretrievekey</span><span class="sxs-lookup"><span data-stu-id="d625e-213">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
<span data-ttu-id="d625e-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="d625e-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>
