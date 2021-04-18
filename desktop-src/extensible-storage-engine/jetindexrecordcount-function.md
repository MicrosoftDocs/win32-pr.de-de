---
description: Weitere Informationen finden Sie in der jetindexrecordcount-Funktion.
title: Jetindexrecordcount-Funktion
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3324ad2fe68d106c7f4d2dcdcd1c3dd6ddefd608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524965"
---
# <a name="jetindexrecordcount-function"></a><span data-ttu-id="14001-103">Jetindexrecordcount-Funktion</span><span class="sxs-lookup"><span data-stu-id="14001-103">JetIndexRecordCount Function</span></span>


<span data-ttu-id="14001-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="14001-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetindexrecordcount-function"></a><span data-ttu-id="14001-105">Jetindexrecordcount-Funktion</span><span class="sxs-lookup"><span data-stu-id="14001-105">JetIndexRecordCount Function</span></span>

<span data-ttu-id="14001-106">Die **jetindexrecordcount** -Funktion zählt die Anzahl der Einträge im aktuellen Index von der aktuellen Position nach vorne.</span><span class="sxs-lookup"><span data-stu-id="14001-106">The **JetIndexRecordCount** function counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="14001-107">Die aktuelle Position ist in der Anzahl enthalten.</span><span class="sxs-lookup"><span data-stu-id="14001-107">The current position is included in the count.</span></span> <span data-ttu-id="14001-108">Die Anzahl kann größer als die Gesamtanzahl der Datensätze in der Tabelle sein, wenn der aktuelle Index eine mehrwertige Spalte überschreitet und Instanzen der Spalte mehrere Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="14001-108">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="14001-109">Wenn die Tabelle leer ist, wird 0 für die Anzahl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="14001-109">If the table is empty, then 0 will be returned for the count.</span></span>

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a><span data-ttu-id="14001-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="14001-110">Parameters</span></span>

<span data-ttu-id="14001-111">*-sid*</span><span class="sxs-lookup"><span data-stu-id="14001-111">*sesid*</span></span>

<span data-ttu-id="14001-112">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="14001-112">The session to use for this call.</span></span>

<span data-ttu-id="14001-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="14001-113">*tableid*</span></span>

<span data-ttu-id="14001-114">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="14001-114">The cursor to use for this call.</span></span>

<span data-ttu-id="14001-115">*pkrec*</span><span class="sxs-lookup"><span data-stu-id="14001-115">*pcrec*</span></span>

<span data-ttu-id="14001-116">Der Zeiger auf einen Long-Wert ohne Vorzeichen, der die Anzahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="14001-116">The pointer to an unsigned long value to receive the count.</span></span>

<span data-ttu-id="14001-117">*crecmax*</span><span class="sxs-lookup"><span data-stu-id="14001-117">*crecMax*</span></span>

<span data-ttu-id="14001-118">Die maximale Anzahl der zu zählenden Datensätze.</span><span class="sxs-lookup"><span data-stu-id="14001-118">The maximum number of records to count.</span></span> <span data-ttu-id="14001-119">Ein *crecmax* -Wert von 0 gibt an, dass die Anzahl unbegrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="14001-119">A *crecMax* value of 0 indicates that the count is unlimited.</span></span>

### <a name="return-value"></a><span data-ttu-id="14001-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14001-120">Return Value</span></span>

<span data-ttu-id="14001-121">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="14001-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="14001-122">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="14001-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="14001-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="14001-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="14001-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14001-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14001-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="14001-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="14001-126">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="14001-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14001-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="14001-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="14001-128">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="14001-128">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14001-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="14001-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="14001-130">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität dieser Daten zu schützen</span><span class="sxs-lookup"><span data-stu-id="14001-130">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="14001-131"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="14001-131"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14001-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="14001-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="14001-133">Der Cursor befindet sich derzeit nicht in einem Datensatz, und die Tabelle ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="14001-133">The cursor is not currently on a record and the table is not empty.</span></span></p>
<p><span data-ttu-id="14001-134"><strong>Windows XP, Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:</strong>  Wenn der Cursor auf einem leeren Index oder Index Bereich positioniert ist, gibt <strong>jetindexrecordcount</strong> irrtümlich JET_errNoCurrentRecord zurück.</span><span class="sxs-lookup"><span data-stu-id="14001-134"><strong>Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:</strong>  If the cursor is positioned on an empty index or index range then <strong>JetIndexRecordCount</strong> erroneously returns JET_errNoCurrentRecord.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14001-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="14001-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="14001-136">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="14001-136">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14001-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="14001-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="14001-138">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14001-138">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14001-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="14001-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="14001-140">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14001-140">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="14001-141"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="14001-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14001-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="14001-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="14001-143">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="14001-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14001-144">Wenn diese Funktion erfolgreich ausgeführt wird, wird die genaue Anzahl von Indexeinträgen, einschließlich der aktuellen Position und bis zu *crecmax* (wenn Sie nicht 0 ist), in "Ganzzahl ohne Vorzeichen long" zurückgegeben, auf das *pkrec* zeigt.</span><span class="sxs-lookup"><span data-stu-id="14001-144">If this function succeeds, the exact number of index entries including the current position and up to *crecMax* (if it is not 0), is returned in the unsigned long pointed to by *pcrec*.</span></span>

<span data-ttu-id="14001-145">Wenn diese Funktion fehlschlägt, werden keine Änderungen an dem bei den *Vorgängen* zugeordneten Arbeitsspeicher vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="14001-145">If this function fails, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="14001-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14001-146">Remarks</span></span>

<span data-ttu-id="14001-147">Wenn die Tabelle nicht leer ist, sollte der Cursor auf dem Datensatz positioniert werden, von dem aus die Anzahl begonnen werden soll.</span><span class="sxs-lookup"><span data-stu-id="14001-147">If the table is not empty, then the cursor should be positioned onto the record from which to begin the count.</span></span> <span data-ttu-id="14001-148">Die Anzahl schließt diesen Datensatz ein, und der Zähler wird auf den angegebenen Grenzwert in *crecmax* angerechnet.</span><span class="sxs-lookup"><span data-stu-id="14001-148">The count will include this record, and count forward up to the given limit in *crecMax*.</span></span> <span data-ttu-id="14001-149">Wenn *crecmax* den Wert 0 hat, wird der Vorgang bis zum Ende des Indexes fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="14001-149">If *crecMax* is 0 then the operation will continue counting until the end of the index.</span></span>

<span data-ttu-id="14001-150">Index Bereiche können zum Erstellen von künstlichen Index Beschränkungen für die Anzahl verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14001-150">Index ranges can be used to construct artificial end-of-index limitations for the count.</span></span> <span data-ttu-id="14001-151">Auf diese Weise können die Unterbereiche eines Indexes genau gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="14001-151">In this way, subranges of an index can be counted exactly.</span></span> <span data-ttu-id="14001-152">Der Cursor sollte in der ersten Zeile im Bereich positioniert werden.</span><span class="sxs-lookup"><span data-stu-id="14001-152">The cursor should be positioned to the first row in the range.</span></span> <span data-ttu-id="14001-153">Das Ende des Bereichs Schlüssels sollte festgelegt werden, und anschließend sollte [jetsetindexrange](./jetsetindexrange-function.md) verwendet werden, um den oberen Bereich festzulegen, entweder inklusiv oder exklusiv.</span><span class="sxs-lookup"><span data-stu-id="14001-153">The end of the range key should be made and then [JetSetIndexRange](./jetsetindexrange-function.md) should be used to set the upper range, either inclusively or exclusively.</span></span> <span data-ttu-id="14001-154">Schließlich sollte **jetindexrecordcount** aufgerufen werden, um den Bereich exakt zu zählen.</span><span class="sxs-lookup"><span data-stu-id="14001-154">Lastly, **JetIndexRecordCount** should be called to exactly count the range.</span></span>

<span data-ttu-id="14001-155">**Jetindexrecordcount** befolgt die Transaktions Semantik und gibt eine Anzahl zurück, die für diese bestimmte Sitzung im aktuellen Transaktionszustand korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="14001-155">**JetIndexRecordCount** obeys transaction semantics and returns a count that is accurate for this particular session in its current transactional state.</span></span>

<span data-ttu-id="14001-156">**Jetindexrecordcount** greift auf Blattseiten des Indexes zu, um Einträge exakt zu zählen.</span><span class="sxs-lookup"><span data-stu-id="14001-156">**JetIndexRecordCount** accesses index leaf pages in order to exactly count entries.</span></span> <span data-ttu-id="14001-157">Folglich kann es viele e/a-Vorgänge durchführen und kann langsam sein.</span><span class="sxs-lookup"><span data-stu-id="14001-157">Consequently, it can perform a great deal of I/O and can be slow.</span></span> <span data-ttu-id="14001-158">Die *crecmax* -Einschränkung sollte verwendet werden, um eine übermäßige Auslastung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="14001-158">The *crecMax* limitation should be used to prevent excessive load.</span></span> <span data-ttu-id="14001-159">Wenn ein Bereich groß ist, kann es vorkommen, dass der Bereich mithilfe von [jetgetrecordposition](./jetgetrecordposition-function.md)in einer näherten Weise gezählt wird.</span><span class="sxs-lookup"><span data-stu-id="14001-159">If a range is large, then it might be possible to count the range in an approximated fashion using [JetGetRecordPosition](./jetgetrecordposition-function.md).</span></span>

<span data-ttu-id="14001-160">**Windows XP, Windows Server 2003, Windows 2000 Server und Windows 2000 Professional:**  Wenn der Cursor auf einem leeren Index oder Index Bereich positioniert ist, gibt **jetindexrecordcount** irrtümlich JET_errNoCurrentRecord zurück, anstatt eine Daten Satz Anzahl von 0 (null) zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="14001-160">**Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:**  If the cursor is positioned on an empty index or index range then **JetIndexRecordCount** erroneously returns JET_errNoCurrentRecord rather than returning a record count of zero.</span></span> <span data-ttu-id="14001-161">Die Anwendung sollte überprüfen, ob der Index-oder Index Bereich in diesem Fall leer ist.</span><span class="sxs-lookup"><span data-stu-id="14001-161">The application should check to see if the index or index range is empty in this case.</span></span>

#### <a name="requirements"></a><span data-ttu-id="14001-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14001-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14001-163"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="14001-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="14001-164">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="14001-164">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14001-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="14001-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="14001-166">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="14001-166">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14001-167"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="14001-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="14001-168">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="14001-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14001-169"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="14001-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="14001-170">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="14001-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14001-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="14001-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="14001-172">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="14001-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="14001-173">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14001-173">See Also</span></span>

[<span data-ttu-id="14001-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="14001-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="14001-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="14001-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="14001-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="14001-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="14001-177">Jetgetrecordposition</span><span class="sxs-lookup"><span data-stu-id="14001-177">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="14001-178">Jetsetindexrange</span><span class="sxs-lookup"><span data-stu-id="14001-178">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="14001-179">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="14001-179">JetStopService</span></span>](./jetstopservice-function.md)
