---
description: 'Anzeigen einer Vorschau eines Projekts: Beispiel Code'
ms.assetid: 8a4af82a-5611-4c53-8de8-04eaefd51df9
title: 'Anzeigen einer Vorschau eines Projekts: Beispiel Code'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c5527fd93d0f05d5388739cc936e4a4dd203e18
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481723"
---
# <a name="previewing-a-project-example-code"></a><span data-ttu-id="d9e6f-103">Anzeigen einer Vorschau eines Projekts: Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="d9e6f-103">Previewing a Project: Example Code</span></span>

<span data-ttu-id="d9e6f-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="d9e6f-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="d9e6f-105">Im folgenden Codebeispiel wird veranschaulicht, wie ein [DirectShow-Bearbeitungs Dienst](directshow-editing-services.md) Projekt geladen und in der Vorschau angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d9e6f-105">The following code example shows how to load and preview a [DirectShow Editing Services](directshow-editing-services.md) project.</span></span> <span data-ttu-id="d9e6f-106">Die Fehlerüberprüfung wird aus Gründen der Übersichtlichkeit ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="d9e6f-106">Error checking is omitted for clarity.</span></span>


```C++
#include <dshow.h>
#include <qedit.h>

// Preview a timeline.
void PreviewTL(IAMTimeline *pTL, IRenderEngine *pRender) 
{
    HRESULT hr;
    IGraphBuilder   *pGraph = NULL;
    IMediaControl   *pControl = NULL;
    IMediaEvent     *pEvent = NULL;

    // Build the graph.
    hr = pRender->SetTimelineObject(pTL);
    hr = pRender->ConnectFrontEnd( );
    hr = pRender->RenderOutputPins( );

    // Run the graph.
    hr = pRender->GetFilterGraph(&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
    hr = pControl->Run();

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
    pControl->Stop();

    // Clean up.
    pEvent->Release();
    pControl->Release();
    pGraph->Release();
}

void main( void )
{
    HRESULT         hr;
    IAMTimeline     *pTL = NULL;
    IRenderEngine   *pRender = NULL; 
    IXml2Dex        *pXML = NULL; 

    CoInitialize(NULL);
    hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
                IID_IAMTimeline, (void**)&pTL);
    hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
                IID_IXml2Dex, (void**)&pXML);
    hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
                IID_IRenderEngine, (void**)&pRender);

    // Load a project file.
    BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
    hr = pXML->ReadXMLFile(pTL, bstrFile); 
    SysFreeString(bstrFile);
    pXML->Release();

    PreviewTL(pTL, pRender);

    // Clean up.    
    pRender->ScrapIt();
    pTL->Release();
    pRender->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a><span data-ttu-id="d9e6f-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d9e6f-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9e6f-108">Laden und Anzeigen der Vorschau eines Projekts</span><span class="sxs-lookup"><span data-stu-id="d9e6f-108">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



