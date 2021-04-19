---
description: In diesem Tutorial wird gezeigt, wie Sie mithilfe des ASF-Splitters Datenpakete aus einer ASF-Datei (Advanced Systems Format) erhalten.
ms.assetid: e3a55275-e8f0-4ab7-98db-a2f2c54d5a51
title: 'Tutorial: Lesen einer ASF-Datei mithilfe von wmcontainer-Objekten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0225f434f650f0423771122e6fc345022e69ec1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348540"
---
# <a name="tutorial-reading-an-asf-file-by-using-wmcontainer-objects"></a><span data-ttu-id="8f260-103">Tutorial: Lesen einer ASF-Datei mithilfe von wmcontainer-Objekten</span><span class="sxs-lookup"><span data-stu-id="8f260-103">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>

<span data-ttu-id="8f260-104">In diesem Tutorial wird gezeigt, wie Sie mithilfe des [ASF-Splitters](asf-splitter.md)Datenpakete aus einer ASF-Datei (Advanced Systems Format) erhalten.</span><span class="sxs-lookup"><span data-stu-id="8f260-104">This tutorial shows how to get data packets from an Advanced Systems Format (ASF) file using the [ASF Splitter](asf-splitter.md).</span></span> <span data-ttu-id="8f260-105">In diesem Tutorial erstellen Sie eine einfache Konsolenanwendung, die eine ASF-Datei liest und komprimierte Medien Beispiele für den ersten Videostream in der Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="8f260-105">In this tutorial, you will create a simple console application that reads an ASF file and generates compressed media samples for the first video stream in the file.</span></span> <span data-ttu-id="8f260-106">Die Anwendung zeigt Informationen zu den Keyframes im Videostream an.</span><span class="sxs-lookup"><span data-stu-id="8f260-106">The application displays information about the key frames in the video stream.</span></span>

<span data-ttu-id="8f260-107">Folgende Themen werden in diesem Lernprogramm behandelt:</span><span class="sxs-lookup"><span data-stu-id="8f260-107">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="8f260-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8f260-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="8f260-109">1. richten Sie das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="8f260-109">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="8f260-110">2. Öffnen einer ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="8f260-110">2. Open an ASF File</span></span>](#2-open-an-asf-file)
-   [<span data-ttu-id="8f260-111">3. Lesen des ASF-Header Objekts</span><span class="sxs-lookup"><span data-stu-id="8f260-111">3. Read the ASF Header Object</span></span>](#3-read-the-asf-header-object)
-   [<span data-ttu-id="8f260-112">4. Erstellen des ASF-Splitters</span><span class="sxs-lookup"><span data-stu-id="8f260-112">4. Create the ASF Splitter</span></span>](#4-create-the-asf-splitter)
-   [<span data-ttu-id="8f260-113">5. Wählen Sie einen Stream für die Verarbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="8f260-113">5. Select a Stream for Parsing</span></span>](#5-select-a-stream-for-parsing)
-   [<span data-ttu-id="8f260-114">6. Generieren von Beispielen für komprimierte Medien</span><span class="sxs-lookup"><span data-stu-id="8f260-114">6. Generate Compressed Media Samples</span></span>](#6-generate-compressed-media-samples)
-   [<span data-ttu-id="8f260-115">7. Schreiben der Entry-Point-Funktion</span><span class="sxs-lookup"><span data-stu-id="8f260-115">7. Write the Entry-Point Function</span></span>](#7-write-the-entry-point-function)
-   [<span data-ttu-id="8f260-116">Programm Auflistung</span><span class="sxs-lookup"><span data-stu-id="8f260-116">Program Listing</span></span>](#program-listing)
-   [<span data-ttu-id="8f260-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f260-117">Related topics</span></span>](#related-topics)

<span data-ttu-id="8f260-118">In diesem Tutorial wird nicht erläutert, wie die komprimierten Daten decodiert werden, die von der Anwendung aus dem ASF-Splitter abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8f260-118">The tutorial does not cover how to decode the compressed data that the application gets from the ASF splitter.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8f260-119">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8f260-119">Prerequisites</span></span>

<span data-ttu-id="8f260-120">In diesem Tutorial wird Folgendes vorausgesetzt:</span><span class="sxs-lookup"><span data-stu-id="8f260-120">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="8f260-121">Sie sind mit der Struktur einer ASF-Datei und den von Media Foundation bereitgestellten Komponenten vertraut, um mit der Verwendung von ASF-Objekten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8f260-121">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="8f260-122">Zu diesen Komponenten gehören das ContentInfo-Objekt, Splitter, Multiplexer und Profile.</span><span class="sxs-lookup"><span data-stu-id="8f260-122">These components include the ContentInfo object, splitter, multiplexer, and profile.</span></span> <span data-ttu-id="8f260-123">Weitere Informationen finden Sie unter [wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="8f260-123">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="8f260-124">Sie sind mit [Medien Puffern](media-buffers.md) und Bytestreams vertraut: insbesondere Datei Vorgänge mit einem Bytestream, Lesen aus einem Bytestream in einen Medien Puffer und Schreiben des Inhalts eines Medien Puffers in einen Bytestream.</span><span class="sxs-lookup"><span data-stu-id="8f260-124">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, reading from a byte stream into a media buffer, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="8f260-125">1. richten Sie das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="8f260-125">1. Set up the Project</span></span>

<span data-ttu-id="8f260-126">Fügen Sie die folgenden Header in die Quelldatei ein:</span><span class="sxs-lookup"><span data-stu-id="8f260-126">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>
```



<span data-ttu-id="8f260-127">Verknüpfen Sie die folgenden Bibliotheksdateien:</span><span class="sxs-lookup"><span data-stu-id="8f260-127">Link to the following library files:</span></span>

-   <span data-ttu-id="8f260-128">MF. lib</span><span class="sxs-lookup"><span data-stu-id="8f260-128">mfplat.lib</span></span>
-   <span data-ttu-id="8f260-129">MF. lib</span><span class="sxs-lookup"><span data-stu-id="8f260-129">mf.lib</span></span>
-   <span data-ttu-id="8f260-130">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="8f260-130">mfuuid.lib</span></span>

<span data-ttu-id="8f260-131">Deklarieren Sie die [saferelease](saferelease.md) -Funktion:</span><span class="sxs-lookup"><span data-stu-id="8f260-131">Declare the [SafeRelease](saferelease.md) function:</span></span>


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



## <a name="2-open-an-asf-file"></a><span data-ttu-id="8f260-132">2. Öffnen einer ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="8f260-132">2. Open an ASF File</span></span>

<span data-ttu-id="8f260-133">Öffnen Sie als nächstes die angegebene Datei, indem Sie die [**mfcreatefile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8f260-133">Next, open the specified file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="8f260-134">Die-Methode gibt einen Zeiger auf das bytestreamobjekt zurück, das den Inhalt der Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="8f260-134">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="8f260-135">Der Dateiname wird vom Benutzer über Befehlszeilenargumente der Anwendung angegeben.</span><span class="sxs-lookup"><span data-stu-id="8f260-135">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="8f260-136">Im folgenden Beispielcode wird ein Dateiname verwendet, und es wird ein Zeiger auf ein bytestreamobjekt zurückgegeben, das zum Lesen der Datei verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8f260-136">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="3-read-the-asf-header-object"></a><span data-ttu-id="8f260-137">3. Lesen des ASF-Header Objekts</span><span class="sxs-lookup"><span data-stu-id="8f260-137">3. Read the ASF Header Object</span></span>

<span data-ttu-id="8f260-138">Erstellen Sie als nächstes das [Objekt "ASF ContentInfo](asf-contentinfo-object.md) ", und verwenden Sie es zum Analysieren des ASF-Header Objekts der angegebenen Datei.</span><span class="sxs-lookup"><span data-stu-id="8f260-138">Next, create the [ASF ContentInfo Object](asf-contentinfo-object.md) and use it to parse the ASF Header Object of the specified file.</span></span> <span data-ttu-id="8f260-139">Das ContentInfo-Objekt speichert Informationen aus dem ASF-Header, einschließlich globaler Dateiattribute und Informationen zu jedem Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="8f260-139">The ContentInfo object stores information from the ASF header, including global file attributes and information about each stream.</span></span> <span data-ttu-id="8f260-140">Sie verwenden das ContentInfo-Objekt später in diesem Tutorial, um den ASF-Splitter zu initialisieren und die streamnummer des Videodaten Stroms zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8f260-140">You will use the ContentInfo object later in the tutorial to initialize the ASF splitter and get the stream number of the video stream.</span></span>

<span data-ttu-id="8f260-141">So erstellen Sie das Objekt "ASF ContentInfo":</span><span class="sxs-lookup"><span data-stu-id="8f260-141">To create the ASF ContentInfo object:</span></span>

1.  <span data-ttu-id="8f260-142">Rufen Sie die [**mfkreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) -Funktion auf, um ein ContentInfo-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f260-142">Call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function to create a ContentInfo object.</span></span> <span data-ttu-id="8f260-143">Die-Methode gibt einen Zeiger auf die [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="8f260-143">The method returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="8f260-144">Lesen Sie die ersten 30 Bytes der Daten aus der ASF-Datei in einen Medien Puffer.</span><span class="sxs-lookup"><span data-stu-id="8f260-144">Read the first 30 bytes of data from the ASF file into a media buffer.</span></span>
3.  <span data-ttu-id="8f260-145">Übergeben Sie den Medien Puffer an die [**imfasfcontentinfo:: gethadersize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8f260-145">Pass the media buffer to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="8f260-146">Diese Methode gibt die Gesamtgröße des Header Objekts in der ASF-Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="8f260-146">This method returns the total size of the Header Object in the ASF file.</span></span>
4.  <span data-ttu-id="8f260-147">Übergeben Sie den gleichen Medien Puffer an die [**imfasfcontentinfo::P arelheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8f260-147">Pass the same media buffer to the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span>
5.  <span data-ttu-id="8f260-148">Lesen Sie den Rest des Header Objekts in einen neuen Medien Puffer.</span><span class="sxs-lookup"><span data-stu-id="8f260-148">Read the remainder of the Header Object into a new media buffer.</span></span>
6.  <span data-ttu-id="8f260-149">Übergeben Sie den zweiten Puffer an die Methode " [**Parser Header**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) ".</span><span class="sxs-lookup"><span data-stu-id="8f260-149">Pass the second buffer to the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="8f260-150">Geben Sie den 30-Byte-Offset im *cboffsetwithinheader* -Parameter von " **Parser**" an.</span><span class="sxs-lookup"><span data-stu-id="8f260-150">Specify the 30-byte offset in the *cbOffsetWithinHeader* parameter of **ParseHeader**.</span></span> <span data-ttu-id="8f260-151">Die Methode " **samseheader** " initialisiert das ContentInfo-Objekt mit Informationen, die aus den verschiedenen im Header Objekt enthaltenen ASF-Objekten gesammelt wurden.</span><span class="sxs-lookup"><span data-stu-id="8f260-151">The **ParseHeader** method initializes the ContentInfo object with information gathered from the various ASF objects contained in the Header Object.</span></span>


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



<span data-ttu-id="8f260-152">Diese Funktion verwendet die- `ReadFromByteStream` Funktion, um aus einem Bytestream in einen Medien Puffer zu lesen:</span><span class="sxs-lookup"><span data-stu-id="8f260-152">This function uses the `ReadFromByteStream` function to read from a byte stream into a media buffer:</span></span>


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



## <a name="4-create-the-asf-splitter"></a><span data-ttu-id="8f260-153">4. Erstellen des ASF-Splitters</span><span class="sxs-lookup"><span data-stu-id="8f260-153">4. Create the ASF Splitter</span></span>

<span data-ttu-id="8f260-154">Erstellen Sie als nächstes das [ASF-Splitter](asf-splitter.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="8f260-154">Next, create the [ASF Splitter](asf-splitter.md) object.</span></span> <span data-ttu-id="8f260-155">Sie verwenden den ASF-Splitter, um das ASF-Datenobjekt zu analysieren, das packetisiert-Mediendaten für die ASF-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="8f260-155">You will use the ASF splitter to parse the ASF Data Object, which contains packetized media data for the ASF file.</span></span>

<span data-ttu-id="8f260-156">So erstellen Sie ein Splitter Objekt für die ASF-Datei:</span><span class="sxs-lookup"><span data-stu-id="8f260-156">To create a splitter object for the ASF File:</span></span>

1.  <span data-ttu-id="8f260-157">Rufen Sie die [**mfkreateasfsplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) -Funktion auf, um den ASF-Splitter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f260-157">Call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function to create the ASF splitter.</span></span> <span data-ttu-id="8f260-158">Die-Funktion gibt einen Zeiger auf die [**imfasfsplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="8f260-158">The function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
2.  <span data-ttu-id="8f260-159">Um den ASF-Splitter zu initialisieren, wird [**imfasfsplitter:: Initialisieren**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8f260-159">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) to initialize the ASF splitter.</span></span> <span data-ttu-id="8f260-160">Diese Methode nimmt einen Zeiger auf das ContentInfo-Objekt an, das in der Prozedur 3 erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f260-160">This method takes a pointer to the ContentInfo object, which was created in procedure 3.</span></span>


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



## <a name="5-select-a-stream-for-parsing"></a><span data-ttu-id="8f260-161">5. Wählen Sie einen Stream für die Verarbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="8f260-161">5. Select a Stream for Parsing</span></span>

<span data-ttu-id="8f260-162">Auflisten Sie als nächstes die Streams in der ASF-Datei, und wählen Sie den ersten Videostream zum Auswerten aus.</span><span class="sxs-lookup"><span data-stu-id="8f260-162">Next, enumerate the streams in the ASF file and select the first video stream for parsing.</span></span> <span data-ttu-id="8f260-163">Zum Auflisten der Streams verwenden Sie ein ASF-Profil Objekt und suchen nach Streams mit einem Video Medientyp.</span><span class="sxs-lookup"><span data-stu-id="8f260-163">To enumerate the streams, you will use an ASF profile object and search for streams that have a video media type.</span></span>

<span data-ttu-id="8f260-164">So wählen Sie den Videostream aus:</span><span class="sxs-lookup"><span data-stu-id="8f260-164">To select the video stream:</span></span>

1.  <span data-ttu-id="8f260-165">Rufen Sie [**imfasfcontentinfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) für das ContentInfo-Objekt auf, um ein ASF-Profil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f260-165">Call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) on the ContentInfo object to create an ASF profile.</span></span> <span data-ttu-id="8f260-166">Neben anderen Informationen beschreibt das Profil die Datenströme in der ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="8f260-166">Among other information, the profile describes the streams in the ASF file.</span></span>
2.  <span data-ttu-id="8f260-167">Aufrufen von [**imfasfprofile:: getstreamcount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) , um die Anzahl der Streams in der ASF-Datei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8f260-167">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams in the ASF file.</span></span>
3.  <span data-ttu-id="8f260-168">Aufrufen von [**imfasfprofile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) in einer Schleife zum Aufzählen der Streams.</span><span class="sxs-lookup"><span data-stu-id="8f260-168">Call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) in a loop to enumerate the streams.</span></span> <span data-ttu-id="8f260-169">Die-Methode gibt einen Zeiger auf die [**imfasfstreamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="8f260-169">The method returns a pointer to the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="8f260-170">Außerdem wird der Datenstrom Bezeichner zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8f260-170">It also returns the stream identifier.</span></span>
4.  <span data-ttu-id="8f260-171">Aufrufen Sie [**imfasfstreamconfig:: getstreamtype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) , um die GUID des Haupt Typs für den Datenstrom abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8f260-171">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the major type GUID for the stream.</span></span> <span data-ttu-id="8f260-172">Wenn es sich bei der GUID des Haupt Typs um ein MF MediaType- \_ Video handelt, enthält der Stream Video.</span><span class="sxs-lookup"><span data-stu-id="8f260-172">If the major type GUID is MFMediaType\_Video, the stream contains video.</span></span>
5.  <span data-ttu-id="8f260-173">Wenn Sie in Schritt 4 einen Videostream gefunden haben, können Sie [**imfasfsplitter:: selectstreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) abrufen, um den Stream auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="8f260-173">If you found a video stream in step 4, call [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) to select the stream.</span></span> <span data-ttu-id="8f260-174">Diese Methode nimmt ein Array von streambezeichgern an.</span><span class="sxs-lookup"><span data-stu-id="8f260-174">This method takes an array of stream identifiers.</span></span> <span data-ttu-id="8f260-175">Für dieses Tutorial ist die Array Größe 1, da die Anwendung einen einzelnen Stream analysiert.</span><span class="sxs-lookup"><span data-stu-id="8f260-175">For this tutorial, the array size is 1 because the application will parse a single stream.</span></span>

<span data-ttu-id="8f260-176">Der folgende Beispielcode listet die Streams in der ASF-Datei auf und wählt den ersten Videostream auf dem ASF-Splitter aus:</span><span class="sxs-lookup"><span data-stu-id="8f260-176">The following example code enumerates the streams in the ASF file and selects the first video stream on the ASF splitter:</span></span>


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



## <a name="6-generate-compressed-media-samples"></a><span data-ttu-id="8f260-177">6. Generieren von Beispielen für komprimierte Medien</span><span class="sxs-lookup"><span data-stu-id="8f260-177">6. Generate Compressed Media Samples</span></span>

<span data-ttu-id="8f260-178">Verwenden Sie als nächstes den ASF-Splitter, um das ASF-Datenobjekt zu analysieren und die Datenpakete für den ausgewählten Videostream zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8f260-178">Next, use the ASF splitter to parse the ASF Data Object and get the data packets for the selected video stream.</span></span> <span data-ttu-id="8f260-179">Die Anwendung liest Daten aus der ASF-Datei in Blöcken fester Größe und übergibt die Daten an den ASF-Splitter.</span><span class="sxs-lookup"><span data-stu-id="8f260-179">The application reads data from the ASF file in fixed-size blocks and passes the data to the ASF splitter.</span></span> <span data-ttu-id="8f260-180">Der Splitter analysiert die Daten und generiert [Medien Beispiele](media-samples.md) , die die komprimierten Videodaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="8f260-180">The splitter parses the data and generates [Media Samples](media-samples.md) that contain the compressed video data.</span></span> <span data-ttu-id="8f260-181">Die Anwendung überprüft, ob jedes Beispiel einen Keyframe darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f260-181">The application checks whether each sample represents a key frame.</span></span> <span data-ttu-id="8f260-182">Wenn dies der Fall ist, zeigt die Anwendung einige grundlegende Informationen zum Beispiel an:</span><span class="sxs-lookup"><span data-stu-id="8f260-182">If so, the application displays some basic information about the sample:</span></span>

-   <span data-ttu-id="8f260-183">Anzahl der Medien Puffer</span><span class="sxs-lookup"><span data-stu-id="8f260-183">Number of media buffers</span></span>
-   <span data-ttu-id="8f260-184">Gesamtgröße der Daten</span><span class="sxs-lookup"><span data-stu-id="8f260-184">Total size of the data</span></span>
-   <span data-ttu-id="8f260-185">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="8f260-185">Time stamp</span></span>

<span data-ttu-id="8f260-186">So generieren Sie Beispiele für komprimierte Medien:</span><span class="sxs-lookup"><span data-stu-id="8f260-186">To generate compressed media samples:</span></span>

1.  <span data-ttu-id="8f260-187">Zuordnen eines neuen Medien Puffers.</span><span class="sxs-lookup"><span data-stu-id="8f260-187">Allocate a new media buffer.</span></span>
2.  <span data-ttu-id="8f260-188">Liest Daten aus dem Bytestream in den Medien Puffer.</span><span class="sxs-lookup"><span data-stu-id="8f260-188">Read data from the byte stream into the media buffer.</span></span>
3.  <span data-ttu-id="8f260-189">Übergeben Sie den Medien Puffer an die [**imfasfsplitter::P areldata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8f260-189">Pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="8f260-190">Die-Methode analysiert die ASF-Daten im Puffer.</span><span class="sxs-lookup"><span data-stu-id="8f260-190">The method parses the ASF data in the buffer.</span></span>
4.  <span data-ttu-id="8f260-191">Rufen Sie in einer-Schleife die Medien Beispiele aus dem Splitter ab, indem Sie [**imfasfsplitter:: getnextsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8f260-191">In a loop, get media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample).</span></span> <span data-ttu-id="8f260-192">Wenn der Parameter *ppisample* einen gültigen [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Zeiger erhält, bedeutet dies, dass der ASF-Splitter ein oder mehrere Datenpakete analysiert hat.</span><span class="sxs-lookup"><span data-stu-id="8f260-192">If the *ppISample* parameter receives a valid [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, it means the ASF splitter has parsed one or more data packets.</span></span> <span data-ttu-id="8f260-193">Wenn *ppisample* den Wert **null** erhält, brechen Sie aus der Schleife, und kehren Sie zu Schritt 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="8f260-193">If *ppISample* receives the value **NULL**, break from the loop and go back to step 1.</span></span>
5.  <span data-ttu-id="8f260-194">Zeigt Informationen zum Beispiel an.</span><span class="sxs-lookup"><span data-stu-id="8f260-194">Display information about the sample.</span></span>
6.  <span data-ttu-id="8f260-195">Unterbrechen Sie die Schleife unter folgenden Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="8f260-195">Break from the loop in the following conditions:</span></span>
    -   <span data-ttu-id="8f260-196">Der *ppisample* -Parameter empfängt den Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="8f260-196">The *ppISample* parameter receives the value **NULL**.</span></span>
    -   <span data-ttu-id="8f260-197">Der *pdwstatusflags* -Parameter empfängt das nicht **\_ \_ unvollständige "ASF Statusflags** "-Flag nicht.</span><span class="sxs-lookup"><span data-stu-id="8f260-197">The *pdwStatusFlags* parameter does not receive the **ASF\_STATUSFLAGS\_INCOMPLETE** flag.</span></span>

<span data-ttu-id="8f260-198">Wiederholen Sie diese Schritte, bis das Ende der Datei erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="8f260-198">Repeat these steps until you reach the end of the file.</span></span> <span data-ttu-id="8f260-199">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="8f260-199">The following code shows these steps:</span></span>


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



<span data-ttu-id="8f260-200">Die iskeyframe-Funktion testet, ob es sich bei einem Beispiel um einen Keyframe handelt, indem der Wert des [**\_ Cleanpoint-Attributs "mfsampleextension**](mfsampleextension-cleanpoint-attribute.md) " erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="8f260-200">The IsKeyFrame function tests whether a sample is a key frame, by getting the value of the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



<span data-ttu-id="8f260-201">Zu Veranschaulichung werden in diesem Tutorial einige Informationen zu jedem Video Keyframe angezeigt, indem die folgende Funktion aufgerufen wird:</span><span class="sxs-lookup"><span data-stu-id="8f260-201">For illustration purposes, this tutorial displays some information for each video key frame, by calling the following function:</span></span>


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



<span data-ttu-id="8f260-202">Eine typische Anwendung verwendet die Datenpakete zum Decodieren, remuxing, senden über das Netzwerk oder eine andere Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="8f260-202">A typical application would use the data packets for decoding, remuxing, sending over the network, or some other task.</span></span>

## <a name="7-write-the-entry-point-function"></a><span data-ttu-id="8f260-203">7. Schreiben der Entry-Point-Funktion</span><span class="sxs-lookup"><span data-stu-id="8f260-203">7. Write the Entry-Point Function</span></span>

<span data-ttu-id="8f260-204">Nun können Sie die vorherigen Schritte in eine komplette Anwendung einfügen.</span><span class="sxs-lookup"><span data-stu-id="8f260-204">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="8f260-205">Initialisieren Sie vor dem Verwenden eines der Media Foundation Objekte die Media Foundation Plattform durch Aufrufen von [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="8f260-205">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="8f260-206">Wenn Sie den Vorgang abgeschlossen haben, wenden Sie sich an [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="8f260-206">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="8f260-207">Weitere Informationen finden Sie unter [Initialisieren von Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="8f260-207">For more information, [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


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



## <a name="program-listing"></a><span data-ttu-id="8f260-208">Programm Auflistung</span><span class="sxs-lookup"><span data-stu-id="8f260-208">Program Listing</span></span>

<span data-ttu-id="8f260-209">Der folgende Code zeigt die komplette Auflistung für das Tutorial.</span><span class="sxs-lookup"><span data-stu-id="8f260-209">The following code shows the complete listing for the tutorial.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8f260-210">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f260-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f260-211">Wmcontainer-ASF-Komponenten</span><span class="sxs-lookup"><span data-stu-id="8f260-211">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="8f260-212">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8f260-212">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



