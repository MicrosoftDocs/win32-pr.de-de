---
description: Informationen zum Erfassungs Diagramm-Generator
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: Informationen zum Erfassungs Diagramm-Generator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae321665e0eae65a1d464bf87a12ac33e935d7ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958043"
---
# <a name="about-the-capture-graph-builder"></a><span data-ttu-id="d1fea-103">Informationen zum Erfassungs Diagramm-Generator</span><span class="sxs-lookup"><span data-stu-id="d1fea-103">About the Capture Graph Builder</span></span>

<span data-ttu-id="d1fea-104">Ein Filter Diagramm, das Video-oder Audioerfassung durchführt, wird als *Aufzeichnungs Diagramm* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d1fea-104">A filter graph that performs video or audio capture is called a *capture graph*.</span></span> <span data-ttu-id="d1fea-105">Erfassungs Diagramme sind häufig komplizierter als Diagramme für die Dateiwiedergabe.</span><span class="sxs-lookup"><span data-stu-id="d1fea-105">Capture graphs are often more complicated than file playback graphs.</span></span> <span data-ttu-id="d1fea-106">Um die Erstellung von Erfassungs Diagrammen für Anwendungen zu vereinfachen, stellt DirectShow ein Hilfsobjekt namens Erfassungs Diagramm-Generator bereit.</span><span class="sxs-lookup"><span data-stu-id="d1fea-106">To make it easier for applications to build capture graphs, DirectShow provides a helper object called the Capture Graph Builder.</span></span> <span data-ttu-id="d1fea-107">Der Erfassungs Diagramm-Generator macht die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle verfügbar, die Methoden zum Erstellen und Steuern eines Aufzeichnungs Diagramms enthält.</span><span class="sxs-lookup"><span data-stu-id="d1fea-107">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, which contains methods for building and controlling a capture graph.</span></span> <span data-ttu-id="d1fea-108">Das folgende Diagramm veranschaulicht den Erfassungs Diagramm-Generator und die **ICaptureGraphBuilder2** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d1fea-108">The following diagram illustrates the Capture Graph Builder and the **ICaptureGraphBuilder2** interface.</span></span>

![Verwenden des Erfassungs Diagramm-Generators](images/cgb01.png)

<span data-ttu-id="d1fea-110">Beginnen Sie, indem Sie CoCreateInstance aufrufen, um neue Instanzen des Erfassungs Diagramm-Generators und des Filter-Graph-Managers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1fea-110">Start by calling CoCreateInstance to create new instances of the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="d1fea-111">Initialisieren Sie dann den Erfassungs Diagramm-Generator, indem Sie [**ICaptureGraphBuilder2:: setfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) mit einem Zeiger auf die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle des Filter Diagramms aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d1fea-111">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="d1fea-112">Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d1fea-112">The following diagram illustrates this process.</span></span>

![Initialisieren des Erfassungs Diagramm-Generators](images/cgb03.png)

<span data-ttu-id="d1fea-114">Der folgende Code zeigt eine Hilfsfunktion, um die folgenden Schritte auszuführen:</span><span class="sxs-lookup"><span data-stu-id="d1fea-114">The following code shows a helper function to perform these steps:</span></span>


```C++
HRESULT InitCaptureGraphBuilder(
  IGraphBuilder **ppGraph,  // Receives the pointer.
  ICaptureGraphBuilder2 **ppBuild  // Receives the pointer.
)
{
    if (!ppGraph || !ppBuild)
    {
        return E_POINTER;
    }
    IGraphBuilder *pGraph = NULL;
    ICaptureGraphBuilder2 *pBuild = NULL;

    // Create the Capture Graph Builder.
    HRESULT hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, (void**)&pBuild );
    if (SUCCEEDED(hr))
    {
        // Create the Filter Graph Manager.
        hr = CoCreateInstance(CLSID_FilterGraph, 0, CLSCTX_INPROC_SERVER,
            IID_IGraphBuilder, (void**)&pGraph);
        if (SUCCEEDED(hr))
        {
            // Initialize the Capture Graph Builder.
            pBuild->SetFiltergraph(pGraph);

            // Return both interface pointers to the caller.
            *ppBuild = pBuild;
            *ppGraph = pGraph; // The caller must release both interfaces.
            return S_OK;
        }
        else
        {
            pBuild->Release();
        }
    }
    return hr; // Failed
}
```



<span data-ttu-id="d1fea-115">In diesem Abschnitt zur Video Erfassung wird davon ausgegangen, dass Sie den Erfassungs Diagramm-Generator verwenden, um das Aufzeichnungs Diagramm zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1fea-115">Throughout this section on video capture, it is assumed that you are using the Capture Graph Builder to create the capture graph.</span></span> <span data-ttu-id="d1fea-116">Es ist jedoch möglich, Erfassungs Diagramme vollständig mithilfe von igraphbuilder-Methoden zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1fea-116">However, it is possible to build capture graphs entirely by using IGraphBuilder methods.</span></span> <span data-ttu-id="d1fea-117">Dies wird jedoch als erweitertes Thema angesehen, und die Methoden des Erfassungs Diagramm-Generators werden bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="d1fea-117">This is considered an advanced topic, however, and the Capture Graph Builder methods are preferred.</span></span> <span data-ttu-id="d1fea-118">Weitere Informationen finden Sie unter [Erweiterte Erfassungs Themen](advanced-capture-topics.md).</span><span class="sxs-lookup"><span data-stu-id="d1fea-118">For more information, see [Advanced Capture Topics](advanced-capture-topics.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1fea-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d1fea-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1fea-120">Informationen zur Video Erfassung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d1fea-120">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



