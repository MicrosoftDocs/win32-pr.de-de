---
title: RTM_IPX_ROUTE Struktur (RTM. h)
description: Die RTM- \_ IPX- \_ Routen Struktur enthält Informationen, die eine Route für die IPX-Protokollfamilie beschreiben.
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RTM_IPX_ROUTE Struktur-RAS
- PRTM_IPX_ROUTE-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949653"
---
# <a name="rtm_ipx_route-structure"></a><span data-ttu-id="ec768-105">RTM- \_ IPX- \_ Routen Struktur</span><span class="sxs-lookup"><span data-stu-id="ec768-105">RTM\_IPX\_ROUTE structure</span></span>

<span data-ttu-id="ec768-106">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec768-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="ec768-107">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="ec768-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="ec768-108">Die **RTM- \_ IPX- \_ Routen** Struktur enthält Informationen, die eine Route für die IPX-Protokollfamilie beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ec768-108">The **RTM\_IPX\_ROUTE** structure contains information that describes a route for the IPX protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec768-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec768-109">Syntax</span></span>


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
```



## <a name="members"></a><span data-ttu-id="ec768-110">Member</span><span class="sxs-lookup"><span data-stu-id="ec768-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="ec768-111">**RR- \_ Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="ec768-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="ec768-112">Gibt die Uhrzeit an, zu der der Routen Eintrag erstellt oder zuletzt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ec768-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="ec768-113">Dieser Member wird vom Routing Tabellen-Manager festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ec768-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="ec768-114">Die Zeit wird als FILETIME-Struktur ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="ec768-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="ec768-115">**RR \_ routingprotocol**</span><span class="sxs-lookup"><span data-stu-id="ec768-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="ec768-116">Gibt das Routing Protokoll an, das die Route hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="ec768-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="ec768-117">**RR- \_ interfakeid**</span><span class="sxs-lookup"><span data-stu-id="ec768-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="ec768-118">Gibt die Schnittstelle an, über die die Route abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ec768-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="ec768-119">**RR \_ protocolspecificdata**</span><span class="sxs-lookup"><span data-stu-id="ec768-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="ec768-120">Gibt eine [**Protokoll \_ spezifische \_ Daten**](protocol-specific-data.md) Struktur mit Arbeitsspeicher an, der für die für Routing Protokolle spezifischen Daten reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="ec768-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure containing memory reserved for data specific to routing protocols.</span></span>

</dd> <dt>

<span data-ttu-id="ec768-121">**RR- \_ Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="ec768-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="ec768-122">Gibt eine [**IPX- \_ Netzwerk**](ipx-network.md) Struktur an, die eine IP-Netzwerkadresse enthält.</span><span class="sxs-lookup"><span data-stu-id="ec768-122">Specifies an [**IPX\_NETWORK**](ipx-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="ec768-123">**RR \_ NextHopAddress**</span><span class="sxs-lookup"><span data-stu-id="ec768-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ec768-124">Gibt eine [**IPX \_ - \_ \_ Adresse für den nächsten Hop**](ipx-next-hop-address.md) an, die die Adresse des Routers für den nächsten Hop enthält.</span><span class="sxs-lookup"><span data-stu-id="ec768-124">Specifies an [**IPX\_NEXT\_HOP\_ADDRESS**](ipx-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="ec768-125">**RR \_ familyspecificdata**</span><span class="sxs-lookup"><span data-stu-id="ec768-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="ec768-126">Gibt eine [**IPX- \_ spezifische \_ Daten**](ipx-specific-data.md) Struktur an, die für die IPX-Protokollfamilie spezifische Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="ec768-126">Specifies an [**IPX\_SPECIFIC\_DATA**](ipx-specific-data.md) structure that contains data specific to the IPX protocol family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec768-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec768-127">Remarks</span></span>

<span data-ttu-id="ec768-128">Die Elemente der **RTM- \_ IPX- \_ Routen** Struktur sind alle **DWORD** -Elemente ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="ec768-128">The members of the **RTM\_IPX\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec768-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec768-129">Requirements</span></span>



| <span data-ttu-id="ec768-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec768-130">Requirement</span></span> | <span data-ttu-id="ec768-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ec768-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec768-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec768-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ec768-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ec768-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="ec768-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec768-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ec768-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec768-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ec768-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ec768-136">End of server support</span></span><br/>    | <span data-ttu-id="ec768-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec768-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="ec768-138">Header</span><span class="sxs-lookup"><span data-stu-id="ec768-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec768-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec768-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec768-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec768-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec768-141">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="ec768-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="ec768-142">Routing Tabellen-Manager, Version \_ 1, \_ Strukturen</span><span class="sxs-lookup"><span data-stu-id="ec768-142">Routing Table Manager Version\_1\_Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="ec768-143">**IPX- \_ Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="ec768-143">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="ec768-144">**IPX- \_ Adresse für nächsten \_ Hop \_**</span><span class="sxs-lookup"><span data-stu-id="ec768-144">**IPX\_NEXT\_HOP\_ADDRESS**</span></span>](ipx-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="ec768-145">**IPX- \_ spezifische \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="ec768-145">**IPX\_SPECIFIC\_DATA**</span></span>](ipx-specific-data.md)
</dt> </dl>

 

 





