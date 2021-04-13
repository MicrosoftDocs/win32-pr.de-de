---
description: Anzeigen einer Vorschau eines Projekts
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: Anzeigen einer Vorschau eines Projekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd9d299a99a0a7315cec986fbc044d427385647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341729"
---
# <a name="previewing-a-project"></a><span data-ttu-id="5612b-103">Anzeigen einer Vorschau eines Projekts</span><span class="sxs-lookup"><span data-stu-id="5612b-103">Previewing a Project</span></span>

<span data-ttu-id="5612b-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="5612b-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="5612b-105">Zum Anzeigen einer Vorschau eines Projekts rufen Sie zuerst **cokreateinstance** auf, um eine Instanz der grundlegenden Renderingengine zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5612b-105">To preview a project, first call **CoCreateInstance** to create an instance of the Basic Render Engine.</span></span> <span data-ttu-id="5612b-106">Der Klassen Bezeichner ist CLSID- \_ Renderengine.</span><span class="sxs-lookup"><span data-stu-id="5612b-106">The class identifier is CLSID\_RenderEngine.</span></span> <span data-ttu-id="5612b-107">Anschließend können Sie die Methode " [**irienderengine:: settimelineobject**](irenderengine-settimelineobject.md) " aufrufen, um die Zeitachse anzugeben, die Sie rendern.</span><span class="sxs-lookup"><span data-stu-id="5612b-107">Then call the [**IRenderEngine::SetTimelineObject**](irenderengine-settimelineobject.md) method to specify the timeline that you are rendering.</span></span>

<span data-ttu-id="5612b-108">Wenn Sie die Zeitachse zum ersten Mal in der Vorschau anzeigen, führen Sie die folgenden Aufrufe in der aufgeführten Reihenfolge durch</span><span class="sxs-lookup"><span data-stu-id="5612b-108">The first time that you preview the timeline, perform the following calls in the order listed:</span></span>

1.  <span data-ttu-id="5612b-109">Geben Sie " [**irienderengine:: strenderrange**](irenderengine-setrenderrange.md) " an, um den Teil der Zeitachse für die Vorschau anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5612b-109">Call [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md) to specify which portion of the timeline to preview.</span></span> <span data-ttu-id="5612b-110">(Optional)</span><span class="sxs-lookup"><span data-stu-id="5612b-110">(Optional)</span></span>
2.  <span data-ttu-id="5612b-111">Zum Erstellen des Front-Ends des Diagramms müssen Sie " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md) " ausführen.</span><span class="sxs-lookup"><span data-stu-id="5612b-111">Call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span>
3.  <span data-ttu-id="5612b-112">Nennen Sie " [**irienderengine:: renderoutputpins**](irenderengine-renderoutputpins.md)".</span><span class="sxs-lookup"><span data-stu-id="5612b-112">Call [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span> <span data-ttu-id="5612b-113">Diese Methode verbindet jede Ausgabe-PIN mit einem Videorenderer oder audiorenderer und vervollständigt das Diagramm.</span><span class="sxs-lookup"><span data-stu-id="5612b-113">This method connects each output pin to a video renderer or audio renderer, completing the graph.</span></span>

<span data-ttu-id="5612b-114">Das folgende Codebeispiel zeigt die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="5612b-114">The following code example shows these steps:</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



<span data-ttu-id="5612b-115">Führen Sie nun das Filter Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="5612b-115">Now run the filter graph.</span></span> <span data-ttu-id="5612b-116">Rufen Sie zuerst die Methode " [**unenderengine:: getfiltergraph**](irenderengine-getfiltergraph.md) " auf, um einen Zeiger auf die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle des Filter Graph-Managers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5612b-116">First, call the [**IRenderEngine::GetFilterGraph**](irenderengine-getfiltergraph.md) method to retrieve a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="5612b-117">Fragen Sie anschließend den Filter Graph-Manager nach der Schnittstelle [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) ab, und nennen Sie [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), wie im folgenden Code gezeigt:</span><span class="sxs-lookup"><span data-stu-id="5612b-117">Then query the Filter Graph Manager for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface and call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), as shown in the following code:</span></span>


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



<span data-ttu-id="5612b-118">Verwenden Sie die [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Schnittstelle des Filter Graph-Managers, um auf den Abschluss der Vorschau zu warten.</span><span class="sxs-lookup"><span data-stu-id="5612b-118">Use the Filter Graph Manager's [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to wait for the preview to complete.</span></span> <span data-ttu-id="5612b-119">Sie können das Diagramm auch mit der [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle des Filter Diagramms suchen, genauso wie bei einem Dateiwiedergabe Diagramm.</span><span class="sxs-lookup"><span data-stu-id="5612b-119">You can also seek the graph using the Filter Graph Manager's [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, just as you would with a file playback graph.</span></span>

<span data-ttu-id="5612b-120">Um das Projekt erneut in der Vorschau anzuzeigen, suchen Sie im Diagramm nach der Zeit NULL, und **führen** Sie den Aufruf erneut aus</span><span class="sxs-lookup"><span data-stu-id="5612b-120">To preview the project again, seek the graph back to time zero and call **Run** again.</span></span> <span data-ttu-id="5612b-121">Wenn Sie den Inhalt der Zeitachse ändern, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="5612b-121">If you change the contents of the timeline, do the following:</span></span>

1.  <span data-ttu-id="5612b-122">Ruft den "\*"- **trendbereich** auf.</span><span class="sxs-lookup"><span data-stu-id="5612b-122">Call **SetRenderRange**.</span></span> <span data-ttu-id="5612b-123">(Optional)</span><span class="sxs-lookup"><span data-stu-id="5612b-123">(Optional)</span></span>
2.  <span data-ttu-id="5612b-124">Ruft **connectfrontend** auf.</span><span class="sxs-lookup"><span data-stu-id="5612b-124">Call **ConnectFrontEnd**.</span></span>
3.  <span data-ttu-id="5612b-125">Wenn die **connectfrontend** -Methode "S Warn Ausgabe" zurückgibt \_ \_ , wird " **renderoutputpins**" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5612b-125">If the **ConnectFrontEnd** method returns S\_WARN\_OUTPUTRESET, call **RenderOutputPins**.</span></span> <span data-ttu-id="5612b-126">(Wenn **connectfrontend** S \_ zurückgibt OK, Sie können diesen Schritt überspringen.)</span><span class="sxs-lookup"><span data-stu-id="5612b-126">(If **ConnectFrontEnd** returns S\_OK, you can skip this step.)</span></span>
4.  <span data-ttu-id="5612b-127">Suchen Sie im Diagramm nach der Zeit NULL.</span><span class="sxs-lookup"><span data-stu-id="5612b-127">Seek the graph back to time zero.</span></span>
5.  <span data-ttu-id="5612b-128">Führen Sie das Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="5612b-128">Run the graph.</span></span>

<span data-ttu-id="5612b-129">Das folgende Beispiel zeigt die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="5612b-129">The following example shows these steps:</span></span>


```C++
hr = pRender->ConnectFrontEnd();
if (hr == S_WARN_OUTPUTRESET)
{
    hr = pRender->RenderOutputPins();
}
LONGLONG llStart = 0; 
hr = pSeek->SetPositions(&llStart, AM_SEEKING_AbsolutePositioning, 0, 0); 
hr = pControl->Run();
```



<span data-ttu-id="5612b-130">Ein umfassendes Beispiel, das eine Projektdatei lädt und anzeigt, finden Sie unter [Laden und Anzeigen der Vorschau eines Projekts](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="5612b-130">For a complete example that loads and previews a project file, see [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5612b-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5612b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5612b-132">Verwalten von Video Bearbeitungs Projekten</span><span class="sxs-lookup"><span data-stu-id="5612b-132">Managing Video Editing Projects</span></span>](managing-video-editing-projects.md)
</dt> <dt>

[<span data-ttu-id="5612b-133">Rendern eines Projekts</span><span class="sxs-lookup"><span data-stu-id="5612b-133">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



