---
description: Weitere Informationen finden Sie in der jetgotoposition-Funktion
title: Jetgotoposition-Funktion
TOCTitle: JetGotoPosition Function
ms:assetid: 77b099f1-4a21-4ddb-b269-83ca74219b4d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269300(v=EXCHG.10)
ms:contentKeyID: 32765592
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aae5148431ad46c5a75bbd804f2c0d777b279561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749720"
---
# <a name="jetgotoposition-function"></a><span data-ttu-id="72d19-103">Jetgotoposition-Funktion</span><span class="sxs-lookup"><span data-stu-id="72d19-103">JetGotoPosition Function</span></span>


<span data-ttu-id="72d19-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="72d19-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotoposition-function"></a><span data-ttu-id="72d19-105">Jetgotoposition-Funktion</span><span class="sxs-lookup"><span data-stu-id="72d19-105">JetGotoPosition Function</span></span>

<span data-ttu-id="72d19-106">Die **jetgotoposition** -Funktion verschiebt einen Cursor an eine neue Position, die ein Bruchteil der Art und Weise des aktuellen Indexes ist.</span><span class="sxs-lookup"><span data-stu-id="72d19-106">The **JetGotoPosition** function moves a cursor to a new location that is a fraction of the way through the current index.</span></span> <span data-ttu-id="72d19-107">Der Bruchteil entspricht ungefähr folgendem:</span><span class="sxs-lookup"><span data-stu-id="72d19-107">The fraction is approximately equal to the following:</span></span>

<span data-ttu-id="72d19-108">precpos- \> centrieslt/precpos- \> zentriestotal</span><span class="sxs-lookup"><span data-stu-id="72d19-108">precpos-\>centriesLT/precpos-\>centriesTotal</span></span>

<span data-ttu-id="72d19-109">Dieser Vorgang wird als Reaktion auf die Eingabe des Benutzer Bild Lauf Felds ausgeführt, die empfangen wird, wenn der Benutzer versucht, Daten anzuzeigen, die teilweise durch ein DataSet gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="72d19-109">This operation is performed in response to user scroll box input that is received when the user attempts to show data that starts part way through a data set.</span></span>

```cpp
    JET_ERR JET_API JetGotoPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_RECPOS* precpos
    );
```

### <a name="parameters"></a><span data-ttu-id="72d19-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="72d19-110">Parameters</span></span>

<span data-ttu-id="72d19-111">*-sid*</span><span class="sxs-lookup"><span data-stu-id="72d19-111">*sesid*</span></span>

<span data-ttu-id="72d19-112">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72d19-112">The session to use for this call.</span></span>

<span data-ttu-id="72d19-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="72d19-113">*tableid*</span></span>

<span data-ttu-id="72d19-114">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72d19-114">The cursor to use for this call.</span></span>

<span data-ttu-id="72d19-115">*präpos*</span><span class="sxs-lookup"><span data-stu-id="72d19-115">*precpos*</span></span>

<span data-ttu-id="72d19-116">Die Beschreibung des Bruchteils, der zum Positionieren des Cursors im aktuellen Index verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72d19-116">The description of the fraction to use in positioning the cursor in the current index.</span></span>

### <a name="return-value"></a><span data-ttu-id="72d19-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72d19-117">Return Value</span></span>

<span data-ttu-id="72d19-118">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="72d19-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="72d19-119">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="72d19-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72d19-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="72d19-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="72d19-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72d19-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72d19-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="72d19-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="72d19-123">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="72d19-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72d19-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="72d19-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="72d19-125">Der Vorgang konnte nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="72d19-125">The operation could not complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72d19-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="72d19-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="72d19-127">Der Vorgang konnte nicht ausgeführt werden, da der-Instanz, die der Sitzung zugeordnet ist, ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="72d19-127">The operation could not complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="72d19-128"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="72d19-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72d19-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="72d19-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="72d19-130">Die angegebene "precpos- &gt; cbStruct" ist keine gültige Größe für die <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> Struktur, oder "precpos- &gt; centrieslt" ist größer als "precpos- &gt; centriestotal".</span><span class="sxs-lookup"><span data-stu-id="72d19-130">The given precpos-&gt;cbStruct is not a valid size for the <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> structure, or precpos-&gt;centriesLT is greater than precpos-&gt;centriesTotal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72d19-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="72d19-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="72d19-132">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="72d19-132">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72d19-133">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="72d19-133">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="72d19-134">Dieser Fehler wird zurückgegeben, wenn der Index leer ist.</span><span class="sxs-lookup"><span data-stu-id="72d19-134">This error will be returned if the index is empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72d19-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="72d19-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="72d19-136">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72d19-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72d19-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="72d19-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="72d19-138">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72d19-138">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="72d19-139"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="72d19-139"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72d19-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="72d19-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="72d19-141">Der Vorgang kann nicht ausgeführt werden, da die-Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="72d19-141">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="72d19-142">Wenn diese Funktion erfolgreich ausgeführt wird, wird der Cursor zu einem aktuellen Datensatz verschoben, der ein Bruchteil der Methode durch den Index ist, bei dem der Bruchteil "precpos- \> centrieslt dividiert" durch "precpos- \> centriestotal" ist.</span><span class="sxs-lookup"><span data-stu-id="72d19-142">If this function succeeds, the cursor is moved to a current record that is a fraction of the way through the index where the fraction is precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="72d19-143">Wenn diese Funktion fehlschlägt, bleibt die Cursorposition unverändert.</span><span class="sxs-lookup"><span data-stu-id="72d19-143">If this function fails, the cursor location is left unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="72d19-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72d19-144">Remarks</span></span>

<span data-ttu-id="72d19-145">Mit diesem Vorgang wird der Cursor durch die Tabelle an eine Position am folgenden ungefähren Punkt verschoben: precpos- \> centrieslt dividiert durch precpos- \> zentriestotal.</span><span class="sxs-lookup"><span data-stu-id="72d19-145">This operation moves the cursor through the table to a position at the following approximate point: precpos-\>centriesLT divided by precpos-\>centriesTotal.</span></span>

<span data-ttu-id="72d19-146">Wenn Updates fortlaufend in der Tabelle auftreten, können nachfolgende Aufrufe mit dem gleichen [JET_RECPOS](./jet-recpos-structure.md) den Cursor an verschiedene Positionen im Index verschieben, sowohl vor als auch nach der vorherigen Position.</span><span class="sxs-lookup"><span data-stu-id="72d19-146">When updates are occurring continuously on the table, subsequent calls with the same [JET_RECPOS](./jet-recpos-structure.md) can move the cursor to different positions in the index, both before and after the previous position.</span></span> <span data-ttu-id="72d19-147">Die Transaktions Isolation gilt nicht für die Positionierung durch [JET_RECPOS](./jet-recpos-structure.md) , da Sie von den physischen Eigenschaften des Indexes abhängig ist, die nicht Transaktions isoliert sind.</span><span class="sxs-lookup"><span data-stu-id="72d19-147">Transactional isolation does not apply to positioning through [JET_RECPOS](./jet-recpos-structure.md) since it depends on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="72d19-148">[JET_RECPOS](./jet-recpos-structure.md) sollten nicht zum Beschreiben eines Datensatzes innerhalb einer Tabelle oder zum Neupositionieren eines Datensatzes in der Nähe eines vorhandenen Datensatzes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72d19-148">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="72d19-149">Stattdessen sollten Lesezeichen für einen vorhandenen Datensatz nach einer anfänglichen **jetgotoposition** abgerufen und dann zum Neupositionieren desselben Datensatzes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72d19-149">Instead, bookmarks for an existing record should be retrieved after an initial **JetGotoPosition** and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="72d19-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72d19-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72d19-151"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="72d19-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="72d19-152">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="72d19-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72d19-153"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="72d19-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="72d19-154">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="72d19-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72d19-155"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="72d19-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="72d19-156">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="72d19-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72d19-157"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="72d19-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="72d19-158">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="72d19-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72d19-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="72d19-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="72d19-160">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="72d19-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="72d19-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="72d19-161">See Also</span></span>

[<span data-ttu-id="72d19-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="72d19-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="72d19-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="72d19-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="72d19-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="72d19-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="72d19-165">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="72d19-165">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="72d19-166">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="72d19-166">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="72d19-167">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="72d19-167">JET_SETINFO</span></span>](./jet-setinfo-structure.md)
