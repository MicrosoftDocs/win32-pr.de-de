---
title: Beispiel für Prioritäts Vergleich
description: Zeigt, wie die Windows-Animation mit einem eigenen Prioritäts Vergleich verwendet wird, wobei Direct2D für das Rendering verwendet wird.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfcb20785d6a4c3c3384b85327a0e27d93c58d7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "104101391"
---
# <a name="priority-comparison-sample"></a><span data-ttu-id="c9b3a-103">Beispiel für Prioritäts Vergleich</span><span class="sxs-lookup"><span data-stu-id="c9b3a-103">Priority Comparison Sample</span></span>

<span data-ttu-id="c9b3a-104">Zeigt, wie die Windows-Animation mit einem eigenen Prioritäts Vergleich verwendet wird, wobei Direct2D für das Rendering verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-104">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="c9b3a-105">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c9b3a-105">Downloading the Sample</span></span>

<span data-ttu-id="c9b3a-106">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="c9b3a-107">Standort</span><span class="sxs-lookup"><span data-stu-id="c9b3a-107">Location</span></span>                               | <span data-ttu-id="c9b3a-108">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="c9b3a-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b3a-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="c9b3a-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="c9b3a-110">Microsoft Windows Software Development Kit 7,0</span><span class="sxs-lookup"><span data-stu-id="c9b3a-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="c9b3a-111">Codegalerie</span><span class="sxs-lookup"><span data-stu-id="c9b3a-111">Code Gallery</span></span>                           | [<span data-ttu-id="c9b3a-112">Windows Animation Manager-Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="c9b3a-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="c9b3a-113">Nachdem Sie die Windows SDK heruntergeladen und installiert haben, finden Sie die Beispiele im Installationsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="c9b3a-114">Wenn Sie z. b. den Standard Installationspfad für die Windows SDK für Windows 7 verwenden, werden die Beispiele unter C: \\ Programme \\ Microsoft sdert \\ Windows \\ v 7.0 Samples installiert \\ .</span><span class="sxs-lookup"><span data-stu-id="c9b3a-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="c9b3a-115">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c9b3a-115">Building the Sample</span></span>

<span data-ttu-id="c9b3a-116">Verwenden Sie eine der folgenden Methoden, um das Beispiel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="c9b3a-117">**So erstellen Sie das Beispiel an der Eingabeaufforderung**</span><span class="sxs-lookup"><span data-stu-id="c9b3a-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="c9b3a-118">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis prioritycomparison.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-118">Open the Command Prompt window and navigate to the PriorityComparison project directory.</span></span> <span data-ttu-id="c9b3a-119">Der Standard Installationspfad für dieses Beispiel lautet z. b. C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ windowsanimation \\ prioritycomparison.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\PriorityComparison.</span></span>

2.  <span data-ttu-id="c9b3a-120">Führen Sie den folgenden Befehl aus: **MSBuild prioritycomparison. sln**</span><span class="sxs-lookup"><span data-stu-id="c9b3a-120">Run the following command: **msbuild PriorityComparison.sln**</span></span>

<span data-ttu-id="c9b3a-121">**So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt)**</span><span class="sxs-lookup"><span data-stu-id="c9b3a-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="c9b3a-122">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis prioritycomparison.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-122">Open Windows Explorer and navigate to the PriorityComparison project directory.</span></span>

2.  <span data-ttu-id="c9b3a-123">Doppelklicken Sie auf das Symbol für die Datei prioritycomparison. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-123">Double-click the icon for the PriorityComparison.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="c9b3a-124">Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="c9b3a-125">In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="c9b3a-126">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c9b3a-127">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="c9b3a-127">Running the Sample</span></span>

<span data-ttu-id="c9b3a-128">So führen Sie das Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="c9b3a-128">To run the sample:</span></span>

1.  <span data-ttu-id="c9b3a-129">Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält. verwenden Sie dazu entweder die Eingabeaufforderung oder den Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="c9b3a-130">Führen Sie **PriorityComparison.exe** an der Eingabeaufforderung aus, oder Doppelklicken Sie im Windows-Explorer auf das Symbol für PriorityComparison.exe.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-130">Run **PriorityComparison.exe** at the command prompt, or double-click the icon for PriorityComparison.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="c9b3a-131">Beispiel Bilder werden aus der Bildbibliothek geladen.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-131">Sample images are loaded from the Picture Library.</span></span> <span data-ttu-id="c9b3a-132">Ändern Sie die Größe des Fensters, oder drücken Sie die Leertaste, und die Bilder werden in die Mitte verschoben.</span><span class="sxs-lookup"><span data-stu-id="c9b3a-132">Resize the window or press the spacebar and the images will move to the center.</span></span>

4.  <span data-ttu-id="c9b3a-133">Verwenden Sie die nach-links-und nach-rechts-Taste, um unterschiedliche Bilder auszuwählen (je schneller die Taste gedrückt wird, desto schneller wird die Auswahl geändert).</span><span class="sxs-lookup"><span data-stu-id="c9b3a-133">Use the left and right arrow keys to select different images (the faster the key is pressed the faster the selection will change).</span></span>

5.  <span data-ttu-id="c9b3a-134">Verwenden Sie die nach-oben-und nach-unten-Taste, um eine Welle durch die Bilder zu erstellen (desto schneller wird die Taste gedrückt, desto schneller wird die Welle).</span><span class="sxs-lookup"><span data-stu-id="c9b3a-134">Use the up and down arrow keys to create a wave through the images (the faster the key is pressed, the faster the wave).</span></span>

 

 




