---
description: Vorschau einer Project
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: Vorschau einer Project
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159303c175c459b4d5d93ba4c7b4b2622caddac2a35d3474a3059ac703d62645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583559"
---
# <a name="previewing-a-project"></a>Vorschau einer Project

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Um eine Vorschau eines Projekts anzuzeigen, rufen Sie zunächst **CoCreateInstance** auf, um eine Instanz der Basic-Render-Engine zu erstellen. Der Klassenbezeichner ist CLSID \_ RenderEngine. Rufen Sie dann die [**IRenderEngine::SetTimelineObject-Methode**](irenderengine-settimelineobject.md) auf, um die Zeitachse anzugeben, die Sie rendern.

Wenn Sie zum ersten Mal eine Vorschau der Zeitachse anzeigen, führen Sie die folgenden Aufrufe in der aufgeführten Reihenfolge aus:

1.  Rufen Sie [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md) auf, um anzugeben, welcher Teil der Zeitachse in der Vorschau angezeigt werden soll. (Optional)
2.  Rufen Sie [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) auf, um das Front-End des Graphen zu erstellen.
3.  Rufen Sie [**IRenderEngine::RenderOutputPins auf.**](irenderengine-renderoutputpins.md) Diese Methode verbindet jeden Ausgabepin mit einem Videorenderer oder Audiorenderer und vervollständigt das Diagramm.

Das folgende Codebeispiel zeigt diese Schritte:


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



Führen Sie nun das Filterdiagramm aus. Rufen Sie zunächst die [**IRenderEngine::GetFilterGraph-Methode**](irenderengine-getfiltergraph.md) auf, um einen Zeiger auf die [**IGraphBuilder-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) von Filter Graph Manager abzurufen. Fragen Sie dann den Filter Graph Manager für die [**IMediaControl-Schnittstelle**](/windows/desktop/api/Control/nn-control-imediacontrol) ab, und rufen [**Sie IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run)auf, wie im folgenden Code gezeigt:


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



Verwenden Sie die [**IMediaEventEx-Schnittstelle**](/windows/desktop/api/Control/nn-control-imediaeventex) von Filter Graph Manager, um auf den Abschluss der Vorschau zu warten. Sie können das Diagramm auch mithilfe der [**IMediaSeeking-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) von Filter Graph Manager suchen, genau wie bei einem Dateiwiedergabediagramm.

Um die Vorschau des Projekts erneut anzuzeigen, suchen Sie den Graphen zurück zur Zeit 0 (null), und rufen **Sie erneut Ausführen auf.** Wenn Sie den Inhalt der Zeitachse ändern, gehen Sie wie folgt vor:

1.  Rufen Sie **SetRenderRange auf.** (Optional)
2.  Rufen Sie **ConnectFrontEnd auf.**
3.  Wenn die **ConnectFrontEnd-Methode** S \_ WARN \_ OUTPUTRESET zurückgibt, rufen **Sie RenderOutputPins auf.** (Wenn **ConnectFrontEnd** S \_ zurückgibt OK, Sie können diesen Schritt überspringen.)
4.  Suchen Sie den Graphen zurück zur Zeit 0 (null).
5.  Führen Sie das Diagramm aus.

Das folgende Beispiel zeigt diese Schritte:


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



Ein vollständiges Beispiel, in dem eine Projektdatei geladen und in der Vorschau angezeigt wird, finden Sie unter [Loading and Previewing a Project](loading-and-previewing-a-project.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten von Videobearbeitungsprojekten](managing-video-editing-projects.md)
</dt> <dt>

[Rendern eines Project](rendering-a-project.md)
</dt> </dl>

 

 



