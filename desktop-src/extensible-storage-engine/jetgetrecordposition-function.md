---
description: 'Weitere Informationen zu: jetgetrecordposition-Funktion'
title: JetGetRecordPosition-Funktion
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4301b25ca111228b742ce7b35ab9ae28e170526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042356"
---
# <a name="jetgetrecordposition-function"></a><span data-ttu-id="27ac8-103">JetGetRecordPosition-Funktion</span><span class="sxs-lookup"><span data-stu-id="27ac8-103">JetGetRecordPosition Function</span></span>


<span data-ttu-id="27ac8-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="27ac8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordposition-function"></a><span data-ttu-id="27ac8-105">JetGetRecordPosition-Funktion</span><span class="sxs-lookup"><span data-stu-id="27ac8-105">JetGetRecordPosition Function</span></span>

<span data-ttu-id="27ac8-106">Die **jetgetrecordposition** -Funktion gibt die Bruch Position des aktuellen Datensatzes im aktuellen Index in Form einer [JET_RECPOS](./jet-recpos-structure.md) Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="27ac8-106">The **JetGetRecordPosition** function returns the fractional position of the current record in the current index in the form of a [JET_RECPOS](./jet-recpos-structure.md) structure.</span></span> <span data-ttu-id="27ac8-107">Diese Struktur beschreibt Bruch Positionen in Bezug auf eine ungefähre Anzahl von Indexeinträgen vor dem aktuellen Datensatz und eine ungefähre Gesamtzahl von Einträgen im Index.</span><span class="sxs-lookup"><span data-stu-id="27ac8-107">This structure describes fractional positions in terms of an approximate number of index entries before the current record and an approximate total number of entries in the index.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a><span data-ttu-id="27ac8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="27ac8-108">Parameters</span></span>

<span data-ttu-id="27ac8-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="27ac8-109">*sesid*</span></span>

<span data-ttu-id="27ac8-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="27ac8-110">The session to use for this call.</span></span>

<span data-ttu-id="27ac8-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="27ac8-111">*tableid*</span></span>

<span data-ttu-id="27ac8-112">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="27ac8-112">The cursor to use for this call.</span></span>

<span data-ttu-id="27ac8-113">*präpos*</span><span class="sxs-lookup"><span data-stu-id="27ac8-113">*precpos*</span></span>

<span data-ttu-id="27ac8-114">Die Beschreibung des Bruchteils, der verwendet wird, um die Position des aktuellen Datensatzes im aktuellen Index zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="27ac8-114">The description of the fraction to use in getting the position of the current record in the current index.</span></span>

<span data-ttu-id="27ac8-115">*cbrecpos*</span><span class="sxs-lookup"><span data-stu-id="27ac8-115">*cbRecpos*</span></span>

<span data-ttu-id="27ac8-116">Die Größe des Arbeitsspeichers, der in den- *präpos* zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="27ac8-116">The size of memory allocated at *precpos*.</span></span>

### <a name="return-value"></a><span data-ttu-id="27ac8-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27ac8-117">Return Value</span></span>

<span data-ttu-id="27ac8-118">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="27ac8-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="27ac8-119">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="27ac8-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27ac8-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="27ac8-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="27ac8-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27ac8-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27ac8-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="27ac8-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="27ac8-123">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="27ac8-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27ac8-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="27ac8-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="27ac8-125">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="27ac8-125">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27ac8-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="27ac8-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="27ac8-127">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="27ac8-127">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27ac8-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="27ac8-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="27ac8-129">Dieser Vorgang kann nicht ausgeführt werden, weil der der Sitzung zugeordnete Instanz ein schwerwiegender Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="27ac8-129">This operation cannot complete because the instance, associated with the session, encountered a fatal error.</span></span> <span data-ttu-id="27ac8-130">Es ist erforderlich, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="27ac8-130">It is required that access to all data be revoked in order to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="27ac8-131"><strong>Windows 2000:</strong>  Dieser Fehler wird vom Betriebssystem Windows 2000 nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27ac8-131"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27ac8-132">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="27ac8-132">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="27ac8-133">Die Größe des zugeordneten Arbeitsspeichers bei den <em>präpos</em> ist nicht ausreichend.</span><span class="sxs-lookup"><span data-stu-id="27ac8-133">The size of the allocated memory at <em>precpos</em> is not a sufficient size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27ac8-134">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="27ac8-134">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="27ac8-135">Der Cursor befindet sich derzeit nicht in einem Datensatz und kann keine Position zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="27ac8-135">The cursor is not currently on a record and cannot return a position.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27ac8-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="27ac8-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="27ac8-137">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27ac8-137">It is not possible to complete the operation because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27ac8-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="27ac8-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="27ac8-139">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27ac8-139">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="27ac8-140"><strong>Windows 2000:</strong>  Dieser Fehler wird vom Betriebssystem Windows 2000 nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27ac8-140"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27ac8-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="27ac8-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="27ac8-142">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="27ac8-142">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="27ac8-143">Bei Erfolg wird die ungefähre Anzahl der Indexeinträge, die dem aktuellen Datensatz im Index vorangestellt sind, in "precpos- \> centrieslt" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27ac8-143">On success, the approximate number of index entries preceding the current record in the index are returned in precpos-\>centriesLT.</span></span> <span data-ttu-id="27ac8-144">1 wird in "precpos- \> centriesinrange" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27ac8-144">1 is returned in precpos-\>centriesInRange.</span></span> <span data-ttu-id="27ac8-145">Die ungefähre Anzahl von Einträgen im Index wird in "precpos- \> centriestotal" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27ac8-145">The approximate number of entries in the index is returned in precpos-\>centriesTotal.</span></span>

<span data-ttu-id="27ac8-146">Bei einem Fehler werden keine Änderungen an dem Arbeitsspeicher vorgenommen, der in den *präpos* zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="27ac8-146">On failure, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="27ac8-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27ac8-147">Remarks</span></span>

<span data-ttu-id="27ac8-148">Mit diesem Vorgang werden unterschiedliche Daten zurückgegeben, wenn Updates kontinuierlich in der Tabelle auftreten.</span><span class="sxs-lookup"><span data-stu-id="27ac8-148">This operation returns varying data when updates occur continuously on the table.</span></span> <span data-ttu-id="27ac8-149">Die Änderungen in den Werten entsprechen nicht immer den Erwartungen, die auf dem Wissen der Updates basieren, da die Werte auf Grundlage physischer Eigenschaften des Indexes zu Näherungen gehören.</span><span class="sxs-lookup"><span data-stu-id="27ac8-149">The changes in the values will not always match expectations based on knowledge of the updates, since the values are approximations based on physical properties of the index.</span></span> <span data-ttu-id="27ac8-150">Die Transaktions Isolation gilt nicht für Positionen von **jetgetrecordposition** , da die Werte von den physischen Eigenschaften des Indexes abhängen, die nicht Transaktions isoliert sind.</span><span class="sxs-lookup"><span data-stu-id="27ac8-150">Transactional isolation does not apply to positions from **JetGetRecordPosition** since the values depend on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="27ac8-151">[JET_RECPOS](./jet-recpos-structure.md) sollten nicht zum Beschreiben eines Datensatzes innerhalb einer Tabelle oder zum Neupositionieren eines Datensatzes in der Nähe eines vorhandenen Datensatzes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27ac8-151">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="27ac8-152">Stattdessen sollten Lesezeichen für einen vorhandenen Datensatz abgerufen und dann zum Neupositionieren desselben Datensatzes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27ac8-152">Instead, bookmarks for an existing record should be retrieved and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="27ac8-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27ac8-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27ac8-154"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="27ac8-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="27ac8-155">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="27ac8-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27ac8-156"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="27ac8-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="27ac8-157">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="27ac8-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27ac8-158"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="27ac8-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="27ac8-159">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="27ac8-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27ac8-160"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="27ac8-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="27ac8-161">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="27ac8-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27ac8-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="27ac8-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="27ac8-163">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="27ac8-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="27ac8-164">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="27ac8-164">See Also</span></span>

[<span data-ttu-id="27ac8-165">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="27ac8-165">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="27ac8-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="27ac8-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="27ac8-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="27ac8-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="27ac8-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="27ac8-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="27ac8-169">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="27ac8-169">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="27ac8-170">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="27ac8-170">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="27ac8-171">Jetgotoposition</span><span class="sxs-lookup"><span data-stu-id="27ac8-171">JetGotoPosition</span></span>](./jetgotoposition-function.md)  
[<span data-ttu-id="27ac8-172">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="27ac8-172">JetStopService</span></span>](./jetstopservice-function.md)
