---
title: Beispiel für Application-Driven Animation
description: Zeigt die Windows-Animation in der Anwendungs gesteuerten Konfiguration mithilfe von Direct2D zum Animieren der Hintergrundfarbe eines Fensters und zum Synchronisieren der Aktualisierungsrate.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b24905d09ac6559527146ebf572666a6a84f5
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "106337213"
---
# <a name="application-driven-animation-sample"></a><span data-ttu-id="ff9e6-103">Beispiel für Application-Driven Animation</span><span class="sxs-lookup"><span data-stu-id="ff9e6-103">Application-Driven Animation Sample</span></span>

<span data-ttu-id="ff9e6-104">Zeigt die Windows-Animation in der Anwendungs gesteuerten Konfiguration mithilfe von Direct2D zum Animieren der Hintergrundfarbe eines Fensters und zum Synchronisieren der Aktualisierungsrate.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-104">Shows Windows Animation in the application-driven configuration by using Direct2D to animate the background color of a window and syncing to the refresh rate.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="ff9e6-105">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="ff9e6-105">Downloading the Sample</span></span>

<span data-ttu-id="ff9e6-106">Dieses Beispiel ist in den folgenden Speicherorten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="ff9e6-107">Standort</span><span class="sxs-lookup"><span data-stu-id="ff9e6-107">Location</span></span>                               | <span data-ttu-id="ff9e6-108">Pfad/URL</span><span class="sxs-lookup"><span data-stu-id="ff9e6-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff9e6-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="ff9e6-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="ff9e6-110">Microsoft Windows Software Development Kit 7,0</span><span class="sxs-lookup"><span data-stu-id="ff9e6-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="ff9e6-111">Codegalerie</span><span class="sxs-lookup"><span data-stu-id="ff9e6-111">Code Gallery</span></span>                           | [<span data-ttu-id="ff9e6-112">Windows Animation Manager-Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="ff9e6-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="ff9e6-113">Nachdem Sie die Windows SDK heruntergeladen und installiert haben, finden Sie die Beispiele im Installationsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="ff9e6-114">Wenn Sie z. b. den Standard Installationspfad für die Windows SDK für Windows 7 verwenden, werden die Beispiele unter C: \\ Programme \\ Microsoft sdert \\ Windows \\ v 7.0 Samples installiert \\ .</span><span class="sxs-lookup"><span data-stu-id="ff9e6-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="ff9e6-115">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="ff9e6-115">Building the Sample</span></span>

<span data-ttu-id="ff9e6-116">Verwenden Sie eine der folgenden Methoden, um das Beispiel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="ff9e6-117">**So erstellen Sie das Beispiel an der Eingabeaufforderung**</span><span class="sxs-lookup"><span data-stu-id="ff9e6-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="ff9e6-118">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis "appgesteuerte".</span><span class="sxs-lookup"><span data-stu-id="ff9e6-118">Open the Command Prompt window and navigate to the AppDriven project directory.</span></span> <span data-ttu-id="ff9e6-119">Der Standard Installationspfad für dieses Beispiel lautet z. b. C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ windowsanimation \\ appgesteu.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\AppDriven.</span></span>

2.  <span data-ttu-id="ff9e6-120">Führen Sie den folgenden Befehl aus: **MSBuild apprun. sln**</span><span class="sxs-lookup"><span data-stu-id="ff9e6-120">Run the following command: **msbuild AppDriven.sln**</span></span>

<span data-ttu-id="ff9e6-121">**So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt)**</span><span class="sxs-lookup"><span data-stu-id="ff9e6-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="ff9e6-122">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis "appgesteuerte".</span><span class="sxs-lookup"><span data-stu-id="ff9e6-122">Open Windows Explorer and navigate to the AppDriven project directory.</span></span>

2.  <span data-ttu-id="ff9e6-123">Doppelklicken Sie auf das Symbol für die Datei appgesteuerte sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-123">Double-click the icon for the AppDriven.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="ff9e6-124">Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="ff9e6-125">In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="ff9e6-126">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="ff9e6-127">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="ff9e6-127">Running the Sample</span></span>

<span data-ttu-id="ff9e6-128">So führen Sie das Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="ff9e6-128">To run the sample:</span></span>

1.  <span data-ttu-id="ff9e6-129">Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält. verwenden Sie dazu entweder die Eingabeaufforderung oder den Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="ff9e6-130">Führen Sie **AppDriven.exe** an der Eingabeaufforderung aus, oder Doppelklicken Sie im Windows-Explorer auf das Symbol für AppDriven.exe.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-130">Run **AppDriven.exe** at the command prompt, or double-click the icon for AppDriven.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="ff9e6-131">Klicken Sie im Client Bereich auf eine beliebige Stelle, und die Hintergrundfarbe des Fensters wechselt in eine zufällige Farbe.</span><span class="sxs-lookup"><span data-stu-id="ff9e6-131">Click anywhere in the client area, and the background color of the window will change to a random color.</span></span>

 

 




