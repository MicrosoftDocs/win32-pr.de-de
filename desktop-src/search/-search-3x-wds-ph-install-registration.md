---
description: Die Installation eines Protokoll Handlers umfasst das Kopieren der dll (s) an einen geeigneten Speicherort im Verzeichnis "Programme" und das anschließende Registrieren des Protokoll Handlers über die Registrierung.
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: Installieren und Registrieren von Protokoll Handlern (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb30032ef200832446a8a2f37b2ec427ab40b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353028"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a><span data-ttu-id="06f29-103">Installieren und Registrieren von Protokoll Handlern (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="06f29-103">Installing and Registering Protocol Handlers (Windows Search)</span></span>

<span data-ttu-id="06f29-104">Die Installation eines Protokoll Handlers umfasst das Kopieren der dll (s) an einen geeigneten Speicherort im Verzeichnis "Programme" und das anschließende Registrieren des Protokoll Handlers über die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="06f29-104">Installing a protocol handler involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the protocol handler through the registry.</span></span> <span data-ttu-id="06f29-105">Die Installationsanwendung kann auch eine Such Stamm-und Bereichs Regel hinzufügen, um einen Standard-Crawlen Bereich für die shelldatenquelle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="06f29-105">The installation application can also add a search root and scope rules to define a default crawl scope for the Shell data source.</span></span>

<span data-ttu-id="06f29-106">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="06f29-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="06f29-107">Informationen zu URLs</span><span class="sxs-lookup"><span data-stu-id="06f29-107">About URLs</span></span>](#about-urls)
-   [<span data-ttu-id="06f29-108">Implementieren von protokollhandlerschnittstellen</span><span class="sxs-lookup"><span data-stu-id="06f29-108">Implementing Protocol Handler Interfaces</span></span>](#implementing-protocol-handler-interfaces)
    -   [<span data-ttu-id="06f29-109">Isearchprotocol und ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="06f29-109">ISearchProtocol and ISearchProtocol2</span></span>](#isearchprotocol-and-isearchprotocol2)
    -   [<span data-ttu-id="06f29-110">Iurlaccessor, IUrlAccessor2, IUrlAccessor3 und IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="06f29-110">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [<span data-ttu-id="06f29-111">Iprotocolhandlersite</span><span class="sxs-lookup"><span data-stu-id="06f29-111">IProtocolHandlerSite</span></span>](#iprotocolhandlersite)
-   [<span data-ttu-id="06f29-112">Implementieren von Filter Handlern für Container</span><span class="sxs-lookup"><span data-stu-id="06f29-112">Implementing Filter Handlers for Containers</span></span>](#implementing-filter-handlers-for-containers)
-   [<span data-ttu-id="06f29-113">Installieren und Registrieren eines Protokoll Handlers</span><span class="sxs-lookup"><span data-stu-id="06f29-113">Installing and Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="06f29-114">Richtlinien zum Registrieren eines Protokoll Handlers</span><span class="sxs-lookup"><span data-stu-id="06f29-114">Guidelines for Registering a Protocol Handler</span></span>](#guidelines-for-registering-a-protocol-handler)
    -   [<span data-ttu-id="06f29-115">Registrieren eines Protokoll Handlers</span><span class="sxs-lookup"><span data-stu-id="06f29-115">Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="06f29-116">Registrieren des Dateityp Handlers des Protokoll Handlers</span><span class="sxs-lookup"><span data-stu-id="06f29-116">Registering the Protocol Handler's File Type Handler</span></span>](#registering-the-protocol-handlers-file-type-handler)
-   [<span data-ttu-id="06f29-117">Sicherstellen, dass ihre Elemente indiziert werden</span><span class="sxs-lookup"><span data-stu-id="06f29-117">Ensuring that Your Items are Indexed</span></span>](#ensuring-that-your-items-are-indexed)
-   [<span data-ttu-id="06f29-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06f29-118">Related topics</span></span>](#related-topics)

## <a name="about-urls"></a><span data-ttu-id="06f29-119">Informationen zu URLs</span><span class="sxs-lookup"><span data-stu-id="06f29-119">About URLs</span></span>

<span data-ttu-id="06f29-120">Windows Search verwendet URLs, um Elemente in der Hierarchie der shelldatenquelle eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="06f29-120">Windows Search uses URLs to uniquely identify items in the hierarchy of your Shell data source.</span></span> <span data-ttu-id="06f29-121">Die URL, die der erste Knoten in der Hierarchie ist, wird als [Suchstamm](-search-3x-wds-extidx-csm-searchroots.md)bezeichnet. Windows Search beginnt mit der Indizierung am Suchstamm und fordert an, dass der Protokollhandler für jede URL untergeordnete Links aufzählt.</span><span class="sxs-lookup"><span data-stu-id="06f29-121">The URL that is the first node in the hierarchy is called the [search root](-search-3x-wds-extidx-csm-searchroots.md); Windows Search will begin indexing at the search root, requesting that the protocol handler enumerate child links for each URL.</span></span>

<span data-ttu-id="06f29-122">Die typische URL-Struktur lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="06f29-122">The typical URL structure is:</span></span>


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



<span data-ttu-id="06f29-123">Die URL-Syntax wird in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="06f29-123">The URL syntax is described in the following table.</span></span>



| <span data-ttu-id="06f29-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="06f29-124">Syntax</span></span>           | <span data-ttu-id="06f29-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06f29-125">Description</span></span>                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <protocol> | <span data-ttu-id="06f29-126">Gibt an, welcher Protokollhandler für die URL aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="06f29-126">Identifies which protocol handler to invoke for the URL.</span></span>                                                                                                                                                           |
| <span data-ttu-id="06f29-127">{Benutzer-sid}</span><span class="sxs-lookup"><span data-stu-id="06f29-127">{user SID}</span></span>       | <span data-ttu-id="06f29-128">Gibt den Benutzer Sicherheitskontext an, unter dem der Protokollhandler aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="06f29-128">Identifies the user security context under which the protocol handler is called.</span></span> <span data-ttu-id="06f29-129">Wenn keine Benutzersicherheits-ID (SID) identifiziert wird, wird der Protokollhandler im Sicherheitskontext des-System Diensts aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="06f29-129">If no user security identifier (SID) is identified, the protocol handler is called in the security context of the system service.</span></span> |
| <path>     | <span data-ttu-id="06f29-130">Definiert die Hierarchie des Stores, wobei jeder Schrägstrich ("/") ein Trennzeichen zwischen den Ordnernamen ist.</span><span class="sxs-lookup"><span data-stu-id="06f29-130">Defines the hierarchy of the store, where each forward slash ('/') is a separator between folder names.</span></span>                                                                                                            |
| <ItemID>   | <span data-ttu-id="06f29-131">Stellt eine eindeutige Zeichenfolge dar, die das untergeordnete Element identifiziert (z. b. den Dateinamen).</span><span class="sxs-lookup"><span data-stu-id="06f29-131">Represents a unique string that identifies the child item (for example, the file name).</span></span>                                                                                                                            |



 

<span data-ttu-id="06f29-132">Der Windows Search-Indexer schneidet den abschließenden Schrägstrich aus den URLs ab.</span><span class="sxs-lookup"><span data-stu-id="06f29-132">The Windows Search Indexer trims the final slash from URLs.</span></span> <span data-ttu-id="06f29-133">Daher können Sie sich nicht darauf verlassen, dass ein abschließender Schrägstrich vorhanden ist, um ein Verzeichnis im Vergleich zu einem Element zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="06f29-133">As a result you cannot rely on the existence of a final slash to identify a directory versus an item.</span></span> <span data-ttu-id="06f29-134">Der Protokollhandler muss diese URL-Syntax verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="06f29-134">Your protocol handler must be able to handle this URL syntax.</span></span> <span data-ttu-id="06f29-135">Stellen Sie sicher, dass der Protokoll Name, den Sie zur Identifizierung der shelldatenquelle ausgewählt haben, nicht mit den aktuellen Konflikten in Konflikt steht.</span><span class="sxs-lookup"><span data-stu-id="06f29-135">Ensure that the protocol name that you select to identify your Shell data source does not conflict with current ones.</span></span> <span data-ttu-id="06f29-136">Diese Benennungs Konvention wird empfohlen: `companyName.scheme` .</span><span class="sxs-lookup"><span data-stu-id="06f29-136">We recommend this naming convention: `companyName.scheme`.</span></span>

<span data-ttu-id="06f29-137">Weitere Informationen zum Erstellen einer shelldatenquelle finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="06f29-137">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

## <a name="implementing-protocol-handler-interfaces"></a><span data-ttu-id="06f29-138">Implementieren von protokollhandlerschnittstellen</span><span class="sxs-lookup"><span data-stu-id="06f29-138">Implementing Protocol Handler Interfaces</span></span>

<span data-ttu-id="06f29-139">Das Erstellen eines Protokoll Handlers erfordert die Implementierung der folgenden drei Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="06f29-139">Creating a protocol handler requires the implementation of the following three interfaces:</span></span>

-   <span data-ttu-id="06f29-140">[**Isearchprotocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) zum Verwalten von urlaccessor-Objekten.</span><span class="sxs-lookup"><span data-stu-id="06f29-140">[**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects.</span></span>
-   <span data-ttu-id="06f29-141">[**Iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) , um Eigenschaften verfügbar zu machen und geeignete Filter für Elemente in der shelldatenquelle zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="06f29-141">[**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) to expose properties and identify appropriate filters for items in the Shell data source.</span></span>
-   <span data-ttu-id="06f29-142">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) zum Filtern von proprietären Dateien oder zum Auflisten und Filtern hierarchisch gespeicherter Dateien.</span><span class="sxs-lookup"><span data-stu-id="06f29-142">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span>

<span data-ttu-id="06f29-143">Die anderen Schnittstellen sind optional, außer den drei obligatorischen aufgelisteten Schnittstellen, sind optional, und Sie haben die Wahl, welche optionalen Schnittstellen für die jeweilige Aufgabe am besten geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="06f29-143">Other than the three mandatory interfaces listed, the other interfaces are optional, and you are at liberty to implement whichever optional interfaces are most appropriate for the task at hand.</span></span>

### <a name="isearchprotocol-and-isearchprotocol2"></a><span data-ttu-id="06f29-144">Isearchprotocol und ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="06f29-144">ISearchProtocol and ISearchProtocol2</span></span>

<span data-ttu-id="06f29-145">Die searchprotocol-Schnittstellen initialisieren und verwalten die urlaccessor-Objekte des Protokoll Handlers.</span><span class="sxs-lookup"><span data-stu-id="06f29-145">The SearchProtocol interfaces initialize and manage your protocol handler UrlAccessor objects.</span></span> <span data-ttu-id="06f29-146">Die [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) -Schnittstelle ist eine optionale Erweiterung von [**isearchprotocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)und umfasst eine zusätzliche Methode, um weitere Informationen über den Benutzer und das Element anzugeben.</span><span class="sxs-lookup"><span data-stu-id="06f29-146">The [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) interface is an optional extension of [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol), and includes an extra method to specify more information about the user and the item.</span></span>

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a><span data-ttu-id="06f29-147">Iurlaccessor, IUrlAccessor2, IUrlAccessor3 und IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="06f29-147">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>

<span data-ttu-id="06f29-148">Die [**iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) -Schnittstellen werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="06f29-148">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces are described in the following table.</span></span>



| <span data-ttu-id="06f29-149">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="06f29-149">Interface</span></span>                                                 | <span data-ttu-id="06f29-150">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06f29-150">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06f29-151">**Iurlaccessor**</span><span class="sxs-lookup"><span data-stu-id="06f29-151">**IUrlAccessor**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | <span data-ttu-id="06f29-152">Für eine angegebene URL bietet die [**iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) -Schnittstelle Zugriff auf die Eigenschaften des Elements, das in der URL verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="06f29-152">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interface provides access to the properties of the item that is exposed in the URL.</span></span> <span data-ttu-id="06f29-153">Diese Eigenschaften können auch an einen protokollhandlerspezifischen Filter gebunden werden (d. h., es handelt sich um einen anderen Filter als den, der dem Dateinamen zugeordnet ist).</span><span class="sxs-lookup"><span data-stu-id="06f29-153">It can also bind those properties to a protocol handler-specific filter (that is, a filter other than the one associated with the file name).</span></span> |
| <span data-ttu-id="06f29-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (optional)</span><span class="sxs-lookup"><span data-stu-id="06f29-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (optional)</span></span> | <span data-ttu-id="06f29-155">Die [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) -Schnittstelle erweitert [**iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) mit Methoden, die eine Codepage für die Eigenschaften des Elements und seine Anzeige-URL erhalten und den Typ des Elements in der URL (Dokument oder Verzeichnis) erhalten.</span><span class="sxs-lookup"><span data-stu-id="06f29-155">The [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) interface extends [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) with methods that get a code page for the item's properties and its display URL, and that get the type of item in the URL (document or directory).</span></span>                                    |
| <span data-ttu-id="06f29-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (optional)</span><span class="sxs-lookup"><span data-stu-id="06f29-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (optional)</span></span> | <span data-ttu-id="06f29-157">Die [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) -Schnittstelle erweitert [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) mit einer Methode, die ein Array von Benutzer-SIDs abruft, sodass der Such Protokoll Host die Identität dieser Benutzer annimmt, um das Element zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="06f29-157">The [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface extends [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) with a method that gets an array of user SIDs, enabling the search protocol host to impersonate these users to index the item.</span></span>                                                      |
| <span data-ttu-id="06f29-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (optional)</span><span class="sxs-lookup"><span data-stu-id="06f29-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (optional)</span></span> | <span data-ttu-id="06f29-159">Die [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) -Schnittstelle erweitert die Funktionalität der [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) -Schnittstelle mit einer Methode, die angibt, ob der Inhalt des Elements indiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="06f29-159">The [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) interface extends the functionality of the [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface with a method that identifies whether the content of the item should be indexed.</span></span>                                                                 |



 

<span data-ttu-id="06f29-160">Das urlaccessor-Objekt wird von einem searchprotocol-Objekt instanziiert und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="06f29-160">The UrlAccessor object is instantiated and initialized by a SearchProtocol object.</span></span> <span data-ttu-id="06f29-161">Die [**iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) -Schnittstellen ermöglichen den Zugriff auf wichtige Informationen mithilfe der in der folgenden Tabelle beschriebenen Methoden.</span><span class="sxs-lookup"><span data-stu-id="06f29-161">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces provide access to important pieces of information through the methods described in the following table.</span></span>



| <span data-ttu-id="06f29-162">Methode</span><span class="sxs-lookup"><span data-stu-id="06f29-162">Method</span></span>                                                                                        | <span data-ttu-id="06f29-163">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06f29-163">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06f29-164">**Iurlaccessor:: getLastModified**</span><span class="sxs-lookup"><span data-stu-id="06f29-164">**IUrlAccessor::GetLastModified**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | <span data-ttu-id="06f29-165">Gibt die Uhrzeit zurück, zu der die URL zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="06f29-165">Returns the time that the URL was last modified.</span></span> <span data-ttu-id="06f29-166">Wenn diese Zeit aktueller ist als der letzte Zeitpunkt, zu dem der Indexer diese URL verarbeitet hat, werden Filter Handler (Implementierungen der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle) aufgerufen, um die (möglicherweise) geänderten Daten für dieses Element zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="06f29-166">If this time is more recent than the last time the indexer processed this URL, filter handlers (implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) are called to extract the (possibly) changed data for that item.</span></span> <span data-ttu-id="06f29-167">Geänderte Zeiten für Verzeichnisse werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="06f29-167">Modified times for directories are ignored.</span></span> |
| [<span data-ttu-id="06f29-168">**Iurlaccessor:: IsDirectory**</span><span class="sxs-lookup"><span data-stu-id="06f29-168">**IUrlAccessor::IsDirectory**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | <span data-ttu-id="06f29-169">Gibt an, ob die URL einen Ordner mit untergeordneten URLs darstellt.</span><span class="sxs-lookup"><span data-stu-id="06f29-169">Identifies whether the URL represents a folder containing a child URLs.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="06f29-170">**Iurlaccessor:: BindTo Stream**</span><span class="sxs-lookup"><span data-stu-id="06f29-170">**IUrlAccessor::BindToStream**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | <span data-ttu-id="06f29-171">Bindet an eine [IStream-Schnittstelle](/windows/win32/api/objidl/nn-objidl-istream) , die die Daten einer Datei in einem benutzerdefinierten Datenspeicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="06f29-171">Binds to an [IStream interface](/windows/win32/api/objidl/nn-objidl-istream) that represents the data of a file in a custom data store.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="06f29-172">**Iurlaccessor:: BindTo Filter**</span><span class="sxs-lookup"><span data-stu-id="06f29-172">**IUrlAccessor::BindToFilter**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | <span data-ttu-id="06f29-173">Bindet an einen protokollhandlerspezifischen [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), der Eigenschaften für das Element verfügbar machen kann.</span><span class="sxs-lookup"><span data-stu-id="06f29-173">Binds to a protocol handler-specific [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), which can expose properties for the item.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="06f29-174">**IUrlAccessor4:: Schultern**</span><span class="sxs-lookup"><span data-stu-id="06f29-174">**IUrlAccessor4::ShouldIndexItemContent**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | <span data-ttu-id="06f29-175">Gibt an, ob der Inhalt des Elements indiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="06f29-175">Identifies whether the content of the item should be indexed.</span></span>                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a><span data-ttu-id="06f29-176">Iprotocolhandlersite</span><span class="sxs-lookup"><span data-stu-id="06f29-176">IProtocolHandlerSite</span></span>

<span data-ttu-id="06f29-177">Die [**iprotocolhandlersite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) -Schnittstelle wird verwendet, um einen Filter Handler zu instanziieren, der in einem isolierten Prozess gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="06f29-177">The [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) interface is used to instantiate a filter handler, which is hosted in an isolated process.</span></span> <span data-ttu-id="06f29-178">Der geeignete Filter Handler wird für eine angegebene CLSID (persistente Klassen-ID), Dokument Speicher Klasse oder Dateinamenerweiterung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="06f29-178">The appropriate filter handler is obtained for a specified persistent class identifier (CLSID), document storage class, or file name extension.</span></span> <span data-ttu-id="06f29-179">Der Vorteil, dass der Host Prozess an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) gebunden werden muss, besteht darin, dass der Host Prozess den Prozess des Auffinden eines geeigneten Filter Handlers verwalten und die beim Aufrufen des Handlers beteiligte Sicherheit steuern kann.</span><span class="sxs-lookup"><span data-stu-id="06f29-179">The benefit of asking the host process to bind to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is that the host process can manage the process of locating an appropriate filter handler, and control the security involved in calling the handler.</span></span>

## <a name="implementing-filter-handlers-for-containers"></a><span data-ttu-id="06f29-180">Implementieren von Filter Handlern für Container</span><span class="sxs-lookup"><span data-stu-id="06f29-180">Implementing Filter Handlers for Containers</span></span>

<span data-ttu-id="06f29-181">Wenn Sie einen hierarchischen Protokollhandler implementieren, müssen Sie einen Filter Handler für einen Container implementieren, der untergeordnete URLs auflistet.</span><span class="sxs-lookup"><span data-stu-id="06f29-181">If you are implementing a hierarchical protocol handler, then you must implement a filter handler for a container that enumerates child URLs.</span></span> <span data-ttu-id="06f29-182">Ein Filter Handler ist eine Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="06f29-182">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span> <span data-ttu-id="06f29-183">Der enumerationsprozess ist eine Schleife durch die [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) -Methode und die [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) -Methode der **IFilter** -Schnittstelle. Jede untergeordnete URL wird als Wert der-Eigenschaft verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="06f29-183">The enumeration process is a loop through the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) and [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) methods of the **IFilter** interface; each child URL is exposed as the value of the property.</span></span>

<span data-ttu-id="06f29-184">[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) gibt die Eigenschaften des Containers zurück.</span><span class="sxs-lookup"><span data-stu-id="06f29-184">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns the properties of the container.</span></span> <span data-ttu-id="06f29-185">Um untergeordnete URLs aufzulisten, gibt **IFilter:: GetChunk** einen der folgenden zurück:</span><span class="sxs-lookup"><span data-stu-id="06f29-185">To enumerate child URLs, **IFilter::GetChunk** returns either of the following:</span></span>

-   <span data-ttu-id="06f29-186">[Pkey \_ \_Urlyindex durchsuchen](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="06f29-186">[PKEY\_Search\_UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):</span></span>

    <span data-ttu-id="06f29-187">Die URL des Elements ohne den Zeitpunkt der letzten Änderung.</span><span class="sxs-lookup"><span data-stu-id="06f29-187">The URL to the item without the last modified time.</span></span> <span data-ttu-id="06f29-188">[**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) gibt eine PROPVARIANT zurück, die die untergeordnete URL enthält.</span><span class="sxs-lookup"><span data-stu-id="06f29-188">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing the child URL.</span></span>

-   <span data-ttu-id="06f29-189">[Pkey \_ Suchen Sie \_ urldeindexwithmodificationtime](../properties/props-system-search-urltoindexwithmodificationtime.md):</span><span class="sxs-lookup"><span data-stu-id="06f29-189">[PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):</span></span>

    <span data-ttu-id="06f29-190">Die URL und die Uhrzeit der letzten Änderung.</span><span class="sxs-lookup"><span data-stu-id="06f29-190">The URL and the last modified time.</span></span> <span data-ttu-id="06f29-191">[**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) gibt eine PROPVARIANT zurück, die einen Vektor der untergeordneten URL und der Uhrzeit der letzten Änderung enthält.</span><span class="sxs-lookup"><span data-stu-id="06f29-191">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing a vector of the child URL and the last modified time.</span></span>

<span data-ttu-id="06f29-192">Das Zurückgeben der [pkey- \_ Suche \_ urltoindexwithmodificationtime](../properties/props-system-search-urltoindexwithmodificationtime.md) ist effizienter, da der Indexer sofort ermitteln kann, ob das Element indiziert werden muss, ohne die Methoden [**isearchprotocol:: CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) und [**iurlaccessor:: getLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) aufrufen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="06f29-192">Returning [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the [**ISearchProtocol::CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) and [**IUrlAccessor::GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) methods.</span></span>

<span data-ttu-id="06f29-193">Im folgenden Beispielcode wird veranschaulicht, wie die Eigenschaft " [ \_ \_ urltoindexwithmodificationtime" der pkey-Suche](../properties/props-system-search-urltoindexwithmodificationtime.md) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="06f29-193">The following example code demonstrates how to return the [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) property.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="06f29-194">Copyright (c) Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="06f29-194">Copyright (c) Microsoft Corporation.</span></span> <span data-ttu-id="06f29-195">Alle Rechte vorbehalten.</span><span class="sxs-lookup"><span data-stu-id="06f29-195">All rights reserved.</span></span>

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]  
> <span data-ttu-id="06f29-196">Eine [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Container Komponente sollte immer alle untergeordneten URLs auflisten, auch wenn sich die untergeordneten URLs nicht geändert haben, da der Indexer Löschungen durch den enumerationsprozess erkennt.</span><span class="sxs-lookup"><span data-stu-id="06f29-196">A container [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) component should always enumerate all child URLs even if the child URLs have not changed, because the indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="06f29-197">Wenn die Datums Ausgabe in einer [pkey- \_ Suche \_ urltoindexwithmodificationtime](../properties/props-system-search-urltoindexwithmodificationtime.md) angibt, dass die Daten nicht geändert wurden, aktualisiert der Indexer nicht die Daten für diese URL.</span><span class="sxs-lookup"><span data-stu-id="06f29-197">If the date output in a [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

## <a name="installing-and-registering-a-protocol-handler"></a><span data-ttu-id="06f29-198">Installieren und Registrieren eines Protokoll Handlers</span><span class="sxs-lookup"><span data-stu-id="06f29-198">Installing and Registering a Protocol Handler</span></span>

<span data-ttu-id="06f29-199">Das Installieren von Protokoll Handlern umfasst das Kopieren der dll (s) an einen geeigneten Speicherort im Verzeichnis "Programme" und das anschließende Registrieren der dll (s).</span><span class="sxs-lookup"><span data-stu-id="06f29-199">Installing protocol handlers involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the DLL(s).</span></span> <span data-ttu-id="06f29-200">Protokollhandler sollten die Selbstregistrierung für die Installation implementieren.</span><span class="sxs-lookup"><span data-stu-id="06f29-200">Protocol handlers should implement self-registration for installation.</span></span> <span data-ttu-id="06f29-201">Die Installationsanwendung kann auch einen Such Stamm und Bereichs Regeln hinzufügen, um einen Standard-Crawlen Bereich für die Shell-Datenquelle zu definieren. Dies wird unter [sicherstellen, dass ihre Elemente](#ensuring-that-your-items-are-indexed) am Ende dieses Themas indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="06f29-201">The installation application can also add a search root, and scope rules to define a default crawl scope for the Shell data source, which is discussed in [Ensuring that Your Items are Indexed](#ensuring-that-your-items-are-indexed) at the end of this topic.</span></span>

### <a name="guidelines-for-registering-a-protocol-handler"></a><span data-ttu-id="06f29-202">Richtlinien zum Registrieren eines Protokoll Handlers</span><span class="sxs-lookup"><span data-stu-id="06f29-202">Guidelines for Registering a Protocol Handler</span></span>

<span data-ttu-id="06f29-203">Beachten Sie beim Registrieren eines Protokoll Handlers die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="06f29-203">You should follow these guidelines when registering a protocol handler:</span></span>

-   <span data-ttu-id="06f29-204">Das Installationsprogramm muss entweder exe oder das MSI-Installationsprogramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="06f29-204">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="06f29-205">Anmerkungen zu dieser Version müssen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="06f29-205">Release notes must be provided.</span></span>
-   <span data-ttu-id="06f29-206">Ein Eintrag zum Hinzufügen/Entfernen von Programmen muss für jedes installierte Add-in erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="06f29-206">An Add/Remove Programs entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="06f29-207">Das Installationsprogramm muss alle Registrierungs Einstellungen für einen bestimmten Dateityp oder-Speicher übernehmen, den das aktuelle Add-in versteht.</span><span class="sxs-lookup"><span data-stu-id="06f29-207">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="06f29-208">Wenn ein vorheriges Add-in überschrieben wird, sollte das Installationsprogramm den Benutzer benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="06f29-208">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="06f29-209">Wenn das vorherige Add-in von einem neueren Add-in überschrieben wurde, sollte es möglich sein, die vorherige Add-in-Funktionalität wiederherzustellen und das Standard-Add-in für diesen Dateityp erneut zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="06f29-209">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>
-   <span data-ttu-id="06f29-210">Das Installationsprogramm sollte einen Standard Durchforstungs Bereich für den Indexer definieren, indem er mithilfe von Crawl Scope Manager (CSM) einen Such Stamm und Bereichs Regeln hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="06f29-210">The installer should define a default crawl scope for the indexer by adding a search root, and scope rules using the Crawl Scope Manager (CSM).</span></span>

### <a name="registering-a-protocol-handler"></a><span data-ttu-id="06f29-211">Registrieren eines Protokoll Handlers</span><span class="sxs-lookup"><span data-stu-id="06f29-211">Registering a Protocol Handler</span></span>

<span data-ttu-id="06f29-212">Sie müssen 14 Einträge in der Registrierung vornehmen, um die Protokollhandlerkomponente zu registrieren, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="06f29-212">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="06f29-213">*Ver \_ IND \_ ProgID* ist die Versions unabhängige ProgID der protokollhandlerimplementierung.</span><span class="sxs-lookup"><span data-stu-id="06f29-213">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="06f29-214">*Ver \_ DEP \_ ProgID* ist die Versions abhängige ProgID der protokollhandlerimplementierung.</span><span class="sxs-lookup"><span data-stu-id="06f29-214">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="06f29-215">*CLSID \_ 1* ist die CLSID der protokollhandlerimplementierung.</span><span class="sxs-lookup"><span data-stu-id="06f29-215">*CLSID\_1* is the CLSID of the protocol handler implementation.</span></span>

<span data-ttu-id="06f29-216">**So registrieren Sie einen Protokollhandler:**</span><span class="sxs-lookup"><span data-stu-id="06f29-216">**To register a protocol handler:**</span></span>

1.  <span data-ttu-id="06f29-217">Registrieren Sie die Versions unabhängige ProgID mit den folgenden Schlüsseln und Werten:</span><span class="sxs-lookup"><span data-stu-id="06f29-217">Register the version independent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  <span data-ttu-id="06f29-218">Registrieren Sie die Versions abhängige ProgID mit den folgenden Schlüsseln und Werten:</span><span class="sxs-lookup"><span data-stu-id="06f29-218">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="06f29-219">Registrieren Sie die CLSID des Protokoll Handlers mit den folgenden Schlüsseln und Werten:</span><span class="sxs-lookup"><span data-stu-id="06f29-219">Register the protocol handler's CLSID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  <span data-ttu-id="06f29-220">Registrieren Sie den Protokollhandler bei Windows Search.</span><span class="sxs-lookup"><span data-stu-id="06f29-220">Register the protocol handler with Windows Search.</span></span> <span data-ttu-id="06f29-221">Im folgenden Beispiel <Protocol Name> ist der Name des Protokolls, wie z. b. File, MAPI usw.:</span><span class="sxs-lookup"><span data-stu-id="06f29-221">In the following example, <Protocol Name> is the name of the protocol itself, such as file, mapi, and so forth:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    <span data-ttu-id="06f29-222">Vor Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="06f29-222">Prior to Windows Vista:</span></span>

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a><span data-ttu-id="06f29-223">Registrieren des Dateityp Handlers des Protokoll Handlers</span><span class="sxs-lookup"><span data-stu-id="06f29-223">Registering the Protocol Handler's File Type Handler</span></span>

<span data-ttu-id="06f29-224">Sie müssen zwei Einträge in der Registrierung vornehmen, um den Dateityp Handler des Protokoll Handlers zu registrieren (dieser wird auch als Shellerweiterung bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="06f29-224">You need to make two entries in the registry to register the protocol handler's file type handler (which is also known as a Shell extension).</span></span>

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a><span data-ttu-id="06f29-225">Sicherstellen, dass ihre Elemente indiziert werden</span><span class="sxs-lookup"><span data-stu-id="06f29-225">Ensuring that Your Items are Indexed</span></span>

<span data-ttu-id="06f29-226">Nachdem Sie den Protokollhandler implementiert haben, müssen Sie angeben, welche shellelemente der Protokollhandler indizieren soll.</span><span class="sxs-lookup"><span data-stu-id="06f29-226">After you have implemented your protocol handler, you must specify which Shell items your protocol handler is to index.</span></span> <span data-ttu-id="06f29-227">Sie können den Katalog-Manager verwenden, um die erneute Indizierung zu initiieren (Weitere Informationen finden Sie unter [Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md)).</span><span class="sxs-lookup"><span data-stu-id="06f29-227">You can use the Catalog Manager to initiate re-indexing (for more information, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md)).</span></span> <span data-ttu-id="06f29-228">Sie können auch den Crawl Scope Manager (CSM) zum Einrichten von Standardregeln verwenden, um die URLs anzugeben, die der Indexer durchforsten soll (Weitere Informationen finden Sie unter [Verwenden von Crawl Scope Manager](-search-3x-wds-extidx-csm.md) und [Verwalten von Bereichs Regeln](-search-3x-wds-extidx-csm-scoperules.md)).</span><span class="sxs-lookup"><span data-stu-id="06f29-228">Or you can also use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl (for more information, see [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md) and [Managing Scope Rules](-search-3x-wds-extidx-csm-scoperules.md)).</span></span> <span data-ttu-id="06f29-229">Sie können auch einen Suchstamm hinzufügen (Weitere Informationen finden Sie unter [Verwalten von Such](-search-3x-wds-extidx-csm-searchroots.md)Stämmen).</span><span class="sxs-lookup"><span data-stu-id="06f29-229">You can also add a search root (for more information, see [Managing Search Roots](-search-3x-wds-extidx-csm-searchroots.md)).</span></span> <span data-ttu-id="06f29-230">Eine weitere Option, die Ihnen zur Verfügung steht, ist die Vorgehensweise im Beispiel zum erneuten indizieren in den [Windows Search SDK-Beispielen](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="06f29-230">Another option available to you is to follow the procedure in the ReIndex sample in [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="06f29-231">Die [**isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) -Schnittstelle stellt Methoden bereit, die das Suchmodul von Containern zum durchforsten und/oder überwachen sowie Elemente unter diesen Containern Benachrichtigen, die beim Crawlen oder beim Zuschauen eingeschlossen oder ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="06f29-231">The [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.</span></span> <span data-ttu-id="06f29-232">In Windows 7 und höher erweitert [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) **isearchcrawlscopemanager** mit der [**ISearchCrawlScopeManager2:: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) -Methode, die die Version abruft, die Clients informiert, ob sich der Zustand des CSM geändert hat.</span><span class="sxs-lookup"><span data-stu-id="06f29-232">In Windows 7 and later, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) extends **ISearchCrawlScopeManager** with the [**ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) method that gets the version, which informs clients whether the state of the CSM has changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06f29-233">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06f29-233">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="06f29-234">**Licher**</span><span class="sxs-lookup"><span data-stu-id="06f29-234">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="06f29-235">Grundlegendes zu Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="06f29-235">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="06f29-236">Entwickeln von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="06f29-236">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="06f29-237">Benachrichtigen des Index von Änderungen</span><span class="sxs-lookup"><span data-stu-id="06f29-237">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="06f29-238">Hinzufügen von Symbolen und Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="06f29-238">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="06f29-239">Code Beispiel: Shellerweiterungen für Protokollhandler</span><span class="sxs-lookup"><span data-stu-id="06f29-239">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="06f29-240">Erstellen eines Suchconnector für einen Protokoll Handler</span><span class="sxs-lookup"><span data-stu-id="06f29-240">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="06f29-241">Debuggen von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="06f29-241">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
