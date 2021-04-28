---
title: TraceLogging
description: TraceLogging
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7bd83c608d2ac98fdccce760c851496af80c217
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116718"
---
# <a name="tracelogging"></a><span data-ttu-id="18abb-103">TraceLogging</span><span class="sxs-lookup"><span data-stu-id="18abb-103">TraceLogging</span></span>

## <a name="purpose"></a><span data-ttu-id="18abb-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="18abb-104">Purpose</span></span>

<span data-ttu-id="18abb-105">TraceLogging ist das neue Windows 10 Framework für die Ereignisablaufverfolgung für Benutzermodusanwendungen und Kernelmodustreiber.</span><span class="sxs-lookup"><span data-stu-id="18abb-105">TraceLogging is the new Windows 10 event tracing framework for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="18abb-106">TraceLogging baut auf der Ereignisablaufverfolgung für Windows (EVENT Tracing for Windows, ETW) auf und bietet eine vereinfachte Möglichkeit zum Instrumentieren von Code.</span><span class="sxs-lookup"><span data-stu-id="18abb-106">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="18abb-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="18abb-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18abb-108">Thema</span><span class="sxs-lookup"><span data-stu-id="18abb-108">Topic</span></span></th>
<th><span data-ttu-id="18abb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18abb-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18abb-110"><a href="trace-logging-about.md">Informationen zu TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="18abb-110"><a href="trace-logging-about.md">About TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="18abb-111">TraceLogging ist die neue Windows 10 Ereignisablaufverfolgung für Benutzermodusanwendungen und Kernelmodustreiber.</span><span class="sxs-lookup"><span data-stu-id="18abb-111">TraceLogging is the new Windows 10 event tracing for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="18abb-112">TraceLogging ist ein Format für die selbstbeschreibende Ereignisablaufverfolgung für Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="18abb-112">TraceLogging is a format for self-describing Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="18abb-113">TraceLogging baut auf der Ereignisablaufverfolgung für Windows (EVENT Tracing for Windows, ETW) auf und bietet eine vereinfachte Möglichkeit zum Instrumentieren von Code.</span><span class="sxs-lookup"><span data-stu-id="18abb-113">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18abb-114"><a href="tracelogging-using-tracelogging.md">Verwenden von TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="18abb-114"><a href="tracelogging-using-tracelogging.md">Using TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="18abb-115">Die folgenden Themen enthalten einen TraceLogging-Schnellstart für nativen und verwalteten Code mit Beispielen.</span><span class="sxs-lookup"><span data-stu-id="18abb-115">The following topics provide a TraceLogging quick start for native and managed code, with examples.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18abb-116"><a href="trace-logging-reference.md">TraceLogging-Referenz</a></span><span class="sxs-lookup"><span data-stu-id="18abb-116"><a href="trace-logging-reference.md">TraceLogging Reference</a></span></span><br/></td>
<td><span data-ttu-id="18abb-117">Die folgenden Themen enthalten Informationen zur nativen TraceLogging-API.</span><span class="sxs-lookup"><span data-stu-id="18abb-117">The following topics provide information about the native TraceLogging API.</span></span><br/> <span data-ttu-id="18abb-118">TraceLogging baut auf der Ereignisablaufverfolgung für Windows (EVENT Tracing for Windows, ETW) auf und bietet eine vereinfachte Möglichkeit zum Instrumentieren von Code.</span><span class="sxs-lookup"><span data-stu-id="18abb-118">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="18abb-119">Mit TraceLogging können Sie strukturierte Daten mit Ereignissen einreihen, Ereignisse korrelieren und benötigen keine separate Instrumentierungsmanifest-XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="18abb-119">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span><br/> <span data-ttu-id="18abb-120"><span class="underline">Für WinRT-Entwickler</span></span><span class="sxs-lookup"><span data-stu-id="18abb-120"><span class="underline">For WinRT developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="18abb-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel wurde</strong></a> in Windows 10 erweitert, um selbstbeschreibende ETW-Ereignisse (Event Tracing for Windows) zu protokollieren, ohne dass ein Manifest benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="18abb-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span></li>
<li><span data-ttu-id="18abb-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> wurde in Windows 10 erweitert, um Aktivitätsstart- und -stop-Methoden zur Verfügung zu stellen, die die Kontrolle über das Format und den Inhalt der Start- und Stop-Ereignisse bieten.</span><span class="sxs-lookup"><span data-stu-id="18abb-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="18abb-123">Darüber hinaus können Aktivitäten geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="18abb-123">Additionally, activities can be nested.</span></span></li>
</ul><span data-ttu-id="18abb-124">
<span class="underline">Für Entwickler von verwaltetem Code (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="18abb-124">
<span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="18abb-125">Die <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource-Klasse,</a> die mit früheren Versionen des .NET Framework ausgeliefert wurde, unterstützt bereits das Schreiben von ETW-Ereignissen, ohne dass ein Manifest benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="18abb-125">The <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="18abb-126">Entwickler mussten jedoch EventSource als Basisklasse verwenden und der abgeleiteten Klasse Attribute und Methoden hinzufügen, die automatisch in ein ETW-Manifest umgesetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="18abb-126">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="18abb-127">Entwickler müssen jetzt nicht von EventSource ableiten und können eventSource stattdessen direkt verwenden, um selbstbeschreibende Ereignisse zu protokollieren, die kein Manifest erfordern.</span><span class="sxs-lookup"><span data-stu-id="18abb-127">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span></li>
</ul><span data-ttu-id="18abb-128">
<span class="underline">Für C/C++-Entwickler</span></span><span class="sxs-lookup"><span data-stu-id="18abb-128">
<span class="underline">For C/C++ developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="18abb-129">TraceLoggingProvider.h ist die empfohlene API für C/C++-Entwickler im Benutzer- oder Kernelmodus.</span><span class="sxs-lookup"><span data-stu-id="18abb-129">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="18abb-130">Diese API eignet sich nicht gut für die Verwendung in dynamischen (skriptgesteuerten) Szenarien wie JavaScript.</span><span class="sxs-lookup"><span data-stu-id="18abb-130">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="18abb-131">Unter den folgenden Links wird die C/C++-API beschrieben.</span><span class="sxs-lookup"><span data-stu-id="18abb-131">The following links describe the C/C++ API.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a><span data-ttu-id="18abb-132">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="18abb-132">Developer audience</span></span>

<span data-ttu-id="18abb-133">TraceLogging ist für die Verwendung durch Anwendungsentwickler im Benutzermodus und Entwickler von Kernelmodustreibern konzipiert, die ihrem Code Ablaufverfolgung hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="18abb-133">TraceLogging is designed for use by user-mode application developers and kernel-mode driver developers who want to add tracing to their code.</span></span>

