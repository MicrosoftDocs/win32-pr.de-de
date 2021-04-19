---
description: 'Weitere Informationen finden Sie hier: JET_COLUMNCREATE Struktur'
title: JET_COLUMNCREATE-Struktur
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
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
ms.openlocfilehash: ee2d9d194a03cf575eb0296163526c1c50301cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363609"
---
# <a name="jet_columncreate-structure"></a><span data-ttu-id="6411b-103">JET_COLUMNCREATE-Struktur</span><span class="sxs-lookup"><span data-stu-id="6411b-103">JET_COLUMNCREATE Structure</span></span>


<span data-ttu-id="6411b-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6411b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columncreate-structure"></a><span data-ttu-id="6411b-105">JET_COLUMNCREATE-Struktur</span><span class="sxs-lookup"><span data-stu-id="6411b-105">JET_COLUMNCREATE Structure</span></span>

<span data-ttu-id="6411b-106">Die **JET_COLUMNCREATE** -Struktur beschreibt eine Spalte, die in einer Datenbank erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6411b-106">The **JET_COLUMNCREATE** structure describes a column to create in a database.</span></span>

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a><span data-ttu-id="6411b-107">Member</span><span class="sxs-lookup"><span data-stu-id="6411b-107">Members</span></span>

<span data-ttu-id="6411b-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="6411b-108">**cbStruct**</span></span>

<span data-ttu-id="6411b-109">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="6411b-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="6411b-110">Dieses Feld muss mit **sizeof (JET_COLUMNCREATE)** initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-110">This field must be initialized to **sizeof( JET_COLUMNCREATE )**.</span></span>

<span data-ttu-id="6411b-111">**szcolumnname**</span><span class="sxs-lookup"><span data-stu-id="6411b-111">**szColumnName**</span></span>

<span data-ttu-id="6411b-112">Der Name der zu erstellenden Spalte.</span><span class="sxs-lookup"><span data-stu-id="6411b-112">The name of the column to create.</span></span> <span data-ttu-id="6411b-113">Der Name muss die folgenden Kriterien erfüllen:</span><span class="sxs-lookup"><span data-stu-id="6411b-113">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="6411b-114">Es muss weniger als JET_cbNameMost Zeichen lang sein, ohne das abschließende Null-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6411b-114">It must be fewer than JET_cbNameMost characters in length, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="6411b-115">Sie darf nur Zeichen aus den folgenden Sätzen enthalten: 0 bis 9, A bis Z, A bis Z und alle anderen Interpunktions Punkte außer Ausrufezeichen ( \! ), Komma (,), öffnende eckige Klammer ( \[ ) und schließende Klammer ( \] ), d. h. ASCII-Zeichen 0x20, 0x22 bis 0x2D, 0x2F bis 0x5A, 0x5c, 0x5d bis 0x7F.</span><span class="sxs-lookup"><span data-stu-id="6411b-115">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="6411b-116">Er darf nicht mit einem Leerzeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="6411b-116">It cannot begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="6411b-117">Sie muss mindestens ein Zeichen enthalten, das kein Leerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="6411b-117">It must contain at least one non-space character.</span></span>

<span data-ttu-id="6411b-118">**colyp**</span><span class="sxs-lookup"><span data-stu-id="6411b-118">**coltyp**</span></span>

<span data-ttu-id="6411b-119">Der Typ der Spalte (z. b. "Text", "Binary" oder "Numerisch").</span><span class="sxs-lookup"><span data-stu-id="6411b-119">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="6411b-120">Weitere Informationen finden Sie unter [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="6411b-120">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="6411b-121">**cbmax**</span><span class="sxs-lookup"><span data-stu-id="6411b-121">**cbMax**</span></span>

<span data-ttu-id="6411b-122">Die maximale Länge einer Spalte variabler Länge in Bytes.</span><span class="sxs-lookup"><span data-stu-id="6411b-122">The maximum length, in bytes, of a variable-length column.</span></span> <span data-ttu-id="6411b-123">Die Länge der Spalte für Spalten mit fester Länge.</span><span class="sxs-lookup"><span data-stu-id="6411b-123">The length of the column for fixed-length columns.</span></span>

<span data-ttu-id="6411b-124">**grbit**</span><span class="sxs-lookup"><span data-stu-id="6411b-124">**grbit**</span></span>

<span data-ttu-id="6411b-125">Eine Gruppe von Bits, die die Optionen für diese-Struktur enthalten und die 0 (null) oder mehrere der folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="6411b-125">A group of bits that contain the options for this structure, and which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6411b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6411b-126">Value</span></span></p></th>
<th><p><span data-ttu-id="6411b-127">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6411b-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6411b-128">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="6411b-128">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="6411b-129">Die Spalte ist korrigiert.</span><span class="sxs-lookup"><span data-stu-id="6411b-129">The column is fixed.</span></span> <span data-ttu-id="6411b-130">Es wird immer die gleiche Menge an Speicherplatz in einer Zeile verwendet, unabhängig davon, wie viele Daten in der Spalte gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-130">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="6411b-131">JET_bitColumnFixed können nicht mit JET_bitColumnTagged verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-131">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="6411b-132">Dieses Bit kann nicht mit langen Werten wie <strong>JET_coltypLongText</strong> und <strong>JET_coltypLongBinary</strong>verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-132">This bit cannot be used with long values such as <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6411b-133">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="6411b-133">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="6411b-134">Die Spalte ist gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6411b-134">The column is tagged.</span></span> <span data-ttu-id="6411b-135">Markierte Spalten beanspruchen keinen Speicherplatz in der Datenbank, wenn Sie keine Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="6411b-135">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="6411b-136">Dieses Bit kann nicht mit JET_bitColumnFixed verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-136">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6411b-137">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="6411b-137">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="6411b-138">Die Spalte darf nie auf einen NULL-Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-138">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6411b-139">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="6411b-139">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="6411b-140">Die Spalte wird automatisch inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="6411b-140">The column is automatically incremented.</span></span> <span data-ttu-id="6411b-141">Die Zahl ist eine steigende Zahl, die in einer Tabelle garantiert eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="6411b-141">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="6411b-142">Die Zahl ist jedoch möglicherweise nicht kontinuierlich.</span><span class="sxs-lookup"><span data-stu-id="6411b-142">The number, however, might not be continuous.</span></span> <span data-ttu-id="6411b-143">Wenn z. b. fünf Zeilen in eine Tabelle eingefügt werden, kann die AutoIncrement-Spalte die Werte {1, 2, 6, 7, 8} enthalten.</span><span class="sxs-lookup"><span data-stu-id="6411b-143">For example, if five rows are inserted into a table, the autoincrement column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="6411b-144"><strong>Windows 2000:  </strong> Dieses Bit kann nur für Spalten vom Typ <strong>JET_coltypLong</strong>verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-144"><strong>Windows 2000:  </strong>This bit can be used only on columns of type <strong>JET_coltypLong</strong>.</span></span></p>
<p><span data-ttu-id="6411b-145"><strong>Windows Server 2003 und höher:  </strong> Dieses Bit kann nur für Spalten vom Typ <strong>JET_coltypLong</strong> oder <strong>JET_coltypCurrency</strong>verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-145"><strong>Windows Server 2003 and later:  </strong>This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6411b-146">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="6411b-146">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="6411b-147">Dieses Bit ist nur bei Aufrufen von <a href="gg269215(v=exchg.10).md">jetgetcolumninfo</a>gültig.</span><span class="sxs-lookup"><span data-stu-id="6411b-147">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6411b-148">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="6411b-148">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="6411b-149">Dieses Bit ist nur bei Aufrufen von <a href="gg269211(v=exchg.10).md">jetopentemptable</a>gültig.</span><span class="sxs-lookup"><span data-stu-id="6411b-149">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6411b-150">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="6411b-150">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="6411b-151">Dieses Bit ist nur bei Aufrufen von <a href="gg269211(v=exchg.10).md">jetopentemptable</a>gültig.</span><span class="sxs-lookup"><span data-stu-id="6411b-151">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6411b-152">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="6411b-152">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="6411b-153">Die Spalte kann mehr wertig sein.</span><span class="sxs-lookup"><span data-stu-id="6411b-153">The column can be multi-valued.</span></span> <span data-ttu-id="6411b-154">Für eine mehrwertige Spalte können NULL, ein oder mehrere Werte zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-154">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="6411b-155">Die verschiedenen Werte in einer mehrwertigen Spalte werden durch den <strong>itagsequence</strong> -Member verschiedener Strukturen identifiziert, z. b. <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="6411b-155">The various values in a multi-valued column are identified by the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="6411b-156">Mehrwertige Spalten müssen markierte Spalten sein. Das heißt, Sie können keine Spalten fester Länge oder Spalten mit variabler Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6411b-156">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6411b-157">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="6411b-157">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="6411b-158">Die Spalte ist eine Spalte zum Aktualisieren von Spalten.</span><span class="sxs-lookup"><span data-stu-id="6411b-158">The column is an escrow update column.</span></span> <span data-ttu-id="6411b-159">Eine Spalte für das Hinterlegungs Update kann gleichzeitig von verschiedenen Sitzungen mit <a href="gg294125(v=exchg.10).md">jetescrowupdate</a> aktualisiert werden und die Transaktions Konsistenz beibehalten.</span><span class="sxs-lookup"><span data-stu-id="6411b-159">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and maintain transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="6411b-160">Eine Spalte für das Hinterlegungs Update kann nur erstellt werden, wenn die Tabelle leer ist.</span><span class="sxs-lookup"><span data-stu-id="6411b-160">An escrow update column can be created only when the table is empty.</span></span></p></li>
<li><p><span data-ttu-id="6411b-161">Eine Spalte vom Typ "hinterlegter" muss vom Typ "JET_coltypLong" sein <strong>.</strong></span><span class="sxs-lookup"><span data-stu-id="6411b-161">An escrow update column must be of type <strong>JET_coltypLong.</strong></span></span></p></li>
<li><p><span data-ttu-id="6411b-162">Eine Spalte für das Hinterlegungs Update muss über einen Standardwert verfügen (" <strong>cbdefault</strong> " muss positiv sein).</span><span class="sxs-lookup"><span data-stu-id="6411b-162">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
<li><p><span data-ttu-id="6411b-163">JET_bitColumnEscrowUpdate kann nicht in Verbindung mit den folgenden Konstanten verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="6411b-163">JET_bitColumnEscrowUpdate cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="6411b-164">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="6411b-164">JET_bitColumnTagged</span></span></p></li>
<li><p><span data-ttu-id="6411b-165">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="6411b-165">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="6411b-166">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="6411b-166">JET_bitColumnAutoincrement</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6411b-167">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="6411b-167">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="6411b-168">Die Spalte wird ohne eine Version erstellt.</span><span class="sxs-lookup"><span data-stu-id="6411b-168">The column is created without a version.</span></span> <span data-ttu-id="6411b-169">Bei anderen Transaktionen, die versuchen, eine Spalte mit demselben Namen hinzuzufügen, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="6411b-169">Other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="6411b-170">Dieses Bit ist nur bei <a href="gg294122(v=exchg.10).md">jetaddcolumn</a>nützlich.</span><span class="sxs-lookup"><span data-stu-id="6411b-170">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="6411b-171">Sie kann nicht innerhalb einer Transaktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-171">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6411b-172">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="6411b-172">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="6411b-173">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="6411b-173">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6411b-174">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="6411b-174">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="6411b-175">Verwenden Sie JET_bitColumnDeleteOnZero anstelle von JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="6411b-175">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="6411b-176">JET_bitColumnFinalize gibt an, dass eine Spalte fertiggestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6411b-176">JET_bitColumnFinalize specifies that a column can be finalized.</span></span> <span data-ttu-id="6411b-177">Wenn eine Spalte, die abgeschlossen werden kann, eine Spalte mit dem Wert "hinterlegter Update" aufweist, die Null erreicht, wird die Zeile gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6411b-177">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="6411b-178">Zukünftige Versionen können stattdessen eine Rückruffunktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6411b-178">Future versions can invoke a callback function instead.</span></span> <span data-ttu-id="6411b-179">Weitere Informationen finden Sie unter <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="6411b-179">For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="6411b-180">Eine Spalte, die abgeschlossen werden kann, muss eine Spalte für die hinterlegte Aktualisierung sein.</span><span class="sxs-lookup"><span data-stu-id="6411b-180">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="6411b-181">JET_bitColumnFinalize können nicht mit JET_bitColumnUserDefinedDefault verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-181">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6411b-182">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="6411b-182">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="6411b-183">Der Standardwert für eine Spalte wird von der Rückruffunktion <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6411b-183">The default value for a column is provided by the callback function, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="6411b-184">Eine Spalte, die über einen benutzerdefinierten Standardwert verfügt, muss eine markierte Spalte sein.</span><span class="sxs-lookup"><span data-stu-id="6411b-184">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="6411b-185"><strong>pvdefault</strong> muss auf eine <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> Struktur verweisen, und <strong>cbdefault</strong> muss auf sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-185"><strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p>
<p><span data-ttu-id="6411b-186">JET_bitColumnUserDefinedDefault kann nicht in Verbindung mit den folgenden Konstanten verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="6411b-186">JET_bitColumnUserDefinedDefault cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="6411b-187">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="6411b-187">JET_bitColumnFixed</span></span></p></li>
<li><p><span data-ttu-id="6411b-188">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="6411b-188">JET_bitColumnNotNULL</span></span></p></li>
<li><p><span data-ttu-id="6411b-189">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="6411b-189">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="6411b-190">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="6411b-190">JET_bitColumnAutoincrement</span></span></p></li>
<li><p><span data-ttu-id="6411b-191">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="6411b-191">JET_bitColumnUpdatable</span></span></p></li>
<li><p><span data-ttu-id="6411b-192">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="6411b-192">JET_bitColumnEscrowUpdate</span></span></p></li>
<li><p><span data-ttu-id="6411b-193">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="6411b-193">JET_bitColumnFinalize</span></span></p></li>
<li><p><span data-ttu-id="6411b-194">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="6411b-194">JET_bitColumnDeleteOnZero</span></span></p></li>
<li><p><span data-ttu-id="6411b-195">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="6411b-195">JET_bitColumnMaybeNull</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6411b-196">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="6411b-196">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="6411b-197">Bei der Spalte handelt es sich um eine Spalte zum Löschen von Spalten. Wenn Sie 0 (null) erreicht, wird der Datensatz gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6411b-197">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="6411b-198">Eine gängige Verwendung für eine Spalte, die fertiggestellt werden kann, ist die Verwendung als Verweis Zähler Feld. wenn das Feld Null erreicht, wird der Datensatz gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6411b-198">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="6411b-199">JET_bitColumnDeleteOnZero bezieht sich auf JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="6411b-199">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="6411b-200">Eine DELETE-on-Zero-Spalte muss eine Spalte für die hinterlegte Aktualisierung sein.</span><span class="sxs-lookup"><span data-stu-id="6411b-200">A delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="6411b-201">JET_bitColumnDeleteOnZero können nicht mit JET_bitColumnFinalize verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-201">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="6411b-202">JET_bitColumnDeleteOnZero kann nicht mit benutzerdefinierten Standard Spalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-202">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6411b-203">**pvdefault**</span><span class="sxs-lookup"><span data-stu-id="6411b-203">**pvDefault**</span></span>

<span data-ttu-id="6411b-204">Verweist auf einen Puffer, bei dem es sich um den Standardwert für eine Spalte handelt.</span><span class="sxs-lookup"><span data-stu-id="6411b-204">Points to a buffer which will be the default value for a column.</span></span> <span data-ttu-id="6411b-205">Die Länge des Puffers ist **cbdefault**.</span><span class="sxs-lookup"><span data-stu-id="6411b-205">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="6411b-206">Wenn kein Standardwert vorhanden ist, sollte **pvdefault** auf NULL festgelegt werden, und **cbdefault** sollte auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6411b-206">If there is no default, **pvDefault** should be set to NULL and **cbDefault** should be set to zero.</span></span> <span data-ttu-id="6411b-207">Wenn *grbit* JET_bitColumnUserDefinedDefault festgelegt ist, wird **pvdefault** als Zeiger auf eine JET_USERDEFINEDDEFAULT Struktur interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6411b-207">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a JET_USERDEFINEDDEFAULT structure.</span></span> <span data-ttu-id="6411b-208">Standardwerte dürfen nicht größer als 255 Bytes sein.</span><span class="sxs-lookup"><span data-stu-id="6411b-208">Default values cannot be larger than 255 bytes.</span></span> <span data-ttu-id="6411b-209">Wenn ein Standardwert größer als 255 Bytes ist, wird er automatisch abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="6411b-209">If a default value is larger than 255 bytes, it will be silently truncated.</span></span>

<span data-ttu-id="6411b-210">**cbdefault**</span><span class="sxs-lookup"><span data-stu-id="6411b-210">**cbDefault**</span></span>

<span data-ttu-id="6411b-211">Die Größe (in Bytes) des Puffers, der von **pvdefault** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6411b-211">The size, in bytes, of the buffer specified by **pvDefault**.</span></span>

<span data-ttu-id="6411b-212">**cp**</span><span class="sxs-lookup"><span data-stu-id="6411b-212">**cp**</span></span>

<span data-ttu-id="6411b-213">Die Codepage für die Spalte.</span><span class="sxs-lookup"><span data-stu-id="6411b-213">The code page for the column.</span></span> <span data-ttu-id="6411b-214">Die einzigen gültigen Werte für Textspalten sind Englisch (1252) und Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="6411b-214">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="6411b-215">Der Wert 0 (null) bedeutet, dass der Standardwert verwendet wird (English, 1252).</span><span class="sxs-lookup"><span data-stu-id="6411b-215">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="6411b-216">Handelt es sich bei der Spalte nicht um eine Text Spalte, wird die Codepage automatisch auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6411b-216">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="6411b-217">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="6411b-217">**columnid**</span></span>

<span data-ttu-id="6411b-218">Bei Erfolg wird der Spalten Bezeichner der neu erstellten Spalte in diesem Feld zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6411b-218">On success, the column identifier of the newly-created column will be passed back in this field.</span></span> <span data-ttu-id="6411b-219">Bei einem Fehler ist der Wert nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="6411b-219">On failure, the value is undefined.</span></span>

<span data-ttu-id="6411b-220">**irre**</span><span class="sxs-lookup"><span data-stu-id="6411b-220">**err**</span></span>

<span data-ttu-id="6411b-221">Das **Err** -Feld enthält den Status, in dem diese Spalte erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6411b-221">The **err** field will contain the status of creating this column.</span></span> <span data-ttu-id="6411b-222">Eine Liste der wahrscheinlichen Rückgabewerte finden Sie unter [jetaddcolumn](./jetaddcolumn-function.md) .</span><span class="sxs-lookup"><span data-stu-id="6411b-222">See [JetAddColumn](./jetaddcolumn-function.md) for a list of likely return values.</span></span>

### <a name="requirements"></a><span data-ttu-id="6411b-223">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6411b-223">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6411b-224"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6411b-224"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6411b-225">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6411b-225">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6411b-226"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6411b-226"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6411b-227">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6411b-227">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6411b-228"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6411b-228"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6411b-229">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="6411b-229">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6411b-230"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6411b-230"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6411b-231">Wird als <strong>JET_COLUMNCREATE_W</strong> (Unicode) und <strong>JET_COLUMNCREATE_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="6411b-231">Implemented as <strong>JET_COLUMNCREATE_W</strong> (Unicode) and <strong>JET_COLUMNCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="6411b-232">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6411b-232">See Also</span></span>

[<span data-ttu-id="6411b-233">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="6411b-233">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="6411b-234">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="6411b-234">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="6411b-235">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6411b-235">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6411b-236">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6411b-236">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6411b-237">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="6411b-237">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="6411b-238">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="6411b-238">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="6411b-239">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="6411b-239">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="6411b-240">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="6411b-240">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="6411b-241">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="6411b-241">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="6411b-242">Jetaddcolumn</span><span class="sxs-lookup"><span data-stu-id="6411b-242">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="6411b-243">Jetkreatetablecolumnindex</span><span class="sxs-lookup"><span data-stu-id="6411b-243">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="6411b-244">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="6411b-244">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="6411b-245">Jetescrowupdate</span><span class="sxs-lookup"><span data-stu-id="6411b-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="6411b-246">Jetrenamecolumschlag</span><span class="sxs-lookup"><span data-stu-id="6411b-246">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)  
[<span data-ttu-id="6411b-247">Jetsetcolumns</span><span class="sxs-lookup"><span data-stu-id="6411b-247">JetSetColumns</span></span>](./jetsetcolumns-function.md)
