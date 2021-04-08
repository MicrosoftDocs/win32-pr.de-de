---
description: 'Weitere Informationen finden Sie hier: JetUpdate2-Funktion'
title: JetUpdate2-Funktion
TOCTitle: JetUpdate2 Function
ms:assetid: 125f372c-9c4c-4be8-b0df-bbf53d79e90b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269190(v=EXCHG.10)
ms:contentKeyID: 32765493
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc08b26ebff33a68654ed33a2cb0539af1fa2a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750473"
---
# <a name="jetupdate2-function"></a><span data-ttu-id="44ea1-103">JetUpdate2-Funktion</span><span class="sxs-lookup"><span data-stu-id="44ea1-103">JetUpdate2 Function</span></span>


<span data-ttu-id="44ea1-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="44ea1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate2-function"></a><span data-ttu-id="44ea1-105">JetUpdate2-Funktion</span><span class="sxs-lookup"><span data-stu-id="44ea1-105">JetUpdate2 Function</span></span>

<span data-ttu-id="44ea1-106">Die **JetUpdate2** -Funktion führt einen Aktualisierungs Vorgang aus, einschließlich des Einfügens einer neuen Zeile in eine Tabelle oder der Aktualisierung einer vorhandenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="44ea1-106">The **JetUpdate2** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="44ea1-107">Diese Funktion enthält eine Liste von *grbit* -Optionen, die beim Ausführen eines Updates festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="44ea1-107">This function contains a list of *grbit* options that can be set while performing an update.</span></span> <span data-ttu-id="44ea1-108">Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von [jetdelete](./jetdelete-function.md).</span><span class="sxs-lookup"><span data-stu-id="44ea1-108">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="44ea1-109">**Windows Server 2003: JetUpdate2** wird in Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="44ea1-109">**Windows Server 2003:  JetUpdate2** is introduced in Windows Server 2003.</span></span>

<span data-ttu-id="44ea1-110">**JetUpdate2** ist der letzte Schritt beim Ausführen einer INSERT-oder Update-Ausführung.</span><span class="sxs-lookup"><span data-stu-id="44ea1-110">**JetUpdate2** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="44ea1-111">Das Update wird zunächst durch Aufrufen von [jetprepareupdate](./jetprepareupdate-function.md) und anschließendes Aufrufen von [jetsetcolumn](./jetsetcolumn-function.md) oder [jetsetcolumns](./jetsetcolumns-function.md) gestartet, um den Daten Satz Status festzulegen.</span><span class="sxs-lookup"><span data-stu-id="44ea1-111">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="44ea1-112">Zum Schluss wird **JetUpdate2** aufgerufen, um den Aktualisierungs Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="44ea1-112">Finally, **JetUpdate2** is called to complete the update operation.</span></span> <span data-ttu-id="44ea1-113">Indizes werden nur von [jetupdate](./jetupdate-function.md) oder **JetUpdate2** und nicht von [jetsetcolumn](./jetsetcolumn-function.md) oder [jetsetcolumns](./jetsetcolumns-function.md)aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="44ea1-113">Indexes are updated only by [JetUpdate](./jetupdate-function.md) or **JetUpdate2**, and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual,
      __in            const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="44ea1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="44ea1-114">Parameters</span></span>

<span data-ttu-id="44ea1-115">*-sid*</span><span class="sxs-lookup"><span data-stu-id="44ea1-115">*sesid*</span></span>

<span data-ttu-id="44ea1-116">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="44ea1-116">The session to use for this call.</span></span>

<span data-ttu-id="44ea1-117">*TableID*</span><span class="sxs-lookup"><span data-stu-id="44ea1-117">*tableid*</span></span>

<span data-ttu-id="44ea1-118">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="44ea1-118">The cursor to use for this call.</span></span>

<span data-ttu-id="44ea1-119">*pvbookmark*</span><span class="sxs-lookup"><span data-stu-id="44ea1-119">*pvBookmark*</span></span>

<span data-ttu-id="44ea1-120">Zeiger auf ein zurück gegebenes Lesezeichen für eine eingefügte Zeile.</span><span class="sxs-lookup"><span data-stu-id="44ea1-120">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="44ea1-121">*cbbookmark*</span><span class="sxs-lookup"><span data-stu-id="44ea1-121">*cbBookmark*</span></span>

<span data-ttu-id="44ea1-122">Größe des Puffers, auf den *pvbookmark* zeigt.</span><span class="sxs-lookup"><span data-stu-id="44ea1-122">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="44ea1-123">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="44ea1-123">*pcbActual*</span></span>

<span data-ttu-id="44ea1-124">Die zurückgegebene Größe des Lesezeichens für die eingefügte Zeile, die in *pvbookmark* zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="44ea1-124">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

<span data-ttu-id="44ea1-125">*grbit*</span><span class="sxs-lookup"><span data-stu-id="44ea1-125">*grbit*</span></span>

<span data-ttu-id="44ea1-126">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="44ea1-126">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44ea1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="44ea1-127">Value</span></span></p></th>
<th><p><span data-ttu-id="44ea1-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="44ea1-128">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44ea1-129">JET_bitUpdateCheckESE97Compatibility</span><span class="sxs-lookup"><span data-stu-id="44ea1-129">JET_bitUpdateCheckESE97Compatibility</span></span></p></td>
<td><p><span data-ttu-id="44ea1-130">Dieses Flag bewirkt, dass das Update einen Fehler zurückgibt, wenn das Update in der Windows 2000-Version von ESE nicht möglich wäre, was eine geringere maximale Anzahl von mehrwertigen Spalten Instanzen in jedem Datensatz erzwungen hat als spätere Versionen von ESE.</span><span class="sxs-lookup"><span data-stu-id="44ea1-130">This flag causes the update to return an error if the update would not have been possible in the Windows 2000 version of ESE, which enforced a smaller maximum number of multi-valued column instances in each record than later versions of ESE.</span></span> <span data-ttu-id="44ea1-131">Dies ist nur für Anwendungen wichtig, die Daten zwischen Anwendungen replizieren möchten, die unter Windows 2000 gehostet werden, und Anwendungen, die unter Windows Server 2003 oder höheren Versionen von ESE gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="44ea1-131">This is important only for applications that wish to replicate data between applications hosted on Windows 2000 and applications hosted on Windows Server 2003, or later versions of ESE.</span></span> <span data-ttu-id="44ea1-132">Dies sollte für die meisten Anwendungen nicht erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="44ea1-132">It should not be necessary for most applications.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="44ea1-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44ea1-133">Return Value</span></span>

<span data-ttu-id="44ea1-134">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="44ea1-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="44ea1-135">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="44ea1-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44ea1-136">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="44ea1-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="44ea1-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44ea1-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44ea1-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="44ea1-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="44ea1-139">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="44ea1-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ea1-140">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="44ea1-140">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="44ea1-141">Der angegebene Puffer für das Daten Satz-Lesezeichen ist nicht ausreichend groß genug zum Speichern des Daten Satz-Lesezeichens.</span><span class="sxs-lookup"><span data-stu-id="44ea1-141">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ea1-142">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="44ea1-142">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="44ea1-143">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="44ea1-143">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ea1-144">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="44ea1-144">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="44ea1-145">Der Aktualisierungs Vorgang erfordert eine Vergrößerung der Datenbankdatei oder die Protokolldatei Zuordnung, aber das Laufwerk, auf dem sich die Datenbankdatei oder die Protokoll Reihe befindet, ist voll.</span><span class="sxs-lookup"><span data-stu-id="44ea1-145">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="44ea1-146">Alternativ dazu befindet sich die Datenbankdatei auf einem auf FAT32 formatierten Volume, und die Datenbankdatei ist bereits 4gbytes, der Grenzwert pro Datei für FAT32.</span><span class="sxs-lookup"><span data-stu-id="44ea1-146">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ea1-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="44ea1-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="44ea1-148">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="44ea1-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="44ea1-149"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44ea1-149"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ea1-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="44ea1-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="44ea1-151">Der angegebene <em>prep</em> -Parameter in der <a href="gg269339(v=exchg.10).md">jetprepareupdate</a> -Funktion ist kein gültiges Flag.</span><span class="sxs-lookup"><span data-stu-id="44ea1-151">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ea1-152">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="44ea1-152">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="44ea1-153">Ein Index Schlüssel für diesen Datensatz ist ein Duplikat eines anderen Index Schlüssels für einen anderen Datensatz, der bereits in der Tabelle vorhanden ist, und der Index lässt keine Duplikate zu.</span><span class="sxs-lookup"><span data-stu-id="44ea1-153">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ea1-154">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="44ea1-154">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="44ea1-155">Der eingefügte oder aktualisierte Datensatz weist mindestens einen Index auf, für den der generierte Schlüssel die maximal zulässige Größe überschreiten würde.</span><span class="sxs-lookup"><span data-stu-id="44ea1-155">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="44ea1-156">Dies hat zur Folge, dass der Vorgang das Abschneiden von Schlüsseln nicht verhindern konnte.</span><span class="sxs-lookup"><span data-stu-id="44ea1-156">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ea1-157">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="44ea1-157">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="44ea1-158">Der eingefügte oder aktualisierte Datensatz verfügt über eine indizierte mehrwertige Spalte mit zwei oder Mehrwerten, die innerhalb der für den Index festgelegten maximalen Längen Schlüsselgröße identisch sind.</span><span class="sxs-lookup"><span data-stu-id="44ea1-158">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="44ea1-159">Folglich hat der Datensatz zwei identische Einträge im Index, die ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="44ea1-159">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ea1-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="44ea1-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="44ea1-161">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="44ea1-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ea1-162">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="44ea1-162">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="44ea1-163">Mindestens eine Spalte im Datensatz, die eingefügt werden soll, oder der aktualisierte Zustand eines zu ersetzenden Datensatzes ist <strong>null</strong> . Dies verstößt gegen die definierte Einschränkung für diese Spalten.</span><span class="sxs-lookup"><span data-stu-id="44ea1-163">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ea1-164">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="44ea1-164">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="44ea1-165">Mindestens ein Index ist so definiert, dass kein <strong>null</strong> -Schlüssel zulässig ist, und der eingefügte oder aktualisierte Status eines Datensatzes, der ersetzt wird, verstößt gegen diese definierte Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="44ea1-165">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ea1-166">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="44ea1-166">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="44ea1-167">Der Primärschlüssel wurde durch einen Daten Satz Ersetzungs Vorgang aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="44ea1-167">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="44ea1-168">Aktualisierungen an Primärschlüssel Spalten müssen durch Löschen des vorhandenen Datensatzes und Einfügen eines neuen Datensatzes mit den gewünschten Daten erfolgen.</span><span class="sxs-lookup"><span data-stu-id="44ea1-168">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ea1-169">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="44ea1-169">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="44ea1-170">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44ea1-170">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ea1-171">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="44ea1-171">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="44ea1-172">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44ea1-172">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="44ea1-173"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44ea1-173"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ea1-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="44ea1-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="44ea1-175">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="44ea1-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ea1-176">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="44ea1-176">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="44ea1-177"><a href="gg269339(v=exchg.10).md">Jetprepareupdate</a> wurde mit JET_prepCancel aufgerufen, aber der Cursor befand sich nicht im vorbereiteten Zustand.</span><span class="sxs-lookup"><span data-stu-id="44ea1-177"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ea1-178">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="44ea1-178">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="44ea1-179">Beim Ersetzen eines Datensatzes, für den noch keine Schreibsperre zugewiesen wurde, kann zum Zeitpunkt des Updates ein Schreib Konflikt auftreten.</span><span class="sxs-lookup"><span data-stu-id="44ea1-179">A record replacement operation for which a write lock was not already allocated can encounter a write conflict at the time of update.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="44ea1-180">Bei Erfolg ist der Aktualisierungs Vorgang für den Cursor abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="44ea1-180">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="44ea1-181">Wenn für die Tabelle eine automatische Inkrement-Spalte definiert ist, wird dieser Wert für eingefügte Datensätze festgelegt.</span><span class="sxs-lookup"><span data-stu-id="44ea1-181">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="44ea1-182">Wenn für die Tabelle eine Versions Spalte definiert ist, wird der Wert für neu eingefügte Datensätze initialisiert oder jedes Mal, wenn ein Datensatz ersetzt wird, um 1 erhöht.</span><span class="sxs-lookup"><span data-stu-id="44ea1-182">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="44ea1-183">Alle Indizes, einschließlich gruppierter und nicht gruppierter Indizes, werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="44ea1-183">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="44ea1-184">Bei einem Fehler werden keine Änderungen an der Datenbank vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="44ea1-184">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="44ea1-185">Vor dem Einfügen und vor dem ersetzen wurden möglicherweise Rückruf Funktionen aufgerufen, aber nach INSERT-und After-replace-Rückrufe wurden die Rückrufe nicht aufgerufen, da letztere nicht bewirken kann, dass ein Update fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="44ea1-185">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="44ea1-186">Der Kopier Puffer des Cursors verbleibt im vorbereiteten Zustand, sodass die Möglichkeit besteht, die Probleme, die zu Fehlern geführt haben, inkrementell zu korrigieren und den Aktualisierungs Vorgang zu wiederholen.</span><span class="sxs-lookup"><span data-stu-id="44ea1-186">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="44ea1-187">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44ea1-187">Remarks</span></span>

<span data-ttu-id="44ea1-188">Einschränkungen der Daten Satz Größe werden von [jetsetcolumn](./jetsetcolumn-function.md)erzwungen, nicht im Allgemeinen durch [jetupdate](./jetupdate-function.md).</span><span class="sxs-lookup"><span data-stu-id="44ea1-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by [JetUpdate](./jetupdate-function.md).</span></span> <span data-ttu-id="44ea1-189">Die einzige Ausnahme ist, wenn das Flag für die JET_bitUpdateCheckESE97Compatibility Kompatibilität verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44ea1-189">The only exception is when the JET_bitUpdateCheckESE97Compatibility compatibility flag is being used.</span></span> <span data-ttu-id="44ea1-190">In diesem Fall wird der gesamte Datensatz geprüft, da ein einzelner [jetsetcolumn](./jetsetcolumn-function.md) -Vorgang, der den Grenzwert überschritten hat, durch einen nachfolgenden Befehl von [jetsetcolumn](./jetsetcolumn-function.md)kompensiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="44ea1-190">In this case, the whole record is checked since an individual [JetSetColumn](./jetsetcolumn-function.md) operation that exceeded the limit may be compensated by a subsequent call to [JetSetColumn](./jetsetcolumn-function.md).</span></span>

<span data-ttu-id="44ea1-191">Weitere Informationen finden Sie im Abschnitt "Hinweise" in [jetupdate](./jetupdate-function.md) .</span><span class="sxs-lookup"><span data-stu-id="44ea1-191">See the Remarks section in [JetUpdate](./jetupdate-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="44ea1-192">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44ea1-192">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44ea1-193"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="44ea1-193"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="44ea1-194">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="44ea1-194">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ea1-195"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="44ea1-195"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="44ea1-196">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="44ea1-196">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ea1-197"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="44ea1-197"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="44ea1-198">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="44ea1-198">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44ea1-199"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="44ea1-199"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="44ea1-200">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="44ea1-200">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44ea1-201"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="44ea1-201"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="44ea1-202">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="44ea1-202">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="44ea1-203">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="44ea1-203">See Also</span></span>

[<span data-ttu-id="44ea1-204">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="44ea1-204">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="44ea1-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="44ea1-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="44ea1-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="44ea1-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="44ea1-207">Jetdelete</span><span class="sxs-lookup"><span data-stu-id="44ea1-207">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="44ea1-208">Jetprepareupdate</span><span class="sxs-lookup"><span data-stu-id="44ea1-208">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="44ea1-209">Jetregistercallback</span><span class="sxs-lookup"><span data-stu-id="44ea1-209">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="44ea1-210">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="44ea1-210">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="44ea1-211">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="44ea1-211">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="44ea1-212">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="44ea1-212">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="44ea1-213">Jetsetcolumns</span><span class="sxs-lookup"><span data-stu-id="44ea1-213">JetSetColumns</span></span>](./jetsetcolumns-function.md)
