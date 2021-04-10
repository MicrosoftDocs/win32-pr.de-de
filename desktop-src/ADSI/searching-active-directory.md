---
title: Such Active Directory
description: Eine wichtige Funktion von Active Directory besteht darin, Daten Abfragen für Personen und Konfigurationsdaten für Computer und Dienste aufzulösen.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Suchen Active Directory ADSI
- ADSI ADSI, suchen Active Directory
- Abfragen von ADSI, suchen Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1881872be6092312015f22eba477599ed9394df7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309219"
---
# <a name="searching-active-directory"></a><span data-ttu-id="952be-106">Such Active Directory</span><span class="sxs-lookup"><span data-stu-id="952be-106">Searching Active Directory</span></span>

<span data-ttu-id="952be-107">Eine wichtige Funktion von Active Directory besteht darin, Daten Abfragen für Personen und Konfigurationsdaten für Computer und Dienste aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="952be-107">An important function of Active Directory is to resolve data queries for people, as well as configuration data for computers and services.</span></span> <span data-ttu-id="952be-108">Wenn Sie effiziente Abfragen für Active Directory schreiben möchten, ist es hilfreich, sich mit folgenden Informationen vertraut zu machen:</span><span class="sxs-lookup"><span data-stu-id="952be-108">To write efficient queries for Active Directory, it is helpful to be familiar with the following:</span></span>

-   <span data-ttu-id="952be-109">Bestimmen des Gültigkeits Bereichs der Abfrage: muss der Client Eigenschaften für Objekte suchen, die sich an einer beliebigen Stelle innerhalb einer Gesamtstruktur oder nur innerhalb einer einzelnen Domäne oder innerhalb einer bestimmten Organisationseinheit befinden können?</span><span class="sxs-lookup"><span data-stu-id="952be-109">Determining the scope of the query: Must the client find properties for objects that might be located anywhere within a forest, or only within one domain, or within a given organizational unit (OU)?</span></span>
-   <span data-ttu-id="952be-110">Bestimmen der Tiefe der Abfrage: muss die Abfrage nur eine Ebene durchsuchen oder Sie in andere LDAP-Verzeichnisse überqueren?</span><span class="sxs-lookup"><span data-stu-id="952be-110">Determining the depth of the query: Must the query only search one level or might it cross into other LDAP directories?</span></span>
-   <span data-ttu-id="952be-111">Leistung und Verarbeitung großer Resultsets: wie soll der Client das Potenzial eines großen Resultsets effektiv verarbeiten?</span><span class="sxs-lookup"><span data-stu-id="952be-111">Performance and handling large result sets: How should the client effectively handle the potential of a large result set?</span></span>
-   <span data-ttu-id="952be-112">Ermitteln der besten Abfragen: welche Art von Abfragen bietet die effizientesten Ergebnisse?</span><span class="sxs-lookup"><span data-stu-id="952be-112">Determining the best queries: What type of queries provide the most efficient results?</span></span> <span data-ttu-id="952be-113">Welche Art von Abfragen sollte der Entwickler vermeiden?</span><span class="sxs-lookup"><span data-stu-id="952be-113">What type of queries should the developer avoid?</span></span>
-   <span data-ttu-id="952be-114">Grundlegendes zur Abfrage Syntax: ADSI unterstützt sowohl die LDAP-Syntax, wie in RFC 2254 dokumentiert, als auch eine Teilmenge von SQL.</span><span class="sxs-lookup"><span data-stu-id="952be-114">Understanding the query syntax: ADSI supports both the LDAP syntax as documented in RFC 2254, as well as a subset of SQL.</span></span>
-   <span data-ttu-id="952be-115">Auswahl der Schnittstellen: ADSI bietet sowohl OLE DB Unterstützung als auch eine C/C++-Schnittstelle mit dem Namen " [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)".</span><span class="sxs-lookup"><span data-stu-id="952be-115">Choice of interfaces: ADSI provides both OLE DB support as well as a C/C++ interface called [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span></span> <span data-ttu-id="952be-116">Da ADSI für mehrere Namespaces verwendet wird, können Sie diese Schnittstellen zum Abfragen anderer Namespaces (z. b. Exchange) und Active Directory verwenden.</span><span class="sxs-lookup"><span data-stu-id="952be-116">Because ADSI works for multiple namespaces, you can use these interfaces for querying other namespaces such as Exchange, as well as Active Directory.</span></span> <span data-ttu-id="952be-117">Da es sich bei dem ActiveX Data Object (ADO) um ein einfaches Skript fähige Data Access-Objektmodell auf OLE DB handelt, funktionieren die OLE DB Schnittstellen gut für Visual Basic Programmierer und Webseiten Skript Schreiber.</span><span class="sxs-lookup"><span data-stu-id="952be-117">Because the ActiveX Data Object (ADO) is a simple scriptable data access object model on top of OLE DB, the OLE DB interfaces work well for Visual Basic programmers and webpage script writers.</span></span> <span data-ttu-id="952be-118">Die neuen Datenzugriffs Features innerhalb von Visual Studio und Office-Anwendungen, die ADO und OLE DB nutzen, können jetzt auf die gleiche Weise auf Active Directory Daten zugreifen, wie Sie auf Daten von anderen OLE DB Anbietern wie SQL Server zugreifen.</span><span class="sxs-lookup"><span data-stu-id="952be-118">The new data access features within Visual Studio and Office applications that take advantage of ADO and OLE DB can now access Active Directory data in the same way that they access data from other OLE DB providers, such as SQL Server.</span></span> <span data-ttu-id="952be-119">Wenn jedoch ein C/C++-Entwickler eine einfache Verzeichnis Suche ausführen muss, ist die **idirector ysearch** -Schnittstelle möglicherweise besser geeignet als die OLE DB Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="952be-119">However, if a C/C++ developer must perform a simple directory search, the **IDirectorySearch** interface might be more appropriate than the OLE DB interfaces.</span></span>

<span data-ttu-id="952be-120">In den folgenden Themen wird beschrieben, wie Sie Active Directory durchsuchen, um sicherzustellen, dass Ihre Anwendung die effizienteste Abfrage mit den Anforderungen des Clients ausgibt:</span><span class="sxs-lookup"><span data-stu-id="952be-120">The following topics describe how to search Active Directory to ensure your application issues the most efficient query, given the requirements of the client:</span></span>

-   [<span data-ttu-id="952be-121">Abfrage Bereich</span><span class="sxs-lookup"><span data-stu-id="952be-121">Scope of Query</span></span>](scope-of-query.md)
-   [<span data-ttu-id="952be-122">Leistung und Behandlung von großen Resultsets</span><span class="sxs-lookup"><span data-stu-id="952be-122">Performance and Handling Large Result Sets</span></span>](performance-and-handling-large-result-sets.md)
-   [<span data-ttu-id="952be-123">Such Filter Syntax</span><span class="sxs-lookup"><span data-stu-id="952be-123">Search Filter Syntax</span></span>](search-filter-syntax.md)
-   [<span data-ttu-id="952be-124">Abfrageschnittstellen</span><span class="sxs-lookup"><span data-stu-id="952be-124">Query Interfaces</span></span>](query-interfaces.md)
-   [<span data-ttu-id="952be-125">Suchen von Binärdaten</span><span class="sxs-lookup"><span data-stu-id="952be-125">Searching Binary Data</span></span>](searching-binary-data.md)
-   [<span data-ttu-id="952be-126">Verteilte Abfrage</span><span class="sxs-lookup"><span data-stu-id="952be-126">Distributed Query</span></span>](distributed-query.md)

 

 




