---
title: IPX_NETWORK Struktur (RTM. h)
description: Die IPX-Netzwerk \_ Struktur beschreibt eine IPX-Netzwerkadresse.
ms.assetid: 83fc4022-8515-4a51-ac47-f92572447fbf
keywords:
- IPX_NETWORK Struktur-RAS
- PIPX_NETWORK-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- IPX_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04aabf363c0152ba520bb5c8894142715b5bff56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949388"
---
# <a name="ipx_network-structure"></a><span data-ttu-id="76ec6-105">IPX- \_ Netzwerkstruktur</span><span class="sxs-lookup"><span data-stu-id="76ec6-105">IPX\_NETWORK structure</span></span>

<span data-ttu-id="76ec6-106">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76ec6-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="76ec6-107">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="76ec6-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="76ec6-108">Die **IPX \_** -Netzwerkstruktur beschreibt eine IPX-Netzwerkadresse.</span><span class="sxs-lookup"><span data-stu-id="76ec6-108">The **IPX\_NETWORK** structure describes an IPX network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ec6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="76ec6-109">Syntax</span></span>


```C++
typedef struct _IPX_NETWORK {
  DWORD N_NetNumber;
} IPX_NETWORK, *PIPX_NETWORK;
```



## <a name="members"></a><span data-ttu-id="76ec6-110">Member</span><span class="sxs-lookup"><span data-stu-id="76ec6-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="76ec6-111">**N \_ netnumber**</span><span class="sxs-lookup"><span data-stu-id="76ec6-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="76ec6-112">Enthält die IPX-Netzwerk Nummer in der Computer-Byte-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="76ec6-112">Contains the IPX network number in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76ec6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76ec6-113">Requirements</span></span>



| <span data-ttu-id="76ec6-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76ec6-114">Requirement</span></span> | <span data-ttu-id="76ec6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="76ec6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="76ec6-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76ec6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="76ec6-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="76ec6-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="76ec6-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76ec6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="76ec6-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76ec6-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="76ec6-120">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="76ec6-120">End of server support</span></span><br/>    | <span data-ttu-id="76ec6-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76ec6-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="76ec6-122">Header</span><span class="sxs-lookup"><span data-stu-id="76ec6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="76ec6-123"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="76ec6-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76ec6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76ec6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ec6-125">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="76ec6-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="76ec6-126">Routing Tabellen-Manager, Version 1, Strukturen</span><span class="sxs-lookup"><span data-stu-id="76ec6-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="76ec6-127">**RTM- \_ IPX- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="76ec6-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





