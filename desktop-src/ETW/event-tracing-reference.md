---
description: Listet die mit der Ereignis Ablauf Verfolgung verwendeten Elemente auf.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Referenz zur Ereignis Ablauf Verfolgung
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 7e0ee4576b9b9d64a5766c6ab096ea34abc2b176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980576"
---
# <a name="event-tracing-reference"></a>Referenz zur Ereignis Ablauf Verfolgung

Verwenden Sie die folgenden Programmier Elemente zum Schreiben von Anwendungen, die die Ereignis Ablauf Verfolgung einschließen:

-   [Ereignistracing-Enumerationen](/windows/desktop/api/_etw/#enumerations)
-   [Funktionen der Ereignis Ablauf Verfolgung](/windows/desktop/api/_etw/#functions)
-   [Ereignis Ablauf Verfolgungs Schnittstellen](/windows/desktop/api/_etw/#interfaces)
-   [Ereignisse der Ereignis Ablauf Verfolgung](/windows/desktop/api/_etw/#structures)
-   [Ereignis Ablauf Verfolgungs Konstanten](event-tracing-constants.md)

Ausführliche Informationen zu Beispielen, die diese Programmier Elemente verwenden, finden Sie unter Beispiele für die [Ereignis Ablauf Verfolgung](event-tracing-samples.md).

Dieser Abschnitt enthält auch Informationen zu:

-   Von etw bereitgestellte [Tools](event-tracing-tools.md)
-   [MOF-Klassendefinitionen](event-tracing-mof-classes.md) für Kernel Ereignisse
-   [MOF-Klassen Qualifizierer](event-tracing-mof-qualifiers.md) , die beim Definieren der Ereignis Klassen verwendet

## <a name="process-etw-traces-in-net-code"></a>Verarbeiten von etw-Ablauf Verfolgungen in .NET-Code

Sie können auch die [.net traceprocessing-API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) verwenden, um etw-Ablauf Verfolgungen für Ihre Anwendungen und andere Softwarekomponenten zu analysieren. Diese API wird intern bei Microsoft verwendet, um etw-Daten zu analysieren, die das Windows-Engineering-System erzeugt haben, und es wird auch verwendet, um mehrere Tabellen in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer)zu unterhalten. Diese API ist als nuget-Paket verfügbar.

[hier finden Sie weitere Informationen](/windows/apps/trace-processing/overview)
