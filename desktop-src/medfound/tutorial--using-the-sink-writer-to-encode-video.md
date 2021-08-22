---
description: In diesem Tutorial wird der Sink Writer verwendet, um eine Videodatei zu codieren.
ms.assetid: 3E297366-0863-4E89-A0D5-438CD1FC5AF9
title: 'Tutorial: Verwenden des Senkenwriters zum Codieren von Videos'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5347a82fd40355c8006b15492a59543018ae5868cb02fcefeeb1812bd26930c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972779"
---
# <a name="tutorial-using-the-sink-writer-to-encode-video"></a>Tutorial: Verwenden des Senkenwriters zum Codieren von Videos

In diesem Tutorial wird [der Sink Writer verwendet,](sink-writer.md) um eine Videodatei zu codieren.

## <a name="define-the-video-format"></a>Definieren des Videoformats

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



Diese Konstanten geben die folgenden Parameter des Videoformats an:

-   Framegröße (Breite und Höhe)
-   Frames pro Sekunde.
-   Codierte Bitrate.
-   Codierungsformat, das Windows Media Video 9 (**MFVideoFormat \_ WMV3 ) ist.**
-   Eingabeformat, das 32-Bit-RGB ist.
-   Dauer der Ausgabedatei.

Das Programm verwendet diese Konstanten, um die Medientypen zu erstellen, die das Format beschreiben. In einer echten Anwendung würden Sie in der Regel eine Reihe von Codierungsprofilen unterstützen.

## <a name="create-an-uncompressed-video-frame"></a>Erstellen eines unkomprimierten Videoframes

Der Einfachheit halber wird in diesem Tutorial ein statischer Videoframe als Eingabe verwendet. Der Videoframe enthält ein vollgrünes Rechteck und wird programmgesteuert generiert. Der Videoframe wird in einer globalen Variablen als Array von **DWORD-s** gespeichert:


```C++
// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];
```



Der folgende Code legt jedes Pixel im Frame auf Grün fest:


```C++
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }
```



## <a name="initialize-the-sink-writer"></a>Initialisieren des Senkenwriters

Führen Sie die folgenden Schritte aus, um den Senkenwriter zu initialisieren.

1.  Rufen [**Sie MFCreateSinkWriterFromURL auf,**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) um eine neue Instanz des Senkenwriters zu erstellen.
2.  Erstellen Sie einen Medientyp, der das codierte Video beschreibt.
3.  Übergeben Sie diesen Medientyp an [**die METHODE BESinkWriter::AddStream.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream)
4.  Erstellen Sie einen zweiten Medientyp, der die unkomprimierte Eingabe beschreibt.
5.  Übergeben Sie den unkomprimierten Medientyp an die [**METHODE DURCHSinkWriter::SetInputMediaType.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype)
6.  Rufen Sie [**die METHODE BESinkWriter::BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) auf.
7.  Der Senkenwriter kann jetzt Eingabebeispiele akzeptieren.

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



Die meisten Schritte im vorherigen Codebeispiel sind das Festlegen der Medientypattribute für die beiden Medientypen. Die Details der Medientypen hängen von Ihrem Quellinhalt und dem gewünschten Codierungsprofil ab.

## <a name="send-video-frames-to-the-sink-writer"></a>Senden von Videoframes an den Senkenwriter

Um einen Videoframe an den Senkenwriter zu senden, rufen Sie [**die METHODE VORRINKWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) auf. Die **WriteSample-Methode** verwendet einen Zeiger auf die [**NSSAMPLE-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) die ein *Medienbeispielobjekt* darstellt. Das Medienbeispiel enthält ein *Medienpufferobjekt,* das wiederum einen Zeiger auf den Videoframe enthält. Weitere Informationen zu Medienbeispielen und Puffern finden Sie in den folgenden Themen.

-   [Medienbeispiele](media-samples.md)
-   [Medienpuffer](media-buffers.md)

Abhängig von Ihrer Anwendung können Sie die Medienbeispiele vom [Quellleser erhalten.](source-reader.md) Alternativ können Sie die Medienbeispiele erstellen und die Daten im Puffer direkt bearbeiten. Der folgende Code zeigt den zweiten Ansatz. Er erstellt einen Speicherpuffer und schreibt einen einzelnen Videoframe in den Puffer. Anschließend fügt er diesen Puffer einem Medienbeispiel hinzu und sendet das Medienbeispiel an den Senkenwriter.


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

1.  Rufen [**Sie MFCreateMemoryBuffer auf,**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) um ein Medienpufferobjekt zu erstellen. Diese Funktion weist den Arbeitsspeicher für den Puffer zu.
2.  Rufen [**Sie DIEBMEDIABuffer::Lock auf,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) um den Puffer zu sperren und einen Zeiger auf den Arbeitsspeicher zu erhalten.
3.  Rufen [**Sie MFCopyImage auf,**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) um den Videoframe in den Puffer zu kopieren.
    > [!Note]  
    > In diesem speziellen Beispiel funktioniert **die Verwendung von memcpy** genauso gut. Die [**MFCopyImage-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) verarbeitet jedoch den Fall ordnungsgemäß, in dem der Schritt des Quellimages nicht mit dem Zielpuffer übereinstimmen kann. Weitere Informationen finden Sie unter [Image Stride](image-stride.md).

     

4.  Rufen [**Sie ZUM Entsperren des Puffers DIEMEDIABUFFER::Unlock-Sperre**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) auf.
5.  Rufen [**Sie DIEBMEDIABuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) auf, um die Länge der gültigen Daten im Puffer zu aktualisieren. (Andernfalls wird dieser Wert standardmäßig auf 0 (null) festgelegt.)
6.  Rufen [**Sie MFCreateSample auf,**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) um ein Medienbeispielobjekt zu erstellen.
7.  Rufen [**Sie DEN MEDIENSAMPLE::AddBuffer auf,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) um dem Medienbeispiel den Medienpuffer hinzuzufügen.
8.  Rufen [**Sie DEN TIMESample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) auf, um den Zeitstempel für den Videoframe zu festlegen.
9.  Rufen [**Sie DIEBSAMPLE::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) auf, um die Dauer des Videoframes zu festlegen.
10. Rufen [**Sie DEN BESCHRIFTUNGSinkWriter::WriteSample auf,**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) um das Medienbeispiel an den Senkenwriter zu senden.

## <a name="write-the-main-function"></a>Schreiben der main-Funktion

Führen Sie `main` innerhalb der Funktion die folgenden Schritte aus.

1.  Rufen [**Sie CoInitializeEx auf,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) um die COM-Bibliothek zu initialisieren.
2.  Rufen Sie [**MFStartup auf,**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) um die Microsoft Media Foundation.
3.  Erstellen Sie den Senkenwriter.
4.  Senden von Videoframes an den Senkenwriter
5.  Rufen [**Sie DEN BESCHRIFTUNGSinkWriter::Finalize auf,**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) um die Ausgabedatei zu finalisieren.
6.  Geben Sie den Zeiger auf den Senkenwriter frei.
7.  Rufen Sie [**MFShutdown auf.**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)
8.  Rufen Sie [**CoUninitialize auf.**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)


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

Der folgende Code zeigt das vollständige Programm.


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

[Sink Writer](sink-writer.md)
</dt> </dl>

 

 
