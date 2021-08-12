---
description: Threads und kritische Abschnitte
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Threads und kritische Abschnitte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d13473a917ae49e80ec658b0d6187fdfdff80c6e3a080a229aca7ccbbe536c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651403"
---
# <a name="threads-and-critical-sections"></a>Threads und kritische Abschnitte

In diesem Abschnitt wird das Threading in DirectShow-Filtern und die Schritte beschrieben, die Sie ausführen sollten, um Abstürze oder Deadlocks in einem benutzerdefinierten Filter zu vermeiden.

In den Beispielen in diesem Abschnitt wird pseudocode verwendet, um den Code zu veranschaulichen, den Sie schreiben müssen. Sie gehen davon aus, dass ein benutzerdefinierter Filter klassen verwendet, die wie folgt von den DirectShow-Basisklassen abgeleitet werden:

-   CMyInputPin: Abgeleitet von [**CBaseInputPin.**](cbaseinputpin.md)
-   CMyOutputPin: Abgeleitet von [**CBaseOutputPin**](cbaseoutputpin.md).
-   CMyFilter: Abgeleitet von [**CBaseFilter**](cbasefilter.md).
-   CMyInputAllocator: Die Zuweisung des Eingabepins, abgeleitet von [**CMemAllocator.**](cmemallocator.md) Nicht jeder Filter benötigt eine benutzerdefinierte Zuweisung. Für viele Filter ist die **CMemAllocator-Klasse** ausreichend.

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [Streaming- und Anwendungsthreads](the-streaming-and-application-threads.md)
-   [Wird angehalten](pausing.md)
-   [Empfangen und Übermitteln von Beispielen](receiving-and-delivering-samples.md)
-   [Bereitstellen des Endes von Stream](delivering-the-end-of-stream.md)
-   [Leeren von Daten](flushing-data.md)
-   [Wird beendet](stopping.md)
-   [Abrufen von Puffern](getting-buffers.md)
-   [Streamingthreads und filter Graph Manager](streaming-threads-and-the-filter-graph-manager.md)
-   [Zusammenfassung des Filterthreadings](summary-of-filter-threading.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Daten Flow für Filterentwickler](data-flow-for-filter-developers.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



