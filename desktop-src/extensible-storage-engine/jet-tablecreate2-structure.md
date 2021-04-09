---
description: 'Weitere Informationen finden Sie hier: JET_TABLECREATE2 Struktur'
title: JET_TABLECREATE2-Struktur
TOCTitle: JET_TABLECREATE2 Structure
ms:assetid: 2029e684-0d10-44e7-8033-d9cdbdffd7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269203(v=EXCHG.10)
ms:contentKeyID: 32765506
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
ms.openlocfilehash: d7ce983d393954c0d82f0d4e43108ff845d31571
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869136"
---
# <a name="jet_tablecreate2-structure"></a><span data-ttu-id="73627-103">JET_TABLECREATE2-Struktur</span><span class="sxs-lookup"><span data-stu-id="73627-103">JET_TABLECREATE2 Structure</span></span>


<span data-ttu-id="73627-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="73627-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tablecreate2-structure"></a><span data-ttu-id="73627-105">JET_TABLECREATE2-Struktur</span><span class="sxs-lookup"><span data-stu-id="73627-105">JET_TABLECREATE2 Structure</span></span>

<span data-ttu-id="73627-106">Die **JET_TABLECREATE2** Struktur enthält die Informationen, die erforderlich sind, um eine Tabelle zu erstellen, die mit Spalten und Indizes in einer ESE-Datenbank aufgefüllt ist, und die eine Rückruffunktion festlegt.</span><span class="sxs-lookup"><span data-stu-id="73627-106">The **JET_TABLECREATE2** structure contains the information that is needed to create a table populated with columns and indexes in an ESE database, and that designates a callback function.</span></span> <span data-ttu-id="73627-107">Die **JET_TABLECREATE2** Struktur wird von [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="73627-107">The **JET_TABLECREATE2** structure is used by [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span>

<span data-ttu-id="73627-108">**Windows XP:** Die **JET_TABLECREATE2** Struktur wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="73627-108">**Windows XP:** The **JET_TABLECREATE2** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tagJET_TABLECREATE2 {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      tchar* szCallback;
      JET_CBTYP cbtyp;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE2;
```

### <a name="members"></a><span data-ttu-id="73627-109">Member</span><span class="sxs-lookup"><span data-stu-id="73627-109">Members</span></span>

<span data-ttu-id="73627-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="73627-110">**cbStruct**</span></span>

<span data-ttu-id="73627-111">Die Größe dieser-Struktur in Bytes (für zukünftige Erweiterungen).</span><span class="sxs-lookup"><span data-stu-id="73627-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="73627-112">Er muss auf sizeof (JET_TABLECREATE2) in Bytes festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="73627-112">It must be set to sizeof( JET_TABLECREATE2 ) in bytes.</span></span>

<span data-ttu-id="73627-113">**sztablename**</span><span class="sxs-lookup"><span data-stu-id="73627-113">**szTableName**</span></span>

<span data-ttu-id="73627-114">Der Name der zu erstellenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="73627-114">The name of table to create.</span></span>

<span data-ttu-id="73627-115">Der Name muss die folgenden Bedingungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="73627-115">The name must use meet the following conditions:</span></span>

  - <span data-ttu-id="73627-116">Ein Wert, der kleiner als JET_cbNameMost ist, ohne den abschließenden NULL-Wert.</span><span class="sxs-lookup"><span data-stu-id="73627-116">Have a value less than JET_cbNameMost, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="73627-117">Besteht aus folgendem Zeichensatz: 0 bis 9, A bis Z, A bis Z und alle anderen Interpunktions Punkte außer Ausrufezeichen ( \! ), Komma (,), öffnende eckige Klammer ( \[ ) und schließende Klammer ( \] ), d. h. ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c und 0x5d bis 0x7F.</span><span class="sxs-lookup"><span data-stu-id="73627-117">Consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="73627-118">Beginnen Sie nicht mit einem Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="73627-118">Not begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="73627-119">Besteht aus mindestens einem Zeichen, das kein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="73627-119">Consist of at least one non-space character.</span></span>

<span data-ttu-id="73627-120">**sztemplatetablename**</span><span class="sxs-lookup"><span data-stu-id="73627-120">**szTemplateTableName**</span></span>

<span data-ttu-id="73627-121">Der Name einer bereits vorhandenen Tabelle, aus der die Basis-DDL (Data Definition Language) geerbt werden soll.</span><span class="sxs-lookup"><span data-stu-id="73627-121">The name of an already-existing table from which to inherit base DDL (Data Definition Language).</span></span> <span data-ttu-id="73627-122">Die Verwendung einer Vorlagen Tabelle ermöglicht eine einfache Erstellung vieler Tabellen mit identischen Spalten und Indizes.</span><span class="sxs-lookup"><span data-stu-id="73627-122">Using a template table allows easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="73627-123">**ulpages**</span><span class="sxs-lookup"><span data-stu-id="73627-123">**ulPages**</span></span>

<span data-ttu-id="73627-124">Die anfängliche Anzahl von Datenbankseiten, die für die Tabelle zuzuordnen sind.</span><span class="sxs-lookup"><span data-stu-id="73627-124">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="73627-125">Wenn eine Zahl größer als 1 angegeben wird, kann die Fragmentierung reduziert werden, wenn viele Zeilen in diese Tabelle eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="73627-125">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="73627-126">**uldensity**</span><span class="sxs-lookup"><span data-stu-id="73627-126">**ulDensity**</span></span>

<span data-ttu-id="73627-127">Die Tabellen Dichte in Prozent.</span><span class="sxs-lookup"><span data-stu-id="73627-127">The table density, in percentage points.</span></span> <span data-ttu-id="73627-128">Die Zahl muss entweder 0 oder im Bereich von 20 bis 100 sein.</span><span class="sxs-lookup"><span data-stu-id="73627-128">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="73627-129">Das übergeben von 0 bedeutet, dass der Standardwert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="73627-129">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="73627-130">Der Standardwert ist 80.</span><span class="sxs-lookup"><span data-stu-id="73627-130">The default is 80.</span></span>

<span data-ttu-id="73627-131">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="73627-131">**rgcolumncreate**</span></span>

<span data-ttu-id="73627-132">Ein Array von [JET_COLUMNCREATE](./jet-columncreate-structure.md) Strukturen, die jeweils einer Spalte entsprechen, die in der neuen Tabelle erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="73627-132">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="73627-133">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="73627-133">**cColumns**</span></span>

<span data-ttu-id="73627-134">die Anzahl der [JET_COLUMNCREATE](./jet-columncreate-structure.md) Elemente in **rgcolumncreate**.</span><span class="sxs-lookup"><span data-stu-id="73627-134">the number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in **rgcolumncreate**.</span></span>

<span data-ttu-id="73627-135">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="73627-135">**rgindexcreate**</span></span>

<span data-ttu-id="73627-136">Ein Array von [JET_INDEXCREATE](./jet-indexcreate-structure.md) Strukturen, von denen jede einem Index entspricht, der in der neuen Tabelle erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="73627-136">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="73627-137">**cindexes**</span><span class="sxs-lookup"><span data-stu-id="73627-137">**cIndexes**</span></span>

<span data-ttu-id="73627-138">Die Anzahl der [JET_INDEXCREATE](./jet-indexcreate-structure.md) Elemente in **rgindexcreate**.</span><span class="sxs-lookup"><span data-stu-id="73627-138">The number of [JET_INDEXCREATE](./jet-indexcreate-structure.md) elements in **rgindexcreate**.</span></span>

<span data-ttu-id="73627-139">**szcallback**</span><span class="sxs-lookup"><span data-stu-id="73627-139">**szCallback**</span></span>

<span data-ttu-id="73627-140">Die Funktion, die während bestimmter Ereignisse aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="73627-140">The function that gets called during certain events.</span></span> <span data-ttu-id="73627-141">**cbyp** bestimmt, wann die Rückruffunktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="73627-141">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="73627-142">Das Format von **szcallback** muss "Module \! Function" lauten, – z. b. "Alpha \! Beta" bezieht sich auf die Beta Funktion im Modul "Alpha".</span><span class="sxs-lookup"><span data-stu-id="73627-142">The format of **szCallback** must be "module\!function"—for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span> <span data-ttu-id="73627-143">Der Prototyp der Funktion muss [JET_CALLBACK](./jet-callback-callback-function.md)entsprechen.</span><span class="sxs-lookup"><span data-stu-id="73627-143">The prototype of the function must match [JET_CALLBACK](./jet-callback-callback-function.md).</span></span> <span data-ttu-id="73627-144">Weitere Informationen finden Sie unter [JET_CALLBACK](./jet-callback-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="73627-144">For more information, see [JET_CALLBACK](./jet-callback-callback-function.md).</span></span>

<span data-ttu-id="73627-145">**cbyp**</span><span class="sxs-lookup"><span data-stu-id="73627-145">**cbtyp**</span></span>

<span data-ttu-id="73627-146">Beschreibt den Typ der durch **szcallback** bezeichneten Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="73627-146">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="73627-147">Weitere Informationen finden Sie unter [JET_CBTYP](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="73627-147">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span> <span data-ttu-id="73627-148">Dieses Bitfeld besteht aus einem oder mehreren der folgenden Bits.</span><span class="sxs-lookup"><span data-stu-id="73627-148">This bitfield is composed of one or more of the following bits.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73627-149">Wert</span><span class="sxs-lookup"><span data-stu-id="73627-149">Value</span></span></p></th>
<th><p><span data-ttu-id="73627-150">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="73627-150">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73627-151">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="73627-151">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="73627-152">Die Rückruffunktion wird aufgerufen, wenn eine Spalte, die abgeschlossen werden kann, auf NULL gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="73627-152">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73627-153">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="73627-153">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="73627-154">Die Rückruffunktion wird vor dem Einfügen von Datensätzen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="73627-154">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73627-155">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="73627-155">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="73627-156">Die Rückruffunktion wird aufgerufen, sobald die Datenbank-Engine das Einfügen eines Datensatzes abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="73627-156">The callback function will be called once the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73627-157">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="73627-157">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="73627-158">Die Rückruffunktion wird vor der Änderung eines Datensatzes aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="73627-158">The callback function will be called prior to modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73627-159">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="73627-159">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="73627-160">Die Rückruffunktion wird nach Abschluss der Änderung eines Datensatzes aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="73627-160">The callback function will be called after finishing modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73627-161">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="73627-161">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="73627-162">Die Rückruffunktion wird vor dem Löschen eines Datensatzes aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="73627-162">The callback function will be called prior to deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73627-163">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="73627-163">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="73627-164">Die Rückruffunktion wird aufgerufen, nachdem ein Datensatz gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="73627-164">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73627-165">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="73627-165">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="73627-166">Die Rückruffunktion wird aufgerufen, um einen benutzerdefinierten Standardwert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="73627-166">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73627-167">JET_cbtypOnlineDefragCompleted</span><span class="sxs-lookup"><span data-stu-id="73627-167">JET_cbtypOnlineDefragCompleted</span></span></p></td>
<td><p><span data-ttu-id="73627-168">Die Rückruffunktion wird aufgerufen, nachdem ein Aufruf von <a href="gg294095(v=exchg.10).md">JetDefragment2</a> abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="73627-168">The callback function will be called after a call to <a href="gg294095(v=exchg.10).md">JetDefragment2</a> has completed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73627-169">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="73627-169">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="73627-170">Die Rückruffunktion wird aufgerufen, wenn der lokale Speicher, der einem Cursor zugeordnet ist, freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="73627-170">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73627-171">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="73627-171">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="73627-172">Die Rückruffunktion wird aufgerufen, wenn der lokale Speicher, der einer Tabelle zugeordnet ist, freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="73627-172">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73627-173">**grbit**</span><span class="sxs-lookup"><span data-stu-id="73627-173">**grbit**</span></span>

<span data-ttu-id="73627-174">Eine Gruppe von Bits, die die Optionen für diesen-Befehl enthalten, die 0 (null) oder mehrere der folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="73627-174">A group of bits that contain the options for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73627-175">Wert</span><span class="sxs-lookup"><span data-stu-id="73627-175">Value</span></span></p></th>
<th><p><span data-ttu-id="73627-176">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="73627-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73627-177">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="73627-177">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="73627-178">Das Festlegen von JET_bitTableCreateFixedDDL verhindert DDL-Vorgänge für die Tabelle (z. b. das Hinzufügen oder Entfernen von Spalten)</span><span class="sxs-lookup"><span data-stu-id="73627-178">Setting JET_bitTableCreateFixedDDL prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73627-179">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="73627-179">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="73627-180">Das Festlegen von JET_bitTableCreateTemplateTable bewirkt, dass die Tabelle eine Vorlagen Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="73627-180">Setting JET_bitTableCreateTemplateTable causes the table to be a template table.</span></span> <span data-ttu-id="73627-181">In neuen Tabellen kann dann der Name dieser Tabelle als Vorlagen Tabelle angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="73627-181">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="73627-182">Das Festlegen JET_bitTableCreateTemplateTable impliziert JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="73627-182">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73627-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="73627-183">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="73627-184">Muss in Verbindung mit JET_bitTableCreateTemplateTable verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73627-184">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="73627-185">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="73627-185">Deprecated.</span></span> <span data-ttu-id="73627-186">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="73627-186">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73627-187">**TableID**</span><span class="sxs-lookup"><span data-stu-id="73627-187">**tableid**</span></span>

<span data-ttu-id="73627-188">Ein Ausgabefeld, das den [JET_TABLEID](./jet-tableid.md) der neuen Tabelle enthält, wenn der API-Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73627-188">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="73627-189">Wenn der API-Befehl fehlschlägt, ist der Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="73627-189">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="73627-190">**erstellt**</span><span class="sxs-lookup"><span data-stu-id="73627-190">**cCreated**</span></span>

<span data-ttu-id="73627-191">Ein Ausgabefeld, das die Anzahl der-Objekte enthält, die erstellt werden, wenn der API-Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73627-191">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="73627-192">Wenn der API-Befehl fehlschlägt, ist der Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="73627-192">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="73627-193">Die Anzahl der erstellten Objekte entspricht der Summe der Spalten, Tabellen und Indizes, die erfolgreich erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="73627-193">The count of objects that is created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="73627-194">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73627-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73627-195"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="73627-195"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="73627-196">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="73627-196">Requires Windows  Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73627-197"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="73627-197"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="73627-198">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="73627-198">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73627-199"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="73627-199"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="73627-200">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="73627-200">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73627-201"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="73627-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="73627-202">Wird als <strong>JET_TABLECREATE2_W</strong> (Unicode) und <strong>JET_TABLECREATE2_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="73627-202">Implemented as <strong>JET_TABLECREATE2_W</strong> (Unicode) and <strong>JET_TABLECREATE2_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="73627-203">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="73627-203">See Also</span></span>

[<span data-ttu-id="73627-204">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="73627-204">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="73627-205">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="73627-205">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="73627-206">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="73627-206">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="73627-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="73627-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="73627-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="73627-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="73627-209">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="73627-209">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="73627-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="73627-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="73627-211">Jetkreatetable</span><span class="sxs-lookup"><span data-stu-id="73627-211">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="73627-212">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="73627-212">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="73627-213">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="73627-213">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="73627-214">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="73627-214">JetDefragment2</span></span>](./jetdefragment2-function.md)
