---
description: 'Weitere Informationen finden Sie hier: JetCreateIndex2-Funktion'
title: JetCreateIndex2-Funktion
TOCTitle: JetCreateIndex2 Function
ms:assetid: 8810eaed-40cb-4561-aafc-9a9bbdb0d05b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269324(v=EXCHG.10)
ms:contentKeyID: 32765614
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex2W
- JetCreateIndex2A
- JetCreateIndex2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42c1eb8fa1bb7fa880cf7286a1ec472ddc7ba7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373201"
---
# <a name="jetcreateindex2-function"></a><span data-ttu-id="8ddad-103">JetCreateIndex2-Funktion</span><span class="sxs-lookup"><span data-stu-id="8ddad-103">JetCreateIndex2 Function</span></span>


<span data-ttu-id="8ddad-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8ddad-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex2-function"></a><span data-ttu-id="8ddad-105">JetCreateIndex2-Funktion</span><span class="sxs-lookup"><span data-stu-id="8ddad-105">JetCreateIndex2 Function</span></span>

<span data-ttu-id="8ddad-106">Die **JetCreateIndex2** -Funktion erstellt Indizes für Daten in einer ESE-Datenbank, die zum schnellen Auffinden spezifischer Daten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8ddad-106">The **JetCreateIndex2** function creates indexes over data in an ESE database, which can be used to locate specific data quickly.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a><span data-ttu-id="8ddad-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ddad-107">Parameters</span></span>

<span data-ttu-id="8ddad-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="8ddad-108">*sesid*</span></span>

<span data-ttu-id="8ddad-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="8ddad-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="8ddad-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="8ddad-110">*tableid*</span></span>

<span data-ttu-id="8ddad-111">Die Tabelle, für die der Index erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8ddad-111">The table on which the index will be created.</span></span>

<span data-ttu-id="8ddad-112">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="8ddad-112">*pindexcreate*</span></span>

<span data-ttu-id="8ddad-113">Ein Array von [JET_INDEXCREATE](./jet-indexcreate-structure.md) -Strukturen, von denen jede einen zu erstellenden Index definiert.</span><span class="sxs-lookup"><span data-stu-id="8ddad-113">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="8ddad-114">*cindexcreate*</span><span class="sxs-lookup"><span data-stu-id="8ddad-114">*cIndexCreate*</span></span>

<span data-ttu-id="8ddad-115">Die Anzahl der Elemente im *pindexcreate* -Array.</span><span class="sxs-lookup"><span data-stu-id="8ddad-115">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="8ddad-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ddad-116">Return Value</span></span>

<span data-ttu-id="8ddad-117">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="8ddad-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8ddad-118">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8ddad-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ddad-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8ddad-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="8ddad-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ddad-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ddad-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8ddad-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8ddad-122">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8ddad-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddad-123">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="8ddad-123">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="8ddad-124">Es wurde versucht, über eine Spalte vom Typ "Escrow-Update" oder "SLV" zu indizieren (Beachten Sie, dass SLV-Spalten veraltet sind).</span><span class="sxs-lookup"><span data-stu-id="8ddad-124">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddad-125">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="8ddad-125">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="8ddad-126">Es wurde versucht, eine nicht vorhandene Spalte zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="8ddad-126">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="8ddad-127">Der Versuch, bedingt eine Indizierung über eine nicht vorhandene Spalte durchführen zu können, kann ebenfalls diesen Fehler verursachen.</span><span class="sxs-lookup"><span data-stu-id="8ddad-127">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddad-128">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="8ddad-128">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="8ddad-129">Dieser Fehler wird zurückgegeben, wenn der <strong>uldensity</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur auf eine Zahl kleiner als 20 oder mehr als 100 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8ddad-129">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddad-130">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="8ddad-130">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="8ddad-131">Es wurde versucht, zwei identische Indizes zu definieren.</span><span class="sxs-lookup"><span data-stu-id="8ddad-131">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddad-132">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="8ddad-132">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="8ddad-133">Es wurde versucht, mehr als einen primären Index für eine Tabelle anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8ddad-133">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="8ddad-134">Eine Tabelle muss genau einen primären Index aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8ddad-134">A table must have exactly one primary index.</span></span> <span data-ttu-id="8ddad-135">Wenn kein primärer Index angegeben ist, wird von der Datenbank-Engine eine transparente Erstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="8ddad-135">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddad-136">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="8ddad-136">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="8ddad-137">Es wurde eine ungültige Index Definition angegeben.</span><span class="sxs-lookup"><span data-stu-id="8ddad-137">An invalid index definition was specified.</span></span> <span data-ttu-id="8ddad-138">Mögliche Ursachen für den Empfang dieses Fehlers:</span><span class="sxs-lookup"><span data-stu-id="8ddad-138">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="8ddad-139">Ein primärer Index ist bedingt (<strong>grbit</strong> -Member von <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> JET_bitIndexPrimary festgelegt haben, und der <strong>cconditionalcolumn</strong> -Member von <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ist größer als 0 (null)).</span><span class="sxs-lookup"><span data-stu-id="8ddad-139">A primary index is conditional (<strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> has JET_bitIndexPrimary set, and the <strong>cConditionalColumn</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="8ddad-140">Windows Server 2003 und höher.</span><span class="sxs-lookup"><span data-stu-id="8ddad-140">Windows Server 2003 and later.</span></span> <span data-ttu-id="8ddad-141">Es wurde versucht, einen Tupelindex mit tupellimits zu erstellen, aber ohne Informationen im <strong>ptuplelimits</strong> -Member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> zu übergeben (das heißt, dass <em>grbit</em> JET_bitIndexTupleLimits festgelegt ist, der <strong>ptuplelimits</strong> -Zeiger aber NULL ist).</span><span class="sxs-lookup"><span data-stu-id="8ddad-141">Attempting to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (that is, <em>grbit</em> has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="8ddad-142">Übergeben einer ungültigen Schlüssel Definition im <strong>szkey</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8ddad-142">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="8ddad-143">Eine Erörterung gültiger Definitionen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="8ddad-143">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="8ddad-144">Das Festlegen des <strong>cbvarsegmac</strong> -Members in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> auf größer als JET_cbPrimaryKeyMost (für einen primären Index) oder größer als JET_cbSecondaryKeyMost (für einen sekundären Index).</span><span class="sxs-lookup"><span data-stu-id="8ddad-144">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="8ddad-145">Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einen, bei dem das JET_bitIndexUnicode Bit im <strong>grbit</strong> -Member von <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="8ddad-145">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="8ddad-146">Einige häufige Gründe können sein, dass das pidxunicode-Feld der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur NULL ist oder die in der pidxunicode-Struktur angegebene LCID ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="8ddad-146">Some common causes may be that the pidxunicode field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="8ddad-147">Angeben einer mehrwertigen Spalte für einen primären Index.</span><span class="sxs-lookup"><span data-stu-id="8ddad-147">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="8ddad-148">Es wird versucht, zu viele bedingte Spalten zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="8ddad-148">Trying to index too many conditional columns.</span></span> <span data-ttu-id="8ddad-149">Der <strong>cconditionalcolumn</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur darf nicht größer als JET_ccolKeyMost sein.</span><span class="sxs-lookup"><span data-stu-id="8ddad-149">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddad-150">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="8ddad-150">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="8ddad-151">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="8ddad-151">Windows XP and later.</span></span> <span data-ttu-id="8ddad-152">Es wurde eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur angegeben, und ihre Grenzen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ddad-152">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="8ddad-153">Weitere Informationen finden Sie im Abschnitt "Hinweise" der <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur.</span><span class="sxs-lookup"><span data-stu-id="8ddad-153">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddad-154">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="8ddad-154">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="8ddad-155">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="8ddad-155">Windows XP and later.</span></span> <span data-ttu-id="8ddad-156">Ein Tupelindex kann nicht eindeutig sein (für<em>grbit</em> dürfen nicht sowohl JET_bitIndexTuples als auch JET_bitIndexUnique festgelegt sein).</span><span class="sxs-lookup"><span data-stu-id="8ddad-156">A tuple index cannot be unique (<em>grbit</em> must not have both JET_bitIndexTuples and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddad-157">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="8ddad-157">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="8ddad-158">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="8ddad-158">Windows XP and later.</span></span> <span data-ttu-id="8ddad-159">Ein Tupelindex kann nur über eine einzelne Spalte verfügen (d. h., der <strong>grbit</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur verfügt über JET_bitIndexTuples Menge, und der <strong>szkey</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur gibt mehr als eine Spalte an).</span><span class="sxs-lookup"><span data-stu-id="8ddad-159">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddad-160">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="8ddad-160">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="8ddad-161">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="8ddad-161">Windows XP and later.</span></span> <span data-ttu-id="8ddad-162">Bei einem Tupelindex kann es sich nicht um einen primären Index handeln (d. h., der <strong>grbit</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexTuples festgelegt werden).</span><span class="sxs-lookup"><span data-stu-id="8ddad-162">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddad-163">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="8ddad-163">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="8ddad-164">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="8ddad-164">Windows XP and later.</span></span> <span data-ttu-id="8ddad-165">Ein Tupelindex kann nur für eine Text-oder Unicode-Spalte gelten.</span><span class="sxs-lookup"><span data-stu-id="8ddad-165">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="8ddad-166">Der Versuch, andere Spalten zu indizieren (z. b. binäre Spalten), führt zu JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="8ddad-166">An attempt to index other columns (for example, binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddad-167">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="8ddad-167">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="8ddad-168">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="8ddad-168">Windows XP and later.</span></span> <span data-ttu-id="8ddad-169">Ein Tupelindex lässt nicht zu, dass der <strong>cbvarsegmac</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8ddad-169">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddad-170">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="8ddad-170">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="8ddad-171">Es wurde versucht, einen Index ohne Versionsinformationen zu erstellen, während eine Transaktion durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8ddad-171">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddad-172">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="8ddad-172">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="8ddad-173">Die Index Definition ist ungültig, da der <strong>grbit</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur inkonsistente Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="8ddad-173">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure contains inconsistent values.</span></span> <span data-ttu-id="8ddad-174">Mögliche Ursachen:</span><span class="sxs-lookup"><span data-stu-id="8ddad-174">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="8ddad-175">Für einen primären Index wurde ein Ignore-Bit angegeben (JET_bitIndexPrimary mit einem JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull oder JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="8ddad-175">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="8ddad-176">Ein leerer Index ignoriert keine NULL-Felder (d. h., das <strong>grbit</strong> -Element der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur hat JET_bitIndexEmpty festgelegt, aber nicht JET_bitIndexIgnoreAnyNull festgelegt).</span><span class="sxs-lookup"><span data-stu-id="8ddad-176">An empty index does not ignore any NULL fields (that is, <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="8ddad-177">Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> -Struktur mit einem ungültigen <strong>grbit</strong> -Member.</span><span class="sxs-lookup"><span data-stu-id="8ddad-177">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="8ddad-178">Siehe <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="8ddad-178">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="8ddad-179">Wenn mehrere Indizes gleichzeitig erstellt werden (d. h., wenn der <em>cindexcreate</em> -Parameter größer als 1 ist), kann keiner der Indizes einen der folgenden Bits enthalten:</span><span class="sxs-lookup"><span data-stu-id="8ddad-179">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="8ddad-180">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="8ddad-180">JET_bitIndexPrimary</span></span></p></li>
<li><p><span data-ttu-id="8ddad-181">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="8ddad-181">JET_bitIndexUnversioned</span></span></p></li>
<li><p><span data-ttu-id="8ddad-182">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="8ddad-182">JET_bitIndexEmpty</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddad-183">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="8ddad-183">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="8ddad-184">Es wurde eine ungültige Gebiets Schema-ID (LCID) übergeben (entweder über den <strong>LCID</strong> -Member in der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> -Struktur, in der das <strong>pidxunicode</strong> -Element in der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur einen Zeiger auf enthält, oder über den <strong>LCID</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur).</span><span class="sxs-lookup"><span data-stu-id="8ddad-184">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddad-185">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="8ddad-185">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="8ddad-186">Es wurde ein ungültiger Indexname angegeben.</span><span class="sxs-lookup"><span data-stu-id="8ddad-186">An invalid index name was specified.</span></span> <span data-ttu-id="8ddad-187">Weitere Informationen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="8ddad-187">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddad-188">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="8ddad-188">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="8ddad-189">Ein ungültiger Parameter wurde an die API übergeben.</span><span class="sxs-lookup"><span data-stu-id="8ddad-189">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="8ddad-190">Dieser Fehler kann aus folgenden Gründen zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="8ddad-190">Some of the reasons this error may be returned are:</span></span></p>
<ul>
<li><p><span data-ttu-id="8ddad-191">Das <strong>cbkey</strong> -Feld einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur ist auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8ddad-191">The <strong>cbKey</strong> field of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="8ddad-192">Der <strong>cbStruct</strong> -Member einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur ist nicht auf sizeof (<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8ddad-192">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof(<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddad-193">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="8ddad-193">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="8ddad-194">Fehler beim Versuch, eine Unicode-Spalte zu normalisieren.</span><span class="sxs-lookup"><span data-stu-id="8ddad-194">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="8ddad-195">Dies kann darauf zurückzuführen sein, dass die Systemressourcen nicht mehr ausreichen.</span><span class="sxs-lookup"><span data-stu-id="8ddad-195">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="8ddad-196">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ddad-196">Remarks</span></span>

<span data-ttu-id="8ddad-197">Der Rückgabewert wird nach erfolgreichem Abschluss aller angegebenen Indizes JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="8ddad-197">The return value is JET_errSuccess on successful completion of all indexes specified.</span></span>

<span data-ttu-id="8ddad-198">**JetCreateIndex2** durchläuft die in **pindexcreate** angegebenen Indizes und bricht bei dem ersten Fehler manchmal ab.</span><span class="sxs-lookup"><span data-stu-id="8ddad-198">**JetCreateIndex2** iterates through the indexes given in **pindexcreate**, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="8ddad-199">Möglicherweise wurden keine Indizes nach dem ersten Index mit einem Fehler versucht, obwohl der **Err** -Member der [JET_INDEXCREATE](./jet-indexcreate-structure.md) Struktur JET_errSuccess enthält.</span><span class="sxs-lookup"><span data-stu-id="8ddad-199">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8ddad-200">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ddad-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ddad-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8ddad-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddad-202">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8ddad-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddad-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8ddad-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddad-204">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8ddad-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddad-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8ddad-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddad-206">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="8ddad-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddad-207"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="8ddad-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddad-208">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8ddad-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ddad-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8ddad-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddad-210">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8ddad-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ddad-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="8ddad-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8ddad-212">Implementiert als <strong>JetCreateIndex2W</strong> (Unicode) und <strong>JetCreateIndex2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="8ddad-212">Implemented as <strong>JetCreateIndex2W</strong> (Unicode) and <strong>JetCreateIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8ddad-213">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8ddad-213">See Also</span></span>

[<span data-ttu-id="8ddad-214">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="8ddad-214">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="8ddad-215">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8ddad-215">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8ddad-216">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8ddad-216">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="8ddad-217">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8ddad-217">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8ddad-218">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8ddad-218">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8ddad-219">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="8ddad-219">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="8ddad-220">Jetkreateingedex</span><span class="sxs-lookup"><span data-stu-id="8ddad-220">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="8ddad-221">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="8ddad-221">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="8ddad-222">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="8ddad-222">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
