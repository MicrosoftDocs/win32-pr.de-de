---
description: In diesem Abschnitt werden die neuen Features beschrieben, die in jeder Version der Ereignis Ablauf Verfolgung für Windows hinzugefügt wurden.
ms.assetid: 5d94a6d2-2280-4a97-aa5a-c9ca2c016c84
title: Neuerungen bei der Ereignis Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613433834e5a11f2886b6ee314fdb60114f66976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753032"
---
# <a name="whats-new-in-event-tracing"></a>Neuerungen bei der Ereignis Ablauf Verfolgung

In diesem Abschnitt werden die neuen Features beschrieben, die in jeder Version der Ereignis Ablauf Verfolgung für Windows hinzugefügt wurden.

## <a name="windows-10-version-1709"></a>Windows 10, Version 1709

Etw kann nun optional Binärdateien für alle Anbieter nachverfolgen, die für die Sitzung aktiviert sind. Die Nachverfolgung gilt rückwirkend für Anbieter, die vor dem-Befehl für die Sitzung aktiviert wurden, sowie für alle zukünftigen Anbieter, die für die Sitzung aktiviert sind. Sie können jetzt auch Abfragen für die aktuell konfigurierte maximale Anzahl von systemprotokollierungen durch das Betriebssystem durchsuchen. Weitere Informationen finden Sie unter den **traceproviderbinarytracking** -und **tracemaxloggersquery** -Werten der [**Trace \_ Info \_ Class**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) -Enumeration sowie unter [Abrufen zusätzlicher Ereignis Ablauf Verfolgungs Daten](retrieving-additional-event-tracing-data.md).

Etw kann nun Ereignisse basierend auf dem Ereignis Namen filtern. Sie können auch bestimmen, auf welche Ereignisse die Stapel aufgezeichnet werden. Weitere Informationen finden Sie unter Ereignis **\_ Filter \_ Type \_ Ereignis \_ Name**, **Ereignis \_ Filter \_ Type \_ Stackwalk \_ Name** und **Ereignis \_ Filter \_ Type \_ Stackwalk \_ Level \_** kWh Values der [**Ereignis \_ Filter \_ Deskriptor**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) -Struktur sowie die zugeordneten Strukturen [**Ereignis \_ Filter \_ Ereignis \_ Name**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_name) und [**Ereignis \_ Filter \_ Ebene \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_level_kw) kWh.

## <a name="windows-10"></a>Windows 10

[Tracelogging](../tracelogging/trace-logging-portal.md) basiert auf etw und bietet eine vereinfachte Möglichkeit, Code für Native, .net-und WinRT-Entwickler zu instrumentieren. Mithilfe von tracelogging können Sie strukturierte Daten mit Ereignissen einschließen, Ereignisse korrelieren und keine separate XML-Datei des Instrumentierungs Manifests benötigen.

[Anbieter Merkmale](provider-traits.md) wurden als Methode zum Anfügen von mehr Daten an eine einzelne Anbieter Registrierung hinzugefügt. Sie können für Manifestressourcen oder tracelogging-Anbieter verwendet werden. Dies umfasst derzeit die Unterstützung für das Hinzufügen eines Anbieter namens und/oder einer Anbieter Gruppe zu einer einzelnen Anbieter Registrierung. Anbietergruppen sind ein neues Feature, mit dem mehrere ETW-Anbieter in Aggregaten von der Gruppe gesteuert werden können, zu der Sie gehören.

Der periodische Erfassungs Status ist eine Möglichkeit, Benachrichtigungen zu Erfassungs Zuständen routinemäßig an Anbieter zu senden. Wenn diese Option aktiviert ist, werden Benachrichtigungen nur an die Anbieter Registrierungen gesendet, die zuvor für die aktuelle Sitzung aktiviert wurden. Jeder Anbieter kann eine eigene Antwort (sofern vorhanden) für eine Benachrichtigung definieren. Weitere Informationen zur Implementierung finden Sie unter [**\_ Periodische \_ Aufzeichnungs \_ Status \_ Informationen**](/windows/win32/api/evntrace/ns-evntrace-trace_periodic_capture_state_info).

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 und Windows Server 2012 R2

Die folgenden Features wurden der Ereignis Ablauf Verfolgung auf Windows 8.1 und Windows Server 2012 R2 hinzugefügt.

Funktionen, die die Verwendung von Ereignis Nutzlast, Bereich und Stapel Durchlauf filtern, die von der [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) -Funktion verwendet werden, und das Aktivieren von Ablauf [**\_ Verfolgungs \_ Parametern**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) und [**Ereignis \_ Filter \_ Deskriptor**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) -Strukturen zum Filtern nach bestimmten Bedingungen in einer Protokollierungs Sitzung. Weitere Informationen finden Sie unter:

-   [**Tdhaggregatepayloadfilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
-   [**Tdhcleanuppayloadeventfilterdescriptor**](/windows/desktop/api/Tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor)
-   [**Tdhkreatepayloadfilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
-   [**Tdhdeletepayloadfilter**](/windows/desktop/api/Tdh/nf-tdh-tdhdeletepayloadfilter)

Weitere Informationen finden Sie in der umfassend überarbeiteten Dokumentation für die [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) -Funktion und in den von diesen Funktionen verwendeten Funktionen zum Aktivieren von Ablauf [**\_ Verfolgungs \_ Parametern**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) und [**Ereignis \_ Filter \_ Deskriptoren**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) .

Eine-Struktur, die ein Ereignis Nutz Last Filter-Prädikat definiert, das beschreibt, wie nach einem einzelnen Feld in einer Ablauf Verfolgungs Sitzung gefiltert wird, das von der neuen [**tdhkreatepayloadfilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter) -Funktion verwendet wird, und einer neuen Struktur, die von Ereignis-ID und Stapel Durchlauf Filtern Weitere Informationen finden Sie unter:

-   [**Ereignis \_ Filter \_ Ereignis- \_ ID**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_id)
-   [**Nutz Last \_ Filter- \_ Prädikat**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Funktionen, die Informationen zu Ereignissen abrufen, die im Anbieter Manifest vorhanden sind. Weitere Informationen finden Sie unter:

-   [**Tdhenumschlag-atemanifestproviderevents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents)
-   [**TdhGetManifestEventInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhgetmanifesteventinformation)

Eine-Struktur, die ein Array von Ereignissen in einem von der neuen [**tdheneneratemanifestproviderevents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents) -Funktion verwendeten Anbieter Manifest definiert. Weitere Informationen finden Sie unter:

-   [**Informationen zum Anbieter \_ Ereignis \_**](/windows/desktop/api/Tdh/ns-tdh-provider_event_info)

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 und Windows Server 2012

Die folgenden Funktionen wurden der Ereignis Ablauf Verfolgung unter Windows 8 und Windows Server 2012 hinzugefügt.

Funktionen, die Vorgänge für ein Registrierungs Objekt ausführen, Ereignis Nutz Last Verarbeitung bereitstellen, das Durchsuchen von Ablauf Verfolgungs Anbietern, Sitzungs Einstellungen für Abfrage Ereignisse und die Verarbeitung einer erneut protokollierten Ablauf Verfolgungs Datei bereitstellen. Weitere Informationen finden Sie unter:

-   [**Eventsetinformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation)
-   [**Tdhclosedecodinghandle**](/windows/desktop/api/Tdh/nf-tdh-tdhclosedecodinghandle)
-   [**Tdhgetdecodingparameter**](/windows/desktop/api/Tdh/nf-tdh-tdhgetdecodingparameter)
-   [**Tdhgetwppproperty**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppproperty)
-   [**Tdhgetwppmessage**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppmessage)
-   [**TdhLoadManifestFromBinary**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifestfrombinary)
-   [**Tdhopendecodinghandle**](/windows/desktop/api/Tdh/nf-tdh-tdhopendecodinghandle)
-   [**Tdhsetdecodingparameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)
-   [**Tracequeryinformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation)

Schnittstellen, die Informationen für die erneute Protokollierung für den Ablauf Verfolgungs Prozess bereitstellen, sowie für den Fall, dass Ereignisse protokolliert werden, Zugriff auf Daten für ein bestimmtes Ereignis und Zugriff auf der reloggersitzung-Funktionen, die die Bearbeitung von ETL-Dateien (Event Trace Log) ermöglichen. Weitere Informationen finden Sie unter:

-   [**Itraceevent**](/windows/desktop/api/Relogger/nn-relogger-itraceevent)
-   [**Itraceeventcallback**](/windows/desktop/api/Relogger/nn-relogger-itraceeventcallback)
-   [**Itracerelogger**](/windows/desktop/api/Relogger/nn-relogger-itracerelogger)

Weitere Enumerationen, die von den neuen Funktionen und Schnittstellen verwendet werden. Weitere Informationen finden Sie unter:

-   [**Ereignis \_ Informations \_ Klasse**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class)
-   [**\_ \_ Informations \_ Klasse der Ablauf Verfolgungs Abfrage**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 und Windows Server 2008 R2

In dieser Version wurden die folgenden Features hinzugefügt:

-   Die Fähigkeit von Anbietern, Filter im Manifest zu definieren. In Windows Vista konnten Controller Filterdaten an den Anbieter übergeben. Allerdings wurde das Layout der Filterdaten nicht im Manifest definiert, sodass der Anbieter andere Mittel verwenden muss, um die Filter Definition für Controller bereitzustellen. Mit dieser Version können Anbieter die Filter Definition im Manifest definieren (siehe das **Filter** -Attribut des komplexen Typs " [**ProviderType**](../wes/eventmanifestschema-providertype-complextype.md) "). Controller können dann mithilfe der [**tdhenreerateproviderfilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters) -Funktion die Filter Definition ermitteln. Anbieter, die Filter verwenden, müssen die [**EventWrite-Ex**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) -Funktion verwenden, um das Ereignis zu schreiben.
-   Die Möglichkeit, einen einzelnen Puffer zum Erfassen von Ereignissen zu verwenden, die auf mehreren Prozessoren generiert werden. Durch die Verwendung eines einzelnen Puffers werden Ereignisse nicht mehr in der richtigen Reihenfolge auf Computern mit mehreren Prozessoren angezeigt. Weitere Informationen finden Sie im Protokollierungs Modus [**Ereignis Ablauf \_ Verfolgung \_ \_ pro \_ Prozessor \_ Pufferung**](logging-mode-constants.md) . Standardmäßig verwendet ETW Puffer Prozessor Puffer.
-   Die Möglichkeit, eine Stapel Überwachung für Ereignisse zu erfassen. Informationen zum Aktivieren der Stapel Ablauf Verfolgung für Kernel Ereignisse finden Sie unter der [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) -Funktion. Informationen zum Aktivieren der Stapel Überwachung für Benutzer Ereignisse finden Sie im **Ereignis \_ enable \_ Property \_ Stack \_ Trace** Flag für das **enableproperty** -Element von [**enable \_ Trace \_ Parameters**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters).
-   Die Möglichkeit, den Protokollierungs Modus der **Ereignis Ablauf \_ Verfolgung \_ \_** oder den Modus für die Wiederverwendung des Datei **\_ \_ \_ \_ Modus** für die Ereignis Ablauf Verfolgung mit dem Protokollierungs Modus für **\_ \_ private \_ \_** Protokollierungs Modi der Ereignis Ablauf Verfolgung anzugeben (siehe [Protokollierungs Modus](logging-mode-constants.md)
-   Die Möglichkeit, einen Anbieter synchron zu aktivieren. Standardmäßig werden Anbieter asynchron aktiviert. Um einen Anbieter synchron zu aktivieren, legen Sie den *Timeout* -Parameter von [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)fest.
-   Die Fähigkeit des Controllers, anzufordern, dass der Anbieter seinen Zustand protokolliert. Weitere Informationen finden Sie unter Flag für den **\_ \_ Code \_ Erfassungs \_ Status des Ereignis Steuer** Elements für den *ControlCode* -Parameter von [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).
-   Die Möglichkeit für Consumer, Ereignisdaten mithilfe der [**tdhformatproperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty) -Funktion zu formatieren.
-   Die Möglichkeit, manifestierte Ereignisse auf Computern zu decodieren, die den Anbieter nicht enthalten. Weitere Informationen finden Sie unter der [**tdhloadmanifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest) -Funktion.

In dieser Version wurden die folgenden Funktionen hinzugefügt:

-   [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   [**EventWrite-Ex**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex)
-   [**Tdhenvererateproviderfilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters)
-   [**Tdhformatproperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   [**Tdhloadmanifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)
-   [**Tdhunloadmanifest**](/windows/desktop/api/Tdh/nf-tdh-tdhunloadmanifest)
-   [**Tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)

In dieser Version wurden die folgenden Strukturen hinzugefügt:

-   [**klassische \_ Ereignis- \_ ID**](/windows/win32/api/evntrace/ns-evntrace-classic_event_id)
-   [**Aktivieren von Ablauf \_ Verfolgungs \_ Parametern**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
-   [**\_Erweiterte Element Stapel für Ereignisse \_ \_ \_ TRACE32**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace32)
-   [**\_Erweiterte Element Stapel für Ereignisse \_ \_ \_ TRACE64**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace64)
-   [**Ereignis \_ Filter \_ Header**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_header)
-   [**Anbieter \_ Filter \_ Informationen**](/windows/desktop/api/Tdh/ns-tdh-provider_filter_info)

Die folgenden Enumerationen wurden in dieser Version hinzugefügt:

-   [**Trace \_ Info- \_ Klasse**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

In dieser Version wurden die folgenden MOF-Klassen hinzugefügt:

-   [**Stackwalk**](stackwalk.md)
-   [**Stackwalk- \_ Ereignis**](stackwalk-event.md)

 

 
