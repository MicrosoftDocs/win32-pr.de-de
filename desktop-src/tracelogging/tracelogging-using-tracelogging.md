---
title: Verwenden von TraceLogging
description: Die folgenden Themen enthalten einen TraceLogging-Schnellstart für nativen und verwalteten Code mit Beispielen.
ms.assetid: CEC57517-7A0E-45AA-85F7-F358AE51EF4A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be48ff03e1efe37b2ed18314557514c81715ea7e36dacfda309f473522dac39a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966489"
---
# <a name="using-tracelogging"></a>Verwenden von TraceLogging

Die folgenden Themen enthalten einen TraceLogging-Schnellstart für nativen und verwalteten Code mit Beispielen.

## <a name="prerequisites"></a>Voraussetzungen

-   Windows 10 Das Software Development Kit (SDK) ist erforderlich, um einen Benutzermodusanbieter zu schreiben.
-   Windows Driver Kit (WDK) ist erforderlich, um einen Kernelmodusanbieter zu schreiben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TraceLogging C/C++-Schnellstart](tracelogging-native-quick-start.md)<br/>                             | Im folgenden Abschnitt werden die grundlegenden Schritte beschrieben, die zum Hinzufügen von TraceLogging zu nativem Benutzermoduscode erforderlich sind. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [TraceLogging Managed Schnellstart](tracelogging-managed-quick-start.md)<br/>                          | Im folgenden Abschnitt werden die grundlegenden Schritte beschrieben, die zum Hinzufügen von TraceLogging zu verwaltetem Code erforderlich sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Aufzeichnen und Anzeigen von TraceLogging-Ereignissen](tracelogging-record-and-display-tracelogging-events.md)<br/> | Zeichnen Sie TraceLogging-Ereignisse mit dem Windows Performance Recorder (WPR) auf, und zeigen Sie sie mit dem Windows Leistungsanalyse (WPA) an.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [C/C++-Beispiele für die Ablaufverfolgung](tracelogging-c-cpp-tracelogging-examples.md)<br/>                       | Dieses Thema enthält C/C++-Beispiele für die Ablaufverfolgung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [Beispiele für die .NET-Ablaufverfolgung](tracelogging-net-examples.md)<br/>                                       | Dieses Thema enthält ein Beispiel für die Ablaufverfolgung mit verwaltetem Code, das veranschaulicht, wie ein Ereignis nur protokolliert wird, wenn der Ausführlichkeitsgrad der Sitzung ausführlich ist, und wie strukturierte Ereignisdaten protokolliert werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [Beispiel für die Protokollierung der universellen Windows-Plattform](universal-windows-platform-logging-examples.md)<br/>     | In diesem Beispiel wird gezeigt, wie die Protokollierungs-APIs im Windows verwendet werden. Foundation.Diagnostics-Namespace, einschließlich LoggingChannel, LoggingActivity, LoggingSession und FileLoggingSession. Diese Klassen sind für die Diagnoseprotokollierung in einer Windows-App konzipiert. Diese APIs wurden in Windows 8.1 hinzugefügt. <br/> Die LoggingChannel- und LoggingActivity-APIs wurden in Windows 10 erweitert, um das Schreiben komplexer Ereignisse mithilfe der TraceLogging-Ereigniscodierung zu unterstützen.<br/> Das Beispiel für die Universal Windows Platform-Protokollierung kann von GitHub heruntergeladen [werden.](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/Logging)<br/> |



 

TraceLogging-Beispiele.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TraceLogging für Kernelmodustreiber und -komponenten](/windows-hardware/drivers/devtest/tracelogging-for-kernel-mode-drivers-and-components)
</dt> </dl>

 

