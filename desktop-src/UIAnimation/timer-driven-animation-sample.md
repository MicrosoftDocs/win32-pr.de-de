---
title: Beispiel für Timer-Driven Animation
description: Zeigt, wie die Windows-Animation mit dem Animations Timer verwendet wird, während GDI+ zum Animieren der Hintergrundfarbe eines Fensters verwendet wird.
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec145b087a112c7482de3a749c690a1824195ea3
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "104314583"
---
# <a name="timer-driven-animation-sample"></a><span data-ttu-id="5e06a-103">Beispiel für Timer-Driven Animation</span><span class="sxs-lookup"><span data-stu-id="5e06a-103">Timer-Driven Animation Sample</span></span>

<span data-ttu-id="5e06a-104">Zeigt, wie die Windows-Animation mit dem Animations Timer verwendet wird, während GDI+ zum Animieren der Hintergrundfarbe eines Fensters verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e06a-104">Shows how to use Windows Animation with the Animation Timer, while using GDI+ to animate the background color of a window.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="5e06a-105">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="5e06a-105">Downloading the Sample</span></span>

<span data-ttu-id="5e06a-106">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5e06a-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="5e06a-107">Standort</span><span class="sxs-lookup"><span data-stu-id="5e06a-107">Location</span></span>                               | <span data-ttu-id="5e06a-108">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="5e06a-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e06a-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="5e06a-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="5e06a-110">Microsoft Windows Software Development Kit 7,0</span><span class="sxs-lookup"><span data-stu-id="5e06a-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="5e06a-111">Codegalerie</span><span class="sxs-lookup"><span data-stu-id="5e06a-111">Code Gallery</span></span>                           | [<span data-ttu-id="5e06a-112">Windows Animation Manager-Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="5e06a-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

<span data-ttu-id="5e06a-113">Nachdem Sie die Windows SDK heruntergeladen und installiert haben, finden Sie die Beispiele im Installationsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="5e06a-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="5e06a-114">Wenn Sie z. b. den Standard Installationspfad für die Windows SDK für Windows 7 verwenden, werden die Beispiele unter C: \\ Programme \\ Microsoft sdert \\ Windows \\ v 7.0 Samples installiert \\ .</span><span class="sxs-lookup"><span data-stu-id="5e06a-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="5e06a-115">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="5e06a-115">Building the Sample</span></span>

<span data-ttu-id="5e06a-116">Verwenden Sie eine der folgenden Methoden, um das Beispiel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5e06a-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="5e06a-117">**So erstellen Sie das Beispiel an der Eingabeaufforderung**</span><span class="sxs-lookup"><span data-stu-id="5e06a-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="5e06a-118">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum timergesteuerte Projektverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="5e06a-118">Open the Command Prompt window and navigate to the TimerDriven project directory.</span></span> <span data-ttu-id="5e06a-119">Der Standard Installationspfad für dieses Beispiel lautet z. b. C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ windowsanimation \\ Timer-gesteuert.</span><span class="sxs-lookup"><span data-stu-id="5e06a-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\TimerDriven.</span></span>

2.  <span data-ttu-id="5e06a-120">Führen Sie den folgenden Befehl aus: **MSBuild Timer-gesteuerte. sln**</span><span class="sxs-lookup"><span data-stu-id="5e06a-120">Run the following command: **msbuild TimerDriven.sln**</span></span>

<span data-ttu-id="5e06a-121">**So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt)**</span><span class="sxs-lookup"><span data-stu-id="5e06a-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="5e06a-122">Öffnen Sie Windows-Explorer, und navigieren Sie zum Verzeichnis "timergesteuerte Projekt".</span><span class="sxs-lookup"><span data-stu-id="5e06a-122">Open Windows Explorer and navigate to the TimerDriven project directory.</span></span>

2.  <span data-ttu-id="5e06a-123">Doppelklicken Sie auf das Symbol für die Datei timergesteuerte. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5e06a-123">Double-click the icon for the TimerDriven.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="5e06a-124">Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e06a-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="5e06a-125">In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="5e06a-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="5e06a-126">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="5e06a-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="5e06a-127">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="5e06a-127">Running the Sample</span></span>

<span data-ttu-id="5e06a-128">So führen Sie das Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="5e06a-128">To run the sample:</span></span>

1.  <span data-ttu-id="5e06a-129">Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält. verwenden Sie dazu entweder die Eingabeaufforderung oder den Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="5e06a-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="5e06a-130">Führen Sie **TimerDriven.exe** an der Eingabeaufforderung aus, oder Doppelklicken Sie im Windows-Explorer auf das Symbol für TimerDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="5e06a-130">Run **TimerDriven.exe** at the command prompt, or double-click the icon for TimerDriven.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="5e06a-131">Klicken Sie im Client Bereich auf eine beliebige Stelle, und die Hintergrundfarbe des Fensters wechselt in eine zufällige Farbe.</span><span class="sxs-lookup"><span data-stu-id="5e06a-131">Click anywhere in the client area, and the background color of the window will change to a random color.</span></span>

 

 




