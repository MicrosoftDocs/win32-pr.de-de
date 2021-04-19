---
description: 'Weitere Informationen finden Sie hier: JetCreateTableColumnIndex4W-Funktion'
title: JetCreateTableColumnIndex4W-Funktion
TOCTitle: JetCreateTableColumnIndex4W Function
ms:assetid: 5a74b397-dfb4-4a1d-807b-284329239bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835042(v=EXCHG.10)
ms:contentKeyID: 49894664
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateTableColumnIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ebdb8cf62123febe2d44b5a638c285c180062c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366309"
---
# <a name="jetcreatetablecolumnindex4w-function"></a><span data-ttu-id="6d1ed-103">JetCreateTableColumnIndex4W-Funktion</span><span class="sxs-lookup"><span data-stu-id="6d1ed-103">JetCreateTableColumnIndex4W Function</span></span>


<span data-ttu-id="6d1ed-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6d1ed-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="6d1ed-105">Die **JetCreateTableColumnIndex4W** -Funktion erstellt eine Tabelle in einem Extensible Storage Engine (ESE (Datenbank mit einem anfänglichen Satz von Indizes und ein ursprünglicher Satz von Spalten aus einem Array von [JET_TABLECREATE3](./jet-tablecreate3-structure.md) Strukturen).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-105">The **JetCreateTableColumnIndex4W** function creates a table in an Extensible Storage Engine (ESE( database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structures.</span></span> <span data-ttu-id="6d1ed-106">Die [JET_TABLECREATE3](./jet-tablecreate3-structure.md) -Struktur ermöglicht das Angeben einer Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-106">The [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="6d1ed-107">Die **JetCreateTableColumnIndex4W** -Funktion wurde im Windows 8-Betriebssystem eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-107">The **JetCreateTableColumnIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a><span data-ttu-id="6d1ed-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d1ed-108">Parameters</span></span>

<span data-ttu-id="6d1ed-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="6d1ed-109">*sesid*</span></span>

<span data-ttu-id="6d1ed-110">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="6d1ed-111">*DBID*</span><span class="sxs-lookup"><span data-stu-id="6d1ed-111">*dbid*</span></span>

<span data-ttu-id="6d1ed-112">Der für den API-Befehl zu verwendende Daten Bank Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-112">The database identifier to use for the API call.</span></span>

<span data-ttu-id="6d1ed-113">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="6d1ed-113">*ptablecreate*</span></span>

<span data-ttu-id="6d1ed-114">Ein Zeiger auf eine [JET_TABLECREATE3](./jet-tablecreate3-structure.md) -Struktur, die die zu erstellende Tabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-114">A pointer to a [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure that defines the table to be created.</span></span> <span data-ttu-id="6d1ed-115">Weitere Informationen finden Sie unter [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="6d1ed-115">See [JET_TABLECREATE3](./jet-tablecreate3-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="6d1ed-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d1ed-116">Return value</span></span>

<span data-ttu-id="6d1ed-117">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="6d1ed-118">Weitere Informationen zu den möglichen ESE-Fehlern (Extensible Storage Enginge) finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-118">For more information about the possible Extensible Storage Enginge (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d1ed-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6d1ed-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="6d1ed-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d1ed-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6d1ed-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-122">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-123">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="6d1ed-123">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-124">Die Rückruffunktion konnte nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-124">The callback function could not be resolved.</span></span> <span data-ttu-id="6d1ed-125">Die dll wurde möglicherweise nicht gefunden, oder die Funktion in der dll wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-125">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="6d1ed-126">Wenn eine ausreichende Protokollierung aktiviert ist, werden im Ereignisprotokoll weitere Details angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-126">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-127">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="6d1ed-127">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-128">Es wurde versucht, über eine Spalte vom Typ "Escrow-Update" oder "SLV" zu indizieren (Beachten Sie, dass SLV-Spalten veraltet sind).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-128">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-129">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="6d1ed-129">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-130">Wird zurückgegeben, wenn der <em>ptablecreate- &gt; grbit-</em> Parameter den JET_bitTableCreateTemplateTable Wert angibt, der <em>ptablecreate- &gt; sztemplatetablename</em> -Parameter jedoch auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-130">Returned if the <em>ptablecreate-&gt;grbit</em> parameter specifies the JET_bitTableCreateTemplateTable value, but the <em>ptablecreate-&gt;szTemplateTableName</em> parameter is set to null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-131">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="6d1ed-131">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-132">Eine Spalte ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-132">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="6d1ed-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-134">Es wurde versucht, einen Index für eine nicht vorhandene Spalte zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-134">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="6d1ed-135">Der Versuch, bedingt eine Indizierung über eine nicht vorhandene Spalte durchführen zu können, kann ebenfalls diesen Fehler verursachen.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-135">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-136">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="6d1ed-136">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-137">Es wurde versucht, eine redundante Spalte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-137">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="6d1ed-138">Es darf nicht mehr als eine AUTOINCREMENT-Spalte vorhanden sein, und es sollte nicht mehr als eine Versions Spalte pro Tabelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-138">No more than one autoincrement column should exist, and no more than one version column should exist per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-139">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="6d1ed-139">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-140">Dieser Fehler wird zurückgegeben, wenn der <strong>uldensity</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur auf eine Zahl kleiner als 20 oder mehr als 100 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-140">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-141">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="6d1ed-141">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-142">Gibt an, dass die Tabelle im <strong>sztemplatetablename</strong> -Member der <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> Struktur nicht als Vorlagen Tabelle gekennzeichnet ist (d. h., für diese Tabelle wurde der JET_bitTableCreateTemplateTable Parameterwert nicht festgelegt).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-142">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure was not marked as a template table (that is, that table did not have the JET_bitTableCreateTemplateTable parameter value set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-143">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="6d1ed-143">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-144">Es wurde versucht, zwei identische Indizes zu definieren.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-144">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-145">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="6d1ed-145">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-146">Es wurde versucht, mehr als einen primären Index für eine Tabelle anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-146">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="6d1ed-147">Eine Tabelle muss genau einen primären Index aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-147">A table must have exactly one primary index.</span></span> <span data-ttu-id="6d1ed-148">Wenn kein primärer Index angegeben ist, wird von der Datenbank-Engine eine transparente Erstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-148">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-149">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="6d1ed-149">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-150">Es wurde eine ungültige Index Definition angegeben.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-150">An invalid index definition was specified.</span></span> <span data-ttu-id="6d1ed-151">Im folgenden sind die möglichen Ursachen für diesen Fehler aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="6d1ed-151">The following are some of the possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="6d1ed-152">Ein primärer Index ist bedingt (d. h., der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur hat den JET_bitIndexPrimary Wert festgelegt, und der <strong>cconditionalcolumn</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur ist größer als 0 (null)).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-152">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexPrimary value set, and the <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="6d1ed-153">Gilt für Versionen des Windows Server-Betriebssystems, beginnend mit Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-153">Applies to versions of the Windows Server operating system starting with Windows Server 2003.</span></span> <span data-ttu-id="6d1ed-154">Es wurde versucht, einen Tupelindex mit tupellimits zu erstellen, ohne den <strong>ptuplelimits</strong> -Member in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur zu übergeben (d. h., der <strong>grbit</strong> -Member der <strong>JET_INDEXCREATE2</strong> Struktur hat JET_bitIndexTupleLimits Wert festgelegt, der <strong>ptuplelimits</strong> -Zeiger ist jedoch NULL).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-154">An attempt to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure (that is, the <strong>grbit</strong> member of the <strong>JET_INDEXCREATE2</strong> structure has JET_bitIndexTupleLimits value set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="6d1ed-155">Übergeben einer ungültigen Schlüssel Definition im <strong>szkey</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-155">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="6d1ed-156">Informationen zu gültigen Definitionen finden Sie unter <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-156">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="6d1ed-157">Das Festlegen des <strong>cbvarsegmac</strong> -Members in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> muss größer sein als der JET_cbPrimaryKeyMost Wert (für einen primären Index) oder größer als der JET_cbSecondaryKeyMost Wert (für einen sekundären Index).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-157">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than the JET_cbPrimaryKeyMost value (for a primary index) or greater than the JET_cbSecondaryKeyMost value (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="6d1ed-158">Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einen, bei dem das JET_bitIndexUnicode-wertbit im <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-158">Passing an invalid combination for a user-defined Unicode index (one that has the JET_bitIndexUnicode value bit set in the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span> <span data-ttu-id="6d1ed-159">Zu den häufigsten Gründen gehören das <strong>pidxunicode</strong> -Element der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur ist NULL, oder die in der <strong>pidxunicode</strong> -Struktur angegebene LCID ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-159">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="6d1ed-160">Angeben einer mehrwertigen Spalte für einen primären Index.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-160">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="6d1ed-161">Es wird versucht, zu viele bedingte Spalten zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-161">Trying to index too many conditional columns.</span></span> <span data-ttu-id="6d1ed-162">Der <strong>cconditionalcolumn</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur darf nicht größer als <strong>JET_ccolKeyMost</strong>sein.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-162">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-163">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="6d1ed-163">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-164">Gilt für Windows-Versionen ab Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="6d1ed-165">Es wurde eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur angegeben, und ihre Grenzen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-165">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="6d1ed-166">Weitere Informationen finden Sie im Abschnitt "Hinweise" in der <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-166">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-167">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="6d1ed-167">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-168">Gilt für Windows-Versionen ab Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="6d1ed-169">Ein Tupelindex kann nicht eindeutig sein (d. h., für den <em>grbit</em> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur dürfen nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexUnique Werte festgelegt sein).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-169">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique values set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-170">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="6d1ed-170">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-171">Gilt für Windows-Versionen ab Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-171">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="6d1ed-172">Ein Tupelindex kann nur über eine einzelne Spalte verfügen (d. h., wenn für das <strong>grbit</strong> -Element der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur JET_bitIndexTuples Wert festgelegt wurde und der <strong>szkey</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur mehr als eine Spalte angibt).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-172">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples value set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-173">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="6d1ed-173">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-174">Gilt für Windows-Versionen ab Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-174">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="6d1ed-175">Bei einem Tupelindex kann es sich nicht um einen primären Index handeln (d. h., der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexTuples festgelegt werden).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-175">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-176">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="6d1ed-176">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-177">Gilt für Windows-Versionen ab Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-177">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="6d1ed-178">Ein Tupelindex kann nur für eine Text-oder Unicode-Spalte gelten.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-178">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="6d1ed-179">Der Versuch, andere Spalten (z. b. binäre Spalten) zu indizieren, führt zu einem JET_errIndexTuplesTextColumnsOnly-Antwort Code.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-179">An attempt to index other columns (such as binary columns) will result in a JET_errIndexTuplesTextColumnsOnly response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-180">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="6d1ed-180">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-181">Gilt für Windows-Versionen ab Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-181">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="6d1ed-182">Ein Tupelindex lässt nicht zu, dass der <strong>cbvarsegmac</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-182">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-183">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="6d1ed-183">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-184">Es wurde versucht, einen Index ohne Versionsinformationen zu erstellen, während eine Transaktion durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-184">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-185">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="6d1ed-185">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-186">Der <strong>CP</strong> -Member der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur wurde nicht auf eine gültige Codepage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-186">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="6d1ed-187">Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-187">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="6d1ed-188">Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-188">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-189">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="6d1ed-189">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-190">Der <strong>colttmember</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur wurde nicht auf einen gültigen Spaltentyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-190">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-191">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="6d1ed-191">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-192">Im folgenden sind einige Gründe aufgeführt, warum dieser Fehler auftreten kann:</span><span class="sxs-lookup"><span data-stu-id="6d1ed-192">The following are some reasons why this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="6d1ed-193">Der <strong>rgindexcreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> Struktur wurde auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-193">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="6d1ed-194">Der <strong>rgcolumncreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> Struktur wurde auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-194">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="6d1ed-195">Der <strong>cbStruct</strong> -Member einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur wurde nicht auf einen gültigen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-195">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-196">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="6d1ed-196">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-197">In der <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> Struktur wurde eine ungültige Kombination von <strong>grbit</strong> -Membern angegeben.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-197">An invalid combination of <strong>grbit</strong> members was specified in the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure.</span></span></p>
<p><span data-ttu-id="6d1ed-198">Die Index Definition ist ungültig, da der <strong>grbit</strong> -Member inkonsistente Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-198">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="6d1ed-199">Folgende Ursachen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="6d1ed-199">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="6d1ed-200">Für einen primären Index wurde ein Ignore-Bit angegeben (d. h. JET_bitIndexPrimary Wert wurde mit den Werten JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull oder JET_bitIndexIgnoreFirstNull) übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-200">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary value was passed with the JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull values).</span></span></p></li>
<li><p><span data-ttu-id="6d1ed-201">Ein leerer Index ignoriert keine NULL-Elemente (d. h., der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur hat den JET_bitIndexEmpty Wert festgelegt, aber nicht JET_bitIndexIgnoreAnyNull Wert festgelegt).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-201">An empty index does not ignore any null members (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexEmpty value set, but does not have JET_bitIndexIgnoreAnyNull value set).</span></span></p></li>
<li><p><span data-ttu-id="6d1ed-202">Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> -Struktur mit einem ungültigen <strong>grbit</strong> -Member.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-202">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="6d1ed-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-204">Es wurde eine ungültige Gebiets Schema-ID (LCID) übergeben (entweder über den <strong>LCID</strong> -Member der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> -Struktur, auf die der <strong>pidxunicode</strong> -Member in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur verweist, oder über das <strong>LCID</strong> -Feld der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur).</span><span class="sxs-lookup"><span data-stu-id="6d1ed-204">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure that the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure points to, or through the <strong>lcid</strong> field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-205">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6d1ed-205">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-206">Ein ungültiger Parameter wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-206">An invalid parameter was given.</span></span> <span data-ttu-id="6d1ed-207">Folgende Ursachen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="6d1ed-207">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="6d1ed-208">Der <strong>rgcolumncreate</strong> -Member der <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> -Struktur ist NULL.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-208">The <strong>rgcolumncreate</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure is null.</span></span></p></li>
<li><p><span data-ttu-id="6d1ed-209">Der <strong>cbStruct</strong> -Member einer der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Strukturen, die im <strong>rgcolumncreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> -Struktur angegeben sind, wurde nicht auf sizeof (JET_COLUMNCREATE) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-209">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="6d1ed-210">Der <strong>cbkey</strong> -Member einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur ist auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-210">The <strong>cbKey</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="6d1ed-211">Der <strong>cbStruct</strong> -Member einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur ist nicht auf sizeof (JET_INDEXCREATE2) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-211">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( JET_INDEXCREATE2 ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-212">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="6d1ed-212">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-213">Der Datensatz ist zu groß.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-213">The record is too big.</span></span> <span data-ttu-id="6d1ed-214">Die Summe des <strong>cbmax</strong> -Members der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur für alle festgelegten Spalten darf einen bestimmten Wert nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-214">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-215">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="6d1ed-215">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-216">Die Tabelle ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-216">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-217">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="6d1ed-217">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-218">Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-218">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="6d1ed-219">Eine Tabelle kann nicht mehr als <strong>JET_ccolFixedMost</strong> fester Spalten, nicht mehr als <strong>JET_ccolVarMost</strong> Spalten variabler Länge und nicht mehr als <strong>JET_ccolTaggedMost</strong> markierte Spalten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-219">A table can have no more than <strong>JET_ccolFixedMost</strong> fixed columns, no more than <strong>JET_ccolVarMost</strong> variable-length columns, and no more than <strong>JET_ccolTaggedMost</strong> tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-220">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="6d1ed-220">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-221">Fehler beim Versuch, eine Unicode-Spalte zu normalisieren.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-221">An error occurred when an attempt was made to normalize a Unicode column.</span></span> <span data-ttu-id="6d1ed-222">Dies kann darauf zurückzuführen sein, dass die Systemressourcen nicht mehr ausreichen.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-222">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-223">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="6d1ed-223">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="6d1ed-224">Ein Element der Jet-Raum Hinweise-Struktur war nicht korrekt oder kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-224">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="6d1ed-225">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d1ed-225">Remarks</span></span>

<span data-ttu-id="6d1ed-226">Die **JetCreateTableColumnIndex4W** -Funktion erstellt eine Tabelle mit einem anfänglichen Satz von Spalten und Indizes.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-226">The **JetCreateTableColumnIndex4W** function creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="6d1ed-227">Zusätzliche Spalten und Indizes können mithilfe der Funktionen [jetaddcolumn](./jetaddcolumn-function.md), [jetdeletecolumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [jetkreateindex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md)und [jetdeleteindex](./jetdeleteindex-function.md) dynamisch hinzugefügt und entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-227">Additional columns and indexes can be added and removed dynamically by means of the [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md) functions.</span></span>

<span data-ttu-id="6d1ed-228">Wie bei der [jetopentable](./jetopentable-function.md) -Funktion sollte die [jetclosetable](./jetclosetable-function.md) -Funktion die Anwendung schließen, wenn die Anwendung mit der zurückgegebenen *TableID*-Funktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-228">As with the [JetOpenTable](./jetopentable-function.md) function, when the application is done using the returned *tableid*, the [JetCloseTable](./jetclosetable-function.md) function should close the application.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6d1ed-229">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d1ed-229">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-230"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ed-230"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6d1ed-231">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-231">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-232"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ed-232"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6d1ed-233">Erfordert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-233">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-234"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ed-234"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6d1ed-235">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-235">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d1ed-236"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ed-236"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6d1ed-237">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-237">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d1ed-238"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6d1ed-238"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6d1ed-239">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6d1ed-239">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6d1ed-240">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d1ed-240">See also</span></span>

[<span data-ttu-id="6d1ed-241">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="6d1ed-241">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="6d1ed-242">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="6d1ed-242">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="6d1ed-243">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6d1ed-243">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6d1ed-244">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6d1ed-244">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6d1ed-245">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="6d1ed-245">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="6d1ed-246">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="6d1ed-246">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="6d1ed-247">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6d1ed-247">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6d1ed-248">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="6d1ed-248">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="6d1ed-249">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="6d1ed-249">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="6d1ed-250">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="6d1ed-250">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)  
[<span data-ttu-id="6d1ed-251">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="6d1ed-251">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="6d1ed-252">Jetaddcolumn</span><span class="sxs-lookup"><span data-stu-id="6d1ed-252">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="6d1ed-253">Jetkreateingedex</span><span class="sxs-lookup"><span data-stu-id="6d1ed-253">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="6d1ed-254">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="6d1ed-254">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="6d1ed-255">JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="6d1ed-255">JetCreateIndex3</span></span>](./jetcreateindex3-function.md)  
[<span data-ttu-id="6d1ed-256">Jetkreatetable</span><span class="sxs-lookup"><span data-stu-id="6d1ed-256">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="6d1ed-257">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="6d1ed-257">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="6d1ed-258">Jetdeletecolumn</span><span class="sxs-lookup"><span data-stu-id="6d1ed-258">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="6d1ed-259">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="6d1ed-259">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
