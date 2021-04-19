---
description: Schreiben einer Windows-Mediendatei in des
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: Schreiben einer Windows-Mediendatei in des
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106357155"
---
# <a name="writing-a-windows-media-file-in-des"></a><span data-ttu-id="049d3-103">Schreiben einer Windows-Mediendatei in des</span><span class="sxs-lookup"><span data-stu-id="049d3-103">Writing a Windows Media File in DES</span></span>

<span data-ttu-id="049d3-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="049d3-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="049d3-105">In diesem Abschnitt wird beschrieben, wie Sie eine Windows Media-Datei mithilfe von [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) (de) schreiben.</span><span class="sxs-lookup"><span data-stu-id="049d3-105">This section describes how to write a Windows Media file using [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="049d3-106">Verwenden Sie die Smart-Rendering-Engine nicht zum Schreiben von Windows Media-Dateien.</span><span class="sxs-lookup"><span data-stu-id="049d3-106">Do not use the Smart Render Engine to write Windows Media files.</span></span> <span data-ttu-id="049d3-107">Verwenden Sie immer die einfache Renderengine (CLSID- \_ Renderengine).</span><span class="sxs-lookup"><span data-stu-id="049d3-107">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

 

<span data-ttu-id="049d3-108">Gehen Sie folgendermaßen vor, um eine Windows Media-Datei zu schreiben:</span><span class="sxs-lookup"><span data-stu-id="049d3-108">To write a Windows Media file, do the following:</span></span>

1.  <span data-ttu-id="049d3-109">Aufrufen von **SetSite** für die Rendering-Engine mit einem Zeiger auf den Schlüssel Anbieter.</span><span class="sxs-lookup"><span data-stu-id="049d3-109">Call **SetSite** on the render engine, with a pointer to your key provider.</span></span>
2.  <span data-ttu-id="049d3-110">Erstellen Sie das Front-End des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="049d3-110">Build the front end of the graph.</span></span> <span data-ttu-id="049d3-111">(Siehe [Rendern eines Projekts](rendering-a-project.md).)</span><span class="sxs-lookup"><span data-stu-id="049d3-111">(See [Rendering a Project](rendering-a-project.md).)</span></span>
3.  <span data-ttu-id="049d3-112">Erstellen Sie den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter, und fügen Sie ihn dem Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="049d3-112">Create the [WM ASF Writer](wm-asf-writer-filter.md) filter and add it to the graph.</span></span>
4.  <span data-ttu-id="049d3-113">Verwenden Sie die [**ifilesink Filter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) -Schnittstelle für den WM-ASF-Writer-Filter, um den Dateinamen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="049d3-113">Use the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface on the WM ASF Writer filter to set the file name.</span></span>
5.  <span data-ttu-id="049d3-114">Konfigurieren Sie den WM-ASF-Writer für die Verwendung eines Windows Media-Profils.</span><span class="sxs-lookup"><span data-stu-id="049d3-114">Configure the WM ASF Writer to use a Windows Media profile.</span></span> <span data-ttu-id="049d3-115">Jedes Profil verfügt über eine vordefinierte Anzahl von Streams.</span><span class="sxs-lookup"><span data-stu-id="049d3-115">Each profile has a predefined number of streams.</span></span> <span data-ttu-id="049d3-116">Sie müssen ein Profil auswählen, das den Gruppen im Projekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="049d3-116">You must choose a profile that matches the groups in your project.</span></span>

    <span data-ttu-id="049d3-117">Die [**iconfigasfwriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) -Schnittstelle enthält verschiedene Methoden zum Festlegen des Profils.</span><span class="sxs-lookup"><span data-stu-id="049d3-117">The [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface contains a few different methods for setting the profile.</span></span> <span data-ttu-id="049d3-118">Beispielsweise gibt die Methode " **konfigurifisingprofileguid** " ein Systemprofil als GUID an.</span><span class="sxs-lookup"><span data-stu-id="049d3-118">For example, the **ConfigureFilterUsingProfileGuid** method specifies a system profile as a GUID.</span></span> <span data-ttu-id="049d3-119">Oder Sie können Windows Media-Methoden verwenden, um einen **iwmprofile** -Zeiger zu erhalten, und dann [**iconfigasfwriter:: konfigurifisingprofile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="049d3-119">Or, you can use Windows Media Format methods to get an **IWMProfile** pointer and then call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile).</span></span> <span data-ttu-id="049d3-120">Weitere Informationen finden Sie unter [Konfigurieren des ASF-Writers](configuring-the-asf-writer.md).</span><span class="sxs-lookup"><span data-stu-id="049d3-120">For more information, see [Configuring the ASF Writer](configuring-the-asf-writer.md).</span></span>

6.  <span data-ttu-id="049d3-121">Verbinden Sie das Front-End mit dem ASF-Writer.</span><span class="sxs-lookup"><span data-stu-id="049d3-121">Connect the front end to the ASF Writer.</span></span> <span data-ttu-id="049d3-122">Das Front-End des Diagramms enthält eine Ausgabe-PIN für jede Gruppe.</span><span class="sxs-lookup"><span data-stu-id="049d3-122">The front end of the graph contains one output pin for each group.</span></span> <span data-ttu-id="049d3-123">Angenommen, Sie haben ein kompatibles Profil angegeben, muss der ASF-Writer über einen passenden Satz von Eingabe Pins verfügen.</span><span class="sxs-lookup"><span data-stu-id="049d3-123">Assuming that you specified a compatible profile, the ASF Writer should have a matching set of input pins.</span></span> <span data-ttu-id="049d3-124">Verbinden Sie jede Ausgabe-PIN mit der entsprechenden Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="049d3-124">Connect each output pin to the corresponding input pin.</span></span> <span data-ttu-id="049d3-125">Die einfachste Möglichkeit hierfür ist die Verwendung der [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode.</span><span class="sxs-lookup"><span data-stu-id="049d3-125">The easiest way to do this is using the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="049d3-126">Erstellen Sie zunächst eine neue Instanz des [Erfassungs Diagramm](capture-graph-builder.md) -Generators, und initialisieren Sie Sie mit einem Zeiger auf den Filter Graph-Manager:</span><span class="sxs-lookup"><span data-stu-id="049d3-126">First, create a new instance of the [Capture Graph Builder](capture-graph-builder.md) and initialize it with a pointer to the Filter Graph Manager:</span></span>

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    <span data-ttu-id="049d3-127">Rufen Sie als nächstes die Ausgabe-PIN für jede Gruppe ab, indem Sie die Methode " [**irienderengine:: getgroupoutputpin**](irenderengine-getgroupoutputpin.md) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="049d3-127">Next, retrieve the output pin for each group by calling the [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) method.</span></span> <span data-ttu-id="049d3-128">**RenderStream** zum Verbinden der PIN mit dem ASF-Writer aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="049d3-128">Call **RenderStream** to connect the pin to the ASF Writer:</span></span>

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a><span data-ttu-id="049d3-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="049d3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="049d3-130">Verwenden von Windows Media mit DirectShow-Bearbeitungs Diensten</span><span class="sxs-lookup"><span data-stu-id="049d3-130">Using Windows Media With DirectShow Editing Services</span></span>](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



