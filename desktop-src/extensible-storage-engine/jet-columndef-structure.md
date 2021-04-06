---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNDEF Struktur'
title: JET_COLUMNDEF-Struktur
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: c541b5801c95f4b269e33360f5ffa2404ff8fc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960869"
---
# <a name="jet_columndef-structure"></a><span data-ttu-id="61d75-103">JET_COLUMNDEF-Struktur</span><span class="sxs-lookup"><span data-stu-id="61d75-103">JET_COLUMNDEF Structure</span></span>


<span data-ttu-id="61d75-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="61d75-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columndef-structure"></a><span data-ttu-id="61d75-105">JET_COLUMNDEF-Struktur</span><span class="sxs-lookup"><span data-stu-id="61d75-105">JET_COLUMNDEF Structure</span></span>

<span data-ttu-id="61d75-106">Die **JET_COLUMNDEF** -Struktur definiert die Daten, die in einer-Spalte gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="61d75-106">The **JET_COLUMNDEF** structure defines the data that can be stored in a column.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a><span data-ttu-id="61d75-107">Member</span><span class="sxs-lookup"><span data-stu-id="61d75-107">Members</span></span>

<span data-ttu-id="61d75-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="61d75-108">**cbStruct**</span></span>

<span data-ttu-id="61d75-109">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="61d75-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="61d75-110">Er muss auf sizeof (JET_COLUMNDEF) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-110">It must be set to sizeof( JET_COLUMNDEF).</span></span>

<span data-ttu-id="61d75-111">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="61d75-111">**columnid**</span></span>

<span data-ttu-id="61d75-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="61d75-112">Reserved.</span></span> <span data-ttu-id="61d75-113">**ColumnID** muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-113">**columnid** must be set to 0 (zero).</span></span>

<span data-ttu-id="61d75-114">**colyp**</span><span class="sxs-lookup"><span data-stu-id="61d75-114">**coltyp**</span></span>

<span data-ttu-id="61d75-115">Der Typ der Spalte (z. b. "Text", "Binary" oder "Numerisch").</span><span class="sxs-lookup"><span data-stu-id="61d75-115">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="61d75-116">Weitere Informationen finden Sie unter [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="61d75-116">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="61d75-117">**wcountry**</span><span class="sxs-lookup"><span data-stu-id="61d75-117">**wCountry**</span></span>

<span data-ttu-id="61d75-118">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="61d75-118">Reserved.</span></span> <span data-ttu-id="61d75-119">**wcountry** muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-119">**wCountry** must be set to 0 (zero).</span></span>

<span data-ttu-id="61d75-120">**langid**</span><span class="sxs-lookup"><span data-stu-id="61d75-120">**langid**</span></span>

<span data-ttu-id="61d75-121">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="61d75-121">Obsolete.</span></span> <span data-ttu-id="61d75-122">**LangID** muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-122">**langid** should be set to 0 (zero).</span></span>

<span data-ttu-id="61d75-123">**cp**</span><span class="sxs-lookup"><span data-stu-id="61d75-123">**cp**</span></span>

<span data-ttu-id="61d75-124">Die Codepage für die Spalte.</span><span class="sxs-lookup"><span data-stu-id="61d75-124">The code page for the column.</span></span> <span data-ttu-id="61d75-125">Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="61d75-125">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="61d75-126">Der Wert 0 (null) bedeutet, dass der Standardwert verwendet wird (English, 1252).</span><span class="sxs-lookup"><span data-stu-id="61d75-126">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="61d75-127">Handelt es sich bei der Spalte nicht um eine Text Spalte, wird die Codepage automatisch auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="61d75-127">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="61d75-128">**wcollate**</span><span class="sxs-lookup"><span data-stu-id="61d75-128">**wCollate**</span></span>

<span data-ttu-id="61d75-129">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="61d75-129">Reserved.</span></span> <span data-ttu-id="61d75-130">**wcollate** muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-130">**wCollate** must be set to 0 (zero).</span></span>

<span data-ttu-id="61d75-131">**cbmax**</span><span class="sxs-lookup"><span data-stu-id="61d75-131">**cbMax**</span></span>

<span data-ttu-id="61d75-132">Die maximale Länge (in Byte) einer Spalte variabler Länge oder die Länge einer Spalte mit fester Länge.</span><span class="sxs-lookup"><span data-stu-id="61d75-132">The maximum length, in bytes, of a variable-length column, or the length of a fixed-length column.</span></span>

<span data-ttu-id="61d75-133">**grbit**</span><span class="sxs-lookup"><span data-stu-id="61d75-133">**grbit**</span></span>

<span data-ttu-id="61d75-134">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die 0 (null) oder mehrere der folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="61d75-134">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61d75-135">Wert</span><span class="sxs-lookup"><span data-stu-id="61d75-135">Value</span></span></p></th>
<th><p><span data-ttu-id="61d75-136">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="61d75-136">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61d75-137">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="61d75-137">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="61d75-138">Die Spalte wird korrigiert.</span><span class="sxs-lookup"><span data-stu-id="61d75-138">The column will be fixed.</span></span> <span data-ttu-id="61d75-139">Es wird immer die gleiche Menge an Speicherplatz in einer Zeile verwendet, unabhängig davon, wie viele Daten in der Spalte gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-139">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="61d75-140">JET_bitColumnFixed können nicht mit JET_bitColumnTagged verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-140">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="61d75-141">Dieses Bit kann nicht mit langen Werten (d. h. <strong>JET_coltypLongText</strong> und <strong>JET_coltypLongBinary</strong>) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-141">This bit cannot be used with long values (that is <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61d75-142">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="61d75-142">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="61d75-143">Die Spalte wird gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="61d75-143">The column will be tagged.</span></span> <span data-ttu-id="61d75-144">Markierte Spalten beanspruchen keinen Speicherplatz in der Datenbank, wenn Sie keine Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="61d75-144">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="61d75-145">Dieses Bit kann nicht mit JET_bitColumnFixed verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-145">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61d75-146">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="61d75-146">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="61d75-147">Die Spalte darf nie auf einen NULL-Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-147">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61d75-148">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="61d75-148">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="61d75-149">Die Spalte ist eine Versions Spalte, die die Version der Zeile angibt.</span><span class="sxs-lookup"><span data-stu-id="61d75-149">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="61d75-150">Der Wert dieser Spalte beginnt bei Null und wird für jedes Update in der Zeile automatisch inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="61d75-150">The value of this column starts at zero and will be automatically incremented for each update on the row.</span></span></p>
<p><span data-ttu-id="61d75-151">Dieses Bit kann nur auf <strong>JET_coltypLong</strong> Spalten angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-151">This bit can only be applied to <strong>JET_coltypLong</strong> columns.</span></span> <span data-ttu-id="61d75-152">Dieses Bit kann nicht mit JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate oder JET_bitColumnTagged verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-152">This bit cannot be used with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, or JET_bitColumnTagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61d75-153">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="61d75-153">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="61d75-154">Die Spalte wird automatisch inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="61d75-154">The column will automatically be incremented.</span></span> <span data-ttu-id="61d75-155">Die Zahl ist eine steigende Zahl, die in einer Tabelle garantiert eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="61d75-155">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="61d75-156">Die Zahlen sind jedoch möglicherweise nicht kontinuierlich.</span><span class="sxs-lookup"><span data-stu-id="61d75-156">The numbers, however, might not be continuous.</span></span> <span data-ttu-id="61d75-157">Wenn z. b. fünf Zeilen in eine Tabelle eingefügt werden, &quot; kann die AutoIncrement- &quot; Spalte die Werte {1, 2, 6, 7, 8} enthalten.</span><span class="sxs-lookup"><span data-stu-id="61d75-157">For example, if five rows are inserted into a table, the &quot;autoincrement&quot; column could contain the values { 1, 2, 6, 7, 8 }.</span></span> <span data-ttu-id="61d75-158">Dieses Bit kann nur für Spalten vom Typ <strong>JET_coltypLong</strong> oder <strong>JET_coltypCurrency</strong>verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-158">This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p>
<p><span data-ttu-id="61d75-159"><strong>Windows 2000:  </strong> In Windows 2000 kann dieses Bit nur für Spalten vom Typ <strong>JET_coltypLong</strong>verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-159"><strong>Windows 2000:  </strong>In Windows 2000, this bit can only be used on columns of type <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61d75-160">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="61d75-160">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="61d75-161">Dieses Bit ist nur bei Aufrufen von <a href="gg269215(v=exchg.10).md">jetgetcolumninfo</a>gültig.</span><span class="sxs-lookup"><span data-stu-id="61d75-161">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61d75-162">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="61d75-162">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="61d75-163">Dieses Bit ist nur bei Aufrufen von <a href="gg294118(v=exchg.10).md">jetopentable</a>gültig.</span><span class="sxs-lookup"><span data-stu-id="61d75-163">This bit is valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61d75-164">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="61d75-164">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="61d75-165">Dieses Bit ist nur bei Aufrufen von <a href="gg269211(v=exchg.10).md">jetopentemptable</a>gültig.</span><span class="sxs-lookup"><span data-stu-id="61d75-165">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61d75-166">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="61d75-166">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="61d75-167">Die Spalte kann mehr wertig sein.</span><span class="sxs-lookup"><span data-stu-id="61d75-167">The column can be multi-valued.</span></span> <span data-ttu-id="61d75-168">Für eine mehrwertige Spalte können NULL, ein oder mehrere Werte zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-168">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="61d75-169">Die verschiedenen Werte in einer mehrwertigen Spalte werden durch eine Zahl gekennzeichnet, die als <strong>itagsequence</strong> -Member bezeichnet wird, der zu verschiedenen Strukturen gehört, einschließlich: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>und <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="61d75-169">The various values in a multi-valued column are identified by a number called the <strong>itagSequence</strong> member, which belongs to various structures, including: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, and <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="61d75-170">Mehrwertige Spalten müssen markierte Spalten sein. Das heißt, Sie können keine Spalten fester Länge oder Spalten mit variabler Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="61d75-170">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61d75-171">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="61d75-171">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="61d75-172">Gibt an, dass eine Spalte eine Spalte für die hinterlegte Aktualisierung ist.</span><span class="sxs-lookup"><span data-stu-id="61d75-172">Specifies that a column is an escrow update column.</span></span> <span data-ttu-id="61d75-173">Eine Spalte für das Hinterlegungs Update kann gleichzeitig von verschiedenen Sitzungen mit <a href="gg294125(v=exchg.10).md">jetescrowupdate</a> aktualisiert werden und behält die Transaktions Konsistenz bei.</span><span class="sxs-lookup"><span data-stu-id="61d75-173">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will maintain transactional consistency.</span></span> <span data-ttu-id="61d75-174">Eine Spalte für das Hinterlegungs Update muss außerdem die folgenden Bedingungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="61d75-174">An escrow update column must also meet the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="61d75-175">Eine Spalte für das Hinterlegungs Update kann nur erstellt werden, wenn die Tabelle leer ist.</span><span class="sxs-lookup"><span data-stu-id="61d75-175">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="61d75-176">Eine Spalte vom Typ "hinterlegter" muss vom Typ " <strong>JET_coltypLong</strong>" sein.</span><span class="sxs-lookup"><span data-stu-id="61d75-176">An escrow update column must be of type <strong>JET_coltypLong</strong>.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="61d75-177">Eine Spalte für das Hinterlegungs Update muss über einen Standardwert verfügen (" <strong>cbdefault</strong> " muss positiv sein).</span><span class="sxs-lookup"><span data-stu-id="61d75-177">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="61d75-178">JET_bitColumnEscrowUpdate kann nicht zusammen mit JET_bitColumnTagged, JET_bitColumnVersion oder JET_bitColumnAutoincrement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-178">JET_bitColumnEscrowUpdate cannot be used in conjunction with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61d75-179">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="61d75-179">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="61d75-180">Die Spalte wird in einem ohne Versionsinformationen erstellt.</span><span class="sxs-lookup"><span data-stu-id="61d75-180">The column will be created in an without version information.</span></span> <span data-ttu-id="61d75-181">Dies bedeutet, dass andere Transaktionen, die versuchen, eine Spalte mit demselben Namen hinzuzufügen, fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="61d75-181">This means that other transactions that attempt to add a column with the same name will fail.</span></span> <span data-ttu-id="61d75-182">Dieses Bit ist nur bei <a href="gg294122(v=exchg.10).md">jetaddcolumn</a>nützlich.</span><span class="sxs-lookup"><span data-stu-id="61d75-182">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="61d75-183">Sie kann nicht innerhalb einer Transaktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-183">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61d75-184">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="61d75-184">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="61d75-185">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="61d75-185">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61d75-186">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="61d75-186">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="61d75-187">Verwenden Sie JET_bitColumnDeleteOnZero anstelle von JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="61d75-187">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="61d75-188">JET_bitColumnFinalize, dass eine Spalte fertiggestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="61d75-188">JET_bitColumnFinalize that a column can be finalized.</span></span> <span data-ttu-id="61d75-189">Wenn eine Spalte, die abgeschlossen werden kann, eine Spalte mit dem Wert "hinterlegter Update" aufweist, die Null erreicht, wird die Zeile gelöscht.</span><span class="sxs-lookup"><span data-stu-id="61d75-189">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="61d75-190">In zukünftigen Versionen wird stattdessen möglicherweise eine Rückruffunktion aufgerufen (Weitere Informationen finden Sie unter <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span><span class="sxs-lookup"><span data-stu-id="61d75-190">Future versions might invoke a callback function instead (For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="61d75-191">Eine Spalte, die abgeschlossen werden kann, muss eine Spalte für die hinterlegte Aktualisierung sein.</span><span class="sxs-lookup"><span data-stu-id="61d75-191">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="61d75-192">JET_bitColumnFinalize können nicht mit JET_bitColumnUserDefinedDefault verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-192">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61d75-193">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="61d75-193">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="61d75-194">Der Standardwert für eine Spalte wird von einer Rückruffunktion bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="61d75-194">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="61d75-195">Siehe <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="61d75-195">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="61d75-196">Eine Spalte, die über einen benutzerdefinierten Standardwert verfügt, muss eine markierte Spalte sein.</span><span class="sxs-lookup"><span data-stu-id="61d75-196">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="61d75-197">Das Angeben von JET_bitColumnUserDefinedDefault bedeutet, dass <strong>pvdefault</strong> auf eine <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> Struktur verweisen muss und <strong>cbdefault</strong> auf sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ) festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="61d75-197">Specifying JET_bitColumnUserDefinedDefault means that <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</span></span></p>
<ul>
<li><p><span data-ttu-id="61d75-198">JET_bitColumnUserDefinedDefault können nicht zusammen mit JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero oder JET_bitColumnMaybeNull verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-198">JET_bitColumnUserDefinedDefault cannot be used in conjunction with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61d75-199">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="61d75-199">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="61d75-200">Bei der Spalte handelt es sich um eine Spalte zum Löschen von Spalten. Wenn Sie 0 (null) erreicht, wird der Datensatz gelöscht.</span><span class="sxs-lookup"><span data-stu-id="61d75-200">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="61d75-201">Eine gängige Verwendung für eine Spalte, die fertiggestellt werden kann, ist die Verwendung als Verweis Zähler Feld. wenn das Feld Null erreicht, wird der Datensatz gelöscht.</span><span class="sxs-lookup"><span data-stu-id="61d75-201">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="61d75-202">JET_bitColumnDeleteOnZero bezieht sich auf JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="61d75-202">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="61d75-203">Eine DELETE-on-Zero-Spalte muss eine Spalte für die hinterlegte Aktualisierung sein.</span><span class="sxs-lookup"><span data-stu-id="61d75-203">A Delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="61d75-204">JET_bitColumnDeleteOnZero können nicht mit JET_bitColumnFinalize verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-204">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="61d75-205">JET_bitColumnDeleteOnZero kann nicht mit benutzerdefinierten Standard Spalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61d75-205">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="61d75-206">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61d75-206">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61d75-207"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="61d75-207"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="61d75-208">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="61d75-208">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61d75-209"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="61d75-209"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="61d75-210">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="61d75-210">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61d75-211"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="61d75-211"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="61d75-212">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="61d75-212">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="61d75-213">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="61d75-213">See Also</span></span>

[<span data-ttu-id="61d75-214">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="61d75-214">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="61d75-215">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="61d75-215">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="61d75-216">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="61d75-216">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="61d75-217">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="61d75-217">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="61d75-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="61d75-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="61d75-219">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="61d75-219">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="61d75-220">Jetaddcolumn</span><span class="sxs-lookup"><span data-stu-id="61d75-220">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="61d75-221">Jetescrowupdate</span><span class="sxs-lookup"><span data-stu-id="61d75-221">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="61d75-222">Jetgettablecolumninfo</span><span class="sxs-lookup"><span data-stu-id="61d75-222">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="61d75-223">Jetopumtemptable</span><span class="sxs-lookup"><span data-stu-id="61d75-223">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="61d75-224">JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="61d75-224">JetOpenTempTable2</span></span>](./jetopentemptable2-function.md)  
[<span data-ttu-id="61d75-225">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="61d75-225">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)  
[<span data-ttu-id="61d75-226">Jetrenamecolumschlag</span><span class="sxs-lookup"><span data-stu-id="61d75-226">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
