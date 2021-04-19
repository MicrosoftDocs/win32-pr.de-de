---
description: Server-Side Fehler
ms.assetid: ce8ddb52-237c-4d46-a088-9f592afadcd2
title: Server-Side Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7946b8197553874b8da22d35f8fab5b83f14862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345443"
---
# <a name="server-side-errors"></a>Server-Side Fehler

Der Listener und der Player arbeiten zusammen, um mit nicht verarbeitbaren Nachrichten umzugehen. Wenn eine Transaktion, die wiedergegeben wird, fehlschlägt, verschiebt [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) die Eingabe Nachricht zurück in die Eingabe Warteschlange. Der Player bricht die Transaktion ab, wenn er ein fehlerhafter HRESULT von der Serverkomponente empfängt oder eine Ausnahme abfängt. Wenn das Problem weiterhin besteht, könnte der Listener fortlaufend im folgenden Muster Schleifen:

-   Entfernt die Nachricht aus der Warteschlange
-   Instanziiert das Objekt.
-   Führt ein Rollback aus.
-   Setzt die Nachricht am Anfang der Warteschlange zurück.

Der Dienst für in der Warteschlange befindliche Komponenten verarbeitet diesen Fehler mithilfe einer Reihe von anwendungsspezifischen Wiederholungs Warteschlangen. Wird bei der Installation der-Komponente erstellt, sind für jede Anwendung sieben Warteschlangen verfügbar, wie im folgenden dargestellt:

1.  Die normale Eingabe Warteschlange. Der Name dieser Warteschlange ist der com+-Anwendungsname. Dies ist eine Message Queuing öffentliche Warteschlange.

2.  Die erste Wiederholungs Warteschlange. Nachrichten werden hier verschoben, wenn die Transaktion beim Verarbeiten von Nachrichten aus der normalen Eingabe Warteschlange wiederholt ausfällt. Nachrichten in dieser Warteschlange werden nach einer Minute verarbeitet. Eine Nachricht kann dreimal in dieser Warteschlange wiederholt werden, bevor Sie in die zweite Wiederholungs Warteschlange verschoben wird. Diese Warteschlange hat den Namen *ApplicationName* \_ 0. Diese Warteschlange ist eine private Message Queuing Warteschlange.

3.  Die zweite Wiederholungs Warteschlange. Nachrichten werden hier verschoben, wenn die Transaktion beim Verarbeiten von Nachrichten aus der ersten Wiederholungs Warteschlange wiederholt fehlschlägt. Nachrichten in dieser Warteschlange werden nach zwei Minuten verarbeitet. Eine Nachricht kann dreimal in dieser Warteschlange wiederholt werden, bevor Sie in die dritte Wiederholungs Warteschlange verschoben wird. Diese Warteschlange hat den Namen *ApplicationName* \_ 1. Diese Warteschlange ist eine private Message Queuing Warteschlange.

4.  Die dritte Wiederholungs Warteschlange. Nachrichten werden hier verschoben, wenn die Transaktion beim Verarbeiten von Nachrichten aus der zweiten Wiederholungs Warteschlange wiederholt fehlschlägt. Nachrichten in dieser Warteschlange werden nach vier Minuten verarbeitet. Eine Nachricht kann dreimal in dieser Warteschlange wiederholt werden, bevor Sie in die vierte Wiederholungs Warteschlange verschoben wird. Diese Warteschlange hat den Namen *ApplicationName* \_ 2. Diese Warteschlange ist eine private Message Queuing Warteschlange.

5.  Die vierte Wiederholungs Warteschlange. Nachrichten werden hier verschoben, wenn die Transaktion beim Verarbeiten von Nachrichten aus der dritten Wiederholungs Warteschlange wiederholt fehlschlägt. Nachrichten in dieser Warteschlange werden nach acht Minuten verarbeitet. Eine Nachricht kann dreimal in dieser Warteschlange wiederholt werden, bevor Sie in die fünfte Wiederholungs Warteschlange verschoben wird. Diese Warteschlange weist den Namen *ApplicationName* \_ 3 auf. Diese Warteschlange ist eine private Message Queuing Warteschlange.

6.  Die fünfte Wiederholungs Warteschlange. Nachrichten werden hier verschoben, wenn die Transaktion beim Verarbeiten von Nachrichten aus der vierten Wiederholungs Warteschlange wiederholt fehlschlägt. Nachrichten in dieser Warteschlange werden nach 16 Minuten verarbeitet. Eine Nachricht kann dreimal in dieser Warteschlange wiederholt werden, bevor Sie in die letzte ruhende Warteschlange verschoben wird. Diese Warteschlange hat den Namen *ApplicationName* \_ 4. Dies ist eine private Message Queuing Warteschlange.

7.  Eine anwendungsspezifische abschließende ruhende Warteschlange. Nachrichten werden hier verschoben, wenn die Transaktion bei einem Versuch in der fünften Wiederholungs Warteschlange wiederholt abgebrochen wird. Diese Warteschlange heißt " *ApplicationName* \_ deadqueue". Dies ist eine private Message Queuing Warteschlange. Die letzte ruhende Warteschlange wird von einem Warteschlangenlistener nicht bedient. Nachrichten bleiben hier, bis Sie manuell verschoben werden (möglicherweise durch das Nachrichten verschiebungsprogramm der Warteschlange in der Warteschlange) oder durch Message Queuing Explorer gelöscht werden.

Nachrichten, die nicht wieder verwendet werden können, weil klar ist, dass jeder Wiederholungsversuch fehlschlägt, kann direkt in die anwendungsspezifische endgültige ruhende Warteschlange verschoben werden, ohne dass diese über alle Wiederholungs Stufen erweitert wird.

Der Player gibt ein com+-Ereignis aus, um interessierten Parteien mitzuteilen, dass Nachrichten nicht wiedergegeben werden können. Com+-Ereignisse werden in den folgenden Situationen ausgegeben:

-   Wenn eine Transaktion abgebrochen wird
-   Wenn eine Nachricht von einer Warteschlange in eine andere verschoben wird
-   Wenn eine Nachricht in der letzten ruhenden Warteschlange abgelegt wird

Nachrichten können geändert werden, bevor Sie von einer Warteschlange in eine andere verschoben werden. Der Sicherheitsmechanismus der in der Warteschlange befindlichen Komponenten von com+ ermöglicht es, eine Nachricht in Wiederholungs Warteschlangen zu verschieben und Sie dann in die anfängliche Eingabe Warteschlange der Anwendung erneut einzufügen. Weitere Informationen zur Sicherheit in der Warteschlange befindliche Komponenten finden Sie unter Sicherheit in der [Warteschlange](queued-components-security.md)für die Sicherheit.

Wiederholungs Warteschlangen werden zusammen mit der Haupt Anwendungs Warteschlange erstellt, wenn die Anwendung entweder vom Verwaltungs Tool für Komponenten Dienste als in die Warteschlange eingereiht oder mithilfe der com+-Funktionen für das administrative SDK gekennzeichnet wird. Der Dienst für in der Warteschlange befindliche Komponenten ermöglicht die Flexibilität des Wiederholungs Mechanismus, indem das Löschen von Wiederholungs Warteschlangen zugelassen wird. Wenn z. b. alle Wiederholungs Warteschlangen gelöscht werden, wird eine Nachricht, die permanent abgebrochen wird, direkt aus der Anwendungs Warteschlange in die anwendungsspezifische endgültige ruhende Warteschlange verschoben. Wenn Sie eine oder mehrere Wiederholungs Warteschlangen entfernen, kann die Anzahl und Länge der Wiederholungen verringert werden. Wenn Warteschlangen aus der Wiederholungs Sequenz entfernt werden, entspricht die zeitliche Steuerung der restlichen Warteschlangen der Position in der Sequenz von Wiederholungs Warteschlangen. Wenn Sie z. b. die Wiederholungs Warteschlange *ApplicationName* \_ 1, *ApplicationName* \_ 2 und *ApplicationName* \_ 3 entfernen, werden die Nachrichten auf *ApplicationName* \_ 4 so verarbeitet, als ob es sich bei der Warteschlange um die zweite Wiederholungs Warteschlange handelt.

Der Wiederholungs Mechanismus ist so konzipiert, dass eine Nachricht nach Möglichkeit vollständig ausgeführt wird. In einigen Fällen ist es möglicherweise nicht möglich, dass die Nachricht erfolgreich ist. Beispielsweise versucht ein Client möglicherweise, Geld von einem Konto mit unzureichendem Guthaben zu entziehen. In diesen Fällen können Sie den Fehler auf verschiedene Weise behandeln, einschließlich der folgenden:

-   Diagnose generieren und eine Warnung ausgeben
-   Erstellen einer kompensierenden Transaktion
-   Ignorieren des Problems und verwerfen der Nachricht

Wie bei Client seitigen persistenten Fehlern ermöglicht der Dienst für die Warteschlangen Dienste eine Zuordnung einer Ausnahme Klasse zu einer Komponente. Die Ausnahme Klasse wird der Komponente mithilfe der Registerkarte **erweitert** auf der Seite Komponenteneigenschaften des Verwaltungs Tools für Komponenten Dienste oder mithilfe der com+-Verwaltungsfunktionen zugeordnet. Die Exception-Klasse ermöglicht es dem Entwickler, die Kontrolle zu haben, nachdem eine Nachricht wiederholt wurde und bevor diese Nachricht in die anwendungsspezifische endgültige ruhende Warteschlange verschoben wird. Weitere Informationen zur Ausnahme Klasse finden Sie unter [persistente Client-Side Fehler](persistent-client-side-failures.md).

Im folgenden wird die Abfolge der Ereignisse für die serverseitige Ausnahmebehandlung aufgeführt:

1.  Die Meldung wird durch die verfügbaren anwendungsspezifischen Wiederholungs Warteschlangen verschoben.
2.  Der letzte Wiederholungsversuch für die letzte Wiederholungs Warteschlange schlägt fehl.
3.  Die Dienst Laufzeit der in der Warteschlange befindlichen Komponenten Ruft die Zielkomponente aus der Nachricht ab und überprüft, ob eine Ausnahme Klasse besteht.
4.  Die Lauf Zeit Instanz instanziiert die Exception-Klasse.
5.  Die Lauf Zeit Abfragen von [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) für die Exception-Klasse.
6.  Die Laufzeit ruft [**IPlaybackControl:: FinalServerRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalserverretry) in der Ausnahme Klasse auf.
7.  Die Laufzeit gibt alle Eigenschaften-und Methodenaufrufe von der Nachricht an die Exception-Klasse zurück.
8.  Wenn die Schritte 4 bis 6 nicht erfolgreich sind, wird die Nachricht von der Laufzeit in die anwendungsspezifische abschließende ruhende Warteschlange verschoben.

Wenn Sie in den oben beschriebenen Prozess eingreifen müssen oder eine nicht verarbeitbare Nachricht aus der letzten ruhenden Warteschlange entfernen müssen, verwenden Sie das Hilfsprogramm Nachrichten Verschiebung. Weitere Informationen zum Hilfsprogramm für den Nachrichten Verschiebungsvorgang finden Sie unter [Behandeln von Fehlern](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Client seitige Fehler](client-side-errors.md)
</dt> <dt>

[Persistente Client-Side Fehler](persistent-client-side-failures.md)
</dt> </dl>

 

 



