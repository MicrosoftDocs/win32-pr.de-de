---
title: TraceLogging Managed Schnellstart
description: Im folgenden Abschnitt werden die grundlegenden Schritte beschrieben, die zum Hinzufügen von TraceLogging zu verwaltetem Code erforderlich sind.
ms.assetid: E144214D-8DCC-4263-8232-9F468C1A3CC0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be29e4a1bd6721b8f53dbe2394be3552ca4845143cf948f130ef55e11881b518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589240"
---
# <a name="tracelogging-managed-quick-start"></a>TraceLogging Managed Schnellstart

Im folgenden Abschnitt werden die grundlegenden Schritte beschrieben, die zum Hinzufügen von TraceLogging zu verwaltetem Code erforderlich sind.

## <a name="prerequisites"></a>Voraussetzungen

-   Windows 10

### <a name="simpletraceloggingexamplecs"></a>SimpleTraceLoggingExample.cs

In diesem Beispiel wird veranschaulicht, wie Ablaufverfolgungsprotokollierungsereignisse protokolliert werden, ohne dass manuell eine separate INSTRUMENTIERUNGsmanifest-XML-Datei erstellt werden muss.


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



### <a name="create-the-eventsource"></a>Erstellen der EventSource

Bevor Sie Ereignisse protokollieren können, müssen Sie eine Instanz der EventSource-Klasse erstellen. Der erste Konstruktorparameter identifiziert den Namen dieses Anbieters. Der Anbieter wird automatisch für Sie registriert, wie im Beispiel gezeigt.


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



Die -Instanz ist statisch, da jeweils nur eine Instanz eines bestimmten Anbieters in Ihrer Anwendung vorhanden sein sollte.

### <a name="log-tracelogging-events"></a>Protokollieren von Ablaufverfolgungsprotokollierungsereignissen

Nachdem der Anbieter erstellt wurde, protokolliert der folgende Code aus dem obigen Beispiel ein einfaches Ereignis.


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a>Protokollieren strukturierter Ereignisnutzlastdaten

Sie können strukturierte Nutzlastdaten definieren, die mit dem Ereignis protokolliert werden. Stellen Sie strukturierte Nutzlastdaten entweder als anonymen Typ oder als Instanz einer Klasse bereit, die mit dem -Attribut versehen wurde, `[EventData]` wie im folgenden Beispiel gezeigt.


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



Sie müssen das `[EventData]` Attribut den Ereignisnutzlastklassen hinzufügen, die Sie wie unten dargestellt definieren.


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



Das -Attribut ersetzt die Notwendigkeit, manuell eine Manifestdatei zu erstellen, um die Ereignisdaten zu beschreiben. Nun müssen Sie nur noch eine Instanz der -Klasse an die EventSource.Write()-Methode übergeben, um das Ereignis und die entsprechenden Nutzlastdaten zu protokollieren.

## <a name="summary-and-next-steps"></a>Zusammenfassung und nächste Schritte

Informationen zum Erfassen und Anzeigen von TraceLogging-Daten mithilfe der neuesten internen Versionen der Windows Performance Tools (WPT) finden Sie unter Aufzeichnen und Anzeigen von [TraceLogging-Ereignissen.](tracelogging-record-and-display-tracelogging-events.md)

Weitere verwaltete TraceLogging-Beispiele finden Sie unter Beispiele für die [.NET-Ablaufverfolgung.](tracelogging-net-examples.md)

 

 




