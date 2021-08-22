---
description: Ab Windows 7 verbleiben Inkonsistenzen bei der Behandlung und Analyse von URLs. Dieses Thema enthält eine eingeschränkte Anleitung zum Navigieren in Inkonsistenzen in Datei-URL-Formaten.
ms.assetid: E9792368-517B-4FD7-A244-6C4B7F78B66E
title: URL-Formatierungsanforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1bb413501548922eaf1b60801b6d35495d7f8a37dc743675052d4e0e5bae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462232"
---
# <a name="url-formatting-requirements"></a>URL-Formatierungsanforderungen

Ab Windows 7 verbleiben Inkonsistenzen bei der Behandlung und Analyse von URLs. Dieses Thema enthält eine eingeschränkte Anleitung zum Navigieren in Inkonsistenzen in Datei-URL-Formaten.

Dieses Thema ist wie folgt organisiert:

-   [URL-Formate in Verwendung](#url-formats-in-use)
-   [Schrägstrichrichtung, nach trailing star und trailing slash sensitivity](#slash-direction-trailing-star-and-trailing-slash-sensitivity)
-   [URL-Formate nach API und Abfrage](#url-formats-by-api-and-query)
-   [Zugehörige Themen](#related-topics)

## <a name="url-formats-in-use"></a>URL-Formate in Verwendung

Protokolle von Drittanbietern sind dafür verantwortlich, ihr URL-Format und Abfragen so zu definieren, dass sie ihren Standards entsprechen. Beispielsweise unterstützt Microsoft Outlook Ordnernamen mit beliebigen Zeichen, einschließlich derer, die in URLs, z. B. dem Zeichen, unzulässig `"?"` sind. Der MAPI-Protokollhandler führt eine eigene URL-Codierung seiner URLs durch. Daher speichert der Index anstelle von , und Outlook muss dies beim Erstellen `"%3F"` `"?"` von Abfragen berücksichtigen.

Die verschiedenen Formate sind in der folgenden Tabelle aufgeführt und erhalten jeweils einen Buchstabenbezeichner, um später in diesem Thema darauf zu verweisen.



| ID  | Lokale Datei-URL oder Remotedatei | Beispiel                     |
|-----|--------------------------|-----------------------------|
| Ein   | Lokal                    | file:///c: \\ \\ Testbeispiel\\ |
| B   | Lokal                    | file:c:/test/example/       |
| C   | Lokal                    | c: \\ \\ Testbeispiel\\         |
| D   | Remote                   | \\ \\ file:///-Serverfreigabe \\\\ |
| E   | Remote                   | file://server/share/        |
| F   | Remote                   | \\\\\\Serverfreigabe\\         |



 

## <a name="slash-direction-trailing-star-and-trailing-slash-sensitivity"></a>Schrägstrichrichtung, nach trailing star und trailing slash sensitivity

In Windows Suche gibt es größtenteils keine Empfindlichkeit gegenüber der Schrägstrichrichtung. Wenn das Format `c:\test\example` akzeptiert wird, wird auch c:/test/example akzeptiert. Obwohl [SCOPE](-search-sql-folderdepth.md) im Allgemeinen keine Schrägstrichrichtung beachtet, ist die Schrägstrichrichtung im Fall des Remote-URL-Formats F nicht zu sehen. Daher funktioniert `Scope = '//server/share'` nicht.

Die einzige API, die auf nach trailende Sterne reagieren und zwischen `c:\test\ ` und unterscheidet, `c:\test\*` ist [**ISearchCrawlScopeManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) Wenn eine Ausschlussregel für vorhanden ist, wird das `c:\test\*` `c:\test` URL-Verzeichnis selbst weiterhin indiziert. Wenn die Ausschluss-URL jedoch ist, wird das `c:\test\` `c:\test` URL-Verzeichnis selbst nicht indiziert.

Es gibt zwei Stellen, an denen Windows Suchfunktion auf nachgeschlagene Schrägstriche reagieren kann: ItemUrl- und Path-Abfragen. Wenn ein Verzeichnis vorhanden ist, behandelt Windows Search anders `c:\test` `c:\test\` als für `c:\test` Prädikate wie `path = 'c:\test'` und `System.ItemUrl = 'c:\test'` . Das Prädikat würde z. B. mit dem Verzeichnis übereinstimmen, aber nicht aufgrund des nach folgenden `path='file:c:/test'` `c:\test` `path='file:c:/test/'` Schrägstrichs.

## <a name="url-formats-by-api-and-query"></a>URL-Formate nach API und Abfrage

Url-Formate lokaler Dateien, die von ausgewählten APIs und Abfragen akzeptiert werden, sind in der folgenden Tabelle aufgeführt. Die Formate sind einem Buchstaben (A bis F) zugeordnet, dessen Bedeutung im Abschnitt["URL-Formate in Verwendung"](#url-formats-in-use)weiter oben in diesem Thema angegeben wurde.



| API oder Abfrage                                                                                                    | Format A | Format B | Format C |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | J        | N        | J        |
| [**IGatherNotifyInline::OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | J        | J        | J        |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | J        | J        | J        |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | J        | N        | N        |
| [**ISearchCatalogManager2::P izeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | J        | J        | J        |
| Scope=                                                                                                          | N        | J        | J        |
| Directory=                                                                                                      | N        | J        | J        |
| ItemUrl=                                                                                                        | N        | J        | J        |
| Path=                                                                                                           | N        | J        | J        |



 

Url-Formate für Remotedatei, die von ausgewählten Abfragen akzeptiert werden, sind in der folgenden Tabelle aufgeführt.



| Abfrage                                                                                                           | Format D | Format E | Format F |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | Nicht zutreffend      | Nicht zutreffend      | Nicht zutreffend      |
| [**IGatherNotifyInline::OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | Nicht zutreffend      | Nicht zutreffend      | Nicht zutreffend      |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | Nicht zutreffend      | Nicht zutreffend      | Nicht zutreffend      |
| [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | Nicht zutreffend      | Nicht zutreffend      | Nicht zutreffend      |
| [**ISearchCatalogManager2::P rioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | Nicht zutreffend      | Nicht zutreffend      | Nicht zutreffend      |
| Scope=                                                                                                          | J        | J        | J        |
| Directory=                                                                                                      | J        | J        | J        |
| ItemUrl=                                                                                                        | J        | J        | J        |
| Path=                                                                                                           | J        | J        | J        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Was ist im Index enthalten?](-search-indexing-process-overview.md)
</dt> <dt>

[Indizierungsprozess in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Abfrageprozess in Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Benachrichtigungsprozess in Windows Search](-search-3x-wds-support.md)
</dt> </dl>

 

 
