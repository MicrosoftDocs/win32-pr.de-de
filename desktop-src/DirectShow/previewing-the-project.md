---
description: Anzeigen der Vorschau des Projekts
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Anzeigen der Vorschau des Projekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf38fe19e500cfe9bd9a8dfb77f7ff56528a2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958019"
---
# <a name="previewing-the-project"></a><span data-ttu-id="17b7a-103">Anzeigen der Vorschau des Projekts</span><span class="sxs-lookup"><span data-stu-id="17b7a-103">Previewing the Project</span></span>

<span data-ttu-id="17b7a-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="17b7a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="17b7a-105">Zum Anzeigen einer Vorschau des Projekts benötigen Sie eine Komponente, die als *Renderengine* bezeichnet wird und ein DirectShow-Filter Diagramm aus einer Zeitachse erstellt.</span><span class="sxs-lookup"><span data-stu-id="17b7a-105">To preview the project, you need a component called a *render engine*, which builds a DirectShow filter graph from a timeline.</span></span> <span data-ttu-id="17b7a-106">Das Filter Diagramm rendert das Projekt tatsächlich.</span><span class="sxs-lookup"><span data-stu-id="17b7a-106">The filter graph is what actually renders the project.</span></span> <span data-ttu-id="17b7a-107">Mit der Rendering-Engine können Sie eine Vorschau eines Projekts anzeigen oder die endgültige Ausgabedatei schreiben.</span><span class="sxs-lookup"><span data-stu-id="17b7a-107">You can use the render engine to preview a project or to write the final output file.</span></span>

<span data-ttu-id="17b7a-108">In diesem Artikel wird die Renderingengine nicht ausführlich behandelt.</span><span class="sxs-lookup"><span data-stu-id="17b7a-108">This article does not go into detail about the render engine.</span></span> <span data-ttu-id="17b7a-109">Für die Vorschau benötigen Sie nur einige Methodenaufrufe.</span><span class="sxs-lookup"><span data-stu-id="17b7a-109">For preview, you only need a few method calls.</span></span> <span data-ttu-id="17b7a-110">Eine ausführlichere Erörterung finden Sie unter Informationen zum Schreiben von Ausgabedateien in [Rendern eines Projekts](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="17b7a-110">You can find a more thorough discussion, including how to write output files, in [Rendering a Project](rendering-a-project.md).</span></span> <span data-ttu-id="17b7a-111">Im folgenden Codebeispiel wird das Erstellen eines Vorschau Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="17b7a-111">The following code example shows how to construct a preview graph.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



<span data-ttu-id="17b7a-112">Erstellen Sie die Renderingengine mithilfe der **cokreateinstance** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="17b7a-112">Create the render engine using the **CoCreateInstance** function.</span></span> <span data-ttu-id="17b7a-113">Anschließend werden die folgenden Methoden für die " [**unenderengine**](irenderengine.md) "-Schnittstelle der Rendering-Engine aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="17b7a-113">Then call the following methods on the render engine's [**IRenderEngine**](irenderengine.md) interface:</span></span>

-   <span data-ttu-id="17b7a-114">[**Settimelineobject**](irenderengine-settimelineobject.md).</span><span class="sxs-lookup"><span data-stu-id="17b7a-114">[**SetTimelineObject**](irenderengine-settimelineobject.md).</span></span> <span data-ttu-id="17b7a-115">Gibt die zu verwendende Zeitachse an.</span><span class="sxs-lookup"><span data-stu-id="17b7a-115">Specifies the timeline to use.</span></span>
-   <span data-ttu-id="17b7a-116">[**Connectfrontend**](irenderengine-connectfrontend.md).</span><span class="sxs-lookup"><span data-stu-id="17b7a-116">[**ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span> <span data-ttu-id="17b7a-117">Erstellt ein partielles Filter Diagramm mit einem Ausgabepin für jede Gruppe in der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="17b7a-117">Builds a partial filter graph, with one output pin for each group in the timeline.</span></span>
-   <span data-ttu-id="17b7a-118">[**Renderoutputpins**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="17b7a-118">[**RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="17b7a-119">Schließt das Vorschau Diagramm ab, indem jede Ausgabe-PIN mit einem Video-oder audiorenderer verbunden wird.</span><span class="sxs-lookup"><span data-stu-id="17b7a-119">Completes the preview graph by connecting each output pin to a video or audio renderer.</span></span>

<span data-ttu-id="17b7a-120">Nachdem das Diagramm erstellt wurde, können Sie das Projekt in der Vorschau anzeigen, indem Sie das Diagramm wie bei jedem beliebigen DirectShow-Filter Diagramm ausführen.</span><span class="sxs-lookup"><span data-stu-id="17b7a-120">Once the graph is built, you can preview the project by running the graph, as you would with any DirectShow filter graph.</span></span> <span data-ttu-id="17b7a-121">Rufen Sie zuerst einen Zeiger auf das Filter Diagramm ab, indem Sie die Methode " [**irienderengine:: getfiltergraph**](irenderengine-getfiltergraph.md) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="17b7a-121">First, obtain a pointer to the filter graph by calling the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method.</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



<span data-ttu-id="17b7a-122">Abfragen des Filter Diagramms für die Schnittstellen [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) und [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="17b7a-122">Query the filter graph for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interfaces.</span></span> <span data-ttu-id="17b7a-123">Verwenden Sie diese beiden Schnittstellen zum Ausführen des Diagramms, und warten Sie auf den Abschluss der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="17b7a-123">Use these two interfaces to run the graph and wait for playback to complete.</span></span> <span data-ttu-id="17b7a-124">Eine Erläuterung zur Verwendung dieser Schnittstellen finden Sie unter wieder [Gabe einer Datei](how-to-play-a-file.md) und [reagieren auf Ereignisse](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="17b7a-124">For an explanation of how to use these interfaces, see [How To Play a File](how-to-play-a-file.md) and [Responding to Events](responding-to-events.md).</span></span> <span data-ttu-id="17b7a-125">Der folgende Code zeigt eine Möglichkeit, diese Schnittstellen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="17b7a-125">The following code shows one way to use these interfaces.</span></span>


```C++
IMediaControl   *pControl = NULL;
IMediaEvent     *pEvent = NULL;
long evCode;
pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
hr = pControl->Run();
hr = pEvent->WaitForCompletion(INFINITE, &evCode);
pControl->Stop();
```



<span data-ttu-id="17b7a-126">Der Code in diesem Beispiel blockiert die Ausführung des Programms, bis die Wiedergabe abgeschlossen ist, weil der unendliche Parameter im [**imediaevent:: waitforcompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) -Methodenaufrufe ist.</span><span class="sxs-lookup"><span data-stu-id="17b7a-126">The code in this example blocks program execution until playback completes, because of the INFINITE parameter in the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method call.</span></span> <span data-ttu-id="17b7a-127">Wenn während der Wiedergabe etwas schief geht, kann dies dazu führen, dass das Programm nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="17b7a-127">If something goes wrong during playback, however, it could cause the program to stop responding.</span></span> <span data-ttu-id="17b7a-128">Verwenden Sie in einer echten Anwendung eine Nachrichten Schleife, um auf den Abschluss der Wiedergabe zu warten.</span><span class="sxs-lookup"><span data-stu-id="17b7a-128">In a real application, use a message loop to wait for playback to complete.</span></span> <span data-ttu-id="17b7a-129">Außerdem wird empfohlen, dass Sie dem Benutzer eine Möglichkeit zur Unterbrechung der Wiedergabe bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="17b7a-129">It's also recommended that you provide the user with a way to interrupt playback.</span></span>

<span data-ttu-id="17b7a-130">Wenn Sie die Verwendung der Rendering-Engine abgeschlossen haben, müssen Sie immer die Methode " [**irienderengine:: scrapit**](irenderengine-scrapit.md) " aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="17b7a-130">When you finish using the render engine, always call the [**IRenderEngine::ScrapIt**](irenderengine-scrapit.md) method.</span></span> <span data-ttu-id="17b7a-131">Diese Methode löscht das Filter Diagramm und gibt alle Ressourcen frei, die von der Rendering-Engine aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="17b7a-131">This method deletes the filter graph and releases any resources held by the render engine.</span></span>


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a><span data-ttu-id="17b7a-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="17b7a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17b7a-133">Laden und Anzeigen der Vorschau eines Projekts</span><span class="sxs-lookup"><span data-stu-id="17b7a-133">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



