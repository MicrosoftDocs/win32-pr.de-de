---
description: Vorschau des Project
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Vorschau des Project
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d17d5fd0c87d98db2dac0a7ace97a72e2107eeb252561bbc535a5bd8b4a56d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748260"
---
# <a name="previewing-the-project"></a>Vorschau des Project

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Um eine Vorschau des Projekts anzuzeigen, benötigen Sie eine Komponente namens *Render-Engine,* die ein DirectShow-Filterdiagramm aus einer Zeitachse erstellt. Das Filterdiagramm rendert das Projekt tatsächlich. Sie können die Render-Engine verwenden, um eine Vorschau eines Projekts anzuzeigen oder die endgültige Ausgabedatei zu schreiben.

In diesem Artikel wird die Render-Engine nicht ausführlich behandelt. Für die Vorschau benötigen Sie nur einige Methodenaufrufe. Eine eingehendere Erörterung, einschließlich des Schreibens von Ausgabedateien, finden Sie unter [Rendering a Project.](rendering-a-project.md) Im folgenden Codebeispiel wird das Erstellen eines Vorschaudiagramms veranschaulicht.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



Erstellen Sie die Render-Engine mithilfe der **CoCreateInstance-Funktion.** Rufen Sie dann die folgenden Methoden auf der [**IRenderEngine-Schnittstelle der Render-Engine**](irenderengine.md) auf:

-   [**SetTimelineObject**](irenderengine-settimelineobject.md). Gibt die zu verwendende Zeitachse an.
-   [**ConnectFrontEnd**](irenderengine-connectfrontend.md). Erstellt ein partielles Filterdiagramm mit einem Ausgabepin für jede Gruppe in der Zeitachse.
-   [**RenderOutputPins**](irenderengine-renderoutputpins.md). Schließt das Vorschaudiagramm ab, indem jeder Ausgabepin mit einem Video- oder Audiorenderer verbunden wird.

Sobald das Diagramm erstellt wurde, können Sie eine Vorschau des Projekts anzeigen, indem Sie das Diagramm wie bei jedem DirectShow-Filterdiagramm ausführen. Rufen Sie zunächst einen Zeiger auf das Filterdiagramm ab, indem Sie die [**IRenderEngine::GetFilterGraph-Methode**](irenderengine-getfiltergraph.md) aufrufen.


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



Fragen Sie das Filterdiagramm für die [**Schnittstellen IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) und [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) ab. Verwenden Sie diese beiden Schnittstellen, um den Graphen ausführen und auf den Abschluss der Wiedergabe warten zu können. Eine Erläuterung der Verwendung dieser Schnittstellen finden Sie unter [How To Play a File](how-to-play-a-file.md) and [Responding to Events](responding-to-events.md). Der folgende Code zeigt eine Möglichkeit, diese Schnittstellen zu verwenden.


```C++
IMediaControl   *pControl = NULL;
IMediaEvent     *pEvent = NULL;
long evCode;
pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
hr = pControl->Run();
hr = pEvent->WaitForCompletion(INFINITE, &evCode);
pControl->Stop();
```



Der Code in diesem Beispiel blockiert die Programmausführung, bis die Wiedergabe abgeschlossen ist, da der INFINITE-Parameter im [**IMediaEvent::WaitForCompletion-Methodenaufruf**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) verwendet wird. Wenn während der Wiedergabe jedoch etwas schief geht, kann dies dazu führen, dass das Programm nicht mehr reagiert. Verwenden Sie in einer echten Anwendung eine Meldungsschleife, um auf den Abschluss der Wiedergabe zu warten. Es wird auch empfohlen, dass Sie dem Benutzer eine Möglichkeit bieten, die Wiedergabe zu unterbrechen.

Wenn Sie die Verwendung der Render-Engine abgeschlossen haben, rufen Sie immer die [**IRenderEngine::ScrapIt-Methode**](irenderengine-scrapit.md) auf. Diese Methode löscht das Filterdiagramm und gibt alle Ressourcen frei, die von der Render-Engine gespeichert werden.


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Laden und Anzeigen einer Vorschau Project](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



