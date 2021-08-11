---
description: Eine Möglichkeit zum Erstellen einer ASF-Datei besteht darin, ASF-Streams aus einer vorhandenen Datei zu kopieren.
ms.assetid: 158fe3a1-42e6-461d-b56b-5419cd961fca
title: 'Tutorial: Kopieren von ASF-Streams mit WMContainer-Objekten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2149358d216e044f3392b882a997ef4aa455ae799b6ece450bca11f0f22a6781
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237874"
---
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a>Tutorial: Kopieren von ASF-Streams mit WMContainer-Objekten

Eine Möglichkeit zum Erstellen einer ASF-Datei besteht darin, ASF-Streams aus einer vorhandenen Datei zu kopieren. Hierzu können Sie die Mediendaten aus der Quelldatei abrufen und in die Ausgabedatei schreiben. Wenn es sich bei der Quelldatei um eine ASF-Datei handelt, können Sie Streambeispiele kopieren, ohne sie zu dekomprimieren und neu zu dekomprimieren.

In diesem Tutorial wird dieses Szenario veranschaulicht, indem der erste Audiostream aus einer ASF-Audiovideodatei (WMV) extrahiert und in eine neue ASF-Audiodatei (WMA) kopiert wird. In diesem Tutorial erstellen Sie eine Konsolenanwendung, die die Eingabe- und Ausgabedateinamen als Argumente verwendet. Die Anwendung verwendet den ASF-Splitter, um die Eingabestreambeispiele zu analysieren, und sendet sie dann an asf Multiplexer, um die ASF-Datenpakete für den Audiostream zu schreiben.

Folgende Themen werden in diesem Lernprogramm behandelt:

-   [Voraussetzungen](#prerequisites)
-   [Terminologie](#terminology)
-   [1. Einrichten der Project](#1-set-up-the-project)
-   [2. Deklarieren von Hilfsfunktionen](#2-declare-helper-functions)
-   [3. Öffnen der EINGABE-ASF-Datei](#3-open-the-input-asf-file)
-   [4. Initialisieren von Objekten für die Eingabedatei](#4-initialize-objects-for-the-input-file)
-   [5. Erstellen eines Audioprofils](#5-create-an-audio-profile)
-   [6. Initialisieren von Objekten für die Ausgabedatei](#6-initialize-objects-for-the-output-file)
-   [7. Generieren neuer ASF-Datenpakete](#7-generate-new-asf-data-packets)
-   [8. Schreiben der ASF-Objekte in die neue Datei](#8-write-the-asf-objects-in-the-new-file)
-   [9 Schreiben der Entry-Point-Funktion](#9-write-the-entry-point-function)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

In diesem Tutorial wird Folgendes vorausgesetzt:

-   Sie sind mit der Struktur einer ASF-Datei und den von Media Foundation bereitgestellten Komponenten für die Arbeit mit ASF-Objekten vertraut. Zu diesen Komponenten gehören ContentInfo-, Splitter-, Multiplexer- und Profilobjekte. Weitere Informationen finden Sie unter [WMContainer ASF Components](wmcontainer-asf-components.md).
-   Sie sind mit dem Prozess der Analyse des ASF-Headerobjekts und der ASF-Datenpakete einer vorhandenen Datei und dem Generieren komprimierter Datenstrombeispiele mithilfe des Splitters vertraut. Weitere Informationen finden Sie unter [Tutorial: Lesen einer ASF-Datei.](tutorial--reading-an-asf-file.md)
-   Sie sind mit Medienpuffern und Bytestreams vertraut: Insbesondere Dateivorgänge, die einen Bytestream verwenden und den Inhalt eines Medienpuffers in einen Bytestream schreiben. (Siehe [2. Deklarieren von Hilfsfunktionen](#2-declare-helper-functions).)

## <a name="terminology"></a>Begriff

In diesem Tutorial werden die folgenden Begriffe verwendet:

-   Quellbytestream: Bytestreamobjekt, verfügbar macht [**DIE GIGABYTEByteStream-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) die den Inhalt der Eingabedatei enthält.
-   ContentInfo-Quellobjekt: ContentInfo-Objekt, macht die [**IMFASFContentInfo-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) verfügbar, die das ASF-Headerobjekt der Eingabedatei darstellt.
-   Audioprofil: Profilobjekt, macht [**die IMFASFProfile-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) verfügbar, die nur Audiodatenströme der Eingabedatei enthält.
-   Streambeispiel: Medienbeispiel, verfügbar gemacht VON DER Splitter generierte [**SCHNITTSTELLE VONSAMPLE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) stellt die Mediendaten des ausgewählten Streams dar, die aus der Eingabedatei im komprimierten Zustand abgerufen werden.
-   ContentInfo-Ausgabeobjekt: ContentInfo-Objekt, macht die [**IMFASFContentInfo-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) verfügbar, die das ASF-Headerobjekt der Ausgabedatei darstellt.
-   Datenbytedatenstrom: Bytestreamobjekt, verfügbar macht [**DIE GIGABYTEByteStream-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) die den gesamten ASF-Datenobjektteil der Ausgabedatei darstellt.
-   Datenpaket: Medienbeispiel, stellt die VOM Multiplexer generierte [**SCHNITTSTELLE "OPCSample"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) bereit und stellt ein ASF-Datenpaket dar, das in den Daten bytestream geschrieben wird.
-   Ausgabebytestream: Bytestreamobjekt, verfügbar macht [**DIE GIGABYTEByteStream-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) die den Inhalt der Ausgabedatei enthält.

## <a name="1-set-up-the-project"></a>1. Einrichten der Project

Fügen Sie die folgenden Header in Ihre Quelldatei ein:


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



Link zu den folgenden Bibliotheksdateien:

-   mfplat.lib
-   mf.lib
-   mfuuid.lib

Deklarieren Sie die [SafeRelease-Funktion:](saferelease.md)


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



## <a name="2-declare-helper-functions"></a>2. Deklarieren von Hilfsfunktionen

In diesem Tutorial werden die folgenden Hilfsfunktionen zum Lesen und Schreiben aus einem Bytestream verwendet.

Die `AllocReadFromByteStream` Funktion liest Daten aus einem Bytestream und ordnet einen neuen Medienpuffer zu, um die Daten zu speichern. Weitere Informationen finden Sie unter [**GIGABYTEByteStream::Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).


```C++
//-------------------------------------------------------------------
// AllocReadFromByteStream
//
// Reads data from a byte stream and returns a media buffer that
// contains the data.
//-------------------------------------------------------------------

HRESULT AllocReadFromByteStream(
    IMFByteStream *pStream,         // Pointer to the byte stream.
    DWORD cbToRead,                 // Number of bytes to read.
    IMFMediaBuffer **ppBuffer       // Receives a pointer to the media buffer. 
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;
    DWORD cbRead = 0;   // Actual amount of data read.

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer. 
    // This function allocates the memory for the buffer.
    hr = MFCreateMemoryBuffer(cbToRead, &pBuffer);

    // Get a pointer to the memory buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    // Read the data from the byte stream.
    if (SUCCEEDED(hr))
    {
        hr = pStream->Read(pData, cbToRead, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    if (pData)
    {
        pBuffer->Unlock();
    }
    SafeRelease(&pBuffer);
    return hr;
}
```



Die `WriteBufferToByteStream` Funktion schreibt Daten aus einem Medienpuffer in einen Bytestream. Weitere Informationen finden Sie unter [**GIGABYTEByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).


```C++
//-------------------------------------------------------------------
// WriteBufferToByteStream
//
// Writes data from a media buffer to a byte stream.
//-------------------------------------------------------------------

HRESULT WriteBufferToByteStream(
    IMFByteStream *pStream,   // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,  // Pointer to the media buffer.
    DWORD *pcbWritten         // Receives the number of bytes written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbData = 0;
    DWORD cbWritten = 0;
    BYTE *pMem = NULL;

    hr = pBuffer->Lock(&pMem, NULL, &cbData);

    if (SUCCEEDED(hr))
    {
        hr = pStream->Write(pMem, cbData, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        if (pcbWritten)
        {
            *pcbWritten = cbWritten;
        }
    }

    if (pMem)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



Die `AppendToByteStream` Funktion fügt den Inhalt eines Bytestreams an einen anderen an:


```C++
//-------------------------------------------------------------------
// AppendToByteStream
//
// Reads the contents of pSrc and writes them to pDest.
//-------------------------------------------------------------------

HRESULT AppendToByteStream(IMFByteStream *pSrc, IMFByteStream *pDest)
{
    HRESULT hr = S_OK;

    const DWORD READ_SIZE = 1024;

    BYTE buffer[READ_SIZE];

    while (1)
    {
        ULONG cbRead;

        hr = pSrc->Read(buffer, READ_SIZE, &cbRead);

        if (FAILED(hr)) { break; }

        if (cbRead == 0)
        {
            break;
        }

        hr = pDest->Write(buffer, cbRead, &cbRead);

        if (FAILED(hr)) { break; }
    }

    return hr;
}
```



## <a name="3-open-the-input-asf-file"></a>3. Öffnen der EINGABE-ASF-Datei

Öffnen Sie die Eingabedatei, indem Sie die [**MFCreateFile-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) aufrufen. Die -Methode gibt einen Zeiger auf das Bytestreamobjekt zurück, das den Inhalt der Datei enthält. Der Dateiname wird vom Benutzer über Befehlszeilenargumente der Anwendung angegeben.

Der folgende Beispielcode verwendet einen Dateinamen und gibt einen Zeiger auf ein Bytestreamobjekt zurück, das zum Lesen der Datei verwendet werden kann.


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a>4. Initialisieren von Objekten für die Eingabedatei

Als Nächstes erstellen und initialisieren Sie das ContentInfo-Quellobjekt und den Splitter zum Generieren von Streambeispielen.

Dieser in Schritt 2 erstellte Quell-Bytestream wird verwendet, um das ASF-Headerobjekt zu analysieren und das ContentInfo-Quellobjekt aufzufüllen. Dieses Objekt wird verwendet, um den Splitter zu initialisieren, um die Analyse der ASF-Datenpakete für den Audiostream in der Eingabedatei zu vereinfachen. Außerdem rufen Sie die Länge des ASF-Datenobjekts in der Eingabedatei und den Offset zum ersten ASF-Datenpaket relativ zum Anfang der Datei ab. Diese Attribute werden vom Splitter verwendet, um Audiostreambeispiele zu generieren.

So erstellen und initialisieren Sie ASF-Komponenten für die Eingabedatei:

1.  Rufen Sie [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) auf, um das ContentInfo-Objekt zu erstellen. Diese Funktion gibt einen Zeiger auf die [**IMFASFContentInfo-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) zurück.
2.  Rufen Sie [**IMFASFContentInfo::P arseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) auf, um den ASF-Header zu analysieren. Weitere Informationen zu diesem Schritt finden Sie unter [Lesen des ASF-Headerobjekts einer vorhandenen Datei.](reading-the-asf-header-object-of-an-existing-file.md)
3.  Rufen Sie [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) auf, um das ASF-Splitterobjekt zu erstellen. Diese Funktion gibt einen Zeiger auf die [**IMFASFSplitter-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) zurück.
4.  Rufen Sie [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize)auf, und übergeben Sie den [**IMFASFContentInfo-Zeiger.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) Weitere Informationen zu diesem Schritt finden Sie unter [Erstellen des ASF-Splitterobjekts.](creating-the-asf-splitter-object.md)
5.  Rufen Sie [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) auf, um einen Präsentationsdeskriptor für die ASF-Datei abzurufen.
6.  Abrufen des Werts des [**MF \_ PD \_ ASF DATA START \_ \_ \_ OFFSET-Attributs**](mf-pd-asf-data-start-offset-attribute.md) aus dem Präsentationsdeskriptor. Dieser Wert ist der Speicherort des ASF-Datenobjekts in der Datei als Byteoffset vom Anfang der Datei.
7.  Abrufen des Werts des [**MF \_ PD \_ ASF DATA \_ \_ LENGTH-Attributs**](mf-pd-asf-data-length-attribute.md) aus dem Präsentationsdeskriptor. Dieser Wert ist die Gesamtgröße des ASF-Datenobjekts in Bytes. Weitere Informationen finden Sie unter [Abrufen von Informationen aus ASF-Headerobjekten.](getting-information-from-asf-header-objects.md)

Der folgende Beispielcode zeigt eine Funktion, die alle Schritte konsolidiert. Diese Funktion verwendet einen Zeiger auf den Quell-Bytestream und gibt Zeiger auf das ContentInfo-Quellobjekt und den Splitter zurück. Außerdem empfängt er die Länge und offsets zum ASF-Datenobjekt.


```C++
//-------------------------------------------------------------------
// CreateSourceParsers
//
// Creates the ASF splitter and the ASF Content Info object for the 
// source file.
// 
// This function also calulates the offset and length of the ASF 
// Data Object.
//-------------------------------------------------------------------

HRESULT CreateSourceParsers(
    IMFByteStream *pSourceStream,
    IMFASFContentInfo **ppSourceContentInfo,
    IMFASFSplitter **ppSplitter,
    UINT64 *pcbDataOffset,
    UINT64 *pcbDataLength
    )
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;

    IMFMediaBuffer *pBuffer = NULL;
    IMFPresentationDescriptor *pPD = NULL;
    IMFASFContentInfo *pSourceContentInfo = NULL;
    IMFASFSplitter *pSplitter = NULL;

    QWORD cbHeader = 0;

    /*------- Parse the ASF header. -------*/

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pSourceContentInfo);
    
    // Read the first 30 bytes to find the total header size.
    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            MIN_ASF_HEADER_SIZE, 
            &pBuffer
            );
    }

    // Get the header size.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Release the buffer; we will reuse it.
    SafeRelease(&pBuffer);
    
    // Read the entire header into a buffer.
    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(0);
    }

    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            (DWORD)cbHeader, 
            &pBuffer
            );
    }

    // Parse the buffer and populate the header object.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->ParseHeader(pBuffer, 0);
    }

    /*------- Initialize the ASF splitter. -------*/

    // Create the splitter.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFSplitter(&pSplitter);
    }
    
    // initialize the splitter with the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pSourceContentInfo);
    }


    /*------- Get the offset and size of the ASF Data Object. -------*/

    // Generate the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr =  pSourceContentInfo->GeneratePresentationDescriptor(&pPD);
    }

    // Get the offset to the start of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_START_OFFSET, pcbDataOffset);
    }

    // Get the length of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_LENGTH, pcbDataLength);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSourceContentInfo = pSourceContentInfo;
        (*ppSourceContentInfo)->AddRef();

        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();

    }

    SafeRelease(&pPD);
    SafeRelease(&pBuffer);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSplitter);

    return S_OK;
}
```



## <a name="5-create-an-audio-profile"></a>5. Erstellen eines Audioprofils

Als Nächstes erstellen Sie ein Profilobjekt für die Eingabedatei, indem Sie es aus dem ContentInfo-Quellobjekt abrufen. Anschließend konfigurieren Sie das Profil so, dass es nur die Audiodatenströme der Eingabedatei enthält. Dazu müssen Sie die Datenströme aufzählen und Nicht-Audiostreams aus dem Profil entfernen. Das Audioprofilobjekt wird später in diesem Tutorial verwendet, um das ContentInfo-Ausgabeobjekt zu initialisieren.

So erstellen Sie ein Audioprofil

1.  Rufen Sie das Profilobjekt für die Eingabedatei aus dem ContentInfo-Quellobjekt ab, indem [**Sie IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)aufrufen. Die -Methode gibt einen Zeiger auf ein Profilobjekt zurück, das alle Datenströme in der Eingabedatei enthält. Weitere Informationen finden Sie unter [Erstellen eines ASF-Profils.](creating-an-asf-profile.md)
2.  Entfernen Sie alle gegenseitigen Ausschlussobjekte aus dem Profil. Dieser Schritt ist erforderlich, da Nicht-Audiostreams aus dem Profil entfernt werden, wodurch die objekte für gegenseitigen Ausschluss ungültig werden können.
3.  Entfernen Sie alle Nicht-Audiostreams wie folgt aus dem Profil:
    -   Rufen Sie [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) auf, um die Anzahl der Streams abzurufen.
    -   Rufen Sie in einer Schleife [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) auf, um jeden Stream nach Index abzurufen.
    -   Rufen Sie [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) auf, um den Streamtyp abzurufen.
    -   Rufen Sie für Nicht-Audiostreams [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) auf, um den Stream zu entfernen.
4.  Store die Streamnummer des ersten Audiostreams. Dies wird im Splitter ausgewählt, um Streambeispiele zu generieren. Wenn die Streamnummer 0 (null) ist, kann der Aufrufer davon ausgehen, dass keine Audiostreamdatei vor sich liegt.

Im folgenden Code werden diese Schritte beschrieben:


```C++
//-------------------------------------------------------------------
// GetAudioProfile
//
// Gets the ASF profile from the source file and removes any video
// streams from the profile.
//-------------------------------------------------------------------

HRESULT GetAudioProfile(
    IMFASFContentInfo *pSourceContentInfo, 
    IMFASFProfile **ppAudioProfile, 
    WORD *pwSelectStreamNumber
    )
{
    IMFASFStreamConfig *pStream = NULL;
    IMFASFProfile *pProfile = NULL;

    DWORD dwTotalStreams = 0;
    WORD  wStreamNumber = 0; 
    GUID guidMajorType = GUID_NULL;
    
    // Get the profile object from the source ContentInfo object.
    HRESULT hr = pSourceContentInfo->GetProfile(&pProfile);

    // Remove mutexes from the profile
    if (SUCCEEDED(hr))
    {
        hr = RemoveMutexes(pProfile);
    }

    // Get the total number of streams on the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&dwTotalStreams);
    }

    // Enumerate the streams and remove the non-audio streams.
    if (SUCCEEDED(hr))
    {
        for (DWORD index = 0; index < dwTotalStreams; )
        {
            hr = pProfile->GetStream(index, &wStreamNumber, &pStream);

            if (FAILED(hr)) { break; }

            hr = pStream->GetStreamType(&guidMajorType);

            SafeRelease(&pStream);

            if (FAILED(hr)) { break; }

            if (guidMajorType != MFMediaType_Audio)
            {
                hr = pProfile->RemoveStream(wStreamNumber);
    
                if (FAILED(hr)) { break; }

                index = 0;
                dwTotalStreams--;
            }
            else
            {
                // Store the first audio stream number. 
                // This will be selected on the splitter.

                if (*pwSelectStreamNumber == 0)
                {
                    *pwSelectStreamNumber = wStreamNumber;
                }

                index++;
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppAudioProfile = pProfile;
        (*ppAudioProfile)->AddRef();
    }

    SafeRelease(&pStream);
    SafeRelease(&pProfile);

    return S_OK;
}
```



Die `RemoveMutexes` Funktion entfernt alle Objekte für gegenseitigen Ausschluss aus dem Profil:


```C++
HRESULT RemoveMutexes(IMFASFProfile *pProfile)
{
    DWORD cMutex = 0;
    HRESULT hr = pProfile->GetMutualExclusionCount(&cMutex);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cMutex; i++)
        {
            hr = pProfile->RemoveMutualExclusion(0);

            if (FAILED(hr))
            {
                break;
            }
        }
    }

    return hr;
}
```



## <a name="6-initialize-objects-for-the-output-file"></a>6. Initialisieren von Objekten für die Ausgabedatei

Als Nächstes erstellen Sie das ContentInfo-Ausgabeobjekt und den Multiplexer zum Generieren von Datenpaketen für die Ausgabedatei.

Das in Schritt 4 erstellte Audioprofil wird zum Auffüllen des ContentInfo-Ausgabeobjekts verwendet. Dieses Objekt enthält Informationen wie globale Dateiattribute und Streameigenschaften. Das ContentInfo-Ausgabeobjekt wird verwendet, um den Multiplexer zu initialisieren, der Datenpakete für die Ausgabedatei generiert. Nachdem die Datenpakete generiert wurden, muss das ContentInfo-Objekt aktualisiert werden, um die neuen Werte widerzufiltern.

So erstellen und initialisieren Sie ASF-Komponenten für die Ausgabedatei

1.  Erstellen Sie ein leeres ContentInfo-Objekt, indem Sie [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) aufrufen, und füllen Sie es mit Informationen aus dem in Schritt 3 erstellten Audioprofil auf, indem Sie [**IMFASFContentInfo::SetProfile aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) Weitere Informationen finden Sie unter [Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei.](initializing-the-contentinfo-object-of-a-new-asf-file.md)
2.  Erstellen und initialisieren Sie das Multiplexer-Objekt mithilfe des ContentInfo-Ausgabeobjekts. Weitere Informationen finden Sie unter [Erstellen des Multiplexer-Objekts.](creating-the-multiplexer-object.md)

Der folgende Beispielcode zeigt eine Funktion, die die Schritte konsolidiert. Diese Funktion verwendet einen Zeiger auf ein Profilobjekt und gibt Zeiger auf das ContentInfo-Ausgabeobjekt und den Multiplexer zurück.


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a>7. Generieren neuer ASF-Datenpakete

Als Nächstes generieren Sie Audiostreambeispiele aus dem Quell-Bytestream mithilfe des Splitters und senden sie an den Multiplexer, um ASF-Datenpakete zu erstellen. Diese Datenpakete bilden das endgültige ASF-Datenobjekt für die neue Datei.

So generieren Sie Audiostreambeispiele

1.  Wählen Sie den ersten Audiostream im Splitter aus, indem Sie [**IMFASFSplitter::SelectStreams aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams)
2.  Liest Blöcke von Mediendaten fester Größe aus dem Quell-Bytestream in einen Medienpuffer.
3.  Sammeln Sie die Streambeispiele als Medienbeispiele aus dem Splitter, indem Sie [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in einer Schleife aufrufen, solange das FLAG ASF \_ STATUSFLAGS INCOMPLETE im parameter \_ *pdwStatusFlags* empfangen wird. Weitere Informationen finden Sie unter Generieren von Beispielen für ASF-Datenpakete" unter [Generieren von Streambeispielen aus einem vorhandenen ASF-Datenobjekt.](generating-stream-samples-from-an-existing-asf-data-object.md)
4.  Rufen Sie für jedes Medienbeispiel [**IMFASFMultiplexer::P rocessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) auf, um das Medienbeispiel an den Multiplexer zu senden. Der Multiplexer generiert die Datenpakete für das ASF-Datenobjekt.
5.  Schreiben Sie das vom Multiplexer generierte Datenpaket in den Daten bytestream.
6.  Nachdem alle Datenpakete generiert wurden, rufen Sie [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) auf, um das ContentInfo-Ausgabeobjekt mit Informationen zu aktualisieren, die während der ASF-Datenpaketgenerierung gesammelt wurden.

Der folgende Beispielcode generiert Streambeispiele aus dem ASF-Splitter und sendet sie an den Multiplexer. Der Multiplexer generiert ASF-Datenpakete und schreibt sie in einen Stream.


```C++
//-------------------------------------------------------------------
// GenerateASFDataObject
// 
// Creates a byte stream that contains the ASF Data Object for the
// output file.
//-------------------------------------------------------------------

HRESULT GenerateASFDataObject(
    IMFByteStream *pSourceStream, 
    IMFASFSplitter *pSplitter, 
    IMFASFMultiplexer *pMux, 
    UINT64   cbDataOffset,
    UINT64   cbDataLength,
    IMFByteStream **ppDataStream
    )
{
    IMFMediaBuffer *pBuffer = NULL;
    IMFByteStream *pDataStream = NULL;
    
    const DWORD READ_SIZE = 1024 * 4;

    // Flush the splitter to remove any pending samples.
    HRESULT hr = pSplitter->Flush();

    if (SUCCEEDED(hr))
    {
        hr = MFCreateTempFile(
            MF_ACCESSMODE_READWRITE, 
            MF_OPENMODE_DELETE_IF_EXIST,
            MF_FILEFLAGS_NONE,
            &pDataStream
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(cbDataOffset);
    }

    if (SUCCEEDED(hr))
    {
        while (cbDataLength > 0)
        {
            DWORD cbRead = min(READ_SIZE, (DWORD)cbDataLength);

            hr = AllocReadFromByteStream(
                pSourceStream, 
                cbRead, 
                &pBuffer
                );

            if (FAILED(hr)) 
            { 
                break; 
            }

            cbDataLength -= cbRead;

            // Push data on the splitter.
            hr =  pSplitter->ParseData(pBuffer, 0, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            // Get ASF packets from the splitter and feed them to the mux.
            hr = GetPacketsFromSplitter(pSplitter, pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }

            SafeRelease(&pBuffer);
        }
    }

    // Flush the mux and generate any remaining samples.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Flush();
    }

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataPackets(pMux, pDataStream);
    }

     // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppDataStream = pDataStream;
        (*ppDataStream)->AddRef();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pDataStream);
    return hr;
}
```



Um Pakete aus dem ASF-Splitter zu erhalten, ruft der vorherige Code die `GetPacketsFromSplitter` -Funktion auf, wie hier gezeigt:


```C++
//-------------------------------------------------------------------
// GetPacketsFromSplitter
//
// Gets samples from the ASF splitter.
//
// This function is called after calling IMFASFSplitter::ParseData.
//-------------------------------------------------------------------

HRESULT GetPacketsFromSplitter(
    IMFASFSplitter *pSplitter,
    IMFASFMultiplexer *pMux,
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;
    DWORD   dwStatus = ASF_STATUSFLAGS_INCOMPLETE;
    WORD    wStreamNum = 0;

    IMFSample *pSample = NULL;

    while (dwStatus & ASF_STATUSFLAGS_INCOMPLETE) 
    {
        hr = pSplitter->GetNextSample(&dwStatus, &wStreamNum, &pSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pSample)
        {
            //Send to the multiplexer to convert it into ASF format
            hr = pMux->ProcessSample(wStreamNum, pSample, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            hr = GenerateASFDataPackets(pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }
        }

        SafeRelease(&pSample);
    }

    SafeRelease(&pSample);
    return hr;
}
```



Die `GenerateDataPackets` Funktion ruft Datenpakete aus multiplexer ab. Weitere Informationen finden Sie unter [Abrufen von ASF-Datenpaketen.](generating-new-asf-data-packets.md)


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



## <a name="8-write-the-asf-objects-in-the-new-file"></a>8. Schreiben der ASF-Objekte in die neue Datei

Als Nächstes schreiben Sie den Inhalt des ContentInfo-Ausgabeobjekts in einen Medienpuffer, indem Sie [**IMFASFContentInfo::GenerateHeader aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) Diese Methode konvertiert im ContentInfo-Objekt gespeicherte Daten in Binärdaten im ASF-Headerobjektformat. Weitere Informationen finden Sie unter [Generieren eines neuen ASF-Headerobjekts.](generating-a-new-asf-header-object.md)

Nachdem das neue ASF-Headerobjekt generiert wurde, schreiben Sie die Ausgabedatei, indem Sie zunächst das Headerobjekt in den Ausgabebytestream schreiben, der in Schritt 2 erstellt wurde, indem Sie die Hilfsfunktion WriteBufferToByteStream aufrufen. Folgen Sie dem Header-Objekt mit dem Datenobjekt, das im Daten bytestream enthalten ist. Der Beispielcode zeigt eine Funktion, die Inhalte des Datenbytestreams in den Ausgabebytestream überträgt.


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="9-write-the-entry-point-function"></a>9 Schreiben der Entry-Point-Funktion

Nun können Sie die vorherigen Schritte in einer vollständigen Anwendung zusammenbringen. Initialisieren Sie die Media Foundation, bevor Sie eines der Media Foundation-Objekte verwenden, indem Sie [**MFStartup aufrufen.**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) Wenn Sie fertig sind, rufen Sie [**MFShutdown auf.**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) Weitere Informationen finden Sie unter [Initialisieren Media Foundation](initializing-media-foundation.md).

Der folgende Code zeigt die vollständige Konsolenanwendung. Das Befehlszeilenargument gibt den Namen der zu konvertierenden Datei und den Namen der neuen Audiodatei an.


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma\n");
        return 0;
    }

    HRESULT hr = MFStartup(MF_VERSION);

    if (FAILED(hr))
    {
        wprintf_s(L"MFStartup failed: 0x%X\n", hr);
        return 0;
    }

    PCWSTR pszInputFile = argv[1];      
    PCWSTR pszOutputFile = argv[2];     
    
    IMFByteStream      *pSourceStream = NULL;       
    IMFASFContentInfo  *pSourceContentInfo = NULL;  
    IMFASFProfile      *pAudioProfile = NULL;       
    IMFASFContentInfo  *pOutputContentInfo = NULL;  
    IMFByteStream      *pDataStream = NULL;         
    IMFASFSplitter     *pSplitter = NULL;           
    IMFASFMultiplexer  *pMux = NULL;                

    UINT64  cbDataOffset = 0;           
    UINT64  cbDataLength = 0;           
    WORD    wSelectStreamNumber = 0;    

    // Open the input file.

    hr = OpenFile(pszInputFile, &pSourceStream);

    // Initialize the objects that will parse the source file.

    if (SUCCEEDED(hr))
    {
        hr = CreateSourceParsers(
            pSourceStream, 
            &pSourceContentInfo,    // ASF Header for the source file.
            &pSplitter,             // Generates audio samples.
            &cbDataOffset,          // Offset to the first data packet.
            &cbDataLength           // Length of the ASF Data Object.
            );
    }

    // Create a profile object for the audio streams in the source file.

    if (SUCCEEDED(hr))
    {
        hr = GetAudioProfile(
            pSourceContentInfo, 
            &pAudioProfile,         // ASF profile for the audio stream.
            &wSelectStreamNumber    // Stream number of the first audio stream.
            );
    }

    // Initialize the objects that will generate the output data.

    if (SUCCEEDED(hr))
    {
        hr = CreateOutputGenerators(
            pAudioProfile, 
            &pOutputContentInfo,    // ASF Header for the output file.
            &pMux                   // Generates ASF data packets.
            );
    }

    // Set up the splitter to generate samples for the first
    // audio stream in the source media.

    if (SUCCEEDED(hr))
    {
        hr = pSplitter->SelectStreams(&wSelectStreamNumber, 1);
    }
    
    // Generate ASF Data Packets and store them in a byte stream.

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataObject(
               pSourceStream, 
               pSplitter, 
               pMux, 
               cbDataOffset, 
               cbDataLength, 
               &pDataStream    // Byte stream for the ASF data packets.    
               );
    }

    // Update the header with new information if any.

    if (SUCCEEDED(hr))
    {
        hr = pMux->End(pOutputContentInfo);
    }

    //Write the ASF objects to the output file
    if (SUCCEEDED(hr))
    {
        hr = WriteASFFile(pOutputContentInfo, pDataStream, pszOutputFile);
    }

    // Clean up.
    SafeRelease(&pMux);
    SafeRelease(&pSplitter);
    SafeRelease(&pDataStream);
    SafeRelease(&pOutputContentInfo);
    SafeRelease(&pAudioProfile);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSourceStream);

    MFShutdown();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the audio file: 0x%X\n", hr);
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

 

 



