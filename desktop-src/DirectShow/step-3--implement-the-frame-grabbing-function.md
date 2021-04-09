---
description: Schritt 3 Implementieren der Frame-Grabbing-Funktion
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: Schritt 3 Implementieren der Frame-Grabbing-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97f585ff365e40ec611a9e11ce365839aa87be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867088"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a><span data-ttu-id="25d82-103">Schritt 3: Implementieren der Frame-Grabbing-Funktion</span><span class="sxs-lookup"><span data-stu-id="25d82-103">Step 3: Implement the Frame-Grabbing Function</span></span>

<span data-ttu-id="25d82-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="25d82-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="25d82-105">Dieses Thema ist Schritt 3 zum Durchlaufen [eines Poster Frame](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="25d82-105">This topic is Step 3 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="25d82-106">Der nächste Schritt ist die Implementierung der getbitmap-Funktion, die mithilfe des Medien Detektors einen Poster-Frame verwendet.</span><span class="sxs-lookup"><span data-stu-id="25d82-106">The next step is to implement the GetBitmap function, which uses the Media Detector to grab a poster frame.</span></span> <span data-ttu-id="25d82-107">Führen Sie in dieser Funktion die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="25d82-107">Inside this function, perform the following steps:</span></span>

1.  <span data-ttu-id="25d82-108">Erstellen Sie den Medien Detektor.</span><span class="sxs-lookup"><span data-stu-id="25d82-108">Create the Media Detector.</span></span>
2.  <span data-ttu-id="25d82-109">Geben Sie eine Mediendatei an.</span><span class="sxs-lookup"><span data-stu-id="25d82-109">Specify a media file.</span></span>
3.  <span data-ttu-id="25d82-110">Untersuchen Sie jeden Stream in der Datei.</span><span class="sxs-lookup"><span data-stu-id="25d82-110">Examine each stream in the file.</span></span> <span data-ttu-id="25d82-111">Wenn es sich um einen Videostream handelt, erhalten Sie die systemeigenen Dimensionen des Videos.</span><span class="sxs-lookup"><span data-stu-id="25d82-111">If it is a video stream, get the native dimensions of the video.</span></span>
4.  <span data-ttu-id="25d82-112">Rufen Sie einen Poster-Frame ab, der die Suchzeit und die Ziel Dimension angibt.</span><span class="sxs-lookup"><span data-stu-id="25d82-112">Obtain a poster frame, specifying the seek time and the target dimension.</span></span>

<span data-ttu-id="25d82-113">Erstellen Sie das Medien Erkennungs Objekt, indem Sie [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)aufrufen:</span><span class="sxs-lookup"><span data-stu-id="25d82-113">Create the Media Detector object by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):</span></span>


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



<span data-ttu-id="25d82-114">Geben Sie einen Dateinamen an, und verwenden Sie dabei die [**imediadet::p UT \_ -Datei**](imediadet-put-filename.md) namens Methode.</span><span class="sxs-lookup"><span data-stu-id="25d82-114">Specify a file name, using the [**IMediaDet::put\_Filename**](imediadet-put-filename.md) method.</span></span> <span data-ttu-id="25d82-115">Diese Methode nimmt einen **BSTR** -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="25d82-115">This method takes a **BSTR** parameter.</span></span>


```C++
hr = pDet->put_Filename(bstrFilename);
```



<span data-ttu-id="25d82-116">Holen Sie sich die Anzahl der Streams, und durchlaufen Sie jeden Stream, indem Sie den Medientyp überprüfen.</span><span class="sxs-lookup"><span data-stu-id="25d82-116">Get the number of streams, and loop through each stream checking the media type.</span></span> <span data-ttu-id="25d82-117">Die [**imediadet:: get \_ outputstreams**](imediadet-get-outputstreams.md) -Methode ruft die Anzahl der Streams ab, und die [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md) -Methode gibt an, welcher Stream untersucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="25d82-117">The [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) method retrieves the number of streams, and the [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md) method specifies which stream to examine.</span></span> <span data-ttu-id="25d82-118">Beenden Sie die Schleife für den ersten Videostream.</span><span class="sxs-lookup"><span data-stu-id="25d82-118">Exit the loop on the first video stream.</span></span>


```C++
long lStreams;
bool bFound = false;
hr = pDet->get_OutputStreams(&lStreams);
for (long i = 0; i < lStreams; i++)
{
    GUID major_type;
    hr = pDet->put_CurrentStream(i);
    hr = pDet->get_StreamType(&major_type);
    if (major_type == MEDIATYPE_Video)  // Found a video stream.
    {
        bFound = true;
        break;
    }
}
if (!bFound) return VFW_E_INVALIDMEDIATYPE;
```



<span data-ttu-id="25d82-119">Wenn kein Videostream gefunden wurde, wird die Funktion beendet.</span><span class="sxs-lookup"><span data-stu-id="25d82-119">If no video stream was found, the function exits.</span></span>

<span data-ttu-id="25d82-120">Im vorherigen Code gibt die [**imediadet:: get \_ Streamtype**](imediadet-get-streamtype.md) -Methode nur die GUID des Haupt Typs zurück.</span><span class="sxs-lookup"><span data-stu-id="25d82-120">In the previous code, the [**IMediaDet::get\_StreamType**](imediadet-get-streamtype.md) method returns just the major type GUID.</span></span> <span data-ttu-id="25d82-121">Dies ist praktisch, wenn Sie den gesamten Medientyp nicht überprüfen müssen.</span><span class="sxs-lookup"><span data-stu-id="25d82-121">This is convenient if you do not need to examine the complete media type.</span></span> <span data-ttu-id="25d82-122">Um die Video Dimensionen zu erhalten, ist es jedoch notwendig, den Format Block zu untersuchen, sodass der vollständige Medientyp erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="25d82-122">To get the video dimensions, however, it is necessary to examine the format block, so the full media type is needed.</span></span> <span data-ttu-id="25d82-123">Sie können dies abrufen, indem Sie die [**imediadet:: get \_ streammediatype**](imediadet-get-streammediatype.md) -Methode aufrufen, die eine [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur füllt.</span><span class="sxs-lookup"><span data-stu-id="25d82-123">You can retrieve that by calling the [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md) method, which fills in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="25d82-124">Der Medien Detektor konvertiert alle Videodaten Ströme mit einem [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Format Block in ein unkomprimiertes Format.</span><span class="sxs-lookup"><span data-stu-id="25d82-124">The Media Detector converts all video streams into uncompressed format, with a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format block.</span></span>


```C++
long width = 0, height = 0; 
AM_MEDIA_TYPE mt;
hr = pDet->get_StreamMediaType(&mt);
if (mt.formattype == FORMAT_VideoInfo) 
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
    width = pVih->bmiHeader.biWidth;
    height = pVih->bmiHeader.biHeight;
    
    // We want the absolute height, and don't care about up-down orientation.
    if (height < 0) height *= -1;
}
else {
    return VFW_E_INVALIDMEDIATYPE; // This should not happen, in theory.
}
FreeMediaType(mt);
```



<span data-ttu-id="25d82-125">Die [**get \_ streammediatype**](imediadet-get-streammediatype.md) -Methode ordnet den Format Block zu, der vom Aufrufer freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="25d82-125">The [**get\_StreamMediaType**](imediadet-get-streammediatype.md) method allocates the format block, which the caller must free.</span></span> <span data-ttu-id="25d82-126">In diesem Beispiel wird die Funktion " [**fremediatype**](freemediatype.md) " aus der Basisklassen Bibliothek verwendet.</span><span class="sxs-lookup"><span data-stu-id="25d82-126">This example uses the [**FreeMediaType**](freemediatype.md) function from the base class library.</span></span>

<span data-ttu-id="25d82-127">Nun können Sie den Poster-Frame erhalten.</span><span class="sxs-lookup"><span data-stu-id="25d82-127">Now you are ready to get the poster frame.</span></span> <span data-ttu-id="25d82-128">Aufrufen Sie zuerst die [**imediadet:: getbitmapbits**](imediadet-getbitmapbits.md) -Methode mit einem **null** -Zeiger für den Puffer:</span><span class="sxs-lookup"><span data-stu-id="25d82-128">First call the [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) method with a **NULL** pointer for the buffer:</span></span>


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



<span data-ttu-id="25d82-129">Dieser Rückruf gibt die erforderliche Puffergröße im *LSIZE* -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="25d82-129">This call returns the required buffer size in the *lSize* parameter.</span></span> <span data-ttu-id="25d82-130">Der erste Parameter gibt die streamzeit an, nach der gesucht werden soll. in diesem Beispiel wird die Zeit NULL verwendet.</span><span class="sxs-lookup"><span data-stu-id="25d82-130">The first parameter specifies the stream time to seek to; this example uses time zero.</span></span> <span data-ttu-id="25d82-131">Für Breite und Höhe verwendet dieses Beispiel die systemeigenen Video Dimensionen, die Sie zuvor erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="25d82-131">For the width and height, this example uses the native video dimensions obtained earlier.</span></span> <span data-ttu-id="25d82-132">Wenn Sie andere Werte angeben, wird die Bitmap vom Medien Detektor entsprechend gestreckt.</span><span class="sxs-lookup"><span data-stu-id="25d82-132">If you specify other values, the Media Detector will stretch the bitmap to match.</span></span>

<span data-ttu-id="25d82-133">Wenn die Methode erfolgreich ist, weisen Sie den Puffer zu, und wiederholen Sie dann [**getbitmapbits**](imediadet-getbitmapbits.md) :</span><span class="sxs-lookup"><span data-stu-id="25d82-133">If the method succeeds, allocate the buffer and call [**GetBitmapBits**](imediadet-getbitmapbits.md) again:</span></span>


```C++
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[lSize];
    if (!pBuffer) return E_OUTOFMEMORY;
    hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
    if (FAILED(hr))
        delete [] pBuffer;
}
```



<span data-ttu-id="25d82-134">Hier finden Sie die gesamte Funktion, mit einer etwas besseren Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="25d82-134">Here is the complete function, with somewhat better error handling.</span></span>


```C++
HRESULT GetBitmap(LPTSTR pszFileName, BITMAPINFOHEADER** ppbmih)
{
    HRESULT hr;
    CComPtr<IMediaDet> pDet;
    hr = pDet.CoCreateInstance(__uuidof(MediaDet));
    if (FAILED(hr)) return hr;

    // Convert the file name to a BSTR.
    CComBSTR bstrFilename(pszFileName);
    hr = pDet->put_Filename(bstrFilename);
    if (FAILED(hr)) return hr;

    long lStreams;
    bool bFound = false;
    hr = pDet->get_OutputStreams(&lStreams);
    if (FAILED(hr)) return hr;

    for (long i = 0; i < lStreams; i++)
    {
        GUID major_type;
        hr = pDet->put_CurrentStream(i);
        if (SUCCEEDED(hr))
        {
            hr = pDet->get_StreamType(&major_type);
        }
        if (FAILED(hr)) break;

        if (major_type == MEDIATYPE_Video)
        {
            bFound = true;
            break;
        }
    }
    if (!bFound) return VFW_E_INVALIDMEDIATYPE;

    long width = 0, height = 0; 
    AM_MEDIA_TYPE mt;
    hr = pDet->get_StreamMediaType(&mt);
    if (SUCCEEDED(hr)) 
    {
        if ((mt.formattype == FORMAT_VideoInfo) && 
            (mt.cbFormat >= sizeof(VIDEOINFOHEADER)))
        {
            VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
            width = pVih->bmiHeader.biWidth;
            height = pVih->bmiHeader.biHeight;
        
            // We want the absolute height, don't care about orientation.
            if (height < 0) height *= -1;
        }
        else
        {
            hr = VFW_E_INVALIDMEDIATYPE; // Should not happen, in theory.
        }
        FreeMediaType(mt);
    }
    if (FAILED(hr)) return hr;
    
    // Find the required buffer size.
    long size;
    hr = pDet->GetBitmapBits(0, &size, NULL, width, height);
    if (SUCCEEDED(hr)) 
    {
        char *pBuffer = new char[size];
        if (!pBuffer) return E_OUTOFMEMORY;
        try {
            hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
            if (SUCCEEDED(hr))
            {
                // Delete the old image, if any.
                if (*ppbmih) delete[] (*ppbmih);
                (*ppbmih) = (BITMAPINFOHEADER*)pBuffer;
            }
            else
            {
                delete [] pBuffer;
            }
        }
        catch (...) {
            delete [] pBuffer;
            return E_OUTOFMEMORY;
        }
    }
    return hr;
}
```



<span data-ttu-id="25d82-135">Weiter: [Schritt 4: Zeichnen der Bitmap im Client Bereich](step-4--draw-the-bitmap-on-the-client-area.md)</span><span class="sxs-lookup"><span data-stu-id="25d82-135">Next: [Step 4: Draw the Bitmap on the Client Area](step-4--draw-the-bitmap-on-the-client-area.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="25d82-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="25d82-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25d82-137">Ein Poster-Frame wird gepackt.</span><span class="sxs-lookup"><span data-stu-id="25d82-137">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
