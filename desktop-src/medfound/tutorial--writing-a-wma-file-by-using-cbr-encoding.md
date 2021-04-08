---
description: Dieses Tutorial veranschaulicht das Schreiben einer neuen Audiodatei (. WMA) durch Extrahieren von Medieninhalten aus einer unkomprimierten Audiodatei (. wav) und die anschließende Komprimierung im ASF-Format.
ms.assetid: f310c6ed-52e7-4828-9d4c-2f7ced9080c5
title: 'Tutorial: Schreiben einer WMA-Datei mithilfe von wmcontainer-Objekten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d156b75ced6cde2953ec90362ed13b0cc53bb83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863936"
---
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a>Tutorial: Schreiben einer WMA-Datei mithilfe von wmcontainer-Objekten

Dieses Tutorial veranschaulicht das Schreiben einer neuen Audiodatei (. WMA) durch Extrahieren von Medieninhalten aus einer unkomprimierten Audiodatei (. wav) und die anschließende Komprimierung im ASF-Format. Der für die Konvertierung verwendete Codierungs Modus ist die [Konstante Bitrate-Codierung](constant-bit-rate-encoding.md) (CBR). In diesem Modus gibt die Anwendung vor der Codierungs Sitzung eine Zielbitrate an, die vom Encoder erreicht werden muss.

In diesem Tutorial erstellen Sie eine Konsolenanwendung, die die Eingabe-und Ausgabe Dateinamen als Argumente annimmt. Die Anwendung ruft die Beispiele für nicht komprimierte Medien aus einer Anwendung für die Verarbeitung von Wave-Dateien ab, die in diesem Tutorial bereitgestellt wird. Diese Beispiele werden an den Encoder für die Konvertierung in Windows Media Audio 9-Format gesendet. Der Encoder ist für die CBR-Codierung konfiguriert und verwendet die erste Bitrate, die während der Medientyp Aushandlung als Zielbitrate verfügbar ist. Die codierten Beispiele werden an den Multiplexer für die packetisierung im ASF-Datenformat gesendet. Diese Pakete werden in einen Bytestream geschrieben, der das ASF-Datenobjekt darstellt. Nachdem der Daten Abschnitt bereit ist, erstellen Sie eine ASF-Audiodatei und schreiben das neue ASF-Header Objekt, das alle Header Informationen konsolidiert und dann den Datenstrom des ASF-Datenobjekts anfügt.

Dieses Tutorial enthält die folgenden Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Terminologie](#terminology)
-   [1. richten Sie das Projekt ein.](#1-set-up-the-project)
-   [2. Deklarieren von Hilfsfunktionen](#2-declare-helper-functions)
-   [3. Öffnen Sie eine Audiodatei.](#3-open-an-audio-file)
-   [4. Konfigurieren des Encoders](#4-configure-the-encoder)
-   [5. Erstellen Sie das Objekt "ASF ContentInfo".](#5-create-the-asf-contentinfo-object)
-   [6. Erstellen des ASF Multiplexer](#6-create-the-asf-multiplexer)
-   [7. Generieren neuer ASF-Datenpakete](#7-generate-new-asf-data-packets)
-   [8. Schreiben der ASF-Datei](#8-write-the-asf-file)
-   [9. Definieren der Entry-Point-Funktion](#9-define-the-entry-point-function)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

In diesem Tutorial wird Folgendes vorausgesetzt:

-   Sie sind mit der Struktur einer ASF-Datei und den von Media Foundation bereitgestellten Komponenten vertraut, um mit der Verwendung von ASF-Objekten zu arbeiten. Zu diesen Komponenten gehören ContentInfo-, Splitter-, Multiplexer-und Profile-Objekte. Weitere Informationen finden Sie unter [wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md).
-   Sie sind mit Windows Media Encoder und den verschiedenen Codierungs Typen vertraut, insbesondere mit CBR. Weitere Informationen finden Sie unter [Windows Media Encoder](windows-media-encoders.md) .
-   Sie sind mit [Medien Puffern](media-buffers.md) und Bytestreams vertraut: insbesondere Datei Vorgänge mit einem Bytestream und das Schreiben des Inhalts eines Medien Puffers in einen Bytestream.

## <a name="terminology"></a>Begriff

In diesem Tutorial werden die folgenden Begriffe verwendet:

-   Quell Medientyp: Medientyp Objekt macht die [**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle verfügbar, die den Inhalt der Eingabedatei beschreibt.
-   Audioprofil: Profil Objekt macht die [**imfasf profile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) -Schnittstelle verfügbar, die nur Audiostreams der Ausgabedatei enthält.
-   Stream Sample: Media Sample, macht die [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle verfügbar und stellt die Mediendaten der Eingabedatei dar, die vom Encoder in einem komprimierten Zustand abgerufen wurden.
-   ContentInfo-Objekt: das [Objekt "ASF ContentInfo](asf-contentinfo-object.md)" macht die [**imfasf ContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Schnittstelle verfügbar, die das ASF-Header Objekt der Ausgabedatei darstellt.
-   Daten Byte Datenstrom: das [**bytestreamobjekt macht die IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Schnittstelle verfügbar, die den gesamten Teil des ASF-Datenobjekts der Ausgabedatei darstellt.
-   Data Packet: Media Sample, macht die [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle verfügbar, die vom [ASF Multiplexer](asf-multiplexer.md)generiert wurde. stellt ein ASF-Datenpaket dar, das in den datenbytestream geschrieben wird.
-   Ausgabe Byte Datenstrom: das Byte Datenstrom Objekt macht die [**IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Schnittstelle verfügbar, die den Inhalt der Ausgabedatei enthält.

## <a name="1-set-up-the-project"></a>1. richten Sie das Projekt ein.

1.  Fügen Sie die folgenden Header in die Quelldatei ein:

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  Verknüpfen Sie die folgenden Bibliotheksdateien:

    -   MF. lib
    -   MF. lib
    -   mfuuid. lib

3.  Deklarieren Sie die Funktion [saferelease](saferelease.md) .
4.  Schließen Sie die cwmaencoder-Klasse in Ihr Projekt ein. Den gesamten Quellcode dieser Klasse finden Sie unter Encoder- [Beispielcode](encoder-example-code.md).

## <a name="2-declare-helper-functions"></a>2. Deklarieren von Hilfsfunktionen

In diesem Tutorial werden die folgenden Hilfsfunktionen verwendet, um aus einem Bytestream zu lesen und zu schreiben.

-   `AppendToByteStream`: Fügt den Inhalt eines Bytestreams an einen anderen Bytestream an.
-   Write-bufferdebytestream: schreibt Daten aus einem Medien Puffer in einen Bytestream.

Weitere Informationen finden Sie unter [**IMF Bytestream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write). Der folgende Code zeigt diese Hilfsfunktionen:


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



## <a name="3-open-an-audio-file"></a>3. Öffnen Sie eine Audiodatei.

In diesem Tutorial wird davon ausgegangen, dass Ihre Anwendung nicht komprimierte Audiodaten für die Codierung generiert. Zu diesem Zweck werden zwei Funktionen in diesem Tutorial deklariert:


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



Die Implementierung dieser Funktionen wird dem Reader überlassen.

-   Die `OpenAudioFile` Funktion sollte die von *pszurl* angegebene Mediendatei öffnen und einen Zeiger auf einen Medientyp zurückgeben, der einen Audiostream beschreibt.
-   Die `GetNextAudioSample` Funktion sollte nicht komprimiertes PCM-Audiodaten aus der Datei lesen, die von geöffnet wurde `OpenAudioFile` . Wenn das Ende der Datei erreicht ist, empfängt *pbeos* den Wert " **true**". Andernfalls empfängt *ppsample* ein Medien Beispiel, das den Audiopuffer enthält.

## <a name="4-configure-the-encoder"></a>4. Konfigurieren des Encoders

Erstellen Sie als nächstes den Encoder, konfigurieren Sie ihn so, dass CBR-codierte streambeispiele erstellt werden, und verhandeln Sie die Eingabe-und Ausgabemedien Typen.

In Media Foundation werden Encoder (die die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle verfügbar machen) als [Media Foundation Transformationen](media-foundation-transforms.md) (MFT) implementiert.

In diesem Tutorial wird der Encoder in der-Klasse implementiert, die `CWmaEncoder` einen Wrapper für die MFT bereitstellt. Den gesamten Quellcode dieser Klasse finden Sie unter Encoder- [Beispielcode](encoder-example-code.md).

> [!Note]  
> Optional können Sie den Codierungstyp als CBR angeben. Standardmäßig ist der Encoder für die Verwendung der CBR-Codierung konfiguriert. Weitere Informationen finden Sie unter [Konstante Bitrate-Codierung](constant-bit-rate-encoding.md). Sie können zusätzliche Eigenschaften abhängig vom Codierungstyp festlegen. Informationen zu den Eigenschaften, die für einen Codierungs Modus spezifisch sind, finden Sie unter [Qualitäts basierte Variablen-](quality-based-variable-bit-rate--vbr--encoding.md)Bitrate-Codierung, [unbeschränkte Variablen Bitrate-Codierung](unconstrained-variable-bit-rate--vbr--encoding.md)und [Maximale Codierung der Variablen Bitrate](peak-constrained-variable-bit-rate--vbr--encoding.md).

 


```C++
    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="5-create-the-asf-contentinfo-object"></a>5. Erstellen Sie das Objekt "ASF ContentInfo".

Das [Objekt "ASF ContentInfo](asf-contentinfo-object.md) " enthält Informationen zu den verschiedenen Header Objekten der Ausgabedatei.

Erstellen Sie zunächst ein ASF-Profil für den Audiostream:

1.  Rufen Sie [**mfkreateasfprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) auf, um ein leeres ASF-Profil Objekt zu erstellen. Das ASF-Profil macht die [**imfasf profile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) -Schnittstelle verfügbar. Weitere Informationen finden Sie unter [Erstellen und Konfigurieren von ASF-Streams](creating-and-configuring-asf-streams.md).
2.  Das codierte Audioformat aus dem-Objekt zu erhalten `CWmaEncoder` .
3.  Rufen Sie [**imfasfprofile:: kreatestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) auf, um einen neuen Datenstrom für das ASF-Profil zu erstellen. Übergeben Sie einen Zeiger auf die [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle, die das Streamformat darstellt.
4.  Aufrufen von [**imfasfstreamconfig:: setstreamnumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) zum Zuweisen eines Datenstrom Bezeichners.
5.  Legen Sie die Parameter "Leaky Bucket" fest, indem Sie das [**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) -Attribut für das Stream-Objekt festlegen.
6.  Aufrufen von [**imfasfprofile:: setStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) , um dem Profil den neuen Stream hinzuzufügen.

Erstellen Sie nun das Objekt "ASF ContentInfo" wie folgt:

1.  Rufen Sie [**mfkreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) auf, um ein leeres ContentInfo-Objekt zu erstellen.
2.  Aufrufen von [**imfasfcontentinfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) , um das ASF-Profil festzulegen.

Diese Schritte sind im folgenden Code dargestellt:


```C++
HRESULT CreateASFContentInfo(
    CWmaEncoder* pEncoder,
    IMFASFContentInfo** ppContentInfo
    )
{
    HRESULT hr = S_OK;
    
    IMFASFProfile* pProfile = NULL;
    IMFMediaType* pMediaType = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFASFContentInfo* pContentInfo = NULL;

    // Create the ASF profile object.

    hr = MFCreateASFProfile(&pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a stream description for the encoded audio.

    hr = pEncoder->GetOutputType(&pMediaType); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->CreateStream(pMediaType, &pStream); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetStreamNumber(DEFAULT_STREAM_NUMBER); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Set "leaky bucket" values.

    LeakyBucket bucket;

    hr = pEncoder->GetLeakyBucket1(&bucket);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetBlob(
        MF_ASFSTREAMCONFIG_LEAKYBUCKET1, 
        (UINT8*)&bucket, 
        sizeof(bucket)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile

    hr = pProfile->SetStream(pStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the ASF ContentInfo object.

    hr = MFCreateASFContentInfo(&pContentInfo); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContentInfo->SetProfile(pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.

    *ppContentInfo = pContentInfo;
    (*ppContentInfo)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pStream);
    SafeRelease(&pMediaType);
    SafeRelease(&pContentInfo);
    return hr;
}
```



## <a name="6-create-the-asf-multiplexer"></a>6. Erstellen des ASF Multiplexer

Der [ASF Multiplexer](asf-multiplexer.md) generiert ASF-Datenpakete.

1.  Rufen Sie [**mfkreateasfmultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) auf, um den ASF Multiplexer zu erstellen.
2.  Zum Initialisieren des Multiplexer muss [**imfasfmultiplexer:: Initialisieren**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) aufgerufen werden. Übergeben Sie einen Zeiger auf das Objekt "ASF Content Info", das im vorherigen Abschnitt erstellt wurde.
3.  [**Imfasfmultiplexer:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) aufrufen, um das Flag für die **Automatische Anpassung der mfasf \_ Multiplexer- \_ \_ Bitrate** festzulegen. Wenn diese Einstellung verwendet wird, passt der Multiplexer die Bitrate des ASF-Inhalts automatisch an die Merkmale der zu multipleckenden Streams an.


```C++
HRESULT CreateASFMux( 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer** ppMultiplexer
    )
{
    HRESULT hr = S_OK;
    
    IMFMediaType* pMediaType = NULL;
    IMFASFMultiplexer *pMultiplexer = NULL;

    // Create and initialize the ASF Multiplexer object.

    hr = MFCreateASFMultiplexer(&pMultiplexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pMultiplexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Enable automatic bit-rate adjustment.

    hr = pMultiplexer->SetFlags(MFASF_MULTIPLEXER_AUTOADJUST_BITRATE);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppMultiplexer = pMultiplexer;
    (*ppMultiplexer)->AddRef();

done:
    SafeRelease(&pMultiplexer);
    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a>7. Generieren neuer ASF-Datenpakete

Generieren Sie als nächstes ASF-Datenpakete für die neue Datei. Diese Datenpakete bilden das endgültige ASF-Datenobjekt für die neue Datei. So generieren Sie neue ASF-Datenpakete:

1.  Rufen Sie [**mfkreatetempfile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) auf, um einen temporären Bytestream zum Speichern der ASF-Datenpakete zu erstellen.
2.  Ruft die Anwendungs definierte `GetNextAudioSample` Funktion auf, um unkomprimierte Audiodaten für den Encoder abzurufen.
3.  Übergeben Sie die unkomprimierte Audiodatei zur Komprimierung an den Encoder. Weitere Informationen finden Sie unter [Verarbeiten von Daten im Encoder](processing-data-in-the-encoder.md) .
4.  Nennen Sie [**imfasfmultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) , um die komprimierten Audiobeispiele an den ASF Multiplexer für packetisierung zu senden.
5.  Holen Sie sich die ASF-Pakete aus dem Multiplexer, und schreiben Sie Sie in den temporären Byte Datenstrom. Weitere Informationen finden Sie unter [Erstellen neuer ASF-Datenpakete](generating-new-asf-data-packets.md).
6.  Wenn Sie das Ende des Quelldaten Stroms erreicht haben, müssen Sie den Encoder entladen und die verbleibenden komprimierten Beispiele aus dem Encoder abrufen. Weitere Informationen zum Entleeren von MFT finden Sie unter [Grundlegendes MFT-Verarbeitungsmodell](basic-mft-processing-model.md).
7.  Nachdem alle Beispiele an den Multiplexer gesendet wurden, rufen Sie [**imfasfmultiplexer:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) auf, und rufen Sie die verbleibenden ASF-Pakete aus dem Multiplexer ab.
8.  [**Imfasfmultiplexer:: End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end)aufzurufen.

Der folgende Code generiert ASF-Datenpakete. Die-Funktion gibt einen Zeiger auf einen Bytestream zurück, der das ASF-Datenobjekt enthält.


```C++
HRESULT EncodeData(
    CWmaEncoder* pEncoder, 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer* pMux, 
    IMFByteStream** ppDataStream) 
{
    HRESULT hr = S_OK;

    IMFByteStream* pStream = NULL;
    IMFSample* pInputSample = NULL;
    IMFSample* pWmaSample = NULL;

    BOOL bEOF = FALSE;

   // Create a temporary file to hold the data stream.
   hr = MFCreateTempFile(
        MF_ACCESSMODE_READWRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        &pStream
        );

   if (FAILED(hr))
   {
       goto done;
   }

    BOOL bNeedInput = TRUE;

    while (TRUE)
    {
        if (bNeedInput)
        {
            hr = GetNextAudioSample(&bEOF, &pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            if (bEOF)
            {
                // Reached the end of the input file.
                break;
            }

            // Encode the uncompressed audio sample.
            hr = pEncoder->ProcessInput(pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            bNeedInput = FALSE;
        }

        if (bNeedInput == FALSE)
        {
            // Get data from the encoder.

            hr = pEncoder->ProcessOutput(&pWmaSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // pWmaSample can be NULL if the encoder needs more input.

            if (pWmaSample)
            {
                hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
                if (FAILED(hr))
                {
                    goto done;
                }

                //Collect the data packets and write them to a stream
                hr = GenerateASFDataPackets(pMux, pStream);
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else
            {
                bNeedInput = TRUE;
            }
        }
        
        SafeRelease(&pInputSample);
        SafeRelease(&pWmaSample);
    }

    // Drain the MFT and pull any remaining samples from the encoder.

    hr = pEncoder->Drain();
    if (FAILED(hr))
    {
        goto done;
    }

    while (TRUE)
    {
        hr = pEncoder->ProcessOutput(&pWmaSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pWmaSample == NULL)
        {
            break;
        }

        hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
        if (FAILED(hr))
        {
            goto done;
        }

        //Collect the data packets and write them to a stream
        hr = GenerateASFDataPackets(pMux, pStream);
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pWmaSample);
    }

    // Flush the mux and get any pending ASF data packets.
    hr = pMux->Flush();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GenerateASFDataPackets(pMux, pStream);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Update the ContentInfo object
    hr = pMux->End(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return stream to the caller that contains the ASF encoded data.
    *ppDataStream = pStream;
    (*ppDataStream)->AddRef();

done:
    SafeRelease(&pStream);
    SafeRelease(&pInputSample);
    SafeRelease(&pWmaSample);
    return hr;
}
```



Code für die `GenerateASFDataPackets` Funktion finden Sie im Thema [Erstellen neuer ASF-Datenpakete](generating-new-asf-data-packets.md).

## <a name="8-write-the-asf-file"></a>8. Schreiben der ASF-Datei

Schreiben Sie als nächstes den ASF-Header in einen Medien Puffer, indem Sie [**imfasfcontentinfo:: generateheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader)aufrufen. Diese Methode konvertiert die im ContentInfo-Objekt gespeicherten Daten im Objekt Format des ASF-Headers in Binärdaten. Weitere Informationen finden Sie unter [Erstellen eines neuen ASF-Header Objekts](generating-a-new-asf-header-object.md).

Nachdem das neue ASF-Header Objekt generiert wurde, erstellen Sie einen Bytestream für die Ausgabedatei. Schreiben Sie zuerst das Header Objekt in den ausgabebytestream. Befolgen Sie das Header Objekt mit dem Datenobjekt, das im datenbytestream enthalten ist.


```C++
HRESULT WriteASFFile( 
     IMFASFContentInfo *pContentInfo, 
     IMFByteStream *pDataStream,
     PCWSTR pszFile
     )
{
    HRESULT hr = S_OK;
    
    IMFMediaBuffer* pHeaderBuffer = NULL;
    IMFByteStream* pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    //Create output file
    hr = MFCreateFile(MF_ACCESSMODE_WRITE, MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE, pszFile, &pWmaStream);

    if (FAILED(hr))
    {
        goto done;
    }


    // Get the size of the ASF Header Object.
    hr = pContentInfo->GenerateHeader (NULL, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a media buffer.
    hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Populate the media buffer with the ASF Header Object.
    hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF header to the output file.
    hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    if (FAILED(hr))
    {
        goto done;
    }

    // Append the data stream to the file.

    hr = pDataStream->SetCurrentPosition(0);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = AppendToByteStream(pDataStream, pWmaStream);

done:
    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);
    return hr;
}
```



## <a name="9-define-the-entry-point-function"></a>9. Definieren der Entry-Point-Funktion

Nun können Sie die vorherigen Schritte in eine komplette Anwendung einfügen. Initialisieren Sie vor dem Verwenden eines der Media Foundation Objekte die Media Foundation Plattform durch Aufrufen von [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Wenn Sie den Vorgang abgeschlossen haben, wenden Sie sich an [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Weitere Informationen finden Sie unter [Initialisieren von Media Foundation](initializing-media-foundation.md).

Der folgende Code zeigt die komplette Konsolenanwendung. Das Befehlszeilenargument gibt den Namen der zu konvertierenden Datei und den Namen der neuen Audiodatei an.


```C++
int wmain(int argc, WCHAR* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma");
        return 0;
    }

    const WCHAR* sInputFileName = argv[1];    // Source file name
    const WCHAR* sOutputFileName = argv[2];  // Output file name
    
    IMFMediaType* pInputType = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFMultiplexer* pMux = NULL;
    IMFByteStream* pDataStream = NULL;

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    HRESULT hr = CoInitializeEx(
        NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the WMContainer objects.
    hr = CreateASFContentInfo(pEncoder, &pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateASFMux(pContentInfo, &pMux);
    if (FAILED(hr))
    {
        goto done;
    }

    // Convert uncompressed data to ASF format.
    hr = EncodeData(pEncoder, pContentInfo, pMux, &pDataStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF objects to the output file.
    hr = WriteASFFile(pContentInfo, pDataStream, sOutputFileName);

done:
    SafeRelease(&pInputType);
    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);
    SafeRelease(&pDataStream);
    delete pEncoder;

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
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

 

 



