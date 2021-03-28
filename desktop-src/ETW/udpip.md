---
description: Diese Klasse ist die übergeordnete Klasse für UDP/IP-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: Udpip-Klasse
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
ms.openlocfilehash: 5116b5f97a4aa7e3bafa9da1c1208ce7ee9d5794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527287"
---
# <a name="udpip-class"></a><span data-ttu-id="6a117-104">Udpip-Klasse</span><span class="sxs-lookup"><span data-stu-id="6a117-104">UdpIp class</span></span>

<span data-ttu-id="6a117-105">Diese Klasse ist die übergeordnete Klasse für UDP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="6a117-105">This class is the parent class for UDP/IP events.</span></span>

<span data-ttu-id="6a117-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="6a117-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a117-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a117-107">Syntax</span></span>

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="6a117-108">Member</span><span class="sxs-lookup"><span data-stu-id="6a117-108">Members</span></span>

<span data-ttu-id="6a117-109">Die **udpip** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="6a117-109">The **UdpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a117-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a117-110">Remarks</span></span>

<span data-ttu-id="6a117-111">Um UDP/IP-Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das Flag für das **ereignisablaufverfolgungsflag \_ \_ \_ Network \_ tcpip** im **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion</span><span class="sxs-lookup"><span data-stu-id="6a117-111">To enable UDP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="6a117-112">Ereignisablaufverfolgungsconsumer können eine spezielle Verarbeitung für UDP/IP-Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**udpipguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="6a117-112">Event trace consumers can implement special processing for UDP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**UdpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="6a117-113">Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Netzwerk Ereignis (UDP/IP) beim Verarbeiten von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6a117-113">Use the following event types to identify the actual network (UDP/IP) event when consuming events.</span></span>



| <span data-ttu-id="6a117-114">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="6a117-114">Event type</span></span>                                                         | <span data-ttu-id="6a117-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a117-115">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a117-116">**Ereignis \_ \_ \_ Empfang von Ablauf Verfolgungs Typen**(Ereignistyp Wert ist 11)</span><span class="sxs-lookup"><span data-stu-id="6a117-116">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/> | <span data-ttu-id="6a117-117">Receive-Ereignis für IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="6a117-117">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="6a117-118">Die [**udpip \_ TypeGroup1**](udpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6a117-118">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="6a117-119">**Ereignis \_ Ablaufverfolgungstyp \_ \_ senden**(Ereignistyp Wert ist 10)</span><span class="sxs-lookup"><span data-stu-id="6a117-119">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>    | <span data-ttu-id="6a117-120">Sende Ereignis für IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="6a117-120">Send event for IPv4 protocol.</span></span> <span data-ttu-id="6a117-121">Die [**udpip \_ TypeGroup1**](udpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6a117-121">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="6a117-122">Ereignistyp Wert, 17</span><span class="sxs-lookup"><span data-stu-id="6a117-122">Event type value, 17</span></span>                                               | <span data-ttu-id="6a117-123">Fehler Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6a117-123">Fail event.</span></span> <span data-ttu-id="6a117-124">Die [**udpip \_**](udpip-fail.md) -MOF-Klasse "Fail" definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6a117-124">The [**UdpIp\_Fail**](udpip-fail.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="6a117-125">Ereignistyp Wert, 26</span><span class="sxs-lookup"><span data-stu-id="6a117-125">Event type value, 26</span></span>                                               | <span data-ttu-id="6a117-126">Sende Ereignis für IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="6a117-126">Send event for IPv6 protocol.</span></span> <span data-ttu-id="6a117-127">Die [**udpip \_ TypeGroup2**](udpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6a117-127">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="6a117-128">Ereignistyp Wert, 27</span><span class="sxs-lookup"><span data-stu-id="6a117-128">Event type value, 27</span></span>                                               | <span data-ttu-id="6a117-129">Receive-Ereignis für IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="6a117-129">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="6a117-130">Die [**udpip \_ TypeGroup2**](udpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="6a117-130">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="6a117-131">Sie können Netzwerkereignisse mithilfe der **ProcessID-** Eigenschaft an einen Quell-und Ziel Prozess überführen.</span><span class="sxs-lookup"><span data-stu-id="6a117-131">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="6a117-132">Da einige Netzwerkereignisse von separaten Threads protokolliert werden, können Sie die **ProcessID** -und **ThreadId** -Member des [**Ereignis Ablauf \_ Verfolgungs \_ Headers**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) nicht verwenden, um den Prozess oder den Thread zu identifizieren, der die Netzwerkaktivitäten ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="6a117-132">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a117-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6a117-133">Requirements</span></span>



| <span data-ttu-id="6a117-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a117-134">Requirement</span></span> | <span data-ttu-id="6a117-135">Wert</span><span class="sxs-lookup"><span data-stu-id="6a117-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6a117-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a117-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6a117-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a117-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6a117-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a117-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6a117-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a117-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a117-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6a117-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a117-141">**MSNT \_ systemtrace**</span><span class="sxs-lookup"><span data-stu-id="6a117-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="6a117-142">**Udpip \_ schlägt fehl**</span><span class="sxs-lookup"><span data-stu-id="6a117-142">**UdpIp\_Fail**</span></span>](udpip-fail.md)
</dt> <dt>

[<span data-ttu-id="6a117-143">**Udpip \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="6a117-143">**UdpIp\_TypeGroup1**</span></span>](udpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="6a117-144">**Udpip \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="6a117-144">**UdpIp\_TypeGroup2**</span></span>](udpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="6a117-145">**Udpip \_ v0**</span><span class="sxs-lookup"><span data-stu-id="6a117-145">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> <dt>

[<span data-ttu-id="6a117-146">**Udpip \_ v1**</span><span class="sxs-lookup"><span data-stu-id="6a117-146">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> </dl>

 

 
