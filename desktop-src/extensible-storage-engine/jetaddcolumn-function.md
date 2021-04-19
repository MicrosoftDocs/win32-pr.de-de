---
description: 'Weitere Informationen zu: jetaddcolumn-Funktion'
title: JetAddColumn-Funktion
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b8c3eac113daeae43ec4a8e62b7fcda9ddbf9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368962"
---
# <a name="jetaddcolumn-function"></a><span data-ttu-id="76a9e-103">JetAddColumn-Funktion</span><span class="sxs-lookup"><span data-stu-id="76a9e-103">JetAddColumn Function</span></span>


<span data-ttu-id="76a9e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="76a9e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetaddcolumn-function"></a><span data-ttu-id="76a9e-105">JetAddColumn-Funktion</span><span class="sxs-lookup"><span data-stu-id="76a9e-105">JetAddColumn Function</span></span>

<span data-ttu-id="76a9e-106">Die **jetaddcolumn** -Funktion fügt einer vorhandenen Tabelle in einer ESE-Datenbank eine neue Spalte hinzu.</span><span class="sxs-lookup"><span data-stu-id="76a9e-106">The **JetAddColumn** function adds a new column to an existing table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="76a9e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="76a9e-107">Parameters</span></span>

<span data-ttu-id="76a9e-108">*-sid*</span><span class="sxs-lookup"><span data-stu-id="76a9e-108">*sesid*</span></span>

<span data-ttu-id="76a9e-109">Der für den API-Befehl zu verwendende Daten Bank Sitzungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="76a9e-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="76a9e-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="76a9e-110">*tableid*</span></span>

<span data-ttu-id="76a9e-111">Die Tabelle, der die Spalte hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76a9e-111">The table to which to add the column.</span></span>

<span data-ttu-id="76a9e-112">*szcolumnname*</span><span class="sxs-lookup"><span data-stu-id="76a9e-112">*szColumnName*</span></span>

<span data-ttu-id="76a9e-113">Der Name der hinzu zufügenden Spalte.</span><span class="sxs-lookup"><span data-stu-id="76a9e-113">The name of the column to add.</span></span> <span data-ttu-id="76a9e-114">Der Name muss die folgenden Kriterien erfüllen:</span><span class="sxs-lookup"><span data-stu-id="76a9e-114">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="76a9e-115">Es muss weniger als JET_cbNameMost Zeichen lang sein, ohne das abschließende **null**-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="76a9e-115">It must be fewer than JET_cbNameMost characters in length, not including the terminating **NULL**.</span></span>

  - <span data-ttu-id="76a9e-116">Sie darf nur Zeichen aus den folgenden Sätzen enthalten: 0 bis 9, A bis Z, A bis Z und alle anderen Interpunktions Zeichen außer Ausrufezeichen ( \! ), Komma (,), öffnende eckige Klammer ( \[ ) und schließende Klammer ( \] ) – das heißt, die ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c und 0x5d bis 0x7F.</span><span class="sxs-lookup"><span data-stu-id="76a9e-116">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="76a9e-117">Er darf nicht mit einem Leerzeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="76a9e-117">It cannot begin with a space.</span></span>

  - <span data-ttu-id="76a9e-118">Sie muss mindestens ein Zeichen enthalten, das kein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="76a9e-118">It must contain at least one non-space character.</span></span>

<span data-ttu-id="76a9e-119">*pcolumndef*</span><span class="sxs-lookup"><span data-stu-id="76a9e-119">*pcolumndef*</span></span>

<span data-ttu-id="76a9e-120">Ein Zeiger auf eine [JET_COLUMNDEF](./jet-columndef-structure.md) -Struktur, die die Daten definiert, die in einer Spalte gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="76a9e-120">A pointer to a [JET_COLUMNDEF](./jet-columndef-structure.md) structure, which defines the data that can be stored in a column.</span></span>

<span data-ttu-id="76a9e-121">*pvdefault*</span><span class="sxs-lookup"><span data-stu-id="76a9e-121">*pvDefault*</span></span>

<span data-ttu-id="76a9e-122">Ein Zeiger auf einen Puffer, der den Standardwert für die Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="76a9e-122">A pointer to a buffer that contains the default value for the column.</span></span> <span data-ttu-id="76a9e-123">Die Länge des Puffers ist **cbdefault**.</span><span class="sxs-lookup"><span data-stu-id="76a9e-123">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="76a9e-124">Wenn kein Standardwert vorhanden ist, legen Sie **pvdefault** auf **null** und **cbdefault** auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="76a9e-124">If there is no default, set **pvDefault** to **NULL** and **cbDefault** to zero.</span></span> <span data-ttu-id="76a9e-125">Standardwerte dürfen nicht größer als JET_cbColumnMost Bytes für Fixed-Spalten oder JET_cbLVDefaultValueMost Bytes für Long-Werte sein.</span><span class="sxs-lookup"><span data-stu-id="76a9e-125">Default values cannot be larger than JET_cbColumnMost bytes for fixed columns or JET_cbLVDefaultValueMost bytes for long values.</span></span> <span data-ttu-id="76a9e-126">Wenn ein Standardwert größer als dieser Wert ist, wird er automatisch abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="76a9e-126">If a default value is larger than that, it will be silently truncated.</span></span>

<span data-ttu-id="76a9e-127">Wenn *grbit* JET_bitColumnUserDefinedDefault festgelegt ist, wird **pvdefault** als Zeiger auf eine [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="76a9e-127">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure.</span></span>

<span data-ttu-id="76a9e-128">*cbdefault*</span><span class="sxs-lookup"><span data-stu-id="76a9e-128">*cbDefault*</span></span>

<span data-ttu-id="76a9e-129">Die Größe (in Bytes) des Puffers, der in **pvdefault** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="76a9e-129">The size, in bytes, of the buffer that is specified in **pvDefault**.</span></span>

<span data-ttu-id="76a9e-130">*pColumnID*</span><span class="sxs-lookup"><span data-stu-id="76a9e-130">*pcolumnid*</span></span>

<span data-ttu-id="76a9e-131">Ein Zeiger auf eine [JET_COLUMNID](./jet-columnid.md) -Struktur, die bei Erfolg den Bezeichner der neu erstellten Spalte empfängt.</span><span class="sxs-lookup"><span data-stu-id="76a9e-131">A pointer to a [JET_COLUMNID](./jet-columnid.md) structure, which, on success, will receive the identifier of the newly created column.</span></span> <span data-ttu-id="76a9e-132">Bei einem Fehler ist der Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="76a9e-132">On failure, the value is undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="76a9e-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76a9e-133">Return Value</span></span>

<span data-ttu-id="76a9e-134">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="76a9e-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="76a9e-135">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="76a9e-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76a9e-136">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="76a9e-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="76a9e-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76a9e-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76a9e-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="76a9e-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="76a9e-139">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="76a9e-139">The operation was successful.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a9e-140">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="76a9e-140">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="76a9e-141">Es wurde versucht, die Datendefinition einer fixierten DDL-Tabelle zu ändern.</span><span class="sxs-lookup"><span data-stu-id="76a9e-141">An attempt was made to modify the data definition of a fixed DDL table.</span></span> <span data-ttu-id="76a9e-142">Ein Beispiel für eine Tabelle mit fester DDL ist eine Vorlagen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="76a9e-142">An example of a table with fixed DDL is a Template Table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a9e-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="76a9e-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="76a9e-144">Ein ungültiger Parameter wurde an die API übergeben.</span><span class="sxs-lookup"><span data-stu-id="76a9e-144">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="76a9e-145">Einige Beispiele für ungültige Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="76a9e-145">Some examples of invalid parameters are:</span></span></p>
<ul>
<li><p><span data-ttu-id="76a9e-146">Übergeben der falschen Größe der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> -Struktur in Ihrem <em>cbStruct</em> -Member.</span><span class="sxs-lookup"><span data-stu-id="76a9e-146">Passing in the wrong size of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure in its <em>cbStruct</em> member.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-147">Das übergeben von JET_bitColumnUserDefinedDefault, aber nicht das Festlegen von <strong>cbdefault</strong> auf sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span><span class="sxs-lookup"><span data-stu-id="76a9e-147">Passing in JET_bitColumnUserDefinedDefault, but not setting <strong>cbDefault</strong> to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a9e-148">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="76a9e-148">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="76a9e-149">Es wurde versucht, eine Spalte mit dem JET_bitColumnUnversioned-Bit hinzuzufügen, aber die Sitzung befindet sich derzeit in einer Transaktion.</span><span class="sxs-lookup"><span data-stu-id="76a9e-149">An attempt was made to add a column with the JET_bitColumnUnversioned bit set, but the session is currently in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a9e-150">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="76a9e-150">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="76a9e-151">Eine Spalte ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="76a9e-151">A column already exists.</span></span> <span data-ttu-id="76a9e-152">Es wurde versucht, eine Spalte ohne Versionsinformationen hinzuzufügen, und diese Spalte ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="76a9e-152">An attempt was made to add a column without version information, and that column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a9e-153">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="76a9e-153">JET_errTableNotEmpty</span></span></p></td>
<td><p><span data-ttu-id="76a9e-154">Die Tabelle enthält Daten.</span><span class="sxs-lookup"><span data-stu-id="76a9e-154">The table contains data.</span></span> <span data-ttu-id="76a9e-155">Eine Spalte für das Hinterlegungs Update kann nur einer leeren Tabelle hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="76a9e-155">An Escrow Update column can only be added to an empty table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a9e-156">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="76a9e-156">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="76a9e-157">Der Datensatz ist zu groß.</span><span class="sxs-lookup"><span data-stu-id="76a9e-157">The record is too big.</span></span> <span data-ttu-id="76a9e-158">Die Summe des <strong>cbmax</strong> -Parameters für die Fixed-Spalten darf einen bestimmten Wert nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="76a9e-158">The sum of the <strong>cbMax</strong> parameter for the fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a9e-159">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="76a9e-159">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="76a9e-160">Es wurde versucht, der Tabelle zu viele Spalten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="76a9e-160">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="76a9e-161">Eine Tabelle kann nicht mehr als JET_ccolFixedMost fester Spalten, nicht mehr als JET_ccolVarMost Spalten variabler Länge und nicht mehr als JET_ccolTaggedMost markierte Spalten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="76a9e-161">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a9e-162">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="76a9e-162">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="76a9e-163">Es wurde versucht, eine redundante Spalte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="76a9e-163">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="76a9e-164">Es darf nicht mehr als eine AUTOINCREMENT-Spalte und höchstens eine Versions Spalte pro Tabelle vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="76a9e-164">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a9e-165">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="76a9e-165">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="76a9e-166">Die Rückruffunktion konnte nicht aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="76a9e-166">The callback function could not be resolved.</span></span> <span data-ttu-id="76a9e-167">Die dll wurde möglicherweise nicht gefunden, oder die Funktion in der dll wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="76a9e-167">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="76a9e-168">Wenn eine ausreichende Protokollierung aktiviert ist, werden im Ereignisprotokoll weitere Details angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76a9e-168">The event log will provide more details if sufficient logging is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a9e-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="76a9e-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="76a9e-170">Eine Warnung, die angibt, dass die maximale Länge (<strong>cbmax</strong>) einer Fixed-oder Variable-Spalte größer als JET_cbColumnMost ist.</span><span class="sxs-lookup"><span data-stu-id="76a9e-170">A warning indicating that the maximum length (<strong>cbMax</strong>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="76a9e-171">Dieser Grenzwert gilt nicht für lange Werte ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> und <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="76a9e-171">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a9e-172">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="76a9e-172">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="76a9e-173">Ein ungültiger Name wurde als <strong>szcolumnname</strong>-Element übermittelt.</span><span class="sxs-lookup"><span data-stu-id="76a9e-173">An invalid name was passed as <strong>szColumnName</strong>.</span></span> <span data-ttu-id="76a9e-174">Weitere Informationen zu den Einschränkungen finden Sie unter den Kriterien für <strong>szcolumnname</strong>.</span><span class="sxs-lookup"><span data-stu-id="76a9e-174">For more information about the restrictions, see the criteria for <strong>szColumnName</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a9e-175">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="76a9e-175">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="76a9e-176">Das Feld <strong>colyp</strong> wurde nicht auf einen gültigen Spaltentyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="76a9e-176">The <strong>coltyp</strong> field was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a9e-177">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="76a9e-177">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="76a9e-178">Der <strong>CP</strong> -Parameter der <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> Struktur wurde nicht auf eine gültige Codepage festgelegt.</span><span class="sxs-lookup"><span data-stu-id="76a9e-178">The <strong>cp</strong> parameter of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="76a9e-179">Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="76a9e-179">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="76a9e-180">Der Wert 0 bedeutet, dass der Standardwert verwendet wird (Englisch, 1252).</span><span class="sxs-lookup"><span data-stu-id="76a9e-180">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a9e-181">JET_errTaggedNotNULL</span><span class="sxs-lookup"><span data-stu-id="76a9e-181">JET_errTaggedNotNULL</span></span></p></td>
<td><p><span data-ttu-id="76a9e-182">JET_bitColumnNotNULL können nicht mit markierten, langen Wert-oder SLV-Spalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76a9e-182">JET_bitColumnNotNULL cannot be used with tagged, Long Value, or SLV columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a9e-183">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="76a9e-183">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="76a9e-184">Es wurde eine ungültige Kombination von <em>grbits</em> angegeben.</span><span class="sxs-lookup"><span data-stu-id="76a9e-184">An invalid combination of <em>grbits</em> was specified.</span></span> <span data-ttu-id="76a9e-185">Mögliche Ursachen für diesen Fehler sind:</span><span class="sxs-lookup"><span data-stu-id="76a9e-185">Some of the reasons for this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="76a9e-186">JET_bitColumnFixed wurde für eine markierte, lange Wert-oder SLV-Spalte verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-186">JET_bitColumnFixed was used on a tagged, Long Value, or SLV column.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-187">JET_bitColumnEscrowUpdate wurde für eine Spalte verwendet, die nicht vom Typ " <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>" war.</span><span class="sxs-lookup"><span data-stu-id="76a9e-187">JET_bitColumnEscrowUpdate was used on a column that was not of type <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-188">JET_bitColumnEscrowUpdate wurde für eine Versions Spalte (JET_bitColumnVersion) verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-188">JET_bitColumnEscrowUpdate was used on a Version column (JET_bitColumnVersion).</span></span></p></li>
<li><p><span data-ttu-id="76a9e-189">JET_bitColumnEscrowUpdate wurde in einer autoincrememnt-Spalte (JET_bitColumnAutoincrement) verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-189">JET_bitColumnEscrowUpdate was used on an AutoIncrememnt column (JET_bitColumnAutoincrement).</span></span></p></li>
<li><p><span data-ttu-id="76a9e-190">JET_bitColumnEscrowUpdate wurde für eine Spalte verwendet, die keinen Standardwert enthielt (<strong>cbdefault</strong> war gleich null).</span><span class="sxs-lookup"><span data-stu-id="76a9e-190">JET_bitColumnEscrowUpdate was used on a column that did not have a default value (<strong>cbDefault</strong> was equal to zero).</span></span></p></li>
<li><p><span data-ttu-id="76a9e-191">JET_bitColumnFinalize wurde für eine Spalte verwendet, bei der es sich nicht um eine Spalte für eine hinterlegte Aktualisierung handelt (JET_bitColumnEscrowUpdate nicht festgelegt wurde).</span><span class="sxs-lookup"><span data-stu-id="76a9e-191">JET_bitColumnFinalize was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="76a9e-192">JET_bitColumnDeleteOnZero wurde für eine Spalte verwendet, bei der es sich nicht um eine Spalte für eine hinterlegte Aktualisierung handelt (JET_bitColumnEscrowUpdate nicht festgelegt wurde).</span><span class="sxs-lookup"><span data-stu-id="76a9e-192">JET_bitColumnDeleteOnZero was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="76a9e-193">JET_bitColumnAutoincrement wurde für eine Spalte verwendet, die nicht <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>wurde.</span><span class="sxs-lookup"><span data-stu-id="76a9e-193">JET_bitColumnAutoincrement was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p>
<p><span data-ttu-id="76a9e-194"><strong>Windows 2000:  </strong> Dieser Fehlercode wird nur in Windows 2000 verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-194"><strong>Windows 2000:  </strong>This reason for the error code is used only in Windows 2000.</span></span></p>
<p><span data-ttu-id="76a9e-195">JET_bitColumnAutoincrement wurde für eine Spalte verwendet, die weder <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> noch <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>war.</span><span class="sxs-lookup"><span data-stu-id="76a9e-195">JET_bitColumnAutoincrement was used on a column that was neither <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> nor <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</span></span></p>
<p><span data-ttu-id="76a9e-196"><strong>Windows XP:  </strong> Dieser Fehlercode wird in Windows XP und neueren Betriebssystemen verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-196"><strong>Windows XP:  </strong>This reason for the error code is used in Windows XP and later operating systems.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-197">JET_bitColumnVersion wurde für eine Spalte verwendet, die nicht <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>wurde.</span><span class="sxs-lookup"><span data-stu-id="76a9e-197">JET_bitColumnVersion was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-198">In einer autoincrement-Spalte wurde JET_bitColumnVersion verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-198">JET_bitColumnVersion was used on an autoincrement column.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-199">JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnFixed verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-199">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFixed.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-200">JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnNotNULL verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-200">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnNotNULL.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-201">JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnVersion verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-201">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnVersion.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-202">JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnAutoincrement verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-202">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnAutoincrement.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-203">JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnUpdatable verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-203">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnUpdatable.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-204">JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnEscrowUpdate verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-204">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnEscrowUpdate.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-205">JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnFinalize verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-205">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFinalize.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-206">JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnDeleteOnZero verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-206">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnDeleteOnZero.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-207">JET_bitColumnUserDefinedDefault in Verbindung mit JET_bitColumnMaybeNull verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-207">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnMaybeNull.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-208">JET_bitColumnUserDefinedDefault wurde für eine nicht markierte Spalte (fest oder Variable) verwendet.</span><span class="sxs-lookup"><span data-stu-id="76a9e-208">JET_bitColumnUserDefinedDefault was used on a non-tagged column (that is fixed or variable).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a9e-209">JET_errMultiValuedColumnMustBeTagged</span><span class="sxs-lookup"><span data-stu-id="76a9e-209">JET_errMultiValuedColumnMustBeTagged</span></span></p></td>
<td><p><span data-ttu-id="76a9e-210">Eine mehrwertige Spalte (JET_bitColumnMultiValued) kann nur für eine markierte oder lange Wert Spalte (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76a9e-210">A multi-valued column (JET_bitColumnMultiValued) can only be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a9e-211">JET_errCannotBeTagged</span><span class="sxs-lookup"><span data-stu-id="76a9e-211">JET_errCannotBeTagged</span></span></p></td>
<td><p><span data-ttu-id="76a9e-212">Es wurde versucht, eine markierte Spalte zu verwenden, wenn die Spalte möglicherweise nicht markiert ist.</span><span class="sxs-lookup"><span data-stu-id="76a9e-212">An attempt was made to use a tagged column when the column might not be tagged.</span></span> <span data-ttu-id="76a9e-213">Folgende Einschränkungen gelten für das Zulassen von markierten Spalten:</span><span class="sxs-lookup"><span data-stu-id="76a9e-213">Some of the constraints for disallowing tagged columns are:</span></span></p>
<ul>
<li><p><span data-ttu-id="76a9e-214">Eine Spalte für das Hinterlegungs Update (JET_bitColumnEscrowUpdate) kann nicht für eine markierte oder lange Wert Spalte (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76a9e-214">An Escrow Update column (JET_bitColumnEscrowUpdate) cannot be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-215">Eine AUTOINCREMENT-Spalte kann nicht markiert werden.</span><span class="sxs-lookup"><span data-stu-id="76a9e-215">An autoincrement column might not be tagged.</span></span></p></li>
<li><p><span data-ttu-id="76a9e-216">Eine Versions Spalte kann nicht markiert werden.</span><span class="sxs-lookup"><span data-stu-id="76a9e-216">A Version column might not be tagged.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a9e-217">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="76a9e-217">JET_errExclusiveTableLockRequired</span></span></p></td>
<td><p><span data-ttu-id="76a9e-218">Für diesen Vorgang war eine exklusive Sperre für die Tabelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="76a9e-218">An exclusive lock on the table was required for this operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a9e-219">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="76a9e-219">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="76a9e-220">Eine Warnung, die angibt, dass die maximale Länge (<em>cbmax</em>) einer Fixed-oder Variable-Spalte größer als JET_cbColumnMost ist.</span><span class="sxs-lookup"><span data-stu-id="76a9e-220">A warning indicating that the maximum length (<em>cbMax</em>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="76a9e-221">Dieser Grenzwert gilt nicht für lange Werte ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> und <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="76a9e-221">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="76a9e-222">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76a9e-222">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76a9e-223"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="76a9e-223"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="76a9e-224">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="76a9e-224">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a9e-225"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="76a9e-225"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="76a9e-226">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="76a9e-226">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a9e-227"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="76a9e-227"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="76a9e-228">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="76a9e-228">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a9e-229"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="76a9e-229"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="76a9e-230">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="76a9e-230">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76a9e-231"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="76a9e-231"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="76a9e-232">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="76a9e-232">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76a9e-233"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="76a9e-233"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="76a9e-234">Implementiert als <strong>jetaddcolumnw</strong> (Unicode) und <strong>jetaddcolumna</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="76a9e-234">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="76a9e-235">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="76a9e-235">See Also</span></span>

[<span data-ttu-id="76a9e-236">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="76a9e-236">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="76a9e-237">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="76a9e-237">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="76a9e-238">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="76a9e-238">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="76a9e-239">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="76a9e-239">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="76a9e-240">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="76a9e-240">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="76a9e-241">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="76a9e-241">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="76a9e-242">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="76a9e-242">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="76a9e-243">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="76a9e-243">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="76a9e-244">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="76a9e-244">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="76a9e-245">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="76a9e-245">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
