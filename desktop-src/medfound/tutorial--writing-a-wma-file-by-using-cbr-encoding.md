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
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a><span data-ttu-id="7bce5-103">Tutorial: Schreiben einer WMA-Datei mithilfe von wmcontainer-Objekten</span><span class="sxs-lookup"><span data-stu-id="7bce5-103">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>

<span data-ttu-id="7bce5-104">Dieses Tutorial veranschaulicht das Schreiben einer neuen Audiodatei (. WMA) durch Extrahieren von Medieninhalten aus einer unkomprimierten Audiodatei (. wav) und die anschließende Komprimierung im ASF-Format.</span><span class="sxs-lookup"><span data-stu-id="7bce5-104">This tutorial demonstrates writing a new audio file (.wma) by extracting media content from an uncompressed audio file (.wav) and then compressing it in ASF format.</span></span> <span data-ttu-id="7bce5-105">Der für die Konvertierung verwendete Codierungs Modus ist die [Konstante Bitrate-Codierung](constant-bit-rate-encoding.md) (CBR).</span><span class="sxs-lookup"><span data-stu-id="7bce5-105">The encoding mode used for the conversion is [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR).</span></span> <span data-ttu-id="7bce5-106">In diesem Modus gibt die Anwendung vor der Codierungs Sitzung eine Zielbitrate an, die vom Encoder erreicht werden muss.</span><span class="sxs-lookup"><span data-stu-id="7bce5-106">In this mode, before the encoding session, the application specifies a target bit rate that the encoder must achieve.</span></span>

<span data-ttu-id="7bce5-107">In diesem Tutorial erstellen Sie eine Konsolenanwendung, die die Eingabe-und Ausgabe Dateinamen als Argumente annimmt.</span><span class="sxs-lookup"><span data-stu-id="7bce5-107">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="7bce5-108">Die Anwendung ruft die Beispiele für nicht komprimierte Medien aus einer Anwendung für die Verarbeitung von Wave-Dateien ab, die in diesem Tutorial bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7bce5-108">The application gets the uncompressed media samples from a wave file parsing application, which is provided with this tutorial.</span></span> <span data-ttu-id="7bce5-109">Diese Beispiele werden an den Encoder für die Konvertierung in Windows Media Audio 9-Format gesendet.</span><span class="sxs-lookup"><span data-stu-id="7bce5-109">These samples are sent to the encoder for conversion to Windows Media Audio 9 format.</span></span> <span data-ttu-id="7bce5-110">Der Encoder ist für die CBR-Codierung konfiguriert und verwendet die erste Bitrate, die während der Medientyp Aushandlung als Zielbitrate verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7bce5-110">The encoder is configured for CBR encoding and uses the first bit rate available during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="7bce5-111">Die codierten Beispiele werden an den Multiplexer für die packetisierung im ASF-Datenformat gesendet.</span><span class="sxs-lookup"><span data-stu-id="7bce5-111">The encoded samples are sent to the multiplexer for packetization in ASF data format.</span></span> <span data-ttu-id="7bce5-112">Diese Pakete werden in einen Bytestream geschrieben, der das ASF-Datenobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="7bce5-112">These packets will be written to a byte stream that represents the ASF Data Object.</span></span> <span data-ttu-id="7bce5-113">Nachdem der Daten Abschnitt bereit ist, erstellen Sie eine ASF-Audiodatei und schreiben das neue ASF-Header Objekt, das alle Header Informationen konsolidiert und dann den Datenstrom des ASF-Datenobjekts anfügt.</span><span class="sxs-lookup"><span data-stu-id="7bce5-113">After the data section is ready, you will create an ASF audio file and write the new ASF Header Object that consolidates all the header information and then append the ASF Data Object byte stream.</span></span>

<span data-ttu-id="7bce5-114">Dieses Tutorial enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="7bce5-114">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="7bce5-115">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="7bce5-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="7bce5-116">Terminologie</span><span class="sxs-lookup"><span data-stu-id="7bce5-116">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="7bce5-117">1. richten Sie das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="7bce5-117">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="7bce5-118">2. Deklarieren von Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="7bce5-118">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="7bce5-119">3. Öffnen Sie eine Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="7bce5-119">3. Open an Audio File</span></span>](#3-open-an-audio-file)
-   [<span data-ttu-id="7bce5-120">4. Konfigurieren des Encoders</span><span class="sxs-lookup"><span data-stu-id="7bce5-120">4. Configure the Encoder</span></span>](#4-configure-the-encoder)
-   [<span data-ttu-id="7bce5-121">5. Erstellen Sie das Objekt "ASF ContentInfo".</span><span class="sxs-lookup"><span data-stu-id="7bce5-121">5. Create the ASF ContentInfo object.</span></span>](#5-create-the-asf-contentinfo-object)
-   [<span data-ttu-id="7bce5-122">6. Erstellen des ASF Multiplexer</span><span class="sxs-lookup"><span data-stu-id="7bce5-122">6. Create the ASF Multiplexer</span></span>](#6-create-the-asf-multiplexer)
-   [<span data-ttu-id="7bce5-123">7. Generieren neuer ASF-Datenpakete</span><span class="sxs-lookup"><span data-stu-id="7bce5-123">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="7bce5-124">8. Schreiben der ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="7bce5-124">8. Write the ASF File</span></span>](#8-write-the-asf-file)
-   [<span data-ttu-id="7bce5-125">9. Definieren der Entry-Point-Funktion</span><span class="sxs-lookup"><span data-stu-id="7bce5-125">9. Define the Entry-Point Function</span></span>](#9-define-the-entry-point-function)
-   [<span data-ttu-id="7bce5-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7bce5-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="7bce5-127">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="7bce5-127">Prerequisites</span></span>

<span data-ttu-id="7bce5-128">In diesem Tutorial wird Folgendes vorausgesetzt:</span><span class="sxs-lookup"><span data-stu-id="7bce5-128">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="7bce5-129">Sie sind mit der Struktur einer ASF-Datei und den von Media Foundation bereitgestellten Komponenten vertraut, um mit der Verwendung von ASF-Objekten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7bce5-129">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="7bce5-130">Zu diesen Komponenten gehören ContentInfo-, Splitter-, Multiplexer-und Profile-Objekte.</span><span class="sxs-lookup"><span data-stu-id="7bce5-130">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="7bce5-131">Weitere Informationen finden Sie unter [wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="7bce5-131">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="7bce5-132">Sie sind mit Windows Media Encoder und den verschiedenen Codierungs Typen vertraut, insbesondere mit CBR.</span><span class="sxs-lookup"><span data-stu-id="7bce5-132">You are familiar with Windows Media encoders, and the various encoding types, particularly CBR.</span></span> <span data-ttu-id="7bce5-133">Weitere Informationen finden Sie unter [Windows Media Encoder](windows-media-encoders.md) .</span><span class="sxs-lookup"><span data-stu-id="7bce5-133">For more information, see [Windows Media Encoders](windows-media-encoders.md) .</span></span>
-   <span data-ttu-id="7bce5-134">Sie sind mit [Medien Puffern](media-buffers.md) und Bytestreams vertraut: insbesondere Datei Vorgänge mit einem Bytestream und das Schreiben des Inhalts eines Medien Puffers in einen Bytestream.</span><span class="sxs-lookup"><span data-stu-id="7bce5-134">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="terminology"></a><span data-ttu-id="7bce5-135">Begriff</span><span class="sxs-lookup"><span data-stu-id="7bce5-135">Terminology</span></span>

<span data-ttu-id="7bce5-136">In diesem Tutorial werden die folgenden Begriffe verwendet:</span><span class="sxs-lookup"><span data-stu-id="7bce5-136">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="7bce5-137">Quell Medientyp: Medientyp Objekt macht die [**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle verfügbar, die den Inhalt der Eingabedatei beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7bce5-137">Source media type: Media type object, exposes [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which describes the contents of the input file.</span></span>
-   <span data-ttu-id="7bce5-138">Audioprofil: Profil Objekt macht die [**imfasf profile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) -Schnittstelle verfügbar, die nur Audiostreams der Ausgabedatei enthält.</span><span class="sxs-lookup"><span data-stu-id="7bce5-138">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the output file.</span></span>
-   <span data-ttu-id="7bce5-139">Stream Sample: Media Sample, macht die [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle verfügbar und stellt die Mediendaten der Eingabedatei dar, die vom Encoder in einem komprimierten Zustand abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="7bce5-139">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, represents the input file's media data obtained from the encoder in a compressed state.</span></span>
-   <span data-ttu-id="7bce5-140">ContentInfo-Objekt: das [Objekt "ASF ContentInfo](asf-contentinfo-object.md)" macht die [**imfasf ContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Schnittstelle verfügbar, die das ASF-Header Objekt der Ausgabedatei darstellt.</span><span class="sxs-lookup"><span data-stu-id="7bce5-140">ContentInfo object: [ASF ContentInfo Object](asf-contentinfo-object.md), exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="7bce5-141">Daten Byte Datenstrom: das [**bytestreamobjekt macht die IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Schnittstelle verfügbar, die den gesamten Teil des ASF-Datenobjekts der Ausgabedatei darstellt.</span><span class="sxs-lookup"><span data-stu-id="7bce5-141">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="7bce5-142">Data Packet: Media Sample, macht die [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle verfügbar, die vom [ASF Multiplexer](asf-multiplexer.md)generiert wurde. stellt ein ASF-Datenpaket dar, das in den datenbytestream geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7bce5-142">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the [ASF Multiplexer](asf-multiplexer.md); represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="7bce5-143">Ausgabe Byte Datenstrom: das Byte Datenstrom Objekt macht die [**IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Schnittstelle verfügbar, die den Inhalt der Ausgabedatei enthält.</span><span class="sxs-lookup"><span data-stu-id="7bce5-143">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="7bce5-144">1. richten Sie das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="7bce5-144">1. Set up the Project</span></span>

1.  <span data-ttu-id="7bce5-145">Fügen Sie die folgenden Header in die Quelldatei ein:</span><span class="sxs-lookup"><span data-stu-id="7bce5-145">Include the following headers in your source file:</span></span>

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  <span data-ttu-id="7bce5-146">Verknüpfen Sie die folgenden Bibliotheksdateien:</span><span class="sxs-lookup"><span data-stu-id="7bce5-146">Link to the following library files:</span></span>

    -   <span data-ttu-id="7bce5-147">MF. lib</span><span class="sxs-lookup"><span data-stu-id="7bce5-147">mfplat.lib</span></span>
    -   <span data-ttu-id="7bce5-148">MF. lib</span><span class="sxs-lookup"><span data-stu-id="7bce5-148">mf.lib</span></span>
    -   <span data-ttu-id="7bce5-149">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="7bce5-149">mfuuid.lib</span></span>

3.  <span data-ttu-id="7bce5-150">Deklarieren Sie die Funktion [saferelease](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="7bce5-150">Declare the [SafeRelease](saferelease.md) function.</span></span>
4.  <span data-ttu-id="7bce5-151">Schließen Sie die cwmaencoder-Klasse in Ihr Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="7bce5-151">Include the CWmaEncoder class in your project.</span></span> <span data-ttu-id="7bce5-152">Den gesamten Quellcode dieser Klasse finden Sie unter Encoder- [Beispielcode](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="7bce5-152">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

## <a name="2-declare-helper-functions"></a><span data-ttu-id="7bce5-153">2. Deklarieren von Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="7bce5-153">2. Declare Helper Functions</span></span>

<span data-ttu-id="7bce5-154">In diesem Tutorial werden die folgenden Hilfsfunktionen verwendet, um aus einem Bytestream zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="7bce5-154">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

-   <span data-ttu-id="7bce5-155">`AppendToByteStream`: Fügt den Inhalt eines Bytestreams an einen anderen Bytestream an.</span><span class="sxs-lookup"><span data-stu-id="7bce5-155">`AppendToByteStream`: Appends the contents of one byte stream to another byte stream.</span></span>
-   <span data-ttu-id="7bce5-156">Write-bufferdebytestream: schreibt Daten aus einem Medien Puffer in einen Bytestream.</span><span class="sxs-lookup"><span data-stu-id="7bce5-156">WriteBufferToByteStream: Writes data from a media buffer to a byte stream.</span></span>

<span data-ttu-id="7bce5-157">Weitere Informationen finden Sie unter [**IMF Bytestream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="7bce5-157">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span> <span data-ttu-id="7bce5-158">Der folgende Code zeigt diese Hilfsfunktionen:</span><span class="sxs-lookup"><span data-stu-id="7bce5-158">The following code shows these helper functions:</span></span>


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



## <a name="3-open-an-audio-file"></a><span data-ttu-id="7bce5-159">3. Öffnen Sie eine Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="7bce5-159">3. Open an Audio File</span></span>

<span data-ttu-id="7bce5-160">In diesem Tutorial wird davon ausgegangen, dass Ihre Anwendung nicht komprimierte Audiodaten für die Codierung generiert.</span><span class="sxs-lookup"><span data-stu-id="7bce5-160">This tutorial assumes that your application will generate uncompressed audio for encoding.</span></span> <span data-ttu-id="7bce5-161">Zu diesem Zweck werden zwei Funktionen in diesem Tutorial deklariert:</span><span class="sxs-lookup"><span data-stu-id="7bce5-161">For that purpose, two functions are declared in this tutorial:</span></span>


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



<span data-ttu-id="7bce5-162">Die Implementierung dieser Funktionen wird dem Reader überlassen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-162">The implementation of these functions is left to the reader.</span></span>

-   <span data-ttu-id="7bce5-163">Die `OpenAudioFile` Funktion sollte die von *pszurl* angegebene Mediendatei öffnen und einen Zeiger auf einen Medientyp zurückgeben, der einen Audiostream beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7bce5-163">The `OpenAudioFile` function should open the media file specified by *pszURL* and return a pointer to a media type that describes an audio stream.</span></span>
-   <span data-ttu-id="7bce5-164">Die `GetNextAudioSample` Funktion sollte nicht komprimiertes PCM-Audiodaten aus der Datei lesen, die von geöffnet wurde `OpenAudioFile` .</span><span class="sxs-lookup"><span data-stu-id="7bce5-164">The `GetNextAudioSample` function should read uncompressed PCM audio from the file that was opened by `OpenAudioFile`.</span></span> <span data-ttu-id="7bce5-165">Wenn das Ende der Datei erreicht ist, empfängt *pbeos* den Wert " **true**".</span><span class="sxs-lookup"><span data-stu-id="7bce5-165">When the end of the file is reached, *pbEOS* receives the value **TRUE**.</span></span> <span data-ttu-id="7bce5-166">Andernfalls empfängt *ppsample* ein Medien Beispiel, das den Audiopuffer enthält.</span><span class="sxs-lookup"><span data-stu-id="7bce5-166">Otherwise, *ppSample* receives a media sample that contains the audio buffer.</span></span>

## <a name="4-configure-the-encoder"></a><span data-ttu-id="7bce5-167">4. Konfigurieren des Encoders</span><span class="sxs-lookup"><span data-stu-id="7bce5-167">4. Configure the Encoder</span></span>

<span data-ttu-id="7bce5-168">Erstellen Sie als nächstes den Encoder, konfigurieren Sie ihn so, dass CBR-codierte streambeispiele erstellt werden, und verhandeln Sie die Eingabe-und Ausgabemedien Typen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-168">Next, create the encoder, configure it to produce CBR-encoded stream samples, and negotiate the input and the output media types.</span></span>

<span data-ttu-id="7bce5-169">In Media Foundation werden Encoder (die die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle verfügbar machen) als [Media Foundation Transformationen](media-foundation-transforms.md) (MFT) implementiert.</span><span class="sxs-lookup"><span data-stu-id="7bce5-169">In Media Foundation, encoders (expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface) are implemented as [Media Foundation Transforms](media-foundation-transforms.md) (MFT).</span></span>

<span data-ttu-id="7bce5-170">In diesem Tutorial wird der Encoder in der-Klasse implementiert, die `CWmaEncoder` einen Wrapper für die MFT bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7bce5-170">In this tutorial, the encoder is implemented in the `CWmaEncoder` class that provides a wrapper for the MFT.</span></span> <span data-ttu-id="7bce5-171">Den gesamten Quellcode dieser Klasse finden Sie unter Encoder- [Beispielcode](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="7bce5-171">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

> [!Note]  
> <span data-ttu-id="7bce5-172">Optional können Sie den Codierungstyp als CBR angeben.</span><span class="sxs-lookup"><span data-stu-id="7bce5-172">You can optionally specify the encoding type as CBR.</span></span> <span data-ttu-id="7bce5-173">Standardmäßig ist der Encoder für die Verwendung der CBR-Codierung konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7bce5-173">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="7bce5-174">Weitere Informationen finden Sie unter [Konstante Bitrate-Codierung](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="7bce5-174">For more information, see [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="7bce5-175">Sie können zusätzliche Eigenschaften abhängig vom Codierungstyp festlegen. Informationen zu den Eigenschaften, die für einen Codierungs Modus spezifisch sind, finden Sie unter [Qualitäts basierte Variablen-](quality-based-variable-bit-rate--vbr--encoding.md)Bitrate-Codierung, [unbeschränkte Variablen Bitrate-Codierung](unconstrained-variable-bit-rate--vbr--encoding.md)und [Maximale Codierung der Variablen Bitrate](peak-constrained-variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="7bce5-175">You can set additional properties depending on the type of encoding, for information about the properties that are specific to an encoding mode, see [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md), [Unconstrained Variable Bit Rate Encoding](unconstrained-variable-bit-rate--vbr--encoding.md), and [Peak-Constrained Variable Bit Rate Encoding](peak-constrained-variable-bit-rate--vbr--encoding.md).</span></span>

 


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



## <a name="5-create-the-asf-contentinfo-object"></a><span data-ttu-id="7bce5-176">5. Erstellen Sie das Objekt "ASF ContentInfo".</span><span class="sxs-lookup"><span data-stu-id="7bce5-176">5. Create the ASF ContentInfo object.</span></span>

<span data-ttu-id="7bce5-177">Das [Objekt "ASF ContentInfo](asf-contentinfo-object.md) " enthält Informationen zu den verschiedenen Header Objekten der Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="7bce5-177">The [ASF ContentInfo Object](asf-contentinfo-object.md) contains information about the various header objects of the output file.</span></span>

<span data-ttu-id="7bce5-178">Erstellen Sie zunächst ein ASF-Profil für den Audiostream:</span><span class="sxs-lookup"><span data-stu-id="7bce5-178">First, create an ASF profile for the audio stream:</span></span>

1.  <span data-ttu-id="7bce5-179">Rufen Sie [**mfkreateasfprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) auf, um ein leeres ASF-Profil Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-179">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty ASF profile object.</span></span> <span data-ttu-id="7bce5-180">Das ASF-Profil macht die [**imfasf profile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7bce5-180">The ASF profile exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="7bce5-181">Weitere Informationen finden Sie unter [Erstellen und Konfigurieren von ASF-Streams](creating-and-configuring-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="7bce5-181">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>
2.  <span data-ttu-id="7bce5-182">Das codierte Audioformat aus dem-Objekt zu erhalten `CWmaEncoder` .</span><span class="sxs-lookup"><span data-stu-id="7bce5-182">Get the encoded audio format from the `CWmaEncoder` object.</span></span>
3.  <span data-ttu-id="7bce5-183">Rufen Sie [**imfasfprofile:: kreatestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) auf, um einen neuen Datenstrom für das ASF-Profil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-183">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) to create a new stream for the ASF profile.</span></span> <span data-ttu-id="7bce5-184">Übergeben Sie einen Zeiger auf die [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle, die das Streamformat darstellt.</span><span class="sxs-lookup"><span data-stu-id="7bce5-184">Pass in a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which represents the stream format.</span></span>
4.  <span data-ttu-id="7bce5-185">Aufrufen von [**imfasfstreamconfig:: setstreamnumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) zum Zuweisen eines Datenstrom Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="7bce5-185">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a stream identifier.</span></span>
5.  <span data-ttu-id="7bce5-186">Legen Sie die Parameter "Leaky Bucket" fest, indem Sie das [**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) -Attribut für das Stream-Objekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-186">Set the "leaky bucket" parameters by setting the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream object.</span></span>
6.  <span data-ttu-id="7bce5-187">Aufrufen von [**imfasfprofile:: setStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) , um dem Profil den neuen Stream hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-187">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the new stream to the profile.</span></span>

<span data-ttu-id="7bce5-188">Erstellen Sie nun das Objekt "ASF ContentInfo" wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7bce5-188">Now create the ASF ContentInfo object as follows:</span></span>

1.  <span data-ttu-id="7bce5-189">Rufen Sie [**mfkreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) auf, um ein leeres ContentInfo-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-189">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="7bce5-190">Aufrufen von [**imfasfcontentinfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) , um das ASF-Profil festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-190">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to set the ASF profile.</span></span>

<span data-ttu-id="7bce5-191">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="7bce5-191">The following code shows these steps:</span></span>


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



## <a name="6-create-the-asf-multiplexer"></a><span data-ttu-id="7bce5-192">6. Erstellen des ASF Multiplexer</span><span class="sxs-lookup"><span data-stu-id="7bce5-192">6. Create the ASF Multiplexer</span></span>

<span data-ttu-id="7bce5-193">Der [ASF Multiplexer](asf-multiplexer.md) generiert ASF-Datenpakete.</span><span class="sxs-lookup"><span data-stu-id="7bce5-193">The [ASF Multiplexer](asf-multiplexer.md) generates ASF data packets.</span></span>

1.  <span data-ttu-id="7bce5-194">Rufen Sie [**mfkreateasfmultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) auf, um den ASF Multiplexer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-194">Call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) to create the ASF multiplexer.</span></span>
2.  <span data-ttu-id="7bce5-195">Zum Initialisieren des Multiplexer muss [**imfasfmultiplexer:: Initialisieren**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7bce5-195">Call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) to initialize the multiplexer.</span></span> <span data-ttu-id="7bce5-196">Übergeben Sie einen Zeiger auf das Objekt "ASF Content Info", das im vorherigen Abschnitt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7bce5-196">Pass in a pointer to the ASF Content Info object, which was created in the previous section.</span></span>
3.  <span data-ttu-id="7bce5-197">[**Imfasfmultiplexer:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) aufrufen, um das Flag für die **Automatische Anpassung der mfasf \_ Multiplexer- \_ \_ Bitrate** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-197">Call [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span> <span data-ttu-id="7bce5-198">Wenn diese Einstellung verwendet wird, passt der Multiplexer die Bitrate des ASF-Inhalts automatisch an die Merkmale der zu multipleckenden Streams an.</span><span class="sxs-lookup"><span data-stu-id="7bce5-198">When this setting is used, the multiplexer automatically adjusts the bit rate of the ASF content to match the characteristics of the streams being multiplexed.</span></span>


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



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="7bce5-199">7. Generieren neuer ASF-Datenpakete</span><span class="sxs-lookup"><span data-stu-id="7bce5-199">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="7bce5-200">Generieren Sie als nächstes ASF-Datenpakete für die neue Datei.</span><span class="sxs-lookup"><span data-stu-id="7bce5-200">Next, generate ASF data packets for the new file.</span></span> <span data-ttu-id="7bce5-201">Diese Datenpakete bilden das endgültige ASF-Datenobjekt für die neue Datei.</span><span class="sxs-lookup"><span data-stu-id="7bce5-201">These data packets will constitute the final ASF Data Object for the new file.</span></span> <span data-ttu-id="7bce5-202">So generieren Sie neue ASF-Datenpakete:</span><span class="sxs-lookup"><span data-stu-id="7bce5-202">To generate new ASF data packets:</span></span>

1.  <span data-ttu-id="7bce5-203">Rufen Sie [**mfkreatetempfile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) auf, um einen temporären Bytestream zum Speichern der ASF-Datenpakete zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-203">Call [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) to create a temporary byte stream to hold the ASF data packets.</span></span>
2.  <span data-ttu-id="7bce5-204">Ruft die Anwendungs definierte `GetNextAudioSample` Funktion auf, um unkomprimierte Audiodaten für den Encoder abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-204">Call the application-defined `GetNextAudioSample` function to get uncompressed audio data for the encoder.</span></span>
3.  <span data-ttu-id="7bce5-205">Übergeben Sie die unkomprimierte Audiodatei zur Komprimierung an den Encoder.</span><span class="sxs-lookup"><span data-stu-id="7bce5-205">Pass the uncompressed audio to the encoder for compression.</span></span> <span data-ttu-id="7bce5-206">Weitere Informationen finden Sie unter [Verarbeiten von Daten im Encoder](processing-data-in-the-encoder.md) .</span><span class="sxs-lookup"><span data-stu-id="7bce5-206">For more information, see [Processing Data in the Encoder](processing-data-in-the-encoder.md)</span></span>
4.  <span data-ttu-id="7bce5-207">Nennen Sie [**imfasfmultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) , um die komprimierten Audiobeispiele an den ASF Multiplexer für packetisierung zu senden.</span><span class="sxs-lookup"><span data-stu-id="7bce5-207">Call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the compressed audio samples to the ASF multiplexer for packetization.</span></span>
5.  <span data-ttu-id="7bce5-208">Holen Sie sich die ASF-Pakete aus dem Multiplexer, und schreiben Sie Sie in den temporären Byte Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="7bce5-208">Get the ASF packets from the multiplexer and write them to the temporary byte stream.</span></span> <span data-ttu-id="7bce5-209">Weitere Informationen finden Sie unter [Erstellen neuer ASF-Datenpakete](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="7bce5-209">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>
6.  <span data-ttu-id="7bce5-210">Wenn Sie das Ende des Quelldaten Stroms erreicht haben, müssen Sie den Encoder entladen und die verbleibenden komprimierten Beispiele aus dem Encoder abrufen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-210">When you reach the end of the source stream, drain the encoder and pull the remaining compressed samples from the encoder.</span></span> <span data-ttu-id="7bce5-211">Weitere Informationen zum Entleeren von MFT finden Sie unter [Grundlegendes MFT-Verarbeitungsmodell](basic-mft-processing-model.md).</span><span class="sxs-lookup"><span data-stu-id="7bce5-211">For more information about draining an MFT, see [Basic MFT Processing Model](basic-mft-processing-model.md).</span></span>
7.  <span data-ttu-id="7bce5-212">Nachdem alle Beispiele an den Multiplexer gesendet wurden, rufen Sie [**imfasfmultiplexer:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) auf, und rufen Sie die verbleibenden ASF-Pakete aus dem Multiplexer ab.</span><span class="sxs-lookup"><span data-stu-id="7bce5-212">After all samples are sent to the multiplexer, call [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) and pull the remaining ASF packets from the multiplexer.</span></span>
8.  <span data-ttu-id="7bce5-213">[**Imfasfmultiplexer:: End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-213">Call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).</span></span>

<span data-ttu-id="7bce5-214">Der folgende Code generiert ASF-Datenpakete.</span><span class="sxs-lookup"><span data-stu-id="7bce5-214">The following code generates ASF data packets.</span></span> <span data-ttu-id="7bce5-215">Die-Funktion gibt einen Zeiger auf einen Bytestream zurück, der das ASF-Datenobjekt enthält.</span><span class="sxs-lookup"><span data-stu-id="7bce5-215">The function returns a pointer to a byte stream that contains the ASF Data Object.</span></span>


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



<span data-ttu-id="7bce5-216">Code für die `GenerateASFDataPackets` Funktion finden Sie im Thema [Erstellen neuer ASF-Datenpakete](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="7bce5-216">Code for the `GenerateASFDataPackets` function is shown in the topic [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="8-write-the-asf-file"></a><span data-ttu-id="7bce5-217">8. Schreiben der ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="7bce5-217">8. Write the ASF File</span></span>

<span data-ttu-id="7bce5-218">Schreiben Sie als nächstes den ASF-Header in einen Medien Puffer, indem Sie [**imfasfcontentinfo:: generateheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-218">Next, write the ASF header to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="7bce5-219">Diese Methode konvertiert die im ContentInfo-Objekt gespeicherten Daten im Objekt Format des ASF-Headers in Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="7bce5-219">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="7bce5-220">Weitere Informationen finden Sie unter [Erstellen eines neuen ASF-Header Objekts](generating-a-new-asf-header-object.md).</span><span class="sxs-lookup"><span data-stu-id="7bce5-220">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="7bce5-221">Nachdem das neue ASF-Header Objekt generiert wurde, erstellen Sie einen Bytestream für die Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="7bce5-221">After the new ASF Header Object has been generated, create a byte stream for the output file.</span></span> <span data-ttu-id="7bce5-222">Schreiben Sie zuerst das Header Objekt in den ausgabebytestream.</span><span class="sxs-lookup"><span data-stu-id="7bce5-222">First write the Header Object to the output byte stream.</span></span> <span data-ttu-id="7bce5-223">Befolgen Sie das Header Objekt mit dem Datenobjekt, das im datenbytestream enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7bce5-223">Follow the Header Object with the Data Object contained in the data byte stream.</span></span>


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



## <a name="9-define-the-entry-point-function"></a><span data-ttu-id="7bce5-224">9. Definieren der Entry-Point-Funktion</span><span class="sxs-lookup"><span data-stu-id="7bce5-224">9. Define the Entry-Point Function</span></span>

<span data-ttu-id="7bce5-225">Nun können Sie die vorherigen Schritte in eine komplette Anwendung einfügen.</span><span class="sxs-lookup"><span data-stu-id="7bce5-225">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="7bce5-226">Initialisieren Sie vor dem Verwenden eines der Media Foundation Objekte die Media Foundation Plattform durch Aufrufen von [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="7bce5-226">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="7bce5-227">Wenn Sie den Vorgang abgeschlossen haben, wenden Sie sich an [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="7bce5-227">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="7bce5-228">Weitere Informationen finden Sie unter [Initialisieren von Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="7bce5-228">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="7bce5-229">Der folgende Code zeigt die komplette Konsolenanwendung.</span><span class="sxs-lookup"><span data-stu-id="7bce5-229">The following code shows the complete console application.</span></span> <span data-ttu-id="7bce5-230">Das Befehlszeilenargument gibt den Namen der zu konvertierenden Datei und den Namen der neuen Audiodatei an.</span><span class="sxs-lookup"><span data-stu-id="7bce5-230">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7bce5-231">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7bce5-231">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bce5-232">Wmcontainer-ASF-Komponenten</span><span class="sxs-lookup"><span data-stu-id="7bce5-232">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="7bce5-233">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7bce5-233">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



