---
description: 'Das Codebeispiel "maxmatchingurls" veranschaulicht, wie drei Möglichkeiten zum Angeben der zu indizierenden Dateien bereitgestellt werden: URLs, die einem Dateityp, einem MIME-Typ oder einer angegebenen WHERE-Klausel entsprechen.'
ms.assetid: f7b3a8a6-b464-46d4-a99c-fc56eea9b1ec
title: Neu indiken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a7bb6ae3148f6969fc5349e1ebdf666a527282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484419"
---
# <a name="reindexmatchingurls"></a><span data-ttu-id="3836c-103">Neu indiken</span><span class="sxs-lookup"><span data-stu-id="3836c-103">ReindexMatchingUrls</span></span>

<span data-ttu-id="3836c-104">Das Codebeispiel "maxmatchingurls" veranschaulicht, wie drei Möglichkeiten zum Angeben der zu indizierenden Dateien bereitgestellt werden: URLs, die einem Dateityp, einem MIME-Typ oder einer angegebenen WHERE-Klausel entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3836c-104">The ReindexMatchingUrls code sample demonstrates how to provide three ways to specify the files to re-index: URLs that match a file type, mime type, or a specified WHERE clause.</span></span>

<span data-ttu-id="3836c-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="3836c-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="3836c-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3836c-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="3836c-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="3836c-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="3836c-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="3836c-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="3836c-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="3836c-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="3836c-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3836c-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="3836c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3836c-111">Requirements</span></span>

| <span data-ttu-id="3836c-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="3836c-112">Product</span></span>     | <span data-ttu-id="3836c-113">Produktversion</span><span class="sxs-lookup"><span data-stu-id="3836c-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="3836c-114">Windows</span><span class="sxs-lookup"><span data-stu-id="3836c-114">Windows</span></span>     | <span data-ttu-id="3836c-115">Windows 7, 8.1 oder 10</span><span class="sxs-lookup"><span data-stu-id="3836c-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="3836c-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="3836c-116">Windows SDK</span></span> | <span data-ttu-id="3836c-117">7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="3836c-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="3836c-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="3836c-118">Downloading the Sample</span></span>

<span data-ttu-id="3836c-119">Dieses Beispiel ist im folgenden Speicherort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3836c-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="3836c-120">Standort</span><span class="sxs-lookup"><span data-stu-id="3836c-120">Location</span></span>      | <span data-ttu-id="3836c-121">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="3836c-121">Path URL</span></span>                                                                      |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="3836c-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="3836c-122">GitHub</span></span>  | [<span data-ttu-id="3836c-123">Beispiel für "-xmatchingurls"</span><span class="sxs-lookup"><span data-stu-id="3836c-123">ReindexMatchingUrls sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/ReindexMatchingUrls) |

> [!NOTE]  
> <span data-ttu-id="3836c-124">Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="3836c-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="3836c-125">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="3836c-125">Building the Sample</span></span>

1. <span data-ttu-id="3836c-126">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis " **mamatchingurls** ".</span><span class="sxs-lookup"><span data-stu-id="3836c-126">Open Windows Explorer and navigate to the **ReindexMatchingUrls** project directory.</span></span> <span data-ttu-id="3836c-127">Der vollständige Standard Installationspfad lautet beispielsweise `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls` .</span><span class="sxs-lookup"><span data-stu-id="3836c-127">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls`.</span></span>
2. <span data-ttu-id="3836c-128">Doppelklicken Sie auf das Symbol für die Datei REINDEX. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3836c-128">Double-click the icon for the Reindex.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="3836c-129">Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen.</span><span class="sxs-lookup"><span data-stu-id="3836c-129">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="3836c-130">Dies wirkt sich nicht auf das Verhalten des Beispiels aus.</span><span class="sxs-lookup"><span data-stu-id="3836c-130">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="3836c-131">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="3836c-131">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="3836c-132">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="3836c-132">Running the Sample</span></span>

1. <span data-ttu-id="3836c-133">Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="3836c-133">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="3836c-134">Geben Sie an der Eingabeaufforderung ein, `Reindex.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für Reindex.exe.</span><span class="sxs-lookup"><span data-stu-id="3836c-134">At the command prompt, enter `Reindex.exe`, or from Windows Explorer, double-click the icon for Reindex.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3836c-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3836c-135">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="3836c-136">Referenz</span><span class="sxs-lookup"><span data-stu-id="3836c-136">Reference</span></span>

[<span data-ttu-id="3836c-137">**Isearchcatalogmanager**</span><span class="sxs-lookup"><span data-stu-id="3836c-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="3836c-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="3836c-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="3836c-139">**Isearchmanager**</span><span class="sxs-lookup"><span data-stu-id="3836c-139">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="3836c-140">**Isearchpersistentitemschangedsink**</span><span class="sxs-lookup"><span data-stu-id="3836c-140">**ISearchPersistentItemsChangedSink**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)

[<span data-ttu-id="3836c-141">**Isearchviewchangedsink**</span><span class="sxs-lookup"><span data-stu-id="3836c-141">**ISearchViewChangedSink**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink)

[<span data-ttu-id="3836c-142">**Priorisieren von \_ Flags**</span><span class="sxs-lookup"><span data-stu-id="3836c-142">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)

### <a name="other-samples"></a><span data-ttu-id="3836c-143">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="3836c-143">Other Samples</span></span>

[<span data-ttu-id="3836c-144">Code Beispiele durchsuchen</span><span class="sxs-lookup"><span data-stu-id="3836c-144">Search Code Samples</span></span>](-search-samples-ovw.md)
