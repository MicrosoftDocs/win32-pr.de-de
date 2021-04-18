---
description: Die sessionstats-Struktur enthält Statistiken zu einer Sitzung.
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: Sessionstats-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4eddfa6b0a45627c59e61fd083eb11b8d5f26caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215469"
---
# <a name="sessionstats-structure"></a><span data-ttu-id="ff0c7-103">Sessionstats-Struktur</span><span class="sxs-lookup"><span data-stu-id="ff0c7-103">SESSIONSTATS structure</span></span>

<span data-ttu-id="ff0c7-104">Die **sessionstats** -Struktur enthält Statistiken zu einer [*Sitzung*](s.md).</span><span class="sxs-lookup"><span data-stu-id="ff0c7-104">The **SESSIONSTATS** structure provides statistics about a [*session*](s.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff0c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff0c7-105">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD NextSession;
  DWORD StationOwner;
  DWORD StationPartner;
  DWORD Flags;
  DWORD TotalPacketsSent;
} SESSIONSTATS, *LPSESSIONSTATS;
```



## <a name="members"></a><span data-ttu-id="ff0c7-106">Member</span><span class="sxs-lookup"><span data-stu-id="ff0c7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ff0c7-107">**Nexzession**</span><span class="sxs-lookup"><span data-stu-id="ff0c7-107">**NextSession**</span></span>
</dt> <dd>

<span data-ttu-id="ff0c7-108">Index der nächsten Sitzung des Stations Besitzers.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-108">Index of the station owner's next session.</span></span>

</dd> <dt>

<span data-ttu-id="ff0c7-109">**Stationowner**</span><span class="sxs-lookup"><span data-stu-id="ff0c7-109">**StationOwner**</span></span>
</dt> <dd>

<span data-ttu-id="ff0c7-110">Index einer Besitzer Station innerhalb des zugeordneten [Stations Statistik](stationstats.md) -Struktur Arrays.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-110">Index of a owner station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="ff0c7-111">Die Besitzer Station ist die Station, die die Sitzung initiiert hat, der Station, die die Pakete der Sitzung gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-111">The owner station is the station that initiated the session, the station that sent the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="ff0c7-112">**Stationpartner**</span><span class="sxs-lookup"><span data-stu-id="ff0c7-112">**StationPartner**</span></span>
</dt> <dd>

<span data-ttu-id="ff0c7-113">Index der anderen Station innerhalb des zugeordneten [Stations Statistik](stationstats.md) -Struktur Arrays.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-113">Index of the other station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="ff0c7-114">Die Partnerstation ist die Station, die die Pakete der Sitzung empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-114">The partner station is the station that received the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="ff0c7-115">**Flags**</span><span class="sxs-lookup"><span data-stu-id="ff0c7-115">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="ff0c7-116">Dieser Member ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-116">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="ff0c7-117">**Totalpacketssent**</span><span class="sxs-lookup"><span data-stu-id="ff0c7-117">**TotalPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="ff0c7-118">Anzahl der in der Sitzung gesendeten Pakete.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-118">Number of packets sent in the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff0c7-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff0c7-119">Remarks</span></span>

<span data-ttu-id="ff0c7-120">Netzwerkmonitor speichert Sitzungs-und Stations Informationen in zwei zugeordneten Arrays, deren Elemente **sessionstats** bzw. [stationstats](stationstats.md) -Strukturen sind.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-120">Network Monitor stores session and station information in two associated arrays, whose elements are **SESSIONSTATS** and [STATIONSTATS](stationstats.md) structures respectively.</span></span> <span data-ttu-id="ff0c7-121">Die Member dieser Strukturen können verwendet werden, um zwischen Ihnen zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-121">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="ff0c7-122">Wenn Sie z. b. zur nächsten Sitzung für einen bestimmten Stations Besitzer wechseln möchten, verwenden Sie **nexzession**.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-122">For example, to move to the next session for a specific station owner, use **NextSession**.</span></span> <span data-ttu-id="ff0c7-123">Um zum Besitzer und zur Partnerstation der Sitzung im stationstats-Array zu springen, verwenden Sie den in **stationowner** und **stationpartner** bereitgestellten Index.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-123">To jump to the owner and partner station of the session in the STATIONSTATS array, use the index provided in **StationOwner** and **StationPartner**.</span></span>

> [!Note]  
> <span data-ttu-id="ff0c7-124">Das sessionstats-Array enthält ein-Element für jede Sitzung in der aktuellen Erfassung.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-124">The SESSIONSTATS array contains an element for each session in the current capture.</span></span> <span data-ttu-id="ff0c7-125">Der Netzwerkmonitor Algorithmus, der zum Hinzufügen von Elementen zum sessionstats-Array verwendet wird, basiert auf der effizienten Aufzeichnung von Informationen, während die Erfassung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-125">The algorithm Network Monitor uses to add elements to the SESSIONSTATS array is based on efficiently recording information while the capture is in progress.</span></span> <span data-ttu-id="ff0c7-126">Folglich ist die nächste Sitzung für eine bestimmte Besitzer Station nicht immer das nächste Element im Array.</span><span class="sxs-lookup"><span data-stu-id="ff0c7-126">Consequently, the next session for a specific owner station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ff0c7-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff0c7-127">Requirements</span></span>



| <span data-ttu-id="ff0c7-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff0c7-128">Requirement</span></span> | <span data-ttu-id="ff0c7-129">Wert</span><span class="sxs-lookup"><span data-stu-id="ff0c7-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ff0c7-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff0c7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ff0c7-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff0c7-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ff0c7-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff0c7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ff0c7-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff0c7-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ff0c7-134">Header</span><span class="sxs-lookup"><span data-stu-id="ff0c7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff0c7-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff0c7-135"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff0c7-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff0c7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff0c7-137">Idelta aydc:: getconversation ationstatistics</span><span class="sxs-lookup"><span data-stu-id="ff0c7-137">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="ff0c7-138">"Irren:: getconversation ationstatistics"</span><span class="sxs-lookup"><span data-stu-id="ff0c7-138">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="ff0c7-139">IStats:: getconversation ationstatistics</span><span class="sxs-lookup"><span data-stu-id="ff0c7-139">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




