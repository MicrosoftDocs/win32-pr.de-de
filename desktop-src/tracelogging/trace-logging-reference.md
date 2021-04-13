---
title: Tracelogging-Referenz
description: In den folgenden Themen finden Sie Informationen zur nativen tracelogging-API. Tracelogging basiert auf der Ereignis Ablauf Verfolgung für Windows (ETW) und bietet eine vereinfachte Möglichkeit, Code zu instrumentieren.
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d81874e7aeb1a0618716b00d225d215c382ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390939"
---
# <a name="tracelogging-reference"></a>Tracelogging-Referenz

In den folgenden Themen finden Sie Informationen zur nativen tracelogging-API.

Tracelogging basiert auf der Ereignis Ablauf Verfolgung für Windows (ETW) und bietet eine vereinfachte Möglichkeit, Code zu instrumentieren. Mithilfe von tracelogging können Sie strukturierte Daten mit Ereignissen einschließen, Ereignisse korrelieren und keine separate XML-Datei des Instrumentierungs Manifests benötigen.

<span class="underline">Für WinRT-Entwickler</span>

-   [**Loggingchannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) wurde in Windows 10 erweitert, um die selbst Beschreibungs Ereignisse der Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw) zu protokollieren, ohne ein Manifest zu benötigen.
-   [**Loggingactivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) wurde in Windows 10 erweitert, um Aktivitäts Start-und-Endmethoden bereitzustellen, die die Kontrolle über das Format und den Inhalt der Start-und Endereignisse ermöglichen. Darüber hinaus können Aktivitäten in eine andere Liste eingefügt werden.

<span class="underline">Für Entwickler von verwaltetem Code (Microsoft .NET Framework)</span>

-   Die [eventSource](/dotnet/api/system.diagnostics.tracing.eventsource) -Klasse, die mit früheren Versionen des-.NET Framework ausgeliefert wurde, unterstützt bereits das Schreiben von ETW-Ereignissen, ohne dass ein Manifest erforderlich ist. Entwickler mussten jedoch eventSource als Basisklasse verwenden und der abgeleiteten Klasse Attribute und Methoden hinzufügen, die automatisch in ein etw-Manifest umgewandelt wurden. Nun müssen Entwickler nicht mehr von eventSource ableiten und stattdessen eventSource direkt zum Protokollieren von selbst beschreibenden Ereignissen verwenden, für die kein Manifest erforderlich ist.

<span class="underline">Für C/C++-Entwickler</span>

-   "Traceloggingprovider. h" ist die empfohlene API für C/C++-Entwickler im Benutzer-oder Kernel Modus. Diese API eignet sich nicht gut für die Verwendung in dynamischen (Skript gesteuerten) Szenarios wie JavaScript. Unter den folgenden Links wird die C/C++-API beschrieben.

<!-- -->

-   [Klassen](trace-logging-classes.md)
-   [Funktionen](trace-logging-functions.md)
-   [Makros](trace-logging-macros.md)

Beachten Sie, dass sich der Wert von WINVER auf die Art und Weise von traceloggingprovider. h auswirkt.

-   Wenn winver nicht festgelegt ist, bevor <Windows. h-> eingeschlossen werden, legt <Windows. h-> den winver auf einen Standardwert fest, der der SDK-Version entspricht.
-   Wenn Sie "traceloggingprovider. h" verwenden und "winver" auf "0x0602 (Windows 8)" oder höher festgelegt ist, kann das Programm nicht unter Windows Vista oder Windows 7 ausgeführt werden.
-   Wenn Sie traceloggingprovider. h mit winver auf 0x0600 sein (Windows Vista) oder 0x0601 (Windows 7) festlegen, wird das Programm aus Kompatibilitätsgründen konfiguriert und funktioniert in den angegebenen Versionen von Windows.

 

 