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
# <a name="previewing-a-project"></a>Anzeigen einer Vorschau eines Projekts

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Zum Anzeigen einer Vorschau eines Projekts rufen Sie zuerst **cokreateinstance** auf, um eine Instanz der grundlegenden Renderingengine zu erstellen. Der Klassen Bezeichner ist CLSID- \_ Renderengine. Anschließend können Sie die Methode " [**irienderengine:: settimelineobject**](irenderengine-settimelineobject.md) " aufrufen, um die Zeitachse anzugeben, die Sie rendern.

Wenn Sie die Zeitachse zum ersten Mal in der Vorschau anzeigen, führen Sie die folgenden Aufrufe in der aufgeführten Reihenfolge durch

1.  Geben Sie " [**irienderengine:: strenderrange**](irenderengine-setrenderrange.md) " an, um den Teil der Zeitachse für die Vorschau anzugeben. (Optional)
2.  Zum Erstellen des Front-Ends des Diagramms müssen Sie " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md) " ausführen.
3.  Nennen Sie " [**irienderengine:: renderoutputpins**](irenderengine-renderoutputpins.md)". Diese Methode verbindet jede Ausgabe-PIN mit einem Videorenderer oder audiorenderer und vervollständigt das Diagramm.

Das folgende Codebeispiel zeigt die folgenden Schritte:


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



Führen Sie nun das Filter Diagramm aus. Rufen Sie zuerst die Methode " [**unenderengine:: getfiltergraph**](irenderengine-getfiltergraph.md) " auf, um einen Zeiger auf die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle des Filter Graph-Managers abzurufen. Fragen Sie anschließend den Filter Graph-Manager nach der Schnittstelle [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) ab, und nennen Sie [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), wie im folgenden Code gezeigt:


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



Verwenden Sie die [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Schnittstelle des Filter Graph-Managers, um auf den Abschluss der Vorschau zu warten. Sie können das Diagramm auch mit der [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle des Filter Diagramms suchen, genauso wie bei einem Dateiwiedergabe Diagramm.

Um das Projekt erneut in der Vorschau anzuzeigen, suchen Sie im Diagramm nach der Zeit NULL, und **führen** Sie den Aufruf erneut aus Wenn Sie den Inhalt der Zeitachse ändern, gehen Sie folgendermaßen vor:

1.  Ruft den "*"- **trendbereich** auf. (Optional)
2.  Ruft **connectfrontend** auf.
3.  Wenn die **connectfrontend** -Methode "S Warn Ausgabe" zurückgibt \_ \_ , wird " **renderoutputpins**" aufgerufen. (Wenn **connectfrontend** S \_ zurückgibt OK, Sie können diesen Schritt überspringen.)
4.  Suchen Sie im Diagramm nach der Zeit NULL.
5.  Führen Sie das Diagramm aus.

Das folgende Beispiel zeigt die folgenden Schritte:


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



Ein umfassendes Beispiel, das eine Projektdatei lädt und anzeigt, finden Sie unter [Laden und Anzeigen der Vorschau eines Projekts](loading-and-previewing-a-project.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten von Video Bearbeitungs Projekten](managing-video-editing-projects.md)
</dt> <dt>

[Rendern eines Projekts](rendering-a-project.md)
</dt> </dl>

 

 



