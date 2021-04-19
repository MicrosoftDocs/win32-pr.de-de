---
description: 'Weitere Informationen zu: jetdelete-Funktion'
title: JetDelete-Funktion
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f3422bc623bbd4f0cc99365df51bb797100811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362840"
---
# <a name="jetdelete-function"></a><span data-ttu-id="fcefc-103">JetDelete-Funktion</span><span class="sxs-lookup"><span data-stu-id="fcefc-103">JetDelete Function</span></span>


<span data-ttu-id="fcefc-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fcefc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdelete-function"></a><span data-ttu-id="fcefc-105">JetDelete-Funktion</span><span class="sxs-lookup"><span data-stu-id="fcefc-105">JetDelete Function</span></span>

<span data-ttu-id="fcefc-106">Die **jetdelete** -Funktion löscht den aktuellen Datensatz in einer Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="fcefc-106">The **JetDelete** function deletes the current record in a database table.</span></span>

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="fcefc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcefc-107">Parameters</span></span>

<span data-ttu-id="fcefc-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="fcefc-108">*sesid*</span></span>

<span data-ttu-id="fcefc-109">Der Daten Bank Sitzungs Kontext, der für den API-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fcefc-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="fcefc-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="fcefc-110">*tableid*</span></span>

<span data-ttu-id="fcefc-111">Der Cursor in einer Datenbanktabelle.</span><span class="sxs-lookup"><span data-stu-id="fcefc-111">The cursor on a database table.</span></span> <span data-ttu-id="fcefc-112">Die aktuelle Zeile wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fcefc-112">The current row will be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="fcefc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fcefc-113">Return Value</span></span>

<span data-ttu-id="fcefc-114">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="fcefc-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fcefc-115">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fcefc-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fcefc-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fcefc-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="fcefc-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcefc-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcefc-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fcefc-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fcefc-119">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="fcefc-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcefc-120">JET_errCallbackFailed</span><span class="sxs-lookup"><span data-stu-id="fcefc-120">JET_errCallbackFailed</span></span></p></td>
<td><p><span data-ttu-id="fcefc-121">Fehler bei der Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="fcefc-121">The callback function failed in some manner.</span></span> <span data-ttu-id="fcefc-122">Zugriffs Verletzungen in Rückruf Funktionen werden z. b. abgefangen und in JET_errCallbackFailed übersetzt.</span><span class="sxs-lookup"><span data-stu-id="fcefc-122">For example, access violations in callback functions are caught and translated into JET_errCallbackFailed.</span></span> <span data-ttu-id="fcefc-123">Dieser Fehler wird nur von Windows XP und höher zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fcefc-123">This error will only be returned by Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcefc-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="fcefc-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="fcefc-125">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="fcefc-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcefc-126">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="fcefc-126">JET_errIllegalOperation</span></span></p></td>
<td><p><span data-ttu-id="fcefc-127">Der von <em>TableID</em> angegebene Cursor unterstützt das Löschen nicht.</span><span class="sxs-lookup"><span data-stu-id="fcefc-127">The cursor specified by <em>tableid</em> does not support deletion.</span></span> <span data-ttu-id="fcefc-128">Weitere Informationen finden Sie im Abschnitt mit den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="fcefc-128">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcefc-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="fcefc-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="fcefc-130">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="fcefc-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="fcefc-131">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fcefc-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcefc-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="fcefc-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="fcefc-133">Der von <em>TableID</em> angegebene Cursor befindet sich nicht in einem Datensatz.</span><span class="sxs-lookup"><span data-stu-id="fcefc-133">The cursor specified by <em>tableid</em> is not on a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcefc-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="fcefc-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="fcefc-135">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="fcefc-135">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcefc-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="fcefc-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="fcefc-137">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcefc-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcefc-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="fcefc-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="fcefc-139">Die Datenbank-Engine verfügt nicht über ausreichende Berechtigungen zum Löschen des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="fcefc-139">The database engine does not have sufficient permissions to delete the record.</span></span> <span data-ttu-id="fcefc-140">Dies kann vorkommen, wenn die Datenbankdatei mit Schreib geschütztem Zugriff geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="fcefc-140">This may happen if the database file was opened with read-only access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcefc-141">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="fcefc-141">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="fcefc-142">Ein Update Puffer (siehe <a href="gg269339(v=exchg.10).md">jetprepareupdate</a>) ist vorhanden, aber nicht alle Änderungen, die an Spalten vom Typ JET_coltypLongText und/oder Spalten vom Typ JET_coltypLongBinary vorgenommen werden, können zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="fcefc-142">An update buffer (see <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) exists, but not all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary could be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcefc-143">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="fcefc-143">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="fcefc-144">Es ist nicht zulässig, dieselbe Sitzung von mehr als einem Thread gleichzeitig zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fcefc-144">It is illegal to use the same session from more than one thread at the same time.</span></span> <span data-ttu-id="fcefc-145">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fcefc-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcefc-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="fcefc-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="fcefc-147">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="fcefc-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcefc-148">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="fcefc-148">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="fcefc-149">Bei der Transaktion handelt es sich um eine schreibgeschützte Transaktion, die Löschvorgänge nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fcefc-149">The transaction is a read-only transaction, and does not support deletes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcefc-150">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="fcefc-150">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="fcefc-151">Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher vorhanden ist, um transaktionale Informationen zum Update beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="fcefc-151">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcefc-152">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="fcefc-152">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="fcefc-153">Eine andere Sitzung hat den Datensatz bereits für das Update gesperrt.</span><span class="sxs-lookup"><span data-stu-id="fcefc-153">Another session has previously locked the record for update.</span></span> <span data-ttu-id="fcefc-154">Das von dieser Sitzung versuchte Update schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="fcefc-154">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fcefc-155">Bei Erfolg wird die Währung direkt vor dem nächsten Datensatz verbleiben.</span><span class="sxs-lookup"><span data-stu-id="fcefc-155">On success, the currency is left just before the next record.</span></span> <span data-ttu-id="fcefc-156">Wenn der gelöschte Datensatz der letzte in der Tabelle war, bleibt die Währung am Ende der Tabelle (d. h. nach dem neuen letzten Datensatz).</span><span class="sxs-lookup"><span data-stu-id="fcefc-156">If the deleted record was the last in the table, the currency is left at the end of the table (that is, after the new last record).</span></span> <span data-ttu-id="fcefc-157">Wenn der gelöschte Datensatz der einzige Datensatz in der Tabelle war, wird die Währung auf den Anfang festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fcefc-157">If the deleted record was the only record in the table, the currency is set to the beginning.</span></span>

<span data-ttu-id="fcefc-158">Die entsprechenden Indizes werden automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fcefc-158">The appropriate indexes are automatically updated.</span></span>

<span data-ttu-id="fcefc-159">Wenn ein Update vorbereitet wird (mithilfe von [jetprepareupdate](./jetprepareupdate-function.md)), wird es abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="fcefc-159">If an update is prepared (using [JetPrepareUpdate](./jetprepareupdate-function.md)), it will be canceled.</span></span> <span data-ttu-id="fcefc-160">Der Update Puffer wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="fcefc-160">The update buffer will be reset.</span></span>

<span data-ttu-id="fcefc-161">Bei einem Fehler bleibt die Währung unverändert.</span><span class="sxs-lookup"><span data-stu-id="fcefc-161">On failure, the currency remains unchanged.</span></span> <span data-ttu-id="fcefc-162">Wenn ein Update vorbereitet wird (siehe [jetprepareupdate](./jetprepareupdate-function.md)), wird der Update Puffer möglicherweise zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="fcefc-162">If an update is prepared (see [JetPrepareUpdate](./jetprepareupdate-function.md)), the update buffer may be reset.</span></span>

#### <a name="remarks"></a><span data-ttu-id="fcefc-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcefc-163">Remarks</span></span>

<span data-ttu-id="fcefc-164">Nicht alle Tabellen unterstützen das Löschen von Zeilen.</span><span class="sxs-lookup"><span data-stu-id="fcefc-164">Not all tables support deletion of rows.</span></span> <span data-ttu-id="fcefc-165">In einer temporären Tabelle wird das Löschen von Zeilen normalerweise nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fcefc-165">A temporary table does not normally support deletion of rows.</span></span> <span data-ttu-id="fcefc-166">Das Löschen von Datensätzen kann für temporäre Tabellen aus vielen Gründen aktiviert werden. einige davon sind:</span><span class="sxs-lookup"><span data-stu-id="fcefc-166">Deletion of records may be enabled on temporary tables for many reasons, some of which are:</span></span>

  - <span data-ttu-id="fcefc-167">JET_bitTTUpdatable wurde während der Erstellung angegeben.</span><span class="sxs-lookup"><span data-stu-id="fcefc-167">JET_bitTTUpdatable was specified during creation.</span></span>

  - <span data-ttu-id="fcefc-168">Große temporäre Tabellen können das Löschen unterstützen, wenn Sie mit JET_bitTTScrollable oder JET_bitTTIndexed erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="fcefc-168">Large temporary tables can support deletion if they were created with JET_bitTTScrollable or JET_bitTTIndexed.</span></span> <span data-ttu-id="fcefc-169">Der Schwellenwert, bei dem eine temporäre Tabelle "Large" ist, beträgt derzeit 64 Kilobyte, kann jedoch in zukünftigen Versionen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fcefc-169">The threshold at which a temporary table becomes "large" is currently 64 kilobytes, but it may be changed in future releases.</span></span>

<span data-ttu-id="fcefc-170">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="fcefc-170">Windows XP and later.</span></span> <span data-ttu-id="fcefc-171">Rückruf Funktionen können von **jetdelete** aufgerufen werden, einschließlich JET_cbtypBeforeDelete und JET_cbtypAfterDelete.</span><span class="sxs-lookup"><span data-stu-id="fcefc-171">Callback functions can be invoked by **JetDelete**, including JET_cbtypBeforeDelete and JET_cbtypAfterDelete.</span></span>

<span data-ttu-id="fcefc-172">Es ist wichtig, die Auswirkungen der Ausführung einer großen Anzahl von Aktualisierungs Vorgängen in einer einzelnen Transaktion zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="fcefc-172">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="fcefc-173">Jedes Update der Datenbank muss von der Datenbank-Engine im Versionsspeicher nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="fcefc-173">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="fcefc-174">Der Versionsspeicher enthält einen Live Datensatz aller verschiedenen Versionen der einzelnen Datensatz-oder Indexeinträge in der Datenbank, die von allen aktiven Transaktionen angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="fcefc-174">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="fcefc-175">Diese Versionen werden zur Unterstützung der Parallelitäts Steuerung mit mehreren Versionsverwaltung verwendet, die von der Datenbank-Engine verwendet wird, um Transaktionen mithilfe der Momentaufnahme Isolation zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fcefc-175">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="fcefc-176">Sobald die Datenbank-Engine die Ressourcen erschöpft hat, die zum Speichern dieser Versionen verwendet werden, kann Sie keine weiteren Änderungen mehr akzeptieren, bis einige Transaktionen abgeschlossen sind, damit diese Ressourcen freigegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="fcefc-176">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="fcefc-177">Wenn sich die Engine in diesem Zustand befindet, schlagen alle Updates mit Jet_errVersionStoreOutOfMemory fehl.</span><span class="sxs-lookup"><span data-stu-id="fcefc-177">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="fcefc-178">Die Ressourcen, die für die Datenbank-Engine zum Speichern dieser Versionen verfügbar sind, können mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit *JET_paramMaxVerPages* und *JET_paramGlobalMinVerPages* gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="fcefc-178">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxVerPages* and *JET_paramGlobalMinVerPages*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fcefc-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fcefc-179">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcefc-180"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="fcefc-180"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fcefc-181">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fcefc-181">Requires Windows Vista, Windows XP or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcefc-182"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fcefc-182"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fcefc-183">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fcefc-183">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcefc-184"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="fcefc-184"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fcefc-185">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="fcefc-185">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcefc-186"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="fcefc-186"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fcefc-187">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fcefc-187">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fcefc-188"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fcefc-188"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fcefc-189">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fcefc-189">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fcefc-190">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fcefc-190">See Also</span></span>

[<span data-ttu-id="fcefc-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fcefc-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fcefc-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="fcefc-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="fcefc-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="fcefc-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="fcefc-194">Jetopumtemptable</span><span class="sxs-lookup"><span data-stu-id="fcefc-194">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="fcefc-195">Jetprepareupdate</span><span class="sxs-lookup"><span data-stu-id="fcefc-195">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="fcefc-196">System Parameter</span><span class="sxs-lookup"><span data-stu-id="fcefc-196">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
