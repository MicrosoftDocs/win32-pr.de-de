---
description: Listet die mit der Ereignis Ablauf Verfolgung verwendeten Elemente auf.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Referenz zur Ereignis Ablauf Verfolgung
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 7e0ee4576b9b9d64a5766c6ab096ea34abc2b176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980576"
---
# <a name="event-tracing-reference"></a><span data-ttu-id="8e067-103">Referenz zur Ereignis Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="8e067-103">Event Tracing Reference</span></span>

<span data-ttu-id="8e067-104">Verwenden Sie die folgenden Programmier Elemente zum Schreiben von Anwendungen, die die Ereignis Ablauf Verfolgung einschließen:</span><span class="sxs-lookup"><span data-stu-id="8e067-104">You use the following programming elements to write applications that incorporate event tracing:</span></span>

-   [<span data-ttu-id="8e067-105">Ereignistracing-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="8e067-105">Event Tracing Enumerations</span></span>](/windows/desktop/api/_etw/#enumerations)
-   [<span data-ttu-id="8e067-106">Funktionen der Ereignis Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="8e067-106">Event Tracing Functions</span></span>](/windows/desktop/api/_etw/#functions)
-   [<span data-ttu-id="8e067-107">Ereignis Ablauf Verfolgungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8e067-107">Event Tracing Interfaces</span></span>](/windows/desktop/api/_etw/#interfaces)
-   [<span data-ttu-id="8e067-108">Ereignisse der Ereignis Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="8e067-108">Event Tracing Structures</span></span>](/windows/desktop/api/_etw/#structures)
-   [<span data-ttu-id="8e067-109">Ereignis Ablauf Verfolgungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="8e067-109">Event Tracing Constants</span></span>](event-tracing-constants.md)

<span data-ttu-id="8e067-110">Ausführliche Informationen zu Beispielen, die diese Programmier Elemente verwenden, finden Sie unter Beispiele für die [Ereignis Ablauf Verfolgung](event-tracing-samples.md).</span><span class="sxs-lookup"><span data-stu-id="8e067-110">For details on samples that use these programming elements, see [Event Tracing Samples](event-tracing-samples.md).</span></span>

<span data-ttu-id="8e067-111">Dieser Abschnitt enthält auch Informationen zu:</span><span class="sxs-lookup"><span data-stu-id="8e067-111">This section also contains information on:</span></span>

-   <span data-ttu-id="8e067-112">Von etw bereitgestellte [Tools](event-tracing-tools.md)</span><span class="sxs-lookup"><span data-stu-id="8e067-112">[Tools](event-tracing-tools.md) that ETW provides</span></span>
-   <span data-ttu-id="8e067-113">[MOF-Klassendefinitionen](event-tracing-mof-classes.md) für Kernel Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8e067-113">[MOF class definitions](event-tracing-mof-classes.md) for kernel events</span></span>
-   <span data-ttu-id="8e067-114">[MOF-Klassen Qualifizierer](event-tracing-mof-qualifiers.md) , die beim Definieren der Ereignis Klassen verwendet</span><span class="sxs-lookup"><span data-stu-id="8e067-114">[MOF class qualifiers](event-tracing-mof-qualifiers.md) used when defining your event classes</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="8e067-115">Verarbeiten von etw-Ablauf Verfolgungen in .NET-Code</span><span class="sxs-lookup"><span data-stu-id="8e067-115">Process ETW traces in .NET code</span></span>

<span data-ttu-id="8e067-116">Sie können auch die [.net traceprocessing-API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) verwenden, um etw-Ablauf Verfolgungen für Ihre Anwendungen und andere Softwarekomponenten zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="8e067-116">You can also use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="8e067-117">Diese API wird intern bei Microsoft verwendet, um etw-Daten zu analysieren, die das Windows-Engineering-System erzeugt haben, und es wird auch verwendet, um mehrere Tabellen in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer)zu unterhalten.</span><span class="sxs-lookup"><span data-stu-id="8e067-117">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="8e067-118">Diese API ist als nuget-Paket verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8e067-118">This API is available as a NuGet package.</span></span>

<span data-ttu-id="8e067-119">[hier finden Sie weitere Informationen](/windows/apps/trace-processing/overview)</span><span class="sxs-lookup"><span data-stu-id="8e067-119">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>
