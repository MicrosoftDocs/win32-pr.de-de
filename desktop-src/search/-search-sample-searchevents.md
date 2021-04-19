---
description: Das searchevents-Codebeispiel veranschaulicht, wie Indizierungs Ereignisse priorisiert werden.
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: Searchevents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21472d113694a41a3c7855c0fdaf8f2fa2b3b2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353027"
---
# <a name="searchevents"></a><span data-ttu-id="39954-103">Searchevents</span><span class="sxs-lookup"><span data-stu-id="39954-103">SearchEvents</span></span>

<span data-ttu-id="39954-104">Das searchevents-Codebeispiel veranschaulicht, wie Indizierungs Ereignisse priorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="39954-104">The SearchEvents code sample demonstrates how to prioritize indexing events.</span></span>

<span data-ttu-id="39954-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="39954-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="39954-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39954-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="39954-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="39954-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="39954-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="39954-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="39954-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="39954-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="39954-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39954-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="39954-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39954-111">Requirements</span></span>

| <span data-ttu-id="39954-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="39954-112">Product</span></span>     | <span data-ttu-id="39954-113">Produktversion</span><span class="sxs-lookup"><span data-stu-id="39954-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="39954-114">Windows</span><span class="sxs-lookup"><span data-stu-id="39954-114">Windows</span></span>     | <span data-ttu-id="39954-115">Windows 7, 8.1 oder 10</span><span class="sxs-lookup"><span data-stu-id="39954-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="39954-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="39954-116">Windows SDK</span></span> | <span data-ttu-id="39954-117">7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="39954-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="39954-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="39954-118">Downloading the Sample</span></span>

<span data-ttu-id="39954-119">Dieses Beispiel ist im folgenden Speicherort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="39954-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="39954-120">Standort</span><span class="sxs-lookup"><span data-stu-id="39954-120">Location</span></span>      | <span data-ttu-id="39954-121">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="39954-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="39954-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="39954-122">GitHub</span></span>        | [<span data-ttu-id="39954-123">Searchevents-Beispiel</span><span class="sxs-lookup"><span data-stu-id="39954-123">SearchEvents sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> <span data-ttu-id="39954-124">Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="39954-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="39954-125">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="39954-125">Building the Sample</span></span>

1. <span data-ttu-id="39954-126">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **searchevents** .</span><span class="sxs-lookup"><span data-stu-id="39954-126">Open Windows Explorer and navigate to the **SearchEvents** project directory.</span></span>
2. <span data-ttu-id="39954-127">Doppelklicken Sie auf das Symbol für die Datei Eventing. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="39954-127">Double-click the icon for the Eventing.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="39954-128">Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen.</span><span class="sxs-lookup"><span data-stu-id="39954-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="39954-129">Dies wirkt sich nicht auf das Verhalten des Beispiels aus.</span><span class="sxs-lookup"><span data-stu-id="39954-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="39954-130">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="39954-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="39954-131">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="39954-131">Running the Sample</span></span>

1. <span data-ttu-id="39954-132">Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="39954-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="39954-133">Geben Sie an der Eingabeaufforderung ein, `Eventing.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für Eventing.exe.</span><span class="sxs-lookup"><span data-stu-id="39954-133">At the command prompt, enter `Eventing.exe`, or from Windows Explorer, double-click the icon for Eventing.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39954-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39954-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="39954-135">Referenz</span><span class="sxs-lookup"><span data-stu-id="39954-135">Reference</span></span>

[<span data-ttu-id="39954-136">**IRow-tevents**</span><span class="sxs-lookup"><span data-stu-id="39954-136">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[<span data-ttu-id="39954-137">**Irowsetpriorisierung**</span><span class="sxs-lookup"><span data-stu-id="39954-137">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[<span data-ttu-id="39954-138">**Prioritäts \_ Stufe**</span><span class="sxs-lookup"><span data-stu-id="39954-138">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[<span data-ttu-id="39954-139">**rowevent- \_ Ausdruck ItemState**</span><span class="sxs-lookup"><span data-stu-id="39954-139">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[<span data-ttu-id="39954-140">**rowsertevent- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="39954-140">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a><span data-ttu-id="39954-141">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="39954-141">Other Samples</span></span>

[<span data-ttu-id="39954-142">Code Beispiele durchsuchen</span><span class="sxs-lookup"><span data-stu-id="39954-142">Search Code Samples</span></span>](-search-samples-ovw.md)
