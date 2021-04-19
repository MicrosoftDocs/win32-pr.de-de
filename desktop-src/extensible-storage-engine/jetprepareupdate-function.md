---
description: 'Weitere Informationen zu: jetprepareupdate-Funktion'
title: Jetprepareupdate-Funktion
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16362463194d945d7b451f784bc0942bda2d03e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369086"
---
# <a name="jetprepareupdate-function"></a><span data-ttu-id="d5f27-103">Jetprepareupdate-Funktion</span><span class="sxs-lookup"><span data-stu-id="d5f27-103">JetPrepareUpdate Function</span></span>


<span data-ttu-id="d5f27-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d5f27-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprepareupdate-function"></a><span data-ttu-id="d5f27-105">Jetprepareupdate-Funktion</span><span class="sxs-lookup"><span data-stu-id="d5f27-105">JetPrepareUpdate Function</span></span>

<span data-ttu-id="d5f27-106">Die **jetprepareupdate** -Funktion ist der erste Vorgang, bei dem ein Update durchgeführt wird, um einen neuen Datensatz einzufügen oder einen vorhandenen Datensatz durch neue Werte zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="d5f27-106">The **JetPrepareUpdate** function is the first operation in performing an update, for the purposes of inserting a new record or replacing an existing record with new values.</span></span> <span data-ttu-id="d5f27-107">Updates werden durch Aufrufen von **jetprepareupdate** und anschließendes Aufrufen von [jetsetcolumn](./jetsetcolumn-function.md) oder [jetsetcolumns](./jetsetcolumns-function.md) (null oder mehrmals) und schließlich durch Aufrufen von [jetupdate](./jetupdate-function.md) zum Durchführen des Vorgangs durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5f27-107">Updates are done by calling **JetPrepareUpdate**, then calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) zero or more times and finally by calling [JetUpdate](./jetupdate-function.md) to complete the operation.</span></span> <span data-ttu-id="d5f27-108">**Jetprepareupdate** und [jetupdate](./jetupdate-function.md) legen die Grenzen für einen Aktualisierungs Vorgang fest und sind wichtig, wenn nur der endgültige Aktualisierungs Status eines Datensatzes in Indizes eingegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5f27-108">**JetPrepareUpdate** and [JetUpdate](./jetupdate-function.md) set the boundaries for an update operation and are important in having only the final update state of a record entered into indexes.</span></span> <span data-ttu-id="d5f27-109">Dies ist sowohl effizienter als auch bei Fällen erforderlich, in denen Daten mit einem gültigen Zustand über mehr als den Vorgang zum Festlegen von Spalten verglichen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d5f27-109">This is both more efficient, but also required in cases where data must match a valid state through more than on set column operation.</span></span>

<span data-ttu-id="d5f27-110">Es gibt verschiedene Optionen zum Einfügen oder Austauschen von Datensätzen. Diese werden im folgenden ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d5f27-110">There are a few different options for inserting or replacing records and they are described in more detail below.</span></span>

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a><span data-ttu-id="d5f27-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5f27-111">Parameters</span></span>

<span data-ttu-id="d5f27-112">*-sid*</span><span class="sxs-lookup"><span data-stu-id="d5f27-112">*sesid*</span></span>

<span data-ttu-id="d5f27-113">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5f27-113">The session to use for this call.</span></span>

<span data-ttu-id="d5f27-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d5f27-114">*tableid*</span></span>

<span data-ttu-id="d5f27-115">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5f27-115">The cursor to use for this call.</span></span>

<span data-ttu-id="d5f27-116">*vorzubereiten*</span><span class="sxs-lookup"><span data-stu-id="d5f27-116">*prep*</span></span>

<span data-ttu-id="d5f27-117">Die Optionen, die verwendet werden können, um ein Update vorzubereiten, einschließlich der folgenden.</span><span class="sxs-lookup"><span data-stu-id="d5f27-117">The options that can be used to prepare for an update, which include the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d5f27-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d5f27-118">Value</span></span></p></th>
<th><p><span data-ttu-id="d5f27-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d5f27-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5f27-120">JET_prepCancel</span><span class="sxs-lookup"><span data-stu-id="d5f27-120">JET_prepCancel</span></span></p></td>
<td><p><span data-ttu-id="d5f27-121">Dieses Flag bewirkt, dass <strong>jetprepareupdate</strong> das Update für diesen Cursor abbricht.</span><span class="sxs-lookup"><span data-stu-id="d5f27-121">This flag causes <strong>JetPrepareUpdate</strong> to cancel the update for this cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f27-122">JET_prepInsert</span><span class="sxs-lookup"><span data-stu-id="d5f27-122">JET_prepInsert</span></span></p></td>
<td><p><span data-ttu-id="d5f27-123">Dieses Flag bewirkt, dass der Cursor eine Einfügung eines neuen Datensatzes vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="d5f27-123">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="d5f27-124">Alle Daten werden auf den Standardstatus für den Datensatz initialisiert.</span><span class="sxs-lookup"><span data-stu-id="d5f27-124">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="d5f27-125">Wenn die Tabelle eine automatische Inkrement-Spalte aufweist, wird diesem Datensatz ein neuer Wert zugewiesen, unabhängig davon, ob das Update letztendlich erfolgreich ist, fehlschlägt oder abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="d5f27-125">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f27-126">JET_prepInsertCopy</span><span class="sxs-lookup"><span data-stu-id="d5f27-126">JET_prepInsertCopy</span></span></p></td>
<td><p><span data-ttu-id="d5f27-127">Dieses Flag bewirkt, dass der Cursor eine Einfügung einer Kopie des vorhandenen Datensatzes vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="d5f27-127">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="d5f27-128">Wenn diese Option verwendet wird, muss ein aktueller Datensatz vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d5f27-128">There must be a current record if this option is used.</span></span> <span data-ttu-id="d5f27-129">Der ursprüngliche Zustand des neuen Datensatzes wird aus dem aktuellen Datensatz kopiert.</span><span class="sxs-lookup"><span data-stu-id="d5f27-129">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="d5f27-130">Lange Werte, die außerhalb des Datensatzes gespeichert werden, werden virtuell kopiert.</span><span class="sxs-lookup"><span data-stu-id="d5f27-130">Long values that are stored off-record are virtually copied.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f27-131">JET_prepInsertCopyDeleteOriginal</span><span class="sxs-lookup"><span data-stu-id="d5f27-131">JET_prepInsertCopyDeleteOriginal</span></span></p></td>
<td><p><span data-ttu-id="d5f27-132">Dieses Flag bewirkt, dass der Cursor eine Einfügung desselben Datensatzes und einen Löschvorgang oder den ursprünglichen Datensatz vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="d5f27-132">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="d5f27-133">Sie wird in Fällen verwendet, in denen sich der Primärschlüssel geändert hat.</span><span class="sxs-lookup"><span data-stu-id="d5f27-133">It is used in cases in which the primary key has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f27-134">JET_prepReplace</span><span class="sxs-lookup"><span data-stu-id="d5f27-134">JET_prepReplace</span></span></p></td>
<td><p><span data-ttu-id="d5f27-135">Dieses Flag bewirkt, dass der Cursor eine Ersetzung des aktuellen Datensatzes vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="d5f27-135">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="d5f27-136">Wenn die Tabelle eine Versions Spalte aufweist, wird die Versions Spalte auf den nächsten Wert in der zugehörigen Reihenfolge festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d5f27-136">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="d5f27-137">Wenn dieses Update nicht vollständig ausgeführt wird, ist der Versions Wert im Datensatz nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="d5f27-137">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="d5f27-138">Es wird eine Update Sperre für den Datensatz erstellt, um zu verhindern, dass dieser Datensatz von anderen Sitzungen aktualisiert wird, bevor diese Sitzung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d5f27-138">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f27-139">JET_prepReplaceNoLock</span><span class="sxs-lookup"><span data-stu-id="d5f27-139">JET_prepReplaceNoLock</span></span></p></td>
<td><p><span data-ttu-id="d5f27-140">Dieses Flag ähnelt JET_prepReplace, es wird jedoch keine Sperre erstellt, um zu verhindern, dass andere Sitzungen diesen Datensatz aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d5f27-140">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="d5f27-141">Stattdessen erhält diese Sitzung möglicherweise JET_errWriteConflict, wenn <a href="gg269288(v=exchg.10).md">jetupdate</a> aufgerufen wird, um das Update abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d5f27-141">Instead, this session may receive JET_errWriteConflict when it calls <a href="gg269288(v=exchg.10).md">JetUpdate</a> to complete the update.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d5f27-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5f27-142">Return Value</span></span>

<span data-ttu-id="d5f27-143">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="d5f27-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d5f27-144">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d5f27-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d5f27-145">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d5f27-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="d5f27-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5f27-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5f27-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d5f27-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d5f27-148">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d5f27-148">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f27-149">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="d5f27-149">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="d5f27-150"><strong>Jetprepareupdate</strong> wurde mit einem gültigen Flag für prep aufgerufen, aber nicht JET_prepCancel, und der Cursor war bereits im vorbereiteten Zustand.</span><span class="sxs-lookup"><span data-stu-id="d5f27-150"><strong>JetPrepareUpdate</strong> was called with a valid flag for prep but not JET_prepCancel and the cursor was already in the prepared state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f27-151">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d5f27-151">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d5f27-152">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d5f27-152">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f27-153">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d5f27-153">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d5f27-154">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="d5f27-154">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="d5f27-155">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d5f27-155">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f27-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d5f27-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d5f27-157">Das angegebene prep-Flag ist kein gültiges Flag.</span><span class="sxs-lookup"><span data-stu-id="d5f27-157">The given prep flag is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f27-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d5f27-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d5f27-159">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d5f27-159">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f27-160">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="d5f27-160">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="d5f27-161"><strong>Jetprepareupdate</strong> wurde aufgerufen, um einen Datensatz zu ersetzen, der über SLV-Spalten verfügte.</span><span class="sxs-lookup"><span data-stu-id="d5f27-161"><strong>JetPrepareUpdate</strong> was called to replace a record which had SLV columns.</span></span> <span data-ttu-id="d5f27-162">SLV-Spalten.</span><span class="sxs-lookup"><span data-stu-id="d5f27-162">SLV columns.</span></span> <span data-ttu-id="d5f27-163">Beachten Sie, dass SLV-Spalten ein Feature sind, das nicht für die allgemeine Verwendung vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="d5f27-163">Please note that SLV columns are a feature not intended for general usage.</span></span> <span data-ttu-id="d5f27-164">Diese Funktion wird zur Unterstützung der Microsoft Exchange-Infrastruktur verwendet und ist nicht für die Verwendung in Ihrer Anwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="d5f27-164">This feature is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f27-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d5f27-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d5f27-166">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5f27-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f27-167">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="d5f27-167">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="d5f27-168"><strong>Jetprepareupdate</strong> wurde mit JET_prepCancel aufgerufen, konnte aber nicht alle Änderungen zurücksetzen, die an Spalten vom Typ JET_coltypLongText und/oder Spalten vom Typ JET_coltypLongBinary vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="d5f27-168"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but could not rollback all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f27-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d5f27-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d5f27-170">Dieses Flag kann nicht mit derselben Sitzung von mehreren Threads gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5f27-170">This flag cannot be used with the same session from more than one thread at the same time.</span></span> <span data-ttu-id="d5f27-171">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d5f27-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f27-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d5f27-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d5f27-173">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="d5f27-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f27-174">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="d5f27-174">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="d5f27-175"><strong>Jetprepareupdate</strong> wurde mit JET_prepCancel aufgerufen, aber der Cursor befand sich nicht im vorbereiteten Zustand.</span><span class="sxs-lookup"><span data-stu-id="d5f27-175"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d5f27-176">Bei Erfolg wechselt der Cursor zum Zweck der gewünschten Aktualisierung in den vorbereiteten Zustand, oder im Fall von JET_prepCancel wird der Cursor in den Zustand "nicht vorbereitet" versetzt, und alle Änderungen werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="d5f27-176">On success, the cursor is changed to the prepared state for the purpose of the desired update, or in the case of JET_prepCancel, the cursor is reverted to the non-prepared state and any changes are discarded.</span></span>

<span data-ttu-id="d5f27-177">Bei einem Fehler bleibt der Cursor Zustand unverändert.</span><span class="sxs-lookup"><span data-stu-id="d5f27-177">On failure, the cursor state is left unchanged.</span></span> <span data-ttu-id="d5f27-178">Wenn der Fehler JET_errRollbackError wurde, wird der Cursor Zustand in den Zustand "nicht vorbereitet" geändert, aber nicht alle Änderungen wurden zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d5f27-178">If the failure was JET_errRollbackError then the cursor state is changed to the non-prepared state but not all of the changes have been reverted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d5f27-179">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5f27-179">Remarks</span></span>

<span data-ttu-id="d5f27-180">Das Einfügen einer Kopie eines Datensatzes ist eine wichtige Optimierung, wenn Datensätze Daten vom Typ JET_coltypLongText und/oder JET_coltypLongBinary gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="d5f27-180">Inserting a copy of a record is an important optimization when records share data of type JET_coltypLongText and/or JET_coltypLongBinary.</span></span> <span data-ttu-id="d5f27-181">Diese Daten werden bei großen Datensätzen außerhalb des Datensatzes gespeichert, und es ist möglich, dass mehrere Datensätze dieselbe physische Darstellung der Daten gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="d5f27-181">This data is stored off-record when large and it is possible for multiple records to share the same physical representation of the data.</span></span> <span data-ttu-id="d5f27-182">In diesem Fall können die Daten von jedem Datensatz aus aktualisiert werden. Dies führt jedoch dazu, dass die Daten so Burst werden, dass jeder Datensatz über eine eigene Kopie verfügt.</span><span class="sxs-lookup"><span data-stu-id="d5f27-182">In this case, the data can be updated from either record, but doing so will cause the data to be burst such that each record has its own copy.</span></span> <span data-ttu-id="d5f27-183">Es ist nicht möglich, Daten in einem Datensatz durch eine Änderung eines anderen Datensatzes zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d5f27-183">It is not possible to change data in one record by a modification from another record.</span></span> <span data-ttu-id="d5f27-184">Außerdem ist es nicht möglich, ein Update eines einzelnen Datensatzes durch Aktualisieren eines anderen Datensatzes zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="d5f27-184">Also, it is not possible to block an update of one record by an update of another record.</span></span> <span data-ttu-id="d5f27-185">Dies ist ein zentrales Feature von ESE und wird als Sperren auf Datensatzebene bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d5f27-185">This is a central feature to ESE and is known as Record Level Locking.</span></span>

<span data-ttu-id="d5f27-186">Bei [jetupdate](./jetupdate-function.md) -Vorgängen, bei denen der Cursor nicht erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="d5f27-186">[JetUpdate](./jetupdate-function.md) operations which fail leave the cursor in the update prepared state.</span></span> <span data-ttu-id="d5f27-187">Dadurch können einige Fehler korrigiert werden, z. b. ein falscher Spaltenwert, ohne dass der Aktualisierungs Status neu erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="d5f27-187">This is to permit correction to some errors, such as a wrong column value, without requiring the update state to be recreated.</span></span> <span data-ttu-id="d5f27-188">Dies bedeutet, dass in allen Fällen, in denen ein Cursor ein Update abbricht, " **jetprepareupdate** " explizit mit JET_prepCancel aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="d5f27-188">This means that in all cases where a cursor abandons an update, it must explicitly call **JetPrepareUpdate** with JET_prepCancel.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d5f27-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5f27-189">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5f27-190"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d5f27-190"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d5f27-191">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d5f27-191">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f27-192"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d5f27-192"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d5f27-193">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d5f27-193">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f27-194"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d5f27-194"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d5f27-195">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="d5f27-195">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f27-196"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="d5f27-196"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d5f27-197">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d5f27-197">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f27-198"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d5f27-198"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d5f27-199">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d5f27-199">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d5f27-200">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d5f27-200">See Also</span></span>

[<span data-ttu-id="d5f27-201">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d5f27-201">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d5f27-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d5f27-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d5f27-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d5f27-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d5f27-204">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="d5f27-204">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="d5f27-205">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="d5f27-205">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="d5f27-206">Jetupdate</span><span class="sxs-lookup"><span data-stu-id="d5f27-206">JetUpdate</span></span>](./jetupdate-function.md)
