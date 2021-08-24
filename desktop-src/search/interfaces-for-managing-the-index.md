---
description: Erfahren Sie, wie Sie mit Windows Search den Windows Search-Index mit Dem Such-Manager, Katalog-Manager und Durchforstungsbereich-Manager verwalten können.
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Schnittstellen zum Verwalten des Indexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505752cc496d55057eece87bd673b31a323c6597
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476796"
---
# <a name="interfaces-for-managing-the-index"></a>Schnittstellen zum Verwalten des Indexes

Windows Mit search können Sie den Windows Search-Index mit drei Hauptkomponenten verwalten: Such-Manager, Katalog-Manager und Durchforstungsbereich-Manager. Einige dieser Verwaltungsschnittstellen können mit Standardbenutzerberechtigungen verwendet werden, aber solche, die den Status des Index ändern, erfordern Administratorrechte.

## <a name="about-the-interfaces-for-managing-the-index"></a>Informationen zu den Schnittstellen zum Verwalten des Indexes


| Komponente | Schnittstellen | BESCHREIBUNG | 
|-----------|------------|-------------|
| Such-Manager | <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a> | Stellt Methoden zum Abrufen und Festlegen von Informationen über Windows Search bereit:<ul><li>Abrufen einer Instanz des Katalog-Managers für einen bestimmten Katalog.</li><li>Abrufen oder Festlegen von Proxyinformationen.</li><li>Abrufen von Versionsinformationen zur Windows-Suchmaschine.</li></ul>Weitere Informationen finden Sie unter <a href="-search-3x-wds-mngidx-searchmanager.md">Verwenden des Such-Managers.</a><br /> | 
| Katalog-Manager | <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a><br /> | Stellt Methoden zum Verwalten eines einzelnen Suchkatalogs bereit, z. B. das Auslösen einer erneuten Indizierung oder das Festlegen von Time outs. Diese Schnittstelle verwaltet den Katalog in vier Bereichen:<ul><li>Kataloginhalte: Sicherstellen, dass neue Daten indiziert werden und dass andere Anwendungen und Komponenten ordnungsgemäß funktionieren, indem eine erneute Indizierung des gesamten Katalogs oder eines Teils des Katalogs erzwungen oder der gesamte Katalog zurückgesetzt wird.</li><li>Katalogeigenschaften: Festlegen von Eigenschaften, die bestimmen, wie der Katalog Time outs beim Herstellen einer Verbindung mit Protokollhandlern verwaltet und wie diakritische Markierungen in Suchvorgängen behandelt werden.</li><li>Katalogstatus: Abrufen von Informationen zum Katalog, einschließlich Status, Größe und aktuellem Aktivitätsstatus.</li><li>Zugriff auf andere Schnittstellen: Abrufen anderer suchbezogener Schnittstellen, die für die Durchforstungsbereich-Manager, Datenänderungsbenachrichtigungen und die <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper-Schnittstelle</strong></a> erforderlich sind.</li></ul>Weitere Informationen finden Sie unter <a href="-search-3x-wds-mngidx-catalog-manager.md">Verwenden des Katalog-Managers.</a><br /> | 
| Durchforstungsbereich-Manager | <a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a><br /><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a><br /> | Stellt Methoden bereit, um die Suchmaschine über Container zu informieren, die durchforstet oder überwacht werden sollen, sowie Elemente unter diesen Containern, die in den Index eingeschlossen oder ausgeschlossen werden sollen. Sie können auch die Durchforstungsbereich-Manager abfragen, um festzustellen, ob sich eine bestimmte URL im Durchforstungsbereich befindet. Weitere Informationen finden Sie unter <a href="-search-3x-wds-extidx-csm.md">Verwenden des Durchforstungsbereich-Manager</a>.<br /> | 


## <a name="related-topics"></a>Zugehörige Themen

[Verwalten des Indexes](-search-3x-wds-mngidx-overview.md)

[Verwenden des Such-Managers](-search-3x-wds-mngidx-searchmanager.md)

[Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md)

[Verwenden der Durchforstungsbereich-Manager](-search-3x-wds-extidx-csm.md)
