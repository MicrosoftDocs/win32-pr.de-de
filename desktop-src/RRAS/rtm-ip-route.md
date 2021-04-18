---
title: RTM_IP_ROUTE Struktur (RTM. h)
description: Die RTM \_ -IP- \_ Routen Struktur enthält Informationen, die eine Route beschreiben, die der IP-Protokollfamilie gehört.
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RTM_IP_ROUTE Struktur-RAS
- PRTM_IP_ROUTE-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1978503a3ec37e0c39716569030d5ea6599e19d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345524"
---
# <a name="rtm_ip_route-structure"></a><span data-ttu-id="d9cc2-105">RTM \_ -IP- \_ Routen Struktur</span><span class="sxs-lookup"><span data-stu-id="d9cc2-105">RTM\_IP\_ROUTE structure</span></span>

<span data-ttu-id="d9cc2-106">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9cc2-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="d9cc2-107">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="d9cc2-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="d9cc2-108">Die **RTM \_ -IP- \_ Routen** Struktur enthält Informationen, die eine Route beschreiben, die der IP-Protokollfamilie gehört.</span><span class="sxs-lookup"><span data-stu-id="d9cc2-108">The **RTM\_IP\_ROUTE** structure contains information that describes a route owned by the IP protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9cc2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9cc2-109">Syntax</span></span>


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
```



## <a name="members"></a><span data-ttu-id="d9cc2-110">Member</span><span class="sxs-lookup"><span data-stu-id="d9cc2-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d9cc2-111">**RR- \_ Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="d9cc2-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="d9cc2-112">Gibt die Uhrzeit an, zu der der Routen Eintrag erstellt oder zuletzt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d9cc2-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="d9cc2-113">Dieser Member wird vom Routing Tabellen-Manager festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9cc2-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="d9cc2-114">Die Zeit wird als FILETIME-Struktur ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="d9cc2-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="d9cc2-115">**RR \_ routingprotocol**</span><span class="sxs-lookup"><span data-stu-id="d9cc2-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="d9cc2-116">Gibt das Routing Protokoll an, das die Route hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="d9cc2-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="d9cc2-117">**RR- \_ interfakeid**</span><span class="sxs-lookup"><span data-stu-id="d9cc2-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="d9cc2-118">Gibt die Schnittstelle an, über die die Route abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d9cc2-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="d9cc2-119">**RR \_ protocolspecificdata**</span><span class="sxs-lookup"><span data-stu-id="d9cc2-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="d9cc2-120">Gibt eine [**Protokoll \_ spezifische \_ Daten**](protocol-specific-data.md) Struktur an, die Arbeitsspeicher enthält, der für Routing Protokoll spezifische Daten reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="d9cc2-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure that contains memory reserved for routing-protocol-specific data.</span></span>

</dd> <dt>

<span data-ttu-id="d9cc2-121">**RR- \_ Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="d9cc2-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="d9cc2-122">Gibt eine [**IP- \_ Netzwerk**](ip-network.md) Struktur an, die eine IP-Netzwerkadresse enthält.</span><span class="sxs-lookup"><span data-stu-id="d9cc2-122">Specifies an [**IP\_NETWORK**](ip-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="d9cc2-123">**RR \_ NextHopAddress**</span><span class="sxs-lookup"><span data-stu-id="d9cc2-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d9cc2-124">Gibt eine [**IP \_ - \_ \_ Adress**](ip-next-hop-address.md) Struktur mit dem nächsten Hop an, die die Adresse des Routers für den nächsten Hop enthält.</span><span class="sxs-lookup"><span data-stu-id="d9cc2-124">Specifies an [**IP\_NEXT\_HOP\_ADDRESS**](ip-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="d9cc2-125">**RR \_ familyspecificdata**</span><span class="sxs-lookup"><span data-stu-id="d9cc2-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="d9cc2-126">Gibt eine [**IP- \_ spezifische \_ Daten**](ip-specific-data.md) Struktur an, die für die IP-Protokollfamilie spezifische Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="d9cc2-126">Specifies an [**IP\_SPECIFIC\_DATA**](ip-specific-data.md) structure that contains IP protocol-family-specific data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9cc2-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9cc2-127">Remarks</span></span>

<span data-ttu-id="d9cc2-128">Die Mitglieder der **RTM \_ -IP- \_ Routen** Struktur sind alle **DWORD** -Elemente ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="d9cc2-128">The members of the **RTM\_IP\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9cc2-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9cc2-129">Requirements</span></span>



| <span data-ttu-id="d9cc2-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9cc2-130">Requirement</span></span> | <span data-ttu-id="d9cc2-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d9cc2-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d9cc2-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9cc2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d9cc2-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d9cc2-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="d9cc2-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9cc2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d9cc2-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9cc2-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d9cc2-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d9cc2-136">End of server support</span></span><br/>    | <span data-ttu-id="d9cc2-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d9cc2-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="d9cc2-138">Header</span><span class="sxs-lookup"><span data-stu-id="d9cc2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9cc2-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9cc2-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9cc2-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9cc2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9cc2-141">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="d9cc2-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="d9cc2-142">Routing Tabellen-Manager, Version 1, Strukturen</span><span class="sxs-lookup"><span data-stu-id="d9cc2-142">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="d9cc2-143">**IP- \_ Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="d9cc2-143">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="d9cc2-144">**IP- \_ Adresse des nächsten \_ Hops \_**</span><span class="sxs-lookup"><span data-stu-id="d9cc2-144">**IP\_NEXT\_HOP\_ADDRESS**</span></span>](ip-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="d9cc2-145">**IP- \_ spezifische \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="d9cc2-145">**IP\_SPECIFIC\_DATA**</span></span>](ip-specific-data.md)
</dt> </dl>

 

 





