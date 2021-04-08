---
description: Weitere Informationen finden Sie in der jetgoto secondaryindexbookmark-Funktion
title: Jetgoto secondaryindexbookmark-Funktion
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893833fd1770fe3d972033a4d10f9047b0f61dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959899"
---
# <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="01273-103">Jetgoto secondaryindexbookmark-Funktion</span><span class="sxs-lookup"><span data-stu-id="01273-103">JetGotoSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="01273-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="01273-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="01273-105">Jetgoto secondaryindexbookmark-Funktion</span><span class="sxs-lookup"><span data-stu-id="01273-105">JetGotoSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="01273-106">Die **jetgoto secondaryindexbookmark** -Funktion positioniert einen Cursor auf einen Index Eintrag, der dem angegebenen sekundären Index Lesezeichen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="01273-106">The **JetGotoSecondaryIndexBookmark** function positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="01273-107">Das sekundäre Index Lesezeichen muss mit demselben Index für dieselbe Tabelle verwendet werden, aus der es ursprünglich abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="01273-107">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="01273-108">Das sekundäre Index Lesezeichen für einen Index Eintrag kann mithilfe von **jetgoysecondaryindexbookmark** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="01273-108">The secondary index bookmark for an index entry can be retrieved using **JetGotoSecondaryIndexBookmark**.</span></span>

<span data-ttu-id="01273-109">**Windows XP:**  **jetgodesecondaryindexbookmark** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="01273-109">**Windows XP:**  **JetGotoSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="01273-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="01273-110">Parameters</span></span>

<span data-ttu-id="01273-111">*-sid*</span><span class="sxs-lookup"><span data-stu-id="01273-111">*sesid*</span></span>

<span data-ttu-id="01273-112">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01273-112">The session to use for this call.</span></span>

<span data-ttu-id="01273-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="01273-113">*tableid*</span></span>

<span data-ttu-id="01273-114">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01273-114">The cursor to use for this call.</span></span>

<span data-ttu-id="01273-115">*pvsecondarykey*</span><span class="sxs-lookup"><span data-stu-id="01273-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="01273-116">Der Puffer, der den sekundären Schlüssel enthält, der zum Positionieren des Cursors verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01273-116">The buffer that contains the secondary key to use to position the cursor.</span></span>

<span data-ttu-id="01273-117">*cbsecondarykey*</span><span class="sxs-lookup"><span data-stu-id="01273-117">*cbSecondaryKey*</span></span>

<span data-ttu-id="01273-118">Die Größe des sekundären Schlüssels im Puffer.</span><span class="sxs-lookup"><span data-stu-id="01273-118">The size of the secondary key in the buffer.</span></span>

<span data-ttu-id="01273-119">*pvprimarybookmark*</span><span class="sxs-lookup"><span data-stu-id="01273-119">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="01273-120">Der Puffer, der das Primärschlüssel-Lesezeichen enthält, das zum Positionieren des Cursors verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01273-120">The buffer that contains the primary key bookmark to use to position the cursor.</span></span>

<span data-ttu-id="01273-121">*cbprimarybookmark*</span><span class="sxs-lookup"><span data-stu-id="01273-121">*cbPrimaryBookmark*</span></span>

<span data-ttu-id="01273-122">Die Größe des Primärschlüssel-Lesezeichens im Puffer.</span><span class="sxs-lookup"><span data-stu-id="01273-122">The size of the primary key bookmark in the buffer.</span></span>

<span data-ttu-id="01273-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="01273-123">*grbit*</span></span>

<span data-ttu-id="01273-124">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="01273-124">A group of bits that specifies zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="01273-125">Wert</span><span class="sxs-lookup"><span data-stu-id="01273-125">Value</span></span></p></th>
<th><p><span data-ttu-id="01273-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="01273-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01273-127">JET_bitBookmarkPermitVirtualCurrency</span><span class="sxs-lookup"><span data-stu-id="01273-127">JET_bitBookmarkPermitVirtualCurrency</span></span></p></td>
<td><p><span data-ttu-id="01273-128">Wenn der Index Eintrag nicht mehr gefunden werden kann, wird der Cursor positioniert, wo der Index Eintrag bereits gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="01273-128">In the event that the index entry can no longer be found, the cursor will be left positioned where that index entry was previously found.</span></span> <span data-ttu-id="01273-129">Der Vorgang schlägt weiterhin mit JET_errRecordDeleted fehl. Es ist jedoch möglich, zum nächsten oder vorherigen Index Eintrag relativ zum Index Eintrag zu wechseln, der jetzt fehlt.</span><span class="sxs-lookup"><span data-stu-id="01273-129">The operation will still fail with JET_errRecordDeleted; however, it will be possible to move to the next or previous index entry relative to the index entry that is now missing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="01273-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01273-130">Return Value</span></span>

<span data-ttu-id="01273-131">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="01273-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="01273-132">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="01273-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="01273-133">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="01273-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="01273-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01273-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01273-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="01273-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="01273-136">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="01273-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01273-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="01273-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="01273-138">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="01273-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01273-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="01273-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="01273-140">Der Vorgang kann nicht durchgeführt werden, weil die-Instanz, die der Sitzung zugeordnet ist, einen schwerwiegenden Fehler festgestellt hat, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="01273-140">The operation cannot complete because is because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="01273-141"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="01273-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01273-142">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="01273-142">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="01273-143">Das angegebene sekundäre Index Textzeichen ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="01273-143">The secondary index bookmark that was provided was invalid.</span></span> <span data-ttu-id="01273-144">Dieser Fehler ist möglicherweise aufgetreten, weil der sekundäre Schlüssel NULL ist oder der Sekundär Schlüsselpuffer Zeiger <strong>null</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="01273-144">This error might have occurred because the secondary key is zero or the secondary key buffer pointer is <strong>NULL</strong>.</span></span> <span data-ttu-id="01273-145">Dieser Fehler tritt auf, weil</span><span class="sxs-lookup"><span data-stu-id="01273-145">This error occurs because</span></span></p>
<ul>
<li><p><span data-ttu-id="01273-146">Der aktuelle sekundäre Index verfügt nicht über eine Unique-Einschränkung, und die Größe des bereitgestellten Lesezeichens ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="01273-146">The current secondary index does not have a uniqueness constraint and the size of the provided bookmark is zero.</span></span></p></li>
<li><p><span data-ttu-id="01273-147">Der Lesezeichen-Puffer Zeiger ist <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="01273-147">The bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01273-148">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="01273-148">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="01273-149">Der Cursor befindet sich derzeit nicht auf einem sekundären Index.</span><span class="sxs-lookup"><span data-stu-id="01273-149">The cursor is not currently on a secondary index.</span></span> <span data-ttu-id="01273-150">Es ist nicht sinnvoll, zu einem sekundären Index Lesezeichen zu wechseln, wenn der Cursor aktuell keinen sekundären Index verwendet.</span><span class="sxs-lookup"><span data-stu-id="01273-150">It is not meaningful to go to a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="01273-151"><a href="gg294053(v=exchg.10).md">Jetgojebookmark</a> sollte verwendet werden, wenn sich der Cursor nicht auf einem sekundären Index befindet.</span><span class="sxs-lookup"><span data-stu-id="01273-151"><a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01273-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="01273-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="01273-153">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="01273-153">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01273-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="01273-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="01273-155">Der Index Eintrag, der dem sekundären Index Lesezeichen zugeordnet ist, wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="01273-155">The index entry that is associated with the secondary index bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01273-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="01273-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="01273-157">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01273-157">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01273-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="01273-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="01273-159">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01273-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="01273-160"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="01273-160"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01273-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="01273-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="01273-162">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="01273-162">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="01273-163">Wenn diese Funktion erfolgreich ausgeführt wird, wird der Cursor an einem Index Eintrag positioniert, der dem angegebenen sekundären Index Lesezeichen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="01273-163">If this function succeeds, the cursor will be positioned at an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="01273-164">Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="01273-164">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="01273-165">Wenn ein Index Bereich wirksam ist, wird dieser Index Bereich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="01273-165">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="01273-166">Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="01273-166">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="01273-167">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="01273-167">No change to the database state will occur.</span></span>

<span data-ttu-id="01273-168">Wenn diese Funktion fehlschlägt, bleibt die Position des Cursors unverändert, es sei denn, JET_errRecordDeleted zurückgegeben und JET_bitBookmarkPermitVirtualCurrency angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="01273-168">If this function fails, the position of the cursor remains unchanged unless JET_errRecordDeleted is returned and JET_bitBookmarkPermitVirtualCurrency is specified.</span></span> <span data-ttu-id="01273-169">In diesem Fall wird der Cursor positioniert, wo der Index Eintrag, der dem angegebenen sekundären Index Textzeichen zugeordnet ist, wäre.</span><span class="sxs-lookup"><span data-stu-id="01273-169">In that case, the cursor will be positioned where the index entry that is associated with the specified secondary index bookmark would have been.</span></span> <span data-ttu-id="01273-170">Der Cursor kann relativ zu dieser Position verschoben werden, befindet sich jedoch noch nicht in einem gültigen Index Eintrag.</span><span class="sxs-lookup"><span data-stu-id="01273-170">The cursor can be moved relative to that position, but is still not on a valid index entry.</span></span>

<span data-ttu-id="01273-171">Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="01273-171">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="01273-172">Wenn ein Index Bereich wirksam ist, wird dieser Index Bereich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="01273-172">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="01273-173">Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="01273-173">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="01273-174">In jedem Fall erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="01273-174">In any case, no change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="01273-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01273-175">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01273-176"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="01273-176"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="01273-177">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="01273-177">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01273-178"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="01273-178"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="01273-179">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="01273-179">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01273-180"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="01273-180"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="01273-181">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="01273-181">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01273-182"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="01273-182"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="01273-183">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="01273-183">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01273-184"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="01273-184"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="01273-185">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="01273-185">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="01273-186">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="01273-186">See Also</span></span>

[<span data-ttu-id="01273-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="01273-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="01273-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="01273-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="01273-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="01273-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="01273-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="01273-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="01273-191">Jetgetsecondaryindexbookmark</span><span class="sxs-lookup"><span data-stu-id="01273-191">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)  
[<span data-ttu-id="01273-192">Jetgojebookmark</span><span class="sxs-lookup"><span data-stu-id="01273-192">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="01273-193">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="01273-193">JetStopService</span></span>](./jetstopservice-function.md)
