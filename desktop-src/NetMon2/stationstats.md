---
description: Die stationstats-Struktur enthält Statistiken zu einer bestimmten Station, die von der aktuellen Erfassung beschrieben wird.
ms.assetid: f85d53d6-f496-4242-875f-e173c76b046a
title: Stationstats-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0b37d4570fe8f4c27ea66e6350b79e14a10e544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042070"
---
# <a name="stationstats-structure"></a><span data-ttu-id="234b7-103">Stationstats-Struktur</span><span class="sxs-lookup"><span data-stu-id="234b7-103">STATIONSTATS structure</span></span>

<span data-ttu-id="234b7-104">Die **stationstats** -Struktur enthält Statistiken zu einer bestimmten [*Station*](s.md) , die von der aktuellen Erfassung beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="234b7-104">The **STATIONSTATS** structure provides statistics about a specific [*station*](s.md) described by the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="234b7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="234b7-105">Syntax</span></span>


```C++
typedef struct _STATIONSTATS {
  DWORD NextStationStats;
  DWORD SessionPartnerList;
  DWORD Flags;
  BYTE  StationAddress[6];
  WORD  Pad;
  DWORD TotalPacketsReceived;
  DWORD TotalDirectedPacketsSent;
  DWORD TotalBroadcastPacketsSent;
  DWORD TotalMulticastPacketsSent;
  DWORD TotalBytesReceived;
  DWORD TotalBytesSent;
} STATIONSTATS, *LPSTATIONSTATS;
```



## <a name="members"></a><span data-ttu-id="234b7-106">Member</span><span class="sxs-lookup"><span data-stu-id="234b7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="234b7-107">**Nextstationstats**</span><span class="sxs-lookup"><span data-stu-id="234b7-107">**NextStationStats**</span></span>
</dt> <dd>

<span data-ttu-id="234b7-108">Index der nächsten Station, die im **stationstats** -Struktur Array aufgezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="234b7-108">Index of the next station recorded in the **STATIONSTATS** structure array.</span></span>

</dd> <dt>

<span data-ttu-id="234b7-109">**Sessionpartnerlist**</span><span class="sxs-lookup"><span data-stu-id="234b7-109">**SessionPartnerList**</span></span>
</dt> <dd>

<span data-ttu-id="234b7-110">Index der Stations Partnerliste.</span><span class="sxs-lookup"><span data-stu-id="234b7-110">Index of the station partner list.</span></span>

</dd> <dt>

<span data-ttu-id="234b7-111">**Flags**</span><span class="sxs-lookup"><span data-stu-id="234b7-111">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="234b7-112">Dieser Member ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="234b7-112">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="234b7-113">**Stationaddress**</span><span class="sxs-lookup"><span data-stu-id="234b7-113">**StationAddress**</span></span>
</dt> <dd>

<span data-ttu-id="234b7-114">Die Mac-Adresse der Station.</span><span class="sxs-lookup"><span data-stu-id="234b7-114">The MAC address of the station.</span></span>

</dd> <dt>

<span data-ttu-id="234b7-115">**Pad**</span><span class="sxs-lookup"><span data-stu-id="234b7-115">**Pad**</span></span>
</dt> <dd>

<span data-ttu-id="234b7-116">**DWORD** -Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="234b7-116">**DWORD** alignment.</span></span>

</dd> <dt>

<span data-ttu-id="234b7-117">**Totalpacket empfangen**</span><span class="sxs-lookup"><span data-stu-id="234b7-117">**TotalPacketsReceived**</span></span>
</dt> <dd>

<span data-ttu-id="234b7-118">Gesamtanzahl der an die Station gesendeten Pakete.</span><span class="sxs-lookup"><span data-stu-id="234b7-118">Total number of packets sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="234b7-119">**Totaldirectedpacketssent**</span><span class="sxs-lookup"><span data-stu-id="234b7-119">**TotalDirectedPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="234b7-120">Die Gesamtanzahl der von der Station gesendeten gerichteten Pakete.</span><span class="sxs-lookup"><span data-stu-id="234b7-120">Total number of directed packets sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="234b7-121">**Totalbroadcastpacketssent**</span><span class="sxs-lookup"><span data-stu-id="234b7-121">**TotalBroadcastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="234b7-122">Die Gesamtanzahl der Broadcast gesteuerten Pakete (Mac-Adresse FF FF FF FF FF FF), die von der Station gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="234b7-122">Total number of broadcast-directed packets (MAC address FF FF FF FF FF FF) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="234b7-123">**Totalmulticastpacketssent**</span><span class="sxs-lookup"><span data-stu-id="234b7-123">**TotalMulticastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="234b7-124">Die Gesamtanzahl der Multicast Pakete (in der Zieladresse festgelegtes Gruppen Bit), die von der Station gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="234b7-124">Total number of multicast packets (Group bit set in destination address) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="234b7-125">**TotalBytesReceived**</span><span class="sxs-lookup"><span data-stu-id="234b7-125">**TotalBytesReceived**</span></span>
</dt> <dd>

<span data-ttu-id="234b7-126">Gesamtanzahl der an die Station gesendeten Bytes.</span><span class="sxs-lookup"><span data-stu-id="234b7-126">Total number of bytes sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="234b7-127">**TotalBytesSent**</span><span class="sxs-lookup"><span data-stu-id="234b7-127">**TotalBytesSent**</span></span>
</dt> <dd>

<span data-ttu-id="234b7-128">Die Gesamtanzahl der von der Station gesendeten Bytes.</span><span class="sxs-lookup"><span data-stu-id="234b7-128">Total number of bytes sent by the station.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="234b7-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="234b7-129">Remarks</span></span>

<span data-ttu-id="234b7-130">Netzwerkmonitor speichert Sitzungs-und Stations Informationen in zwei zugeordneten Arrays.</span><span class="sxs-lookup"><span data-stu-id="234b7-130">Network Monitor stores session and station information in two associated arrays.</span></span> <span data-ttu-id="234b7-131">, dessen Elemente [sessionstats](sessionstats.md) bzw. **stationstats** -Strukturen sind.</span><span class="sxs-lookup"><span data-stu-id="234b7-131">whose elements are [SESSIONSTATS](sessionstats.md) and **STATIONSTATS** structures respectively.</span></span> <span data-ttu-id="234b7-132">Die Member dieser Strukturen können verwendet werden, um zwischen Ihnen zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="234b7-132">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="234b7-133">Verwenden Sie beispielsweise **nextstationstats**, um zur nächsten Station zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="234b7-133">For example, to move to the next station use **NextStationStats**.</span></span> <span data-ttu-id="234b7-134">Um zur Sitzungspartner Liste im sessionstats-Array zu springen, verwenden Sie den in **sessionpartnerlist** angegebenen Index.</span><span class="sxs-lookup"><span data-stu-id="234b7-134">To jump to the session partner list in the SESSIONSTATS array, use the index provided in **SessionPartnerList**.</span></span>

> [!Note]  
> <span data-ttu-id="234b7-135">Das **stationstats** -Array enthält ein-Element für jede Station, die während der aktuellen Erfassung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="234b7-135">The **STATIONSTATS** array contains an element for each station used during the current capture.</span></span> <span data-ttu-id="234b7-136">Der Netzwerkmonitor Algorithmus, der zum Hinzufügen von Elementen zu diesem Array verwendet wird, basiert auf der effizientesten Methode, Informationen aufzuzeichnen, während die Erfassung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="234b7-136">The algorithm Network Monitor uses to add elements to this array is based on the most efficient way to record information while the capture is in progress.</span></span> <span data-ttu-id="234b7-137">Folglich ist die nächste Station nicht immer das nächste Element im Array.</span><span class="sxs-lookup"><span data-stu-id="234b7-137">Consequently, the next station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="234b7-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="234b7-138">Requirements</span></span>



| <span data-ttu-id="234b7-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="234b7-139">Requirement</span></span> | <span data-ttu-id="234b7-140">Wert</span><span class="sxs-lookup"><span data-stu-id="234b7-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="234b7-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="234b7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="234b7-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="234b7-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="234b7-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="234b7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="234b7-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="234b7-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="234b7-145">Header</span><span class="sxs-lookup"><span data-stu-id="234b7-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="234b7-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="234b7-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="234b7-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="234b7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="234b7-148">Idelta aydc:: getconversation ationstatistics</span><span class="sxs-lookup"><span data-stu-id="234b7-148">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="234b7-149">"Irren:: getconversation ationstatistics"</span><span class="sxs-lookup"><span data-stu-id="234b7-149">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="234b7-150">IStats:: getconversation ationstatistics</span><span class="sxs-lookup"><span data-stu-id="234b7-150">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




