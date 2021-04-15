---
description: Die Unterstützung von Windows 7 zum Durchsuchen von Verbund zu Remote Daten speichern mithilfe von OpenSearch-Technologien ermöglicht Benutzern den Zugriff auf und die Interaktion mit ihren Remote Daten aus Windows-Explorer.
ms.assetid: 2014b7ac-4885-4f17-b6d4-5fd95872ed59
title: Verbundsuche in Windows 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d7718bb5215072ceeb8786f5728017ed329e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484435"
---
# <a name="federated-search-in-windows"></a><span data-ttu-id="e6ea5-103">Verbundsuche in Windows 10</span><span class="sxs-lookup"><span data-stu-id="e6ea5-103">Federated Search in Windows</span></span>

<span data-ttu-id="e6ea5-104">Die Unterstützung von Windows 7 zum Durchsuchen von Verbund zu Remote Daten speichern mithilfe von OpenSearch-Technologien ermöglicht Benutzern den Zugriff auf und die Interaktion mit ihren Remote Daten aus Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="e6ea5-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span>

<span data-ttu-id="e6ea5-105">In der folgenden Themenliste wird beschrieben, wie Sie einen webbasierten Datenspeicher erstellen können, der mithilfe der Windows-Verbund Suche durchsucht werden kann, und umfassende Integration Ihrer Remote Datenquellen mit Windows-Explorer aktivieren, ohne dass Windows-Client seitiger Code geschrieben oder bereitgestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="e6ea5-105">The following list of topics describe how you can build a web-based data store that can be searched using Windows federated search, and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

-   [<span data-ttu-id="e6ea5-106">Ersten Einstieg in die Verbund Suche in Windows</span><span class="sxs-lookup"><span data-stu-id="e6ea5-106">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
-   [<span data-ttu-id="e6ea5-107">Verbinden des Webdiensts in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="e6ea5-107">Connecting Your Web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
-   [<span data-ttu-id="e6ea5-108">Aktivieren des Datenspeicher in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="e6ea5-108">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
-   [<span data-ttu-id="e6ea5-109">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="e6ea5-109">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
-   [<span data-ttu-id="e6ea5-110">Bewährte Methoden bei der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="e6ea5-110">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
-   [<span data-ttu-id="e6ea5-111">Bereitstellen von Suchconnectors in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="e6ea5-111">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
-   [<span data-ttu-id="e6ea5-112">Suchdienst-Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="e6ea5-112">Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)

## <a name="additional-resources"></a><span data-ttu-id="e6ea5-113">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e6ea5-113">Additional Resources</span></span>

-   <span data-ttu-id="e6ea5-114">Das [OpenSearch](-search-sample-opensearch.md) -Codebeispiel veranschaulicht, wie ein Verbund Suchdienst mithilfe des [OpenSearch](https://github.com/dewitt/opensearch) -Protokolls und einer OpenSearch-Deskriptor Datei (. OSDX) (Suchconnector) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e6ea5-114">The [OpenSearch](-search-sample-opensearch.md) code sample demonstrates how to create a federated search service using the [OpenSearch](https://github.com/dewitt/opensearch) protocol, and an OpenSearch Descriptor (.osdx) file (a search connector).</span></span>
-   <span data-ttu-id="e6ea5-115">Eine Video Demonstration zum Erstellen eines [OpenSearch](https://github.com/dewitt/opensearch) -Webdiensts für eine SQL-Datenbank finden [Sie unter Windows 7: ermöglichen Sie Benutzern das suchen, visualisieren und organisieren von Daten mit Bibliotheken und dem Explorer](https://channel9.msdn.com/pdc2008/PC16/).</span><span class="sxs-lookup"><span data-stu-id="e6ea5-115">For a video demonstration of creating an [OpenSearch](https://github.com/dewitt/opensearch) web service for a SQL database, see [Windows 7: Empower Users to Find, Visualize and Organize their Data with Libraries and the Explorer](https://channel9.msdn.com/pdc2008/PC16/).</span></span>
-   <span data-ttu-id="e6ea5-116">Wenn Sie einen Client seitigen [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter schreiben, finden Sie weitere Informationen unter:</span><span class="sxs-lookup"><span data-stu-id="e6ea5-116">If you are writing a client-side [OpenSearch](https://github.com/dewitt/opensearch) provider, see:</span></span>
    -   <span data-ttu-id="e6ea5-117">Der [OpenSearch-Entwickler führt](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) Sie durch, um weitere Informationen zum Herstellen einer Verbindung mit einem Client seitigen Anbieter mithilfe der Protokolle oder APIs eines proprietären Daten Stores zu finden.</span><span class="sxs-lookup"><span data-stu-id="e6ea5-117">The [OpenSearch Developer How To Guide](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) for more information on connecting to a client-side provider by using a proprietary data store's protocols or APIs.</span></span>
    -   <span data-ttu-id="e6ea5-118">Die [Übersicht über die Schema Dokumentation für das Suchconnector-Beschreibungs Schema](search-sconn-desc-schema-entry.md) (. searchconnector-MS).</span><span class="sxs-lookup"><span data-stu-id="e6ea5-118">The [Overview of the Search Connector Description Schema](search-sconn-desc-schema-entry.md) (.searchconnector-ms) schema documentation.</span></span>
-   <span data-ttu-id="e6ea5-119">Die folgende herunterladbare Ressource finden Sie auf der [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) -Website: Search Server 2008 Sample: Federated Search Connector Sample.</span><span class="sxs-lookup"><span data-stu-id="e6ea5-119">See the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) website for the following downloadable resource: Search Server 2008 Sample: Federated Search Connector Sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6ea5-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6ea5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6ea5-121">Übersicht über Windows Search</span><span class="sxs-lookup"><span data-stu-id="e6ea5-121">Windows Search Overview</span></span>](-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="e6ea5-122">Entwicklerhandbuch für Windows Search</span><span class="sxs-lookup"><span data-stu-id="e6ea5-122">Windows Search Developer's Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="e6ea5-123">Referenz zur Windows-Suche</span><span class="sxs-lookup"><span data-stu-id="e6ea5-123">Windows Search Reference</span></span>](-search-reference-entry-page.md)
</dt> <dt>

[<span data-ttu-id="e6ea5-124">Code Beispiele für Windows Search</span><span class="sxs-lookup"><span data-stu-id="e6ea5-124">Windows Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

[<span data-ttu-id="e6ea5-125">Verwandte Suchtechnologien</span><span class="sxs-lookup"><span data-stu-id="e6ea5-125">Related Search Technologies</span></span>](-search-3x-wds-sampleentry.md)
</dt> <dt>

[<span data-ttu-id="e6ea5-126">Glossar für Windows-Suche</span><span class="sxs-lookup"><span data-stu-id="e6ea5-126">Windows Search Glossary</span></span>](search-glossary.md)
</dt> </dl>

 

 



