---
description: 'Weitere Informationen finden Sie hier: JET_TABLECREATE3 Struktur'
title: JET_TABLECREATE3-Struktur
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 587649b592f2b0d213a481c3bfbecc723240e486
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353013"
---
# <a name="jet_tablecreate3-structure"></a><span data-ttu-id="90b79-103">JET_TABLECREATE3-Struktur</span><span class="sxs-lookup"><span data-stu-id="90b79-103">JET_TABLECREATE3 Structure</span></span>


<span data-ttu-id="90b79-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="90b79-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="90b79-105">Die **JET_TABLECREATE3** Struktur enthält die Informationen, die erforderlich sind, um eine Tabelle zu erstellen, die mit Spalten und Indizes in einer ESE-Datenbank (Extensible Storage Engine) gefüllt ist und die eine Rückruffunktion festlegt.</span><span class="sxs-lookup"><span data-stu-id="90b79-105">The **JET_TABLECREATE3** structure contains the information that is needed to create a table populated with columns and indexes in an Extensible Storage Engine (ESE) database, and that designates a callback function.</span></span> <span data-ttu-id="90b79-106">Die **JET_TABLECREATE3** -Struktur wird von der [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="90b79-106">The **JET_TABLECREATE3** structure is used by the [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) function.</span></span>

<span data-ttu-id="90b79-107">Die **JET_TABLECREATE3** Struktur wurde mit dem Betriebssystem Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="90b79-107">The **JET_TABLECREATE3** structure was introduced in the Windows 7 operating system.</span></span>

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a><span data-ttu-id="90b79-108">Member</span><span class="sxs-lookup"><span data-stu-id="90b79-108">Members</span></span>

<span data-ttu-id="90b79-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="90b79-109">**cbStruct**</span></span>

<span data-ttu-id="90b79-110">Die Größe dieser-Struktur in Bytes (für zukünftige Erweiterungen).</span><span class="sxs-lookup"><span data-stu-id="90b79-110">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="90b79-111">Er muss auf sizeof (JET_TABLECREATE3) in Bytes festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="90b79-111">It must be set to sizeof( JET_TABLECREATE3 ) in bytes.</span></span>

<span data-ttu-id="90b79-112">**sztablename**</span><span class="sxs-lookup"><span data-stu-id="90b79-112">**szTableName**</span></span>

<span data-ttu-id="90b79-113">Der Name der zu erstellenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="90b79-113">The name of the table to create.</span></span>

<span data-ttu-id="90b79-114">Der Name muss die folgenden Bedingungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="90b79-114">The name must meet the following conditions:</span></span>

  - <span data-ttu-id="90b79-115">Er muss einen Wert aufweisen, der kleiner als JET_cbNameMost ist, ohne den abschließenden NULL-Wert.</span><span class="sxs-lookup"><span data-stu-id="90b79-115">It must have a value that is less than JET_cbNameMost, not including the terminating null.</span></span>

  - <span data-ttu-id="90b79-116">Sie muss aus folgenden Zeichen bestehen: 0 bis 9, A bis Z, A bis Z und alle anderen Interpunktions Punkte außer Ausrufezeichen ( \! ), Komma (,), öffnende eckige Klammer ( \[ ) und schließende Klammer (), d. h \] . ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c und 0x5d bis 0x7F.</span><span class="sxs-lookup"><span data-stu-id="90b79-116">It must consist of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]); that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="90b79-117">Er darf nicht mit einem Leerzeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="90b79-117">It must not begin with a space.</span></span>

  - <span data-ttu-id="90b79-118">Sie muss aus mindestens einem Zeichen bestehen, das kein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="90b79-118">It must consist of at least one non-space character.</span></span>

<span data-ttu-id="90b79-119">**sztemplatetablename**</span><span class="sxs-lookup"><span data-stu-id="90b79-119">**szTemplateTableName**</span></span>

<span data-ttu-id="90b79-120">Der Name einer vorhandenen Tabelle, aus der die Basis-DDL (Data Definition Language) geerbt werden soll.</span><span class="sxs-lookup"><span data-stu-id="90b79-120">The name of an existing table from which to inherit the base data definition language (DDL).</span></span> <span data-ttu-id="90b79-121">Die Verwendung einer Vorlagen Tabelle ermöglicht die einfache Erstellung von vielen Tabellen mit identischen Spalten und Indizes.</span><span class="sxs-lookup"><span data-stu-id="90b79-121">Use of a template table allows for the easy creation of many tables with identical columns and indexes.</span></span>

<span data-ttu-id="90b79-122">**ulpages**</span><span class="sxs-lookup"><span data-stu-id="90b79-122">**ulPages**</span></span>

<span data-ttu-id="90b79-123">Die anfängliche Anzahl von Datenbankseiten, die für die Tabelle zuzuordnen sind.</span><span class="sxs-lookup"><span data-stu-id="90b79-123">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="90b79-124">Wenn eine Zahl größer als 1 angegeben wird, kann die Fragmentierung reduziert werden, wenn viele Zeilen in diese Tabelle eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="90b79-124">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="90b79-125">**uldensity**</span><span class="sxs-lookup"><span data-stu-id="90b79-125">**ulDensity**</span></span>

<span data-ttu-id="90b79-126">Die Tabellen Dichte in Prozent.</span><span class="sxs-lookup"><span data-stu-id="90b79-126">The table density, in percentage points.</span></span> <span data-ttu-id="90b79-127">Die Zahl muss entweder 0 oder im Bereich von 20 bis 100 sein.</span><span class="sxs-lookup"><span data-stu-id="90b79-127">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="90b79-128">Das übergeben von 0 bedeutet, dass der Standardwert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="90b79-128">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="90b79-129">Der Standardwert ist 80.</span><span class="sxs-lookup"><span data-stu-id="90b79-129">The default value is 80.</span></span>

<span data-ttu-id="90b79-130">**rgcolumncreate**</span><span class="sxs-lookup"><span data-stu-id="90b79-130">**rgcolumncreate**</span></span>

<span data-ttu-id="90b79-131">Ein Array von [JET_COLUMNCREATE](./jet-columncreate-structure.md) Strukturen, die jeweils einer Spalte entsprechen, die in der neuen Tabelle erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="90b79-131">An array of [JET_COLUMNCREATE](./jet-columncreate-structure.md) structures, each of which corresponds to a column to be created in the new table.</span></span>

<span data-ttu-id="90b79-132">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="90b79-132">**cColumns**</span></span>

<span data-ttu-id="90b79-133">Die Anzahl der [JET_COLUMNCREATE](./jet-columncreate-structure.md) Elemente im *rgcolumncreate* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="90b79-133">The number of [JET_COLUMNCREATE](./jet-columncreate-structure.md) elements in the *rgcolumncreate* parameter.</span></span>

<span data-ttu-id="90b79-134">**rgindexcreate**</span><span class="sxs-lookup"><span data-stu-id="90b79-134">**rgindexcreate**</span></span>

<span data-ttu-id="90b79-135">Ein Array von [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) Strukturen, von denen jede einem Index entspricht, der in der neuen Tabelle erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="90b79-135">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which corresponds to an index to be created in the new table.</span></span>

<span data-ttu-id="90b79-136">**cindexes**</span><span class="sxs-lookup"><span data-stu-id="90b79-136">**cIndexes**</span></span>

<span data-ttu-id="90b79-137">Die Anzahl der [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) Elemente im *rgindexcreate* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="90b79-137">The number of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) elements in the *rgindexcreate* parameter.</span></span>

<span data-ttu-id="90b79-138">**szcallback**</span><span class="sxs-lookup"><span data-stu-id="90b79-138">**szCallback**</span></span>

<span data-ttu-id="90b79-139">Die Funktion, die während bestimmter Ereignisse aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="90b79-139">The function that gets called during certain events.</span></span> <span data-ttu-id="90b79-140">**cbyp** bestimmt, wann die Rückruffunktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="90b79-140">**cbtyp** determines when the callback function will be called.</span></span>

<span data-ttu-id="90b79-141">Das Format von **szcallback** muss "Module \! Function" lauten, – z. b. "Alpha \! Beta" bezieht sich auf die Beta Funktion im Modul "Alpha".</span><span class="sxs-lookup"><span data-stu-id="90b79-141">The format of **szCallback** must be "module\!function" — for example, "alpha\!beta" refers to the beta function in the module named "alpha".</span></span>

<span data-ttu-id="90b79-142">Der Prototyp der Funktion muss mit der [JET_CALLBACK](./jet-callback-callback-function.md) Rückruffunktion identisch sein.</span><span class="sxs-lookup"><span data-stu-id="90b79-142">The prototype of the function must match the [JET_CALLBACK](./jet-callback-callback-function.md) callback function.</span></span>

<span data-ttu-id="90b79-143">**cbyp**</span><span class="sxs-lookup"><span data-stu-id="90b79-143">**cbtyp**</span></span>

<span data-ttu-id="90b79-144">Beschreibt den Typ der durch **szcallback** bezeichneten Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="90b79-144">Describes the type of callback function designated by **szCallback**.</span></span> <span data-ttu-id="90b79-145">Weitere Informationen finden Sie unter [JET_CBTYP](./jet-cbtyp.md).</span><span class="sxs-lookup"><span data-stu-id="90b79-145">For more information, see [JET_CBTYP](./jet-cbtyp.md).</span></span>

<span data-ttu-id="90b79-146">Dieses Bitfeld besteht aus einem oder mehreren Bitwerten, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="90b79-146">This bitfield is composed of one or more of the bit values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90b79-147">Wert</span><span class="sxs-lookup"><span data-stu-id="90b79-147">Value</span></span></p></th>
<th><p><span data-ttu-id="90b79-148">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90b79-148">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90b79-149">JET_cbtypFinalize</span><span class="sxs-lookup"><span data-stu-id="90b79-149">JET_cbtypFinalize</span></span></p></td>
<td><p><span data-ttu-id="90b79-150">Die Rückruffunktion wird aufgerufen, wenn eine Spalte, die abgeschlossen werden kann, auf NULL gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="90b79-150">The callback function will be called when a column that can be finalized has gone to zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90b79-151">JET_cbtypBeforeInsert</span><span class="sxs-lookup"><span data-stu-id="90b79-151">JET_cbtypBeforeInsert</span></span></p></td>
<td><p><span data-ttu-id="90b79-152">Die Rückruffunktion wird vor dem Einfügen von Datensätzen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="90b79-152">The callback function will be called prior to record insertion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90b79-153">JET_cbtypAfterInsert</span><span class="sxs-lookup"><span data-stu-id="90b79-153">JET_cbtypAfterInsert</span></span></p></td>
<td><p><span data-ttu-id="90b79-154">Die Rückruffunktion wird aufgerufen, nachdem die Datenbank-Engine das Einfügen eines Datensatzes abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="90b79-154">The callback function will be called after the database engine has finished inserting a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90b79-155">JET_cbtypBeforeReplace</span><span class="sxs-lookup"><span data-stu-id="90b79-155">JET_cbtypBeforeReplace</span></span></p></td>
<td><p><span data-ttu-id="90b79-156">Die Rückruffunktion wird vor der Änderung eines Datensatzes aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="90b79-156">The callback function will be called prior to the modification of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90b79-157">JET_cbtypAfterReplace</span><span class="sxs-lookup"><span data-stu-id="90b79-157">JET_cbtypAfterReplace</span></span></p></td>
<td><p><span data-ttu-id="90b79-158">Die Rückruffunktion wird aufgerufen, nachdem die Änderung eines Datensatzes abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="90b79-158">The callback function will be called after finishing the modification of a record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90b79-159">JET_cbtypBeforeDelete</span><span class="sxs-lookup"><span data-stu-id="90b79-159">JET_cbtypBeforeDelete</span></span></p></td>
<td><p><span data-ttu-id="90b79-160">Die Rückruffunktion wird vor dem Löschen eines Datensatzes aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="90b79-160">The callback function will be called prior to the deletion of a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90b79-161">JET_cbtypAfterDelete</span><span class="sxs-lookup"><span data-stu-id="90b79-161">JET_cbtypAfterDelete</span></span></p></td>
<td><p><span data-ttu-id="90b79-162">Die Rückruffunktion wird aufgerufen, nachdem ein Datensatz gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="90b79-162">The callback function will be called after a record has been deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90b79-163">JET_cbtypUserDefinedDefaultValue</span><span class="sxs-lookup"><span data-stu-id="90b79-163">JET_cbtypUserDefinedDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="90b79-164">Die Rückruffunktion wird aufgerufen, um einen benutzerdefinierten Standardwert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="90b79-164">The callback function will be called to calculate a user-defined default.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90b79-165">JET_cbtypFreeCursorLS</span><span class="sxs-lookup"><span data-stu-id="90b79-165">JET_cbtypFreeCursorLS</span></span></p></td>
<td><p><span data-ttu-id="90b79-166">Die Rückruffunktion wird aufgerufen, wenn der lokale Speicher, der einem Cursor zugeordnet ist, freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="90b79-166">The callback function will be called when the local storage that is associated with a cursor must be freed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90b79-167">JET_cbtypFreeTableLS</span><span class="sxs-lookup"><span data-stu-id="90b79-167">JET_cbtypFreeTableLS</span></span></p></td>
<td><p><span data-ttu-id="90b79-168">Die Rückruffunktion wird aufgerufen, wenn der lokale Speicher, der einer Tabelle zugeordnet ist, freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="90b79-168">The callback function will be called when the local storage that is associated with a table must be freed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="90b79-169">**grbit**</span><span class="sxs-lookup"><span data-stu-id="90b79-169">**grbit**</span></span>

<span data-ttu-id="90b79-170">Eine Gruppe von Bits, die NULL oder mehr der in der folgenden Tabelle aufgeführten aufrufoptions Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="90b79-170">A group of bits that contains zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90b79-171">Wert</span><span class="sxs-lookup"><span data-stu-id="90b79-171">Value</span></span></p></th>
<th><p><span data-ttu-id="90b79-172">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90b79-172">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90b79-173">JET_bitTableCreateFixedDDL</span><span class="sxs-lookup"><span data-stu-id="90b79-173">JET_bitTableCreateFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="90b79-174">Verhindert DDL-Vorgänge für die Tabelle (z. b. das Hinzufügen oder Entfernen von Spalten).</span><span class="sxs-lookup"><span data-stu-id="90b79-174">Prevents DDL operations on the table (such as adding or removing columns).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90b79-175">JET_bitTableCreateTemplateTable</span><span class="sxs-lookup"><span data-stu-id="90b79-175">JET_bitTableCreateTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="90b79-176">Bewirkt, dass die Tabelle eine Vorlagen Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="90b79-176">Causes the table to be a template table.</span></span> <span data-ttu-id="90b79-177">In neuen Tabellen kann dann der Name dieser Tabelle als Vorlagen Tabelle angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="90b79-177">New tables can then specify the name of this table as their template table.</span></span> <span data-ttu-id="90b79-178">Das Festlegen JET_bitTableCreateTemplateTable impliziert JET_bitTableCreateFixedDDL.</span><span class="sxs-lookup"><span data-stu-id="90b79-178">Setting JET_bitTableCreateTemplateTable implies JET_bitTableCreateFixedDDL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90b79-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="90b79-179">JET_bitTableCreateNoFixedVarColumnsInDerivedTables</span></span></p></td>
<td><p><span data-ttu-id="90b79-180">Muss in Verbindung mit JET_bitTableCreateTemplateTable verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90b79-180">Must be used in conjunction with JET_bitTableCreateTemplateTable.</span></span> <span data-ttu-id="90b79-181">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="90b79-181">Deprecated.</span></span> <span data-ttu-id="90b79-182">Nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="90b79-182">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="90b79-183">**pssqspacehints**</span><span class="sxs-lookup"><span data-stu-id="90b79-183">**pSeqSpacehints**</span></span>

<span data-ttu-id="90b79-184">Ein Zeiger auf eine [JET_SPACEHINTS](./jet-spacehints-structure.md) -Struktur für den sequenziellen Standard Index.</span><span class="sxs-lookup"><span data-stu-id="90b79-184">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for default sequential index.</span></span>

<span data-ttu-id="90b79-185">**p* qspacehints*\* wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="90b79-185">**pSeqSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="90b79-186">**plvspacehints**</span><span class="sxs-lookup"><span data-stu-id="90b79-186">**pLVSpacehints**</span></span>

<span data-ttu-id="90b79-187">Ein Zeiger auf eine [JET_SPACEHINTS](./jet-spacehints-structure.md) Struktur für eine getrennte Struktur mit langen Werten.</span><span class="sxs-lookup"><span data-stu-id="90b79-187">A pointer to a [JET_SPACEHINTS](./jet-spacehints-structure.md) structure for a Separated Long Value tree.</span></span>

<span data-ttu-id="90b79-188">**plvspacehints** wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="90b79-188">**pLVSpacehints** was introduced in Windows 7.</span></span>

<span data-ttu-id="90b79-189">**cbseparatelv**</span><span class="sxs-lookup"><span data-stu-id="90b79-189">**cbSeparateLV**</span></span>

<span data-ttu-id="90b79-190">Die Größe, mit der ein System internes LV vom primären Datensatz getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="90b79-190">The size to separate an intrinsic LV from the primary record.</span></span> <span data-ttu-id="90b79-191">Eine beliebige lange Wert-c-Struktur für eine getrennte LV-Struktur.</span><span class="sxs-lookup"><span data-stu-id="90b79-191">Any long-value c structure for a Separated LV tree.</span></span> <span data-ttu-id="90b79-192">Weitere Informationen finden Sie unter ng-Value in [JET_SPACEHINTS](./jet-spacehints-structure.md).</span><span class="sxs-lookup"><span data-stu-id="90b79-192">For more information, see ng-value in [JET_SPACEHINTS](./jet-spacehints-structure.md).</span></span> <span data-ttu-id="90b79-193">Lange Wert Spalten, die kleiner als dieser Wert sind, können getrennt werden, wenn der Datensatz zu groß wird.</span><span class="sxs-lookup"><span data-stu-id="90b79-193">Long-value columns smaller than this value may be separated if the record becomes too large.</span></span>

<span data-ttu-id="90b79-194">**cbseparatelv** wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="90b79-194">**cbSeparateLV** was introduced in Windows 7.</span></span>

<span data-ttu-id="90b79-195">**TableID**</span><span class="sxs-lookup"><span data-stu-id="90b79-195">**tableid**</span></span>

<span data-ttu-id="90b79-196">Ein Ausgabefeld, das den [JET_TABLEID](./jet-tableid.md) der neuen Tabelle enthält, wenn der API-Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90b79-196">An output field that holds the [JET_TABLEID](./jet-tableid.md) of the new table if the API call succeeds.</span></span> <span data-ttu-id="90b79-197">Wenn der API-Befehl fehlschlägt, ist der Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="90b79-197">If the API call fails, the value is undefined.</span></span> <span data-ttu-id="90b79-198">Diese Tabelle wird exklusiv geöffnet.</span><span class="sxs-lookup"><span data-stu-id="90b79-198">This table is opened exclusively.</span></span>

<span data-ttu-id="90b79-199">**erstellt**</span><span class="sxs-lookup"><span data-stu-id="90b79-199">**cCreated**</span></span>

<span data-ttu-id="90b79-200">Ein Ausgabefeld, das die Anzahl der-Objekte enthält, die erstellt werden, wenn der API-Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90b79-200">An output field that contains the count of objects that are created if the API call succeeds.</span></span> <span data-ttu-id="90b79-201">Wenn der API-Befehl fehlschlägt, ist der Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="90b79-201">If the API call fails, the value is undefined.</span></span>

<span data-ttu-id="90b79-202">Die Anzahl der Objekte, die erstellt werden, entspricht der Summe der Spalten, Tabellen und Indizes, die erfolgreich erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="90b79-202">The count of objects that are created is equal to the sum of columns, tables, and indexes that are successfully created.</span></span>

### <a name="requirements"></a><span data-ttu-id="90b79-203">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90b79-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90b79-204"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="90b79-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="90b79-205">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="90b79-205">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90b79-206"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="90b79-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="90b79-207">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="90b79-207">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90b79-208"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="90b79-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="90b79-209">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="90b79-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90b79-210"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="90b79-210"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="90b79-211">Wird als <strong>JET_TABLECREATE3_W</strong> (Unicode) und <strong>JET_TABLECREATE3_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="90b79-211">Implemented as <strong>JET_TABLECREATE3_W</strong> (Unicode) and <strong>JET_TABLECREATE3_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="90b79-212">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90b79-212">See also</span></span>

[<span data-ttu-id="90b79-213">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="90b79-213">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="90b79-214">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="90b79-214">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="90b79-215">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="90b79-215">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="90b79-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="90b79-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="90b79-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="90b79-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="90b79-218">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="90b79-218">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="90b79-219">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="90b79-219">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="90b79-220">Jetkreatetable</span><span class="sxs-lookup"><span data-stu-id="90b79-220">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="90b79-221">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="90b79-221">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="90b79-222">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="90b79-222">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="90b79-223">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="90b79-223">JetDefragment2</span></span>](./jetdefragment2-function.md)
