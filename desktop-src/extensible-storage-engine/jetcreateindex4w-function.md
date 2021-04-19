---
description: 'Weitere Informationen finden Sie hier: JetCreateIndex4W-Funktion'
title: JetCreateIndex4W-Funktion
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a4c7671cbe361b6214552f4c611cd1706c0e48d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363268"
---
# <a name="jetcreateindex4w-function"></a><span data-ttu-id="18eaa-103">JetCreateIndex4W-Funktion</span><span class="sxs-lookup"><span data-stu-id="18eaa-103">JetCreateIndex4W Function</span></span>


<span data-ttu-id="18eaa-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="18eaa-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="18eaa-105">Die **JetCreateIndex4W** -Funktion erstellt Indizes für Daten in einer ESE-Datenbank (Extensible Storage Engine), die zum schnellen Auffinden spezifischer Daten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="18eaa-105">The **JetCreateIndex4W** function creates indexes over data in an Extensible Storage Engine (ESE) database, which can be used to locate specific data quickly.</span></span>

<span data-ttu-id="18eaa-106">Die **JetCreateIndex4W** -Funktion wurde im Windows 8-Betriebssystem eingeführt.</span><span class="sxs-lookup"><span data-stu-id="18eaa-106">The **JetCreateIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a><span data-ttu-id="18eaa-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="18eaa-107">Parameters</span></span>

<span data-ttu-id="18eaa-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="18eaa-108">*sesid*</span></span>

<span data-ttu-id="18eaa-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="18eaa-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="18eaa-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="18eaa-110">*tableid*</span></span>

<span data-ttu-id="18eaa-111">Die Tabelle, für die der Index erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="18eaa-111">The table on which the index will be created.</span></span>

<span data-ttu-id="18eaa-112">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="18eaa-112">*pindexcreate*</span></span>

<span data-ttu-id="18eaa-113">Ein Array von [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) -Strukturen, von denen jede einen zu erstellenden Index definiert.</span><span class="sxs-lookup"><span data-stu-id="18eaa-113">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="18eaa-114">*cindexcreate*</span><span class="sxs-lookup"><span data-stu-id="18eaa-114">*cIndexCreate*</span></span>

<span data-ttu-id="18eaa-115">Die Anzahl der Elemente im *pindexcreate* -Array.</span><span class="sxs-lookup"><span data-stu-id="18eaa-115">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="18eaa-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18eaa-116">Return value</span></span>

<span data-ttu-id="18eaa-117">Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der in der folgenden Tabelle aufgelisteten Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="18eaa-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="18eaa-118">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="18eaa-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18eaa-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="18eaa-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="18eaa-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18eaa-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18eaa-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="18eaa-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="18eaa-122">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="18eaa-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18eaa-123">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="18eaa-123">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="18eaa-124">Es wurde versucht, über eine Spalte vom Typ "Escrow-Update" oder "SLV" zu indizieren (Beachten Sie, dass SLV-Spalten veraltet sind).</span><span class="sxs-lookup"><span data-stu-id="18eaa-124">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18eaa-125">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="18eaa-125">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="18eaa-126">Es wurde versucht, einen Index für eine nicht vorhandene Spalte zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="18eaa-126">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="18eaa-127">Der Versuch, bedingt eine Indizierung über eine nicht vorhandene Spalte durchführen zu können, kann ebenfalls diesen Fehler verursachen.</span><span class="sxs-lookup"><span data-stu-id="18eaa-127">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18eaa-128">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="18eaa-128">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="18eaa-129">Dieser Fehler wird zurückgegeben, wenn der <strong>uldensity</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur auf eine Zahl kleiner als 20 oder größer als 100 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="18eaa-129">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or greater than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18eaa-130">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="18eaa-130">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="18eaa-131">Es wurde versucht, zwei identische Indizes zu definieren.</span><span class="sxs-lookup"><span data-stu-id="18eaa-131">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18eaa-132">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="18eaa-132">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="18eaa-133">Es wurde versucht, mehr als einen primären Index für eine Tabelle anzugeben.</span><span class="sxs-lookup"><span data-stu-id="18eaa-133">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="18eaa-134">Eine Tabelle muss genau einen primären Index aufweisen.</span><span class="sxs-lookup"><span data-stu-id="18eaa-134">A table must have exactly one primary index.</span></span> <span data-ttu-id="18eaa-135">Wenn kein primärer Index angegeben ist, wird von der Datenbank-Engine eine transparente Erstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="18eaa-135">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18eaa-136">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="18eaa-136">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="18eaa-137">Es wurde eine ungültige Index Definition angegeben.</span><span class="sxs-lookup"><span data-stu-id="18eaa-137">An invalid index definition was specified.</span></span> <span data-ttu-id="18eaa-138">Im folgenden sind einige mögliche Ursachen für diesen Fehler aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="18eaa-138">The following are some possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="18eaa-139">Ein primärer Index ist bedingt (<strong>grbit</strong> -Member von <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> <strong>JET_bitIndexPrimary</strong> festgelegt haben, und der <strong>cconditionalcolumn</strong> -Member von <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ist größer als 0 (null)).</span><span class="sxs-lookup"><span data-stu-id="18eaa-139">A primary index is conditional (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has <strong>JET_bitIndexPrimary</strong> set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="18eaa-140">Gilt für Windows-Versionen ab Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="18eaa-140">Applies to versions of Windows starting with Windows Server 2003.</span></span> <span data-ttu-id="18eaa-141">Es wurde versucht, einen Tupelindex mit tupellimits zu erstellen, aber ohne Informationen im <strong>ptuplelimits</strong> -Member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> zu übergeben (das heißt, dass für <em>grbit</em> <strong>JET_bitIndexTupleLimits</strong> festgelegt ist, der <strong>ptuplelimits</strong> -Zeiger aber NULL ist).</span><span class="sxs-lookup"><span data-stu-id="18eaa-141">An attempt was made to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (that is, <em>grbit</em> has <strong>JET_bitIndexTupleLimits</strong> set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="18eaa-142">Übergeben einer ungültigen Schlüssel Definition im <strong>szkey</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="18eaa-142">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="18eaa-143">Informationen zu gültigen Definitionen finden Sie unter <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span><span class="sxs-lookup"><span data-stu-id="18eaa-143">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="18eaa-144">Das Festlegen des <strong>cbvarsegmac</strong> -Members in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> auf größer als <strong>JET_cbPrimaryKeyMost</strong> (für einen primären Index) oder größer als <strong>JET_cbSecondaryKeyMost</strong> (für einen sekundären Index).</span><span class="sxs-lookup"><span data-stu-id="18eaa-144">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than <strong>JET_cbPrimaryKeyMost</strong> (for a primary index) or greater than <strong>JET_cbSecondaryKeyMost</strong> (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="18eaa-145">Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einen, bei dem das <strong>JET_bitIndexUnicode</strong> Bit im <strong>grbit</strong> -Member von <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="18eaa-145">Passing an invalid combination for a user-defined Unicode index (one which has the <strong>JET_bitIndexUnicode</strong> bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="18eaa-146">Einige häufige Gründe können sein, dass das pidxunicode-Feld der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur NULL ist oder die in der pidxunicode-Struktur angegebene LCID ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="18eaa-146">Some common causes may be that the pidxunicode field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="18eaa-147">Angeben einer mehrwertigen Spalte für einen primären Index.</span><span class="sxs-lookup"><span data-stu-id="18eaa-147">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="18eaa-148">Es wird versucht, zu viele bedingte Spalten zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="18eaa-148">Trying to index too many conditional columns.</span></span> <span data-ttu-id="18eaa-149">Der <strong>cconditionalcolumn</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur darf nicht größer als <strong>JET_ccolKeyMost</strong>sein.</span><span class="sxs-lookup"><span data-stu-id="18eaa-149">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18eaa-150">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="18eaa-150">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="18eaa-151">Gilt für Windows-Versionen ab Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18eaa-151">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="18eaa-152">Es wurde eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur angegeben, und ihre Grenzen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="18eaa-152">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="18eaa-153">Weitere Informationen finden Sie im Abschnitt "Hinweise" in der <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="18eaa-153">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18eaa-154">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="18eaa-154">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="18eaa-155">Gilt für Windows-Versionen ab Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18eaa-155">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="18eaa-156">Ein Tupelindex kann nicht eindeutig sein (für<em>grbit</em> dürfen nicht sowohl <strong>JET_bitIndexTuples</strong> als auch <strong>JET_bitIndexUnique</strong> festgelegt sein).</span><span class="sxs-lookup"><span data-stu-id="18eaa-156">A tuple index cannot be unique (<em>grbit</em> must not have both <strong>JET_bitIndexTuples</strong> and <strong>JET_bitIndexUnique</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18eaa-157">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="18eaa-157">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="18eaa-158">Gilt für Windows-Versionen ab Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18eaa-158">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="18eaa-159">Ein Tupelindex kann nur über eine einzelne Spalte verfügen (d. h., der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur verfügt über <strong>JET_bitIndexTuples</strong> Menge, und der <strong>szkey</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur gibt mehr als eine Spalte an).</span><span class="sxs-lookup"><span data-stu-id="18eaa-159">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexTuples</strong> set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18eaa-160">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="18eaa-160">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="18eaa-161">Gilt für Windows-Versionen ab Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18eaa-161">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="18eaa-162">Bei einem Tupelindex kann es sich nicht um einen primären Index handeln (d. h., der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur darf nicht sowohl <strong>JET_bitIndexPrimary</strong> als auch <strong>JET_bitIndexTuples</strong> festgelegt werden).</span><span class="sxs-lookup"><span data-stu-id="18eaa-162">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both <strong>JET_bitIndexPrimary</strong> and <strong>JET_bitIndexTuples</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18eaa-163">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="18eaa-163">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="18eaa-164">Gilt für Windows-Versionen ab Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18eaa-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="18eaa-165">Ein Tupelindex kann nur für eine Text-oder Unicode-Spalte gelten.</span><span class="sxs-lookup"><span data-stu-id="18eaa-165">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="18eaa-166">Der Versuch, andere Spalten zu indizieren (z. b. binäre Spalten), führt zu <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</span><span class="sxs-lookup"><span data-stu-id="18eaa-166">An attempt to index other columns (for example, binary columns) will result in <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18eaa-167">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="18eaa-167">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="18eaa-168">Gilt für Windows-Versionen ab Windows XP.</span><span class="sxs-lookup"><span data-stu-id="18eaa-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="18eaa-169">Ein Tupelindex lässt nicht zu, dass der <strong>cbvarsegmac</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="18eaa-169">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18eaa-170">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="18eaa-170">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="18eaa-171">Es wurde versucht, einen Index ohne Versionsinformationen zu erstellen, während eine Transaktion durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="18eaa-171">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18eaa-172">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="18eaa-172">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="18eaa-173">Die Index Definition ist ungültig, da der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur inkonsistente Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="18eaa-173">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains inconsistent values.</span></span> <span data-ttu-id="18eaa-174">Folgende Ursachen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="18eaa-174">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="18eaa-175">Für einen primären Index wurde ein Ignore-Bit angegeben (JET_bitIndexPrimary mit einem <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>oder <strong>JET_bitIndexIgnoreFirstNull</strong>).</span><span class="sxs-lookup"><span data-stu-id="18eaa-175">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>, or <strong>JET_bitIndexIgnoreFirstNull</strong>).</span></span></p></li>
<li><p><span data-ttu-id="18eaa-176">Ein leerer Index ignoriert keine NULL-Felder (d. h., das <strong>grbit</strong> -Element der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur hat <strong>JET_bitIndexEmpty</strong> festgelegt, aber nicht <strong>JET_bitIndexIgnoreAnyNull</strong> festgelegt).</span><span class="sxs-lookup"><span data-stu-id="18eaa-176">An empty index does not ignore any null fields (that is, <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexEmpty</strong> set, but does not have <strong>JET_bitIndexIgnoreAnyNull</strong> set).</span></span></p></li>
<li><p><span data-ttu-id="18eaa-177">Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> -Struktur mit einem ungültigen <strong>grbit</strong> -Member.</span><span class="sxs-lookup"><span data-stu-id="18eaa-177">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="18eaa-178">Siehe <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="18eaa-178">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="18eaa-179">Wenn mehrere Indizes gleichzeitig erstellt werden (d. h., wenn der <em>cindexcreate</em> -Parameter größer als 1 ist), kann keiner der Indizes einen der folgenden Bits enthalten:</span><span class="sxs-lookup"><span data-stu-id="18eaa-179">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="18eaa-180"><strong>JET_bitIndexPrimary</strong></span><span class="sxs-lookup"><span data-stu-id="18eaa-180"><strong>JET_bitIndexPrimary</strong></span></span></p></li>
<li><p><span data-ttu-id="18eaa-181"><strong>JET_bitIndexUnversioned</strong></span><span class="sxs-lookup"><span data-stu-id="18eaa-181"><strong>JET_bitIndexUnversioned</strong></span></span></p></li>
<li><p><span data-ttu-id="18eaa-182"><strong>JET_bitIndexEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="18eaa-182"><strong>JET_bitIndexEmpty</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18eaa-183">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="18eaa-183">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="18eaa-184">Es wurde eine ungültige Gebiets Schema-ID (LCID) übergeben (entweder über den <strong>LCID</strong> -Member in der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> -Struktur, in der das <strong>pidxunicode</strong> -Element in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur einen Zeiger auf enthält, oder über den <strong>LCID</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur).</span><span class="sxs-lookup"><span data-stu-id="18eaa-184">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18eaa-185">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="18eaa-185">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="18eaa-186">Es wurde ein ungültiger Indexname angegeben.</span><span class="sxs-lookup"><span data-stu-id="18eaa-186">An invalid index name was specified.</span></span> <span data-ttu-id="18eaa-187">Weitere Informationen finden Sie unter <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="18eaa-187">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18eaa-188">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="18eaa-188">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="18eaa-189">Ein ungültiger Parameter wurde an die API übergeben.</span><span class="sxs-lookup"><span data-stu-id="18eaa-189">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="18eaa-190">Im folgenden sind einige Gründe aufgeführt, warum dieser Fehler zurückgegeben werden kann:</span><span class="sxs-lookup"><span data-stu-id="18eaa-190">The following are some reasons why this error may be returned:</span></span></p>
<ul>
<li><p><span data-ttu-id="18eaa-191">Das <strong>cbkey</strong> -Feld einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur ist auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="18eaa-191">The <strong>cbKey</strong> field of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="18eaa-192">Der <strong>cbStruct</strong> -Member einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur ist nicht auf sizeof (JET_INDEXCREATE2) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="18eaa-192">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof(JET_INDEXCREATE2).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18eaa-193">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="18eaa-193">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="18eaa-194">Fehler beim Versuch, eine Unicode-Spalte zu normalisieren.</span><span class="sxs-lookup"><span data-stu-id="18eaa-194">An error occurred while trying to normalize a Unicode column.</span></span> <span data-ttu-id="18eaa-195">Dies kann darauf zurückzuführen sein, dass die Systemressourcen nicht mehr ausreichen.</span><span class="sxs-lookup"><span data-stu-id="18eaa-195">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18eaa-196">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="18eaa-196">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="18eaa-197">Ein Element der Jet-Raum Hinweise-Struktur war nicht korrekt oder kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="18eaa-197">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="18eaa-198">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18eaa-198">Remarks</span></span>

<span data-ttu-id="18eaa-199">Die **JetCreateIndex4W** -Funktion durchläuft die im *pindexcreate* -Parameter angegebenen Indizes und bricht bei dem ersten Fehler manchmal ab.</span><span class="sxs-lookup"><span data-stu-id="18eaa-199">The **JetCreateIndex4W** function iterates through the indexes given in the *pindexcreate* parameter, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="18eaa-200">Möglicherweise wurden keine Indizes nach dem ersten Index mit einem Fehler versucht, obwohl der **Err** -Member der [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) Struktur JET_errSuccess enthält.</span><span class="sxs-lookup"><span data-stu-id="18eaa-200">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="18eaa-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18eaa-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18eaa-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="18eaa-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="18eaa-203">Erfordert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="18eaa-203">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18eaa-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="18eaa-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="18eaa-205">Erfordert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="18eaa-205">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18eaa-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="18eaa-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="18eaa-207">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="18eaa-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18eaa-208"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="18eaa-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="18eaa-209">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="18eaa-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18eaa-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="18eaa-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="18eaa-211">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="18eaa-211">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="18eaa-212">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18eaa-212">See also</span></span>

[<span data-ttu-id="18eaa-213">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="18eaa-213">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="18eaa-214">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="18eaa-214">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="18eaa-215">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="18eaa-215">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="18eaa-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="18eaa-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="18eaa-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="18eaa-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="18eaa-218">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="18eaa-218">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="18eaa-219">Jetkreateingedex</span><span class="sxs-lookup"><span data-stu-id="18eaa-219">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="18eaa-220">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="18eaa-220">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="18eaa-221">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="18eaa-221">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="18eaa-222">JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="18eaa-222">JET_SPACEHINTS</span></span>](./jet-spacehints-structure.md)
