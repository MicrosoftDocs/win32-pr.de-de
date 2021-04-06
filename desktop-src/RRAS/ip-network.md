---
title: IP_NETWORK Struktur (RTM. h)
description: Die IP- \_ Netzwerkstruktur beschreibt eine IP-Netzwerkadresse.
ms.assetid: 5dcc733f-c86f-407e-8727-64f3ae71dd48
keywords:
- IP_NETWORK Struktur-RAS
- PIP_NETWORK-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- IP_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2541c493b1b2e3805e3705c71e890c6a6aaa98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742480"
---
# <a name="ip_network-structure"></a><span data-ttu-id="793a9-105">IP- \_ Netzwerkstruktur</span><span class="sxs-lookup"><span data-stu-id="793a9-105">IP\_NETWORK structure</span></span>

<span data-ttu-id="793a9-106">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="793a9-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="793a9-107">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="793a9-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="793a9-108">Die **IP- \_ Netzwerk** Struktur beschreibt eine IP-Netzwerkadresse.</span><span class="sxs-lookup"><span data-stu-id="793a9-108">The **IP\_NETWORK** structure describes an IP network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="793a9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="793a9-109">Syntax</span></span>


```C++
typedef struct _IP_NETWORK {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NETWORK, *PIP_NETWORK;
```



## <a name="members"></a><span data-ttu-id="793a9-110">Member</span><span class="sxs-lookup"><span data-stu-id="793a9-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="793a9-111">**N \_ netnumber**</span><span class="sxs-lookup"><span data-stu-id="793a9-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="793a9-112">Gibt die IP-Netzwerk Nummer an, die als IP-Adresse in Computer-Byte-Reihenfolge ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="793a9-112">Specifies the IP network number expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="793a9-113">**N \_ Netzmaske**</span><span class="sxs-lookup"><span data-stu-id="793a9-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="793a9-114">Gibt die Netzwerk Maske an.</span><span class="sxs-lookup"><span data-stu-id="793a9-114">Specifies the network mask.</span></span> <span data-ttu-id="793a9-115">Wenden Sie diese Maske auf die IP-Adresse an, um die Netzwerkadresse zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="793a9-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="793a9-116">Die Netzwerk Maske befindet sich in der Computer-Byte-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="793a9-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="793a9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="793a9-117">Requirements</span></span>



| <span data-ttu-id="793a9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="793a9-118">Requirement</span></span> | <span data-ttu-id="793a9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="793a9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="793a9-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="793a9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="793a9-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="793a9-121">None supported</span></span><br/>                                                        |
| <span data-ttu-id="793a9-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="793a9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="793a9-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="793a9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="793a9-124">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="793a9-124">End of server support</span></span><br/>    | <span data-ttu-id="793a9-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="793a9-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="793a9-126">Header</span><span class="sxs-lookup"><span data-stu-id="793a9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="793a9-127"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="793a9-127"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="793a9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="793a9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="793a9-129">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="793a9-129">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="793a9-130">Routing Tabellen-Manager, Version 1, Strukturen</span><span class="sxs-lookup"><span data-stu-id="793a9-130">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="793a9-131">**RTM \_ -IP- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="793a9-131">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





