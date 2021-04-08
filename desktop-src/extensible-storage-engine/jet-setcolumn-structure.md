---
description: 'Weitere Informationen finden Sie hier: JET_SETCOLUMN Struktur'
title: JET_SETCOLUMN Struktur
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
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
ms.openlocfilehash: a170132fd4d832133e0f0bcad4a3499fa743db38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750520"
---
# <a name="jet_setcolumn-structure"></a><span data-ttu-id="49048-103">JET_SETCOLUMN Struktur</span><span class="sxs-lookup"><span data-stu-id="49048-103">JET_SETCOLUMN Structure</span></span>


<span data-ttu-id="49048-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="49048-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setcolumn-structure"></a><span data-ttu-id="49048-105">JET_SETCOLUMN Struktur</span><span class="sxs-lookup"><span data-stu-id="49048-105">JET_SETCOLUMN Structure</span></span>

<span data-ttu-id="49048-106">Die **JET_SETCOLUMN** -Struktur enthält Eingabe-und Ausgabeparameter für [jetsetcolumns](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="49048-106">The **JET_SETCOLUMN** structure contains input and output parameters for [JetSetColumns](./jetsetcolumns-function.md).</span></span> <span data-ttu-id="49048-107">Felder in der Struktur beschreiben, welcher Spaltenwert festgelegt werden soll, wie er festgelegt wird und wo die Spalten Satz Daten zu finden sind.</span><span class="sxs-lookup"><span data-stu-id="49048-107">Fields in the structure describe what column value to set, how to set it, and where to get the column set data.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a><span data-ttu-id="49048-108">Member</span><span class="sxs-lookup"><span data-stu-id="49048-108">Members</span></span>

<span data-ttu-id="49048-109">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="49048-109">**columnid**</span></span>

<span data-ttu-id="49048-110">Der Spalten Bezeichner für eine Spalte, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="49048-110">The column identifier for a column to set.</span></span>

<span data-ttu-id="49048-111">**pvData**</span><span class="sxs-lookup"><span data-stu-id="49048-111">**pvData**</span></span>

<span data-ttu-id="49048-112">Ein Zeiger auf Daten, die in eine Spalte festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="49048-112">A pointer to data to set into a column.</span></span>

<span data-ttu-id="49048-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="49048-113">**cbData**</span></span>

<span data-ttu-id="49048-114">Die Größe der Zuordnung in Bytes, beginnend bei **pvData** (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="49048-114">The size of allocation, in bytes, starting at **pvData** in bytes.</span></span>

<span data-ttu-id="49048-115">**grbit**</span><span class="sxs-lookup"><span data-stu-id="49048-115">**grbit**</span></span>

<span data-ttu-id="49048-116">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="49048-116">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49048-117">Wert</span><span class="sxs-lookup"><span data-stu-id="49048-117">Value</span></span></p></th>
<th><p><span data-ttu-id="49048-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="49048-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49048-119">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="49048-119">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="49048-120">Fügt Daten an eine Spalte vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>an.</span><span class="sxs-lookup"><span data-stu-id="49048-120">Appends data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="49048-121">Das gleiche Verhalten können Sie erreichen, indem Sie die Größe des vorhandenen Long-Werts ermitteln und <strong>iblongvalue</strong> in <strong>psetup</strong>angeben.</span><span class="sxs-lookup"><span data-stu-id="49048-121">The same behavior can be achieved by determining the size of the existing long value and specifying <strong>ibLongValue</strong> in <strong>psetinfo</strong>.</span></span> <span data-ttu-id="49048-122">Es ist jedoch einfacher, dieses <em>grbit</em>zu verwenden, da das Wissen der Größe des vorhandenen Spaltenwerts nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="49048-122">However, it's simpler to use this <em>grbit</em>, since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49048-123">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="49048-123">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="49048-124">Ersetzt den vorhandenen Long-Wert durch die neuen Daten.</span><span class="sxs-lookup"><span data-stu-id="49048-124">Replaces the existing long value with the new data.</span></span> <span data-ttu-id="49048-125">Wenn diese Option verwendet wird, ist es so, als ob der vorhandene Long-Wert auf 0 (null) festgelegt wurde, bevor die neuen Daten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="49048-125">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49048-126">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="49048-126">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="49048-127">Interpretiert den Eingabepuffer als ganzzahlige Anzahl von Bytes, die als Länge des Long-Werts festgelegt werden soll, der durch das angegebene ColumnID und ggf. die Sequenznummer in psetinfo- &gt; itagsequence beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="49048-127">Interprets the input buffer as an integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="49048-128">Wenn die angegebene Größe größer ist als der vorhandene Spaltenwert, wird die Spalte um 0s erweitert.</span><span class="sxs-lookup"><span data-stu-id="49048-128">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="49048-129">Wenn die Größe kleiner als der vorhandene Spaltenwert ist, wird der Wert abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="49048-129">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49048-130">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="49048-130">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="49048-131">Legt einen Wert auf die Länge 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="49048-131">Sets a value to zero length.</span></span> <span data-ttu-id="49048-132">Normalerweise wird ein Spaltenwert auf NULL festgelegt, indem ein cbmax von 0 übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="49048-132">Normally, a column value is set to NULL by passing a cbMax of 0.</span></span> <span data-ttu-id="49048-133">Bei manchen Typen, wie z. b. <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, kann ein Spaltenwert jedoch eine Länge von 0 (null) und nicht NULL sein, und diese Option wird verwendet, um zwischen null und 0 zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="49048-133">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 length instead of NULL, and this option is used to differentiate between NULL and 0 length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49048-134">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="49048-134">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="49048-135">Erzwingt, dass ein langer Wert, Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>getrennt vom Rest der Daten Satz Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="49048-135">Forces a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="49048-136">Dies tritt normalerweise auf, wenn die Größe des Long-Werts verhindert, dass Sie mit den verbleibenden Daten Satz Daten gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="49048-136">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="49048-137">Diese Option kann jedoch verwendet werden, um zu erzwingen, dass der lange Wert separat gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="49048-137">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="49048-138">Beachten Sie, dass lange Werte, die vier Bytes groß oder kleiner sind, nicht getrennt werden können.</span><span class="sxs-lookup"><span data-stu-id="49048-138">Note that long values four bytes in size or smaller cannot be forced to be separate.</span></span> <span data-ttu-id="49048-139">In solchen Fällen wird die Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="49048-139">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49048-140">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="49048-140">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="49048-141">Erzwingt unterschiedliche Werte in einer mehrwertigen Spalte.</span><span class="sxs-lookup"><span data-stu-id="49048-141">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="49048-142">Mit dieser Option werden die Quell Spaltendaten ohne Transformationen mit anderen vorhandenen Spaltenwerten verglichen, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="49048-142">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="49048-143">Wenn diese Option angegeben wird, können JET_bitSetAppendLv, JET_bitSetOverwriteLV und JET_bitSetSizeLV nicht ebenfalls angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="49048-143">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49048-144">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="49048-144">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="49048-145">Erzwingt unterschiedliche Werte in einer mehrwertigen Spalte.</span><span class="sxs-lookup"><span data-stu-id="49048-145">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="49048-146">Mit dieser Option wird die normalisierte Transformation von Spaltendaten mit anderen ähnlich transformierten vorhandenen Spaltenwerten verglichen, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="49048-146">This option compares the key normalized transformation of column data to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="49048-147">Wenn diese Option angegeben wird, können JET_bitSetAppendLv, JET_bitSetOverwriteLV und JET_bitSetSizeLV nicht ebenfalls angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="49048-147">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49048-148">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="49048-148">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="49048-149">Bewirkt, dass die Spalte für nachfolgende Vorgänge zum Abrufen von Spalten den Standard Spaltenwert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="49048-149">Causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="49048-150">Alle vorhandenen Spaltenwerte werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="49048-150">All existing column values are removed.</span></span> <span data-ttu-id="49048-151">Diese Option gilt nur für gekennzeichnete, sparsespalten oder mehrwertige Spalten.</span><span class="sxs-lookup"><span data-stu-id="49048-151">This option is only applicable for tagged, sparse, or multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49048-152">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="49048-152">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="49048-153">Behält den langen Wert, Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder JET_coltypeLongBinary bei Bedarf mit den verbleibenden Daten Satz Daten.</span><span class="sxs-lookup"><span data-stu-id="49048-153">Keeps the long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or JET_coltypeLongBinary, stored with the remaining record data if possible.</span></span> <span data-ttu-id="49048-154">Normalerweise werden lange Spalten separat gespeichert, wenn Ihre Länge 1024 Bytes überschreitet oder andernfalls die Daten Satz Länge die Größe der Größenbeschränkung auf Seitengröße überschreiten würde.</span><span class="sxs-lookup"><span data-stu-id="49048-154">Normally, long columns are stored separately when their length exceeds 1024 bytes or would otherwise cause the record length to exceed its page size related size limitation.</span></span> <span data-ttu-id="49048-155">Wenn diese Option festgelegt ist, schlägt der Vorgang zum Festlegen von Spalten jedoch mit einem Fehler JET_errColumnTooBig fehl, anstatt diesen Spaltenwert getrennt von den verbleibenden Daten Satz Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="49048-155">However, if this option is set, the set column operation will fail with error JET_errColumnTooBig rather than store this column value separate from the remaining record data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49048-156">**iblongvalue**</span><span class="sxs-lookup"><span data-stu-id="49048-156">**ibLongValue**</span></span>

<span data-ttu-id="49048-157">Der Offset zum ersten Byte, der aus einer Spalte vom Typ [JET_coltypLongBinary](./jet-coltyp.md)abgerufen werden soll, oder [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="49048-157">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="49048-158">**itagsequence**</span><span class="sxs-lookup"><span data-stu-id="49048-158">**itagSequence**</span></span>

<span data-ttu-id="49048-159">Beschreibt die Sequenznummer des Werts in einer mehrwertigen Spalte.</span><span class="sxs-lookup"><span data-stu-id="49048-159">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="49048-160">Eine **itagsequence** von 0 gibt an, dass der festgelegte Spaltenwert als neue Instanz einer mehrwertigen Spalte hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="49048-160">An **itagSequence** of 0 indicates that the column value set should be added as a new instance of a multi-valued column.</span></span>

<span data-ttu-id="49048-161">**irre**</span><span class="sxs-lookup"><span data-stu-id="49048-161">**err**</span></span>

<span data-ttu-id="49048-162">Fehlercodes und Warnungen, die vom Vorgang zum Festlegen der Spalte zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="49048-162">Error codes and warnings returned from the set column operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="49048-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49048-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49048-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="49048-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="49048-165">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="49048-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49048-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="49048-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="49048-167">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="49048-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49048-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="49048-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="49048-169">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="49048-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="49048-170">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="49048-170">See Also</span></span>

[<span data-ttu-id="49048-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="49048-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="49048-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="49048-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="49048-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="49048-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="49048-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="49048-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="49048-175">Jetsetcolumns</span><span class="sxs-lookup"><span data-stu-id="49048-175">JetSetColumns</span></span>](./jetsetcolumns-function.md)
