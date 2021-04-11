---
description: Erfassen in mehreren Dateien
ms.assetid: 6073a891-e9f5-442d-a2d9-3a7b97f7f735
title: Erfassen in mehreren Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b40091acff8edffbe84550b03d1ccd4073ddb6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124088"
---
# <a name="capturing-to-multiple-files"></a><span data-ttu-id="b08d8-103">Erfassen in mehreren Dateien</span><span class="sxs-lookup"><span data-stu-id="b08d8-103">Capturing to Multiple Files</span></span>

<span data-ttu-id="b08d8-104">Nachdem Sie einige Videos in einer Datei aufgezeichnet haben, können Sie zu einer neuen Datei wechseln, indem Sie das Diagramm beenden und den Dateinamen für den [dateiwriter](file-writer-filter.md) -Filter festlegen.</span><span class="sxs-lookup"><span data-stu-id="b08d8-104">After you have captured some video to a file, you can switch to a new file by stopping the graph and setting the file name on the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="b08d8-105">Aufrufen der [**ifilesinkfilter:: setFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) -Methode für den dateiwriter.</span><span class="sxs-lookup"><span data-stu-id="b08d8-105">Call the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method on the File Writer.</span></span> <span data-ttu-id="b08d8-106">Sie können einen Zeiger auf die [**ifilesinkfilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) -Schnittstelle erhalten, wenn Sie das Diagramm mit dem *psink* -Parameter der setoutputfilename-Methode erstellen.</span><span class="sxs-lookup"><span data-stu-id="b08d8-106">You can get a pointer to the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface when you build the graph, through the *pSink* parameter of the SetOutputFileName method.</span></span> <span data-ttu-id="b08d8-107">Dies wird im folgenden Code veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="b08d8-107">The following code shows how to do this:</span></span>


```C++
IBaseFilter *pMux;
IFileSinkFilter *pSink
hr = pBuild->SetOutputFileName(&MEDIASUBTYPE_Avi, L"C:\\YourFileName.avi", 
    &pMux, &pSink);
if (SUCCEEDED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
        pCap, NULL, pMux);

    if (SUCCEEDED(hr))
    {
        pControl->Run();
        /* Wait awhile, then stop the graph. */
        pControl->Stop();
        // Change the file name and run the graph again.
        pSink->SetFileName(L"YourFileName02.avi", 0);
        pControl->Run();
    }
    pMux->Release();
    pSink->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="b08d8-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b08d8-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b08d8-109">Aufzeichnen von Videos in einer Datei</span><span class="sxs-lookup"><span data-stu-id="b08d8-109">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



