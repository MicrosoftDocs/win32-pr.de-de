---
description: In diesem Abschnitt werden die neuen Features beschrieben, die der Ereignisablaufverfolgung für Windows in jedem Release hinzugefügt wurden.
ms.assetid: 5d94a6d2-2280-4a97-aa5a-c9ca2c016c84
title: Neues bei der Ereignisablaufverfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da1c6f1b54ae8bc4b91bd511bface8569bcf43b2893329b1b0462b46c001724
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102020"
---
# <a name="whats-new-in-event-tracing"></a>Neues bei der Ereignisablaufverfolgung

In diesem Abschnitt werden die neuen Features beschrieben, die der Ereignisablaufverfolgung für Windows in jedem Release hinzugefügt wurden.

## <a name="windows-10-version-1709"></a>Windows 10, Version 1709

ETW kann jetzt optional Binärdateien für alle Anbieter nachverfolgen, die für die Sitzung aktiviert sind. Die Nachverfolgung gilt rückwirkend für Anbieter, die vor dem Aufruf für die Sitzung aktiviert wurden, sowie für alle zukünftigen Anbieter, die für die Sitzung aktiviert wurden. Sie können jetzt auch die derzeit konfigurierte maximale Anzahl von Systemprotokollen abfragen, die vom Betriebssystem zugelassen wird. Weitere Informationen finden Sie unter den **TraceProviderBinaryTracking-** und **TraceMaxLoggersQuery-Werten** der [**TRACE INFO \_ \_ CLASS-Enumeration**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) sowie unter Abrufen zusätzlicher Ereignisablaufverfolgungsdaten. [](retrieving-additional-event-tracing-data.md)

ETW kann jetzt Ereignisse basierend auf dem Ereignisnamen filtern. Sie können auch bestimmen, welche Ereignisse ihre Stapel erfassen. Weitere Informationen finden Sie in den Werten EVENT **\_ FILTER TYPE EVENT \_ \_ \_ NAME**, EVENT **FILTER TYPE \_ \_ \_ STACKWALK \_ NAME** und EVENT **FILTER TYPE \_ \_ \_ STACKWALK LEVEL \_ \_ KW** der [**EVENT FILTER \_ \_ DESCRIPTOR-Struktur**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) sowie in den zugeordneten [**EVENT FILTER EVENT \_ \_ \_ NAME-**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_name) und [**EVENT FILTER LEVEL \_ \_ \_ KW-Strukturen.**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_level_kw)

## <a name="windows-10"></a>Windows 10

[TraceLogging](../tracelogging/trace-logging-portal.md) baut auf ETW auf und bietet eine vereinfachte Möglichkeit zum Instrumentieren von Code für native .NET- und WinRT-Entwickler. Mit TraceLogging können Sie strukturierte Daten mit Ereignissen einreihen, Ereignisse korrelieren und benötigen keine separate INSTRUMENTIERUNGsmanifest-XML-Datei.

[Anbietermerkmale wurden als](provider-traits.md) Methode zum Anfügen von mehr Daten an eine individuelle Anbieterregistrierung hinzugefügt. Sie können für manifestbasierte anbieter oder TraceLogging-Anbieter verwendet werden. Dies umfasst derzeit unterstützung für das Hinzufügen eines Anbieternamens und/oder einer Anbietergruppe zu einer individuellen Anbieterregistrierung. Anbietergruppen sind ein neues Feature, mit dem mehrere ETW-Anbieter aggregiert durch die Gruppe gesteuert werden können, zu der sie gehören.

Der periodische Erfassungszustand ist eine Möglichkeit, das routinemäßige Senden von Erfassungsstatusbenachrichtigungen an Anbieter zu ermöglichen. Wenn dies aktiviert ist, werden Benachrichtigungen nur an Anbieterregistrierungen gesendet, die zuvor für die aktuelle Sitzung aktiviert wurden. Jeder Anbieter kann eine eigene Antwort (falls eine solche) auf eine Benachrichtigung definieren. Implementierungsdetails finden Sie unter [**TRACE PERIODIC CAPTURE STATE \_ \_ \_ \_ INFO**](/windows/win32/api/evntrace/ns-evntrace-trace_periodic_capture_state_info).

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 und Windows Server 2012 R2

Die folgenden Funktionen wurden der Ereignisablaufverfolgung auf Windows 8.1 und Windows Server 2012 R2 hinzugefügt.

Funktionen, die die Verwendung von Ereignisnutzlast-, Bereichs- und Stapel-Walkfiltern unterstützen, die von der [**EnableTraceEx2-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) und den [**ENABLE TRACE \_ \_ PARAMETERS-**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) und [**EVENT FILTER \_ \_ DESCRIPTOR-Strukturen**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) verwendet werden, um nach bestimmten Bedingungen in einer Protokollierungssitzung zu filtern. Weitere Informationen finden Sie unter

-   [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
-   [**TdhCleanupPayloadEventFilterDescriptor**](/windows/desktop/api/Tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor)
-   [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
-   [**TdhDeletePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhdeletepayloadfilter)

Lesen Sie darüber hinaus die umfassend überarbeitete Dokumentation für die [**EnableTraceEx2-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) und die [**ENABLE TRACE \_ \_ PARAMETERS-**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) und [**EVENT \_ \_ FILTER-DESCRIPTOR-Strukturen,**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) die von diesen Funktionen verwendet werden.

Eine Struktur, die ein Ereignisnutzlastfilter-Prädikat definiert, das beschreibt, wie nach einem einzelnen Feld in einer Ablaufverfolgungssitzung gefiltert wird, die von der neuen [**TdhCreatePayloadFilter-Funktion**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter) verwendet wird, und eine neue Struktur, die von Ereignis-ID- und Stapel-Walkfiltern verwendet wird. Weitere Informationen finden Sie unter

-   [**\_ \_ \_ EREIGNISFILTER-EREIGNIS-ID**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_id)
-   [**\_ \_ NUTZLASTFILTER-PRÄDIKAT**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Funktionen, die Informationen zu Ereignissen abrufen, die im Anbietermanifest vorhanden sind. Weitere Informationen finden Sie unter

-   [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents)
-   [**TdhGetManifestEventInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhgetmanifesteventinformation)

Eine -Struktur, die ein Array von Ereignissen in einem Anbietermanifest definiert, das von der neuen [**TdhEnumerateManifestProviderEvents-Funktion verwendet**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents) wird. Weitere Informationen finden Sie unter

-   [**\_ \_ ANBIETEREREIGNISINFORMATIONEN**](/windows/desktop/api/Tdh/ns-tdh-provider_event_info)

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 und Windows Server 2012

Die folgenden Funktionen wurden der Ereignisablaufverfolgung auf Windows 8 und Windows Server 2012.

Funktionen, die Vorgänge für ein Registrierungsobjekt ausführen, Ereignisnutzlasten-Analyse bereitstellen, Suchvorgänge des Ablaufverfolgungsanbieters bereitstellen, Sitzungseinstellungen für die Ereignisablaufverfolgung abfragen und eine neuprotokollierte Ablaufverfolgungsdatei verarbeiten. Weitere Informationen finden Sie unter

-   [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation)
-   [**TdhCloseDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhclosedecodinghandle)
-   [**TdhGetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhgetdecodingparameter)
-   [**TdhGetWppProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppproperty)
-   [**TdhGetWppMessage**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppmessage)
-   [**TdhLoadManifestFromBinary**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifestfrombinary)
-   [**TdhOpenDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhopendecodinghandle)
-   [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)
-   [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation)

Schnittstellen, die Informationen zur Neuprotokollierung des Ablaufverfolgungsprozesses und zum Protokollieren von Ereignissen bereitstellen, Zugriff auf Daten für ein bestimmtes Ereignis und Zugriff auf Reloggerfunktionen, die die Bearbeitung von Ereignisablaufverfolgungsprotokolldateien (Event Trace Log, ETL) ermöglichen. Weitere Informationen finden Sie unter

-   [**ITraceEvent**](/windows/desktop/api/Relogger/nn-relogger-itraceevent)
-   [**ITraceEventCallback**](/windows/desktop/api/Relogger/nn-relogger-itraceeventcallback)
-   [**ITraceRelogger**](/windows/desktop/api/Relogger/nn-relogger-itracerelogger)

Zusätzliche Enumerationen, die von den neuen Funktionen und Schnittstellen verwendet werden. Weitere Informationen finden Sie unter

-   [**\_ \_ EREIGNISINFORMATIONSKLASSE**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class)
-   [**TRACE \_ QUERY \_ \_ INFO-KLASSE**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 und Windows Server 2008 R2

In dieser Version wurden die folgenden Features hinzugefügt:

-   Die Fähigkeit von Anbietern, Filter im Manifest zu definieren. In Windows Vista könnten Controller Filterdaten an den Anbieter übergeben. Das Layout der Filterdaten wurde jedoch nicht im Manifest definiert, sodass der Anbieter andere Mittel verwenden muss, um die Filterdefinition controllern zur Verfügung zu stellen. Mit diesem Release können Anbieter die Filterdefinition im  Manifest definieren (siehe filter-Attribut des komplexen [**ProviderType-Typs).**](../wes/eventmanifestschema-providertype-complextype.md) Controller können dann die [**TdhEnumerateProviderFilters-Funktion**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters) verwenden, um die Filterdefinition zu bestimmen. Anbieter, die Filter verwenden, sollten die [**EventWriteEx-Funktion**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) verwenden, um das Ereignis zu schreiben.
-   Die Möglichkeit, einen einzelnen Puffer zum Sammeln von Ereignissen zu verwenden, die auf mehreren Prozessoren generiert werden. Die Verwendung eines einzelnen Puffers verhindert, dass Ereignisse auf Computern mit mehreren Prozessoren nicht mehr in der Reihenfolge angezeigt werden. Weitere Informationen finden Sie im [**Protokollierungsmodus \_ EREIGNISVERFOLGUNG \_ NEIN PRO \_ \_ \_ PROZESSORPUFFERUNG.**](logging-mode-constants.md) Standardmäßig verwendet ETW Puffer pro Prozessor.
-   Die Fähigkeit, eine Stapelüberwachung für Ereignisse zu erfassen. Informationen zum Aktivieren der Stapelablaufverfolgung für Kernelereignisse finden Sie in der [**TraceSetInformation-Funktion.**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) Informationen zum Aktivieren der Stapelablaufverfolgung für Benutzerereignisse finden Sie unter dem **EVENT ENABLE PROPERTY STACK \_ \_ \_ \_ TRACE-Flag** für den **EnableProperty-Member** [**von ENABLE TRACE \_ \_ PARAMETERS.**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
-   Die Möglichkeit, den **EVENT \_ TRACE \_ BUFFERING \_ MODE** oder **DEN EVENT TRACE FILE MODE \_ \_ \_ \_ NEWFILE-Protokollierungsmodus** mit dem Protokollierungsmodus EVENT TRACE PRIVATE **\_ \_ \_ LOGGER \_ MODE** anzugeben (siehe [Protokollierungsmoduskonst constants](logging-mode-constants.md)).
-   Die Fähigkeit, einen Anbieter synchron zu aktivieren. Standardmäßig werden Anbieter asynchron aktiviert. Um einen Anbieter synchron zu aktivieren, legen Sie den *Timeout-Parameter* von [**EnableTraceEx2 fest.**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   Die Fähigkeit des Controllers, den Zustand des Anbieters zu protokollieren. Weitere Informationen finden Sie unter dem **FLAG EVENT CONTROL CODE CAPTURE \_ \_ \_ \_ STATE** für den *ControlCode-Parameter* von [**EnableTraceEx2.**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   Die Fähigkeit von Consumers, Ereignisdaten mithilfe der [**TdhFormatProperty-Funktion zu**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty) formatieren.
-   Die Möglichkeit, manifestierte Ereignisse auf Computern zu decodieren, die den Anbieter nicht enthalten. Weitere Informationen finden Sie in der [**TdhLoadManifest-Funktion.**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)

In dieser Version wurden die folgenden Funktionen hinzugefügt:

-   [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex)
-   [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters)
-   [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)
-   [**TdhUnloadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhunloadmanifest)
-   [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)

In dieser Version wurden die folgenden Strukturen hinzugefügt:

-   [**KLASSISCHE \_ \_ EREIGNIS-ID**](/windows/win32/api/evntrace/ns-evntrace-classic_event_id)
-   [**AKTIVIEREN VON \_ ABLAUFVERFOLGUNGSPARAMETERN \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
-   [**ABLAUFVERFOLGUNG \_ DES ERWEITERTEN \_ \_ ELEMENTSTAPELS \_ FÜR EREIGNISSE32**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace32)
-   [**ABLAUFVERFOLGUNG \_ DES ERWEITERTEN \_ \_ ELEMENTSTAPELS \_ FÜR EREIGNISSE64**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace64)
-   [**\_ \_ EREIGNISFILTERHEADER**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_header)
-   [**\_ \_ ANBIETERFILTERINFORMATIONEN**](/windows/desktop/api/Tdh/ns-tdh-provider_filter_info)

Die folgenden Enumerationen wurden in dieser Version hinzugefügt:

-   [**TRACE \_ \_ INFO-KLASSE**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

Die folgenden MOF-Klassen wurden in dieser Version hinzugefügt:

-   [**StackWalk**](stackwalk.md)
-   [**\_StackWalk-Ereignis**](stackwalk-event.md)

 

 
