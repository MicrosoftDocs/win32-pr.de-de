---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNBASE Struktur'
title: JET_COLUMNBASE-Struktur
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: 9276c36a08a429f44568b3a909af77f5ae038c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352594"
---
# <a name="jet_columnbase-structure"></a><span data-ttu-id="947cb-103">JET_COLUMNBASE-Struktur</span><span class="sxs-lookup"><span data-stu-id="947cb-103">JET_COLUMNBASE Structure</span></span>


<span data-ttu-id="947cb-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="947cb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnbase-structure"></a><span data-ttu-id="947cb-105">JET_COLUMNBASE-Struktur</span><span class="sxs-lookup"><span data-stu-id="947cb-105">JET_COLUMNBASE Structure</span></span>

<span data-ttu-id="947cb-106">Die **JET_COLUMNBASE** -Struktur beschreibt die Parameter einer Basis Spalte.</span><span class="sxs-lookup"><span data-stu-id="947cb-106">The **JET_COLUMNBASE** structure describes the parameters of a base column.</span></span> <span data-ttu-id="947cb-107">Die [jetgetcolumninfo](./jetgetcolumninfo-function.md) -und [jetgettablecolumninfo](./jetgettablecolumninfo-function.md) -Funktionen verwenden die **JET_COLUMNBASE** Struktur.</span><span class="sxs-lookup"><span data-stu-id="947cb-107">The [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions use the **JET_COLUMNBASE** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a><span data-ttu-id="947cb-108">Member</span><span class="sxs-lookup"><span data-stu-id="947cb-108">Members</span></span>

<span data-ttu-id="947cb-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="947cb-109">**cbStruct**</span></span>

<span data-ttu-id="947cb-110">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="947cb-110">The size of this structure, in bytes.</span></span> <span data-ttu-id="947cb-111">Legen Sie **cbStruct** auf sizeof (JET_COLUMNBASE) fest.</span><span class="sxs-lookup"><span data-stu-id="947cb-111">Set **cbStruct** to sizeof( JET_COLUMNBASE ).</span></span>

<span data-ttu-id="947cb-112">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="947cb-112">**columnid**</span></span>

<span data-ttu-id="947cb-113">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="947cb-113">Reserved.</span></span> <span data-ttu-id="947cb-114">Legen Sie **ColumnID** auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="947cb-114">Set **columnid** to 0 (zero).</span></span>

<span data-ttu-id="947cb-115">**colyp**</span><span class="sxs-lookup"><span data-stu-id="947cb-115">**coltyp**</span></span>

<span data-ttu-id="947cb-116">Der Typ der Spalte (z. b. "Text", "Binary" oder "Numerisch").</span><span class="sxs-lookup"><span data-stu-id="947cb-116">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="947cb-117">Weitere Informationen finden Sie unter [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="947cb-117">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="947cb-118">**wcountry**</span><span class="sxs-lookup"><span data-stu-id="947cb-118">**wCountry**</span></span>

<span data-ttu-id="947cb-119">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="947cb-119">Reserved.</span></span> <span data-ttu-id="947cb-120">Legen Sie den Wert auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="947cb-120">Set to 0 (zero).</span></span>

<span data-ttu-id="947cb-121">**langid**</span><span class="sxs-lookup"><span data-stu-id="947cb-121">**langid**</span></span>

<span data-ttu-id="947cb-122">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="947cb-122">Reserved.</span></span> <span data-ttu-id="947cb-123">Legen Sie den Wert auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="947cb-123">Set to 0 (zero).</span></span>

<span data-ttu-id="947cb-124">**cp**</span><span class="sxs-lookup"><span data-stu-id="947cb-124">**cp**</span></span>

<span data-ttu-id="947cb-125">Die Codepage für die Spalte.</span><span class="sxs-lookup"><span data-stu-id="947cb-125">The code page for the column.</span></span> <span data-ttu-id="947cb-126">Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="947cb-126">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="947cb-127">Der Wert 0 (null) bedeutet, dass der Standardwert verwendet wird (English, 1252).</span><span class="sxs-lookup"><span data-stu-id="947cb-127">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="947cb-128">Handelt es sich bei der Spalte nicht um eine Text Spalte, wird die Codepage automatisch auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="947cb-128">If the column is not a text column, the code page is automatically set to zero.</span></span>

<span data-ttu-id="947cb-129">**wfiller**</span><span class="sxs-lookup"><span data-stu-id="947cb-129">**wFiller**</span></span>

<span data-ttu-id="947cb-130">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="947cb-130">Reserved.</span></span> <span data-ttu-id="947cb-131">Legen Sie den Wert auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="947cb-131">Set to 0 (zero).</span></span>

<span data-ttu-id="947cb-132">**cbmax**</span><span class="sxs-lookup"><span data-stu-id="947cb-132">**cbMax**</span></span>

<span data-ttu-id="947cb-133">Die maximale Länge (in Byte) einer Spalte variabler Länge oder die tatsächliche Länge einer Spalte fester Länge in Bytes.</span><span class="sxs-lookup"><span data-stu-id="947cb-133">The maximum length, in bytes, of a variable-length column, or the actual length, in bytes, of a fixed-length column.</span></span>

<span data-ttu-id="947cb-134">**grbit**</span><span class="sxs-lookup"><span data-stu-id="947cb-134">**grbit**</span></span>

<span data-ttu-id="947cb-135">Optionen für die Spalte, einschließlich NULL oder mehr der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="947cb-135">Options for the column, including zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="947cb-136">Wert</span><span class="sxs-lookup"><span data-stu-id="947cb-136">Value</span></span></p></th>
<th><p><span data-ttu-id="947cb-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="947cb-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="947cb-138">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="947cb-138">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="947cb-139">Die Spalte ist korrigiert und belegt den gleichen Speicherplatz in einer Zeile, unabhängig davon, wie viele Daten Sie enthält.</span><span class="sxs-lookup"><span data-stu-id="947cb-139">The column is fixed and occupies the same amount of space in a row regardless of how much data it contains.</span></span> <span data-ttu-id="947cb-140">JET_bitColumnFixed kann nicht mit JET_bitColumnTagged kombiniert werden und kann nicht verwendet werden, wenn das <strong>colttmember</strong> auf <strong>JET_coltypLongText</strong> oder <strong>JET_coltypLongBinary</strong>festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="947cb-140">JET_bitColumnFixed cannot be combined with JET_bitColumnTagged, and cannot be used when the <strong>coltyp</strong> member is set to <strong>JET_coltypLongText</strong> or <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="947cb-141">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="947cb-141">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="947cb-142">Die Spalte ist gekennzeichnet und belegt nur dann Speicherplatz in der Datenbank, wenn Sie Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="947cb-142">The column is tagged and occupies space in the database only if it contains data.</span></span> <span data-ttu-id="947cb-143">JET_bitColumnTagged können nicht mit JET_bitColumnFixed, JET_bitColumnVersion oder JET_bitColumnEscrowUpdate kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-143">JET_bitColumnTagged cannot be combined with JET_bitColumnFixed, JET_bitColumnVersion, or JET_bitColumnEscrowUpdate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="947cb-144">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="947cb-144">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="947cb-145">Die Spalte darf nicht auf einen <strong>null</strong> -Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-145">The column must not be set to a <strong>NULL</strong> value.</span></span></p>
<p><span data-ttu-id="947cb-146">JET_bitColumnNotNULL können nicht mit JET_bitColumnUserDefinedDefault kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-146">JET_bitColumnNotNULL cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="947cb-147">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="947cb-147">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="947cb-148">Die Spalte ist eine Versions Spalte, die die Version der Zeile angibt.</span><span class="sxs-lookup"><span data-stu-id="947cb-148">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="947cb-149">Der Wert dieser Spalte beginnt bei Null und wird für jedes Update der Zeile automatisch inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="947cb-149">The value of this column starts at zero and is automatically incremented for each update of the row.</span></span></p>
<p><span data-ttu-id="947cb-150">JET_bitColumnVersion können nur verwendet werden, wenn das <strong>colttmember</strong> auf <strong>JET_coltypLong</strong> festgelegt ist und nicht mit JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged oder JET_bitColumnUserDefinedDefault kombiniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="947cb-150">JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> and cannot be combined with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged, or JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="947cb-151">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="947cb-151">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="947cb-152">Die Spalte wird automatisch inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="947cb-152">The column is automatically incremented.</span></span> <span data-ttu-id="947cb-153">Die Zahl ist eine steigende Zahl, die in einer Tabelle garantiert eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="947cb-153">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="947cb-154">Die Zahlen sind jedoch möglicherweise nicht sequenziell.</span><span class="sxs-lookup"><span data-stu-id="947cb-154">The numbers, however, may not be sequential.</span></span> <span data-ttu-id="947cb-155">Wenn z. b. fünf Zeilen in eine Tabelle eingefügt werden, kann die automatisch inkrementierte Spalte die Werte {1, 2, 6, 7, 8} enthalten.</span><span class="sxs-lookup"><span data-stu-id="947cb-155">For example, if five rows are inserted into a table, the automatically incremented column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="947cb-156">JET_bitColumnAutoincrement können nur verwendet werden, wenn das <strong>colttmember</strong> auf <strong>JET_coltypLong</strong> oder <strong>JET_coltypCurrency</strong> festgelegt ist und nicht mit JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault oder JET_bitColumnVersion kombiniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="947cb-156">JET_bitColumnAutoincrement can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong> and cannot be combined with JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault, or JET_bitColumnVersion.</span></span></p>
<p><span data-ttu-id="947cb-157"><strong>Windows 2000:  </strong> JET_bitColumnVersion können nur verwendet werden, wenn das <strong>colttmember</strong> auf <strong>JET_coltypLong</strong>festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="947cb-157"><strong>Windows 2000:  </strong>JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="947cb-158">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="947cb-158">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="947cb-159">Gilt nur für Aufrufe von <a href="gg269215(v=exchg.10).md">jetgetcolumninfo</a>.</span><span class="sxs-lookup"><span data-stu-id="947cb-159">Valid only for calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span> <span data-ttu-id="947cb-160">JET_bitColumnUpdatable können nicht mit JET_bitColumnUserDefinedDefault kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-160">JET_bitColumnUpdatable cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="947cb-161">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="947cb-161">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="947cb-162">Nur bei Aufrufen von <a href="gg294118(v=exchg.10).md">jetopentable</a>gültig.</span><span class="sxs-lookup"><span data-stu-id="947cb-162">Valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="947cb-163">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="947cb-163">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="947cb-164">Nur bei Aufrufen von <a href="gg269211(v=exchg.10).md">jetopumtemptable</a>gültig.</span><span class="sxs-lookup"><span data-stu-id="947cb-164">Valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="947cb-165">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="947cb-165">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="947cb-166">Die Spalte kann mehr wertig sein.</span><span class="sxs-lookup"><span data-stu-id="947cb-166">The column can be multi-valued.</span></span> <span data-ttu-id="947cb-167">Für eine mehrwertige Spalte können NULL, ein oder mehrere Werte zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-167">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="947cb-168">Die verschiedenen Werte in einer mehrwertigen Spalte werden durch eine Zahl im <strong>itagsequence</strong> -Member verschiedener Strukturen identifiziert, z. b. <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="947cb-168">The various values in a multi-valued column are identified by a number in the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="947cb-169">Mehrwertige Spalten müssen markierte Spalten sein. Das heißt, Sie sind möglicherweise keine Spalten fester Länge oder Spalten variabler Länge.</span><span class="sxs-lookup"><span data-stu-id="947cb-169">Multi-valued columns must be tagged columns; that is, they may not be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="947cb-170">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="947cb-170">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="947cb-171">Gibt an, dass eine Spalte eine Spalte für das Hinterlegungs Update ist, die gleichzeitig von verschiedenen Sitzungen mit <a href="gg294125(v=exchg.10).md">jetescrowupdate</a> aktualisiert werden kann und transaktionale Konsistenz aufweist.</span><span class="sxs-lookup"><span data-stu-id="947cb-171">Specifies that a column is an escrow update column that can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will have transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="947cb-172">Eine Spalte für das Hinterlegungs Update kann nur erstellt werden, wenn die Tabelle leer ist.</span><span class="sxs-lookup"><span data-stu-id="947cb-172">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="947cb-173">Für eine Spalte mit einem Hinterlegungs Update muss das <strong>colttmember</strong> auf JET_coltypLong festgelegt werden <strong>.</strong></span><span class="sxs-lookup"><span data-stu-id="947cb-173">For an escrow update column, the <strong>coltyp</strong> member must be set to <strong>JET_coltypLong.</strong></span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="947cb-174">Eine Spalte für das Hinterlegungs Update muss über einen Standardwert verfügen (" <strong>cbdefault</strong> " muss positiv sein).</span><span class="sxs-lookup"><span data-stu-id="947cb-174">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="947cb-175">JET_bitColumnEscrowUpdate können nicht mit JET_bitColumnTagged, JET_bitColumnVersion oder JET_bitColumnAutoincrement kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-175">JET_bitColumnEscrowUpdate cannot be combined with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="947cb-176">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="947cb-176">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="947cb-177">Die Spalte wird ohne Versionsnummer erstellt.</span><span class="sxs-lookup"><span data-stu-id="947cb-177">The column is created without a version number.</span></span> <span data-ttu-id="947cb-178">Dies bedeutet, dass andere Transaktionen, die versuchen, eine Spalte mit demselben Namen hinzuzufügen, fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="947cb-178">This means that other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="947cb-179">JET_bitColumnUnversioned wird nur mit <a href="gg294122(v=exchg.10).md">jetaddcolumn</a>verwendet.</span><span class="sxs-lookup"><span data-stu-id="947cb-179">JET_bitColumnUnversioned is used only with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="947cb-180">Sie kann nicht innerhalb einer Transaktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-180">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="947cb-181">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="947cb-181">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="947cb-182">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="947cb-182">Reserved for future use.</span></span></p>
<p><span data-ttu-id="947cb-183">JET_bitColumnMaybeNull können nicht mit JET_bitColumnUserDefinedDefault kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-183">JET_bitColumnMaybeNull cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="947cb-184">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="947cb-184">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="947cb-185">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-185">Do not use.</span></span> <span data-ttu-id="947cb-186">Verwenden Sie stattdessen JET_bitColumnDeleteOnZero.</span><span class="sxs-lookup"><span data-stu-id="947cb-186">Use JET_bitColumnDeleteOnZero instead.</span></span></p>
<p><span data-ttu-id="947cb-187">Die Spalte kann abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-187">The column can be finalized.</span></span> <span data-ttu-id="947cb-188">Eine Spalte, die abgeschlossen werden kann, ist eine Spalte für das hinterlegen des Updates, die bewirkt, dass die Zeile gelöscht wird, wenn die Spalte NULL erreicht.</span><span class="sxs-lookup"><span data-stu-id="947cb-188">A column that can be finalized is an escrow update column that causes the row to be deleted when the column reaches zero.</span></span> <span data-ttu-id="947cb-189">In zukünftigen Versionen wird stattdessen möglicherweise eine Rückruffunktion aufgerufen (siehe <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span><span class="sxs-lookup"><span data-stu-id="947cb-189">Future versions may invoke a callback function instead (See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="947cb-190">Eine Spalte, die abgeschlossen werden kann, muss eine Spalte für die hinterlegte Aktualisierung sein.</span><span class="sxs-lookup"><span data-stu-id="947cb-190">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="947cb-191">JET_bitColumnFinalize können nicht mit JET_bitColumnUserDefinedDefault kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-191">JET_bitColumnFinalize cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="947cb-192">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="947cb-192">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="947cb-193">Der Standardwert für eine Spalte wird von einer Rückruffunktion bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="947cb-193">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="947cb-194">Siehe <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="947cb-194">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="947cb-195">Eine Spalte, die über einen benutzerdefinierten Standardwert verfügt, muss eine markierte Spalte sein.</span><span class="sxs-lookup"><span data-stu-id="947cb-195">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="947cb-196">Wenn JET_bitColumnUserDefinedDefault angegeben wird, muss <strong>pvdefault</strong> auf eine <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> Struktur verweisen, und <strong>cbdefault</strong> muss auf sizeof (JET_USERDEFINEDDEFAULT) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-196">If JET_bitColumnUserDefinedDefault is specified, the <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( JET_USERDEFINEDDEFAULT ).</span></span></p>
<p><span data-ttu-id="947cb-197">JET_bitColumnUserDefinedDefault können nicht mit JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero oder JET_bitColumnMaybeNull kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-197">JET_bitColumnUserDefinedDefault cannot be combined with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="947cb-198">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="947cb-198">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="947cb-199">Bei der Spalte handelt es sich um eine Spalte zum Aktualisieren von Spalten. Wenn Sie Null erreicht, wird der Datensatz gelöscht.</span><span class="sxs-lookup"><span data-stu-id="947cb-199">The column is an escrow update column and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="947cb-200">Eine häufige Verwendung für Spalten mit dem Wert "Delete-on-Zero" ist als Verweis Zähler Felder.</span><span class="sxs-lookup"><span data-stu-id="947cb-200">A common use for delete-on-zero columns is as reference count fields.</span></span> <span data-ttu-id="947cb-201">Wenn die Anzahl der Verweise auf Null fällt, wird der Datensatz gelöscht.</span><span class="sxs-lookup"><span data-stu-id="947cb-201">When the number of references fall to zero, the record is deleted.</span></span> <span data-ttu-id="947cb-202">Eine DELETE-on-Zero-Spalte muss eine Spalte für die hinterlegte Aktualisierung sein.</span><span class="sxs-lookup"><span data-stu-id="947cb-202">A delete-on-zero column must be an escrow update column.</span></span></p>
<p><span data-ttu-id="947cb-203">JET_bitColumnDeleteOnZero ersetzt JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="947cb-203">JET_bitColumnDeleteOnZero replaces JET_bitColumnFinalize.</span></span></p>
<p><span data-ttu-id="947cb-204">JET_bitColumnDeleteOnZero kann nicht mit JET_bitColumnFinalize oder JET_bitColumnUserDefinedDefault kombiniert werden und kann nicht mit benutzerdefinierten Standard Spalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="947cb-204">JET_bitColumnDeleteOnZero cannot be combined with JET_bitColumnFinalize or JET_bitColumnUserDefinedDefault, and cannot be used with user-defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="947cb-205">**szbasetablename**</span><span class="sxs-lookup"><span data-stu-id="947cb-205">**szBaseTableName**</span></span>

<span data-ttu-id="947cb-206">Die Tabelle, aus der die aktuelle Tabelle Ihre DDL erbt.</span><span class="sxs-lookup"><span data-stu-id="947cb-206">The table from which the current table inherits its DDL.</span></span>

<span data-ttu-id="947cb-207">**szbasecolumschlag Name**</span><span class="sxs-lookup"><span data-stu-id="947cb-207">**szBaseColumnName**</span></span>

<span data-ttu-id="947cb-208">Der Name der Spalte in der Vorlagen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="947cb-208">The name of the column in the template table.</span></span>

### <a name="remarks"></a><span data-ttu-id="947cb-209">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="947cb-209">Remarks</span></span>

<span data-ttu-id="947cb-210">**JET_COLUMNBASE** enthält viele der gleichen Informationen wie [JET_COLUMNDEF](./jet-columndef-structure.md), fügt jedoch Zeichen folgen Felder hinzu, um die Basistabelle zu beschreiben (wenn eine hierarchische DDL verwendet wurde).</span><span class="sxs-lookup"><span data-stu-id="947cb-210">**JET_COLUMNBASE** contains much of the same information as [JET_COLUMNDEF](./jet-columndef-structure.md), but it adds string fields to describe the base table (if a hierarchical DDL was used).</span></span>

### <a name="requirements"></a><span data-ttu-id="947cb-211">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="947cb-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="947cb-212"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="947cb-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="947cb-213">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="947cb-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="947cb-214"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="947cb-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="947cb-215">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="947cb-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="947cb-216"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="947cb-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="947cb-217">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="947cb-217">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="947cb-218"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="947cb-218"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="947cb-219">Wird als <strong>JET_COLUMNBASE_W</strong> (Unicode) und <strong>JET_COLUMNBASE_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="947cb-219">Implemented as <strong>JET_COLUMNBASE_W</strong> (Unicode) and <strong>JET_COLUMNBASE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="947cb-220">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="947cb-220">See Also</span></span>

[<span data-ttu-id="947cb-221">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="947cb-221">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="947cb-222">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="947cb-222">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="947cb-223">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="947cb-223">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="947cb-224">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="947cb-224">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="947cb-225">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="947cb-225">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="947cb-226">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="947cb-226">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="947cb-227">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="947cb-227">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="947cb-228">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="947cb-228">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="947cb-229">Jetgetcolumninfo</span><span class="sxs-lookup"><span data-stu-id="947cb-229">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="947cb-230">Jetgettablecolumninfo</span><span class="sxs-lookup"><span data-stu-id="947cb-230">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="947cb-231">Jetrenamecolumschlag</span><span class="sxs-lookup"><span data-stu-id="947cb-231">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
