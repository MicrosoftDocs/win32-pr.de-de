---
description: 'Weitere Informationen finden Sie hier: JetCreateTableColumnIndex3-Funktion'
title: JetCreateTableColumnIndex3-Funktion
TOCTitle: JetCreateTableColumnIndex3 Function
ms:assetid: c1a1b091-b4a6-4cdc-a0ea-af21c1462449
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294079(v=EXCHG.10)
ms:contentKeyID: 32765694
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex3
- JetCreateTableColumnIndex3W
- JetCreateTableColumnIndex3A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf1d6aed3178f5593826097f8c5d6b01bd8c72d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355441"
---
# <a name="jetcreatetablecolumnindex3-function"></a><span data-ttu-id="ac393-103">JetCreateTableColumnIndex3-Funktion</span><span class="sxs-lookup"><span data-stu-id="ac393-103">JetCreateTableColumnIndex3 Function</span></span>


<span data-ttu-id="ac393-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ac393-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetablecolumnindex3-function"></a><span data-ttu-id="ac393-105">JetCreateTableColumnIndex3-Funktion</span><span class="sxs-lookup"><span data-stu-id="ac393-105">JetCreateTableColumnIndex3 Function</span></span>

<span data-ttu-id="ac393-106">Die **JetCreateTableColumnIndex3** -Funktion erstellt eine Tabelle in einer ESE-Datenbank mit einem anfänglichen Satz von Indizes und einem anfänglichen Satz von Spalten aus einem Array von [JET_TABLECREATE3](./jet-tablecreate3-structure.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="ac393-106">The **JetCreateTableColumnIndex3** function creates a table in an ESE database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structures.</span></span> <span data-ttu-id="ac393-107">Die [JET_TABLECREATE3](./jet-tablecreate3-structure.md) -Struktur ermöglicht das Angeben einer Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="ac393-107">The [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="ac393-108">**Windows 7:** **JetCreateTableColumnIndex3** wird im Betriebssystem Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ac393-108">**Windows 7:** **JetCreateTableColumnIndex3** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex3(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE3* ptablecreate
    );
```

### <a name="parameters"></a><span data-ttu-id="ac393-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac393-109">Parameters</span></span>

<span data-ttu-id="ac393-110">*-sid*</span><span class="sxs-lookup"><span data-stu-id="ac393-110">*sesid*</span></span>

<span data-ttu-id="ac393-111">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="ac393-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="ac393-112">*DBID*</span><span class="sxs-lookup"><span data-stu-id="ac393-112">*dbid*</span></span>

<span data-ttu-id="ac393-113">Der für den API-Befehl zu verwendende Daten Bank Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="ac393-113">The database identifier to use for the API call.</span></span>

<span data-ttu-id="ac393-114">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="ac393-114">*ptablecreate*</span></span>

<span data-ttu-id="ac393-115">Ein Zeiger auf eine [JET_TABLECREATE3](./jet-tablecreate3-structure.md) -Struktur, die die zu erstellende Tabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="ac393-115">A pointer to a [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure that defines the table to be created.</span></span> <span data-ttu-id="ac393-116">Weitere Informationen finden Sie unter [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="ac393-116">See [JET_TABLECREATE3](./jet-tablecreate3-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="ac393-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac393-117">Return Value</span></span>

<span data-ttu-id="ac393-118">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="ac393-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ac393-119">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ac393-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ac393-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ac393-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="ac393-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac393-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac393-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ac393-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ac393-123">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ac393-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-124">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="ac393-124">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="ac393-125">Die Rückruffunktion konnte nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="ac393-125">The callback function could not be resolved.</span></span> <span data-ttu-id="ac393-126">Die dll wurde möglicherweise nicht gefunden, oder die Funktion in der dll wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ac393-126">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="ac393-127">Wenn eine ausreichende Protokollierung aktiviert ist, werden im Ereignisprotokoll weitere Details angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac393-127">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-128">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="ac393-128">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="ac393-129">Es wurde versucht, über eine Spalte vom Typ "Escrow-Update" oder "SLV" zu indizieren (Beachten Sie, dass SLV-Spalten veraltet sind).</span><span class="sxs-lookup"><span data-stu-id="ac393-129">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-130">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="ac393-130">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="ac393-131">, Wenn ptablecreate- &gt; grbit JET_bitTableCreateTemplateTable angibt, ptablecreate- &gt; sztemplatetablename jedoch auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ac393-131">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-132">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="ac393-132">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="ac393-133">Eine Spalte ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ac393-133">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-134">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="ac393-134">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="ac393-135">Es wurde versucht, eine nicht vorhandene Spalte zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="ac393-135">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="ac393-136">Der Versuch, bedingt eine Indizierung über eine nicht vorhandene Spalte durchführen zu können, kann ebenfalls diesen Fehler verursachen.</span><span class="sxs-lookup"><span data-stu-id="ac393-136">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-137">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="ac393-137">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="ac393-138">Es wurde versucht, eine redundante Spalte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ac393-138">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="ac393-139">Es darf nicht mehr als eine AUTOINCREMENT-Spalte und höchstens eine Versions Spalte pro Tabelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ac393-139">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-140">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="ac393-140">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="ac393-141">Dieser Fehler wird zurückgegeben, wenn der <strong>uldensity</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur auf eine Zahl kleiner als 20 oder mehr als 100 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ac393-141">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-142">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="ac393-142">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="ac393-143">Gibt an, dass die Tabelle im <strong>sztemplatetablename</strong> -Member der <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> Struktur nicht als Vorlagen Tabelle gekennzeichnet ist (d. h., dass die Tabelle nicht über JET_bitTableCreateTemplateTable festgelegt wurde).</span><span class="sxs-lookup"><span data-stu-id="ac393-143">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure was not marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-144">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="ac393-144">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="ac393-145">Es wurde versucht, zwei identische Indizes zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ac393-145">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-146">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="ac393-146">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="ac393-147">Es wurde versucht, mehr als einen primären Index für eine Tabelle anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ac393-147">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="ac393-148">Eine Tabelle muss genau einen primären Index aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ac393-148">A table must have exactly one primary index.</span></span> <span data-ttu-id="ac393-149">Wenn kein primärer Index angegeben ist, wird von der Datenbank-Engine eine transparente Erstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="ac393-149">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-150">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="ac393-150">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="ac393-151">Es wurde eine ungültige Index Definition angegeben.</span><span class="sxs-lookup"><span data-stu-id="ac393-151">An invalid index definition was specified.</span></span> <span data-ttu-id="ac393-152">Im folgenden finden Sie einige der möglichen Gründe für den Empfang dieses Fehlers:</span><span class="sxs-lookup"><span data-stu-id="ac393-152">The following are some of the possible reasons for receiving this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="ac393-153">Ein primärer Index ist bedingt (d. h., das <strong>grbit</strong> -Element der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur verfügt über JET_bitIndexPrimary Menge, und der <strong>cconditionalcolumn</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur ist größer als 0 (null)).</span><span class="sxs-lookup"><span data-stu-id="ac393-153">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="ac393-154">Windows Server 2003 und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="ac393-154">Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="ac393-155">Es wurde versucht, einen Tupelindex mit tupellimits zu erstellen, ohne den <strong>ptuplelimits</strong> -Member in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur zu übergeben (d. h., der <strong>grbit</strong> -Member der JET_INDEXCREATE2 Struktur hat JET_bitIndexTupleLimits festgelegt, der <strong>ptuplelimits</strong> -Zeiger ist jedoch NULL).</span><span class="sxs-lookup"><span data-stu-id="ac393-155">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure (that is, the <strong>grbit</strong> member of the JET_INDEXCREATE2 structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="ac393-156">Übergeben einer ungültigen Schlüssel Definition im <strong>szkey</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ac393-156">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="ac393-157">Eine Erörterung gültiger Definitionen finden Sie unter <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="ac393-157">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="ac393-158">Das Festlegen des <strong>cbvarsegmac</strong> -Members in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> auf größer als JET_cbPrimaryKeyMost (für einen primären Index) oder größer als JET_cbSecondaryKeyMost (für einen sekundären Index).</span><span class="sxs-lookup"><span data-stu-id="ac393-158">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="ac393-159">Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einen, bei dem das JET_bitIndexUnicode Bit im <strong>grbit</strong> -Member von <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="ac393-159">Passing an invalid combination for a user-defined Unicode index (one that has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="ac393-160">Zu den häufigsten Gründen gehören das <strong>pidxunicode</strong> -Element der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur ist NULL, oder die in der <strong>pidxunicode</strong> -Struktur angegebene LCID ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ac393-160">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="ac393-161">Angeben einer mehrwertigen Spalte für einen primären Index.</span><span class="sxs-lookup"><span data-stu-id="ac393-161">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="ac393-162">Es wird versucht, zu viele bedingte Spalten zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="ac393-162">Trying to index too many conditional columns.</span></span> <span data-ttu-id="ac393-163">Der <strong>cconditionalcolumn</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur darf nicht größer als JET_ccolKeyMost sein.</span><span class="sxs-lookup"><span data-stu-id="ac393-163">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-164">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="ac393-164">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="ac393-165">Windows XP und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="ac393-165">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="ac393-166">Es wurde eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur angegeben, und ihre Grenzen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ac393-166">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="ac393-167">Weitere Informationen finden Sie im Abschnitt "Hinweise" der <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur.</span><span class="sxs-lookup"><span data-stu-id="ac393-167">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-168">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="ac393-168">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="ac393-169">Windows XP und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="ac393-169">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="ac393-170">Ein Tupelindex kann nicht eindeutig sein (d. h., der <em>grbit</em> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexUnique festgelegt werden).</span><span class="sxs-lookup"><span data-stu-id="ac393-170">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-171">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="ac393-171">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="ac393-172">Windows XP und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="ac393-172">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="ac393-173">Ein Tupelindex kann nur über eine einzelne Spalte verfügen (d. h., wenn der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur JET_bitIndexTuples festgelegt hat und der <strong>szkey</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur mehr als eine Spalte angibt).</span><span class="sxs-lookup"><span data-stu-id="ac393-173">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-174">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="ac393-174">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="ac393-175">Windows XP und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="ac393-175">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="ac393-176">Bei einem Tupelindex kann es sich nicht um einen primären Index handeln (d. h., der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexTuples festgelegt werden).</span><span class="sxs-lookup"><span data-stu-id="ac393-176">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-177">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="ac393-177">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="ac393-178">Windows XP und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="ac393-178">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="ac393-179">Ein Tupelindex kann nur für eine Text-oder Unicode-Spalte gelten.</span><span class="sxs-lookup"><span data-stu-id="ac393-179">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="ac393-180">Der Versuch, andere Spalten (z. b. binäre Spalten) zu indizieren, führt zu JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="ac393-180">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-181">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="ac393-181">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="ac393-182">Windows XP und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="ac393-182">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="ac393-183">Ein Tupelindex lässt nicht zu, dass der <strong>cbvarsegmac</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ac393-183">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-184">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="ac393-184">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="ac393-185">Es wurde versucht, einen Index ohne Versionsinformationen zu erstellen, während eine Transaktion durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ac393-185">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-186">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="ac393-186">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="ac393-187">Der <strong>CP</strong> -Member der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur wurde nicht auf eine gültige Codepage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac393-187">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="ac393-188">Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="ac393-188">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="ac393-189">Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</span><span class="sxs-lookup"><span data-stu-id="ac393-189">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-190">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="ac393-190">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="ac393-191">Der <strong>colttmember</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur wurde nicht auf einen gültigen Spaltentyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac393-191">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-192">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="ac393-192">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="ac393-193">Im folgenden sind einige Gründe aufgeführt, warum dieser Fehler auftreten kann:</span><span class="sxs-lookup"><span data-stu-id="ac393-193">The following are some reasons why this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="ac393-194">Der <strong>rgindexcreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> Struktur wurde auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac393-194">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="ac393-195">Der <strong>rgcolumncreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> Struktur wurde auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac393-195">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="ac393-196">Der <strong>cbStruct</strong> -Member einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur wurde nicht auf einen gültigen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac393-196">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="ac393-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="ac393-198">In <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>wurde eine ungültige Kombination von <strong>grbit</strong> -Membern angegeben.</span><span class="sxs-lookup"><span data-stu-id="ac393-198">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>.</span></span></p>
<p><span data-ttu-id="ac393-199">Die Index Definition ist ungültig, da der <strong>grbit</strong> -Member inkonsistente Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="ac393-199">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="ac393-200">Folgende Ursachen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="ac393-200">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="ac393-201">Für einen primären Index wurde ein Ignore-Bit angegeben (d. h. JET_bitIndexPrimary mit JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull oder JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="ac393-201">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="ac393-202">Ein leerer Index ignoriert keine NULL-Elemente (d. h., das <strong>grbit</strong> -Element der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur hat JET_bitIndexEmpty festgelegt, aber nicht JET_bitIndexIgnoreAnyNull festgelegt).</span><span class="sxs-lookup"><span data-stu-id="ac393-202">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="ac393-203">Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> -Struktur mit einem ungültigen <strong>grbit</strong> -Member.</span><span class="sxs-lookup"><span data-stu-id="ac393-203">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-204">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="ac393-204">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="ac393-205">Es wurde eine ungültige Gebiets Schema-ID (LCID) übergeben (entweder über den <strong>LCID</strong> -Member der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> -Struktur, auf die durch das <strong>pidxunicode</strong> -Element in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur verwiesen wird, oder über das <strong>LCID</strong> -Feld der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur).</span><span class="sxs-lookup"><span data-stu-id="ac393-205">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure, or through the <strong>lcid</strong> field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-206">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ac393-206">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ac393-207">Ein ungültiger Parameter wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="ac393-207">An invalid parameter was given.</span></span> <span data-ttu-id="ac393-208">Folgende Ursachen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="ac393-208">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="ac393-209">Der <strong>rgcolumncreate</strong> -Member der <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> -Struktur ist NULL.</span><span class="sxs-lookup"><span data-stu-id="ac393-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="ac393-210">Der <strong>cbStruct</strong> -Member einer der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Strukturen, die im <strong>rgcolumncreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> -Struktur angegeben sind, wurde nicht auf sizeof (JET_COLUMNCREATE) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac393-210">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="ac393-211">Der <strong>cbkey</strong> -Member einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur ist auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac393-211">The <strong>cbKey</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="ac393-212">Der <strong>cbStruct</strong> -Member einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur ist nicht auf sizeof (JET_INDEXCREATE2) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ac393-212">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( JET_INDEXCREATE2 ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-213">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="ac393-213">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="ac393-214">Der Datensatz ist zu groß.</span><span class="sxs-lookup"><span data-stu-id="ac393-214">The record is too big.</span></span> <span data-ttu-id="ac393-215">Die Summe des <strong>cbmax</strong> -Members der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur für alle festgelegten Spalten darf einen bestimmten Wert nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="ac393-215">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-216">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="ac393-216">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="ac393-217">Die Tabelle ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ac393-217">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-218">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="ac393-218">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="ac393-219">Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ac393-219">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="ac393-220">Eine Tabelle kann nicht mehr als JET_ccolFixedMost fester Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierte Spalten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ac393-220">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-221">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="ac393-221">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="ac393-222">Fehler beim Versuch, eine Unicode-Spalte zu normalisieren.</span><span class="sxs-lookup"><span data-stu-id="ac393-222">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="ac393-223">Dies kann darauf zurückzuführen sein, dass die Systemressourcen nicht mehr ausreichen.</span><span class="sxs-lookup"><span data-stu-id="ac393-223">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-224">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="ac393-224">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="ac393-225">Ein Element der Jet-Raum Hinweise-Struktur war nicht korrekt oder kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ac393-225">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="ac393-226">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac393-226">Remarks</span></span>

<span data-ttu-id="ac393-227">Der Name **JetCreateTableColumnIndex3** stammt aus der Reihenfolge der Erstellung der Objekte: er erstellt zuerst eine Tabelle, Spalten und schließlich Indizes.</span><span class="sxs-lookup"><span data-stu-id="ac393-227">The name **JetCreateTableColumnIndex3** comes from the order of creation of the objects: It first creates a table, columns, and then finally indexes.</span></span> <span data-ttu-id="ac393-228">**JetCreateTableColumnIndex3** erstellt eine Tabelle mit einem anfänglichen Satz von Spalten und Indizes.</span><span class="sxs-lookup"><span data-stu-id="ac393-228">**JetCreateTableColumnIndex3** creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="ac393-229">Weitere Spalten und Indizes können mit [jetaddcolumn](./jetaddcolumn-function.md), [jetdeletecolumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [jetkreateindex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md)und [jetdeleteindex](./jetdeleteindex-function.md)dynamisch hinzugefügt und entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="ac393-229">Additional columns and indexes can be added and removed dynamically with [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md).</span></span>

<span data-ttu-id="ac393-230">Wie [jetopentable](./jetopentable-function.md), wenn die Anwendung mit der zurückgegebenen *TableID* ausgeführt wird, sollte Sie in der Regel mit [jetclosetable](./jetclosetable-function.md)geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ac393-230">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned *tableid*, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="ac393-231">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac393-231">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac393-232"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ac393-232"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ac393-233">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ac393-233">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-234"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ac393-234"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ac393-235">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ac393-235">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-236"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ac393-236"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ac393-237">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="ac393-237">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-238"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="ac393-238"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ac393-239">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ac393-239">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac393-240"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ac393-240"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ac393-241">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ac393-241">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac393-242"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ac393-242"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ac393-243">Implementiert als <strong>JetCreateTableColumnIndex3W</strong> (Unicode) und <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ac393-243">Implemented as <strong>JetCreateTableColumnIndex3W</strong> (Unicode) and <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ac393-244">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ac393-244">See Also</span></span>

[<span data-ttu-id="ac393-245">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="ac393-245">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="ac393-246">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="ac393-246">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="ac393-247">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ac393-247">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ac393-248">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ac393-248">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ac393-249">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="ac393-249">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="ac393-250">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="ac393-250">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="ac393-251">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ac393-251">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ac393-252">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ac393-252">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ac393-253">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="ac393-253">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="ac393-254">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="ac393-254">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)  
[<span data-ttu-id="ac393-255">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="ac393-255">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="ac393-256">Jetaddcolumn</span><span class="sxs-lookup"><span data-stu-id="ac393-256">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="ac393-257">Jetkreateingedex</span><span class="sxs-lookup"><span data-stu-id="ac393-257">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="ac393-258">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="ac393-258">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="ac393-259">JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="ac393-259">JetCreateIndex3</span></span>](./jetcreateindex3-function.md)  
[<span data-ttu-id="ac393-260">Jetkreatetable</span><span class="sxs-lookup"><span data-stu-id="ac393-260">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="ac393-261">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="ac393-261">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="ac393-262">Jetdeletecolumn</span><span class="sxs-lookup"><span data-stu-id="ac393-262">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="ac393-263">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="ac393-263">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
