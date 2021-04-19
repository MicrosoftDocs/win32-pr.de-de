---
description: 'Weitere Informationen: jetgetcurrentindex-Funktion'
title: Jetgetcurrentindex-Funktion
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3337ddaefbea803a137ad8366d2e3df665bacd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363604"
---
# <a name="jetgetcurrentindex-function"></a><span data-ttu-id="8d489-103">Jetgetcurrentindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="8d489-103">JetGetCurrentIndex Function</span></span>


<span data-ttu-id="8d489-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8d489-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcurrentindex-function"></a><span data-ttu-id="8d489-105">Jetgetcurrentindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="8d489-105">JetGetCurrentIndex Function</span></span>

<span data-ttu-id="8d489-106">Die **jetgetcurrentindex** -Funktion bestimmt den Namen des aktuellen Indexes eines angegebenen Cursors.</span><span class="sxs-lookup"><span data-stu-id="8d489-106">The **JetGetCurrentIndex** function determines the name of the current index of a given cursor.</span></span> <span data-ttu-id="8d489-107">Dieser Name wird auch verwendet, um den Index später mithilfe von [jetsetcurrentindex](./jetsetcurrentindex-function.md)als aktuellen Index erneut auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="8d489-107">This name is also used to later re-select that index as the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="8d489-108">Sie kann auch verwendet werden, um die Eigenschaften dieses Indexes mithilfe von [jetgettableindexinfo](./jetgettableindexinfo-function.md)zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="8d489-108">It can also be used to discover the properties of that index using [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="8d489-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d489-109">Parameters</span></span>

<span data-ttu-id="8d489-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="8d489-110">*sesid*</span></span>

<span data-ttu-id="8d489-111">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d489-111">The session to use for this call.</span></span>

<span data-ttu-id="8d489-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="8d489-112">*tableid*</span></span>

<span data-ttu-id="8d489-113">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d489-113">The cursor to use for this call.</span></span>

<span data-ttu-id="8d489-114">*szindexname*</span><span class="sxs-lookup"><span data-stu-id="8d489-114">*szIndexName*</span></span>

<span data-ttu-id="8d489-115">Der Ausgabepuffer, der den Namen des aktuellen Index des Cursors empfängt.</span><span class="sxs-lookup"><span data-stu-id="8d489-115">The output buffer that receives the name of the current index of the cursor.</span></span>

<span data-ttu-id="8d489-116">*cchindexname*</span><span class="sxs-lookup"><span data-stu-id="8d489-116">*cchIndexName*</span></span>

<span data-ttu-id="8d489-117">Die maximale Größe des Ausgabepuffers in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8d489-117">The maximum size in characters of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="8d489-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d489-118">Return Value</span></span>

<span data-ttu-id="8d489-119">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="8d489-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8d489-120">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8d489-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d489-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8d489-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="8d489-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d489-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d489-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8d489-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8d489-124">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8d489-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d489-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8d489-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8d489-126">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="8d489-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d489-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8d489-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8d489-128">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="8d489-128">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="8d489-129">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d489-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d489-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8d489-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8d489-131">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8d489-131">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d489-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8d489-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8d489-133">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d489-133">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d489-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="8d489-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="8d489-135">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d489-135">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="8d489-136">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d489-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d489-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8d489-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8d489-138">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="8d489-138">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d489-139">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="8d489-139">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="8d489-140">Der Vorgang wurde erfolgreich abgeschlossen, aber der Ausgabepuffer war zu klein, um den gesamten Indexnamen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="8d489-140">The operation completed successfully, but the output buffer was too small to receive the entire index name.</span></span></p>
<p><span data-ttu-id="8d489-141">Der Ausgabepuffer wurde mit dem gleichen Namen wie der Indexname gefüllt.</span><span class="sxs-lookup"><span data-stu-id="8d489-141">The output buffer has been filled with as much of the index name as would fit.</span></span> <span data-ttu-id="8d489-142">Wenn der Ausgabepuffer mindestens ein Zeichen lang ist, wird die Zeichenfolge in diesem Ausgabepuffer Null beendet.</span><span class="sxs-lookup"><span data-stu-id="8d489-142">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="8d489-143"><strong>Hinweis  </strong> Dieser Fehler wird nicht zurückgegeben, wenn "cchindexname" 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="8d489-143"><strong>Note  </strong>This error will not be returned if cchIndexName is zero.</span></span> <span data-ttu-id="8d489-144">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="8d489-144">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d489-145">Bei Erfolg wird der Name des aktuellen Index des angegebenen Cursors im Ausgabepuffer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d489-145">On success, the name of the current index of the given cursor will be returned in the output buffer.</span></span> <span data-ttu-id="8d489-146">Wenn JET_wrnBufferTruncated zurückgegeben wird, enthält der Ausgabepuffer den Wert des Index namens, der in den bereitgestellten Speicherplatz passt.</span><span class="sxs-lookup"><span data-stu-id="8d489-146">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the index name as will fit in the space provided.</span></span> <span data-ttu-id="8d489-147">Wenn der Ausgabepuffer mindestens ein Zeichen lang ist, wird die in diesem Puffer zurückgegebene Zeichenfolge Null beendet.</span><span class="sxs-lookup"><span data-stu-id="8d489-147">If the output buffer is at least one character in length then the string returned in that buffer will be null terminated.</span></span> <span data-ttu-id="8d489-148">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="8d489-148">No change to the database state will occur.</span></span>

<span data-ttu-id="8d489-149">Bei einem Fehler wird der Status des Ausgabepuffers nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="8d489-149">On failure, the state of the output buffer will be undefined.</span></span> <span data-ttu-id="8d489-150">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="8d489-150">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8d489-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d489-151">Remarks</span></span>

<span data-ttu-id="8d489-152">Wenn kein aktueller Index für den Cursor vorhanden ist, wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d489-152">If there is no current index for the cursor then an empty string will be returned.</span></span> <span data-ttu-id="8d489-153">Dies kann vorkommen, wenn sich der Cursor auf dem gruppierten Index der Tabelle befindet und kein primärer Index definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8d489-153">This can happen when the cursor is on the clustered index of the table and no primary index was defined.</span></span> <span data-ttu-id="8d489-154">Dieser Index wird als sequenzieller Index der Tabelle bezeichnet und weist keine Definition auf.</span><span class="sxs-lookup"><span data-stu-id="8d489-154">This index is known as the sequential index of the table and has no definition.</span></span> <span data-ttu-id="8d489-155">Wenn Sie den aktuellen Index auf eine leere Zeichenfolge mithilfe von [jetsetcurrentindex](./jetsetcurrentindex-function.md) festlegen, wird der gruppierte Index unabhängig davon ausgewählt, ob eine primär Index Definition vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8d489-155">In any case, setting the current index to an empty string using [JetSetCurrentIndex](./jetsetcurrentindex-function.md) will select the clustered index regardless of the presence of a primary index definition.</span></span>

<span data-ttu-id="8d489-156">In dieser Funktion gibt es einen wichtigen Fehler, der in allen Releases vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8d489-156">There is an important bug in this function that is present in all releases.</span></span> <span data-ttu-id="8d489-157">Wenn der Ausgabepuffer zu klein ist, um den gesamten Indexnamen zu empfangen, und der Ausgabepuffer mindestens ein Zeichen lang ist, wird JET_wrnBufferTruncated nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d489-157">If the output buffer is too small to receive the entire index name and the output buffer is at least one character in length then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="8d489-158">Stattdessen wird JET_errSuccess zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d489-158">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="8d489-159">Um dieses Problem zu vermeiden, sollte der Ausgabepuffer immer mindestens JET_cbNameMost + 1 (65) Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="8d489-159">To avoid this issue, the output buffer should always be at least JET_cbNameMost + 1 (65) characters in length.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8d489-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d489-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d489-161"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8d489-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8d489-162">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8d489-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d489-163"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8d489-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8d489-164">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8d489-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d489-165"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8d489-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8d489-166">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="8d489-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d489-167"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="8d489-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8d489-168">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8d489-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d489-169"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8d489-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8d489-170">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8d489-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d489-171"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="8d489-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8d489-172">Implementiert als <strong>jetgetcurrentindexw</strong> (Unicode) und <strong>jetgetcurrentindexa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="8d489-172">Implemented as <strong>JetGetCurrentIndexW</strong> (Unicode) and <strong>JetGetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8d489-173">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8d489-173">See Also</span></span>

[<span data-ttu-id="8d489-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8d489-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8d489-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8d489-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8d489-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8d489-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8d489-177">Jetgettableindexinfo</span><span class="sxs-lookup"><span data-stu-id="8d489-177">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="8d489-178">Jetsetcurrentindex</span><span class="sxs-lookup"><span data-stu-id="8d489-178">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)
