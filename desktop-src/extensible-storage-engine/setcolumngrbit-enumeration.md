---
description: 'Weitere Informationen finden Sie hier: setcolumngrbit-Enumeration'
title: Setcolumngrbit-Enumeration
TOCTitle: SetColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39509934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893f8e79b910a305bf6caccacd2d928e947be693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485227"
---
# <a name="setcolumngrbit-enumeration"></a><span data-ttu-id="db2fe-103">Setcolumngrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="db2fe-103">SetColumnGrbit enumeration</span></span>

<span data-ttu-id="db2fe-104">Optionen für jetsetcolumn.</span><span class="sxs-lookup"><span data-stu-id="db2fe-104">Options for JetSetColumn.</span></span>

<span data-ttu-id="db2fe-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="db2fe-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="db2fe-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="db2fe-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="db2fe-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="db2fe-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="db2fe-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="db2fe-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetColumnGrbit
'Usage
Dim instance As SetColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum SetColumnGrbit
```

## <a name="members"></a><span data-ttu-id="db2fe-109">Member</span><span class="sxs-lookup"><span data-stu-id="db2fe-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="db2fe-110">Membername</span><span class="sxs-lookup"><span data-stu-id="db2fe-110">Member name</span></span></th>
<th><span data-ttu-id="db2fe-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db2fe-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="db2fe-112">Keine</span><span class="sxs-lookup"><span data-stu-id="db2fe-112">None</span></span></td>
<td><span data-ttu-id="db2fe-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="db2fe-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="db2fe-114">Appendlv</span><span class="sxs-lookup"><span data-stu-id="db2fe-114">AppendLV</span></span></td>
<td><span data-ttu-id="db2fe-115">Diese Option wird zum Anfügen von Daten an eine Spalte vom Typ JET_coltypLongText oder JET_coltypLongBinary verwendet.</span><span class="sxs-lookup"><span data-stu-id="db2fe-115">This option is used to append data to a column of type JET_coltypLongText or JET_coltypLongBinary.</span></span> <span data-ttu-id="db2fe-116">Das gleiche Verhalten können Sie erreichen, indem Sie die Größe des vorhandenen Long-Werts ermitteln und iblongvalue in psetup angeben.</span><span class="sxs-lookup"><span data-stu-id="db2fe-116">The same behavior can be achieved by determining the size of the existing long value and specifying ibLongValue in psetinfo.</span></span> <span data-ttu-id="db2fe-117">Es ist jedoch einfacher, dieses grbit zu verwenden, da es nicht erforderlich ist, die Größe des vorhandenen Spaltenwerts zu kennen.</span><span class="sxs-lookup"><span data-stu-id="db2fe-117">However, its simpler to use this grbit since knowing the size of the existing column value is not necessary.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="db2fe-118">Overschreitelv</span><span class="sxs-lookup"><span data-stu-id="db2fe-118">OverwriteLV</span></span></td>
<td><span data-ttu-id="db2fe-119">Diese Option wird verwendet, um den vorhandenen Long-Wert durch die neu bereitgestellten Daten zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="db2fe-119">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="db2fe-120">Wenn diese Option verwendet wird, ist es so, als ob der vorhandene Long-Wert auf 0 (null) festgelegt wurde, bevor die neuen Daten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="db2fe-120">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="db2fe-121">Revertumdefaultvalue</span><span class="sxs-lookup"><span data-stu-id="db2fe-121">RevertToDefaultValue</span></span></td>
<td><span data-ttu-id="db2fe-122">Diese Option gilt nur für markierte, Spalten mit geringer Dichte oder mehrwertige Spalten.</span><span class="sxs-lookup"><span data-stu-id="db2fe-122">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="db2fe-123">Dies bewirkt, dass die Spalte bei nachfolgenden Spalten Abruf Vorgängen den Standard Spaltenwert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="db2fe-123">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="db2fe-124">Alle vorhandenen Spaltenwerte werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="db2fe-124">All existing column values are removed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="db2fe-125">Separatelv</span><span class="sxs-lookup"><span data-stu-id="db2fe-125">SeparateLV</span></span></td>
<td><span data-ttu-id="db2fe-126">Diese Option wird verwendet, um einen Long-Wert, Spalten vom Typ JET_coltyp zu erzwingen. LONGTEXT oder JET_coltyp. LONGBINARY, das getrennt vom Rest der Daten Satz Daten gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="db2fe-126">This option is used to force a long value, columns of type JET_coltyp.LongText or JET_coltyp.LongBinary, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="db2fe-127">Dies tritt normalerweise auf, wenn die Größe des Long-Werts verhindert, dass Sie mit den verbleibenden Daten Satz Daten gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="db2fe-127">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="db2fe-128">Diese Option kann jedoch verwendet werden, um zu erzwingen, dass der lange Wert separat gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="db2fe-128">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="db2fe-129">Beachten Sie, dass lange Werte mit einer Größe von vier Bytes, die kleiner als getrennt sind, nicht erzwungen werden können.</span><span class="sxs-lookup"><span data-stu-id="db2fe-129">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="db2fe-130">In solchen Fällen wird die Option ignoriert.</span><span class="sxs-lookup"><span data-stu-id="db2fe-130">In such cases, the option is ignored.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="db2fe-131">Sizelv</span><span class="sxs-lookup"><span data-stu-id="db2fe-131">SizeLV</span></span></td>
<td><span data-ttu-id="db2fe-132">Diese Option wird verwendet, um den Eingabepuffer als ganzzahlige Anzahl von Bytes zu interpretieren, die als Länge des Long-Werts festgelegt werden, der durch das angegebene ColumnID und ggf. die Sequenznummer in psetinfo- &gt; itagsequence beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="db2fe-132">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="db2fe-133">Wenn die angegebene Größe größer ist als der vorhandene Spaltenwert, wird die Spalte um 0s erweitert.</span><span class="sxs-lookup"><span data-stu-id="db2fe-133">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="db2fe-134">Wenn die Größe kleiner als der vorhandene Spaltenwert ist, wird der Wert abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="db2fe-134">If the size is smaller than the existing column value then the value will be truncated.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="db2fe-135">Uniquemultivalues</span><span class="sxs-lookup"><span data-stu-id="db2fe-135">UniqueMultiValues</span></span></td>
<td><span data-ttu-id="db2fe-136">Diese Option wird verwendet, um zu erzwingen, dass alle Werte in einer mehrwertigen Spalte voneinander abweichen.</span><span class="sxs-lookup"><span data-stu-id="db2fe-136">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="db2fe-137">Mit dieser Option werden die Quell Spaltendaten ohne Transformationen mit anderen vorhandenen Spaltenwerten verglichen, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db2fe-137">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="db2fe-138">Wenn diese Option angegeben ist, können appendlv, overwrite telv und sizelv nicht gleichzeitig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="db2fe-138">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="db2fe-139">UniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="db2fe-139">UniqueNormalizedMultiValues</span></span></td>
<td><span data-ttu-id="db2fe-140">Diese Option wird verwendet, um zu erzwingen, dass alle Werte in einer mehrwertigen Spalte voneinander abweichen.</span><span class="sxs-lookup"><span data-stu-id="db2fe-140">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="db2fe-141">Mit dieser Option wird die normalisierte Transformation von Spaltendaten mit anderen ähnlich transformierten vorhandenen Spaltenwerten verglichen, und es wird ein Fehler zurückgegeben, wenn ein Duplikat gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db2fe-141">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="db2fe-142">Wenn diese Option angegeben ist, können appendlv, overwrite telv und sizelv nicht gleichzeitig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="db2fe-142">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="db2fe-143">Nullover</span><span class="sxs-lookup"><span data-stu-id="db2fe-143">ZeroLength</span></span></td>
<td><span data-ttu-id="db2fe-144">Diese Option wird verwendet, um einen Wert auf die Länge 0 (null) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="db2fe-144">This option is used to set a value to zero length.</span></span> <span data-ttu-id="db2fe-145">Normalerweise wird ein Spaltenwert auf NULL festgelegt, indem ein cbmax-Wert von 0 (null) übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="db2fe-145">Normally, a column value is set to NULL by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="db2fe-146">Für einige Typen, wie z. b. JET_coltyp. Text: ein Spaltenwert kann eine Länge von 0 (null) anstelle von NULL sein, und diese Option wird verwendet, um zwischen null und 0 (null) zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="db2fe-146">However, for some types, like JET_coltyp.Text, a column value can be 0 (zero) length instead of NULL, and this option is used to differentiate between NULL and 0 (zero) length.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="db2fe-147">Intrinsier-CLV</span><span class="sxs-lookup"><span data-stu-id="db2fe-147">IntrinsicLV</span></span></td>
<td><span data-ttu-id="db2fe-148">Versuchen Sie, lange Wert Spalten im Datensatz zu speichern, auch wenn Sie die Standard Trennungs Größe überschreiten.</span><span class="sxs-lookup"><span data-stu-id="db2fe-148">Try to store long-value columns in the record, even if they exceed the default separation size.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="db2fe-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db2fe-149">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="db2fe-150">Referenz</span><span class="sxs-lookup"><span data-stu-id="db2fe-150">Reference</span></span>

[<span data-ttu-id="db2fe-151">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="db2fe-151">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="db2fe-152">Compressed</span><span class="sxs-lookup"><span data-stu-id="db2fe-152">Compressed</span></span>](./windows7grbits.compressed-field.md)

[<span data-ttu-id="db2fe-153">Nicht komprimiert</span><span class="sxs-lookup"><span data-stu-id="db2fe-153">Uncompressed</span></span>](./windows7grbits.uncompressed-field.md)
