---
title: Schnellstart verwaltetes tracelogging
description: Im folgenden Abschnitt werden die grundlegenden Schritte zum Hinzufügen von tracelogging zu verwaltetem Code beschrieben.
ms.assetid: E144214D-8DCC-4263-8232-9F468C1A3CC0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7108dfc094f3183950dd94e5398263f4bf7cfd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309828"
---
# <a name="tracelogging-managed-quick-start"></a><span data-ttu-id="c1e74-103">Schnellstart verwaltetes tracelogging</span><span class="sxs-lookup"><span data-stu-id="c1e74-103">TraceLogging Managed Quick Start</span></span>

<span data-ttu-id="c1e74-104">Im folgenden Abschnitt werden die grundlegenden Schritte zum Hinzufügen von tracelogging zu verwaltetem Code beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c1e74-104">The following section describes the basic steps required to add TraceLogging to managed code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c1e74-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c1e74-105">Prerequisites</span></span>

-   <span data-ttu-id="c1e74-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c1e74-106">Windows 10</span></span>

### <a name="simpletraceloggingexamplecs"></a><span data-ttu-id="c1e74-107">SimpleTraceLoggingExample. cs</span><span class="sxs-lookup"><span data-stu-id="c1e74-107">SimpleTraceLoggingExample.cs</span></span>

<span data-ttu-id="c1e74-108">In diesem Beispiel wird veranschaulicht, wie tracelogging-Ereignisse protokolliert werden, ohne dass manuell eine separate XML-Datei des Instrumentierungs Manifests erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c1e74-108">This example demonstrates how to log Tracelogging events without the need to manually create a separate instrumentation manifest XML file.</span></span>


```CSharp
using System;
using System.Diagnostics.Tracing;

namespace SimpleTraceLoggingExample
{
    class Program
    {
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
        static void Main(string[] args)
        {
            log.Write("Event 1"); // write an event with no fields
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
        }
    }

    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
}
```



### <a name="create-the-eventsource"></a><span data-ttu-id="c1e74-109">Erstellen der eventSource</span><span class="sxs-lookup"><span data-stu-id="c1e74-109">Create the EventSource</span></span>

<span data-ttu-id="c1e74-110">Bevor Sie Ereignisse protokollieren können, müssen Sie eine Instanz der eventSource-Klasse erstellen.</span><span class="sxs-lookup"><span data-stu-id="c1e74-110">Before you can log events you must create an instance of the EventSource class.</span></span> <span data-ttu-id="c1e74-111">Der erste Konstruktorparameter identifiziert den Namen dieses Anbieters.</span><span class="sxs-lookup"><span data-stu-id="c1e74-111">The first constructor parameter identifies the name of this provider.</span></span> <span data-ttu-id="c1e74-112">Der Anbieter wird automatisch für Sie registriert, wie im Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c1e74-112">The provider is automatically registered for you as illustrated in the example.</span></span>


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



<span data-ttu-id="c1e74-113">Die-Instanz ist statisch, da nur jeweils eine Instanz eines bestimmten Anbieters in der Anwendung vorhanden sein sollte.</span><span class="sxs-lookup"><span data-stu-id="c1e74-113">The instance is static because there should only be one instance of a specific provider in your application at a time.</span></span>

### <a name="log-tracelogging-events"></a><span data-ttu-id="c1e74-114">Protokollieren von tracelogging-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="c1e74-114">Log Tracelogging events</span></span>

<span data-ttu-id="c1e74-115">Nachdem der Anbieter erstellt wurde, protokolliert der folgende Code aus dem obigen Beispiel ein einfaches Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c1e74-115">After the provider is created, the following code from the example above logs a simple event.</span></span>


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a><span data-ttu-id="c1e74-116">Protokollieren strukturierter Ereignis Nutzlastdaten</span><span class="sxs-lookup"><span data-stu-id="c1e74-116">Log structured event payload data</span></span>

<span data-ttu-id="c1e74-117">Sie können strukturierte Nutzlastdaten definieren, die mit dem Ereignis protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="c1e74-117">You can define structured payload data that is logged with the event.</span></span> <span data-ttu-id="c1e74-118">Stellen Sie strukturierte Nutzlastdaten entweder als anonymen Typ oder als Instanz einer Klasse bereit, die mit dem-Attribut kommentiert wurde, `[EventData]` wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1e74-118">Provide structured payload data either as an anonymous type or as an instance of a class that has been annotated with the `[EventData]` attribute as shown in the following example.</span></span>


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



<span data-ttu-id="c1e74-119">Sie müssen das- `[EventData]` Attribut zu den von Ihnen definierten Ereignis nutzlastklassen hinzufügen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c1e74-119">You must add the `[EventData]` attribute to event payload classes that you define as shown below.</span></span>


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



<span data-ttu-id="c1e74-120">Das-Attribut ersetzt die Notwendigkeit, eine Manifest-Datei manuell zu erstellen, um die Ereignisdaten zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c1e74-120">The attribute replaces the need to manually create a manifest file to describe the event data.</span></span> <span data-ttu-id="c1e74-121">Nun müssen Sie lediglich eine Instanz der-Klasse an die eventSource. Write ()-Methode übergeben, um das Ereignis und zugehörige Nutzlastdaten zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="c1e74-121">Now all you have to do is pass an instance of the class to the EventSource.Write() method to log the event and corresponding payload data.</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="c1e74-122">Zusammenfassung und nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="c1e74-122">Summary and next steps</span></span>

<span data-ttu-id="c1e74-123">Informationen zum Erfassen und Anzeigen von tracelogging-Daten mit den neuesten internen Versionen der Windows Performance Tools (WPT) finden Sie unter [aufzeichnen und anzeigen](tracelogging-record-and-display-tracelogging-events.md) von tracelogging-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="c1e74-123">See [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md) for information about how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT).</span></span>

<span data-ttu-id="c1e74-124">Weitere verwaltete tracelogging-Beispiele finden Sie unter [.net tracelogging-Beispiele](tracelogging-net-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="c1e74-124">See [.NET Tracelogging Examples](tracelogging-net-examples.md) for more managed TraceLogging examples.</span></span>

 

 




