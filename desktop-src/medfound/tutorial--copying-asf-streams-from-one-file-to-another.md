---
description: Eine Möglichkeit zum Erstellen einer ASF-Datei besteht darin, die ASF-Streams aus einer vorhandenen Datei zu kopieren.
ms.assetid: 158fe3a1-42e6-461d-b56b-5419cd961fca
title: 'Tutorial: Kopieren von ASF-Streams mithilfe von wmcontainer-Objekten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44bac13626a8c80f474eeb029db4eb1351273910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343423"
---
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a>Tutorial: Kopieren von ASF-Streams mithilfe von wmcontainer-Objekten

Eine Möglichkeit zum Erstellen einer ASF-Datei besteht darin, die ASF-Streams aus einer vorhandenen Datei zu kopieren. Zu diesem Zweck können Sie die Mediendaten aus der Quelldatei abrufen und in die Ausgabedatei schreiben. Wenn die Quelldatei eine ASF-Datei ist, können Sie streambeispiele kopieren, ohne Sie zu dekomprimieren und erneut zu komprimieren.

In diesem Tutorial wird dieses Szenario veranschaulicht, indem der erste Audiostream aus einer ASF-audiovideodatei (. wmv) extrahiert und in eine neue ASF-Audiodatei (. WMA) kopiert wird. In diesem Tutorial erstellen Sie eine Konsolenanwendung, die die Eingabe-und Ausgabe Dateinamen als Argumente annimmt. Die Anwendung verwendet den ASF-Splitter, um die eingabestreambeispiele zu analysieren, und sendet Sie dann an den ASF Multiplexer, um die ASF-Datenpakete für den Audiostream zu schreiben.

Folgende Themen werden in diesem Lernprogramm behandelt:

-   [Voraussetzungen](#prerequisites)
-   [Terminologie](#terminology)
-   [1. richten Sie das Projekt ein.](#1-set-up-the-project)
-   [2. Deklarieren von Hilfsfunktionen](#2-declare-helper-functions)
-   [3. Öffnen Sie die Eingabe-ASF-Datei.](#3-open-the-input-asf-file)
-   [4. Initialisieren von Objekten für die Eingabedatei](#4-initialize-objects-for-the-input-file)
-   [5. Erstellen eines audioprofils](#5-create-an-audio-profile)
-   [6. Initialisieren von Objekten für die Ausgabedatei](#6-initialize-objects-for-the-output-file)
-   [7. Generieren neuer ASF-Datenpakete](#7-generate-new-asf-data-packets)
-   [8. Schreiben der ASF-Objekte in der neuen Datei](#8-write-the-asf-objects-in-the-new-file)
-   [9 Schreiben der Entry-Point-Funktion](#9-write-the-entry-point-function)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

In diesem Tutorial wird Folgendes vorausgesetzt:

-   Sie sind mit der Struktur einer ASF-Datei und den von Media Foundation bereitgestellten Komponenten vertraut, um mit der Verwendung von ASF-Objekten zu arbeiten. Zu diesen Komponenten gehören ContentInfo-, Splitter-, Multiplexer-und Profile-Objekte. Weitere Informationen finden Sie unter [wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md).
-   Sie kennen den Prozess der Verarbeitung des ASF-Header Objekts und der ASF-Datenpakete einer vorhandenen Datei und das Erstellen von komprimierten streambeispielen mithilfe des Splitters. Weitere Informationen finden Sie unter [Tutorial: Lesen einer ASF-Datei](tutorial--reading-an-asf-file.md).
-   Sie sind mit Medien Puffern und Bytestreams vertraut: insbesondere Datei Vorgänge mit einem Bytestream und das Schreiben des Inhalts eines Medien Puffers in einen Bytestream. (Siehe [2. Deklarieren von Hilfsfunktionen](#2-declare-helper-functions).)

## <a name="terminology"></a>Begriff

In diesem Tutorial werden die folgenden Begriffe verwendet:

-   Quelle-Byte-Stream: das [**bytestreamobjekt macht die IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Schnittstelle verfügbar, die den Inhalt der Eingabedatei enthält.
-   Quell-ContentInfo-Objekt: das ContentInfo-Objekt macht die [**imfasf ContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Schnittstelle verfügbar, die das ASF-Header Objekt der Eingabedatei darstellt.
-   Audioprofil: Profil Objekt macht die [**imfasf profile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) -Schnittstelle verfügbar, die nur Audiostreams der Eingabedatei enthält.
-   Stream Sample: Media Sample, macht eine [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle verfügbar, die vom Splitter generiert wurde, stellt die Mediendaten des ausgewählten Streams dar, die aus der Eingabedatei im komprimierten Zustand abgerufen wurden.
-   Output ContentInfo Object: das ContentInfo-Objekt macht die [**imfasf ContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Schnittstelle verfügbar, die das ASF-Header Objekt der Ausgabedatei darstellt.
-   Daten Byte Datenstrom: das [**bytestreamobjekt macht die IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Schnittstelle verfügbar, die den gesamten Teil des ASF-Datenobjekts der Ausgabedatei darstellt.
-   Data Packet: Media Sample, macht die von Multiplexer generierte [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle und stellt ein ASF-Datenpaket dar, das in den datenbytestream geschrieben wird.
-   Ausgabe Byte Datenstrom: das Byte Datenstrom Objekt macht die [**IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Schnittstelle verfügbar, die den Inhalt der Ausgabedatei enthält.

## <a name="1-set-up-the-project"></a>1. richten Sie das Projekt ein.

Fügen Sie die folgenden Header in die Quelldatei ein:


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



Verknüpfen Sie die folgenden Bibliotheksdateien:

-   MF. lib
-   MF. lib
-   mfuuid. lib

Deklarieren Sie die [saferelease](saferelease.md) -Funktion:


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

In diesem Tutorial werden die folgenden Hilfsfunktionen verwendet, um aus einem Bytestream zu lesen und zu schreiben.

Die `AllocReadFromByteStream` -Funktion liest Daten aus einem Bytestream und weist einen neuen Medien Puffer zum Speichern der Daten zu. Weitere Informationen finden Sie unter [**IMF Bytestream:: Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).


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



Die- `WriteBufferToByteStream` Funktion schreibt Daten aus einem Medien Puffer in einen Bytestream. Weitere Informationen finden Sie unter [**IMF Bytestream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).


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



Die- `AppendToByteStream` Funktion fügt den Inhalt eines Bytestreams an einen anderen an:


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



## <a name="3-open-the-input-asf-file"></a>3. Öffnen Sie die Eingabe-ASF-Datei.

Öffnen Sie die Eingabedatei, indem Sie die [**mfcreatefile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) -Funktion aufrufen. Die-Methode gibt einen Zeiger auf das bytestreamobjekt zurück, das den Inhalt der Datei enthält. Der Dateiname wird vom Benutzer über Befehlszeilenargumente der Anwendung angegeben.

Im folgenden Beispielcode wird ein Dateiname verwendet, und es wird ein Zeiger auf ein bytestreamobjekt zurückgegeben, das zum Lesen der Datei verwendet werden kann.


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a>4. Initialisieren von Objekten für die Eingabedatei

Als Nächstes erstellen und initialisieren Sie das Quell-ContentInfo-Objekt und den Splitter zum Erstellen von streambeispielen.

Dieser in Schritt 2 erstellte Quell Byte Datenstrom wird verwendet, um das ASF-Header Objekt zu analysieren und das Quell-ContentInfo-Objekt aufzufüllen. Dieses Objekt wird verwendet, um den Splitter zu initialisieren, um die Analyse der ASF-Datenpakete für den Audiostream in der Eingabedatei zu vereinfachen. Außerdem rufen Sie die Länge des ASF-Datenobjekts in der Eingabedatei und den Offset zum ersten Paket der ASF-Daten in Relation zum Anfang der Datei ab. Diese Attribute werden vom Splitter verwendet, um audiostreambeispiele zu generieren.

So erstellen und initialisieren Sie die ASF-Komponenten für die Eingabedatei:

1.  Rufen Sie [**mfkreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) auf, um das ContentInfo-Objekt zu erstellen. Diese Funktion gibt einen Zeiger auf die [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Schnittstelle zurück.
2.  [**Imfasfcontentinfo::P arsheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) zum Analysieren des ASF-Headers aufzurufen. Weitere Informationen zu diesem Schritt finden Sie unter [Lesen des ASF-Header Objekts einer vorhandenen Datei](reading-the-asf-header-object-of-an-existing-file.md).
3.  Rufen Sie [**mfkreateasfsplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) auf, um das ASF-Splitter Objekt zu erstellen. Diese Funktion gibt einen Zeiger auf die [**imfasfsplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) -Schnittstelle zurück.
4.  Nennen Sie [**imfasfsplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), und übergeben Sie den [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)-Zeiger. Weitere Informationen zu diesem Schritt finden Sie unter [Erstellen des ASF-Splitter Objekts](creating-the-asf-splitter-object.md).
5.  Aufrufen von [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) , um einen Präsentations Deskriptor für die ASF-Datei zu erhalten.
6.  Sie erhalten den Wert des MF-Attribut " [**MF \_ PD \_ ASF \_ Data \_ Start \_ Offset**](mf-pd-asf-data-start-offset-attribute.md) " aus dem Präsentations Deskriptor. Dieser Wert ist der Speicherort des ASF-Datenobjekts in der Datei, als Byte-Offset vom Anfang der Datei.
7.  Den Wert des [**\_ \_ \_ Daten \_ Längen**](mf-pd-asf-data-length-attribute.md) Attributs der MF-PD-Datei aus dem Präsentations Deskriptor erhalten. Dieser Wert ist die Gesamtgröße des ASF-Datenobjekts in Bytes. Weitere Informationen finden Sie unter [erhalten von Informationen aus den ASF-Header Objekten](getting-information-from-asf-header-objects.md).

Der folgende Beispielcode zeigt eine Funktion, die alle Schritte konsolidiert. Diese Funktion nimmt einen Zeiger auf den Quell Byte Datenstrom und gibt Zeiger auf das Quell-ContentInfo-Objekt und den Splitter zurück. Außerdem erhält Sie die Länge und die Offsets für das ASF-Datenobjekt.


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



## <a name="5-create-an-audio-profile"></a>5. Erstellen eines audioprofils

Als Nächstes erstellen Sie ein Profil Objekt für die Eingabedatei, indem Sie es aus dem ContentInfo-Quell Objekt abrufen. Anschließend konfigurieren Sie das Profil so, dass es nur die Audiostreams der Eingabedatei enthält. Auflisten Sie zu diesem Zweck die Streams, und entfernen Sie nicht-Audiodatenströme aus dem Profil. Das audioprofilobjekt wird später in diesem Tutorial verwendet, um das ContentInfo-Ausgabe Objekt zu initialisieren.

So erstellen Sie ein Audioprofil

1.  Rufen Sie das Profil Objekt für die Eingabedatei aus dem ContentInfo-Quell Objekt ab, indem Sie [**imfasfcontentinfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)aufrufen. Die-Methode gibt einen Zeiger auf ein Profil Objekt zurück, das alle Streams in der Eingabedatei enthält. Weitere Informationen finden Sie unter [Erstellen eines ASF-Profils](creating-an-asf-profile.md).
2.  Entfernen Sie alle gegenseitigen Ausschluss Objekte aus dem Profil. Dieser Schritt ist erforderlich, da nicht-Audiodatenströme aus dem Profil entfernt werden, wodurch die gegenseitigen Ausschluss Objekte ungültig werden könnten.
3.  Entfernen Sie alle nicht-Audiodatenströme aus dem Profil wie folgt:
    -   Aufrufen von [**imfasfprofile:: getstreamcount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) , um die Anzahl der Streams zu erhalten.
    -   Aufrufen Sie in einer-Schleife [**imfasfprofile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) , um jeden Stream nach Index abzurufen.
    -   Aufrufen von [**imfasfstreamconfig:: getstreamtype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) zum Abrufen des streamtyps.
    -   Bei nicht-Audiodatenströmen wird [**imfasfprofile:: removestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) aufgerufen, um den Datenstrom zu entfernen.
4.  Speichert die streamnummer des ersten Audiostreams. Diese wird für den Splitter ausgewählt, um streambeispiele zu generieren. Wenn die streamnummer 0 (null) ist, kann der Aufrufer annehmen, dass es keine audiodatenstreamdatei gab.

Der folgende Code führt die folgenden Schritte aus:


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



Die- `RemoveMutexes` Funktion entfernt alle gegenseitigen Ausschluss Objekte aus dem Profil:


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

Als Nächstes erstellen Sie das ContentInfo-Ausgabe Objekt und den Multiplexer zum Erstellen von Datenpaketen für die Ausgabedatei.

Das in Schritt 4 erstellte Audioprofil wird zum Auffüllen des ContentInfo-Ausgabe Objekts verwendet. Dieses Objekt enthält Informationen wie globale Dateiattribute und streameigenschaften. Das ContentInfo-Ausgabe Objekt wird verwendet, um den Multiplexer zu initialisieren, der Datenpakete für die Ausgabedatei generiert. Nachdem die Datenpakete generiert wurden, muss das ContentInfo-Objekt aktualisiert werden, um die neuen Werte widerzuspiegeln.

So erstellen und initialisieren Sie die ASF-Komponenten für die Ausgabedatei

1.  Erstellen Sie ein leeres ContentInfo-Objekt, indem Sie [**mfcreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) aufrufen und es mit Informationen aus dem in Schritt 3 erstellten Audioprofil auffüllen, indem Sie [**imfasfcontentinfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)aufrufen. Weitere Informationen finden Sie unter [Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei](initializing-the-contentinfo-object-of-a-new-asf-file.md).
2.  Erstellen und initialisieren Sie das Multiplexer-Objekt mit dem ContentInfo-Ausgabe Objekt. Weitere Informationen finden Sie unter [Erstellen des Multiplexer-Objekts](creating-the-multiplexer-object.md).

Der folgende Beispielcode zeigt eine Funktion, die die Schritte konsolidiert. Diese Funktion nimmt einen Zeiger auf ein Profil Objekt an und gibt Zeiger auf das Output ContentInfo-Objekt und den Multiplexer zurück.


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

Als nächstes generieren Sie audiostreambeispiele aus dem quellbytestream mithilfe des Splitters und senden Sie an den Multiplexer, um ASF-Datenpakete zu erstellen. Diese Datenpakete bilden das endgültige ASF-Datenobjekt für die neue Datei.

So generieren Sie audiostreambeispiele

1.  Wählen Sie den ersten Audiostream auf dem Splitter aus, indem Sie [**imfasfsplitter:: selectstreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams)aufrufen.
2.  Lesen Sie Blöcke mit fester Größe aus dem Quell-Bytestream in einen Medien Puffer.
3.  Erfassen Sie die streambeispiele als Medien Beispiele aus dem Splitter, indem Sie [**imfasfsplitter:: getnextsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in einer Schleife aufrufen, solange das- \_ Flag "ASF Statusflags \_ unvollständig" im *pdwstatusflags* -Parameter empfangen wird. Weitere Informationen finden Sie unter Erstellen von Beispielen für ASF-Datenpakete in [Erstellen von streambeispielen aus einem vorhandenen ASF-Datenobjekt](generating-stream-samples-from-an-existing-asf-data-object.md).
4.  Nennen Sie für jedes Medien Beispiel [**imfasfmultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) , um das Medien Beispiel an den Multiplexer zu senden. Der Multiplexer generiert die Datenpakete für das ASF-Datenobjekt.
5.  Schreiben des vom Multiplexer generierten Datenpakets in den datenbytestream.
6.  Nachdem alle Datenpakete generiert wurden, wird [**imfasfmultiplexer:: End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) aufgerufen, um das Ausgabe-ContentInfo-Objekt mit Informationen zu aktualisieren, die während der Erstellung des ASF-Datenpakets gesammelt wurden.

Der folgende Beispielcode generiert streambeispiele aus dem ASF-Splitter und sendet Sie an den Multiplexer. Der Multiplexer generiert ASF-Datenpakete und schreibt Sie in einen Stream.


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



Um Pakete aus dem ASF-Splitter zu erhalten, ruft der vorherige Code die- `GetPacketsFromSplitter` Funktion auf, wie hier gezeigt:


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



Die `GenerateDataPackets` Funktion ruft Datenpakete von Multiplexer ab. Weitere Informationen finden Sie unter [erhalten von ASF-Datenpaketen](generating-new-asf-data-packets.md).


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



## <a name="8-write-the-asf-objects-in-the-new-file"></a>8. Schreiben der ASF-Objekte in der neuen Datei

Als nächstes schreiben Sie den Inhalt des ContentInfo-Ausgabe Objekts in einen Medien Puffer, indem Sie [**imfasfcontentinfo:: generateheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader)aufrufen. Diese Methode konvertiert die im ContentInfo-Objekt gespeicherten Daten im Objekt Format des ASF-Headers in Binärdaten. Weitere Informationen finden Sie unter [Erstellen eines neuen ASF-Header Objekts](generating-a-new-asf-header-object.md).

Nachdem das neue ASF-Header Objekt generiert wurde, schreiben Sie die Ausgabedatei, indem Sie zuerst das Header Objekt in den in Schritt 2 erstellten Ausgabe Byte Datenstrom schreiben, indem Sie die Hilfsfunktion "writebuffertobytestream" aufrufen. Befolgen Sie das Header Objekt mit dem Datenobjekt, das im datenbytestream enthalten ist. Der Beispielcode zeigt eine Funktion, die den Inhalt des Datenstrom-Datenstroms an den Bytestream überträgt.


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

Nun können Sie die vorherigen Schritte in eine komplette Anwendung einfügen. Initialisieren Sie vor dem Verwenden eines der Media Foundation Objekte die Media Foundation Plattform durch Aufrufen von [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Wenn Sie den Vorgang abgeschlossen haben, wenden Sie sich an [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Weitere Informationen finden Sie unter [Initialisieren von Media Foundation](initializing-media-foundation.md).

Der folgende Code zeigt die komplette Konsolenanwendung. Das Befehlszeilenargument gibt den Namen der zu konvertierenden Datei und den Namen der neuen Audiodatei an.


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

[Wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md)
</dt> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



