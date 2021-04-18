---
description: Erstellen eines neuen ASF-Header Objekts
ms.assetid: cf73306d-156a-45c0-a3d6-ae48734f5709
title: Erstellen eines neuen ASF-Header Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f303be4eb3353a0e7ddf1dad0eff9956f68d7db5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524512"
---
# <a name="generating-a-new-asf-header-object"></a><span data-ttu-id="cbea5-103">Erstellen eines neuen ASF-Header Objekts</span><span class="sxs-lookup"><span data-stu-id="cbea5-103">Generating a New ASF Header Object</span></span>

<span data-ttu-id="cbea5-104">Um die im ContentInfo-Objekt enthaltenen Informationen in ein binäres Objekt Format des ASF-Headers zu konvertieren, muss die Anwendung [**imfasfcontentinfo:: generateheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cbea5-104">To convert the information contained in the ContentInfo object to a binary ASF Header Object format, the application must call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="cbea5-105">Dieser Rückruf muss erfolgen, nachdem die Datenpakete generiert wurden und das ContentInfo-Objekt aktualisierte Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="cbea5-105">This call must be made after the data packets are generated and the ContentInfo object contains updated information.</span></span> <span data-ttu-id="cbea5-106">**Generateheader** gibt einen Zeiger auf einen Medien Puffer zurück, der die Header Informationen im gültigen Format enthält.</span><span class="sxs-lookup"><span data-stu-id="cbea5-106">**GenerateHeader** returns a pointer to a media buffer that contains the header information in the valid format.</span></span> <span data-ttu-id="cbea5-107">Die Anwendung kann dann die Daten, auf die vom Medien Puffer verwiesen wird, am Anfang einer neuen ASF-Datei schreiben.</span><span class="sxs-lookup"><span data-stu-id="cbea5-107">The application can then write the data, pointed to by the media buffer, at the beginning of a new ASF file.</span></span>

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a><span data-ttu-id="cbea5-108">So schreiben Sie ein neues Header Objekt mit dem ContentInfo-Objekt</span><span class="sxs-lookup"><span data-stu-id="cbea5-108">To write a new Header Object by using the ContentInfo object</span></span>

1.  <span data-ttu-id="cbea5-109">Rufen Sie [**mfkreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) auf, um ein leeres ContentInfo-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cbea5-109">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="cbea5-110">Aufrufen von [**imfasfcontentinfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) , um das Profil Objekt für das ContentInfo-Objekt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cbea5-110">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to supply the profile object to the ContentInfo object.</span></span> <span data-ttu-id="cbea5-111">Weitere Informationen zum Erstellen von Profilen finden Sie unter [Erstellen eines ASF-Profils](creating-an-asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="cbea5-111">For information about creating profiles, see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
3.  <span data-ttu-id="cbea5-112">Aufrufen von [**imfasfcontentinfo:: generateheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) und übergeben von **null** im *piheader* -Parameter und empfangen der Größe des aufgefüllten ContentInfo-Objekts im *pcbheader* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="cbea5-112">Call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) and pass **NULL** in the *pIHeader* parameter and receive the size of the populated ContentInfo object in the *pcbHeader* parameter.</span></span> <span data-ttu-id="cbea5-113">Die Anwendung kann diesen Wert verwenden, um Arbeitsspeicher oder den Medien Puffer zuzuweisen, der das Header Objekt enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="cbea5-113">The application can use this value to allocate memory or the media buffer that will contain the Header Object.</span></span>

    <span data-ttu-id="cbea5-114">Die empfangene Header Größe schließt die Auffüll Größe ein, die abhängig von der tatsächlichen Größe der Header Objekte angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="cbea5-114">The header size received includes the padding size, which is adjusted depending on the actual size of the header objects.</span></span> <span data-ttu-id="cbea5-115">Die maximale Größe der Header Objekte beträgt 10 MB.</span><span class="sxs-lookup"><span data-stu-id="cbea5-115">The maximum size of the header objects is 10 MB.</span></span> <span data-ttu-id="cbea5-116">Wenn die Größe diesen Wert überschreitet, schlägt **generateheader** mit dem \_ Fehler "MF E \_ ASF \_ InvalidData" fehl.</span><span class="sxs-lookup"><span data-stu-id="cbea5-116">If the size exceeds this value, **GenerateHeader** fails with the MF\_E\_ASF\_INVALIDDATA error.</span></span>

4.  <span data-ttu-id="cbea5-117">Rufen Sie [**mfkreatememorybuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) auf, um in Schritt 3 einen Medien Puffer mit der empfangenen Größe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cbea5-117">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer of the received size in step 3.</span></span>
5.  <span data-ttu-id="cbea5-118">Rufen Sie **generateheader** erneut auf, um das neue ASF-Header Objekt aus dem ContentInfo-Objekt im Medien Puffer zu generieren, den Sie in Schritt 4 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="cbea5-118">Call **GenerateHeader** again to generate the new ASF Header Object from the ContentInfo object in the media buffer created in step 4.</span></span>

    <span data-ttu-id="cbea5-119">Die Länge der Daten im Medien Puffer wird aktualisiert, und die neue Größe wird im *pcbheader* -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cbea5-119">The length of the data in the media buffer is updated and the new size is returned in the *pcbHeader* parameter.</span></span>

6.  <span data-ttu-id="cbea5-120">Schreiben Sie den Inhalt des Medien Puffers am Anfang der Datei.</span><span class="sxs-lookup"><span data-stu-id="cbea5-120">Write the contents of the media buffer at the beginning of the file.</span></span> <span data-ttu-id="cbea5-121">Die Anwendung kann den Bytestream verwenden, um den Schreibvorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="cbea5-121">The application can use the byte stream to perform the writing operation.</span></span> <span data-ttu-id="cbea5-122">Beispielcode finden Sie unter [**IMF Bytestream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="cbea5-122">For example code, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>

### <a name="example"></a><span data-ttu-id="cbea5-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cbea5-123">Example</span></span>

<span data-ttu-id="cbea5-124">Der folgende Beispielcode zeigt, wie ein ContentInfo-Objekt erstellt und ein Medien Puffer generiert wird, um das neue Header Objekt zu speichern.</span><span class="sxs-lookup"><span data-stu-id="cbea5-124">The following example code shows how to create a ContentInfo object and generate a media buffer to store the new Header Object.</span></span> <span data-ttu-id="cbea5-125">Ein umfassendes Beispiel, in dem dieser Code verwendet wird, finden [Sie unter Tutorial: Kopieren von ASF-Streams aus einer Datei in eine andere](tutorial--copying-asf-streams-from-one-file-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="cbea5-125">For a complete example that uses this code, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cbea5-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbea5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbea5-127">Schreiben eines ASF-Header Objekts für eine neue Datei</span><span class="sxs-lookup"><span data-stu-id="cbea5-127">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



