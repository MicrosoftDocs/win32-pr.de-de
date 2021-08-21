---
description: Erfassen eines Bilds von einem Anheften eines Stillbilds
ms.assetid: cbcb4d6d-dc85-4ae2-b0a8-110f15092733
title: Erfassen eines Bilds von einem Anheften eines Stillbilds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab750fb6b847bc39d28c8906df8dcb982278f7a4447bfc3d79631ee58eb574e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158662"
---
# <a name="capturing-an-image-from-a-still-image-pin"></a>Erfassen eines Bilds von einem Anheften eines Stillbilds

Einige Kameras können ein Stillbild unabhängig vom Erfassungsstream erzeugen, und häufig hat das Stillbild eine höhere Qualität als die vom Erfassungsstream erzeugten Bilder. Die Kamera kann über eine Taste verfügen, die als Hardwaretrigger fungiert, oder sie unterstützt möglicherweise Softwaretrigger. Eine Kamera, die Noch-Bilder unterstützt, macht einen Noch-Bild-Pin verfügbar, bei dem es sich um die Pinkategorie PIN \_ CATEGORY \_ STILL handelt.

Die empfohlene Methode zum Erhalten von Stillimages vom Gerät ist die Verwendung Windows WIA-APIs (Image Acquisition). Weitere Informationen finden Sie unter "Windows Image Acquisition" in der Platform SDK-Dokumentation. Sie können jedoch auch DirectShow verwenden, um ein Bild zu erfassen.

Verwenden Sie die [**IAMVideoControl::SetMode-Methode,**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) wenn das Diagramm ausgeführt wird, um den Noch-Pin auszulösen:


```C++
IAMVideoControl *pAMVidControl = NULL;

hr = pControl->Run(); // Run the graph.
if (FAILED(hr))
{
    // Handle error.
}

hr = pCap->QueryInterface(IID_IAMVideoControl, (void**)&pAMVidControl);

if (SUCCEEDED(hr))
{
    // Find the still pin.
    IPin *pPin = NULL;

    // pBuild is an ICaptureGraphBuilder2 pointer.

    hr = pBuild->FindPin(
        pCap,                  // Filter.
        PINDIR_OUTPUT,         // Look for an output pin.
        &PIN_CATEGORY_STILL,   // Pin category.
        NULL,                  // Media type (don't care).
        FALSE,                 // Pin must be unconnected.
        0,                     // Get the 0'th pin.
        &pPin                  // Receives a pointer to thepin.
        );

    if (SUCCEEDED(hr))
    {
        hr = pAMVidControl->SetMode(pPin, VideoControlFlag_Trigger);
        pPin->Release();
    }
    pAMVidControl->Release();
}
```



Fragen Sie den Erfassungsfilter für [**IAMVideoControl ab.**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol) Wenn die Schnittstelle unterstützt wird, rufen Sie einen Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Noch-Pins ab, indem Sie die [**ICaptureGraphBuilder2::FindPin-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) aufrufen, wie im vorherigen Beispiel gezeigt. Rufen Sie [**dann IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) mit dem **IPin-Zeiger** und dem VideoControlFlag-Triggerflag \_ auf.

> [!Note]  
> Abhängig von der Kamera müssen Sie möglicherweise den Aufnahmepin (PIN CATEGORY CAPTURE) rendern, bevor die Verbindung mit dem \_ \_ Noch-Pin hergestellt wird.

 

### <a name="example-using-the-sample-grabber-filter"></a>Beispiel: Verwenden des Beispielgrabfilters

Eine Möglichkeit zum Erfassen des Bilds ist der [**Filter Sample Grabber.**](sample-grabber-filter.md) Der Beispielgrabvorgang verwendet eine anwendungsdefinierte Rückruffunktion, um das Bild zu verarbeiten. Weitere Informationen zum Beispielgrabfilter finden Sie unter [Using the Sample Grabber](using-the-sample-grabber.md).

Im folgenden Beispiel wird davon ausgegangen, dass der Noch-Pin ein unkomprimiertes RGB-Bild liefert. Definieren Sie zunächst eine Klasse, die die Rückrufschnittstelle von Sample Grabber, [**ISampleGrabberCB, implementiert:**](isamplegrabbercb.md)


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



Die Implementierung der -Klasse wird in Kürze beschrieben.

Verbinden Sie als Nächstes den Noch-Pin mit dem Sample Grabber, und verbinden Sie den Sample Grabber mit dem [**Filter NULL Renderer.**](null-renderer-filter.md) Der NULL-Renderer verwirft einfach die empfangenen Medienbeispiele. die eigentliche Arbeit erfolgt innerhalb des Rückrufs. (Der einzige Grund für den NULL-Renderer ist, den Ausgabepin des Beispielgrabbers mit etwas zu verbinden.) Rufen [**Sie CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um die Filter Sample Grabber und NULL Renderer zu erstellen, und rufen Sie [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) auf, um dem Diagramm beide Filter hinzuzufügen:


```C++
// Add the Sample Grabber filter to the graph.
IBaseFilter *pSG_Filter;
hr = CoCreateInstance(
    CLSID_SampleGrabber, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pSG_Filter
    );

hr = pGraph->AddFilter(pSG_Filter, L"SampleGrab");

// Add the Null Renderer filter to the graph.
IBaseFilter *pNull;

hr = CoCreateInstance(
    CLSID_NullRenderer, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pNull
    );

hr = pGraph->AddFilter(pNull, L"NullRender");
```



Sie können die [**ICaptureGraphBuilder2::RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) verwenden, um alle drei Filter in einem Methodenaufruf zu verbinden, von der noch angeheften zum Beispielgrabber und vom Sample Grabber zum NULL-Renderer:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



Verwenden Sie nun die [**ISampleGrabber-Schnittstelle,**](isamplegrabber.md) um den Beispielgrabber so zu konfigurieren, dass er Beispiele puffert:


```C++
// Configure the Sample Grabber.
ISampleGrabber *pSG = NULL;

hr = pSG_Filter->QueryInterface(IID_ISampleGrabber, (void**)&pSG);
if (SUCCEEDED(hr))
{
    hr = pSG->SetOneShot(FALSE);
    hr = pSG->SetBufferSamples(TRUE);

    ...
```



Legen Sie die Rückrufschnittstelle mit einem Zeiger auf Ihr Rückrufobjekt fest:


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



Dient zum Erhalten des Medientyps, mit dem die Verbindung mit dem Beispielgramber hergestellt wird:


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



Dieser Medientyp enthält die [**BITMAPINFOHEADER-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) die das Format des Stillbilds definiert. Geben Sie den Medientyp frei, bevor die Anwendung beendet wird:


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



Im Folgenden sehen Sie ein Beispiel für die Rückrufklasse. Beachten Sie, dass die -Klasse **IUnknown** implementiert, das sie über die [**ISampleGrabber-Schnittstelle**](isamplegrabber.md) erbt, aber keine Verweisanzahl beibehalten. Dies ist sicher, da die Anwendung das Objekt auf dem Stapel erstellt und das Objekt während der gesamten Lebensdauer des Filterdiagramms im Gültigkeitsbereich verbleibt.

Die ganze Arbeit erfolgt in der [**BufferCB-Methode,**](isamplegrabbercb-buffercb.md) die vom Sample Grabber aufgerufen wird, wenn sie ein neues Beispiel erhält. Im folgenden Beispiel schreibt die -Methode die Bitmap in eine Datei:


```C++
class SampleGrabberCallback : public ISampleGrabberCB
{
public:
    // Fake referance counting.
    STDMETHODIMP_(ULONG) AddRef() { return 1; }
    STDMETHODIMP_(ULONG) Release() { return 2; }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppvObject)
    {
        if (NULL == ppvObject) return E_POINTER;
        if (riid == __uuidof(IUnknown))
        {
            *ppvObject = static_cast<IUnknown*>(this);
             return S_OK;
        }
        if (riid == __uuidof(ISampleGrabberCB))
        {
            *ppvObject = static_cast<ISampleGrabberCB*>(this);
             return S_OK;
        }
        return E_NOTIMPL;
    }

    STDMETHODIMP SampleCB(double Time, IMediaSample *pSample)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP BufferCB(double Time, BYTE *pBuffer, long BufferLen)
    {
        if ((g_StillMediaType.majortype != MEDIATYPE_Video) ||
            (g_StillMediaType.formattype != FORMAT_VideoInfo) ||
            (g_StillMediaType.cbFormat < sizeof(VIDEOINFOHEADER)) ||
            (g_StillMediaType.pbFormat == NULL))
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
        HANDLE hf = CreateFile("C:\\Example.bmp", GENERIC_WRITE, 
        FILE_SHARE_WRITE, NULL, CREATE_ALWAYS, 0, NULL);
        if (hf == INVALID_HANDLE_VALUE)
        {
            return E_FAIL;
        }
        long cbBitmapInfoSize = g_StillMediaType.cbFormat - SIZE_PREHEADER;
        VIDEOINFOHEADER *pVideoHeader =
           (VIDEOINFOHEADER*)g_StillMediaType.pbFormat;

        BITMAPFILEHEADER bfh;
        ZeroMemory(&bfh, sizeof(bfh));
        bfh.bfType = 'MB';  // Little-endian for "BM".
        bfh.bfSize = sizeof( bfh ) + BufferLen + cbBitmapInfoSize;
        bfh.bfOffBits = sizeof( BITMAPFILEHEADER ) + cbBitmapInfoSize;
        
        // Write the file header.
        DWORD dwWritten = 0;
        WriteFile( hf, &bfh, sizeof( bfh ), &dwWritten, NULL );
        WriteFile(hf, HEADER(pVideoHeader), cbBitmapInfoSize, &dwWritten, NULL);        
        WriteFile( hf, pBuffer, BufferLen, &dwWritten, NULL );
        CloseHandle( hf );
        return S_OK;

    }
};
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgaben der Videoaufzeichnung](video-capture-tasks.md)
</dt> </dl>

 

 
