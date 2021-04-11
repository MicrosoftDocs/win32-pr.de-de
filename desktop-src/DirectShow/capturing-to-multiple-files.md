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
# <a name="capturing-to-multiple-files"></a>Erfassen in mehreren Dateien

Nachdem Sie einige Videos in einer Datei aufgezeichnet haben, können Sie zu einer neuen Datei wechseln, indem Sie das Diagramm beenden und den Dateinamen für den [dateiwriter](file-writer-filter.md) -Filter festlegen. Aufrufen der [**ifilesinkfilter:: setFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) -Methode für den dateiwriter. Sie können einen Zeiger auf die [**ifilesinkfilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) -Schnittstelle erhalten, wenn Sie das Diagramm mit dem *psink* -Parameter der setoutputfilename-Methode erstellen. Dies wird im folgenden Code veranschaulicht:


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Videos in einer Datei](capturing-video-to-a-file.md)
</dt> </dl>

 

 



