---
description: Diese Klasse ist die übergeordnete Klasse für TCP/IP-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: Tcpip-Klasse
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
ms.openlocfilehash: 6488ece2fd8df0670455ceea25560835c352b83e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978225"
---
# <a name="tcpip-class"></a><span data-ttu-id="14a5e-104">Tcpip-Klasse</span><span class="sxs-lookup"><span data-stu-id="14a5e-104">TcpIp class</span></span>

<span data-ttu-id="14a5e-105">Diese Klasse ist die übergeordnete Klasse für TCP/IP-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="14a5e-105">This class is the parent class for TCP/IP events.</span></span>

<span data-ttu-id="14a5e-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="14a5e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a5e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="14a5e-107">Syntax</span></span>

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="14a5e-108">Member</span><span class="sxs-lookup"><span data-stu-id="14a5e-108">Members</span></span>

<span data-ttu-id="14a5e-109">Die **tcpip** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="14a5e-109">The **TcpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="14a5e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14a5e-110">Remarks</span></span>

<span data-ttu-id="14a5e-111">Um TCP/IP-Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das **ereignisablaufverfolgungsflag \_ \_ \_ Network \_ tcpip** in dem **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="14a5e-111">To enable TCP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="14a5e-112">Ereignis Ablauf Verfolgungs Consumer können eine spezielle Verarbeitung für TCP/IP-Ereignisse implementieren, indem Sie die Funktion [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**tcpipguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="14a5e-112">Event trace consumers can implement special processing for TCP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**TcpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="14a5e-113">Verwenden Sie die folgenden Ereignis Typen, um beim Verarbeiten von Ereignissen das tatsächliche Netzwerk (TCP/IP)-Ereignis zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="14a5e-113">Use the following event types to identify the actual network (TCP/IP) event when consuming events.</span></span>



| <span data-ttu-id="14a5e-114">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="14a5e-114">Event type</span></span>                                                            | <span data-ttu-id="14a5e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14a5e-115">Description</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a5e-116">**Ereignis \_ Ablaufverfolgungstyp \_ \_ Annahme**(Ereignistyp Wert ist 15)</span><span class="sxs-lookup"><span data-stu-id="14a5e-116">**EVENT\_TRACE\_TYPE\_ACCEPT**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="14a5e-117">Akzeptieren Sie das Ereignis für das IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-117">Accept event for IPv4 protocol.</span></span> <span data-ttu-id="14a5e-118">Die [**tcpip \_ TypeGroup2**](tcpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-118">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="14a5e-119">**Ereignis \_ Ablaufverfolgungstyp \_ \_ Connect**(Ereignistyp Wert ist 12)</span><span class="sxs-lookup"><span data-stu-id="14a5e-119">**EVENT\_TRACE\_TYPE\_CONNECT**(Event type value is 12)</span></span><br/>    | <span data-ttu-id="14a5e-120">Connect-Ereignis für IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-120">Connect event for IPv4 protocol.</span></span> <span data-ttu-id="14a5e-121">Die [**tcpip \_ TypeGroup2**](tcpip-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-121">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="14a5e-122">**Ereignis \_ Ablauf Verfolgungs \_ Typen \_ Trennung**(Ereignistyp Wert ist 13)</span><span class="sxs-lookup"><span data-stu-id="14a5e-122">**EVENT\_TRACE\_TYPE\_DISCONNECT**(Event type value is 13)</span></span><br/> | <span data-ttu-id="14a5e-123">Disconnect-Ereignis für IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-123">Disconnect event for IPv4 protocol.</span></span> <span data-ttu-id="14a5e-124">Die [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-124">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="14a5e-125">**Ereignis \_ \_ \_ Empfang von Ablauf Verfolgungs Typen**(Ereignistyp Wert ist 11)</span><span class="sxs-lookup"><span data-stu-id="14a5e-125">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/>    | <span data-ttu-id="14a5e-126">Receive-Ereignis für IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-126">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="14a5e-127">Die [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-127">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="14a5e-128">**Ereignis \_ \_ \_ Reconnect** für Ablaufverfolgungstyp (Ereignistyp Wert ist 16)</span><span class="sxs-lookup"><span data-stu-id="14a5e-128">**EVENT\_TRACE\_TYPE\_RECONNECT**(Event type value is 16)</span></span><br/>  | <span data-ttu-id="14a5e-129">Reconnect-Ereignis für IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-129">Reconnect event for IPv4 protocol.</span></span> <span data-ttu-id="14a5e-130">(Ein Verbindungsversuch ist fehlgeschlagen, und es wird ein weiterer Versuch unternommen.) Die [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-130">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="14a5e-131">**Ereignis \_ \_Erneute über \_ Tragung von Ablauf Verfolgungs Typen**(Ereignistyp Wert ist 14)</span><span class="sxs-lookup"><span data-stu-id="14a5e-131">**EVENT\_TRACE\_TYPE\_RETRANSMIT**(Event type value is 14)</span></span><br/> | <span data-ttu-id="14a5e-132">Das Ereignis für das IPv4-Protokoll wird erneut übertragen.</span><span class="sxs-lookup"><span data-stu-id="14a5e-132">Retransmit event for IPv4 protocol.</span></span> <span data-ttu-id="14a5e-133">Die [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-133">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="14a5e-134">**Ereignis \_ Ablaufverfolgungstyp \_ \_ senden**(Ereignistyp Wert ist 10)</span><span class="sxs-lookup"><span data-stu-id="14a5e-134">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>       | <span data-ttu-id="14a5e-135">Sende Ereignis für IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-135">Send event for IPv4 protocol.</span></span> <span data-ttu-id="14a5e-136">Die [**tcpip \_ SendIPV4**](tcpip-sendipv4.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-136">The [**TcpIp\_SendIPV4**](tcpip-sendipv4.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="14a5e-137">Ereignistyp Wert, 17</span><span class="sxs-lookup"><span data-stu-id="14a5e-137">Event type value, 17</span></span>                                                  | <span data-ttu-id="14a5e-138">Fehler Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-138">Fail event.</span></span> <span data-ttu-id="14a5e-139">Die [**tcpip \_ Fail**](tcpip-fail.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-139">The [**TcpIp\_Fail**](tcpip-fail.md) MOF class defines the event data for this event.</span></span>                                                                                            |
| <span data-ttu-id="14a5e-140">Ereignistyp Wert, 18</span><span class="sxs-lookup"><span data-stu-id="14a5e-140">Event type value, 18</span></span>                                                  | <span data-ttu-id="14a5e-141">TCP-Kopier Ereignis für IPv4-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-141">TCP copy event for IPv4 protocol.</span></span> <span data-ttu-id="14a5e-142">Die [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-142">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                          |
| <span data-ttu-id="14a5e-143">Ereignistyp Wert, 26</span><span class="sxs-lookup"><span data-stu-id="14a5e-143">Event type value, 26</span></span>                                                  | <span data-ttu-id="14a5e-144">Sende Ereignis für IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-144">Send event for IPv6 protocol.</span></span> <span data-ttu-id="14a5e-145">Die [**tcpip \_ SendIPV6**](tcpip-sendipv6.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-145">The [**TcpIp\_SendIPV6**](tcpip-sendipv6.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="14a5e-146">Ereignistyp Wert, 27</span><span class="sxs-lookup"><span data-stu-id="14a5e-146">Event type value, 27</span></span>                                                  | <span data-ttu-id="14a5e-147">Receive-Ereignis für IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-147">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="14a5e-148">Die [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-148">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="14a5e-149">Ereignistyp Wert, 28</span><span class="sxs-lookup"><span data-stu-id="14a5e-149">Event type value, 28</span></span>                                                  | <span data-ttu-id="14a5e-150">Connect-Ereignis für IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-150">Connect event for IPv6 protocol.</span></span> <span data-ttu-id="14a5e-151">Die [**tcpip \_ TypeGroup4**](tcpip-typegroup4.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-151">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="14a5e-152">Ereignistyp Wert, 29</span><span class="sxs-lookup"><span data-stu-id="14a5e-152">Event type value, 29</span></span>                                                  | <span data-ttu-id="14a5e-153">Disconnect-Ereignis für IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-153">Disconnect event for IPv6 protocol.</span></span> <span data-ttu-id="14a5e-154">Die [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-154">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="14a5e-155">Ereignistyp Wert, 30</span><span class="sxs-lookup"><span data-stu-id="14a5e-155">Event type value, 30</span></span>                                                  | <span data-ttu-id="14a5e-156">Das Ereignis für das IPv6-Protokoll wird erneut übertragen.</span><span class="sxs-lookup"><span data-stu-id="14a5e-156">Retransmit event for IPv6 protocol.</span></span> <span data-ttu-id="14a5e-157">Die [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-157">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="14a5e-158">Ereignistyp Wert, 31</span><span class="sxs-lookup"><span data-stu-id="14a5e-158">Event type value, 31</span></span>                                                  | <span data-ttu-id="14a5e-159">Akzeptieren Sie das Ereignis für das IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-159">Accept event for IPv6 protocol.</span></span> <span data-ttu-id="14a5e-160">Die [**tcpip \_ TypeGroup4**](tcpip-typegroup4.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-160">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="14a5e-161">Ereignistyp Wert, 32</span><span class="sxs-lookup"><span data-stu-id="14a5e-161">Event type value, 32</span></span>                                                  | <span data-ttu-id="14a5e-162">Reconnect-Ereignis für IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-162">Reconnect event for IPv6 protocol.</span></span> <span data-ttu-id="14a5e-163">(Ein Verbindungsversuch ist fehlgeschlagen, und es wird ein weiterer Versuch unternommen.) Die [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-163">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="14a5e-164">Ereignistyp Wert, 34</span><span class="sxs-lookup"><span data-stu-id="14a5e-164">Event type value, 34</span></span>                                                  | <span data-ttu-id="14a5e-165">TCP-Kopier Ereignis für IPv6-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="14a5e-165">TCP copy event for IPv6 protocol.</span></span> <span data-ttu-id="14a5e-166">Die [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="14a5e-166">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                          |



 

<span data-ttu-id="14a5e-167">Sie können Netzwerkereignisse mithilfe der **ProcessID-** Eigenschaft an einen Quell-und Ziel Prozess überführen.</span><span class="sxs-lookup"><span data-stu-id="14a5e-167">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="14a5e-168">Da einige Netzwerkereignisse von separaten Threads protokolliert werden, können Sie die **ProcessID** -und **ThreadId** -Member des [**Ereignis Ablauf \_ Verfolgungs \_ Headers**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) nicht verwenden, um den Prozess oder den Thread zu identifizieren, der die Netzwerkaktivitäten ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="14a5e-168">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="14a5e-169">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="14a5e-169">Requirements</span></span>



| <span data-ttu-id="14a5e-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14a5e-170">Requirement</span></span> | <span data-ttu-id="14a5e-171">Wert</span><span class="sxs-lookup"><span data-stu-id="14a5e-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14a5e-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14a5e-172">Minimum supported client</span></span><br/> | <span data-ttu-id="14a5e-173">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14a5e-173">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="14a5e-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14a5e-174">Minimum supported server</span></span><br/> | <span data-ttu-id="14a5e-175">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14a5e-175">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14a5e-176">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14a5e-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a5e-177">**MSNT \_ systemtrace**</span><span class="sxs-lookup"><span data-stu-id="14a5e-177">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="14a5e-178">**Tcpip \_ schlägt fehl**</span><span class="sxs-lookup"><span data-stu-id="14a5e-178">**TcpIp\_Fail**</span></span>](tcpip-fail.md)
</dt> <dt>

[<span data-ttu-id="14a5e-179">**Tcpip \_ SendIPV4**</span><span class="sxs-lookup"><span data-stu-id="14a5e-179">**TcpIp\_SendIPV4**</span></span>](tcpip-sendipv4.md)
</dt> <dt>

[<span data-ttu-id="14a5e-180">**Tcpip \_ SendIPV6**</span><span class="sxs-lookup"><span data-stu-id="14a5e-180">**TcpIp\_SendIPV6**</span></span>](tcpip-sendipv6.md)
</dt> <dt>

[<span data-ttu-id="14a5e-181">**Tcpip \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="14a5e-181">**TcpIp\_TypeGroup1**</span></span>](tcpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="14a5e-182">**Tcpip \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="14a5e-182">**TcpIp\_TypeGroup2**</span></span>](tcpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="14a5e-183">**Tcpip \_ TypeGroup3**</span><span class="sxs-lookup"><span data-stu-id="14a5e-183">**TcpIp\_TypeGroup3**</span></span>](tcpip-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="14a5e-184">**Tcpip \_ TypeGroup4**</span><span class="sxs-lookup"><span data-stu-id="14a5e-184">**TcpIp\_TypeGroup4**</span></span>](tcpip-typegroup4.md)
</dt> <dt>

[<span data-ttu-id="14a5e-185">**Tcpip \_ v0**</span><span class="sxs-lookup"><span data-stu-id="14a5e-185">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> <dt>

[<span data-ttu-id="14a5e-186">**Tcpip \_ v1**</span><span class="sxs-lookup"><span data-stu-id="14a5e-186">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 
