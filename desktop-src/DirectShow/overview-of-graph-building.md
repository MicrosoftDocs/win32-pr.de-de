---
description: Übersicht über die Diagramm Bildung
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Übersicht über die Diagramm Bildung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124364"
---
# <a name="overview-of-graph-building"></a><span data-ttu-id="027bc-103">Übersicht über die Diagramm Bildung</span><span class="sxs-lookup"><span data-stu-id="027bc-103">Overview of Graph Building</span></span>

<span data-ttu-id="027bc-104">Erstellen Sie zunächst eine Instanz des Filter Graph-Managers, um ein Filter Diagramm zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="027bc-104">To create a filter graph, begin by creating an instance of the Filter Graph Manager:</span></span>


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



<span data-ttu-id="027bc-105">Der Filter Graph-Manager unterstützt die folgenden Graph-erbauungsmethoden:</span><span class="sxs-lookup"><span data-stu-id="027bc-105">The Filter Graph Manager supports the following graph-building methods:</span></span>

-   <span data-ttu-id="027bc-106">[**Ifiltergraph:: connectdirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) versucht, eine direkte Verbindung zwischen zwei Pins herzustellen.</span><span class="sxs-lookup"><span data-stu-id="027bc-106">[**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) tries to make a direct connection between two pins.</span></span> <span data-ttu-id="027bc-107">Wenn die Pins keine Verbindung herstellen kann, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="027bc-107">If the pins cannot connect, the method fails.</span></span>
-   <span data-ttu-id="027bc-108">[**Igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) verbindet zwei Pins.</span><span class="sxs-lookup"><span data-stu-id="027bc-108">[**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connects two pins.</span></span> <span data-ttu-id="027bc-109">Wenn möglich, wird eine direkte Verbindung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="027bc-109">If possible, it makes a direct connection.</span></span> <span data-ttu-id="027bc-110">Andernfalls werden zwischen Filter verwendet, um die Verbindung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="027bc-110">Otherwise, it uses intermediate filters to complete the connection.</span></span>
-   <span data-ttu-id="027bc-111">[**Igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) beginnt mit einem Ausgabepin und erstellt den Rest des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="027bc-111">[**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) starts from an output pin and builds the rest of the graph.</span></span> <span data-ttu-id="027bc-112">Mit diesen Methoden werden nach Bedarf Filter hinzugefügt, die nach unten laufen, bis ein rendererfilter erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="027bc-112">This methods adds filters as needed, working downstream, until it reaches a renderer filter.</span></span>
-   <span data-ttu-id="027bc-113">[**Igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) erstellt ein ganzes Dateiwiedergabe Diagramm.</span><span class="sxs-lookup"><span data-stu-id="027bc-113">[**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) builds a complete file-playback graph.</span></span>
-   <span data-ttu-id="027bc-114">[**Ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) fügt dem Diagramm einen Filter hinzu.</span><span class="sxs-lookup"><span data-stu-id="027bc-114">[**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) adds a filter to the graph.</span></span> <span data-ttu-id="027bc-115">Der Filter wird nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="027bc-115">It does not connect the filter.</span></span> <span data-ttu-id="027bc-116">Sie müssen den Filter vor dem Aufrufen dieser Methode erstellen, indem Sie entweder **CoCreateInstance** aufrufen oder den Filter Mapper oder den Enumerator des System Geräts verwenden.</span><span class="sxs-lookup"><span data-stu-id="027bc-116">You must create the filter before calling this method, either by calling **CoCreateInstance** or by using the Filter Mapper or System Device Enumerator.</span></span>

<span data-ttu-id="027bc-117">Diese Methoden bieten drei grundlegende Ansätze zum Erstellen des Diagramms:</span><span class="sxs-lookup"><span data-stu-id="027bc-117">These methods provide three basic approaches to building the graph:</span></span>

1.  <span data-ttu-id="027bc-118">Der Filter Graph-Manager erstellt das gesamte Diagramm.</span><span class="sxs-lookup"><span data-stu-id="027bc-118">The Filter Graph Manager builds the entire graph.</span></span>
2.  <span data-ttu-id="027bc-119">Der Filter Graph-Manager erstellt einen Teil des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="027bc-119">The Filter Graph Manager builds part of the graph.</span></span>
3.  <span data-ttu-id="027bc-120">Die Anwendung erstellt das gesamte Diagramm.</span><span class="sxs-lookup"><span data-stu-id="027bc-120">The application builds the entire graph.</span></span>

<span data-ttu-id="027bc-121">**Der Filter Graph-Manager erstellt das gesamte Diagramm.**</span><span class="sxs-lookup"><span data-stu-id="027bc-121">**The Filter Graph Manager Builds the Entire Graph**</span></span>

<span data-ttu-id="027bc-122">Wenn Sie nur eine Datei wiedergeben möchten, die in einem erkannten Format (z. b. AVI, MPEG, WAV oder MP3) erstellt wurde, verwenden Sie die **RenderFile** -Methode.</span><span class="sxs-lookup"><span data-stu-id="027bc-122">If you simply want to play a file that is authored in a recognized format, such as AVI, MPEG, WAV, or MP3, use the **RenderFile** method.</span></span> <span data-ttu-id="027bc-123">Der Artikel [zum Wiedergeben einer Datei](how-to-play-a-file.md) zeigt, wie Sie dies tun.</span><span class="sxs-lookup"><span data-stu-id="027bc-123">The article [How To Play a File](how-to-play-a-file.md) shows how to do this.</span></span>

<span data-ttu-id="027bc-124">Die **RenderFile** -Methode beginnt mit der Suche nach einem Quell Filter, mit dem die Datei analysiert werden kann, in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="027bc-124">The **RenderFile** method starts by looking in the registry for a source filter that can parse the file.</span></span> <span data-ttu-id="027bc-125">Er verwendet das Protokoll (z. b. " `https://` " in der URL), die Dateierweiterung oder vordefinierte Byte Muster in der Datei, um den Quell Filter zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="027bc-125">It uses the protocol (such as " `https://` " in the URL), the file extension, or pre-defined byte patterns in the file to determine the source filter.</span></span> <span data-ttu-id="027bc-126">Weitere Informationen finden Sie unter [Registrieren eines benutzerdefinierten Dateityps](registering-a-custom-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="027bc-126">For details, see [Registering a Custom File Type](registering-a-custom-file-type.md).</span></span>

<span data-ttu-id="027bc-127">Um den Rest des Diagramms zu erstellen, verwendet der Filter Graph-Manager einen iterativen Prozess, bei dem die von einem Filter unterstützten Medientypen auf den Ausgabe Pins verwendet werden, und durchsucht die Registrierung nach Filtern, die den Medientyp als Eingabe akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="027bc-127">To build the rest of the graph, the Filter Graph Manager uses an iterative process wherein it takes the media types that a filter supports on its output pins, and searches the registry for filters that will accept that media type as input.</span></span> <span data-ttu-id="027bc-128">Es werden verschiedene Kriterien verwendet, um die Such-und Priorisieren von Filtern einzuschränken:</span><span class="sxs-lookup"><span data-stu-id="027bc-128">It uses several criteria to narrow the search and prioritize filters:</span></span>

-   <span data-ttu-id="027bc-129">Die *Kategorie Filter* identifiziert die allgemeine Funktionalität des Filters.</span><span class="sxs-lookup"><span data-stu-id="027bc-129">The *filter category* identifies the general functionality of the filter.</span></span>
-   <span data-ttu-id="027bc-130">Der Medientyp beschreibt, welche Art von Daten der Filter als Eingabe oder als Ausgabe annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="027bc-130">The media type describes what kind of data the filter can accept as input or deliver as output.</span></span>
-   <span data-ttu-id="027bc-131">Das *Verdienst* legt die Reihenfolge fest, in der Filter ausprobiert werden.</span><span class="sxs-lookup"><span data-stu-id="027bc-131">The *merit* determines the order in which filters are tried.</span></span> <span data-ttu-id="027bc-132">Wenn zwei Filter in der gleichen Filterkategorie beide dieselben Eingabetypen unterstützen, wählt der Filter Graph-Manager den Wert mit dem höchsten Wert aus.</span><span class="sxs-lookup"><span data-stu-id="027bc-132">If two filters in the same filter category both support the same input types, the Filter Graph Manager selects the one with the highest merit value.</span></span> <span data-ttu-id="027bc-133">Einige Filter verfügen über einen niedrigen Wert, da Sie für spezielle Zwecke konzipiert sind und nur dem Graph von der Anwendung hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="027bc-133">Some filters are purposely given a low merit value because they are designed for specialized purposes and should only be added to the graph by the application.</span></span>

<span data-ttu-id="027bc-134">Der Filter Graph-Manager verwendet das [Filter Mapper](filter-mapper.md) -Objekt, um die Registrierung zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="027bc-134">The Filter Graph Manager uses the [Filter Mapper](filter-mapper.md) object to search the registry.</span></span>

<span data-ttu-id="027bc-135">Wenn jeder Filter hinzugefügt wird, versucht der Filter Graph-Manager, ihn mit der Ausgabe-PIN des vorherigen Filters zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="027bc-135">As each filter is added, the Filter Graph Manager tries to connect it to the previous filter's output pin.</span></span> <span data-ttu-id="027bc-136">Die Filter werden ausgehandelt, um zu bestimmen, ob Sie eine Verbindung herstellen können. wenn dies der Fall ist, welcher Medientyp für die Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="027bc-136">The filters negotiate to determine whether they can connect, and if so, what media type to use for the connection.</span></span> <span data-ttu-id="027bc-137">Wenn der neue Filter keine Verbindung herstellen kann, verwirft der Filter Graph-Manager ihn und versucht einen anderen Filter.</span><span class="sxs-lookup"><span data-stu-id="027bc-137">If the new filter cannot connect, the Filter Graph Manager discards it and tries another filter.</span></span> <span data-ttu-id="027bc-138">Dieser Prozess wird fortgesetzt, bis jeder Stream gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="027bc-138">This process continues until every stream is rendered.</span></span>

<span data-ttu-id="027bc-139">**Der Filter Graph-Manager erstellt einen Teil des Diagramms.**</span><span class="sxs-lookup"><span data-stu-id="027bc-139">**The Filter Graph Manager Builds Part of the Graph**</span></span>

<span data-ttu-id="027bc-140">Um etwas über das einfache Abspielen einer Datei hinaus zu tun, muss Ihre Anwendung mindestens einen Teil der Diagramm erbauarbeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="027bc-140">To do something beyond simply playing a file, your application must perform at least some of the graph building work.</span></span> <span data-ttu-id="027bc-141">Beispielsweise muss eine Video Erfassungs Anwendung einen Erfassungs Quell Filter auswählen und dem Diagramm hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="027bc-141">For example, a video capture application must select a capture source filter and add it to the graph.</span></span> <span data-ttu-id="027bc-142">Wenn Sie Daten in eine AVI-Datei schreiben, müssen Sie dem Diagramm die Filter "AVI MUX" und "File Writer" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="027bc-142">If you are writing data to an AVI file, you must add the AVI Mux and File Writer filters to the graph.</span></span> <span data-ttu-id="027bc-143">Es ist jedoch oft möglich, dass der Filter Graph-Manager das Diagramm vervollständigt.</span><span class="sxs-lookup"><span data-stu-id="027bc-143">However, it is often possible to let the Filter Graph Manager complete the graph.</span></span> <span data-ttu-id="027bc-144">Beispielsweise können Sie eine PIN für die Vorschau durch Aufrufen der **Rendering** -Methode Rendering.</span><span class="sxs-lookup"><span data-stu-id="027bc-144">For example, you can render a pin for preview by calling the **Render** method.</span></span>

<span data-ttu-id="027bc-145">**Die Anwendung erstellt das gesamte Diagramm.**</span><span class="sxs-lookup"><span data-stu-id="027bc-145">**The Application Builds the Entire Graph**</span></span>

<span data-ttu-id="027bc-146">In einigen Szenarien muss Ihre Anwendung möglicherweise das Diagramm erstellen, indem Sie die einzelnen Filter hinzufügen und verbinden.</span><span class="sxs-lookup"><span data-stu-id="027bc-146">In some scenarios, your application may need to build the graph by adding and connecting each filter.</span></span> <span data-ttu-id="027bc-147">In diesem Fall wissen Sie wahrscheinlich genau, welche Filter dem Diagramm hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="027bc-147">In this case, you probably know specifically which filters should be added to the graph.</span></span> <span data-ttu-id="027bc-148">Bei dieser Vorgehensweise fügt die Anwendung jeden Filter hinzu, indem Sie **addFilter** aufrufen, die Pins für die Filter auflistet und Sie durch Aufrufen von **Connect** oder **connectdirect** verbindet.</span><span class="sxs-lookup"><span data-stu-id="027bc-148">With this approach, the application adds each filter by calling **AddFilter**, enumerates the pins on the filters, and connects them by calling either **Connect** or **ConnectDirect**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="027bc-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="027bc-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="027bc-150">Erstellen von Diagrammen mit dem Erfassungs Diagramm-Generator</span><span class="sxs-lookup"><span data-stu-id="027bc-150">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[<span data-ttu-id="027bc-151">Auflisten von Geräten und Filtern</span><span class="sxs-lookup"><span data-stu-id="027bc-151">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="027bc-152">Auflisten von Objekten in einem Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="027bc-152">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="027bc-153">Allgemeine Graph-Building Techniken</span><span class="sxs-lookup"><span data-stu-id="027bc-153">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="027bc-154">Aufbauen des Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="027bc-154">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> </dl>

 

 



