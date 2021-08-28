---
title: TraceLogging
description: TraceLogging
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20f14980646680e0f6a0418470416801240ca17
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473116"
---
# <a name="tracelogging"></a>TraceLogging

## <a name="purpose"></a>Zweck

TraceLogging ist das neue Windows 10 Framework für die Ereignisablaufverfolgung für Benutzermodusanwendungen und Kernelmodustreiber. TraceLogging baut auf der Ereignisablaufverfolgung für Windows (ETW) auf und bietet eine vereinfachte Möglichkeit zum Instrumentieren von Code.

## <a name="in-this-section"></a>In diesem Abschnitt




| Thema | BESCHREIBUNG | 
|-------|-------------|
| <a href="trace-logging-about.md">Informationen zu TraceLogging</a><br /> | TraceLogging ist die neue Windows 10 Ereignisablaufverfolgung für Benutzermodusanwendungen und Kernelmodustreiber. TraceLogging ist ein Format für die selbstbeschreibende Ereignisablaufverfolgung für Windows (ETW). TraceLogging baut auf der Ereignisablaufverfolgung für Windows (ETW) auf und bietet eine vereinfachte Möglichkeit zum Instrumentieren von Code.<br /> | 
| <a href="tracelogging-using-tracelogging.md">Verwenden von TraceLogging</a><br /> | Die folgenden Themen enthalten einen TraceLogging-Schnellstart für nativen und verwalteten Code mit Beispielen.<br /> | 
| <a href="trace-logging-reference.md">TraceLogging-Referenz</a><br /> | Die folgenden Themen enthalten Informationen zur nativen TraceLogging-API.<br /> TraceLogging baut auf der Ereignisablaufverfolgung für Windows (ETW) auf und bietet eine vereinfachte Möglichkeit zum Instrumentieren von Code. Mit TraceLogging können Sie strukturierte Daten mit Ereignissen einreihen, Ereignisse korrelieren und benötigen keine separate INSTRUMENTIERUNGsmanifest-XML-Datei.<br /><span class="underline">Für WinRT-Entwickler</span><br /><ul><li><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> wurde in Windows 10 erweitert, um selbstbeschreibende Ereignisablaufverfolgung für Windows-Ereignisse (ETW) zu protokollieren, ohne dass ein Manifest benötigt wird.</li><li><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> wurde in Windows 10 erweitert, um Aktivitätsstart- und -stop-Methoden zur Verfügung zu stellen, die die Kontrolle über das Format und den Inhalt der Start- und Stop-Ereignisse bieten. Darüber hinaus können Aktivitäten geschachtelt werden.</li></ul><span class="underline">Für Entwickler von verwaltetem Code (Microsoft .NET Framework)</span><br /><ul><li>Die <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource-Klasse,</a> die mit früheren Versionen der .NET Framework ausgeliefert wurde, unterstützt bereits das Schreiben von ETW-Ereignissen, ohne dass ein Manifest benötigt wird. Entwickler mussten jedoch EventSource als Basisklasse verwenden und der abgeleiteten Klasse Attribute und Methoden hinzufügen, die automatisch in ein ETW-Manifest eingegliedert wurden. Entwickler müssen jetzt nicht von EventSource ableiten und können eventSource stattdessen direkt verwenden, um selbstbeschreibende Ereignisse zu protokollieren, die kein Manifest erfordern.</li></ul><span class="underline">Für C/C++-Entwickler</span><br /><ul><li>TraceLoggingProvider.h ist die empfohlene API für C/C++-Entwickler im Benutzer- oder Kernelmodus. Diese API eignet sich nicht gut für die Verwendung in dynamischen (skriptierten) Szenarien wie JavaScript. Unter den folgenden Links wird die C/C++-API beschrieben.</li></ul> | 




 

## <a name="developer-audience"></a>Entwicklergruppe

TraceLogging ist für die Verwendung durch Anwendungsentwickler im Benutzermodus und Kernelmodustreiberentwickler konzipiert, die ihrem Code Ablaufverfolgung hinzufügen möchten.

