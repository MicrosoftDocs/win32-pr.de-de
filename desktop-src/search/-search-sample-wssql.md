---
description: Das wssql-Codebeispiel veranschaulicht die Kommunikation zwischen Microsoft OLE DB und Windows Search über Structured Query Language (SQL).
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: Wssql
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862160"
---
# <a name="wssql"></a><span data-ttu-id="62a9d-103">Wssql</span><span class="sxs-lookup"><span data-stu-id="62a9d-103">WSSQL</span></span>

<span data-ttu-id="62a9d-104">Das wssql-Codebeispiel veranschaulicht die Kommunikation zwischen Microsoft OLE DB und Windows Search über Structured Query Language (SQL).</span><span class="sxs-lookup"><span data-stu-id="62a9d-104">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through Structured Query Language (SQL).</span></span>

<span data-ttu-id="62a9d-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="62a9d-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="62a9d-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62a9d-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="62a9d-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="62a9d-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="62a9d-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="62a9d-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="62a9d-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="62a9d-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="62a9d-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="62a9d-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="62a9d-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62a9d-111">Requirements</span></span>

| <span data-ttu-id="62a9d-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="62a9d-112">Product</span></span>     | <span data-ttu-id="62a9d-113">Produktversion</span><span class="sxs-lookup"><span data-stu-id="62a9d-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="62a9d-114">Windows</span><span class="sxs-lookup"><span data-stu-id="62a9d-114">Windows</span></span>     | <span data-ttu-id="62a9d-115">Windows 7, 8.1 oder 10</span><span class="sxs-lookup"><span data-stu-id="62a9d-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="62a9d-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="62a9d-116">Windows SDK</span></span> | <span data-ttu-id="62a9d-117">7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="62a9d-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="62a9d-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="62a9d-118">Downloading the Sample</span></span>

<span data-ttu-id="62a9d-119">Dieses Beispiel ist im folgenden Speicherort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="62a9d-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="62a9d-120">Standort</span><span class="sxs-lookup"><span data-stu-id="62a9d-120">Location</span></span>      | <span data-ttu-id="62a9d-121">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="62a9d-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="62a9d-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="62a9d-122">GitHub</span></span>        | [<span data-ttu-id="62a9d-123">Wssql-Beispiel</span><span class="sxs-lookup"><span data-stu-id="62a9d-123">WSSQL sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> <span data-ttu-id="62a9d-124">Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="62a9d-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="62a9d-125">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="62a9d-125">Building the Sample</span></span>

1. <span data-ttu-id="62a9d-126">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis von **wssql** .</span><span class="sxs-lookup"><span data-stu-id="62a9d-126">Open Windows Explorer and navigate to the **WSSQL** project directory.</span></span>
2. <span data-ttu-id="62a9d-127">Doppelklicken Sie auf das Symbol für die Datei wssql. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="62a9d-127">Double-click the icon for the WSSQL.sln file to open the project in Visual Studio.</span></span>
    > [!NOTE]  
    > <span data-ttu-id="62a9d-128">Die SLN-Datei wurde mit einer älteren Version von Visual Studio erstellt. Daher ist ein Upgrade erforderlich, wenn Sie Visual Studio 2012 oder höher ausführen.</span><span class="sxs-lookup"><span data-stu-id="62a9d-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="62a9d-129">Dies wirkt sich nicht auf das Verhalten des Beispiels aus.</span><span class="sxs-lookup"><span data-stu-id="62a9d-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="62a9d-130">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="62a9d-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="62a9d-131">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="62a9d-131">Running the Sample</span></span>

1. <span data-ttu-id="62a9d-132">Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="62a9d-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="62a9d-133">Geben Sie an der Eingabeaufforderung ein, `WSSQL.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für WSSQL.exe.</span><span class="sxs-lookup"><span data-stu-id="62a9d-133">At the command prompt, enter `WSSQL.exe`, or from Windows Explorer, double-click the icon for WSSQL.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62a9d-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="62a9d-134">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="62a9d-135">Konzept</span><span class="sxs-lookup"><span data-stu-id="62a9d-135">Conceptual</span></span>

[<span data-ttu-id="62a9d-136">Verwenden der Windows Search-SQL-Syntax</span><span class="sxs-lookup"><span data-stu-id="62a9d-136">Using Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="62a9d-137">Allgemeine Informationen zur Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="62a9d-137">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)

[<span data-ttu-id="62a9d-138">Übersicht über OLE DB Programmierung</span><span class="sxs-lookup"><span data-stu-id="62a9d-138">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="62a9d-139">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="62a9d-139">Other Samples</span></span>

[<span data-ttu-id="62a9d-140">Code Beispiele durchsuchen</span><span class="sxs-lookup"><span data-stu-id="62a9d-140">Search Code Samples</span></span>](-search-samples-ovw.md)
