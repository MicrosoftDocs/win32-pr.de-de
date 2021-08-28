---
description: Die Schnittstellen ISearchCatalogManager und ISearchCatalogManager2 stellen Methoden zum Verwalten eines Suchkatalogs bereit, z. B. das Auslösen einer erneuten Indizierung oder das Festlegen von Time outs.
ms.assetid: 8dad7012-d610-4398-8e86-cd319db8c360
title: Verwenden des Katalog-Managers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deffc748c504b056e9d3f92dc8dcb127b835bec6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472326"
---
# <a name="using-the-catalog-manager"></a>Verwenden des Katalog-Managers

Die Schnittstellen [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) und [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2) stellen Methoden zum Verwalten eines Suchkatalogs bereit, z. B. das Auslösen einer erneuten Indizierung oder das Festlegen von Time outs. Während Windows Search derzeit nur einen Katalog verwendet, wurde diese Schnittstelle so konzipiert, dass Sie mehr Kontrolle über die unabhängige Verwaltung mehrerer Kataloge haben. Die -Schnittstelle verwaltet den Katalog auf folgende Weise:

- Zugriff auf andere Schnittstellen: Abrufen anderer suchbezogener Schnittstellen, die für die Durchforstungsbereich-Manager, Datenänderungsbenachrichtigungen und die [**ISearchQueryHelper-Schnittstelle**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) erforderlich sind.
- Kataloginhalt: Sicherstellen, dass neue Daten indiziert werden und dass andere Anwendungen und Komponenten ordnungsgemäß funktionieren, indem eine erneute Indizierung des gesamten Katalogs oder eines Teils des Katalogs erzwungen oder der gesamte Katalog zurückgesetzt wird.
- Katalogeigenschaften– Festlegen von Eigenschaften, die bestimmen, wie der Katalog Time outs beim Herstellen einer Verbindung mit Protokollhandlern verwaltet und wie diakritische Markierungen in Suchvorgängen behandelt werden.
- Katalogstatus: Abrufen von Informationen zum Katalog, einschließlich Status, Größe und aktuellem Aktivitätsstatus.

Dieses Thema ist wie folgt organisiert:

- [Zugreifen auf verwandte Schnittstellen](#accessing-related-interfaces)
- [Verwalten des Kataloginhalts](#managing-the-catalog-contents)
- [Verwalten des Katalogstatus](#managing-catalog-status)
- [Verwalten von Katalogeigenschaften](#managing-catalog-properties)
- [Ausführen im Modus mit erhöhten Rechten](#running-in-elevated-mode)
- [Zugehörige Themen](#related-topics)

## <a name="accessing-related-interfaces"></a>Zugreifen auf verwandte Schnittstellen

Einige nützliche Schnittstellen in der Windows Search-Plattform erfordern eine Instanz des Katalog-Managers, bevor sie verwendet werden können. Um einen Katalog-Manager für einen angegebenen Katalog zu erstellen, rufen Sie die [**ISearchManager::GetCatalog-Methode**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) auf. Die Methoden des Katalog-Managers können dann verwendet werden, um Schnittstellen zu instanziieren und zurückzugeben, die auf dem angegebenen Katalog basieren.

| Methode                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)                               | Ruft eine Instanz der [**ISearchQueryHelper-Schnittstelle**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) für den aktuellen Katalog ab, damit Sie Abfragen einfach erstellen können.                                                                                                                                                                                                                         |
| [**GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager)                   | Ruft eine Instanz von [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) für diesen Suchkatalog ab, damit Entwickler den Durchforstungsbereich des Windows Search Indexer ändern können.                                                                                                                                                                                    |
| [**GetItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getitemschangedsink)                     | Ruft eine Instanz der [**ISearchItemsChangedSink-Schnittstelle**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) ab, mit der Clientanwendungen den Indexer über Änderungen benachrichtigen, wenn der Client Indizierungsstatusinformationen über das Element zur Unterstützung von vom Anbieter verwalteten Benachrichtigungen erhalten möchte. Weitere Informationen finden Sie unter [Benachrichtigen des Änderungsindexes.](-search-3x-wds-notifyingofchanges.md) |
| [**GetPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getpersistentitemschangedsink) | Ruft eine Instanz von [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)ab, mit der Clientanwendungen den Indexer über Änderungen benachrichtigen, wenn der Client keine Indizierungsstatusinformationen (vom Indexer verwaltete Benachrichtigungen) wünschen. Weitere Informationen finden Sie unter [Benachrichtigen des Änderungsindexes.](-search-3x-wds-notifyingofchanges.md)            |

## <a name="managing-the-catalog-contents"></a>Verwalten des Kataloginhalts

Die Verwaltung des Katalogs umfasst zwei Hauptaufgaben: das erneute Indizieren aller oder einiger URLs im Durchforstungsbereich des Indexers und das Zurücksetzen des gesamten zugrunde liegenden Katalogs. Wenn Sie URLs neu indizieren, verbleiben alte Daten im Katalog, bis sie durch neue Daten ersetzt werden. Wenn Sie den Katalog zurücksetzen, wird der gesamte Katalog neu erstellt, und alle URLs im Durchforstungsbereich werden neu indiziert. Dieser Prozess kann viel Zeit in Anspruch nehmen und sollte nur als letzte Möglichkeit zum Lösen von Problemen wie einem möglicherweise beschädigten Index verwendet werden.

Wenn Sie eine neue Anwendung, einen neuen Protokollhandler oder Filter installieren, sollte die Setupanwendung das Verzeichnis oder den Stamm zum Durchforstungsbereich hinzufügen, um sicherzustellen, dass der Indexer den Speicherort der Daten dieser Anwendung enthält. Wenn die Daten nicht im Katalog angezeigt werden, nachdem der Indexer den Durchforstungsbereich durchforstet hat, sollten Sie zunächst sicherstellen, dass der Speicherort der Daten im Durchforstungsbereich enthalten ist. Sie können es hinzufügen, indem Sie die Benutzeroberfläche für Windows Suchoptionen oder die [Durchforstungsbereich-Manager](-search-3x-wds-extidx-csm.md)verwenden. Wenn sich der Speicherort im Durchforstungsbereich befindet, können Sie manuell eine erneute Indizierung aller URLs im Durchforstungsbereich des Indexers oder einer Teilmenge erzwingen, indem Sie die folgenden Methoden der [**ISearchCatalogManager-Schnittstelle**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) verwenden.

| Methode zur erneuten Indizierung                                                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchCatalogManager::Reindex**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindex)                                                                                                                                                   | Indiziert alle URLs im Katalog neu. Die alten Informationen bleiben so lange erhalten, bis sie durch neue Informationen ersetzt werden.                                                                                                                                                         |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)<br/> [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)<br/> | Indiziert URLs neu, die dem Muster entsprechen oder bei einem bestimmten Stamm beginnen (z. B. file:///C: \\ Ordnername \\ Unterordnername \\ ). Dies ist nützlich, um alles in einem bestimmten Verzeichnis oder mit einer bestimmten Erweiterung wie bei der Installation einer Anwendung erneut zu überlisten. |
| [**PrioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls)                                                                                                                                           | Weist den Indexer an, Indizierungselemente mit URLs, die einem angegebenen Muster entsprechen, gegenüber der Durchführung anderer Indizierungsaufgaben zu priorisieren.                                                                                                                                    |

**Zurücksetzen des Indexes.** Sie können den gesamten Index mit einem Aufruf von [**ISearchCatalogManager::Reset**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reset)zurücksetzen. Dadurch wird der zugrunde liegende Katalog zurückgesetzt, indem die Datenbanken neu erstellt und ein vollständiger Index aller URLs im Durchforstungsbereich ausgeführt wird. Dieser Prozess kann viel Zeit in Anspruch nehmen und sollte nur als letzte Möglichkeit zum Lösen von Problemen wie einem möglicherweise beschädigten Index verwendet werden.

> [!IMPORTANT]
> Aufgrund der Verlangsamung der Indizierung, die diese Methoden verursachen können, sollten sie sorgfältig verwendet werden, wenn Sie versuchen, Indizierungs- oder Katalogprobleme zu identifizieren. Stellen Sie zunächst sicher, dass ihre Suchstamm- und Gültigkeitsbereichsregeln im Durchforstungsbereich-Manager hinzugefügt werden, und stellen Sie dann sicher, dass das FANCI-Bit (File Attribute Not Content Indexed) für Dateien und Ordner ordnungsgemäß festgelegt ist. Wenn Sie bestätigt haben, dass diese korrekt sind, versuchen Sie zuerst ReindexSearchRoot und zuletzt neu zu indizieren. Wenn keines dieser Vorgänge funktioniert, versuchen Sie es als letzte Möglichkeit mit Zurücksetzen.

Weitere Informationen finden Sie unter [Notifying the Index of Changes (Benachrichtigen des Index von Änderungen)](-search-3x-wds-notifyingofchanges.md)und [Querying the Index with ISearchQueryHelper (Abfragen des Index mit ISearchQueryHelper).](-search-3x-wds-qryidx-searchqueryhelper.md)

## <a name="managing-catalog-status"></a>Verwalten des Katalogstatus

Der Katalog-Manager kann verwendet werden, um den Status des Katalogs für Anwendungen abzurufen, die anpassen möchten, wie der Katalog verwaltet wird (z. B. eine benutzerdefinierte Überwachungsanwendung "Katalogstatus"). Für die meisten suchbezogenen Entwicklungsszenarien ist der Katalog-Manager jedoch in der Regel nicht erforderlich. Gängige Verwendungsmöglichkeiten wären für eine Überwachungsanwendung "Katalogstatus" oder eine anwendung im Systemsteuerung Format.

In der folgenden Tabelle werden die Methoden von ISearchCatalogManager beschrieben, die zum Verwalten des Katalogstatus verwendet werden.


| Methode | BESCHREIBUNG | 
|--------|-------------|
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-urlbeingindexed"><strong>URLBeingIndexed</strong></a> | Ruft die URL ab, die derzeit indiziert wird. Diese Methode wäre nützlich, wenn Sie versuchen, zu ermitteln, ob der Indexer für ein Element "hängen geblieben" war. | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitems"><strong>NumberOfItems</strong></a> | Ruft die Anzahl der Elemente im Katalog ab. | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitemstoindex"><strong>NumberOfItemsToIndex</strong></a> | Ruft die folgenden Informationen zu zu indizierten Elementen ab:<ul><li>plIncrementalCount: Die Anzahl der Elemente, die im nächsten inkrementellen Index indiziert werden sollen</li><li>plNotificationQueue: die Anzahl der Elemente in der Benachrichtigungswarteschlange. Diese Informationen sind für eine Benachrichtigungsanwendung nützlich, die überprüfen muss, ob der Indexer die Benachrichtigungen empfängt, die die Anwendung sendet.</li><li>plHighPriorityQueue: Die Anzahl der Elemente in der Warteschlange mit hoher Priorität. Elemente in plHighPriorityQueue werden zuerst indiziert.</li></ul> | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcatalogstatus"><strong>GetCatalogStatus</strong></a> | Ruft den Status des Katalogs ab und gibt einen Enumerationswert zurück, der den aktuellen Status angibt. Folgende Katalogzustände sind möglich:<ul><li>Leerlauf: Es ist keine Indizierung erforderlich.</li><li>Angehalten: Die Indizierung wird angehalten (z. B. aufgrund einer geringen Akkukapazität oder einer hohen CPU-Auslastung).</li><li>Wiederherstellung: Die Indizierung wird wiederhergestellt.</li><li>Vollständige Durchforstung: Der Indexer führt eine vollständige Durchforstung des Durchforstungsbereichs durch.</li><li>Inkrementelle Durchforstung: Der Indexer führt eine inkrementelle Durchforstung durch.</li><li>Verarbeiten von Benachrichtigungen: Der Indexer verarbeitet Benachrichtigungen.</li><li>Herunterfahren: Der Indexer wird heruntergefahren.</li></ul> | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_name"><strong>get_Name</strong></a> | Ruft den Namen des aktuellen Katalogs ab, der in der <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog"><strong>ISearchManager::GetCatalog-Methode</strong></a> angegeben ist. Derzeit wird systemIndex als einziger Katalog unterstützt. | 


## <a name="managing-catalog-properties"></a>Verwalten von Katalogeigenschaften

Es gibt drei Katalogeigenschaften, die Sie mit dem Katalog-Manager verwalten können:

- **Diakritische Empfindlichkeit.** Diakritische Zeichen sind Akzentzeichen, die Buchstaben hinzugefügt werden, um die Bedeutung oder Aussprache eines Worts zu kennzeichnen. Diese Eigenschaft bestimmt, ob der Katalog anfällig für diakritische Zeichen ist, und ist wichtig, wenn Sie oder Ihre Benutzer Text in mehreren Sprachen suchen und indizieren. Wenn diese Eigenschaft beispielsweise auf **FALSE** festgelegt ist, würde der Katalog "resume" und "resumé" so behandeln, als wären sie dasselbe Wort.
- **Verbindungstimeouts.** Diese Eigenschaft stellt die Zeitspanne dar, die auf eine Verbindungsantwort von einem Server oder Datenspeicher gewartet werden soll, wie in einer [**TIMEOUT \_ INFO-Struktur**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) dargestellt. Sie können diese Eigenschaft verwenden, um Windows Search zu optimieren.
- **Datentimeouts** Diese Eigenschaft stellt die Zeitspanne dar, die auf eine Datentransaktion zwischen dem Indexer und einem Protokollhandler oder -filter gewartet werden soll, wie in einer [**TIMEOUT \_ INFO-Struktur**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) dargestellt. Wenn diese Zeit verstrichen ist, wird der Prozess aus dem Filterdaemon beendet, um Deadlocks und andere Ressourcenprobleme zu verhindern.

Die letzten beiden Eigenschaften sind in erster Linie für die zukünftige Verwendung vorgesehen. Jede dieser Eigenschaften verfügt über `get` die Methoden und `put` .

| Methode                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_diacriticsensitivity) /<br/> [**put \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_diacriticsensitivity)<br/> | TRUE, wenn der Katalog Wörter mit diakritischen Zeichen unterscheiden soll. **FALSE,** wenn der Katalog diakritische Zeichen ignorieren soll. Zum Ändern dieser Eigenschaft muss der Index neu erstellt werden, da die Schlüssel des Indexes möglicherweise ungültig werden.                       |
| [**get \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_connecttimeout) /<br/> [**\_put ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_connecttimeout)<br/>                         | Die Zeit in Sekunden, die der Indexer auf eine Verbindungsantwort von einem Server oder Datenspeicher warten soll. Wenn Sie diese Einstellung zu hoch festlegen, kann dies zu Verzögerungen führen, wenn viele Standorte nicht reagieren. Wenn sie zu niedrig festgelegt wird, kann dies dazu führen, dass einige Websites nicht durchforstet werden. |
| [**get \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_datatimeout) /<br/> [**put \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_datatimeout)<br/>                                     | Die Zeit in Sekunden, die der Indexer auf eine Datentransaktion warten soll.                                                                                                                                                                      |

## <a name="running-in-elevated-mode"></a>Ausführen im Modus mit erhöhten Rechten

Für alle Methodenaufrufe, die SystemIndex aktualisieren, muss Ihre Anwendung mit erhöhten Rechten ausgeführt werden. Andernfalls tritt bei Ihrer Anwendung ein Fehler vom Art "Zugriff verweigert" auf.

## <a name="related-topics"></a>Zugehörige Themen


[Verwalten des Indexes](-search-3x-wds-mngidx-overview.md)

[Schnittstellen zum Verwalten des Indexes](interfaces-for-managing-the-index.md)

[Verwenden des Such-Managers](-search-3x-wds-mngidx-searchmanager.md)

[Verwenden der Durchforstungsbereich-Manager](-search-3x-wds-extidx-csm.md)
