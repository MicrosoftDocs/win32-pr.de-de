---
description: Threads und kritische Abschnitte
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Threads und kritische Abschnitte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576cb28e7e382db92328adf09980a825e71b5a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350338"
---
# <a name="threads-and-critical-sections"></a>Threads und kritische Abschnitte

In diesem Abschnitt wird das Threading in DirectShow-Filtern und die Schritte beschrieben, die Sie durchführen sollten, um Abstürze oder Deadlocks in einem benutzerdefinierten Filter zu vermeiden.

In den Beispielen in diesem Abschnitt wird Pseudo Code verwendet, um den Code zu veranschaulichen, den Sie schreiben müssen. Sie gehen davon aus, dass ein benutzerdefinierter Filter von den DirectShow-Basisklassen abgeleitete Klassen wie folgt verwendet:

-   Cmyinputpin: abgeleitet von [**cbaseinputpin**](cbaseinputpin.md).
-   Cmyoutputpin: abgeleitet von [**cbaseoutputpin**](cbaseoutputpin.md).
-   Cmyfilter: abgeleitet von [**cbasefilter**](cbasefilter.md).
-   Cmyinputzucator: die Zuweisung der eingabepin, die von [**cmemzuzuordcator**](cmemallocator.md)abgeleitet ist. Nicht jeder Filter benötigt eine benutzerdefinierte Zuweisung. Für viele Filter ist die Klasse **cmemzuordcator** ausreichend.

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [Streaming-und Anwendungsthreads](the-streaming-and-application-threads.md)
-   [Wird angehalten](pausing.md)
-   [Empfangen und Bereitstellung von Beispielen](receiving-and-delivering-samples.md)
-   [Über das Ende des Streams](delivering-the-end-of-stream.md)
-   [Leeren von Daten](flushing-data.md)
-   [Wird beendet](stopping.md)
-   [Puffer werden erhalten.](getting-buffers.md)
-   [Streamingthreads und der Filter Graph-Manager](streaming-threads-and-the-filter-graph-manager.md)
-   [Zusammenfassung des filterthreading](summary-of-filter-threading.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



