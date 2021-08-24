---
description: 'Dies ist eine Übersicht über die End-to-End-Journey eines Ereignisses für jede der vier von Microsoft entwickelten Ablaufverfolgungstechnologien: TraceLogging, Manifestbasiert, WPP und MOF.'
ms.assetid: 6102593C-C6D5-4BDB-A0EF-067AF91DE00B
title: Übersicht über Ereignismetadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931b8adbdb22cdbf2e0806e2d69c367e64ad92926390825a48a2fa51d50605ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755060"
---
# <a name="event-metadata-overview"></a>Übersicht über Ereignismetadaten

Dies ist eine Übersicht darüber, was für die End-to-End-Journey eines Ereignisses für jede der vier von Microsoft entwickelten Ablaufverfolgungstechnologien zu erwarten ist: [TraceLogging,](../tracelogging/trace-logging-about.md) [manifestbasiert,](writing-manifest-based-events.md) [WPP](windows-software-trace-preprocessor.md)und [MOF](tracing-events.md). Sie nähert sich dem Problem sowohl in Bezug auf die Nutzlast eines einzelnen Ereignisses als auch auf die zugehörigen Metadaten, die seine Struktur beschreiben, sodass das Ereignis später in sinnvolle Datenteile decodiert werden kann. Das Verständnis des Wegs der einzelnen Ereignisse ist wichtig, wenn Sie auswählen, welche Ablaufverfolgungstechnologie für ein Projekt geeignet ist. Es gibt keine lösungsorientierte Lösung für die Ablaufverfolgung.

## <a name="event-payloads"></a>Ereignisnutzlasten

Bei allen von Microsoft bereitgestellten Ablaufverfolgungstechnologien werden beim Aufrufen des Write-Befehls (z. B. [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) für manifestbasiertes oder [**TraceLoggingWrite**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) für TraceLogging) die daten, die zur Laufzeit für das Ereignis bereitgestellt werden, in ein zusammenhängendes binäres Blob, das als Ereignisnutzlast bezeichnet wird, aufgeteilt. Dies ist getrennt vom Ereignisschema oder den Ereignismetadaten (weiter unten erläutert), in dem das Layout dieses binären Blobs für Decodierungstools beschrieben wird. Wie genau die Generierung der Ereignisnutzlast erfolgt, hängt von der verwendeten Ablaufverfolgungstechnologie ab und letztendlich davon, ob das Ereignis klassisch [**(TraceEvent-Stil)**](/windows/win32/api/evntrace/nf-evntrace-traceevent) oder modern **(EventWrite-Stil)** ist.

Bei klassischen Ereignissen wird das Flag in [**EVENT \_ TRACE \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) an [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) übergeben, das bestimmt, wie dies geschieht:

\- Wenn **WNODE \_ FLAG USE MOF \_ \_ \_ PTR** angegeben ist, folgt ein Array von [**\_ MOF-FELDERN**](/windows/win32/api/evntrace/ns-evntrace-mof_field) dem [**\_ EREIGNISABLAUFVERFOLGUNGSHEADer \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) im Arbeitsspeicher. Die ETW-Runtime verkettet die Ereignisdaten wie in diesen Feldern angegeben, um die Ereignisnutzlast zu bilden.

\- Wenn **WNODE \_ FLAG USE MOF \_ \_ \_ PTR** nicht angegeben ist, wird die Ereignisnutzlast vom Benutzer direkt im Arbeitsspeicher nach dem [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)erstellt.

MOF und WPP sind klassische Anbieter. Die WPP-Implementierung übernimmt jedoch all dies für Sie.

Bei nicht klassischen Ereignissen wird eine Reihe von [**EVENT \_ \_ DATA-DESKRIPTOREN**](/windows/desktop/api/Evntprov/ns-evntprov-event_data_descriptor) an [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite)übergeben. Die ETW-Runtime verkettet die Ereignisdaten wie in diesen Deskriptoren angegeben, um die Ereignisnutzlast zu bilden.

Sowohl manifestbasierte als auch TraceLogging-Technologien sind im Allgemeinen moderne Anbieter. Wenn Sie manifestbasiert mc.exe Protokollierungscode für Sie generieren lassen (Um- oder Km-Switch), wird die Nutzlastgenerierung für Sie erledigt. Die Nutzlastgenerierung wird immer durch TraceLogging durchgeführt.

Das Endergebnis ist, dass eine Nutzlast für ein Ereignis zur Laufzeit generiert wird. Alle Nutzlasten sind grundsätzlich ähnlich, da sie binäre Blobs von Daten sind, die nur die Felddaten für dieses bestimmte Ereignis enthalten, unabhängig von der verwendeten Ablaufverfolgungstechnologie und den Feldtypen, die von dieser Ablaufverfolgungstechnologie unterstützt werden. Ohne die Ereignismetadaten ist die Ereignisnutzlast bedeutungslos und nicht lesbar.

Die AUFGABE der ETW-Runtime besteht dann darin, dieses Ereignisblob vom Anbieter an den Consumer zu übertragen, wo es den Metadaten neu zugeordnet wird und decodierbar wird. Die ETW-Runtime fügt einige zusätzliche Metadaten hinzu, die die Umstände der Nutzlast angeben, z. B. Zeitstempel, Thread-ID und Schlüsselwörter des Ereignisses. Diese Informationen sind relevant für die Weiterleitung des Ereignisses durch die Laufzeit und sind auch nützlich, um die Identität und den Kontext des Ereignisses zum Zeitpunkt der Decodierung zu verstehen. Sie wird schließlich als Teil der [**\_ EREIGNISABLAUFVERFOLGUNG**](/windows/win32/api/evntrace/ns-evntrace-event_trace) oder [**DES \_ EREIGNISDATENSATZES**](/windows/win32/api/evntcons/ns-evntcons-event_record) für den Consumer ausgegeben.

## <a name="event-metadata"></a>Ereignismetadaten

Die Journey für Ereignismetadaten unterscheidet sich je nachdem, welche Ablaufverfolgungstechnologie verwendet wird, und es ist einer der größten Überlegungen beim Vergleich der einzelnen Technologien.

### <a name="mof"></a>MOF

Ereignismetadaten werden vom Ersteller des Ereignisses in Form eines speziellen MOF-Schemas in einer MOF-Datei von Hand erstellt. Das erstellte Schema muss mit der Nutzlast übereinstimmen, die protokolliert wird, damit das Ereignis von Consumern ordnungsgemäß decodiert werden kann. Ereignisdecoder erfordern, dass die MOF-Datei mit [mofcomp.exe](../wmisdk/mofcomp.md)auf dem System registriert wird. Weitere Informationen zum Veröffentlichen von MOF-Schemas finden Sie unter [Veröffentlichen ihres Ereignisschemas für einen klassischen Anbieter.](publishing-your-event-schema-for-a-classic-provider.md)

### <a name="wpp"></a>Wpp

Ereignismetadaten werden automatisch generiert und in der PDB-Datei Ihrer Binärdatei gespeichert, indem während des Buildprozesses tracewpp.exe. Diese Metadaten können später in Form einer eigenständigen TMF-Datei mittels tracepdb.exe extrahiert werden. Ereignisdecoder erfordern in der Regel entweder die PDB- oder tmf-Datei. Weitere Informationen zu tracepdb.exe finden Sie unter [Übersicht über Tracepdb.](/windows-hardware/drivers/devtest/tracepdb-overview)Weitere Informationen zu tracewpp.exe finden Sie unter [TraceWPP-Aufgabe.](/windows-hardware/drivers/devtest/tracewpp-task)

### <a name="manifest-based"></a>Manifestbasiert

Ereignisdefinitionen werden in einer MAN-Datei erstellt. Ereignismanifeste werden über den Manifestcompiler ([mc.exe](../wes/message-compiler--mc-exe-.md)) ausgeführt und generieren die Header, die für die Quellkompilierung erforderlich sind, sowie mehrere binäre BIN-Ressourcendateien. Diese Ressourcendateien müssen dann als Ressourcen in eine Binärdatei kompiliert werden, und die resultierende Binärdatei muss auf dem System platziert werden, das Ereignisse von diesem manifestbasierten Anbieter decodieren möchte. Darüber hinaus muss das Manifest auf dem System mit [wevtutil.exe](../wes/windows-event-log-tools.md) installiert werden. Die Attribute **resourceFileName** und **messageFileName** im XML-Anbieterelement im installierten Ereignismanifest müssen den vollständigen absoluten Pfad zur Binärdatei, in der die Ressourcendateien platziert wurden, ordnungsgemäß identifizieren. Beachten Sie, dass diese Pfade zur Manifestinstallationszeit mithilfe der wevtutil.exe Switches /rf und /mf überschrieben werden können. Ein System, das diese Schritte nicht ordnungsgemäß und vollständig ausgeführt hat, kann keine Ereignisse von diesem Anbieter decodieren. Ereignisdecoder erfordern daher ein installiertes Manifest und die Binärdatei mit den zugeordneten Ressourcen, die an dem von Ressourcen- und Nachrichtendateipfaden angegebenen Speicherort installiert sind. Weitere Informationen zum Veröffentlichen manifestbasierter Schemas finden Sie unter [Veröffentlichen ihres Ereignisschemas für einen manifestbasierten Anbieter.](publishing-your-event-schema-for-a-manifest-base-provider.md)

### <a name="tracelogging"></a>TraceLogging

Alle TraceLogging-Ereignisse sind selbstbeschreibend. Die ereignismetadaten, die zum Decodieren des Ereignisses erforderlich sind, werden automatisch generiert und zusammen mit der Nutzlast in einem kompakten Binärformat übertragen. Ereignisdecoder benötigen nur das TraceLogging-Ereignis und ein Verständnis des TraceLogging-Metadatenformats.

## <a name="configuring-tdh-for-decoding"></a>Konfigurieren von TDH für die Decodierung

Es gibt viele Decodierungstools. Es wird jedoch empfohlen, nach Möglichkeit TDH zu verwenden, da alle Ablaufverfolgungstechnologien mit einer einheitlichen API decodiert werden. Je nach Typ der Ablaufverfolgung, die Sie decodieren möchten, erfordert TDH möglicherweise eine explizite Konfiguration.

### <a name="mof"></a>MOF

TDH verwendet MOF-Decodierungsdaten, die auf dem System mithilfe mofcomp.exe registriert sind. Weitere Informationen finden Sie unter [Veröffentlichen des Ereignisschemas für einen klassischen Anbieter.](publishing-your-event-schema-for-a-classic-provider.md)

### <a name="wpp"></a>Wpp

TDH muss entweder auf die PDB-Datei oder die zugeordnete TMF-Datei für den WPP-Anbieter gezeigt werden, den Sie decodieren möchten. Dies kann durch Aufrufen von [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)erfolgen. Andernfalls wird die Decodierungs-Engine auf die Umgebungsvariable TRACE \_ FORMAT \_ SEARCH PATH \_ zurückgreifen.

### <a name="manifest-based"></a>Manifestbasiert

TDH verwendet alle manifestbasierten Anbieter, die mit wevtutil.exe auf dem System registriert sind.

### <a name="tracelogging"></a>TraceLogging

Die neuesten Versionen von TDH erkennen und decodieren TraceLogging-Ereignisse automatisch ohne zusätzliche Schritte.

 

 
