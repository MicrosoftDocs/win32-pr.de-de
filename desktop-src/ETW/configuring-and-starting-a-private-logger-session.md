---
description: Eine private Ereignis Ablauf Verfolgungs Sitzung ist eine Ereignis Ablauf Verfolgungs Sitzung im Benutzermodus, die in demselben Prozess ausgeführt wird wie die Ereignis Ablauf Verfolgungs Anbieter&\# 8212; die private Sitzung und die Anbieter, die Sie aktivieren, müssen sich alle im selben Prozess befinden.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Konfigurieren und Starten einer Sitzung für private Logger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ef13728bfb3516197ab153cf90b301d5930ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485278"
---
# <a name="configuring-and-starting-a-private-logger-session"></a>Konfigurieren und Starten einer Sitzung für private Logger

Eine private Ereignis Ablauf Verfolgungs Sitzung ist eine Ereignis Ablauf Verfolgungs Sitzung im Benutzermodus, die im selben Prozess wie die Ereignis Ablauf Verfolgungs Anbieter ausgeführt wird – die private Sitzung und die Anbieter, die Sie aktivieren, müssen sich alle im selben Prozess befinden. Der Vorteil der Verwendung einer privaten Sitzung besteht darin, dass die private Sitzung nicht die maximale Anzahl der gleichzeitig ausgeführten Ereignis Ablauf Verfolgungs Sitzungen in 64 anzählt.

Das Konfigurieren und Starten einer privaten Sitzung ähnelt dem Starten einer normalen Ereignis Ablauf Verfolgungs Sitzung. Der Unterschied besteht darin, dass der **wnode. GUID** -Member der Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) die **GUID** des Anbieters und nicht die Sitzung enthalten muss und der Anbieter die GUID bereits registriert haben muss. Beachten Sie, dass \_ \_ \_ \_ Sie eine andere **GUID** für die Sitzung und den Anbieter verwenden können, wenn Sie auch die private Ereignis Ablauf Verfolgung im proc-Protokollierungs Modus festlegen. Ausführliche Informationen zum Starten einer normalen Ereignis Ablauf Verfolgungs Sitzung finden Sie unter [Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md).

Beachten Sie, dass es nicht möglich ist, eine private Ablauf Verfolgungs Sitzung von DllMain zu starten, zu verhindern oder zu leeren. Dies sollten Sie in den Initialisierungs-und finalisierungsroutinen der dll tun.

Von Windows 8.1 bis Windows 10, Version 1607, Ereignis Nutzlast, Bereich und Stapel Durchlauf Filter können von der [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) -Funktion und der [**enable \_ Trace \_ Parameters**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) -und [**Ereignis \_ Filter \_ Deskriptor**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) -Strukturen verwendet werden, um nach bestimmten Bedingungen in einer Protokollierungs Sitzung zu filtern. Weitere Informationen zu Ereignis Nutz Last Filtern finden Sie unter den Funktionen " [**tdhkreatepayloadfilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)" und " [**tdhaggregatepayloadfilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) " und " **enable \_ Trace \_ Parameters**", **Ereignis \_ Filter \_ Deskriptor** und [**Payload \_ Filter \_ Predicate**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) Structures.

Ab Windows 10, Version 1703, können Benutzer mit geringen Rechten jetzt in Prozessen, die Sie gestartet haben, eine private Protokollierungs Sitzung starten. Der Anbieter muss nicht mehr registriert werden, bevor die private Sitzung aktiviert oder gestartet wird. Dies bedeutet, dass der Anbieter wie nicht private Sitzungs Anbieter "voraktiviert" ist. Es gibt eine Beschränkung auf 8 systemweite private Protokollierungen für einen einzelnen Prozess. Zur Steigerung der Leistung in prozessübergreifenden Szenarios empfiehlt es sich, beim Starten einer systemweiten privaten Protokollierung das Filtern für Sitzungs-APIs (einschließlich " [**controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)", " [**querytrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace)", " [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)" und " [**stoptrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)") zu verwenden. Beachten Sie, dass dieselben Filter an alle Sitzungs-APIs übermittelt werden sollten. Weitere Informationen zu Filtern finden Sie unter [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften \_ v2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).

Weitere Informationen zum Starten einer Ereignis Ablauf Verfolgungs Sitzung finden Sie unter [Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md).

Weitere Informationen zum Starten einer NT-Kernel Protokollierungs Sitzung finden Sie unter [Konfigurieren und Starten der NT Kernel Logger-Sitzung](configuring-and-starting-the-nt-kernel-logger-session.md).

Weitere Informationen zum Starten einer globalen Protokollierungs Sitzung finden Sie unter [Konfigurieren und Starten einer globalen](configuring-and-starting-the-global-logger-session.md)Protokollierungs Sitzung.

Weitere Informationen zum Starten einer autologger-Sitzung finden Sie unter [Konfigurieren und Starten einer autologger-Sitzung](configuring-and-starting-an-autologger-session.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren und Starten einer systemtraceprovider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Konfigurieren und Starten einer autologger-Sitzung](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Konfigurieren und Starten der NT Kernel Logger-Sitzung](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**Aktivieren von Ablauf \_ Verfolgungs \_ Parametern**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**Eigenschaften der Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**Eigenschaften der Ereignis Ablauf \_ Verfolgung \_ \_ v2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[**Ereignis \_ Filter \_ Deskriptor**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**Nutz Last \_ Filter- \_ Prädikat**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**Tdhaggregatepayloadfilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**Tdhkreatepayloadfilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Aktualisieren einer Ereignis Ablauf Verfolgungs Sitzung](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
