---
description: 'Weitere Informationen finden Sie hier: jetretrievecolumschlag-Funktion'
title: JetRetrieveColumns-Funktion
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 515be3a36932c9a56843f51d2e1b32a41ca94e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218129"
---
# <a name="jetretrievecolumns-function"></a><span data-ttu-id="449d1-103">JetRetrieveColumns-Funktion</span><span class="sxs-lookup"><span data-stu-id="449d1-103">JetRetrieveColumns Function</span></span>


<span data-ttu-id="449d1-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="449d1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumns-function"></a><span data-ttu-id="449d1-105">JetRetrieveColumns-Funktion</span><span class="sxs-lookup"><span data-stu-id="449d1-105">JetRetrieveColumns Function</span></span>

<span data-ttu-id="449d1-106">Die **jetretrievecolenumns** -Funktion ruft in einem einzelnen Vorgang mehrere Spaltenwerte aus dem aktuellen Datensatz ab.</span><span class="sxs-lookup"><span data-stu-id="449d1-106">The **JetRetrieveColumns** function retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="449d1-107">Ein Array von [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) Strukturen wird verwendet, um den Satz von Spaltenwerten zu beschreiben, die abgerufen werden sollen, und um Ausgabepuffer für jeden abzurufenden Spaltenwert zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="449d1-107">An array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="449d1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="449d1-108">Parameters</span></span>

<span data-ttu-id="449d1-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="449d1-109">*sesid*</span></span>

<span data-ttu-id="449d1-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="449d1-110">The session to use for this call.</span></span>

<span data-ttu-id="449d1-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="449d1-111">*tableid*</span></span>

<span data-ttu-id="449d1-112">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="449d1-112">The cursor to use for this call.</span></span>

<span data-ttu-id="449d1-113">*predreifach-ecolumschlag*</span><span class="sxs-lookup"><span data-stu-id="449d1-113">*pretrievecolumn*</span></span>

<span data-ttu-id="449d1-114">Ein Zeiger auf ein Array aus mindestens einer [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="449d1-114">A pointer to an array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="449d1-115">Jede Struktur enthält Beschreibungen, welche Spaltenwerte abgerufen werden sollen und wo die zurückgegebenen Daten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="449d1-115">Each structure includes descriptions of which column value to retrieve and where to store returned data.</span></span>

<span data-ttu-id="449d1-116">*"kretrevecolumschlag"*</span><span class="sxs-lookup"><span data-stu-id="449d1-116">*cretrievecolumn*</span></span>

<span data-ttu-id="449d1-117">Die Anzahl der [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) Strukturen im Array, angegeben durch *prezevecolenumn*.</span><span class="sxs-lookup"><span data-stu-id="449d1-117">The number of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures in the array given by *pretrievecolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="449d1-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="449d1-118">Return Value</span></span>

<span data-ttu-id="449d1-119">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="449d1-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="449d1-120">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="449d1-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="449d1-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="449d1-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="449d1-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="449d1-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="449d1-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="449d1-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="449d1-124">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="449d1-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="449d1-125">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="449d1-125">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="449d1-126">Ein ungültiger Wert für eine mehrwertige spaltensequenznummer wurde in "pretinfo- &gt; itagsequence" übergeben.</span><span class="sxs-lookup"><span data-stu-id="449d1-126">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="449d1-127">Gültige Werte für die Sequenznummern der mehrwertigen Spaltenwerte sind 1 oder höher.</span><span class="sxs-lookup"><span data-stu-id="449d1-127">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="449d1-128">Der Wert 0 (null) ist für diese Funktion gültig, aber für <a href="gg269198(v=exchg.10).md">jetretrievecolumschlag</a>ungültig.</span><span class="sxs-lookup"><span data-stu-id="449d1-128">A value of 0 (zero) is valid for this function but is invalid for <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="449d1-129">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="449d1-129">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="449d1-130">Die angegebene Spalten-ID liegt außerhalb der zulässigen Beschränkungen einer Spalten-ID.</span><span class="sxs-lookup"><span data-stu-id="449d1-130">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="449d1-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="449d1-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="449d1-132">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="449d1-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="449d1-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="449d1-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="449d1-134">Die von der angegebenen Spalte beschriebene Spalte ist in der <em>Tabelle nicht vorhanden</em> .</span><span class="sxs-lookup"><span data-stu-id="449d1-134">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="449d1-135">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="449d1-135">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="449d1-136">Als Teil Zeichenfolgen indizierte Spalten können nicht aus dem Index abgerufen werden, da in jedem Index Eintrag normalerweise nur ein kleiner Teil der Spalte vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="449d1-136">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="449d1-137">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="449d1-137">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="449d1-138">In einigen Fällen muss der für die Spalte abrufen angegebene Puffer ausreichend groß sein, um eine beliebige Menge an Spaltenwerten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="449d1-138">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="449d1-139">So werden z. b. die aktualisierbaren Spalten für die Spalten Anpassung angepasst, damit Sie für den Transaktionskontext der aufrufenden Sitzung konsistent sind. diese Anpassung erfordert den vom Aufrufer bereitgestellten Puffer.</span><span class="sxs-lookup"><span data-stu-id="449d1-139">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="449d1-140">Wenn nicht genügend Pufferspeicher bereitgestellt wird, wird JET_errInvalidBufferSize zurückgegeben, und es werden keine Spaltendaten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="449d1-140">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="449d1-141">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="449d1-141">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="449d1-142">Die angegebenen Optionen sind unbekannt oder eine ungültige Kombination bekannter Biteinstellungen.</span><span class="sxs-lookup"><span data-stu-id="449d1-142">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="449d1-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="449d1-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="449d1-144">Mindestens einer der angegebenen Parameter ist falsch.</span><span class="sxs-lookup"><span data-stu-id="449d1-144">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="449d1-145">Dies kann vorkommen, wenn "retinfo. cbStruct" kleiner ist als die Größe der <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="449d1-145">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="449d1-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="449d1-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="449d1-147">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="449d1-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="449d1-148"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="449d1-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="449d1-149">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="449d1-149">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="449d1-150">Der Cursor ist nicht in einem Datensatz positioniert.</span><span class="sxs-lookup"><span data-stu-id="449d1-150">The cursor is not positioned on a record.</span></span> <span data-ttu-id="449d1-151">Dafür sind viele verschiedene Gründe möglich.</span><span class="sxs-lookup"><span data-stu-id="449d1-151">This can happen for many different reasons.</span></span> <span data-ttu-id="449d1-152">Dies ist beispielsweise der Fall, wenn der Cursor aktuell nach dem letzten Datensatz im aktuellen Index positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="449d1-152">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="449d1-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="449d1-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="449d1-154">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="449d1-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="449d1-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="449d1-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="449d1-156">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="449d1-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="449d1-157">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="449d1-157">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="449d1-158">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="449d1-158">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="449d1-159"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="449d1-159"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="449d1-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="449d1-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="449d1-161">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="449d1-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="449d1-162">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="449d1-162">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="449d1-163">Der gesamte Spaltenwert konnte nicht abgerufen werden, da der angegebene Puffer kleiner ist als die Größe der Spalte.</span><span class="sxs-lookup"><span data-stu-id="449d1-163">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="449d1-164">Bei Erfolg werden Spaltendaten und Spaltengröße in den bereitgestellten Puffern zurückgegeben, die Unterarray von [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) Strukturen beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="449d1-164">On success, columns data and column size are returned in provided buffers described in array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="449d1-165">Wenn eine *itagsequence* auf 0 (null) festgelegt wurde, um anzugeben, dass die Anzahl der Instanzen eines mehrwertigen Felds anstelle von Spaltendaten erwünscht war, wird die Anzahl der Instanzen einer mehrwertigen Spalte im Feld *itagsequence* selbst zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="449d1-165">If an *itagSequence* was set to 0 (zero) to indicate that the number of instances of a multi-valued field was desired instead of column data, then the number of instances of a multi-valued column is returned in the *itagSequence* field itself.</span></span> <span data-ttu-id="449d1-166">Jede [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) Struktur verfügt über ein Fehler Feld, das Warnungen für die abgerufene Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="449d1-166">Each [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure has an error field that contains warnings for the column retrieved.</span></span> <span data-ttu-id="449d1-167">Wenn die Spalte den Wert **null** hat, wird der Fehlercode auf JET_wrnColumnNull festgelegt.</span><span class="sxs-lookup"><span data-stu-id="449d1-167">If the column was **NULL** valued, then the error code will be set to JET_wrnColumnNull.</span></span>

<span data-ttu-id="449d1-168">Bei einem Fehler wird die Cursorposition unverändert bleiben, und es werden keine Daten in den bereitgestellten Puffer kopiert.</span><span class="sxs-lookup"><span data-stu-id="449d1-168">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="449d1-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="449d1-169">Remarks</span></span>

<span data-ttu-id="449d1-170">**Jetretrievecolenns** unterstützt ein Feature, das [jetretrievecolenn](./jetretrievecolumn-function.md) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="449d1-170">**JetRetrieveColumns** supports one feature that [JetRetrieveColumn](./jetretrievecolumn-function.md) does not.</span></span> <span data-ttu-id="449d1-171">Mit dieser Option können Sie die Anzahl der Instanzen einer mehrwertigen Spalte abrufen.</span><span class="sxs-lookup"><span data-stu-id="449d1-171">This is the ability to retrieve the number of instances of a multi-valued column.</span></span> <span data-ttu-id="449d1-172">Der Zweck dieses Features besteht darin, dass eine Anwendung alle Werte einer Spalte abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="449d1-172">The purpose of this feature is to allow an application to retrieve all values of a column.</span></span> <span data-ttu-id="449d1-173">Dies kann erreicht werden, indem zuerst die Anzahl der Werte bestimmt wird, die eine Spalte aufweist.</span><span class="sxs-lookup"><span data-stu-id="449d1-173">This can be done by first determining the number of values that a column has.</span></span> <span data-ttu-id="449d1-174">Anschließend können Ihre Längen durch das erneute Aufrufen von **jetretrievecolumschlag** durch eine [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) Struktur bestimmt werden, die jedem Wert zugeordnet ist, um die Länge der Spaltendaten zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="449d1-174">Next, their lengths can be determined by calling **JetRetrieveColumns** again with one [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure allocated for each value to determine the length of column data.</span></span> <span data-ttu-id="449d1-175">Dies kann erreicht werden, indem **null**_pvData_ -Zeiger mit *cbmax* von 0 (null) übergeben und die Spaltenlänge in *cbactial* abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="449d1-175">This can be done by passing **NULL**_pvData_ pointers with *cbMax* of 0 (zero) and retrieving the column length in *cbActual*.</span></span> <span data-ttu-id="449d1-176">Der dritte und letzte-Befehl können mit zugeordnetem Arbeitsspeicher für die Spaltenwert Daten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="449d1-176">The third and last call can be made with allocated memory for the column value data.</span></span>

<span data-ttu-id="449d1-177">Wenn eine abgerufene Spalte aufgrund eines unzureichenden Längen Puffers abgeschnitten wird, gibt die API JET_wrnBufferTruncated zurück.</span><span class="sxs-lookup"><span data-stu-id="449d1-177">If any column retrieved is truncated due to an insufficient length buffer, then the API will return JET_wrnBufferTruncated.</span></span> <span data-ttu-id="449d1-178">Andere Fehler, JET_wrnColumnNull werden jedoch nur im Feld Fehler in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="449d1-178">However, other errors, JET_wrnColumnNull are returned only in the error field in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="449d1-179">Der Grund hierfür ist, dass Anwendungen häufig sicherstellen möchten, dass alle Daten abgerufen wurden, und diese Fehlermeldung von **jetretrievecolumschlag** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="449d1-179">The reason for this is that applications often want to ensure that all data has been retrieved and returning this error from **JetRetrieveColumns** facilitates this understanding.</span></span>

#### <a name="requirements"></a><span data-ttu-id="449d1-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="449d1-180">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="449d1-181"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="449d1-181"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="449d1-182">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="449d1-182">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="449d1-183"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="449d1-183"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="449d1-184">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="449d1-184">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="449d1-185"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="449d1-185"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="449d1-186">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="449d1-186">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="449d1-187"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="449d1-187"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="449d1-188">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="449d1-188">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="449d1-189"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="449d1-189"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="449d1-190">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="449d1-190">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="449d1-191">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="449d1-191">See Also</span></span>

[<span data-ttu-id="449d1-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="449d1-192">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="449d1-193">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="449d1-193">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="449d1-194">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="449d1-194">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="449d1-195">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="449d1-195">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="449d1-196">Jetenreeratecolumschlag</span><span class="sxs-lookup"><span data-stu-id="449d1-196">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="449d1-197">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="449d1-197">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="449d1-198">Jetsetcolumns</span><span class="sxs-lookup"><span data-stu-id="449d1-198">JetSetColumns</span></span>](./jetsetcolumns-function.md)
