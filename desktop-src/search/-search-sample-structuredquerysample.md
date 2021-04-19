---
description: Das structuredquerysample-Codebeispiel veranschaulicht, wie Zeilen aus der Konsole gelesen, mit dem System Schema analysiert und die resultierenden Bedingungs Strukturen angezeigt werden.
ms.assetid: 9bb56d80-670e-4b2b-bf3f-40d0a75a89b6
title: Structuredquerysample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64da74b56658f74b056c64c314a2986ddce45ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343240"
---
# <a name="structuredquerysample"></a><span data-ttu-id="0dbbe-103">Structuredquerysample</span><span class="sxs-lookup"><span data-stu-id="0dbbe-103">StructuredQuerySample</span></span>

<span data-ttu-id="0dbbe-104">Das structuredquerysample-Codebeispiel veranschaulicht, wie Zeilen aus der Konsole gelesen, mit dem System Schema analysiert und die resultierenden Bedingungs Strukturen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-104">The StructuredQuerySample code sample demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.</span></span>

<span data-ttu-id="0dbbe-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="0dbbe-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="0dbbe-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0dbbe-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="0dbbe-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="0dbbe-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="0dbbe-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="0dbbe-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="0dbbe-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="0dbbe-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="0dbbe-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0dbbe-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="0dbbe-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0dbbe-111">Requirements</span></span>

| <span data-ttu-id="0dbbe-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="0dbbe-112">Product</span></span>     | <span data-ttu-id="0dbbe-113">Produktversion</span><span class="sxs-lookup"><span data-stu-id="0dbbe-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="0dbbe-114">Windows</span><span class="sxs-lookup"><span data-stu-id="0dbbe-114">Windows</span></span>     | <span data-ttu-id="0dbbe-115">Windows 7, 8.1 oder 10</span><span class="sxs-lookup"><span data-stu-id="0dbbe-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="0dbbe-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0dbbe-116">Windows SDK</span></span> | <span data-ttu-id="0dbbe-117">7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0dbbe-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="0dbbe-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="0dbbe-118">Downloading the Sample</span></span>

<span data-ttu-id="0dbbe-119">Dieses Beispiel ist im folgenden Speicherort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="0dbbe-120">Standort</span><span class="sxs-lookup"><span data-stu-id="0dbbe-120">Location</span></span>      | <span data-ttu-id="0dbbe-121">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="0dbbe-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="0dbbe-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="0dbbe-122">GitHub</span></span>        | [<span data-ttu-id="0dbbe-123">Structuredquerysample</span><span class="sxs-lookup"><span data-stu-id="0dbbe-123">StructuredQuerySample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample)  |

> [!NOTE]  
> <span data-ttu-id="0dbbe-124">Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="0dbbe-125">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="0dbbe-125">Building the Sample</span></span>

1. <span data-ttu-id="0dbbe-126">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **structuredquerysample** .</span><span class="sxs-lookup"><span data-stu-id="0dbbe-126">Open Windows Explorer and navigate to the **StructuredQuerySample** project directory.</span></span>
2. <span data-ttu-id="0dbbe-127">Doppelklicken Sie auf das Symbol für die Datei structuredquerysample. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-127">Double-click the icon for the StructuredQuerySample.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="0dbbe-128">Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="0dbbe-129">Dies wirkt sich nicht auf das Verhalten des Beispiels aus.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="0dbbe-130">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0dbbe-131">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="0dbbe-131">Running the Sample</span></span>

1. <span data-ttu-id="0dbbe-132">Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="0dbbe-133">Geben Sie an der Eingabeaufforderung ein, `StructuredQuerySample.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für StructuredQuerySample.exe.</span><span class="sxs-lookup"><span data-stu-id="0dbbe-133">At the command prompt, enter `StructuredQuerySample.exe`, or from Windows Explorer, double-click the icon for StructuredQuerySample.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0dbbe-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0dbbe-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="0dbbe-135">Referenz</span><span class="sxs-lookup"><span data-stu-id="0dbbe-135">Reference</span></span>

[<span data-ttu-id="0dbbe-136">**Icondition**</span><span class="sxs-lookup"><span data-stu-id="0dbbe-136">**ICondition**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)

[<span data-ttu-id="0dbbe-137">**ICondition2**</span><span class="sxs-lookup"><span data-stu-id="0dbbe-137">**ICondition2**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)

[<span data-ttu-id="0dbbe-138">**Iconditionfactory**</span><span class="sxs-lookup"><span data-stu-id="0dbbe-138">**IConditionFactory**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)

[<span data-ttu-id="0dbbe-139">**IConditionFactory2**</span><span class="sxs-lookup"><span data-stu-id="0dbbe-139">**IConditionFactory2**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)

[<span data-ttu-id="0dbbe-140">**Iconditiongenerator**</span><span class="sxs-lookup"><span data-stu-id="0dbbe-140">**IConditionGenerator**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)

[<span data-ttu-id="0dbbe-141">**Iqueryparser**</span><span class="sxs-lookup"><span data-stu-id="0dbbe-141">**IQueryParser**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)

[<span data-ttu-id="0dbbe-142">**Iqueryparamesermanager**</span><span class="sxs-lookup"><span data-stu-id="0dbbe-142">**IQueryParserManager**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparsermanager)

[<span data-ttu-id="0dbbe-143">**Iquerysolution**</span><span class="sxs-lookup"><span data-stu-id="0dbbe-143">**IQuerySolution**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)

### <a name="other-samples"></a><span data-ttu-id="0dbbe-144">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="0dbbe-144">Other Samples</span></span>

[<span data-ttu-id="0dbbe-145">Code Beispiele durchsuchen</span><span class="sxs-lookup"><span data-stu-id="0dbbe-145">Search Code Samples</span></span>](-search-samples-ovw.md)
