---
description: Auswählen eines Decoders in DirectShow-Bearbeitungs Diensten
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: Auswählen eines Decoders in DirectShow-Bearbeitungs Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956ad0284722eb394590b1b0065f167c55b3cf51
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481510"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a><span data-ttu-id="0417c-103">Auswählen eines Decoders in DirectShow-Bearbeitungs Diensten</span><span class="sxs-lookup"><span data-stu-id="0417c-103">Selecting a Decoder in DirectShow Editing Services</span></span>

<span data-ttu-id="0417c-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="0417c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="0417c-105">Wenn [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) ein Video Bearbeitungs Projekt rendert, wählt die Rendering-Engine automatisch die erforderlichen Decoder aus.</span><span class="sxs-lookup"><span data-stu-id="0417c-105">When [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project, the Rendering Engine automatically selects the necessary decoders.</span></span> <span data-ttu-id="0417c-106">Dies kann innerhalb der Methode " [**unenderengine:: connectfrontend**](irenderengine-connectfrontend.md) " oder dynamisch während des Renderings vorkommen.</span><span class="sxs-lookup"><span data-stu-id="0417c-106">This may happen inside the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method, or else dynamically during rendering.</span></span>

<span data-ttu-id="0417c-107">Ein Benutzer kann mehrere decoderer installieren, die eine bestimmte Datei decodieren können.</span><span class="sxs-lookup"><span data-stu-id="0417c-107">A user might install several decoders that are capable of decoding a particular file.</span></span> <span data-ttu-id="0417c-108">Wenn mehrere Decoder verfügbar sind, verwendet des den [intelligenten Verbindungs](intelligent-connect.md) Algorithmus, um den Decoder auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="0417c-108">When multiple decoders are available, DES uses the [Intelligent Connect](intelligent-connect.md) algorithm to select the decoder.</span></span>

<span data-ttu-id="0417c-109">Es gibt keine Möglichkeit für die Anwendung, den zu verwendenden Decoder direkt anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0417c-109">There is no way for the application to specify directly which decoder to use.</span></span> <span data-ttu-id="0417c-110">Sie können den Decoder jedoch indirekt über die [**iamgraphbuildercallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) -Rückruf Schnittstelle auswählen.</span><span class="sxs-lookup"><span data-stu-id="0417c-110">However, you can choose the decoder indirectly through the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) callback interface.</span></span> <span data-ttu-id="0417c-111">Durch Implementieren dieser Schnittstelle in der Anwendung können Sie während des Graph-Erstellens Benachrichtigungen empfangen und bestimmte Filter aus dem Diagramm ablehnen.</span><span class="sxs-lookup"><span data-stu-id="0417c-111">By implementing this interface in your application, you can receive notifications during the graph-building process and reject certain filters from the graph.</span></span>

<span data-ttu-id="0417c-112">Beginnen Sie mit der Implementierung einer Klasse, die die [**iamgraphbuildercallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) -Schnittstelle verfügbar macht:</span><span class="sxs-lookup"><span data-stu-id="0417c-112">Start by implementing a class that exposes the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) interface:</span></span>


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



<span data-ttu-id="0417c-113">Erstellen Sie dann eine Instanz des Filter Graph-Managers, und registrieren Sie Ihre Klasse für den Empfang von Rückruf Benachrichtigungen:</span><span class="sxs-lookup"><span data-stu-id="0417c-113">Then create an instance of the Filter Graph Manager and register your class to receive callback notifications:</span></span>


```C++
// Declare an instance of the callback object.
GraphBuilderCB GraphCB; 

// Create the Filter Graph Manager.
CComPtr<IGraphBuilder> pGraph;
hr = pGraph.CoCreateInstance(CLSID_FilterGraph);
if (FAILED(hr))
{
    // Handle error (not shown).
}
// Register to receive the callbacks.
CComQIPtr<IObjectWithSite> pSite(pGraph);
if (pSite)
{
    hr = pSite->SetSite((IUnknown*)&GraphCB);
}
```



<span data-ttu-id="0417c-114">Erstellen Sie als nächstes die Renderengine, und rufen Sie die Methode " [**irienderengine:: setfiltergraph**](irenderengine-setfiltergraph.md) " mit einem Zeiger auf den Filter Graph-Manager auf.</span><span class="sxs-lookup"><span data-stu-id="0417c-114">Next, create the Render Engine and call the [**IRenderEngine::SetFilterGraph**](irenderengine-setfiltergraph.md) method with a pointer to the Filter Graph Manager.</span></span> <span data-ttu-id="0417c-115">Dadurch wird sichergestellt, dass die Renderingengine keinen eigenen Filter Diagramm-Manager erstellt, sondern stattdessen die Instanz verwendet, die Sie für Rückrufe konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="0417c-115">This ensures that the Render Engine does not create its own Filter Graph Manager, but instead uses the instance that you have configured for callbacks.</span></span>


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



<span data-ttu-id="0417c-116">Wenn das Projekt gerendert wird, wird die [**iamgraphbuildercallback:: selectedfilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) -Methode der Anwendung sofort aufgerufen, bevor der Filter Graph-Manager einen neuen Filter erstellt.</span><span class="sxs-lookup"><span data-stu-id="0417c-116">When the project is rendered, the application's [**IAMGraphBuilderCallback::SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) method is called immediately before the Filter Graph Manager creates a new filter.</span></span> <span data-ttu-id="0417c-117">Die **selectedfilter** -Methode empfängt einen Zeiger auf eine **IMoniker** -Schnittstelle, die einen Moniker für den Filter darstellt.</span><span class="sxs-lookup"><span data-stu-id="0417c-117">The **SelectedFilter** method receives a pointer to an **IMoniker** interface that represents a moniker for the filter.</span></span> <span data-ttu-id="0417c-118">Überprüfen Sie den Moniker, und geben Sie, wenn Sie sich entschließen, den Filter abzulehnen, einen Fehlercode von der **selectedfilter** -Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="0417c-118">Examine the moniker, and if you decide to reject the filter, return a failure code from the **SelectedFilter** method.</span></span>

<span data-ttu-id="0417c-119">Der schwierige Teil besteht darin, zu ermitteln, welche Moniker Decoder darstellen – und insbesondere, welche Moniker Decoder darstellen, die Sie ablehnen möchten.</span><span class="sxs-lookup"><span data-stu-id="0417c-119">The difficult part is to identify which monikers represent decoders — and in particular, which monikers represent decoders that you want to reject.</span></span> <span data-ttu-id="0417c-120">Eine Lösung ist Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0417c-120">One solution is the following:</span></span>

-   <span data-ttu-id="0417c-121">Bevor Sie das Projekt rendern, verwenden Sie die [**IFilterMapper2:: enummatchingfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) -Methode, um eine Liste von Filtern zu erstellen, die als akzeptieren des gewünschten Eingabetyps registriert sind.</span><span class="sxs-lookup"><span data-stu-id="0417c-121">Before rendering the project, use the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method to create a list of filters that are registered as accepting the desired input type.</span></span> <span data-ttu-id="0417c-122">Bei Video-oder Audiokomprimierungs Typen sollte diese Liste einem Satz von Decodern zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0417c-122">For video or audio compression types, this list should map to a set of decoders.</span></span>
-   <span data-ttu-id="0417c-123">Die **enummatchingfilters** -Methode gibt eine Sammlung von Monikern zurück.</span><span class="sxs-lookup"><span data-stu-id="0417c-123">The **EnumMatchingFilters** method returns a collection of monikers.</span></span> <span data-ttu-id="0417c-124">Für jeden Moniker in der Auflistung wird die **DisplayName** -Eigenschaft wie unter [Verwenden des Filter Mappers](using-the-filter-mapper.md)beschrieben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0417c-124">For each moniker in the collection, get the **DisplayName** property, as described in [Using the Filter Mapper](using-the-filter-mapper.md).</span></span>
-   <span data-ttu-id="0417c-125">Speichern Sie eine Liste der anzeigen Amen, aber lassen Sie den anzeigen Amen aus, der mit dem Filter übereinstimmt, den Sie für die Decodierung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="0417c-125">Store a list of the display names, but omit the display name that matches the filter you want to use for decoding.</span></span> <span data-ttu-id="0417c-126">Anzeigen Amen für Softwarefilter haben folgende Form:</span><span class="sxs-lookup"><span data-stu-id="0417c-126">Display names for software filters have the following form:</span></span>

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    <span data-ttu-id="0417c-127">where</span><span class="sxs-lookup"><span data-stu-id="0417c-127">where</span></span>

    ```C++
    CategoryGUID
    ```

    

    <span data-ttu-id="0417c-128">ist die GUID der Filterkategorie, und</span><span class="sxs-lookup"><span data-stu-id="0417c-128">is the GUID of the filter category, and</span></span>

    ```C++
    FilterCLSID
    ```

    

    <span data-ttu-id="0417c-129">die CLSID des Filters.</span><span class="sxs-lookup"><span data-stu-id="0417c-129">is the filter's CLSID.</span></span> <span data-ttu-id="0417c-130">Für DMOS ist das Format identisch, aber ändern `sw` Sie in `dmo` .</span><span class="sxs-lookup"><span data-stu-id="0417c-130">For DMOs, the format is the same, but change `sw` to `dmo`.</span></span>

    <span data-ttu-id="0417c-131">Die Liste enthält nun anzeigen Amen für jeden Filter, der den gewünschten Medientyp ausgibt, aber nicht Ihren bevorzugten Filter.</span><span class="sxs-lookup"><span data-stu-id="0417c-131">The list now contains display names for every filter that outputs the desired media type but is not your preferred filter.</span></span>

-   <span data-ttu-id="0417c-132">In der **selectedfilter** -Methode können Sie die **Display Name** -Eigenschaft für den vorgeschlagenen Moniker aufrufen und diese anhand der gespeicherten Liste überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0417c-132">In the **SelectedFilter** method, get the **DisplayName** property on the proposed moniker and check it against the stored list.</span></span> <span data-ttu-id="0417c-133">Wenn der Anzeige Name mit einem Eintrag in der Liste übereinstimmt, lehnen Sie diesen Filter ab.</span><span class="sxs-lookup"><span data-stu-id="0417c-133">If the display name matches an entry in the list, reject that filter.</span></span> <span data-ttu-id="0417c-134">Andernfalls akzeptieren Sie es, indem Sie S OK zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="0417c-134">Otherwise, accept it by returning S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0417c-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0417c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0417c-136">Rendern eines Projekts</span><span class="sxs-lookup"><span data-stu-id="0417c-136">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



