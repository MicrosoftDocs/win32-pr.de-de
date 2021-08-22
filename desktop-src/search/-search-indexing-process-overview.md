---
description: In diesem Thema werden die drei Phasen des Indizierungsprozesses und die beteiligten Hauptkomponenten beschrieben, der Zeitpunkt der Indizierungsaktivität erläutert und einige Hinweise für Drittanbieterentwickler angezeigt, die ihre Datenspeicher oder Dateiformate indiziert möchten.
ms.assetid: cfba12eb-4123-4b57-8311-d4fc8f9f514e
title: Indizierungsprozess in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5f69306834c001a122a18087205d64b6164d51618226fe0e0fb735f7f5b905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119095021"
---
# <a name="indexing-process-in-windows-search"></a>Indizierungsprozess in Windows Search

In diesem Thema werden die drei Phasen des Indizierungsprozesses und die beteiligten Hauptkomponenten beschrieben, der Zeitpunkt der Indizierungsaktivität erläutert und einige Hinweise für Drittanbieterentwickler angezeigt, die ihre Datenspeicher oder Dateiformate indiziert möchten.

Dieses Thema ist wie folgt organisiert:

- [Übersicht](#overview)
- [Phase 1: Warteschlangen-URLs für die Indizierung](#stage-1-queuing-urls-for-indexing)
- [Phase 2: Durchforsten von URLs](#stage-2-crawling-urls)
- [Phase 3: Aktualisieren des Indexes](#stage-3-updating-the-index)
- [Wie die Indizierung geplant ist](#how-indexing-is-scheduled)
- [Hinweise für Ausführende](#notes-to-implementers)
- [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Windows Die Suche unterstützt die Indizierung von Eigenschaften und Inhalten aus Dateien mit unterschiedlichen Dateiformaten, z. B. .doc- oder JPEG-Formaten, und Datenspeichern, z. B. dem Dateisystem oder Windows Outlook Postfächern. Es gibt zwei Arten von Indizes: Wertindizes, die das Filtern und Sortieren nach dem gesamten Wert einer Eigenschaft ermöglichen, und invertierte Indizes, die Wörter in Texteigenschaften oder -inhalten indizieren. Wenn Sie über ein benutzerdefiniertes Dateiformat oder einen benutzerdefinierten Datenspeicher verfügen, müssen Sie verstehen, wie Windows suchen, damit Ihre Elemente ordnungsgemäß indiziert werden.

Der Indizierungsprozess erfolgt in drei Phasen, die von einer Windows Search-Komponente gesteuert werden, die als Gatherer bezeichnet wird. In der ersten Phase fügt der Gatherer URLs zu Warteschlangen hinzu. Die URLs identifizieren die zu indizierenden Elemente, und die Warteschlangen sind lediglich priorisierte Listen mit URLs. In der zweiten Phase koordiniert der Gatherer andere Windows Search- und Drittanbieterkomponenten, um auf die Elemente zu zugreifen und Daten darüber zu sammeln. Schließlich werden in der dritten Phase die gesammelten Daten dem Index hinzugefügt.

Das folgende Diagramm zeigt die Hauptkomponenten und den Datenfluss durch den Indizierungsprozess. Eine Reihe von Komponenten ist an der Erfassung von Daten für den Index beteiligt. Einige davon sind Teil von Windows Search, und einige stammen aus Anwendungen von Drittanbietern. Wenn Sie über einen benutzerdefinierten Datenspeicher oder ein benutzerdefiniertes Dateiformat verfügen, verwendet Windows Search ihren Protokollhandler und Filter für den Zugriff auf URLs und die Ausgabe von Eigenschaften für die Indizierung. Windows Suchkomponenten werden blau und Komponenten von Drittanbietern grün angezeigt.

![Diagramm, das die Interaktion zwischen Komponenten während des Indizierungsprozesses zeigt](images/indexingcompoverview.jpg)

## <a name="stage-1-queuing-urls-for-indexing"></a>Phase 1: Warteschlangen-URLs für die Indizierung

In der ersten Phase der Indizierung sammelt der Gatherer Informationen zu Aktualisierungen von Datenspeichern, vergleicht diese Informationen mit dem bekannten Durchforstungsbereich und erstellt dann eine Warteschlange mit URLs, die durchlaufen werden, um Daten für den Index zu sammeln. Für Quellen, die nicht auf Benachrichtigungen basieren, z. B. FAT-Laufwerke, initiiert der Gatherer in regelmäßigen Abständen einen vollständigen Durchlauf des Durchforstungsbereichs, damit die Daten im Index auf dem neuen Datenträger bleiben. Für Quellen wie NTFS gibt es nur eine einzelne Durchforstung, und alles andere wird von Benachrichtigungen aus dem [USN Change Journal verarbeitet.](/windows/desktop/FileIO/change-journals) Es gibt auch keine Durchforstung von Microsoft Outlook. Das folgende Diagramm zeigt eine Übersicht über den Warteschlangenprozess für die Indizierung ohne Durchforstung.

![Diagramm, das den Abfrageprozess für die Indizierung ohne Durchforstung zeigt](images/queuingurls.jpg)

Im restlichen Teil dieses Abschnitts wird erläutert, Windows Search bestimmt, welche URLs durchforstung werden müssen. Außerdem werden einige wichtige Begriffe definiert.

**Durchforstungsbereich**  Der Durchforstungsbereich ist ein Satz von URLs, die die Suche Windows, um Daten zu Elementen zu sammeln, die der Benutzer für schnellere Suchvorgänge indiziert haben möchte. Windows Die Suche fügt dem Durchforstungsbereich standardmäßig einige URLs hinzu, z. B. Pfade zu den Ordnern **Dokumente** und Bilder **von** Benutzern. Andere URLs können von Anwendungen, Benutzern und Benutzern von Drittanbietern hinzugefügt Gruppenrichtlinie. Schließlich können sowohl Benutzer als auch Gruppenrichtlinie URLs explizit ausschließen. Windows Die Suche übernimmt alle hinzugefügten URLs und entfernt die ausgeschlossenen URLs, um den Durchforstungsbereich zu bestimmen. Dies ist der Arbeitssatz von URLs, mit denen der Gatherer seine Arbeit beginnt.

**Gatherer**  Der Gatherer ist eine Windows Search-Komponente, die Informationen zu URLs innerhalb des Durchforstungsbereichs sammelt und eine Warteschlange von URLs für den Indexer zum Durchforsten erstellt. Wenn ein Element im Durchforstungsbereich hinzugefügt, gelöscht oder aktualisiert wird, wird der Gatherer vom Benachrichtigungsanbieter des Datenspeichers benachrichtigt. Es gibt eine erste Durchforstung, bei der der Gatherer am Stamm des Durchforstungsbereichs beginnt. Die URL wird an den Protokollhandler und dann an den entsprechenden [**IFilter übergeben.**](/windows/win32/api/filter/nn-filter-ifilter) Der Filter ist normalerweise eine Verzeichnisenumeration, die mehr URLs erzeugt. Benachrichtigungen sind der stabile Zustand. In der Regel verfügt jeder Datenspeicher über einen eigenen Protokollhandler, der diese Benachrichtigungen bietet. Beispielsweise fungiert das [USN Change Journal](/windows/desktop/FileIO/change-journals) im lokalen Dateisystem als Benachrichtigungsanbieter für alle URLs unter dem file:// Protokoll. Ebenso fungiert Microsoft Outlook als Benachrichtigungsanbieter für alle URLs unter dem mapi:// Protokoll. Wenn ein Benutzer E-Mails empfängt, verschiebt oder löscht, benachrichtigt Outlook den Gatherer über den geänderten Status der E-Mail. Aus diesen Benachrichtigungen erstellt der Gatherer Indizierungswarteschlangen mit URLs, die durchforscht werden sollen.

**Indizieren von Warteschlangen**  Die Indizierungswarteschlangen sind Listen mit URLs, die Elemente identifizieren, die indiziert oder erneut indiziert werden müssen. Der Gatherer vergleicht die URLs, die er von Benachrichtigungsanbietern empfängt, mit den URLs im Durchforstungsbereich. Jede URL von Benachrichtigungsanbietern, die in den Durchforstungsbereich fällt, wird einer Warteschlange hinzugefügt, die der Gatherer verwendet, um zu priorisieren, welche URLs als Nächstes zu verarbeiten sind.

Es gibt drei Warteschlangen: Benachrichtigungen mit hoher Priorität, normale Benachrichtigungen und regelmäßige Durchforstungen. Die Warteschlange mit hoher Priorität ist für Benachrichtigungen, die sofort verarbeitet werden sollten. Wenn ein Benutzer beispielsweise die Titeleigenschaft eines Elements im Windows-Explorer ändert, muss die Ansicht Windows Explorer unmittelbar nach der Änderung aktualisiert werden. Die normale Benachrichtigungswarteschlange gilt für alle verbleibenden Änderungsbenachrichtigungen. Die Benachrichtigungswarteschlangen werden vor der Durchforstungswarteschlange verarbeitet, da geänderte Elemente für einen Benutzer wahrscheinlicher von Interesse sind. Der Gatherer greifen in fiFO-Reihenfolge (First In, First Out) auf Daten für die URLs in jeder Warteschlange zu.

Weitere Informationen zu Priorisierungs- und Ereignis-APIs, die in Windows 7 eingeführt wurden, finden Sie unter Indizierungspriorisierungs- und [Rowsetereignisse in Windows 7.](indexing-prioritization-and-rowset-events.md) Weitere Informationen zur Verwaltung des Durchforstungsbereichs und zu Benachrichtigungen finden Sie unter Bereitstellen von [Änderungsbenachrichtigungen](-search-3x-wds-notifyingofchanges.md) und [Verwenden der Durchforstungsbereich-Manager.](-search-3x-wds-extidx-csm.md)

## <a name="stage-2-crawling-urls"></a>Phase 2: Durchforsten von URLs

In der zweiten Phase der Indizierung durchforscht der Gatherer die Warteschlangen, greifen auf Datenspeicher zu und ruft Elementstreams ab. Zuerst sucht der Gatherer den entsprechenden Protokollhandler für jede URL. Anschließend übergibt der Gatherer die URL an den Protokollhandler. Der Protokollhandler greifen auf das Element zu und übergibt Elementmetadaten zurück an den Gatherer. Der Gatherer verwendet die Metadaten, um den richtigen Filter zu identifizieren.

Das folgende Diagramm zeigt eine übersichtsbasierte Ansicht des URL-Crawlingprozesses. Diese Phase umfasst eine erhebliche Koordination und Kommunikation zwischen Komponenten.

![Diagramm, das den Prozess des Durchforstens von URLs und des Zugriffs auf Elemente zeigt](images/crawlingqueues.jpg)

Im restlichen Teil dieses Abschnitts wird beschrieben, wie Windows Search auf Elemente für die Indizierung zuknüpft, und erläutert die Rollen der einzelnen beteiligten Komponenten.

**Gatherer**  In Phase 2, der Durchforstungsphase, verarbeitet der Gatherer die URLs in den Warteschlangen, beginnend mit der Warteschlange mit hoher Priorität. Jede URL wird untersucht, um ihr Protokoll zu identifizieren. Der Gatherer sucht dann den für dieses Protokoll registrierten Protokollhandler und instanziiert ihn im Suchprotokoll-Hostprozess.

**Suchprotokollhost**  Der Suchprotokollhost ist lediglich ein geschachtelter Hostprozess für Protokollhandler. Normalerweise erstellt Windows Search zwei solche Hostprozesse, einen, der im Systemsicherheitskontext ausgeführt wird, und einen, der im Benutzersicherheitskontext ausgeführt wird. Diese Trennung stellt sicher, dass benutzerspezifische Daten nie im Systemkontext ausgeführt werden.

Windows Die Suche verwendet auch den Hostprozess, um eine Instanz eines Protokollhandlers von anderen Prozessen oder Anwendungen zu isolieren. Auf diese Weise kann keine externe Anwendung auf diese spezifische Instanz des Protokollhandlers zugreifen, und wenn der Protokollhandler unerwartet fehlschlägt, ist nur der Indizierungsprozess betroffen. Da der Hostprozess Code von Drittanbietern (Protokollhandler) ausgeführt, verwendet Windows Search den Prozess regelmäßig, um die Zeit zu minimieren, in der ein erfolgreicher Angriff Informationen im Prozess ausnutzen muss. Darüber hinaus wirkt sich der Suchprotokollhost nicht auf das Durchforsten von URLs oder die Indizierung von Elementen aus.

**Protokollhandler**  Protokollhandler ermöglichen den Zugriff auf Elemente in einem Datenspeicher mithilfe des -Protokolls des Datenspeichers. Der NTFS-Protokollhandler ermöglicht beispielsweise den Zugriff auf Dateien auf einem lokalen Laufwerk mithilfe des file:// Protokolls. Der Protokollhandler weiß, wie er den Datenspeicher durchläuft, neue oder aktualisierte Elemente identifiziert und den Gatherer benachrichtigt. Wenn das Durchforsten beginnt, stellt der Protokollhandler dann ein [**IUrlAccessor-Objekt**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) für den Gatherer bereit, um eine Bindung an den zugrunde liegenden Stream des Elements zu erstellen und Elementmetadaten wie Sicherheitseinschränkungen und zeitpunkt der letzten Änderung zurückzukehren.

> [!NOTE]  
> Protokollhandler sind keine Windows Search-Komponenten. sie sind Komponenten des spezifischen Protokolls und Datenspeichers, auf den sie zugreifen sollen. Wenn Sie über einen benutzerdefinierten Datenspeicher verfügen, den Sie indizieren möchten, müssen Sie einen Protokollhandler implementieren. Weitere Informationen zu Protokollhandlern und zur Implementierung finden Sie unter [Entwickeln von Protokollhandlern.](-search-3x-wds-phaddins.md)

**Metadaten und Stream**  Mithilfe von Metadaten, die vom [**IUrlAccessor-Objekt**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) des Protokollhandlers zurückgegeben werden, identifiziert der Gatherer den richtigen Filter für die URL. Der Gatherer analysiert die Dateinamenerweiterung des Elements und sucht den für diese Erweiterung registrierten Filter. Wenn der Gatherer keinen Filter finden kann, verwendet Windows Search die Metadaten, um einen minimalen Satz von Systemeigenschaftsinformationen (z.B. System.ItemName) zu leiten und den Index zu aktualisieren. Andernfalls beginnt die dritte Phase der Indizierung, wenn der Gatherer den Filter findet.

## <a name="stage-3-updating-the-index"></a>Phase 3: Aktualisieren des Indexes

In der dritten Phase der Indizierung instanziiert der Gatherer den richtigen Filter für die URL und initialisiert den Filter mit dem Stream aus dem [**IUrlAccessor-Objekt.**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) Der Filter greifen dann auf das Element zu und gibt Inhalt für den Index zurück. Wenn Sie über ein benutzerdefiniertes Dateiformat verfügen, verwendet Windows Search ihren Filter für den Zugriff auf URLs und die Ausgabe von Inhalt und Eigenschaften für die Indizierung.

Das folgende Diagramm zeigt eine Übersicht über den Datenzugriffsprozess. Diese Phase umfasst eine erhebliche Koordination und Kommunikation zwischen Komponenten.

![Diagramm mit für den Index ausgegebenen Elementdaten](images/filteringdata.jpg)

Im weiteren Verlauf dieses Abschnitts wird beschrieben, wie Windows Search auf Elementdaten für die Indizierung zugreift, und die Rollen der einzelnen beteiligten Komponenten erläutert.

**Gatherer**  Am Anfang dieser Phase besteht die Aufgabe des Gatherers darin, den richtigen Filter für das Element zu instanziieren und an den Elementstream zu übergeben. Am Ende dieser Phase übernimmt der Gatherer die vom Filter- und Eigenschaftenhandler ausgegebenen Inhalte und Eigenschaften und aktualisiert den Index.

**Filterhost**  Der Filterhost ist lediglich ein Hostprozess für Filter und Eigenschaftenhandler und dient einem ähnlichen Zweck wie der Suchprotokollhost. Der Hostprozess isoliert Filter und Eigenschaftenhandler aus den gleichen Sicherheits- und Stabilitätsgründen vom Rest des Systems, aus denen Suchprotokollhostprozesse Protokollhandler isolieren. Der Hostprozess wird mit minimalen Rechten ausgeführt (er kann nicht einmal auf das Dateisystem zugreifen) und wird gelegentlich wiederverwendet, um vor Sicherheitsangriffen zu schützen. Windows Die Suche überwacht auch die Ressourcennutzung, sodass der Hostprozess wiederverwendet wird, wenn ein Filter zu viele Ressourcen verbraucht.

**Filter**  Filter sind wichtige Komponenten im Indizierungsprozess, die Elementinformationen für den Gatherer ausgeben. Filter werden nach der Prinzipalschnittstelle benannt, die in ihrer Implementierung verwendet wird, der [**IFilter-Schnittstelle,**](/windows/win32/api/filter/nn-filter-ifilter) und werden daher manchmal als IFilters bezeichnet. Es gibt zwei Arten von Filtern: einen, der mit einzelnen Elementen wie Dateien interagiert, und einen, der mit Containern wie Ordnern interagiert. Beide stellen Daten für den Index bereit.

Mithilfe von Metadaten, die vom [**IUrlAccessor-Objekt**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) des Protokollhandlers zurückgegeben werden, identifiziert der Gatherer den richtigen Filter für eine bestimmte URL und übergibt ihn an den Stream. Der Gatherer identifiziert den richtigen Filter entweder über einen Protokollhandler oder durch die Dateinamenerweiterung, den MIME-Typ oder den Klassenbezeichner (CLSID). Wenn die URL auf einen Container verweist, gibt der Filter Eigenschaften für den Container aus und listet die Elemente im Container auf (untergeordnete URLs). Wenn die URL auf ein Element verweist, gibt der Filter den Textinhalt zurück, wenn das Lesen von Eigenschaften und komplexer als Eigenschaftenhandler ist. Im Allgemeinen wird empfohlen, dass Filter Elementinhalte ausgeben, während Eigenschaftenhandler Elementeigenschaften ausgeben. Wenn Ihr Filter jedoch mit älteren Anwendungen arbeiten muss, die keine Eigenschaftenhandler erkennen, können Sie den Filter auch implementieren, um Eigenschaften auszugeben.

> [!NOTE]  
> Filter sind keine Windows Search-Komponenten. sie sind Komponenten im Zusammenhang mit dem spezifischen Dateiformat oder Container, auf das bzw. den sie zugreifen sollen. Weitere Informationen zu Filtern und zum Implementieren eines Filters für ein benutzerdefiniertes Dateiformat oder einen benutzerdefinierten Container finden Sie unter [Best Practices for Creating Filter Handlers in Windows Search](-search-3x-wds-extidx-filters.md).

In der folgenden Tabelle sind die Ergebnisse aufgeführt, die der Gatherer während des Indizierungsprozesses von einem Filter ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)) und einem Eigenschaftenhandler ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) empfängt.

|                            | [**Ifilter**](/windows/win32/api/filter/nn-filter-ifilter) | [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) |
|----------------------------|------------------------------------|-------------------------------------------------|
| **Schreibzugriff zulassen**                | Nein                                 | Ja                                             |
| **Mischen von Inhalt und Eigenschaften** | Ja                                | Nein                                              |
| **Mehrsprachige**               | Ja                                | Nein                                              |
| **Ausgeben von Links**                 | Ja                                | Nein                                              |
| **Mime**                       | Ja                                | Nein                                              |
| **Textgrenzen**            | Satz, Absatz, Kapitel       | Keine                                            |
| **Client/Server**            | Beide                               | Client                                          |
| **Implementierung**             | Komplex                            | Einfach                                          |

**Eigenschaftenhandler**  Eigenschaftenhandler sind Komponenten, die Eigenschaften für ein bestimmtes Dateiformat lesen und schreiben. Sie greifen auf Elemente zu und geben Eigenschaften für den Gatherer auf die gleiche Weise aus wie Filter für Inhalte. Eigenschaftenhandler sind einfacher zu implementieren als Filter. Wenn ein textbasiertes Dateiformat sehr einfach ist oder die Dateien sehr klein sein sollen, kann der Eigenschaftenhandler sowohl Eigenschaften als auch Inhalt ausgeben.

> [!NOTE]  
> Eigenschaftenhandler sind keine Windows Search-Komponenten. sie sind Komponenten, die sich auf das spezifische Dateiformat beziehen, auf das sie zugreifen sollen. Weitere Informationen zu Eigenschaftenhandlern und zur Implementierung eines Handlers für ein benutzerdefiniertes Dateiformat finden Sie unter [Developing Property Handlers for Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

**Eigenschaften** Windows Search stellt ein [Eigenschaftensystem](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) bereit, das eine große Bibliothek von Eigenschaften enthält. Jede Eigenschaft kann für jedes Element angezeigt werden, wie vom Filter oder Eigenschaftenhandler definiert. Wenn Sie über ein benutzerdefiniertes Dateiformat verfügen, können Sie die Eigenschaften Ihres Dateiformats diesen Systemeigenschaften zuordnen und neue benutzerdefinierte Eigenschaften erstellen. Wenn Ihr Filter- oder Eigenschaftenhandler diese Eigenschaften ausgibt, aktualisiert der Gatherer den Index, sodass Benutzer mit Ihren Eigenschaften suchen können. Weitere Informationen zum Erstellen und Registrieren von benutzerdefinierten Eigenschaften für ein Dateiformat finden Sie unter [Eigenschaftensystem.](../properties/building-property-handlers.md)

**SystemIndex**  Der Index namens SystemIndex speichert indizierte Daten und besteht aus einem Eigenschaftenspeicher und Indizes für die Eigenschaften und den Inhalt für Elementeigenschaften sowie einem invertierten Index für Textinhalte und -eigenschaften. Nachdem der Gatherer den Index aktualisiert hat, kann der Index durch Windows Search und andere Anwendungen abgefragt werden. Weitere Informationen zu Denkmethoden zum Abfragen des Index finden Sie unter [Programmgesteuertes Abfragen des Indexes.](-search-3x-wds-qryidx-overview.md)

> [!NOTE]  
> Beachten Sie, dass Änderungen an Attributen zuvor definierter Eigenschaften beim erneuten Registrieren eines Schemas vom Indexer möglicherweise nicht berücksichtigt werden. Die Lösung besteht darin, entweder den Index neu zu erstellen oder neue Eigenschaften einzuführen, die die Änderungen widerspiegeln, anstatt alte zu aktualisieren (nicht empfohlen). Weitere Informationen finden Sie unter [Hinweis zu Implementierern](#notes-to-implementers) in [Eigenschaftensystemübersicht.](../properties/property-system-overview.md)

## <a name="how-indexing-is-scheduled"></a>Planen der Indizierung

Wenn Windows Search zum ersten Mal installiert wird, führt sie eine vollständige Indizierung des Durchforstungsbereichs durch und hält während Zeiträumen mit hoher E/A- und Benutzeraktivität an. Der Standardmäßige Durchforstungsbereich besteht aus den Standardbibliotheksspeicherorten, z. B. **Dokumente,** **Musik,** **Bilder** und **Videos.** Benachrichtigungen werden noch vor Abschluss der ersten Durchforstung verarbeitet. Gelegentlich durchforstet der Gatherer die URLs aus dem vollständigen Durchforstungsbereich. Diese vollständigen Durchforstungen stellen sicher, dass die Daten im Index neu sind. Wenn beispielsweise ein Benachrichtigungsanbieter keine Benachrichtigungen senden kann oder die Windows Suchdienst unerwartet beendet wird, hat der Gatherer keine Kenntnis von neuen oder geänderten Elementen und indiziert diese Elemente nicht. Es gibt zwei Arten von Quellen: nur Benachrichtigung und Benachrichtigung aktiviert. In beiden Quellen durchforstet der Gatherer zunächst den Index. Nach der ersten Durchforstung werden die quellen, die nur für Benachrichtigungen verwendet werden, nie wieder eine vollständige Durchforstung durchführen, es sei denn, es ist ein Fehler vorhanden, z. B. ein Rollback des [USN-Änderungsjournals.](/windows/desktop/FileIO/change-journals) Benachrichtigungsfähige Quellen führen eine inkrementelle Durchforstung durch, wenn der Indexer gestartet wird, lauschen dann aber während der Ausführung auf Benachrichtigungen. NTFS und Microsoft Outlook sind nur Benachrichtigungen. Internet Explorer und FAT sind Benachrichtigungen aktiviert.

## <a name="notes-to-implementers"></a>Hinweise für Ausführende

Die Qualität der Daten im Index und die Effizienz des Indizierungsprozesses hängen größtenteils von ihrer Implementierung des Filter- und Eigenschaftenhandlers ab. Da der Filter jedes Mal aufgerufen wird, wenn eine URL Ihr Dateiformat identifiziert, kann der Indizierungsprozess erheblich verlangsamt werden, wenn ihr Filter ineffizient ist. Wenn Ihr Eigenschaftenhandler nicht alle Dateieigenschaften ordnungsgemäß systemeigenschaften zuweist oder diese Eigenschaften nicht ordnungsgemäß ausgibt, sind die Daten im Index falsch, und spätere Suchvorgänge nach diesen Eigenschaften geben falsche Ergebnisse zurück. Wenn ihr Filter- oder Eigenschaftenhandler fehlschlägt, kann der Indexer keine Daten indizieren.

Andere Anwendungen und Prozesse als Windows Search basieren auf Protokollhandlern, Filtern und Eigenschaftenhandlern. Ihre Implementierungen können diese Anwendungen auf eine Weise beeinflussen, die Sie möglicherweise nicht erwarten. Das [Windows Search Development Guide (Entwicklungshandbuch](-search-developers-guide-entry-page.md) für die Suche) enthält Hinweise zu Entwurfsentscheidungen und zum Testen jeder dieser Komponenten.

## <a name="related-topics"></a>Zugehörige Themen

[Indizieren, Abfragen und Benachrichtigungen in Windows Search](-search-3x-wds-included-in-index.md)

[Was ist im Index enthalten?](-search-indexing-process-overview.md)

[Abfrageprozess in Windows Search](querying-process--windows-search-.md)

[Benachrichtigungsprozess in Windows Search](-search-3x-wds-support.md)

[Anforderungen an die URL-Formatierung](url-formatting-requirements.md)
