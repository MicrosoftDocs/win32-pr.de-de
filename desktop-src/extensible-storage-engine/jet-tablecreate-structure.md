---
description: 'Weitere Informationen finden Sie hier: JET_TABLECREATE Struktur'
title: JET_TABLECREATE-Struktur
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
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
ms.openlocfilehash: f96b73daaf446023a7fe3a5729dcb1c90b5f14e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128184"
---
# <a name="jet_tablecreate-structure"></a><span data-ttu-id="4f8d4-103">JET_TABLECREATE-Struktur</span><span class="sxs-lookup"><span data-stu-id="4f8d4-103">JET_TABLECREATE Structure</span></span>


<span data-ttu-id="4f8d4-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4f8d4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate-structure"></a><span data-ttu-id="4f8d4-105">JET_TABLECREATE-Struktur</span><span class="sxs-lookup"><span data-stu-id="4f8d4-105">JET_TABLECREATE Structure</span></span>

<span data-ttu-id="4f8d4-106">Die **JET_TABLECREATE** Struktur enthält die Informationen, die erforderlich sind, um eine Tabelle zu erstellen, die mit Spalten und Indizes in einer ESE-Datenbank aufgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-106">The **JET_TABLECREATE** structure contains the information that is necessary to create a table populated with columns and indexes in an ESE database.</span></span> <span data-ttu-id="4f8d4-107">Die **JET_TABLECREATE** Struktur wird von [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-107">The **JET_TABLECREATE** structure is used by [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)</span></span>

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a><span data-ttu-id="4f8d4-108">Member</span><span class="sxs-lookup"><span data-stu-id="4f8d4-108">Members</span></span>

<span data-ttu-id="4f8d4-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="4f8d4-109">**cbStruct**</span></span>

<span data-ttu-id="4f8d4-110">Die Größe dieser-Struktur in Bytes (für zukünftige Erweiterungen).</span><span class="sxs-lookup"><span data-stu-id="4f8d4-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="4f8d4-111">Er muss auf sizeof (JET_TABLECREATE) in Bytes festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-111">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="4f8d4-112">**sztablename**</span><span class="sxs-lookup"><span data-stu-id="4f8d4-112">**szTableName**</span></span>

<span data-ttu-id="4f8d4-113">Der Name der zu erstellenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-113">The name of the table to create.</span></span>

<span data-ttu-id="4f8d4-114">Der Name muss die folgenden Bedingungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="4f8d4-114">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="4f8d4-115">Ein Wert, der kleiner als JET_cbNameMost ist, ohne den abschließenden NULL-Wert.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-115">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="4f8d4-116">Besteht aus folgendem Zeichensatz: 0 bis 9, A bis Z, A bis Z und alle anderen Interpunktions Punkte außer Ausrufezeichen ( \! ), Komma (,), öffnende eckige Klammer ( \[ ) und schließende Klammer ( \] ), d. h. ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c und 0x5d bis 0x7F.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-116">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="4f8d4-117">Beginnen Sie nicht mit einem Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-117">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="4f8d4-118">Besteht aus mindestens einem Zeichen, das kein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-118">Consist of at least one non-space character.</span></span>

<span data-ttu-id="4f8d4-119">**sztemplatetablename**</span><span class="sxs-lookup"><span data-stu-id="4f8d4-119">**szTemplateTableName**</span></span>

<span data-ttu-id="4f8d4-120">Der Name einer bereits vorhandenen Tabelle, aus der die Basis-DDL (Data Definition Language) geerbt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-120">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="4f8d4-121">Die Verwendung einer Vorlagen Tabelle ermöglicht die einfache Erstellung von vielen Tabellen mit identischen Spalten und Indizes.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="4f8d4-122">**ulpages**</span><span class="sxs-lookup"><span data-stu-id="4f8d4-122">**ulPages**</span></span>

<span data-ttu-id="4f8d4-123">Die anfängliche Anzahl von Datenbankseiten, die für die Tabelle zuzuordnen sind.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="4f8d4-124">Wenn eine Zahl größer als 1 angegeben wird, kann die Fragmentierung reduziert werden, wenn viele Zeilen in diese Tabelle eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="4f8d4-125">**uldensity**</span><span class="sxs-lookup"><span data-stu-id="4f8d4-125">**ulDensity**</span></span>

<span data-ttu-id="4f8d4-126">Die Tabellen Dichte in Prozent.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-126">The table density, in percentage points.</span></span> <span data-ttu-id="4f8d4-127">Die Zahl muss entweder 0 oder im Bereich von 20 bis 100 sein.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="4f8d4-128">Das übergeben von 0 bedeutet, dass der Standardwert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="4f8d4-129">Der Standardwert ist 80.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-129">The default is 80.</span></span>

<span data-ttu-id="4f8d4-130">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="4f8d4-130">**rgcolumncreate**</span></span>

<span data-ttu-id="4f8d4-131">Ein Array von [JET_COLUMNCREATE](./jet-columncreate-structure.md) Strukturen, die jeweils einer Spalte entsprechen, die in der neuen Tabelle erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="4f8d4-132">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="4f8d4-132">**cColumns**</span></span>

<span data-ttu-id="4f8d4-133">Die Anzahl der [JET_COLUMNCREATE](./jet-columncreate-structure.md) Elemente in **rgcolumncreate**.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="4f8d4-134">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="4f8d4-134">**rgindexcreate**</span></span>

<span data-ttu-id="4f8d4-135">Ein Array von [JET_INDEXCREATE](./jet-indexcreate-structure.md) Strukturen, von denen jede einem Index entspricht, der in der neuen Tabelle erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-135">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="4f8d4-136">**cindexes**</span><span class="sxs-lookup"><span data-stu-id="4f8d4-136">**cIndexes**</span></span>

<span data-ttu-id="4f8d4-137">Die Anzahl der [JET_INDEXCREATE](./jet-indexcreate-structure.md) Elemente in **rgindexcreate**.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-137">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="4f8d4-138">**grbit**</span><span class="sxs-lookup"><span data-stu-id="4f8d4-138">**grbit**</span></span>

<span data-ttu-id="4f8d4-139">Eine Gruppe von Bits, die die Optionen für diesen-Befehl enthalten, die 0 (null) oder mehrere der folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-139">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f8d4-140">Wert</span><span class="sxs-lookup"><span data-stu-id="4f8d4-140">Value</span></span></p></th>
<th><p><span data-ttu-id="4f8d4-141">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4f8d4-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f8d4-142">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="4f8d4-142">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="4f8d4-143">Das Festlegen von JET_bitTableCreateFixedDDL verhindert DDL-Vorgänge für die Tabelle (z. b. das Hinzufügen oder Entfernen von Spalten)</span><span class="sxs-lookup"><span data-stu-id="4f8d4-143">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f8d4-144">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="4f8d4-144">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="4f8d4-145">Das Festlegen von JET_bitTableCreateTemplateTable bewirkt, dass die Tabelle eine Vorlagen Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-145">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="4f8d4-146">In neuen Tabellen kann dann der Name dieser Tabelle als Vorlagen Tabelle angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-146">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="4f8d4-147">Das Festlegen JET_bitTableCreateTemplateTable impliziert JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-147">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f8d4-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="4f8d4-148">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="4f8d4-149">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-149">Deprecated.</span></span> <span data-ttu-id="4f8d4-150">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-150">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4f8d4-151">**TableID**</span><span class="sxs-lookup"><span data-stu-id="4f8d4-151">**tableid**</span></span>

<span data-ttu-id="4f8d4-152">Ein Ausgabefeld, das den [JET_TABLEID](./jet-tableid.md) der neuen Tabelle enthält, wenn der API-Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-152">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="4f8d4-153">Wenn der API-Befehl fehlschlägt, ist der Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-153">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="4f8d4-154">**erstellt**</span><span class="sxs-lookup"><span data-stu-id="4f8d4-154">**cCreated**</span></span>

<span data-ttu-id="4f8d4-155">Ein Ausgabefeld, das die Anzahl der-Objekte enthält, die beim erfolgreichen API-Rückruf erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-155">An output field that contains the count of objects created if the API call succeeds.</span></span> <span data-ttu-id="4f8d4-156">Wenn der API-Befehl fehlschlägt, ist der Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-156">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="4f8d4-157">Die Anzahl der Objekte, die erstellt werden, entspricht der Summe der Spalten, Tabellen und Indizes, die erfolgreich erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-157">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="4f8d4-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f8d4-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f8d4-159"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="4f8d4-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4f8d4-160">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f8d4-161"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4f8d4-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4f8d4-162">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f8d4-163"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4f8d4-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4f8d4-164">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f8d4-165"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4f8d4-165"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4f8d4-166">Wird als <strong>JET_TABLECREATE_W</strong> (Unicode) und <strong>JET_TABLECREATE_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="4f8d4-166">Implemented as <strong>JET_TABLECREATE_W</strong> (Unicode) and <strong>JET_TABLECREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4f8d4-167">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4f8d4-167">See Also</span></span>

[<span data-ttu-id="4f8d4-168">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="4f8d4-168">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="4f8d4-169">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="4f8d4-169">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="4f8d4-170">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="4f8d4-170">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="4f8d4-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4f8d4-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4f8d4-172">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4f8d4-172">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4f8d4-173">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4f8d4-173">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4f8d4-174">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="4f8d4-174">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="4f8d4-175">Jetkreatetable</span><span class="sxs-lookup"><span data-stu-id="4f8d4-175">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="4f8d4-176">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="4f8d4-176">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="4f8d4-177">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="4f8d4-177">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
