---
description: Das dsearch-Codebeispiel veranschaulicht, wie eine Klasse für eine statische Konsolenanwendung erstellt wird, um die Windows-Suche mithilfe der Microsoft. search. Interop-Assembly für isearchqueryhelper abzufragen.
ms.assetid: 9c09b1fe-c63e-4c6e-9c8b-f5e29cf0fe9e
title: Dsearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285596a8109361accd6b3adecf80ea98074e55e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343264"
---
# <a name="dsearch"></a><span data-ttu-id="d708c-103">Dsearch</span><span class="sxs-lookup"><span data-stu-id="d708c-103">DSearch</span></span>

<span data-ttu-id="d708c-104">Das dsearch-Codebeispiel veranschaulicht, wie eine Klasse für eine statische Konsolenanwendung erstellt wird, um die Windows-Suche mithilfe der Microsoft. search. Interop-Assembly für [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)abzufragen.</span><span class="sxs-lookup"><span data-stu-id="d708c-104">The DSearch code sample demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).</span></span>

<span data-ttu-id="d708c-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="d708c-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="d708c-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d708c-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="d708c-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d708c-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="d708c-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="d708c-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="d708c-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d708c-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="d708c-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d708c-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="d708c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d708c-111">Requirements</span></span>

| <span data-ttu-id="d708c-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="d708c-112">Product</span></span>     | <span data-ttu-id="d708c-113">Produktversion</span><span class="sxs-lookup"><span data-stu-id="d708c-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="d708c-114">Windows</span><span class="sxs-lookup"><span data-stu-id="d708c-114">Windows</span></span>     | <span data-ttu-id="d708c-115">Windows 7, 8.1 oder 10</span><span class="sxs-lookup"><span data-stu-id="d708c-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="d708c-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d708c-116">Windows SDK</span></span> | <span data-ttu-id="d708c-117">7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="d708c-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="d708c-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d708c-118">Downloading the Sample</span></span>

<span data-ttu-id="d708c-119">Dieses Beispiel ist im folgenden Speicherort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d708c-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="d708c-120">Standort</span><span class="sxs-lookup"><span data-stu-id="d708c-120">Location</span></span>      | <span data-ttu-id="d708c-121">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="d708c-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="d708c-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="d708c-122">GitHub</span></span>        | [<span data-ttu-id="d708c-123">Dsearch-Beispiel</span><span class="sxs-lookup"><span data-stu-id="d708c-123">DSearch sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/DSearch)         |

> [!NOTE]  
> <span data-ttu-id="d708c-124">Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="d708c-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="d708c-125">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d708c-125">Building the Sample</span></span>

1. <span data-ttu-id="d708c-126">Öffnen Sie Windows-Explorer, und navigieren Sie zum **dsearch** -Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="d708c-126">Open Windows Explorer and navigate to the **DSearch** project directory.</span></span>
2. <span data-ttu-id="d708c-127">Doppelklicken Sie auf das Symbol für die Datei dsearch. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d708c-127">Double-click the icon for the DSearch.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="d708c-128">Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen.</span><span class="sxs-lookup"><span data-stu-id="d708c-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="d708c-129">Dies wirkt sich nicht auf das Verhalten des Beispiels aus.</span><span class="sxs-lookup"><span data-stu-id="d708c-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="d708c-130">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="d708c-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d708c-131">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d708c-131">Running the Sample</span></span>

1. <span data-ttu-id="d708c-132">Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="d708c-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="d708c-133">Geben Sie an der Eingabeaufforderung ein, `DSearch.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für DSearch.exe.</span><span class="sxs-lookup"><span data-stu-id="d708c-133">At the command prompt, enter `DSearch.exe`, or from Windows Explorer, double-click the icon for DSearch.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d708c-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d708c-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="d708c-135">Referenz</span><span class="sxs-lookup"><span data-stu-id="d708c-135">Reference</span></span>

[<span data-ttu-id="d708c-136">**Isearchqueryhelper**</span><span class="sxs-lookup"><span data-stu-id="d708c-136">**ISearchQueryHelper**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

[<span data-ttu-id="d708c-137">**Isearchcatalogmanager**</span><span class="sxs-lookup"><span data-stu-id="d708c-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="d708c-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="d708c-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

### <a name="other-samples"></a><span data-ttu-id="d708c-139">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="d708c-139">Other Samples</span></span>

[<span data-ttu-id="d708c-140">Code Beispiele durchsuchen</span><span class="sxs-lookup"><span data-stu-id="d708c-140">Search Code Samples</span></span>](-search-samples-ovw.md)
