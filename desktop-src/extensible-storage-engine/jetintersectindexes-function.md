---
description: 'Weitere Informationen über: jetintersectindexes-Funktion'
title: JetIntersectIndexes-Funktion
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bdffa6f21a65ae7f438f87ea0d8d2adf4aed6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344651"
---
# <a name="jetintersectindexes-function"></a><span data-ttu-id="a995d-103">JetIntersectIndexes-Funktion</span><span class="sxs-lookup"><span data-stu-id="a995d-103">JetIntersectIndexes Function</span></span>


<span data-ttu-id="a995d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a995d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetintersectindexes-function"></a><span data-ttu-id="a995d-105">JetIntersectIndexes-Funktion</span><span class="sxs-lookup"><span data-stu-id="a995d-105">JetIntersectIndexes Function</span></span>

<span data-ttu-id="a995d-106">Die **jetintersectindexes** -Funktion berechnet die Schnittmenge zwischen mehreren Sätzen von Indexeinträgen aus unterschiedlichen sekundären Indizes für dieselbe Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a995d-106">The **JetIntersectIndexes** function computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="a995d-107">Dieser Vorgang ist nützlich, um die Gruppe von Datensätzen in einer Tabelle zu suchen, die mit zwei oder mehr Kriterien übereinstimmen, die mithilfe von Index Bereichen ausgedrückt werden können.</span><span class="sxs-lookup"><span data-stu-id="a995d-107">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span>

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="a995d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a995d-108">Parameters</span></span>

<span data-ttu-id="a995d-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="a995d-109">*sesid*</span></span>

<span data-ttu-id="a995d-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a995d-110">The session to use for this call.</span></span>

<span data-ttu-id="a995d-111">*rgindexrange*</span><span class="sxs-lookup"><span data-stu-id="a995d-111">*rgindexrange*</span></span>

<span data-ttu-id="a995d-112">Ein Zeiger auf ein Array von [JET_IndexRange](./jet-indexrange-structure.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="a995d-112">A pointer to an array of [JET_IndexRange](./jet-indexrange-structure.md) structures.</span></span> <span data-ttu-id="a995d-113">Jede Struktur enthält eine [JET_TABLEID](./jet-tableid.md) , die zum Speichern eines der zu überschneidenden Index Bereiche eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="a995d-113">Each structure includes a [JET_TABLEID](./jet-tableid.md) that has been set up to hold one of the index ranges to be intersected.</span></span> <span data-ttu-id="a995d-114">Weitere Informationen finden Sie unter [JET_IndexRange](./jet-indexrange-structure.md).</span><span class="sxs-lookup"><span data-stu-id="a995d-114">For more information, see [JET_IndexRange](./jet-indexrange-structure.md).</span></span>

<span data-ttu-id="a995d-115">*cindexrange*</span><span class="sxs-lookup"><span data-stu-id="a995d-115">*cindexrange*</span></span>

<span data-ttu-id="a995d-116">Die Anzahl der [JET_IndexRange](./jet-indexrange-structure.md) Strukturen im-Array, die im *rgindexrange* -Parameter enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a995d-116">The number of [JET_IndexRange](./jet-indexrange-structure.md) structures in the array that is contained in the *rgindexrange* parameter.</span></span>

<span data-ttu-id="a995d-117">*precordlist*</span><span class="sxs-lookup"><span data-stu-id="a995d-117">*precordlist*</span></span>

<span data-ttu-id="a995d-118">Zeiger auf eine [JET_RECORDLIST](./jet-recordlist-structure.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a995d-118">Pointer to a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="a995d-119">Diese Struktur wird mit ausreichenden Informationen aufgefüllt, um die temporäre Tabelle mit den Ergebnissen von **jetintersectindexes** zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="a995d-119">This structure will be populated with enough information to traverse the temporary table with the results from **JetIntersectIndexes**.</span></span>

<span data-ttu-id="a995d-120">Der Ausgabepuffer, der eine [JET_RECORDLIST](./jet-recordlist-structure.md) Struktur empfängt.</span><span class="sxs-lookup"><span data-stu-id="a995d-120">The output buffer that receives a [JET_RECORDLIST](./jet-recordlist-structure.md) structure.</span></span> <span data-ttu-id="a995d-121">Die Struktur enthält eine Beschreibung des Resultsets der Schnittmenge.</span><span class="sxs-lookup"><span data-stu-id="a995d-121">The structure contains a description of the result set of the intersection.</span></span>

<span data-ttu-id="a995d-122">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a995d-122">*grbit*</span></span>

<span data-ttu-id="a995d-123">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="a995d-123">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="a995d-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a995d-124">Return Value</span></span>

<span data-ttu-id="a995d-125">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="a995d-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a995d-126">Weitere Informationen zu ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a995d-126">For more information about ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a995d-127">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a995d-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="a995d-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a995d-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a995d-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a995d-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a995d-130">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a995d-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a995d-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a995d-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a995d-132">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a995d-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a995d-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a995d-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a995d-134">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="a995d-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a995d-135"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a995d-135"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a995d-136">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="a995d-136">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="a995d-137">Eine der angeforderten Optionen war ungültig, wurde falsch verwendet oder nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a995d-137">One of the options requested was invalid, used incorrectly, or not implemented.</span></span></p>
<p><span data-ttu-id="a995d-138">Dieser Fehler wird von <strong>jetintersectindexes</strong> zurückgegeben, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="a995d-138">This error is returned by <strong>JetIntersectIndexes</strong> when:</span></span></p>
<p><span data-ttu-id="a995d-139">Das in der <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> Struktur enthaltene <em>grbit</em> , auf das von einem Element im <em>rgindexrange</em> -Array verwiesen wird, ist nicht gleich JET_bitRecordInIndex.</span><span class="sxs-lookup"><span data-stu-id="a995d-139">The <em>grbit</em> contained in the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure pointed to by any element in the <em>rgindexrange</em> array is not equal to JET_bitRecordInIndex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a995d-140">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a995d-140">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a995d-141">Einer der angegebenen Parameter enthält einen unerwarteten Wert oder einen Wert, der inkonsistent ist, wenn er mit dem Wert eines anderen Parameters kombiniert wird.</span><span class="sxs-lookup"><span data-stu-id="a995d-141">One of the parameters provided contains an unexpected value or a value that is inconsistent when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="a995d-142">Dieser Fehler wird von <strong>jetintersectindexes</strong> aus den folgenden Gründen zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="a995d-142">This error is returned by <strong>JetIntersectIndexes</strong> for of the following reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="a995d-143">Der <em>precordlist</em> -Parameter ist NULL.</span><span class="sxs-lookup"><span data-stu-id="a995d-143">The <em>precordlist</em> parameter is NULL.</span></span></p></li>
<li><p><span data-ttu-id="a995d-144">Der <strong>cbStruct</strong> -Member der im <em>precordlist</em> -Parameter angegebenen <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> Struktur entspricht nicht der Größe der <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> Struktur.</span><span class="sxs-lookup"><span data-stu-id="a995d-144">The <strong>cbStruct</strong> member of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure specified in the <em>precordlist</em> parameter is not equal to size of the <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="a995d-145">Der <em>cindexrange</em> -Parameter ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a995d-145">The <em>cindexrange</em> parameter is zero.</span></span></p></li>
<li><p><span data-ttu-id="a995d-146">Der <em>cindexrange</em> -Parameter ist größer als 64.</span><span class="sxs-lookup"><span data-stu-id="a995d-146">The <em>cindexrange</em> parameter is greater than 64.</span></span></p></li>
<li><p><span data-ttu-id="a995d-147">Das <strong>cbStruct</strong> -Element für jedes Element im Array, das durch den <em>rgindexrange</em> -Parameter angegeben wird, entspricht nicht der Größe der <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> Struktur.</span><span class="sxs-lookup"><span data-stu-id="a995d-147">The <strong>cbStruct</strong> member for any element in the array specified by the <em>rgindexrange</em> parameter is not equal to the size of the <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> structure.</span></span></p></li>
<li><p><span data-ttu-id="a995d-148">Die Elemente im <em>rgindexrange</em> -Array enthalten <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s aus unterschiedlichen Tabellen.</span><span class="sxs-lookup"><span data-stu-id="a995d-148">The elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s from different tables.</span></span></p></li>
<li><p><span data-ttu-id="a995d-149">Ein Element im <em>rgindexrange</em> -Array enthält eine <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> , die nicht auf einem sekundären Index positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="a995d-149">An element in the <em>rgindexrange</em> array contains a <a href="gg269182(v=exchg.10).md">JET_TABLEID</a> that is not positioned on a secondary index.</span></span></p></li>
<li><p><span data-ttu-id="a995d-150">Mindestens eines der Elemente im <em>rgindexrange</em> -Array enthält <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>en, die sich auf demselben sekundären Index befinden.</span><span class="sxs-lookup"><span data-stu-id="a995d-150">One or more of the elements in the <em>rgindexrange</em> array contain <a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s positioned on the same secondary index.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a995d-151">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="a995d-151">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="a995d-152">Das Sitzungs Handle ist ungültig oder verweist auf eine geschlossene Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a995d-152">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="a995d-153">Dieser Fehler wird unter allen Umständen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a995d-153">This error is not returned under all circumstances.</span></span> <span data-ttu-id="a995d-154">Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</span><span class="sxs-lookup"><span data-stu-id="a995d-154">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a995d-155">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a995d-155">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a995d-156">Der Vorgang kann nicht abgeschlossen werden, da die-Instanz, die der Sitzung zugeordnet ist, nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a995d-156">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a995d-157">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="a995d-157">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="a995d-158">Der Vorgang ist fehlgeschlagen, da die Engine die zum Öffnen eines neuen Cursors erforderlichen Ressourcen nicht zuordnen konnte.</span><span class="sxs-lookup"><span data-stu-id="a995d-158">The operation failed because the engine could not allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="a995d-159">Cursor Ressourcen werden durch Aufrufen von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <em>JET_paramMaxCursors</em> im <em>paramID</em> -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a995d-159">Cursor resources are configured by calling <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxCursors</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a995d-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a995d-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="a995d-161">Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a995d-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="a995d-162"><strong>Jetintersectindexes</strong> kann JET_errOutOfMemory zurückgeben, wenn der Adressraum des Host Prozesses zu fragmentiert wird.</span><span class="sxs-lookup"><span data-stu-id="a995d-162"><strong>JetIntersectIndexes</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="a995d-163">Der temporäre Tabellen-Manager weist immer einen 1-MB-Adressraum für jede temporäre Tabelle zu, die unabhängig von der zu speichernden Datenmenge erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a995d-163">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span> <span data-ttu-id="a995d-164"><strong>Jetintersectindexes</strong> erstellt eine temporäre Tabelle für jede <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> , die im <em>rgindexrange</em> -Parameter angegeben ist, und eine temporäre Tabelle für die Ausgabe in <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="a995d-164"><strong>JetIntersectIndexes</strong> will create one temporary table for each <a href="gg269335(v=exchg.10).md">JET_IndexRange</a> specified in the <em>rgindexrange</em> parameter, and one temporary table for the output in <a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a995d-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a995d-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a995d-166">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a995d-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a995d-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a995d-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a995d-168">Es ist nicht zulässig, dieselbe Sitzung von mehr als einem Thread gleichzeitig zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a995d-168">It is illegal to use the same session from more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="a995d-169"><strong>Windows XP:</strong>  Dieser Rückgabewert wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a995d-169"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a995d-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a995d-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a995d-171">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="a995d-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a995d-172">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="a995d-172">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="a995d-173">Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern der Indizes der Tabelle erforderlichen Ressourcen nicht zuordnen konnte.</span><span class="sxs-lookup"><span data-stu-id="a995d-173">The operation failed because the engine could not allocate the resources required to cache the indices of the table.</span></span> <span data-ttu-id="a995d-174">Die Anzahl der Indizes, deren Schema zwischengespeichert werden kann, wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <em>JET_paramMaxOpenTables</em> im <em>paramID</em> -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a995d-174">The number of indices whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a995d-175">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="a995d-175">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="a995d-176">Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern des Schemas der Tabelle erforderlichen Ressourcen nicht zuordnen konnte.</span><span class="sxs-lookup"><span data-stu-id="a995d-176">The operation failed because the engine could not allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="a995d-177">Die Anzahl der Tabellen, deren Schema zwischengespeichert werden kann, wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <em>JET_paramMaxOpenTables</em> im <em>paramID</em> -Parameter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a995d-177">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <em>JET_paramMaxOpenTables</em> specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a995d-178">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="a995d-178">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="a995d-179">Der Vorgang ist fehlgeschlagen, da die Engine die zum Erstellen einer temporären Tabelle erforderlichen Ressourcen nicht zuordnen konnte.</span><span class="sxs-lookup"><span data-stu-id="a995d-179">The operation failed because the engine could not allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="a995d-180">Temporäre Tabellen Ressourcen werden mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit JET_paramMaxTemporaryTables konfiguriert, die im <em>paramID</em> -Parameter angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a995d-180">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with JET_paramMaxTemporaryTables specified in the <em>paramid</em> parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a995d-181">Bei Erfolg wird eine neue temporäre Tabelle zurückgegeben, die die Lesezeichen der Datensätze enthält, die mit den Kriterien übereinstimmen, die durch die einzelnen Beschreibungen der Eingabe Index Bereiche dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a995d-181">On success, a new temporary table is returned that contains the bookmarks of the records that match the criteria represented by each of the input index range descriptions.</span></span>

<span data-ttu-id="a995d-182">Bei einem Fehler wird die temporäre Tabelle, die die Ergebnisse enthält, nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="a995d-182">On failure, the temporary table containing the results will not be created.</span></span> <span data-ttu-id="a995d-183">Der Status der temporären Datenbank kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a995d-183">The state of the temporary database may be changed.</span></span> <span data-ttu-id="a995d-184">Der Status aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="a995d-184">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span> <span data-ttu-id="a995d-185">Die aktuelle Position der [JET_TABLEID](./jet-tableid.md)s, die für diese Funktion bereitgestellt wird, kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a995d-185">The current position of the [JET_TABLEID](./jet-tableid.md)s provided to this function may be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a995d-186">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a995d-186">Remarks</span></span>

<span data-ttu-id="a995d-187">**Jetintersectindexes** kann verwendet werden, um die Datensätze in einer Tabelle anhand mehrerer Kriterien effizient zu filtern, wenn diese Kriterien in Bezug auf die sekundären Indizes für diese Tabelle ausgedrückt werden können.</span><span class="sxs-lookup"><span data-stu-id="a995d-187">**JetIntersectIndexes** can be used to efficiently filter the records in a table by multiple criteria if those criteria can be expressed in terms of the secondary indices over that table.</span></span> <span data-ttu-id="a995d-188">Nehmen Sie beispielsweise an, dass Sie über eine sehr große Tabelle mit Personen verfügen.</span><span class="sxs-lookup"><span data-stu-id="a995d-188">For example, consider that you have a very large table containing people.</span></span> <span data-ttu-id="a995d-189">Die Tabelle kann Spalten für Ihre Benutzer-ID, den Vornamen, den Nachnamen usw. aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a995d-189">The table can have columns for their user id, first name, last name, and so on.</span></span> <span data-ttu-id="a995d-190">Angenommen, jede dieser Spalten wird separat indiziert, und der primäre Index der Tabelle ist über die Benutzer-ID. Wenn Sie alle Benutzer suchen möchten, deren Vorname mit einem beginnt und dessen Nachname mit G beginnt, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="a995d-190">Suppose that each of these columns is indexed separately and that the primary index of the table is over user id. If you wanted to find everyone whose first name starts with an A and whose last name starts with G, you would perform the following steps:</span></span>

1.  <span data-ttu-id="a995d-191">Öffnen Sie einen neuen Cursor in der Tabelle, und legen Sie für diesen Cursor fest, dass der Index für die Spalte "Vorname" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a995d-191">Open a new cursor on the table, and set that cursor to use the index over the "first name" column.</span></span> <span data-ttu-id="a995d-192">Richten Sie dann einen Index Bereich für alle Personen ein, deren "Vorname" mit "A" beginnt, und erstellen Sie eine [JET_IndexRange](./jet-indexrange-structure.md) Struktur, die diesen Cursor enthält.</span><span class="sxs-lookup"><span data-stu-id="a995d-192">Then setup an index range for all people whose "first name" started with 'A', and build a [JET_IndexRange](./jet-indexrange-structure.md) struct that contains this cursor.</span></span>

2.  <span data-ttu-id="a995d-193">Wiederholen Sie Schritt 1 mit einem neuen Cursor für den Index "Last Name" für alle Personen, deren "Nachname" mit "G" begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="a995d-193">Repeat step 1 with a new cursor on the "last name" index for all people whose "last name" started with 'G'.</span></span>

3.  <span data-ttu-id="a995d-194">Übergeben Sie diese Kriterien an **jetintersectindexes** , um das Ergebnis in einer temporären Tabelle zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="a995d-194">Pass these criteria to **JetIntersectIndexes** to compute the result into a temporary table.</span></span>

4.  <span data-ttu-id="a995d-195">Durchlaufen Sie die temporäre Tabelle, und rufen Sie jeden Datensatz ab, der die Kriterien nach Lesezeichen übergibt.</span><span class="sxs-lookup"><span data-stu-id="a995d-195">Traverse the temporary table and retrieve each of the records that pass the criteria by bookmark.</span></span>

<span data-ttu-id="a995d-196">Die temporäre Tabelle, die das Resultset enthält, ist eine einfache Tabelle mit einer Spalte, die das Lesezeichen der einzelnen Datensätze enthält, die alle zum Berechnen der Schnittmenge verwendeten Kriterien überschritten haben.</span><span class="sxs-lookup"><span data-stu-id="a995d-196">The temporary table containing the result set is a simple table with one column that contains the bookmark of each record that passed all the criteria used to compute the intersection.</span></span> <span data-ttu-id="a995d-197">Das Resultset wird in derselben Reihenfolge wie der primäre Index sortiert und enthält keine doppelten Einträge.</span><span class="sxs-lookup"><span data-stu-id="a995d-197">The result set is sorted in the same order as the primary index and contains no duplicate entries.</span></span> <span data-ttu-id="a995d-198">Die Anwendung kann die Ergebnisse der Schnittmenge auflisten, indem Sie die Zeilen in der temporären Tabelle aufzählt, das Lesezeichen für jedes Ergebnis mithilfe von [jetretrievecolumn](./jetretrievecolumn-function.md)abrufen und dann den Datensatz in der Datenbank aufrufen, indem Sie [jetgotobookmark](./jetgotobookmark-function.md) mit diesem Lesezeichen auf einem Cursor aufrufen, der auf dem primären Index positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="a995d-198">The application can enumerate the results of the intersection by enumerating the rows in the temporary table, retrieving the bookmark for each result using [JetRetrieveColumn](./jetretrievecolumn-function.md), and then visiting the record in the database by calling [JetGotoBookmark](./jetgotobookmark-function.md) with that bookmark on a cursor positioned on the primary index.</span></span>

<span data-ttu-id="a995d-199">Die von **jetintersectindexes** zurückgegebene temporäre Tabelle kann nur in Vorwärtsrichtung gescannt werden.</span><span class="sxs-lookup"><span data-stu-id="a995d-199">The temporary table returned by **JetIntersectIndexes** can only be scanned in a forward direction.</span></span> <span data-ttu-id="a995d-200">Er sollte auch über [jetclosetable](./jetclosetable-function.md) geschlossen werden, wenn die Überprüfung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a995d-200">It should also be closed via [JetCloseTable](./jetclosetable-function.md) when the scan has been completed.</span></span> <span data-ttu-id="a995d-201">Weitere Informationen zu temporären Tabellen und ihrer Funktionsweise finden Sie unter [jetopertemporarytable](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="a995d-201">For more information about temporary tables and how they work, see [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

<span data-ttu-id="a995d-202">**Jetintersectindexes** ist im Allgemeinen eine effiziente und bequeme Möglichkeit zum Filtern von Datensätzen basierend auf mehreren indizierten Kriterien.</span><span class="sxs-lookup"><span data-stu-id="a995d-202">**JetIntersectIndexes** is generally an efficient and convenient way to filter records based on multiple indexed criteria.</span></span> <span data-ttu-id="a995d-203">Es gibt jedoch einige wichtige Tipps, die befolgt werden sollten, um die Nützlichkeit dieses Features zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="a995d-203">However, there are some important tips that should be followed to maximize the usefulness of this feature.</span></span> <span data-ttu-id="a995d-204">Wenn Sie wissen, dass eines der Kriterien so restriktiv ist, dass der resultierende Index Bereich nur sehr wenige Datensätze enthält, ist es wahrscheinlich besser, diesen Index Bereich zu durchlaufen und die Datensätze auf Anwendungsebene zu filtern.</span><span class="sxs-lookup"><span data-stu-id="a995d-204">If you know that one of the criteria is so restrictive that the resulting index range has very few records then it is probably better to simply walk that index range and filter the records at the application level.</span></span> <span data-ttu-id="a995d-205">Wenn Sie darüber hinaus wissen, dass Sie Kriterien haben, die weitaus weniger restriktiv sind als andere Kriterien in ihrer Schnittmenge, sollten Sie in Erwägung ziehen, diese weitaus weniger restriktiven Kriterien aus der Schnittmenge zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="a995d-205">Further, if you know that you have criteria that are much less restrictive than other criteria in your intersection then you might consider dropping those much less restrictive criteria from the intersection.</span></span> <span data-ttu-id="a995d-206">Wenn Sie wissen, dass eines der Kriterien überhaupt nicht restriktiv ist, sodass der resultierende Index Bereich fast so groß wie der primäre Index ist, ist es unwahrscheinlich, dass die überschneidende Verwendung dieses Index Bereichs den Wert für das Resultset (reduzieren der Größe) beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="a995d-206">Finally, if you know that one of the criteria is not at all restrictive such that the resulting index range is almost as large as the primary index then it is unlikely that intersecting with that index range will benefit (reduce the size of) the result set.</span></span> <span data-ttu-id="a995d-207">In allen Fällen sollten Sie Kriterien auf eine Weise auswählen, die möglichst wenige Indexeinträge für die Eingabe verwendet und den spezifischsten Satz an Lesezeichen bei der Ausgabe generiert, um die maximale Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="a995d-207">In all cases, you should be selecting criteria in a manner that will take the fewest possible index entries on input and generate the most specific set of bookmarks on output for maximum performance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a995d-208">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a995d-208">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a995d-209"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a995d-209"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a995d-210">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a995d-210">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a995d-211"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a995d-211"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a995d-212">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a995d-212">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a995d-213"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a995d-213"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a995d-214">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a995d-214">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a995d-215"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="a995d-215"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a995d-216">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a995d-216">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a995d-217"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a995d-217"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a995d-218">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a995d-218">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a995d-219">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a995d-219">See Also</span></span>

[<span data-ttu-id="a995d-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a995d-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a995d-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a995d-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a995d-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a995d-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a995d-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a995d-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a995d-224">JET_IndexRange</span><span class="sxs-lookup"><span data-stu-id="a995d-224">JET_IndexRange</span></span>](./jet-indexrange-structure.md)  
[<span data-ttu-id="a995d-225">JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="a995d-225">JET_RECORDLIST</span></span>](./jet-recordlist-structure.md)  
[<span data-ttu-id="a995d-226">Jetgojebookmark</span><span class="sxs-lookup"><span data-stu-id="a995d-226">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="a995d-227">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="a995d-227">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="a995d-228">Jetsetindexrange</span><span class="sxs-lookup"><span data-stu-id="a995d-228">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
