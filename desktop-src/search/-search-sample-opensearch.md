---
description: Das OpenSearch-Codebeispiel veranschaulicht, wie ein Verbund Suchdienst mithilfe des OpenSearch-Protokolls und einer OpenSearch-Deskriptor Datei (. OSDX) (Suchconnector) erstellt wird.
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393458"
---
# <a name="opensearch"></a><span data-ttu-id="5d19a-103">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="5d19a-103">OpenSearch</span></span>

<span data-ttu-id="5d19a-104">Das OpenSearch-Codebeispiel veranschaulicht, wie ein Verbund Suchdienst mithilfe des [OpenSearch](https://github.com/dewitt/opensearch) -Protokolls und einer OpenSearch-Deskriptor Datei (. OSDX) (Suchconnector) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5d19a-104">The OpenSearch code sample demonstrates how to create a federated search service using the [OpenSearch](https://github.com/dewitt/opensearch) protocol, and an OpenSearch Descriptor (.osdx) file (a search connector).</span></span>

<span data-ttu-id="5d19a-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="5d19a-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5d19a-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d19a-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5d19a-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="5d19a-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="5d19a-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="5d19a-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="5d19a-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="5d19a-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="5d19a-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d19a-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="5d19a-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d19a-111">Requirements</span></span>



| <span data-ttu-id="5d19a-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="5d19a-112">Product</span></span>     | <span data-ttu-id="5d19a-113">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="5d19a-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="5d19a-114">Windows</span><span class="sxs-lookup"><span data-stu-id="5d19a-114">Windows</span></span>     | <span data-ttu-id="5d19a-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5d19a-115">Windows 7</span></span>               |
| <span data-ttu-id="5d19a-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="5d19a-116">Windows SDK</span></span> | <span data-ttu-id="5d19a-117">7.0</span><span class="sxs-lookup"><span data-stu-id="5d19a-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="5d19a-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="5d19a-118">Downloading the Sample</span></span>

<span data-ttu-id="5d19a-119">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d19a-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="5d19a-120">Standort</span><span class="sxs-lookup"><span data-stu-id="5d19a-120">Location</span></span>      | <span data-ttu-id="5d19a-121">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="5d19a-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="5d19a-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="5d19a-122">GitHub</span></span>  | [<span data-ttu-id="5d19a-123">OpenSearch-Beispiel</span><span class="sxs-lookup"><span data-stu-id="5d19a-123">OpenSearch sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> <span data-ttu-id="5d19a-124">Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="5d19a-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="5d19a-125">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="5d19a-125">Building the Sample</span></span>

<span data-ttu-id="5d19a-126">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="5d19a-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="5d19a-127">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum **adventuresearch** -Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="5d19a-127">Open the Command Prompt window and navigate to the **AdventureSearch** project directory.</span></span> 
2.  <span data-ttu-id="5d19a-128">Geben Sie `msbuild AdventureSearch.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="5d19a-128">Enter `msbuild AdventureSearch.sln`.</span></span>

<span data-ttu-id="5d19a-129">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="5d19a-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="5d19a-130">Öffnen Sie Windows-Explorer, und navigieren Sie zum **adventuresearch** -Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="5d19a-130">Open Windows Explorer and navigate to the **AdventureSearch** project directory.</span></span>
2.  <span data-ttu-id="5d19a-131">Doppelklicken Sie auf das Symbol für die Datei "adventuresearch. sln", um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5d19a-131">Double-click the icon for the AdventureSearch.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="5d19a-132">Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5d19a-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="5d19a-133">In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="5d19a-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="5d19a-134">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="5d19a-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="5d19a-135">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="5d19a-135">Running the Sample</span></span>

1.  <span data-ttu-id="5d19a-136">Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="5d19a-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="5d19a-137">Geben Sie an der Eingabeaufforderung ein, `AdventureSearch.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für AdventureSearch.exe.</span><span class="sxs-lookup"><span data-stu-id="5d19a-137">At the command prompt, enter `AdventureSearch.exe`, or from Windows Explorer, double-click the icon for AdventureSearch.exe.</span></span>
3.  <span data-ttu-id="5d19a-138">Geben Sie an der Eingabeaufforderung ein, `GetOSDX.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für GetOSDX.exe.</span><span class="sxs-lookup"><span data-stu-id="5d19a-138">At the command prompt, enter `GetOSDX.exe`, or from Windows Explorer, double-click the icon for GetOSDX.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d19a-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d19a-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5d19a-140">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="5d19a-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5d19a-141">Übersicht über das Suchconnector-Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="5d19a-141">Overview of the Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)
</dt> <dt>

<span data-ttu-id="5d19a-142">**Licher**</span><span class="sxs-lookup"><span data-stu-id="5d19a-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5d19a-143">Verbundsuche in Windows 10</span><span class="sxs-lookup"><span data-stu-id="5d19a-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="5d19a-144">Code Beispiele durchsuchen</span><span class="sxs-lookup"><span data-stu-id="5d19a-144">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="5d19a-145">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="5d19a-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5d19a-146">Bibliotheks Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="5d19a-146">Library Description Schema</span></span>](../shell/library-schema-entry.md)
</dt> </dl>

 

 
