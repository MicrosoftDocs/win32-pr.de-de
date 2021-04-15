---
description: Ab Windows 7 verbleiben Inkonsistenzen bei der Verarbeitung und der Verarbeitung von URLs. Dieses Thema enthält eine beschränkte Anleitung zum Navigieren in den Datei-URL-Formaten.
ms.assetid: E9792368-517B-4FD7-A244-6C4B7F78B66E
title: URL-Formatierungs Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08d7945578118f4d3103f44e6da60b96022e472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525439"
---
# <a name="url-formatting-requirements"></a>URL-Formatierungs Anforderungen

Ab Windows 7 verbleiben Inkonsistenzen bei der Verarbeitung und der Verarbeitung von URLs. Dieses Thema enthält eine beschränkte Anleitung zum Navigieren in den Datei-URL-Formaten.

Dieses Thema ist wie folgt organisiert:

-   [Verwendete URL-Formate](#url-formats-in-use)
-   [Schrägstrich Richtung, nach gestellter Stern und nach gestellter Schrägstrich](#slash-direction-trailing-star-and-trailing-slash-sensitivity)
-   [URL-Formate nach API und Abfrage](#url-formats-by-api-and-query)
-   [Zugehörige Themen](#related-topics)

## <a name="url-formats-in-use"></a>Verwendete URL-Formate

Protokolle von Drittanbietern sind dafür verantwortlich, das URL-Format zu definieren und Abfragen auf eine Weise zu definieren, die Ihrem Standard entspricht. Beispielsweise unterstützt Microsoft Outlook Ordnernamen mit willkürlichen Zeichen, einschließlich derjenigen, die in URLs, wie z. b. dem Zeichen, nicht zulässig sind `"?"` . Der MAPI-Protokollhandler übernimmt seine eigene URL-Codierung seiner URLs. Daher muss der Index Speicher `"%3F"` anstelle von `"?"` und Outlook bei der Erstellung von Abfragen berücksichtigt werden.

Die unterschiedlichen Formate sind in der folgenden Tabelle aufgeführt und werden jeweils einem Buchstaben Bezeichner zugewiesen, der später in diesem Thema beschrieben wird.



| id  | Lokale Datei-URL oder Remote | Beispiel                     |
|-----|--------------------------|-----------------------------|
| A   | Lokal                    | file:///c: \\ Test \\ Beispiel\\ |
| B   | Lokal                    | Datei: c:/Test/example/       |
| C   | Lokal                    | c: \\ Test \\ Beispiel\\         |
| D   | Remote                   | file:///- \\ \\ Server \\ Freigabe\\ |
| E   | Remote                   | file://server/share/        |
| F   | Remote                   | \\\\Server \\ Freigabe\\         |



 

## <a name="slash-direction-trailing-star-and-trailing-slash-sensitivity"></a>Schrägstrich Richtung, nach gestellter Stern und nach gestellter Schrägstrich

In Windows Search gibt es größtenteils keine Sensitivität für Schrägstriche. Wenn das Format `c:\test\example` akzeptiert wird, wird auch c:/Test/example akzeptiert. Obwohl der [Bereich](-search-sql-folderdepth.md) in der Regel der Schrägstrich Richtung nicht unterschieden wird, ist er im Fall des Remote-URL-Formats F für die Schrägstrich Richtung sensibel. daher `Scope = '//server/share'` funktioniert nicht.

Die einzige API, die auf nachfolgende Sterne sensibel ist und zwischen und unterscheidet, `c:\test\ ` `c:\test\*` ist [**isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager). Wenn eine Ausschlussregel für vorhanden ist `c:\test\*` , wird das URL-Verzeichnis `c:\test` selbst immer noch indiziert. Wenn die Ausschluss-URL `c:\test\` jedoch ist, wird das URL-Verzeichnis `c:\test` selbst nicht indiziert.

Es gibt zwei Orte, an denen Windows Search von nachgestellten Schrägstrichen abhängig ist: itemurl und Path Queries. Wenn ein Verzeichnis vorhanden ist `c:\test` , behandelt Windows Search `c:\test\` anders als `c:\test` bei Prädikaten wie `path = 'c:\test'` und `System.ItemUrl = 'c:\test'` . Beispielsweise würde das Prädikat `path='file:c:/test'` aufgrund des nachgestellten Schrägstrichs dem Verzeichnis entsprechen `c:\test` , dies würde jedoch nicht der Fall sein `path='file:c:/test/'` .

## <a name="url-formats-by-api-and-query"></a>URL-Formate nach API und Abfrage

Lokale Datei-URL-Formate, die von ausgewählten APIs und Abfragen akzeptiert werden, sind in der folgenden Tabelle aufgeführt. Die Formate sind einem Buchstaben (a bis F) zugeordnet. die Bedeutung von ist im Abschnitt "[verwendete URL-Formate](#url-formats-in-use)" weiter oben in diesem Thema angegeben.



| API oder Abfrage                                                                                                    | Formatieren | Format B | C-Format |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**Isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | J        | N        | J        |
| [**Igathernotifyinline:: OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | J        | J        | J        |
| [**Isearchcatalogmanager::.**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | J        | J        | J        |
| [**Isearchcatalogmanager:: in xsearchroot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | J        | N        | N        |
| [**ISearchCatalogManager2::P rioritizematchingurls**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | J        | J        | J        |
| Bereich =                                                                                                          | N        | J        | J        |
| Verzeichnis =                                                                                                      | N        | J        | J        |
| Itemurl =                                                                                                        | N        | J        | J        |
| Pfad =                                                                                                           | N        | J        | J        |



 

Remote Datei-URL-Formate, die von ausgewählten Abfragen akzeptiert werden, sind in der folgenden Tabelle aufgeführt.



| Abfrage                                                                                                           | Format D | E | F-Format |
|-----------------------------------------------------------------------------------------------------------------|----------|----------|----------|
| [**Isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)                                            | –      | –      | –      |
| [**Igathernotifyinline:: OnDataChange**](/previous-versions/windows/desktop/legacy/bb231472(v=vs.85))                           | –      | –      | –      |
| [**Isearchcatalogmanager::.**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)         | –      | –      | –      |
| [**Isearchcatalogmanager:: in xsearchroot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)             | –      | –      | –      |
| [**ISearchCatalogManager2::P rioritizematchingurls**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls) | –      | –      | –      |
| Bereich =                                                                                                          | J        | J        | J        |
| Verzeichnis =                                                                                                      | J        | J        | J        |
| Itemurl =                                                                                                        | J        | J        | J        |
| Pfad =                                                                                                           | J        | J        | J        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Was ist im Index enthalten?](-search-indexing-process-overview.md)
</dt> <dt>

[Indizierungsprozess in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Abfrageprozess in Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Benachrichtigungs Prozess in Windows Search](-search-3x-wds-support.md)
</dt> </dl>

 

 
