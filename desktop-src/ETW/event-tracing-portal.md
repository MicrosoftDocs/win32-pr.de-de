---
description: Diese Dokumentation ist für Benutzermodusanwendungen vorgesehen, die ETW verwenden möchten. Informationen zum Instrumentieren von Gerätetreibern, die im Kernel Modus ausgeführt werden, finden Sie unter WPP-Software Ablauf Verfolgung und Hinzufügen von Ereignis Ablauf Verfolgung zu Kernel-Mode Treibern im Windows-Treiberkit (WDK).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Ereignisablaufverfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9802635fffddfea79c979534771605af13949d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349328"
---
# <a name="event-tracing"></a><span data-ttu-id="9c893-104">Ereignisablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="9c893-104">Event Tracing</span></span>

## <a name="purpose"></a><span data-ttu-id="9c893-105">Zweck</span><span class="sxs-lookup"><span data-stu-id="9c893-105">Purpose</span></span>

<span data-ttu-id="9c893-106">Mit der Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw) können Anwendungsprogrammierer Ereignis Ablauf Verfolgungs Sitzungen starten und beenden, eine Anwendung instrumentieren, um Ablauf Verfolgungs Ereignisse bereitzustellen und Ablauf Verfolgungs Ereignisse zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="9c893-106">Event Tracing for Windows (ETW) provides application programmers the ability to start and stop event tracing sessions, instrument an application to provide trace events, and consume trace events.</span></span> <span data-ttu-id="9c893-107">Ablauf Verfolgungs Ereignisse enthalten einen Ereignis Header und Anbieter definierte Daten, die den aktuellen Zustand einer Anwendung oder eines Vorgangs beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9c893-107">Trace events contain an event header and provider-defined data that describes the current state of an application or operation.</span></span> <span data-ttu-id="9c893-108">Sie können die-Ereignisse verwenden, um eine Anwendung zu Debuggen und die Kapazitäts-und Leistungsanalyse auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9c893-108">You can use the events to debug an application and perform capacity and performance analysis.</span></span>

<span data-ttu-id="9c893-109">Diese Dokumentation ist für Benutzermodusanwendungen vorgesehen, die ETW verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9c893-109">This documentation is for user-mode applications that want to use ETW.</span></span> <span data-ttu-id="9c893-110">Informationen zum Instrumentieren von Gerätetreibern, die im Kernel Modus ausgeführt werden, finden Sie unter [WPP-Software Ablauf Verfolgung](/windows-hardware/drivers/devtest/wpp-software-tracing) und [Hinzufügen von Ereignis Ablauf Verfolgung zu Kernel-Mode Treibern](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) im Windows-Treiberkit (WDK).</span><span class="sxs-lookup"><span data-stu-id="9c893-110">For information about instrumenting device drivers that run in kernel mode, see [WPP Software Tracing](/windows-hardware/drivers/devtest/wpp-software-tracing) and [Adding Event Tracing to Kernel-Mode Drivers](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) in the Windows Driver Kit (WDK).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="9c893-111">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="9c893-111">Where applicable</span></span>

<span data-ttu-id="9c893-112">Verwenden Sie etw, wenn Sie Ihre Anwendung instrumentieren, Benutzer-oder Kernel Ereignisse in einer Protokolldatei protokollieren und Ereignisse aus einer Protokolldatei oder in Echtzeit verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9c893-112">Use ETW when you want to instrument your application, log user or kernel events to a log file, and consume events from a log file or in real time.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9c893-113">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="9c893-113">Developer audience</span></span>

<span data-ttu-id="9c893-114">Etw wurde für C-und C++-Entwickler entwickelt, die Benutzermodus-Anwendungen schreiben.</span><span class="sxs-lookup"><span data-stu-id="9c893-114">ETW is designed for C and C++ developers who write user-mode applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9c893-115">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="9c893-115">Run-time requirements</span></span>

<span data-ttu-id="9c893-116">Etw ist in Microsoft Windows 2000 und höher enthalten.</span><span class="sxs-lookup"><span data-stu-id="9c893-116">ETW is included in Microsoft Windows 2000 and later.</span></span> <span data-ttu-id="9c893-117">Informationen dazu, welche Betriebssysteme für die Verwendung einer bestimmten Funktion erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der Dokumentation für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="9c893-117">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="9c893-118">Verarbeiten von etw-Ablauf Verfolgungen in .NET-Code</span><span class="sxs-lookup"><span data-stu-id="9c893-118">Process ETW traces in .NET code</span></span>

<span data-ttu-id="9c893-119">Sie können die [.net traceprocessing-API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) verwenden, um etw-Ablauf Verfolgungen für Ihre Anwendungen und andere Softwarekomponenten zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="9c893-119">You can use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="9c893-120">Diese API wird intern bei Microsoft verwendet, um etw-Daten zu analysieren, die das Windows-Engineering-System erzeugt haben, und es wird auch verwendet, um mehrere Tabellen in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer)zu unterhalten.</span><span class="sxs-lookup"><span data-stu-id="9c893-120">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="9c893-121">Diese API ist als nuget-Paket verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9c893-121">This API is available as a NuGet package.</span></span>

<span data-ttu-id="9c893-122">[hier finden Sie weitere Informationen](/windows/apps/trace-processing/overview)</span><span class="sxs-lookup"><span data-stu-id="9c893-122">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9c893-123">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9c893-123">In this section</span></span>



| <span data-ttu-id="9c893-124">Thema</span><span class="sxs-lookup"><span data-stu-id="9c893-124">Topic</span></span>                                                                     | <span data-ttu-id="9c893-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c893-125">Description</span></span>                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c893-126">Neuerungen bei der Ereignis Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="9c893-126">What's New in Event Tracing</span></span>](what-s-new-in-event-tracing.md)<br/> | <span data-ttu-id="9c893-127">Neue Features, die in jeder Version der Ereignis Ablauf Verfolgung hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="9c893-127">New features that were added to Event Tracing in each release.</span></span><br/>          |
| [<span data-ttu-id="9c893-128">Informationen zur Ereignis Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="9c893-128">About Event Tracing</span></span>](about-event-tracing.md)<br/>                 | <span data-ttu-id="9c893-129">Allgemeine Informationen zur Ereignis Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="9c893-129">General information about Event Tracing.</span></span><br/>                                |
| [<span data-ttu-id="9c893-130">Verwenden der Ereignis Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="9c893-130">Using Event Tracing</span></span>](using-event-tracing.md)<br/>                 | <span data-ttu-id="9c893-131">Aufgabenbezogene Themen, in denen die Verwendung der ETW-API beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="9c893-131">Task-related topics that describe how to use the ETW API.</span></span><br/>               |
| [<span data-ttu-id="9c893-132">Referenz zur Ereignis Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="9c893-132">Event Tracing Reference</span></span>](event-tracing-reference.md)<br/>         | <span data-ttu-id="9c893-133">Ausführliche Beschreibungen der etw-Funktionen und anderer Programmier Elemente.</span><span class="sxs-lookup"><span data-stu-id="9c893-133">Detailed descriptions of ETW functions and other programming elements.</span></span> <br/> |



 

 

 
