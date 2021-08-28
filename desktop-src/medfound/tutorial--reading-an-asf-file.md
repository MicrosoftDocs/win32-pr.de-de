---
description: In diesem Tutorial erfahren Sie, wie Sie Datenpakete aus einer ASF-Datei (Advanced Systems Format) mithilfe des ASF-Splitters erhalten.
ms.assetid: e3a55275-e8f0-4ab7-98db-a2f2c54d5a51
title: 'Tutorial: Lesen einer ASF-Datei mithilfe von WMContainer-Objekten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e456f9e0061be97198623c2422801b5fd9fc196874cd8aa1a467692277319c9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713290"
---
# <a name="tutorial-reading-an-asf-file-by-using-wmcontainer-objects"></a>Tutorial: Lesen einer ASF-Datei mithilfe von WMContainer-Objekten

In diesem Tutorial erfahren Sie, wie Sie Datenpakete aus einer ASF-Datei (Advanced Systems Format) mithilfe des [ASF-Splitters erhalten.](asf-splitter.md) In diesem Tutorial erstellen Sie eine einfache Konsolenanwendung, die eine ASF-Datei liest und komprimierte Medienbeispiele für den ersten Videostream in der Datei generiert. Die Anwendung zeigt Informationen zu den Keyframes im Videostream an.

Folgende Themen werden in diesem Lernprogramm behandelt:

-   [Voraussetzungen](#prerequisites)
-   [1. Einrichten der Project](#1-set-up-the-project)
-   [2. Öffnen einer ASF-Datei](#2-open-an-asf-file)
-   [3. Lesen des ASF-Headerobjekts](#3-read-the-asf-header-object)
-   [4. Erstellen des ASF-Splitters](#4-create-the-asf-splitter)
-   [5. Auswählen eines Datenstroms für die Analyse](#5-select-a-stream-for-parsing)
-   [6. Generieren komprimierter Medienbeispiele](#6-generate-compressed-media-samples)
-   [7. Schreiben der Entry-Point-Funktion](#7-write-the-entry-point-function)
-   [Programmauflistung](#program-listing)
-   [Zugehörige Themen](#related-topics)

Das Tutorial enthält keine Informationen zum Decodieren der komprimierten Daten, die die Anwendung aus dem ASF-Splitter erhält.

## <a name="prerequisites"></a>Voraussetzungen

In diesem Tutorial wird Folgendes vorausgesetzt:

-   Sie sind mit der Struktur einer ASF-Datei und den komponenten vertraut, die von Media Foundation für die Arbeit mit ASF-Objekten bereitgestellt werden. Zu diesen Komponenten gehören das ContentInfo-Objekt, der Splitter, der Multiplexer und das Profil. Weitere Informationen finden Sie unter [WMContainer ASF Components](wmcontainer-asf-components.md).
-   Sie sind mit Medienpuffern und Bytestreams vertraut: insbesondere Dateivorgänge, die einen Bytestream verwenden, aus einem Bytestream in einen Medienpuffer lesen und den Inhalt eines [Medienpuffers](media-buffers.md) in einen Bytestream schreiben.

## <a name="1-set-up-the-project"></a>1. Einrichten der Project

Schließen Sie die folgenden Header in ihre Quelldatei ein:


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>
```



Link zu den folgenden Bibliotheksdateien:

-   mfplat.lib
-   mf.lib
-   mfuuid.lib

Deklarieren [Sie die SafeRelease-Funktion:](saferelease.md)


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="2-open-an-asf-file"></a>2. Öffnen einer ASF-Datei

Öffnen Sie als Nächstes die angegebene Datei, indem Sie die [**MFCreateFile-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) aufrufen. Die -Methode gibt einen Zeiger auf das Bytestreamobjekt zurück, das den Inhalt der Datei enthält. Der Dateiname wird vom Benutzer über Befehlszeilenargumente der Anwendung angegeben.

Der folgende Beispielcode verwendet einen Dateinamen und gibt einen Zeiger auf ein Bytestreamobjekt zurück, das zum Lesen der Datei verwendet werden kann.


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="3-read-the-asf-header-object"></a>3. Lesen des ASF-Headerobjekts

Erstellen Sie als Nächstes das [ASF ContentInfo-Objekt,](asf-contentinfo-object.md) und verwenden Sie es, um das ASF-Headerobjekt der angegebenen Datei zu analysieren. Das ContentInfo-Objekt speichert Informationen aus dem ASF-Header, einschließlich globaler Dateiattribute und Informationen zu jedem Stream. Sie verwenden das ContentInfo-Objekt später im Tutorial, um den ASF-Splitter zu initialisieren und die Streamnummer des Videostreams zu erhalten.

So erstellen Sie das ASF ContentInfo-Objekt:

1.  Rufen Sie die [**MFCreateASFContentInfo-Funktion auf,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) um ein ContentInfo-Objekt zu erstellen. Die -Methode gibt einen Zeiger auf die [**IMFASFContentInfo-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) zurück.
2.  Liest die ersten 30 Bytes von Daten aus der ASF-Datei in einen Medienpuffer.
3.  Übergeben Sie den Medienpuffer an die [**IMFASFContentInfo::GetHeaderSize-Methode.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) Diese Methode gibt die Gesamtgröße des Headerobjekts in der ASF-Datei zurück.
4.  Übergeben Sie den gleichen Medienpuffer an die [**IMFASFContentInfo::P arseHeader-Methode.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader)
5.  Liest den Rest des Headerobjekts in einen neuen Medienpuffer.
6.  Übergeben Sie den zweiten Puffer an die [**ParseHeader-Methode.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) Geben Sie den 30-Byte-Offset im *cbOffsetWithinHeader-Parameter* von **ParseHeader an.** Die **ParseHeader-Methode** initialisiert das ContentInfo-Objekt mit Informationen, die aus den verschiedenen ASF-Objekten erfasst werden, die im Headerobjekt enthalten sind.


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



Diese Funktion verwendet die `ReadFromByteStream` -Funktion, um aus einem Bytestream in einen Medienpuffer zu lesen:


```C++
// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="4-create-the-asf-splitter"></a>4. Erstellen des ASF-Splitters

Erstellen Sie als Nächstes das [ASF-Splitterobjekt.](asf-splitter.md) Sie verwenden den ASF-Splitter, um das ASF-Datenobjekt zu analysieren, das paketierte Mediendaten für die ASF-Datei enthält.

So erstellen Sie ein Splitterobjekt für die ASF-Datei:

1.  Rufen Sie die [**MFCreateASFSplitter-Funktion auf,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) um den ASF-Splitter zu erstellen. Die Funktion gibt einen Zeiger auf die [**IMFASFSplitter-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) zurück.
2.  Rufen [**Sie IMFASFSplitter::Initialize auf, um**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) den ASF-Splitter zu initialisieren. Diese Methode verwendet einen Zeiger auf das ContentInfo-Objekt, das in Prozedur 3 erstellt wurde.


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



## <a name="5-select-a-stream-for-parsing"></a>5. Auswählen eines Datenstroms für die Analyse

Als Nächstes aufzählen Sie die Datenströme in der ASF-Datei, und wählen Sie den ersten Videostream für die Analyse aus. Zum Aufzählen der Streams verwenden Sie ein ASF-Profilobjekt und suchen nach Streams mit einem Videomedientyp.

So wählen Sie den Videostream aus:

1.  Rufen [**Sie IMFASFContentInfo::GetProfile für**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) das ContentInfo-Objekt auf, um ein ASF-Profil zu erstellen. Unter anderem beschreibt das Profil die Streams in der ASF-Datei.
2.  Rufen [**Sie IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) auf, um die Anzahl der Streams in der ASF-Datei zu erhalten.
3.  Rufen [**Sie IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) in einer Schleife auf, um die Streams aufzählen. Die -Methode gibt einen Zeiger auf die [**IMFASFStreamConfig-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) zurück. Außerdem wird der Streambezeichner zurückgegeben.
4.  Rufen [**Sie IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) auf, um die Haupttyp-GUID für den Stream zu erhalten. Wenn die Haupttyp-GUID MFMediaType \_ Video ist, enthält der Stream Video.
5.  Wenn Sie in Schritt 4 einen Videostream gefunden haben, rufen Sie [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) auf, um den Stream auszuwählen. Diese Methode verwendet ein Array von Streambezeichnern. Für dieses Tutorial beträgt die Arraygröße 1, da die Anwendung einen einzelnen Stream analysiert.

Im folgenden Beispielcode werden die Streams in der ASF-Datei aufzählt und der erste Videostream im ASF-Splitter ausgewählt:


```C++
// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}
```



## <a name="6-generate-compressed-media-samples"></a>6. Generieren komprimierter Medienbeispiele

Verwenden Sie als Nächstes den ASF-Splitter, um das ASF-Datenobjekt zu analysieren und die Datenpakete für den ausgewählten Videostream zu erhalten. Die Anwendung liest Daten aus der ASF-Datei in Blöcken fester Größe und übergibt die Daten an den ASF-Splitter. Der Splitter analysiert die Daten und generiert [Medienbeispiele,](media-samples.md) die die komprimierten Videodaten enthalten. Die Anwendung überprüft, ob jedes Beispiel einen Keyframe darstellt. Wenn ja, zeigt die Anwendung einige grundlegende Informationen zum Beispiel an:

-   Anzahl der Medienpuffer
-   Gesamtgröße der Daten
-   Zeitstempel

So generieren Sie komprimierte Medienbeispiele:

1.  Ordnen Sie einen neuen Medienpuffer zu.
2.  Liest Daten aus dem Bytestream in den Medienpuffer.
3.  Übergeben Sie den Medienpuffer an die [**IMFASFSplitter::P arseData-Methode.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) Die -Methode analysiert die ASF-Daten im Puffer.
4.  Rufen Sie in einer Schleife Medienbeispiele aus dem Splitter ab, indem Sie [**IMFASFSplitter::GetNextSample aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) Wenn der *ppISample-Parameter* einen gültigen [**PARSESample-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) empfängt, bedeutet dies, dass der ASF-Splitter mindestens ein Datenpaket analysiert hat. Wenn *ppISample den* Wert **NULL empfängt,** brechen Sie die Schleife ab, und fahren Sie mit Schritt 1 fort.
5.  Zeigt Informationen zum Beispiel an.
6.  Brechen Sie die Schleife unter den folgenden Bedingungen ab:
    -   Der *ppISample-Parameter* empfängt den Wert **NULL.**
    -   Der *pdwStatusFlags-Parameter* erhält nicht das **ASF \_ STATUSFLAGS \_ INCOMPLETE-Flag.**

Wiederholen Sie diese Schritte, bis Sie das Ende der Datei erreichen. Diese Schritte sind im folgenden Code dargestellt:


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



Die IsKeyFrame-Funktion testet, ob ein Beispiel ein Keyframe ist, indem sie den Wert des [**\_ CleanPoint-Attributs MFSampleExtension**](mfsampleextension-cleanpoint-attribute.md) abrufen.


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



Zur Veranschaulichung zeigt dieses Tutorial einige Informationen für jeden Videoschlüsselrahmen an, indem die folgende Funktion aufruft:


```C++
void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}
```



Eine typische Anwendung verwendet die Datenpakete zum Decodieren, Neuverschlüsseln, Senden über das Netzwerk oder eine andere Aufgabe.

## <a name="7-write-the-entry-point-function"></a>7. Schreiben der Entry-Point-Funktion

Nun können Sie die vorherigen Schritte in einer vollständigen Anwendung zusammenbringen. Initialisieren Sie vor der Verwendung Media Foundation -Objekte die Media Foundation-Plattform, indem Sie [**MFStartup aufrufen.**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) Wenn Sie fertig sind, rufen Sie [**MFShutdown auf.**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) Weitere Informationen finden Sie unter [Initialisieren Media Foundation](initializing-media-foundation.md).


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="program-listing"></a>Programmauflistung

Der folgende Code zeigt die vollständige Auflistung für das Tutorial.


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>

#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}


// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 

// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}


// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}

inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}

void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}


// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMContainer-ASF-Komponenten](wmcontainer-asf-components.md)
</dt> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



