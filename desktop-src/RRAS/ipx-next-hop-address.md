---
title: IPX_NEXT_HOP_ADDRESS Struktur (RTM. h)
description: Die IPX \_ \_ -Adressstruktur "Nächster Hop" \_ enthält die Adresse für den Router für den nächsten Hop für eine IPX-Route.
ms.assetid: 079e3284-6238-4bcf-a17f-68ff86775f18
keywords:
- IPX_NEXT_HOP_ADDRESS Struktur-RAS
- PIPX_NEXT_HOP_ADDRESS-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- IPX_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c3eb135f1d87050cd190fe47d0088fd1ab86f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475057"
---
# <a name="ipx_next_hop_address-structure"></a><span data-ttu-id="de82c-105">IPX \_ - \_ Adressstruktur "Nächster Hop" \_</span><span class="sxs-lookup"><span data-stu-id="de82c-105">IPX\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="de82c-106">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="de82c-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="de82c-107">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="de82c-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="de82c-108">Die **IPX \_ - \_ \_ Adressstruktur "Nächster Hop** " enthält die Adresse für den Router für den nächsten Hop für eine IPX-Route.</span><span class="sxs-lookup"><span data-stu-id="de82c-108">The **IPX\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IPX route.</span></span>

## <a name="syntax"></a><span data-ttu-id="de82c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="de82c-109">Syntax</span></span>


```C++
typedef struct _IPX_NEXT_HOP_ADDRESS {
  BYTE NHA_Mac[6];
} IPX_NEXT_HOP_ADDRESS, *PIPX_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="de82c-110">Member</span><span class="sxs-lookup"><span data-stu-id="de82c-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="de82c-111">**Nha- \_ Mac**</span><span class="sxs-lookup"><span data-stu-id="de82c-111">**NHA\_Mac**</span></span>
</dt> <dd>

<span data-ttu-id="de82c-112">Gibt die Mac-Adresse des Routers des nächsten Hops an.</span><span class="sxs-lookup"><span data-stu-id="de82c-112">Specifies the MAC address of next-hop router.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de82c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de82c-113">Requirements</span></span>



| <span data-ttu-id="de82c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de82c-114">Requirement</span></span> | <span data-ttu-id="de82c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="de82c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="de82c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de82c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de82c-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="de82c-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="de82c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de82c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de82c-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de82c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="de82c-120">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="de82c-120">End of server support</span></span><br/>    | <span data-ttu-id="de82c-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="de82c-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="de82c-122">Header</span><span class="sxs-lookup"><span data-stu-id="de82c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="de82c-123"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="de82c-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de82c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de82c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de82c-125">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="de82c-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="de82c-126">Routing Tabellen-Manager, Version 1, Strukturen</span><span class="sxs-lookup"><span data-stu-id="de82c-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="de82c-127">**RTM- \_ IPX- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="de82c-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





