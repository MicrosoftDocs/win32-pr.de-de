---
title: TraceLogging
description: .
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975c2f70cc645cc04d6b1461e32bb3b899097d1c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103733648"
---
# <a name="tracelogging"></a><span data-ttu-id="253b9-103">TraceLogging</span><span class="sxs-lookup"><span data-stu-id="253b9-103">TraceLogging</span></span>

## <a name="purpose"></a><span data-ttu-id="253b9-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="253b9-104">Purpose</span></span>

<span data-ttu-id="253b9-105">Tracelogging ist das neue Windows 10-Ereignis Ablauf Verfolgungs Framework für Benutzermodusanwendungen und Kernelmodustreiber.</span><span class="sxs-lookup"><span data-stu-id="253b9-105">TraceLogging is the new Windows 10 event tracing framework for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="253b9-106">Tracelogging basiert auf der Ereignis Ablauf Verfolgung für Windows (ETW) und bietet eine vereinfachte Möglichkeit, Code zu instrumentieren.</span><span class="sxs-lookup"><span data-stu-id="253b9-106">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="253b9-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="253b9-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="253b9-108">Thema</span><span class="sxs-lookup"><span data-stu-id="253b9-108">Topic</span></span></th>
<th><span data-ttu-id="253b9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="253b9-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="253b9-110"><a href="trace-logging-about.md">Informationen zu tracelogging</a></span><span class="sxs-lookup"><span data-stu-id="253b9-110"><a href="trace-logging-about.md">About TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="253b9-111">Tracelogging ist die neue Windows 10-Ereignis Ablauf Verfolgung für Benutzermodusanwendungen und Kernelmodustreiber.</span><span class="sxs-lookup"><span data-stu-id="253b9-111">TraceLogging is the new Windows 10 event tracing for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="253b9-112">Tracelogging ist ein Format für die selbst beschreibende Ereignis Ablauf Verfolgung für Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="253b9-112">TraceLogging is a format for self-describing Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="253b9-113">Tracelogging basiert auf der Ereignis Ablauf Verfolgung für Windows (ETW) und bietet eine vereinfachte Möglichkeit, Code zu instrumentieren.</span><span class="sxs-lookup"><span data-stu-id="253b9-113">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="253b9-114"><a href="tracelogging-using-tracelogging.md">Verwenden von tracelogging</a></span><span class="sxs-lookup"><span data-stu-id="253b9-114"><a href="tracelogging-using-tracelogging.md">Using TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="253b9-115">In den folgenden Themen finden Sie einen Schnellstart für einen tracelogging-Schnellstart für nativen und verwalteten Code mit Beispielen.</span><span class="sxs-lookup"><span data-stu-id="253b9-115">The following topics provide a TraceLogging quick start for native and managed code, with examples.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="253b9-116"><a href="trace-logging-reference.md">Tracelogging-Referenz</a></span><span class="sxs-lookup"><span data-stu-id="253b9-116"><a href="trace-logging-reference.md">TraceLogging Reference</a></span></span><br/></td>
<td><span data-ttu-id="253b9-117">In den folgenden Themen finden Sie Informationen zur nativen tracelogging-API.</span><span class="sxs-lookup"><span data-stu-id="253b9-117">The following topics provide information about the native TraceLogging API.</span></span><br/> <span data-ttu-id="253b9-118">Tracelogging basiert auf der Ereignis Ablauf Verfolgung für Windows (ETW) und bietet eine vereinfachte Möglichkeit, Code zu instrumentieren.</span><span class="sxs-lookup"><span data-stu-id="253b9-118">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="253b9-119">Mithilfe von tracelogging können Sie strukturierte Daten mit Ereignissen einschließen, Ereignisse korrelieren und keine separate XML-Datei des Instrumentierungs Manifests benötigen.</span><span class="sxs-lookup"><span data-stu-id="253b9-119">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span><br/> <span data-ttu-id="253b9-120"><span class="underline">Für WinRT-Entwickler</span></span><span class="sxs-lookup"><span data-stu-id="253b9-120"><span class="underline">For WinRT developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="253b9-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>Loggingchannel</strong></a> wurde in Windows 10 erweitert, um die selbst Beschreibungs Ereignisse der Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw) zu protokollieren, ohne ein Manifest zu benötigen.</span><span class="sxs-lookup"><span data-stu-id="253b9-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span></li>
<li><span data-ttu-id="253b9-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>Loggingactivity</strong></a> wurde in Windows 10 erweitert, um Aktivitäts Start-und-Endmethoden bereitzustellen, die die Kontrolle über das Format und den Inhalt der Start-und Endereignisse ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="253b9-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="253b9-123">Darüber hinaus können Aktivitäten in eine andere Liste eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="253b9-123">Additionally, activities can be nested.</span></span></li>
</ul><span data-ttu-id="253b9-124">
<span class="underline">Für Entwickler von verwaltetem Code (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="253b9-124">
<span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="253b9-125">Die <a href="/dotnet/api/system.diagnostics.tracing.eventsource">eventSource</a> -Klasse, die mit früheren Versionen des-.NET Framework ausgeliefert wurde, unterstützt bereits das Schreiben von ETW-Ereignissen, ohne dass ein Manifest erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="253b9-125">The <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="253b9-126">Entwickler mussten jedoch eventSource als Basisklasse verwenden und der abgeleiteten Klasse Attribute und Methoden hinzufügen, die automatisch in ein etw-Manifest umgewandelt wurden.</span><span class="sxs-lookup"><span data-stu-id="253b9-126">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="253b9-127">Nun müssen Entwickler nicht mehr von eventSource ableiten und stattdessen eventSource direkt zum Protokollieren von selbst beschreibenden Ereignissen verwenden, für die kein Manifest erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="253b9-127">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span></li>
</ul><span data-ttu-id="253b9-128">
<span class="underline">Für C/C++-Entwickler</span></span><span class="sxs-lookup"><span data-stu-id="253b9-128">
<span class="underline">For C/C++ developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="253b9-129">"Traceloggingprovider. h" ist die empfohlene API für C/C++-Entwickler im Benutzer-oder Kernel Modus.</span><span class="sxs-lookup"><span data-stu-id="253b9-129">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="253b9-130">Diese API eignet sich nicht gut für die Verwendung in dynamischen (Skript gesteuerten) Szenarios wie JavaScript.</span><span class="sxs-lookup"><span data-stu-id="253b9-130">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="253b9-131">Unter den folgenden Links wird die C/C++-API beschrieben.</span><span class="sxs-lookup"><span data-stu-id="253b9-131">The following links describe the C/C++ API.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a><span data-ttu-id="253b9-132">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="253b9-132">Developer audience</span></span>

<span data-ttu-id="253b9-133">Tracelogging ist für die Verwendung durch Entwicklermodus-Anwendungsentwickler und Kernel Modus-Treiber Entwickler konzipiert, die eine Ablauf Verfolgung zu Ihrem Code hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="253b9-133">TraceLogging is designed for use by user-mode application developers and kernel-mode driver developers who want to add tracing to their code.</span></span>

