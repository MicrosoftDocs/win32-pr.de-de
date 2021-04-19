---
description: 'Weitere Informationen zu: jetgojebookmark-Funktion'
title: Jetgoto Bookmark-Funktion
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 89dde261648b396bcfc9532911c0d4acd3c88828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364238"
---
# <a name="jetgotobookmark-function"></a><span data-ttu-id="4bcbf-103">Jetgoto Bookmark-Funktion</span><span class="sxs-lookup"><span data-stu-id="4bcbf-103">JetGotoBookmark Function</span></span>


<span data-ttu-id="4bcbf-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4bcbf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotobookmark-function"></a><span data-ttu-id="4bcbf-105">Jetgoto Bookmark-Funktion</span><span class="sxs-lookup"><span data-stu-id="4bcbf-105">JetGotoBookmark Function</span></span>

<span data-ttu-id="4bcbf-106">Die **jetgoatbookmark** -Funktion positioniert einen Cursor auf einen Index Eintrag für den Datensatz, der dem angegebenen Lesezeichen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-106">The **JetGotoBookmark** function positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="4bcbf-107">Das Lesezeichen kann mit jedem für eine Tabelle definierten Index verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-107">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="4bcbf-108">Das Lesezeichen für einen Datensatz kann mit [jetgetbookmark](./jetgetbookmark-function.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-108">The bookmark for a record can be retrieved using [JetGetBookmark](./jetgetbookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a><span data-ttu-id="4bcbf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bcbf-109">Parameters</span></span>

<span data-ttu-id="4bcbf-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="4bcbf-110">*sesid*</span></span>

<span data-ttu-id="4bcbf-111">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-111">The session to use for this call.</span></span>

<span data-ttu-id="4bcbf-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="4bcbf-112">*tableid*</span></span>

<span data-ttu-id="4bcbf-113">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-113">The cursor to use for this call.</span></span>

<span data-ttu-id="4bcbf-114">*pvbookmark*</span><span class="sxs-lookup"><span data-stu-id="4bcbf-114">*pvBookmark*</span></span>

<span data-ttu-id="4bcbf-115">Der Puffer, der das Lesezeichen enthält, das zum Positionieren des Cursors verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-115">The buffer that contains the bookmark to use to position the cursor.</span></span>

<span data-ttu-id="4bcbf-116">*cbbookmark*</span><span class="sxs-lookup"><span data-stu-id="4bcbf-116">*cbBookmark*</span></span>

<span data-ttu-id="4bcbf-117">Die Größe des Lesezeichens im Puffer.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-117">The size of the bookmark in the buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="4bcbf-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4bcbf-118">Return Value</span></span>

<span data-ttu-id="4bcbf-119">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4bcbf-120">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4bcbf-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4bcbf-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4bcbf-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="4bcbf-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bcbf-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bcbf-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4bcbf-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4bcbf-124">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bcbf-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4bcbf-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4bcbf-126">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bcbf-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4bcbf-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4bcbf-128">Der Vorgang kann nicht ausgeführt werden, da der-Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten gesperrt wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-128">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="4bcbf-129"><strong>Windows XP:</strong>   Dieser Rückgabewert wurde in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-129"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bcbf-130">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="4bcbf-130">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="4bcbf-131">Das angegebene Lesezeichen ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-131">The bookmark that was provided is invalid.</span></span> <span data-ttu-id="4bcbf-132">Dieser Fehler ist möglicherweise aufgetreten, weil die Größe des Lesezeichens 0 (null) ist oder der Lesezeichen-Puffer Zeiger <strong>null</strong>ist.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-132">This might have occurred because the size of the bookmark is zero or the bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bcbf-133">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="4bcbf-133">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="4bcbf-134">Der Cursor befindet sich auf einem sekundären Index, und für den Datensatz, der dem Lesezeichen zugeordnet ist, wurde kein Index Eintrag gefunden.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-134">The cursor is on a secondary index and no index entry could be found for the record that is associated with the bookmark.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bcbf-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4bcbf-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4bcbf-136">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-136">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bcbf-137">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="4bcbf-137">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="4bcbf-138">Der Datensatz, der dem Lesezeichen zugeordnet ist, konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-138">The record that is associated with the bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bcbf-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4bcbf-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4bcbf-140">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-140">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bcbf-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4bcbf-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4bcbf-142">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-142">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="4bcbf-143"><strong>Windows XP:</strong>   Dieser Rückgabewert wurde in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-143"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bcbf-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4bcbf-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4bcbf-145">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-145">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4bcbf-146">Wenn diese Funktion erfolgreich ausgeführt wird, wird der Cursor an einem Index Eintrag für den Datensatz positioniert, der dem angegebenen Lesezeichen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-146">If this function succeeds, the cursor will be positioned at an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="4bcbf-147">Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-147">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="4bcbf-148">Wenn ein Index Bereich wirksam ist, wird dieser Index Bereich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-148">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="4bcbf-149">Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-149">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="4bcbf-150">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-150">No change to the database state will occur.</span></span>

<span data-ttu-id="4bcbf-151">Wenn diese Funktion fehlschlägt, bleibt die Position des Cursors unverändert.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-151">If this function fails, the position of the cursor will remain unchanged.</span></span> <span data-ttu-id="4bcbf-152">Wenn ein Datensatz für die Aktualisierung vorbereitet wurde, wird das Update abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-152">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="4bcbf-153">Wenn ein Index Bereich wirksam ist, wird dieser Index Bereich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-153">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="4bcbf-154">Wenn ein Suchschlüssel für den Cursor erstellt wurde, wird der Suchschlüssel gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-154">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="4bcbf-155">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4bcbf-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bcbf-156">Remarks</span></span>

<span data-ttu-id="4bcbf-157">Es gibt zwei Möglichkeiten, ein Lesezeichen zu verwenden, um einen Cursor auf einem Index zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-157">There are two ways to use a bookmark to position a cursor on an index.</span></span> <span data-ttu-id="4bcbf-158">Der erste besteht darin, das Lesezeichen zu verwenden, um den Datensatz direkt zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-158">The first is to use the bookmark to position on the record directly.</span></span> <span data-ttu-id="4bcbf-159">Dies tritt auf, wenn der aktuelle Index des Cursors der primäre Index ist.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-159">This occurs when the current index of the cursor is the primary index.</span></span> <span data-ttu-id="4bcbf-160">Diese Technik funktioniert, weil ein ESENT-Lesezeichen mit dem Primärschlüssel des zugehörigen Datensatzes identisch ist.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-160">This technique works because an ESENT bookmark is the same as the associated record's primary key.</span></span>

<span data-ttu-id="4bcbf-161">Die zweite Möglichkeit zur Verwendung eines Lesezeichens besteht darin, es in einem Eintrag in einem sekundären Index zu positionieren, der dem Datensatz entspricht, der diesem Lesezeichen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-161">The second way to use a bookmark is to position it on an entry in a secondary index that corresponds to the record that is associated with that bookmark.</span></span> <span data-ttu-id="4bcbf-162">Während dieses Vorgangs sucht die Engine den tatsächlichen Datensatz mit dem Lesezeichen auf dem primären Index.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-162">During this process, the engine looks up the actual record using the bookmark on the primary index.</span></span> <span data-ttu-id="4bcbf-163">Anschließend werden die Daten Satz Daten und die sekundäre Index Definition verwendet, um einen Schlüssel in den sekundären Index zu berechnen, der auf den Datensatz verweist.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-163">It then uses the record data and the secondary index definition to compute a key into the secondary index that points to the record.</span></span> <span data-ttu-id="4bcbf-164">Anschließend positioniert Sie den Cursor auf dem Index Eintrag für diesen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-164">It then positions the cursor on the index entry for that key.</span></span> <span data-ttu-id="4bcbf-165">Wenn sich der Cursor aktuell auf einem sekundären Index über eine oder mehrere mehrwertige Schlüssel Spalten befindet, wird der Cursor auf dem Index Eintrag positioniert, der dem ersten mehrwertigen Wert der einzelnen Schlüssel Spalten entspricht.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-165">If the cursor is currently on a secondary index over one or more multi-valued key columns, the cursor will be positioned on the index entry corresponding to the first multi-value of each of those key columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4bcbf-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bcbf-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bcbf-167"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="4bcbf-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4bcbf-168">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bcbf-169"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4bcbf-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4bcbf-170">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bcbf-171"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4bcbf-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4bcbf-172">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bcbf-173"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="4bcbf-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4bcbf-174">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bcbf-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4bcbf-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4bcbf-176">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4bcbf-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4bcbf-177">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4bcbf-177">See Also</span></span>

[<span data-ttu-id="4bcbf-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4bcbf-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4bcbf-179">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4bcbf-179">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4bcbf-180">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4bcbf-180">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4bcbf-181">Jetgetbookmark</span><span class="sxs-lookup"><span data-stu-id="4bcbf-181">JetGetBookmark</span></span>](./jetgetbookmark-function.md)
