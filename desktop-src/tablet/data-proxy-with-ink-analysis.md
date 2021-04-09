---
description: Wie in der Übersicht über die frei Hand Analyse erwähnt, verwaltet die frei Hand Analyse-Technologie intern ein Struktur basiertes Dokument Modell, das Analyseergebnisse und-Beziehungen enthält.
ms.assetid: 33ba9292-3bc7-41ba-a602-e2fc94cd3a57
title: Daten Proxy mit Ink-Analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52717b955625e67f50c20703dd0e84449aa1037f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868299"
---
# <a name="data-proxy-with-ink-analysis"></a>Daten Proxy mit Ink-Analyse

Wie in der [Übersicht über](ink-analysis-overview.md)die frei Hand Analyse erwähnt, verwaltet die frei Hand Analyse-Technologie intern ein Struktur basiertes Dokument Modell, das Analyseergebnisse und-Beziehungen enthält. Wenn Ihre Anwendung bereits über einen anderen eingerichteten Dokument Speicher verfügt, müssen Sie die Funktionen zur frei Hand Analyse verwenden, die für den Proxy von Daten zwischen verschiedenartigen Dokument Modellen konzipiert sind.

## <a name="types-of-data-proxy"></a>Typen von Daten Proxys

Die Daten Proxy Features ermöglichen der Anwendung Folgendes:

-   Integrieren Sie Analyseergebnis Daten zurück in ein vorhandenes Dokument Modell.
-   Übermitteln Sie vorherige Ergebnisse (oder Status) wieder in den [**InkAnalyzer**](inkanalyzer.md).
-   Kommunizieren Sie den Non-Ink-Zustand mit dem [**InkAnalyzer**](inkanalyzer.md).
-   Übermitteln Sie nur den minimalen Satz von Daten (sowohl vorheriger als auch nicht-frei Hand Zustand), der zum Abschluss des Analyse Vorgangs erforderlich ist.
-   Aktualisieren Sie das interne Anwendungs Dokument Modell problemlos mit den Analyseergebnissen.

Es gibt zwei grundlegende Ansätze für den frei Hand Analyse-Daten Proxy. Die Unterschiede werden in den Details der Art und Weise der Synchronisierung zwischen den Dokument Modellen aufgeführt. Der erste Ansatz (synchrones Update) erfordert die Änderung des frei Hand Analyse-Dokument Modells, wenn Änderungen im Anwendungs Dokument auftreten. Der zweite Ansatz erfordert, dass bei Bedarf nur die Daten, die von Änderungen am Anwendungs Dokument Modell betroffen sind, an den [**InkAnalyzer**](inkanalyzer.md)weitergeleitet werden. Das heißt, dass nur die Daten für die Teile des frei Hand Analyse-Dokument Modells, die sich im gleichen Bereich wie Änderungen am Anwendungs Dokument befinden, an den **InkAnalyzer** übermittelt werden müssen, wenn Sie Sie benötigen.

### <a name="synchronous-update"></a>Synchrones Update

Der synchrone Aktualisierungs Ansatz erfordert die Änderung (Erstellung und Löschung) der Knoten in der Auflistung von [**ContextNode**](icontextnode.md) -Objekten des [**InkAnalyzer**](inkanalyzer.md) -Objekts, wie Sie im Anwendungs Dokument vorkommen. Wenn z. b. ein textwort der Anwendung hinzugefügt wird, wird ein entsprechendes **textword** -Format " **ContextNode** " im " **InkAnalyzer**" erstellt. Wenn sich der Speicherort des Textworts auf der Seite ändert, wird der Speicherort des entsprechenden **ContextNode** gleichzeitig aktualisiert. Diese Methode ist im Hinblick auf die computingressourcen weniger effizient als bei der bedarfsgesteuerten Methode, da jede Dokument Änderung ein Update des **inkanalyzers** umfasst, selbst wenn sich die Änderung nicht auf die zu analysierende Überschrift auswirkt.

Im folgenden Beispiel wird gezeigt, wie das synchrone Update funktioniert. Stellen Sie sich eine Anwendung vor, die ein vorhandenes Dokument Modell aufweist. Wenn der Endbenutzer eine Änderung am Dokument vornimmt, wie z. b. das Hinzufügen von neuem Text, wird die Änderung wie folgt verarbeitet:

1.  Der Endbenutzer erstellt die neuen Daten.
2.  Die Anwendung bestimmt, wie die Daten verarbeitet, gespeichert und gerendert werden.
3.  Aus praktischen Gründen erfolgen die folgenden Schritte gleichzeitig.
    1.  Die Anwendung speichert die Daten in das Dokument Modell.
    2.  Von der Anwendung wird ein [**InkAnalyzer**](inkanalyzer.md) erstellt und aktualisiert. Gleichzeitig wird sichergestellt, dass der **InkAnalyzer** immer über die aktuellsten Informationen verfügt.
    3.  Die Anwendung ruft [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) für den [**InkAnalyzer**](inkanalyzer.md) auf, um die Analyse zu starten.
4.  Eine Reihe von Ereignissen wird ausgelöst, wenn die Änderung frei Hand Eingaben umfasst und der [**InkAnalyzer**](inkanalyzer.md) neue Ergebnisse bestimmt. Ein Ereignis wird für jede Änderung ausgelöst, die an der Auflistung von [**ContextNode**](icontextnode.md) -Objekten im **InkAnalyzer** vorgenommen wird. Diese Ereignisse umfassen " [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md)", " [**contextnodelösch**](-ianalysisproxyevents-contextnodedeleting.md)", " [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)", " [**contextnodepropertiesaktualisierten**](-ianalysisproxyevents-contextnodepropertiesupdated.md)", " [**contextnodelinkadditions**](-ianalysisproxyevents-contextnodelinkadding.md)", " [**contextnodelinklösch**](-ianalysisproxyevents-contextnodelinkdeleting.md)" und " [**contextnodereterenting**](-ianalysisproxyevents-contextnodereparenting.md)". Die Anwendung verarbeitet diese Ereignisse, um die Ergebnisse des Analyse Vorgangs nach Bedarf wieder in das Dokument Modell zu überführen.
5.  Die Anwendung aktualisiert das Layout des Dokuments und zieht die neuen Daten aus dem Dokument Modell.
6.  Die neuen Daten werden wieder an den Endbenutzer gerendert.

### <a name="on-demand-update"></a>Bedarfs gesteuertes Update

Der Bedarfs gesteuerte Ansatz erfordert nur, dass die Daten für die [**ContextNode**](icontextnode.md) -Objekte, die sich in den analysierten Bereichen befinden, übergeben werden. Die benötigten **ContextNode** -Objekte werden direkt nach dem Aufrufen des Analyse Vorgangs aus dem Dokument Modell der Anwendung extrahiert, und auch unmittelbar vor dem Abgleich der Ergebnisse. Diese Vorgehensweise führt bei der Implementierung komplizierter als bei synchronen Updates zu besseren Leistungsergebnissen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Link Analyse](ink-analysis-overview.md)
</dt> <dt>

[**InkAnalyzer-Klasse (C++)**](inkanalyzer.md)
</dt> <dt>

[**Microsoft. Ink. InkAnalyzer**](/previous-versions/ms583671(v=vs.100))
</dt> <dt>

[**Microsoft. Ink. ContextNode**](/previous-versions/ms551996(v=vs.100))
</dt> </dl>

 

 
