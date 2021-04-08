---
description: Das wsoledb-Codebeispiel veranschaulicht Active Template Library (ATL)-OLE DB Zugriff auf Windows Search-Anwendungen und zeigt zwei zusätzliche Methoden zum Abrufen von Ergebnissen aus der Windows-Suche.
ms.assetid: c81bf3af-e023-4384-8c89-0fa9c8f08773
title: Wsoledb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cecfc308fdfa9af796e64ab8bc6273f9c4d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862163"
---
# <a name="wsoledb"></a><span data-ttu-id="90484-103">Wsoledb</span><span class="sxs-lookup"><span data-stu-id="90484-103">WSOleDB</span></span>

<span data-ttu-id="90484-104">Das wsoledb-Codebeispiel veranschaulicht Active Template Library (ATL)-OLE DB Zugriff auf Windows Search-Anwendungen und zeigt zwei zusätzliche Methoden zum Abrufen von Ergebnissen aus der Windows-Suche.</span><span class="sxs-lookup"><span data-stu-id="90484-104">The WSOleDB code sample demonstrates Active Template Library (ATL) OLE DB access to Windows Search applications, and demonstrates two additional methods for retrieving results from Windows Search.</span></span>

<span data-ttu-id="90484-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="90484-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="90484-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90484-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="90484-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="90484-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="90484-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="90484-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="90484-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="90484-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="90484-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90484-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="90484-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90484-111">Requirements</span></span>

| <span data-ttu-id="90484-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="90484-112">Product</span></span>     | <span data-ttu-id="90484-113">Produktversion</span><span class="sxs-lookup"><span data-stu-id="90484-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="90484-114">Windows</span><span class="sxs-lookup"><span data-stu-id="90484-114">Windows</span></span>     | <span data-ttu-id="90484-115">Windows 7, 8.1 oder 10</span><span class="sxs-lookup"><span data-stu-id="90484-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="90484-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="90484-116">Windows SDK</span></span> | <span data-ttu-id="90484-117">7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="90484-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="90484-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="90484-118">Downloading the Sample</span></span>

<span data-ttu-id="90484-119">Dieses Beispiel ist im folgenden Speicherort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90484-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="90484-120">Standort</span><span class="sxs-lookup"><span data-stu-id="90484-120">Location</span></span>      | <span data-ttu-id="90484-121">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="90484-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="90484-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="90484-122">GitHub</span></span>        | [<span data-ttu-id="90484-123">Wsoledb-Beispiel</span><span class="sxs-lookup"><span data-stu-id="90484-123">WSOleDB sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSOleDB)         |

> [!NOTE]  
> <span data-ttu-id="90484-124">Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="90484-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="90484-125">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="90484-125">Building the Sample</span></span>

1. <span data-ttu-id="90484-126">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis von **wsoledb** .</span><span class="sxs-lookup"><span data-stu-id="90484-126">Open Windows Explorer and navigate to the **WSOleDB** project directory.</span></span>
2. <span data-ttu-id="90484-127">Doppelklicken Sie auf das Symbol für die Datei wsoledb. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="90484-127">Double-click the icon for the WSOleDB.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="90484-128">Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen.</span><span class="sxs-lookup"><span data-stu-id="90484-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="90484-129">Dies wirkt sich nicht auf das Verhalten des Beispiels aus.</span><span class="sxs-lookup"><span data-stu-id="90484-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="90484-130">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="90484-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="90484-131">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="90484-131">Running the Sample</span></span>

1. <span data-ttu-id="90484-132">Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="90484-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="90484-133">Geben Sie an der Eingabeaufforderung ein, `WSOleDB.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für WSOleDB.exe.</span><span class="sxs-lookup"><span data-stu-id="90484-133">At the command prompt, enter `WSOleDB.exe`, or from Windows Explorer, double-click the icon for WSOleDB.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90484-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90484-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="90484-135">Referenz</span><span class="sxs-lookup"><span data-stu-id="90484-135">Reference</span></span>

[<span data-ttu-id="90484-136">**Isearchcatalogmanager**</span><span class="sxs-lookup"><span data-stu-id="90484-136">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="90484-137">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="90484-137">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="90484-138">**Isearchmanager**</span><span class="sxs-lookup"><span data-stu-id="90484-138">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="90484-139">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="90484-139">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)

### <a name="conceptual"></a><span data-ttu-id="90484-140">Konzept</span><span class="sxs-lookup"><span data-stu-id="90484-140">Conceptual</span></span>

[<span data-ttu-id="90484-141">Übersicht über OLE DB Programmierung</span><span class="sxs-lookup"><span data-stu-id="90484-141">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="90484-142">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="90484-142">Other Samples</span></span>

[<span data-ttu-id="90484-143">Code Beispiele durchsuchen</span><span class="sxs-lookup"><span data-stu-id="90484-143">Search Code Samples</span></span>](-search-samples-ovw.md)
