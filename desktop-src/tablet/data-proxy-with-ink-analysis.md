---
description: Wie unter Übersicht über die Ink-Analyse erwähnt, verwaltet die Ink-Analysetechnologie intern ein strukturbasiertes Dokumentmodell, das Analyseergebnisse und Beziehungen enthält.
ms.assetid: 33ba9292-3bc7-41ba-a602-e2fc94cd3a57
title: Datenproxy mit Ink-Analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad79a37a3220351adad56c0a131392e96964714114ba1e0a982833b07bc85077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092779"
---
# <a name="data-proxy-with-ink-analysis"></a>Datenproxy mit Ink-Analyse

Wie unter Übersicht über die [Ink-Analyse](ink-analysis-overview.md)erwähnt, verwaltet die Ink-Analysetechnologie intern ein strukturbasiertes Dokumentmodell, das Analyseergebnisse und Beziehungen enthält. Wenn Ihre Anwendung bereits über einen anderen Dokumentspeicher verfügt, müssen Sie die Funktionen für die Ink-Analyse verwenden, um Daten zwischen unterschiedlichen Dokumentmodellen zu proxyn.

## <a name="types-of-data-proxy"></a>Typen von Datenproxys

Die Datenproxyfeatures ermöglichen Ihrer Anwendung Folgendes:

-   Integrieren Sie Analyseergebnisdaten wieder in ein vorhandenes Dokumentmodell.
-   Geben Sie die vorherigen Ergebnisse (oder den Zustand) wieder an [**inkAnalyzer**](inkanalyzer.md)weiter.
-   Kommunizieren Sie den Nicht-Freihandzustand mit [**inkAnalyzer**](inkanalyzer.md).
-   Kommunizieren Sie nur den minimalen Satz von Daten (sowohl den vorherigen als auch den Nicht-Freihandzustand), der zum Abschließen des Analysevorgangs erforderlich ist.
-   Aktualisieren Sie ganz einfach das interne Anwendungsdokumentmodell mit Analyseergebnissen.

Es gibt zwei grundlegende Ansätze für den Ink-Analysedatenproxy. Die Unterschiede liegen in den Details dazu, wann und wie die Synchronisierung zwischen den Dokumentmodellen erfolgt. Der erste Ansatz, das synchrone Update, erfordert die Änderung des Dokumentmodells für die Ink-Analyse, wenn Änderungen im Anwendungsdokument auftreten. Der zweite Ansatz, das bedarfsorientierte Update, erfordert, dass nur die Daten, die von Änderungen am Anwendungsdokumentmodell betroffen sind, an [**InkAnalyzer**](inkanalyzer.md)übergeben werden. Das heißt, nur die Daten für die Teile des Dokumentmodells für die Inkanalyse, die sich im selben Bereich wie Änderungen am Anwendungsdokument befinden, müssen je nach Bedarf an **InkAnalyzer** übergeben werden.

### <a name="synchronous-update"></a>Synchrones Update

Der synchrone Updateansatz erfordert die Änderung (Erstellung und Löschung) von Knoten in der Sammlung von [**ContextNode-Objekten**](icontextnode.md) des [**InkAnalyzer-Objekts,**](inkanalyzer.md) wie sie im Anwendungsdokument auftreten. Jedes Mal, wenn der Anwendung ein Textwort hinzugefügt wird, wird beispielsweise im **InkAnalyzer** ein entsprechender **ContextNode** im **TextWord-Format** erstellt. Wenn sich die Position des Textworts auf der Seite ändert, wird der Speicherort des entsprechenden **ContextNode** gleichzeitig aktualisiert. Diese Methode ist im Hinblick auf die Berechnung von Ressourcen weniger effizient als die on-demand-Methode, da jede Dokumentänderung eine Aktualisierung des **InkAnalyzer** beinhaltet, auch wenn sich die Änderung nicht auf die zu analysierende Ink-Methode auswirkt.

Das folgende Beispiel soll zeigen, wie synchrone Updates funktionieren. Imagine eine Anwendung, die über ein vorhandenes Dokumentmodell verfügt. Wenn der Endbenutzer eine Änderung am Dokument vornimmt, z. B. neuen Text hinzufügt, wird die Änderung wie folgt verarbeitet:

1.  Der Endbenutzer erstellt die neuen Daten.
2.  Die Anwendung bestimmt, wie die Daten verarbeitet, gespeichert und gerendert werden.
3.  Aus praktischen Gründen werden die folgenden Schritte gleichzeitig ausgeführt.
    1.  Die Anwendung platziert die Daten in ihr Dokumentmodell.
    2.  Die Anwendung erstellt einen [**InkAnalyzer**](inkanalyzer.md) und aktualisiert ihn. Dadurch wird gleichzeitig sichergestellt, dass **InkAnalyzer** immer über die neuesten Informationen verfügt.
    3.  Die Anwendung ruft [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) für [**inkAnalyzer**](inkanalyzer.md) auf, um mit der Analyse zu beginnen.
4.  Eine Reihe von Ereignissen wird ausgelöst, wenn die Änderung [**InkAnalyzer**](inkanalyzer.md) beinhaltet und neue Ergebnisse ermittelt. Ein Ereignis wird für jede Änderung ausgelöst, die an der Auflistung von [**ContextNode-Objekten**](icontextnode.md) im **InkAnalyzer** vorgenommen wird. Zu diesen Ereignissen gehören [**ContextNodeCreated,**](-ianalysisproxyevents-contextnodecreated.md) [**ContextNodeDeleting,**](-ianalysisproxyevents-contextnodedeleting.md) [**ContextNodeMovingToPosition,**](-ianalysisproxyevents-contextnodemovingtoposition.md) [**ContextNodePropertiesUpdated,**](-ianalysisproxyevents-contextnodepropertiesupdated.md) [**ContextNodeLinkAdding,**](-ianalysisproxyevents-contextnodelinkadding.md) [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)und [**ContextNodeReparenting.**](-ianalysisproxyevents-contextnodereparenting.md) Die Anwendung verarbeitet diese Ereignisse, um die Ergebnisse des Analysevorgangs nach Bedarf an das Dokumentmodell zurückzugeben.
5.  Die Anwendung aktualisiert das Layout des Dokuments und pullt die neuen Daten aus dem Dokumentmodell.
6.  Die neuen Daten werden an den Endbenutzer zurück gerendert.

### <a name="on-demand-update"></a>Bedarfsorientiertes Update

Der Bedarfsorientierte Ansatz erfordert nur, dass die Daten für die [**ContextNode-Objekte**](icontextnode.md) übergeben werden, die sich in den Bereichen befinden, die analysiert werden. Die erforderlichen **ContextNode-Objekte** werden direkt nach dem Aufruf des Analysevorgangs und unmittelbar vor der Abstimmung der Ergebnisse aus dem Dokumentmodell der Anwendung extrahiert. Obwohl die Implementierung komplizierter als synchrone Updates ist, führt dieser Ansatz zu besseren Leistungsergebnissen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Ink-Analyse](ink-analysis-overview.md)
</dt> <dt>

[**InkAnalyzer-Klasse (C++)**](inkanalyzer.md)
</dt> <dt>

[**Microsoft.Ink.InkAnalyzer**](/previous-versions/ms583671(v=vs.100))
</dt> <dt>

[**Microsoft.Ink.ContextNode**](/previous-versions/ms551996(v=vs.100))
</dt> </dl>

 

 
