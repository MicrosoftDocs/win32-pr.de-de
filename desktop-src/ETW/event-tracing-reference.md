---
description: Listet die Elemente auf, die mit der Ereignisablaufverfolgung verwendet werden.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Ereignisablaufverfolgungsreferenz
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 20aaf59de3419b4015f03b38db69839b6f258ccd561b1e918694396e875ae5a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083280"
---
# <a name="event-tracing-reference"></a>Ereignisablaufverfolgungsreferenz

Sie verwenden die folgenden Programmierelemente, um Anwendungen zu schreiben, die die Ereignisablaufverfolgung enthalten:

-   [Ereignisablaufverfolgungsenumerationen](/windows/desktop/api/_etw/#enumerations)
-   [Ereignisablaufverfolgungsfunktionen](/windows/desktop/api/_etw/#functions)
-   [Schnittstellen für die Ereignisablaufverfolgung](/windows/desktop/api/_etw/#interfaces)
-   [Ereignisablaufverfolgungsstrukturen](/windows/desktop/api/_etw/#structures)
-   [Ereignisablaufverfolgungskonstanten](event-tracing-constants.md)

Ausführliche Informationen zu Beispielen, die diese Programmierelemente verwenden, finden Sie unter [Beispiele für die Ereignisablaufverfolgung.](event-tracing-samples.md)

Dieser Abschnitt enthält auch Informationen zu:

-   [Tools,](event-tracing-tools.md) die ETW bereitstellt
-   [MOF-Klassendefinitionen](event-tracing-mof-classes.md) für Kernelereignisse
-   [MOF-Klassenqualifizierer,](event-tracing-mof-qualifiers.md) die beim Definieren ihrer Ereignisklassen verwendet werden

## <a name="process-etw-traces-in-net-code"></a>Verarbeiten von ETW-Ablaufverfolgungen in .NET-Code

Sie können auch die [.NET TraceProcessing-API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) verwenden, um ETW-Ablaufverfolgungen für Ihre Anwendungen und andere Softwarekomponenten zu analysieren. Diese API wird intern bei Microsoft verwendet, um ETW-Daten zu analysieren, die das Windows Engineering-System erzeugt haben, und sie wird auch verwendet, um mehrere Tabellen in [Windows Leistungsanalyse](/windows-hardware/test/wpt/windows-performance-analyzer)zu schalten. Diese API ist als NuGet-Paket verfügbar.

Weitere Informationen finden Sie in [diesem Artikel](/windows/apps/trace-processing/overview).
