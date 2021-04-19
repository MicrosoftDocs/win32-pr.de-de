---
description: 'Weitere Informationen finden Sie hier: JET_INDEXRANGE Struktur'
title: JET_INDEXRANGE Struktur
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
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
ms.openlocfilehash: ecbd8151be8ef278fc1bddc12323f41abd05b09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363608"
---
# <a name="jet_indexrange-structure"></a><span data-ttu-id="a87ea-103">JET_INDEXRANGE Struktur</span><span class="sxs-lookup"><span data-stu-id="a87ea-103">JET_INDEXRANGE Structure</span></span>


<span data-ttu-id="a87ea-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a87ea-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexrange-structure"></a><span data-ttu-id="a87ea-105">JET_INDEXRANGE Struktur</span><span class="sxs-lookup"><span data-stu-id="a87ea-105">JET_INDEXRANGE Structure</span></span>

<span data-ttu-id="a87ea-106">Die **JET_INDEXRANGE** -Struktur identifiziert einen Index Bereich, wenn er mit der [jetintersectindexes](./jetintersectindexes-function.md) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a87ea-106">The **JET_INDEXRANGE** structure identifies an index range when it is used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a><span data-ttu-id="a87ea-107">Member</span><span class="sxs-lookup"><span data-stu-id="a87ea-107">Members</span></span>

<span data-ttu-id="a87ea-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="a87ea-108">**cbStruct**</span></span>

<span data-ttu-id="a87ea-109">Die Größe (in Bytes) der **JET_INDEXRANGE**.</span><span class="sxs-lookup"><span data-stu-id="a87ea-109">The size, in bytes, of the **JET_INDEXRANGE**.</span></span>

<span data-ttu-id="a87ea-110">**TableID**</span><span class="sxs-lookup"><span data-stu-id="a87ea-110">**tableid**</span></span>

<span data-ttu-id="a87ea-111">Ein Cursor, für den zuvor ein Index Bereich mit [jetsetindexrange](./jetsetindexrange-function.md)festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a87ea-111">A cursor that has previously had an index range set with [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="a87ea-112">**grbit**</span><span class="sxs-lookup"><span data-stu-id="a87ea-112">**grbit**</span></span>

<span data-ttu-id="a87ea-113">Eine Bitmaske, die aus genau einer der folgenden Elemente besteht.</span><span class="sxs-lookup"><span data-stu-id="a87ea-113">A bitmask composed of exactly one of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a87ea-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a87ea-114">Value</span></span></p></th>
<th><p><span data-ttu-id="a87ea-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a87ea-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a87ea-116">JET_bitRecordInIndex</span><span class="sxs-lookup"><span data-stu-id="a87ea-116">JET_bitRecordInIndex</span></span></p></td>
<td><p><span data-ttu-id="a87ea-117">Gibt an, dass der Index Bereich normal behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a87ea-117">Specifies that the index range should be treated normally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a87ea-118">JET_bitRecordNotInIndex</span><span class="sxs-lookup"><span data-stu-id="a87ea-118">JET_bitRecordNotInIndex</span></span></p></td>
<td><p><span data-ttu-id="a87ea-119">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="a87ea-119">Reserved for future use.</span></span> <span data-ttu-id="a87ea-120">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a87ea-120">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="a87ea-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a87ea-121">Remarks</span></span>

<span data-ttu-id="a87ea-122">Jede **JET_INDEXRANGE** Struktur, die an [jetintersectindexes](./jetintersectindexes-function.md) übermittelt wird, stellt einen Index Bereich dar, der durch den API--Befehl interdiert wird.</span><span class="sxs-lookup"><span data-stu-id="a87ea-122">Each **JET_INDEXRANGE** structure that is passed to [JetIntersectIndexes](./jetintersectindexes-function.md) represents an index range, which will be intersected by the API call.</span></span> <span data-ttu-id="a87ea-123">Der Cursor, der in **JET_INDEXRANGE** angegeben ist, muss bereits über einen gültigen Index Bereich verfügen, wobei [jetsetindexrange](./jetsetindexrange-function.md)erfolgreich aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a87ea-123">The cursor that is given in **JET_INDEXRANGE** must have a valid index range set on it already, with a successful call to [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="a87ea-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a87ea-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a87ea-125"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a87ea-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a87ea-126">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a87ea-126">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a87ea-127"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a87ea-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a87ea-128">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a87ea-128">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a87ea-129"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a87ea-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a87ea-130">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="a87ea-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a87ea-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a87ea-131">See Also</span></span>

[<span data-ttu-id="a87ea-132">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="a87ea-132">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="a87ea-133">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a87ea-133">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a87ea-134">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a87ea-134">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a87ea-135">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="a87ea-135">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="a87ea-136">Jetintersectindexes</span><span class="sxs-lookup"><span data-stu-id="a87ea-136">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="a87ea-137">Jetsetindexrange</span><span class="sxs-lookup"><span data-stu-id="a87ea-137">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
