---
description: 'Weitere Informationen finden Sie hier: JET_INDEXID Struktur'
title: JET_INDEXID Struktur
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
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
ms.openlocfilehash: e1a9c6a971e44604240d750163f0570937f9d4db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364247"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="2e9d3-103">JET_INDEXID Struktur</span><span class="sxs-lookup"><span data-stu-id="2e9d3-103">JET_INDEXID Structure</span></span>


<span data-ttu-id="2e9d3-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2e9d3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexid-structure"></a><span data-ttu-id="2e9d3-105">JET_INDEXID Struktur</span><span class="sxs-lookup"><span data-stu-id="2e9d3-105">JET_INDEXID Structure</span></span>

<span data-ttu-id="2e9d3-106">Die **JET_INDEXID** -Struktur enthält eine Index-ID.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-106">The **JET_INDEXID** structure holds an index ID.</span></span> <span data-ttu-id="2e9d3-107">Eine Index-ID ist ein Hinweis, der verwendet wird, um die Auswahl des aktuellen Indexes mithilfe von [jetsetcurrentindex](./jetsetcurrentindex-function.md)zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-107">An index ID is a hint that is used to accelerate the selection of the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="2e9d3-108">Dies ist besonders nützlich, wenn eine Tabelle eine große Anzahl von Indizes enthält.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-108">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="2e9d3-109">Die Index-ID kann mit [jetgetindexinfo](./jetgetindexinfo-function.md) oder [jetgettableindexinfo](./jetgettableindexinfo-function.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-109">The index ID can be retrieved using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a><span data-ttu-id="2e9d3-110">Member</span><span class="sxs-lookup"><span data-stu-id="2e9d3-110">Members</span></span>

<span data-ttu-id="2e9d3-111">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="2e9d3-111">**cbStruct**</span></span>

<span data-ttu-id="2e9d3-112">Die Größe (in Bytes) der Index-ID.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-112">The size, in bytes, of the index ID.</span></span>

<span data-ttu-id="2e9d3-113">Dies ist die tatsächliche Größe der Index-ID, die im Ausgabepuffer von [jetgetindexinfo](./jetgetindexinfo-function.md) oder [jetgettableindexinfo](./jetgettableindexinfo-function.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-113">This is the actual size of the index ID that is returned in the output buffer from [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

<span data-ttu-id="2e9d3-114">**rgbindexid**</span><span class="sxs-lookup"><span data-stu-id="2e9d3-114">**rgbIndexId**</span></span>

<span data-ttu-id="2e9d3-115">Ein undurchsichtiges BLOB von Informationen, die von der-Engine verwendet werden, um schnell einen Index im Schema Cache zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-115">An opaque BLOB of information that is used by the engine to quickly identify an index in its schema cache.</span></span>

<span data-ttu-id="2e9d3-116">Versuchen Sie nicht, das BLOB von Informationen zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-116">Do not attempt to interpret the BLOB of information.</span></span> <span data-ttu-id="2e9d3-117">Es handelt sich nicht um eine festgelegte Größe.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-117">It is not a set size.</span></span>

### <a name="requirements"></a><span data-ttu-id="2e9d3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e9d3-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e9d3-119"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2e9d3-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2e9d3-120">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e9d3-121"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2e9d3-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2e9d3-122">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e9d3-123"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2e9d3-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2e9d3-124">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="2e9d3-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2e9d3-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2e9d3-125">See Also</span></span>

[<span data-ttu-id="2e9d3-126">Jetgetindexinfo</span><span class="sxs-lookup"><span data-stu-id="2e9d3-126">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="2e9d3-127">Jetgettableindexinfo</span><span class="sxs-lookup"><span data-stu-id="2e9d3-127">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="2e9d3-128">Jetgettableinfo</span><span class="sxs-lookup"><span data-stu-id="2e9d3-128">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="2e9d3-129">Jetsetcurrentindex</span><span class="sxs-lookup"><span data-stu-id="2e9d3-129">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)
