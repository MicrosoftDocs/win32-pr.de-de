---
description: Der Beispiel-Grabber Filter ist ein Transformations Filter, der zum Erfassen von Medien Beispielen aus einem Stream verwendet werden kann, während diese das Filter Diagramm durchlaufen.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Verwenden der Beispiel-Grabber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4886c796691e83e02b58ddea129d60d5004c9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357877"
---
# <a name="using-the-sample-grabber"></a>Verwenden der Beispiel-Grabber

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Der [**Beispiel-Grabber**](sample-grabber-filter.md) Filter ist ein Transformations Filter, der zum Erfassen von Medien Beispielen aus einem Stream verwendet werden kann, während diese das Filter Diagramm durchlaufen.

Wenn Sie einfach eine Bitmap aus einer Videodatei erfassen möchten, ist es einfacher, das [Media Detector-Objekt (mediadet)](media-detector--mediadet.md) zu verwenden. Ausführliche Informationen finden Sie unter [Erfassen eines Poster-Frames](grabbing-a-poster-frame.md) . Der Beispiel-Grabber ist jedoch flexibler, da er mit nahezu jedem Medientyp funktioniert (siehe [**isamplegrabber:: setmediatype**](isamplegrabber-setmediatype.md) für die wenigen Ausnahmen) und eine größere Kontrolle für die Anwendung bietet.

-   [Erstellen des Filter Graph-Managers](#create-the-filter-graph-manager)
-   [Hinzufügen des beispielgrabsteins zum Filter Diagramm](#add-the-sample-grabber-to-the-filter-graph)
-   [Festlegen des Medientyps](#set-the-media-type)
-   [Erstellen des Filter Diagramms](#build-the-filter-graph)
-   [Ausführen des Diagramms](#run-the-graph)
-   [Holen Sie sich das Beispiel](#grab-the-sample)
-   [Beispiel Code](#example-code)
-   [Zugehörige Themen](#related-topics)

## <a name="create-the-filter-graph-manager"></a>Erstellen des Filter Graph-Managers

Erstellen Sie zunächst den [Filter Graph-Manager](filter-graph-manager.md) , und Fragen Sie die Schnittstellen [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) und [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) ab.


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





## <a name="add-the-sample-grabber-to-the-filter-graph"></a>Hinzufügen des beispielgrabsteins zum Filter Diagramm

Erstellen Sie eine Instanz des Sample-Grabber Filters und addieren Sie zum Filter Diagramm. Fragen Sie den beispielgrabfilter für die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle ab.


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

Wenn Sie die Beispiel-Grabber erstmalig erstellen, hat Sie keinen bevorzugten Medientyp. Dies bedeutet, dass Sie eine Verbindung mit fast jedem Filter im Diagramm herstellen können, aber Sie haben keine Kontrolle über die Art der empfangenen Daten. Bevor Sie den Rest des Diagramms aufbauen, müssen Sie daher einen Medientyp für den beispielgrabber festlegen, indem Sie die [**isamplegrabber:: setmediatype**](isamplegrabber-setmediatype.md) -Methode aufrufen.

Wenn der Sample Grabber eine Verbindung herstellt, vergleicht dieser den Medientyp mit dem Medientyp, der vom anderen Filter angeboten wird. Die einzigen Felder, die überprüft werden, sind der Haupttyp, der Untertyp und der Formattyp. Für einen dieser Werte bedeutet der Wert GUID \_ NULL, dass "beliebige Werte akzeptieren" angezeigt wird. In den meisten Fällen möchten Sie den Haupttyp und den Untertyp festlegen. Der folgende Code gibt beispielsweise ein unkomprimiertes 24-Bit-RGB-Video an:


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



## <a name="build-the-filter-graph"></a>Erstellen des Filter Diagramms

Nun können Sie den Rest des Filter Diagramms erstellen. Da der beispielgrabber nur mithilfe des von Ihnen angegebenen Medientyps eine Verbindung herstellt, können Sie die [intelligenten Verbindungs](intelligent-connect.md) Mechanismen des Filter Graph-Managers nutzen, wenn Sie das Diagramm erstellen.

Wenn Sie z. b. nicht komprimierte Videos angegeben haben, können Sie einen Quell Filter mit dem beispielgrabber verbinden, und der Filter Graph-Manager fügt automatisch den Datei Parser und den Decoder hinzu. Im folgenden Beispiel wird die Hilfsfunktion connectfilters verwendet, die unter [Verbinden von zwei Filtern](connect-two-filters.md)aufgeführt ist:


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





Der Beispiel Grabber ist ein Transformations Filter, sodass die Ausgabe-PIN mit einem anderen Filter verbunden werden muss. Häufig möchten Sie die Beispiele auch verwerfen, wenn Sie Sie nicht mehr benötigen. Verbinden Sie in diesem Fall den Beispiel-Grabber mit dem [**Filter NULL-Renderer**](null-renderer-filter.md), der die empfangenen Daten verwirft.

Im folgenden Beispiel wird die Beispiel-Grabber mit dem NULL-rendererfilter verbunden:


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





Beachten Sie, dass das Platzieren des Beispiel Grabsteins zwischen einem Video Decoder und dem Videorenderer die Renderingleistung erheblich beeinträchtigen kann. Der Beispiel Grabber ist ein übergreifendes Filter, d. h. der Ausgabepuffer ist mit dem Eingabepuffer identisch. Beim Video Rendering befindet sich der Ausgabepuffer wahrscheinlich auf der Grafikkarte, bei der Lesevorgänge im Vergleich zu Lesevorgängen im Hauptspeicher wesentlich langsamer sind.

## <a name="run-the-graph"></a>Ausführen des Diagramms

Der Beispiel Grabber funktioniert in einem von zwei Modi:

-   Der Puffer Modus erstellt eine Kopie jeder Stichprobe, bevor das Beispiel für die downstreamausgabe bereitgestellt wird.
-   Der Rückruf Modus Ruft eine Anwendungs definierte Rückruffunktion für jedes Beispiel auf.

In diesem Artikel wird der Puffer Modus beschrieben. (Bevor Sie den Rückruf Modus verwenden, beachten Sie, dass die Rückruffunktion sehr eingeschränkt sein muss. Andernfalls kann die Leistung drastisch reduziert werden, und es kann sogar zu Deadlocks führen. Weitere Informationen finden Sie unter [**isamplegrabber:: SetCallback**](isamplegrabber-setcallback.md).) Um den Puffer Modus zu aktivieren, müssen Sie die [**isamplegrabber:: setbuffersamples**](isamplegrabber-setbuffersamples.md) -Methode mit dem Wert " **true**" aufrufen.

Optional können Sie die [**isamplegrabber:: setoneshot**](isamplegrabber-setoneshot.md) -Methode mit dem Wert " **true**" aufzurufen. Dies bewirkt, dass der Sample Grabber nach dem Empfang des ersten Medien Beispiels angehalten wird. Dies ist hilfreich, wenn Sie einen einzelnen Frame aus dem Stream ziehen möchten. Suchen Sie nach der gewünschten Zeit, führen Sie das Diagramm aus, und warten Sie auf das " [**EC \_ Complete**](ec-complete.md) "-Ereignis. Beachten Sie, dass die Ebene der Frame Genauigkeit von der Quelle abhängig ist. Beispielsweise ist das Suchen einer MPEG-Datei oft nicht Frame genau.

Wenn Sie das Diagramm so schnell wie möglich ausführen möchten, schalten Sie die Diagramm Uhr ein, wie unter [Festlegen der Graph-Uhr](setting-the-graph-clock.md)beschrieben.

Im folgenden Beispiel werden der One-Shot-Modus und der Puffer Modus aktiviert, das Filter Diagramm ausgeführt und auf den Abschluss gewartet.


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



## <a name="grab-the-sample"></a>Holen Sie sich das Beispiel

Im Puffer Modus speichert der Beispiel Grabber eine Kopie jeder Stichprobe. Die Methode [**isamplegrabber:: getcurrentbuffer**](isamplegrabber-getcurrentbuffer.md) kopiert den Puffer in ein Array, das vom Aufrufer zugeordnet wird. Um die Größe des benötigten Arrays zu ermitteln, müssen Sie zuerst **getcurrentbuffer** mit einem **null** -Zeiger für die Array Adresse aufrufen. Weisen Sie dann das Array zu, und nennen Sie die Methode ein zweites Mal, um den Puffer zu kopieren. Das folgende Beispiel zeigt die erforderlichen Schritte:


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



Sie müssen das genaue Format der Daten im Puffer kennen. Um diese Informationen abzurufen, nennen Sie die [**isamplegrabber:: getconnectedmediatype**](isamplegrabber-getconnectedmediatype.md) -Methode. Diese Methode füllt eine [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur mit dem-Format auf.

Bei einem unkomprimierten Videostream sind die Formatinformationen in einer [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur enthalten. Im folgenden Beispiel wird veranschaulicht, wie die Formatinformationen für einen unkomprimierten Videostream angezeigt werden.


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
> Der Beispiel Grabber unterstützt [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)nicht.

 

## <a name="example-code"></a>Beispielcode

Dies ist der gesamte Code für die vorherigen Beispiele.

> [!Note]  
> In diesem Beispiel wird die Funktion " [saferelease](../medfound/saferelease.md) " verwendet, um Schnittstellen Zeiger freizugeben.

 


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

[Verwenden von DirectShow-Bearbeitungs Diensten](using-directshow-editing-services.md)
</dt> </dl>

 

 
