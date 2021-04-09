---
description: Weitere Informationen finden Sie in der jetgetrecordsize-Funktion
title: Jetgetrecordsize-Funktion
TOCTitle: JetGetRecordSize Function
ms:assetid: a28567ed-c732-4509-9f8d-6f8104f62a86
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294045(v=EXCHG.10)
ms:contentKeyID: 32765644
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 255ca71f3b57c0d1f1bc8440a9a6d4697c09c670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960296"
---
# <a name="jetgetrecordsize-function"></a><span data-ttu-id="7c7a5-103">Jetgetrecordsize-Funktion</span><span class="sxs-lookup"><span data-stu-id="7c7a5-103">JetGetRecordSize Function</span></span>


<span data-ttu-id="7c7a5-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7c7a5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordsize-function"></a><span data-ttu-id="7c7a5-105">Jetgetrecordsize-Funktion</span><span class="sxs-lookup"><span data-stu-id="7c7a5-105">JetGetRecordSize Function</span></span>

<span data-ttu-id="7c7a5-106">Die **jetgetrecordsize** -Funktion Ruft Informationen zur Daten Satz Größe vom gewünschten Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-106">The **JetGetRecordSize** function retrieves record size information from the desired location.</span></span>

<span data-ttu-id="7c7a5-107">**Windows Vista: jetgetrecordsize** wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-107">**Windows Vista:  JetGetRecordSize** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordSize(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="7c7a5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c7a5-108">Parameters</span></span>

<span data-ttu-id="7c7a5-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="7c7a5-109">*sesid*</span></span>

<span data-ttu-id="7c7a5-110">Identifiziert den Daten Bank Sitzungs Kontext, der für den API-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="7c7a5-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="7c7a5-111">*tableid*</span></span>

<span data-ttu-id="7c7a5-112">Identifiziert die Tabelle oder den Cursor, die für den API-Befehl verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-112">Identifies the table or cursor that will be used for the API call.</span></span> <span data-ttu-id="7c7a5-113">Der Cursor muss auf einem Datensatz positioniert werden, oder es muss ein Update vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-113">The cursor must be positioned on a record, or have an update prepared.</span></span>

<span data-ttu-id="7c7a5-114">*prägrößengröße*</span><span class="sxs-lookup"><span data-stu-id="7c7a5-114">*precsize*</span></span>

<span data-ttu-id="7c7a5-115">Ein Zeiger auf einen Ausgabepuffer für die [JET_RECSIZE](./jet-recsize-structure.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-115">A pointer to an output buffer for the [JET_RECSIZE](./jet-recsize-structure.md) structure.</span></span>

<span data-ttu-id="7c7a5-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="7c7a5-116">*grbit*</span></span>

<span data-ttu-id="7c7a5-117">Dabei handelt es sich um einen oder mehrere der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-117">This is one or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c7a5-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7c7a5-118">Value</span></span></p></th>
<th><p><span data-ttu-id="7c7a5-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7c7a5-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c7a5-120">JET_bitRecordSizeInCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="7c7a5-120">JET_bitRecordSizeInCopyBuffer</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-121">Dadurch wird die Größe des Datensatzes abgerufen, der sich im Kopier Puffer befindet, der für das Update vorbereitet wurde.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-121">This retrieves the size of the record that is in the copy buffer prepared for update.</span></span> <span data-ttu-id="7c7a5-122">Andernfalls muss <em>TableID</em> oder Cursor auf einem Datensatz positioniert werden, und dieser Datensatz wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-122">Otherwise, the <em>tableid</em> or cursor must be positioned on a record, and that record will be used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7a5-123">JET_bitRecordSizeRunningTotal</span><span class="sxs-lookup"><span data-stu-id="7c7a5-123">JET_bitRecordSizeRunningTotal</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-124">Wenn dieses Bit festgelegt ist, wird das <a href="gg294072(v=exchg.10).md">JET_RECSIZE</a> vor dem Ausfüllen des Inhalts nicht mit nullte versehen, was effektiv als Ansammlung der Statistiken für mehrere besuchte oder aktualisierte Datensätze fungiert.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-124">When this bit is specified, the <a href="gg294072(v=exchg.10).md">JET_RECSIZE</a> is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c7a5-125">JET_bitRecordSizeLocal</span><span class="sxs-lookup"><span data-stu-id="7c7a5-125">JET_bitRecordSizeLocal</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-126">Dies bewirkt, dass die API nicht intrinsische Long-Werte ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-126">This causes the API to ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="7c7a5-127">Beispielsweise wird nur der lokale Datensatz auf der Seite verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-127">For example, only the local record on the page will be used.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="7c7a5-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c7a5-128">Return Value</span></span>

<span data-ttu-id="7c7a5-129">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7c7a5-130">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7c7a5-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c7a5-131">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7c7a5-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="7c7a5-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c7a5-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c7a5-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7c7a5-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-134">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7a5-135">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="7c7a5-135">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-136">Eine der angeforderten Optionen war ungültig oder nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-136">One of the requested options was invalid or not implemented.</span></span> <span data-ttu-id="7c7a5-137">Dieser Fehler wird von der <strong>jetgetrecordsize</strong> -Funktion zurückgegeben, wenn ein ungültiges <em>grbit</em> angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-137">This error will be returned by the <strong>JetGetRecordSize</strong> function when an illegal <em>grbit</em> is specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c7a5-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="7c7a5-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-139">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-139">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7a5-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="7c7a5-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-141">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c7a5-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="7c7a5-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-143">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="7c7a5-144"><strong>Windows XP:</strong>  JET_errInstanceUnavailable werden nur von Versionen von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-144"><strong>Windows XP:</strong>  JET_errInstanceUnavailable will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7a5-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="7c7a5-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-146">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-146">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c7a5-147">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="7c7a5-147">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-148">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-148">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7a5-149">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="7c7a5-149">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-150">Es ist nicht zulässig, dieselbe Sitzung von mehr als einem Thread gleichzeitig zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-150">It is illegal to use the same session from more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="7c7a5-151"><strong>Windows XP:</strong>  JET_errInstanceUnavailable werden nur von Versionen von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-151"><strong>Windows XP:</strong>  JET_errInstanceUnavailable will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c7a5-152">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="7c7a5-152">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-153">Dies kann vorkommen, wenn der Cursor falsch positioniert wurde.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-153">This can happen if the cursor was positioned incorrectly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7a5-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="7c7a5-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-155">Wenn der Cursor nicht in einer Transaktion positioniert war, kann dies vorkommen, wenn der Datensatz von einem anderen Thread aus in dieser Sitzung gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-155">If the cursor was not positioned in a transaction, this can happen if another thread deletes the record out from under this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c7a5-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7c7a5-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7c7a5-157">Dies kann zurückgegeben werden, wenn eine <strong>null</strong>-<em>prägrößengröße</em> überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-157">This can be returned if a <strong>NULL</strong><em>precsize</em> was passed.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="7c7a5-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c7a5-158">Remarks</span></span>

<span data-ttu-id="7c7a5-159">Die Größe des Schlüssels, der im **cboverhead** -Feld von [JET_RECSIZE](./jet-recsize-structure.md)akkumuliert wurde, ist von JET_bitRecordSizeInCopyBuffer betroffen.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-159">The size of the key accumulated in the **cbOverhead** field of [JET_RECSIZE](./jet-recsize-structure.md), is affected by JET_bitRecordSizeInCopyBuffer.</span></span> <span data-ttu-id="7c7a5-160">Wenn dieses Bit angegeben ist, ist die Schlüsselgröße, die im Feld **cboverhead** akkumuliert wurde, die vollständige Schlüsselgröße.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-160">If this bit is specified, the key size accumulated in the **cbOverhead** field is the full key size.</span></span> <span data-ttu-id="7c7a5-161">Wenn dieses Bit nicht verwendet wird, enthält die akkumulierte Schlüsselgröße keine Größe, die aufgrund der Schlüssel Präfix Komprimierung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-161">If this bit is not used, then the key size accumulated will not include any size saved due to key prefix compression.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7c7a5-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c7a5-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c7a5-163"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7c7a5-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7c7a5-164">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-164">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7a5-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7c7a5-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7c7a5-166">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-166">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c7a5-167"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7c7a5-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7c7a5-168">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7a5-169"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="7c7a5-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7c7a5-170">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c7a5-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7c7a5-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7c7a5-172">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7c7a5-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7c7a5-173">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7c7a5-173">See Also</span></span>

[<span data-ttu-id="7c7a5-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7c7a5-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7c7a5-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7c7a5-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7c7a5-176">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7c7a5-176">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7c7a5-177">JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="7c7a5-177">JET_RECSIZE</span></span>](./jet-recsize-structure.md)  
[<span data-ttu-id="7c7a5-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7c7a5-178">JET_TABLEID</span></span>](./jet-tableid.md)
