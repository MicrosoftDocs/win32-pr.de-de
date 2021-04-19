---
description: Das ifiltersample-Codebeispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der IFilter-Schnittstelle erstellt wird.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: Ifiltersample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f66bf32c4abe25038aa6b2a3b6d879ba65cf7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346077"
---
# <a name="ifiltersample"></a><span data-ttu-id="c6013-103">Ifiltersample</span><span class="sxs-lookup"><span data-stu-id="c6013-103">IFilterSample</span></span>

<span data-ttu-id="c6013-104">Das ifiltersample-Codebeispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c6013-104">The IFilterSample code sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

<span data-ttu-id="c6013-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="c6013-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="c6013-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6013-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="c6013-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c6013-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="c6013-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="c6013-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="c6013-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c6013-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="c6013-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6013-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="c6013-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6013-111">Requirements</span></span>

| <span data-ttu-id="c6013-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="c6013-112">Product</span></span>     | <span data-ttu-id="c6013-113">Produktversion</span><span class="sxs-lookup"><span data-stu-id="c6013-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="c6013-114">Windows</span><span class="sxs-lookup"><span data-stu-id="c6013-114">Windows</span></span>     | <span data-ttu-id="c6013-115">Windows 7, 8.1 oder 10</span><span class="sxs-lookup"><span data-stu-id="c6013-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="c6013-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c6013-116">Windows SDK</span></span> | <span data-ttu-id="c6013-117">7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c6013-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="c6013-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c6013-118">Downloading the Sample</span></span>

<span data-ttu-id="c6013-119">Dieses Beispiel ist im folgenden Speicherort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c6013-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="c6013-120">Standort</span><span class="sxs-lookup"><span data-stu-id="c6013-120">Location</span></span>      | <span data-ttu-id="c6013-121">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="c6013-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="c6013-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="c6013-122">GitHub</span></span>        | [<span data-ttu-id="c6013-123">Ifiltersample</span><span class="sxs-lookup"><span data-stu-id="c6013-123">IFilterSample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> <span data-ttu-id="c6013-124">Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="c6013-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="c6013-125">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c6013-125">Building the Sample</span></span>

1. <span data-ttu-id="c6013-126">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **FilterBase** .</span><span class="sxs-lookup"><span data-stu-id="c6013-126">Open Windows Explorer and navigate to the **FilterBase** project directory.</span></span>
2. <span data-ttu-id="c6013-127">Doppelklicken Sie auf das Symbol für die Datei FilterBase. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c6013-127">Double-click the icon for the FilterBase.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="c6013-128">Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6013-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="c6013-129">Dies wirkt sich nicht auf das Verhalten des Beispiels aus.</span><span class="sxs-lookup"><span data-stu-id="c6013-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="c6013-130">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c6013-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c6013-131">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c6013-131">Running the Sample</span></span>

1. <span data-ttu-id="c6013-132">Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="c6013-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="c6013-133">Geben Sie an der Eingabeaufforderung ein, `FilterBase.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für FilterBase.exe.</span><span class="sxs-lookup"><span data-stu-id="c6013-133">At the command prompt, enter `FilterBase.exe`, or from Windows Explorer, double-click the icon for FilterBase.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6013-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6013-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="c6013-135">Referenz</span><span class="sxs-lookup"><span data-stu-id="c6013-135">Reference</span></span>

[<span data-ttu-id="c6013-136">**IFilter**</span><span class="sxs-lookup"><span data-stu-id="c6013-136">**IFilter**</span></span>](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a><span data-ttu-id="c6013-137">Konzept</span><span class="sxs-lookup"><span data-stu-id="c6013-137">Conceptual</span></span>

[<span data-ttu-id="c6013-138">Entwickeln von Filter Handlern</span><span class="sxs-lookup"><span data-stu-id="c6013-138">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

### <a name="other-samples"></a><span data-ttu-id="c6013-139">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6013-139">Other Samples</span></span>

[<span data-ttu-id="c6013-140">Code Beispiele durchsuchen</span><span class="sxs-lookup"><span data-stu-id="c6013-140">Search Code Samples</span></span>](-search-samples-ovw.md)
