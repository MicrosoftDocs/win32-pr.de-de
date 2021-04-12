---
description: 'Weitere Informationen finden Sie hier: JetCreateIndex3-Funktion'
title: JetCreateIndex3-Funktion
TOCTitle: JetCreateIndex3 Function
ms:assetid: bc9b940e-65c6-49d6-ad32-74434527d29f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294075(v=EXCHG.10)
ms:contentKeyID: 32765690
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex3A
- JetCreateIndex3
- JetCreateIndex3W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4f3331a903d4885499ff6c2cd2cad0d8b8534a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346968"
---
# <a name="jetcreateindex3-function"></a><span data-ttu-id="be543-103">JetCreateIndex3-Funktion</span><span class="sxs-lookup"><span data-stu-id="be543-103">JetCreateIndex3 Function</span></span>


<span data-ttu-id="be543-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="be543-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex3-function"></a><span data-ttu-id="be543-105">JetCreateIndex3-Funktion</span><span class="sxs-lookup"><span data-stu-id="be543-105">JetCreateIndex3 Function</span></span>

<span data-ttu-id="be543-106">Die **JetCreateIndex3** -Funktion erstellt Indizes für Daten in einer ESE-Datenbank, die zum schnellen Auffinden spezifischer Daten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="be543-106">The **JetCreateIndex3** function creates indexes over data in an ESE database, which can be used to locate specific data quickly.</span></span>

<span data-ttu-id="be543-107">**Windows 7: JetCreateIndex3** wird im Betriebssystem Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="be543-107">**Windows 7:  JetCreateIndex3** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE2* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a><span data-ttu-id="be543-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="be543-108">Parameters</span></span>

<span data-ttu-id="be543-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="be543-109">*sesid*</span></span>

<span data-ttu-id="be543-110">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="be543-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="be543-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="be543-111">*tableid*</span></span>

<span data-ttu-id="be543-112">Die Tabelle, für die der Index erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="be543-112">The table on which the index will be created.</span></span>

<span data-ttu-id="be543-113">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="be543-113">*pindexcreate*</span></span>

<span data-ttu-id="be543-114">Ein Array von [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) -Strukturen, von denen jede einen zu erstellenden Index definiert.</span><span class="sxs-lookup"><span data-stu-id="be543-114">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="be543-115">*cindexcreate*</span><span class="sxs-lookup"><span data-stu-id="be543-115">*cIndexCreate*</span></span>

<span data-ttu-id="be543-116">Die Anzahl der Elemente im *pindexcreate* -Array.</span><span class="sxs-lookup"><span data-stu-id="be543-116">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="be543-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be543-117">Return Value</span></span>

<span data-ttu-id="be543-118">Diese Funktion gibt den [JET_ERR](./jet-err.md) -Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="be543-118">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="be543-119">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="be543-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be543-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="be543-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="be543-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be543-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be543-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="be543-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="be543-123">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="be543-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be543-124">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="be543-124">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="be543-125">Es wurde versucht, über eine Spalte vom Typ "Escrow-Update" oder "SLV" zu indizieren (Beachten Sie, dass SLV-Spalten veraltet sind).</span><span class="sxs-lookup"><span data-stu-id="be543-125">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be543-126">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="be543-126">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="be543-127">Es wurde versucht, eine nicht vorhandene Spalte zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="be543-127">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="be543-128">Der Versuch, bedingt eine Indizierung über eine nicht vorhandene Spalte durchführen zu können, kann ebenfalls diesen Fehler verursachen.</span><span class="sxs-lookup"><span data-stu-id="be543-128">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be543-129">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="be543-129">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="be543-130">Dieser Fehler wird zurückgegeben, wenn der <strong>uldensity</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur auf eine Zahl kleiner als 20 oder größer als 100 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="be543-130">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or greater than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be543-131">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="be543-131">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="be543-132">Es wurde versucht, zwei identische Indizes zu definieren.</span><span class="sxs-lookup"><span data-stu-id="be543-132">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be543-133">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="be543-133">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="be543-134">Es wurde versucht, mehr als einen primären Index für eine Tabelle anzugeben.</span><span class="sxs-lookup"><span data-stu-id="be543-134">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="be543-135">Eine Tabelle muss genau einen primären Index aufweisen.</span><span class="sxs-lookup"><span data-stu-id="be543-135">A table must have exactly one primary index.</span></span> <span data-ttu-id="be543-136">Wenn kein primärer Index angegeben ist, wird von der Datenbank-Engine eine transparente Erstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="be543-136">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be543-137">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="be543-137">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="be543-138">Es wurde eine ungültige Index Definition angegeben.</span><span class="sxs-lookup"><span data-stu-id="be543-138">An invalid index definition was specified.</span></span> <span data-ttu-id="be543-139">Im folgenden finden Sie einige mögliche Gründe für den Empfang dieses Fehlers:</span><span class="sxs-lookup"><span data-stu-id="be543-139">The following are some possible reasons for receiving this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="be543-140">Ein primärer Index ist bedingt (<strong>grbit</strong> -Member von <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> JET_bitIndexPrimary festgelegt haben, und der <strong>cconditionalcolumn</strong> -Member von <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ist größer als 0 (null)).</span><span class="sxs-lookup"><span data-stu-id="be543-140">A primary index is conditional (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has JET_bitIndexPrimary set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="be543-141">Windows Server 2003 und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="be543-141">Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="be543-142">Es wurde versucht, einen Tupelindex mit tupellimits zu erstellen, aber ohne Informationen im <strong>ptuplelimits</strong> -Member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> zu übergeben (das heißt, dass <em>grbit</em> JET_bitIndexTupleLimits festgelegt ist, der <strong>ptuplelimits</strong> -Zeiger aber NULL ist).</span><span class="sxs-lookup"><span data-stu-id="be543-142">Attempting to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (that is, <em>grbit</em> has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="be543-143">Übergeben einer ungültigen Schlüssel Definition im <strong>szkey</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="be543-143">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="be543-144">Eine Erörterung gültiger Definitionen finden Sie unter <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="be543-144">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="be543-145">Das Festlegen des <strong>cbvarsegmac</strong> -Members in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> auf größer als JET_cbPrimaryKeyMost (für einen primären Index) oder größer als JET_cbSecondaryKeyMost (für einen sekundären Index).</span><span class="sxs-lookup"><span data-stu-id="be543-145">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="be543-146">Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einen, bei dem das JET_bitIndexUnicode Bit im <strong>grbit</strong> -Member von <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="be543-146">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="be543-147">Einige häufige Gründe können sein, dass das pidxunicode-Feld der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur NULL ist oder die in der pidxunicode-Struktur angegebene LCID ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="be543-147">Some common causes may be that the pidxunicode field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is NULL, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="be543-148">Angeben einer mehrwertigen Spalte für einen primären Index.</span><span class="sxs-lookup"><span data-stu-id="be543-148">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="be543-149">Es wird versucht, zu viele bedingte Spalten zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="be543-149">Trying to index too many conditional columns.</span></span> <span data-ttu-id="be543-150">Der <strong>cconditionalcolumn</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur darf nicht größer als JET_ccolKeyMost sein.</span><span class="sxs-lookup"><span data-stu-id="be543-150">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be543-151">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="be543-151">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="be543-152">Windows XP und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="be543-152">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="be543-153">Es wurde eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur angegeben, und ihre Grenzen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="be543-153">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="be543-154">Weitere Informationen finden Sie im Abschnitt "Hinweise" der <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur.</span><span class="sxs-lookup"><span data-stu-id="be543-154">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be543-155">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="be543-155">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="be543-156">Windows XP und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="be543-156">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="be543-157">Ein Tupelindex kann nicht eindeutig sein (für<em>grbit</em> dürfen nicht sowohl JET_bitIndexTuples als auch JET_bitIndexUnique festgelegt sein).</span><span class="sxs-lookup"><span data-stu-id="be543-157">A tuple index cannot be unique (<em>grbit</em> must not have both JET_bitIndexTuples and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be543-158">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="be543-158">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="be543-159">Windows XP und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="be543-159">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="be543-160">Ein Tupelindex kann nur über eine einzelne Spalte verfügen (d. h., der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur verfügt über JET_bitIndexTuples Menge, und der <strong>szkey</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur gibt mehr als eine Spalte an).</span><span class="sxs-lookup"><span data-stu-id="be543-160">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be543-161">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="be543-161">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="be543-162">Windows XP und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="be543-162">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="be543-163">Bei einem Tupelindex kann es sich nicht um einen primären Index handeln (d. h., der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexTuples festgelegt werden).</span><span class="sxs-lookup"><span data-stu-id="be543-163">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be543-164">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="be543-164">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="be543-165">Windows XP und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="be543-165">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="be543-166">Ein Tupelindex kann nur für eine Text-oder Unicode-Spalte gelten.</span><span class="sxs-lookup"><span data-stu-id="be543-166">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="be543-167">Der Versuch, andere Spalten zu indizieren (z. b. binäre Spalten), führt zu JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="be543-167">An attempt to index other columns (for example, binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be543-168">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="be543-168">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="be543-169">Windows XP und höhere Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="be543-169">Windows XP and later versions of Windows.</span></span> <span data-ttu-id="be543-170">Ein Tupelindex lässt nicht zu, dass der <strong>cbvarsegmac</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="be543-170">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be543-171">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="be543-171">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="be543-172">Es wurde versucht, einen Index ohne Versionsinformationen zu erstellen, während eine Transaktion durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="be543-172">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be543-173">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="be543-173">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="be543-174">Die Index Definition ist ungültig, da der <strong>grbit</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur inkonsistente Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="be543-174">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains inconsistent values.</span></span> <span data-ttu-id="be543-175">Folgende Ursachen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="be543-175">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="be543-176">Für einen primären Index wurde ein Ignore-Bit angegeben (JET_bitIndexPrimary mit einem JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull oder JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="be543-176">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="be543-177">Ein leerer Index ignoriert keine NULL-Felder (d. h., das <strong>grbit</strong> -Element der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur hat JET_bitIndexEmpty festgelegt, aber nicht JET_bitIndexIgnoreAnyNull festgelegt).</span><span class="sxs-lookup"><span data-stu-id="be543-177">An empty index does not ignore any NULL fields (that is, <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="be543-178">Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> -Struktur mit einem ungültigen <strong>grbit</strong> -Member.</span><span class="sxs-lookup"><span data-stu-id="be543-178">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="be543-179">Siehe <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span><span class="sxs-lookup"><span data-stu-id="be543-179">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="be543-180">Wenn mehrere Indizes gleichzeitig erstellt werden (d. h., wenn der <em>cindexcreate</em> -Parameter größer als 1 ist), kann keiner der Indizes einen der folgenden Bits enthalten:</span><span class="sxs-lookup"><span data-stu-id="be543-180">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="be543-181">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="be543-181">JET_bitIndexPrimary</span></span></p></li>
<li><p><span data-ttu-id="be543-182">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="be543-182">JET_bitIndexUnversioned</span></span></p></li>
<li><p><span data-ttu-id="be543-183">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="be543-183">JET_bitIndexEmpty</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be543-184">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="be543-184">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="be543-185">Es wurde eine ungültige Gebiets Schema-ID (LCID) übergeben (entweder über den <strong>LCID</strong> -Member in der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> -Struktur, in der das <strong>pidxunicode</strong> -Element in der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur einen Zeiger auf enthält, oder über den <strong>LCID</strong> -Member der <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur).</span><span class="sxs-lookup"><span data-stu-id="be543-185">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be543-186">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="be543-186">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="be543-187">Es wurde ein ungültiger Indexname angegeben.</span><span class="sxs-lookup"><span data-stu-id="be543-187">An invalid index name was specified.</span></span> <span data-ttu-id="be543-188">Weitere Informationen finden Sie unter <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="be543-188">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be543-189">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="be543-189">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="be543-190">Ein ungültiger Parameter wurde an die API übergeben.</span><span class="sxs-lookup"><span data-stu-id="be543-190">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="be543-191">Im folgenden sind einige Gründe aufgeführt, warum dieser Fehler zurückgegeben werden kann:</span><span class="sxs-lookup"><span data-stu-id="be543-191">The following are some reasons why this error may be returned:</span></span></p>
<ul>
<li><p><span data-ttu-id="be543-192">Das <strong>cbkey</strong> -Feld einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> -Struktur ist auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="be543-192">The <strong>cbKey</strong> field of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="be543-193">Der <strong>cbStruct</strong> -Member einer <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> Struktur ist nicht auf sizeof ( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="be543-193">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be543-194">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="be543-194">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="be543-195">Fehler beim Versuch, eine Unicode-Spalte zu normalisieren.</span><span class="sxs-lookup"><span data-stu-id="be543-195">An error occurred while trying to normalize a Unicode column.</span></span> <span data-ttu-id="be543-196">Dies kann darauf zurückzuführen sein, dass die Systemressourcen nicht mehr ausreichen.</span><span class="sxs-lookup"><span data-stu-id="be543-196">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be543-197">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="be543-197">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="be543-198">Ein Element der Jet-Raum Hinweise-Struktur war nicht korrekt oder kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="be543-198">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="be543-199">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be543-199">Remarks</span></span>

<span data-ttu-id="be543-200">Der Rückgabewert wird nach erfolgreichem Abschluss aller angegebenen Indizes JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="be543-200">The return value is JET_errSuccess on successful completion of all indexes specified.</span></span>

<span data-ttu-id="be543-201">**JetCreateIndex3** durchläuft die in **pindexcreate** angegebenen Indizes und bricht bei dem ersten Fehler manchmal ab.</span><span class="sxs-lookup"><span data-stu-id="be543-201">**JetCreateIndex3** iterates through the indexes given in **pindexcreate**, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="be543-202">Möglicherweise wurden keine Indizes nach dem ersten Index mit einem Fehler versucht, obwohl der **Err** -Member der [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) Struktur JET_errSuccess enthält.</span><span class="sxs-lookup"><span data-stu-id="be543-202">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="be543-203">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be543-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be543-204"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="be543-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="be543-205">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="be543-205">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be543-206"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="be543-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="be543-207">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="be543-207">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be543-208"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="be543-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="be543-209">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="be543-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be543-210"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="be543-210"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="be543-211">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="be543-211">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be543-212"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="be543-212"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="be543-213">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="be543-213">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be543-214"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="be543-214"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="be543-215">Implementiert als <strong>JetCreateIndex3W</strong> (Unicode) und <strong>JetCreateIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="be543-215">Implemented as <strong>JetCreateIndex3W</strong> (Unicode) and <strong>JetCreateIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="be543-216">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="be543-216">See Also</span></span>

[<span data-ttu-id="be543-217">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="be543-217">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="be543-218">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="be543-218">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="be543-219">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="be543-219">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="be543-220">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="be543-220">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="be543-221">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="be543-221">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="be543-222">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="be543-222">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="be543-223">Jetkreateingedex</span><span class="sxs-lookup"><span data-stu-id="be543-223">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="be543-224">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="be543-224">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="be543-225">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="be543-225">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="be543-226">JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="be543-226">JET_SPACEHINTS</span></span>](./jet-spacehints-structure.md)
