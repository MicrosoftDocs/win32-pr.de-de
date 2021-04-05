---
title: Raster Layout-Beispiel
description: Veranschaulicht die Verwendung der Windows-Animation mit Direct2D zum Animieren eines Bild Blatts.
ms.assetid: f2f24058-c532-45ad-bde8-d05cfffcd505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4d691ffa6396e294fd2dfbd07eaf9329f19519
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "103724360"
---
# <a name="grid-layout-sample"></a><span data-ttu-id="49e61-103">Raster Layout-Beispiel</span><span class="sxs-lookup"><span data-stu-id="49e61-103">Grid Layout Sample</span></span>

<span data-ttu-id="49e61-104">Veranschaulicht die Verwendung der Windows-Animation mit Direct2D zum Animieren eines Bild Blatts.</span><span class="sxs-lookup"><span data-stu-id="49e61-104">Shows how to use Windows Animation, using Direct2D to animate a grid of images.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="49e61-105">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="49e61-105">Downloading the Sample</span></span>

<span data-ttu-id="49e61-106">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="49e61-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="49e61-107">Standort</span><span class="sxs-lookup"><span data-stu-id="49e61-107">Location</span></span>                               | <span data-ttu-id="49e61-108">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="49e61-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49e61-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="49e61-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="49e61-110">Microsoft Windows Software Development Kit 7,0</span><span class="sxs-lookup"><span data-stu-id="49e61-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="49e61-111">Codegalerie</span><span class="sxs-lookup"><span data-stu-id="49e61-111">Code Gallery</span></span>                           | [<span data-ttu-id="49e61-112">Windows Animation Manager-Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="49e61-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

<span data-ttu-id="49e61-113">Nachdem Sie die Windows SDK heruntergeladen und installiert haben, finden Sie die Beispiele im Installationsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="49e61-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="49e61-114">Wenn Sie z. b. den Standard Installationspfad für die Windows SDK für Windows 7 verwenden, werden die Beispiele unter C: \\ Programme \\ Microsoft sdert \\ Windows \\ v 7.0 Samples installiert \\ .</span><span class="sxs-lookup"><span data-stu-id="49e61-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="49e61-115">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="49e61-115">Building the Sample</span></span>

<span data-ttu-id="49e61-116">Verwenden Sie eine der folgenden Methoden, um das Beispiel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="49e61-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="49e61-117">**So erstellen Sie das Beispiel an der Eingabeaufforderung**</span><span class="sxs-lookup"><span data-stu-id="49e61-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="49e61-118">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum GridLayout-Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="49e61-118">Open the Command Prompt window and navigate to the GridLayout project directory.</span></span> <span data-ttu-id="49e61-119">Der Standard Installationspfad für dieses Beispiel lautet z. b. C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ windowsanimation \\ GridLayout</span><span class="sxs-lookup"><span data-stu-id="49e61-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\GridLayout</span></span>

2.  <span data-ttu-id="49e61-120">Führen Sie den folgenden Befehl aus: **MSBuild GridLayout. sln**</span><span class="sxs-lookup"><span data-stu-id="49e61-120">Run the following command: **msbuild GridLayout.sln**</span></span>

<span data-ttu-id="49e61-121">**So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt)**</span><span class="sxs-lookup"><span data-stu-id="49e61-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="49e61-122">Öffnen Sie Windows-Explorer, und navigieren Sie zum GridLayout-Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="49e61-122">Open Windows Explorer and navigate to the GridLayout project directory.</span></span>

    > [!Note]  
    > <span data-ttu-id="49e61-123">Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="49e61-123">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="49e61-124">In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="49e61-124">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

2.  <span data-ttu-id="49e61-125">Doppelklicken Sie auf das Symbol für die Datei GridLayout. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="49e61-125">Double-click the icon for the GridLayout.sln file to open the project in Visual Studio.</span></span>

3.  <span data-ttu-id="49e61-126">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="49e61-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="49e61-127">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="49e61-127">Running the Sample</span></span>

<span data-ttu-id="49e61-128">So führen Sie das Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="49e61-128">To run the sample:</span></span>

1.  <span data-ttu-id="49e61-129">Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält. verwenden Sie dazu entweder die Eingabeaufforderung oder den Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="49e61-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="49e61-130">Führen Sie **GridLayout.exe** an der Eingabeaufforderung aus, oder Doppelklicken Sie im Windows-Explorer auf das Symbol für GridLayout.exe.</span><span class="sxs-lookup"><span data-stu-id="49e61-130">Run **GridLayout.exe** at the command prompt, or double-click the icon for GridLayout.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="49e61-131">Beispiel Bilder werden aus der Bildbibliothek geladen.</span><span class="sxs-lookup"><span data-stu-id="49e61-131">Sample images are loaded from the Picture Library.</span></span> <span data-ttu-id="49e61-132">Ändern Sie die Größe des Fensters, und die Bilder werden sich in einem Raster anordnen.</span><span class="sxs-lookup"><span data-stu-id="49e61-132">Resize the window and the images will arrange themselves into a grid.</span></span>

 

 




