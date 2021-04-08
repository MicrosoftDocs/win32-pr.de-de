---
description: Aufbauen eines VMR-9-Filter Diagramms
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Aufbauen eines VMR-9-Filter Diagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860391"
---
# <a name="building-a-vmr-9-filter-graph"></a>Aufbauen eines VMR-9-Filter Diagramms

Da der Video Mischungs-Renderer 9-Filter (VMR-9) nicht der Standardvideorenderer ist, muss eine Anwendung, die VMR-9 verwendet, Sie explizit dem Diagramm hinzufügen und eine Verbindung herstellen. In diesem Abschnitt werden zwei unterschiedliche Ansätze zum Entwickeln von Filter Diagrammen mit VMR-9 vorgestellt.

Verwenden des Erfassungs Diagramm-Generators

Der Erfassungs Diagramm-Generator ist ein Hilfsobjekt zum Erstellen von benutzerdefinierten Filter Diagrammen. Sie können es verwenden, um VMR-9-Diagramme wie folgt zu erstellen:

1.  Erstellen und initialisieren Sie den Erfassungs Diagramm-Generator, wie im Thema [über den Erfassungs Diagramm](about-the-capture-graph-builder.md)-Generator beschrieben.
2.  Rufen Sie cokreateinstance auf, um VMR-9 zu erstellen:
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  Nennen Sie [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) im Filter Graph-Manager, um VMR-9 dem Filter Diagramm hinzuzufügen:
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  Aufrufen von [**igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) zum Hinzufügen eines Quell Filters für die Videodatei:
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  Nennen Sie die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode, um den Videostream für den VMR zu rendern:
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  Optional können Sie RenderStream erneut aufzurufen, um den Audiostream zu rendern:
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

Sie können mehrere Videostreams durch Aufrufen von addsourcefilter und RenderStream für jede Quelldatei mischen.

Verwenden des Filter Graph-Managers

Wenn Sie den Erfassungs Diagramm-Generator nicht verwenden möchten, können Sie wie folgt ein VMR-9-Diagramm erstellen, indem Sie einfach die Methoden im Diagramm-Manager des Filters verwenden:

1.  Erstellen Sie VMR-9, und fügen Sie es dem Diagramm hinzu, wie im vorherigen Verfahren gezeigt.
2.  Verwenden Sie addsourcefilter, um einen Quell Filter für die Videodatei hinzuzufügen, wie im vorherigen Verfahren gezeigt.
3.  Wenn Sie die Audiodatei Renren möchten, erstellen Sie eine Instanz des [DirectSound](directsound-renderer-filter.md) -rendererfilters, und fügen Sie Sie dem Filter Diagramm hinzu.
4.  Verwenden Sie die ibasefilter:: enumpins-Methode, um eine Ausgabe-PIN für den Quell Filter zu suchen. Weitere Informationen finden Sie unter Auflisten von [Pins](enumerating-pins.md) .
5.  Fragen Sie den Filter Graph-Manager nach der IFilterGraph2-Schnittstelle ab.
6.  Aufrufen von [**IFilterGraph2:: renderex**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) mit dem "am \_ renderex \_ renderonexistingrenderzer"-Flag. Dieser Aufruf rendert die Ausgabe-PIN, wobei nur die rendererfilter verwendet werden, die bereits im Diagramm vorhanden sind – in diesem Fall der VMR-9 und der DirectSound-Renderer. Dadurch wird verhindert, dass die intelligente Verbindungs Logik dem Diagramm den Standardvideorenderer hinzufügt, sodass die VMR-9 nicht verbunden ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Diagrammen mit dem Erfassungs Diagramm-Generator](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



