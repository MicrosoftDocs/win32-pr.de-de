---
title: Informationen zu tracelogging
description: Tracelogging ist die neue Windows 10-Ereignis Ablauf Verfolgung für Benutzermodusanwendungen und Kernelmodustreiber.
ms.assetid: 8C6A9E91-98F9-4D6B-A937-A22BA7CEB1E4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c2b1ca72385a51df1e0cd82f3e91c198f15b5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858314"
---
# <a name="about-tracelogging"></a>Informationen zu tracelogging

Tracelogging ist die neue Windows 10-Ereignis Ablauf Verfolgung für Benutzermodusanwendungen und Kernelmodustreiber. Tracelogging ist ein Format für die selbst beschreibende Ereignis Ablauf Verfolgung für Windows (ETW). Tracelogging basiert auf der Ereignis Ablauf Verfolgung für Windows (ETW) und bietet eine vereinfachte Möglichkeit, Code zu instrumentieren.

Tracelogging bietet die Einfachheit des Windows-Software-Trace-präprozessorcodes (WPP) mit dem zusätzlichen Vorteil, dass es möglich ist, strukturierte Daten mit Ereignissen, der Funktion der korrelierenden Ereignisse und ohne eine separate XML-Datei des Instrumentierungs Manifests einzubeziehen. Ereignisse sind selbst beschreibend. Dies bedeutet, dass eine Binärdatei, die das Instrumentations Manifest enthält, nicht auf dem System registriert werden muss, um die TDH-APIs (Trace Data Helper) zum Decodieren und Anzeigen von Ereignissen zu verwenden.

Die Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw) wurde mit Windows 2000 eingeführt und in Windows Vista aktualisiert. Tracelogging baut auf den Windows Vista-ETW-APIs auf. Anbieter können die tracelogging-Technologie verwenden und weiterhin unter Windows Vista arbeiten. Vorhandene Controller (mit Windows vistaapis) können verwendet werden, um tracelogging-Anbieter zu steuern.

Tracelogging ist auch mit vorhandenen Tools kompatibel. Anbieter, die Manifest-basiertes etw verwenden, werden weiterhin unterstützt. Sie müssen keine manifestressourcenbasierten ETW-Anbieter in tracelogging-Anbieter konvertieren, es sei denn, Sie möchten die Einfachheit, die tracelogging bietet, nutzen. Die WPP-Ablauf Verfolgung wird auch weiterhin unterstützt.

Tracelogging basiert auf etw, führt jedoch einige wichtige Verbesserungen durch:

-   Die Ablauf Verfolgung eines Ereignisses ist so einfach wie ein API-Aufrufe.
-   Ereignisse sind selbst beschreibend und erfordern keine zusätzlichen Binärdateien, die das kompilierte Ereignis Manifest enthalten, um das Ereignis zu interpretieren. Alle Metadaten über das Ereignis werden im Ereignis aufgezeichnet.
-   Aktivitäten innerhalb eines einzelnen Prozesses können problemlos durch Start-und Endereignisse ausgedrückt werden.
-   Tracelogging ist mit vorhandener Instrumentations Unterstützung kompatibel. Die neuen ETW-APIs unterstützen weiterhin die alten Anbieter. Sie können in die neuen ETW-APIs für strategische Szenarien investieren und ihre alten Instrumentations Punkte unverändert lassen.
-   Tracelogging bietet dieselbe API für die Ereignis Ablauf Verfolgung für Windows 10, Xbox One und Windows 10 Mobile.
-   Die tracelogging-APIs sind über C, C++, .net und Windows-Runtime zugänglich.

## <a name="api-high-level-overview"></a>Allgemeine API-Übersicht

Es gibt drei separate tracelogging-APIs, die unterschiedliche Entwickler Zielgruppen als Ziel haben. Jede API ist so konzipiert, dass Sie unterschiedliche Sätze von Anforderungen erfüllt, die für die Zielgruppe dieser API geeignet sind.

Für WinRT-Entwickler:

-   [**Loggingchannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) wurde in Windows 10 erweitert, um die selbst Beschreibungs Ereignisse der Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw) zu protokollieren, ohne ein Manifest zu benötigen.
-   [**Loggingactivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) wurde in Windows 10 erweitert, um Aktivitäts Start-und-Endmethoden bereitzustellen, die die Kontrolle über das Format und den Inhalt der Start-und Endereignisse ermöglichen. Darüber hinaus können Aktivitäten in eine andere Liste eingefügt werden.

Für C/C++-Entwickler:

-   Traceloggingprovider. h enthält die effizienteste API. diese API eignet sich jedoch nicht gut für die Verwendung in dynamischen (Skript gesteuerten) Szenarios wie JavaScript. Diese API kann im Benutzermodus und im Kernel Modus-Code verwendet werden.

Für Entwickler von verwaltetem Code (Microsoft .NET Framework):

-   Die [eventSource](/dotnet/api/system.diagnostics.tracing.eventsource) -Klasse, die mit früheren Versionen des-.NET Framework ausgeliefert wurde, hat bereits das Schreiben von ETW-Ereignissen unterstützt: Automatisches Erstellen des Manifests und Einbetten des Manifests in den Ereignisdaten Strom. Der Entwickler musste jedoch weiterhin das Manifest nachverfolgen, um die Ereignisse zu decodieren (es sei denn, Sie arbeiten in einem Szenario, in dem das eingebettete Manifest unterstützt wurde). Tracelogging ermöglicht das vollständige eliminieren des Manifests.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Ereignis Ablauf Verfolgung](/windows/desktop/ETW/about-event-tracing)
</dt> </dl>

 

 