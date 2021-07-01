---
description: Erfahren Sie, wie Sie mit Windows Search den Windows Search Index mit dem Such-Manager, Katalog-Manager und Durchforstungsbereich-Manager verwalten können.
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Schnittstellen zum Verwalten des Indexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68360ec9c4a616f74392fd9dd34fc9f53b46114
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120015"
---
# <a name="interfaces-for-managing-the-index"></a><span data-ttu-id="5da1e-103">Schnittstellen zum Verwalten des Indexes</span><span class="sxs-lookup"><span data-stu-id="5da1e-103">Interfaces for Managing the Index</span></span>

<span data-ttu-id="5da1e-104">Windows Search können Sie den Windows Search Index mit drei Hauptkomponenten verwalten: Such-Manager, Katalog-Manager und Durchforstungsbereich-Manager.</span><span class="sxs-lookup"><span data-stu-id="5da1e-104">Windows Search enables you to manage the Windows Search index with three main components: Search Manager, Catalog Manager, and Crawl Scope Manager.</span></span> <span data-ttu-id="5da1e-105">Einige dieser Verwaltungsschnittstellen können mit Standardbenutzerberechtigungen verwendet werden, aber solche, die den Status des Index ändern, erfordern Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="5da1e-105">Some of these management interfaces can be used with standard user privileges, but those that change the state of the index require administrative privileges.</span></span>

## <a name="about-the-interfaces-for-managing-the-index"></a><span data-ttu-id="5da1e-106">Informationen zu den Schnittstellen zum Verwalten des Indexes</span><span class="sxs-lookup"><span data-stu-id="5da1e-106">About the Interfaces for Managing the Index</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5da1e-107">Komponente</span><span class="sxs-lookup"><span data-stu-id="5da1e-107">Component</span></span></th>
<th><span data-ttu-id="5da1e-108">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5da1e-108">Interfaces</span></span></th>
<th><span data-ttu-id="5da1e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5da1e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5da1e-110">Such-Manager</span><span class="sxs-lookup"><span data-stu-id="5da1e-110">Search Manager</span></span></td>
<td><span data-ttu-id="5da1e-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span><span class="sxs-lookup"><span data-stu-id="5da1e-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span></span></td>
<td><span data-ttu-id="5da1e-112">Stellt Methoden zum Abrufen und Festlegen von Informationen zu Windows Search bereit:</span><span class="sxs-lookup"><span data-stu-id="5da1e-112">Provides methods to retrieve and set information about Windows Search:</span></span>
<ul>
<li><span data-ttu-id="5da1e-113">Abrufen einer Instanz des Katalog-Managers für einen bestimmten Katalog.</span><span class="sxs-lookup"><span data-stu-id="5da1e-113">Getting an instance of the Catalog Manager for a specific catalog.</span></span></li>
<li><span data-ttu-id="5da1e-114">Abrufen oder Festlegen von Proxyinformationen.</span><span class="sxs-lookup"><span data-stu-id="5da1e-114">Getting or setting proxy information.</span></span></li>
<li><span data-ttu-id="5da1e-115">Abrufen von Versionsinformationen zur Windows Search-Engine.</span><span class="sxs-lookup"><span data-stu-id="5da1e-115">Getting version information about the Windows Search engine.</span></span></li>
</ul>
<span data-ttu-id="5da1e-116">Weitere Informationen finden Sie unter <a href="-search-3x-wds-mngidx-searchmanager.md">Verwenden des Such-Managers.</a></span><span class="sxs-lookup"><span data-stu-id="5da1e-116">For more information, see <a href="-search-3x-wds-mngidx-searchmanager.md">Using the Search Manager</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5da1e-117">Katalog-Manager</span><span class="sxs-lookup"><span data-stu-id="5da1e-117">Catalog Manager</span></span></td>
<td><span data-ttu-id="5da1e-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span><span class="sxs-lookup"><span data-stu-id="5da1e-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span></span><br/> <span data-ttu-id="5da1e-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span><span class="sxs-lookup"><span data-stu-id="5da1e-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span></span><br/></td>
<td><span data-ttu-id="5da1e-120">Stellt Methoden zum Verwalten eines einzelnen Suchkatalogs bereit, z. B. das Auslösen einer erneuten Indizierung oder das Festlegen von Time outs.</span><span class="sxs-lookup"><span data-stu-id="5da1e-120">Provides methods to manage an individual search catalog, such as causing a re-indexing or setting time-outs.</span></span> <span data-ttu-id="5da1e-121">Diese Schnittstelle verwaltet den Katalog in vier Bereichen:</span><span class="sxs-lookup"><span data-stu-id="5da1e-121">This interface manages the catalog in four areas:</span></span>
<ul>
<li><span data-ttu-id="5da1e-122">Kataloginhalte: Sicherstellen, dass neue Daten indiziert werden und dass andere Anwendungen und Komponenten ordnungsgemäß funktionieren, indem eine erneute Indizierung des gesamten Katalogs oder eines Teils des Katalogs erzwungen oder der gesamte Katalog zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="5da1e-122">Catalog contents - ensuring that new data is indexed and that other applications and components work properly by forcing a re-indexing of all or part of the catalog or by resetting the entire catalog.</span></span></li>
<li><span data-ttu-id="5da1e-123">Katalogeigenschaften: Festlegen von Eigenschaften, die bestimmen, wie der Katalog Time outs beim Herstellen einer Verbindung mit Protokollhandlern verwaltet und wie diakritische Markierungen in Suchvorgängen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="5da1e-123">Catalog properties - setting properties that determine how the catalog manages time-outs when connecting to protocol handlers and how diacritical marks are treated in searches.</span></span></li>
<li><span data-ttu-id="5da1e-124">Katalogstatus: Abrufen von Informationen zum Katalog, einschließlich Status, Größe und aktuellem Aktivitätsstatus.</span><span class="sxs-lookup"><span data-stu-id="5da1e-124">Catalog status - getting information about the catalog, including status, size, and current activity state.</span></span></li>
<li><span data-ttu-id="5da1e-125">Zugriff auf andere Schnittstellen: Abrufen anderer suchbezogener Schnittstellen, die für die Durchforstungsbereich-Manager, Datenänderungsbenachrichtigungen und die <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper-Schnittstelle</strong></a> erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5da1e-125">Access to other interfaces - retrieving other search-related interfaces required by the Crawl Scope Manager, data change notifications, and the <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> interface.</span></span></li>
</ul>
<span data-ttu-id="5da1e-126">Weitere Informationen finden Sie unter <a href="-search-3x-wds-mngidx-catalog-manager.md">Verwenden des Katalog-Managers.</a></span><span class="sxs-lookup"><span data-stu-id="5da1e-126">For more information, see <a href="-search-3x-wds-mngidx-catalog-manager.md">Using the Catalog Manager</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5da1e-127">Durchforstungsbereich-Manager</span><span class="sxs-lookup"><span data-stu-id="5da1e-127">Crawl Scope Manager</span></span></td>
<td><span data-ttu-id="5da1e-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span><span class="sxs-lookup"><span data-stu-id="5da1e-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span></span><br/> <span data-ttu-id="5da1e-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span><span class="sxs-lookup"><span data-stu-id="5da1e-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span></span><br/> <span data-ttu-id="5da1e-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="5da1e-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span></span><br/> <span data-ttu-id="5da1e-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span><span class="sxs-lookup"><span data-stu-id="5da1e-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span></span><br/> <span data-ttu-id="5da1e-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="5da1e-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span></span><br/> <span data-ttu-id="5da1e-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span><span class="sxs-lookup"><span data-stu-id="5da1e-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span></span><br/> <span data-ttu-id="5da1e-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span><span class="sxs-lookup"><span data-stu-id="5da1e-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span></span><br/></td>
<td><span data-ttu-id="5da1e-135">Stellt Methoden bereit, um die Suchmaschine über Container zu informieren, die durchforstet oder überwacht werden sollen, sowie Elemente unter diesen Containern, die in den Index eingeschlossen oder ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5da1e-135">Provides methods to inform the search engine about containers to crawl or watch, and items under those containers to include or exclude in the index.</span></span> <span data-ttu-id="5da1e-136">Sie können auch die Durchforstungsbereich-Manager abfragen, um festzustellen, ob sich eine bestimmte URL im Durchforstungsbereich befindet.</span><span class="sxs-lookup"><span data-stu-id="5da1e-136">You can also query the Crawl Scope Manager to see if a particular URL is in the crawl scope.</span></span> <span data-ttu-id="5da1e-137">Weitere Informationen finden Sie unter <a href="-search-3x-wds-extidx-csm.md">Verwenden des Durchforstungsbereich-Manager</a>.</span><span class="sxs-lookup"><span data-stu-id="5da1e-137">For more information, see <a href="-search-3x-wds-extidx-csm.md">Using the Crawl Scope Manager</a>.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="5da1e-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5da1e-138">Related topics</span></span>

[<span data-ttu-id="5da1e-139">Verwalten des Indexes</span><span class="sxs-lookup"><span data-stu-id="5da1e-139">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)

[<span data-ttu-id="5da1e-140">Verwenden des Such-Managers</span><span class="sxs-lookup"><span data-stu-id="5da1e-140">Using the Search Manager</span></span>](-search-3x-wds-mngidx-searchmanager.md)

[<span data-ttu-id="5da1e-141">Verwenden des Katalog-Managers</span><span class="sxs-lookup"><span data-stu-id="5da1e-141">Using the Catalog Manager</span></span>](-search-3x-wds-mngidx-catalog-manager.md)

[<span data-ttu-id="5da1e-142">Verwenden der Durchforstungsbereich-Manager</span><span class="sxs-lookup"><span data-stu-id="5da1e-142">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)
