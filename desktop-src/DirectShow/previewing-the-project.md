---
description: Anzeigen der Vorschau des Projekts
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Anzeigen der Vorschau des Projekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf38fe19e500cfe9bd9a8dfb77f7ff56528a2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958019"
---
# <a name="previewing-the-project"></a>Anzeigen der Vorschau des Projekts

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Zum Anzeigen einer Vorschau des Projekts benötigen Sie eine Komponente, die als *Renderengine* bezeichnet wird und ein DirectShow-Filter Diagramm aus einer Zeitachse erstellt. Das Filter Diagramm rendert das Projekt tatsächlich. Mit der Rendering-Engine können Sie eine Vorschau eines Projekts anzeigen oder die endgültige Ausgabedatei schreiben.

In diesem Artikel wird die Renderingengine nicht ausführlich behandelt. Für die Vorschau benötigen Sie nur einige Methodenaufrufe. Eine ausführlichere Erörterung finden Sie unter Informationen zum Schreiben von Ausgabedateien in [Rendern eines Projekts](rendering-a-project.md). Im folgenden Codebeispiel wird das Erstellen eines Vorschau Diagramms veranschaulicht.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



Erstellen Sie die Renderingengine mithilfe der **cokreateinstance** -Funktion. Anschließend werden die folgenden Methoden für die " [**unenderengine**](irenderengine.md) "-Schnittstelle der Rendering-Engine aufgerufen:

-   [**Settimelineobject**](irenderengine-settimelineobject.md). Gibt die zu verwendende Zeitachse an.
-   [**Connectfrontend**](irenderengine-connectfrontend.md). Erstellt ein partielles Filter Diagramm mit einem Ausgabepin für jede Gruppe in der Zeitachse.
-   [**Renderoutputpins**](irenderengine-renderoutputpins.md). Schließt das Vorschau Diagramm ab, indem jede Ausgabe-PIN mit einem Video-oder audiorenderer verbunden wird.

Nachdem das Diagramm erstellt wurde, können Sie das Projekt in der Vorschau anzeigen, indem Sie das Diagramm wie bei jedem beliebigen DirectShow-Filter Diagramm ausführen. Rufen Sie zuerst einen Zeiger auf das Filter Diagramm ab, indem Sie die Methode " [**irienderengine:: getfiltergraph**](irenderengine-getfiltergraph.md) " aufrufen.


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



Abfragen des Filter Diagramms für die Schnittstellen [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) und [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) . Verwenden Sie diese beiden Schnittstellen zum Ausführen des Diagramms, und warten Sie auf den Abschluss der Wiedergabe. Eine Erläuterung zur Verwendung dieser Schnittstellen finden Sie unter wieder [Gabe einer Datei](how-to-play-a-file.md) und [reagieren auf Ereignisse](responding-to-events.md). Der folgende Code zeigt eine Möglichkeit, diese Schnittstellen zu verwenden.


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



Der Code in diesem Beispiel blockiert die Ausführung des Programms, bis die Wiedergabe abgeschlossen ist, weil der unendliche Parameter im [**imediaevent:: waitforcompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) -Methodenaufrufe ist. Wenn während der Wiedergabe etwas schief geht, kann dies dazu führen, dass das Programm nicht mehr reagiert. Verwenden Sie in einer echten Anwendung eine Nachrichten Schleife, um auf den Abschluss der Wiedergabe zu warten. Außerdem wird empfohlen, dass Sie dem Benutzer eine Möglichkeit zur Unterbrechung der Wiedergabe bereitstellen.

Wenn Sie die Verwendung der Rendering-Engine abgeschlossen haben, müssen Sie immer die Methode " [**irienderengine:: scrapit**](irenderengine-scrapit.md) " aufzurufen. Diese Methode löscht das Filter Diagramm und gibt alle Ressourcen frei, die von der Rendering-Engine aufbewahrt werden.


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Laden und Anzeigen der Vorschau eines Projekts](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



