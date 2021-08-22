---
title: Windows-Ereignisse
description: Ereignisse werden in der Regel für die Problembehandlung von Anwendungs- und Treibersoftware verwendet. Vor der Windows Vista würden Sie entweder die Ereignisablaufverfolgung für Windows (ETW) oder die Ereignisprotokollierung verwenden, um Ereignisse zu protokollieren. Windows Vista hat ein neues Ereignismodell eingeführt, das sowohl die Ereignisablaufverfolgung für Windows (ETW) als auch Windows Ereignisprotokoll-API vereinheitlicht hat. Windows 10 führt TraceLogging ein, das auf ETW aufbaut und eine vereinfachte Möglichkeit zum Instrumentieren von Code für native .NET- und WinRT-Entwickler bietet.
ms.assetid: c10baa8d-50b9-4fda-89d0-d00b1d9f5404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdf0ecc85f8eed49fd32c30904c73d45bba3436d806ba408fe3ec39afb3e3af9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388940"
---
# <a name="windows-events"></a>Windows-Ereignisse

Ereignisse werden in der Regel für die Problembehandlung von Anwendungs- und Treibersoftware verwendet.

-   Vor der Windows Vista würden Sie [](/windows/desktop/ETW/event-tracing-portal) entweder die Ereignisablaufverfolgung für Windows (ETW) oder die Ereignisprotokollierung verwenden, [um](/windows/desktop/EventLog/event-logging) Ereignisse zu protokollieren.
-   Windows Vista hat ein neues Ereignismodell eingeführt, das sowohl die Ereignisablaufverfolgung für [Windows](/windows/desktop/ETW/event-tracing-portal) (ETW) als auch Windows [Ereignisprotokoll-API vereinheitlicht](/windows/desktop/WES/windows-event-log) hat.
-   Windows 10 führt [TraceLogging](/windows/desktop/tracelogging/trace-logging-portal) ein, das auf ETW aufbaut und eine vereinfachte Möglichkeit zum Instrumentieren von Code für native .NET- und WinRT-Entwickler bietet.

Mit dem [neuen TraceLogging-Modell](/windows/desktop/tracelogging/trace-logging-portal) können Sie strukturierte Daten mit Ereignissen einreihen, Ereignisse korrelieren und benötigen keine separate INSTRUMENTIERUNGsmanifest-XML-Datei.

Das Windows Vista-Modell verwendet ein XML-Manifest, um die Ereignisse zu definieren, die Sie veröffentlichen möchten. Ereignisse können in einem Kanal oder einer ETW-Sitzung veröffentlicht werden. Sie können die Ereignisse in den folgenden Kanälen veröffentlichen: Admin, Operational, Analytics und Debug. Wenn Sie nur ETW verwenden, um den Herausgeber zu aktivieren, müssen Sie keine Kanäle in Ihrem Manifest angeben. Vollständige Details zum Schreiben eines Manifests finden Sie unter [Schreiben eines Instrumentierungsmanifests,](/windows/desktop/WES/writing-an-instrumentation-manifest)und Informationen zu Kanälen finden Sie unter [Definieren von Kanälen.](/windows/desktop/WES/defining-channels)

Um Ihren Ereignisherausgeber zu registrieren und Ereignisse zu veröffentlichen, verwenden Sie die ETW-API. Weitere Informationen finden Sie unter [Bereitstellen von Ereignissen](/windows/desktop/ETW/providing-events) und Entwickeln eines [Anbieters.](/windows/desktop/WES/developing-a-provider) Der Ereignisherausgeber schreibt die Ereignisse automatisch in die im Manifest angegebenen Kanäle, wenn sie aktiviert sind.

Wenn Sie die Ereignisse steuern möchten, die ein Ereignisherausgeber mit einer feineren Granularität veröffentlicht, verwenden Sie die ETW-API. Wenn das Manifest beispielsweise Sowohl Schreib- als auch Leseereignisse definiert, können Sie nur die Schreibereignisse aktivieren. Ein Ereignis kann auch einen Ebenewert wie Warnung oder Fehler angeben, sodass Sie die geschriebenen Ereignisse auf die Ereignisse beschränken können, die die Fehlerebene angeben. Weitere Informationen finden Sie unter [Steuern von Ereignisablaufverfolgungssitzungen.](/windows/desktop/ETW/controlling-event-tracing-sessions) Die Ereignisse werden in die Protokolldatei der Sitzung geschrieben.

Das Nutzen von Ereignissen umfasst das Abrufen der Ereignisse aus einem Ereigniskanal, einer Ereignisprotokolldatei (EVTX- oder EVT-Dateien), einer Ablaufverfolgungsdatei (ETL-Dateien) oder einer ETW-Echtzeitsitzung. Um Ereignisse aus einer ETW-Ablaufverfolgungsdatei oder einer ETW-Echtzeitsitzung zu nutzen, verwenden Sie die TDH-Funktionen (Trace Data Helper) in ETW, um die Ereignisse zu nutzen. Sie können auch TDH verwenden, um die Ereignismetadaten zu lesen. Weitere Informationen finden Sie unter [Verwenden von Ereignissen.](/windows/desktop/ETW/consuming-events) Um Ereignisse aus einem Ereigniskanal oder einer Ereignisprotokolldatei zu nutzen, verwenden Sie die Windows-Ereignisprotokollfunktionen zum Abfragen oder Abonnieren von Ereignissen. Weitere Informationen finden Sie unter [Abfragen von Ereignissen](/windows/desktop/WES/querying-for-events) oder Abonnieren von [Ereignissen.](/windows/desktop/WES/subscribing-to-events)

Vor der Windows Vista müssen Sie [](/windows/desktop/ETW/event-tracing-portal) die Ereignisablaufverfolgung für Windows oder die [Ereignisprotokollierung](/windows/desktop/EventLog/event-logging) verwenden, um Ereignisse zu veröffentlichen und zu nutzen.

 

 