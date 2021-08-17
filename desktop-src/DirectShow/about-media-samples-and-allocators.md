---
description: Informationen zu Medienbeispielen und Zuweisungen
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: Informationen zu Medienbeispielen und Zuweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9390bd99ab019effa40f9edca1f8d9e03ea73c5b0085ed8b1bc13f013cad6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430280"
---
# <a name="about-media-samples-and-allocators"></a>Informationen zu Medienbeispielen und Zuweisungen

Filter stellen Daten über Pinverbindungen hinweg bereit. Daten werden vom Ausgabepin eines Filters zum Eingabepin eines anderen Filters verschoben. Die gängigste Methode zum Übermitteln der Daten durch den Ausgabepin besteht darin, die [**IMemInputPin::Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) für die Eingabe aufzurufen, obwohl auch einige andere Mechanismen vorhanden sind.

Je nach Filter kann Speicher für die Mediendaten auf verschiedene Weise zugeordnet werden: auf dem Heap, auf einer DirectDraw-Oberfläche, mit freigegebenen GDI-Speicher oder mit einem anderen Zuordnungsmechanismus. Das Objekt, das für die Zuweisung des Arbeitsspeichers verantwortlich ist, wird als *Allocator* bezeichnet. Dabei handelt es sich um ein COM-Objekt, das die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) verfügbar macht.

Wenn zwei Stecknadeln verbunden sind, muss einer der Stecknadeln eine Zuweisung bereitstellen. DirectShow definiert eine Sequenz von Methodenaufrufen, die verwendet werden, um festzulegen, welcher Pin die Zuweisung bereitstellt. Die Pins stimmen auch über die Anzahl der Puffer, die von der Zuweisung erstellt werden, und die Größe der Puffer überein.

Bevor das Streaming beginnt, erstellt die Zuweisung einen Pufferpool. Während des Streamings füllt der Upstreamfilter Puffer mit Daten auf und übermittelt sie an den Downstreamfilter. Der Upstreamfilter gibt dem Downstreamfilter jedoch keine rohen Zeiger auf die Puffer. Stattdessen werden COM-Objekte verwendet, die als *Medienbeispiele* bezeichnet werden und von der Zuweisung erstellt werden, um die Puffer zu verwalten. Medienbeispiele machen die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) verfügbar. Ein Medienbeispiel enthält Folgendes:

-   ein Zeiger auf den zugrunde liegenden Puffer
-   einen Zeitstempel
-   verschiedene Flags
-   optional ein Medientyp

Der Zeitstempel definiert die Präsentationszeit, die der Rendererfilter zum Planen des Renderings verwendet. Die Flags geben z. B. an, ob die Daten seit dem vorherigen Beispiel eine Unterbrechung auftraten. Der Medientyp bietet eine Möglichkeit für Filter, Formate während des Streams zu ändern. In der Regel weist das Beispiel keinen Medientyp auf, was angibt, dass sich das Format seit dem vorherigen Beispiel nicht geändert hat.

Während ein Filter einen Puffer verwendet, enthält er die Verweisanzahl für das Beispiel. Die Zuweisung verwendet den Verweiszähler, um zu bestimmen, wann der Puffer wiederverwendet werden kann. Dadurch wird verhindert, dass ein Filter einen Puffer überschreibt, den ein anderer Filter noch verwendet. Ein Beispiel kehrt erst dann zum Pool der verfügbaren Stichproben zurück, wenn jeder Filter ihn freigegeben hat.

Weitere Informationen finden Sie in den folgenden Themen:

-   Das Thema [Beispiele und Zuweisungen](samples-and-allocators.md) enthält eine ausführlichere Beschreibung der Funktionsweise von Zuweisungen.
-   Das Thema [Daten Flow im Graph Filter](data-flow-in-the-filter-graph.md) bietet eine allgemeine Übersicht über den Datenfluss in DirectShow.

Die folgenden Themen sind für Entwickler gedacht, die ihre eigenen benutzerdefinierten Filter schreiben:

-   [Daten Flow für Filterentwickler](data-flow-for-filter-developers.md)
-   [Threads und kritische Abschnitte](threads-and-critical-sections.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Filter Graph und die zugehörigen Komponenten](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



