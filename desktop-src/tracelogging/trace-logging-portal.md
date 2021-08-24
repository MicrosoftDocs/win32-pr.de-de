---
title: TraceLogging
description: TraceLogging
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1263f040707a1e0ea7578b35165c581f6847b5263af42dff76808a7518e5fcae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119818510"
---
# <a name="tracelogging"></a>TraceLogging

## <a name="purpose"></a>Zweck

TraceLogging ist das neue Windows 10 Ereignisablaufverfolgungsframework für Benutzermodusanwendungen und Kernelmodustreiber. TraceLogging baut auf der Ereignisablaufverfolgung für Windows (ETW) auf und bietet eine vereinfachte Möglichkeit zum Instrumentieren von Code.

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="trace-logging-about.md">Informationen zu TraceLogging</a><br/></td>
<td>TraceLogging ist die neue Windows 10 Ereignisablaufverfolgung für Benutzermodusanwendungen und Kernelmodustreiber. TraceLogging ist ein Format für die selbstbeschreibende Ereignisablaufverfolgung für Windows (ETW). TraceLogging baut auf der Ereignisablaufverfolgung für Windows (ETW) auf und bietet eine vereinfachte Möglichkeit zum Instrumentieren von Code.<br/></td>
</tr>
<tr class="even">
<td><a href="tracelogging-using-tracelogging.md">Verwenden von TraceLogging</a><br/></td>
<td>Die folgenden Themen enthalten einen TraceLogging-Schnellstart für nativen und verwalteten Code mit Beispielen.<br/></td>
</tr>
<tr class="odd">
<td><a href="trace-logging-reference.md">TraceLogging-Referenz</a><br/></td>
<td>Die folgenden Themen enthalten Informationen zur nativen TraceLogging-API.<br/> TraceLogging baut auf der Ereignisablaufverfolgung für Windows (ETW) auf und bietet eine vereinfachte Möglichkeit zum Instrumentieren von Code. TraceLogging ermöglicht es Ihnen, strukturierte Daten mit Ereignissen einzuschließen, Ereignisse zu korrelieren, und erfordert keine separate INSTRUMENTIERUNGsmanifest-XML-Datei.<br/> <span class="underline">Für WinRT-Entwickler</span><br/>
<ul>
<li><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> wurde in Windows 10 erweitert, um selbstbeschreibende Ereignisse der Ereignisablaufverfolgung für Windows (ETW) zu protokollieren, ohne dass ein Manifest erforderlich ist.</li>
<li><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> wurde in Windows 10 erweitert, um Methoden zum Starten und Beenden von Aktivitäten bereitzustellen, die die Kontrolle über das Format und den Inhalt der Start- und Stop-Ereignisse ermöglichen. Darüber hinaus können Aktivitäten geschachtelt werden.</li>
</ul>
<span class="underline">Für Entwickler mit verwaltetem Code (Microsoft .NET Framework)</span><br/>
<ul>
<li>Die <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource-Klasse,</a> die mit früheren Versionen des .NET Framework geliefert wurde, unterstützt bereits das Schreiben von ETW-Ereignissen ohne Manifest. Entwickler mussten EventSource jedoch als Basisklasse verwenden und der abgeleiteten Klasse Attribute und Methoden hinzufügen, die automatisch in ein ETW-Manifest umgewandelt wurden. Entwickler müssen jetzt nicht von EventSource ableiten und können stattdessen EventSource direkt verwenden, um selbstbeschreibende Ereignisse zu protokollieren, die kein Manifest erfordern.</li>
</ul>
<span class="underline">Für C/C++-Entwickler</span><br/>
<ul>
<li>TraceLoggingProvider.h ist die empfohlene API für C/C++-Entwickler im Benutzer- oder Kernelmodus. Diese API eignet sich nicht gut für die Verwendung in dynamischen (skriptgesteuerten) Szenarien wie JavaScript. Unter den folgenden Links wird die C/C++-API beschrieben.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a>Entwicklergruppe

TraceLogging ist für die Verwendung durch Anwendungsentwickler im Benutzermodus und Entwickler von Kernelmodustreibern konzipiert, die ihrem Code die Ablaufverfolgung hinzufügen möchten.

