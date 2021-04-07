---
title: Windows-Ereignisse
description: Ereignisse werden in der Regel zur Problembehandlung von Anwendungen und Treibersoftware verwendet. Vor Windows Vista verwenden Sie entweder die Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw) oder die Ereignisprotokollierung zum Protokollieren von Ereignissen. In Windows Vista wurde ein neues Ereignis Modell eingeführt, das sowohl die Ereignis Ablauf Verfolgung für Windows (ETW) als auch die Windows-Ereignisprotokoll-API vereinheitlicht. Windows 10 führt tracelogging ein, das auf etw aufbaut und eine vereinfachte Methode zum Instrumentieren von Code für Native .net-und WinRT-Entwickler bietet.
ms.assetid: c10baa8d-50b9-4fda-89d0-d00b1d9f5404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3d22580c38e45d06f5362e99626642eebdfe20
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038939"
---
# <a name="windows-events"></a>Windows-Ereignisse

Ereignisse werden in der Regel zur Problembehandlung von Anwendungen und Treibersoftware verwendet.

-   Vor Windows Vista verwenden Sie entweder die Ereignis Ablauf [Verfolgung für Windows (Event Tracing for Windows](/windows/desktop/ETW/event-tracing-portal) , etw) oder die [Ereignisprotokollierung](/windows/desktop/EventLog/event-logging) zum Protokollieren von Ereignissen.
-   In Windows Vista wurde ein neues Ereignis Modell eingeführt, das sowohl die [Ereignis Ablauf Verfolgung für Windows](/windows/desktop/ETW/event-tracing-portal) (ETW) als auch die [Windows-Ereignisprotokoll](/windows/desktop/WES/windows-event-log) -API vereinheitlicht.
-   Windows 10 führt [tracelogging](/windows/desktop/tracelogging/trace-logging-portal) ein, das auf etw aufbaut und eine vereinfachte Methode zum Instrumentieren von Code für Native .net-und WinRT-Entwickler bietet.

Mit dem neuen [tracelogging](/windows/desktop/tracelogging/trace-logging-portal) -Modell können Sie strukturierte Daten mit Ereignissen einschließen, Ereignisse korrelieren und keine separate XML-Datei des Instrumentierungs Manifests benötigen.

Das Windows Vista-Modell verwendet ein XML-Manifest, um die Ereignisse zu definieren, die Sie veröffentlichen möchten. Ereignisse können in einem Kanal oder einer ETW-Sitzung veröffentlicht werden. Sie können die Ereignisse in den folgenden Typen von Kanälen veröffentlichen: admin, Operational, Analytic und Debug. Wenn Sie den Verleger nur mit etw aktivieren, müssen Sie keine Kanäle im Manifest angeben. Ausführliche Informationen zum Schreiben eines Manifests finden Sie unter [Schreiben eines Instrumentierungs Manifests](/windows/desktop/WES/writing-an-instrumentation-manifest). Informationen zu Kanälen finden Sie unter [Definieren von Kanälen](/windows/desktop/WES/defining-channels).

Verwenden Sie die ETW-API, um Ihren Ereignis Verleger zu registrieren und Ereignisse zu veröffentlichen. Weitere Informationen finden Sie unter [Bereitstellen von Ereignissen](/windows/desktop/ETW/providing-events) und [Entwickeln eines Anbieters](/windows/desktop/WES/developing-a-provider). Der Ereignis Herausgeber schreibt die Ereignisse automatisch in die Kanäle, die im Manifest angegeben sind, wenn Sie aktiviert sind.

Wenn Sie die Ereignisse steuern möchten, die von einem Ereignis Herausgeber auf einer präziseteren Ebene der Granularität veröffentlicht werden, verwenden Sie die ETW-API. Wenn das Manifest z. b. Schreib-und Lese Ereignisse definiert, können Sie nur die Schreib Ereignisse aktivieren. Ein Ereignis kann auch einen Ebenenwert angeben, z. b. "Warning" oder "Error", sodass Sie die Ereignisse, die auf die Fehler Ebene festgelegt werden, einschränken können. Weitere Informationen finden Sie unter [Steuern von Ereignis Ablauf Verfolgungs Sitzungen](/windows/desktop/ETW/controlling-event-tracing-sessions). Die Ereignisse werden in die Protokolldatei der Sitzung geschrieben.

Die Verwendung von Ereignissen umfasst das Abrufen der Ereignisse aus einem Ereignis Kanal, eine Ereignisprotokoll Datei (evtx-oder EVT-Dateien), eine Ablauf Verfolgungs Datei (ETL-Dateien) oder eine echt Zeit-ETW-Sitzung. Um Ereignisse aus einer etw-Ablauf Verfolgungs Datei oder in einer echt Zeit-ETW-Sitzung zu nutzen, verwenden Sie die Funktionen des Trace Data Helper (TDH) in etw, um die Ereignisse zu verarbeiten. Sie können TDH auch zum Lesen der Ereignis Metadaten verwenden. Weitere Informationen finden Sie unter Verwenden von [Ereignissen](/windows/desktop/ETW/consuming-events). Zum Verarbeiten von Ereignissen aus einem Ereignis Kanal oder einer Ereignisprotokoll Datei verwenden Sie die Windows-Ereignisprotokoll Funktionen, um Ereignisse abzufragen oder zu abonnieren. Weitere Informationen finden Sie unter [Abfragen von Ereignissen](/windows/desktop/WES/querying-for-events) oder [Abonnieren von Ereignissen](/windows/desktop/WES/subscribing-to-events).

Vor Windows Vista müssen Sie die Ereignis Ablauf [Verfolgung für Windows](/windows/desktop/ETW/event-tracing-portal) oder die [Ereignisprotokollierung](/windows/desktop/EventLog/event-logging) verwenden, um Ereignisse zu veröffentlichen und zu nutzen.

 

 