---
description: Dieses Thema gilt für Windows XP Service Pack 2 oder höher. Die kstopology \_ -Verbindungs Struktur beschreibt eine Knoten Verbindung innerhalb eines Kernel Streaming-Filters (KS). Ein Knoten kann mit einem anderen Knoten innerhalb des Filters oder mit einer PIN im Filter verbunden werden.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: KSTOPOLOGY_CONNECTION Struktur (". h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: f523d378a54311845781c144b33e131d5875e41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371224"
---
# <a name="kstopology_connection-structure"></a><span data-ttu-id="c4ebc-105">Kstopology- \_ Verbindungs Struktur</span><span class="sxs-lookup"><span data-stu-id="c4ebc-105">KSTOPOLOGY\_CONNECTION structure</span></span>

<span data-ttu-id="c4ebc-106">Dieses Thema gilt für Windows XP Service Pack 2 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-106">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="c4ebc-107">Die **kstopology- \_ Verbindungs** Struktur beschreibt eine Knoten Verbindung innerhalb eines Kernel Streaming-Filters (KS).</span><span class="sxs-lookup"><span data-stu-id="c4ebc-107">The **KSTOPOLOGY\_CONNECTION** structure describes a node connection within a kernel-streaming (KS) filter.</span></span> <span data-ttu-id="c4ebc-108">Ein Knoten kann mit einem anderen Knoten innerhalb des Filters oder mit einer PIN im Filter verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-108">A node can be connected to another node within the filter, or to a pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4ebc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4ebc-109">Syntax</span></span>


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a><span data-ttu-id="c4ebc-110">Member</span><span class="sxs-lookup"><span data-stu-id="c4ebc-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="c4ebc-111">**Fromnode**</span><span class="sxs-lookup"><span data-stu-id="c4ebc-111">**FromNode**</span></span>
</dt> <dd>

<span data-ttu-id="c4ebc-112">Index des Upstream-Knotens in der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-112">Index of the upstream node in the connection.</span></span> <span data-ttu-id="c4ebc-113">Wenn die Upstreamverbindung anstelle eines Knotens eine PIN ist, ist der Wert der ksfilter- \_ Knoten.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-113">If the upstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="c4ebc-114">**Fromnodepin**</span><span class="sxs-lookup"><span data-stu-id="c4ebc-114">**FromNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="c4ebc-115">Wenn der Wert des Felds **fromnode** ein ksfilter- \_ Knoten ist, gibt dieses Feld den Index der upstreampin an.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-115">If the value of the **FromNode** field is KSFILTER\_NODE, this field specifies the index of the upstream pin.</span></span> <span data-ttu-id="c4ebc-116">Andernfalls wird dieses Feld ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-116">Otherwise, this field is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c4ebc-117">**ToNode**</span><span class="sxs-lookup"><span data-stu-id="c4ebc-117">**ToNode**</span></span>
</dt> <dd>

<span data-ttu-id="c4ebc-118">Index des Downstream-Knotens in der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-118">Index of the downstream node in the connection.</span></span> <span data-ttu-id="c4ebc-119">Wenn die Downstreamverbindung anstelle eines Knotens eine PIN ist, lautet der Wert ksfilter- \_ Knoten.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-119">If the downstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="c4ebc-120">**Tonodepin**</span><span class="sxs-lookup"><span data-stu-id="c4ebc-120">**ToNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="c4ebc-121">Wenn der Wert des **ToNode** -Felds der ksfilter- \_ Knoten ist, gibt dieses Feld den Index des Downstream-Pins an.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-121">If the value of the **ToNode** field is KSFILTER\_NODE, this field specifies the index of the downstream pin.</span></span> <span data-ttu-id="c4ebc-122">Andernfalls wird dieses Feld ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c4ebc-122">Otherwise, this field is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4ebc-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4ebc-123">Requirements</span></span>



| <span data-ttu-id="c4ebc-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4ebc-124">Requirement</span></span> | <span data-ttu-id="c4ebc-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c4ebc-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="c4ebc-126">Header</span><span class="sxs-lookup"><span data-stu-id="c4ebc-126">Header</span></span><br/> | <dl> <span data-ttu-id="c4ebc-127"><dt>. H.</dt></span><span class="sxs-lookup"><span data-stu-id="c4ebc-127"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4ebc-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4ebc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ebc-129">DirectShow-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c4ebc-129">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="c4ebc-130">**"IKsTopologyInfo:: get \_ ConnectionInfo"**</span><span class="sxs-lookup"><span data-stu-id="c4ebc-130">**IKsTopologyInfo::get\_ConnectionInfo**</span></span>](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




