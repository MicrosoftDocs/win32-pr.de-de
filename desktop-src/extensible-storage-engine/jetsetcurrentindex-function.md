---
description: 'Weitere Informationen zu: jetsetcurrentindex-Funktion'
title: JetSetCurrentIndex-Funktion
TOCTitle: JetSetCurrentIndex Function
ms:assetid: a2a15eab-b8bf-4a67-a63a-830ed1fdb3d9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294046(v=EXCHG.10)
ms:contentKeyID: 32765645
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex
- JetSetCurrentIndexA
- JetSetCurrentIndexW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7698a12f470fadd5c43dc2afe23f95f8e51bdf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346079"
---
# <a name="jetsetcurrentindex-function"></a><span data-ttu-id="cc010-103">JetSetCurrentIndex-Funktion</span><span class="sxs-lookup"><span data-stu-id="cc010-103">JetSetCurrentIndex Function</span></span>


<span data-ttu-id="cc010-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cc010-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex-function"></a><span data-ttu-id="cc010-105">JetSetCurrentIndex-Funktion</span><span class="sxs-lookup"><span data-stu-id="cc010-105">JetSetCurrentIndex Function</span></span>

<span data-ttu-id="cc010-106">Die **jetsetcurrentindex** -Funktion kann verwendet werden, um den aktuellen Index eines Cursors festzulegen.</span><span class="sxs-lookup"><span data-stu-id="cc010-106">The **JetSetCurrentIndex** function can be used to set the current index of a cursor.</span></span> <span data-ttu-id="cc010-107">Der aktuelle Index eines Cursors definiert, welche Datensätze in einer Tabelle für diesen Cursor sichtbar sind, und die Reihenfolge, in der Sie angezeigt werden, indem der Satz von Indexeinträgen ausgewählt wird, der zum verfügbar machen dieser Datensätze verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc010-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const tchar* szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="cc010-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc010-108">Parameters</span></span>

<span data-ttu-id="cc010-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="cc010-109">*sesid*</span></span>

<span data-ttu-id="cc010-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc010-110">The session to use for this call.</span></span>

<span data-ttu-id="cc010-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="cc010-111">*tableid*</span></span>

<span data-ttu-id="cc010-112">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc010-112">The cursor to use for this call.</span></span>

<span data-ttu-id="cc010-113">*szindexname*</span><span class="sxs-lookup"><span data-stu-id="cc010-113">*szIndexName*</span></span>

<span data-ttu-id="cc010-114">Der Name des Indexes, der für den Cursor ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc010-114">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="cc010-115">Wenn dieser Parameter NULL oder eine leere Zeichenfolge ist, wird der gruppierte Index ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="cc010-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="cc010-116">Wenn ein primärer Index für die Tabelle definiert ist, wird dieser Index ausgewählt, da er mit dem gruppierten Index identisch ist.</span><span class="sxs-lookup"><span data-stu-id="cc010-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="cc010-117">Wenn kein primärer Index für die Tabelle definiert ist, wird der sequenzielle Index ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="cc010-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="cc010-118">Der sequenzielle Index hat keine Index Definition.</span><span class="sxs-lookup"><span data-stu-id="cc010-118">The sequential index has no index definition.</span></span> <span data-ttu-id="cc010-119">Weitere Informationen finden Sie unter [jetkreateindex](./jetcreateindex-function.md) .</span><span class="sxs-lookup"><span data-stu-id="cc010-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="cc010-120">Wenn *pIndexID* nicht NULL ist, wird der Indexname ignoriert, und der Index wird durch die Index-ID ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="cc010-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

### <a name="return-value"></a><span data-ttu-id="cc010-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc010-121">Return Value</span></span>

<span data-ttu-id="cc010-122">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="cc010-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cc010-123">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cc010-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc010-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cc010-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="cc010-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc010-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc010-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cc010-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cc010-127">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cc010-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc010-128">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="cc010-128">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="cc010-129">Ein sekundärer Index wird mit der JET_bitNoMove-Option ausgewählt, und es gibt keinen Wert für die erste mehrwertige Schlüssel Spalte in der Definition des neuen Indexes, die der angegebenen Sequenznummer entspricht.</span><span class="sxs-lookup"><span data-stu-id="cc010-129">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new index's definition that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc010-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="cc010-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="cc010-131">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="cc010-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc010-132">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="cc010-132">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="cc010-133">Der Inhalt der Index-ID war ungültig oder abgelaufen und muss aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="cc010-133">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="cc010-134">Dies kann bei <strong>jetsetcurrentindex</strong> vorkommen, wenn:</span><span class="sxs-lookup"><span data-stu-id="cc010-134">This can happen for <strong>JetSetCurrentIndex</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="cc010-135">pIndexID- &gt; cbStruct weist nicht die erwartete Größe auf (Windows Server 2003 und spätere Releases).</span><span class="sxs-lookup"><span data-stu-id="cc010-135">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="cc010-136">Die Engine wurde heruntergefahren, seit die Index-ID abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="cc010-136">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="cc010-137">Alle Cursor, die auf die Tabelle verweisen, die den Index enthält, der der Index-ID entspricht, wurden geschlossen, und die Engine hat die Definition des Indexes aus dem Schema Cache entfernt.</span><span class="sxs-lookup"><span data-stu-id="cc010-137">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted that index's definition from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="cc010-138">Die Index-ID wird mit einem Cursor verwendet, der für die falsche Tabelle geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="cc010-138">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="cc010-139">Der Index wurde gelöscht oder ist für die Sitzung noch nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="cc010-139">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc010-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="cc010-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="cc010-141">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="cc010-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="cc010-142">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cc010-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc010-143">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="cc010-143">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="cc010-144">Einer der angegebenen Objektnamen war ungültig.</span><span class="sxs-lookup"><span data-stu-id="cc010-144">One of the specified object names was invalid.</span></span> <span data-ttu-id="cc010-145">Alle Objektnamen müssen mit demselben Regelsatz übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="cc010-145">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="cc010-146">Nachfolgend sind diese Regeln aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="cc010-146">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="cc010-147">Objektnamen müssen aus ASCII-Zeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="cc010-147">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="cc010-148">Objektnamen müssen mindestens ein Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="cc010-148">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="cc010-149">Objektnamen dürfen nicht mehr als JET_cbNameMost (64) Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="cc010-149">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="cc010-150">Objektnamen dürfen nicht mit einem Leerzeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="cc010-150">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="cc010-151">Objektnamen dürfen keine ASCII-Steuerzeichen (0x00 bis 0x1F) enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc010-151">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="cc010-152">Objektnamen dürfen keine Ausrufezeichen (!), Punkte (.), linke eckige Klammer ([) oder rechte eckige Klammer (]) enthalten.</span><span class="sxs-lookup"><span data-stu-id="cc010-152">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="cc010-153">Nach der Validierung wird nur der Teil der Zeichenfolge bis zum ersten Leerzeichen (sofern vorhanden) für den Objektnamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc010-153">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="cc010-154">Dies bedeutet, dass Objektnamen keine Leerzeichen enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="cc010-154">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc010-155">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="cc010-155">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="cc010-156">Einer der angegebenen Parameter enthielt einen unerwarteten Wert oder enthielt einen Wert, der nicht sinnvoll war, wenn er mit dem Wert eines anderen Parameters kombiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="cc010-156">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="cc010-157">Dies kann bei <strong>jetsetcurrentindex</strong> vorkommen, wenn <em>pIndexID</em> nicht NULL ist und pIndexID- &gt; cbStruct nicht die erwartete Größe aufweist (Windows XP und frühere Versionen).</span><span class="sxs-lookup"><span data-stu-id="cc010-157">This can happen for <strong>JetSetCurrentIndex</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc010-158">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="cc010-158">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="cc010-159">Ein sekundärer Index wird mit der JET_bitNoMove-Option ausgewählt, und es gibt keinen Index Eintrag im neuen Index, der dem Datensatz entspricht, der mit dem Index Eintrag an der aktuellen Position des Cursors auf dem alten Index verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="cc010-159">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc010-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="cc010-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="cc010-161">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cc010-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc010-162">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="cc010-162">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="cc010-163">Die Engine hat den Ressourcenpool erschöpft, der zum Öffnen von Cursorn verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc010-163">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="cc010-164">Die maximale Anzahl von Cursorn, die zu einem beliebigen Zeitpunkt geöffnet werden können, wird mit <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>gesteuert.</span><span class="sxs-lookup"><span data-stu-id="cc010-164">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="cc010-165">Weitere Informationen finden Sie unter <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> .</span><span class="sxs-lookup"><span data-stu-id="cc010-165">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="cc010-166">Dies kann bei <strong>jetsetcurrentindex</strong> vorkommen, wenn ein sekundärer Index ausgewählt wurde und die Engine keinen internen Cursor öffnen kann, um diesen Index zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc010-166">This can happen for <strong>JetSetCurrentIndex</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc010-167">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="cc010-167">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="cc010-168">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc010-168">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc010-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="cc010-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="cc010-170">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc010-170">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="cc010-171">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cc010-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc010-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="cc010-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="cc010-173">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="cc010-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cc010-174">Bei Erfolg wird der aktuelle Index des Cursors auf den angeforderten Index festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cc010-174">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="cc010-175">Indexeinträge können nun mithilfe von [JetSeek](./jetseek-function.md) entsprechend der Index Definition des angeforderten Indexes gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="cc010-175">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="cc010-176">Index Einträge können auch mithilfe von [jetmove](./jetmove-function.md) in der von dieser Index Definition angegebenen Reihenfolge aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="cc010-176">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="cc010-177">Die aktuelle Position des Cursors ist entweder auf den ersten Index Eintrag im Index (JET_bitMoveFirst) oder auf einen bestimmten Index Eintrag festgelegt, der mit der aktuellen Position des Cursors im alten Index (JET_bitNoMove) verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="cc010-177">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="cc010-178">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="cc010-178">No change to the database state will occur.</span></span>

<span data-ttu-id="cc010-179">Bei einem Fehler sind der aktuelle Index und die aktuelle Position des Cursors in einem nicht definierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="cc010-179">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="cc010-180">Es erfolgt keine Änderung des Daten Bank Status.</span><span class="sxs-lookup"><span data-stu-id="cc010-180">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc010-181">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc010-181">Remarks</span></span>

<span data-ttu-id="cc010-182">Wenn der Index-ID-Hinweis veraltet ist, schlägt die API einfach fehl.</span><span class="sxs-lookup"><span data-stu-id="cc010-182">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="cc010-183">Es gibt in diesem Fall keinen Fall Back auf den Textnamen des Indexes, wie dies zu erwarten ist.</span><span class="sxs-lookup"><span data-stu-id="cc010-183">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="cc010-184">Dieser Fall Back muss manuell vom Aufrufer der API durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cc010-184">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="cc010-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc010-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc010-186"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cc010-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cc010-187">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="cc010-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc010-188"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cc010-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cc010-189">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cc010-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc010-190"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="cc010-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cc010-191">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="cc010-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc010-192"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="cc010-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cc010-193">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cc010-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc010-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cc010-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cc010-195">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cc010-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc010-196"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="cc010-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="cc010-197">Implementiert als <strong>jetsetcurrentindexw</strong> (Unicode) und <strong>jetsetcurrentindexa</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="cc010-197">Implemented as <strong>JetSetCurrentIndexW</strong> (Unicode) and <strong>JetSetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cc010-198">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cc010-198">See Also</span></span>

[<span data-ttu-id="cc010-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cc010-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cc010-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="cc010-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="cc010-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="cc010-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="cc010-202">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="cc010-202">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="cc010-203">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="cc010-203">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="cc010-204">Jetkreateingedex</span><span class="sxs-lookup"><span data-stu-id="cc010-204">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="cc010-205">Jetgetcurrentindex</span><span class="sxs-lookup"><span data-stu-id="cc010-205">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="cc010-206">Jetgetindexinfo</span><span class="sxs-lookup"><span data-stu-id="cc010-206">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="cc010-207">Jetgettableindexinfo</span><span class="sxs-lookup"><span data-stu-id="cc010-207">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="cc010-208">Jetmove</span><span class="sxs-lookup"><span data-stu-id="cc010-208">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="cc010-209">JetSeek</span><span class="sxs-lookup"><span data-stu-id="cc010-209">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="cc010-210">Jetsetcurrentindex</span><span class="sxs-lookup"><span data-stu-id="cc010-210">JetSetCurrentIndex</span></span>]()  
[<span data-ttu-id="cc010-211">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="cc010-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="cc010-212">Jetstopservice</span><span class="sxs-lookup"><span data-stu-id="cc010-212">JetStopService</span></span>](./jetstopservice-function.md)
