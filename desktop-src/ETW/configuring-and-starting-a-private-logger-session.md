---
description: Eine private Ereignis Ablauf Verfolgungs Sitzung ist eine Ereignis Ablauf Verfolgungs Sitzung im Benutzermodus, die in demselben Prozess ausgeführt wird wie die Ereignis Ablauf Verfolgungs Anbieter&\# 8212; die private Sitzung und die Anbieter, die Sie aktivieren, müssen sich alle im selben Prozess befinden.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Konfigurieren und Starten einer Sitzung für private Logger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ef13728bfb3516197ab153cf90b301d5930ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485278"
---
# <a name="configuring-and-starting-a-private-logger-session"></a><span data-ttu-id="325a4-103">Konfigurieren und Starten einer Sitzung für private Logger</span><span class="sxs-lookup"><span data-stu-id="325a4-103">Configuring and Starting a Private Logger Session</span></span>

<span data-ttu-id="325a4-104">Eine private Ereignis Ablauf Verfolgungs Sitzung ist eine Ereignis Ablauf Verfolgungs Sitzung im Benutzermodus, die im selben Prozess wie die Ereignis Ablauf Verfolgungs Anbieter ausgeführt wird – die private Sitzung und die Anbieter, die Sie aktivieren, müssen sich alle im selben Prozess befinden.</span><span class="sxs-lookup"><span data-stu-id="325a4-104">A private event tracing session is a user-mode event tracing session that runs in the same process as its event trace providers—the private session and the providers that it enables must all be in the same process.</span></span> <span data-ttu-id="325a4-105">Der Vorteil der Verwendung einer privaten Sitzung besteht darin, dass die private Sitzung nicht die maximale Anzahl der gleichzeitig ausgeführten Ereignis Ablauf Verfolgungs Sitzungen in 64 anzählt.</span><span class="sxs-lookup"><span data-stu-id="325a4-105">The benefit of using a private session is that the private session does not count against the maximum of 64 event tracing sessions executing simultaneously.</span></span>

<span data-ttu-id="325a4-106">Das Konfigurieren und Starten einer privaten Sitzung ähnelt dem Starten einer normalen Ereignis Ablauf Verfolgungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="325a4-106">Configuring and starting a private session is similar to starting a normal event trace session.</span></span> <span data-ttu-id="325a4-107">Der Unterschied besteht darin, dass der **wnode. GUID** -Member der Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) die **GUID** des Anbieters und nicht die Sitzung enthalten muss und der Anbieter die GUID bereits registriert haben muss.</span><span class="sxs-lookup"><span data-stu-id="325a4-107">The difference is that **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure must contain the **GUID** of the provider, not the session, and the provider must have already registered the GUID.</span></span> <span data-ttu-id="325a4-108">Beachten Sie, dass \_ \_ \_ \_ Sie eine andere **GUID** für die Sitzung und den Anbieter verwenden können, wenn Sie auch die private Ereignis Ablauf Verfolgung im proc-Protokollierungs Modus festlegen.</span><span class="sxs-lookup"><span data-stu-id="325a4-108">Note that if you also set the EVENT\_TRACE\_PRIVATE\_IN\_PROC logging mode, you can use a different **GUID** for the session and provider.</span></span> <span data-ttu-id="325a4-109">Ausführliche Informationen zum Starten einer normalen Ereignis Ablauf Verfolgungs Sitzung finden Sie unter [Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="325a4-109">For details on starting a normal event trace session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="325a4-110">Beachten Sie, dass es nicht möglich ist, eine private Ablauf Verfolgungs Sitzung von DllMain zu starten, zu verhindern oder zu leeren. Dies sollten Sie in den Initialisierungs-und finalisierungsroutinen der dll tun.</span><span class="sxs-lookup"><span data-stu-id="325a4-110">Note that you cannot start, stop, or flush a private trace session from DllMain; you should do so in the initialization and finalization routines of the DLL.</span></span>

<span data-ttu-id="325a4-111">Von Windows 8.1 bis Windows 10, Version 1607, Ereignis Nutzlast, Bereich und Stapel Durchlauf Filter können von der [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) -Funktion und der [**enable \_ Trace \_ Parameters**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) -und [**Ereignis \_ Filter \_ Deskriptor**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) -Strukturen verwendet werden, um nach bestimmten Bedingungen in einer Protokollierungs Sitzung zu filtern.</span><span class="sxs-lookup"><span data-stu-id="325a4-111">From Windows 8.1 to Windows 10, version 1607, event payload, scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="325a4-112">Weitere Informationen zu Ereignis Nutz Last Filtern finden Sie unter den Funktionen " [**tdhkreatepayloadfilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)" und " [**tdhaggregatepayloadfilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) " und " **enable \_ Trace \_ Parameters**", **Ereignis \_ Filter \_ Deskriptor** und [**Payload \_ Filter \_ Predicate**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) Structures.</span><span class="sxs-lookup"><span data-stu-id="325a4-112">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="325a4-113">Ab Windows 10, Version 1703, können Benutzer mit geringen Rechten jetzt in Prozessen, die Sie gestartet haben, eine private Protokollierungs Sitzung starten.</span><span class="sxs-lookup"><span data-stu-id="325a4-113">Starting with Windows 10, version 1703, low privilege users can now start a private logger session in processes they started.</span></span> <span data-ttu-id="325a4-114">Der Anbieter muss nicht mehr registriert werden, bevor die private Sitzung aktiviert oder gestartet wird. Dies bedeutet, dass der Anbieter wie nicht private Sitzungs Anbieter "voraktiviert" ist.</span><span class="sxs-lookup"><span data-stu-id="325a4-114">The provider no longer needs to be registered prior to enabling or starting the private session, meaning the provider is "pre-enabled" similar to how non-private session providers are.</span></span> <span data-ttu-id="325a4-115">Es gibt eine Beschränkung auf 8 systemweite private Protokollierungen für einen einzelnen Prozess.</span><span class="sxs-lookup"><span data-stu-id="325a4-115">There is a limit of 8 system wide private loggers to an individual process.</span></span> <span data-ttu-id="325a4-116">Zur Steigerung der Leistung in prozessübergreifenden Szenarios empfiehlt es sich, beim Starten einer systemweiten privaten Protokollierung das Filtern für Sitzungs-APIs (einschließlich " [**controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)", " [**querytrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace)", " [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)" und " [**stoptrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)") zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="325a4-116">For increased performance in cross process scenarios, it's recommended to use filtering for session APIs (including [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) when starting a system wide private logger.</span></span> <span data-ttu-id="325a4-117">Beachten Sie, dass dieselben Filter an alle Sitzungs-APIs übermittelt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="325a4-117">Note that the same filters should be passed to all session APIs.</span></span> <span data-ttu-id="325a4-118">Weitere Informationen zu Filtern finden Sie unter [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften \_ v2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).</span><span class="sxs-lookup"><span data-stu-id="325a4-118">For more information about filters, see [**EVENT\_TRACE\_PROPERTIES\_V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).</span></span>

<span data-ttu-id="325a4-119">Weitere Informationen zum Starten einer Ereignis Ablauf Verfolgungs Sitzung finden Sie unter [Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="325a4-119">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="325a4-120">Weitere Informationen zum Starten einer NT-Kernel Protokollierungs Sitzung finden Sie unter [Konfigurieren und Starten der NT Kernel Logger-Sitzung](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="325a4-120">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="325a4-121">Weitere Informationen zum Starten einer globalen Protokollierungs Sitzung finden Sie unter [Konfigurieren und Starten einer globalen](configuring-and-starting-the-global-logger-session.md)Protokollierungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="325a4-121">For details on starting a Global Logger session, see [Configuring and Starting a Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="325a4-122">Weitere Informationen zum Starten einer autologger-Sitzung finden Sie unter [Konfigurieren und Starten einer autologger-Sitzung](configuring-and-starting-an-autologger-session.md).</span><span class="sxs-lookup"><span data-stu-id="325a4-122">For details on starting an AutoLogger session, see [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="325a4-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="325a4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="325a4-124">Konfigurieren und Starten einer systemtraceprovider-Sitzung</span><span class="sxs-lookup"><span data-stu-id="325a4-124">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="325a4-125">Konfigurieren und Starten einer autologger-Sitzung</span><span class="sxs-lookup"><span data-stu-id="325a4-125">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="325a4-126">Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="325a4-126">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="325a4-127">Konfigurieren und Starten der NT Kernel Logger-Sitzung</span><span class="sxs-lookup"><span data-stu-id="325a4-127">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="325a4-128">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="325a4-128">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="325a4-129">**Aktivieren von Ablauf \_ Verfolgungs \_ Parametern**</span><span class="sxs-lookup"><span data-stu-id="325a4-129">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="325a4-130">**Eigenschaften der Ereignis Ablauf \_ Verfolgung \_**</span><span class="sxs-lookup"><span data-stu-id="325a4-130">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="325a4-131">**Eigenschaften der Ereignis Ablauf \_ Verfolgung \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="325a4-131">**EVENT\_TRACE\_PROPERTIES\_V2**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[<span data-ttu-id="325a4-132">**Ereignis \_ Filter \_ Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="325a4-132">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="325a4-133">**Nutz Last \_ Filter- \_ Prädikat**</span><span class="sxs-lookup"><span data-stu-id="325a4-133">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="325a4-134">**Tdhaggregatepayloadfilters**</span><span class="sxs-lookup"><span data-stu-id="325a4-134">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="325a4-135">**Tdhkreatepayloadfilter**</span><span class="sxs-lookup"><span data-stu-id="325a4-135">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="325a4-136">Aktualisieren einer Ereignis Ablauf Verfolgungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="325a4-136">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
