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
# <a name="capturing-an-image-from-a-still-image-pin"></a><span data-ttu-id="8556d-103">Aufzeichnen eines Bilds aus einer weiterhin Abbild-PIN</span><span class="sxs-lookup"><span data-stu-id="8556d-103">Capturing an Image From a Still Image Pin</span></span>

<span data-ttu-id="8556d-104">Einige Kameras können ein anderes Image als den Erfassungsdaten Strom erzeugen, und häufig ist das Image von höherer Qualität als die vom Erfassungsdaten Strom erzeugten Bilder.</span><span class="sxs-lookup"><span data-stu-id="8556d-104">Some cameras can produce a still image separate from the capture stream, and often the still image is of higher quality than the images produced by the capture stream.</span></span> <span data-ttu-id="8556d-105">Die Kamera verfügt möglicherweise über eine Schaltfläche, die als Hardware Trigger fungiert oder das Auslösen von Software unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8556d-105">The camera may have a button that acts as a hardware trigger, or it may support software triggering.</span></span> <span data-ttu-id="8556d-106">Eine Kamera, die weiterhin Bilder unterstützt, macht eine Bild-Pin verfügbar, die die PIN-Kategorie der PIN-Kategorie \_ \_ weiterhin enthält.</span><span class="sxs-lookup"><span data-stu-id="8556d-106">A camera that supports still images will expose a still image pin, which is pin category PIN\_CATEGORY\_STILL.</span></span>

<span data-ttu-id="8556d-107">Die empfohlene Vorgehensweise zum Abrufen von Images vom Gerät ist die Verwendung der Windows-Abbild Erfassungs-APIs (WIA).</span><span class="sxs-lookup"><span data-stu-id="8556d-107">The recommended way to get still images from the device is to use the Windows Image Acquisition (WIA) APIs.</span></span> <span data-ttu-id="8556d-108">Weitere Informationen finden Sie unter "Windows-Abbild Beschaffung" in der Platform SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="8556d-108">For more information, see "Windows Image Acquisition" in the Platform SDK documentation.</span></span> <span data-ttu-id="8556d-109">Sie können jedoch auch DirectShow verwenden, um ein Image zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="8556d-109">However, you can also use DirectShow to capture an image.</span></span>

<span data-ttu-id="8556d-110">Verwenden Sie die [**IAMVideoControl:: setmode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) -Methode, wenn das Diagramm ausgeführt wird, um die immer noch anzuheften, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8556d-110">To trigger the still pin, use the [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) method when the graph is running, as follows:</span></span>


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



<span data-ttu-id="8556d-111">Fragen Sie den Erfassungs Filter für [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)ab.</span><span class="sxs-lookup"><span data-stu-id="8556d-111">Query the capture filter for [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol).</span></span> <span data-ttu-id="8556d-112">Wenn die Schnittstelle unterstützt wird, erhalten Sie einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN, indem Sie die [**ICaptureGraphBuilder2:: findpin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) -Methode aufrufen, wie im vorherigen Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8556d-112">If the interface is supported, get a pointer to the still pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface by calling the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method, as shown in the previous example.</span></span> <span data-ttu-id="8556d-113">Dann wenden Sie [**IAMVideoControl:: setmode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) mit dem **IPin** -Zeiger und dem "videocontrolflag"- \_ auslöserflag an.</span><span class="sxs-lookup"><span data-stu-id="8556d-113">Then call [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) with the **IPin** pointer and the VideoControlFlag\_Trigger flag.</span></span>

> [!Note]  
> <span data-ttu-id="8556d-114">Abhängig von der Kamera müssen Sie möglicherweise die Erfassungs-PIN (PIN \_ - \_ kategorieerfassung) wiederherstellen, bevor die PIN eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="8556d-114">Depending on the camera, you might need to render the capture pin (PIN\_CATEGORY\_CAPTURE) before the still pin will connect.</span></span>

 

### <a name="example-using-the-sample-grabber-filter"></a><span data-ttu-id="8556d-115">Beispiel: Verwenden des Sample-Grabber Filters</span><span class="sxs-lookup"><span data-stu-id="8556d-115">Example: Using the Sample Grabber Filter</span></span>

<span data-ttu-id="8556d-116">Eine Möglichkeit, das Image aufzuzeichnen, ist der [**Beispiel**](sample-grabber-filter.md) Filter für die Erfassung.</span><span class="sxs-lookup"><span data-stu-id="8556d-116">One way to capture the image is with the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="8556d-117">Der Beispiel Grabber verwendet eine Anwendungs definierte Rückruffunktion, um das Bild zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8556d-117">The Sample Grabber uses an application-defined callback function to process the image.</span></span> <span data-ttu-id="8556d-118">Weitere Informationen zum Sample-Grabber Filter finden Sie unter [Verwenden der Beispiel-Grabber](using-the-sample-grabber.md).</span><span class="sxs-lookup"><span data-stu-id="8556d-118">For more information about the Sample Grabber filter, see [Using the Sample Grabber](using-the-sample-grabber.md).</span></span>

<span data-ttu-id="8556d-119">Im folgenden Beispiel wird davon ausgegangen, dass die immer noch PIN ein unkomprimiertes RGB-Bild bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8556d-119">The following example assumes that the still pin delivers an uncompressed RGB image.</span></span> <span data-ttu-id="8556d-120">Definieren Sie zuerst eine Klasse, die die Rückruf Schnittstelle des beispielgrabers implementiert, [**isamplegrabbercb**](isamplegrabbercb.md):</span><span class="sxs-lookup"><span data-stu-id="8556d-120">First, define a class that will implement the Sample Grabber's callback interface, [**ISampleGrabberCB**](isamplegrabbercb.md):</span></span>


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



<span data-ttu-id="8556d-121">Die Implementierung der-Klasse wird in Kürze beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8556d-121">The implementation of the class is described shortly.</span></span>

<span data-ttu-id="8556d-122">Verbinden Sie als nächstes den immer noch mit dem beispielgrabpunkt, und verbinden Sie den Beispiel-Grabber mit dem Filter [**null-Renderer**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="8556d-122">Next, connect the still pin to the Sample Grabber, and connect the Sample Grabber to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span> <span data-ttu-id="8556d-123">Der NULL-Renderer verwirft einfach empfangene Medien Beispiele. die tatsächliche Arbeit erfolgt innerhalb des Rückrufs.</span><span class="sxs-lookup"><span data-stu-id="8556d-123">The Null Renderer simply discards media samples that it receives; the actual work will be done within the callback.</span></span> <span data-ttu-id="8556d-124">(Der einzige Grund für den NULL-Renderer besteht darin, die Ausgabe-PIN der Stichprobenentnahme mit etwas zu verbinden.) Rufen Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um die Beispiel Filter für das Grabber und NULL-Renderer zu erstellen, und rufen Sie [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) auf, um dem Diagramm beide Filter hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="8556d-124">(The only reason for the Null Renderer is to connect the Sample Grabber's output pin to something.) Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Sample Grabber and Null Renderer filters, and call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add both filters to the graph:</span></span>


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



<span data-ttu-id="8556d-125">Sie können die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode verwenden, um alle drei Filter in einem Methoden aufzurufenden zu verbinden, von der noch an die Stichprobenentnahme angeheftet und von der Stichprobenentnahme zum NULL-Renderer zu gelangen:</span><span class="sxs-lookup"><span data-stu-id="8556d-125">You can use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect all three filters in one method call, going from the still pin to the Sample Grabber, and from the Sample Grabber to the Null Renderer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



<span data-ttu-id="8556d-126">Verwenden Sie nun die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle, um den beispielgrabber so zu konfigurieren, dass er Beispiele puffert:</span><span class="sxs-lookup"><span data-stu-id="8556d-126">Now use the [**ISampleGrabber**](isamplegrabber.md) interface to configure the Sample Grabber so that it buffers samples:</span></span>


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



<span data-ttu-id="8556d-127">Legen Sie die Rückruf Schnittstelle mit einem Zeiger auf das Rückruf Objekt fest:</span><span class="sxs-lookup"><span data-stu-id="8556d-127">Set the callback interface with a pointer to your callback object:</span></span>


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



<span data-ttu-id="8556d-128">Dient zum erhalten des Medientyps, den die PIN zum Herstellen einer Verbindung mit dem beispielgrabgeber verwendet hat:</span><span class="sxs-lookup"><span data-stu-id="8556d-128">Get the media type that the still pin used to connect with the Sample Grabber:</span></span>


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



<span data-ttu-id="8556d-129">Dieser Medientyp enthält die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur, die das Format des weiterhin Bilds definiert.</span><span class="sxs-lookup"><span data-stu-id="8556d-129">This media type will contain the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the format of the still image.</span></span> <span data-ttu-id="8556d-130">Geben Sie den Medientyp frei, bevor die Anwendung beendet wird:</span><span class="sxs-lookup"><span data-stu-id="8556d-130">Free the media type before the application exits:</span></span>


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



<span data-ttu-id="8556d-131">Im folgenden finden Sie ein Beispiel für die Rückruf Klasse.</span><span class="sxs-lookup"><span data-stu-id="8556d-131">What follows is an example of the callback class.</span></span> <span data-ttu-id="8556d-132">Beachten Sie, dass die-Klasse **IUnknown** implementiert, das Sie über die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle erbt, aber keinen Verweis Zähler beibehält.</span><span class="sxs-lookup"><span data-stu-id="8556d-132">Note that the class implements **IUnknown**, which it inherits through the [**ISampleGrabber**](isamplegrabber.md) interface, but it does not keep a reference count.</span></span> <span data-ttu-id="8556d-133">Dies ist sicher, da die Anwendung das-Objekt auf dem Stapel erstellt und das-Objekt während der gesamten Lebensdauer des Filter Diagramms im Gültigkeitsbereich bleibt.</span><span class="sxs-lookup"><span data-stu-id="8556d-133">This is safe because the application creates the object on the stack, and the object remains in scope throughout the lifetime of the filter graph.</span></span>

<span data-ttu-id="8556d-134">Die gesamte Arbeit erfolgt in der [**buffercb**](isamplegrabbercb-buffercb.md) -Methode, die von der Sample Grabber aufgerufen wird, wenn Sie ein neues Beispiel erhält.</span><span class="sxs-lookup"><span data-stu-id="8556d-134">All of the work happens in the [**BufferCB**](isamplegrabbercb-buffercb.md) method, which is called by the Sample Grabber whenever it gets a new sample.</span></span> <span data-ttu-id="8556d-135">Im folgenden Beispiel schreibt die-Methode die Bitmap in eine Datei:</span><span class="sxs-lookup"><span data-stu-id="8556d-135">In the following example, the method writes the bitmap to a file:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8556d-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8556d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8556d-137">Video Erfassungs Aufgaben</span><span class="sxs-lookup"><span data-stu-id="8556d-137">Video Capture Tasks</span></span>](video-capture-tasks.md)
</dt> </dl>

 

 
