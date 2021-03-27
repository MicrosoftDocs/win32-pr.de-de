---
description: Veranschaulicht Überlagerungen und Status leisten des Task leisten Symbols.
title: Peripheriestatus der Taskleiste (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E4B693FB-EE7D-47d0-A5D8-91205AD4A3DC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 793c09853e3174f426b7b41685f2593daaae9b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995046"
---
# <a name="taskbar-peripheral-status-sample"></a><span data-ttu-id="ef98a-103">Peripheriestatus der Taskleiste (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="ef98a-103">Taskbar Peripheral Status Sample</span></span>

<span data-ttu-id="ef98a-104">Veranschaulicht Überlagerungen und Status leisten des Task leisten Symbols.</span><span class="sxs-lookup"><span data-stu-id="ef98a-104">Demonstrates taskbar icon overlays and progress bars.</span></span>

<span data-ttu-id="ef98a-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="ef98a-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ef98a-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef98a-106">Description</span></span>](#description)
-   [<span data-ttu-id="ef98a-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef98a-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ef98a-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="ef98a-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="ef98a-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="ef98a-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="ef98a-110">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="ef98a-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="ef98a-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef98a-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="ef98a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef98a-112">Description</span></span>

<span data-ttu-id="ef98a-113">In diesem Beispiel wird eine Beispiel-Task leisten Schaltfläche erstellt, die die Verwendung von [**ITaskbarList3:: setverlayicon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) veranschaulicht, indem Sie verschiedene über ein Menü ausgewählte Überlagerungen anwenden können.</span><span class="sxs-lookup"><span data-stu-id="ef98a-113">This sample creates an example taskbar button on which it demonstrates the use of [**ITaskbarList3::SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) by allowing you to apply various overlays chosen from a menu.</span></span>

<span data-ttu-id="ef98a-114">Das Beispiel bietet außerdem die Option, eine Statusanzeige auf der Schaltfläche zu simulieren, die die Verwendung von [**ITaskbarList3:: setprogressstate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) und [**ITaskbarList3:: setprogressvalue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) veranschaulicht, indem zunächst eine unbedingte Statusanzeige (tbpf- \_ unbestimmt) und dann ein normaler proportionaler Indikator (tbpf \_ Normal) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ef98a-114">The sample also provides the option of simulating a progress indicator on the button, demonstrating the use of [**ITaskbarList3::SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) and [**ITaskbarList3::SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) by showing at first an indeterminate progress indicator (TBPF\_INDETERMINATE), and then a normal proportional indicator (TBPF\_NORMAL).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef98a-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ef98a-115">Requirements</span></span>



| <span data-ttu-id="ef98a-116">Produkt</span><span class="sxs-lookup"><span data-stu-id="ef98a-116">Product</span></span>                                | <span data-ttu-id="ef98a-117">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="ef98a-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="ef98a-118">Windows</span><span class="sxs-lookup"><span data-stu-id="ef98a-118">Windows</span></span>                                | <span data-ttu-id="ef98a-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ef98a-119">Windows 7</span></span>               |
| <span data-ttu-id="ef98a-120">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="ef98a-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="ef98a-121">7.0</span><span class="sxs-lookup"><span data-stu-id="ef98a-121">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="ef98a-122">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="ef98a-122">Downloading the Sample</span></span>

| <span data-ttu-id="ef98a-123">Standort</span><span class="sxs-lookup"><span data-stu-id="ef98a-123">Location</span></span>      | <span data-ttu-id="ef98a-124">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="ef98a-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef98a-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="ef98a-125">GitHub</span></span>  | [<span data-ttu-id="ef98a-126">Taskbarperipheralstatus-Beispiel</span><span class="sxs-lookup"><span data-stu-id="ef98a-126">TaskBarPeripheralStatus sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarPeripheralStatus) |

## <a name="building-the-sample"></a><span data-ttu-id="ef98a-127">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="ef98a-127">Building the Sample</span></span>

<span data-ttu-id="ef98a-128">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="ef98a-128">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="ef98a-129">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **taskbarperipheralstatus** .</span><span class="sxs-lookup"><span data-stu-id="ef98a-129">Open the command prompt window and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="ef98a-130">Geben Sie `msbuild PeripheralStatus.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="ef98a-130">Enter `msbuild PeripheralStatus.sln`.</span></span>

<span data-ttu-id="ef98a-131">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="ef98a-131">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="ef98a-132">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **taskbarperipheralstatus** .</span><span class="sxs-lookup"><span data-stu-id="ef98a-132">Open Windows Explorer and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="ef98a-133">Doppelklicken Sie auf das Symbol für die Datei "peripheralstatus. sln", um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ef98a-133">Double-click the icon for the PeripheralStatus.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="ef98a-134">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ef98a-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="ef98a-135">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="ef98a-135">Running the Sample</span></span>

1.  <span data-ttu-id="ef98a-136">Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält (z.b. `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug` ), indem Sie die Eingabeaufforderung oder den Windows-Explorer verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef98a-136">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="ef98a-137">Wenn Sie die Befehlszeile verwenden, geben Sie ein `PeripheralStatus.exe` .</span><span class="sxs-lookup"><span data-stu-id="ef98a-137">If using the command line, enter `PeripheralStatus.exe`.</span></span>
    -   <span data-ttu-id="ef98a-138">Wenn Sie Windows-Explorer verwenden, doppelklicken Sie auf das Symbol für PeripheralStatus.exe.</span><span class="sxs-lookup"><span data-stu-id="ef98a-138">If using Windows Explorer, double-click the icon for PeripheralStatus.exe.</span></span>

    <span data-ttu-id="ef98a-139">Ein neues Fenster wird mit einer zugeordneten Task leisten Schaltfläche geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ef98a-139">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="ef98a-140">Um die Überlagerungen zu veranschaulichen, wählen Sie über **Lagerung 1** oder über **Lagerung 2** im Fenster **Peripherie Status** des Fensters aus.</span><span class="sxs-lookup"><span data-stu-id="ef98a-140">To demonstrate overlays, choose **Overlay 1** or **Overlay 2** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="ef98a-141">Das ausgewählte Overlay wird auf der Task leisten Schaltfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ef98a-141">The chosen overlay appears on the taskbar button.</span></span> <span data-ttu-id="ef98a-142">Um das Overlay zu entfernen, wählen Sie **Overlay löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="ef98a-142">To remove the overlay, choose **Clear Overlay**.</span></span>
3.  <span data-ttu-id="ef98a-143">Um die Status Anzeige zu veranschaulichen, wählen Sie im Fenster **Peripherie Status** des Fensters die Option Status **simulieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ef98a-143">To demonstrate the progress bar, choose **Simulate Progress** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="ef98a-144">Die Task leisten Schaltfläche zeigt eine unbestimmende Statusanzeige an und wechselt dann zu einem normalen Indikator.</span><span class="sxs-lookup"><span data-stu-id="ef98a-144">The taskbar button will show an indeterminate progress indicator then switch to a normal indicator.</span></span>
4.  <span data-ttu-id="ef98a-145">Wählen Sie im Menü **Datei** des Fensters die Option **Beenden** aus, um das Programm zu beenden.</span><span class="sxs-lookup"><span data-stu-id="ef98a-145">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef98a-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef98a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef98a-147">Task leisten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="ef98a-147">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 



