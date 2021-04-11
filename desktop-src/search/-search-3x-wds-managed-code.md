---
description: Das Windows Search SDK stellt eine Interoperabilität Assembly bereit, damit Sie mit Component Object Model (com)-Objekten arbeiten können, die von Windows Search und anderen Programmen für die Schnittstellen und Klassen mit verwaltetem Code verfügbar gemacht werden.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Verwenden von verwaltetem Code mit Shelldaten und Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128608"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a><span data-ttu-id="00670-103">Verwenden von verwaltetem Code mit Shelldaten und Windows Search</span><span class="sxs-lookup"><span data-stu-id="00670-103">Using Managed Code with Shell Data and Windows Search</span></span>

<span data-ttu-id="00670-104">Das Windows Search SDK stellt eine Interoperabilität Assembly bereit, damit Sie mit Component Object Model (com)-Objekten arbeiten können, die von Windows Search und anderen Programmen für die Schnittstellen und Klassen mit verwaltetem Code verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="00670-104">The Windows Search SDK provides an interopability assembly for you to work with Component Object Model (COM) objects that are exposed by Windows Search and other programs against the interfaces and classes using managed code.</span></span> <span data-ttu-id="00670-105">Die Interoperabilität-Assembly wird von Microsoft digital signiert und kann mit den [Windows-Such Beispielen](-search-samples-ovw.md)gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="00670-105">The interopability assembly is digitally signed by Microsoft and can be found with the [Windows Search samples](-search-samples-ovw.md).</span></span>

<span data-ttu-id="00670-106">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="00670-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="00670-107">Verwenden der Windows-API-codepack</span><span class="sxs-lookup"><span data-stu-id="00670-107">Using the Windows API CodePack</span></span>](#using-the-windows-api-codepack)
    -   [<span data-ttu-id="00670-108">Zugreifen auf Index Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="00670-108">Accessing Index Results</span></span>](#accessing-index-results)
    -   [<span data-ttu-id="00670-109">Beispielanwendung mit der Windows-API-codepack</span><span class="sxs-lookup"><span data-stu-id="00670-109">Sample Application Using the Windows API Codepack</span></span>](#sample-application-using-the-windows-api-codepack)
-   [<span data-ttu-id="00670-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00670-110">Related topics</span></span>](#related-topics)

## <a name="using-the-windows-api-codepack"></a><span data-ttu-id="00670-111">Verwenden der Windows-API-codepack</span><span class="sxs-lookup"><span data-stu-id="00670-111">Using the Windows API CodePack</span></span>

<span data-ttu-id="00670-112">Wenn Sie in der Microsoft .NET-Umgebung arbeiten, verwenden Sie das [Windows-API-Code Paket für Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) , um Suchergebnisse zu erhalten, oder Durchsuchen Sie einfach den-Namespace.</span><span class="sxs-lookup"><span data-stu-id="00670-112">If you are working in the Microsoft .NET environment, use the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) to obtain search results, or just browse the namespace.</span></span> <span data-ttu-id="00670-113">Das [Windows-API-Code Paket für Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) stellt eine Sammlung von shellelementen bereit, die im Grunde Wrapper um die native [IShellItem-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem)sind.</span><span class="sxs-lookup"><span data-stu-id="00670-113">The [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) provides you with a collection of Shell items that are essentially wrappers around the native [IShellItem Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem).</span></span> <span data-ttu-id="00670-114">Sie können diese Auflistung durchlaufen und die verschiedenen Eigenschaftswerte auf ähnliche Weise wie die Ergebnisse in einer Tabelle aus einer Objekt Verknüpfungs-und Einbettungs Datenbank (OLE DB) aufzählen.</span><span class="sxs-lookup"><span data-stu-id="00670-114">You can iterate over this collection and get the various property values in a fashion similar to how you would enumerate the results in a table from an Object Linking and Embedding Database (OLE DB) query.</span></span>

<span data-ttu-id="00670-115">Der folgende Code Ausschnitt veranschaulicht, wie Sie Such Elemente durchlaufen und die Eigenschaftswerte für jedes Element abrufen können.</span><span class="sxs-lookup"><span data-stu-id="00670-115">The following code snippet illustrates how to iterate over Search items and obtain the property values for each.</span></span>


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a><span data-ttu-id="00670-116">Zugreifen auf Index Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="00670-116">Accessing Index Results</span></span>

<span data-ttu-id="00670-117">Sie können entweder über OLE DB oder das shelldatenmodell auf Index Ergebnisse zugreifen.</span><span class="sxs-lookup"><span data-stu-id="00670-117">You can access index results through either OLE DB or the Shell data model.</span></span> <span data-ttu-id="00670-118">Bei beiden Ansätzen gibt es vor-und Nachteile.</span><span class="sxs-lookup"><span data-stu-id="00670-118">There are advantages and disadvantages with either approach.</span></span> <span data-ttu-id="00670-119">Ein Vorteil besteht darin, dass OLE DB und Structured Query Language (SQL) den Daten Bank Programmierern vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="00670-119">One advantage is that OLE DB and Structured Query Language (SQL) are familiar to database programmers.</span></span> <span data-ttu-id="00670-120">Andere Vorteile sind eine bessere Kontrolle über die Leistung, wenn nur der Indexer abgefragt wird, sowie der Zugriff auf zusätzliche Funktionen, wie z. b. die Möglichkeit, vorherige Ergebnisse schnell in einem neuen Rowset zu finden.</span><span class="sxs-lookup"><span data-stu-id="00670-120">Other advantages are better control over performance when querying only the indexer, and access to additional functionality such as the ability to locate previous results in a new rowset quickly.</span></span>

<span data-ttu-id="00670-121">Der Vorteil des shelldatenmodells besteht darin, dass es sich über verschiedene Informationsquellen wie z. b. OpenSearch zusammenfasst und den Zugriff auf zusätzliche Funktionen ermöglicht, wie z. b. Miniaturansichten und Eigenschaften Handler.</span><span class="sxs-lookup"><span data-stu-id="00670-121">Advantages of the Shell data model are that it abstracts across different sources of information such as OpenSearch, and provides access to additional functionality such as thumbnails and property handlers.</span></span> <span data-ttu-id="00670-122">Außerdem erfordert das shellobjektmodell keine besondere Unterstützung für nicht-Dateinamen, wie z. b. e-Mail-Elemente und OneNote-Ergebnisse, sowie für Elemente, die sich im Index des Benutzers befinden.</span><span class="sxs-lookup"><span data-stu-id="00670-122">Nor does the Shell object model require special case support for non-filename results such as mail items and OneNote results, nor for any item that resides in the user's index.</span></span> <span data-ttu-id="00670-123">Beachten Sie, dass in Shell [KNOWNFOLDERID](../shell/knownfolderid.md) der bekannte Ordner Bereich für lokale indizierte Inhalte ist.</span><span class="sxs-lookup"><span data-stu-id="00670-123">Note that in Shell [KNOWNFOLDERID](../shell/knownfolderid.md) is the known folder scope for local indexed content.</span></span> <span data-ttu-id="00670-124">Weitere Informationen zum Erstellen einer shelldatenquelle finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00670-124">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="00670-125">OpenSearch-Datenquellen werden nicht über OLE DB für die Verbund Suche in Windows 7 und höher verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="00670-125">OpenSearch data sources are not exposed through OLE DB for federated search in Windows 7 and later.</span></span> <span data-ttu-id="00670-126">Aus diesem Grund empfiehlt es sich, einen LINQ-Anbieter für den Shellnamespace zu schreiben, anstatt OLE DB für den Zugriff auf die indexerergebnisse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="00670-126">For this reason we recommend that you consider writing a LINQ provider for the Shell namespace instead of using OLE DB to access the indexer results.</span></span> <span data-ttu-id="00670-127">Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Erstellen eines iquerable LINQ-Anbieters](/previous-versions/bb546158(v=vs.140)).</span><span class="sxs-lookup"><span data-stu-id="00670-127">For more information, see [Walkthrough: Creating an IQueryable LINQ Provider](/previous-versions/bb546158(v=vs.140)).</span></span>

### <a name="sample-application-using-the-windows-api-codepack"></a><span data-ttu-id="00670-128">Beispielanwendung mit der Windows-API-codepack</span><span class="sxs-lookup"><span data-stu-id="00670-128">Sample Application Using the Windows API Codepack</span></span>

<span data-ttu-id="00670-129">Der folgende Screenshot zeigt ein Mock einer Beispielanwendung, die mit dem [Windows-API-Code Pack für Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="00670-129">The following screenshot represents a mock up of a sample application created with the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span></span>

![Screenshot der Media Player-Anwendung mit e-Mail-Nachrichten](images/folderid-searchhome.png)

## <a name="related-topics"></a><span data-ttu-id="00670-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00670-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="00670-132">**Licher**</span><span class="sxs-lookup"><span data-stu-id="00670-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="00670-133">Verbundsuche in Windows 10</span><span class="sxs-lookup"><span data-stu-id="00670-133">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

<span data-ttu-id="00670-134">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="00670-134">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="00670-135">[Sprachübergreifende Interoperabilität](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="00670-135">[Cross-Language Interoperability](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span></span>
</dt> </dl>

 

 
