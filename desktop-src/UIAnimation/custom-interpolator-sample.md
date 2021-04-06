---
title: Beispiel für benutzerdefiniertes Interpolator
description: Zeigt, wie die Windows-Animation mit Ihrem eigenen benutzerdefinierten Interpolator verwendet wird, wobei Direct2D zum Rendern verwendet wird.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a1a2ef09d603eaefac90b2ae25b3f533ba307
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "104101394"
---
# <a name="custom-interpolator-sample"></a><span data-ttu-id="35517-103">Beispiel für benutzerdefiniertes Interpolator</span><span class="sxs-lookup"><span data-stu-id="35517-103">Custom Interpolator Sample</span></span>

<span data-ttu-id="35517-104">Zeigt, wie die Windows-Animation mit Ihrem eigenen benutzerdefinierten Interpolator verwendet wird, wobei Direct2D zum Rendern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="35517-104">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <span data-ttu-id="35517-105">Beispiel Bilder werden aus der Bildbibliothek geladen.</span><span class="sxs-lookup"><span data-stu-id="35517-105">Sample images are loaded from the Picture Library.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="35517-106">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="35517-106">Downloading the Sample</span></span>

<span data-ttu-id="35517-107">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="35517-107">This sample is available in the following locations.</span></span>



| <span data-ttu-id="35517-108">Standort</span><span class="sxs-lookup"><span data-stu-id="35517-108">Location</span></span>                               | <span data-ttu-id="35517-109">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="35517-109">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35517-110">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="35517-110">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="35517-111">Microsoft Windows Software Development Kit 7,0</span><span class="sxs-lookup"><span data-stu-id="35517-111">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="35517-112">Codegalerie</span><span class="sxs-lookup"><span data-stu-id="35517-112">Code Gallery</span></span>                           | [<span data-ttu-id="35517-113">Windows Animation Manager-Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="35517-113">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="35517-114">Nachdem Sie die Windows SDK heruntergeladen und installiert haben, finden Sie die Beispiele im Installationsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="35517-114">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="35517-115">Wenn Sie z. b. den Standard Installationspfad für die Windows SDK für Windows 7 verwenden, werden die Beispiele unter C: \\ Programme \\ Microsoft sdert \\ Windows \\ v 7.0 Samples installiert \\ .</span><span class="sxs-lookup"><span data-stu-id="35517-115">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="35517-116">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="35517-116">Building the Sample</span></span>

<span data-ttu-id="35517-117">Verwenden Sie eine der folgenden Methoden, um das Beispiel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="35517-117">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="35517-118">**So erstellen Sie das Beispiel an der Eingabeaufforderung**</span><span class="sxs-lookup"><span data-stu-id="35517-118">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="35517-119">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis custominterpolator.</span><span class="sxs-lookup"><span data-stu-id="35517-119">Open the Command Prompt window and navigate to the CustomInterpolator project directory.</span></span> <span data-ttu-id="35517-120">Der Standard Installationspfad für dieses Beispiel lautet z. b. C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ windowsanimation \\ custominterpolator.</span><span class="sxs-lookup"><span data-stu-id="35517-120">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\CustomInterpolator</span></span>

2.  <span data-ttu-id="35517-121">Führen Sie den folgenden Befehl aus: **MSBuild custominterpolator. sln**</span><span class="sxs-lookup"><span data-stu-id="35517-121">Run the following command: **msbuild CustomInterpolator.sln**</span></span>

<span data-ttu-id="35517-122">**So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt)**</span><span class="sxs-lookup"><span data-stu-id="35517-122">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="35517-123">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis custominterpolator.</span><span class="sxs-lookup"><span data-stu-id="35517-123">Open Windows Explorer and navigate to the CustomInterpolator project directory.</span></span>

    > [!Note]  
    > <span data-ttu-id="35517-124">Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="35517-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="35517-125">In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="35517-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

2.  <span data-ttu-id="35517-126">Doppelklicken Sie auf das Symbol für die Datei custominterpolator. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="35517-126">Double-click the icon for the CustomInterpolator.sln file to open the project in Visual Studio.</span></span>

3.  <span data-ttu-id="35517-127">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="35517-127">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="35517-128">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="35517-128">Running the Sample</span></span>

<span data-ttu-id="35517-129">So führen Sie das Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="35517-129">To run the sample:</span></span>

1.  <span data-ttu-id="35517-130">Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält. verwenden Sie dazu entweder die Eingabeaufforderung oder den Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="35517-130">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="35517-131">Führen Sie **CustomInterpolator.exe** an der Eingabeaufforderung aus, oder Doppelklicken Sie im Windows-Explorer auf das Symbol für CustomInterpolator.exe.</span><span class="sxs-lookup"><span data-stu-id="35517-131">Run **CustomInterpolator.exe** at the command prompt, or double-click the icon for CustomInterpolator.exe in Windows Explorer.</span></span>
3.  <span data-ttu-id="35517-132">Ändern Sie die Größe des Fensters, oder drücken Sie die Leertaste, und die Bilder werden sich nach dem Zufallsprinzip in der Mitte des Client Bereichs anordnen.</span><span class="sxs-lookup"><span data-stu-id="35517-132">Resize the window or press the spacebar, and the images will arrange themselves randomly in the middle of the client area.</span></span>

4.  <span data-ttu-id="35517-133">Drücken Sie die nach-oben-oder nach-unten-Taste, und die Bilder werden in Richtung oben oder unten im Client Bereich beschleunigt.</span><span class="sxs-lookup"><span data-stu-id="35517-133">Press the up or down arrow and the images will accelerate toward the top or bottom of the client area.</span></span>

 

 




