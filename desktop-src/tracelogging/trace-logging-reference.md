---
title: Tracelogging-Referenz
description: In den folgenden Themen finden Sie Informationen zur nativen tracelogging-API. Tracelogging basiert auf der Ereignis Ablauf Verfolgung für Windows (ETW) und bietet eine vereinfachte Möglichkeit, Code zu instrumentieren.
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d81874e7aeb1a0618716b00d225d215c382ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390939"
---
# <a name="tracelogging-reference"></a><span data-ttu-id="2082d-103">Tracelogging-Referenz</span><span class="sxs-lookup"><span data-stu-id="2082d-103">TraceLogging Reference</span></span>

<span data-ttu-id="2082d-104">In den folgenden Themen finden Sie Informationen zur nativen tracelogging-API.</span><span class="sxs-lookup"><span data-stu-id="2082d-104">The following topics provide information about the native TraceLogging API.</span></span>

<span data-ttu-id="2082d-105">Tracelogging basiert auf der Ereignis Ablauf Verfolgung für Windows (ETW) und bietet eine vereinfachte Möglichkeit, Code zu instrumentieren.</span><span class="sxs-lookup"><span data-stu-id="2082d-105">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="2082d-106">Mithilfe von tracelogging können Sie strukturierte Daten mit Ereignissen einschließen, Ereignisse korrelieren und keine separate XML-Datei des Instrumentierungs Manifests benötigen.</span><span class="sxs-lookup"><span data-stu-id="2082d-106">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span>

<span data-ttu-id="2082d-107"><span class="underline">Für WinRT-Entwickler</span></span><span class="sxs-lookup"><span data-stu-id="2082d-107"><span class="underline">For WinRT developers</span></span></span>

-   <span data-ttu-id="2082d-108">[**Loggingchannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) wurde in Windows 10 erweitert, um die selbst Beschreibungs Ereignisse der Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw) zu protokollieren, ohne ein Manifest zu benötigen.</span><span class="sxs-lookup"><span data-stu-id="2082d-108">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span>
-   <span data-ttu-id="2082d-109">[**Loggingactivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) wurde in Windows 10 erweitert, um Aktivitäts Start-und-Endmethoden bereitzustellen, die die Kontrolle über das Format und den Inhalt der Start-und Endereignisse ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="2082d-109">[**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="2082d-110">Darüber hinaus können Aktivitäten in eine andere Liste eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2082d-110">Additionally, activities can be nested.</span></span>

<span data-ttu-id="2082d-111"><span class="underline">Für Entwickler von verwaltetem Code (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="2082d-111"><span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span>

-   <span data-ttu-id="2082d-112">Die [eventSource](/dotnet/api/system.diagnostics.tracing.eventsource) -Klasse, die mit früheren Versionen des-.NET Framework ausgeliefert wurde, unterstützt bereits das Schreiben von ETW-Ereignissen, ohne dass ein Manifest erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2082d-112">The [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="2082d-113">Entwickler mussten jedoch eventSource als Basisklasse verwenden und der abgeleiteten Klasse Attribute und Methoden hinzufügen, die automatisch in ein etw-Manifest umgewandelt wurden.</span><span class="sxs-lookup"><span data-stu-id="2082d-113">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="2082d-114">Nun müssen Entwickler nicht mehr von eventSource ableiten und stattdessen eventSource direkt zum Protokollieren von selbst beschreibenden Ereignissen verwenden, für die kein Manifest erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2082d-114">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span>

<span data-ttu-id="2082d-115"><span class="underline">Für C/C++-Entwickler</span></span><span class="sxs-lookup"><span data-stu-id="2082d-115"><span class="underline">For C/C++ developers</span></span></span>

-   <span data-ttu-id="2082d-116">"Traceloggingprovider. h" ist die empfohlene API für C/C++-Entwickler im Benutzer-oder Kernel Modus.</span><span class="sxs-lookup"><span data-stu-id="2082d-116">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="2082d-117">Diese API eignet sich nicht gut für die Verwendung in dynamischen (Skript gesteuerten) Szenarios wie JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2082d-117">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="2082d-118">Unter den folgenden Links wird die C/C++-API beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2082d-118">The following links describe the C/C++ API.</span></span>

<!-- -->

-   [<span data-ttu-id="2082d-119">Klassen</span><span class="sxs-lookup"><span data-stu-id="2082d-119">Classes</span></span>](trace-logging-classes.md)
-   [<span data-ttu-id="2082d-120">Funktionen</span><span class="sxs-lookup"><span data-stu-id="2082d-120">Functions</span></span>](trace-logging-functions.md)
-   [<span data-ttu-id="2082d-121">Makros</span><span class="sxs-lookup"><span data-stu-id="2082d-121">Macros</span></span>](trace-logging-macros.md)

<span data-ttu-id="2082d-122">Beachten Sie, dass sich der Wert von WINVER auf die Art und Weise von traceloggingprovider. h auswirkt.</span><span class="sxs-lookup"><span data-stu-id="2082d-122">Note that the value of WINVER will impact the way TraceLoggingProvider.h behaves.</span></span>

-   <span data-ttu-id="2082d-123">Wenn winver nicht festgelegt ist, bevor <Windows. h-> eingeschlossen werden, legt <Windows. h-> den winver auf einen Standardwert fest, der der SDK-Version entspricht.</span><span class="sxs-lookup"><span data-stu-id="2082d-123">If WINVER is not set before including <windows.h>, then <windows.h> will set WINVER to a default value corresponding to the SDK version.</span></span>
-   <span data-ttu-id="2082d-124">Wenn Sie "traceloggingprovider. h" verwenden und "winver" auf "0x0602 (Windows 8)" oder höher festgelegt ist, kann das Programm nicht unter Windows Vista oder Windows 7 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2082d-124">Using TraceLoggingProvider.h with WINVER set to 0x0602 (Windows 8) or higher, the program will not run on Windows Vista or Windows 7.</span></span>
-   <span data-ttu-id="2082d-125">Wenn Sie traceloggingprovider. h mit winver auf 0x0600 sein (Windows Vista) oder 0x0601 (Windows 7) festlegen, wird das Programm aus Kompatibilitätsgründen konfiguriert und funktioniert in den angegebenen Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="2082d-125">Using TraceLoggingProvider.h with WINVER set to 0x0600 (Windows Vista) or 0x0601 (Windows 7), the program will be configured for compatibility and will work on the specified versions of Windows.</span></span>

 

 