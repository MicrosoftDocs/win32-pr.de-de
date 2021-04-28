---
description: 'UdpIp-Klasse: Diese Klasse ist die übergeordnete Klasse für UDP/IP-Ereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: UdpIp-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: d76aeb00ece18b026d9e5515a74ce830eb14af32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105388"
---
# <a name="udpip-class"></a><span data-ttu-id="98292-104">UdpIp-Klasse</span><span class="sxs-lookup"><span data-stu-id="98292-104">UdpIp class</span></span>

<span data-ttu-id="98292-105">Diese Klasse ist die übergeordnete Klasse für UDP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="98292-105">This class is the parent class for UDP/IP events.</span></span>

<span data-ttu-id="98292-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="98292-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="98292-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="98292-107">Syntax</span></span>

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="98292-108">Member</span><span class="sxs-lookup"><span data-stu-id="98292-108">Members</span></span>

<span data-ttu-id="98292-109">Die **UdpIp-Klasse** definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="98292-109">The **UdpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="98292-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98292-110">Remarks</span></span>

<span data-ttu-id="98292-111">Um UDP/IP-Ereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **FLAG EVENT TRACE FLAG NETWORK \_ \_ \_ \_ TCPIP** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an.</span><span class="sxs-lookup"><span data-stu-id="98292-111">To enable UDP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="98292-112">Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für UDP/IP-Ereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**UdpIpGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben.</span><span class="sxs-lookup"><span data-stu-id="98292-112">Event trace consumers can implement special processing for UDP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**UdpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="98292-113">Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Netzwerkereignis (UDP/IP) bei der Nutzung von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="98292-113">Use the following event types to identify the actual network (UDP/IP) event when consuming events.</span></span>



| <span data-ttu-id="98292-114">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="98292-114">Event type</span></span>                                                         | <span data-ttu-id="98292-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98292-115">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98292-116">**EVENT \_ TRACE \_ TYPE \_ RECEIVE**(Ereignistypwert ist 11)</span><span class="sxs-lookup"><span data-stu-id="98292-116">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/> | <span data-ttu-id="98292-117">Empfangsereignis für das IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="98292-117">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="98292-118">Die [**MOF-Klasse UdpIp \_ TypeGroup1**](udpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="98292-118">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="98292-119">**EVENT \_ TRACE \_ TYPE \_ SEND**(Ereignistypwert ist 10)</span><span class="sxs-lookup"><span data-stu-id="98292-119">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>    | <span data-ttu-id="98292-120">Senden des Ereignisses für das IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="98292-120">Send event for IPv4 protocol.</span></span> <span data-ttu-id="98292-121">Die [**MOF-Klasse UdpIp \_ TypeGroup1**](udpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="98292-121">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="98292-122">Ereignistypwert, 17</span><span class="sxs-lookup"><span data-stu-id="98292-122">Event type value, 17</span></span>                                               | <span data-ttu-id="98292-123">Fehlerereignis.</span><span class="sxs-lookup"><span data-stu-id="98292-123">Fail event.</span></span> <span data-ttu-id="98292-124">Die [**UdpIp \_ Fail**](udpip-fail.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="98292-124">The [**UdpIp\_Fail**](udpip-fail.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="98292-125">Ereignistypwert, 26</span><span class="sxs-lookup"><span data-stu-id="98292-125">Event type value, 26</span></span>                                               | <span data-ttu-id="98292-126">Senden eines Ereignisses für das IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="98292-126">Send event for IPv6 protocol.</span></span> <span data-ttu-id="98292-127">Die [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="98292-127">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="98292-128">Ereignistypwert, 27</span><span class="sxs-lookup"><span data-stu-id="98292-128">Event type value, 27</span></span>                                               | <span data-ttu-id="98292-129">Empfangen des Ereignisses für das IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="98292-129">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="98292-130">Die [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="98292-130">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="98292-131">Sie können Netzwerkereignisse mithilfe der **ProcessId-Eigenschaft** zu einem Quell- und Zielprozess nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="98292-131">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="98292-132">Da einige Netzwerkereignisse von separaten Threads protokolliert werden, können Sie die **ProcessId-** und **ThreadId-Member** von [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht verwenden, um den Prozess oder Thread zu identifizieren, von dem bzw. dem die Netzwerkaktivitäten stammen.</span><span class="sxs-lookup"><span data-stu-id="98292-132">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="98292-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98292-133">Requirements</span></span>



| <span data-ttu-id="98292-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98292-134">Requirement</span></span> | <span data-ttu-id="98292-135">Wert</span><span class="sxs-lookup"><span data-stu-id="98292-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="98292-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98292-136">Minimum supported client</span></span><br/> | <span data-ttu-id="98292-137">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98292-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="98292-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98292-138">Minimum supported server</span></span><br/> | <span data-ttu-id="98292-139">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98292-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98292-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="98292-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98292-141">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="98292-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="98292-142">**\_UdpIp-Fehler**</span><span class="sxs-lookup"><span data-stu-id="98292-142">**UdpIp\_Fail**</span></span>](udpip-fail.md)
</dt> <dt>

[<span data-ttu-id="98292-143">**UdpIp \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="98292-143">**UdpIp\_TypeGroup1**</span></span>](udpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="98292-144">**UdpIp \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="98292-144">**UdpIp\_TypeGroup2**</span></span>](udpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="98292-145">**UdpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="98292-145">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> <dt>

[<span data-ttu-id="98292-146">**UdpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="98292-146">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> </dl>

 

 
