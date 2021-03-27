---
description: Verwenden Sie zum Konfigurieren einer Ereignis Ablauf Verfolgungs Sitzung die Struktur der Ereignis Ablauf Verfolgungs \_ \_ Eigenschaften, um die Eigenschaften der Sitzung anzugeben.
ms.assetid: 8a6aa39c-ec81-42ac-a26e-29f1f6960220
title: Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f86ec57975e8f12ede17e5e2cda962c010aa1af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980952"
---
# <a name="configuring-and-starting-an-event-tracing-session"></a>Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung

Verwenden Sie zum Konfigurieren einer Ereignis Ablauf Verfolgungs Sitzung die Struktur der Ereignis Ablauf Verfolgungs [**\_ \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) , um die Eigenschaften der Sitzung anzugeben. Der Arbeitsspeicher, den Sie **der \_ \_ Eigenschaften** Struktur der Ereignis Ablauf Verfolgung zuordnen, muss groß genug sein, um auch die Sitzungs-und Protokoll Dateinamen zu enthalten, die der Struktur im Arbeitsspeicher folgen

Nachdem Sie die Eigenschaften der Sitzung angegeben haben, müssen Sie die [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion aufrufen, um die Sitzung zu starten. Wenn die Funktion erfolgreich ausgeführt wird, enthält der *SessionHandle* -Parameter das Sitzungs handle, und die **loggernameoffset** -Eigenschaft enthält den Offset für den Namen der Sitzung.

Um die Anbieter zu aktivieren, für die Sie Ereignisse in der Sitzung protokollieren möchten, müssen Sie die Funktion [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) aufrufen, um klassische Anbieter und die Funktion [**enabletraceex**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) zum Aktivieren von [Manifest-basierten](about-event-tracing.md) Anbietern zu aktivieren. Um Anbietern zu ermöglichen, die Ereignisse an ihrer Sitzung protokollieren möchten, Filtern Sie nach bestimmten Bedingungen auf Windows 8.1, Windows Server 2012 R2 und höher, um die [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) -Funktion aufzurufen.

Darüber hinaus können Sie auch zusätzliche Informationen zu einem Ereignis mithilfe eines Aufrufes der [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) -Funktion verfolgen. **Tracesetinformation** fügt zusätzliche Ablauf Verfolgungs Informationen in den erweiterten Daten Abschnitt eines Ereignisses ein und kann Informationen wie z. b. die Informationen zur Ablauf Verfolgungs Version oder die derzeit auf dem System registrierten Anbieter enthalten. Weitere Informationen finden Sie unter [Abrufen zusätzlicher Ereignis Ablauf Verfolgungs Daten](retrieving-additional-event-tracing-data.md).

Bis zu acht Ablauf Verfolgungs Sitzungen können Ereignisse desselben [Manifest-basierten](about-event-tracing.md) Anbieters aktivieren und empfangen. Es kann jedoch nur eine Ablauf Verfolgungs Sitzung einen [klassischen](about-event-tracing.md) Anbieter aktivieren. Wenn mehr als eine Ablauf Verfolgungs Sitzung versucht, einen klassischen Anbieter zu aktivieren, würde die erste Sitzung keine Ereignisse mehr empfangen, wenn die zweite Sitzung den Anbieter aktiviert. Wenn z. B. Session a Provider 1 und dann Session b Provider 1 aktiviert hat, empfängt nur Sitzung b Ereignisse von Anbieter 1.

Sie können eine der drei Funktionen verwenden, um einen Anbieter zu aktivieren. Sie können jedoch auch die Funktionalität verlieren, wenn Sie mithilfe von [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) einen Manifest-basierten Anbieter aktivieren, da Sie keinen matchallkeyword-Wert bereitstellen können, erweiterte Datenelemente angeben, die in das Ereignis eingeschlossen werden sollen, oder Anbieter definierte Filterdaten bereitstellen. Weitere Informationen finden Sie im Abschnitt "Hinweise" der einzelnen Funktionen.

Unter Windows 8.1 können Windows Server 2012 R2 und höhere Ereignis Nutz Last-, Bereichs-und Stapel Durchlauf Filter von der [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) -Funktion und den [**\_ \_ Deskriptor**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) -Strukturen zum Aktivieren von Ablauf [**\_ Verfolgungs \_ Parametern**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) und Ereignis Filtern verwendet werden, um nach bestimmten Bedingungen in einer Protokollierungs Sitzung zu filtern. Weitere Informationen zu Ereignis Nutz Last Filtern finden Sie unter den Funktionen " [**tdhkreatepayloadfilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)" und " [**tdhaggregatepayloadfilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) " und " **enable \_ Trace \_ Parameters**", **Ereignis \_ Filter \_ Deskriptor** und [**Payload \_ Filter \_ Predicate**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) Structures.

Verwenden Sie einen der folgenden Befehle, um die Ebene und die Schlüsselwörter zu ermitteln, die zum Aktivieren eines Manifest-basierten Anbieters verwendet werden:

-   **Logman** **Query** *Provider-Name*
-   **Wevtutil** - **GP** *-Anbieter-Name*

Die Befehle Listen nur die Ebene und die Schlüsselwörter auf. der Anbieter muss alle Filterdaten Anforderungen für potenzielle Controller dokumentieren.

Verwenden Sie zum Auflisten der Manifest-basierten Anbieter **wevtutil** **EP**.

Bei klassischen Anbietern ist es dem Anbieter zu ermöglichen, potenzielle Controller zu dokumentieren und für potenzielle Controller die Schweregrade oder aktivierbare Flags verfügbar zu machen. Wenn der Anbieter von einem beliebigen Controller aktiviert werden soll, sollte der Anbieter 0 für den Schweregrad akzeptieren und Flags aktivieren und 0 als Anforderung zum Durchführen der Standard Protokollierung interpretieren (was möglich ist).

Sie können den Anbieter aktivieren, bevor oder nachdem sich der Anbieter selbst registriert hat. Nachdem der Anbieter aktiviert wurde, ruft etw dann die Rückruffunktion des Anbieters auf. Wenn der Anbieter nicht registriert ist, ruft etw die Rückruffunktion des Anbieters auf, nachdem er sich selbst registriert hat.

Sie können auch die [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) -Funktion verwenden, um den Anbieter zu deaktivieren (die Protokollierung der Ereignisse in Ihrer Sitzung zu verhindern) oder um den Protokolliergrad zu aktualisieren oder Flags des Anbieters zu aktivieren. Mit der Funktion [**enabletraceex**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) können Sie den Anbieter deaktivieren oder die Ebene, die Schlüsselwörter, die erweiterten Daten und die Filterdaten aktualisieren. Jedes Mal, wenn Sie die Funktion **EnableTrace** oder **enabletraceex** aufrufen, ruft etw die Rückruffunktion des Anbieters auf. Der Anbieter bleibt für die Sitzung aktiviert, bis die Sitzung den Anbieter deaktiviert.

Um die Ablauf Verfolgungs Sitzung nach dem Erfassen von Ereignissen zu unterbinden, können Sie die [**controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) -Funktion aufzurufen und das Ablauf Verfolgungs Steuerelement für Ereignisse \_ \_ \_ als Steuerungs Code Wenn Sie die Sitzung angeben möchten, die beendet werden soll, können Sie das Sitzungs Handle der Ereignis Ablauf Verfolgung übergeben, das von einem früheren Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion abgerufen wurde, oder den Namen einer zuvor gestarteten Sitzung. Stellen Sie sicher, dass Sie alle Anbieter deaktivieren, bevor Sie die Sitzung beenden. Wenn Sie die Sitzung vor der erstmaligen Deaktivierung des Anbieters abbrechen, wird der Anbieter von etw deaktiviert, und es wird versucht, die Rückruffunktion des Anbieters aufzurufen. Wenn die Anwendung, die die Sitzung gestartet hat, beendet wird, ohne den Anbieter zu deaktivieren oder die **controltrace** -Funktion Aufrufs, bleibt der Anbieter aktiviert.

Wenn [**controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) erfolgreich ist, werden die Sitzungs Eigenschaften aktualisiert, um die endgültigen Eigenschaftswerte und die Ausführungs Statistik für die Ereignis Ablauf Verfolgungs Sitzung widerzuspiegeln.

Ein Beispiel, das eine Ereignis Ablauf Verfolgungs Sitzung startet, finden Sie hier:

-   [Beispiel für das Erstellen einer Sitzung und das Aktivieren eines Manifest-basierten Anbieters](example-that-creates-a-session-and-enables-a-manifest-based-provider.md) : startet eine Ablauf Verfolgungs Sitzung, aktiviert einen Manifest-basierten Anbieter, deaktiviert den Anbieter und beendet dann die Sitzung.

Weitere Informationen zum Starten einer Ablauf Verfolgungs Sitzung finden Sie in einer der folgenden Informationen:

-   [Konfigurieren und Starten einer systemtraceprovider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Konfigurieren und Starten der NT Kernel Logger-Sitzung](configuring-and-starting-the-nt-kernel-logger-session.md)
-   [Konfigurieren und Starten einer autologger-Sitzung](configuring-and-starting-an-autologger-session.md)
-   [Konfigurieren und Starten der globalen Protokollierungs Sitzung](configuring-and-starting-the-global-logger-session.md)
-   [Konfigurieren und Starten einer Sitzung für private Logger](configuring-and-starting-a-private-logger-session.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren und Starten einer Sitzung für private Logger](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer systemtraceprovider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Konfigurieren und Starten einer autologger-Sitzung](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Konfigurieren und Starten der NT Kernel Logger-Sitzung](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**Controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)
</dt> <dt>

[**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace)
</dt> <dt>

[**Enabletraceex**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**Aktivieren von Ablauf \_ Verfolgungs \_ Parametern**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**Ereignis \_ Filter \_ Deskriptor**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**Eigenschaften der Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**Nutz Last \_ Filter- \_ Prädikat**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**Starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)
</dt> <dt>

[**Tdhaggregatepayloadfilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**Tdhkreatepayloadfilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Aktualisieren einer Ereignis Ablauf Verfolgungs Sitzung](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
