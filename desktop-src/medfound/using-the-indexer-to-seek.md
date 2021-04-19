---
description: Der ASF-Indexer ist eine wmcontainer-Ebenenkomponente, die verwendet wird, um Index Objekte in einer ASF-Datei (Advanced Systems Format) zu lesen oder zu schreiben. Dieses Thema enthält Informationen zur Verwendung des-ASF-Indexers, um in einer ASF-Datei zu suchen.
ms.assetid: 9c501d33-847e-448e-a19c-39dfbc7757ca
title: Verwenden des Indexers zum Suchen in einer ASF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40c35f876fdc5452c596048d121fb0c2933094a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360000"
---
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a><span data-ttu-id="502f4-104">Verwenden des Indexers zum Suchen in einer ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="502f4-104">Using the Indexer to Seek Within an ASF File</span></span>

<span data-ttu-id="502f4-105">Der ASF- *Indexer* ist eine wmcontainer-Ebenenkomponente, die verwendet wird, um Index Objekte in einer ASF-Datei (Advanced Systems Format) zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="502f4-105">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="502f4-106">Dieses Thema enthält Informationen zur Verwendung des-ASF-Indexers, um in einer ASF-Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="502f4-106">This topic provides information about using the ASF indexer to seek within an ASF file.</span></span>

-   [<span data-ttu-id="502f4-107">Initialisieren des Indexers für die Suche</span><span class="sxs-lookup"><span data-stu-id="502f4-107">Initializing the Indexer for Seeking</span></span>](#initializing-the-indexer-for-seeking)
-   [<span data-ttu-id="502f4-108">Die Such Position wird erhalten.</span><span class="sxs-lookup"><span data-stu-id="502f4-108">Getting the Seek Position.</span></span>](#getting-the-seek-position)
-   [<span data-ttu-id="502f4-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="502f4-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="502f4-110">Weitere Informationen zur Struktur einer ASF-Datei finden Sie unter [Struktur der ASF-Datei](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="502f4-110">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

## <a name="initializing-the-indexer-for-seeking"></a><span data-ttu-id="502f4-111">Initialisieren des Indexers für die Suche</span><span class="sxs-lookup"><span data-stu-id="502f4-111">Initializing the Indexer for Seeking</span></span>

<span data-ttu-id="502f4-112">So initialisieren Sie den ASF-Indexer für die Suche:</span><span class="sxs-lookup"><span data-stu-id="502f4-112">To initialize the ASF indexer for seeking:</span></span>

1.  <span data-ttu-id="502f4-113">Rufen Sie [**mfkreateasfindexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) auf, um eine neue Instanz des ASF-Indexers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="502f4-113">Call [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) to create a new instance of the ASF indexer.</span></span>
2.  <span data-ttu-id="502f4-114">Um den Indexer zu initialisieren, wird [**imfasfindexer:: Initialisieren**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="502f4-114">Call [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) to initialize the indexer.</span></span> <span data-ttu-id="502f4-115">Diese Methode ruft Informationen aus dem ASF-Header ab, um zu bestimmen, welche ASF-Streams indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="502f4-115">This method gets information from the ASF header to determine which ASF streams are indexed.</span></span> <span data-ttu-id="502f4-116">Standardmäßig ist das Indexer-Objekt für die Suche konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="502f4-116">By default, the indexer object is configured for seeking.</span></span>
3.  <span data-ttu-id="502f4-117">Aufrufen von [**imfasfindexer:: getindexposition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) , um den Offset des Indexes innerhalb der ASF-Datei zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="502f4-117">Call [**IMFASFIndexer::GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) to find the offset of the index within the ASF file.</span></span>
4.  <span data-ttu-id="502f4-118">Rufen Sie die [**mfkreateasfindexerbytestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) -Funktion auf, um einen Bytestream zum Lesen des Indexes zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="502f4-118">Call the [**MFCreateASFIndexerByteStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) function to create a byte stream for reading the index.</span></span> <span data-ttu-id="502f4-119">Die Eingabe für diese Funktion ist ein Zeiger auf einen Bytestream, der die ASF-Datei enthält, und auf den Offset des Indexes (aus dem vorherigen Schritt).</span><span class="sxs-lookup"><span data-stu-id="502f4-119">The input to this function is a pointer to a byte stream that contains the ASF file, and the offset of the index (from the previous step).</span></span>
5.  <span data-ttu-id="502f4-120">Aufrufen von [**imfasfindexer:: setindexbytestreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) zum Festlegen des Index Byte-Streams für den Indexer.</span><span class="sxs-lookup"><span data-stu-id="502f4-120">Call [**IMFASFIndexer::SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) to set the index byte stream on the indexer.</span></span>

<span data-ttu-id="502f4-121">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="502f4-121">The following code shows these steps:</span></span>


```C++
HRESULT CreateASFIndexer(
    IMFByteStream *pContentByteStream,  // Pointer to the content byte stream
    IMFASFContentInfo *pContentInfo,
    IMFASFIndexer **ppIndexer
    )
{
    IMFASFIndexer *pIndexer = NULL;
    IMFByteStream *pIndexerByteStream = NULL;

    QWORD qwLength = 0, qwIndexOffset = 0, qwBytestreamLength = 0;

    // Create the indexer.
    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    //Initialize the indexer to work with this ASF library
    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Check if the index exists. You can only do this after creating the indexer

    //Get byte stream length
    hr = pContentByteStream->GetLength(&qwLength);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get index offset
    hr = pIndexer->GetIndexPosition(pContentInfo, &qwIndexOffset);
    if (FAILED(hr))
    {
        goto done;
    }

    if ( qwIndexOffset >= qwLength)
    {
        //index object does not exist, release the indexer
        goto done;
    }
    else
    {
        // initialize the indexer
        // Create a byte stream that the Indexer will use to read in
        // and parse the indexers.
         hr = MFCreateASFIndexerByteStream(
             pContentByteStream,
             qwIndexOffset,
             &pIndexerByteStream
             );

        if (FAILED(hr))
        {
            goto done;
        }
   }

    hr = pIndexer->SetIndexByteStreams(&pIndexerByteStream, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    SafeRelease(&pIndexer);
    SafeRelease(&pIndexerByteStream);
    return hr;
}
```



## <a name="getting-the-seek-position"></a><span data-ttu-id="502f4-122">Die Such Position wird erhalten.</span><span class="sxs-lookup"><span data-stu-id="502f4-122">Getting the Seek Position.</span></span>

1.  <span data-ttu-id="502f4-123">Um herauszufinden, ob ein bestimmter Stream indiziert ist, müssen Sie [**imfasfindexer:: getindexstatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="502f4-123">To find out if a particular stream is indexed, call [**IMFASFIndexer::GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus).</span></span> <span data-ttu-id="502f4-124">Wenn der Stream indiziert ist, erhält der *pfisindexed* -Parameter den Wert " **true**". Andernfalls wird der Wert **false** empfangen.</span><span class="sxs-lookup"><span data-stu-id="502f4-124">If the stream is indexed, the *pfIsIndexed* parameter receives the value **TRUE**; otherwise it receives the value **FALSE**.</span></span>
2.  <span data-ttu-id="502f4-125">Standardmäßig verwendet der Indexer Forward-Suche.</span><span class="sxs-lookup"><span data-stu-id="502f4-125">By default, the indexer uses forward seeking.</span></span> <span data-ttu-id="502f4-126">Für Reverse-Suche (d. h. Durchsuchen am Ende der Datei), wird [**imfasfindexer:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) aufgerufen und der **mfasf- \_ Indexer-Lesevorgang für das \_ \_ \_ reverseplayback** -Flag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="502f4-126">For reverse seeking (that is, seeking from the end of the file), call [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) and set the **MFASF\_INDEXER\_READ\_FOR\_REVERSEPLAYBACK** flag.</span></span> <span data-ttu-id="502f4-127">Überspringen Sie andernfalls diesen Schritt.</span><span class="sxs-lookup"><span data-stu-id="502f4-127">Otherwise, skip this step.</span></span>
3.  <span data-ttu-id="502f4-128">Wenn der Stream indiziert ist, rufen Sie die Suchposition für eine bestimmte Präsentationszeit durch Aufrufen von [**imfasfindexer:: getseekpositionforvalue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue)ab.</span><span class="sxs-lookup"><span data-stu-id="502f4-128">If the stream is indexed, get the seek position for a specified presentation time by calling [**IMFASFIndexer::GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue).</span></span> <span data-ttu-id="502f4-129">Diese Methode liest den ASF-Index und findet den Index Eintrag, der der angeforderten Zeit am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="502f4-129">This method reads the ASF index and finds the index entry that is closest to the requested time.</span></span> <span data-ttu-id="502f4-130">Die-Methode gibt den Byte Offset des Datenpakets zurück, das durch den Index Eintrag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="502f4-130">The method returns the byte offset of the data packet specified by the index entry.</span></span> <span data-ttu-id="502f4-131">Der Byte Offset ist relativ zum Anfang des ASF-Datenobjekts.</span><span class="sxs-lookup"><span data-stu-id="502f4-131">The byte offset is relative to the start of the ASF Data Object.</span></span>

<span data-ttu-id="502f4-132">Die [**getseekpositionforvalue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) -Methode nimmt einen Zeiger auf die Struktur des [**ASF- \_ Index \_ Bezeichners**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) an.</span><span class="sxs-lookup"><span data-stu-id="502f4-132">The [**GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) method takes a pointer to the [**ASF\_INDEX\_IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) structure.</span></span> <span data-ttu-id="502f4-133">Diese Struktur gibt einen Indextyp und einen Datenstrom Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="502f4-133">This structure specifies an index type and a stream identifier.</span></span> <span data-ttu-id="502f4-134">Derzeit muss der Indextyp "GUID \_ null" sein, der die zeitbasierte Indizierung angibt.</span><span class="sxs-lookup"><span data-stu-id="502f4-134">Currently, the index type must be GUID\_NULL, which specifies time-based indexing.</span></span>

<span data-ttu-id="502f4-135">Der folgende Code Ruft eine Suchposition ab, wenn ein Datenstrom Bezeichner und eine Ziel Präsentationszeit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="502f4-135">The following code gets a seek position, given a stream identifier and target presentation time.</span></span> <span data-ttu-id="502f4-136">Wenn der Aufruf erfolgreich ist, wird der Daten Offset im *pcbdataoffset* -Parameter und die ungefähre tatsächliche Suchzeit in *phnsapproxseektime* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="502f4-136">If the call succeeds, it returns the data offset in the *pcbDataOffset* parameter and the approximate actual seek time in *phnsApproxSeekTime*.</span></span>


```C++
HRESULT GetSeekPositionWithIndexer(
    IMFASFIndexer *pIndexer,
    WORD          wStreamNumber,
    MFTIME        hnsSeekTime,          // Desired seek time, in 100-nsec.
    BOOL          bReverse,
    QWORD         *pcbDataOffset,       // Receives the offset in bytes.
    MFTIME        *phnsApproxSeekTime   // Receives the approximate seek time.
    )
{
    // Query whether the stream is indexed.

    ASF_INDEX_IDENTIFIER IndexIdentifier = { GUID_NULL, wStreamNumber };

    BOOL fIsIndexed = FALSE;

    ASF_INDEX_DESCRIPTOR descriptor;

    DWORD cbIndexDescriptor = sizeof(descriptor);

    HRESULT hr = pIndexer->GetIndexStatus(
        &IndexIdentifier,
        &fIsIndexed,
        (BYTE*)&descriptor,
        &cbIndexDescriptor
        );

    if (hr == MF_E_BUFFERTOOSMALL)
    {
        hr = S_OK;
    }
    else if (FAILED(hr))
    {
        goto done;
    }

    if (!fIsIndexed)
    {
        hr = MF_E_ASF_NOINDEX;
        goto done;
    }

    if (bReverse)
    {
        hr = pIndexer->SetFlags(MFASF_INDEXER_READ_FOR_REVERSEPLAYBACK);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Get the offset from the indexer.

    PROPVARIANT var;

    var.vt = VT_I8;
    var.hVal.QuadPart = hnsSeekTime;

    hr = pIndexer->GetSeekPositionForValue(
        &var,
        &IndexIdentifier,
        pcbDataOffset,
        phnsApproxSeekTime,
        0
        );

done:
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="502f4-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="502f4-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="502f4-138">ASF-Indexer</span><span class="sxs-lookup"><span data-stu-id="502f4-138">ASF Indexer</span></span>](asf-index-object.md)
</dt> </dl>

 

 



