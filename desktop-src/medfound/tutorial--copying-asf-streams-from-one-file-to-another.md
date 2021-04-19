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
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a><span data-ttu-id="df17b-103">Tutorial: Kopieren von ASF-Streams mithilfe von wmcontainer-Objekten</span><span class="sxs-lookup"><span data-stu-id="df17b-103">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>

<span data-ttu-id="df17b-104">Eine Möglichkeit zum Erstellen einer ASF-Datei besteht darin, die ASF-Streams aus einer vorhandenen Datei zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="df17b-104">One way to create an ASF file is to copy ASF streams from an existing file.</span></span> <span data-ttu-id="df17b-105">Zu diesem Zweck können Sie die Mediendaten aus der Quelldatei abrufen und in die Ausgabedatei schreiben.</span><span class="sxs-lookup"><span data-stu-id="df17b-105">To do this, you can retrieve the media data from the source file and write to the output file.</span></span> <span data-ttu-id="df17b-106">Wenn die Quelldatei eine ASF-Datei ist, können Sie streambeispiele kopieren, ohne Sie zu dekomprimieren und erneut zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="df17b-106">If the source file is an ASF file, you can copy stream samples without decompressing and recompressing them.</span></span>

<span data-ttu-id="df17b-107">In diesem Tutorial wird dieses Szenario veranschaulicht, indem der erste Audiostream aus einer ASF-audiovideodatei (. wmv) extrahiert und in eine neue ASF-Audiodatei (. WMA) kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="df17b-107">This tutorial demonstrates this scenario by extracting the first audio stream from an ASF audio-video file (.wmv) and copying it to a new ASF audio file (.wma).</span></span> <span data-ttu-id="df17b-108">In diesem Tutorial erstellen Sie eine Konsolenanwendung, die die Eingabe-und Ausgabe Dateinamen als Argumente annimmt.</span><span class="sxs-lookup"><span data-stu-id="df17b-108">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="df17b-109">Die Anwendung verwendet den ASF-Splitter, um die eingabestreambeispiele zu analysieren, und sendet Sie dann an den ASF Multiplexer, um die ASF-Datenpakete für den Audiostream zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="df17b-109">The application uses the ASF Splitter to parse the input stream samples and then sends them to the ASF Multiplexer to write the ASF data packets for the audio stream.</span></span>

<span data-ttu-id="df17b-110">Folgende Themen werden in diesem Lernprogramm behandelt:</span><span class="sxs-lookup"><span data-stu-id="df17b-110">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="df17b-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="df17b-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="df17b-112">Terminologie</span><span class="sxs-lookup"><span data-stu-id="df17b-112">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="df17b-113">1. richten Sie das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="df17b-113">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="df17b-114">2. Deklarieren von Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="df17b-114">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="df17b-115">3. Öffnen Sie die Eingabe-ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="df17b-115">3. Open the Input ASF File</span></span>](#3-open-the-input-asf-file)
-   [<span data-ttu-id="df17b-116">4. Initialisieren von Objekten für die Eingabedatei</span><span class="sxs-lookup"><span data-stu-id="df17b-116">4. Initialize Objects for the Input File</span></span>](#4-initialize-objects-for-the-input-file)
-   [<span data-ttu-id="df17b-117">5. Erstellen eines audioprofils</span><span class="sxs-lookup"><span data-stu-id="df17b-117">5. Create an Audio Profile</span></span>](#5-create-an-audio-profile)
-   [<span data-ttu-id="df17b-118">6. Initialisieren von Objekten für die Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="df17b-118">6. Initialize Objects for the Output File</span></span>](#6-initialize-objects-for-the-output-file)
-   [<span data-ttu-id="df17b-119">7. Generieren neuer ASF-Datenpakete</span><span class="sxs-lookup"><span data-stu-id="df17b-119">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="df17b-120">8. Schreiben der ASF-Objekte in der neuen Datei</span><span class="sxs-lookup"><span data-stu-id="df17b-120">8. Write the ASF Objects in the New File</span></span>](#8-write-the-asf-objects-in-the-new-file)
-   [<span data-ttu-id="df17b-121">9 Schreiben der Entry-Point-Funktion</span><span class="sxs-lookup"><span data-stu-id="df17b-121">9 Write the Entry-Point Function</span></span>](#9-write-the-entry-point-function)
-   [<span data-ttu-id="df17b-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df17b-122">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="df17b-123">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="df17b-123">Prerequisites</span></span>

<span data-ttu-id="df17b-124">In diesem Tutorial wird Folgendes vorausgesetzt:</span><span class="sxs-lookup"><span data-stu-id="df17b-124">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="df17b-125">Sie sind mit der Struktur einer ASF-Datei und den von Media Foundation bereitgestellten Komponenten vertraut, um mit der Verwendung von ASF-Objekten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="df17b-125">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="df17b-126">Zu diesen Komponenten gehören ContentInfo-, Splitter-, Multiplexer-und Profile-Objekte.</span><span class="sxs-lookup"><span data-stu-id="df17b-126">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="df17b-127">Weitere Informationen finden Sie unter [wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="df17b-127">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="df17b-128">Sie kennen den Prozess der Verarbeitung des ASF-Header Objekts und der ASF-Datenpakete einer vorhandenen Datei und das Erstellen von komprimierten streambeispielen mithilfe des Splitters.</span><span class="sxs-lookup"><span data-stu-id="df17b-128">You are familiar with the process of parsing the ASF Header Object and the ASF data packets of an existing file and generating compressed stream samples by using the splitter.</span></span> <span data-ttu-id="df17b-129">Weitere Informationen finden Sie unter [Tutorial: Lesen einer ASF-Datei](tutorial--reading-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="df17b-129">For more information see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>
-   <span data-ttu-id="df17b-130">Sie sind mit Medien Puffern und Bytestreams vertraut: insbesondere Datei Vorgänge mit einem Bytestream und das Schreiben des Inhalts eines Medien Puffers in einen Bytestream.</span><span class="sxs-lookup"><span data-stu-id="df17b-130">You are familiar with media buffers and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer into a byte stream.</span></span> <span data-ttu-id="df17b-131">(Siehe [2. Deklarieren von Hilfsfunktionen](#2-declare-helper-functions).)</span><span class="sxs-lookup"><span data-stu-id="df17b-131">(See [2. Declare Helper Functions](#2-declare-helper-functions).)</span></span>

## <a name="terminology"></a><span data-ttu-id="df17b-132">Begriff</span><span class="sxs-lookup"><span data-stu-id="df17b-132">Terminology</span></span>

<span data-ttu-id="df17b-133">In diesem Tutorial werden die folgenden Begriffe verwendet:</span><span class="sxs-lookup"><span data-stu-id="df17b-133">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="df17b-134">Quelle-Byte-Stream: das [**bytestreamobjekt macht die IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Schnittstelle verfügbar, die den Inhalt der Eingabedatei enthält.</span><span class="sxs-lookup"><span data-stu-id="df17b-134">Source byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the input file.</span></span>
-   <span data-ttu-id="df17b-135">Quell-ContentInfo-Objekt: das ContentInfo-Objekt macht die [**imfasf ContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Schnittstelle verfügbar, die das ASF-Header Objekt der Eingabedatei darstellt.</span><span class="sxs-lookup"><span data-stu-id="df17b-135">Source ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the input file.</span></span>
-   <span data-ttu-id="df17b-136">Audioprofil: Profil Objekt macht die [**imfasf profile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) -Schnittstelle verfügbar, die nur Audiostreams der Eingabedatei enthält.</span><span class="sxs-lookup"><span data-stu-id="df17b-136">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the input file.</span></span>
-   <span data-ttu-id="df17b-137">Stream Sample: Media Sample, macht eine [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle verfügbar, die vom Splitter generiert wurde, stellt die Mediendaten des ausgewählten Streams dar, die aus der Eingabedatei im komprimierten Zustand abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="df17b-137">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the splitter represents the selected stream's media data obtained from the input file in compressed state.</span></span>
-   <span data-ttu-id="df17b-138">Output ContentInfo Object: das ContentInfo-Objekt macht die [**imfasf ContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Schnittstelle verfügbar, die das ASF-Header Objekt der Ausgabedatei darstellt.</span><span class="sxs-lookup"><span data-stu-id="df17b-138">Output ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="df17b-139">Daten Byte Datenstrom: das [**bytestreamobjekt macht die IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Schnittstelle verfügbar, die den gesamten Teil des ASF-Datenobjekts der Ausgabedatei darstellt.</span><span class="sxs-lookup"><span data-stu-id="df17b-139">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="df17b-140">Data Packet: Media Sample, macht die von Multiplexer generierte [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle und stellt ein ASF-Datenpaket dar, das in den datenbytestream geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="df17b-140">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the multiplexer represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="df17b-141">Ausgabe Byte Datenstrom: das Byte Datenstrom Objekt macht die [**IMF Bytestream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) -Schnittstelle verfügbar, die den Inhalt der Ausgabedatei enthält.</span><span class="sxs-lookup"><span data-stu-id="df17b-141">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="df17b-142">1. richten Sie das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="df17b-142">1. Set up the Project</span></span>

<span data-ttu-id="df17b-143">Fügen Sie die folgenden Header in die Quelldatei ein:</span><span class="sxs-lookup"><span data-stu-id="df17b-143">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



<span data-ttu-id="df17b-144">Verknüpfen Sie die folgenden Bibliotheksdateien:</span><span class="sxs-lookup"><span data-stu-id="df17b-144">Link to the following library files:</span></span>

-   <span data-ttu-id="df17b-145">MF. lib</span><span class="sxs-lookup"><span data-stu-id="df17b-145">mfplat.lib</span></span>
-   <span data-ttu-id="df17b-146">MF. lib</span><span class="sxs-lookup"><span data-stu-id="df17b-146">mf.lib</span></span>
-   <span data-ttu-id="df17b-147">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="df17b-147">mfuuid.lib</span></span>

<span data-ttu-id="df17b-148">Deklarieren Sie die [saferelease](saferelease.md) -Funktion:</span><span class="sxs-lookup"><span data-stu-id="df17b-148">Declare the [SafeRelease](saferelease.md) function:</span></span>


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



## <a name="2-declare-helper-functions"></a><span data-ttu-id="df17b-149">2. Deklarieren von Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="df17b-149">2. Declare Helper Functions</span></span>

<span data-ttu-id="df17b-150">In diesem Tutorial werden die folgenden Hilfsfunktionen verwendet, um aus einem Bytestream zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="df17b-150">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

<span data-ttu-id="df17b-151">Die `AllocReadFromByteStream` -Funktion liest Daten aus einem Bytestream und weist einen neuen Medien Puffer zum Speichern der Daten zu.</span><span class="sxs-lookup"><span data-stu-id="df17b-151">The `AllocReadFromByteStream` function reads data from a byte stream and allocates a new media buffer to hold the data.</span></span> <span data-ttu-id="df17b-152">Weitere Informationen finden Sie unter [**IMF Bytestream:: Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).</span><span class="sxs-lookup"><span data-stu-id="df17b-152">For more information, see [**IMFByteStream::Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).</span></span>


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



<span data-ttu-id="df17b-153">Die- `WriteBufferToByteStream` Funktion schreibt Daten aus einem Medien Puffer in einen Bytestream.</span><span class="sxs-lookup"><span data-stu-id="df17b-153">The `WriteBufferToByteStream` function writes data from a media buffer to a byte stream.</span></span> <span data-ttu-id="df17b-154">Weitere Informationen finden Sie unter [**IMF Bytestream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="df17b-154">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>


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



<span data-ttu-id="df17b-155">Die- `AppendToByteStream` Funktion fügt den Inhalt eines Bytestreams an einen anderen an:</span><span class="sxs-lookup"><span data-stu-id="df17b-155">The `AppendToByteStream` function appends the contents of one byte stream to another:</span></span>


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



## <a name="3-open-the-input-asf-file"></a><span data-ttu-id="df17b-156">3. Öffnen Sie die Eingabe-ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="df17b-156">3. Open the Input ASF File</span></span>

<span data-ttu-id="df17b-157">Öffnen Sie die Eingabedatei, indem Sie die [**mfcreatefile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="df17b-157">Open the input file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="df17b-158">Die-Methode gibt einen Zeiger auf das bytestreamobjekt zurück, das den Inhalt der Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="df17b-158">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="df17b-159">Der Dateiname wird vom Benutzer über Befehlszeilenargumente der Anwendung angegeben.</span><span class="sxs-lookup"><span data-stu-id="df17b-159">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="df17b-160">Im folgenden Beispielcode wird ein Dateiname verwendet, und es wird ein Zeiger auf ein bytestreamobjekt zurückgegeben, das zum Lesen der Datei verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="df17b-160">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a><span data-ttu-id="df17b-161">4. Initialisieren von Objekten für die Eingabedatei</span><span class="sxs-lookup"><span data-stu-id="df17b-161">4. Initialize Objects for the Input File</span></span>

<span data-ttu-id="df17b-162">Als Nächstes erstellen und initialisieren Sie das Quell-ContentInfo-Objekt und den Splitter zum Erstellen von streambeispielen.</span><span class="sxs-lookup"><span data-stu-id="df17b-162">Next, you will create and initialize the source ContentInfo object and the splitter for generating stream samples.</span></span>

<span data-ttu-id="df17b-163">Dieser in Schritt 2 erstellte Quell Byte Datenstrom wird verwendet, um das ASF-Header Objekt zu analysieren und das Quell-ContentInfo-Objekt aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="df17b-163">This source byte stream created in step 2 will be used to parse the ASF Header Object and populate the source ContentInfo object.</span></span> <span data-ttu-id="df17b-164">Dieses Objekt wird verwendet, um den Splitter zu initialisieren, um die Analyse der ASF-Datenpakete für den Audiostream in der Eingabedatei zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="df17b-164">This object will be used to initialize the splitter to facilitate the parsing of the ASF data packets for the audio stream in the input file.</span></span> <span data-ttu-id="df17b-165">Außerdem rufen Sie die Länge des ASF-Datenobjekts in der Eingabedatei und den Offset zum ersten Paket der ASF-Daten in Relation zum Anfang der Datei ab.</span><span class="sxs-lookup"><span data-stu-id="df17b-165">You will also retrieve the length of the ASF Data Object in the input file and the offset to the first ASF data packet relative to the start of the file.</span></span> <span data-ttu-id="df17b-166">Diese Attribute werden vom Splitter verwendet, um audiostreambeispiele zu generieren.</span><span class="sxs-lookup"><span data-stu-id="df17b-166">These attributes will be used by the splitter to generate audio stream samples.</span></span>

<span data-ttu-id="df17b-167">So erstellen und initialisieren Sie die ASF-Komponenten für die Eingabedatei:</span><span class="sxs-lookup"><span data-stu-id="df17b-167">To create and initialize ASF components for the input file:</span></span>

1.  <span data-ttu-id="df17b-168">Rufen Sie [**mfkreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) auf, um das ContentInfo-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="df17b-168">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create the ContentInfo object.</span></span> <span data-ttu-id="df17b-169">Diese Funktion gibt einen Zeiger auf die [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="df17b-169">This function returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="df17b-170">[**Imfasfcontentinfo::P arsheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) zum Analysieren des ASF-Headers aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="df17b-170">Call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) to parse the ASF Header.</span></span> <span data-ttu-id="df17b-171">Weitere Informationen zu diesem Schritt finden Sie unter [Lesen des ASF-Header Objekts einer vorhandenen Datei](reading-the-asf-header-object-of-an-existing-file.md).</span><span class="sxs-lookup"><span data-stu-id="df17b-171">For more information about this step, see [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span>
3.  <span data-ttu-id="df17b-172">Rufen Sie [**mfkreateasfsplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) auf, um das ASF-Splitter Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="df17b-172">Call [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) to create the ASF splitter object.</span></span> <span data-ttu-id="df17b-173">Diese Funktion gibt einen Zeiger auf die [**imfasfsplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="df17b-173">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
4.  <span data-ttu-id="df17b-174">Nennen Sie [**imfasfsplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), und übergeben Sie den [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="df17b-174">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), passing in the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)pointer.</span></span> <span data-ttu-id="df17b-175">Weitere Informationen zu diesem Schritt finden Sie unter [Erstellen des ASF-Splitter Objekts](creating-the-asf-splitter-object.md).</span><span class="sxs-lookup"><span data-stu-id="df17b-175">For more information about this step, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).</span></span>
5.  <span data-ttu-id="df17b-176">Aufrufen von [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) , um einen Präsentations Deskriptor für die ASF-Datei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="df17b-176">Call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) to get a presentation descriptor for the ASF file.</span></span>
6.  <span data-ttu-id="df17b-177">Sie erhalten den Wert des MF-Attribut " [**MF \_ PD \_ ASF \_ Data \_ Start \_ Offset**](mf-pd-asf-data-start-offset-attribute.md) " aus dem Präsentations Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="df17b-177">Get the value of the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="df17b-178">Dieser Wert ist der Speicherort des ASF-Datenobjekts in der Datei, als Byte-Offset vom Anfang der Datei.</span><span class="sxs-lookup"><span data-stu-id="df17b-178">This value is the location of the ASF Data Object in the file, as a byte offset from the start of the file.</span></span>
7.  <span data-ttu-id="df17b-179">Den Wert des [**\_ \_ \_ Daten \_ Längen**](mf-pd-asf-data-length-attribute.md) Attributs der MF-PD-Datei aus dem Präsentations Deskriptor erhalten.</span><span class="sxs-lookup"><span data-stu-id="df17b-179">Get the value of the [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="df17b-180">Dieser Wert ist die Gesamtgröße des ASF-Datenobjekts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="df17b-180">This value is the total size of the ASF Data Object, in bytes.</span></span> <span data-ttu-id="df17b-181">Weitere Informationen finden Sie unter [erhalten von Informationen aus den ASF-Header Objekten](getting-information-from-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="df17b-181">For more information, see [Getting Information from ASF Header Objects](getting-information-from-asf-header-objects.md).</span></span>

<span data-ttu-id="df17b-182">Der folgende Beispielcode zeigt eine Funktion, die alle Schritte konsolidiert.</span><span class="sxs-lookup"><span data-stu-id="df17b-182">The following example code shows a function that consolidates all of the steps.</span></span> <span data-ttu-id="df17b-183">Diese Funktion nimmt einen Zeiger auf den Quell Byte Datenstrom und gibt Zeiger auf das Quell-ContentInfo-Objekt und den Splitter zurück.</span><span class="sxs-lookup"><span data-stu-id="df17b-183">This function takes a pointer to the source byte stream and returns pointers to the source ContentInfo object and the splitter.</span></span> <span data-ttu-id="df17b-184">Außerdem erhält Sie die Länge und die Offsets für das ASF-Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="df17b-184">Also, it receives the length and offsets to the ASF Data Object.</span></span>


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



## <a name="5-create-an-audio-profile"></a><span data-ttu-id="df17b-185">5. Erstellen eines audioprofils</span><span class="sxs-lookup"><span data-stu-id="df17b-185">5. Create an Audio Profile</span></span>

<span data-ttu-id="df17b-186">Als Nächstes erstellen Sie ein Profil Objekt für die Eingabedatei, indem Sie es aus dem ContentInfo-Quell Objekt abrufen.</span><span class="sxs-lookup"><span data-stu-id="df17b-186">Next, you will create a profile object for the input file by obtaining it from the source ContentInfo object.</span></span> <span data-ttu-id="df17b-187">Anschließend konfigurieren Sie das Profil so, dass es nur die Audiostreams der Eingabedatei enthält.</span><span class="sxs-lookup"><span data-stu-id="df17b-187">You will then configure the profile so that it contains only the audio streams of the input file.</span></span> <span data-ttu-id="df17b-188">Auflisten Sie zu diesem Zweck die Streams, und entfernen Sie nicht-Audiodatenströme aus dem Profil.</span><span class="sxs-lookup"><span data-stu-id="df17b-188">To do this, enumerate the streams and remove non-audio streams from the profile.</span></span> <span data-ttu-id="df17b-189">Das audioprofilobjekt wird später in diesem Tutorial verwendet, um das ContentInfo-Ausgabe Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="df17b-189">The audio profile object will be used later in this tutorial to initialize the output ContentInfo object.</span></span>

<span data-ttu-id="df17b-190">So erstellen Sie ein Audioprofil</span><span class="sxs-lookup"><span data-stu-id="df17b-190">To create an audio profile</span></span>

1.  <span data-ttu-id="df17b-191">Rufen Sie das Profil Objekt für die Eingabedatei aus dem ContentInfo-Quell Objekt ab, indem Sie [**imfasfcontentinfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="df17b-191">Get the profile object for the input file from the source ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="df17b-192">Die-Methode gibt einen Zeiger auf ein Profil Objekt zurück, das alle Streams in der Eingabedatei enthält.</span><span class="sxs-lookup"><span data-stu-id="df17b-192">The method returns a pointer to a profile object that contains all of the streams in the input file.</span></span> <span data-ttu-id="df17b-193">Weitere Informationen finden Sie unter [Erstellen eines ASF-Profils](creating-an-asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="df17b-193">For more information see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
2.  <span data-ttu-id="df17b-194">Entfernen Sie alle gegenseitigen Ausschluss Objekte aus dem Profil.</span><span class="sxs-lookup"><span data-stu-id="df17b-194">Remove any mutual exclusion objects from the profile.</span></span> <span data-ttu-id="df17b-195">Dieser Schritt ist erforderlich, da nicht-Audiodatenströme aus dem Profil entfernt werden, wodurch die gegenseitigen Ausschluss Objekte ungültig werden könnten.</span><span class="sxs-lookup"><span data-stu-id="df17b-195">This step is required because non-audio streams will be removed from the profile, which could invalidate the mutual exclusion objects.</span></span>
3.  <span data-ttu-id="df17b-196">Entfernen Sie alle nicht-Audiodatenströme aus dem Profil wie folgt:</span><span class="sxs-lookup"><span data-stu-id="df17b-196">Remove all non-audio streams from the profile, as follows:</span></span>
    -   <span data-ttu-id="df17b-197">Aufrufen von [**imfasfprofile:: getstreamcount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) , um die Anzahl der Streams zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="df17b-197">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams.</span></span>
    -   <span data-ttu-id="df17b-198">Aufrufen Sie in einer-Schleife [**imfasfprofile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) , um jeden Stream nach Index abzurufen.</span><span class="sxs-lookup"><span data-stu-id="df17b-198">In a loop, call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) to get each stream by index.</span></span>
    -   <span data-ttu-id="df17b-199">Aufrufen von [**imfasfstreamconfig:: getstreamtype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) zum Abrufen des streamtyps.</span><span class="sxs-lookup"><span data-stu-id="df17b-199">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the stream type.</span></span>
    -   <span data-ttu-id="df17b-200">Bei nicht-Audiodatenströmen wird [**imfasfprofile:: removestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) aufgerufen, um den Datenstrom zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="df17b-200">For non-audio streams, call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) to remove the stream.</span></span>
4.  <span data-ttu-id="df17b-201">Speichert die streamnummer des ersten Audiostreams.</span><span class="sxs-lookup"><span data-stu-id="df17b-201">Store the stream number of the first audio stream.</span></span> <span data-ttu-id="df17b-202">Diese wird für den Splitter ausgewählt, um streambeispiele zu generieren.</span><span class="sxs-lookup"><span data-stu-id="df17b-202">This will be selected on the splitter to generate stream samples.</span></span> <span data-ttu-id="df17b-203">Wenn die streamnummer 0 (null) ist, kann der Aufrufer annehmen, dass es keine audiodatenstreamdatei gab.</span><span class="sxs-lookup"><span data-stu-id="df17b-203">If the stream number is zero, the caller can assume that there were no audio streams file.</span></span>

<span data-ttu-id="df17b-204">Der folgende Code führt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="df17b-204">The following code these steps:</span></span>


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



<span data-ttu-id="df17b-205">Die- `RemoveMutexes` Funktion entfernt alle gegenseitigen Ausschluss Objekte aus dem Profil:</span><span class="sxs-lookup"><span data-stu-id="df17b-205">The `RemoveMutexes` function removes any mutual exclusion objects from the profile:</span></span>


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



## <a name="6-initialize-objects-for-the-output-file"></a><span data-ttu-id="df17b-206">6. Initialisieren von Objekten für die Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="df17b-206">6. Initialize Objects for the Output File</span></span>

<span data-ttu-id="df17b-207">Als Nächstes erstellen Sie das ContentInfo-Ausgabe Objekt und den Multiplexer zum Erstellen von Datenpaketen für die Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="df17b-207">Next, you will create the output ContentInfo object and the multiplexer for generating data packets for the output file.</span></span>

<span data-ttu-id="df17b-208">Das in Schritt 4 erstellte Audioprofil wird zum Auffüllen des ContentInfo-Ausgabe Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="df17b-208">The audio profile created in step 4 will be used to populate the output ContentInfo object.</span></span> <span data-ttu-id="df17b-209">Dieses Objekt enthält Informationen wie globale Dateiattribute und streameigenschaften.</span><span class="sxs-lookup"><span data-stu-id="df17b-209">This object contains information such as global file attributes and stream properties.</span></span> <span data-ttu-id="df17b-210">Das ContentInfo-Ausgabe Objekt wird verwendet, um den Multiplexer zu initialisieren, der Datenpakete für die Ausgabedatei generiert.</span><span class="sxs-lookup"><span data-stu-id="df17b-210">The output ContentInfo object will be used to initialize the multiplexer that will generate data packets for the output file.</span></span> <span data-ttu-id="df17b-211">Nachdem die Datenpakete generiert wurden, muss das ContentInfo-Objekt aktualisiert werden, um die neuen Werte widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="df17b-211">After the data packets are generated, the ContentInfo object must be updated to reflect the new values.</span></span>

<span data-ttu-id="df17b-212">So erstellen und initialisieren Sie die ASF-Komponenten für die Ausgabedatei</span><span class="sxs-lookup"><span data-stu-id="df17b-212">To create and initialize ASF components for the output file</span></span>

1.  <span data-ttu-id="df17b-213">Erstellen Sie ein leeres ContentInfo-Objekt, indem Sie [**mfcreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) aufrufen und es mit Informationen aus dem in Schritt 3 erstellten Audioprofil auffüllen, indem Sie [**imfasfcontentinfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="df17b-213">Create an empty ContentInfo object by calling [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) and populate it with information from the audio profile created in step 3 by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span> <span data-ttu-id="df17b-214">Weitere Informationen finden Sie unter [Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="df17b-214">For more information, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>
2.  <span data-ttu-id="df17b-215">Erstellen und initialisieren Sie das Multiplexer-Objekt mit dem ContentInfo-Ausgabe Objekt.</span><span class="sxs-lookup"><span data-stu-id="df17b-215">Create and initialize the multiplexer object by using the output ContentInfo object.</span></span> <span data-ttu-id="df17b-216">Weitere Informationen finden Sie unter [Erstellen des Multiplexer-Objekts](creating-the-multiplexer-object.md).</span><span class="sxs-lookup"><span data-stu-id="df17b-216">For more information, see [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

<span data-ttu-id="df17b-217">Der folgende Beispielcode zeigt eine Funktion, die die Schritte konsolidiert.</span><span class="sxs-lookup"><span data-stu-id="df17b-217">The following example code shows a function that consolidates the steps.</span></span> <span data-ttu-id="df17b-218">Diese Funktion nimmt einen Zeiger auf ein Profil Objekt an und gibt Zeiger auf das Output ContentInfo-Objekt und den Multiplexer zurück.</span><span class="sxs-lookup"><span data-stu-id="df17b-218">This function takes a pointer to a profile object and returns pointers to the output ContentInfo object and the multiplexer.</span></span>


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



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="df17b-219">7. Generieren neuer ASF-Datenpakete</span><span class="sxs-lookup"><span data-stu-id="df17b-219">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="df17b-220">Als nächstes generieren Sie audiostreambeispiele aus dem quellbytestream mithilfe des Splitters und senden Sie an den Multiplexer, um ASF-Datenpakete zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="df17b-220">Next, you will generate audio stream samples from the source byte stream by using the splitter and send them to the multiplexer to create ASF data packets.</span></span> <span data-ttu-id="df17b-221">Diese Datenpakete bilden das endgültige ASF-Datenobjekt für die neue Datei.</span><span class="sxs-lookup"><span data-stu-id="df17b-221">These data packets will constitute the final ASF Data Object for the new file.</span></span>

<span data-ttu-id="df17b-222">So generieren Sie audiostreambeispiele</span><span class="sxs-lookup"><span data-stu-id="df17b-222">To generate audio stream samples</span></span>

1.  <span data-ttu-id="df17b-223">Wählen Sie den ersten Audiostream auf dem Splitter aus, indem Sie [**imfasfsplitter:: selectstreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="df17b-223">Select the first audio stream on the splitter by calling [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).</span></span>
2.  <span data-ttu-id="df17b-224">Lesen Sie Blöcke mit fester Größe aus dem Quell-Bytestream in einen Medien Puffer.</span><span class="sxs-lookup"><span data-stu-id="df17b-224">Read fixed-size blocks of media data from the source byte stream into a media buffer.</span></span>
3.  <span data-ttu-id="df17b-225">Erfassen Sie die streambeispiele als Medien Beispiele aus dem Splitter, indem Sie [**imfasfsplitter:: getnextsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in einer Schleife aufrufen, solange das- \_ Flag "ASF Statusflags \_ unvollständig" im *pdwstatusflags* -Parameter empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="df17b-225">Collect the stream samples as media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop as long as it receives the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter.</span></span> <span data-ttu-id="df17b-226">Weitere Informationen finden Sie unter Erstellen von Beispielen für ASF-Datenpakete in [Erstellen von streambeispielen aus einem vorhandenen ASF-Datenobjekt](generating-stream-samples-from-an-existing-asf-data-object.md).</span><span class="sxs-lookup"><span data-stu-id="df17b-226">For more information, see Generating Samples for ASF Data Packets" in [Generating Stream Samples from an Existing ASF Data Object](generating-stream-samples-from-an-existing-asf-data-object.md).</span></span>
4.  <span data-ttu-id="df17b-227">Nennen Sie für jedes Medien Beispiel [**imfasfmultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) , um das Medien Beispiel an den Multiplexer zu senden.</span><span class="sxs-lookup"><span data-stu-id="df17b-227">For each media sample, call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the media sample to the multiplexer.</span></span> <span data-ttu-id="df17b-228">Der Multiplexer generiert die Datenpakete für das ASF-Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="df17b-228">The multiplexer generates the data packets for the ASF Data Object.</span></span>
5.  <span data-ttu-id="df17b-229">Schreiben des vom Multiplexer generierten Datenpakets in den datenbytestream.</span><span class="sxs-lookup"><span data-stu-id="df17b-229">Write the data packet generated by the multiplexer to the data byte stream.</span></span>
6.  <span data-ttu-id="df17b-230">Nachdem alle Datenpakete generiert wurden, wird [**imfasfmultiplexer:: End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) aufgerufen, um das Ausgabe-ContentInfo-Objekt mit Informationen zu aktualisieren, die während der Erstellung des ASF-Datenpakets gesammelt wurden.</span><span class="sxs-lookup"><span data-stu-id="df17b-230">After all the data packets have been generated, call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) to update the output ContentInfo object with information collected during ASF data packet generation.</span></span>

<span data-ttu-id="df17b-231">Der folgende Beispielcode generiert streambeispiele aus dem ASF-Splitter und sendet Sie an den Multiplexer.</span><span class="sxs-lookup"><span data-stu-id="df17b-231">The following example code generates stream samples from the ASF splitter and sends them to the multiplexer.</span></span> <span data-ttu-id="df17b-232">Der Multiplexer generiert ASF-Datenpakete und schreibt Sie in einen Stream.</span><span class="sxs-lookup"><span data-stu-id="df17b-232">The multiplexer generates ASF data packets and writes it to a stream.</span></span>


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



<span data-ttu-id="df17b-233">Um Pakete aus dem ASF-Splitter zu erhalten, ruft der vorherige Code die- `GetPacketsFromSplitter` Funktion auf, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="df17b-233">To get packets from the ASF splitter, the previous code calls the `GetPacketsFromSplitter` function, shown here:</span></span>


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



<span data-ttu-id="df17b-234">Die `GenerateDataPackets` Funktion ruft Datenpakete von Multiplexer ab.</span><span class="sxs-lookup"><span data-stu-id="df17b-234">The `GenerateDataPackets` function gets data packets from multiplexer.</span></span> <span data-ttu-id="df17b-235">Weitere Informationen finden Sie unter [erhalten von ASF-Datenpaketen](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="df17b-235">For more information, see [Getting ASF Data Packets](generating-new-asf-data-packets.md).</span></span>


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



## <a name="8-write-the-asf-objects-in-the-new-file"></a><span data-ttu-id="df17b-236">8. Schreiben der ASF-Objekte in der neuen Datei</span><span class="sxs-lookup"><span data-stu-id="df17b-236">8. Write the ASF Objects in the New File</span></span>

<span data-ttu-id="df17b-237">Als nächstes schreiben Sie den Inhalt des ContentInfo-Ausgabe Objekts in einen Medien Puffer, indem Sie [**imfasfcontentinfo:: generateheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="df17b-237">Next, you will write the contents of the output ContentInfo object to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="df17b-238">Diese Methode konvertiert die im ContentInfo-Objekt gespeicherten Daten im Objekt Format des ASF-Headers in Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="df17b-238">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="df17b-239">Weitere Informationen finden Sie unter [Erstellen eines neuen ASF-Header Objekts](generating-a-new-asf-header-object.md).</span><span class="sxs-lookup"><span data-stu-id="df17b-239">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="df17b-240">Nachdem das neue ASF-Header Objekt generiert wurde, schreiben Sie die Ausgabedatei, indem Sie zuerst das Header Objekt in den in Schritt 2 erstellten Ausgabe Byte Datenstrom schreiben, indem Sie die Hilfsfunktion "writebuffertobytestream" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="df17b-240">After the new ASF Header Object has been generated, write the output file by first writing the Header Object to the output byte stream created in step 2 by calling the helper function WriteBufferToByteStream.</span></span> <span data-ttu-id="df17b-241">Befolgen Sie das Header Objekt mit dem Datenobjekt, das im datenbytestream enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="df17b-241">Follow the Header Object with the Data Object contained in the data byte stream.</span></span> <span data-ttu-id="df17b-242">Der Beispielcode zeigt eine Funktion, die den Inhalt des Datenstrom-Datenstroms an den Bytestream überträgt.</span><span class="sxs-lookup"><span data-stu-id="df17b-242">The example code shows a function that transfers contents of the data bytes stream to the output byte stream.</span></span>


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



## <a name="9-write-the-entry-point-function"></a><span data-ttu-id="df17b-243">9 Schreiben der Entry-Point-Funktion</span><span class="sxs-lookup"><span data-stu-id="df17b-243">9 Write the Entry-Point Function</span></span>

<span data-ttu-id="df17b-244">Nun können Sie die vorherigen Schritte in eine komplette Anwendung einfügen.</span><span class="sxs-lookup"><span data-stu-id="df17b-244">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="df17b-245">Initialisieren Sie vor dem Verwenden eines der Media Foundation Objekte die Media Foundation Plattform durch Aufrufen von [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="df17b-245">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="df17b-246">Wenn Sie den Vorgang abgeschlossen haben, wenden Sie sich an [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="df17b-246">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="df17b-247">Weitere Informationen finden Sie unter [Initialisieren von Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="df17b-247">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="df17b-248">Der folgende Code zeigt die komplette Konsolenanwendung.</span><span class="sxs-lookup"><span data-stu-id="df17b-248">The following code shows the complete console application.</span></span> <span data-ttu-id="df17b-249">Das Befehlszeilenargument gibt den Namen der zu konvertierenden Datei und den Namen der neuen Audiodatei an.</span><span class="sxs-lookup"><span data-stu-id="df17b-249">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="df17b-250">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df17b-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df17b-251">Wmcontainer-ASF-Komponenten</span><span class="sxs-lookup"><span data-stu-id="df17b-251">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="df17b-252">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="df17b-252">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



