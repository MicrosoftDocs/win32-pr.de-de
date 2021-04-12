---
description: 'DES-Fehler Protokollierung: Beispiel Code'
ms.assetid: e734daed-9230-4376-839f-7e09da7bc275
title: 'DES-Fehler Protokollierung: Beispiel Code'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9e0d47535e1d4035669a0e672a30fb2520c676
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522779"
---
# <a name="des-error-logging-example-code"></a>DES-Fehler Protokollierung: Beispiel Code

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Der folgende Beispielcode zeigt eine komplette Konsolenanwendung, die eine [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) -XML-Projektdatei mithilfe der in diesem Abschnitt beschriebenen Fehler Protokollierungs Klasse lädt und anzeigt. (Siehe [Protokollierungs Fehler](logging-errors.md).) Der Name der Projektdatei ist in der Anwendung hart codiert.

Um den Code zu verkürzen, verwendet die Konsolenanwendung ATL-intelligente Zeiger, sodass **QueryInterface** und **Release** nicht aufgerufen werden müssen. Wenn Sie es vorziehen, können Sie die Beispielanwendung beim [Laden und Anzeigen der Vorschau eines Projekts](loading-and-previewing-a-project.md)ändern. Fügen Sie einfach den im vorherigen Abschnitt gezeigten Code hinzu.


```C++
#include <atlbase.h>
#include <dshow.h>
#include <qedit.h>
#include <stdio.h>

// Declare error logging class.
class CErrReporter;

// (The implementation of CErrReporter was given previously.)

void __cdecl main(void)
{
    HRESULT hr = CoInitialize(NULL);

    if (FAILED(hr))
    {
        // Error handling is omitted for clarity.
    }

    { // Scope for smart pointers.

    CComPtr<IAMTimeline>   pTL;
    CComPtr<IRenderEngine> pRenderEngine; 
    CComPtr<IXml2Dex>      pXML; 
    CComPtr<IGraphBuilder> pGraph;

    hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
                IID_IAMTimeline, (void**) &pTL);
    hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
                IID_IXml2Dex, (void**) &pXML);
    hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
                IID_IRenderEngine, (void**) &pRenderEngine);

    // Set the error log.
    CComQIPtr<IAMSetErrorLog, &IID_IAMSetErrorLog> pSetLog(pTL);
    if (pSetLog)
    {
        IAMErrorLog *pLog = new CErrReporter;    
        pSetLog->put_ErrorLog(pLog);
    }
   
    // Load and preview the project.
    CComBSTR bstrFile(OLESTR("C:\\example.xtl"));
    hr = pXML->ReadXMLFile(pTL, bstrFile); 
    if (SUCCEEDED(hr))
    {
        hr = pRenderEngine->SetTimelineObject(pTL);
        hr = pRenderEngine->ConnectFrontEnd( );
        hr = pRenderEngine->RenderOutputPins( );
        hr = pRenderEngine->GetFilterGraph(&pGraph);

        CComQIPtr<IMediaControl, &IID_IMediaControl> pControl(pGraph);
        CComQIPtr<IMediaEvent, &IID_IMediaEvent> pEvent(pGraph);
        pControl->Run();

        long evCode;
        hr = pEvent->WaitForCompletion(INFINITE, &evCode);
        pControl->Stop();
    }
    // Clean up.
    pRenderEngine->ScrapIt();
    }
    CoUninitialize();
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Protokollierungs Fehler](logging-errors.md)
</dt> </dl>

 

 



