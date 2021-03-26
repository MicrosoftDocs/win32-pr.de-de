---
description: Veranschaulicht die Miniaturansicht einer Miniaturansicht, ein aktives Symbolleisten-Steuerelement, das in die Miniaturansicht des Fensters eingebettet ist, um den Zugriff auf die Schlüsselbefehle eines Fensters zu ermöglichen, ohne dass der Benutzer das Fenster der Anwendung wiederherstellt oder aktiviert.
title: Symbolleistenbeispiel für die Miniaturbild-Taskleiste
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e61208f15772a43138e6cd7a38fd6327445bdfa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980321"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a><span data-ttu-id="64c40-103">Symbolleistenbeispiel für die Miniaturbild-Taskleiste</span><span class="sxs-lookup"><span data-stu-id="64c40-103">Taskbar Thumbnail Toolbar Sample</span></span>

<span data-ttu-id="64c40-104">Veranschaulicht die Miniaturansicht einer Miniaturansicht, ein aktives Symbolleisten-Steuerelement, das in die Miniaturansicht des Fensters eingebettet ist, um den Zugriff auf die Schlüsselbefehle eines Fensters zu ermöglichen, ohne dass der Benutzer das Fenster der Anwendung wiederherstellt oder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="64c40-104">Demonstrates a thumbnail toolbar, an active toolbar control embedded in a window's thumbnail preview, used to provide access to a window's key commands without making the user restore or activate the application's window.</span></span>

<span data-ttu-id="64c40-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="64c40-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="64c40-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64c40-106">Description</span></span>](#description)
-   [<span data-ttu-id="64c40-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64c40-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="64c40-108">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="64c40-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="64c40-109">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="64c40-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="64c40-110">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="64c40-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="64c40-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64c40-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="64c40-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64c40-112">Description</span></span>

<span data-ttu-id="64c40-113">In diesem Beispiel wird gezeigt, wie eine einfache Symbolleiste für eine Vorschau der Task leisten Vorschau bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="64c40-113">This sample shows how to provide a simple toolbar to a taskbar thumbnail preview.</span></span> <span data-ttu-id="64c40-114">Die Symbolleiste besteht aus drei Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="64c40-114">The toolbar consists of three buttons.</span></span> <span data-ttu-id="64c40-115">Durch Klicken auf eine Schaltfläche wird ein Fenster angezeigt, um zu bestätigen, dass die Schaltfläche aktiviert</span><span class="sxs-lookup"><span data-stu-id="64c40-115">Clicking a button displays a window to confirm that the button was activated.</span></span> <span data-ttu-id="64c40-116">Die folgenden APIs werden veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="64c40-116">The following APIs are demonstrated:</span></span>

-   [<span data-ttu-id="64c40-117">**ITaskbarList3:: ThumbBarAddButtons**</span><span class="sxs-lookup"><span data-stu-id="64c40-117">**ITaskbarList3::ThumbBarAddButtons**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [<span data-ttu-id="64c40-118">**ITaskbarList3:: thumbbarsetimagelist**</span><span class="sxs-lookup"><span data-stu-id="64c40-118">**ITaskbarList3::ThumbBarSetImageList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   <span data-ttu-id="64c40-119">[**ThumbButton**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton) -Struktur</span><span class="sxs-lookup"><span data-stu-id="64c40-119">[**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton) structure</span></span>

## <a name="requirements"></a><span data-ttu-id="64c40-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="64c40-120">Requirements</span></span>



| <span data-ttu-id="64c40-121">Produkt</span><span class="sxs-lookup"><span data-stu-id="64c40-121">Product</span></span>                                | <span data-ttu-id="64c40-122">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="64c40-122">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="64c40-123">Windows</span><span class="sxs-lookup"><span data-stu-id="64c40-123">Windows</span></span>                                | <span data-ttu-id="64c40-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="64c40-124">Windows 7</span></span>               |
| <span data-ttu-id="64c40-125">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="64c40-125">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="64c40-126">7.0</span><span class="sxs-lookup"><span data-stu-id="64c40-126">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="64c40-127">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="64c40-127">Downloading the Sample</span></span>

| <span data-ttu-id="64c40-128">Standort</span><span class="sxs-lookup"><span data-stu-id="64c40-128">Location</span></span>      | <span data-ttu-id="64c40-129">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="64c40-129">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c40-130">GitHub</span><span class="sxs-lookup"><span data-stu-id="64c40-130">GitHub</span></span>  | [<span data-ttu-id="64c40-131">Taskbarthumbnailtoolbar-Beispiel</span><span class="sxs-lookup"><span data-stu-id="64c40-131">TaskbarThumbnailToolbar sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a><span data-ttu-id="64c40-132">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="64c40-132">Building the Sample</span></span>

<span data-ttu-id="64c40-133">So erstellen Sie das Beispiel von der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="64c40-133">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="64c40-134">Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **taskbarthumbnailtoolbar** .</span><span class="sxs-lookup"><span data-stu-id="64c40-134">Open the command prompt window and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="64c40-135">Geben Sie `msbuild ThumbnailToolbar.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="64c40-135">Enter `msbuild ThumbnailToolbar.sln`.</span></span>

<span data-ttu-id="64c40-136">So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):</span><span class="sxs-lookup"><span data-stu-id="64c40-136">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="64c40-137">Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **taskbarthumbnailtoolbar** .</span><span class="sxs-lookup"><span data-stu-id="64c40-137">Open Windows Explorer and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="64c40-138">Doppelklicken Sie auf das Symbol für die Datei thumbnailtoolbar. sln, um das Projekt in Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="64c40-138">Double-click the icon for the ThumbnailToolbar.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="64c40-139">Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="64c40-139">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="64c40-140">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="64c40-140">Running the Sample</span></span>

1.  <span data-ttu-id="64c40-141">Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält (z.b. `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` ), indem Sie die Eingabeaufforderung oder den Windows-Explorer verwenden.</span><span class="sxs-lookup"><span data-stu-id="64c40-141">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="64c40-142">Wenn Sie die Befehlszeile verwenden, geben Sie ein `ThumbnailToolbar.exe` .</span><span class="sxs-lookup"><span data-stu-id="64c40-142">If using the command line, enter `ThumbnailToolbar.exe`.</span></span>
    -   <span data-ttu-id="64c40-143">Wenn Sie Windows-Explorer verwenden, doppelklicken Sie auf das Symbol für ThumbnailToolbar.exe.</span><span class="sxs-lookup"><span data-stu-id="64c40-143">If using Windows Explorer, double-click the icon for ThumbnailToolbar.exe.</span></span>

    <span data-ttu-id="64c40-144">Ein neues Fenster wird mit einer zugeordneten Task leisten Schaltfläche geöffnet.</span><span class="sxs-lookup"><span data-stu-id="64c40-144">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="64c40-145">Zeigen Sie mit dem Mauszeiger auf die Schaltfläche **thumbnailtoolbar** Taskleiste, sodass die Vorschau angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="64c40-145">Hover the cursor over the **ThumbnailToolbar** taskbar button so that the preview displays.</span></span> <span data-ttu-id="64c40-146">Klicken Sie auf eine der drei Schaltflächen (grün, gelb, rot), die auf der Symbolleiste der Vorschau angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="64c40-146">Click one of the three buttons (green, yellow, red) shown in the preview's toolbar.</span></span>
3.  <span data-ttu-id="64c40-147">Wählen Sie im Menü **Datei** des Fensters die Option **Beenden** aus, um das Programm zu beenden.</span><span class="sxs-lookup"><span data-stu-id="64c40-147">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64c40-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64c40-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64c40-149">Task leisten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="64c40-149">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 



