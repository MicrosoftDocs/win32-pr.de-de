---
description: Informationen zum Capture Graph Builder
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: Informationen zum Capture Graph Builder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6ef82a160ada6e53fe6d2db830efa85118eb699074630905cd41f0b5412ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664517"
---
# <a name="about-the-capture-graph-builder"></a>Informationen zum Capture Graph Builder

Ein Filterdiagramm, das Video- oder Audioaufnahmen ausführt, wird als *Erfassungsdiagramm bezeichnet.* Erfassungsdiagramme sind oft komplizierter als Dateiwiedergabediagramme. Um Anwendungen das Erstellen von Erfassungsdiagrammen zu erleichtern, stellt DirectShow ein Hilfsobjekt namens Capture Graph Builder zur Verfügung. Der Capture Graph Builder macht die [**ICaptureGraphBuilder2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) verfügbar, die Methoden zum Erstellen und Steuern eines Erfassungsdiagramms enthält. Das folgende Diagramm veranschaulicht den Capture Graph Builder und die **ICaptureGraphBuilder2-Schnittstelle.**

![Verwenden des Generators für Erfassungsdiagramme](images/cgb01.png)

Rufen Sie zunächst CoCreateInstance auf, um neue Instanzen von Capture Graph Builder und Filter Graph Manager zu erstellen. Initialisieren Sie dann den Capture Graph Builder, indem [**Sie ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) mit einem Zeiger auf die [**IGraphBuilder-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) des Graph-Managers aufrufen. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Initialisieren des Generators für Erfassungsdiagramme](images/cgb03.png)

Der folgende Code zeigt eine Hilfsfunktion zum Ausführen dieser Schritte:


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



In diesem Abschnitt zur Videoaufnahme wird davon ausgegangen, dass Sie den Capture Graph Builder verwenden, um den Erfassungsgraphen zu erstellen. Es ist jedoch möglich, Erfassungsdiagramme vollständig mithilfe von IGraphBuilder-Methoden zu erstellen. Dies wird jedoch als erweitertes Thema betrachtet, und die Capture Graph Builder-Methoden werden bevorzugt. Weitere Informationen finden Sie unter [Erweiterte Erfassungsthemen.](advanced-capture-topics.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Videoaufnahme in DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



