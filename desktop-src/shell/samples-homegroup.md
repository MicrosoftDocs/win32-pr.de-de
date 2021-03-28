---
description: Veranschaulicht, wie Sie den Status der Heim Netzgruppen Mitgliedschaft bestimmen, Elemente der obersten Ebene im Ordner "HomeGroup Shell" auflisten und den HomeGroup-Freigabe-Assistenten starten.
title: HomeGroup (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FDEFF261-BF86-4fbb-8567-892F79F23D92
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c22ea84431f464ef8fcae6bfad0d90a45ba310d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042424"
---
# <a name="homegroup-sample"></a><span data-ttu-id="f0164-103">HomeGroup (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="f0164-103">HomeGroup Sample</span></span>

<span data-ttu-id="f0164-104">Veranschaulicht, wie Sie den Status der Heim Netzgruppen Mitgliedschaft bestimmen, Elemente der obersten Ebene im Ordner " **HomeGroup** Shell" auflisten und den **HomeGroup-Freigabe-Assistenten** starten.</span><span class="sxs-lookup"><span data-stu-id="f0164-104">Demonstrates how to determine HomeGroup membership status, enumerate top-level items in the **HomeGroup** Shell folder, and launch the **HomeGroup Sharing Wizard**.</span></span>

<span data-ttu-id="f0164-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="f0164-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f0164-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0164-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f0164-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f0164-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="f0164-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="f0164-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="f0164-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f0164-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="f0164-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0164-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="f0164-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f0164-111">Requirements</span></span>



| <span data-ttu-id="f0164-112">Produkt</span><span class="sxs-lookup"><span data-stu-id="f0164-112">Product</span></span>                                | <span data-ttu-id="f0164-113">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="f0164-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="f0164-114">Windows</span><span class="sxs-lookup"><span data-stu-id="f0164-114">Windows</span></span>                                | <span data-ttu-id="f0164-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f0164-115">Windows 7</span></span>               |
| <span data-ttu-id="f0164-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="f0164-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="f0164-117">7.0</span><span class="sxs-lookup"><span data-stu-id="f0164-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f0164-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f0164-118">Downloading the Sample</span></span>

| <span data-ttu-id="f0164-119">Standort</span><span class="sxs-lookup"><span data-stu-id="f0164-119">Location</span></span>      | <span data-ttu-id="f0164-120">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="f0164-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0164-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="f0164-121">GitHub</span></span>  | [<span data-ttu-id="f0164-122">Beispiel für Heim Netzgruppe</span><span class="sxs-lookup"><span data-stu-id="f0164-122">HomeGroup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/HomeGroup) |

## <a name="building-the-sample"></a><span data-ttu-id="f0164-123">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f0164-123">Building the Sample</span></span>

<span data-ttu-id="f0164-124">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="f0164-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="f0164-125">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis der **Heim Netzgruppe** .</span><span class="sxs-lookup"><span data-stu-id="f0164-125">Open the command prompt window and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="f0164-126">Geben Sie `msbuild HomeGroup.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="f0164-126">Enter `msbuild HomeGroup.sln`.</span></span>

<span data-ttu-id="f0164-127">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="f0164-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="f0164-128">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis der **Heim Netzgruppe** .</span><span class="sxs-lookup"><span data-stu-id="f0164-128">Open Windows Explorer and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="f0164-129">Doppelklicken Sie auf das Symbol für die Datei HomeGroup. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f0164-129">Double-click the icon for the HomeGroup.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="f0164-130">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="f0164-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="f0164-131">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="f0164-131">Running the Sample</span></span>

1.  <span data-ttu-id="f0164-132">Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="f0164-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="f0164-133">Geben Sie in der Befehlszeile ein `HomeGroup.exe` .</span><span class="sxs-lookup"><span data-stu-id="f0164-133">At the command line, enter `HomeGroup.exe`.</span></span> <span data-ttu-id="f0164-134">Alternativ können Sie in Windows-Explorer auf das Symbol für HomeGroup.exe doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="f0164-134">Alternatively, from Windows Explorer double-click the icon for HomeGroup.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0164-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0164-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0164-136">**Ihomegroup**</span><span class="sxs-lookup"><span data-stu-id="f0164-136">**IHomeGroup**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup)
</dt> <dt>

[<span data-ttu-id="f0164-137">**KNOWNFOLDERID**</span><span class="sxs-lookup"><span data-stu-id="f0164-137">**KNOWNFOLDERID**</span></span>](knownfolderid.md)
</dt> </dl>

 

 



