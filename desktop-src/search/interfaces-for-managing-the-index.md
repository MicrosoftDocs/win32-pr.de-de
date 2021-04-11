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
# <a name="interfaces-for-managing-the-index"></a><span data-ttu-id="bffd7-103">Schnittstellen für die Verwaltung des Indexes</span><span class="sxs-lookup"><span data-stu-id="bffd7-103">Interfaces for Managing the Index</span></span>

<span data-ttu-id="bffd7-104">Mithilfe von Windows Search können Sie den Windows-Suchindex mit drei Hauptkomponenten verwalten: Such-Manager, Katalog-Manager und Crawl Bereich-Manager.</span><span class="sxs-lookup"><span data-stu-id="bffd7-104">Windows Search enables you to manage the Windows Search index with three main components: Search Manager, Catalog Manager, and Crawl Scope Manager.</span></span> <span data-ttu-id="bffd7-105">Einige dieser Verwaltungs Schnittstellen können mit Standardbenutzer Berechtigungen verwendet werden, aber für diejenigen, die den Status des Indexes ändern, sind Administratorrechte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bffd7-105">Some of these management interfaces can be used with standard user privileges, but those that change the state of the index require administrative privileges.</span></span>

## <a name="about-the-interfaces-for-managing-the-index"></a><span data-ttu-id="bffd7-106">Informationen zu den Schnittstellen für die Verwaltung des Indexes</span><span class="sxs-lookup"><span data-stu-id="bffd7-106">About the Interfaces for Managing the Index</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bffd7-107">Komponente</span><span class="sxs-lookup"><span data-stu-id="bffd7-107">Component</span></span></th>
<th><span data-ttu-id="bffd7-108">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="bffd7-108">Interfaces</span></span></th>
<th><span data-ttu-id="bffd7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bffd7-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bffd7-110">Such-Manager</span><span class="sxs-lookup"><span data-stu-id="bffd7-110">Search Manager</span></span></td>
<td><span data-ttu-id="bffd7-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">Isearchmanager</a></span><span class="sxs-lookup"><span data-stu-id="bffd7-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span></span></td>
<td><span data-ttu-id="bffd7-112">Stellt Methoden zum Abrufen und Festlegen von Informationen über Windows Search bereit:</span><span class="sxs-lookup"><span data-stu-id="bffd7-112">Provides methods to retrieve and set information about Windows Search:</span></span>
<ul>
<li><span data-ttu-id="bffd7-113">Eine Instanz des Katalog-Managers für einen bestimmten Katalog wird erhalten.</span><span class="sxs-lookup"><span data-stu-id="bffd7-113">Getting an instance of the Catalog Manager for a specific catalog.</span></span></li>
<li><span data-ttu-id="bffd7-114">Proxy Informationen werden erhalten oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bffd7-114">Getting or setting proxy information.</span></span></li>
<li><span data-ttu-id="bffd7-115">Versionsinformationen zur Windows-Such-Engine werden erhalten.</span><span class="sxs-lookup"><span data-stu-id="bffd7-115">Getting version information about the Windows Search engine.</span></span></li>
</ul>
<span data-ttu-id="bffd7-116">Weitere Informationen finden Sie unter <a href="-search-3x-wds-mngidx-searchmanager.md">Verwenden des Such-Managers</a>.</span><span class="sxs-lookup"><span data-stu-id="bffd7-116">For more information, see <a href="-search-3x-wds-mngidx-searchmanager.md">Using the Search Manager</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bffd7-117">Katalog-Manager</span><span class="sxs-lookup"><span data-stu-id="bffd7-117">Catalog Manager</span></span></td>
<td><span data-ttu-id="bffd7-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">Isearchcatalogmanager</a></span><span class="sxs-lookup"><span data-stu-id="bffd7-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span></span><br/> <span data-ttu-id="bffd7-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span><span class="sxs-lookup"><span data-stu-id="bffd7-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span></span><br/></td>
<td><span data-ttu-id="bffd7-120">Stellt Methoden bereit, um einen einzelnen Such Katalog zu verwalten, z. b. die Neuindizierung oder das Festlegen von Timeouts.</span><span class="sxs-lookup"><span data-stu-id="bffd7-120">Provides methods to manage an individual search catalog, such as causing a re-indexing or setting time-outs.</span></span> <span data-ttu-id="bffd7-121">Diese Schnittstelle verwaltet den Katalog in vier Bereichen:</span><span class="sxs-lookup"><span data-stu-id="bffd7-121">This interface manages the catalog in four areas:</span></span>
<ul>
<li><span data-ttu-id="bffd7-122">Katalog Inhalte: Stellen Sie sicher, dass neue Daten indiziert werden und andere Anwendungen und Komponenten ordnungsgemäß funktionieren, indem Sie eine Neuindizierung des gesamten Katalogs oder eines Teils des Katalogs erzwingen oder den gesamten Katalog zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="bffd7-122">Catalog contents - ensuring that new data is indexed and that other applications and components work properly by forcing a re-indexing of all or part of the catalog or by resetting the entire catalog.</span></span></li>
<li><span data-ttu-id="bffd7-123">Katalog Eigenschaften: Festlegen von Eigenschaften, die bestimmen, wie der Katalog Timeouts verwaltet, wenn eine Verbindung mit Protokoll Handlern hergestellt wird und wie Diakritische Markierungen in Such Vorgängen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="bffd7-123">Catalog properties - setting properties that determine how the catalog manages time-outs when connecting to protocol handlers and how diacritical marks are treated in searches.</span></span></li>
<li><span data-ttu-id="bffd7-124">Katalog Status: Informationen zum Katalog erhalten, einschließlich Status, Größe und aktueller Aktivitätsstatus.</span><span class="sxs-lookup"><span data-stu-id="bffd7-124">Catalog status - getting information about the catalog, including status, size, and current activity state.</span></span></li>
<li><span data-ttu-id="bffd7-125">Zugriff auf andere Schnittstellen: Abrufen anderer Such bezogener Schnittstellen, die vom Crawl Bereichs-Manager, Daten Änderungs Benachrichtigungen und der <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>isearchqueryhelper</strong></a> -Schnittstelle benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="bffd7-125">Access to other interfaces - retrieving other search-related interfaces required by the Crawl Scope Manager, data change notifications, and the <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> interface.</span></span></li>
</ul>
<span data-ttu-id="bffd7-126">Weitere Informationen finden Sie unter <a href="-search-3x-wds-mngidx-catalog-manager.md">Verwenden des Katalog-Managers</a>.</span><span class="sxs-lookup"><span data-stu-id="bffd7-126">For more information, see <a href="-search-3x-wds-mngidx-catalog-manager.md">Using the Catalog Manager</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bffd7-127">Bereich-Manager für Crawl</span><span class="sxs-lookup"><span data-stu-id="bffd7-127">Crawl Scope Manager</span></span></td>
<td><span data-ttu-id="bffd7-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>Ienumsearchroots</strong></a></span><span class="sxs-lookup"><span data-stu-id="bffd7-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span></span><br/> <span data-ttu-id="bffd7-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">Ienumsearchscoperules</a></span><span class="sxs-lookup"><span data-stu-id="bffd7-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span></span><br/> <span data-ttu-id="bffd7-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>Isearchcrawlscopemanager</strong></a></span><span class="sxs-lookup"><span data-stu-id="bffd7-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span></span><br/> <span data-ttu-id="bffd7-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span><span class="sxs-lookup"><span data-stu-id="bffd7-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span></span><br/> <span data-ttu-id="bffd7-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>Isearchroot</strong></a></span><span class="sxs-lookup"><span data-stu-id="bffd7-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span></span><br/> <span data-ttu-id="bffd7-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>Isearchscoperule</strong></a></span><span class="sxs-lookup"><span data-stu-id="bffd7-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span></span><br/> <span data-ttu-id="bffd7-134"><a href="/windows/desktop/search/-search-isearchitem">Isearchitem</a></span><span class="sxs-lookup"><span data-stu-id="bffd7-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span></span><br/></td>
<td><span data-ttu-id="bffd7-135">Stellt Methoden bereit, mit denen das Suchmodul über Container zum durchforsten oder überwachen informiert werden kann, sowie von Elementen unter diesen Containern, die im Index eingeschlossen oder ausgeschlossen werden sollen</span><span class="sxs-lookup"><span data-stu-id="bffd7-135">Provides methods to inform the search engine about containers to crawl or watch, and items under those containers to include or exclude in the index.</span></span> <span data-ttu-id="bffd7-136">Sie können auch den Crawl Scope-Manager Abfragen, um festzustellen, ob sich eine bestimmte URL im Crawl Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="bffd7-136">You can also query the Crawl Scope Manager to see if a particular URL is in the crawl scope.</span></span> <span data-ttu-id="bffd7-137">Weitere Informationen finden Sie unter <a href="-search-3x-wds-extidx-csm.md">Verwenden des Crawl Scope-Managers</a>.</span><span class="sxs-lookup"><span data-stu-id="bffd7-137">For more information, see <a href="-search-3x-wds-extidx-csm.md">Using the Crawl Scope Manager</a>.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="bffd7-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bffd7-138">Related topics</span></span>

[<span data-ttu-id="bffd7-139">Verwalten des Indexes</span><span class="sxs-lookup"><span data-stu-id="bffd7-139">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)

[<span data-ttu-id="bffd7-140">Verwenden des Such-Managers</span><span class="sxs-lookup"><span data-stu-id="bffd7-140">Using the Search Manager</span></span>](-search-3x-wds-mngidx-searchmanager.md)

[<span data-ttu-id="bffd7-141">Verwenden des Katalog-Managers</span><span class="sxs-lookup"><span data-stu-id="bffd7-141">Using the Catalog Manager</span></span>](-search-3x-wds-mngidx-catalog-manager.md)

[<span data-ttu-id="bffd7-142">Verwenden des Crawl Scope-Managers</span><span class="sxs-lookup"><span data-stu-id="bffd7-142">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)
