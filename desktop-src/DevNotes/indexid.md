---
description: Der Bezeichner des Indexes, auf den in einer Datenbank zugegriffen werden soll.
ms.assetid: 559e73bf-91c2-4dbf-a667-e5c0431aaffa
title: INDEXID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b6ef6b79dd19183f575930e9793a6ab2f1f5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127253"
---
# <a name="indexid"></a><span data-ttu-id="f7f73-103">INDEXID</span><span class="sxs-lookup"><span data-stu-id="f7f73-103">INDEXID</span></span>

<span data-ttu-id="f7f73-104">Der Bezeichner des Indexes, auf den in einer Datenbank zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7f73-104">The identifier of the index to be accessed in a database.</span></span>


```C++
typedef DWORD INDEXID;
```



## <a name="remarks"></a><span data-ttu-id="f7f73-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7f73-105">Remarks</span></span>

<span data-ttu-id="f7f73-106">Eine **IndexID** kann ein ganzzahliger Wert sein, der den Index darstellt, oder der folgende Wert:</span><span class="sxs-lookup"><span data-stu-id="f7f73-106">An **INDEXID** can be an integer value that represents the index, or the following value:</span></span>

<dl> <dt>

<span data-ttu-id="f7f73-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>IndexID \_ NULL ((IndexID)-1)</span><span class="sxs-lookup"><span data-stu-id="f7f73-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXID\_NULL ((INDEXID)-1)</span></span>
</dt> <dd>

<span data-ttu-id="f7f73-108">Ungültige **IndexID**.</span><span class="sxs-lookup"><span data-stu-id="f7f73-108">An invalid **INDEXID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7f73-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7f73-109">Requirements</span></span>



| <span data-ttu-id="f7f73-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7f73-110">Requirement</span></span> | <span data-ttu-id="f7f73-111">Wert</span><span class="sxs-lookup"><span data-stu-id="f7f73-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f7f73-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f7f73-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f7f73-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7f73-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f7f73-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f7f73-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f7f73-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7f73-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7f73-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7f73-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7f73-117">**Sdbdeclareingedex**</span><span class="sxs-lookup"><span data-stu-id="f7f73-117">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="f7f73-118">**Sdbstartindizierung**</span><span class="sxs-lookup"><span data-stu-id="f7f73-118">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="f7f73-119">**Sdbstopindizierung**</span><span class="sxs-lookup"><span data-stu-id="f7f73-119">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




