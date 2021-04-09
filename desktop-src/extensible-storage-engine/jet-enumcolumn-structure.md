---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMN Struktur'
title: JET_ENUMCOLUMN-Struktur
TOCTitle: JET_ENUMCOLUMN Structure
ms:assetid: f8f512fd-5fcf-47ed-a5db-2fb3bd76c2d7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294138(v=EXCHG.10)
ms:contentKeyID: 32765752
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
ms.openlocfilehash: ca204fef4e67e6883584511b1ac424149a137b79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128224"
---
# <a name="jet_enumcolumn-structure"></a><span data-ttu-id="496e0-103">JET_ENUMCOLUMN-Struktur</span><span class="sxs-lookup"><span data-stu-id="496e0-103">JET_ENUMCOLUMN Structure</span></span>


<span data-ttu-id="496e0-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="496e0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumn-structure"></a><span data-ttu-id="496e0-105">JET_ENUMCOLUMN-Struktur</span><span class="sxs-lookup"><span data-stu-id="496e0-105">JET_ENUMCOLUMN Structure</span></span>

<span data-ttu-id="496e0-106">Die **JET_ENUMCOLUMN** -Struktur listet die Spaltenwerte eines Datensatzes auf, wenn die [jetenumeratecolumns](./jetenumeratecolumns-function.md) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="496e0-106">The **JET_ENUMCOLUMN** structure enumerates the column values of a record when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="496e0-107">[Jetenreeratecolenns](./jetenumeratecolumns-function.md) gibt ein Array von **JET_ENUMCOLUMN** Strukturen zurück.</span><span class="sxs-lookup"><span data-stu-id="496e0-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMN** structures.</span></span> <span data-ttu-id="496e0-108">Das Array wird im Arbeitsspeicher zurückgegeben, der mit dem [rezubelegungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugewiesen wird, der für diese API bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="496e0-108">The array is returned in memory that is allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that API.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      JET_ERR err;
      union {
        struct {
          unsigned long cEnumColumnValue;
          JET_ENUMCOLUMNVALUE rgEnumColumnValue;
        };
        struct {
          unsigned long cbData;
          void* pvData;
        };
      };
    } JET_ENUMCOLUMN;
```

### <a name="members"></a><span data-ttu-id="496e0-109">Member</span><span class="sxs-lookup"><span data-stu-id="496e0-109">Members</span></span>

<span data-ttu-id="496e0-110">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="496e0-110">**columnid**</span></span>

<span data-ttu-id="496e0-111">Die aufgelistete Spalten-ID.</span><span class="sxs-lookup"><span data-stu-id="496e0-111">The column ID that was enumerated.</span></span>

<span data-ttu-id="496e0-112">**irre**</span><span class="sxs-lookup"><span data-stu-id="496e0-112">**err**</span></span>

<span data-ttu-id="496e0-113">Der Spalten Statuscode, der sich aus der Enumeration der Spalte ergibt.</span><span class="sxs-lookup"><span data-stu-id="496e0-113">The column status code that results from the enumeration of the column.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="496e0-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="496e0-114">Error Codes</span></span></p></th>
<th><p><span data-ttu-id="496e0-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="496e0-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="496e0-116">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="496e0-116">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="496e0-117">Die Spalten-ID liegt außerhalb der zulässigen Beschränkungen einer Spalten-ID.</span><span class="sxs-lookup"><span data-stu-id="496e0-117">The column ID is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="496e0-118">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="496e0-118">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="496e0-119">Die von der Spalten-ID beschriebene Spalte ist in der Tabelle nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="496e0-119">The column described by the column ID does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="496e0-120">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="496e0-120">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="496e0-121">Alle Werte für diese Spalte sind NULL.</span><span class="sxs-lookup"><span data-stu-id="496e0-121">All values for this column are NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="496e0-122">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="496e0-122">JET_wrnColumnPresent</span></span></p></td>
<td><p><span data-ttu-id="496e0-123">JET_bitEnumeratePresenceOnly wurde angegeben, und mindestens ein nicht-NULL-Spaltenwert wurde für diese Spalte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="496e0-123">JET_bitEnumeratePresenceOnly was specified and at least one non-NULL column value would have been returned for this column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="496e0-124">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="496e0-124">JET_wrnColumnSingleValue</span></span></p></td>
<td><p><span data-ttu-id="496e0-125">JET_bitEnumerateCompressOutput wurde angegeben, und für diese Spalte wurde genau ein nicht-NULL-Spaltenwert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="496e0-125">JET_bitEnumerateCompressOutput was specified and exactly one non-NULL column value has been returned for this column.</span></span> <span data-ttu-id="496e0-126">Daher wurde die komprimierte Form von <strong>JET_ENUMCOLUMN</strong> zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="496e0-126">As a result, the compressed form of <strong>JET_ENUMCOLUMN</strong> has been returned.</span></span> <span data-ttu-id="496e0-127">Weitere Informationen finden Sie unter <strong>JET_ENUMCOLUMN</strong> .</span><span class="sxs-lookup"><span data-stu-id="496e0-127">See <strong>JET_ENUMCOLUMN</strong> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="496e0-128">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="496e0-128">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="496e0-129">Die Spalten-ID in der <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> Struktur, die dieser <strong>JET_ENUMCOLUMN</strong> Struktur entspricht, war 0 (null).</span><span class="sxs-lookup"><span data-stu-id="496e0-129">The column ID in the <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> struct corresponding to this <strong>JET_ENUMCOLUMN</strong> struct was zero.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="496e0-130">**cenenumcolumnvalue**</span><span class="sxs-lookup"><span data-stu-id="496e0-130">**cEnumColumnValue**</span></span>

<span data-ttu-id="496e0-131">Das Array der Spaltenwerte, die für die Spalte aufgelistet wurden.</span><span class="sxs-lookup"><span data-stu-id="496e0-131">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="496e0-132">Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mit dem [rezubelegungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugewiesen wurde, der für [jetenumeratecolumns](./jetenumeratecolumns-function.md)bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="496e0-132">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="496e0-133">Dieser Ausgabepuffer wird verwendet, wenn der Spalten Statuscode nicht gleich JET_wrnColumnSingleValue ist.</span><span class="sxs-lookup"><span data-stu-id="496e0-133">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="496e0-134">Weitere Informationen finden Sie unter [jetenreeratecolumschlag](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="496e0-134">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="496e0-135">Dies wird zurückgegeben, wenn "Err \! = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="496e0-135">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="496e0-136">**rgenenumcolumnvalue**</span><span class="sxs-lookup"><span data-stu-id="496e0-136">**rgEnumColumnValue**</span></span>

<span data-ttu-id="496e0-137">Das Array der Spaltenwerte, die für die Spalte aufgelistet wurden.</span><span class="sxs-lookup"><span data-stu-id="496e0-137">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="496e0-138">Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mit dem [rezubelegungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugewiesen wurde, der für [jetenumeratecolumns](./jetenumeratecolumns-function.md)bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="496e0-138">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="496e0-139">Dieser Ausgabepuffer wird verwendet, wenn der Spalten Statuscode nicht gleich JET_wrnColumnSingleValue ist.</span><span class="sxs-lookup"><span data-stu-id="496e0-139">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="496e0-140">Weitere Informationen finden Sie unter [jetenreeratecolumschlag](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="496e0-140">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="496e0-141">Dies wird zurückgegeben, wenn "Err \! = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="496e0-141">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="496e0-142">**cbData**</span><span class="sxs-lookup"><span data-stu-id="496e0-142">**cbData**</span></span>

<span data-ttu-id="496e0-143">Der Spaltenwert, der für die Spalte aufgelistet wurde.</span><span class="sxs-lookup"><span data-stu-id="496e0-143">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="496e0-144">Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mit dem [rezubelegungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugewiesen wurde, der für [jetenumeratecolumns](./jetenumeratecolumns-function.md)bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="496e0-144">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="496e0-145">Dieser Ausgabepuffer wird nur verwendet, wenn der Spalten Statuscode JET_wrnColumnSingleValue ist.</span><span class="sxs-lookup"><span data-stu-id="496e0-145">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="496e0-146">Weitere Informationen finden Sie unter [jetenreeratecolumschlag](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="496e0-146">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="496e0-147">Dies wird zurückgegeben, wenn "Err = = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="496e0-147">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="496e0-148">**pvData**</span><span class="sxs-lookup"><span data-stu-id="496e0-148">**pvData**</span></span>

<span data-ttu-id="496e0-149">Der Spaltenwert, der für die Spalte aufgelistet wurde.</span><span class="sxs-lookup"><span data-stu-id="496e0-149">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="496e0-150">Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mit dem [rezubelegungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugewiesen wurde, der für [jetenumeratecolumns](./jetenumeratecolumns-function.md)bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="496e0-150">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="496e0-151">Dieser Ausgabepuffer wird nur verwendet, wenn der Spalten Statuscode JET_wrnColumnSingleValue ist.</span><span class="sxs-lookup"><span data-stu-id="496e0-151">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="496e0-152">Weitere Informationen finden Sie unter [jetenreeratecolumschlag](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="496e0-152">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="496e0-153">Dies wird zurückgegeben, wenn "Err = = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="496e0-153">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

### <a name="requirements"></a><span data-ttu-id="496e0-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="496e0-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="496e0-155"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="496e0-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="496e0-156">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="496e0-156">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="496e0-157"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="496e0-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="496e0-158">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="496e0-158">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="496e0-159"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="496e0-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="496e0-160">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="496e0-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="496e0-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="496e0-161">See Also</span></span>

[<span data-ttu-id="496e0-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="496e0-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="496e0-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="496e0-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="496e0-164">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="496e0-164">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="496e0-165">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="496e0-165">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="496e0-166">Jetenreeratecolumschlag</span><span class="sxs-lookup"><span data-stu-id="496e0-166">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="496e0-167">realloc</span><span class="sxs-lookup"><span data-stu-id="496e0-167">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
