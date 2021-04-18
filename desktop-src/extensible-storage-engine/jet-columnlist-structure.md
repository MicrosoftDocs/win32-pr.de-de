---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNLIST Struktur'
title: JET_COLUMNLIST-Struktur
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9bce36c818dd35408d95c770540ff4865bdf639b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354542"
---
# <a name="jet_columnlist-structure"></a><span data-ttu-id="14202-103">JET_COLUMNLIST-Struktur</span><span class="sxs-lookup"><span data-stu-id="14202-103">JET_COLUMNLIST Structure</span></span>


<span data-ttu-id="14202-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="14202-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnlist-structure"></a><span data-ttu-id="14202-105">JET_COLUMNLIST-Struktur</span><span class="sxs-lookup"><span data-stu-id="14202-105">JET_COLUMNLIST Structure</span></span>

<span data-ttu-id="14202-106">Die **JET_COLUMNLIST** -Struktur enthält die Informationen, die erforderlich sind, um die temporäre Tabelle zu durchlaufen, die von den Funktionen [jetgetcolumninfo](./jetgetcolumninfo-function.md) und [jetgettablecolumninfo](./jetgettablecolumninfo-function.md) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="14202-106">The **JET_COLUMNLIST** structure contains the information necessary to traverse the temporary table that is created by the [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions.</span></span> <span data-ttu-id="14202-107">Jede Zeile in der temporären Tabelle beschreibt eine Spalte in der Tabelle, die im API-Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="14202-107">Each row in the temporary table describes a column in the table given in the API call.</span></span> <span data-ttu-id="14202-108">Diese Struktur wird nur mit [jetgetcolumninfo](./jetgetcolumninfo-function.md) und [jetgettablecolumninfo](./jetgettablecolumninfo-function.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="14202-108">This structure is used with only with [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a><span data-ttu-id="14202-109">Member</span><span class="sxs-lookup"><span data-stu-id="14202-109">Members</span></span>

<span data-ttu-id="14202-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="14202-110">**cbStruct**</span></span>

<span data-ttu-id="14202-111">Die Größe der Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="14202-111">The size of the structure in bytes.</span></span> <span data-ttu-id="14202-112">Der API-Aufruf aktualisiert dieses Feld, sodass der Aufrufer sicherstellen muss, dass dieser Wert sizeof (JET_COLUMNLIST) entspricht.</span><span class="sxs-lookup"><span data-stu-id="14202-112">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_COLUMNLIST ).</span></span>

<span data-ttu-id="14202-113">**TableID**</span><span class="sxs-lookup"><span data-stu-id="14202-113">**tableid**</span></span>

<span data-ttu-id="14202-114">Der Tabellen Bezeichner der temporären Tabelle, die erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="14202-114">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="14202-115">Es liegt in der Verantwortung des Aufrufers, die Tabelle zu schließen.</span><span class="sxs-lookup"><span data-stu-id="14202-115">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="14202-116">**crecord**</span><span class="sxs-lookup"><span data-stu-id="14202-116">**cRecord**</span></span>

<span data-ttu-id="14202-117">Die Anzahl der Datensätze in der temporären Tabelle, die durch den API-Befehl erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="14202-117">The number of records in the temporary table that was created by the API call.</span></span>

<span data-ttu-id="14202-118">**columnidpresentationorder**</span><span class="sxs-lookup"><span data-stu-id="14202-118">**columnidPresentationOrder**</span></span>

<span data-ttu-id="14202-119">Der Spalten Bezeichner der Präsentations Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="14202-119">The column identifier of the presentation order.</span></span>

<span data-ttu-id="14202-120">Die Präsentations Reihenfolge wird verwendet, um die Zeilen der temporären Tabelle zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="14202-120">The presentation order is used to sort the rows of the temporary table.</span></span> <span data-ttu-id="14202-121">Die Präsentations Reihenfolge ist ein festes [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="14202-121">The presentation order is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="14202-122">Wenn die angegebene Informationsebene keine Compact-Ebene war, wird Sie auch als JET_bitColumnTTKey gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="14202-122">If the information level that was specified was not a compact level, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="14202-123">**columnidcolumnname**</span><span class="sxs-lookup"><span data-stu-id="14202-123">**columnidcolumnname**</span></span>

<span data-ttu-id="14202-124">Der Spalten Bezeichner des Spaltennamens.</span><span class="sxs-lookup"><span data-stu-id="14202-124">The column identifier of the name of the column.</span></span>

<span data-ttu-id="14202-125">Wenn die angegebene Informationsebene nicht kompakt ist, wird Sie auch als JET_bitColumnTTKey gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="14202-125">If the information level specified was not compact, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="14202-126">**columnidcolumnid**</span><span class="sxs-lookup"><span data-stu-id="14202-126">**columnidcolumnid**</span></span>

<span data-ttu-id="14202-127">Der Spalten Bezeichner des Spalten Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="14202-127">The column identifier of the column identifier.</span></span>

<span data-ttu-id="14202-128">Der Spalten Bezeichner ist ein fester [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="14202-128">The column identifier is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="14202-129">**columnidcolyp**</span><span class="sxs-lookup"><span data-stu-id="14202-129">**columnidcoltyp**</span></span>

<span data-ttu-id="14202-130">Der Spalten Bezeichner des Spalten Typs.</span><span class="sxs-lookup"><span data-stu-id="14202-130">The column identifier of the column type.</span></span>

<span data-ttu-id="14202-131">Der Spaltentyp ist ein fester [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="14202-131">The column type is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="14202-132">**columnidcountry**</span><span class="sxs-lookup"><span data-stu-id="14202-132">**columnidCountry**</span></span>

<span data-ttu-id="14202-133">Der Spalten Bezeichner des Ländercodes.</span><span class="sxs-lookup"><span data-stu-id="14202-133">The column identifier of the country code.</span></span>

<span data-ttu-id="14202-134">Der Ländercode ist ein fester [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="14202-134">The country code is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="14202-135">**columnidlangid**</span><span class="sxs-lookup"><span data-stu-id="14202-135">**columnidLangid**</span></span>

<span data-ttu-id="14202-136">Der Spalten Bezeichner des sprach Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="14202-136">The column identifier of the language identifier.</span></span>

<span data-ttu-id="14202-137">Der sprach Bezeichner ist ein fester [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="14202-137">The language identifier is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="14202-138">**columnidcp**</span><span class="sxs-lookup"><span data-stu-id="14202-138">**columnidCp**</span></span>

<span data-ttu-id="14202-139">Der Spalten Bezeichner der Codepage.</span><span class="sxs-lookup"><span data-stu-id="14202-139">The column identifier of the code page.</span></span>

<span data-ttu-id="14202-140">Die Codepage ist ein festes [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="14202-140">The code page is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="14202-141">**columnidcollate**</span><span class="sxs-lookup"><span data-stu-id="14202-141">**columnidCollate**</span></span>

<span data-ttu-id="14202-142">Der Spalten Bezeichner der Sortierungs Sequenz.</span><span class="sxs-lookup"><span data-stu-id="14202-142">The column identifier of the collation sequence.</span></span>

<span data-ttu-id="14202-143">Die Sortierreihenfolge ist ein festes [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="14202-143">The collation sequence is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="14202-144">**columnidcbmax**</span><span class="sxs-lookup"><span data-stu-id="14202-144">**columnidcbMax**</span></span>

<span data-ttu-id="14202-145">Der Spalten Bezeichner des **cbmax** -Felds.</span><span class="sxs-lookup"><span data-stu-id="14202-145">The column identifier of the **cbMax** field.</span></span>

<span data-ttu-id="14202-146">**Cbmax** ist ein fester [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="14202-146">The **cbMax** is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="14202-147">**columnidgrbit**</span><span class="sxs-lookup"><span data-stu-id="14202-147">**columnidgrbit**</span></span>

<span data-ttu-id="14202-148">Der Spalten Bezeichner der *grbits* der Spalte.</span><span class="sxs-lookup"><span data-stu-id="14202-148">The column identifier of the *grbits* of the column.</span></span> <span data-ttu-id="14202-149">Das *grbit* -Feld ist ein festes [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="14202-149">The *grbit* field is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="14202-150">Weitere Informationen zu diesen Bits finden Sie unter [JET_COLUMNDEF](./jet-columndef-structure.md).</span><span class="sxs-lookup"><span data-stu-id="14202-150">For more information about these bits, see [JET_COLUMNDEF](./jet-columndef-structure.md).</span></span>

<span data-ttu-id="14202-151">Für **columnidgrbit** sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="14202-151">The following are possible values for **columnidgrbit**:</span></span>

<span data-ttu-id="14202-152">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="14202-152">JET_bitColumnTagged</span></span>

<span data-ttu-id="14202-153">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="14202-153">JET_bitColumnFixed</span></span>

<span data-ttu-id="14202-154">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="14202-154">JET_bitColumnUpdatable</span></span>

<span data-ttu-id="14202-155">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="14202-155">JET_bitColumnNotNULL</span></span>

<span data-ttu-id="14202-156">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="14202-156">JET_bitColumnAutoincrement</span></span>

<span data-ttu-id="14202-157">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="14202-157">JET_bitColumnVersion</span></span>

<span data-ttu-id="14202-158">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="14202-158">JET_bitColumnMultiValued</span></span>

<span data-ttu-id="14202-159">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="14202-159">JET_bitColumnEscrowUpdate</span></span>

<span data-ttu-id="14202-160">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="14202-160">JET_bitColumnFinalize</span></span>

<span data-ttu-id="14202-161">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="14202-161">JET_bitColumnDeleteOnZero</span></span>

<span data-ttu-id="14202-162">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="14202-162">JET_bitColumnUserDefinedDefault</span></span>

<span data-ttu-id="14202-163">**columniddefault**</span><span class="sxs-lookup"><span data-stu-id="14202-163">**columnidDefault**</span></span>

<span data-ttu-id="14202-164">Der Spalten Bezeichner des Standardwerts der Spalte.</span><span class="sxs-lookup"><span data-stu-id="14202-164">The column identifier of the default value of the column.</span></span>

<span data-ttu-id="14202-165">Der Standardwert ist eine [JET_coltypLongBinary](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="14202-165">The default value is a [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

<span data-ttu-id="14202-166">**columnidbasetablename**</span><span class="sxs-lookup"><span data-stu-id="14202-166">**columnidBaseTableName**</span></span>

<span data-ttu-id="14202-167">Der Spalten Bezeichner des Namens der Tabelle, aus der die Tabelle abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="14202-167">The column identifier of the name of the table from which the table was derived.</span></span>

<span data-ttu-id="14202-168">Der Tabellenname ist eine [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="14202-168">The table name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="14202-169">**columnidbasecolumschlag Name**</span><span class="sxs-lookup"><span data-stu-id="14202-169">**columnidBaseColumnName**</span></span>

<span data-ttu-id="14202-170">Der Spalten Bezeichner des Namens der Spalte, von der die Spalte abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="14202-170">The column identifier of the name of the column from which the column was derived.</span></span>

<span data-ttu-id="14202-171">Der Spaltenname ist eine [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="14202-171">The column name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="14202-172">**columnidDefinitionName**</span><span class="sxs-lookup"><span data-stu-id="14202-172">**columnidDefinitionName**</span></span>

<span data-ttu-id="14202-173">Der Spalten Bezeichner des Namens der Spaltendefinition.</span><span class="sxs-lookup"><span data-stu-id="14202-173">The column identifier of the name of the column definition.</span></span>

<span data-ttu-id="14202-174">Der Spalten Definitions Name ist eine [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="14202-174">The column definition name is a [JET_coltypText](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="14202-175">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14202-175">Remarks</span></span>

<span data-ttu-id="14202-176">Standardmäßig wird die Reihenfolge der Zeilen in der temporären Tabelle nach dem Namen der Spalte sortiert.</span><span class="sxs-lookup"><span data-stu-id="14202-176">By default, the order of the rows in the temporary table is sorted by the name of the column.</span></span> <span data-ttu-id="14202-177">Sie kann auch nach Spalten Bezeichner sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="14202-177">It can also be sorted by column identifier.</span></span> <span data-ttu-id="14202-178">Weitere Informationen zum Sortieren nach Spalten Bezeichner finden Sie unter [jetgetcolumninfo](./jetgetcolumninfo-function.md) und [jetgettablecolumninfo](./jetgettablecolumninfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="14202-178">For more information about how to sort by column identifier, see [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

<span data-ttu-id="14202-179">Beim Aufrufen von [jetgetcolumninfo](./jetgetcolumninfo-function.md) oder [jetgettablecolumninfo](./jetgettablecolumninfo-function.md) kann eine kompakte Form von Ergebnissen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="14202-179">The call to [JetGetColumnInfo](./jetgetcolumninfo-function.md) or [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) might specify a compact form of results.</span></span> <span data-ttu-id="14202-180">Wenn Spalten von einer Vorlagen Tabelle geerbt wurden, werden Sie in den Compact-Ergebnissen nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14202-180">If any columns have been inherited from a template table, the compact results will not store them.</span></span>

### <a name="requirements"></a><span data-ttu-id="14202-181">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14202-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14202-182"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="14202-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="14202-183">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="14202-183">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14202-184"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="14202-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="14202-185">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="14202-185">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14202-186"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="14202-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="14202-187">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="14202-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="14202-188">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14202-188">See Also</span></span>

[<span data-ttu-id="14202-189">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="14202-189">JET_COLTYP</span></span>](./jet-coltyp.md)

[<span data-ttu-id="14202-190">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="14202-190">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)

[<span data-ttu-id="14202-191">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="14202-191">JET_COLUMNID</span></span>](./jet-columnid.md)

[<span data-ttu-id="14202-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="14202-192">JET_ERR</span></span>](./jet-err.md)

[<span data-ttu-id="14202-193">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="14202-193">JET_GRBIT</span></span>](./jet-grbit.md)

[<span data-ttu-id="14202-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="14202-194">JET_SESID</span></span>](./jet-sesid.md)

[<span data-ttu-id="14202-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="14202-195">JET_TABLEID</span></span>](./jet-tableid.md)

[<span data-ttu-id="14202-196">Jetgetcolumninfo</span><span class="sxs-lookup"><span data-stu-id="14202-196">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)

[<span data-ttu-id="14202-197">Jetgettablecolumninfo</span><span class="sxs-lookup"><span data-stu-id="14202-197">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
