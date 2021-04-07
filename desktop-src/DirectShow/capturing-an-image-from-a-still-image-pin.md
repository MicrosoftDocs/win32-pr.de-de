---
description: Aufzeichnen eines Bilds aus einer weiterhin Abbild-PIN
ms.assetid: cbcb4d6d-dc85-4ae2-b0a8-110f15092733
title: Aufzeichnen eines Bilds aus einer weiterhin Abbild-PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3510f318f3107dd698dc753704d6c09d70ddd308
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746088"
---
# <a name="capturing-an-image-from-a-still-image-pin"></a>Aufzeichnen eines Bilds aus einer weiterhin Abbild-PIN

Einige Kameras können ein anderes Image als den Erfassungsdaten Strom erzeugen, und häufig ist das Image von höherer Qualität als die vom Erfassungsdaten Strom erzeugten Bilder. Die Kamera verfügt möglicherweise über eine Schaltfläche, die als Hardware Trigger fungiert oder das Auslösen von Software unterstützt. Eine Kamera, die weiterhin Bilder unterstützt, macht eine Bild-Pin verfügbar, die die PIN-Kategorie der PIN-Kategorie \_ \_ weiterhin enthält.

Die empfohlene Vorgehensweise zum Abrufen von Images vom Gerät ist die Verwendung der Windows-Abbild Erfassungs-APIs (WIA). Weitere Informationen finden Sie unter "Windows-Abbild Beschaffung" in der Platform SDK-Dokumentation. Sie können jedoch auch DirectShow verwenden, um ein Image zu erfassen.

Verwenden Sie die [**IAMVideoControl:: setmode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) -Methode, wenn das Diagramm ausgeführt wird, um die immer noch anzuheften, wie folgt:


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



Fragen Sie den Erfassungs Filter für [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)ab. Wenn die Schnittstelle unterstützt wird, erhalten Sie einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN, indem Sie die [**ICaptureGraphBuilder2:: findpin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) -Methode aufrufen, wie im vorherigen Beispiel gezeigt. Dann wenden Sie [**IAMVideoControl:: setmode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) mit dem **IPin** -Zeiger und dem "videocontrolflag"- \_ auslöserflag an.

> [!Note]  
> Abhängig von der Kamera müssen Sie möglicherweise die Erfassungs-PIN (PIN \_ - \_ kategorieerfassung) wiederherstellen, bevor die PIN eine Verbindung herstellt.

 

### <a name="example-using-the-sample-grabber-filter"></a>Beispiel: Verwenden des Sample-Grabber Filters

Eine Möglichkeit, das Image aufzuzeichnen, ist der [**Beispiel**](sample-grabber-filter.md) Filter für die Erfassung. Der Beispiel Grabber verwendet eine Anwendungs definierte Rückruffunktion, um das Bild zu verarbeiten. Weitere Informationen zum Sample-Grabber Filter finden Sie unter [Verwenden der Beispiel-Grabber](using-the-sample-grabber.md).

Im folgenden Beispiel wird davon ausgegangen, dass die immer noch PIN ein unkomprimiertes RGB-Bild bereitstellt. Definieren Sie zuerst eine Klasse, die die Rückruf Schnittstelle des beispielgrabers implementiert, [**isamplegrabbercb**](isamplegrabbercb.md):


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



Die Implementierung der-Klasse wird in Kürze beschrieben.

Verbinden Sie als nächstes den immer noch mit dem beispielgrabpunkt, und verbinden Sie den Beispiel-Grabber mit dem Filter [**null-Renderer**](null-renderer-filter.md) . Der NULL-Renderer verwirft einfach empfangene Medien Beispiele. die tatsächliche Arbeit erfolgt innerhalb des Rückrufs. (Der einzige Grund für den NULL-Renderer besteht darin, die Ausgabe-PIN der Stichprobenentnahme mit etwas zu verbinden.) Rufen Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um die Beispiel Filter für das Grabber und NULL-Renderer zu erstellen, und rufen Sie [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) auf, um dem Diagramm beide Filter hinzuzufügen:


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



Sie können die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode verwenden, um alle drei Filter in einem Methoden aufzurufenden zu verbinden, von der noch an die Stichprobenentnahme angeheftet und von der Stichprobenentnahme zum NULL-Renderer zu gelangen:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



Verwenden Sie nun die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle, um den beispielgrabber so zu konfigurieren, dass er Beispiele puffert:


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



Legen Sie die Rückruf Schnittstelle mit einem Zeiger auf das Rückruf Objekt fest:


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



Dient zum erhalten des Medientyps, den die PIN zum Herstellen einer Verbindung mit dem beispielgrabgeber verwendet hat:


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



Dieser Medientyp enthält die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur, die das Format des weiterhin Bilds definiert. Geben Sie den Medientyp frei, bevor die Anwendung beendet wird:


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



Im folgenden finden Sie ein Beispiel für die Rückruf Klasse. Beachten Sie, dass die-Klasse **IUnknown** implementiert, das Sie über die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle erbt, aber keinen Verweis Zähler beibehält. Dies ist sicher, da die Anwendung das-Objekt auf dem Stapel erstellt und das-Objekt während der gesamten Lebensdauer des Filter Diagramms im Gültigkeitsbereich bleibt.

Die gesamte Arbeit erfolgt in der [**buffercb**](isamplegrabbercb-buffercb.md) -Methode, die von der Sample Grabber aufgerufen wird, wenn Sie ein neues Beispiel erhält. Im folgenden Beispiel schreibt die-Methode die Bitmap in eine Datei:


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

[Video Erfassungs Aufgaben](video-capture-tasks.md)
</dt> </dl>

 

 
