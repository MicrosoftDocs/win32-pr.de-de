---
description: In diesem Thema werden die drei Phasen des Indizierungs Prozesses und die jeweiligen primären Komponenten beschrieben, die zeitliche Steuerung der Indizierungs Aktivität erläutert und einige Hinweise für Entwickler von Drittanbietern bereitgestellt, die Ihre Datenspeicher oder Dateiformate indizieren möchten.
ms.assetid: cfba12eb-4123-4b57-8311-d4fc8f9f514e
title: Indizierungsprozess in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87867d5925cd53b237092435bbc9d16428418b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750401"
---
# <a name="indexing-process-in-windows-search"></a>Indizierungsprozess in Windows Search

In diesem Thema werden die drei Phasen des Indizierungs Prozesses und die jeweiligen primären Komponenten beschrieben, die zeitliche Steuerung der Indizierungs Aktivität erläutert und einige Hinweise für Entwickler von Drittanbietern bereitgestellt, die Ihre Datenspeicher oder Dateiformate indizieren möchten.

Dieses Thema ist wie folgt organisiert:

- [Übersicht](#overview)
- [Phase 1: Warteschlangen-URLs für die Indizierung](#stage-1-queuing-urls-for-indexing)
- [Phase 2: Crawlen von URLs](#stage-2-crawling-urls)
- [Phase 3: Aktualisieren des Indexes](#stage-3-updating-the-index)
- [Planung der Indizierung](#how-indexing-is-scheduled)
- [Hinweise für Ausführende](#notes-to-implementers)
- [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Windows Search unterstützt die Indizierung von Eigenschaften und Inhalten aus Dateien mit unterschiedlichen Dateiformaten, z. b. doc-oder JPEG-Formaten und Daten speichern, wie z. b. das Dateisystem oder Windows Outlook-Postfächer. Es gibt zwei Arten von Indizes: Wert Indizes, die das Filtern und Sortieren nach dem gesamten Wert einer Eigenschaft und umgekehrten Indizes ermöglichen, die Wörter innerhalb von Texteigenschaften oder Inhalt indizieren. Wenn Sie ein benutzerdefiniertes Dateiformat oder einen Datenspeicher haben, müssen Sie verstehen, wie Indizes von Windows durchsucht werden, damit die Elemente korrekt indiziert werden.

Der Indizierungsprozess erfolgt in drei Phasen, die von einer Windows-Such Komponente mit dem Namen Gatherer gesteuert werden. In der ersten Phase fügt der Gatherer Warteschlangen URLs hinzu. Die URLs identifizieren Elemente, die indiziert werden sollen, und die Warteschlangen sind nur priorisierte Listen mit URLs. In der zweiten Phase koordiniert der Gatherer andere Windows-Such Komponenten und Komponenten von Drittanbietern, um auf die Elemente zuzugreifen und Daten zu Ihnen zu erfassen. Schließlich werden in der dritten Phase die gesammelten Daten dem Index hinzugefügt.

Das folgende Diagramm zeigt die Hauptkomponenten und den Datenfluss durch den Indizierungsprozess. Beim Sammeln von Daten für den Index sind eine Reihe von Komponenten beteiligt. Einige davon sind Teil der Windows-Suche, und einige Anwendungen stammen von Drittanbieter Anwendungen. Wenn Sie einen benutzerdefinierten Datenspeicher oder ein benutzerdefiniertes Dateiformat haben, basiert Windows Search auf dem Protokollhandler und filtert den Zugriff auf URLs und gibt Eigenschaften für die Indizierung aus. Windows Search-Komponenten sind in blau dargestellt, und Komponenten von Drittanbietern sind grün dargestellt.

![Diagramm, das die Interaktion zwischen Komponenten während des Indizierungs Prozesses anzeigt](images/indexingcompoverview.jpg)

## <a name="stage-1-queuing-urls-for-indexing"></a>Phase 1: Warteschlangen-URLs für die Indizierung

In der ersten Phase der Indizierung sammelt der Gatherer Informationen zu Updates für Datenspeicher, vergleicht diese Informationen mit dem bekannten Crawl Bereich und erstellt dann eine Warteschlangen-URL, die zum Sammeln von Daten für den Index durchlaufen werden soll. Für Quellen, die nicht auf Benachrichtigungen basieren (z. b. FAT-Laufwerke), initiiert der Gatherer regelmäßig eine vollständige durch Forstung des Durchforstungs Bereichs, sodass die Daten im Index aktuell aufbewahrt werden. Für Quellen wie NTFS gibt es nur eine einzige durch Forstung, und alles andere wird von Benachrichtigungen aus dem [Aktualitäts Änderungs Journal](/windows/desktop/FileIO/change-journals)verarbeitet. Es gibt auch keinen Crawl von Microsoft Outlook. Das folgende Diagramm zeigt eine allgemeine Übersicht über den Warteschlangen Prozess für die nicht-Durchforstungs Indizierung.

![Diagramm, das den Abfrageprozess für die nicht-Crawl-Indizierung anzeigt](images/queuingurls.jpg)

Im restlichen Teil dieses Abschnitts wird erläutert, wie die Windows-Suche bestimmt, welche URLs durchlaufen werden, und es werden einige wichtige Begriffe definiert.

**Crawl Bereich**  Der Crawlen Bereich ist ein Satz von URLs, die von Windows Search durchlaufen werden, um Daten zu Elementen zu sammeln, die der Benutzer für schnellere Suchvorgänge indizieren möchte. Bei der Windows-Suche werden dem Crawl Bereich standardmäßig einige URLs hinzugefügt, z. b. Pfade zu den **Dokumenten** und **Bild** Ordnern von Benutzern. Andere URLs können von Anwendungen, Benutzern und Gruppenrichtlinie von Drittanbietern hinzugefügt werden. Und schließlich können sowohl Benutzer als auch Gruppenrichtlinie URLs explizit ausschließen. Windows Search übernimmt alle hinzugefügten URLs und entfernt die ausgeschlossenen URLs, um den Crawl Bereich zu ermitteln. Dies ist der Arbeits Satz von URLs, von denen der Gatherer seine Arbeit startet.

**Gatherer**  Der Gatherer ist eine Windows-Such Komponente, die Informationen über URLs innerhalb des Durchforstungs Bereichs sammelt und eine Warteschlange von URLs erstellt, die der Indexer durchforsten kann. Wenn ein Element im Crawl Bereich hinzugefügt, gelöscht oder aktualisiert wird, wird der Gatherer vom Benachrichtigungs Anbieter des Daten Stores benachrichtigt. Es gibt eine erste durch Forstung, bei der der Gatherer am Stamm des Crawl Bereichs beginnt. Die URL wird an den Protokollhandler und dann an den entsprechenden [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)weitergegeben. Der Filter ist in der Regel eine verzeichnisenumeration, die weitere URLs erzeugt. Benachrichtigungen sind der stetige Zustand. In der Regel verfügt jeder Datenspeicher über einen eigenen Protokollhandler, der diese Benachrichtigungen bereitstellt. Auf dem lokalen Dateisystem fungiert das [Aktualitäts Änderungs Journal](/windows/desktop/FileIO/change-journals) beispielsweise als Benachrichtigungs Anbieter für alle URLs unter dem file://-Protokoll. Ebenso fungiert Microsoft Outlook als Benachrichtigungs Anbieter für alle URLs unter dem MAPI://-Protokoll. Wenn ein Benutzer eine e-Mail empfängt, verschiebt oder löscht, benachrichtigt Outlook den Gatherer über den geänderten Status der e-Mail. Aus diesen Benachrichtigungen erstellt der Gatherer Index Warteschlangen von URLs, die durchsucht werden sollen.

**Warteschlangen indizieren**  Die Indizierungs Warteschlangen sind Listen von URLs, die Elemente identifizieren, die indiziert oder neu indiziert werden müssen. Der Gatherer vergleicht die empfangenen URLs von Benachrichtigungs Anbietern mit den URLs im Crawl Bereich. Jede URL von Benachrichtigungs Anbietern, die innerhalb des Durchforstungs Bereichs liegt, wird einer Warteschlange hinzugefügt, die der Gatherer verwendet, um festzulegen, welche URLs als Nächstes verarbeitet werden.

Es gibt drei Warteschlangen: Benachrichtigungen mit hoher Priorität, normale Benachrichtigungen und regelmäßige Crawls. Die Warteschlange mit hoher Priorität ist für Benachrichtigungen vorgesehen, die sofort verarbeitet werden sollen. Wenn ein Benutzer beispielsweise die Title-Eigenschaft eines Elements in Windows-Explorer ändert, muss die Windows Explorer-Ansicht sofort nach der Änderung aktualisiert werden. Die normale Benachrichtigungs Warteschlange gilt für alle verbleibenden Änderungs Benachrichtigungen. Die Benachrichtigungs Warteschlangen werden vor der Durchforstungs Warteschlange verarbeitet, da geänderte Elemente eher für einen Benutzer von Interesse sind. Der Gatherer greift auf Daten für die URLs in jeder Warteschlange in der First in, First Out (FIFO)-Reihenfolge zu.

Weitere Informationen zur Priorisierung und zu den in Windows 7 eingeführten APIs finden Sie unter [Indizieren von Priorisierung und rowsetereignissen in Windows 7](indexing-prioritization-and-rowset-events.md). Weitere Informationen zur Verwaltung von Crawl Bereichen und Benachrichtigungen finden Sie unter [Bereitstellen von Änderungs Benachrichtigungen](-search-3x-wds-notifyingofchanges.md) und [Verwenden des Crawl Scope-Managers](-search-3x-wds-extidx-csm.md).

## <a name="stage-2-crawling-urls"></a>Phase 2: Crawlen von URLs

In der zweiten Phase der Indizierung durchläuft der Gatherer die Warteschlangen, greift auf Datenspeicher zu und ruft Elementdaten Ströme ab. Zuerst findet der Gatherer den entsprechenden Protokollhandler für jede URL. Anschließend übergibt der Gatherer die URL an den Protokollhandler. Der Protokollhandler greift auf das Element zu und übergibt die Element Metadaten an den Gatherer zurück. Der Gatherer verwendet die Metadaten, um den richtigen Filter zu ermitteln.

Das folgende Diagramm zeigt eine allgemeine Übersicht über den URL-Crawlen-Prozess. Diese Phase umfasst eine beträchtliche Koordination und Kommunikation zwischen Komponenten.

![Diagramm zum Durchsuchen von URLs und zum Zugreifen auf Elemente](images/crawlingqueues.jpg)

Im restlichen Teil dieses Abschnitts wird beschrieben, wie die Windows-Suche auf Elemente für die Indizierung zugreift und die Rollen der beteiligten Komponenten erläutert.

**Gatherer**  In Phase 2, der Crawlen-Phase, verarbeitet der Gatherer die URLs in den Warteschlangen, beginnend mit der Warteschlange mit hoher Priorität. Jede URL wird untersucht, um Ihr Protokoll zu identifizieren. Der Gatherer sucht dann nach dem Protokollhandler, der für dieses Protokoll registriert ist, und instanziiert ihn im Host Prozess des Suchprotokolls.

**Protokoll Host suchen**  Der Such Protokoll Host ist nur ein geachtelter Host Prozess für Protokollhandler. In der Regel erstellt Windows Search zwei solche Host Prozesse, eine, die im System Sicherheitskontext ausgeführt wird, und eine, die im Sicherheitskontext des Benutzers ausgeführt wird. Durch diese Trennung wird sichergestellt, dass Daten, die für einen Benutzer spezifisch sind, niemals im Systemkontext ausgeführt werden.

In Windows Search wird auch der Host Prozess verwendet, um eine Instanz eines Protokoll Handlers von anderen Prozessen oder Anwendungen zu isolieren. Auf diese Weise kann keine externe Anwendung auf diese bestimmte Instanz des Protokoll Handlers zugreifen. wenn der Protokollhandler unerwartet ausfällt, ist nur der Indizierungsprozess betroffen. Da der Host Prozess Code von Drittanbietern (Protokollhandler) ausführt, wird der Prozess von Windows Search in regelmäßigen Abständen wieder verwendet, um die Zeit zu minimieren, mit der bei einem erfolgreichen Angriff Informationen im Prozess ausgenutzt werden müssen. Darüber hinaus wirkt sich der Such Protokoll Host nicht auf das Crawlen von URLs oder die Indizierung von Elementen aus.

**Protokollhandler**  Protokollhandler ermöglichen den Zugriff auf Elemente in einem Datenspeicher mit dem Protokoll des Daten Stores. Der NTFS-Protokollhandler ermöglicht beispielsweise den Zugriff auf Dateien auf einem lokalen Laufwerk mithilfe des file://-Protokolls. Der Protokollhandler weiß, wie Sie den Datenspeicher durchlaufen, neue oder aktualisierte Elemente ermitteln und den Gatherer benachrichtigen. Wenn beim Crawlen begonnen wird, stellt der Protokollhandler dem Gatherer ein [**iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) -Objekt zur Verfügung, das an den zugrunde liegenden Stream des Elements gebunden und Element Metadaten zurückgibt, wie z. b. Sicherheitseinschränkungen und Uhrzeit der letzten Änderung.

> [!NOTE]  
> Protokollhandler sind keine Windows-Such Komponenten. Dabei handelt es sich um Komponenten des spezifischen Protokolls und des Datenspeicher, auf die Sie zugreifen können. Wenn Sie einen benutzerdefinierten Datenspeicher haben, den Sie indizieren möchten, müssen Sie einen Protokollhandler implementieren. Weitere Informationen zu Protokoll Handlern und deren Implementierung finden Sie unter [entwickeln von Protokoll Handlern](-search-3x-wds-phaddins.md).

**Metadaten und Stream**  Mithilfe von Metadaten, die vom [**iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) -Objekt des Protokoll Handlers zurückgegeben werden, identifiziert der Gatherer den richtigen Filter für die URL. Der Gatherer analysiert die Dateinamenerweiterung des Elements und sucht den Filter, der für diese Erweiterung registriert ist. Wenn der Gatherer keinen Filter finden kann, verwendet Windows Search die Metadaten, um einen minimalen Satz von System Eigenschafts Informationen (z. b. System. ItemName) abzuleiten und den Index zu aktualisieren. Wenn der Gatherer den Filter findet, beginnt andernfalls die dritte Phase der Indizierung.

## <a name="stage-3-updating-the-index"></a>Phase 3: Aktualisieren des Indexes

In der dritten Phase der Indizierung instanziiert der Gatherer den richtigen Filter für die URL und initialisiert den Filter mit dem Datenstrom aus dem [**iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) -Objekt. Der Filter greift dann auf das Element zu und gibt den Inhalt für den Index zurück. Wenn Sie ein benutzerdefiniertes Dateiformat haben, basiert Windows Search auf dem Filter, um auf URLs zuzugreifen und Inhalt und Eigenschaften für die Indizierung auszugeben.

Das folgende Diagramm zeigt eine allgemeine Übersicht über den Datenzugriffs Vorgang. Diese Phase umfasst eine beträchtliche Koordination und Kommunikation zwischen Komponenten.

![Diagramm, das die für den Index ausgegebenen Elementdaten anzeigt](images/filteringdata.jpg)

Im restlichen Teil dieses Abschnitts wird beschrieben, wie Windows Search auf Elementdaten für die Indizierung zugreift und die Rollen der beteiligten Komponenten erläutert.

**Gatherer**  Am Anfang dieser Phase besteht die Rolle des gatherers darin, den korrekten Filter für das Element zu instanziieren und den Elementdaten Strom zu übergeben. Am Ende dieser Phase nimmt der Gatherer den Inhalt und die Eigenschaften, die vom Filter-und Eigenschafts Handler ausgegeben werden, und aktualisiert den Index.

**Host Filtern**  Beim Filter Host handelt es sich lediglich um einen Host Prozess für Filter und Eigenschaften Handler, der einem ähnlichen Zweck wie der suchprotokollhost entspricht. Der Host Prozess isoliert Filter und Eigenschaften Handler aus dem Rest des Systems aus den gleichen Sicherheits-und Stabilitätsgründen, die durch Such Protokoll Host Prozesse zum Isolieren von Protokoll Handlern verarbeitet werden. Der Host Prozess wird mit minimalen Rechten ausgeführt (er kann nicht einmal auf das Dateisystem zugreifen) und wird gelegentlich wieder verwendet, um vor Sicherheitsangriffen zu schützen. Windows Search überwacht auch die Ressourcenverwendung, sodass der Host Prozess wieder verwendet wird, wenn ein Filter zu viele Ressourcen verbraucht.

**Filter**  Filter sind wichtige Komponenten im Indizierungsprozess, die Element Informationen für den Gatherer ausgeben. Filter werden nach der Prinzipal Schnittstelle benannt, die in ihrer Implementierung verwendet wird, der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle und werden folglich auch als IFilters bezeichnet. Es gibt zwei Arten von Filtern: eine, die mit einzelnen Elementen wie Dateien interagiert, und eine, die mit Containern wie Ordnern interagiert. Beide stellen Daten für den Index bereit.

Mithilfe von Metadaten, die vom [**iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) -Objekt des Protokoll Handlers zurückgegeben werden, identifiziert der Gatherer den korrekten Filter für eine bestimmte URL und übergibt ihn an den Stream. Der Gatherer identifiziert den richtigen Filter entweder über einen Protokollhandler oder über die Dateinamenerweiterung, den MIME-Typ oder den Klassen Bezeichner (CLSID). Wenn die URL auf einen Container verweist, gibt der Filtereigenschaften für den Container aus und listet die Elemente im Container (untergeordnete URLs) auf. Wenn die URL auf ein Element verweist, gibt der Filter den Text Inhalt zurück, wenn das Lesen von Eigenschaften und komplexer ist als Eigenschaften Handler. Im Allgemeinen wird empfohlen, dass Filterelement Inhalte ausgeben, während Eigenschaften Handler Element Eigenschaften ausgeben. Wenn der Filter jedoch mit älteren Anwendungen funktionieren muss, die keine Eigenschafts Handler erkennen, können Sie den Filter implementieren, um auch Eigenschaften auszugeben.

> [!NOTE]  
> Filter sind keine Windows-Such Komponenten; Dabei handelt es sich um Komponenten, die mit dem jeweiligen Dateiformat oder Container verknüpft sind, auf den Sie zugreifen können. Weitere Informationen zu filtern und zum Implementieren eines für ein benutzerdefiniertes Dateiformat oder einen Container finden Sie unter [bewährte Methoden zum Erstellen von Filter Handlern in Windows Search](-search-3x-wds-extidx-filters.md).

In der folgenden Tabelle werden die Ergebnisse aufgelistet, die der Gatherer bei der Indizierung von einem Filter ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)) und einem Eigenschafts Handler ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) empfängt.

|                            | [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) | [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) |
|----------------------------|------------------------------------|-------------------------------------------------|
| Schreibzugriff zulassen                | Nein                                 | Ja                                             |
| Inhalt und Eigenschaften mischen | Ja                                | Nein                                              |
| Mehrsprachige               | Ja                                | Nein                                              |
| Links ausgeben                 | Ja                                | Nein                                              |
| MIME                       | Ja                                | Nein                                              |
| Text Begrenzungen            | Satz, Absatz, Kapitel       | Keine                                            |
| Client/Server            | Both                               | Client                                          |
| Implementierung             | Komplex                            | Einfach                                          |

**Eigenschaften Handler**  Eigenschafts Handler sind Komponenten, die Eigenschaften für ein bestimmtes Dateiformat lesen und schreiben. Sie greifen auf Elemente zu und geben Eigenschaften für den Gatherer auf die gleiche Weise aus, wie Filter für Inhalte verwenden. Eigenschaften Handler sind einfacher zu implementieren als Filter. Wenn ein textbasiertes Dateiformat sehr einfach ist oder die Dateien sehr klein sind, kann der Eigenschafts Handler sowohl Eigenschaften als auch Inhalt ausgeben.

> [!NOTE]  
> Eigenschaften Handler sind keine Windows-Such Komponenten. Dabei handelt es sich um Komponenten, die mit dem jeweiligen Dateiformat verknüpft sind, auf das Sie zugreifen können. Weitere Informationen zu Eigenschaften Handlern und zur Implementierung eines für ein benutzerdefiniertes Dateiformat finden Sie unter [entwickeln von Eigenschaften Handlern für Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

**Eigenschaften** Windows Search bietet ein Eigenschaften [System](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) , das eine umfangreiche Bibliothek von Eigenschaften enthält. Jede Eigenschaft kann für ein beliebiges Element wie vom Filter oder Eigenschaften Handler definiert angezeigt werden. Wenn Sie ein benutzerdefiniertes Dateiformat haben, können Sie den Eigenschaften des Datei Formats diese Systemeigenschaften zuordnen, und Sie können neue benutzerdefinierte Eigenschaften erstellen. Wenn Ihr Filter oder Eigenschafts Handler diese Eigenschaften ausgibt, aktualisiert der Gatherer den Index, sodass Benutzer mit ihren Eigenschaften suchen können. Weitere Informationen zum Erstellen und registrieren benutzerdefinierter Eigenschaften für ein Dateiformat finden Sie unter Eigenschaften [System](../properties/building-property-handlers.md).

**SystemIndex**  Der Index namens SystemIndex speichert indizierte Daten und besteht aus einem Eigenschafts Speicher und Indizes über die Eigenschaften und den Inhalt für Element Eigenschaften sowie über einen invertierten Index für Textinhalte und Eigenschaften. Nachdem der Gatherer den Index aktualisiert hat, kann der Index von Windows Search und anderen Anwendungen abgefragt werden. Weitere Informationen zu den Möglichkeiten, den Index abzufragen, finden Sie Unterprogramm gesteuertes [Abfragen des Indexes](-search-3x-wds-qryidx-overview.md).

> [!NOTE]  
> Beachten Sie, dass beim erneuten Registrieren eines Schemas Änderungen, die an Attributen von zuvor definierten Eigenschaften vorgenommen wurden, vom Indexer möglicherweise nicht beachtet werden. Die Lösung besteht darin, den Index neu zu erstellen oder neue Eigenschaften einzuführen, die die Änderungen widerspiegeln, anstatt alte zu aktualisieren (nicht empfohlen). Weitere Informationen finden Sie unter [Hinweis zu Implementierern](#notes-to-implementers) in [Eigenschaften System Übersicht](../properties/property-system-overview.md).

## <a name="how-indexing-is-scheduled"></a>Planung der Indizierung

Bei der erstmaligen Installation von Windows Search wird eine vollständige Indizierung des Durchforstungs Bereichs durchlaufen, während Zeiträume mit hoher e/a-Leistung und Benutzeraktivität angehalten werden. Der standardmäßige Durchforstungs Bereich besteht aus den Standard Bibliotheks Standorten, z. b. **Dokumenten**, **Musik**, **Bildern** und **Videos**. Benachrichtigungen werden verarbeitet, auch wenn die anfängliche durch Forstung abgeschlossen ist. Gelegentlich durchforstet der Gatherer die URLs aus dem vollständigen Crawl Bereich. Diese vollständigen Crawls stellen sicher, dass die Daten im Index neu sind. Wenn z. b. ein Benachrichtigungs Anbieter keine Benachrichtigungen sendet oder der Windows Search-Dienst unerwartet beendet wird, hat der Gatherer keine Kenntnisse über neue oder geänderte Elemente und würde diese Elemente nicht indizieren. Es gibt zwei Arten von Quellen: nur Benachrichtigungs-und Benachrichtigungs Aktivierung. In beiden Quellen crawlt der Gatherer zunächst den Index. Nach der ersten durch Forstung werden die reinen Benachrichtigungs Quellen nie eine vollständige durch Forstung ausführen, es sei denn, es tritt ein Fehler auf, z. b. das Rollover des [USN-Änderungs Journals](/windows/desktop/FileIO/change-journals) Benachrichtigungs aktivierte Quellen führen eine inkrementelle durch Forstung aus, wenn der Indexer gestartet wird, während der Ausführung aber Benachrichtigungen überwacht. NTFS und Microsoft Outlook sind nur Benachrichtigung. Internet Explorer und FAT sind Benachrichtigungen aktiviert.

## <a name="notes-to-implementers"></a>Hinweise für Ausführende

Die Qualität der Daten im Index und die Effizienz des Indizierungs Prozesses hängen größtenteils von ihrer Filter-und eigenschaftenhandlerimplementierung ab. Da der Filter jedes Mal aufgerufen wird, wenn eine URL das Dateiformat identifiziert, kann sich der Indizierungsprozess erheblich verlangsamen, wenn der Filter ineffizient ist. Wenn der Eigenschafts Handler nicht alle Dateieigenschaften ordnungsgemäß den Systemeigenschaften zuordnet oder diese Eigenschaften nicht korrekt ausgibt, sind die Daten im Index falsch, und die Suche nach diesen Eigenschaften gibt falsche Ergebnisse zurück. Wenn der Filter oder Eigenschafts Handler ausfällt, kann der Indexer keine Daten indizieren.

Andere Anwendungen und Prozesse als Windows Search basieren auf Protokoll Handlern, Filtern und Eigenschaften Handlern. Ihre Implementierungen können diese Anwendungen so beeinflussen, wie Sie es möglicherweise nicht erwarten. Das [Entwicklungs Handbuch für Windows Search](-search-developers-guide-entry-page.md) bietet Ratschläge zu Entwurfsentscheidungen und zum Testen der einzelnen Komponenten.

## <a name="related-topics"></a>Zugehörige Themen

[Indizierung, Abfragen und Benachrichtigungen in Windows Search](-search-3x-wds-included-in-index.md)

[Was ist im Index enthalten?](-search-indexing-process-overview.md)

[Abfrageprozess in Windows Search](querying-process--windows-search-.md)

[Benachrichtigungs Prozess in Windows Search](-search-3x-wds-support.md)

[URL-Formatierungs Anforderungen](url-formatting-requirements.md)
