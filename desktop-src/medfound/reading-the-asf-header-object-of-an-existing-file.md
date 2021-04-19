---
description: Lesen des ASF-Header Objekts einer vorhandenen Datei
ms.assetid: 0e37f0d3-a37b-4f36-a133-7b1922e9944b
title: Lesen des ASF-Header Objekts einer vorhandenen Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b231cb0b9af6b24f84efaa6403a4774e66bbb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348258"
---
# <a name="reading-the-asf-header-object-of-an-existing-file"></a><span data-ttu-id="51365-103">Lesen des ASF-Header Objekts einer vorhandenen Datei</span><span class="sxs-lookup"><span data-stu-id="51365-103">Reading the ASF Header Object of an Existing File</span></span>

<span data-ttu-id="51365-104">Das Objekt "ASF ContentInfo" speichert Informationen, die die Objekte des ASF-Headers einer Mediendatei darstellen.</span><span class="sxs-lookup"><span data-stu-id="51365-104">The ASF ContentInfo object stores information that represents the ASF Header Objects of a media file.</span></span> <span data-ttu-id="51365-105">Ein aufgefülltes ContentInfo-Objekt ist erforderlich, um eine vorhandene ASF-Datei zu lesen und zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="51365-105">A populated ContentInfo object is required in order to read and parse an existing ASF file.</span></span>

<span data-ttu-id="51365-106">Nachdem Sie das ContentInfo-Objekt durch Aufrufen der [**mfcreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) -Funktion erstellt haben, muss die Anwendung diese mit Header Informationen aus der zu lesenden ASF-Datei initialisieren.</span><span class="sxs-lookup"><span data-stu-id="51365-106">After creating the ContentInfo object by calling the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function, the application must initialize it with header information from the ASF file that is to be read.</span></span> <span data-ttu-id="51365-107">Um das-Objekt aufzufüllen, nennen Sie [**imfasfcontentinfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span><span class="sxs-lookup"><span data-stu-id="51365-107">To populate the object, call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span>

<span data-ttu-id="51365-108">" **Parser Header** " erfordert einen Medien Puffer, der das Header Objekt der ASF-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="51365-108">**ParseHeader** requires a media buffer that contains the Header Object of the ASF file.</span></span> <span data-ttu-id="51365-109">Eine Möglichkeit besteht darin, einen Medien Puffer mit dem Header Objekt zu füllen, um einen Bytestream für die Datei zu erstellen und dann die ersten 30 Bytes der Daten aus dem Bytestream in einen Medien Puffer zu lesen.</span><span class="sxs-lookup"><span data-stu-id="51365-109">One option is to fill a media buffer with the Header Object to create a byte stream for the file and then read the first 30 bytes of data from the byte stream into a media buffer.</span></span> <span data-ttu-id="51365-110">Sie können dann die Größe erzielen, indem Sie die ersten 24 Bytes des Header Objekts an die [**imfasfcontentinfo:: gethadersize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="51365-110">You can then get the size by passing the first 24 bytes of the Header Object to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="51365-111">Nachdem Sie die Größe erhalten haben, können Sie das gesamte Header Objekt in einem Medien Puffer lesen und an den- **Header** übergeben.</span><span class="sxs-lookup"><span data-stu-id="51365-111">After getting the size, you can read the entire Header Object in a media buffer and pass it to **ParseHeader**.</span></span> <span data-ttu-id="51365-112">Die-Methode beginnt mit der Verarbeitung am Offset vom Anfang des Medien Puffers, der im Parameter *cboffsetwithinheader* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="51365-112">The method starts parsing at the offset from the start of the media buffer specified in the *cbOffsetWithinHeader* parameter.</span></span>

<span data-ttu-id="51365-113">Im folgenden Beispielcode wird ein ContentInfo-Objekt erstellt und initialisiert, um eine vorhandene, in einem Bytestream enthaltene ASF-Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="51365-113">The following example code creates and initializes a ContentInfo object for reading an existing ASF file contained in a byte stream.</span></span> <span data-ttu-id="51365-114">Zuerst definieren wir eine Hilfsfunktion, die Daten aus einem Bytestream liest und einen Medien Puffer zum Speichern der Daten zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="51365-114">First, we define a helper function that reads data from a byte stream and allocates a media buffer to hold the data:</span></span>


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



<span data-ttu-id="51365-115">Im nächsten Beispiel wird das ASF-Header Objekt aus einem Bytestream gelesen und ein "ASF ContentInfo"-Objekt aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="51365-115">The next example reads the ASF Header Object from a byte stream and populates an ASF ContentInfo object.</span></span>


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



> [!Note]  
> <span data-ttu-id="51365-116">In diesen Beispielen wird die [saferelease](saferelease.md) -Funktion verwendet, um Schnittstellen Zeiger freizugeben.</span><span class="sxs-lookup"><span data-stu-id="51365-116">These examples use the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="51365-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51365-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51365-118">ASF-ContentInfo-Objekt</span><span class="sxs-lookup"><span data-stu-id="51365-118">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="51365-119">ASF-Header Objekt</span><span class="sxs-lookup"><span data-stu-id="51365-119">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="51365-120">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="51365-120">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="51365-121">Informationen aus den ASF-Header Objekten werden erhalten.</span><span class="sxs-lookup"><span data-stu-id="51365-121">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
</dt> </dl>

 

 



