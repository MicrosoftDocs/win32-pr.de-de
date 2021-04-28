---
description: 'TcpIp-Klasse: Diese Klasse ist die übergeordnete Klasse für TCP/IP-Ereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: TcpIp-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: abcd805b417451adf2122e7baf3310be101a35ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105728"
---
# <a name="tcpip-class"></a><span data-ttu-id="c178c-104">TcpIp-Klasse</span><span class="sxs-lookup"><span data-stu-id="c178c-104">TcpIp class</span></span>

<span data-ttu-id="c178c-105">Diese Klasse ist die übergeordnete Klasse für TCP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="c178c-105">This class is the parent class for TCP/IP events.</span></span>

<span data-ttu-id="c178c-106">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c178c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c178c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c178c-107">Syntax</span></span>

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="c178c-108">Member</span><span class="sxs-lookup"><span data-stu-id="c178c-108">Members</span></span>

<span data-ttu-id="c178c-109">Die **TcpIp-Klasse** definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="c178c-109">The **TcpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="c178c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c178c-110">Remarks</span></span>

<span data-ttu-id="c178c-111">Um TCP/IP-Ereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie das **EVENT TRACE FLAG NETWORK \_ \_ \_ \_ TCPIP-Flag** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an, wenn Sie die [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c178c-111">To enable TCP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="c178c-112">Consumer der Ereignisablaufverfolgung können eine spezielle Verarbeitung für TCP/IP-Ereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**TcpIpGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben.</span><span class="sxs-lookup"><span data-stu-id="c178c-112">Event trace consumers can implement special processing for TCP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**TcpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="c178c-113">Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Netzwerkereignis (TCP/IP) beim Nutzen von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c178c-113">Use the following event types to identify the actual network (TCP/IP) event when consuming events.</span></span>



| <span data-ttu-id="c178c-114">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="c178c-114">Event type</span></span>                                                            | <span data-ttu-id="c178c-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c178c-115">Description</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c178c-116">**EVENT \_ TRACE \_ TYPE \_ ACCEPT**(Ereignistypwert ist 15)</span><span class="sxs-lookup"><span data-stu-id="c178c-116">**EVENT\_TRACE\_TYPE\_ACCEPT**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="c178c-117">Accept-Ereignis für IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-117">Accept event for IPv4 protocol.</span></span> <span data-ttu-id="c178c-118">Die [**TCPIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-118">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="c178c-119">**EVENT \_ TRACE \_ TYPE \_ CONNECT**(Ereignistypwert ist 12)</span><span class="sxs-lookup"><span data-stu-id="c178c-119">**EVENT\_TRACE\_TYPE\_CONNECT**(Event type value is 12)</span></span><br/>    | <span data-ttu-id="c178c-120">Connect-Ereignis für IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-120">Connect event for IPv4 protocol.</span></span> <span data-ttu-id="c178c-121">Die [**TCPIp \_ TypeGroup2**](tcpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-121">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="c178c-122">**EVENT \_ TRACE \_ TYPE \_ DISCONNECT**(Ereignistypwert ist 13)</span><span class="sxs-lookup"><span data-stu-id="c178c-122">**EVENT\_TRACE\_TYPE\_DISCONNECT**(Event type value is 13)</span></span><br/> | <span data-ttu-id="c178c-123">Disconnect-Ereignis für IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-123">Disconnect event for IPv4 protocol.</span></span> <span data-ttu-id="c178c-124">Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-124">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="c178c-125">**EVENT \_ TRACE \_ TYPE \_ RECEIVE**(Ereignistypwert ist 11)</span><span class="sxs-lookup"><span data-stu-id="c178c-125">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/>    | <span data-ttu-id="c178c-126">Empfangsereignis für das IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-126">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="c178c-127">Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-127">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="c178c-128">**EVENT \_ TRACE \_ TYPE \_ RECONNECT**(Ereignistypwert ist 16)</span><span class="sxs-lookup"><span data-stu-id="c178c-128">**EVENT\_TRACE\_TYPE\_RECONNECT**(Event type value is 16)</span></span><br/>  | <span data-ttu-id="c178c-129">Verbindungsereignis für das IPv4-Protokoll wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="c178c-129">Reconnect event for IPv4 protocol.</span></span> <span data-ttu-id="c178c-130">(Ein Verbindungsversuch ist fehlgeschlagen, und es wird ein weiterer Versuch unternommen.) Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-130">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="c178c-131">**EVENT \_ TRACE \_ TYPE \_ RETRANSMIT**(Ereignistypwert ist 14)</span><span class="sxs-lookup"><span data-stu-id="c178c-131">**EVENT\_TRACE\_TYPE\_RETRANSMIT**(Event type value is 14)</span></span><br/> | <span data-ttu-id="c178c-132">Retransmit-Ereignis für das IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-132">Retransmit event for IPv4 protocol.</span></span> <span data-ttu-id="c178c-133">Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-133">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="c178c-134">**EVENT \_ TRACE \_ TYPE \_ SEND**(Ereignistypwert ist 10)</span><span class="sxs-lookup"><span data-stu-id="c178c-134">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>       | <span data-ttu-id="c178c-135">Senden des Ereignisses für das IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-135">Send event for IPv4 protocol.</span></span> <span data-ttu-id="c178c-136">Die [**MOF-Klasse TcpIp \_ SendIPV4**](tcpip-sendipv4.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-136">The [**TcpIp\_SendIPV4**](tcpip-sendipv4.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="c178c-137">Ereignistypwert, 17</span><span class="sxs-lookup"><span data-stu-id="c178c-137">Event type value, 17</span></span>                                                  | <span data-ttu-id="c178c-138">Fehlerereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-138">Fail event.</span></span> <span data-ttu-id="c178c-139">Die [**TCPIp \_ Fail**](tcpip-fail.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-139">The [**TcpIp\_Fail**](tcpip-fail.md) MOF class defines the event data for this event.</span></span>                                                                                            |
| <span data-ttu-id="c178c-140">Ereignistypwert, 18</span><span class="sxs-lookup"><span data-stu-id="c178c-140">Event type value, 18</span></span>                                                  | <span data-ttu-id="c178c-141">TCP-Kopierereignis für das IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-141">TCP copy event for IPv4 protocol.</span></span> <span data-ttu-id="c178c-142">Die [**MOF-Klasse TcpIp \_ TypeGroup1**](tcpip-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-142">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                          |
| <span data-ttu-id="c178c-143">Ereignistypwert, 26</span><span class="sxs-lookup"><span data-stu-id="c178c-143">Event type value, 26</span></span>                                                  | <span data-ttu-id="c178c-144">Senden eines Ereignisses für das IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-144">Send event for IPv6 protocol.</span></span> <span data-ttu-id="c178c-145">Die [**MOF-Klasse TcpIp \_ SendIPV6**](tcpip-sendipv6.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-145">The [**TcpIp\_SendIPV6**](tcpip-sendipv6.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="c178c-146">Ereignistypwert, 27</span><span class="sxs-lookup"><span data-stu-id="c178c-146">Event type value, 27</span></span>                                                  | <span data-ttu-id="c178c-147">Empfangen des Ereignisses für das IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-147">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="c178c-148">Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-148">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="c178c-149">Ereignistypwert, 28</span><span class="sxs-lookup"><span data-stu-id="c178c-149">Event type value, 28</span></span>                                                  | <span data-ttu-id="c178c-150">Connect-Ereignis für IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-150">Connect event for IPv6 protocol.</span></span> <span data-ttu-id="c178c-151">Die [**TCPIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-151">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="c178c-152">Ereignistypwert, 29</span><span class="sxs-lookup"><span data-stu-id="c178c-152">Event type value, 29</span></span>                                                  | <span data-ttu-id="c178c-153">Disconnect-Ereignis für IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-153">Disconnect event for IPv6 protocol.</span></span> <span data-ttu-id="c178c-154">Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-154">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="c178c-155">Ereignistypwert, 30</span><span class="sxs-lookup"><span data-stu-id="c178c-155">Event type value, 30</span></span>                                                  | <span data-ttu-id="c178c-156">Ereignis für erneutes Übertragen für das IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-156">Retransmit event for IPv6 protocol.</span></span> <span data-ttu-id="c178c-157">Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-157">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="c178c-158">Ereignistypwert, 31</span><span class="sxs-lookup"><span data-stu-id="c178c-158">Event type value, 31</span></span>                                                  | <span data-ttu-id="c178c-159">Accept-Ereignis für das IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-159">Accept event for IPv6 protocol.</span></span> <span data-ttu-id="c178c-160">Die [**TCPIp \_ TypeGroup4**](tcpip-typegroup4.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-160">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="c178c-161">Ereignistypwert, 32</span><span class="sxs-lookup"><span data-stu-id="c178c-161">Event type value, 32</span></span>                                                  | <span data-ttu-id="c178c-162">Ereignis zum Wiederherstellen der Verbindung für das IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-162">Reconnect event for IPv6 protocol.</span></span> <span data-ttu-id="c178c-163">(Ein Verbindungsversuch ist fehlgeschlagen, und es wird ein weiterer Versuch unternommen.) Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-163">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="c178c-164">Ereignistypwert, 34</span><span class="sxs-lookup"><span data-stu-id="c178c-164">Event type value, 34</span></span>                                                  | <span data-ttu-id="c178c-165">TCP-Kopierereignis für das IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="c178c-165">TCP copy event for IPv6 protocol.</span></span> <span data-ttu-id="c178c-166">Die [**TCPIp \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c178c-166">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                          |



 

<span data-ttu-id="c178c-167">Sie können Netzwerkereignisse mithilfe der **ProcessId-Eigenschaft** zu einem Quell- und Zielprozess nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="c178c-167">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="c178c-168">Da einige Netzwerkereignisse von separaten Threads protokolliert werden, können Sie die **ProcessId-** und **ThreadId-Member** von [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht verwenden, um den Prozess oder Thread zu identifizieren, von dem bzw. dem die Netzwerkaktivitäten stammen.</span><span class="sxs-lookup"><span data-stu-id="c178c-168">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="c178c-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c178c-169">Requirements</span></span>



| <span data-ttu-id="c178c-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c178c-170">Requirement</span></span> | <span data-ttu-id="c178c-171">Wert</span><span class="sxs-lookup"><span data-stu-id="c178c-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c178c-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c178c-172">Minimum supported client</span></span><br/> | <span data-ttu-id="c178c-173">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c178c-173">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c178c-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c178c-174">Minimum supported server</span></span><br/> | <span data-ttu-id="c178c-175">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c178c-175">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c178c-176">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c178c-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c178c-177">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="c178c-177">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="c178c-178">**\_TcpIp-Fehler**</span><span class="sxs-lookup"><span data-stu-id="c178c-178">**TcpIp\_Fail**</span></span>](tcpip-fail.md)
</dt> <dt>

[<span data-ttu-id="c178c-179">**TcpIp \_ SendIPV4**</span><span class="sxs-lookup"><span data-stu-id="c178c-179">**TcpIp\_SendIPV4**</span></span>](tcpip-sendipv4.md)
</dt> <dt>

[<span data-ttu-id="c178c-180">**TcpIp \_ SendIPV6**</span><span class="sxs-lookup"><span data-stu-id="c178c-180">**TcpIp\_SendIPV6**</span></span>](tcpip-sendipv6.md)
</dt> <dt>

[<span data-ttu-id="c178c-181">**TcpIp \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="c178c-181">**TcpIp\_TypeGroup1**</span></span>](tcpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="c178c-182">**TcpIp \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="c178c-182">**TcpIp\_TypeGroup2**</span></span>](tcpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="c178c-183">**TcpIp \_ TypeGroup3**</span><span class="sxs-lookup"><span data-stu-id="c178c-183">**TcpIp\_TypeGroup3**</span></span>](tcpip-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="c178c-184">**TcpIp \_ TypeGroup4**</span><span class="sxs-lookup"><span data-stu-id="c178c-184">**TcpIp\_TypeGroup4**</span></span>](tcpip-typegroup4.md)
</dt> <dt>

[<span data-ttu-id="c178c-185">**TcpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="c178c-185">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> <dt>

[<span data-ttu-id="c178c-186">**TcpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="c178c-186">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 
