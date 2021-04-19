---
description: 'Weitere Informationen finden Sie hier: JetGetRecordSize2-Funktion'
title: JetGetRecordSize2-Funktion
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c68eafaaa53b5b88e6b003bdbafce287035cbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363016"
---
# <a name="jetgetrecordsize2-function"></a><span data-ttu-id="28f2b-103">JetGetRecordSize2-Funktion</span><span class="sxs-lookup"><span data-stu-id="28f2b-103">JetGetRecordSize2 Function</span></span>


<span data-ttu-id="28f2b-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="28f2b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordsize2-function"></a><span data-ttu-id="28f2b-105">JetGetRecordSize2-Funktion</span><span class="sxs-lookup"><span data-stu-id="28f2b-105">JetGetRecordSize2 Function</span></span>

<span data-ttu-id="28f2b-106">Die **JetGetRecordSize2** -Funktion Ruft Informationen zur Daten Satz Größe vom gewünschten Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="28f2b-106">The **JetGetRecordSize2** function retrieves record size information from the desired location.</span></span>

<span data-ttu-id="28f2b-107">**Windows 7: JetGetRecordSize2** wird im Betriebssystem Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="28f2b-107">**Windows 7:  JetGetRecordSize2** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="28f2b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="28f2b-108">Parameters</span></span>

<span data-ttu-id="28f2b-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="28f2b-109">*sesid*</span></span>

<span data-ttu-id="28f2b-110">Identifiziert den Daten Bank Sitzungs Kontext, der für den API-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="28f2b-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="28f2b-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="28f2b-111">*tableid*</span></span>

<span data-ttu-id="28f2b-112">Identifiziert die Tabelle oder den Cursor, die für den API-Befehl verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28f2b-112">Identifies the table or cursor that will be used for the API call.</span></span> <span data-ttu-id="28f2b-113">Der Cursor muss auf einem Datensatz positioniert werden, oder es muss ein Update vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="28f2b-113">The cursor must be positioned on a record, or have an update prepared.</span></span>

<span data-ttu-id="28f2b-114">*prägrößengröße*</span><span class="sxs-lookup"><span data-stu-id="28f2b-114">*precsize*</span></span>

<span data-ttu-id="28f2b-115">Ein Zeiger auf einen Ausgabepuffer für die [JET_RECSIZE2](./jet-recsize2-structure.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="28f2b-115">A pointer to an output buffer for the [JET_RECSIZE2](./jet-recsize2-structure.md) structure.</span></span>

<span data-ttu-id="28f2b-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="28f2b-116">*grbit*</span></span>

<span data-ttu-id="28f2b-117">Dabei handelt es sich um einen oder mehrere der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="28f2b-117">This is one or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28f2b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="28f2b-118">Value</span></span></p></th>
<th><p><span data-ttu-id="28f2b-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="28f2b-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28f2b-120">JET_bitRecordSizeInCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="28f2b-120">JET_bitRecordSizeInCopyBuffer</span></span></p></td>
<td><p><span data-ttu-id="28f2b-121">Dadurch wird die Größe des Datensatzes abgerufen, der sich im Kopier Puffer befindet, der für das Update vorbereitet wurde.</span><span class="sxs-lookup"><span data-stu-id="28f2b-121">This retrieves the size of the record that is in the copy buffer prepared for update.</span></span> <span data-ttu-id="28f2b-122">Andernfalls muss <em>TableID</em> oder Cursor auf einem Datensatz positioniert werden, und dieser Datensatz wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="28f2b-122">Otherwise, the <em>tableid</em> or cursor must be positioned on a record, and that record will be used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28f2b-123">JET_bitRecordSizeRunningTotal</span><span class="sxs-lookup"><span data-stu-id="28f2b-123">JET_bitRecordSizeRunningTotal</span></span></p></td>
<td><p><span data-ttu-id="28f2b-124">Wenn dieses Bit festgelegt ist, wird das <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> vor dem Ausfüllen des Inhalts nicht mit nullte versehen, was effektiv als Ansammlung der Statistiken für mehrere besuchte oder aktualisierte Datensätze fungiert.</span><span class="sxs-lookup"><span data-stu-id="28f2b-124">When this bit is specified, the <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28f2b-125">JET_bitRecordSizeLocal</span><span class="sxs-lookup"><span data-stu-id="28f2b-125">JET_bitRecordSizeLocal</span></span></p></td>
<td><p><span data-ttu-id="28f2b-126">Dies bewirkt, dass die API nicht intrinsische Long-Werte ignoriert.</span><span class="sxs-lookup"><span data-stu-id="28f2b-126">This causes the API to ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="28f2b-127">Beispielsweise wird nur der lokale Datensatz auf der Seite verwendet.</span><span class="sxs-lookup"><span data-stu-id="28f2b-127">For example, only the local record on the page will be used.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="28f2b-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28f2b-128">Return Value</span></span>

<span data-ttu-id="28f2b-129">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="28f2b-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="28f2b-130">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="28f2b-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28f2b-131">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="28f2b-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="28f2b-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28f2b-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28f2b-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="28f2b-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="28f2b-134">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="28f2b-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28f2b-135">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="28f2b-135">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="28f2b-136">Eine der angeforderten Optionen war ungültig oder nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="28f2b-136">One of the requested options was invalid or not implemented.</span></span> <span data-ttu-id="28f2b-137">Dieser Fehler wird von der <strong>JetGetRecordSize2</strong> -Funktion zurückgegeben, wenn ein ungültiges <em>grbit</em> angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="28f2b-137">This error will be returned by the <strong>JetGetRecordSize2</strong> function when an illegal <em>grbit</em> is specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28f2b-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="28f2b-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="28f2b-139">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="28f2b-139">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28f2b-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="28f2b-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="28f2b-141">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="28f2b-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28f2b-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="28f2b-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="28f2b-143">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="28f2b-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="28f2b-144"><strong>Windows XP:  </strong> JET_errInstanceUnavailable werden nur vom Betriebssystem Windows XP und höheren Versionen von Windows zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="28f2b-144"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by the Windows XP operating system and later versions of Windows.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28f2b-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="28f2b-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="28f2b-146">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="28f2b-146">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28f2b-147">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="28f2b-147">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="28f2b-148">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28f2b-148">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28f2b-149">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="28f2b-149">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="28f2b-150">Es ist nicht zulässig, dieselbe Sitzung für mehr als einen Thread gleichzeitig zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="28f2b-150">It is illegal to use the same session for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="28f2b-151"><strong>Windows XP:  </strong> JET_errInstanceUnavailable werden nur von Windows XP und höheren Versionen von Windows zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="28f2b-151"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by Windows XP and later versions of Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28f2b-152">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="28f2b-152">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="28f2b-153">Dies kann vorkommen, wenn der Cursor falsch positioniert wurde.</span><span class="sxs-lookup"><span data-stu-id="28f2b-153">This can happen if the cursor was positioned incorrectly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28f2b-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="28f2b-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="28f2b-155">Wenn der Cursor nicht in einer Transaktion positioniert war, kann dies vorkommen, wenn der Datensatz von einem anderen Thread aus in dieser Sitzung gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="28f2b-155">If the cursor was not positioned in a transaction, this can happen if another thread deletes the record out from under this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28f2b-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="28f2b-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="28f2b-157">Dies kann zurückgegeben werden, wenn eine <strong>null</strong>-<em>prägrößengröße</em> überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="28f2b-157">This can be returned if a <strong>NULL</strong><em>precsize</em> was passed.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="28f2b-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28f2b-158">Remarks</span></span>

<span data-ttu-id="28f2b-159">Die Größe des Schlüssels, der im **cboverhead** -Feld von [JET_RECSIZE2](./jet-recsize2-structure.md)akkumuliert wurde, ist von JET_bitRecordSizeInCopyBuffer betroffen.</span><span class="sxs-lookup"><span data-stu-id="28f2b-159">The size of the key accumulated in the **cbOverhead** field of [JET_RECSIZE2](./jet-recsize2-structure.md), is affected by JET_bitRecordSizeInCopyBuffer.</span></span> <span data-ttu-id="28f2b-160">Wenn dieses Bit angegeben ist, ist die Schlüsselgröße, die im Feld **cboverhead** akkumuliert wurde, die vollständige Schlüsselgröße.</span><span class="sxs-lookup"><span data-stu-id="28f2b-160">If this bit is specified, the key size accumulated in the **cbOverhead** field is the full key size.</span></span> <span data-ttu-id="28f2b-161">Wenn dieses Bit nicht verwendet wird, enthält die akkumulierte Schlüsselgröße keine Größe, die aufgrund der Schlüssel Präfix Komprimierung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="28f2b-161">If this bit is not used, the key size accumulated will not include any size saved due to key prefix compression.</span></span>

#### <a name="requirements"></a><span data-ttu-id="28f2b-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28f2b-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28f2b-163"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="28f2b-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="28f2b-164">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="28f2b-164">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28f2b-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="28f2b-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="28f2b-166">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="28f2b-166">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28f2b-167"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="28f2b-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="28f2b-168">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="28f2b-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28f2b-169"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="28f2b-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="28f2b-170">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="28f2b-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28f2b-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="28f2b-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="28f2b-172">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="28f2b-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="28f2b-173">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="28f2b-173">See Also</span></span>

[<span data-ttu-id="28f2b-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="28f2b-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="28f2b-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="28f2b-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="28f2b-176">JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="28f2b-176">JET_RECSIZE</span></span>](./jet-recsize-structure.md)  
[<span data-ttu-id="28f2b-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="28f2b-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="28f2b-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="28f2b-178">JET_TABLEID</span></span>](./jet-tableid.md)
