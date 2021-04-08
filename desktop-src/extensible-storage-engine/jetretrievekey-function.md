---
description: 'Weitere Informationen finden Sie unter: jetretrievekey-Funktion'
title: JetRetrieveKey-Funktion
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e560d28447b7e5d3798949f47dcadf259e49d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050463"
---
# <a name="jetretrievekey-function"></a><span data-ttu-id="ca282-103">JetRetrieveKey-Funktion</span><span class="sxs-lookup"><span data-stu-id="ca282-103">JetRetrieveKey Function</span></span>


<span data-ttu-id="ca282-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ca282-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievekey-function"></a><span data-ttu-id="ca282-105">JetRetrieveKey-Funktion</span><span class="sxs-lookup"><span data-stu-id="ca282-105">JetRetrieveKey Function</span></span>

<span data-ttu-id="ca282-106">Die **jetretrievekey** -Funktion Ruft den Schlüssel für den Index Eintrag an der aktuellen Position eines Cursors ab.</span><span class="sxs-lookup"><span data-stu-id="ca282-106">The **JetRetrieveKey** function retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="ca282-107">Diese Schlüssel werden durch Aufrufe von [jetmakekey](./jetmakekey-function.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="ca282-107">Such keys are constructed by calls to [JetMakeKey](./jetmakekey-function.md).</span></span> <span data-ttu-id="ca282-108">Der abgerufene Schlüssel kann dann verwendet werden, um den Cursor mithilfe eines [JetSeek](./jetseek-function.md)-Aufrufes effizient an denselben Index Eintrag zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ca282-108">The retrieved key can then be used to efficiently return that cursor to the same index entry by a call to [JetSeek](./jetseek-function.md).</span></span>

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="ca282-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca282-109">Parameters</span></span>

<span data-ttu-id="ca282-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="ca282-110">*sesid*</span></span>

<span data-ttu-id="ca282-111">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca282-111">The session to use for this call.</span></span>

<span data-ttu-id="ca282-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="ca282-112">*tableid*</span></span>

<span data-ttu-id="ca282-113">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca282-113">The cursor to use for this call.</span></span>

<span data-ttu-id="ca282-114">*pvData*</span><span class="sxs-lookup"><span data-stu-id="ca282-114">*pvData*</span></span>

<span data-ttu-id="ca282-115">Der Ausgabepuffer, der den Schlüssel empfängt.</span><span class="sxs-lookup"><span data-stu-id="ca282-115">The output buffer that will receive the key.</span></span>

<span data-ttu-id="ca282-116">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="ca282-116">*cbMax*</span></span>

<span data-ttu-id="ca282-117">Die maximale Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ca282-117">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="ca282-118">*pcbactual*</span><span class="sxs-lookup"><span data-stu-id="ca282-118">*pcbActual*</span></span>

<span data-ttu-id="ca282-119">Empfängt die tatsächliche Größe des Schlüssels in Byte.</span><span class="sxs-lookup"><span data-stu-id="ca282-119">Receives the actual size in bytes of the key.</span></span>

<span data-ttu-id="ca282-120">Wenn dieser Parameter NULL ist, wird die tatsächliche Größe des Schlüssels nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca282-120">If this parameter is NULL then the actual size of the key will not be returned.</span></span>

<span data-ttu-id="ca282-121">Wenn der Ausgabepuffer zu klein ist, wird die tatsächliche Größe des Schlüssels weiterhin zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca282-121">If the output buffer is too small, then the actual size of the key will still be returned.</span></span> <span data-ttu-id="ca282-122">Dies bedeutet, dass diese Zahl größer als die Größe des Ausgabepuffers ist.</span><span class="sxs-lookup"><span data-stu-id="ca282-122">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="ca282-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="ca282-123">*grbit*</span></span>

<span data-ttu-id="ca282-124">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="ca282-124">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca282-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ca282-125">Value</span></span></p></th>
<th><p><span data-ttu-id="ca282-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ca282-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca282-127">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="ca282-127">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="ca282-128">Wenn angegeben, gibt die Engine den Suchschlüssel für den Cursor zurück.</span><span class="sxs-lookup"><span data-stu-id="ca282-128">When specified, the engine will return the search key for the cursor.</span></span> <span data-ttu-id="ca282-129">Der Suchschlüssel wird mithilfe eines oder mehrerer vorheriger Aufrufe von <a href="gg269329(v=exchg.10).md">jetmakekey</a> erstellt, um diesen Schlüssel mithilfe von <a href="gg294103(v=exchg.10).md">JetSeek</a> zu suchen oder einen Index Bereich mithilfe von <a href="gg294112(v=exchg.10).md">jetsetindexrange</a>festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ca282-129">The search key is built up using one or more prior calls to <a href="gg269329(v=exchg.10).md">JetMakeKey</a> for the purposes of seeking to that key using <a href="gg294103(v=exchg.10).md">JetSeek</a> or setting an index range using <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ca282-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca282-130">Return Value</span></span>

<span data-ttu-id="ca282-131">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="ca282-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ca282-132">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ca282-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca282-133">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ca282-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="ca282-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca282-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca282-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ca282-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ca282-136">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ca282-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca282-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ca282-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ca282-138">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="ca282-138">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca282-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ca282-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ca282-140">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="ca282-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="ca282-141">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca282-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca282-142">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="ca282-142">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="ca282-143">Es ist kein aktueller Suchschlüssel für den Cursor vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ca282-143">There is no current search key for the cursor.</span></span> <span data-ttu-id="ca282-144">Dies geschieht für <strong>jetretrievekey</strong> , wenn JET_bitRetrieveCopy angegeben wird und ein Suchschlüssel für diesen Cursor nicht mithilfe eines vorherigen Aufrufes von <a href="gg269329(v=exchg.10).md">jetmakekey</a>erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ca282-144">This will happen for <strong>JetRetrieveKey</strong> if JET_bitRetrieveCopy is specified and a search key has not been constructed for this cursor using a prior call to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span> <span data-ttu-id="ca282-145">Der Suchschlüssel wird durch einen vorherigen-Aufrufvorgang für eine beliebige Navigations-API auf dem Cursor außer <a href="gg294117(v=exchg.10).md">jetmove</a>gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ca282-145">The search key will be deleted by a prior call to any navigational API on the cursor other than <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca282-146">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="ca282-146">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="ca282-147">Der Cursor ist nicht in einem Datensatz positioniert.</span><span class="sxs-lookup"><span data-stu-id="ca282-147">The cursor is not positioned on a record.</span></span> <span data-ttu-id="ca282-148">Dafür sind viele verschiedene Gründe möglich.</span><span class="sxs-lookup"><span data-stu-id="ca282-148">This can happen for many different reasons.</span></span> <span data-ttu-id="ca282-149">Dies ist beispielsweise der Fall, wenn der Cursor aktuell nach dem letzten Datensatz im aktuellen Index positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="ca282-149">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca282-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ca282-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ca282-151">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ca282-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca282-152">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ca282-152">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ca282-153">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca282-153">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca282-154">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="ca282-154">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="ca282-155">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca282-155">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="ca282-156">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca282-156">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca282-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ca282-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ca282-158">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="ca282-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca282-159">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="ca282-159">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="ca282-160">Der Vorgang wurde erfolgreich abgeschlossen, aber der Ausgabepuffer war zu klein, um den gesamten Schlüssel zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="ca282-160">The operation completed successfully, but the output buffer was too small to receive the entire key.</span></span> <span data-ttu-id="ca282-161">Der Ausgabepuffer wurde mit dem gleichen Wert wie der Schlüssel gefüllt.</span><span class="sxs-lookup"><span data-stu-id="ca282-161">The output buffer has been filled with as much of the key as would fit.</span></span> <span data-ttu-id="ca282-162">Die tatsächliche Größe des Schlüssels wurde auch zurückgegeben, wenn dies angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="ca282-162">The actual size of the key has also been returned, if requested.</span></span></p>
<p><span data-ttu-id="ca282-163"><strong>Hinweis</strong>   Dieser Fehler wird nicht zurückgegeben, wenn JET_bitRetrieveCopy angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ca282-163"><strong>Note</strong>   This error will not be returned if JET_bitRetrieveCopy is specified.</span></span> <span data-ttu-id="ca282-164">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="ca282-164">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ca282-165">Bei Erfolg wird der Schlüssel für den Index Eintrag an der aktuellen Position eines Cursors im Ausgabepuffer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca282-165">On success, the key for the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="ca282-166">Wenn JET_wrnBufferTruncated zurückgegeben wird, enthält der Ausgabepuffer den großen Teil des Schlüssels, der in den bereitgestellten Speicherplatz passt, und die tatsächliche Größe des Schlüssels ist genau.</span><span class="sxs-lookup"><span data-stu-id="ca282-166">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the key as will fit in the space provided and the actual size of the key will be accurate.</span></span> <span data-ttu-id="ca282-167">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="ca282-167">No change to the database state will occur.</span></span>

<span data-ttu-id="ca282-168">Bei einem Fehler werden der Status des Ausgabepuffers und die tatsächliche Größe des Schlüssels nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="ca282-168">On failure, the state of the output buffer and the actual size of the key will be undefined.</span></span> <span data-ttu-id="ca282-169">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="ca282-169">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ca282-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca282-170">Remarks</span></span>

<span data-ttu-id="ca282-171">Schlüssel sollten im Allgemeinen als nicht transparente Datenblöcke behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="ca282-171">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="ca282-172">Es sollte nicht versucht werden, die interne Struktur dieser Daten auszunutzen.</span><span class="sxs-lookup"><span data-stu-id="ca282-172">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="ca282-173">Allerdings können die folgenden Eigenschaften für alle ESENT-Schlüssel bekannt sein:</span><span class="sxs-lookup"><span data-stu-id="ca282-173">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="ca282-174">Schlüssel können miteinander verglichen werden, indem die [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) -Funktion verwendet wird, um ihre relative Reihenfolge im Ursprungs Index für die Tabelle der Quell Indexeinträge festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ca282-174">Keys may be compared against each other using [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) function to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="ca282-175">Es ist bedeutungslos, Schlüssel von Indexeinträgen aus verschiedenen Indizes miteinander zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="ca282-175">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="ca282-176">Ein Schlüssel ist immer kleiner oder gleich JET_cbKeyMost (255) Bytes in der Länge vor Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ca282-176">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="ca282-177">Unter Windows Vista und späteren Versionen können Schlüssel größer sein.</span><span class="sxs-lookup"><span data-stu-id="ca282-177">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="ca282-178">Die maximale Größe eines Schlüssels ist gleich dem aktuellen Wert JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="ca282-178">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

<span data-ttu-id="ca282-179">Zusätzlich zu den oben genannten Eigenschaften von ESENT-Schlüsseln ist es wichtig zu beachten, dass sich ein Suchschlüssel von dem Schlüssel für einen Index Eintrag unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="ca282-179">In addition to the above properties of ESENT keys in general, it is important to note that a search key is different from the key for an index entry.</span></span> <span data-ttu-id="ca282-180">Ein Suchschlüssel ist möglicherweise länger als ein normaler Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ca282-180">Specifically, a search key may be longer than an ordinary key.</span></span> <span data-ttu-id="ca282-181">Diese zusätzliche Länge tritt auf, wenn beim Erstellen des Suchschlüssels eine Platzhalter Option verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ca282-181">This extra length occurs when a wildcard option is used while constructing the search key.</span></span> <span data-ttu-id="ca282-182">Weitere Informationen finden Sie unter [jetmakekey](./jetmakekey-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ca282-182">See [JetMakeKey](./jetmakekey-function.md) for more information.</span></span>

<span data-ttu-id="ca282-183">Es gibt einen wichtigen Fehler in dieser API, der in allen Releases vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ca282-183">There is an important bug in this API that is present in all releases.</span></span> <span data-ttu-id="ca282-184">Wenn der Suchschlüssel mit der Verwendung von JET_bitRetrieveCopy angefordert wird und der Ausgabepuffer zu klein ist, um den gesamten Schlüssel zu empfangen, wird JET_wrnBufferTruncated nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca282-184">If the search key is requested using the use of JET_bitRetrieveCopy and the output buffer is too small to receive the entire key then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="ca282-185">Stattdessen wird JET_errSuccess zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca282-185">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="ca282-186">Es ist wichtig sicherzustellen, dass die tatsächliche Größe des Schlüssels, der mit *pcbactual* zurückgegeben wird, kleiner oder gleich der Größe des Ausgabepuffers ist.</span><span class="sxs-lookup"><span data-stu-id="ca282-186">It is important to verify that the actual size of the key as returned using *pcbActual* is less than or equal to the size of the output buffer.</span></span> <span data-ttu-id="ca282-187">Wenn die tatsächliche Größe größer ist als die Größe des Ausgabepuffers, sollte der **Aufrufer von jetretrievekey** so reagieren, als ob JET_wrnBufferTruncated stattdessen zurückgegeben würden.</span><span class="sxs-lookup"><span data-stu-id="ca282-187">If the actual size is larger than the size of the output buffer, then the caller of **JetRetrieveKey** should react as if JET_wrnBufferTruncated were returned instead.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ca282-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca282-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca282-189"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ca282-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ca282-190">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ca282-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca282-191"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ca282-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ca282-192">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ca282-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca282-193"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ca282-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ca282-194">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="ca282-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca282-195"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="ca282-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ca282-196">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ca282-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca282-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ca282-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ca282-198">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ca282-198">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ca282-199">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ca282-199">See Also</span></span>

[<span data-ttu-id="ca282-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ca282-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ca282-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ca282-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ca282-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ca282-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ca282-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ca282-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ca282-204">Jetmakekey</span><span class="sxs-lookup"><span data-stu-id="ca282-204">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="ca282-205">JetSeek</span><span class="sxs-lookup"><span data-stu-id="ca282-205">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="ca282-206">Jetsetindexrange</span><span class="sxs-lookup"><span data-stu-id="ca282-206">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
