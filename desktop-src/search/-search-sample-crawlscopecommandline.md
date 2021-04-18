---
description: Das Codebeispiel crawlscopecommandline veranschaulicht, wie Befehlszeilenoptionen für CSM-Indizierungs Vorgänge (Crawl Scope Manager) definiert werden.
ms.assetid: 8c82fe18-8676-43d2-a3da-027a733ee0a4
title: Crawlscopecommandline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb770c44f82af320e2b39fe679b632cf03825e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344414"
---
# <a name="crawlscopecommandline"></a><span data-ttu-id="d3529-103">Crawlscopecommandline</span><span class="sxs-lookup"><span data-stu-id="d3529-103">CrawlScopeCommandLine</span></span>

<span data-ttu-id="d3529-104">Das Codebeispiel crawlscopecommandline veranschaulicht, wie Befehlszeilenoptionen für CSM-Indizierungs Vorgänge (Crawl Scope Manager) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d3529-104">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span>

<span data-ttu-id="d3529-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="d3529-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="d3529-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3529-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="d3529-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d3529-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="d3529-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="d3529-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="d3529-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d3529-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="d3529-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3529-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="d3529-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3529-111">Requirements</span></span>

| <span data-ttu-id="d3529-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="d3529-112">Product</span></span>     | <span data-ttu-id="d3529-113">Produktversion</span><span class="sxs-lookup"><span data-stu-id="d3529-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="d3529-114">Windows</span><span class="sxs-lookup"><span data-stu-id="d3529-114">Windows</span></span>     | <span data-ttu-id="d3529-115">Windows 7, 8.1 oder 10</span><span class="sxs-lookup"><span data-stu-id="d3529-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="d3529-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d3529-116">Windows SDK</span></span> | <span data-ttu-id="d3529-117">7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="d3529-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="d3529-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d3529-118">Downloading the Sample</span></span>

<span data-ttu-id="d3529-119">Dieses Beispiel ist im folgenden Speicherort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d3529-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="d3529-120">Standort</span><span class="sxs-lookup"><span data-stu-id="d3529-120">Location</span></span> | <span data-ttu-id="d3529-121">Pfad oder URL</span><span class="sxs-lookup"><span data-stu-id="d3529-121">Path or URL</span></span>                                                                |
|----------|----------------------------------------------------------------------------|
| <span data-ttu-id="d3529-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="d3529-122">GitHub</span></span>   |    [<span data-ttu-id="d3529-123">Crawlscopecommandline-Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3529-123">CrawlScopeCommandLine sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine)|

> [!NOTE]  
> <span data-ttu-id="d3529-124">Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="d3529-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="d3529-125">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d3529-125">Building the Sample</span></span>

1. <span data-ttu-id="d3529-126">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **crawlscopecommandline** .</span><span class="sxs-lookup"><span data-stu-id="d3529-126">Open Windows Explorer and navigate to the **CrawlScopeCommandLine** project directory.</span></span>
2. <span data-ttu-id="d3529-127">Doppelklicken Sie auf das Symbol für die Datei csmcmd. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d3529-127">Double-click the icon for the csmcmd.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="d3529-128">Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3529-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="d3529-129">Dies wirkt sich nicht auf das Verhalten des Beispiels aus.</span><span class="sxs-lookup"><span data-stu-id="d3529-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="d3529-130">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="d3529-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d3529-131">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d3529-131">Running the Sample</span></span>

1. <span data-ttu-id="d3529-132">Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="d3529-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="d3529-133">Geben Sie an der Eingabeaufforderung ein, `csmcmd.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für csmcmd.exe.</span><span class="sxs-lookup"><span data-stu-id="d3529-133">At the command prompt, enter `csmcmd.exe`, or from Windows Explorer, double-click the icon for csmcmd.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3529-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3529-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="d3529-135">Referenz</span><span class="sxs-lookup"><span data-stu-id="d3529-135">Reference</span></span>

[<span data-ttu-id="d3529-136">**Ienumsearchroots**</span><span class="sxs-lookup"><span data-stu-id="d3529-136">**IEnumSearchRoots**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)

[<span data-ttu-id="d3529-137">**Ienumsearchscoperules**</span><span class="sxs-lookup"><span data-stu-id="d3529-137">**IEnumSearchScopeRules**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)

[<span data-ttu-id="d3529-138">**Isearchcrawlscopemanager**</span><span class="sxs-lookup"><span data-stu-id="d3529-138">**ISearchCrawlScopeManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

[<span data-ttu-id="d3529-139">**ISearchCrawlScopeManager2**</span><span class="sxs-lookup"><span data-stu-id="d3529-139">**ISearchCrawlScopeManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)

[<span data-ttu-id="d3529-140">**Isearchroot**</span><span class="sxs-lookup"><span data-stu-id="d3529-140">**ISearchRoot**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)

[<span data-ttu-id="d3529-141">**Isearchscoperule**</span><span class="sxs-lookup"><span data-stu-id="d3529-141">**ISearchScopeRule**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)

[<span data-ttu-id="d3529-142">**Isearchcatalogmanager**</span><span class="sxs-lookup"><span data-stu-id="d3529-142">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="d3529-143">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="d3529-143">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="d3529-144">**Isearchmanager**</span><span class="sxs-lookup"><span data-stu-id="d3529-144">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

### <a name="other-samples"></a><span data-ttu-id="d3529-145">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3529-145">Other Samples</span></span>

[<span data-ttu-id="d3529-146">Code Beispiele durchsuchen</span><span class="sxs-lookup"><span data-stu-id="d3529-146">Search Code Samples</span></span>](-search-samples-ovw.md)
