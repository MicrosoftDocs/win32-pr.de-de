---
title: IP_NEXT_HOP_ADDRESS Struktur (RTM. h)
description: Die IP \_ \_ -Adressstruktur "Nächster Hop" \_ enthält die Adresse für den Router für den nächsten Hop für eine IP-Route.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- IP_NEXT_HOP_ADDRESS Struktur-RAS
- PIP_NEXT_HOP_ADDRESS Struktur-RAS
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1818a49e7977dbb4dfa31ebac1dae7651adb8d45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346321"
---
# <a name="ip_next_hop_address-structure"></a><span data-ttu-id="c6854-105">IP \_ - \_ Adressstruktur des nächsten Hops \_</span><span class="sxs-lookup"><span data-stu-id="c6854-105">IP\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="c6854-106">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c6854-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="c6854-107">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="c6854-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="c6854-108">Die **IP-Adressstruktur " \_ Nächster \_ Hop \_** " enthält die Adresse für den Router für den nächsten Hop für eine IP-Route.</span><span class="sxs-lookup"><span data-stu-id="c6854-108">The **IP\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IP route.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6854-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6854-109">Syntax</span></span>


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="c6854-110">Member</span><span class="sxs-lookup"><span data-stu-id="c6854-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="c6854-111">**N \_ netnumber**</span><span class="sxs-lookup"><span data-stu-id="c6854-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="c6854-112">Gibt die IP-Netzwerkadresse an, die als IP-Adresse in Computer-Byte-Reihenfolge ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="c6854-112">Specifies the IP network address expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="c6854-113">**N \_ Netzmaske**</span><span class="sxs-lookup"><span data-stu-id="c6854-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="c6854-114">Gibt die Netzwerk Maske an.</span><span class="sxs-lookup"><span data-stu-id="c6854-114">Specifies the network mask.</span></span> <span data-ttu-id="c6854-115">Wenden Sie diese Maske auf die IP-Adresse an, um die Netzwerkadresse zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="c6854-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="c6854-116">Die Netzwerk Maske befindet sich in der Computer-Byte-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="c6854-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6854-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6854-117">Remarks</span></span>

<span data-ttu-id="c6854-118">Die **IP \_ - \_ \_ Adresse für den nächsten Hop** ist eine typedef der [**IP- \_ Netzwerk**](ip-network.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="c6854-118">The **IP\_NEXT\_HOP\_ADDRESS** structure is a typedef of the [**IP\_NETWORK**](ip-network.md) structure.</span></span> <span data-ttu-id="c6854-119">Die typedef befindet sich in "RTM. h".</span><span class="sxs-lookup"><span data-stu-id="c6854-119">The typedef is in Rtm.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6854-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6854-120">Requirements</span></span>



| <span data-ttu-id="c6854-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6854-121">Requirement</span></span> | <span data-ttu-id="c6854-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c6854-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c6854-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6854-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c6854-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c6854-124">None supported</span></span><br/>                                                        |
| <span data-ttu-id="c6854-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6854-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c6854-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6854-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c6854-127">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c6854-127">End of server support</span></span><br/>    | <span data-ttu-id="c6854-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c6854-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="c6854-129">Header</span><span class="sxs-lookup"><span data-stu-id="c6854-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6854-130"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6854-130"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6854-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6854-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6854-132">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="c6854-132">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="c6854-133">Routing Tabellen-Manager, Version 1, Strukturen</span><span class="sxs-lookup"><span data-stu-id="c6854-133">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="c6854-134">**IP- \_ Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="c6854-134">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="c6854-135">**RTM \_ -IP- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="c6854-135">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





