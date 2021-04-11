---
description: 'Mithilfe von Windows Search können Sie den Windows-Suchindex mit drei Hauptkomponenten verwalten: Such-Manager, Katalog-Manager und Crawl Bereich-Manager.'
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Schnittstellen für die Verwaltung des Indexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7191fbdb4e83c9e3f1460b96123901b5f277b41a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214451"
---
# <a name="interfaces-for-managing-the-index"></a>Schnittstellen für die Verwaltung des Indexes

Mithilfe von Windows Search können Sie den Windows-Suchindex mit drei Hauptkomponenten verwalten: Such-Manager, Katalog-Manager und Crawl Bereich-Manager. Einige dieser Verwaltungs Schnittstellen können mit Standardbenutzer Berechtigungen verwendet werden, aber für diejenigen, die den Status des Indexes ändern, sind Administratorrechte erforderlich.

## <a name="about-the-interfaces-for-managing-the-index"></a>Informationen zu den Schnittstellen für die Verwaltung des Indexes

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Komponente</th>
<th>Schnittstellen</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Such-Manager</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">Isearchmanager</a></td>
<td>Stellt Methoden zum Abrufen und Festlegen von Informationen über Windows Search bereit:
<ul>
<li>Eine Instanz des Katalog-Managers für einen bestimmten Katalog wird erhalten.</li>
<li>Proxy Informationen werden erhalten oder festgelegt.</li>
<li>Versionsinformationen zur Windows-Such-Engine werden erhalten.</li>
</ul>
Weitere Informationen finden Sie unter <a href="-search-3x-wds-mngidx-searchmanager.md">Verwenden des Such-Managers</a>.<br/></td>
</tr>
<tr class="even">
<td>Katalog-Manager</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">Isearchcatalogmanager</a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a><br/></td>
<td>Stellt Methoden bereit, um einen einzelnen Such Katalog zu verwalten, z. b. die Neuindizierung oder das Festlegen von Timeouts. Diese Schnittstelle verwaltet den Katalog in vier Bereichen:
<ul>
<li>Katalog Inhalte: Stellen Sie sicher, dass neue Daten indiziert werden und andere Anwendungen und Komponenten ordnungsgemäß funktionieren, indem Sie eine Neuindizierung des gesamten Katalogs oder eines Teils des Katalogs erzwingen oder den gesamten Katalog zurücksetzen.</li>
<li>Katalog Eigenschaften: Festlegen von Eigenschaften, die bestimmen, wie der Katalog Timeouts verwaltet, wenn eine Verbindung mit Protokoll Handlern hergestellt wird und wie Diakritische Markierungen in Such Vorgängen behandelt werden.</li>
<li>Katalog Status: Informationen zum Katalog erhalten, einschließlich Status, Größe und aktueller Aktivitätsstatus.</li>
<li>Zugriff auf andere Schnittstellen: Abrufen anderer Such bezogener Schnittstellen, die vom Crawl Bereichs-Manager, Daten Änderungs Benachrichtigungen und der <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>isearchqueryhelper</strong></a> -Schnittstelle benötigt werden.</li>
</ul>
Weitere Informationen finden Sie unter <a href="-search-3x-wds-mngidx-catalog-manager.md">Verwenden des Katalog-Managers</a>.<br/></td>
</tr>
<tr class="odd">
<td>Bereich-Manager für Crawl</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>Ienumsearchroots</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">Ienumsearchscoperules</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>Isearchcrawlscopemanager</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>Isearchroot</strong></a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>Isearchscoperule</strong></a><br/> <a href="/windows/desktop/search/-search-isearchitem">Isearchitem</a><br/></td>
<td>Stellt Methoden bereit, mit denen das Suchmodul über Container zum durchforsten oder überwachen informiert werden kann, sowie von Elementen unter diesen Containern, die im Index eingeschlossen oder ausgeschlossen werden sollen Sie können auch den Crawl Scope-Manager Abfragen, um festzustellen, ob sich eine bestimmte URL im Crawl Bereich befindet. Weitere Informationen finden Sie unter <a href="-search-3x-wds-extidx-csm.md">Verwenden des Crawl Scope-Managers</a>.<br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Zugehörige Themen

[Verwalten des Indexes](-search-3x-wds-mngidx-overview.md)

[Verwenden des Such-Managers](-search-3x-wds-mngidx-searchmanager.md)

[Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md)

[Verwenden des Crawl Scope-Managers](-search-3x-wds-extidx-csm.md)
