---
description: Der Sample Grabber-Filter ist ein Transformationsfilter, der verwendet werden kann, um Medienbeispiele aus einem Stream zu greifen, während sie das Filterdiagramm durchlaufen.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Verwenden des Beispielgrabbers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47318b7bd4dbbad57fb82bec11e0a1293a0284c906c78fc7175d8a758ad477f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083560"
---
# <a name="using-the-sample-grabber"></a>Verwenden des Beispielgrabbers

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Der [**Sample Grabber-Filter**](sample-grabber-filter.md) ist ein Transformationsfilter, der verwendet werden kann, um Medienbeispiele aus einem Stream zu greifen, während sie das Filterdiagramm durchlaufen.

Wenn Sie einfach eine Bitmap aus einer Videodatei abrufen möchten, ist es einfacher, das [Media Detector -Objekt (MediaDet)](media-detector--mediadet.md) zu verwenden. Weitere Informationen finden Sie unter [Grabbing a Poster Frame (Greifen](grabbing-a-poster-frame.md) eines Posterrahmens). Der Beispielgrabber ist jedoch flexibler, da er mit nahezu jedem Medientyp funktioniert (einige Ausnahmen finden Sie unter [**ISampleGrabber::SetMediaType),**](isamplegrabber-setmediatype.md) und bietet mehr Kontrolle für die Anwendung.

-   [Erstellen des Filter-Graph-Managers](#create-the-filter-graph-manager)
-   [Hinzufügen des Beispielgrabbers zum Filter Graph](#add-the-sample-grabber-to-the-filter-graph)
-   [Festlegen des Medientyps](#set-the-media-type)
-   [Erstellen des filter-Graph](#build-the-filter-graph)
-   [Ausführen des Graph](#run-the-graph)
-   [Greifen Sie auf das Beispiel zu.](#grab-the-sample)
-   [Beispielcode](#example-code)
-   [Zugehörige Themen](#related-topics)

## <a name="create-the-filter-graph-manager"></a>Erstellen des Filter-Graph-Managers

Erstellen Sie zunächst den [Filter Graph-Manager,](filter-graph-manager.md) und fragen Sie die Schnittstellen [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) und [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) ab.


```C++
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;


    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="add-the-sample-grabber-to-the-filter-graph"></a>Hinzufügen des Beispielgrabbers zum Filter Graph

Erstellen Sie eine Instanz des Beispielgrabberfilters, und fügen Sie dem Filterdiagramm hinzu. Fragen Sie den Sample Grabber-Filter für die [**ISampleGrabber-Schnittstelle**](isamplegrabber.md) ab.


```C++
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;


    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="set-the-media-type"></a>Festlegen des Medientyps

Wenn Sie den Beispielgrabber zum ersten Mal erstellen, hat er keinen bevorzugten Medientyp. Dies bedeutet, dass Sie eine Verbindung mit fast jedem Filter im Diagramm herstellen können, aber Sie haben keine Kontrolle über den Typ der empfangenen Daten. Bevor Sie den Rest des Graphen erstellen, müssen Sie daher einen Medientyp für den Sample Grabber festlegen, indem Sie die [**ISampleGrabber::SetMediaType-Methode**](isamplegrabber-setmediatype.md) aufrufen.

Wenn der Beispielgrabber eine Verbindung herstellt, wird dieser Medientyp mit dem Medientyp verglichen, der vom anderen Filter angeboten wird. Die einzigen Felder, die überprüft werden, sind Haupttyp, Untertyp und Formattyp. Für jede dieser Werte bedeutet der Wert GUID \_ NULL "Accept any value". In den meisten Jahren möchten Sie den Haupttyp und den Untertyp festlegen. Der folgende Code gibt beispielsweise ein nicht komprimiertes 24-Bit-RGB-Video an:


```C++
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="build-the-filter-graph"></a>Erstellen des filter-Graph

Jetzt können Sie den Rest des Filterdiagramms erstellen. Da der Beispielgrabber nur eine Verbindung mit dem angegebenen Medientyp herstellt, können Sie die [Intelligent Verbinden-Mechanismen](intelligent-connect.md) von Filter Graph Manager nutzen, wenn Sie das Diagramm erstellen.

Wenn Sie beispielsweise unkomprimiertes Video angegeben haben, können Sie einen Quellfilter mit dem Beispielgrabber verbinden, und der Filter Graph Manager fügt automatisch den Dateiparser und den Decoder hinzu. Im folgenden Beispiel wird die ConnectFilters-Hilfsfunktion verwendet, die in [Verbinden Zwei Filter](connect-two-filters.md)aufgeführt ist:


```C++
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;


    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }
```





Der Beispielgrabber ist ein Transformationsfilter, sodass der Ausgabepin mit einem anderen Filter verbunden werden muss. Häufig möchten Sie die Beispiele einfach verwerfen, nachdem Sie damit fertig sind. Verbinden Sie in diesem Fall den Sample Grabber mit dem [**NULL-Rendererfilter,**](null-renderer-filter.md)der die empfangenen Daten verwirft.

Im folgenden Beispiel wird der Sample Grabber mit dem Filter NULL-Renderer verbunden:


```C++
    IBaseFilter *pNullF = NULL;


    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }
```





Beachten Sie, dass das Platzieren des Beispielgrabbers zwischen einem Videodecoder und dem Videorenderer die Renderingleistung erheblich beeinträchtigen kann. Der Beispielgrabber ist ein trans-in-place-Filter, was bedeutet, dass der Ausgabepuffer mit dem Eingabepuffer identisch ist. Beim Videorendering befindet sich der Ausgabepuffer wahrscheinlich auf der Grafikkarte, wo Lesevorgänge im Vergleich zu Lesevorgängen im Hauptspeicher viel langsamer sind.

## <a name="run-the-graph"></a>Ausführen des Graph

Der Beispielgrabber arbeitet in einem von zwei Modi:

-   Der Puffermodus erstellt eine Kopie jedes Beispiels, bevor das Beispiel nachgeschaltet wird.
-   Der Rückrufmodus ruft eine anwendungsdefinierte Rückruffunktion für jedes Beispiel auf.

In diesem Artikel wird der Puffermodus beschrieben. (Beachten Sie vor der Verwendung des Rückrufmodus, dass die Rückruffunktion recht eingeschränkt sein muss. Andernfalls kann dies die Leistung drastisch reduzieren oder sogar Deadlocks verursachen. Weitere Informationen finden Sie unter [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).) Um den Puffermodus zu aktivieren, rufen Sie die [**ISampleGrabber::SetBufferSamples-Methode**](isamplegrabber-setbuffersamples.md) mit dem Wert **TRUE** auf.

Rufen Sie optional die [**ISampleGrabber::SetOneShot-Methode**](isamplegrabber-setoneshot.md) mit dem Wert **TRUE** auf. Dies bewirkt, dass der Sample Grabber angehalten wird, nachdem er das erste Medienbeispiel empfangen hat. Dies ist hilfreich, wenn Sie einen einzelnen Frame aus dem Stream greifen möchten. Suchen Sie nach der gewünschten Zeit, führen Sie das Diagramm aus, und warten Sie auf das [**EC \_ COMPLETE-Ereignis.**](ec-complete.md) Beachten Sie, dass der Grad der Framegenauigkeit von der Quelle abhängt. Beispielsweise ist die Suche nach einer MPEG-Datei häufig nicht framegenau.

Um das Diagramm so schnell wie möglich auszuführen, drehen Sie die Graphuhr wie unter [Festlegen der Graph Uhr](setting-the-graph-clock.md)beschrieben.

Im folgenden Beispiel werden der Einmalmodus und der Puffermodus aktiviert, das Filterdiagramm ausgeführt und auf den Abschluss gewartet.


```C++
    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
```



## <a name="grab-the-sample"></a>Greifen Sie auf das Beispiel zu.

Im Puffermodus speichert der Beispielgrabber eine Kopie jedes Beispiels. Die [**ISampleGrabber::GetCurrentBuffer-Methode**](isamplegrabber-getcurrentbuffer.md) kopiert den Puffer in ein vom Aufrufer zugeordnetes Array. Um die Größe des benötigten Arrays zu bestimmen, rufen Sie zunächst **GetCurrentBuffer** mit einem **NULL-Zeiger** für die Arrayadresse auf. Ordnen Sie dann das Array zu, und rufen Sie die -Methode ein zweites Mal auf, um den Puffer zu kopieren. Das folgende Beispiel zeigt die erforderlichen Schritte:


```C++
    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }
```



Sie müssen das genaue Format der Daten im Puffer kennen. Rufen Sie zum Abrufen dieser Informationen die [**ISampleGrabber::GetConnectedMediaType-Methode**](isamplegrabber-getconnectedmediatype.md) auf. Diese Methode füllt eine [**AM \_ MEDIA \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) mit dem Format auf.

Bei einem nicht komprimierten Videostream sind die Formatinformationen in einer [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) enthalten. Das folgende Beispiel zeigt, wie Sie die Formatinformationen für einen nicht komprimierten Videostream abrufen.


```C++
    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }
```



> [!Note]  
> Der Beispielgrabber unterstützt [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)nicht.

 

## <a name="example-code"></a>Beispielcode

Hier ist der vollständige Code für die vorherigen Beispiele.

> [!Note]  
> In diesem Beispiel wird die [SafeRelease-Funktion](../medfound/saferelease.md) verwendet, um Schnittstellenzeiger freizugeben.

 


```C++
#include <windows.h>
#include <dshow.h>
#include "qedit.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}



HRESULT WriteBitmap(PCWSTR, BITMAPINFOHEADER*, size_t, BYTE*, size_t);

HRESULT GrabVideoBitmap(PCWSTR pszVideoFile, PCWSTR pszBitmapFile)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    IBaseFilter *pNullF = NULL;

    BYTE *pBuffer = NULL;

    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }

    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }

    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);

    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->GetConnectedMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }

    FreeMediaType(mt);

done:
    CoTaskMemFree(pBuffer);
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    SafeRelease(&pNullF);
    SafeRelease(&pSourceF);
    SafeRelease(&pGrabber);
    SafeRelease(&pGrabberF);
    SafeRelease(&pControl);
    SafeRelease(&pEvent);
    SafeRelease(&pGraph);
    return hr;
};

// Writes a bitmap file
//  pszFileName:  Output file name.
//  pBMI:         Bitmap format information (including pallete).
//  cbBMI:        Size of the BITMAPINFOHEADER, including palette, if present.
//  pData:        Pointer to the bitmap bits.
//  cbData        Size of the bitmap, in bytes.

HRESULT WriteBitmap(PCWSTR pszFileName, BITMAPINFOHEADER *pBMI, size_t cbBMI,
    BYTE *pData, size_t cbData)
{
    HANDLE hFile = CreateFile(pszFileName, GENERIC_WRITE, 0, NULL, 
        CREATE_ALWAYS, 0, NULL);
    if (hFile == NULL)
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }

    BITMAPFILEHEADER bmf = { };

    bmf.bfType = &#39;MB&#39;;
    bmf.bfSize = cbBMI+ cbData + sizeof(bmf); 
    bmf.bfOffBits = sizeof(bmf) + cbBMI; 

    DWORD cbWritten = 0;
    BOOL result = WriteFile(hFile, &bmf, sizeof(bmf), &cbWritten, NULL);
    if (result)
    {
        result = WriteFile(hFile, pBMI, cbBMI, &cbWritten, NULL);
    }
    if (result)
    {
        result = WriteFile(hFile, pData, cbData, &cbWritten, NULL);
    }

    HRESULT hr = result ? S_OK : HRESULT_FROM_WIN32(GetLastError());

    CloseHandle(hFile);

    return hr;
}
```





## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow-Bearbeitungsdiensten](using-directshow-editing-services.md)
</dt> </dl>

 

 
