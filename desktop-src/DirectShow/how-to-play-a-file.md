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
# <a name="how-to-play-a-file"></a><span data-ttu-id="614cd-103">Wiedergeben einer Datei</span><span class="sxs-lookup"><span data-stu-id="614cd-103">How To Play a File</span></span>

<span data-ttu-id="614cd-104">Dieser Artikel soll Ihnen den Geschmack der DirectShow-Programmierung verleihen.</span><span class="sxs-lookup"><span data-stu-id="614cd-104">This article is intended to give you the flavor of DirectShow programming.</span></span> <span data-ttu-id="614cd-105">Sie stellt eine einfache Konsolenanwendung dar, die eine Audiodatei oder Videodatei wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="614cd-105">It presents a simple console application that plays an audio or video file.</span></span> <span data-ttu-id="614cd-106">Das Programm ist nur ein paar Zeilen lang, aber es zeigt einen Teil der Leistungsfähigkeit der DirectShow-Programmierung.</span><span class="sxs-lookup"><span data-stu-id="614cd-106">The program is only a few lines long, but it demonstrates some of the power of DirectShow programming.</span></span>

<span data-ttu-id="614cd-107">Wie im Artikel [Einführung in die DirectShow-Anwendungsprogrammierung](introduction-to-directshow-application-programming.md) beschrieben, führt eine DirectShow-Anwendung immer die gleichen grundlegenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="614cd-107">As the article [Introduction to DirectShow Application Programming](introduction-to-directshow-application-programming.md) describes, a DirectShow application always performs the same basic steps:</span></span>

1.  <span data-ttu-id="614cd-108">Erstellen Sie eine Instanz des [Filter Graph-Managers](filter-graph-manager.md).</span><span class="sxs-lookup"><span data-stu-id="614cd-108">Create an instance of the [Filter Graph Manager](filter-graph-manager.md).</span></span>
2.  <span data-ttu-id="614cd-109">Verwenden Sie den Filter Graph-Manager, um ein Filter Diagramm zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="614cd-109">Use the Filter Graph Manager to build a filter graph.</span></span>
3.  <span data-ttu-id="614cd-110">Führen Sie das Diagramm aus, sodass die Daten durch die Filter verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="614cd-110">Run the graph, causing data to move through the filters.</span></span>

<span data-ttu-id="614cd-111">Um den Code in diesem Thema zu kompilieren und zu verknüpfen, schließen Sie die Header Datei "DShow. h" ein, und verknüpfen Sie die Datei "" mit der statischen Bibliotheksdatei "".</span><span class="sxs-lookup"><span data-stu-id="614cd-111">To compile and link the code in this topic, include the header file Dshow.h and link to the static library file strmiids.lib.</span></span> <span data-ttu-id="614cd-112">Weitere Informationen finden Sie unter [Building DirectShow Applications](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="614cd-112">For more information, see [Building DirectShow Applications](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="614cd-113">Starten Sie, indem Sie [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) oder [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen, um die com-Bibliothek zu initialisieren:</span><span class="sxs-lookup"><span data-stu-id="614cd-113">Start by calling [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library:</span></span>


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



<span data-ttu-id="614cd-114">Um dies zu gewährleisten, wird in diesem Beispiel der Rückgabewert ignoriert, aber Sie sollten den **HRESULT** -Wert immer über einen beliebigen Methoden Aufrufwert überprüfen.</span><span class="sxs-lookup"><span data-stu-id="614cd-114">To keep things simple, this example ignores the return value, but you should always check the **HRESULT** value from any method call.</span></span>

<span data-ttu-id="614cd-115">Rufen Sie als nächstes [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um den Filter Graph-Manager zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="614cd-115">Next, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Filter Graph Manager:</span></span>


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



<span data-ttu-id="614cd-116">Wie gezeigt, ist der Klassen Bezeichner (CLSID) CLSID \_ Filtergraph.</span><span class="sxs-lookup"><span data-stu-id="614cd-116">As shown, the class identifier (CLSID) is CLSID\_FilterGraph.</span></span> <span data-ttu-id="614cd-117">Der Filter Graph-Manager wird von einer Prozess internen dll bereitgestellt, sodass der Ausführungs Kontext **CLSCTX \_ INPROC \_ Server** ist.</span><span class="sxs-lookup"><span data-stu-id="614cd-117">The Filter Graph Manager is provided by an in-process DLL, so the execution context is **CLSCTX\_INPROC\_SERVER**.</span></span> <span data-ttu-id="614cd-118">DirectShow unterstützt das kostenlose Threading Modell, sodass Sie auch [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) mit dem **coinit- \_ multithreadflag** aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="614cd-118">DirectShow supports the free-threading model, so you can also call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="614cd-119">Der Aufruf von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) gibt die [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Schnittstelle zurück, die größtenteils Methoden zum Aufbau des Filter Diagramms enthält.</span><span class="sxs-lookup"><span data-stu-id="614cd-119">The call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) returns the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface, which mostly contains methods for building the filter graph.</span></span> <span data-ttu-id="614cd-120">Für dieses Beispiel sind zwei weitere Schnittstellen erforderlich:</span><span class="sxs-lookup"><span data-stu-id="614cd-120">Two other interfaces are needed for this example:</span></span>

-   <span data-ttu-id="614cd-121">[**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) steuert das Streaming.</span><span class="sxs-lookup"><span data-stu-id="614cd-121">[**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) controls streaming.</span></span> <span data-ttu-id="614cd-122">Sie enthält Methoden zum Beenden und Starten des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="614cd-122">It contains methods for stopping and starting the graph.</span></span>
-   <span data-ttu-id="614cd-123">[**Imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) verfügt über Methoden zum erhalten von Ereignissen aus dem Filter Graph-Manager.</span><span class="sxs-lookup"><span data-stu-id="614cd-123">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) has methods for getting events from the Filter Graph Manager.</span></span> <span data-ttu-id="614cd-124">In diesem Beispiel wird die-Schnittstelle verwendet, um auf den Abschluss der Wiedergabe zu warten.</span><span class="sxs-lookup"><span data-stu-id="614cd-124">In this example, the interface is used to wait for playback to complete.</span></span>

<span data-ttu-id="614cd-125">Beide Schnittstellen werden vom Filter Graph-Manager verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="614cd-125">Both of these interfaces are exposed by the Filter Graph Manager.</span></span> <span data-ttu-id="614cd-126">Verwenden Sie den zurückgegebenen [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Zeiger, um Sie abzufragen:</span><span class="sxs-lookup"><span data-stu-id="614cd-126">Use the returned [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) pointer to query for them:</span></span>


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="614cd-127">Nun können Sie das Filter Diagramm erstellen.</span><span class="sxs-lookup"><span data-stu-id="614cd-127">Now you can build the filter graph.</span></span> <span data-ttu-id="614cd-128">Bei der Wiedergabe von Dateien wird dies durch einen einzelnen Methoden Aufrufvorgang durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="614cd-128">For file playback, this is done by a single method call:</span></span>


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



<span data-ttu-id="614cd-129">Die [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) -Methode erstellt ein Filter Diagramm, das die angegebene Datei wiedergeben kann.</span><span class="sxs-lookup"><span data-stu-id="614cd-129">The [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method builds a filter graph that can play the specified file.</span></span> <span data-ttu-id="614cd-130">Der erste Parameter ist der Dateiname, der als breit Zeichen-Zeichenfolge (2 Byte) dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="614cd-130">The first parameter is the file name, represented as a wide character (2-byte) string.</span></span> <span data-ttu-id="614cd-131">Der zweite Parameter ist reserviert und muss gleich **null** sein.</span><span class="sxs-lookup"><span data-stu-id="614cd-131">The second parameter is reserved and must equal **NULL**.</span></span>

<span data-ttu-id="614cd-132">Diese Methode kann fehlschlagen, wenn die angegebene Datei nicht vorhanden ist oder das Dateiformat nicht erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="614cd-132">This method can fail if the specified file does not exist, or the file format is not recognized.</span></span> <span data-ttu-id="614cd-133">Angenommen, die Methode ist erfolgreich, aber das Filter Diagramm ist jetzt für die Wiedergabe bereit.</span><span class="sxs-lookup"><span data-stu-id="614cd-133">Assuming that the method succeeds, however, the filter graph is now ready for playback.</span></span> <span data-ttu-id="614cd-134">Um das Diagramm auszuführen, müssen Sie die [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) -Methode aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="614cd-134">To run the graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method:</span></span>


```C++
hr = pControl->Run();
```



<span data-ttu-id="614cd-135">Wenn das Filter Diagramm ausgeführt wird, werden die Daten durch die Filter verschoben und als Video und Audiodatei gerendert.</span><span class="sxs-lookup"><span data-stu-id="614cd-135">When the filter graph runs, data moves through the filters and is rendered as video and audio.</span></span> <span data-ttu-id="614cd-136">Die Wiedergabe erfolgt in einem separaten Thread.</span><span class="sxs-lookup"><span data-stu-id="614cd-136">Playback occurs on a separate thread.</span></span> <span data-ttu-id="614cd-137">Sie können warten, bis die Wiedergabe abgeschlossen ist, indem Sie die [**imediaevent:: waitforcompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) -Methode aufrufen:</span><span class="sxs-lookup"><span data-stu-id="614cd-137">You can wait for playback to complete by calling the [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) method:</span></span>


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



<span data-ttu-id="614cd-138">Diese Methode wird blockiert, bis die Wiedergabe der Datei abgeschlossen ist, oder bis das angegebene Timeout Intervall abläuft.</span><span class="sxs-lookup"><span data-stu-id="614cd-138">This method blocks until the file is done playing, or until the specified time-out interval elapses.</span></span> <span data-ttu-id="614cd-139">Der Wert unendlich bedeutet, dass die Anwendung unbegrenzt blockiert wird, bis die Datei wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="614cd-139">The value INFINITE means the application blocks indefinitely until the file is done playing.</span></span> <span data-ttu-id="614cd-140">Ein realistischeres Beispiel für die Ereignis Behandlung finden [Sie unter reagieren auf Ereignisse](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="614cd-140">For a more realistic example of event handling, see [Responding to Events](responding-to-events.md).</span></span>

<span data-ttu-id="614cd-141">Wenn die Anwendung abgeschlossen ist, geben Sie die Schnittstellen Zeiger frei, und schließen Sie die com-Bibliothek:</span><span class="sxs-lookup"><span data-stu-id="614cd-141">When the application is finished, release the interface pointers and close the COM library:</span></span>


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a><span data-ttu-id="614cd-142">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="614cd-142">Example Code</span></span>

<span data-ttu-id="614cd-143">Im folgenden finden Sie den gesamten Code für das Beispiel, das in diesem Artikel beschrieben wird:</span><span class="sxs-lookup"><span data-stu-id="614cd-143">Here is the complete code for the example described in this article:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="614cd-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="614cd-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="614cd-145">Grundlegende DirectShow-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="614cd-145">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 
