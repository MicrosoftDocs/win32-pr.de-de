---
description: 'Weitere Informationen über: jetsetcolumn-Funktion'
title: JetSetColumn-Funktion
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c1fd267bea6bbb995a13ce65f97f1f531572a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347800"
---
# <a name="jetsetcolumn-function"></a><span data-ttu-id="abb0a-103">JetSetColumn-Funktion</span><span class="sxs-lookup"><span data-stu-id="abb0a-103">JetSetColumn Function</span></span>


<span data-ttu-id="abb0a-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="abb0a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumn-function"></a><span data-ttu-id="abb0a-105">JetSetColumn-Funktion</span><span class="sxs-lookup"><span data-stu-id="abb0a-105">JetSetColumn Function</span></span>

<span data-ttu-id="abb0a-106">Die **jetsetcolumn** -Funktion ändert den Wert einer einzelnen Spalte in einem geänderten Datensatz, um eingefügt zu werden, oder um den aktuellen Datensatz zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="abb0a-106">The **JetSetColumn** function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="abb0a-107">Es kann einen vorhandenen Wert überschreiben, einen neuen Wert zu einer Sequenz von Werten in einer mehrwertigen Spalte hinzufügen, einen Wert aus einer Sequenz von Werten in einer mehrwertigen Spalte entfernen oder den gesamten oder einen Teil eines Long-Werts aktualisieren, eine Spalte vom Typ [JET_coltypLongText](./jet-coltyp.md) oder [JET_coltypLongBinary](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="abb0a-107">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value, a column of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="abb0a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="abb0a-108">Parameters</span></span>

<span data-ttu-id="abb0a-109">*-sid*</span><span class="sxs-lookup"><span data-stu-id="abb0a-109">*sesid*</span></span>

<span data-ttu-id="abb0a-110">Die Sitzung, die für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="abb0a-110">The session to use for this call.</span></span>

<span data-ttu-id="abb0a-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="abb0a-111">*tableid*</span></span>

<span data-ttu-id="abb0a-112">Der Cursor, der für diesen-Befehl verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="abb0a-112">The cursor to use for this call.</span></span>

<span data-ttu-id="abb0a-113">*ColumnID*</span><span class="sxs-lookup"><span data-stu-id="abb0a-113">*columnid*</span></span>

<span data-ttu-id="abb0a-114">Der [JET_COLUMNID](./jet-columnid.md) der Spalte, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="abb0a-114">The [JET_COLUMNID](./jet-columnid.md) of the column to be retrieved.</span></span> <span data-ttu-id="abb0a-115">Alternativ kann ein *ColumnID* -Wert von 0 (null) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="abb0a-115">Alternatively, a *columnid* value of 0 (zero) can be given.</span></span> <span data-ttu-id="abb0a-116">Wenn *ColumnID* 0 (null) angegeben wird, werden alle markierten Spalten, Spalten mit geringer Dichte und mehrwertigen Spalten als einzelne Spalte behandelt.</span><span class="sxs-lookup"><span data-stu-id="abb0a-116">When *columnid* 0 (zero) is given, all tagged columns, sparse and multi-valued columns, are treated as a single column.</span></span> <span data-ttu-id="abb0a-117">Dadurch wird das Abrufen aller sparsespalten ermöglicht, die in einem Datensatz vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="abb0a-117">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="abb0a-118">*pvData*</span><span class="sxs-lookup"><span data-stu-id="abb0a-118">*pvData*</span></span>

<span data-ttu-id="abb0a-119">Eingabepuffer, der Daten enthält, die für den Spaltenwert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abb0a-119">Input buffer containing data to use for column value.</span></span>

<span data-ttu-id="abb0a-120">*cbData*</span><span class="sxs-lookup"><span data-stu-id="abb0a-120">*cbData*</span></span>

<span data-ttu-id="abb0a-121">Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="abb0a-121">Size in bytes of the input buffer.</span></span>

<span data-ttu-id="abb0a-122">*grbit*</span><span class="sxs-lookup"><span data-stu-id="abb0a-122">*grbit*</span></span>

<span data-ttu-id="abb0a-123">Eine Gruppe von Bits, die die für diesen-Befehl zu verwendenden Optionen enthalten, die NULL oder mehr der folgenden Elemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="abb0a-123">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="abb0a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="abb0a-124">Value</span></span></p></th>
<th><p><span data-ttu-id="abb0a-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="abb0a-125">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-126">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="abb0a-126">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="abb0a-127">Diese Option wird zum Anfügen von Daten an eine Spalte vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>verwendet.</span><span class="sxs-lookup"><span data-stu-id="abb0a-127">This option is used to append data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="abb0a-128">Das gleiche Verhalten können Sie erreichen, indem Sie die Größe des vorhandenen Long-Werts ermitteln und <em>iblongvalue</em> in <em>psetup</em>angeben.</span><span class="sxs-lookup"><span data-stu-id="abb0a-128">The same behavior can be achieved by determining the size of the existing long value and specifying <em>ibLongValue</em> in <em>psetinfo</em>.</span></span> <span data-ttu-id="abb0a-129">Es ist jedoch einfacher, dieses <em>grbit</em> zu verwenden, da es nicht erforderlich ist, die Größe des vorhandenen Spaltenwerts zu kennen.</span><span class="sxs-lookup"><span data-stu-id="abb0a-129">However, it's simpler to use this <em>grbit</em> since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-130">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="abb0a-130">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="abb0a-131">Diese Option wird verwendet, um den vorhandenen Long-Wert durch die neu bereitgestellten Daten zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="abb0a-131">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="abb0a-132">Wenn diese Option verwendet wird, ist es so, als ob der vorhandene Long-Wert auf 0 (null) festgelegt wurde, bevor die neuen Daten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="abb0a-132">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-133">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="abb0a-133">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="abb0a-134">Diese Option gilt nur für markierte, Spalten mit geringer Dichte oder mehrwertige Spalten.</span><span class="sxs-lookup"><span data-stu-id="abb0a-134">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="abb0a-135">Dies bewirkt, dass die Spalte bei nachfolgenden Spalten Abruf Vorgängen den Standard Spaltenwert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="abb0a-135">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="abb0a-136">Alle vorhandenen Spaltenwerte werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="abb0a-136">All existing column values are removed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-137">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="abb0a-137">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="abb0a-138">Diese Option wird verwendet, um zu erzwingen, dass ein langer Wert, Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>getrennt vom Rest der Daten Satz Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="abb0a-138">This option is used to force a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="abb0a-139">Dies tritt normalerweise auf, wenn die Größe des Long-Werts verhindert, dass Sie mit den verbleibenden Daten Satz Daten gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-139">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="abb0a-140">Diese Option kann jedoch verwendet werden, um zu erzwingen, dass der lange Wert separat gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-140">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="abb0a-141">Beachten Sie, dass lange Werte mit einer Größe von vier Bytes, die kleiner als getrennt sind, nicht erzwungen werden können.</span><span class="sxs-lookup"><span data-stu-id="abb0a-141">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="abb0a-142">In solchen Fällen wird die Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="abb0a-142">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-143">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="abb0a-143">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="abb0a-144">Diese Option wird verwendet, um den Eingabepuffer als ganzzahlige Anzahl von Bytes zu interpretieren, die als Länge des Long-Werts festgelegt werden, der durch das angegebene <em>ColumnID</em> und ggf. die Sequenznummer in psetinfo- &gt; itagsequence beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-144">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given <em>columnid</em> and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="abb0a-145">Wenn die angegebene Größe größer ist als der vorhandene Spaltenwert, wird die Spalte um 0s erweitert.</span><span class="sxs-lookup"><span data-stu-id="abb0a-145">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="abb0a-146">Wenn die Größe kleiner als der vorhandene Spaltenwert ist, wird der Wert abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="abb0a-146">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-147">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="abb0a-147">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="abb0a-148">Diese Option wird verwendet, um zu erzwingen, dass alle Werte in einer mehrwertigen Spalte voneinander abweichen.</span><span class="sxs-lookup"><span data-stu-id="abb0a-148">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="abb0a-149">Mit dieser Option werden die Quell Spaltendaten ohne Transformationen mit anderen vorhandenen Spaltenwerten verglichen, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-149">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="abb0a-150">Wenn diese Option angegeben wird, können JET_bitSetAppendLV, JET_bitSetOverwriteLV und JET_bitSetSizeLV nicht ebenfalls angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="abb0a-150">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-151">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="abb0a-151">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="abb0a-152">Diese Option wird verwendet, um zu erzwingen, dass alle Werte in einer mehrwertigen Spalte voneinander abweichen.</span><span class="sxs-lookup"><span data-stu-id="abb0a-152">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="abb0a-153">Mit dieser Option wird die normalisierte Transformation von Spaltendaten mit anderen ähnlich transformierten vorhandenen Spaltenwerten verglichen, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-153">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="abb0a-154">Wenn diese Option angegeben wird, können JET_bitSetAppendLV, JET_bitSetOverwriteLV und JET_bitSetSizeLV nicht ebenfalls angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="abb0a-154">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-155">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="abb0a-155">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="abb0a-156">Diese Option wird verwendet, um einen Wert auf die Länge 0 (null) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="abb0a-156">This option is used to set a value to zero length.</span></span> <span data-ttu-id="abb0a-157">Normalerweise wird ein Spaltenwert auf <strong>null</strong> festgelegt, indem ein cbmax-Wert von 0 (null) übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-157">Normally, a column value is set to <strong>NULL</strong> by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="abb0a-158">Bei manchen Typen, wie z. b. <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, kann ein Spaltenwert jedoch eine Länge von 0 (null) anstelle von <strong>null</strong>sein, und diese Option wird verwendet, um zwischen <strong>null</strong> und 0 (null) zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="abb0a-158">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 (zero) length instead of <strong>NULL</strong>, and this option is used to differentiate between <strong>NULL</strong> and 0 (zero) length.</span></span></p>
<p><span data-ttu-id="abb0a-159"><strong>Hinweis</strong>  Im Allgemeinen wird dieses Bit ignoriert, wenn die Spalte eine Spalte mit fester Länge ist und die Spalte auf <strong>null</strong>festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="abb0a-159"><strong>Note</strong>  In general, if the column is a fixed-length column, this bit is ignored and the column is set to <strong>NULL</strong>.</span></span> <span data-ttu-id="abb0a-160">Wenn die Spalte jedoch eine markierte Spalte mit fester Länge ist, wird die Länge der Spalte auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="abb0a-160">However, if the column is a fixed-length tagged column, the column length is set to 0.</span></span> <span data-ttu-id="abb0a-161">Wenn die markierte Spalte mit fester Länge auf 0 (null) festgelegt ist, wird versucht, die Spalte mit <a href="gg269198(v=exchg.10).md">jetretrievecolumschlag</a> oder <a href="gg294135(v=exchg.10).md">jetretrievecolumschlag</a> abzurufen, aber die tatsächliche Länge, die im <em>cbactual</em> -Parameter zurückgegeben wird, ist 0.</span><span class="sxs-lookup"><span data-stu-id="abb0a-161">When the fixed-length tagged column is set to 0 length, attempts to retrieve the column with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> will succeed, but the actual length that is returned in the <em>cbActual</em> parameter is 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-162">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="abb0a-162">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="abb0a-163">Diese Option wird verwendet, um den gesamten Long-Wert im Datensatz zu speichern.</span><span class="sxs-lookup"><span data-stu-id="abb0a-163">This option is used to store the entire long value in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-164">JET_bitSetCompressed</span><span class="sxs-lookup"><span data-stu-id="abb0a-164">JET_bitSetCompressed</span></span></p></td>
<td><p><span data-ttu-id="abb0a-165">Diese Option wird verwendet, um die Datenkomprimierung beim Speichern der Daten zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="abb0a-165">This option is used to attempt data compression when storing the data.</span></span></p>
<p><span data-ttu-id="abb0a-166"><strong>Windows 7:</strong>  JET_bitSetCompressed wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="abb0a-166"><strong>Windows 7:</strong>  JET_bitSetCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-167">JET_bitSetUncompressed</span><span class="sxs-lookup"><span data-stu-id="abb0a-167">JET_bitSetUncompressed</span></span></p></td>
<td><p><span data-ttu-id="abb0a-168">Diese Option wird verwendet, wenn beim Speichern der Daten keine Komprimierung versucht wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-168">This option is used not attempt compression when storing the data.</span></span></p>
<p><span data-ttu-id="abb0a-169"><strong>Windows 7:</strong>  JET_bitSetUnCompressed wurde in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="abb0a-169"><strong>Windows 7:</strong>  JET_bitSetUnCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="abb0a-170">*psetup-Info*</span><span class="sxs-lookup"><span data-stu-id="abb0a-170">*psetinfo*</span></span>

<span data-ttu-id="abb0a-171">Zeiger auf optionale Eingabeparameter, die für diese Funktion mithilfe der [JET_SETINFO](./jet-setinfo-structure.md) Struktur festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="abb0a-171">Pointer to optional input parameters that can be set for this function using the [JET_SETINFO](./jet-setinfo-structure.md) structure.</span></span>

<span data-ttu-id="abb0a-172">Wenn *psetinfo* als **null** angegeben wird, verhält sich die Funktion so, als ob eine *itagsequence* von 1 und ein *iblongvalue-Wert* von 0 (null) angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="abb0a-172">If *psetinfo* is given as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="abb0a-173">Dies bewirkt, dass der erste Wert einer mehrwertigen Spalte von Spalten Satz festgelegt wird und lange Daten beginnend am Offset 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="abb0a-173">This causes column set to set the first value of a multi-valued column, and to set long data beginning at offset 0 (zero).</span></span>

<span data-ttu-id="abb0a-174">Die folgenden Optionen können für diesen Parameter festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="abb0a-174">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="abb0a-175">Wert</span><span class="sxs-lookup"><span data-stu-id="abb0a-175">Value</span></span></p></th>
<th><p><span data-ttu-id="abb0a-176">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="abb0a-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-177">iblongvalue</span><span class="sxs-lookup"><span data-stu-id="abb0a-177">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="abb0a-178">Binärer Offset in einen Long-Spaltenwert, in dem Set Data beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="abb0a-178">Binary offset into a long column value where set data should begin.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-179">itagsequence</span><span class="sxs-lookup"><span data-stu-id="abb0a-179">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="abb0a-180">Die Sequenznummer des gewünschten Werts der mehrwertigen Spalte, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="abb0a-180">Sequence number of the desired multi-valued column value to set.</span></span> <span data-ttu-id="abb0a-181">Wenn <em>itagsequence</em> auf 0 (null) festgelegt ist, sollte der angegebene Wert an das Ende der Sequenz von mehrwertigen Werten angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="abb0a-181">If <em>itagSequence</em> is set to 0 (zero), then the value provided should be appended to then end of the sequence of multi-valued values.</span></span> <span data-ttu-id="abb0a-182">Wenn die angegebene Sequenznummer größer als der letzte vorhandene mehrwertige Wert ist, wird der angegebene Wert erneut an das Ende der Sequenz von Werten angehängt.</span><span class="sxs-lookup"><span data-stu-id="abb0a-182">If the sequence number provided is greater than the last existing multi-valued value, then again the given value is appended to the end of the sequence of values.</span></span> <span data-ttu-id="abb0a-183">Wenn die Sequenznummer einem vorhandenen Wert entspricht, wird dieser Wert durch den angegebenen Wert ersetzt.</span><span class="sxs-lookup"><span data-stu-id="abb0a-183">If the sequence number corresponds to an existing value then that value is replaced with the given value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="abb0a-184">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abb0a-184">Return Value</span></span>

<span data-ttu-id="abb0a-185">Diese Funktion gibt den [JET_ERR](./jet-err.md) Datentyp mit einem der folgenden Rückgabecodes zurück.</span><span class="sxs-lookup"><span data-stu-id="abb0a-185">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="abb0a-186">Weitere Informationen zu den möglichen ESE-Fehlern finden Sie unter [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) und [Error Handling Parameters](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="abb0a-186">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="abb0a-187">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="abb0a-187">Return code</span></span></p></th>
<th><p><span data-ttu-id="abb0a-188">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abb0a-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-189">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="abb0a-189">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="abb0a-190">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="abb0a-190">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-191">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="abb0a-191">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="abb0a-192">Die angegebene Spalten-ID liegt außerhalb der zulässigen Beschränkungen einer Spalten-ID.</span><span class="sxs-lookup"><span data-stu-id="abb0a-192">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-193">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="abb0a-193">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="abb0a-194">Der Vorgang kann nicht ausgeführt werden, da alle Aktivitäten auf der Instanz, die der Sitzung zugeordnet ist, aufgrund eines Aufrufens von <a href="gg269240(v=exchg.10).md">jetstopservice</a>beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="abb0a-194">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-195">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="abb0a-195">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="abb0a-196">Die von der angegebenen Spalte beschriebene Spalte ist in der <em>Tabelle nicht vorhanden</em> .</span><span class="sxs-lookup"><span data-stu-id="abb0a-196">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-197">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="abb0a-197">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="abb0a-198">Es wurde ein unzulässiger Versuch unternommen, einen Long-Wert während eines INSERT-Vorgangs zum Löschen des ursprünglichen Updates zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="abb0a-198">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-199">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="abb0a-199">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="abb0a-200">Die angegebenen Spaltenwert Daten, die im Eingabepuffer angegeben sind, überschreiten die Größenbeschränkung für eine Spalte mit fester Länge oder für Text oder Binär Spalten mit fester Länge.</span><span class="sxs-lookup"><span data-stu-id="abb0a-200">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="abb0a-201">Dieser Fehler wird auch zurückgegeben, wenn mehr als 1024 Bytes an Daten für eine lange Spalte übergeben werden und das JET_bitSetIntrinsicLV-Flag festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-201">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-202">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="abb0a-202">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="abb0a-203">Der Vorgang kann nicht ausgeführt werden, da bei der der Sitzung zugeordneten Instanz ein schwerwiegender Fehler aufgetreten ist, der erfordert, dass der Zugriff auf alle Daten widerrufen wird, um die Integrität der Daten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="abb0a-203">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="abb0a-204"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="abb0a-204"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-205">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="abb0a-205">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="abb0a-206">Die angegebene Datengröße für den Spaltenwert stimmt nicht mit dem Wert für den Datentyp mit fester Länge identisch.</span><span class="sxs-lookup"><span data-stu-id="abb0a-206">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-207">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="abb0a-207">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="abb0a-208">Es wurde ein unzulässiger Versuch unternommen, eine automatische Inkrement-Spalte entweder während eines INSERT-oder Update-Vorgangs zu aktualisieren oder eine Versions Spalte während eines Ersetzungs Vorgangs zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="abb0a-208">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-209">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="abb0a-209">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="abb0a-210">Die angegebenen Optionen sind unbekannt oder eine ungültige Kombination bekannter Biteinstellungen.</span><span class="sxs-lookup"><span data-stu-id="abb0a-210">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-211">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="abb0a-211">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="abb0a-212">Die angegebene "psetup Info- &gt; cbStruct" ist keine gültige Größe für die <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> Struktur.</span><span class="sxs-lookup"><span data-stu-id="abb0a-212">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-213">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="abb0a-213">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="abb0a-214">Der Vorgang zum Festlegen der Spalte hat versucht, einen doppelten Wert zu erstellen und entweder JET_bitSetUniqueMultiValues oder JET_bitSetUniqueNormalizedMultiValues anzugeben.</span><span class="sxs-lookup"><span data-stu-id="abb0a-214">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-215">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="abb0a-215">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="abb0a-216">Der Vorgang kann nicht abgeschlossen werden, da die Instanz, die der Sitzung zugeordnet ist, noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="abb0a-216">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-217">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="abb0a-217">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="abb0a-218">Es wurde ein unzulässiger Versuch unternommen, einen Long-Spaltenwert zu aktualisieren, wenn sich die aufrufende Sitzung nicht in einer Transaktion befand.</span><span class="sxs-lookup"><span data-stu-id="abb0a-218">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-219">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="abb0a-219">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="abb0a-220">Es wurde ein unzulässiger Versuch unternommen, eine nicht-<strong>null</strong> -Spalte auf <strong>null</strong>festzulegen.</span><span class="sxs-lookup"><span data-stu-id="abb0a-220">An illegal attempt was made to set a non-<strong>NULL</strong> column to <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-221">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="abb0a-221">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="abb0a-222">Identisch mit JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="abb0a-222">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-223">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="abb0a-223">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="abb0a-224">Der Spaltenwert konnte nicht auf den Wert im Eingabepuffer festgelegt werden, da er dazu geführt hätte, dass der Datensatz seine Größenbeschränkung für die Seitengröße überschreitet.</span><span class="sxs-lookup"><span data-stu-id="abb0a-224">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="abb0a-225">Spalten vom Typ <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> oder <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> können getrennt von den verbleibenden Daten Satz Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="abb0a-225">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="abb0a-226">Allerdings müssen andere Spalten mit dem Datensatz gespeichert werden und können dazu führen, dass die Einschränkung der Daten Satz Größe überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-226">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="abb0a-227">Sogar lange Spalten benötigen 5-Byte-Speicherplatz innerhalb des Datensatzes als Verknüpfung, und dies kann dazu führen, dass JET_errRecordTooBig zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="abb0a-227">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-228">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="abb0a-228">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="abb0a-229">Der Vorgang kann nicht abgeschlossen werden, da für die-Instanz, die der Sitzung zugeordnet ist, ein Wiederherstellungs Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-229">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-230">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="abb0a-230">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="abb0a-231">Dieselbe Sitzung kann nicht für mehr als einen Thread gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abb0a-231">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="abb0a-232"><strong>Windows XP:</strong>  Dieser Fehler wird nur von Windows XP und höheren Versionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="abb0a-232"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-233">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="abb0a-233">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="abb0a-234">Der Vorgang kann nicht ausgeführt werden, da die Instanz, die der Sitzung zugeordnet ist, heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-234">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-235">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="abb0a-235">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="abb0a-236">Der Cursor befindet sich derzeit nicht im Prozess, entweder einen neuen Datensatz einzufügen oder einen vorhandenen Datensatz zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="abb0a-236">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-237">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="abb0a-237">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="abb0a-238">Dieser Fehler tritt auf, wenn die konfigurierte Größe des Versionsspeicher nicht ausreicht, um alle ausstehenden Updates zu speichern.</span><span class="sxs-lookup"><span data-stu-id="abb0a-238">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-239">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="abb0a-239">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="abb0a-240">Der Spaltenwert im Eingabepuffer hat die für eine Spalte mit variabler Länge konfigurierte maximale Länge überschritten und wurde abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="abb0a-240">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="abb0a-241">Bei Erfolg wird der gewünschte Teil eines Spaltenwerts für die angegebene Spalte mit Daten, die aus dem Eingabepuffer kopiert wurden, festgelegt.</span><span class="sxs-lookup"><span data-stu-id="abb0a-241">On success, the desired portion of a column value for the given column is set with data copied from the input buffer.</span></span> <span data-ttu-id="abb0a-242">Das DataSet wurde möglicherweise abgeschnitten, wenn es die für eine Spalte mit variabler Länge angegebene maximale Länge überschreitet.</span><span class="sxs-lookup"><span data-stu-id="abb0a-242">The data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="abb0a-243">Bei einem Fehler wird die Cursorposition unverändert bleiben, und im Kopier Puffer werden keine Spaltenwert Daten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="abb0a-243">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="abb0a-244">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abb0a-244">Remarks</span></span>

<span data-ttu-id="abb0a-245">Das Festlegen langer Werte, Werte für Spalten [JET_coltypLongBinary](./jet-coltyp.md) vom Typ [JET_coltypLongText](./jet-coltyp.md) oder [JET_coltypLongBinary](./jet-coltyp.md)sollten nur dann erfolgen, wenn sich die aufrufende Sitzung in einer Transaktion befindet.</span><span class="sxs-lookup"><span data-stu-id="abb0a-245">Setting long values, values for columns [JET_coltypLongBinary](./jet-coltyp.md) of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md), should be done only when the calling session is in a transaction.</span></span> <span data-ttu-id="abb0a-246">Wenn sich die aufrufende Sitzung nicht in einer Transaktion befindet, werden Änderungen an langen Werten, die separat gespeichert werden, möglicherweise auch dann vollständig ausgeführt, wenn der Aktualisierungs Vorgang später abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-246">If the calling session is not in a transaction, modifications to long values which are stored separately may be committed fully even when the update operation is later cancelled.</span></span> <span data-ttu-id="abb0a-247">Wenn sich die aufrufende Sitzung in einer Transaktion befindet, können die Auswirkungen des Updates vollständig rückgängig gemacht werden, indem das Update abgebrochen und ein Rollback für die Sitzungs Transaktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-247">If the calling session is in a transaction, then the effects of the update can be fully rolled back by canceling the update and rolling back the session transaction.</span></span>

<span data-ttu-id="abb0a-248">Index Aktualisierungen werden nicht als Ergebnis von **jetsetcolumn** -Vorgängen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abb0a-248">Index updates are not performed as a result of **JetSetColumn** operations.</span></span> <span data-ttu-id="abb0a-249">Stattdessen werden Indizes erst aktualisiert, nachdem alle Spalten Änderungen vollständig sind und [jetupdate](./jetupdate-function.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="abb0a-249">Instead, indexes are updated only after all column modifications are complete and [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="abb0a-250">Dies ermöglicht die effizienteste Aktualisierung von Indizes, wenn die Indizes mehr als eine Spalte ändern.</span><span class="sxs-lookup"><span data-stu-id="abb0a-250">This permits the most efficient updating of indexes when indexes involve more than one column being modified.</span></span>

<span data-ttu-id="abb0a-251">Die Größe eines Datensatzes hängt von der Größe der Datenbankseite ab.</span><span class="sxs-lookup"><span data-stu-id="abb0a-251">A record is limited in size based on the database page size.</span></span> <span data-ttu-id="abb0a-252">Alle langen Werte im Datensatz, die größer als fünf Bytes sind, werden getrennt vom Datensatz gespeichert, wenn die Daten im Datensatz aufgrund eines **jetsetcolumn** -Vorgangs den Grenzwert überschreiten.</span><span class="sxs-lookup"><span data-stu-id="abb0a-252">Any long values in the record larger than five bytes will be stored separate from the record should the data in the record exceed its limit as a result of a **JetSetColumn** operation.</span></span> <span data-ttu-id="abb0a-253">Der Fehler JET_errRecordTooBig wird nur zurückgegeben, nachdem alle trennbaren Daten Satz Spaltendaten getrennt vom Datensatz gespeichert wurden und der Datensatz weiterhin das Daten Satz Größenlimit überschreitet.</span><span class="sxs-lookup"><span data-stu-id="abb0a-253">The error JET_errRecordTooBig will only be returned after all separable record column data has been stored separately from the record and the record still exceeds the record size limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="abb0a-254">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abb0a-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-255"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="abb0a-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="abb0a-256">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="abb0a-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-257"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="abb0a-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="abb0a-258">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="abb0a-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-259"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="abb0a-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="abb0a-260">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="abb0a-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abb0a-261"><strong>Bibliothek</strong></span><span class="sxs-lookup"><span data-stu-id="abb0a-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="abb0a-262">Verwenden Sie ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="abb0a-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abb0a-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="abb0a-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="abb0a-264">Erfordert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="abb0a-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="abb0a-265">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="abb0a-265">See Also</span></span>

[<span data-ttu-id="abb0a-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="abb0a-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="abb0a-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="abb0a-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="abb0a-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="abb0a-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="abb0a-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="abb0a-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="abb0a-270">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="abb0a-270">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="abb0a-271">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="abb0a-271">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="abb0a-272">Jetsetcolumns</span><span class="sxs-lookup"><span data-stu-id="abb0a-272">JetSetColumns</span></span>](./jetsetcolumns-function.md)
