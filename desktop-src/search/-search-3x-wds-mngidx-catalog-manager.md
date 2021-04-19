---
description: Die isearchcatalogmanager-und ISearchCatalogManager2-Schnittstellen bieten Methoden zum Verwalten eines Such Katalogs, z. b. durch erneute Indizierung oder das Festlegen von Timeouts.
ms.assetid: 8dad7012-d610-4398-8e86-cd319db8c360
title: Verwenden des Katalog-Managers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1295cc9cc76fb334b4687b876fa1959a22e33235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345672"
---
# <a name="using-the-catalog-manager"></a>Verwenden des Katalog-Managers

Die [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) -und [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2) -Schnittstellen bieten Methoden zum Verwalten eines Such Katalogs, z. b. durch erneute Indizierung oder das Festlegen von Timeouts. Obwohl Windows Search zurzeit nur einen Katalog verwendet, wurde diese Schnittstelle entworfen, um Ihnen mehr Kontrolle über die unabhängige Verwaltung mehrerer Kataloge zu verschaffen. Die-Schnittstelle verwaltet den Katalog wie folgt:

- Zugriff auf andere Schnittstellen – abrufen anderer Such bezogener Schnittstellen, die vom Crawl Bereichs-Manager, Daten Änderungs Benachrichtigungen und der [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle benötigt werden.
- Katalog Inhalt – stellen Sie sicher, dass neue Daten indiziert werden und andere Anwendungen und Komponenten ordnungsgemäß funktionieren, indem Sie eine Neuindizierung des gesamten Katalogs oder eines Teils des Katalogs erzwingen oder den gesamten Katalog zurücksetzen.
- Katalog Eigenschaften – festlegen von Eigenschaften, die bestimmen, wie der Katalog Timeouts verwaltet, wenn eine Verbindung mit Protokoll Handlern hergestellt wird und wie Diakritische Markierungen in Such Vorgängen behandelt werden.
- Katalog Status – erhalten Sie Informationen zum Katalog, einschließlich Status, Größe und aktueller Aktivitätsstatus.

Dieses Thema ist wie folgt organisiert:

- [Zugreifen auf verwandte Schnittstellen](#accessing-related-interfaces)
- [Verwalten des Katalog Inhalts](#managing-the-catalog-contents)
- [Verwalten des Katalog Status](#managing-catalog-status)
- [Verwalten von Katalog Eigenschaften](#managing-catalog-properties)
- [Ausführen im erweiterten Modus](#running-in-elevated-mode)
- [Zugehörige Themen](#related-topics)

## <a name="accessing-related-interfaces"></a>Zugreifen auf verwandte Schnittstellen

Einige nützliche Schnittstellen in der Windows Search-Plattform erfordern eine Instanz des Katalog-Managers, bevor Sie verwendet werden können. Um einen Katalog-Manager für einen angegebenen Katalog zu erstellen, rufen Sie die [**isearchmanager:: getCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) -Methode auf. Die Methoden des Katalog-Managers können dann verwendet werden, um Schnittstellen zu instanziieren und zurückzugeben, die auf dem angegebenen Katalog basieren.

| Methode                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getqueryhelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)                               | Ruft eine Instanz der [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle für den aktuellen Katalog ab, um die einfache Erstellung von Abfragen zu ermöglichen.                                                                                                                                                                                                                         |
| [**Getcrawlscopemanager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager)                   | Ruft eine Instanz des [**isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) -Elements für diesen Such Katalog ab, damit Entwickler den Crawl Bereich des Windows Search-Indexers ändern können.                                                                                                                                                                                    |
| [**Getitemschangedsink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getitemschangedsink)                     | Ruft eine Instanz der [**isearchitemschangedsink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) -Schnittstelle ab, die von Client Anwendungen verwendet wird, um den Indexer von Änderungen zu benachrichtigen, wenn der Client das Indizieren von Statusinformationen zum Element anfordert, um vom Anbieter verwaltete Benachrichtigungen zu unterstützen. Weitere Informationen finden Sie [unter Benachrichtigen des Index von Änderungen](-search-3x-wds-notifyingofchanges.md) . |
| [**Getpersistentitemschangedsink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getpersistentitemschangedsink) | Ruft eine Instanz von [**isearchpersistentitemschangedsink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)ab, die von Client Anwendungen verwendet wird, um den Indexer von Änderungen zu benachrichtigen, wenn der Client keine Indizierungs Statusinformationen (von Indexer verwaltete Benachrichtigungen) abrufen möchte. Weitere Informationen finden Sie [unter Benachrichtigen des Index von Änderungen](-search-3x-wds-notifyingofchanges.md) .            |

## <a name="managing-the-catalog-contents"></a>Verwalten des Katalog Inhalts

Die Verwaltung des Katalogs besteht aus zwei Hauptaufgaben: das erneute indizieren aller oder einiger URLs im Crawl Bereich des Indexers und das Zurücksetzen des gesamten zugrunde liegenden Katalogs. Wenn Sie URLs neu indizieren, verbleiben alte Daten im Katalog bis oder, wenn Sie nicht durch neue Daten ersetzt werden. Wenn Sie den Katalog zurücksetzen, wird der gesamte Katalog neu erstellt, und alle URLs im Crawl Bereich werden neu indiziert. Dieser Vorgang kann viel Zeit in Anspruch nehmen und sollte nur als letzte Möglichkeit zum Beheben von Problemen, wie z. b. einem möglicherweise beschädigten Index, verwendet werden.

Wenn Sie eine neue Anwendung, einen Protokollhandler oder einen Filter installieren, sollte die Setup Anwendung das zugehörige Verzeichnis oder den Stamm dem Crawl Bereich hinzufügen, um sicherzustellen, dass der Indexer den Speicherort der Daten der Anwendung enthält. Wenn die Daten nicht im Katalog angezeigt werden, nachdem der Indexer den Crawl Bereich durchlaufen hat, sollten Sie zunächst sicherstellen, dass der Speicherort der Daten im Crawl Bereich enthalten ist. Sie können ihn über die Benutzeroberfläche für Windows-Suchoptionen oder den [Crawl Scope-Manager](-search-3x-wds-extidx-csm.md)hinzufügen. Wenn sich der Speicherort im Crawl Bereich befindet, können Sie mithilfe der folgenden Methoden der [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) -Schnittstelle eine erneute Indizierung aller URLs im Durchforstungs Bereich des Indexers oder eine Teilmenge manuell erzwingen.

| Neuindizierungs Methode                                                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Isearchcatalogmanager:: REINDEX**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindex)                                                                                                                                                   | Indiziert alle URLs im Katalog neu. Die alten Informationen bleiben bestehen, bis Sie durch neue Informationen ersetzt werden.                                                                                                                                                         |
| [**Isearchcatalogmanager::.**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)<br/> [**Isearchcatalogmanager:: in xsearchroot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)<br/> | Neuindizierung von URLs, die dem Muster entsprechen, oder starten an einem bestimmten Stamm (z. b. file:///C: \\ FolderName \\ subfoldername \\ ). Dies ist nützlich, um alle Elemente in einem bestimmten Verzeichnis oder mit einer bestimmten Erweiterung zu wiederholen, wie bei der Installation einer Anwendung. |
| [**Priorizematchingurls**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls)                                                                                                                                           | Weist den Indexer an, die Indizierungs Elemente mit URLs zu priorisieren, die einem angegebenen Muster entsprechen, wenn andere Indizierungs Aufgaben abgeschlossen werden.                                                                                                                                    |

**Zurücksetzen des Indexes** Sie können den gesamten Index mit einem [**isearchcatalogmanager:: Reset**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reset)-Rückruf zurücksetzen. Dadurch wird der zugrunde liegende Katalog zurückgesetzt, indem die Datenbanken neu erstellt und ein vollständiger Index aller URLs im Crawl Bereich durchgeführt wird. Dieser Vorgang kann viel Zeit in Anspruch nehmen und sollte nur als letzte Möglichkeit zum Beheben von Problemen, wie z. b. einem möglicherweise beschädigten Index, verwendet werden.

> [!IMPORTANT]
> Aufgrund der Verlangsamung der Indizierung, die diese Methoden verursachen können, sollten Sie sorgfältig verwendet werden, wenn Sie versuchen, Indizierungs-oder Katalog Probleme zu identifizieren. Stellen Sie zunächst sicher, dass die Such Stämme und Bereichs Regeln im Crawl Scope-Manager hinzugefügt werden, und stellen Sie sicher, dass das Fanci-Bit (Datei Attribut nicht für Inhalt indiziert) ordnungsgemäß für Dateien und Ordner festgelegt ist. Wenn Sie sich vergewissert haben, dass diese korrekt sind, versuchen Sie es zuerst mit der Datei "". Wenn keines dieser Aufgaben funktioniert, versuchen Sie, die zurück Setzung als letztes Mittel auszuführen.

Weitere Informationen finden Sie unter [Benachrichtigen des Index von Änderungen](-search-3x-wds-notifyingofchanges.md)und [Abfragen des Indexes mit isearchqueryhelper](-search-3x-wds-qryidx-searchqueryhelper.md) .

## <a name="managing-catalog-status"></a>Verwalten des Katalog Status

Der Katalog-Manager kann verwendet werden, um den Status des Katalogs für Anwendungen zu erhalten, die die Verwaltung des Katalogs anpassen möchten (z. b. eine benutzerdefinierte "Katalog Status"-Überwachungsanwendung). Der Katalog-Manager ist jedoch in der Regel für die meisten Such bezogenen Entwicklungsszenarien nicht erforderlich. Häufig verwendete Verwendungsmöglichkeiten für eine Überwachungsanwendung vom Typ "Katalog Status" oder eine Anwendung im Bereich "Systemsteuerung".

In der folgenden Tabelle werden die Methoden von isearchcatalogmanager beschrieben, die zum Verwalten des Katalog Status verwendet werden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Methode</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-urlbeingindexed"><strong>Urlbeingindebug</strong></a></td>
<td>Ruft die URL ab, die gerade indiziert wird. Diese Methode ist hilfreich, wenn Sie feststellen möchten, ob der Indexer &quot; &quot; an einem Element hängen bleibt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitems"><strong>Numotems</strong></a></td>
<td>Ruft die Anzahl der Elemente im Katalog ab.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitemstoindex"><strong>"Numoftemstoindex"</strong></a></td>
<td>Ruft die folgenden Informationen zu den zu indizierenden Elementen ab:
<ul>
<li>plincrementalcount: die Anzahl der Elemente, die im nächsten inkrementellen Index indiziert werden sollen.</li>
<li>plnotificationqueue: die Anzahl der Elemente in der Benachrichtigungs Warteschlange. Diese Informationen sind nützlich für eine Benachrichtigungs Anwendung, die überprüfen musste, ob der Indexer die von der Anwendung gesendeten Benachrichtigungen empfängt.</li>
<li>plhighpriorityqueue: die Anzahl der Elemente in der Warteschlange mit hoher Priorität. Elemente in plhighpriorityqueue werden zuerst indiziert.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcatalogstatus"><strong>Getcatalogstatus</strong></a></td>
<td>Ruft den Status des Katalogs ab und gibt einen Enumerationswert zurück, der den aktuellen Status erhält. Folgende Katalog Zustände sind möglich:
<ul>
<li>Im Leerlauf: Es ist keine Indizierung erforderlich.</li>
<li>Angehalten: die Indizierung wurde angehalten (z. b. aufgrund von geringer Akku Auslastung oder hoher CPU-Auslastung).</li>
<li>Wiederherstellung: die Indizierung wird wieder hergestellt.</li>
<li>Vollständige durch Forstung: der Indexer führt eine vollständige durch Forstung des Crawl Bereichs aus.</li>
<li>Inkrementelles Crawlen: der Indexer führt eine inkrementelle</li>
<li>Verarbeitungs Benachrichtigungen: der Indexer verarbeitet Benachrichtigungen.</li>
<li>Herunterfahren: Indexer wird heruntergefahren.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_name"><strong>get_Name</strong></a></td>
<td>Ruft den Namen des aktuellen Katalogs ab, der in der <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog"><strong>isearchmanager:: getCatalog</strong></a> -Methode angegeben wird. Derzeit ist der einzige unterstützte Katalog der Systemindex.</td>
</tr>
</tbody>
</table>

## <a name="managing-catalog-properties"></a>Verwalten von Katalog Eigenschaften

Es gibt drei Katalog Eigenschaften, die Sie mit dem Katalog-Manager verwalten können:

- **Diakritische Sensitivität.** Diakritik sind der Buchstaben hinzugefügte Akzentzeichen, um die Bedeutung oder Aussprache eines Worts anzugeben. Diese Eigenschaft bestimmt, ob der Katalog von Diakritik abhängig ist, und ist wichtig, wenn Sie oder Ihre Benutzer Text in mehreren Sprachen suchen und indizieren. Wenn diese Eigenschaft z. b. auf " **false**" festgelegt ist, würde der Katalog "Resume" und "Resumé" so behandeln, als ob es sich um dasselbe Wort handelt.
- **Verbindungs Timeouts.** Diese Eigenschaft stellt die Zeitspanne dar, die auf eine Verbindungs Antwort von einem Server oder Datenspeicher gewartet werden soll, wie in einer [**Timeout \_ Info**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) -Struktur dargestellt. Mit dieser Eigenschaft können Sie Windows Search fein optimieren.
- **Daten Timeouts** Diese Eigenschaft stellt die Zeitspanne dar, die auf eine Daten Transaktion zwischen dem Indexer und einem Protokollhandler oder Filter gewartet werden soll, wie in einer [**Timeout \_ Info**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) -Struktur dargestellt. Wenn diese Zeit abgelaufen ist, wird der Prozess vom Filterdaemon beendet, um Deadlocks und andere Ressourcenprobleme zu vermeiden.

Die letzten beiden Eigenschaften sind hauptsächlich für die zukünftige Verwendung vorgesehen. Jede dieser Eigenschaften hat die `get` -Methode und die- `put` Methode.

| Methode                                                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_diakriticsensitivität erhalten**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_diacriticsensitivity) /<br/> [**\_diakriticsensitivität ablegen**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_diacriticsensitivity)<br/> | TRUE, wenn der Katalog Wörter mit Diakritik unterscheiden soll. **False** , wenn der Katalog Diakritik ignorieren soll. Zum Ändern dieser Eigenschaft muss der Index neu erstellt werden, da die Schlüssel des Indexes möglicherweise ungültig werden.                       |
| [**\_ConnectTimeout erhalten**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_connecttimeout) /<br/> [**\_ConnectTimeout platzieren**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_connecttimeout)<br/>                         | Die Zeit (in Sekunden), die der Indexer auf eine Verbindungs Antwort von einem Server oder Datenspeicher warten soll. Wenn diese Einstellung zu hoch ist, kann dies zu Verzögerungen führen, wenn viele Sites nicht mehr reagiert. Eine zu geringe Einstellung kann dazu führen, dass einige Websites nicht durchsucht werden. |
| [**\_DataTimeout erhalten**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_datatimeout) /<br/> [**\_DataTimeout einfügen**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_datatimeout)<br/>                                     | Die Zeit (in Sekunden), die der Indexer auf eine Daten Transaktion warten soll.                                                                                                                                                                      |

## <a name="running-in-elevated-mode"></a>Ausführen im erweiterten Modus

Alle Methodenaufrufe, die den SystemIndex aktualisieren, erfordern, dass Ihre Anwendung mit erhöhten Rechten ausgeführt wird. Andernfalls schlägt die Anwendung mit dem Fehler "Zugriff verweigert" fehl.

## <a name="related-topics"></a>Zugehörige Themen


[Verwalten des Indexes](-search-3x-wds-mngidx-overview.md)

[Schnittstellen für die Verwaltung des Indexes](interfaces-for-managing-the-index.md)

[Verwenden des Such-Managers](-search-3x-wds-mngidx-searchmanager.md)

[Verwenden des Crawl Scope-Managers](-search-3x-wds-extidx-csm.md)
