---
description: 'Weitere Informationen über: jetsetcolumns-Funktion'
title: JetSetColumns-Funktion
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4535b66064c19257f4bb7b51b059453660916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128160"
---
# <a name="jetsetcolumns-function"></a><span data-ttu-id="7bac0-103">JetSetColumns-Funktion</span><span class="sxs-lookup"><span data-stu-id="7bac0-103">JetSetColumns Function</span></span>


<span data-ttu-id="7bac0-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7bac0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumns-function"></a><span data-ttu-id="7bac0-105">JetSetColumns-Funktion</span><span class="sxs-lookup"><span data-stu-id="7bac0-105">JetSetColumns Function</span></span>

<span data-ttu-id="7bac0-106">Die **jetsetcolumns** -Funktion ähnelt dem Verhalten von [jetsetcolumn](./jetsetcolumn-function.md) , ermöglicht einer Anwendung jedoch das Festlegen mehrerer Spaltenwerte in einem einzelnen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7bac0-106">The **JetSetColumns** function is similar in behavior to [JetSetColumn](./jetsetcolumn-function.md) but allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="7bac0-107">Ein Array von [JET_SETCOLUMN](./jet-setcolumn-structure.md) Strukturen wird verwendet, um den Satz von Spaltenwerten zu beschreiben, die festgelegt werden sollen, und um Eingabepuffer für jeden festzulegenden Spaltenwert zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7bac0-107">An array of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="7bac0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bac0-108">Parameters</span></span>

<span data-ttu-id="7bac0-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="7bac0-109">*sesid*</span></span>

<span data-ttu-id="7bac0-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bac0-110">The session to use for this call.</span></span>

<span data-ttu-id="7bac0-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="7bac0-111">*tableid*</span></span>

<span data-ttu-id="7bac0-112">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bac0-112">The cursor to use for this call.</span></span>

<span data-ttu-id="7bac0-113">*psetcolumn*</span><span class="sxs-lookup"><span data-stu-id="7bac0-113">*psetcolumn*</span></span>

<span data-ttu-id="7bac0-114">Ein Zeiger auf ein Array aus mindestens einer [JET_SETCOLUMN](./jet-setcolumn-structure.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7bac0-114">A pointer to an array of one or more [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures.</span></span> <span data-ttu-id="7bac0-115">Jede Struktur enthält Beschreibungen, welcher Spaltenwert festgelegt werden soll und von wo die Spaltendaten festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7bac0-115">Each structure includes descriptions of which column value to set and from where to get column data to set.</span></span>

<span data-ttu-id="7bac0-116">*csetcolumn*</span><span class="sxs-lookup"><span data-stu-id="7bac0-116">*csetcolumn*</span></span>

<span data-ttu-id="7bac0-117">Die Anzahl der [JET_SETCOLUMN](./jet-setcolumn-structure.md) Strukturen in dem Array, das von *psetcolumn* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7bac0-117">The number of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures in the array given by *psetcolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="7bac0-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7bac0-118">Return Value</span></span>

<span data-ttu-id="7bac0-119">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="7bac0-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7bac0-120">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7bac0-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bac0-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7bac0-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="7bac0-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bac0-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-123">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="7bac0-123">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="7bac0-124">Die angegebene Spalten-ID liegt außerhalb der zulässigen Beschränkungen einer Spalten-ID.</span><span class="sxs-lookup"><span data-stu-id="7bac0-124">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bac0-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="7bac0-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="7bac0-126">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="7bac0-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-127">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="7bac0-127">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="7bac0-128">Identisch mit JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="7bac0-128">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bac0-129">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="7bac0-129">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="7bac0-130">Die von der angegebenen Spalte beschriebene Spalte ist in der <em>Tabelle nicht vorhanden</em> .</span><span class="sxs-lookup"><span data-stu-id="7bac0-130">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-131">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="7bac0-131">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="7bac0-132">Es wurde ein unzulässiger Versuch unternommen, einen Long-Wert während eines INSERT-Vorgangs zum Löschen des ursprünglichen Updates zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7bac0-132">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bac0-133">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="7bac0-133">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="7bac0-134">Die angegebenen Spaltenwert Daten, die im Eingabepuffer angegeben sind, überschreiten die Größenbeschränkung für eine Spalte mit fester Länge oder für Text oder Binär Spalten mit fester Länge.</span><span class="sxs-lookup"><span data-stu-id="7bac0-134">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="7bac0-135">Dieser Fehler wird auch zurückgegeben, wenn mehr als 1024 Bytes an Daten für eine lange Spalte übergeben werden und das JET_bitSetIntrinsicLV-Flag festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7bac0-135">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="7bac0-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="7bac0-137">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="7bac0-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="7bac0-138">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7bac0-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bac0-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="7bac0-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="7bac0-140">Die angegebene Datengröße für den Spaltenwert stimmt nicht mit dem Wert für den Datentyp mit fester Länge identisch.</span><span class="sxs-lookup"><span data-stu-id="7bac0-140">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-141">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="7bac0-141">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="7bac0-142">Es wurde ein unzulässiger Versuch unternommen, eine automatische Inkrement-Spalte entweder während eines INSERT-oder Update-Vorgangs zu aktualisieren oder eine Versions Spalte während eines Ersetzungs Vorgangs zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7bac0-142">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bac0-143">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="7bac0-143">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="7bac0-144">Die angegebenen Optionen sind unbekannt oder eine ungültige Kombination bekannter Biteinstellungen.</span><span class="sxs-lookup"><span data-stu-id="7bac0-144">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7bac0-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7bac0-146">Die angegebene "psetup Info- &gt; cbStruct" ist keine gültige Größe für die <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> Struktur.</span><span class="sxs-lookup"><span data-stu-id="7bac0-146">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bac0-147">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="7bac0-147">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="7bac0-148">Der Vorgang zum Festlegen der Spalte hat versucht, einen doppelten Wert zu erstellen und entweder JET_bitSetUniqueMultiValues oder JET_bitSetUniqueNormalizedMultiValues anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7bac0-148">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-149">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="7bac0-149">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="7bac0-150">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7bac0-150">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bac0-151">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="7bac0-151">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="7bac0-152">Es wurde ein unzulässiger Versuch unternommen, einen Long-Spaltenwert zu aktualisieren, wenn sich die aufrufende Sitzung nicht in einer Transaktion befand.</span><span class="sxs-lookup"><span data-stu-id="7bac0-152">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-153">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="7bac0-153">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="7bac0-154">Es wurde ein unzulässiger Versuch unternommen, eine nicht-NULL-Spalte auf NULL festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7bac0-154">An illegal attempt was made to set a non-NULL column to NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bac0-155">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="7bac0-155">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="7bac0-156">Der Spaltenwert konnte nicht auf den Wert im Eingabepuffer festgelegt werden, da er dazu geführt hätte, dass der Datensatz seine Größenbeschränkung für die Seitengröße überschreitet.</span><span class="sxs-lookup"><span data-stu-id="7bac0-156">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="7bac0-157">Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> können getrennt von den verbleibenden Daten Satz Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7bac0-157">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="7bac0-158">Allerdings müssen andere Spalten mit dem Datensatz gespeichert werden und können dazu führen, dass die Einschränkung der Daten Satz Größe überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="7bac0-158">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="7bac0-159">Sogar lange Spalten benötigen 5-Byte-Speicherplatz innerhalb des Datensatzes als Verknüpfung, und dies kann dazu führen, dass JET_errRecordTooBig zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7bac0-159">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="7bac0-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="7bac0-161">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bac0-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bac0-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="7bac0-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="7bac0-163">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7bac0-163">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="7bac0-164">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7bac0-164">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="7bac0-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="7bac0-166">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="7bac0-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bac0-167">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="7bac0-167">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="7bac0-168">Der Cursor befindet sich derzeit nicht im Prozess, entweder einen neuen Datensatz einzufügen oder einen vorhandenen Datensatz zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7bac0-168">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="7bac0-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="7bac0-170">Der Spaltenwert im Eingabepuffer hat die für eine Spalte mit variabler Länge konfigurierte maximale Länge überschritten und wurde abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="7bac0-170">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7bac0-171">Bei Erfolg wird für jede Spalte, die in den psetcolumns beschrieben wird, der gewünschte Teil des Spaltenwerts mit Daten festgelegt, die aus dem Eingabepuffer kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="7bac0-171">On success, for each column described in the psetcolumns, the desired portion of the column value is set with data copied from the input buffer.</span></span> <span data-ttu-id="7bac0-172">Das Spalten DataSet wurde möglicherweise abgeschnitten, wenn es die für eine Spalte mit variabler Länge angegebene maximale Länge überschreitet.</span><span class="sxs-lookup"><span data-stu-id="7bac0-172">The column data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="7bac0-173">Bei einem Fehler wird die Cursorposition unverändert bleiben, und im Kopier Puffer werden keine Spaltenwert Daten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7bac0-173">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7bac0-174">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bac0-174">Remarks</span></span>

<span data-ttu-id="7bac0-175">Wenn ein einzelner Satz Spalten Vorgang einen Fehler zurückgibt, gibt der gesamte **jetsetcolumns** -Vorgang einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7bac0-175">If any individual set column operation returns an error then the whole **JetSetColumns** operation will return an error.</span></span> <span data-ttu-id="7bac0-176">Warnungen werden im Allgemeinen in "psetcolumns- \> Error" und nicht im Rückgabecode dieser Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7bac0-176">Warnings, in general, are returned in the psetcolumns-\>error and not in the return code from this function.</span></span> <span data-ttu-id="7bac0-177">Wenn für den letzten Spalten Satz jedoch eine Warnung angezeigt wird, wird diese Warnung von **jetsetcolumns** selbst zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7bac0-177">However, if the last column set has a warning, then this warning will be returned from **JetSetColumns** itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7bac0-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bac0-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-179"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7bac0-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7bac0-180">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7bac0-180">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bac0-181"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7bac0-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7bac0-182">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7bac0-182">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-183"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7bac0-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7bac0-184">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="7bac0-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bac0-185"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="7bac0-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7bac0-186">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7bac0-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bac0-187"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7bac0-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7bac0-188">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7bac0-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7bac0-189">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7bac0-189">See Also</span></span>

[<span data-ttu-id="7bac0-190">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="7bac0-190">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="7bac0-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7bac0-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7bac0-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7bac0-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7bac0-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7bac0-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="7bac0-194">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="7bac0-194">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="7bac0-195">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="7bac0-195">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="7bac0-196">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="7bac0-196">JetSetColumn</span></span>](./jetsetcolumn-function.md)
