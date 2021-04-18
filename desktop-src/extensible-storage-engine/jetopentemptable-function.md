---
description: 'Weitere Informationen zu: jetopentemptable-Funktion'
title: JetOpenTempTable-Funktion
TOCTitle: JetOpenTempTable Function
ms:assetid: 29261333-a1bc-4159-9046-c32c36f47410
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269211(v=EXCHG.10)
ms:contentKeyID: 32765514
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66c58abc5cff433bb4d944e39c283ba712d7cebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344246"
---
# <a name="jetopentemptable-function"></a><span data-ttu-id="6c338-103">JetOpenTempTable-Funktion</span><span class="sxs-lookup"><span data-stu-id="6c338-103">JetOpenTempTable Function</span></span>


<span data-ttu-id="6c338-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6c338-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable-function"></a><span data-ttu-id="6c338-105">JetOpenTempTable-Funktion</span><span class="sxs-lookup"><span data-stu-id="6c338-105">JetOpenTempTable Function</span></span>

<span data-ttu-id="6c338-106">Die **jetopentemptable** -Funktion erstellt eine temporäre Tabelle mit einem einzelnen Index.</span><span class="sxs-lookup"><span data-stu-id="6c338-106">The **JetOpenTempTable** function creates a temporary table with a single index.</span></span> <span data-ttu-id="6c338-107">Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6c338-107">A temporary table stores and retrieves records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="6c338-108">Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen.</span><span class="sxs-lookup"><span data-stu-id="6c338-108">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="6c338-109">Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="6c338-109">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="6c338-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c338-110">Parameters</span></span>

<span data-ttu-id="6c338-111">*-sid*</span><span class="sxs-lookup"><span data-stu-id="6c338-111">*sesid*</span></span>

<span data-ttu-id="6c338-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6c338-112">The session to use.</span></span>

<span data-ttu-id="6c338-113">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="6c338-113">*prgcolumndef*</span></span>

<span data-ttu-id="6c338-114">Spaltendefinitionen für die Spalten, die in der temporären Tabelle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6c338-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="6c338-115">**Wichtige**   Einschränkungen gelten für die Spalten Definitions Optionen, die für eine temporäre Tabelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c338-115">**Important**   limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="6c338-116">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6c338-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="6c338-117">Zusätzlich zu den üblichen Spalten Definitions Optionen können auch keine oder mehrere der folgenden Optionen angegeben werden, die nur im Kontext einer temporären Tabelle relevant sind.</span><span class="sxs-lookup"><span data-stu-id="6c338-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c338-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6c338-118">Value</span></span></p></th>
<th><p><span data-ttu-id="6c338-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6c338-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c338-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="6c338-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="6c338-121">Die Sortierreihenfolge der Schlüssel Spalte für die temporäre Tabelle sollte absteigend und nicht aufsteigend sein.</span><span class="sxs-lookup"><span data-stu-id="6c338-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="6c338-122">Wenn diese Option ohne JET_bitColumnTTKey angegeben wird, wird diese Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6c338-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="6c338-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="6c338-124">Die Spalte ist eine Schlüssel Spalte für die temporäre Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6c338-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="6c338-125">Die Reihenfolge der Spaltendefinitionen, bei denen diese Option im Eingabe Array angegeben ist, bestimmt die Rangfolge der einzelnen Schlüssel Spalten für die temporäre Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6c338-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="6c338-126">Die erste Spaltendefinition im Array, für die diese Option festgelegt ist, ist die wichtigste Schlüssel Spalte usw.</span><span class="sxs-lookup"><span data-stu-id="6c338-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="6c338-127">Wenn mehr Schlüssel Spalten angefordert werden, als von der Datenbank-Engine unterstützt werden können, wird diese Option für die nicht supportablen Schlüssel Spalten ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6c338-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c338-128">*CColumn*</span><span class="sxs-lookup"><span data-stu-id="6c338-128">*ccolumn*</span></span>

<span data-ttu-id="6c338-129">Siehe *prgcolumndef*.</span><span class="sxs-lookup"><span data-stu-id="6c338-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="6c338-130">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6c338-130">*grbit*</span></span>

<span data-ttu-id="6c338-131">Eine Gruppe von Bits, die NULL oder mehr der folgenden Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="6c338-131">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c338-132">Wert</span><span class="sxs-lookup"><span data-stu-id="6c338-132">Value</span></span></p></th>
<th><p><span data-ttu-id="6c338-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6c338-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c338-134">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="6c338-134">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="6c338-135">Jeder Versuch, einen Datensatz mit dem gleichen Index Schlüssel wie ein zuvor eingefügter Datensatz einzufügen, schlägt mit JET_errKeyDuplicate sofort fehl.</span><span class="sxs-lookup"><span data-stu-id="6c338-135">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="6c338-136">Wenn diese Option nicht angefordert wird, wird sofort ein Duplikat erkannt, und es wird ein Fehler zurückgegeben. Dies hängt von der Strategie ab, die von der Datenbank-Engine zum Implementieren der temporären Tabelle basierend auf der angeforderten Funktionalität gewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="6c338-136">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="6c338-137">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="6c338-137">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="6c338-138">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="6c338-138">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-139">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="6c338-139">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="6c338-140">Zwingt den temporären Tabellen-Manager, die Suche nach der optimalen Strategie zu verwerfen, um die Verwaltung der temporären Tabelle zu verbessern, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="6c338-140">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-141">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="6c338-141">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="6c338-142">Die temporäre Tabelle wird nur erstellt, wenn der temporäre Tabellen-Manager die-Implementierung verwenden kann, die für zwischen Abfrageergebnisse optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="6c338-142">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="6c338-143">Wenn ein beliebiges Merkmal der temporären Tabelle die Verwendung dieser Optimierung verhindern würde, schlägt der Vorgang mit JET_errCannotMaterializeForwardOnlySort fehl.</span><span class="sxs-lookup"><span data-stu-id="6c338-143">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="6c338-144">Ein Nebeneffekt dieser Option besteht darin, zuzulassen, dass die temporäre Tabelle Datensätze mit doppelten Index Schlüsseln enthält.</span><span class="sxs-lookup"><span data-stu-id="6c338-144">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="6c338-145">Weitere Informationen finden Sie unter JET_bitTTUnique.</span><span class="sxs-lookup"><span data-stu-id="6c338-145">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="6c338-146">Diese Option ist nur für Windows Server 2003 und spätere Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c338-146">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-147">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="6c338-147">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="6c338-148">Mit dieser Option wird angefordert, dass die temporäre Tabelle flexibel genug ist, um die Verwendung von <a href="gg294103(v=exchg.10).md">JetSeek</a> für die Suche nach Datensätzen nach Index Schlüssel zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="6c338-148">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="6c338-149">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="6c338-149">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="6c338-150">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="6c338-150">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-151">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="6c338-151">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="6c338-152">Fordert an, dass Datensätze mit doppelten Index Schlüsseln aus dem endgültigen Satz von Datensätzen in der temporären Tabelle entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6c338-152">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="6c338-153">Vor Windows Server 2003 hat die Datenbank-Engine immer angenommen, dass diese Option wirksam ist, weil alle gruppierten Indizes auch ein Primärschlüssel sein müssen und daher eindeutig sein müssen.</span><span class="sxs-lookup"><span data-stu-id="6c338-153">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="6c338-154">Ab Windows Server 2003 ist es möglich, eine temporäre Tabelle zu erstellen, die keine Duplikate entfernt, wenn die JET_bitTTForwardOnly-Option ebenfalls angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6c338-154">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="6c338-155">Im Allgemeinen ist es nicht möglich, zu ermitteln, welches Duplikat erfolgreich ist und welche Duplikate verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="6c338-155">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="6c338-156">Wenn jedoch die JET_bitTTErrorOnDuplicateInsertion-Option angefordert wird, ist der erste Datensatz mit einem bestimmten Index Schlüssel, der in die temporäre Tabelle eingefügt werden soll, immer erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6c338-156">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-157">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="6c338-157">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="6c338-158">Fordert an, dass die temporäre Tabelle flexibel genug ist, damit Datensätze, die zuvor eingefügt wurden, geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="6c338-158">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="6c338-159">Wenn diese Funktionalität nicht erforderlich ist, empfiehlt es sich, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="6c338-159">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="6c338-160">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="6c338-160">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-161">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="6c338-161">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="6c338-162">Fordert an, dass die temporäre Tabelle flexibel genug ist, um das Scannen von Datensätzen in beliebiger Reihenfolge und Richtung mithilfe von <a href="gg294117(v=exchg.10).md">jetmove</a>zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="6c338-162">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="6c338-163">Wenn diese Funktionalität nicht erforderlich ist, ist es am besten, Sie nicht anzufordern.</span><span class="sxs-lookup"><span data-stu-id="6c338-163">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="6c338-164">Wenn diese Funktion nicht angefordert wird, kann der temporäre Tabellen-Manager möglicherweise eine Strategie zum Verwalten der temporären Tabelle auswählen, die zu einer verbesserten Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="6c338-164">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-165">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="6c338-165">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="6c338-166">Fordert an, dass NULL-Schlüssel Spaltenwerte näher am Ende des Indexes liegen als Schlüssel Spaltenwerte ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="6c338-166">Requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-167">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="6c338-167">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="6c338-168">Anforderungen, um nur systeminterne Long-Werte zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="6c338-168">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="6c338-169"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6c338-169"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c338-170">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="6c338-170">*ptableid*</span></span>

<span data-ttu-id="6c338-171">Der Ausgabepuffer, der den neuen Cursor empfängt, der in der neu erstellten temporären Tabelle geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="6c338-171">The output buffer that receives the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="6c338-172">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="6c338-172">*prgcolumnid*</span></span>

<span data-ttu-id="6c338-173">Der Ausgabepuffer, der das Array der Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6c338-173">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="6c338-174">Die Spalten-IDs in diesem Array entsprechen exakt dem Eingabe Array von Spaltendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6c338-174">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="6c338-175">Folglich muss die Größe dieses Puffers der Größe des Eingabe Arrays entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6c338-175">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="6c338-176">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c338-176">Return Value</span></span>

<span data-ttu-id="6c338-177">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="6c338-177">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6c338-178">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6c338-178">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c338-179">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6c338-179">Return code</span></span></p></th>
<th><p><span data-ttu-id="6c338-180">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c338-180">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c338-181">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6c338-181">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6c338-182">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6c338-182">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-183">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="6c338-183">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="6c338-184">Fehler bei <strong>jetopentemptable</strong> , weil JET_bitTTForwardOnly angegeben wurde und die temporäre Tabelle wie angegeben nicht mithilfe der vorwärts Optimierung erstellt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="6c338-184"><strong>JetOpenTempTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="6c338-185">Dieser Fehler wird nur von Windows Server 2003 und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c338-185">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-186">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="6c338-186">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="6c338-187">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="6c338-187">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-188">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="6c338-188">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="6c338-189">Der Index konnte nicht erstellt werden, da eine ungültige Index Definition angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6c338-189">The index could not be created because an invalid index definition was specified.</span></span></p>
<p><span data-ttu-id="6c338-190"><strong>Jetopertemptable</strong> gibt den folgenden Fehler zurück:</span><span class="sxs-lookup"><span data-stu-id="6c338-190"><strong>JetOpenTempTable</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="6c338-191">Das sprachneutrale Gebiets Schema ist angegeben.</span><span class="sxs-lookup"><span data-stu-id="6c338-191">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="6c338-192">Es wurde ein ungültiger Satz von normalisierungs Flags angegeben.</span><span class="sxs-lookup"><span data-stu-id="6c338-192">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="6c338-193">Dieser Fehler wird nur von Windows 2000 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c338-193">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="6c338-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="6c338-195">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="6c338-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="6c338-196">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c338-196">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-197">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="6c338-197">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="6c338-198">Das CP-Feld des <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf eine gültige Codepage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c338-198">The cp field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid code page.</span></span> <span data-ttu-id="6c338-199">Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="6c338-199">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="6c338-200">Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</span><span class="sxs-lookup"><span data-stu-id="6c338-200">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-201">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="6c338-201">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="6c338-202">Das <em>colyp</em> -Feld des <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> wurde nicht auf einen gültigen Spaltentyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c338-202">The <em>coltyp</em> field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="6c338-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="6c338-204">Der Index konnte nicht erstellt werden, da versucht wurde, eine ungültige Gebiets Schema-ID zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c338-204">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="6c338-205">Die Gebiets Schema-ID ist möglicherweise vollständig ungültig, oder das zugehörige Sprachpaket ist möglicherweise nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="6c338-205">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-206">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="6c338-206">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="6c338-207">Der Index konnte nicht erstellt werden, da versucht wurde, einen ungültigen Satz von normalisierungs Flags zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c338-207">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="6c338-208">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c338-208">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="6c338-209">Bei Windows 2000 resultieren ungültige normalisierungs Flags stattdessen JET_errIndexInvalidDef.</span><span class="sxs-lookup"><span data-stu-id="6c338-209">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-210">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="6c338-210">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="6c338-211">Das Sitzungs Handle ist ungültig oder verweist auf eine geschlossene Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6c338-211">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="6c338-212"><strong>Hinweis</strong>  Dieser Fehler wird unter allen Umständen nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c338-212"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="6c338-213">Handles werden nur auf Grundlage der bestmöglichen Leistung überprüft.</span><span class="sxs-lookup"><span data-stu-id="6c338-213">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-214">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6c338-214">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="6c338-215">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6c338-215">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-216">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="6c338-216">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="6c338-217">Der Vorgang ist fehlgeschlagen, da die Engine die zum Öffnen eines neuen Cursors erforderlichen Ressourcen nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="6c338-217">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="6c338-218">Cursor Ressourcen werden mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6c338-218">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-219">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="6c338-219">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="6c338-220">Der Vorgang ist fehlgeschlagen, da nicht genügend Arbeitsspeicher zugeordnet werden konnte, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6c338-220">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="6c338-221"><strong>Jetopertemptable</strong> kann JET_errOutOfMemory zurückgeben, wenn der Adressraum des Host Prozesses zu fragmentiert wird.</span><span class="sxs-lookup"><span data-stu-id="6c338-221"><strong>JetOpenTempTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="6c338-222">Der temporäre Tabellen-Manager weist immer einen 1-MB-Adressraum für jede temporäre Tabelle zu, die unabhängig von der zu speichernden Datenmenge erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6c338-222">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-223">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="6c338-223">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="6c338-224">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c338-224">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-225">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="6c338-225">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="6c338-226">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c338-226">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="6c338-227">Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c338-227">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-228">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="6c338-228">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="6c338-229">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="6c338-229">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-230">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="6c338-230">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="6c338-231">Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6c338-231">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="6c338-232">Eine Tabelle kann nicht mehr als JET_ccolFixedMost fester Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierte Spalten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6c338-232">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-233">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="6c338-233">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="6c338-234">Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern der Indizes der Tabelle erforderlichen Ressourcen nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="6c338-234">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="6c338-235">Die Anzahl der Indizes, deren Schema zwischengespeichert werden kann, wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6c338-235">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-236">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="6c338-236">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="6c338-237">Der Vorgang ist fehlgeschlagen, da die Engine die zum Zwischenspeichern des Schemas der Tabelle erforderlichen Ressourcen nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="6c338-237">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="6c338-238">Die Anzahl der Tabellen, deren Schema zwischengespeichert werden kann, wird mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6c338-238">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-239">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="6c338-239">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="6c338-240">Der Vorgang ist fehlgeschlagen, da die Engine die zum Erstellen einer temporären Tabelle erforderlichen Ressourcen nicht zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="6c338-240">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="6c338-241">Temporäre Tabellen Ressourcen werden mithilfe von <a href="gg294044(v=exchg.10).md">jetsetsystemparameter</a> mit <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6c338-241">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c338-242">Bei Erfolg wird ein Cursor zurückgegeben, der für die neu erstellte temporäre Tabelle geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="6c338-242">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="6c338-243">Der Status der temporären Datenbank wird darauf vorbereitet, die neue temporäre Tabelle zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="6c338-243">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="6c338-244">Der Status aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="6c338-244">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="6c338-245">Bei einem Fehler wird die temporäre Tabelle nicht erstellt, und ein Cursor wird nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c338-245">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="6c338-246">Der Status der temporären Datenbank kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6c338-246">The state of the temporary database may be changed.</span></span> <span data-ttu-id="6c338-247">Der Status aller normalen Datenbanken, die von der Datenbank-Engine verwendet werden, bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="6c338-247">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6c338-248">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c338-248">Remarks</span></span>

<span data-ttu-id="6c338-249">Temporäre Tabellen unterstützen nicht die vollständige Ergänzung der Spalten Definitions Optionen, die normalerweise von der Datenbank-Engine unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6c338-249">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="6c338-250">Tatsächlich werden nur JET_bitColumnFixed und JET_bitColumnTagged unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6c338-250">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="6c338-251">Dies bedeutet, dass es nicht möglich ist, eine automatische Inkrement-, Versions-oder mehrwertige Spalte in einer temporären Tabelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6c338-251">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="6c338-252">Zum Schluss werden die Spalten zum Aktualisieren von Spalten nicht unterstützt, da Sie in einer temporären Tabelle nicht nützlich sind, da Sie nur von einer Sitzung gleichzeitig verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6c338-252">Finally, escrow update columns are not supported because they are not useful in a temporary table since they can only be used by one session at a time.</span></span> <span data-ttu-id="6c338-253">Wenn eine dieser Optionen angefordert wird, werden Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6c338-253">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="6c338-254">Temporäre Tabellen unterstützen keine Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="6c338-254">Temporary tables do not support default values.</span></span> <span data-ttu-id="6c338-255">Wenn eine Spaltendefinition bereitgestellt wird, die eine Standardwert Spezifikation enthält, wird diese Angabe ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6c338-255">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="6c338-256">Temporäre Tabellen werden als Ergebnis vieler unterschiedlicher ESE-Funktionen an den Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6c338-256">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="6c338-257">Beispielsweise gibt [jetgetindexinfo](./jetgetindexinfo-function.md) mit der JET_IdxInfo-Option, die im *infolevel* -Parameter festgelegt ist, eine temporäre Tabelle zurück, die eine Liste aller Schlüssel Spalten in einem bestimmten Index enthält.</span><span class="sxs-lookup"><span data-stu-id="6c338-257">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set in the *InfoLevel* parameter will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="6c338-258">Die temporären Tabellen folgen den gleichen Lebenszyklus Regeln wie gewöhnliche temporäre Tabellen, wie hier beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6c338-258">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="6c338-259">Temporäre Tabellen werden auch intern von der Datenbank-Engine für viele Tasks verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c338-259">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="6c338-260">Die wichtigsten dieser Aufgaben sind die Erstellung eines Indexes für eine vorhandene Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6c338-260">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="6c338-261">Eine temporäre Tabelle wird zum Sortieren der Index Schlüssel verwendet, die zum Erstellen dieses Indexes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c338-261">A temporary table will be used to sort the index keys used to construct that index.</span></span>

<span data-ttu-id="6c338-262">Alle temporären Tabellen werden in der temporären Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6c338-262">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="6c338-263">Die temporäre Datenbank ist eine spezielle Datenbankdatei, die während der Lebensdauer einer ESE-Instanz verwaltet wird und gelöscht wird, wenn diese Instanz heruntergefahren oder neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="6c338-263">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="6c338-264">Der Speicherort der temporären Datenbank kann mithilfe von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit [JET_paramTempPath](./temporary-database-parameters.md)konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="6c338-264">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="6c338-265">Die Platzierung der temporären Datenbank auf dem Datenträger in Relation zu den Transaktionsprotokoll Dateien und Datenbankdateien ist möglicherweise wichtig, wenn die Anwendung temporäre Tabellen stark nutzt oder häufig Indizes erstellt.</span><span class="sxs-lookup"><span data-stu-id="6c338-265">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="6c338-266">Der Lebenszyklus einer temporären Tabelle ist an die Cursor gebunden, die auf diese Tabelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="6c338-266">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="6c338-267">Wenn alle Cursor, die auf eine temporäre Tabelle verweisen, entweder implizit oder explizit geschlossen werden, wird die temporäre Tabelle gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6c338-267">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="6c338-268">Wenn eine temporäre Tabelle innerhalb einer Transaktion erstellt wird und anschließend ein Rollback für diese Transaktion ausgeführt wird, wird die temporäre Tabelle gelöscht, da alle Cursor, auf die Sie zu diesem Zeitpunkt verwiesen hat, implizit geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6c338-268">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="6c338-269">Neue Cursor können nur durch die Verwendung von [jetdupcursor](./jetdupcursor-function.md)auf eine temporäre Tabelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="6c338-269">New cursors may reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="6c338-270">In diesem Fall werden die neuen Cursor auf dem ersten Index Eintrag der temporären Tabelle positioniert.</span><span class="sxs-lookup"><span data-stu-id="6c338-270">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="6c338-271">[Jetdupcursor](./jetdupcursor-function.md) funktioniert nur in bestimmten Phasen der Verwendung für die temporäre Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6c338-271">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="6c338-272">Weitere Informationen finden Sie in den Hinweisen zu den Cursor Funktionen für temporäre Tabellen.</span><span class="sxs-lookup"><span data-stu-id="6c338-272">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="6c338-273">Es ist nicht möglich, auf eine temporäre Tabelle von mehreren Sitzungen gleichzeitig zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="6c338-273">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="6c338-274">In [jetdupcursor](./jetdupcursor-function.md) liegt ein wichtiges Problem vor, das sich auf temporäre Tabellen auswirkt.</span><span class="sxs-lookup"><span data-stu-id="6c338-274">There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="6c338-275">Wenn versucht wird, eine temporäre Tabelle zu duplizieren, die sich im vorwärts Modus befindet, wird der resultierende Cursor nicht ordnungsgemäß erstellt und funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="6c338-275">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="6c338-276">Es ist immer noch sicher, einen Cursor über eine materialisierte temporäre Tabelle zu duplizieren.</span><span class="sxs-lookup"><span data-stu-id="6c338-276">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="6c338-277">Der temporäre Tabellen-Manager kann eine temporäre Tabelle auf drei Arten implementieren.</span><span class="sxs-lookup"><span data-stu-id="6c338-277">The temporary table manager may choose to implement a temporary table in three ways.</span></span> <span data-ttu-id="6c338-278">Die erste Methode besteht darin, eine in-Memory-Tabelle beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="6c338-278">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="6c338-279">Diese Strategie ist der schnellste, kann aber nur für kleine, einfache temporäre Tabellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c338-279">This strategy is the fastest but can only be used for small, simple temporary tables.</span></span> <span data-ttu-id="6c338-280">Die zweite Methode besteht darin, eine Datenträger basierte Sortierung zu erstellen, die mit einem vorwärts-Iterator gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6c338-280">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="6c338-281">Diese Strategie kann nur unter bestimmten Umständen verwendet werden und ist die schnellste Möglichkeit, Duplikate aus einem sehr großen Dataset zu sortieren und zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="6c338-281">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="6c338-282">Die dritte Methode ist das Erstellen einer B +-Struktur in der temporären Datenbank, um die temporäre Tabelle zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6c338-282">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="6c338-283">Diese Strategie ist die langsamste, aber die vielseitigste und wird als materialisierte temporäre Tabelle bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6c338-283">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="6c338-284">Diese Strategien können in Kombination verwendet werden, um letztendlich die von der temporären Tabelle angeforderte Funktionalität zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="6c338-284">These strategies may be used in combination to ultimately achieve the functionality requested of the temporary table.</span></span>

<span data-ttu-id="6c338-285">Wenn die temporäre Tabelle nicht materialisiert ist, wird Sie in erster Linie in zwei Hauptphasen verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c338-285">When the temporary table is not materialized then it is used in primarily two major phases.</span></span> <span data-ttu-id="6c338-286">Die erste Phase ist die Einfügungs Phase, in der die Tabelle mit dem ersten DataSet aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="6c338-286">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="6c338-287">In dieser Phase ist nur die Daten Einfügung zulässig.</span><span class="sxs-lookup"><span data-stu-id="6c338-287">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="6c338-288">Diese Phase endet, wenn versucht wird, den Cursor mithilfe von [jetmove](./jetmove-function.md) oder [JetSeek](./jetseek-function.md)zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="6c338-288">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="6c338-289">Die zweite Phase ist die Daten Extraktions Phase.</span><span class="sxs-lookup"><span data-stu-id="6c338-289">The second phase is the data extraction phase.</span></span> <span data-ttu-id="6c338-290">In dieser Phase können die in der temporären Tabelle gespeicherten Daten gemäß den Funktionen extrahiert werden, die beim Erstellen der temporären Tabelle angefordert wurden.</span><span class="sxs-lookup"><span data-stu-id="6c338-290">During this phase, the data stored in the temporary table may be extracted according to the capabilities requested when the temporary table was created.</span></span>

<span data-ttu-id="6c338-291">**Cursor Funktionen für temporäre Tabellen**</span><span class="sxs-lookup"><span data-stu-id="6c338-291">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="6c338-292">Wenn die temporäre Tabelle materialisiert ist, verfügt der Cursor über die folgenden Funktionen, kann jedoch durch die angeforderten Optionen weiter eingeschränkt werden:</span><span class="sxs-lookup"><span data-stu-id="6c338-292">When the temporary table is materialized, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="6c338-293">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="6c338-293">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="6c338-294">Jetdelete</span><span class="sxs-lookup"><span data-stu-id="6c338-294">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="6c338-295">Jetdupcursor</span><span class="sxs-lookup"><span data-stu-id="6c338-295">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="6c338-296">Jetenreeratecolumschlag</span><span class="sxs-lookup"><span data-stu-id="6c338-296">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="6c338-297">Jetescrowupdate</span><span class="sxs-lookup"><span data-stu-id="6c338-297">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="6c338-298">Jetgetbookmark</span><span class="sxs-lookup"><span data-stu-id="6c338-298">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="6c338-299">Jetgetcursor Info</span><span class="sxs-lookup"><span data-stu-id="6c338-299">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="6c338-300">Jetgetls</span><span class="sxs-lookup"><span data-stu-id="6c338-300">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="6c338-301">Jetgetrecordsize</span><span class="sxs-lookup"><span data-stu-id="6c338-301">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="6c338-302">Jetgettableinfo</span><span class="sxs-lookup"><span data-stu-id="6c338-302">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="6c338-303">Jetgojebookmark</span><span class="sxs-lookup"><span data-stu-id="6c338-303">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="6c338-304">Jetmakekey</span><span class="sxs-lookup"><span data-stu-id="6c338-304">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="6c338-305">Jetmove</span><span class="sxs-lookup"><span data-stu-id="6c338-305">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="6c338-306">Jetprepareupdate</span><span class="sxs-lookup"><span data-stu-id="6c338-306">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="6c338-307">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="6c338-307">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="6c338-308">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="6c338-308">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="6c338-309">Jetretrievekey</span><span class="sxs-lookup"><span data-stu-id="6c338-309">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="6c338-310">JetSeek</span><span class="sxs-lookup"><span data-stu-id="6c338-310">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="6c338-311">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="6c338-311">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="6c338-312">Jetsetcolumns</span><span class="sxs-lookup"><span data-stu-id="6c338-312">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="6c338-313">Jetsetindexrange</span><span class="sxs-lookup"><span data-stu-id="6c338-313">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="6c338-314">Jetsetls</span><span class="sxs-lookup"><span data-stu-id="6c338-314">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="6c338-315">Jetupdate</span><span class="sxs-lookup"><span data-stu-id="6c338-315">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="6c338-316">Wenn die temporäre Tabelle nicht materialisiert wird und sich in der einfügephase befindet, verfügt der Cursor über die folgenden Funktionen, kann jedoch durch die angeforderten Optionen weiter eingeschränkt werden:</span><span class="sxs-lookup"><span data-stu-id="6c338-316">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="6c338-317">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="6c338-317">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="6c338-318">Jetescrowupdate</span><span class="sxs-lookup"><span data-stu-id="6c338-318">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="6c338-319">Jetmakekey</span><span class="sxs-lookup"><span data-stu-id="6c338-319">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="6c338-320">Jetmove</span><span class="sxs-lookup"><span data-stu-id="6c338-320">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="6c338-321">**Hinweis**  Bewirkt einen Übergang zur Extrahierungs Phase.</span><span class="sxs-lookup"><span data-stu-id="6c338-321">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="6c338-322">Jetprepareupdate</span><span class="sxs-lookup"><span data-stu-id="6c338-322">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="6c338-323">Jetretrievekey</span><span class="sxs-lookup"><span data-stu-id="6c338-323">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="6c338-324">JetSeek</span><span class="sxs-lookup"><span data-stu-id="6c338-324">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="6c338-325">**Hinweis**  Bewirkt einen Übergang zur Extrahierungs Phase.</span><span class="sxs-lookup"><span data-stu-id="6c338-325">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="6c338-326">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="6c338-326">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="6c338-327">Jetsetcolumns</span><span class="sxs-lookup"><span data-stu-id="6c338-327">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="6c338-328">Jetupdate</span><span class="sxs-lookup"><span data-stu-id="6c338-328">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="6c338-329">Wenn die temporäre Tabelle nicht materialisiert wird und sich in der Extrahierungs Phase befindet, verfügt der Cursor über die folgenden Funktionen, kann jedoch durch die angeforderten Optionen weiter eingeschränkt werden:</span><span class="sxs-lookup"><span data-stu-id="6c338-329">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="6c338-330">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="6c338-330">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="6c338-331">Jetdupcursor</span><span class="sxs-lookup"><span data-stu-id="6c338-331">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="6c338-332">**Hinweis**  Wenn versucht wird, eine temporäre Tabelle zu duplizieren, die sich im vorwärts Modus befindet, wird der resultierende Cursor nicht ordnungsgemäß erstellt und funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="6c338-332">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="6c338-333">Es ist immer noch sicher, einen Cursor über eine materialisierte temporäre Tabelle zu duplizieren.</span><span class="sxs-lookup"><span data-stu-id="6c338-333">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="6c338-334">Jetenreeratecolumschlag</span><span class="sxs-lookup"><span data-stu-id="6c338-334">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="6c338-335">Jetgetbookmark</span><span class="sxs-lookup"><span data-stu-id="6c338-335">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="6c338-336">Jetgetls</span><span class="sxs-lookup"><span data-stu-id="6c338-336">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="6c338-337">Jetgetrecordsize</span><span class="sxs-lookup"><span data-stu-id="6c338-337">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="6c338-338">Jetgettableinfo</span><span class="sxs-lookup"><span data-stu-id="6c338-338">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="6c338-339">Jetgojebookmark</span><span class="sxs-lookup"><span data-stu-id="6c338-339">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="6c338-340">Jetmakekey</span><span class="sxs-lookup"><span data-stu-id="6c338-340">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="6c338-341">Jetmove</span><span class="sxs-lookup"><span data-stu-id="6c338-341">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="6c338-342">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="6c338-342">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="6c338-343">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="6c338-343">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="6c338-344">Jetretrievekey</span><span class="sxs-lookup"><span data-stu-id="6c338-344">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="6c338-345">JetSeek</span><span class="sxs-lookup"><span data-stu-id="6c338-345">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="6c338-346">Jetsetindexrange</span><span class="sxs-lookup"><span data-stu-id="6c338-346">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="6c338-347">Jetsetls</span><span class="sxs-lookup"><span data-stu-id="6c338-347">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="6c338-348">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c338-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c338-349"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6c338-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6c338-350">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6c338-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-351"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6c338-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6c338-352">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6c338-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-353"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6c338-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6c338-354">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="6c338-354">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c338-355"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="6c338-355"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6c338-356">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6c338-356">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c338-357"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6c338-357"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6c338-358">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6c338-358">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6c338-359">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6c338-359">See Also</span></span>

[<span data-ttu-id="6c338-360">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="6c338-360">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="6c338-361">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="6c338-361">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="6c338-362">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6c338-362">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6c338-363">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6c338-363">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6c338-364">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6c338-364">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6c338-365">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="6c338-365">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="6c338-366">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="6c338-366">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="6c338-367">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="6c338-367">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="6c338-368">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="6c338-368">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="6c338-369">Jetdupcursor</span><span class="sxs-lookup"><span data-stu-id="6c338-369">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="6c338-370">Jetmove</span><span class="sxs-lookup"><span data-stu-id="6c338-370">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="6c338-371">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="6c338-371">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="6c338-372">JetSeek</span><span class="sxs-lookup"><span data-stu-id="6c338-372">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="6c338-373">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="6c338-373">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="6c338-374">Temporäre Daten Bank Parameter</span><span class="sxs-lookup"><span data-stu-id="6c338-374">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)
