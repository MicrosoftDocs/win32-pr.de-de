---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMNVALUE Struktur'
title: JET_ENUMCOLUMNVALUE Struktur
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
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
ms.openlocfilehash: bc95c6b8403a64432451ea29dbb66868fad25264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363664"
---
# <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="55112-103">JET_ENUMCOLUMNVALUE Struktur</span><span class="sxs-lookup"><span data-stu-id="55112-103">JET_ENUMCOLUMNVALUE Structure</span></span>


<span data-ttu-id="55112-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="55112-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="55112-105">JET_ENUMCOLUMNVALUE Struktur</span><span class="sxs-lookup"><span data-stu-id="55112-105">JET_ENUMCOLUMNVALUE Structure</span></span>

<span data-ttu-id="55112-106">Die **JET_ENUMCOLUMNVALUE** -Struktur listet die Spaltenwerte eines Datensatzes mithilfe der [jetenumeratecolumns](./jetenumeratecolumns-function.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="55112-106">The **JET_ENUMCOLUMNVALUE** structure enumerates the column values of a record using the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function.</span></span> <span data-ttu-id="55112-107">[Jetenreeratecolenns](./jetenumeratecolumns-function.md) gibt ein Array von **JET_ENUMCOLUMNVALUE** Strukturen zurück.</span><span class="sxs-lookup"><span data-stu-id="55112-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNVALUE** structures.</span></span> <span data-ttu-id="55112-108">Das Array wird im Arbeitsspeicher zurückgegeben, der mit dem [rezubelegungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugewiesen wurde, der für diese Funktion bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="55112-108">The array is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that function.</span></span>

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a><span data-ttu-id="55112-109">Member</span><span class="sxs-lookup"><span data-stu-id="55112-109">Members</span></span>

<span data-ttu-id="55112-110">**itagsequence**</span><span class="sxs-lookup"><span data-stu-id="55112-110">**itagSequence**</span></span>

<span data-ttu-id="55112-111">Der aufgelistete Spaltenwert (durch einen einsbasierten Index).</span><span class="sxs-lookup"><span data-stu-id="55112-111">The column value (by one-based index) that was enumerated.</span></span>

<span data-ttu-id="55112-112">**irre**</span><span class="sxs-lookup"><span data-stu-id="55112-112">**err**</span></span>

<span data-ttu-id="55112-113">Der Spalten Statuscode, der sich aus der Enumeration des Spaltenwerts ergibt.</span><span class="sxs-lookup"><span data-stu-id="55112-113">The column status code resulting from the enumeration of the column value.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55112-114">Wert</span><span class="sxs-lookup"><span data-stu-id="55112-114">Value</span></span></p></th>
<th><p><span data-ttu-id="55112-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="55112-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55112-116">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="55112-116">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="55112-117">Der angeforderte Spaltenwert ist NULL.</span><span class="sxs-lookup"><span data-stu-id="55112-117">The requested column value is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55112-118">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="55112-118">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="55112-119">Die <em>itagsequence</em> , die im-Element des <em>rgtagsequence</em> -Arrays in der <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> Struktur angegeben ist, die dieser <strong>JET_ENUMCOLUMNVALUE</strong> Struktur entspricht, war 0 (null).</span><span class="sxs-lookup"><span data-stu-id="55112-119">The <em>itagSequence</em> that is specified in the element of the <em>rgtagSequence</em> array in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> struct corresponding to this <strong>JET_ENUMCOLUMNVALUE</strong> struct was zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55112-120">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="55112-120">JET_wrnColumnTruncated</span></span></p></td>
<td><p><span data-ttu-id="55112-121">Der angeforderte Spaltenwert wurde auf die angegebene Größe abgeschnitten, bevor er zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="55112-121">The requested column value was truncated to the specified size before being returned.</span></span></p>
<p><span data-ttu-id="55112-122">Diese Kürzung erfolgt nur für lange Text-und lange binäre Spalten, die große Datenmengen enthalten.</span><span class="sxs-lookup"><span data-stu-id="55112-122">This truncation occurs only for long text and long binary columns that contain large amounts of data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="55112-123">**cbData**</span><span class="sxs-lookup"><span data-stu-id="55112-123">**cbData**</span></span>

<span data-ttu-id="55112-124">Der Spaltenwert, der für die Spalte aufgelistet wurde.</span><span class="sxs-lookup"><span data-stu-id="55112-124">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="55112-125">Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mit dem [rezubelegungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugewiesen wurde, der für [jetenumeratecolumns](./jetenumeratecolumns-function.md)bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="55112-125">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="55112-126">**pvData**</span><span class="sxs-lookup"><span data-stu-id="55112-126">**pvData**</span></span>

<span data-ttu-id="55112-127">Der Spaltenwert, der für die Spalte aufgelistet wurde.</span><span class="sxs-lookup"><span data-stu-id="55112-127">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="55112-128">Der Ausgabepuffer wird im Arbeitsspeicher zurückgegeben, der mit dem [rezubelegungskompatiblen](/cpp/c-runtime-library/reference/realloc?view=vs-2019) Rückruf zugewiesen wurde, der für [jetenumeratecolumns](./jetenumeratecolumns-function.md)bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="55112-128">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="55112-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55112-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55112-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="55112-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="55112-131">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="55112-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55112-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="55112-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="55112-133">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="55112-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55112-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="55112-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="55112-135">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="55112-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="55112-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="55112-136">See Also</span></span>

[<span data-ttu-id="55112-137">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="55112-137">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="55112-138">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="55112-138">JET_ENUMCOLUMNVALUE</span></span>]()  
[<span data-ttu-id="55112-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="55112-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="55112-140">Jetenreeratecolumschlag</span><span class="sxs-lookup"><span data-stu-id="55112-140">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="55112-141">realloc</span><span class="sxs-lookup"><span data-stu-id="55112-141">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
