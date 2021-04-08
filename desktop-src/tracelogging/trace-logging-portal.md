---
title: TraceLogging
description: .
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975c2f70cc645cc04d6b1461e32bb3b899097d1c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103733648"
---
# <a name="tracelogging"></a>TraceLogging

## <a name="purpose"></a>Zweck

Tracelogging ist das neue Windows 10-Ereignis Ablauf Verfolgungs Framework für Benutzermodusanwendungen und Kernelmodustreiber. Tracelogging basiert auf der Ereignis Ablauf Verfolgung für Windows (ETW) und bietet eine vereinfachte Möglichkeit, Code zu instrumentieren.

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
<td><a href="trace-logging-about.md">Informationen zu tracelogging</a><br/></td>
<td>Tracelogging ist die neue Windows 10-Ereignis Ablauf Verfolgung für Benutzermodusanwendungen und Kernelmodustreiber. Tracelogging ist ein Format für die selbst beschreibende Ereignis Ablauf Verfolgung für Windows (ETW). Tracelogging basiert auf der Ereignis Ablauf Verfolgung für Windows (ETW) und bietet eine vereinfachte Möglichkeit, Code zu instrumentieren.<br/></td>
</tr>
<tr class="even">
<td><a href="tracelogging-using-tracelogging.md">Verwenden von tracelogging</a><br/></td>
<td>In den folgenden Themen finden Sie einen Schnellstart für einen tracelogging-Schnellstart für nativen und verwalteten Code mit Beispielen.<br/></td>
</tr>
<tr class="odd">
<td><a href="trace-logging-reference.md">Tracelogging-Referenz</a><br/></td>
<td>In den folgenden Themen finden Sie Informationen zur nativen tracelogging-API.<br/> Tracelogging basiert auf der Ereignis Ablauf Verfolgung für Windows (ETW) und bietet eine vereinfachte Möglichkeit, Code zu instrumentieren. Mithilfe von tracelogging können Sie strukturierte Daten mit Ereignissen einschließen, Ereignisse korrelieren und keine separate XML-Datei des Instrumentierungs Manifests benötigen.<br/> <span class="underline">Für WinRT-Entwickler</span><br/>
<ul>
<li><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>Loggingchannel</strong></a> wurde in Windows 10 erweitert, um die selbst Beschreibungs Ereignisse der Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw) zu protokollieren, ohne ein Manifest zu benötigen.</li>
<li><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>Loggingactivity</strong></a> wurde in Windows 10 erweitert, um Aktivitäts Start-und-Endmethoden bereitzustellen, die die Kontrolle über das Format und den Inhalt der Start-und Endereignisse ermöglichen. Darüber hinaus können Aktivitäten in eine andere Liste eingefügt werden.</li>
</ul>
<span class="underline">Für Entwickler von verwaltetem Code (Microsoft .NET Framework)</span><br/>
<ul>
<li>Die <a href="/dotnet/api/system.diagnostics.tracing.eventsource">eventSource</a> -Klasse, die mit früheren Versionen des-.NET Framework ausgeliefert wurde, unterstützt bereits das Schreiben von ETW-Ereignissen, ohne dass ein Manifest erforderlich ist. Entwickler mussten jedoch eventSource als Basisklasse verwenden und der abgeleiteten Klasse Attribute und Methoden hinzufügen, die automatisch in ein etw-Manifest umgewandelt wurden. Nun müssen Entwickler nicht mehr von eventSource ableiten und stattdessen eventSource direkt zum Protokollieren von selbst beschreibenden Ereignissen verwenden, für die kein Manifest erforderlich ist.</li>
</ul>
<span class="underline">Für C/C++-Entwickler</span><br/>
<ul>
<li>"Traceloggingprovider. h" ist die empfohlene API für C/C++-Entwickler im Benutzer-oder Kernel Modus. Diese API eignet sich nicht gut für die Verwendung in dynamischen (Skript gesteuerten) Szenarios wie JavaScript. Unter den folgenden Links wird die C/C++-API beschrieben.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a>Entwicklergruppe

Tracelogging ist für die Verwendung durch Entwicklermodus-Anwendungsentwickler und Kernel Modus-Treiber Entwickler konzipiert, die eine Ablauf Verfolgung zu Ihrem Code hinzufügen möchten.

