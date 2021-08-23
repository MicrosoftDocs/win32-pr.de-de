---
description: Erstellen eines VMR-9-Graph
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Erstellen eines VMR-9-Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86a76b2d4519299bbd9cde498ccf6a4bc33f0b819d3996faac794154d08c8bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689350"
---
# <a name="building-a-vmr-9-filter-graph"></a>Erstellen eines VMR-9-Graph

Da der Video Mixing Renderer 9-Filter (VMR-9) nicht der Standardvideorenderer ist, muss eine Anwendung, die VMR-9 verwendet, ihn explizit dem Diagramm hinzufügen und verbinden. In diesem Abschnitt werden zwei verschiedene Ansätze zum Erstellen von Filterdiagrammen mit VMR-9 beschrieben.

Verwenden des Capture Graph Builder

Der Capture Graph Builder ist ein Hilfsobjekt zum Erstellen benutzerdefinierter Filterdiagramme. Sie können damit VMR-9-Diagramme wie folgt erstellen:

1.  Erstellen und initialisieren Sie den Capture Graph Builder, wie im Thema [About the Capture Graph Builder beschrieben.](about-the-capture-graph-builder.md)
2.  Rufen Sie CoCreateInstance auf, um VMR-9 zu erstellen:
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  Rufen [**Sie IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) im Filter Graph Manager auf, um VMR-9 dem Filterdiagramm hinzuzufügen:
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  Rufen [**Sie IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) auf, um einen Quellfilter für die Videodatei hinzuzufügen:
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  Rufen Sie die [**ICaptureGraphBuilder2::RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) auf, um den Videostream an den virtuellen Computer zu rendern:
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  Optional können Sie RenderStream erneut aufrufen, um den Audiostream zu rendern:
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

Sie können mehrere Videostreams mischen, indem Sie AddSourceFilter und RenderStream für jede Quelldatei aufrufen.

Verwenden des Filter-Graph-Managers

Wenn Sie den Capture Graph Builder nicht verwenden möchten, können Sie ein VMR-9-Diagramm wie folgt einfach mithilfe von Methoden im Filter Graph Manager erstellen:

1.  Erstellen Sie VMR-9, und fügen Sie es dem Diagramm hinzu, wie im vorherigen Verfahren gezeigt.
2.  Verwenden Sie AddSourceFilter, um einen Quellfilter für die Videodatei hinzuzufügen, wie im vorherigen Verfahren gezeigt.
3.  Wenn Sie die Audiodaten rendern möchten, erstellen Sie eine Instanz des [DirectSound-Rendererfilters,](directsound-renderer-filter.md) und fügen Sie sie dem Filterdiagramm hinzu.
4.  Verwenden Sie die IBaseFilter::EnumPins-Methode, um einen Ausgabepin im Quellfilter zu finden. Weitere [Informationen finden Sie unter Aufzählen von Pins.](enumerating-pins.md)
5.  Fragen Sie den Filter Graph Manager für die IFilterGraph2-Schnittstelle ab.
6.  Rufen [**Sie IFilterGraph2::RenderEx mit**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) dem AM \_ RENDEREX \_ RENDERTOEXISTINGRENDERERS-Flag auf. Durch diesen Aufruf wird der Ausgabepin gerendert, und es werden nur die Rendererfilter verwendet, die bereits im Diagramm vorhanden sind– in diesem Fall vmr-9 und directsound renderer. Dadurch wird verhindert, Verbinden Intelligent Verbinden dem Diagramm den Standardvideorenderer hinzufügen kann, wodurch vmr-9 nicht verbunden ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Diagrammen mit dem Capture Graph Builder](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



