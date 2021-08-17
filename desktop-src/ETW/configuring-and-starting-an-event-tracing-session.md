---
description: Verwenden Sie zum Konfigurieren einer Ereignisablaufverfolgungssitzung die EVENT \_ TRACE \_ PROPERTIES-Struktur, um die Eigenschaften der Sitzung anzugeben.
ms.assetid: 8a6aa39c-ec81-42ac-a26e-29f1f6960220
title: Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1650e503b8c54108d58f6e7cebda546eb9d9e32d8ef014da0c27e5d062af4567
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963160"
---
# <a name="configuring-and-starting-an-event-tracing-session"></a>Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung

Verwenden Sie zum Konfigurieren einer Ereignisablaufverfolgungssitzung die [**EVENT \_ TRACE \_ PROPERTIES-Struktur,**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) um die Eigenschaften der Sitzung anzugeben. Der Arbeitsspeicher, den Sie für die **EVENT \_ TRACE \_ PROPERTIES-Struktur** zuordnen, muss groß genug sein, um auch die Sitzungs- und Protokolldateinamen enthalten zu können, die der Struktur im Arbeitsspeicher folgen.

Nachdem Sie die Eigenschaften der Sitzung angegeben haben, rufen Sie die [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) auf, um die Sitzung zu starten. Wenn die Funktion erfolgreich ist, enthält der *SessionHandle-Parameter* das Sitzungshandle, und die **LoggerNameOffset-Eigenschaft** enthält den Offset zum Namen der Sitzung.

Um die Anbieter zu aktivieren, die Ereignisse in Ihrer Sitzung protokollieren möchten, rufen Sie die [**EnableTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) auf, um klassische Anbieter zu aktivieren, und die [**EnableTraceEx-Funktion,**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) um [manifestbasierte](about-event-tracing.md) Anbieter zu aktivieren. Rufen Sie die [**EnableTraceEx2-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) auf, um Anbieter zu aktivieren, die Ereignisse in Ihrer Sitzung nach bestimmten Bedingungen für Windows 8.1,Windows Server 2012 R2 und höher filtern möchten.

Darüber hinaus können Sie zusätzliche Informationen zu einem Ereignis mit einem Aufruf der [**TraceSetInformation-Funktion**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) nachverfolgen. **TraceSetInformation** gibt zusätzliche Ablaufverfolgungsinformationen in den erweiterten Datenabschnitt eines Ereignisses ein und kann Informationen wie die Informationen zur Ablaufverfolgungsversion oder die derzeit im System registrierten Anbieter enthalten. Weitere Informationen finden Sie unter [Abrufen zusätzlicher Ereignisablaufverfolgungsdaten.](retrieving-additional-event-tracing-data.md)

Bis zu acht Ablaufverfolgungssitzungen können Ereignisse vom gleichen [manifestbasierten Anbieter aktivieren und](about-event-tracing.md) empfangen. Allerdings kann nur eine Ablaufverfolgungssitzung einen [klassischen Anbieter](about-event-tracing.md) aktivieren. Wenn mehrere Ablaufverfolgungssitzung versuchen, einen klassischen Anbieter zu aktivieren, empfängt die erste Sitzung keine Ereignisse mehr, wenn die zweite Sitzung den Anbieter aktiviert. Wenn z. B. Sitzung A Anbieter 1 und dann Sitzung B Anbieter 1 aktiviert hat, würde nur Sitzung B Ereignisse von Anbieter 1 empfangen.

Sie können eine der drei Funktionen verwenden, um einen Anbieter zu aktivieren. Sie verlieren jedoch möglicherweise die Funktionalität, wenn Sie [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) zum Aktivieren eines manifestbasierten Anbieters verwenden, da Sie keinen MatchAllKeyword-Wert angeben, erweiterte Datenelemente angeben können, die in das Ereignis enthalten sein sollen, oder anbieterdefinierte Filterdaten bereitstellen können. Weitere Informationen finden Sie im Abschnitt "Hinweise" jeder Funktion.

In Windows 8.1,Windows Server 2012 R2 und höher können Ereignisnutzlast-, Bereichs- und Stapelfilter von der [**EnableTraceEx2-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) und den [**ENABLE TRACE \_ \_ PARAMETERS-**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) und [**EVENT \_ \_ FILTER-DESCRIPTOR-Strukturen**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) verwendet werden, um nach bestimmten Bedingungen in einer Protokollierungssitzung zu filtern. Weitere Informationen zu Ereignisnutzlastfiltern finden Sie in den Funktionen [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)und [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) sowie in den **STRUKTUREN ENABLE TRACE \_ \_ PARAMETERS,** **EVENT FILTER \_ \_ DESCRIPTOR** und [**PAYLOAD FILTER \_ \_ PREDICATE.**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Verwenden Sie einen der folgenden Befehle, um die Ebene und die Schlüsselwörter zu bestimmen, die zum Aktivieren eines manifestbasierten Anbieters verwendet werden:

-    **Logman-Abfrageanbietername** 
-   **Wevtutil** **gp** *provider-name*

Die Befehle listen nur die Ebene und Schlüsselwörter auf. Der Anbieter muss alle Filterdatenanforderungen für potenzielle Controller dokumentieren.

Um die manifestbasierten Anbieter aufzählen zu können, verwenden **Sie Wevtutil** **ep.**

Bei klassischen Anbietern liegt es in der Hand des Anbieters, die von ihm unterstützten Schweregrade zu dokumentieren und potenziellen Controllern zur Verfügung zu stellen. Wenn der Anbieter von einem Controller aktiviert werden möchte, sollte der Anbieter 0 für den Schweregrad akzeptieren und Flags aktivieren und 0 als Anforderung zum Ausführen der Standardprotokollierung interpretieren (was auch immer der Fall ist).

Sie können den Anbieter aktivieren, bevor oder nachdem der Anbieter sich selbst registriert hat. Nach der Aktivierung des Anbieters wird die Rückruffunktion des Anbieters von ETW aufrufen. Wenn der Anbieter nicht registriert ist, wird die Rückruffunktion des Anbieters von ETW nach der Registrierung selbst aufrufen.

Sie können auch die [**EnableTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) verwenden, um den Anbieter zu deaktivieren (die Protokollierung von Ereignissen in Ihrer Sitzung zu beenden), oder um den Protokollierstand zu aktualisieren oder Flags des Anbieters zu aktivieren. Mit der [**EnableTraceEx-Funktion**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) können Sie den Anbieter deaktivieren oder die Ebene, Schlüsselwörter, erweiterten Daten und Filterdaten aktualisieren. Jedes Mal, wenn Sie die **EnableTrace-** oder **EnableTraceEx-Funktion** aufrufen, ruft ETW die Rückruffunktion des Anbieters auf. Der Anbieter bleibt für die Sitzung aktiviert, bis die Sitzung den Anbieter deaktiviert.

Um die Ablaufverfolgungssitzung nach dem Sammeln von Ereignissen zu beenden, rufen Sie die [**ControlTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-controltracea) auf, und übergeben Sie EVENT \_ TRACE CONTROL STOP als \_ \_ Steuerungscode. Um die zu beendende Sitzung anzugeben, können Sie das Ereignisablaufverfolgungs-Sitzungshand handle, das aus einem früheren Aufruf der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) ermittelt wurde, oder den Namen einer zuvor gestarteten Sitzung übergeben. Achten Sie darauf, dass Sie alle Anbieter deaktivieren, bevor Sie die Sitzung beenden. Wenn Sie die Sitzung beenden, bevor Sie zuerst den Anbieter deaktivieren, deaktiviert ETW den Anbieter und versucht, die Rückruffunktion des Anbieters auf aufruft. Wenn die Anwendung, die die Sitzung gestartet hat, beendet wird, ohne den Anbieter zu deaktivieren oder die **ControlTrace-Funktion** auf aufruft, bleibt der Anbieter aktiviert.

Wenn [**ControlTrace erfolgreich**](/windows/win32/api/evntrace/nf-evntrace-controltracea) ist, werden die Sitzungseigenschaften aktualisiert, um die endgültigen Eigenschaftswerte und Ausführungsstatistiken für die Ereignisablaufverfolgungssitzung widerzuleiten.

Ein Beispiel zum Starten einer Ereignisablaufverfolgungssitzung finden Sie im folgenden Artikel:

-   [Beispiel:](example-that-creates-a-session-and-enables-a-manifest-based-provider.md) Erstellt eine Sitzung und aktiviert einen manifestbasierten Anbieter – startet eine Ablaufverfolgungssitzung, aktiviert einen manifestbasierten Anbieter, deaktiviert den Anbieter und beendet dann die Sitzung.

Weitere Informationen zum Starten einer Ablaufverfolgungssitzung finden Sie in einer der folgenden Themen:

-   [Konfigurieren und Starten einer SystemTraceProvider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Konfigurieren und Starten der NT-Kernelprotokollierungssitzung](configuring-and-starting-the-nt-kernel-logger-session.md)
-   [Konfigurieren und Starten einer AutoLogger-Sitzung](configuring-and-starting-an-autologger-session.md)
-   [Konfigurieren und Starten der globalen Protokollierungssitzung](configuring-and-starting-the-global-logger-session.md)
-   [Konfigurieren und Starten einer privaten Protokollierungssitzung](configuring-and-starting-a-private-logger-session.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren und Starten einer privaten Protokollierungssitzung](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer SystemTraceProvider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Konfigurieren und Starten einer AutoLogger-Sitzung](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Konfigurieren und Starten der NT-Kernelprotokollierungssitzung](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)
</dt> <dt>

[**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace)
</dt> <dt>

[**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**AKTIVIEREN VON \_ ABLAUFVERFOLGUNGSPARAMETERN \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**\_ \_ EREIGNISFILTERDESKRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**EIGENSCHAFTEN \_ DER \_ EREIGNISVERFOLGUNG**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**\_ \_ NUTZLASTFILTER-PRÄDIKAT**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Aktualisieren einer Ereignisablaufverfolgungssitzung](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
