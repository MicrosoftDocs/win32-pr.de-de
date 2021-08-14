---
title: Informationen zu TraceLogging
description: TraceLogging ist die neue Windows 10 Ereignisablaufverfolgung für Benutzermodusanwendungen und Kernelmodustreiber.
ms.assetid: 8C6A9E91-98F9-4D6B-A937-A22BA7CEB1E4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cc38210bf4c3ed1ed0b1ebf56ca22a0597b9288fc30ae4c0231d5317465644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218391"
---
# <a name="about-tracelogging"></a>Informationen zu TraceLogging

TraceLogging ist die neue Windows 10 Ereignisablaufverfolgung für Benutzermodusanwendungen und Kernelmodustreiber. TraceLogging ist ein Format für die selbstbeschreibende Ereignisablaufverfolgung für Windows (ETW). TraceLogging baut auf der Ereignisablaufverfolgung für Windows (ETW) auf und bietet eine vereinfachte Möglichkeit zum Instrumentieren von Code.

TraceLogging bietet die Einfachheit des Windows-Software-Ablaufverfolgungs-Präprozessors (Software Trace Preprocessor, WPP) mit dem zusätzlichen Vorteil, dass strukturierte Daten mit Ereignissen, der Funktion zum Korrelieren von Ereignissen und ohne separate Instrumentierungsmanifest-XML-Datei aufgenommen werden können. Ereignisse sind selbstbeschreibend, was bedeutet, dass eine Binärdatei, die das Instrumentierungsmanifest enthält, nicht auf dem System registriert werden muss, um die TDH-APIs (Trace Data Helper) zum Decodieren und Anzeigen von Ereignissen zu verwenden.

Die Ereignisablaufverfolgung für Windows (ETW) wurde mit Windows 2000 eingeführt und in Windows Vista aktualisiert. Die Ablaufverfolgung baut auf den Windows Vista-ETW-APIs auf. Anbieter können die TraceLogging-Technologie verwenden und weiterhin auf Windows Vista arbeiten. Vorhandene Controller (mit Windows VistaAPIs) können verwendet werden, um TraceLogging-Anbieter zu steuern.

TraceLogging ist auch mit vorhandenen Tools kompatibel. Anbieter, die manifestbasierte ETW verwenden, werden weiterhin unterstützt. Sie müssen manifestbasierte ETW-Anbieter nur dann in TraceLogging-Anbieter konvertieren, wenn Sie die Einfachheit von TraceLogging nutzen möchten. Die WPP-Ablaufverfolgung wird ebenfalls weiterhin unterstützt.

TraceLogging baut auf ETW auf, führt aber einige wichtige Verbesserungen ein:

-   Die Ablaufverfolgung eines Ereignisses ist so einfach wie ein API-Aufruf.
-   Ereignisse sind selbstbeschreibend und erfordern keine zusätzlichen Binärdateien, die das kompilierte Ereignismanifest enthalten, um das Ereignis zu interpretieren. Alle Metadaten zum Ereignis werden im Ereignis aufgezeichnet.
-   Aktivitäten innerhalb eines einzelnen Prozesses können einfach durch Start- und Stoppereignisse ausgedrückt werden.
-   TraceLogging ist mit der vorhandenen Instrumentierungsunterstützung kompatibel. Die neuen ETW-APIs unterstützen weiterhin die alten Anbieter. Sie können in die neuen ETW-APIs für strategische Szenarien investieren, während Sie Ihre alten Instrumentierungspunkte erhalten.
-   TraceLogging bietet die gleiche Ereignisablaufverfolgungs-API für Windows 10, Xbox One und Windows 10 Mobile.
-   TraceLogging-APIs sind über C, C++, .NET und Windows Runtime zugänglich.

## <a name="api-high-level-overview"></a>Übersicht über die API auf hoher Ebene

Es gibt drei separate TraceLogging-APIs, die für verschiedene Entwicklerzielgruppe gelten. Jede API wurde so konzipiert, dass sie unterschiedliche Anforderungen erfüllt, die für die Zielgruppe dieser API geeignet sind.

Für WinRT-Entwickler:

-   [**LoggingChannel wurde**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) in Windows 10 erweitert, um selbstbeschreibende Ereignisablaufverfolgung für Windows-Ereignisse (ETW) zu protokollieren, ohne dass ein Manifest benötigt wird.
-   [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) wurde in Windows 10 erweitert, um Methoden zum Starten und Beenden von Aktivitäten zu bieten, die die Kontrolle über das Format und den Inhalt der Start- und Stop-Ereignisse bieten. Darüber hinaus können Aktivitäten geschachtelt werden.

Für C/C++-Entwickler:

-   TraceLoggingProvider.h enthält die effizienteste API, aber diese API eignet sich nicht gut für die Verwendung in dynamischen (skriptierten) Szenarien wie JavaScript. Diese API kann im Benutzermodus- und Kernelmoduscode verwendet werden.

Für Entwickler von verwaltetem Code (Microsoft .NET Framework):

-   Die [EventSource-Klasse,](/dotnet/api/system.diagnostics.tracing.eventsource) die mit früheren Versionen des .NET Framework ausgeliefert wurde, hat bereits das Schreiben von ETW-Ereignissen unterstützt. Das Manifest wird automatisch generiert und in den Ereignisstream eingebettet. Der Entwickler musste das Manifest jedoch weiterhin nachverfolgen, um die Ereignisse zu decodieren (es sei denn, er arbeitet in einem Szenario, in dem das eingebettete Manifest unterstützt wurde). TraceLogging ermöglicht es, das Manifest vollständig zu entfernen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Ereignisablaufverfolgung](/windows/desktop/ETW/about-event-tracing)
</dt> </dl>

 

 