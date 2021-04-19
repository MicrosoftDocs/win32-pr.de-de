---
description: In diesem Tutorial wird der senkwriter verwendet, um eine Videodatei zu codieren.
ms.assetid: 3E297366-0863-4E89-A0D5-438CD1FC5AF9
title: 'Tutorial: Verwenden des senkwriter zum Codieren von Videos'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3e6095355e18db6c8335cadcbc4afc56b35406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348297"
---
# <a name="tutorial-using-the-sink-writer-to-encode-video"></a><span data-ttu-id="3e6e9-103">Tutorial: Verwenden des senkwriter zum Codieren von Videos</span><span class="sxs-lookup"><span data-stu-id="3e6e9-103">Tutorial: Using the Sink Writer to Encode Video</span></span>

<span data-ttu-id="3e6e9-104">In diesem Tutorial wird der [senkwriter](sink-writer.md) verwendet, um eine Videodatei zu codieren.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-104">This tutorial uses the [Sink Writer](sink-writer.md) to encode a video file.</span></span>

## <a name="define-the-video-format"></a><span data-ttu-id="3e6e9-105">Definieren des Video Formats</span><span class="sxs-lookup"><span data-stu-id="3e6e9-105">Define the Video Format</span></span>

<span data-ttu-id="3e6e9-106">Der Einfachheit halber wird in diesem Tutorial ein festes Videoformat verwendet, das durch die folgenden Konstanten definiert wird:</span><span class="sxs-lookup"><span data-stu-id="3e6e9-106">For simplicity, this tutorial uses a fixed video format, defined by the following constants:</span></span>


```C++
// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;
```



<span data-ttu-id="3e6e9-107">Diese Konstanten geben die folgenden Parameter des Video Formats an:</span><span class="sxs-lookup"><span data-stu-id="3e6e9-107">These constants specify the following parameters of the video format:</span></span>

-   <span data-ttu-id="3e6e9-108">Frame Größe (Breite und Höhe)</span><span class="sxs-lookup"><span data-stu-id="3e6e9-108">Frame size (width and height)</span></span>
-   <span data-ttu-id="3e6e9-109">Frames pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-109">Frames per second.</span></span>
-   <span data-ttu-id="3e6e9-110">Codierte Bitrate.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-110">Encoded bit rate.</span></span>
-   <span data-ttu-id="3e6e9-111">Codierungsformat, das Windows Media Video 9 ist (**MF-Format \_ WMV3**).</span><span class="sxs-lookup"><span data-stu-id="3e6e9-111">Encoding format, which is Windows Media Video 9 (**MFVideoFormat\_WMV3**).</span></span>
-   <span data-ttu-id="3e6e9-112">Das Eingabeformat (32-Bit-RGB).</span><span class="sxs-lookup"><span data-stu-id="3e6e9-112">Input format, which is 32-bit RGB.</span></span>
-   <span data-ttu-id="3e6e9-113">Die Dauer der Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-113">Duration of the output file.</span></span>

<span data-ttu-id="3e6e9-114">Das Programm verwendet diese Konstanten, um die Medientypen zu erstellen, die das Format beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-114">The program uses these constants to create the media types that describe the format.</span></span> <span data-ttu-id="3e6e9-115">In einer echten Anwendung würden Sie in der Regel eine Reihe von Codierungs Profilen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-115">In a real application, you would typically support a range of encoding profiles.</span></span>

## <a name="create-an-uncompressed-video-frame"></a><span data-ttu-id="3e6e9-116">Erstellen eines nicht komprimierten Video Rahmens</span><span class="sxs-lookup"><span data-stu-id="3e6e9-116">Create an Uncompressed Video Frame</span></span>

<span data-ttu-id="3e6e9-117">Der Einfachheit halber wird in diesem Tutorial ein statischer Videorahmen als Eingabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-117">Also for simplicity, this tutorial uses a static video frame as input.</span></span> <span data-ttu-id="3e6e9-118">Der Videoframe enthält ein solides grünes Rechteck und wird Programm gesteuert generiert.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-118">The video frame contains a solid green rectangle and is generated programmatically.</span></span> <span data-ttu-id="3e6e9-119">Der Videoframe wird in einer globalen Variablen als Array von **DWORD** s gespeichert:</span><span class="sxs-lookup"><span data-stu-id="3e6e9-119">The video frame is stored in a global variable as an array of **DWORD** s:</span></span>


```C++
// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];
```



<span data-ttu-id="3e6e9-120">Mit dem folgenden Code wird jedes Pixel im Frame auf grün festgelegt:</span><span class="sxs-lookup"><span data-stu-id="3e6e9-120">The following code sets every pixel in the frame to green:</span></span>


```C++
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }
```



## <a name="initialize-the-sink-writer"></a><span data-ttu-id="3e6e9-121">Initialisieren des Senke Writers</span><span class="sxs-lookup"><span data-stu-id="3e6e9-121">Initialize the Sink Writer</span></span>

<span data-ttu-id="3e6e9-122">Führen Sie die folgenden Schritte aus, um den Senke-Writer zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-122">To initialize the sink writer, perform the following steps.</span></span>

1.  <span data-ttu-id="3e6e9-123">Rufen Sie [**mfkreatesinkschreiterfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) auf, um eine neue Instanz des senkwriter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-123">Call [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) to create a new instance of the sink writer.</span></span>
2.  <span data-ttu-id="3e6e9-124">Erstellen Sie einen Medientyp, der das codierte Video beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-124">Create a media type that describes the encoded video.</span></span>
3.  <span data-ttu-id="3e6e9-125">Übergeben Sie diesen Medientyp an die [**imfsinkwriter:: addstream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-125">Pass this media type to the [**IMFSinkWriter::AddStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) method.</span></span>
4.  <span data-ttu-id="3e6e9-126">Erstellen Sie einen zweiten Medientyp, der die nicht komprimierte Eingabe beschreibt.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-126">Create a second media type that describes the uncompressed input.</span></span>
5.  <span data-ttu-id="3e6e9-127">Übergeben Sie den unkomprimierten Medientyp an die Methode [\**imfsinkwriter:: *-putmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) .</span><span class="sxs-lookup"><span data-stu-id="3e6e9-127">Pass the uncompressed media type to the [**IMFSinkWriter::SetInputMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) method.</span></span>
6.  <span data-ttu-id="3e6e9-128">Aufrufen der [**imfsinkwriter:: BeginWrite**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-128">Call the [**IMFSinkWriter::BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) method.</span></span>
7.  <span data-ttu-id="3e6e9-129">Der senderwriter ist nun bereit, Eingabe Beispiele zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-129">The sink writer is now ready to accept input samples.</span></span>

<span data-ttu-id="3e6e9-130">Der folgende Code zeigt diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-130">The following code shows these steps.</span></span>


```C++
HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}
```



<span data-ttu-id="3e6e9-131">In den meisten Schritten des vorherigen Code Beispiels werden die Medientyp Attribute für die beiden Medientypen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-131">Most of the steps in previous code example are setting the media type attributes for the two media types.</span></span> <span data-ttu-id="3e6e9-132">Die Details der Medientypen hängen vom Quell Inhalt und dem gewünschten Codierungs Profil ab.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-132">The details of the media types will depend on your source content and the desired encoding profile.</span></span>

## <a name="send-video-frames-to-the-sink-writer"></a><span data-ttu-id="3e6e9-133">Video Frames an den senkwriter senden</span><span class="sxs-lookup"><span data-stu-id="3e6e9-133">Send Video Frames to the Sink Writer</span></span>

<span data-ttu-id="3e6e9-134">Um einen Videoframe an den senkwriter zu senden, müssen Sie die [**imfsinkwriter:: schreitesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-134">To send a video frame to the sink writer, call the [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method.</span></span> <span data-ttu-id="3e6e9-135">Die **beschreitesample** -Methode nimmt einen Zeiger auf die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle an, die ein *Medien Beispiel* Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-135">The **WriteSample** method takes a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which represents a *media sample* object.</span></span> <span data-ttu-id="3e6e9-136">Das Medien Beispiel enthält ein *Medien Puffer* Objekt, das wiederum einen Zeiger auf den Videoframe enthält.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-136">The media sample contains a *media buffer* object, which in turn contains a pointer to the video frame.</span></span> <span data-ttu-id="3e6e9-137">Weitere Informationen zu Medien Beispielen und Puffern finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-137">For more information about media samples and buffer, see the following topics.</span></span>

-   [<span data-ttu-id="3e6e9-138">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e6e9-138">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="3e6e9-139">Medien Puffer</span><span class="sxs-lookup"><span data-stu-id="3e6e9-139">Media Buffers</span></span>](media-buffers.md)

<span data-ttu-id="3e6e9-140">Abhängig von Ihrer Anwendung erhalten Sie möglicherweise die Medien Beispiele des [Quell Readers](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="3e6e9-140">Depending on your application, you might get the media samples from the [Source Reader](source-reader.md).</span></span> <span data-ttu-id="3e6e9-141">Alternativ können Sie die Medien Beispiele erstellen und die Daten im Puffer direkt bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-141">Alternatively, you can create the media samples and directly manipulate the data in the buffer.</span></span> <span data-ttu-id="3e6e9-142">Der folgende Code zeigt den zweiten Ansatz.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-142">The following code shows the second approach.</span></span> <span data-ttu-id="3e6e9-143">Er erstellt einen Arbeitsspeicher Puffer und schreibt einen einzelnen Videoframe in den Puffer.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-143">It creates a memory buffer and writes a single video frame to the buffer.</span></span> <span data-ttu-id="3e6e9-144">Anschließend wird dieser Puffer einem Medien Beispiel hinzugefügt, und das Medien Beispiel wird an den Senke-Writer gesendet.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-144">Then it adds that buffer to a media sample, and sends the media sample to the sink writer.</span></span>


```C++
HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="3e6e9-145">Dieser Code führt die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-145">This code performs the following steps.</span></span>

1.  <span data-ttu-id="3e6e9-146">Rufen Sie [**mfkreatememorybuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) auf, um ein Medien Puffer Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-146">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer object.</span></span> <span data-ttu-id="3e6e9-147">Mit dieser Funktion wird der Arbeitsspeicher für den Puffer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-147">This function allocates the memory for the buffer.</span></span>
2.  <span data-ttu-id="3e6e9-148">Um den Puffer zu sperren und einen Zeiger auf den Speicher zu erhalten, wird [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-148">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to lock the buffer and get a pointer to the memory.</span></span>
3.  <span data-ttu-id="3e6e9-149">[**Mfcopyimage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) wird aufgerufen, um den Video Frame in den Puffer zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-149">Call [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) to copy the video frame into the buffer.</span></span>
    > [!Note]  
    > <span data-ttu-id="3e6e9-150">In diesem speziellen Beispiel funktioniert die Verwendung von **memcpy** ebenfalls genauso.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-150">In this particular example, using **memcpy** would work just as well.</span></span> <span data-ttu-id="3e6e9-151">Die [**mfcopyimage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) -Funktion behandelt jedoch den Fall, in dem der Stride des Quell Bilds nicht mit dem Ziel Puffer identisch ist, ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-151">However, the [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) function correctly handles the case where the stride of the source image does not match the target buffer.</span></span> <span data-ttu-id="3e6e9-152">Weitere Informationen finden Sie unter [Image Stride](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="3e6e9-152">For more information, see [Image Stride](image-stride.md).</span></span>

     

4.  <span data-ttu-id="3e6e9-153">Zum Entsperren des Puffers muss [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-153">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>
5.  <span data-ttu-id="3e6e9-154">Aufrufen von [**imfmediabuffer:: setcurrentlength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) zum Aktualisieren der Länge der gültigen Daten im Puffer.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-154">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the length of the valid data in the buffer.</span></span> <span data-ttu-id="3e6e9-155">(Andernfalls ist dieser Wert standardmäßig auf 0 (null) gesetzt.)</span><span class="sxs-lookup"><span data-stu-id="3e6e9-155">(Otherwise, this value defaults to zero.)</span></span>
6.  <span data-ttu-id="3e6e9-156">Rufen Sie [**mfkreatesample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) auf, um ein Beispiel Objekt für Medien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-156">Call [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) to create a media sample object.</span></span>
7.  <span data-ttu-id="3e6e9-157">Wenn Sie [**imfsample:: addbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) hinzufügen, fügen Sie dem Medien Beispiel den Medien Puffer hinzu.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-157">Call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) to add the media buffer to the media sample.</span></span>
8.  <span data-ttu-id="3e6e9-158">Aufrufen von [**imfsample:: setsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) zum Festlegen des Zeitstempels für den Videoframe.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-158">Call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) to set the time stamp for the video frame.</span></span>
9.  <span data-ttu-id="3e6e9-159">Aufrufen von [**imfsample:: setsampleduration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) , um die Dauer des Video Frames festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-159">Call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) to set the duration of the video frame.</span></span>
10. <span data-ttu-id="3e6e9-160">Wenn Sie [**imfsinkwriter:: schreitesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) aufzurufen, senden Sie das Medien Beispiel an den sendenden Writer.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-160">Call [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) to send the media sample to the sink writer.</span></span>

## <a name="write-the-main-function"></a><span data-ttu-id="3e6e9-161">Schreiben der Main-Funktion</span><span class="sxs-lookup"><span data-stu-id="3e6e9-161">Write the main Function</span></span>

<span data-ttu-id="3e6e9-162">Führen Sie in der- `main` Funktion die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-162">Inside the `main` function, perform the following steps.</span></span>

1.  <span data-ttu-id="3e6e9-163">[**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen, um die com-Bibliothek zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-163">Call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="3e6e9-164">[**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) wird aufgerufen, um Microsoft Media Foundation zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-164">Call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize Microsoft Media Foundation.</span></span>
3.  <span data-ttu-id="3e6e9-165">Erstellen Sie den Senke-Writer.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-165">Create the sink writer.</span></span>
4.  <span data-ttu-id="3e6e9-166">Senden von Video Frames an den senkwriter.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-166">Send video frames to the sink writer.</span></span>
5.  <span data-ttu-id="3e6e9-167">Zum Abschließen der Ausgabedatei wird [**imfsink Writer:: Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-167">Call [**IMFSinkWriter::Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) to finalize the output file.</span></span>
6.  <span data-ttu-id="3e6e9-168">Geben Sie den Zeiger auf den Senke-Writer frei.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-168">Release the pointer to the sink writer.</span></span>
7.  <span data-ttu-id="3e6e9-169">[**Mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)aufruft.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-169">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>
8.  <span data-ttu-id="3e6e9-170">[**CallInitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)aufruft.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-170">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>


```C++
void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="example-code"></a><span data-ttu-id="3e6e9-171">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="3e6e9-171">Example Code</span></span>

<span data-ttu-id="3e6e9-172">Der folgende Code zeigt das gesamte Programm.</span><span class="sxs-lookup"><span data-stu-id="3e6e9-172">The following code shows the complete program.</span></span>


```C++
#include <Windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <Mfreadwrite.h>
#include <mferror.h>

#pragma comment(lib, "mfreadwrite")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;

// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];

HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}

HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="3e6e9-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3e6e9-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e6e9-174">Senke-Writer</span><span class="sxs-lookup"><span data-stu-id="3e6e9-174">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 
