---
title: TraceLogging-Referenz
description: Die folgenden Themen enthalten Informationen zur nativen TraceLogging-API. TraceLogging baut auf der Ereignisablaufverfolgung für Windows (ETW) auf und bietet eine vereinfachte Möglichkeit zum Instrumentieren von Code.
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6563186411ace599f249220b9fd44b9ee4c682fdebd1391b4a3027a87c3482e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349990"
---
# <a name="tracelogging-reference"></a>TraceLogging-Referenz

Die folgenden Themen enthalten Informationen zur nativen TraceLogging-API.

TraceLogging baut auf der Ereignisablaufverfolgung für Windows (ETW) auf und bietet eine vereinfachte Möglichkeit zum Instrumentieren von Code. Mit TraceLogging können Sie strukturierte Daten mit Ereignissen einreihen, Ereignisse korrelieren und benötigen keine separate INSTRUMENTIERUNGsmanifest-XML-Datei.

<span class="underline">Für WinRT-Entwickler</span>

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) wurde in Windows 10 erweitert, um selbstbeschreibende Ereignisablaufverfolgung für Windows-Ereignisse (ETW) zu protokollieren, ohne dass ein Manifest benötigt wird.
-   [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) wurde in Windows 10 erweitert, um Aktivitätsstart- und -stop-Methoden zur Verfügung zu stellen, die die Kontrolle über das Format und den Inhalt der Start- und Stop-Ereignisse bieten. Darüber hinaus können Aktivitäten geschachtelt werden.

<span class="underline">Für Entwickler von verwaltetem Code (Microsoft .NET Framework)</span>

-   Die [EventSource-Klasse,](/dotnet/api/system.diagnostics.tracing.eventsource) die mit früheren Versionen des .NET Framework ausgeliefert wurde, unterstützt bereits das Schreiben von ETW-Ereignissen, ohne dass ein Manifest benötigt wird. Entwickler mussten jedoch EventSource als Basisklasse verwenden und der abgeleiteten Klasse Attribute und Methoden hinzufügen, die automatisch in ein ETW-Manifest eingegliedert wurden. Entwickler müssen jetzt nicht von EventSource ableiten und können eventSource stattdessen direkt verwenden, um selbstbeschreibende Ereignisse zu protokollieren, die kein Manifest erfordern.

<span class="underline">Für C/C++-Entwickler</span>

-   TraceLoggingProvider.h ist die empfohlene API für C/C++-Entwickler im Benutzer- oder Kernelmodus. Diese API eignet sich nicht gut für die Verwendung in dynamischen (skriptierten) Szenarien wie JavaScript. Unter den folgenden Links wird die C/C++-API beschrieben.

<!-- -->

-   [Klassen](trace-logging-classes.md)
-   [Funktionen](trace-logging-functions.md)
-   [Makros](trace-logging-macros.md)

Beachten Sie, dass sich der Wert von WINVER auf das Verhalten von TraceLoggingProvider.h auswirken wird.

-   Wenn WINVER nicht festgelegt ist, bevor <windows.h> eingestellt wird, wird winver von <windows.h> auf einen Standardwert festgelegt, der der SDK-Version entspricht.
-   Bei Verwendung von TraceLoggingProvider.h, bei der WINVER auf 0x0602 (Windows 8) oder höher festgelegt ist, wird das Programm nicht unter Windows Vista oder Windows 7 ausgeführt.
-   Bei Verwendung von TraceLoggingProvider.h, bei der WINVER auf 0x0600 (Windows Vista) oder 0x0601 (Windows 7) festgelegt ist, wird das Programm aus Kompatibilitäts- und Kompatibilitätseinstellungen konfiguriert und kann mit den angegebenen Versionen von Windows.

 

 