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
# <a name="about-the-capture-graph-builder"></a>Informationen zum Erfassungs Diagramm-Generator

Ein Filter Diagramm, das Video-oder Audioerfassung durchführt, wird als *Aufzeichnungs Diagramm* bezeichnet. Erfassungs Diagramme sind häufig komplizierter als Diagramme für die Dateiwiedergabe. Um die Erstellung von Erfassungs Diagrammen für Anwendungen zu vereinfachen, stellt DirectShow ein Hilfsobjekt namens Erfassungs Diagramm-Generator bereit. Der Erfassungs Diagramm-Generator macht die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle verfügbar, die Methoden zum Erstellen und Steuern eines Aufzeichnungs Diagramms enthält. Das folgende Diagramm veranschaulicht den Erfassungs Diagramm-Generator und die **ICaptureGraphBuilder2** -Schnittstelle.

![Verwenden des Erfassungs Diagramm-Generators](images/cgb01.png)

Beginnen Sie, indem Sie CoCreateInstance aufrufen, um neue Instanzen des Erfassungs Diagramm-Generators und des Filter-Graph-Managers zu erstellen. Initialisieren Sie dann den Erfassungs Diagramm-Generator, indem Sie [**ICaptureGraphBuilder2:: setfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) mit einem Zeiger auf die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle des Filter Diagramms aufrufen. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Initialisieren des Erfassungs Diagramm-Generators](images/cgb03.png)

Der folgende Code zeigt eine Hilfsfunktion, um die folgenden Schritte auszuführen:


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



In diesem Abschnitt zur Video Erfassung wird davon ausgegangen, dass Sie den Erfassungs Diagramm-Generator verwenden, um das Aufzeichnungs Diagramm zu erstellen. Es ist jedoch möglich, Erfassungs Diagramme vollständig mithilfe von igraphbuilder-Methoden zu erstellen. Dies wird jedoch als erweitertes Thema angesehen, und die Methoden des Erfassungs Diagramm-Generators werden bevorzugt. Weitere Informationen finden Sie unter [Erweiterte Erfassungs Themen](advanced-capture-topics.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Video Erfassung in DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



