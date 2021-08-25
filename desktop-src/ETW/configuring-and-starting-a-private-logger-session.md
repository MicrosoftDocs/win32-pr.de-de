---
description: Eine private Ereignisablaufverfolgungssitzung ist eine Ereignisablaufverfolgungssitzung im Benutzermodus, die im selben Prozess wie die Ereignisablaufverfolgungsanbieter&\# 8212 ausgeführt wird. Die private Sitzung und die aktivierten Anbieter müssen sich alle im selben Prozess befinden.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Konfigurieren und Starten einer privaten Protokollierungssitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf15db05c03e5a412cf07ee6e020d2321380f2d48abba465669dc807729fe38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901500"
---
# <a name="configuring-and-starting-a-private-logger-session"></a>Konfigurieren und Starten einer privaten Protokollierungssitzung

Eine private Ereignisablaufverfolgungssitzung ist eine Ereignisablaufverfolgungssitzung im Benutzermodus, die im selben Prozess wie die Ereignisablaufverfolgungsanbieter ausgeführt wird. Die private Sitzung und die aktivierten Anbieter müssen sich alle im selben Prozess befinden. Der Vorteil der Verwendung einer privaten Sitzung besteht darin, dass die private Sitzung nicht mit den maximal 64 Gleichzeitig ausgeführten Ereignisablaufverfolgungssitzungen gezählt wird.

Das Konfigurieren und Starten einer privaten Sitzung ähnelt dem Starten einer normalen Ereignisablaufverfolgungssitzung. Der Unterschied besteht darin, dass **der Wnode.Guid-Member** der [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) die **GUID** des Anbieters und nicht die Sitzung enthalten muss und der Anbieter die GUID bereits registriert haben muss. Beachten Sie Folgendes: Wenn Sie auch den \_ PROTOKOLLierungsmodus EVENT TRACE \_ PRIVATE IN \_ PROC \_ festlegen, können Sie eine andere **GUID** für die Sitzung und den Anbieter verwenden. Ausführliche Informationen zum Starten einer normalen Ereignisablaufverfolgungssitzung finden Sie unter [Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung.](configuring-and-starting-an-event-tracing-session.md)

Beachten Sie, dass Sie eine private Ablaufverfolgungssitzung nicht aus DllMain starten, beenden oder leeren können. Dies sollten Sie in den Initialisierungs- und Finalisierungsroutinen der DLL tun.

Von Windows 8.1 bis Windows 10 Version 1607 können Ereignisnutzlast-, Bereichs- und Stapellauffilter von der [**EnableTraceEx2-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) und den [**ENABLE TRACE \_ \_ PARAMETERS-**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) und [**EVENT FILTER \_ \_ DESCRIPTOR-Strukturen**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) verwendet werden, um nach bestimmten Bedingungen in einer Protokollierungssitzung zu filtern. Weitere Informationen zu Ereignisnutzlastfiltern finden Sie in den Funktionen [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)und [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) sowie in den Strukturen **ENABLE TRACE \_ \_ PARAMETERS,** **EVENT FILTER \_ \_ DESCRIPTOR** und [**PAYLOAD FILTER \_ \_ PREDICATE.**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Ab Windows 10 Version 1703 können Benutzer mit geringen Rechten jetzt eine private Protokollierungssitzung in prozessen starten, die sie gestartet haben. Der Anbieter muss vor dem Aktivieren oder Starten der privaten Sitzung nicht mehr registriert werden, was bedeutet, dass der Anbieter ähnlich wie nicht private Sitzungsanbieter "vorab aktiviert" ist. Es gibt einen Grenzwert von 8 systemweiten privaten Protokollierungen für einen einzelnen Prozess. Für eine höhere Leistung in prozessübergreifenden Szenarien wird empfohlen, beim Starten einer systemweiten privaten Protokollierung die Filterung für Sitzungs-APIs (einschließlich [**ControlTrace,**](/windows/win32/api/evntrace/nf-evntrace-controltracea) [**QueryTrace,**](/windows/win32/api/evntrace/nf-evntrace-querytrace) [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)und [**StopTrace)**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)zu verwenden. Beachten Sie, dass die gleichen Filter an alle Sitzungs-APIs übergeben werden sollten. Weitere Informationen zu Filtern finden Sie unter [**EVENT \_ TRACE PROPERTIES \_ \_ V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).

Ausführliche Informationen zum Starten einer Ereignisablaufverfolgungssitzung finden Sie unter [Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung.](configuring-and-starting-an-event-tracing-session.md)

Ausführliche Informationen zum Starten einer NT-Kernelprotokollierungssitzung finden Sie unter [Konfigurieren und Starten der NT-Kernelprotokollierungssitzung.](configuring-and-starting-the-nt-kernel-logger-session.md)

Ausführliche Informationen zum Starten einer globalen Protokollierungssitzung finden Sie unter [Konfigurieren und Starten einer globalen Protokollierungssitzung.](configuring-and-starting-the-global-logger-session.md)

Ausführliche Informationen zum Starten einer AutoLogger-Sitzung finden Sie unter [Konfigurieren und Starten einer AutoLogger-Sitzung.](configuring-and-starting-an-autologger-session.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren und Starten einer SystemTraceProvider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Konfigurieren und Starten einer AutoLogger-Sitzung](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Konfigurieren und Starten der NT-Kernelprotokollierungssitzung](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**AKTIVIEREN VON \_ ABLAUFVERFOLGUNGSPARAMETERN \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**\_ \_ EREIGNISABLAUFVERFOLGUNGSEIGENSCHAFTEN**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**\_EREIGNISABLAUFVERFOLGUNGSEIGENSCHAFTEN \_ \_ V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[**\_ \_ EREIGNISFILTERDESKRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**\_ \_ NUTZLASTFILTERPRÄDIKAT**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Aktualisieren einer Ereignisablaufverfolgungssitzung](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
