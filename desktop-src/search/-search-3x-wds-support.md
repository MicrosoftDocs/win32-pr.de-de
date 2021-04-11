---
description: .
ms.assetid: 378e346b-2067-484f-85e9-76673a35550b
title: Benachrichtigungs Prozess in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7dd37979eab7ef32a5a8917ba6a3589e976105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128585"
---
# <a name="notifications-process-in-windows-search"></a>Benachrichtigungs Prozess in Windows Search

Dieses Thema ist wie folgt organisiert:

-   [Übersicht über den Benachrichtigungs Prozess](#overview-of-the-notifications-process)
-   [Crawls](#crawls)
-   [Von Indexer verwaltete Benachrichtigungen](#indexer-managed-notifications)
-   [Vom Anbieter verwaltete Benachrichtigungen](#provider-managed-notifications)
-   [Benachrichtigungen zu Rowsets](#notifications-on-rowsets)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-the-notifications-process"></a>Übersicht über den Benachrichtigungs Prozess

Es gibt drei Ansätze, mit denen Daten aus dem Datenspeicher indiziert werden können:

-   Crawls
-   Von Indexer verwaltete Benachrichtigungen
-   Vom Anbieter verwaltete Benachrichtigungen

Die Vorzüge der einzelnen Verfahren werden in den folgenden Abschnitten beschrieben.

## <a name="crawls"></a>Crawls

Benachrichtigungs aktivierte Quellen führen beim Start eine inkrementelle durch Forstung aus und verwenden dann Benachrichtigungen oder einen expliziten Befehl, um erneut zu durchforsten. Dies erfolgt automatisch unter Windows Vista und höher. Bei Betriebssystemen vor Windows Vista müssen Sie in der [Taskplaner](../taskschd/task-scheduler-start-page.md) ein geplantes Ereignis einrichten, das Ihren Code aufruft, um eine durch Forstung für Ihre Startseite (n) zu initiieren. Sie müssen keine Form von Benachrichtigungen implementieren. Als Hintergrundprozess durchläuft der Indexer seinen Crawl Bereich, sucht nach Änderungen und aktualisiert den Katalog. Diese Option wird in fast allen Situationen empfohlen.

## <a name="indexer-managed-notifications"></a>Indexer-Managed Benachrichtigungen

Bei von Indexern verwalteten Benachrichtigungen implementieren Sie eine Benachrichtigungs Strategie, die den Indexer benachrichtigt, wenn sich Daten im Datenspeicher geändert haben, und der Indexer verwaltet die Nachverfolgung der Benachrichtigungen und die Indizierung der Daten. In dieser Situation überwacht die Komponente (die wir als Benachrichtigungs Anbieter bezeichnen) den Datenspeicher, sammelt Informationen zu Änderungen im Speicher und benachrichtigt den Indexer dann regelmäßig mit einer Liste von Elementen, die indiziert werden müssen. Der Indexer ist für das Wiederherstellen und Auflösen von Benachrichtigungen im Falle eines Fehlers verantwortlich. Diese Option, die Sie als die Strategie "senden und vergessen" vorstellen können, verringert die Häufigkeit der Indexer-Crawls.

## <a name="provider-managed-notifications"></a>Provider-Managed Benachrichtigungen

Bei vom Anbieter verwalteten Benachrichtigungen implementieren Sie eine Benachrichtigungs Strategie, die dem zweiten Ansatz ähnelt, mit dem Unterschied, dass Ihr Benachrichtigungs Anbieter Benachrichtigungen nachverfolgen muss und für das Wiederherstellen und Auflösen von Benachrichtigungen im Falle eines Fehlers zuständig ist. In diesem Fall überwacht Ihr Benachrichtigungs Anbieter den Datenspeicher, sammelt und verwaltet Informationen zu Änderungen im Speicher, benachrichtigt den Indexer regelmäßig mit einer Liste von Elementen, die indiziert werden müssen, empfängt Statusaktualisierungen vom Indexer und sendet Benachrichtigungen bei einem Fehler erneut.

> [!Note]  
> Diese Option wird **nicht empfohlen, es sei denn** , Sie erwarten, dass inkrementelle Durchforstungen Ihres Datenspeicher die Leistung erheblich beeinträchtigen, und Sie benötigen eine differenzierte Kontrolle über den Indizierungs Status oder einen Einblick in diesen

 

## <a name="notifications-on-rowsets"></a>Benachrichtigungen zu Rowsets

In Windows 7 und höher ermöglicht das Indizieren von Ereignissen das Empfangen von Benachrichtigungen über die Rowsets. Anbieter, die Indizierungs Ereignisse verwenden, können Ihre Rowsets auf eine Weise verwalten, die dem Verhalten tatsächlicher Dateisystem Speicherorte ähnelt. Bibliotheken und Suchvorgänge sind die wichtigsten Beispiele für nicht-Dateisystem-Speicherorte in Windows 7. Indexer-Ereignisse werden in Bibliotheks Ansichten als Benachrichtigungen zu Datei Ordner Sichten angezeigt. Die [**irowantevents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) -Schnittstelle muss implementiert werden, um Benachrichtigungen über Ereignisse zu empfangen. Die Datenschicht ist der primäre Client von Indexer und entscheidet, was mit Ereignissen in der Benutzeroberfläche der Elemente angezeigt werden soll. Weitere Informationen finden Sie unter [Indizieren von Priorisierung und rowsetereignissen in Windows 7](indexing-prioritization-and-rowset-events.md).

Im Gegensatz dazu haben in Windows Vista Abfrage basierte Sichten keine zugeordneten Ereignisse, außer dem shellcache für die Bearbeitung von Dateieigenschaften. Wenn Sie eine Suche durchführen, sind die zurückgegebenen Ergebnisse statisch. Wenn dem System ein anderes Dokument hinzugefügt wird, das mit dem Suchbegriff übereinstimmt, wird die Ansicht nicht so aktualisiert, dass Sie die neue Addition enthält. Dieses Verhalten ist bei statischen webbasierten Ergebnissen standardmäßig. Statische Ergebnisse sind jedoch weniger akzeptabel, wenn Sie versuchen, eine Abfrage basierte Sicht über einen Speicherort bereitzustellen. Benutzer erwarten, dass der Inhalt des Indexers aktuell ist. Weitere Informationen finden Sie unter [Benachrichtigen des Index von Änderungen](-search-3x-wds-notifyingofchanges.md). Die Referenz Dokumentation finden Sie unter [Benachrichtigungs Schnittstellen](-search-notifications-interfaces-entry-page.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Indizierung, Abfragen und Benachrichtigungen in Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Was ist im Index enthalten?](-search-indexing-process-overview.md)
</dt> <dt>

[Indizierungsprozess in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Abfrageprozess in Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[URL-Formatierungs Anforderungen](url-formatting-requirements.md)
</dt> </dl>

 

 
