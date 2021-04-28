---
description: Benachrichtigungsprozess in Windows Search
ms.assetid: 378e346b-2067-484f-85e9-76673a35550b
title: Benachrichtigungsprozess in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b37747d1ec13c3a4a865e16721c64d4a0186dbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089818"
---
# <a name="notifications-process-in-windows-search"></a>Benachrichtigungsprozess in Windows Search

Dieses Thema ist wie folgt organisiert:

-   [Übersicht über den Benachrichtigungsprozess](#overview-of-the-notifications-process)
-   [Durchforstungen](#crawls)
-   [Vom Indexer verwaltete Benachrichtigungen](#indexer-managed-notifications)
-   [Vom Anbieter verwaltete Benachrichtigungen](#provider-managed-notifications)
-   [Benachrichtigungen für Rowsets](#notifications-on-rowsets)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-the-notifications-process"></a>Übersicht über den Benachrichtigungsprozess

Es gibt drei Ansätze, mit denen Daten aus Ihrem Datenspeicher indiziert werden können:

-   Durchforstungen
-   Vom Indexer verwaltete Benachrichtigungen
-   Vom Anbieter verwaltete Benachrichtigungen

Die Vorteile der einzelnen Ansätze werden in den folgenden Abschnitten beschrieben.

## <a name="crawls"></a>Durchforstungen

Benachrichtigungsfähige Quellen führt beim Start eine inkrementelle Durchforstung durch und verwenden dann Benachrichtigungen oder einen expliziten Befehl zum erneuten Durchforsten. Dies geschieht automatisch unter Windows Vista und höher. Unter Betriebssystemen vor Windows Vista müssen Sie ein geplantes Ereignis in der [Taskplaner](../taskschd/task-scheduler-start-page.md) einrichten, das ihren Code aufruft, um eine Durchforstung über Ihre Startseiten zu initiieren. Sie müssen keine Form von Benachrichtigungen implementieren. Als Hintergrundprozess durchläuft der Indexer seinen Durchforstungsbereich, sucht nach Änderungen und aktualisiert den Katalog. Diese Option wird für fast alle Situationen empfohlen.

## <a name="indexer-managed-notifications"></a>Indexer-Managed Benachrichtigungen

Mit vom Indexer verwalteten Benachrichtigungen implementieren Sie eine Benachrichtigungsstrategie, die den Indexer benachrichtigt, wenn sich Daten im Datenspeicher geändert haben, und der Indexer verwaltet die Nachverfolgung der Benachrichtigungen und die Indizierung der Daten. In diesem Fall überwacht Ihre Komponente (die wir als Benachrichtigungsanbieter bezeichnen) den Datenspeicher, sammelt Informationen zu Änderungen am Speicher und benachrichtigt den Indexer dann in regelmäßigen Abständen mit einer Liste von Elementen, die indiziert werden müssen. Der Indexer ist für die Wiederherstellung und Auflösung von Benachrichtigungen im Falle eines Fehlers verantwortlich. Diese Option, die Sie sich als Strategie "Senden und Vergessen" einhandeln können, reduziert die Häufigkeit von Indexerforstungen.

## <a name="provider-managed-notifications"></a>Provider-Managed Benachrichtigungen

Mit vom Anbieter verwalteten Benachrichtigungen implementieren Sie eine Benachrichtigungsstrategie, die dem zweiten Ansatz ähnelt, mit der Ausnahme, dass Ihr Benachrichtigungsanbieter Benachrichtigungen nachverfolgen muss und für die Wiederherstellung und Behebung von Benachrichtigungen im Falle eines Fehlers verantwortlich ist. In diesem Fall überwacht Ihr Benachrichtigungsanbieter den Datenspeicher, sammelt und verwaltet Informationen zu Änderungen am Speicher, benachrichtigt den Indexer in regelmäßigen Abständen mit einer Liste von Elementen, die indiziert werden müssen, empfängt Statusaktualisierungen vom Indexer und sendet Benachrichtigungen im Falle eines Fehlers erneut.

> [!Note]  
> Diese Option **wird** nicht empfohlen, es sei denn, Sie erwarten, dass inkrementelle Durchforstungen Ihres Datenspeichers die Leistung erheblich beeinträchtigen, und Sie benötigen eine präzise Kontrolle über den Indizierungsstatus oder einen Einblick in den Indizierungsstatus.

 

## <a name="notifications-on-rowsets"></a>Benachrichtigungen zu Rowsets

In Windows 7 und höher ermöglicht die Indizierungsereignisierung Anbietern das Empfangen von Benachrichtigungen über ihre Rowsets. Anbieter, die indizierungsereignis verwenden, können ihre Rowsets so verwalten, dass sie dem Verhalten der tatsächlichen Dateisystemstandorte ähneln. Bibliotheken und Suchvorgänge sind die wichtigsten Beispiele für Speicherorte ohne Dateisystem in Windows 7. Beim Indexerereignis werden Bibliotheksansichten als Benachrichtigungen an Dateiordneransichten verwendet. Die [**IRowsetEvents-Schnittstelle**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) muss implementiert werden, um Benachrichtigungen über Ereignisse zu empfangen. Die Datenebene ist der primäre Client für Indexerereignisse und entscheidet, was mit Ereignissen auf der Benutzeroberfläche der Elementansicht geschehen soll. Weitere Informationen finden Sie unter [Indizieren von Priorisierungs- und Rowsetereignissen in Windows 7.](indexing-prioritization-and-rowset-events.md)

Im Gegensatz dazu weisen abfragebasierte Sichten in Windows Vista keine zugeordneten Ereignisse auf, mit Ausnahme des Shellcaches für Dateieigenschaftenbearbeitungen. Wenn Sie eine Suche ausführen, sind die zurückgegebenen Ergebnisse statisch. Wenn Ihrem System also ein anderes Dokument hinzugefügt wird, das ihrem Suchbegriff entspricht, wird Ihre Ansicht nicht aktualisiert, sodass sie die neue Hinzufügung enthält. Dieses Verhalten ist standard für statische webbasierte Ergebnisse. Statische Ergebnisse sind jedoch weniger akzeptabel, wenn Sie versuchen, eine abfragebasierte Ansicht über einen Speicherort bereitzustellen. Benutzer erwarten, dass der Inhalt des Indexers aktuell ist. Weitere Informationen finden Sie unter [Notifying the Index of Changes](-search-3x-wds-notifyingofchanges.md). Eine Referenzdokumentation finden Sie unter [Benachrichtigungsschnittstellen.](-search-notifications-interfaces-entry-page.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Indizieren, Abfragen und Benachrichtigungen in Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Was ist im Index enthalten?](-search-indexing-process-overview.md)
</dt> <dt>

[Indizierungsprozess in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Abfrageprozess in Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Anforderungen an die URL-Formatierung](url-formatting-requirements.md)
</dt> </dl>

 

 
