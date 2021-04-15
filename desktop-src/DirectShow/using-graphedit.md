---
description: Verwenden von GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Verwenden von GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e78118253d86a88231456b72dc8c42ed2a674f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529522"
---
# <a name="using-graphedit"></a><span data-ttu-id="d88c9-103">Verwenden von GraphEdit</span><span class="sxs-lookup"><span data-stu-id="d88c9-103">Using GraphEdit</span></span>

<span data-ttu-id="d88c9-104">GraphEdit ist im Microsoft Windows Software Development Kit (SDK) () verfügbar <https://go.microsoft.com/fwlink/p/?linkid=62332> .</span><span class="sxs-lookup"><span data-stu-id="d88c9-104">GraphEdit is available in the Microsoft Windows Software Development Kit (SDK) (<https://go.microsoft.com/fwlink/p/?linkid=62332>).</span></span>

<span data-ttu-id="d88c9-105">Der Name der GraphEdit-Anwendung ist "graphedt.exe".</span><span class="sxs-lookup"><span data-stu-id="d88c9-105">The name of the GraphEdit application is "graphedt.exe".</span></span> <span data-ttu-id="d88c9-106">Nachdem Sie das SDK installiert haben, befindet sich "graphedt.exe" im folgenden Verzeichnis: \[ Programmdateien \] \\ Microsoft SDKs \\ Windows- \\ \[ Version \] \\ bin \\ .</span><span class="sxs-lookup"><span data-stu-id="d88c9-106">After you install the SDK, "graphedt.exe" is located in the following directory: \[Program Files\]\\Microsoft SDKs\\Windows\\\[version\]\\Bin\\.</span></span>

<span data-ttu-id="d88c9-107">Verwenden Sie vor dem Ausführen von GraphEdit das regsvr32-Hilfsprogramm, um die folgenden DLLs zu registrieren, die sich im selben Verzeichnis befinden:</span><span class="sxs-lookup"><span data-stu-id="d88c9-107">Before running GraphEdit, use the regsvr32 utility to register the following DLLs, which are located in the same directory:</span></span>

-   <span data-ttu-id="d88c9-108">proppage.dll</span><span class="sxs-lookup"><span data-stu-id="d88c9-108">proppage.dll</span></span>
-   <span data-ttu-id="d88c9-109">evrprop.dll</span><span class="sxs-lookup"><span data-stu-id="d88c9-109">evrprop.dll</span></span>

<span data-ttu-id="d88c9-110">Diese DLLs ermöglichen GraphEdit das Anzeigen von Eigenschaften Seiten für einige der integrierten DirectShow-Filter.</span><span class="sxs-lookup"><span data-stu-id="d88c9-110">These DLLs enable GraphEdit to display property pages for some of the built-in DirectShow filters.</span></span>

## <a name="build-a-file-playback-graph"></a><span data-ttu-id="d88c9-111">Erstellen eines Dateiwiedergabe Diagramms</span><span class="sxs-lookup"><span data-stu-id="d88c9-111">Build a File Playback Graph</span></span>

<span data-ttu-id="d88c9-112">GraphEdit kann ein Filter Diagramm für die Wiedergabe von Dateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="d88c9-112">GraphEdit can build a filter graph for file playback.</span></span> <span data-ttu-id="d88c9-113">Diese Funktion entspricht dem Aufrufen der [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) -Methode in einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d88c9-113">This feature is equivalent to calling the [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method in an application.</span></span> <span data-ttu-id="d88c9-114">Klicken Sie im Menü **Datei** auf **Mediendatei Rendering**.</span><span class="sxs-lookup"><span data-stu-id="d88c9-114">From the **File** menu, click **Render Media File**.</span></span> <span data-ttu-id="d88c9-115">GraphEdit zeigt das Dialogfeld **Datei öffnen** an.</span><span class="sxs-lookup"><span data-stu-id="d88c9-115">GraphEdit displays an **Open File** dialog box.</span></span> <span data-ttu-id="d88c9-116">Wählen Sie eine Multimedia-Datei aus, **und klicken Sie** auf</span><span class="sxs-lookup"><span data-stu-id="d88c9-116">Select a multimedia file and click **Open**.</span></span> <span data-ttu-id="d88c9-117">GraphEdit erstellt ein Filter Diagramm, um die Datei wiederzugeben, die Sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="d88c9-117">GraphEdit builds a filter graph to play the file you've selected.</span></span>

<span data-ttu-id="d88c9-118">Sie können auch eine Mediendatei an einer URL Rendering.</span><span class="sxs-lookup"><span data-stu-id="d88c9-118">You can also render a media file located at a URL.</span></span> <span data-ttu-id="d88c9-119">Klicken Sie im Menü **Datei** auf **URL** Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="d88c9-119">From the **File** menu, click **Render URL**.</span></span> <span data-ttu-id="d88c9-120">GraphEdit zeigt ein Dialogfeld an, in das Sie die URL eingeben können.</span><span class="sxs-lookup"><span data-stu-id="d88c9-120">GraphEdit displays a dialog box in which to type the URL.</span></span>

## <a name="build-a-filter-graph"></a><span data-ttu-id="d88c9-121">Erstellen eines Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="d88c9-121">Build a Filter Graph</span></span>

<span data-ttu-id="d88c9-122">GraphEdit kann mithilfe eines beliebigen Filters, der auf Ihrem System registriert ist, ein benutzerdefiniertes Filter Diagramm erstellen.</span><span class="sxs-lookup"><span data-stu-id="d88c9-122">GraphEdit can build a custom filter graph, using any of the filters registered on your system.</span></span> <span data-ttu-id="d88c9-123">Klicken Sie im Menü **Diagramm** auf **Filter einfügen**.</span><span class="sxs-lookup"><span data-stu-id="d88c9-123">From the **Graph** menu, click **Insert Filters**.</span></span> <span data-ttu-id="d88c9-124">Es wird ein Dialogfeld mit einer Liste der Filter in Ihrem System angezeigt, geordnet Nachfilter Kategorie.</span><span class="sxs-lookup"><span data-stu-id="d88c9-124">A dialog box appears with a list of the filters on your system, organized by filter category.</span></span> <span data-ttu-id="d88c9-125">GraphEdit erstellt diese Liste aus den Informationen in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="d88c9-125">GraphEdit builds this list from information in the registry.</span></span> <span data-ttu-id="d88c9-126">Die folgende Abbildung zeigt das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="d88c9-126">The following illustration shows the dialog box.</span></span>

![welche Filter möchten Sie einfügen?](images/gedit12.png)

<span data-ttu-id="d88c9-128">Wenn Sie dem Diagramm einen Filter hinzufügen möchten, wählen Sie den Namen des Filters aus, und klicken Sie auf die Schaltfläche **Filter einfügen** , oder Doppelklicken Sie auf den Filternamen.</span><span class="sxs-lookup"><span data-stu-id="d88c9-128">To add a filter to the graph, select the name of the filter and click the **Insert Filters** button, or double-click the filter name.</span></span> <span data-ttu-id="d88c9-129">Nachdem Sie die Filter hinzugefügt haben, können Sie zwei Filter verbinden, indem Sie die Maus von der Ausgabe-PIN eines Filters zur Eingabe-PIN eines anderen Filters ziehen.</span><span class="sxs-lookup"><span data-stu-id="d88c9-129">After you have added the filters, you can connect two filters by dragging the mouse from one filter's output pin to another filter's input pin.</span></span> <span data-ttu-id="d88c9-130">Wenn die Pins die Verbindung akzeptieren, zeichnet GraphEdit einen Pfeil, der Sie verbindet.</span><span class="sxs-lookup"><span data-stu-id="d88c9-130">If the pins accept the connection, GraphEdit draws an arrow connecting them.</span></span>

![Verbinden von zwei Filtern](images/gedit-connect.png)

## <a name="run-the-graph"></a><span data-ttu-id="d88c9-132">Ausführen des Diagramms</span><span class="sxs-lookup"><span data-stu-id="d88c9-132">Run the Graph</span></span>

<span data-ttu-id="d88c9-133">Nachdem Sie ein Filter Diagramm in der Graph-Bearbeitung erstellt haben, können Sie das Diagramm ausführen, um zu sehen, ob es erwartungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d88c9-133">Once you have built a filter graph in Graph Edit, you can run the graph to see whether it works as you expect.</span></span> <span data-ttu-id="d88c9-134">Das Menü **Diagramm** enthält die Menübefehle **abspielen**,  **Anhalten und anhalten**.</span><span class="sxs-lookup"><span data-stu-id="d88c9-134">The **Graph** menu contains the menu commands **Play**, **Pause**, and **Stop**.</span></span> <span data-ttu-id="d88c9-135">Diese Befehle rufen [**auf, um**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)die [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) -Methoden [**auszuführen**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**anzuhalten**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)und zu stoppen.</span><span class="sxs-lookup"><span data-stu-id="d88c9-135">These commands invoke to the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods [**Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause), and [**Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), respectively.</span></span> <span data-ttu-id="d88c9-136">Die GraphEdit-Symbolleiste verfügt auch über Schaltflächen für diese Befehle:</span><span class="sxs-lookup"><span data-stu-id="d88c9-136">The GraphEdit toolbar has buttons for these commands, as well:</span></span>

![anhalten, wiedergeben und stoppen der Schaltflächen](images/gedit-toolbar.png)

> [!Note]  
> <span data-ttu-id="d88c9-138">Der GraphEdit-Befehl zum **Anhalten hält** zuerst das Diagramm an und versucht, die Zeit NULL (vorausgesetzt, das Diagramm ist suchbar).</span><span class="sxs-lookup"><span data-stu-id="d88c9-138">The GraphEdit **Stop** command first pauses the graph and seeks to time zero (assuming the graph is seekable).</span></span> <span data-ttu-id="d88c9-139">Bei der Wiedergabe von Dateien setzt diese Aktion das Videofenster auf den ersten Frame zurück.</span><span class="sxs-lookup"><span data-stu-id="d88c9-139">For file playback, this action resets the video window to the first frame.</span></span> <span data-ttu-id="d88c9-140">Dann ruft GraphEdit [**IMediaControl:: Station**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)auf.</span><span class="sxs-lookup"><span data-stu-id="d88c9-140">Then GraphEdit calls [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span></span>

 

<span data-ttu-id="d88c9-141">Wenn das Diagramm suchbar ist, können Sie es durchziehen des Schiebereglers, der unterhalb der Symbolleiste angezeigt wird, durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="d88c9-141">If the graph is seekable, you can seek it by dragging the slider bar that appears below the toolbar.</span></span> <span data-ttu-id="d88c9-142">Durchziehen des Schiebereglers wird die [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d88c9-142">Dragging the slider bar invokes the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="view-property-pages"></a><span data-ttu-id="d88c9-143">Anzeigen von Eigenschaften Seiten</span><span class="sxs-lookup"><span data-stu-id="d88c9-143">View Property Pages</span></span>

<span data-ttu-id="d88c9-144">Einige Filter unterstützen benutzerdefinierte Eigenschaften Seiten, die eine Benutzeroberfläche für das Festlegen von Eigenschaften für den Filter bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d88c9-144">Some filters support custom property pages, which provide a user interface for setting properties on the filter.</span></span> <span data-ttu-id="d88c9-145">Um die Eigenschaften Seite eines Filters in GraphEdit anzuzeigen, klicken Sie mit der rechten Maustaste auf den Filter, und wählen Sie im Popup Fenster **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="d88c9-145">To view a filter's property page in GraphEdit, right-click the filter and select **Properties** from the pop-up window.</span></span> <span data-ttu-id="d88c9-146">GraphEdit zeigt eine Eigenschaften Seite an, die die durch den Filter definierten Eigenschaften Blätter enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="d88c9-146">GraphEdit displays a property page that contains the property sheets defined by the filter (if any).</span></span> <span data-ttu-id="d88c9-147">Außerdem enthält GraphEdit ein Eigenschaften Blatt für jede PIN im Filter.</span><span class="sxs-lookup"><span data-stu-id="d88c9-147">In addition, GraphEdit includes a property sheet for each pin on the filter.</span></span> <span data-ttu-id="d88c9-148">Die PIN-Eigenschaften Blätter werden durch GraphEdit, nicht durch den Filter definiert.</span><span class="sxs-lookup"><span data-stu-id="d88c9-148">The pin property sheets are defined by GraphEdit, not by the filter.</span></span> <span data-ttu-id="d88c9-149">Wenn die PIN verbunden ist, zeigt das PIN-Eigenschaften Blatt den Medientyp für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="d88c9-149">If the pin is connected, the pin property sheet displays the media type for the connection.</span></span> <span data-ttu-id="d88c9-150">Andernfalls werden die bevorzugten Medientypen der PIN aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d88c9-150">Otherwise, it lists the pin's preferred media types.</span></span>

> [!Note]  
> <span data-ttu-id="d88c9-151">Wenn Sie die integrierten Eigenschaften Seiten von GraphEdit verwenden möchten, müssen Sie proppage.dll registrieren.</span><span class="sxs-lookup"><span data-stu-id="d88c9-151">To use GraphEdit's built-in property pages, you must register proppage.dll.</span></span> <span data-ttu-id="d88c9-152">Diese dll ist in der Windows SDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d88c9-152">This DLL is available in the Windows SDK.</span></span> <span data-ttu-id="d88c9-153">Die dll enthält auch zusätzliche Eigenschaften Seiten für einige DirectShow-Filter.</span><span class="sxs-lookup"><span data-stu-id="d88c9-153">The DLL also contains additional property pages for some DirectShow filters.</span></span> <span data-ttu-id="d88c9-154">Diese Eigenschaften Seiten werden nur zu Debugzwecken bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d88c9-154">These property pages are provided for debugging purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d88c9-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d88c9-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d88c9-156">Simulieren der Diagramm Erstellung mit GraphEdit</span><span class="sxs-lookup"><span data-stu-id="d88c9-156">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



