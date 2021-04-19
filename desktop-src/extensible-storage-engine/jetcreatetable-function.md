---
description: Weitere Informationen finden Sie in der jetkreatetable-Funktion.
title: JetCreateTable-Funktion
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f385cfd668af934bfde2669277db7ed048a1fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352373"
---
# <a name="jetcreatetable-function"></a><span data-ttu-id="4bd94-103">JetCreateTable-Funktion</span><span class="sxs-lookup"><span data-stu-id="4bd94-103">JetCreateTable Function</span></span>


<span data-ttu-id="4bd94-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4bd94-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetable-function"></a><span data-ttu-id="4bd94-105">JetCreateTable-Funktion</span><span class="sxs-lookup"><span data-stu-id="4bd94-105">JetCreateTable Function</span></span>

<span data-ttu-id="4bd94-106">Die **jetkreatetable** -Funktion erstellt eine leere Tabelle in einer ESE-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="4bd94-106">The **JetCreateTable** function creates an empty table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="4bd94-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bd94-107">Parameters</span></span>

<span data-ttu-id="4bd94-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="4bd94-108">*sesid*</span></span>

<span data-ttu-id="4bd94-109">Der zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="4bd94-109">The database session context to use.</span></span>

<span data-ttu-id="4bd94-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="4bd94-110">*dbid*</span></span>

<span data-ttu-id="4bd94-111">Der zu verwendende Daten Bank Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="4bd94-111">The database identifier to use.</span></span>

<span data-ttu-id="4bd94-112">*sztablename*</span><span class="sxs-lookup"><span data-stu-id="4bd94-112">*szTableName*</span></span>

<span data-ttu-id="4bd94-113">Der Name des zu erstellenden Indexes.</span><span class="sxs-lookup"><span data-stu-id="4bd94-113">The name of the index to create.</span></span>

<span data-ttu-id="4bd94-114">Der Name muss gemäß den folgenden Regeln formatiert werden:</span><span class="sxs-lookup"><span data-stu-id="4bd94-114">The name must be formatted according to the following rules:</span></span>

  - <span data-ttu-id="4bd94-115">Ist kleiner als JET_cbNameMost, ohne dass der abschließende NULL-Wert eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="4bd94-115">Be less than JET_cbNameMost, not including the terminating NULL.</span></span>

  - <span data-ttu-id="4bd94-116">Der folgende Zeichensatz besteht aus den folgenden Zeichen: 0 bis 9, a bis z, a bis z und alle anderen Interpunktions Zeichen mit Ausnahme von " \! "</span><span class="sxs-lookup"><span data-stu-id="4bd94-116">Be made of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="4bd94-117">(Ausrufezeichen), "," (Komma), " \[ " (öffnende eckige Klammer) und " \] " (schließende Klammer) – das heißt, die ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c, 0x5d bis 0x7F.</span><span class="sxs-lookup"><span data-stu-id="4bd94-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="4bd94-118">Beginnen Sie nicht mit einem Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="4bd94-118">Not begin with a space.</span></span>

  - <span data-ttu-id="4bd94-119">Besteht aus mindestens einem Zeichen, das kein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="4bd94-119">Be made of at least one non-space character.</span></span>

<span data-ttu-id="4bd94-120">*lpages*</span><span class="sxs-lookup"><span data-stu-id="4bd94-120">*lPages*</span></span>

<span data-ttu-id="4bd94-121">Die anfängliche Anzahl von Datenbankseiten, die für die Tabelle zuzuordnen sind.</span><span class="sxs-lookup"><span data-stu-id="4bd94-121">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="4bd94-122">Wenn eine Zahl größer als 1 angegeben wird, kann die Fragmentierung reduziert werden, wenn viele Zeilen in diese Tabelle eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4bd94-122">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="4bd94-123">*ldensity*</span><span class="sxs-lookup"><span data-stu-id="4bd94-123">*lDensity*</span></span>

<span data-ttu-id="4bd94-124">Die Tabellen Dichte in Prozent.</span><span class="sxs-lookup"><span data-stu-id="4bd94-124">The table density, in percentage points.</span></span> <span data-ttu-id="4bd94-125">Die Zahl muss entweder 0 oder im Bereich von 20 bis 100 sein.</span><span class="sxs-lookup"><span data-stu-id="4bd94-125">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="4bd94-126">Das übergeben von 0 bedeutet, dass der Standardwert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bd94-126">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="4bd94-127">Der Standardwert ist 80.</span><span class="sxs-lookup"><span data-stu-id="4bd94-127">The default is 80.</span></span>

<span data-ttu-id="4bd94-128">*pTableID*</span><span class="sxs-lookup"><span data-stu-id="4bd94-128">*ptableid*</span></span>

<span data-ttu-id="4bd94-129">Bei Erfolg wird der Tabellen Bezeichner in diesem Feld zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4bd94-129">On success, the table identifier is returned in this field.</span></span> <span data-ttu-id="4bd94-130">Der Wert ist nicht definiert, wenn die API keine JET_errSuccess zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-130">The value is undefined if the API does not return JET_errSuccess.</span></span>

### <a name="return-value"></a><span data-ttu-id="4bd94-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4bd94-131">Return Value</span></span>

<span data-ttu-id="4bd94-132">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="4bd94-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4bd94-133">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4bd94-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4bd94-134">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4bd94-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="4bd94-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bd94-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4bd94-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4bd94-137">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4bd94-137">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-138">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="4bd94-138">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="4bd94-139">Die Rückruffunktion konnte nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4bd94-139">The callback function could not be resolved.</span></span> <span data-ttu-id="4bd94-140">Die dll wurde möglicherweise nicht gefunden, oder die Funktion in der dll wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="4bd94-140">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="4bd94-141">Wenn eine ausreichende Protokollierung aktiviert ist, werden im Ereignisprotokoll weitere Details angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-141">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-142">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="4bd94-142">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="4bd94-143">Es wurde versucht, über eine Spalte vom Typ "Escrow-Update" oder "SLV" zu indizieren (Beachten Sie, dass SLV-Spalten veraltet sind).</span><span class="sxs-lookup"><span data-stu-id="4bd94-143">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-144">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="4bd94-144">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="4bd94-145">, Wenn ptablecreate- &gt; grbit JET_bitTableCreateTemplateTable angibt, ptablecreate- &gt; sztemplatetablename jedoch auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4bd94-145">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-146">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="4bd94-146">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="4bd94-147">Eine Spalte ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4bd94-147">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-148">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="4bd94-148">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="4bd94-149">Es wurde versucht, eine nicht vorhandene Spalte zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="4bd94-149">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="4bd94-150">Der Versuch, bedingt eine Indizierung über eine nicht vorhandene Spalte durchführen zu können, kann ebenfalls diesen Fehler verursachen.</span><span class="sxs-lookup"><span data-stu-id="4bd94-150">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-151">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="4bd94-151">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="4bd94-152">Es wurde versucht, eine redundante Spalte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4bd94-152">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="4bd94-153">Es darf nicht mehr als eine AUTOINCREMENT-Spalte und höchstens eine Versions Spalte pro Tabelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4bd94-153">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-154">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="4bd94-154">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="4bd94-155">Im <em>uldensity</em> -Element in der <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> -oder <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> -Struktur wurde eine ungültige Dichte übermittelt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-155">An invalid density was passed in the <em>ulDensity</em> member in the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-156">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="4bd94-156">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="4bd94-157">Gibt an, dass die Tabelle im <strong>sztemplatetablename</strong> -Member der <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> Struktur nicht als Vorlagen Tabelle gekennzeichnet ist (d. h., dass die Tabelle nicht über JET_bitTableCreateTemplateTable festgelegt wurde).</span><span class="sxs-lookup"><span data-stu-id="4bd94-157">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure was not a marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-158">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="4bd94-158">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="4bd94-159">Es wurde versucht, zwei identische Indizes zu definieren.</span><span class="sxs-lookup"><span data-stu-id="4bd94-159">An attempt was made to define two identical indexes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-160">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="4bd94-160">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="4bd94-161">Es wurde versucht, mehr als einen primären Index für eine Tabelle anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4bd94-161">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="4bd94-162">Eine Tabelle muss genau einen primären Index aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4bd94-162">A table must have exactly one primary index.</span></span> <span data-ttu-id="4bd94-163">Wenn kein primärer Index angegeben ist, wird von der Datenbank-Engine eine transparente Erstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-163">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-164">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="4bd94-164">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="4bd94-165">Es wurde eine ungültige Index Definition angegeben.</span><span class="sxs-lookup"><span data-stu-id="4bd94-165">An invalid index definition was specified.</span></span> <span data-ttu-id="4bd94-166">Mögliche Ursachen für den Empfang dieses Fehlers:</span><span class="sxs-lookup"><span data-stu-id="4bd94-166">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="4bd94-167">Ein primärer Index ist bedingt (d. h., das <strong>grbit</strong> -Element der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur verfügt über JET_bitIndexPrimary Menge, und der <strong>cconditionalcolumn</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur ist größer als 0 (null)).</span><span class="sxs-lookup"><span data-stu-id="4bd94-167">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="4bd94-168">Windows Server 2003 und höher.</span><span class="sxs-lookup"><span data-stu-id="4bd94-168">Windows Server 2003 and later.</span></span> <span data-ttu-id="4bd94-169">Es wurde versucht, einen Tupelindex mit tupellimits zu erstellen, ohne den <strong>ptuplelimits</strong> -Member in der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur zu übergeben (d. h., der <strong>grbit</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur hat JET_bitIndexTupleLimits festgelegt, der <strong>ptuplelimits</strong> -Zeiger ist jedoch NULL).</span><span class="sxs-lookup"><span data-stu-id="4bd94-169">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="4bd94-170">Übergeben einer ungültigen Schlüssel Definition im <strong>szkey</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4bd94-170">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="4bd94-171">Eine Erörterung gültiger Definitionen finden Sie unter <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="4bd94-171">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="4bd94-172">Das Festlegen des <strong>cbvarsegmac</strong> -Members in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> auf größer als JET_cbPrimaryKeyMost (für einen primären Index) oder größer als JET_cbSecondaryKeyMost (für einen sekundären Index).</span><span class="sxs-lookup"><span data-stu-id="4bd94-172">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="4bd94-173">Übergeben einer ungültigen Kombination für einen benutzerdefinierten Unicode-Index (einen, bei dem das JET_bitIndexUnicode Bit im <strong>grbit</strong> -Member von <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="4bd94-173">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="4bd94-174">Zu den häufigsten Gründen gehören das <strong>pidxunicode</strong> -Element der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur ist NULL, oder die in der <strong>pidxunicode</strong> -Struktur angegebene LCID ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4bd94-174">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="4bd94-175">Angeben einer mehrwertigen Spalte für einen primären Index.</span><span class="sxs-lookup"><span data-stu-id="4bd94-175">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="4bd94-176">Es wird versucht, zu viele bedingte Spalten zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="4bd94-176">Trying to index too many conditional columns.</span></span> <span data-ttu-id="4bd94-177">Der <strong>cconditionalcolumn</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur darf nicht größer als JET_ccolKeyMost sein.</span><span class="sxs-lookup"><span data-stu-id="4bd94-177">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-178">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="4bd94-178">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="4bd94-179">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="4bd94-179">Windows XP and later.</span></span> <span data-ttu-id="4bd94-180">Es wurde eine <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur angegeben, und ihre Grenzen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-180">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="4bd94-181">Weitere Informationen finden Sie im Abschnitt "Hinweise" der <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> Struktur.</span><span class="sxs-lookup"><span data-stu-id="4bd94-181">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-182">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="4bd94-182">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="4bd94-183">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="4bd94-183">Windows XP and later.</span></span> <span data-ttu-id="4bd94-184">Ein Tupelindex kann nicht eindeutig sein (d. h., der <em>grbit</em> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexUnique festgelegt werden).</span><span class="sxs-lookup"><span data-stu-id="4bd94-184">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-185">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="4bd94-185">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="4bd94-186">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="4bd94-186">Windows XP and later.</span></span> <span data-ttu-id="4bd94-187">Ein Tupelindex kann nur über eine einzelne Spalte verfügen (d. h., wenn der <strong>grbit</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur JET_bitIndexTuples festgelegt hat und der <strong>szkey</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur mehr als eine Spalte angibt).</span><span class="sxs-lookup"><span data-stu-id="4bd94-187">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-188">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="4bd94-188">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="4bd94-189">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="4bd94-189">Windows XP and later.</span></span> <span data-ttu-id="4bd94-190">Bei einem Tupelindex kann es sich nicht um einen primären Index handeln (d. h., der <strong>grbit</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur darf nicht sowohl JET_bitIndexPrimary als auch JET_bitIndexTuples festgelegt werden).</span><span class="sxs-lookup"><span data-stu-id="4bd94-190">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-191">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="4bd94-191">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="4bd94-192">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="4bd94-192">Windows XP and later.</span></span> <span data-ttu-id="4bd94-193">Ein Tupelindex lässt nicht zu, dass der <strong>cbvarsegmac</strong> -Member der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4bd94-193">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-194">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="4bd94-194">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="4bd94-195">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="4bd94-195">Windows XP and later.</span></span> <span data-ttu-id="4bd94-196">Ein Tupelindex kann nur für eine Text-oder Unicode-Spalte gelten.</span><span class="sxs-lookup"><span data-stu-id="4bd94-196">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="4bd94-197">Der Versuch, andere Spalten (z. b. binäre Spalten) zu indizieren, führt zu JET_errIndexTuplesTextColumnsOnly.</span><span class="sxs-lookup"><span data-stu-id="4bd94-197">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-198">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="4bd94-198">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="4bd94-199">Es wurde versucht, einen Index ohne Versionsinformationen zu erstellen, während eine Transaktion durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="4bd94-199">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-200">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="4bd94-200">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="4bd94-201">Der <strong>CP</strong> -Member der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur wurde nicht auf eine gültige Codepage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-201">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="4bd94-202">Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="4bd94-202">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="4bd94-203">Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</span><span class="sxs-lookup"><span data-stu-id="4bd94-203">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-204">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="4bd94-204">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="4bd94-205">Der <strong>colttmember</strong> der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur wurde nicht auf einen gültigen Spaltentyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-205">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-206">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="4bd94-206">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="4bd94-207">Mögliche Ursachen für diesen Fehler:</span><span class="sxs-lookup"><span data-stu-id="4bd94-207">Some of the reasons this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="4bd94-208">Der <strong>rgindexcreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> Struktur wurde auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-208">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="4bd94-209">Der <strong>rgcolumncreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> Struktur wurde auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="4bd94-210">Der <strong>cbStruct</strong> -Member einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur wurde nicht auf einen gültigen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-210">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-211">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="4bd94-211">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="4bd94-212">In <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> oder <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>wurde eine ungültige Kombination von <strong>grbit</strong> -Membern angegeben.</span><span class="sxs-lookup"><span data-stu-id="4bd94-212">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span></span></p>
<p><span data-ttu-id="4bd94-213">Die Index Definition ist ungültig, da der <strong>grbit</strong> -Member inkonsistente Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="4bd94-213">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="4bd94-214">Mögliche Ursachen:</span><span class="sxs-lookup"><span data-stu-id="4bd94-214">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="4bd94-215">Für einen primären Index wurde ein Ignore-Bit angegeben (d. h. JET_bitIndexPrimary mit JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull oder JET_bitIndexIgnoreFirstNull).</span><span class="sxs-lookup"><span data-stu-id="4bd94-215">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="4bd94-216">Ein leerer Index ignoriert keine NULL-Elemente (d. h., das <strong>grbit</strong> -Element der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur hat JET_bitIndexEmpty festgelegt, aber nicht JET_bitIndexIgnoreAnyNull festgelegt).</span><span class="sxs-lookup"><span data-stu-id="4bd94-216">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="4bd94-217">Übergeben einer <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> -Struktur mit einem ungültigen <strong>grbit</strong> -Member.</span><span class="sxs-lookup"><span data-stu-id="4bd94-217">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-218">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="4bd94-218">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="4bd94-219">Es wurde eine ungültige Gebiets Schema-ID (LCID) übergeben (entweder über den <strong>LCID</strong> -Member der <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> -Struktur, auf die durch das <strong>pidxunicode</strong> -Element in der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur verwiesen wird, oder über das <strong>LCID</strong> -Feld der <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur).</span><span class="sxs-lookup"><span data-stu-id="4bd94-219">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure, or through the <strong>lcid</strong> field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-220">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4bd94-220">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="4bd94-221">Ein ungültiger Parameter wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="4bd94-221">An invalid parameter was given.</span></span> <span data-ttu-id="4bd94-222">Mögliche Ursachen:</span><span class="sxs-lookup"><span data-stu-id="4bd94-222">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="4bd94-223">Der <strong>rgcolumncreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> -Struktur ist NULL.</span><span class="sxs-lookup"><span data-stu-id="4bd94-223">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="4bd94-224">Der <strong>cbStruct</strong> -Member einer der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Strukturen, die im <strong>rgcolumncreate</strong> -Member der <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> -Struktur angegeben sind, wurde nicht auf sizeof (JET_COLUMNCREATE) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-224">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="4bd94-225">Der <strong>cbkey</strong> -Member einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> -Struktur ist auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-225">The <strong>cbKey</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="4bd94-226">Der <strong>cbStruct</strong> -Member einer <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> Struktur ist nicht auf sizeof (JET_INDEXCREATE) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-226">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof( JET_INDEXCREATE ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-227">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="4bd94-227">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="4bd94-228">Der Datensatz ist zu groß.</span><span class="sxs-lookup"><span data-stu-id="4bd94-228">The record is too big.</span></span> <span data-ttu-id="4bd94-229">Die Summe des <strong>cbmax</strong> -Members der <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> Struktur für alle festgelegten Spalten darf einen bestimmten Wert nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="4bd94-229">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-230">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="4bd94-230">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="4bd94-231">Die Tabelle ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4bd94-231">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-232">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="4bd94-232">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="4bd94-233">Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4bd94-233">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="4bd94-234">Eine Tabelle kann nicht mehr als JET_ccolFixedMost fester Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierte Spalten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4bd94-234">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-235">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="4bd94-235">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="4bd94-236">Fehler beim Versuch, eine Unicode-Spalte zu normalisieren.</span><span class="sxs-lookup"><span data-stu-id="4bd94-236">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="4bd94-237">Dies kann darauf zurückzuführen sein, dass die Systemressourcen nicht mehr ausreichen.</span><span class="sxs-lookup"><span data-stu-id="4bd94-237">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="4bd94-238">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bd94-238">Remarks</span></span>

<span data-ttu-id="4bd94-239">**Jetkreatetable** erstellt eine Tabelle, die keine Spalten enthält.</span><span class="sxs-lookup"><span data-stu-id="4bd94-239">**JetCreateTable** creates a table which does not contain any columns.</span></span> <span data-ttu-id="4bd94-240">Informationen zum Hinzufügen von Spalten finden Sie unter [jetaddcolumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="4bd94-240">To add columns, see [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="4bd94-241">Im internen Aufruf ruft **jetkreatetable** [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)auf und füllt eine [JET_TABLECREATE2](./jet-tablecreate2-structure.md) Struktur mit folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="4bd94-241">Internally, **JetCreateTable** calls [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), filling in a [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure with:</span></span>

  - <span data-ttu-id="4bd94-242">JET_TABLECREATE2. cbStruct = sizeof (JET_TABLECREATE2)</span><span class="sxs-lookup"><span data-stu-id="4bd94-242">JET_TABLECREATE2.cbStruct = sizeof( JET_TABLECREATE2 )</span></span>

  - <span data-ttu-id="4bd94-243">JET_TABLECREATE2. sztablename = sztablename</span><span class="sxs-lookup"><span data-stu-id="4bd94-243">JET_TABLECREATE2.szTableName = szTableName</span></span>

  - <span data-ttu-id="4bd94-244">JET_TABLECREATE2. ulpages = lpage</span><span class="sxs-lookup"><span data-stu-id="4bd94-244">JET_TABLECREATE2.ulPages = lPage</span></span>

  - <span data-ttu-id="4bd94-245">JET_TABLECREATE2. uldensity = ldensity</span><span class="sxs-lookup"><span data-stu-id="4bd94-245">JET_TABLECREATE2.ulDensity = lDensity</span></span>

  - <span data-ttu-id="4bd94-246">JET_TABLECREATE2. TableID = JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="4bd94-246">JET_TABLECREATE2.tableid = JET_tableidNil</span></span>

<span data-ttu-id="4bd94-247">Alle anderen Felder der internen [JET_TABLECREATE2](./jet-tablecreate2-structure.md) Struktur werden auf 0 (null) oder NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-247">All the other fields of the internal [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure are set to zero or NULL.</span></span> <span data-ttu-id="4bd94-248">Bei der Ausgabe wird *pTableID* auf JET_TABLECREATE2. TableID festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4bd94-248">On output, *ptableid* will be set to JET_TABLECREATE2.tableid.</span></span>

<span data-ttu-id="4bd94-249">Weitere Informationen finden Sie unter [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="4bd94-249">See [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) for more details.</span></span>

<span data-ttu-id="4bd94-250">Wenn die Anwendung mit dem zurückgegebenen **TableID** -Member aus der [JET_TABLECREATE2](./jet-tablecreate2-structure.md) Struktur ausgeführt [wird, sollte](./jetopentable-function.md)Sie in der Regel mit " [jetclosetable](./jetclosetable-function.md)" geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="4bd94-250">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned **tableid** member from the [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="4bd94-251">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bd94-251">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-252"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="4bd94-252"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4bd94-253">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4bd94-253">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-254"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4bd94-254"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4bd94-255">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4bd94-255">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-256"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4bd94-256"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4bd94-257">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="4bd94-257">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-258"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="4bd94-258"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4bd94-259">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4bd94-259">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bd94-260"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4bd94-260"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4bd94-261">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4bd94-261">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bd94-262"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4bd94-262"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4bd94-263">Implementiert als <strong>jetkreatetablew</strong> (Unicode) und <strong>jetkreatetablea</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="4bd94-263">Implemented as <strong>JetCreateTableW</strong> (Unicode) and <strong>JetCreateTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4bd94-264">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4bd94-264">See Also</span></span>

[<span data-ttu-id="4bd94-265">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="4bd94-265">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="4bd94-266">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4bd94-266">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4bd94-267">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4bd94-267">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4bd94-268">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4bd94-268">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4bd94-269">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="4bd94-269">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="4bd94-270">Jetaddcolumn</span><span class="sxs-lookup"><span data-stu-id="4bd94-270">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="4bd94-271">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="4bd94-271">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="4bd94-272">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="4bd94-272">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
