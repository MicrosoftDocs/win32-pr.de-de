---
description: 'Weitere Informationen finden Sie hier: JET_INDEXLIST Struktur'
title: JET_INDEXLIST-Struktur
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
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
ms.openlocfilehash: a696d1c52a42cad2b3b67b047984b48d77637a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346998"
---
# <a name="jet_indexlist-structure"></a><span data-ttu-id="e637f-103">JET_INDEXLIST-Struktur</span><span class="sxs-lookup"><span data-stu-id="e637f-103">JET_INDEXLIST Structure</span></span>


<span data-ttu-id="e637f-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e637f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexlist-structure"></a><span data-ttu-id="e637f-105">JET_INDEXLIST-Struktur</span><span class="sxs-lookup"><span data-stu-id="e637f-105">JET_INDEXLIST Structure</span></span>

<span data-ttu-id="e637f-106">Die **JET_INDEXLIST** -Struktur enthält die erforderlichen Informationen zum Durchlaufen einer temporären Tabelle, die von der [jetgetindexinfo](./jetgetindexinfo-function.md) -Funktion oder der [jetgettableindexinfo](./jetgettableindexinfo-function.md) -Funktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e637f-106">The **JET_INDEXLIST** structure contains the necessary information to traverse a temporary table that is created by the [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) functions.</span></span> <span data-ttu-id="e637f-107">Jede Zeile in der temporären Tabelle beschreibt eine Spalte eines Indexes.</span><span class="sxs-lookup"><span data-stu-id="e637f-107">Each row in the temporary table describes a column of an index.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a><span data-ttu-id="e637f-108">Member</span><span class="sxs-lookup"><span data-stu-id="e637f-108">Members</span></span>

<span data-ttu-id="e637f-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="e637f-109">**cbStruct**</span></span>

<span data-ttu-id="e637f-110">Die Größe der Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e637f-110">The size of the structure in bytes.</span></span> <span data-ttu-id="e637f-111">Der API-Aufruf aktualisiert dieses Feld, sodass der Aufrufer sicherstellen muss, dass dieser Wert sizeof (JET_INDEXLIST) entspricht.</span><span class="sxs-lookup"><span data-stu-id="e637f-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="e637f-112">**TableID**</span><span class="sxs-lookup"><span data-stu-id="e637f-112">**tableid**</span></span>

<span data-ttu-id="e637f-113">Der Tabellen Bezeichner der temporären Tabelle, die erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e637f-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="e637f-114">Es liegt in der Verantwortung des Aufrufers, die Tabelle zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e637f-114">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="e637f-115">**crecord**</span><span class="sxs-lookup"><span data-stu-id="e637f-115">**cRecord**</span></span>

<span data-ttu-id="e637f-116">Die Anzahl der Datensätze in der temporären Tabelle, die erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e637f-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="e637f-117">**columnidindexname**</span><span class="sxs-lookup"><span data-stu-id="e637f-117">**columnidindexname**</span></span>

<span data-ttu-id="e637f-118">Der Spalten Bezeichner des Index namens.</span><span class="sxs-lookup"><span data-stu-id="e637f-118">The column identifier of the name of the index.</span></span>

<span data-ttu-id="e637f-119">Diese Spalte ist eine [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-119">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="e637f-120">**columnidgrbitindex**</span><span class="sxs-lookup"><span data-stu-id="e637f-120">**columnidgrbitIndex**</span></span>

<span data-ttu-id="e637f-121">Der Spalten Bezeichner der *grbits* , die für den Index verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e637f-121">The column identifier of the *grbits* used on the index.</span></span> <span data-ttu-id="e637f-122">Eine Liste der gültigen Bits finden Sie unter [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="e637f-122">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for a list of valid bits.</span></span>

<span data-ttu-id="e637f-123">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-123">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="e637f-124">**columnidckey**</span><span class="sxs-lookup"><span data-stu-id="e637f-124">**columnidcKey**</span></span>

<span data-ttu-id="e637f-125">Der Spalten Bezeichner der Anzahl der Schlüssel im Index.</span><span class="sxs-lookup"><span data-stu-id="e637f-125">The column identifier of the number of keys in the index.</span></span>

<span data-ttu-id="e637f-126">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-126">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="e637f-127">**columnidcentry**</span><span class="sxs-lookup"><span data-stu-id="e637f-127">**columnidcEntry**</span></span>

<span data-ttu-id="e637f-128">Der Spalten Bezeichner der Anzahl der Einträge im Index.</span><span class="sxs-lookup"><span data-stu-id="e637f-128">The column identifier of the number of entries in the index.</span></span>

<span data-ttu-id="e637f-129">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-129">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="e637f-130">**columnidcpage**</span><span class="sxs-lookup"><span data-stu-id="e637f-130">**columnidcPage**</span></span>

<span data-ttu-id="e637f-131">Der Spalten Bezeichner der Anzahl der Seiten, die vom Index verwendet werden. Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-131">The column identifier of the number of pages the index uses.This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="e637f-132">**columnidccolumn**</span><span class="sxs-lookup"><span data-stu-id="e637f-132">**columnidcColumn**</span></span>

<span data-ttu-id="e637f-133">Der Spalten Bezeichner der Gesamtzahl der Spalten, die der Index umfasst.</span><span class="sxs-lookup"><span data-stu-id="e637f-133">The column identifier of the total number of columns that the index spans.</span></span>

<span data-ttu-id="e637f-134">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-134">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="e637f-135">**columnidicolumn**</span><span class="sxs-lookup"><span data-stu-id="e637f-135">**columnidiColumn**</span></span>

<span data-ttu-id="e637f-136">Der Spalten Bezeichner der Anzahl der Spalten im Index.</span><span class="sxs-lookup"><span data-stu-id="e637f-136">The column identifier of the number of the columns in the index.</span></span> <span data-ttu-id="e637f-137">Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="e637f-137">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="e637f-138">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-138">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e637f-139">Wert</span><span class="sxs-lookup"><span data-stu-id="e637f-139">Value</span></span></p></th>
<th><p><span data-ttu-id="e637f-140">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e637f-140">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e637f-141">cindexinfocols</span><span class="sxs-lookup"><span data-stu-id="e637f-141">cIndexInfoCols</span></span><br />
<span data-ttu-id="e637f-142">15</span><span class="sxs-lookup"><span data-stu-id="e637f-142">15</span></span></p></td>
<td><p><span data-ttu-id="e637f-143">Gibt an, dass 15 Spalten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e637f-143">Specifies that 15 columns are allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e637f-144">ccolumninfocols</span><span class="sxs-lookup"><span data-stu-id="e637f-144">cColumnInfoCols</span></span><br />
<span data-ttu-id="e637f-145">14</span><span class="sxs-lookup"><span data-stu-id="e637f-145">14</span></span></p></td>
<td><p><span data-ttu-id="e637f-146">Gibt an, dass 14 Spalten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e637f-146">Specifies that 14 columns are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e637f-147">cobjectinfocols</span><span class="sxs-lookup"><span data-stu-id="e637f-147">cObjectInfoCols</span></span><br />
<span data-ttu-id="e637f-148">9</span><span class="sxs-lookup"><span data-stu-id="e637f-148">9</span></span></p></td>
<td><p><span data-ttu-id="e637f-149">Gibt an, dass 9 Spalten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e637f-149">Specifies that 9 columns are allowed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e637f-150">**columnidcolumnid**</span><span class="sxs-lookup"><span data-stu-id="e637f-150">**columnidcolumnid**</span></span>

<span data-ttu-id="e637f-151">Der Spalten Bezeichner der indizierten Spalte. Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="e637f-151">The column identifier of the column that is indexed.For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="e637f-152">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-152">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="e637f-153">**columnidcolyp**</span><span class="sxs-lookup"><span data-stu-id="e637f-153">**columnidcoltyp**</span></span>

<span data-ttu-id="e637f-154">Der Spalten Bezeichner des coltyps der Spalte, der indiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e637f-154">The column identifier of the coltyp of the column which is indexed.</span></span> <span data-ttu-id="e637f-155">Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="e637f-155">For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="e637f-156">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-156">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="e637f-157">**columnidcountry**</span><span class="sxs-lookup"><span data-stu-id="e637f-157">**columnidCountry**</span></span>

<span data-ttu-id="e637f-158">Der Spalten Bezeichner des Ländercodes der indizierten Spalte.</span><span class="sxs-lookup"><span data-stu-id="e637f-158">The column identifier of the country code of the column that is indexed.</span></span> <span data-ttu-id="e637f-159">Der Ländercode ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="e637f-159">The country code is deprecated.</span></span>

<span data-ttu-id="e637f-160">Diese Spalte ist eine [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-160">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="e637f-161">**columnidlangid**</span><span class="sxs-lookup"><span data-stu-id="e637f-161">**columnidLangid**</span></span>

<span data-ttu-id="e637f-162">Der Spalten Bezeichner des sprach Bezeichners (LCID), unter dem der Index erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e637f-162">The column identifier of the language identifier (LCID) under which the index was created.</span></span> <span data-ttu-id="e637f-163">Weitere Informationen finden Sie unter [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-163">For more information, see [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<span data-ttu-id="e637f-164">Diese Spalte ist eine [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-164">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="e637f-165">**columnidcp**</span><span class="sxs-lookup"><span data-stu-id="e637f-165">**columnidCp**</span></span>

<span data-ttu-id="e637f-166">Der Spalten Bezeichner der Codepage, unter der der Index erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e637f-166">The column identifier of the code page under which the index was created.</span></span> <span data-ttu-id="e637f-167">Weitere Informationen finden Sie unter [JET_COLUMNCREATE](./jet-columncreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-167">For more information, see [JET_COLUMNCREATE](./jet-columncreate-structure.md).</span></span>

<span data-ttu-id="e637f-168">Diese Spalte ist eine [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-168">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="e637f-169">**columnidcollate**</span><span class="sxs-lookup"><span data-stu-id="e637f-169">**columnidCollate**</span></span>

<span data-ttu-id="e637f-170">Der Spalten Bezeichner der Sortierungs Sequenz, unter der der Index erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e637f-170">The column identifier of the collation sequence under which the index was created.</span></span> <span data-ttu-id="e637f-171">Die Sortierungs Sequenz ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="e637f-171">The collation sequence is deprecated.</span></span>

<span data-ttu-id="e637f-172">Diese Spalte ist eine [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-172">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="e637f-173">**columnidgrbitcolumn**</span><span class="sxs-lookup"><span data-stu-id="e637f-173">**columnidgrbitColumn**</span></span>

<span data-ttu-id="e637f-174">Der Spalten Bezeichner der *grbits* , die auf die Reihenfolge der Spalte im Index angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e637f-174">The column identifier of the *grbits* that apply to the order of the column in the index.</span></span>

<span data-ttu-id="e637f-175">Die Daten für diese Spalte können als JET_bitKeyAscending oder JET_bitKeyDescending angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="e637f-175">The data for this column can be ordered as JET_bitKeyAscending or JET_bitKeyDescending.</span></span> <span data-ttu-id="e637f-176">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-176">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="e637f-177">Ein Index, der als "-Column1 \\ 0 + Column2 \\ 0" definiert ist, hat z. b. JET_bitKeyDescending für "Column1" und JET_bitKeyAscending für "Column2".</span><span class="sxs-lookup"><span data-stu-id="e637f-177">For example, an index defined as "-column1\\0+column2\\0" will have JET_bitKeyDescending for "column1", and JET_bitKeyAscending for "column2".</span></span>

<span data-ttu-id="e637f-178">Die folgenden Optionen sind für diesen Member gültig.</span><span class="sxs-lookup"><span data-stu-id="e637f-178">The following options are valid for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e637f-179">Wert</span><span class="sxs-lookup"><span data-stu-id="e637f-179">Value</span></span></p></th>
<th><p><span data-ttu-id="e637f-180">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e637f-180">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e637f-181">JET_bitKeyAscending</span><span class="sxs-lookup"><span data-stu-id="e637f-181">JET_bitKeyAscending</span></span></p></td>
<td><p><span data-ttu-id="e637f-182">Ein Index Segment in aufsteigender Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="e637f-182">An index segment in ascending order.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e637f-183">JET_bitKeyDescending</span><span class="sxs-lookup"><span data-stu-id="e637f-183">JET_bitKeyDescending</span></span></p></td>
<td><p><span data-ttu-id="e637f-184">Ein Index Segment in absteigender Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="e637f-184">An index segment in descending order.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e637f-185">**columnidcolumnname**</span><span class="sxs-lookup"><span data-stu-id="e637f-185">**columnidcolumnname**</span></span>

<span data-ttu-id="e637f-186">Der Spalten Bezeichner des Spaltennamens.</span><span class="sxs-lookup"><span data-stu-id="e637f-186">The column identifier of the name of the column.</span></span>

<span data-ttu-id="e637f-187">Diese Spalte ist eine [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-187">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="e637f-188">**columnidlcmapflags**</span><span class="sxs-lookup"><span data-stu-id="e637f-188">**columnidLCMapFlags**</span></span>

<span data-ttu-id="e637f-189">Der Spalten Bezeichner der Flags, die verwendet werden, um den Index zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e637f-189">The column identifier of the flags that are used to create the index.</span></span> <span data-ttu-id="e637f-190">Weitere Informationen finden Sie im Abschnitt **dwmapflags** der [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-190">For more information, see the **dwMapFlags** section of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).</span></span>

<span data-ttu-id="e637f-191">Diese Spalte ist eine [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="e637f-191">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="e637f-192">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e637f-192">Remarks</span></span>

<span data-ttu-id="e637f-193">Jede Zeile in der temporären Tabelle entspricht einer Spalte in einem bestimmten Index.</span><span class="sxs-lookup"><span data-stu-id="e637f-193">Each row in the temporary table corresponds to a column in a particular index.</span></span>

<span data-ttu-id="e637f-194">Der Index "+ A \\ 0 + B \\ 0 + C \\ 0 + D \\ 0 + E 0" ist z. b. \\ größer als fünf Spalten, und es werden fünf Zeilen in der temporären Tabelle belegt.</span><span class="sxs-lookup"><span data-stu-id="e637f-194">For example, the index "+A\\0+B\\0+C\\0+D\\0+E\\0" is more than five columns, and it will occupy five rows in the temporary table.</span></span> <span data-ttu-id="e637f-195">Jede dieser fünf Zeilen hat den Wert 5 in der Spalte, die von der Spalte "ColumnID" identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e637f-195">Each of these five rows will have a value of 5 in the column that is identified by columnid column.</span></span> <span data-ttu-id="e637f-196">Jede Zeile weist jedoch einen anderen Wert für die Spalten Spalte auf (von 0 bis 4).</span><span class="sxs-lookup"><span data-stu-id="e637f-196">But each row will have a different value for columnid column, ranging from 0 to 4.</span></span>

<span data-ttu-id="e637f-197">Die Anzahl der Schlüssel in einem bestimmten Index entspricht der Anzahl der eindeutigen Werte, die ein Aufrufer suchen und eine genaue Übereinstimmung erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="e637f-197">The number of keys in a particular index corresponds to the number of unique values for which a caller can seek and get an exact match.</span></span> <span data-ttu-id="e637f-198">Die Anzahl der Einträge ist die Anzahl der Zeilen, denen ein Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="e637f-198">The number of entries is the number of rows that an index matches.</span></span> <span data-ttu-id="e637f-199">Wenn ein Index eine Eindeutigkeits Einschränkung aufweist, entspricht die Anzahl der Schlüssel der Anzahl der Einträge.</span><span class="sxs-lookup"><span data-stu-id="e637f-199">If an index has a uniqueness constraint, then the number of keys is equal to the number of entries.</span></span> <span data-ttu-id="e637f-200">Wenn eine Tabelle z. b. die folgenden Informationen enthält und ein Index für die Spalte mit dem Namen "Key" erstellt wird, gibt es drei Schlüssel (100, 200 und 500), aber es gibt vier Einträge ("This", "is", "an" und "example").</span><span class="sxs-lookup"><span data-stu-id="e637f-200">For example, if a table contains the following information and an index is created over the column named "key", then there are three keys (100, 200, and 500), but there are four entries ("this", "is", "an", and "example").</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e637f-201">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e637f-201">Key</span></span></p></th>
<th><p><span data-ttu-id="e637f-202">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e637f-202">Entry</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e637f-203">100</span><span class="sxs-lookup"><span data-stu-id="e637f-203">100</span></span></p></td>
<td><p><span data-ttu-id="e637f-204">&quot;this&quot;</span><span class="sxs-lookup"><span data-stu-id="e637f-204">&quot;this&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e637f-205">100</span><span class="sxs-lookup"><span data-stu-id="e637f-205">100</span></span></p></td>
<td><p><span data-ttu-id="e637f-206">&quot;is&quot;</span><span class="sxs-lookup"><span data-stu-id="e637f-206">&quot;is&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e637f-207">200</span><span class="sxs-lookup"><span data-stu-id="e637f-207">200</span></span></p></td>
<td><p><span data-ttu-id="e637f-208">&quot;halbe&quot;</span><span class="sxs-lookup"><span data-stu-id="e637f-208">&quot;an&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e637f-209">500</span><span class="sxs-lookup"><span data-stu-id="e637f-209">500</span></span></p></td>
<td><p><span data-ttu-id="e637f-210">&quot;example&quot;</span><span class="sxs-lookup"><span data-stu-id="e637f-210">&quot;example&quot;</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="e637f-211">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e637f-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e637f-212"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e637f-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e637f-213">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e637f-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e637f-214"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e637f-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e637f-215">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e637f-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e637f-216"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e637f-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e637f-217">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="e637f-217">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e637f-218">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e637f-218">See Also</span></span>

[<span data-ttu-id="e637f-219">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="e637f-219">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="e637f-220">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="e637f-220">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="e637f-221">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e637f-221">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="e637f-222">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e637f-222">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e637f-223">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e637f-223">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e637f-224">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="e637f-224">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="e637f-225">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e637f-225">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e637f-226">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e637f-226">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e637f-227">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="e637f-227">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="e637f-228">Jetgetindexinfo</span><span class="sxs-lookup"><span data-stu-id="e637f-228">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="e637f-229">Jetgettableindexinfo</span><span class="sxs-lookup"><span data-stu-id="e637f-229">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
