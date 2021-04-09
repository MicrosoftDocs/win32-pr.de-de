---
description: 'Weitere Informationen zu: jetupdate-Funktion'
title: JetUpdate-Funktion
TOCTitle: JetUpdate Function
ms:assetid: 6c9a53d0-46bc-403b-bdba-9020e023c14a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269288(v=EXCHG.10)
ms:contentKeyID: 32765580
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38e17c5bc5ac32ab3b904456f2d97aa465fca670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862892"
---
# <a name="jetupdate-function"></a><span data-ttu-id="00b29-103">JetUpdate-Funktion</span><span class="sxs-lookup"><span data-stu-id="00b29-103">JetUpdate Function</span></span>


<span data-ttu-id="00b29-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="00b29-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate-function"></a><span data-ttu-id="00b29-105">JetUpdate-Funktion</span><span class="sxs-lookup"><span data-stu-id="00b29-105">JetUpdate Function</span></span>

<span data-ttu-id="00b29-106">Die **jetupdate** -Funktion führt einen Aktualisierungs Vorgang aus, einschließlich des Einfügens einer neuen Zeile in eine Tabelle oder der Aktualisierung einer vorhandenen Zeile.</span><span class="sxs-lookup"><span data-stu-id="00b29-106">The **JetUpdate** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="00b29-107">Das Löschen einer Tabellenzeile erfolgt durch Aufrufen von [jetdelete](./jetdelete-function.md).</span><span class="sxs-lookup"><span data-stu-id="00b29-107">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="00b29-108">**Jetupdate** ist der letzte Schritt beim Ausführen eines Einfügevorgangs oder eines Updates.</span><span class="sxs-lookup"><span data-stu-id="00b29-108">**JetUpdate** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="00b29-109">Das Update wird zunächst durch Aufrufen von [jetprepareupdate](./jetprepareupdate-function.md) und anschließendes Aufrufen von [jetsetcolumn](./jetsetcolumn-function.md) oder [jetsetcolumns](./jetsetcolumns-function.md) gestartet, um den Daten Satz Status festzulegen.</span><span class="sxs-lookup"><span data-stu-id="00b29-109">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="00b29-110">Schließlich wird **jetupdate** aufgerufen, um den Aktualisierungs Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="00b29-110">Finally, **JetUpdate** is called to complete the update operation.</span></span> <span data-ttu-id="00b29-111">Indizes werden nur von **jetupdate** oder [JetUpdate2](./jetupdate2-function.md)und nicht von [jetsetcolumn](./jetsetcolumn-function.md) oder [jetsetcolumns](./jetsetcolumns-function.md)aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="00b29-111">Indexes are updated only by **JetUpdate** or [JetUpdate2](./jetupdate2-function.md), and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="00b29-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="00b29-112">Parameters</span></span>

<span data-ttu-id="00b29-113">*-sid*</span><span class="sxs-lookup"><span data-stu-id="00b29-113">*sesid*</span></span>

<span data-ttu-id="00b29-114">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00b29-114">The session to use for this call.</span></span>

<span data-ttu-id="00b29-115">*TableID*</span><span class="sxs-lookup"><span data-stu-id="00b29-115">*tableid*</span></span>

<span data-ttu-id="00b29-116">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00b29-116">The cursor to use for this call.</span></span>

<span data-ttu-id="00b29-117">*pvbookmark*</span><span class="sxs-lookup"><span data-stu-id="00b29-117">*pvBookmark*</span></span>

<span data-ttu-id="00b29-118">Zeiger auf ein zurück gegebenes Lesezeichen für eine eingefügte Zeile.</span><span class="sxs-lookup"><span data-stu-id="00b29-118">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="00b29-119">*cbbookmark*</span><span class="sxs-lookup"><span data-stu-id="00b29-119">*cbBookmark*</span></span>

<span data-ttu-id="00b29-120">Größe des Puffers, auf den *pvbookmark* zeigt.</span><span class="sxs-lookup"><span data-stu-id="00b29-120">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="00b29-121">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="00b29-121">*pcbActual*</span></span>

<span data-ttu-id="00b29-122">Die zurückgegebene Größe des Lesezeichens für die eingefügte Zeile, die in *pvbookmark* zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="00b29-122">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

### <a name="return-value"></a><span data-ttu-id="00b29-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00b29-123">Return Value</span></span>

<span data-ttu-id="00b29-124">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="00b29-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="00b29-125">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="00b29-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="00b29-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="00b29-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="00b29-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00b29-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00b29-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="00b29-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="00b29-129">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="00b29-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00b29-130">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="00b29-130">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="00b29-131">Der angegebene Puffer für das Daten Satz-Lesezeichen ist nicht ausreichend groß genug zum Speichern des Daten Satz-Lesezeichens.</span><span class="sxs-lookup"><span data-stu-id="00b29-131">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00b29-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="00b29-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="00b29-133">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="00b29-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00b29-134">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="00b29-134">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="00b29-135">Identisch mit JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="00b29-135">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00b29-136">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="00b29-136">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="00b29-137">Der Aktualisierungs Vorgang erfordert eine Vergrößerung der Datenbankdatei oder die Protokolldatei Zuordnung, aber das Laufwerk, auf dem sich die Datenbankdatei oder die Protokoll Reihe befindet, ist voll.</span><span class="sxs-lookup"><span data-stu-id="00b29-137">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="00b29-138">Alternativ dazu befindet sich die Datenbankdatei auf einem auf FAT32 formatierten Volume, und die Datenbankdatei ist bereits 4gbytes, der Grenzwert pro Datei für FAT32.</span><span class="sxs-lookup"><span data-stu-id="00b29-138">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00b29-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="00b29-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="00b29-140">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="00b29-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="00b29-141"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00b29-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00b29-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="00b29-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="00b29-143">Der angegebene <em>prep</em> -Parameter in der <a href="gg269339(v=exchg.10).md">jetprepareupdate</a> -Funktion ist kein gültiges Flag.</span><span class="sxs-lookup"><span data-stu-id="00b29-143">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00b29-144">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="00b29-144">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="00b29-145">Ein Index Schlüssel für diesen Datensatz ist ein Duplikat eines anderen Index Schlüssels für einen anderen Datensatz, der bereits in der Tabelle vorhanden ist, und der Index lässt keine Duplikate zu.</span><span class="sxs-lookup"><span data-stu-id="00b29-145">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00b29-146">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="00b29-146">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="00b29-147">Der eingefügte oder aktualisierte Datensatz weist mindestens einen Index auf, für den der generierte Schlüssel die maximal zulässige Größe überschreiten würde.</span><span class="sxs-lookup"><span data-stu-id="00b29-147">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="00b29-148">Dies hat zur Folge, dass der Vorgang das Abschneiden von Schlüsseln nicht verhindern konnte.</span><span class="sxs-lookup"><span data-stu-id="00b29-148">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00b29-149">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="00b29-149">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="00b29-150">Der eingefügte oder aktualisierte Datensatz verfügt über eine indizierte mehrwertige Spalte mit zwei oder Mehrwerten, die innerhalb der für den Index festgelegten maximalen Längen Schlüsselgröße identisch sind.</span><span class="sxs-lookup"><span data-stu-id="00b29-150">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="00b29-151">Folglich hat der Datensatz zwei identische Einträge im Index, die ungültig sind.</span><span class="sxs-lookup"><span data-stu-id="00b29-151">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00b29-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="00b29-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="00b29-153">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="00b29-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00b29-154">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="00b29-154">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="00b29-155">Mindestens eine Spalte im Datensatz, die eingefügt werden soll, oder der aktualisierte Zustand eines zu ersetzenden Datensatzes ist <strong>null</strong> . Dies verstößt gegen die definierte Einschränkung für diese Spalten.</span><span class="sxs-lookup"><span data-stu-id="00b29-155">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00b29-156">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="00b29-156">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="00b29-157">Mindestens ein Index ist so definiert, dass kein <strong>null</strong> -Schlüssel zulässig ist, und der eingefügte oder aktualisierte Status eines Datensatzes, der ersetzt wird, verstößt gegen diese definierte Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="00b29-157">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00b29-158">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="00b29-158">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="00b29-159">Der Primärschlüssel wurde durch einen Daten Satz Ersetzungs Vorgang aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="00b29-159">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="00b29-160">Aktualisierungen an Primärschlüssel Spalten müssen durch Löschen des vorhandenen Datensatzes und Einfügen eines neuen Datensatzes mit den gewünschten Daten erfolgen.</span><span class="sxs-lookup"><span data-stu-id="00b29-160">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00b29-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="00b29-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="00b29-162">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00b29-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00b29-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="00b29-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="00b29-164">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00b29-164">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="00b29-165"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00b29-165"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00b29-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="00b29-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="00b29-167">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="00b29-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00b29-168">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="00b29-168">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="00b29-169">Es ist nicht zulässig, ein Update zu versuchen, wenn es innerhalb des Gültigkeits Bereichs einer schreibgeschützten Transaktion liegt.</span><span class="sxs-lookup"><span data-stu-id="00b29-169">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="00b29-170">Eine schreibgeschützte Transaktion ist eine Transaktion, die mit einem <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> -Aufrufvorgang mit JET_bitTransactionReadOnly gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="00b29-170">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span></p>
<p><span data-ttu-id="00b29-171"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00b29-171"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00b29-172">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="00b29-172">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="00b29-173"><a href="gg269339(v=exchg.10).md">Jetprepareupdate</a> wurde mit JET_prepCancel aufgerufen, aber der Cursor befand sich nicht im vorbereiteten Zustand.</span><span class="sxs-lookup"><span data-stu-id="00b29-173"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00b29-174">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="00b29-174">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="00b29-175">Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher vorhanden ist, um transaktionale Informationen zum Update beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="00b29-175">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00b29-176">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="00b29-176">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="00b29-177">Eine andere Sitzung hat den Datensatz bereits für das Update gesperrt.</span><span class="sxs-lookup"><span data-stu-id="00b29-177">Another session has previously locked the record for update.</span></span> <span data-ttu-id="00b29-178">Das von dieser Sitzung versuchte Update schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="00b29-178">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="00b29-179">Bei Erfolg ist der Aktualisierungs Vorgang für den Cursor abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="00b29-179">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="00b29-180">Wenn für die Tabelle eine automatische Inkrement-Spalte definiert ist, wird dieser Wert für eingefügte Datensätze festgelegt.</span><span class="sxs-lookup"><span data-stu-id="00b29-180">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="00b29-181">Wenn für die Tabelle eine Versions Spalte definiert ist, wird der Wert für neu eingefügte Datensätze initialisiert oder jedes Mal, wenn ein Datensatz ersetzt wird, um 1 erhöht.</span><span class="sxs-lookup"><span data-stu-id="00b29-181">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="00b29-182">Alle Indizes, einschließlich gruppierter und nicht gruppierter Indizes, werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="00b29-182">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="00b29-183">Bei einem Fehler werden keine Änderungen an der Datenbank vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="00b29-183">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="00b29-184">Vor dem Einfügen und vor dem ersetzen wurden möglicherweise Rückruf Funktionen aufgerufen, aber nach INSERT-und After-replace-Rückrufe wurden die Rückrufe nicht aufgerufen, da letztere nicht bewirken kann, dass ein Update fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="00b29-184">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="00b29-185">Der Kopier Puffer des Cursors verbleibt im vorbereiteten Zustand, sodass die Möglichkeit besteht, die Probleme, die zu Fehlern geführt haben, inkrementell zu korrigieren und den Aktualisierungs Vorgang zu wiederholen.</span><span class="sxs-lookup"><span data-stu-id="00b29-185">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="00b29-186">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00b29-186">Remarks</span></span>

<span data-ttu-id="00b29-187">Rückruf Funktionen können registriert werden, um vor oder nach dem Einfügen und vor oder nach dem Update aufgerufen zu werden.</span><span class="sxs-lookup"><span data-stu-id="00b29-187">Callback functions can be registered to be called before or after insert, and before or after update.</span></span>

<span data-ttu-id="00b29-188">Einschränkungen der Daten Satz Größe werden von [jetsetcolumn](./jetsetcolumn-function.md)erzwungen, nicht im Allgemeinen durch **jetupdate**.</span><span class="sxs-lookup"><span data-stu-id="00b29-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by **JetUpdate**.</span></span>

<span data-ttu-id="00b29-189">Es ist wichtig, die Auswirkungen der Ausführung einer großen Anzahl von Aktualisierungs Vorgängen in einer einzelnen Transaktion zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="00b29-189">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="00b29-190">Jedes Update der Datenbank muss von der Datenbank-Engine im Versionsspeicher nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="00b29-190">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="00b29-191">Der Versionsspeicher enthält einen Live Datensatz aller verschiedenen Versionen der einzelnen Datensatz-oder Indexeinträge in der Datenbank, die von allen aktiven Transaktionen angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="00b29-191">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="00b29-192">Diese Versionen werden zur Unterstützung der Parallelitäts Steuerung mit mehreren Versionsverwaltung verwendet, die von der Datenbank-Engine verwendet wird, um Transaktionen mithilfe der Momentaufnahme Isolation zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="00b29-192">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="00b29-193">Sobald die Datenbank-Engine die Ressourcen erschöpft hat, die zum Speichern dieser Versionen verwendet werden, kann Sie keine weiteren Änderungen mehr akzeptieren, bis einige Transaktionen abgeschlossen sind, damit diese Ressourcen freigegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="00b29-193">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="00b29-194">Wenn sich die Engine in diesem Zustand befindet, schlagen alle Updates mit Jet_errVersionStoreOutOfMemory fehl.</span><span class="sxs-lookup"><span data-stu-id="00b29-194">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="00b29-195">Die Ressourcen, die für die Datenbank-Engine zum Speichern dieser Versionen verfügbar sind, können mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit [JET_paramMaxVerPages](./resource-parameters.md) und [JET_paramGlobalMinVerPages](./resource-parameters.md)gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="00b29-195">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramMaxVerPages](./resource-parameters.md) and [JET_paramGlobalMinVerPages](./resource-parameters.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="00b29-196">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00b29-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00b29-197"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="00b29-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="00b29-198">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="00b29-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00b29-199"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="00b29-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="00b29-200">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="00b29-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00b29-201"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="00b29-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="00b29-202">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="00b29-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00b29-203"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="00b29-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="00b29-204">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="00b29-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00b29-205"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="00b29-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="00b29-206">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="00b29-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="00b29-207">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="00b29-207">See Also</span></span>

[<span data-ttu-id="00b29-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="00b29-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="00b29-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="00b29-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="00b29-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="00b29-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="00b29-211">Jetdelete</span><span class="sxs-lookup"><span data-stu-id="00b29-211">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="00b29-212">Jetprepareupdate</span><span class="sxs-lookup"><span data-stu-id="00b29-212">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="00b29-213">Jetregistercallback</span><span class="sxs-lookup"><span data-stu-id="00b29-213">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="00b29-214">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="00b29-214">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="00b29-215">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="00b29-215">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="00b29-216">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="00b29-216">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="00b29-217">Jetsetcolumns</span><span class="sxs-lookup"><span data-stu-id="00b29-217">JetSetColumns</span></span>](./jetsetcolumns-function.md)  
[<span data-ttu-id="00b29-218">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="00b29-218">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="00b29-219">System Parameter</span><span class="sxs-lookup"><span data-stu-id="00b29-219">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
