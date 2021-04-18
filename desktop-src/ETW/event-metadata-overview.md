---
description: 'Dies ist ein Überblick darüber, was für die End-to-End-Entwicklung eines Ereignisses für jede der vier von Microsoft bereitgestellten Ablaufverfolgungs Technologien zu erwarten ist: tracelogging, Manifest-based, WPP und MOF.'
ms.assetid: 6102593C-C6D5-4BDB-A0EF-067AF91DE00B
title: Übersicht über Ereignis Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c16853ef2639fd560f5b5da30447556119ec877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484363"
---
# <a name="event-metadata-overview"></a>Übersicht über Ereignis Metadaten

Dies ist ein Überblick darüber, was für die End-to-End-Entwicklung eines Ereignisses für jede der vier von Microsoft bereitgestellten Ablaufverfolgungs Technologien zu erwarten ist: [tracelogging](../tracelogging/trace-logging-about.md), [Manifest-based](writing-manifest-based-events.md), [WPP](windows-software-trace-preprocessor.md)und [MOF](tracing-events.md). Das Problem wird in Bezug auf die Nutzlast eines einzelnen Ereignisses und die zugehörigen Metadaten behandelt, die die Struktur beschreiben, sodass das Ereignis später in sinnvolle Datenelemente decodiert werden kann. Das Verständnis der Journey der einzelnen Ereignis Ereignisse ist wichtig, wenn Sie auswählen, welche Ablauf Verfolgungs Technologie für ein Projekt geeignet ist. Es gibt keine vollständig geeignete Lösung für die Ablauf Verfolgung.

## <a name="event-payloads"></a>Ereignis Nutzlasten

Für alle von Microsoft bereitgestellten Ablauf Verfolgungs Technologien werden beim Aufrufen des Schreib Befehls (z. b. [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) für manifestressor [**traceloggingwrite**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) für tracelogging) die Daten, die für das Ereignis zur Laufzeit bereitgestellt werden, in ein zusammenhängendes binäres Blob gefaltet, das als Ereignis Nutzlast bezeichnet wird. Dies ist unabhängig vom Ereignis Schema oder den Ereignis Metadaten (siehe unten), in dem das Layout dieses binären BLOBs für decoderingtools beschrieben wird. Wie genau die Generierung der Ereignis Nutzlast passiert, hängt von der verwendeten Ablauf Verfolgungs Technologie ab und davon, ob es sich um ein klassisches Ereignis ([**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) Style) oder einen modernen (**EventWrite** -Stil) handelt.

Bei klassischen Ereignissen wird das Flag im [**Ereignis Ablauf \_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) an [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) übermittelt, das bestimmt, wie dies geschieht:

\- Wenn das **wnode- \_ Flag \_ \_ MOF \_ ptr verwendet** , wird ein Array von [**MOF- \_ Feldern**](/windows/win32/api/evntrace/ns-evntrace-mof_field) auf den [**Ereignis Ablauf \_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) im Arbeitsspeicher folgt. Die ETW-Laufzeit verkettet die Ereignisdaten, die in diesen Feldern angegeben werden, um die Ereignis Nutzlast zu bilden.

\- Wenn das **wnode- \_ Flag \_ \_ MOF \_ ptr verwenden** nicht angegeben ist, wird die Ereignis Nutzlast vom Benutzer direkt im Arbeitsspeicher erstellt, und zwar nach dem [**Ereignis Ablauf \_ Verfolgungs \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).

MOF und WPP sind klassische Anbieter. Allerdings übernimmt die WPP-Implementierung all dies für Sie.

Bei nichtklassischen Ereignissen werden eine Reihe von [**Ereignis \_ Daten \_ Deskriptoren**](/windows/desktop/api/Evntprov/ns-evntprov-event_data_descriptor) an [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite)übermittelt. Die ETW-Laufzeit verkettet die Ereignisdaten, die in diesen Deskriptoren angegeben sind, um die Ereignis Nutzlast zu bilden.

Manifest-basierte und tracelogging-Technologien sind im allgemeinen moderne Anbieter. Wenn Sie mit Manifest-basiert mc.exe Protokollierungs Code für Sie (um-oder km-Schalter) generieren lassen, wird die Nutz Last Generierung für Sie erledigt. Die Nutz Last Generierung wird von tracelogging immer berücksichtigt.

Das Endergebnis ist, dass zur Laufzeit eine Nutzlast für ein Ereignis generiert wird. Alle Nutzlasten sind grundsätzlich ähnlich, da es sich um binäre blobdaten handelt, die nur die Felddaten für das jeweilige Ereignis enthalten, unabhängig von der verwendeten Ablauf Verfolgungs Technologie und den Feldtypen, die von dieser Ablauf Verfolgungs Technologie unterstützt werden. Ohne die Ereignis Metadaten ist die Ereignis Nutzlast bedeutungslos und nicht intellibar.

Die Aufgabe der etw-Laufzeit besteht dann darin, dieses ereignisblob vom Anbieter an den Consumer zu übertragen, wo Sie mit den Metadaten erneut verknüpft werden und decodierbar wird. Die ETW-Laufzeit fügt einige zusätzliche Metadaten hinzu, die die Umstände der Nutzlast angeben, z. b. den Zeitstempel, die Thread-ID und die Schlüsselwörter des Ereignisses. Diese Informationen sind für die Art und Weise relevant, wie das Ereignis durch die Laufzeit weitergeleitet wurde, und es ist auch nützlich, um die Identität und den Kontext des Ereignisses beim Decodieren zu verstehen. Sie wird schließlich als Teil der [**Ereignis Ablauf \_ Verfolgung**](/windows/win32/api/evntrace/ns-evntrace-event_trace) oder des [**Ereignis \_ Datensatzes**](/windows/win32/api/evntcons/ns-evntcons-event_record) für den Consumer festgestellt.

## <a name="event-metadata"></a>Ereignis Metadaten

Die Journey für Ereignis Metadaten unterscheidet sich je nachdem, welche Ablauf Verfolgungs Technologie verwendet wird. Dies ist eine der größten Überlegungen beim Vergleich der einzelnen Technologien.

### <a name="mof"></a>MOF

Ereignis Metadaten werden von Hand vom Ersteller des Ereignisses in Form eines speziellen MOF-Schemas in einer MOF-Datei verfasst. Das erstellte Schema muss mit der Nutzlast übereinstimmen, die protokolliert wird, damit das-Ereignis von Consumern ordnungsgemäß decodiert wird. Bei ereignisdecodern muss die MOF-Datei auf dem System mit [mofcomp.exe](../wmisdk/mofcomp.md)registriert werden. Weitere Informationen zum Veröffentlichen von MOF-Schemas finden [Sie unter Veröffentlichen Ihres Ereignis Schemas für einen klassischen Anbieter](publishing-your-event-schema-for-a-classic-provider.md).

### <a name="wpp"></a>WPP

Ereignis Metadaten werden automatisch generiert und in der PDB-Datei der Binärdatei gespeichert, indem tracewpp.exe während des Buildprozesses. Diese Metadaten können später in Form einer eigenständigen TMF-Datei mit tracepdb.exe extrahiert werden. Ereignis Decoder benötigen in der Regel entweder die PDB-oder die TMF-Datei. Weitere Informationen zu tracepdb.exe finden Sie unter [Übersicht über tracepdb](/windows-hardware/drivers/devtest/tracepdb-overview). Weitere Informationen zu tracewpp.exe finden Sie unter [tracewpp-Aufgabe](/windows-hardware/drivers/devtest/tracewpp-task).

### <a name="manifest-based"></a>Manifest-basiert

Ereignis Definitionen werden in einer. man-Datei erstellt. Ereignis Manifeste werden über den manifestressourcencompiler ([mc.exe](../wes/message-compiler--mc-exe-.md)) ausgeführt, der die für die Quell Kompilierung benötigten Header sowie mehrere binäre binärressourcendateien erzeugt. Diese Ressourcen Dateien müssen dann als Ressourcen in eine Binärdatei kompiliert werden, und die resultierende Binärdatei wird auf dem System abgelegt, das Ereignisse von diesem Manifest-basierten Anbieter decodieren soll. Darüber hinaus muss das Manifest auf dem System installiert werden, [wevtutil.exe](../wes/windows-event-log-tools.md) am wichtigsten ist, dass die Attribute **resourceFileName** und **messagefilename** des XML-Anbieters des Anbieters im installierten Ereignis Manifest den vollständigen absoluten Pfad zu der Binärdatei, in der die Ressourcen Dateien platziert wurden, ordnungsgemäß identifizieren müssen. Beachten Sie, dass diese Pfade bei der Installationszeit des Manifests überschrieben werden können, indem die wevtutil.exe Switches/RF und/MF. Ein System, das diese Schritte nicht ordnungsgemäß und vollständig ausgeführt hat, kann Ereignisse von diesem Anbieter nicht decodieren. Ereignis Decoder benötigen daher ein installiertes Manifest, und die Binärdatei mit den zugeordneten Ressourcen ist an dem Speicherort installiert, der durch die Ressourcen-und Nachrichtendatei Pfade angegeben wird. Weitere Informationen zum Veröffentlichen von Manifest-basierten Schemas finden [Sie unter Veröffentlichen des Ereignis Schemas für einen Manifest-basierten Anbieter](publishing-your-event-schema-for-a-manifest-base-provider.md).

### <a name="tracelogging"></a>TraceLogging

Alle tracelogging-Ereignisse sind selbst beschreibend. Die Ereignis Metadaten, die zum Decodieren des Ereignisses erforderlich sind, werden automatisch generiert und zusammen mit der Nutzlast in einem kompakten Binärformat übertragen. Ereignis Decoder benötigen nur das tracelogging-Ereignis und ein Verständnis des tracelogging-metadatenformats.

## <a name="configuring-tdh-for-decoding"></a>Konfigurieren von TDH für das Decodieren

Es sind viele Decodierungs Tools vorhanden. Es wird jedoch empfohlen, nach Möglichkeit TDH zu verwenden, da alle Ablauf Verfolgungs Technologien mit einer einheitlichen API decodiert werden. Abhängig vom Typ der Ablauf Verfolgung, die Sie decodieren möchten, ist für TDH möglicherweise eine explizite Konfiguration erforderlich.

### <a name="mof"></a>MOF

TDH verwendet MOF-Decodierung von Daten, die auf dem System mit mofcomp.exe registriert sind. Weitere Informationen finden Sie unter [Veröffentlichen Ihres Ereignis Schemas für einen klassischen Anbieter](publishing-your-event-schema-for-a-classic-provider.md).

### <a name="wpp"></a>WPP

TDH muss sowohl auf die PDB-Datei als auch auf die zugeordnete TMF-Datei für den WPP-Anbieter, den Sie decodieren möchten, verweisen. Dies kann durch Aufrufen von [**tdhsetdecodingparameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)durchgeführt werden. Andernfalls wird die Decodierungs-Engine auf den Suchpfad für die Umgebungsvariable-Ablauf Verfolgungs Datei zurückgreifen \_ \_ \_ .

### <a name="manifest-based"></a>Manifest-basiert

TDH nutzt alle manifestanbietern, die auf dem System registriert sind, mithilfe von wevtutil.exe.

### <a name="tracelogging"></a>TraceLogging

Die neuesten Versionen von TDH erkennen und decodieren automatisch tracelogging-Ereignisse ohne weitere Schritte.

 

 
