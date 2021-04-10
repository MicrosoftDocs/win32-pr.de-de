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
# <a name="tracelogging-managed-quick-start"></a>Schnellstart verwaltetes tracelogging

Im folgenden Abschnitt werden die grundlegenden Schritte zum Hinzufügen von tracelogging zu verwaltetem Code beschrieben.

## <a name="prerequisites"></a>Voraussetzungen

-   Windows 10

### <a name="simpletraceloggingexamplecs"></a>SimpleTraceLoggingExample. cs

In diesem Beispiel wird veranschaulicht, wie tracelogging-Ereignisse protokolliert werden, ohne dass manuell eine separate XML-Datei des Instrumentierungs Manifests erstellt werden muss.


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



### <a name="create-the-eventsource"></a>Erstellen der eventSource

Bevor Sie Ereignisse protokollieren können, müssen Sie eine Instanz der eventSource-Klasse erstellen. Der erste Konstruktorparameter identifiziert den Namen dieses Anbieters. Der Anbieter wird automatisch für Sie registriert, wie im Beispiel veranschaulicht.


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



Die-Instanz ist statisch, da nur jeweils eine Instanz eines bestimmten Anbieters in der Anwendung vorhanden sein sollte.

### <a name="log-tracelogging-events"></a>Protokollieren von tracelogging-Ereignissen

Nachdem der Anbieter erstellt wurde, protokolliert der folgende Code aus dem obigen Beispiel ein einfaches Ereignis.


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a>Protokollieren strukturierter Ereignis Nutzlastdaten

Sie können strukturierte Nutzlastdaten definieren, die mit dem Ereignis protokolliert werden. Stellen Sie strukturierte Nutzlastdaten entweder als anonymen Typ oder als Instanz einer Klasse bereit, die mit dem-Attribut kommentiert wurde, `[EventData]` wie im folgenden Beispiel gezeigt.


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



Sie müssen das- `[EventData]` Attribut zu den von Ihnen definierten Ereignis nutzlastklassen hinzufügen, wie unten gezeigt.


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



Das-Attribut ersetzt die Notwendigkeit, eine Manifest-Datei manuell zu erstellen, um die Ereignisdaten zu beschreiben. Nun müssen Sie lediglich eine Instanz der-Klasse an die eventSource. Write ()-Methode übergeben, um das Ereignis und zugehörige Nutzlastdaten zu protokollieren.

## <a name="summary-and-next-steps"></a>Zusammenfassung und nächste Schritte

Informationen zum Erfassen und Anzeigen von tracelogging-Daten mit den neuesten internen Versionen der Windows Performance Tools (WPT) finden Sie unter [aufzeichnen und anzeigen](tracelogging-record-and-display-tracelogging-events.md) von tracelogging-Ereignissen.

Weitere verwaltete tracelogging-Beispiele finden Sie unter [.net tracelogging-Beispiele](tracelogging-net-examples.md) .

 

 




