---
description: In diesem Tutorial wird das Schreiben einer neuen Audiodatei (WMA) veranschaulicht, indem Medieninhalte aus einer unkomprimierten Audiodatei (WAV) extrahiert und anschließend im ASF-Format komprimiert werden.
ms.assetid: f310c6ed-52e7-4828-9d4c-2f7ced9080c5
title: 'Tutorial: Schreiben einer WMA-Datei mithilfe von WMContainer-Objekten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aed89eb9ef656fe9240a1ed56e712f92209ba5c7e6d5bea2cca3d909d4315ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972769"
---
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a>Tutorial: Schreiben einer WMA-Datei mithilfe von WMContainer-Objekten

In diesem Tutorial wird das Schreiben einer neuen Audiodatei (WMA) veranschaulicht, indem Medieninhalte aus einer unkomprimierten Audiodatei (WAV) extrahiert und anschließend im ASF-Format komprimiert werden. Der für die Konvertierung verwendete Codierungsmodus ist [Die Codierung der konstanten Bitrate](constant-bit-rate-encoding.md) (Constant Bit Rate Encoding, CBR). In diesem Modus gibt die Anwendung vor der Codierungssitzung eine Zielbitrate an, die der Encoder erreichen muss.

In diesem Tutorial erstellen Sie eine Konsolenanwendung, die die Eingabe- und Ausgabedateinamen als Argumente verwendet. Die Anwendung ruft die unkomprimierten Medienbeispiele aus einer Wavedatei-Analyseanwendung ab, die in diesem Tutorial bereitgestellt wird. Diese Beispiele werden an den Encoder gesendet, um sie in Windows Media Audio 9-Format zu konvertieren. Der Encoder ist für die CBR-Codierung konfiguriert und verwendet die erste Bitrate, die während der Medientypaushandlung verfügbar ist, als Zielbitrate. Die codierten Beispiele werden zur Paketisierung im ASF-Datenformat an den Multiplexer gesendet. Diese Pakete werden in einen Bytestream geschrieben, der das ASF-Datenobjekt darstellt. Nachdem der Datenabschnitt bereit ist, erstellen Sie eine ASF-Audiodatei und schreiben das neue ASF-Headerobjekt, das alle Headerinformationen konsolidiert, und fügen dann den BYTE-Datenstrom des ASF-Datenobjekts an.

Dieses Tutorial enthält die folgenden Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Terminologie](#terminology)
-   [1. Einrichten der Project](#1-set-up-the-project)
-   [2. Deklarieren von Hilfsfunktionen](#2-declare-helper-functions)
-   [3. Öffnen einer Audiodatei](#3-open-an-audio-file)
-   [4. Konfigurieren des Encoders](#4-configure-the-encoder)
-   [5. Erstellen Sie das ASF ContentInfo-Objekt.](#5-create-the-asf-contentinfo-object)
-   [6. Erstellen des ASF-Multiplexers](#6-create-the-asf-multiplexer)
-   [7. Generieren neuer ASF-Datenpakete](#7-generate-new-asf-data-packets)
-   [8. Schreiben der ASF-Datei](#8-write-the-asf-file)
-   [9. Definieren der Entry-Point Funktion](#9-define-the-entry-point-function)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

In diesem Tutorial wird Folgendes vorausgesetzt:

-   Sie sind mit der Struktur einer ASF-Datei und den komponenten vertraut, die von Media Foundation für die Arbeit mit ASF-Objekten bereitgestellt werden. Zu diesen Komponenten gehören ContentInfo-, Splitter-, Multiplexer- und Profilobjekte. Weitere Informationen finden Sie unter [WMContainer ASF Components](wmcontainer-asf-components.md).
-   Sie sind mit den Windows Media Encoder und den verschiedenen Codierungstypen, insbesondere CBR, vertraut. Weitere Informationen finden Sie unter [Windows Media Encoders](windows-media-encoders.md) .
-   Sie sind mit [Medienpuffern](media-buffers.md) und Bytestreams vertraut: Insbesondere Dateivorgänge, die einen Bytestream verwenden und den Inhalt eines Medienpuffers in einen Bytestream schreiben.

## <a name="terminology"></a>Begriff

In diesem Tutorial werden die folgenden Begriffe verwendet:

-   Quellmedientyp: Medientypobjekt, macht [**DIEMEDIAType-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) verfügbar, die den Inhalt der Eingabedatei beschreibt.
-   Audioprofil: Profilobjekt, macht [**die IMFASFProfile-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) verfügbar, die nur Audiostreams der Ausgabedatei enthält.
-   Streambeispiel: Medienbeispiel, verfügbar macht [**DIEZsample-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) verfügbar und stellt die Mediendaten der Eingabedatei dar, die vom Encoder in einem komprimierten Zustand erhalten wurden.
-   ContentInfo-Objekt: [Das ASF ContentInfo-Objekt](asf-contentinfo-object.md)macht die [**IMFASFContentInfo-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) verfügbar, die das ASF-Headerobjekt der Ausgabedatei darstellt.
-   Datenbytedatenstrom: Bytestreamobjekt, macht [**DIEBYTEStream-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) verfügbar, die den gesamten ASF-Datenobjektteil der Ausgabedatei darstellt.
-   Datenpaket: Medienbeispiel, verfügbar macht [**DIESAMple-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) verfügbar, die vom [ASF-Multiplexer generiert wird;](asf-multiplexer.md) stellt ein ASF-Datenpaket dar, das in den Daten bytestream geschrieben wird.
-   Ausgabebytestream: Bytestreamobjekt, macht [**DIEBYTESTREAM-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) verfügbar, die den Inhalt der Ausgabedatei enthält.

## <a name="1-set-up-the-project"></a>1. Einrichten der Project

1.  Schließen Sie die folgenden Header in ihre Quelldatei ein:

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  Link zu den folgenden Bibliotheksdateien:

    -   mfplat.lib
    -   mf.lib
    -   mfuuid.lib

3.  Deklarieren [Sie die SafeRelease-Funktion.](saferelease.md)
4.  Schließen Sie die CWmaEncoder-Klasse in Ihr Projekt ein. Den vollständigen Quellcode dieser Klasse finden Sie unter [Encoder-Beispielcode](encoder-example-code.md).

## <a name="2-declare-helper-functions"></a>2. Deklarieren von Hilfsfunktionen

In diesem Tutorial werden die folgenden Hilfsfunktionen zum Lesen und Schreiben aus einem Bytestream verwendet.

-   `AppendToByteStream`: Fügt den Inhalt eines Bytestreams an einen anderen Bytestream an.
-   WriteBufferToByteStream: Schreibt Daten aus einem Medienpuffer in einen Bytestream.

Weitere Informationen finden Sie unter [**DURCHBYTEStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write). Der folgende Code zeigt diese Hilfsfunktionen:


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



## <a name="3-open-an-audio-file"></a>3. Öffnen einer Audiodatei

In diesem Tutorial wird davon ausgegangen, dass Ihre Anwendung unkomprimierte Audiodaten für die Codierung generiert. Zu diesem Zweck werden in diesem Tutorial zwei Funktionen deklariert:


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



Die Implementierung dieser Funktionen bleibt dem Reader überlassen.

-   Die `OpenAudioFile` Funktion sollte die von *pszURL* angegebene Mediendatei öffnen und einen Zeiger auf einen Medientyp zurückgeben, der einen Audiostream beschreibt.
-   Die `GetNextAudioSample` Funktion sollte unkomprimierte PCM-Audiodaten aus der Datei lesen, die von geöffnet `OpenAudioFile` wurde. Wenn das Ende der Datei erreicht ist, *empfängt pbEOS* den Wert **TRUE**. *Andernfalls empfängt ppSample* ein Medienbeispiel, das den Audiopuffer enthält.

## <a name="4-configure-the-encoder"></a>4. Konfigurieren des Encoders

Erstellen Sie als Nächstes den Encoder, konfigurieren Sie ihn so, dass CBR-codierte Streambeispiele erstellt werden, und handeln Sie die Eingabe- und Ausgabemedientypen aus.

In Media Foundation werden Encoder (die [**DIET-Schnittstelle verfügbar**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) machen) als Media Foundation [Transforms](media-foundation-transforms.md) (MFT) implementiert.

In diesem Tutorial wird der Encoder in der -Klasse `CWmaEncoder` implementiert, die einen Wrapper für MFT bietet. Den vollständigen Quellcode dieser Klasse finden Sie unter [Encoder-Beispielcode](encoder-example-code.md).

> [!Note]  
> Optional können Sie den Codierungstyp als CBR angeben. Standardmäßig ist der Encoder für die Verwendung der CBR-Codierung konfiguriert. Weitere Informationen finden Sie unter [Constant Bit Rate Encoding](constant-bit-rate-encoding.md). Sie können je nach Codierungstyp zusätzliche Eigenschaften festlegen. Informationen zu den eigenschaften, die für einen Codierungsmodus spezifisch sind, finden Sie unter [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md), [Unconstrained Variable Bit Rate Encoding](unconstrained-variable-bit-rate--vbr--encoding.md)und [Peak-Constrained Variable Bit Rate Encoding](peak-constrained-variable-bit-rate--vbr--encoding.md).

 


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



## <a name="5-create-the-asf-contentinfo-object"></a>5. Erstellen Sie das ASF ContentInfo-Objekt.

Das [ASF ContentInfo-Objekt](asf-contentinfo-object.md) enthält Informationen zu den verschiedenen Headerobjekten der Ausgabedatei.

Erstellen Sie zunächst ein ASF-Profil für den Audiostream:

1.  Rufen [**Sie MFCreateASFProfile auf,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) um ein leeres ASF-Profilobjekt zu erstellen. Das ASF-Profil macht die [**IMFASFProfile-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) verfügbar. Weitere Informationen finden Sie unter [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).
2.  Das codierte Audioformat wird aus dem -Objekt `CWmaEncoder` entfernt.
3.  Rufen [**Sie IMFASFProfile::CreateStream auf,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) um einen neuen Stream für das ASF-Profil zu erstellen. Übergeben Sie einen Zeiger auf die [**BESCHRIFTUNGMediaType-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) die das Streamformat darstellt.
4.  Rufen [**Sie IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) auf, um einen Streambezeichner zu zuweisen.
5.  Legen Sie die Parameter "Leaky Bucket" fest, indem Sie das [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1-Attribut**](mf-asfstreamconfig-leakybucket1-attribute.md) für das Streamobjekt festlegen.
6.  Rufen [**Sie IMFASFProfile::SetStream auf,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) um dem Profil den neuen Stream hinzuzufügen.

Erstellen Sie nun das ASF ContentInfo-Objekt wie folgt:

1.  Rufen [**Sie MFCreateASFContentInfo auf,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) um ein leeres ContentInfo-Objekt zu erstellen.
2.  Rufen [**Sie IMFASFContentInfo::SetProfile auf,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) um das ASF-Profil zu festlegen.

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



## <a name="6-create-the-asf-multiplexer"></a>6. Erstellen des ASF-Multiplexers

Der [ASF-Multiplexer](asf-multiplexer.md) generiert ASF-Datenpakete.

1.  Rufen [**Sie MFCreateASFMultiplexer auf,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) um den ASF-Multiplexer zu erstellen.
2.  Rufen [**Sie IMFASFMultiplexer::Initialize auf,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) um den Multiplexer zu initialisieren. Übergeben Sie einen Zeiger auf das ASF-Inhaltsinformationsobjekt, das im vorherigen Abschnitt erstellt wurde.
3.  Rufen [**Sie IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) auf, um das **MFASF \_ MULTIPLEXER \_ AUTOADJUST \_ BITRATE-Flag festlegen.** Wenn diese Einstellung verwendet wird, passt der Multiplexer die Bitrate des ASF-Inhalts automatisch an die Merkmale der Datenströme an, die multiplexiert werden.


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

Generieren Sie als Nächstes ASF-Datenpakete für die neue Datei. Diese Datenpakete bilden das endgültige ASF-Datenobjekt für die neue Datei. So generieren Sie neue ASF-Datenpakete:

1.  Rufen Sie [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) auf, um einen temporären Bytestream für die ASF-Datenpakete zu erstellen.
2.  Rufen Sie die anwendungsdefinierte `GetNextAudioSample` Funktion auf, um unkomprimierte Audiodaten für den Encoder abzurufen.
3.  Übergeben Sie die unkomprimierten Audiodaten zur Komprimierung an den Encoder. Weitere Informationen finden Sie unter [Verarbeiten von Daten im Encoder.](processing-data-in-the-encoder.md)
4.  Rufen Sie [**IMFASFMultiplexer::P rocessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) auf, um die komprimierten Audiobeispiele zur Paketisierung an den ASF-Multiplexer zu senden.
5.  Abrufen der ASF-Pakete aus dem Multiplexer und Schreiben in den temporären Bytestream. Weitere Informationen finden Sie unter [Generieren neuer ASF-Datenpakete.](generating-new-asf-data-packets.md)
6.  Wenn Sie das Ende des Quelldatenstroms erreichen, entladen Sie den Encoder, und ziehen Sie die verbleibenden komprimierten Stichproben vom Encoder. Weitere Informationen zum Entladen eines MFT finden Sie unter [Grundlegendes MFT-Verarbeitungsmodell.](basic-mft-processing-model.md)
7.  Nachdem alle Beispiele an den Multiplexer gesendet wurden, rufen Sie [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) auf, und pullen Sie die verbleibenden ASF-Pakete aus dem Multiplexer.
8.  Rufen Sie [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end)auf.

Der folgende Code generiert ASF-Datenpakete. Die Funktion gibt einen Zeiger auf einen Bytestream zurück, der das ASF-Datenobjekt enthält.


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



Code für die `GenerateASFDataPackets` Funktion wird im Thema Generieren neuer [ASF-Datenpakete](generating-new-asf-data-packets.md)gezeigt.

## <a name="8-write-the-asf-file"></a>8. Schreiben der ASF-Datei

Schreiben Sie als Nächstes den ASF-Header in einen Medienpuffer, indem Sie [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader)aufrufen. Diese Methode konvertiert im ContentInfo-Objekt gespeicherte Daten in Binärdaten im ASF-Headerobjektformat. Weitere Informationen finden Sie unter [Generieren eines neuen ASF-Headerobjekts.](generating-a-new-asf-header-object.md)

Nachdem das neue ASF-Headerobjekt generiert wurde, erstellen Sie einen Bytestream für die Ausgabedatei. Schreiben Sie zuerst das Headerobjekt in den Ausgabe-Bytestream. Folgen Sie dem Headerobjekt mit dem Datenobjekt, das im Daten-Bytestream enthalten ist.


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

Nun können Sie die vorherigen Schritte in einer vollständigen Anwendung zusammenfügen. Bevor Sie eines der Media Foundation -Objekte verwenden, initialisieren Sie die Media Foundation-Plattform, indem Sie [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)aufrufen. Wenn Sie fertig sind, rufen Sie [**MFShutdown auf.**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) Weitere Informationen finden Sie unter [Initialisieren Media Foundation](initializing-media-foundation.md).

Der folgende Code zeigt die vollständige Konsolenanwendung. Das Befehlszeilenargument gibt den Namen der zu konvertierenden Datei und den Namen der neuen Audiodatei an.


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

[WMContainer ASF-Komponenten](wmcontainer-asf-components.md)
</dt> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



