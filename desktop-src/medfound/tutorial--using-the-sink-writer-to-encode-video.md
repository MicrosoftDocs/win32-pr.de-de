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
# <a name="tutorial-using-the-sink-writer-to-encode-video"></a>Tutorial: Verwenden des senkwriter zum Codieren von Videos

In diesem Tutorial wird der [senkwriter](sink-writer.md) verwendet, um eine Videodatei zu codieren.

## <a name="define-the-video-format"></a>Definieren des Video Formats

Der Einfachheit halber wird in diesem Tutorial ein festes Videoformat verwendet, das durch die folgenden Konstanten definiert wird:


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



Diese Konstanten geben die folgenden Parameter des Video Formats an:

-   Frame Größe (Breite und Höhe)
-   Frames pro Sekunde.
-   Codierte Bitrate.
-   Codierungsformat, das Windows Media Video 9 ist (**MF-Format \_ WMV3**).
-   Das Eingabeformat (32-Bit-RGB).
-   Die Dauer der Ausgabedatei.

Das Programm verwendet diese Konstanten, um die Medientypen zu erstellen, die das Format beschreiben. In einer echten Anwendung würden Sie in der Regel eine Reihe von Codierungs Profilen unterstützen.

## <a name="create-an-uncompressed-video-frame"></a>Erstellen eines nicht komprimierten Video Rahmens

Der Einfachheit halber wird in diesem Tutorial ein statischer Videorahmen als Eingabe verwendet. Der Videoframe enthält ein solides grünes Rechteck und wird Programm gesteuert generiert. Der Videoframe wird in einer globalen Variablen als Array von **DWORD** s gespeichert:


```C++
// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];
```



Mit dem folgenden Code wird jedes Pixel im Frame auf grün festgelegt:


```C++
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }
```



## <a name="initialize-the-sink-writer"></a>Initialisieren des Senke Writers

Führen Sie die folgenden Schritte aus, um den Senke-Writer zu initialisieren.

1.  Rufen Sie [**mfkreatesinkschreiterfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) auf, um eine neue Instanz des senkwriter zu erstellen.
2.  Erstellen Sie einen Medientyp, der das codierte Video beschreibt.
3.  Übergeben Sie diesen Medientyp an die [**imfsinkwriter:: addstream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) -Methode.
4.  Erstellen Sie einen zweiten Medientyp, der die nicht komprimierte Eingabe beschreibt.
5.  Übergeben Sie den unkomprimierten Medientyp an die Methode [**imfsinkwriter:: *-putmediatype**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) .
6.  Aufrufen der [**imfsinkwriter:: BeginWrite**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) -Methode.
7.  Der senderwriter ist nun bereit, Eingabe Beispiele zu akzeptieren.

Der folgende Code zeigt diese Schritte.


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



In den meisten Schritten des vorherigen Code Beispiels werden die Medientyp Attribute für die beiden Medientypen festgelegt. Die Details der Medientypen hängen vom Quell Inhalt und dem gewünschten Codierungs Profil ab.

## <a name="send-video-frames-to-the-sink-writer"></a>Video Frames an den senkwriter senden

Um einen Videoframe an den senkwriter zu senden, müssen Sie die [**imfsinkwriter:: schreitesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) -Methode abrufen. Die **beschreitesample** -Methode nimmt einen Zeiger auf die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle an, die ein *Medien Beispiel* Objekt darstellt. Das Medien Beispiel enthält ein *Medien Puffer* Objekt, das wiederum einen Zeiger auf den Videoframe enthält. Weitere Informationen zu Medien Beispielen und Puffern finden Sie in den folgenden Themen.

-   [Medien Beispiele](media-samples.md)
-   [Medien Puffer](media-buffers.md)

Abhängig von Ihrer Anwendung erhalten Sie möglicherweise die Medien Beispiele des [Quell Readers](source-reader.md). Alternativ können Sie die Medien Beispiele erstellen und die Daten im Puffer direkt bearbeiten. Der folgende Code zeigt den zweiten Ansatz. Er erstellt einen Arbeitsspeicher Puffer und schreibt einen einzelnen Videoframe in den Puffer. Anschließend wird dieser Puffer einem Medien Beispiel hinzugefügt, und das Medien Beispiel wird an den Senke-Writer gesendet.


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



Dieser Code führt die folgenden Schritte aus.

1.  Rufen Sie [**mfkreatememorybuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) auf, um ein Medien Puffer Objekt zu erstellen. Mit dieser Funktion wird der Arbeitsspeicher für den Puffer zugewiesen.
2.  Um den Puffer zu sperren und einen Zeiger auf den Speicher zu erhalten, wird [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) aufgerufen.
3.  [**Mfcopyimage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) wird aufgerufen, um den Video Frame in den Puffer zu kopieren.
    > [!Note]  
    > In diesem speziellen Beispiel funktioniert die Verwendung von **memcpy** ebenfalls genauso. Die [**mfcopyimage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) -Funktion behandelt jedoch den Fall, in dem der Stride des Quell Bilds nicht mit dem Ziel Puffer identisch ist, ordnungsgemäß. Weitere Informationen finden Sie unter [Image Stride](image-stride.md).

     

4.  Zum Entsperren des Puffers muss [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) aufgerufen werden.
5.  Aufrufen von [**imfmediabuffer:: setcurrentlength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) zum Aktualisieren der Länge der gültigen Daten im Puffer. (Andernfalls ist dieser Wert standardmäßig auf 0 (null) gesetzt.)
6.  Rufen Sie [**mfkreatesample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) auf, um ein Beispiel Objekt für Medien zu erstellen.
7.  Wenn Sie [**imfsample:: addbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) hinzufügen, fügen Sie dem Medien Beispiel den Medien Puffer hinzu.
8.  Aufrufen von [**imfsample:: setsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) zum Festlegen des Zeitstempels für den Videoframe.
9.  Aufrufen von [**imfsample:: setsampleduration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) , um die Dauer des Video Frames festzulegen.
10. Wenn Sie [**imfsinkwriter:: schreitesample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) aufzurufen, senden Sie das Medien Beispiel an den sendenden Writer.

## <a name="write-the-main-function"></a>Schreiben der Main-Funktion

Führen Sie in der- `main` Funktion die folgenden Schritte aus.

1.  [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen, um die com-Bibliothek zu initialisieren.
2.  [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) wird aufgerufen, um Microsoft Media Foundation zu initialisieren.
3.  Erstellen Sie den Senke-Writer.
4.  Senden von Video Frames an den senkwriter.
5.  Zum Abschließen der Ausgabedatei wird [**imfsink Writer:: Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) aufgerufen.
6.  Geben Sie den Zeiger auf den Senke-Writer frei.
7.  [**Mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)aufruft.
8.  [**CallInitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)aufruft.


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



## <a name="example-code"></a>Beispielcode

Der folgende Code zeigt das gesamte Programm.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Senke-Writer](sink-writer.md)
</dt> </dl>

 

 
