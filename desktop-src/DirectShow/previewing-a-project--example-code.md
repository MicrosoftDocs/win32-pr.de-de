---
description: 'Vorschau einer Project: Beispielcode'
ms.assetid: 8a4af82a-5611-4c53-8de8-04eaefd51df9
title: 'Vorschau einer Project: Beispielcode'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a47970a333ed27e249bddc81ba6fb4fb6e2c706fdfa2dda7c29f886e74022
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583570"
---
# <a name="previewing-a-project-example-code"></a>Vorschau einer Project: Beispielcode

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Das folgende Codebeispiel zeigt, wie Sie ein [DirectShow Editing Services-Projekt](directshow-editing-services.md) laden und eine Vorschau anzeigen. Die Fehlerüberprüfung wird aus Gründen der Übersichtlichkeit ausgelassen.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Laden eines Project und Anzeigen einer Vorschau](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



