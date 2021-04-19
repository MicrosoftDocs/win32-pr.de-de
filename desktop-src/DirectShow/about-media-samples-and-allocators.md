---
description: Informationen zu Medien Beispielen und-Zuweisungen
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: Informationen zu Medien Beispielen und-Zuweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106357146"
---
# <a name="about-media-samples-and-allocators"></a>Informationen zu Medien Beispielen und-Zuweisungen

Filter übermitteln Daten über PIN-Verbindungen. Daten werden von der Ausgabe-PIN eines Filters zur Eingabe-PIN eines anderen Filters verschoben. Die häufigste Methode für die Bereitstellung der Daten durch den Ausgabepin besteht darin, dass die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode für die Eingabe aufgerufen wird, obwohl auch einige andere Mechanismen vorhanden sind.

Abhängig vom Filter kann der Arbeitsspeicher für die Mediendaten auf verschiedene Arten zugewiesen werden: auf dem Heap, in einer DirectDraw-Oberfläche, mithilfe von frei gegebenem GDI-Speicher oder mit einem anderen Zuordnungs Mechanismus. Das für die Zuordnung des Arbeitsspeichers verantwortliche Objekt wird *als Zuweisung bezeichnet*. Hierbei handelt es sich um ein COM-Objekt, das die [**imembelegcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle verfügbar macht.

Wenn zwei Pins eine Verbindung herstellen, muss einer der Pins eine Zuweisung bereitstellen. DirectShow definiert eine Sequenz von Methoden aufrufen, die verwendet wird, um festzulegen, welche PIN die Zuweisung bereitstellt. Die Pins stimmen auch mit der Anzahl von Puffern, die von der Zuweisung erstellt werden, und der Puffergröße überein.

Bevor das Streaming beginnt, erstellt die Zuweisung einen Pufferpool. Beim Streaming füllt der Upstream-Filter Puffer mit Daten und übergibt sie an den downstreamfilter. Der upstreamfilter gibt den nachgeschalteten Filter jedoch keine Rohdaten Zeiger auf die Puffer aus. Stattdessen werden COM-Objekte mit dem Namen " *Media Samples*" verwendet, die von der Zuweisung zum Verwalten der Puffer erstellt werden. Mit Medien Beispielen wird die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle verfügbar gemacht. Ein Medien Beispiel enthält Folgendes:

-   Ein Zeiger auf den zugrunde liegenden Puffer.
-   ein Zeitstempel
-   verschiedene Flags
-   optional ein Medientyp

Der Zeitstempel definiert die Präsentationszeit, die der rendererfilter zum Planen des Rendering verwendet. Die Flags geben an, ob seit dem vorherigen Beispiel eine Unterbrechung der Daten aufgetreten ist. Der Medientyp stellt eine Möglichkeit für Filter zum Ändern von Formaten in der Mitte des Streams bereit. In der Regel hat das Beispiel keinen Medientyp, was darauf hinweist, dass das Format seit dem vorherigen Beispiel nicht geändert wurde.

Während ein Filter einen Puffer verwendet, enthält er den Verweis Zähler für das Beispiel. Die Zuweisung verwendet den Verweis Zähler, um zu bestimmen, wann der Puffer wieder verwendet werden kann. Dadurch wird verhindert, dass ein Filter einen Puffer überschreibt, den ein anderer Filter weiterhin verwendet. Ein Beispiel kehrt nicht zum Pool der verfügbaren Stichproben zurück, bis jeder Filter ihn freigegeben hat.

Weitere Informationen finden Sie unter den folgenden Themen:

-   Das Thema [Beispiele und Zuweisungen](samples-and-allocators.md) bietet eine ausführlichere Beschreibung der Funktionsweise von Zuweisungen.
-   Der Thema [Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md) bietet einen allgemeinen Überblick über den Datenfluss in DirectShow.

Die folgenden Themen sind für Entwickler gedacht, die ihre eigenen benutzerdefinierten Filter schreiben:

-   [Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md)
-   [Threads und kritische Abschnitte](threads-and-critical-sections.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Filter Diagramm und dessen Komponenten](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



