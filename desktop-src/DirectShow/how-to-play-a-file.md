---
description: Wiedergeben einer Datei
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Wiedergeben einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc84ef751db318354da36454e6a30fd2ce4bd8e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392817"
---
# <a name="how-to-play-a-file"></a>Wiedergeben einer Datei

Dieser Artikel soll Ihnen den Geschmack der DirectShow-Programmierung verleihen. Sie stellt eine einfache Konsolenanwendung dar, die eine Audiodatei oder Videodatei wieder gibt. Das Programm ist nur ein paar Zeilen lang, aber es zeigt einen Teil der Leistungsfähigkeit der DirectShow-Programmierung.

Wie im Artikel [Einführung in die DirectShow-Anwendungsprogrammierung](introduction-to-directshow-application-programming.md) beschrieben, führt eine DirectShow-Anwendung immer die gleichen grundlegenden Schritte aus:

1.  Erstellen Sie eine Instanz des [Filter Graph-Managers](filter-graph-manager.md).
2.  Verwenden Sie den Filter Graph-Manager, um ein Filter Diagramm zu erstellen.
3.  Führen Sie das Diagramm aus, sodass die Daten durch die Filter verschoben werden.

Um den Code in diesem Thema zu kompilieren und zu verknüpfen, schließen Sie die Header Datei "DShow. h" ein, und verknüpfen Sie die Datei "" mit der statischen Bibliotheksdatei "". Weitere Informationen finden Sie unter [Building DirectShow Applications](setting-up-the-build-environment.md).

Starten Sie, indem Sie [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) oder [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen, um die com-Bibliothek zu initialisieren:


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



Um dies zu gewährleisten, wird in diesem Beispiel der Rückgabewert ignoriert, aber Sie sollten den **HRESULT** -Wert immer über einen beliebigen Methoden Aufrufwert überprüfen.

Rufen Sie als nächstes [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um den Filter Graph-Manager zu erstellen:


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



Wie gezeigt, ist der Klassen Bezeichner (CLSID) CLSID \_ Filtergraph. Der Filter Graph-Manager wird von einer Prozess internen dll bereitgestellt, sodass der Ausführungs Kontext **CLSCTX \_ INPROC \_ Server** ist. DirectShow unterstützt das kostenlose Threading Modell, sodass Sie auch [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) mit dem **coinit- \_ multithreadflag** aufrufen können.

Der Aufruf von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) gibt die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle zurück, die größtenteils Methoden zum Aufbau des Filter Diagramms enthält. Für dieses Beispiel sind zwei weitere Schnittstellen erforderlich:

-   [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) steuert das Streaming. Sie enthält Methoden zum Beenden und Starten des Diagramms.
-   [**Imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) verfügt über Methoden zum erhalten von Ereignissen aus dem Filter Graph-Manager. In diesem Beispiel wird die-Schnittstelle verwendet, um auf den Abschluss der Wiedergabe zu warten.

Beide Schnittstellen werden vom Filter Graph-Manager verfügbar gemacht. Verwenden Sie den zurückgegebenen [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Zeiger, um Sie abzufragen:


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



Nun können Sie das Filter Diagramm erstellen. Bei der Wiedergabe von Dateien wird dies durch einen einzelnen Methoden Aufrufvorgang durchgeführt:


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



Die [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) -Methode erstellt ein Filter Diagramm, das die angegebene Datei wiedergeben kann. Der erste Parameter ist der Dateiname, der als breit Zeichen-Zeichenfolge (2 Byte) dargestellt wird. Der zweite Parameter ist reserviert und muss gleich **null** sein.

Diese Methode kann fehlschlagen, wenn die angegebene Datei nicht vorhanden ist oder das Dateiformat nicht erkannt wird. Angenommen, die Methode ist erfolgreich, aber das Filter Diagramm ist jetzt für die Wiedergabe bereit. Um das Diagramm auszuführen, müssen Sie die [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) -Methode aufzurufen:


```C++
hr = pControl->Run();
```



Wenn das Filter Diagramm ausgeführt wird, werden die Daten durch die Filter verschoben und als Video und Audiodatei gerendert. Die Wiedergabe erfolgt in einem separaten Thread. Sie können warten, bis die Wiedergabe abgeschlossen ist, indem Sie die [**imediaevent:: waitforcompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) -Methode aufrufen:


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



Diese Methode wird blockiert, bis die Wiedergabe der Datei abgeschlossen ist, oder bis das angegebene Timeout Intervall abläuft. Der Wert unendlich bedeutet, dass die Anwendung unbegrenzt blockiert wird, bis die Datei wiedergegeben wird. Ein realistischeres Beispiel für die Ereignis Behandlung finden [Sie unter reagieren auf Ereignisse](responding-to-events.md).

Wenn die Anwendung abgeschlossen ist, geben Sie die Schnittstellen Zeiger frei, und schließen Sie die com-Bibliothek:


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a>Beispielcode

Im folgenden finden Sie den gesamten Code für das Beispiel, das in diesem Artikel beschrieben wird:


```C++
#include <dshow.h>
void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the filter graph manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file on your system.
    hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende DirectShow-Aufgaben](basic-directshow-tasks.md)
</dt> </dl>

 

 
