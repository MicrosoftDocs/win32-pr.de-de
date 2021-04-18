---
description: Automatisches Erstellen eines Inhaltsverzeichnisses
ms.assetid: 3acb9c12-0158-4b89-87c4-4abd35ae8c2f
title: Automatisches Erstellen eines Inhaltsverzeichnisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22adc4d48ad7f4b1d89a446eb28c25d6011804a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341160"
---
# <a name="generating-a-table-of-contents-automatically"></a><span data-ttu-id="211af-103">Automatisches Erstellen eines Inhaltsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="211af-103">Generating a Table of Contents Automatically</span></span>

<span data-ttu-id="211af-104">In diesem Thema wird veranschaulicht, wie die Komponente "Inhalts [**Generator**](/previous-versions/ee264297(v=vs.85)) " (TOC Generator) zum automatischen Generieren eines Inhaltsverzeichnisses für eine Videodatei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="211af-104">This topic demonstrates how to use [**Table of Contents Generator**](/previous-versions/ee264297(v=vs.85)) (TOC Generator) component to automatically generate a table of contents for a video file.</span></span>

<span data-ttu-id="211af-105">Der TOC-Generator ist ein DirectX-Medienobjekt (DMO).</span><span class="sxs-lookup"><span data-stu-id="211af-105">TOC Generator is a DirectX Media Object (DMO).</span></span> <span data-ttu-id="211af-106">Um den TOC-Generator DMO zu verwenden, erstellen Sie ein DirectX-Filter Diagramm, das eine Videodatei als Quelle hat.</span><span class="sxs-lookup"><span data-stu-id="211af-106">To use the TOC Generator DMO, build a DirectX filter graph that has a video file as its source.</span></span> <span data-ttu-id="211af-107">Fügen Sie den TOC-Generator DMO in das Filter Diagramm ein, und führen Sie das Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="211af-107">Insert the TOC Generator DMO into the filter graph, and run the graph.</span></span> <span data-ttu-id="211af-108">Anschließend können Sie das automatisch generierte Inhaltsverzeichnis aus dem TOC-Generator DMO abrufen.</span><span class="sxs-lookup"><span data-stu-id="211af-108">You can then obtain the automatically generated table of contents from the TOC Generator DMO.</span></span>

<span data-ttu-id="211af-109">Die Schritte werden im folgenden Verfahren ausführlicher erläutert.</span><span class="sxs-lookup"><span data-stu-id="211af-109">The following procedure gives the steps in more detail.</span></span>

1.  <span data-ttu-id="211af-110">Rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um ein Filter Diagramm Objekt (**CLSID \_ Filtergraph**) zu erstellen und eine [**igraphbuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="211af-110">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a Filter Graph object (**CLSID\_FilterGraph**) and obtain an [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
2.  <span data-ttu-id="211af-111">Rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um ein DMO-Wrapper Filter Objekt (**CLSID \_ dmowrapperfilter**) zu erstellen, und rufen Sie eine [**idmowrapperfilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="211af-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a DMO Wrapper Filter object (**CLSID\_DMOWrapperFilter**) and obtain an [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="211af-112">Übergeben Sie **CLSID \_ cdecgeneratordmo** an die [**Init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) -Methode des DMO-Wrapper Filters.</span><span class="sxs-lookup"><span data-stu-id="211af-112">Pass **CLSID\_CTocGeneratorDmo** to the [**Init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) method of your DMO wrapper filter.</span></span> <span data-ttu-id="211af-113">Dadurch wird ein TOC-Generator-DMO erstellt und in den DMO-Wrapper Filter umschlossen.</span><span class="sxs-lookup"><span data-stu-id="211af-113">This creates a TOC Generator DMO and wraps it in your DMO wrapper filter.</span></span>
4.  <span data-ttu-id="211af-114">Wenden Sie die [**addFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) -Methode der [**igraphbuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) -Schnittstelle an, um den umschließenden TOC-Generator DMO dem Filter Diagramm hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="211af-114">Call the [**AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to add the wrapped TOC Generator DMO to the filter graph.</span></span>
    > [!Note]  
    > <span data-ttu-id="211af-115">[**Igraphbuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) erbt von [**ifiltergraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).</span><span class="sxs-lookup"><span data-stu-id="211af-115">[**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) inherits from [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).</span></span>

     

5.  <span data-ttu-id="211af-116">Rufen Sie die [**addsourcefilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) -Methode der [**igraphbuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) -Schnittstelle auf, um einen Quelle-Filter zu erstellen und ihn dem Diagramm hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="211af-116">Call the [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to create a souce filter and add it to the graph.</span></span>
6.  <span data-ttu-id="211af-117">Auflisten von Pins für den DMO-Wrapper Filter und den Quell Filter.</span><span class="sxs-lookup"><span data-stu-id="211af-117">Enumerate pins on the DMO wrapper filter and the source filter.</span></span> <span data-ttu-id="211af-118">Dies umfasst das Abrufen von [**iumumpins**](/windows/win32/api/strmif/nn-strmif-ienumpins) -Schnittstellen und [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="211af-118">This involves obtaining [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) interfaces and [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) interfaces.</span></span>
7.  <span data-ttu-id="211af-119">Verbinden Sie den Quell Filter und den Wrapper Filter, indem Sie die [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) -Methode Ihrer [**igraphbuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) -Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="211af-119">Connect the source filter and the wrapper filter by calling the [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
8.  <span data-ttu-id="211af-120">Vervollständigen Sie das Diagramm, indem Sie die Methode " [**Rendering**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) " Ihrer [**igraphbuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) -Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="211af-120">Complete the graph by calling the [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
9.  <span data-ttu-id="211af-121">Führen Sie das Diagramm ([**IMediaControl:: Run**](/windows/win32/api/control/nf-control-imediacontrol-run)) aus, und warten Sie, bis es abgeschlossen ist ([**imediaevent:: waitforcompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).</span><span class="sxs-lookup"><span data-stu-id="211af-121">Run the graph ([**IMediaControl::Run**](/windows/win32/api/control/nf-control-imediacontrol-run)), and wait for it to complete ([**IMediaEvent::WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).</span></span>
10. <span data-ttu-id="211af-122">Rufen Sie eine [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle für den DMO-Filter-Wrapper ab, und rufen Sie den Wert der [**mfpkey \_ tocgenerator \_ tokready**](/previous-versions/ee264297(v=vs.85)) -Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="211af-122">Obtain an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface on your DMO filter wrapper, and get the value of the [**MFPKEY\_TOCGENERATOR\_TOCREADY**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="211af-123">Wiederholen Sie dies bei Bedarf, bis das Inhaltsverzeichnis bereit ist.</span><span class="sxs-lookup"><span data-stu-id="211af-123">Repeat if necessary until the table of contents is ready.</span></span>
11. <span data-ttu-id="211af-124">Verwenden Sie die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle zum Aufrufen des Werts der Eigenschaft " [**mfpkey \_ tocgenerator \_ tocobject**](/previous-versions/ee264297(v=vs.85)) ".</span><span class="sxs-lookup"><span data-stu-id="211af-124">Use your [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to get the value of the [**MFPKEY\_TOCGENERATOR\_TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="211af-125">Diese Eigenschaft ist eine [**IYC**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) -Schnittstelle, die das automatisch generierte Inhaltsverzeichnis darstellt.</span><span class="sxs-lookup"><span data-stu-id="211af-125">This property is an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface that represents the automatically generated table of contents.</span></span>

<span data-ttu-id="211af-126">Der folgende Code veranschaulicht das Verfahren zum automatischen Erstellen eines Inhaltsverzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="211af-126">The following code demonstrates the procedure for generating a table of contents automatically.</span></span> <span data-ttu-id="211af-127">Der Code verwendet drei Hilfsfunktionen ([**buildgraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**rungraphandwait**](rungraphandwait-method-for-generating-a-table-of-contents.md)und [**gettoc**](gettoc-method-for-generating-a-table-of-contents.md)), die auf anderen Seiten dieser Dokumentation angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="211af-127">The code uses three helper functions ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md), and [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) that are shown on other pages of this documentation.</span></span>


```C++
#include <dshow.h>
#include <dmodshow.h>
#include <wmcodecdsp.h>
#include <dmoreg.h>
#include <propsys.h>
#include <propidl.h>
#include <initguid.h>

HRESULT GetToc(IDMOWrapperFilter* pWrap, IToc** ppToc);
HRESULT RunGraphAndWait(IGraphBuilder* pGraph);
HRESULT BuildGraph(IGraphBuilder* pGraph, IDMOWrapperFilter* pWrap);

WCHAR g_sourceFile[] = L"c:\\experiment\\Seattle.wmv";

void main()
{
   HRESULT hr = E_FAIL;
   hr = CoInitialize(NULL);

   if(SUCCEEDED(hr))
   {
      IGraphBuilder* pBuilder = NULL;
      hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
         IID_IGraphBuilder, (VOID**)&pBuilder);

      if(SUCCEEDED(hr))
      {
         IDMOWrapperFilter* pWrap = NULL;
         hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, CLSCTX_INPROC, 
            IID_IDMOWrapperFilter, (VOID**)&pWrap);

         if(SUCCEEDED(hr))
         {
            hr = pWrap->Init(CLSID_CTocGeneratorDmo, DMOCATEGORY_VIDEO_EFFECT); 

            if(SUCCEEDED(hr))
            {
               hr = BuildGraph(pBuilder, pWrap);

               if(SUCCEEDED(hr))
               {
                  hr = RunGraphAndWait(pBuilder);

                  if(SUCCEEDED(hr))
                  {
                     IToc* pToc = NULL;
                     hr = GetToc(pWrap, &pToc);

                     if(SUCCEEDED(hr))
                     {
                        // Inspect the table of contents by calling IToc methods.

                        pToc->Release();
                        pToc = NULL;
                     }
                  }
               }
            }

            pWrap->Release();
            pWrap = NULL;
         }

         pBuilder->Release();
         pBuilder = NULL;
      }

      CoUninitialize();
   }
}
```



## <a name="related-topics"></a><span data-ttu-id="211af-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="211af-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="211af-129">Buildgraph-Funktion zum Erstellen eines Inhaltsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="211af-129">BuildGraph Function for Generating a Table of Contents</span></span>](buildgraph-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="211af-130">Getdec-Funktion zum Erstellen eines Inhaltsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="211af-130">GetToc Function for Generating a Table of Contents</span></span>](gettoc-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="211af-131">Rungraphandwait-Funktion zum Erstellen eines Inhaltsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="211af-131">RunGraphAndWait Function for Generating a Table of Contents</span></span>](rungraphandwait-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="211af-132">Programmier Handbuch für das Inhaltsverzeichnis des Parsers</span><span class="sxs-lookup"><span data-stu-id="211af-132">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 
