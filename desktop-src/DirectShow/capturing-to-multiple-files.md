---
description: Erfassen in mehreren Dateien
ms.assetid: 6073a891-e9f5-442d-a2d9-3a7b97f7f735
title: Erfassen in mehreren Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79ce7a1b4b91a0f78031a661e2c2e10895b4a21b1cfb068ca505429468a3af1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017578"
---
# <a name="capturing-to-multiple-files"></a>Erfassen in mehreren Dateien

Nachdem Sie einige Videos in einer Datei erfasst haben, können Sie zu einer neuen Datei wechseln, indem Sie den Graphen beenden und den Dateinamen im [Filter File Writer](file-writer-filter.md) festlegen. Rufen Sie [**die IFileSinkFilter::SetFileName-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) für den File Writer auf. Sie können einen Zeiger auf die [**IFileSinkFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) beim Erstellen des Graphen über den *pSink-Parameter* der SetOutputFileName-Methode erhalten. Dies wird im folgenden Code veranschaulicht:


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

[Erfassen von Videos in einer Datei](capturing-video-to-a-file.md)
</dt> </dl>

 

 



