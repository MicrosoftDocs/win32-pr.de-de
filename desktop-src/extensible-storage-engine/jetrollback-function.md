---
description: 'Weitere Informationen finden Sie unter: jetrollback-Funktion'
title: Jetrollback-Funktion
TOCTitle: JetRollback Function
ms:assetid: 685c51f4-8fe4-47cc-8a8e-c42014431b8b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269273(v=EXCHG.10)
ms:contentKeyID: 32765575
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRollback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eda0c8947e9609717bbb3f1a16999b450d7e4882
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352543"
---
# <a name="jetrollback-function"></a><span data-ttu-id="e90b3-103">Jetrollback-Funktion</span><span class="sxs-lookup"><span data-stu-id="e90b3-103">JetRollback Function</span></span>


<span data-ttu-id="e90b3-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e90b3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrollback-function"></a><span data-ttu-id="e90b3-105">Jetrollback-Funktion</span><span class="sxs-lookup"><span data-stu-id="e90b3-105">JetRollback Function</span></span>

<span data-ttu-id="e90b3-106">Die **jetrollback** -Funktion macht die am Status der Datenbank vorgenommenen Änderungen rückgängig und kehrt zum letzten Sicherungspunkt zurück.</span><span class="sxs-lookup"><span data-stu-id="e90b3-106">The **JetRollback** function undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="e90b3-107">**Jetrollback** schließt auch alle Cursor, die während des Speicher Punkts geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="e90b3-107">**JetRollback** will also close any cursors opened during the save point.</span></span> <span data-ttu-id="e90b3-108">Wenn der äußerste Speicherpunkt rückgängig gemacht wird, beendet die Sitzung die Transaktion.</span><span class="sxs-lookup"><span data-stu-id="e90b3-108">If the outermost save point is undone, the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetRollback(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e90b3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e90b3-109">Parameters</span></span>

<span data-ttu-id="e90b3-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="e90b3-110">*sesid*</span></span>

<span data-ttu-id="e90b3-111">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e90b3-111">The session to use for this call.</span></span>

<span data-ttu-id="e90b3-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e90b3-112">*grbit*</span></span>

<span data-ttu-id="e90b3-113">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="e90b3-113">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e90b3-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e90b3-114">Value</span></span></p></th>
<th><p><span data-ttu-id="e90b3-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e90b3-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e90b3-116">JET_bitRollbackAll</span><span class="sxs-lookup"><span data-stu-id="e90b3-116">JET_bitRollbackAll</span></span></p></td>
<td><p><span data-ttu-id="e90b3-117">Mit dieser Option wird angefordert, dass alle Änderungen, die an dem Status der Datenbank vorgenommen wurden, bei allen Speicher Punkten rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="e90b3-117">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="e90b3-118">Dies führt dazu, dass die Sitzung die Transaktion beendet.</span><span class="sxs-lookup"><span data-stu-id="e90b3-118">As a result, the session will exit the transaction.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e90b3-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e90b3-119">Return Value</span></span>

<span data-ttu-id="e90b3-120">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="e90b3-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e90b3-121">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e90b3-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e90b3-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e90b3-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="e90b3-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e90b3-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e90b3-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e90b3-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e90b3-125">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e90b3-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90b3-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e90b3-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e90b3-127">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="e90b3-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90b3-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e90b3-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e90b3-129">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="e90b3-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="e90b3-130">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e90b3-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90b3-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e90b3-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e90b3-132">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e90b3-132">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90b3-133">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="e90b3-133">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="e90b3-134">Der Vorgang ist fehlgeschlagen, da die angegebene Sitzung nicht in einer Transaktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e90b3-134">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90b3-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e90b3-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e90b3-136">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e90b3-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90b3-137">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="e90b3-137">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="e90b3-138">Aufgrund eines schwerwiegenden Fehlers war es nicht möglich, die Änderungen zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="e90b3-138">It was not possible to rollback the changes due to a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90b3-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e90b3-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e90b3-140">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e90b3-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="e90b3-141">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e90b3-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90b3-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e90b3-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e90b3-143">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="e90b3-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e90b3-144">Bei Erfolg werden alle Änderungen, die während des aktuellen Speicher Punkts für die jeweilige Sitzung an der Datenbank vorgenommen wurden, rückgängig gemacht, und der Sicherungspunkt wird beendet.</span><span class="sxs-lookup"><span data-stu-id="e90b3-144">On success, any changes made to the database during the current save point for the given session will be undone and that save point will be ended.</span></span> <span data-ttu-id="e90b3-145">Wenn der letzte Sicherungspunkt für die Sitzung beendet wurde, wird die Transaktion von der Sitzung beendet.</span><span class="sxs-lookup"><span data-stu-id="e90b3-145">If the last save point for the session was ended then the session will exit the transaction.</span></span>

<span data-ttu-id="e90b3-146">Bei einem Fehler bleibt der Transaktionsstatus der Sitzung unverändert.</span><span class="sxs-lookup"><span data-stu-id="e90b3-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="e90b3-147">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="e90b3-147">No change to the database state will occur.</span></span> <span data-ttu-id="e90b3-148">Ein Fehler während des Rollbacks wird als schwerwiegender Datenbankfehler betrachtet.</span><span class="sxs-lookup"><span data-stu-id="e90b3-148">A failure during rollback is considered to be a catastrophic database error.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e90b3-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e90b3-149">Remarks</span></span>

<span data-ttu-id="e90b3-150">Es muss ein Aufrufen von [jetcommittransaction](./jetcommittransaction-function.md) oder **jetrollback** vorhanden sein, um jeden beliebigen [jetbegintransaction](./jetbegintransaction-function.md) -Befehl für eine bestimmte Sitzung abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="e90b3-150">There must be one call to [JetCommitTransaction](./jetcommittransaction-function.md) or **JetRollback** to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

<span data-ttu-id="e90b3-151">Wenn z. b. bei einem Sicherungspunkt, für den ein Rollback ausgeführt wird, beliebige Cursor (z. [b. jetopentable](./jetopentable-function.md)) geöffnet wurden, wird der Cursor geschlossen.</span><span class="sxs-lookup"><span data-stu-id="e90b3-151">If any cursors were opened (using [JetOpenTable](./jetopentable-function.md), for example) during a save point that is being rolled back then that cursor will be closed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e90b3-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e90b3-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e90b3-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e90b3-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e90b3-154">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e90b3-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90b3-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e90b3-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e90b3-156">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e90b3-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90b3-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e90b3-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e90b3-158">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="e90b3-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e90b3-159"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="e90b3-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e90b3-160">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e90b3-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e90b3-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e90b3-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e90b3-162">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e90b3-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e90b3-163">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e90b3-163">See Also</span></span>

[<span data-ttu-id="e90b3-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e90b3-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e90b3-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e90b3-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e90b3-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e90b3-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e90b3-167">Jetbegintransaction</span><span class="sxs-lookup"><span data-stu-id="e90b3-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="e90b3-168">Jetcommittransaction</span><span class="sxs-lookup"><span data-stu-id="e90b3-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)
