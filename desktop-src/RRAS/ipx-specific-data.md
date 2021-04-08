---
title: IPX_SPECIFIC_DATA Struktur (RTM. h)
description: Die IPX \_ \_ -spezifische Datenstruktur enthält IPX-spezifische Daten.
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- IPX_SPECIFIC_DATA Struktur-RAS
- PIPX_SPECIFIC_DATA-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56badfb6149e416c71b447aca93564b5eb5aba7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949387"
---
# <a name="ipx_specific_data-structure"></a><span data-ttu-id="81510-105">IPX- \_ spezifische \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="81510-105">IPX\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="81510-106">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="81510-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="81510-107">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="81510-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="81510-108">Die **IPX- \_ spezifische \_ Daten** Struktur enthält IPX-spezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="81510-108">The **IPX\_SPECIFIC\_DATA** structure contains IPX-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="81510-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="81510-109">Syntax</span></span>


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="81510-110">Member</span><span class="sxs-lookup"><span data-stu-id="81510-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="81510-111">**F- \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="81510-111">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="81510-112">Gibt Flags an, die die Route beschreiben.</span><span class="sxs-lookup"><span data-stu-id="81510-112">Specifies flags that describe the route.</span></span> <span data-ttu-id="81510-113">Derzeit ist dieser Member entweder NULL oder der folgende Flagwert.</span><span class="sxs-lookup"><span data-stu-id="81510-113">Currently, this member is either zero or the following flag value.</span></span>



| <span data-ttu-id="81510-114">Wert</span><span class="sxs-lookup"><span data-stu-id="81510-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="81510-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="81510-115">Meaning</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <span data-ttu-id="81510-116"><dt>**globale IPX- \_ \_ Client-WAN- \_ \_ Route**</dt></span><span class="sxs-lookup"><span data-stu-id="81510-116"><dt>**IPX\_GLOBAL\_CLIENT\_WAN\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="81510-117">Gibt an, dass diese Route für das globale Netzwerk bestimmt ist, das allen WAN-Clients zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="81510-117">Specifies that this route is for the global network allocated for all WAN clients.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="81510-118">**Anzahl der Aktivier- \_ Tickanzahl**</span><span class="sxs-lookup"><span data-stu-id="81510-118">**FSD\_TickCount**</span></span>
</dt> <dd>

<span data-ttu-id="81510-119">Gibt die Anzahl der Ticks an, die zum Erreichen des Ziel Netzwerks benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="81510-119">Specifies the number of ticks it takes to reach the destination network.</span></span> <span data-ttu-id="81510-120">Bei anderen Routing Protokollen als RIP sollten ihre Metriken in Ticks konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="81510-120">Routing protocols other than RIP should convert their metrics into ticks.</span></span>

</dd> <dt>

<span data-ttu-id="81510-121">**Anzahl von "f SD" \_**</span><span class="sxs-lookup"><span data-stu-id="81510-121">**FSD\_HopCount**</span></span>
</dt> <dd>

<span data-ttu-id="81510-122">Gibt die Hopanzahl an, die der Route zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="81510-122">Specifies the hop count associated with the route.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81510-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81510-123">Requirements</span></span>



| <span data-ttu-id="81510-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81510-124">Requirement</span></span> | <span data-ttu-id="81510-125">Wert</span><span class="sxs-lookup"><span data-stu-id="81510-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="81510-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81510-126">Minimum supported client</span></span><br/> | <span data-ttu-id="81510-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="81510-127">None supported</span></span><br/>                                                        |
| <span data-ttu-id="81510-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81510-128">Minimum supported server</span></span><br/> | <span data-ttu-id="81510-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81510-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="81510-130">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="81510-130">End of server support</span></span><br/>    | <span data-ttu-id="81510-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="81510-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="81510-132">Header</span><span class="sxs-lookup"><span data-stu-id="81510-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="81510-133"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="81510-133"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81510-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81510-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81510-135">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="81510-135">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="81510-136">Routing Tabellen-Manager, Version 1, Strukturen</span><span class="sxs-lookup"><span data-stu-id="81510-136">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="81510-137">**RTM- \_ IPX- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="81510-137">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





