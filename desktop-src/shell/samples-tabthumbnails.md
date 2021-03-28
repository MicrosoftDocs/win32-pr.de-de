---
description: Veranschaulicht, wie eine Anwendung mehrere switchziele (wie für Registerkarten) in einem TaskBand verfügbar machen und Ihre Miniaturansichten bereitstellen kann.
title: TabThumbnails-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3F48EAA2-98A3-4530-9FC6-A395987157B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 323604d104be3432a5fc251901c4308bfc989f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980745"
---
# <a name="tabthumbnails-sample"></a><span data-ttu-id="8dbad-103">TabThumbnails-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8dbad-103">TabThumbnails Sample</span></span>

<span data-ttu-id="8dbad-104">Veranschaulicht, wie eine Anwendung mehrere switchziele (wie für Registerkarten) in einem TaskBand verfügbar machen und Ihre Miniaturansichten bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="8dbad-104">Demonstrates how an application can expose multiple switch targets (as for tabs) on a taskband and how to provide their thumbnails.</span></span>

<span data-ttu-id="8dbad-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="8dbad-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8dbad-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8dbad-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="8dbad-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="8dbad-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="8dbad-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="8dbad-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="8dbad-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="8dbad-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="8dbad-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8dbad-110">Requirements</span></span>



| <span data-ttu-id="8dbad-111">Produkt</span><span class="sxs-lookup"><span data-stu-id="8dbad-111">Product</span></span>                                | <span data-ttu-id="8dbad-112">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="8dbad-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="8dbad-113">Windows</span><span class="sxs-lookup"><span data-stu-id="8dbad-113">Windows</span></span>                                | <span data-ttu-id="8dbad-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8dbad-114">Windows 7</span></span>               |
| <span data-ttu-id="8dbad-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="8dbad-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="8dbad-116">7.0</span><span class="sxs-lookup"><span data-stu-id="8dbad-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="8dbad-117">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="8dbad-117">Downloading the Sample</span></span>

| <span data-ttu-id="8dbad-118">Standort</span><span class="sxs-lookup"><span data-stu-id="8dbad-118">Location</span></span>      | <span data-ttu-id="8dbad-119">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="8dbad-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dbad-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="8dbad-120">GitHub</span></span>  | [<span data-ttu-id="8dbad-121">Tabthumbnails-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8dbad-121">TabThumbnails sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails) |

## <a name="building-the-sample"></a><span data-ttu-id="8dbad-122">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="8dbad-122">Building the Sample</span></span>

<span data-ttu-id="8dbad-123">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="8dbad-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="8dbad-124">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **tabminiatur Ansichten** .</span><span class="sxs-lookup"><span data-stu-id="8dbad-124">Open the command prompt window and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="8dbad-125">Geben Sie `msbuild TabThumbnails.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="8dbad-125">Enter `msbuild TabThumbnails.sln`.</span></span>

<span data-ttu-id="8dbad-126">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="8dbad-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="8dbad-127">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **tabminiatur Ansichten** .</span><span class="sxs-lookup"><span data-stu-id="8dbad-127">Open Windows Explorer and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="8dbad-128">Doppelklicken Sie auf das Symbol für die Datei tabthumbnails. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8dbad-128">Double-click the icon for the TabThumbnails.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="8dbad-129">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="8dbad-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="8dbad-130">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="8dbad-130">Running the Sample</span></span>

1.  <span data-ttu-id="8dbad-131">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="8dbad-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="8dbad-132">Geben Sie in der Befehlszeile ein `TabThumbnails.exe` .</span><span class="sxs-lookup"><span data-stu-id="8dbad-132">At the command line, enter `TabThumbnails.exe`.</span></span> <span data-ttu-id="8dbad-133">Alternativ können Sie in Windows-Explorer auf das Symbol für TabThumbnails.exe doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="8dbad-133">Alternatively, from Windows Explorer double-click the icon for TabThumbnails.exe.</span></span>

 

 



