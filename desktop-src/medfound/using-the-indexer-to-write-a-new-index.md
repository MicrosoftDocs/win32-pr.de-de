---
description: In diesem Thema wird gezeigt, wie Sie einen Index für eine ASF-Datei (Advanced Systems Format) schreiben.
ms.assetid: a14e3bef-0232-4259-930a-d860ed9230fd
title: Verwenden des Indexers zum Schreiben eines neuen Indexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37922b693c83a8417dea4006fc38397b805fb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753833"
---
# <a name="using-the-indexer-to-write-a-new-index"></a><span data-ttu-id="2805d-103">Verwenden des Indexers zum Schreiben eines neuen Indexes</span><span class="sxs-lookup"><span data-stu-id="2805d-103">Using the Indexer to Write a New Index</span></span>

<span data-ttu-id="2805d-104">In diesem Thema wird gezeigt, wie Sie einen Index für eine ASF-Datei (Advanced Systems Format) schreiben.</span><span class="sxs-lookup"><span data-stu-id="2805d-104">This topic shows how to write an index for an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="2805d-105">Im folgenden finden Sie das allgemeine Verfahren zum Erstellen eines ASF-Indexes:</span><span class="sxs-lookup"><span data-stu-id="2805d-105">Here is the general procedure for creating an ASF index:</span></span>

1.  <span data-ttu-id="2805d-106">Initialisieren Sie eine neue Instanz des ASF [-indexerobjekts, wie unter Indexer-Erstellung und-Konfiguration](indexer-creation-and-configuration.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2805d-106">Initialize a new instance of the ASF indexer object, as described in [Indexer Creation and Configuration](indexer-creation-and-configuration.md).</span></span>
2.  <span data-ttu-id="2805d-107">Konfigurieren Sie optional den Indexer.</span><span class="sxs-lookup"><span data-stu-id="2805d-107">Optionally, configure the indexer.</span></span>
3.  <span data-ttu-id="2805d-108">Senden von ASF-Datenpaketen an den Indexer.</span><span class="sxs-lookup"><span data-stu-id="2805d-108">Send ASF data packets to the indexer.</span></span>
4.  <span data-ttu-id="2805d-109">Commit für den Index durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="2805d-109">Commit the index.</span></span>
5.  <span data-ttu-id="2805d-110">Holen Sie den abgeschlossenen Index aus dem Indexer, und schreiben Sie ihn in einen Stream.</span><span class="sxs-lookup"><span data-stu-id="2805d-110">Get the completed index from the indexer, and write it to a stream.</span></span>

## <a name="configure-the-indexer"></a><span data-ttu-id="2805d-111">Konfigurieren des Indexers</span><span class="sxs-lookup"><span data-stu-id="2805d-111">Configure the Indexer</span></span>

<span data-ttu-id="2805d-112">Um den Indexer zum Schreiben eines neuen Index Objekts zu verwenden, muss das Indexer-Objekt über das Flag "mfasf \_ Indexer \_ schreiben \_ neuen \_ indexset mit einem Aufruf an [**imfasfindexer:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) " verfügen, bevor es mit [**imfasfindexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize)initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2805d-112">To use the indexer to write a new index object, the indexer object must have the flag MFASF\_INDEXER\_WRITE\_NEW\_INDEX set with a call to [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) before it is initialized with [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize).</span></span>

<span data-ttu-id="2805d-113">Wenn der Indexer zum Schreiben eines Indexes konfiguriert ist, wählt der Aufrufer die zu indizierenden Datenströme aus.</span><span class="sxs-lookup"><span data-stu-id="2805d-113">When the indexer is configured for writing an index, the caller chooses the streams to be indexed.</span></span> <span data-ttu-id="2805d-114">Standardmäßig versucht der Indexer, ein Index Objekt für alle Streams zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2805d-114">By default, the indexer attempts to create an Index Object for all streams.</span></span> <span data-ttu-id="2805d-115">Das Standardzeit Intervall beträgt eine Sekunde.</span><span class="sxs-lookup"><span data-stu-id="2805d-115">The default time interval is one second.</span></span>

<span data-ttu-id="2805d-116">[**Imfasfindexer:: setindexstatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) kann verwendet werden, um die standardmäßige Auswahl von Streams und Index Typen des indexerobjekts zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="2805d-116">[**IMFASFIndexer::SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) can be used to override the indexer object's default choice of streams and index types.</span></span>

<span data-ttu-id="2805d-117">Der folgende Beispielcode zeigt die Initialisierung eines ASF \_ -Index \_ Deskriptors und einen ASF- \_ Index \_ Bezeichner vor einem Aufrufen von [**setindexstatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span><span class="sxs-lookup"><span data-stu-id="2805d-117">The following example code shows the initialization of an ASF\_INDEX\_DESCRIPTOR and an ASF\_INDEX\_IDENTIFIER before a call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span>


```
ASF_INDEX_DESCRIPTOR IndexerType;
ZeroMemory(&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR));

ASF_INDEX_IDENTIFIER IndexIdentifier;
ZeroMemory(&IndexIdentifier, sizeof(ASF_INDEX_IDENTIFIER));

IndexIdentifier.guidIndexType = GUID_NULL;
IndexIdentifier.wStreamNumber = 1;

IndexerType.Identifier = IndexIdentifier;
IndexerType.cPerEntryBytes  = MFASFINDEXER_PER_ENTRY_BYTES_DYNAMIC;
IndexerType.dwInterval  = MFASFINDEXER_NO_FIXED_INTERVAL;

hr = pIndexer->SetIndexStatus((BYTE*)&IndexerType, sizeof(ASF_INDEX_DESCRIPTOR), TRUE);
```



<span data-ttu-id="2805d-118">Für den Index Bezeichner muss der GUID-Indextyp auf GUID NULL festgelegt sein \_ , um anzugeben, dass es sich bei dem Indextyp um eine Präsentationszeit basiert.</span><span class="sxs-lookup"><span data-stu-id="2805d-118">The index identifier must have its GUID index type set to GUID\_NULL to indicate that the index type will be presentation time-based.</span></span> <span data-ttu-id="2805d-119">Der Index Bezeichner muss ebenfalls mit der streamnummer des zu indizierenden ASF-Datenstroms initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2805d-119">The index identifier must also be initialized with the stream number of the ASF stream to be indexed.</span></span> <span data-ttu-id="2805d-120">Nachdem der Index Bezeichner festgelegt wurde, verwenden Sie ihn, um den Index Deskriptor zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="2805d-120">After the index identifier is set, use it to initialize the index descriptor.</span></span>

<span data-ttu-id="2805d-121">Die Index deskriptorstruktur enthält Member, die vor dem Aufrufen von [**setindexstatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus)festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2805d-121">The index descriptor structure has members which must be set before the call to [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).</span></span> <span data-ttu-id="2805d-122">Der **Bezeichner** ist eine Struktur des [**ASF- \_ Index \_ Bezeichners**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) , die die streamnummer und den Indextyp identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2805d-122">**Identifier** is an [**ASF\_INDEX\_IDENTIFIER**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) structure that identifies the stream number and the type of index.</span></span> <span data-ttu-id="2805d-123">**cperentrybytes** ist die Anzahl der Bytes, die für jeden Index Eintrag verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2805d-123">**cPerEntryBytes** is the number of bytes used for each index entry.</span></span> <span data-ttu-id="2805d-124">Wenn der Wert "mfasfindexer" für " \_ \_ Dynamic Entry Bytes" ist \_ \_ , haben die Indexeinträge eine Variable Größe.</span><span class="sxs-lookup"><span data-stu-id="2805d-124">If the value is MFASFINDEXER\_PER\_ENTRY\_BYTES\_DYNAMIC, the index entries have variable size.</span></span> <span data-ttu-id="2805d-125">**dwinterval** ist das Indizierungs Intervall.</span><span class="sxs-lookup"><span data-stu-id="2805d-125">**dwInterval** is the indexing interval.</span></span> <span data-ttu-id="2805d-126">Der Wert mfasfindexer \_ kein \_ festes Intervall gibt an \_ , dass kein festes Indizierungs Intervall vorliegt.</span><span class="sxs-lookup"><span data-stu-id="2805d-126">A value of MFASFINDEXER\_NO\_FIXED\_INTERVAL indicates that there is no fixed indexing interval.</span></span>

## <a name="send-asf-data-packets-to-the-indexer"></a><span data-ttu-id="2805d-127">Senden von ASF-Datenpaketen an den Indexer</span><span class="sxs-lookup"><span data-stu-id="2805d-127">Send ASF Data Packets to the Indexer</span></span>

<span data-ttu-id="2805d-128">Da der Indexer ein wmcontainer-Objekt ist, muss es während der Paket Generierung in Verbindung mit dem Multiplexer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2805d-128">Because the indexer is a WMContainer level object, it must be used in conjunction with the multiplexer during packet generation.</span></span>

<span data-ttu-id="2805d-129">Von [**getnextpacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) zurückgegebene Pakete können durch Aufrufe von [**generateindexentries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) an das Indexer-Objekt gesendet werden, wobei Indexeinträge für jedes gesendete Paket erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2805d-129">Packets returned from [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) can be sent to the indexer object through calls to [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) where it creates index entries for each packet sent.</span></span>

<span data-ttu-id="2805d-130">Der folgende Code veranschaulicht, wie dies möglich ist:</span><span class="sxs-lookup"><span data-stu-id="2805d-130">The following code demonstrates how this may be done:</span></span>


```C++
HRESULT SendSampleToMux(
    IMFASFMultiplexer *pMux,
    IMFASFIndexer *pIndex,
    IMFSample *pSample,
    WORD wStream,
    IMFByteStream *pDestStream
    )
{
    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacket = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    HRESULT hr = pMux->ProcessSample(wStream, pSample, 0);
    if (FAILED(hr))
    {
        goto done;
    }

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pOutputSample)
        {
            // Send the data packet to the indexer
            hr = pIndex->GenerateIndexEntries(pOutputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // Convert the sample to a contiguous buffer.
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacket);
            if (FAILED(hr))
            {
                goto done;
            }

            // Write the buffer to the byte stream.
            hr = WriteBufferToByteStream(pDestStream, pDataPacket, NULL);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        SafeRelease(&pOutputSample);
        SafeRelease(&pDataPacket);
    }

done:
    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacket);
    return hr;
}
```



<span data-ttu-id="2805d-131">Weitere Informationen finden Sie unter [Erstellen neuer ASF-Datenpakete](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="2805d-131">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="commit-the-index"></a><span data-ttu-id="2805d-132">Commit für den Index</span><span class="sxs-lookup"><span data-stu-id="2805d-132">Commit the Index</span></span>

<span data-ttu-id="2805d-133">Nachdem für das letzte Paket ein Index Eintrag erstellt wurde, muss für den Index ein Commit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2805d-133">After the last packet has had an index entry created for it, the index must be committed.</span></span> <span data-ttu-id="2805d-134">Dies erfolgt mit einem Rückruf von [**imfasfindexer:: commitindex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex).</span><span class="sxs-lookup"><span data-stu-id="2805d-134">This is done with a call to [**IMFASFIndexer::CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex).</span></span> <span data-ttu-id="2805d-135">**Commitindex** übernimmt einen Zeiger auf das ContentInfo-Objekt, das den Inhalt der ASF-Datei beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2805d-135">**CommitIndex** takes a pointer to the ContentInfo object which describes the content of the ASF file.</span></span> <span data-ttu-id="2805d-136">Das Ausführen eines Commits für den Index schließt die Indizierung ein und aktualisiert den Header mit neuen Informationen über die Dateigröße und die seekzulässigkeit.</span><span class="sxs-lookup"><span data-stu-id="2805d-136">Committing the index finishes the indexing and updates the header with new information about file size and seekability.</span></span>

## <a name="get-the-completed-index"></a><span data-ttu-id="2805d-137">Abgeschlossener Index erhalten</span><span class="sxs-lookup"><span data-stu-id="2805d-137">Get the Completed Index</span></span>

<span data-ttu-id="2805d-138">Um den abgeschlossenen Index vom Indexer zu erhalten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="2805d-138">To get the completed index from the indexer, perform the following steps:</span></span>

1.  <span data-ttu-id="2805d-139">Aufrufen von [**imfasfindexer:: getindexwrite tespace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) , um die Größe des Indexes zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2805d-139">Call [**IMFASFIndexer::GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) to get the size of the index.</span></span>
2.  <span data-ttu-id="2805d-140">Rufen Sie [**mfkreatememorybuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) auf, um einen Medien Puffer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2805d-140">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer.</span></span> <span data-ttu-id="2805d-141">Sie können entweder einen Puffer zuordnen, der groß genug ist, um den gesamten Index aufzunehmen, indem Sie einen kleineren Puffer zuordnen und den Index in Blöcken erhalten.</span><span class="sxs-lookup"><span data-stu-id="2805d-141">You can either allocate an buffer that is large enough to hold the entire index, of allocate a smaller buffer and get the index in chunks.</span></span>
3.  <span data-ttu-id="2805d-142">Zum Abrufen der Indexdaten muss [**imfasfindexer:: getcompletedindex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2805d-142">Call [**IMFASFIndexer::GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) to get the index data.</span></span> <span data-ttu-id="2805d-143">Legen Sie beim ersten Aufrufen den *cboffsetwithinindex* -Parameter auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="2805d-143">On the first call, set the *cbOffsetWithinIndex* parameter to zero.</span></span> <span data-ttu-id="2805d-144">Wenn Sie den Index in Blöcken abrufen, erhöhen Sie *cboffsetwithinindex* jedes Mal um die Größe der Daten aus dem vorherigen Aufruf.</span><span class="sxs-lookup"><span data-stu-id="2805d-144">If you get the index in chunks, increment *cbOffsetWithinIndex* each time by the size of the data from the previous call.</span></span>
4.  <span data-ttu-id="2805d-145">Um einen Zeiger auf die Indexdaten und die Größe der Daten zu erhalten, wird [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2805d-145">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the index data and the size of the data.</span></span>
5.  <span data-ttu-id="2805d-146">Schreiben Sie die Indexdaten in die ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="2805d-146">Write the index data to the ASF file.</span></span>
6.  <span data-ttu-id="2805d-147">Zum Entsperren des Medien Puffers wird [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2805d-147">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the media buffer.</span></span>
7.  <span data-ttu-id="2805d-148">Wiederholen Sie die Schritte 3 – 6, bis Sie den gesamten Index geschrieben haben.</span><span class="sxs-lookup"><span data-stu-id="2805d-148">Repeat steps 3–6 until you have written the entire index.</span></span>

<span data-ttu-id="2805d-149">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="2805d-149">The following code shows these steps:</span></span>


```C++
HRESULT WriteASFIndex(IMFASFIndexer *pIndex,IMFByteStream *pStream)
{
    const DWORD cbChunkSize = 4096;

    IMFMediaBuffer *pBuffer = NULL;

    QWORD cbIndex = 0;
    DWORD cbIndexWritten = 0;

    HRESULT hr = pIndex->GetIndexWriteSpace(&cbIndex);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateMemoryBuffer(cbChunkSize, &pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    while (cbIndexWritten < cbIndex)
    {
        BYTE *pData = NULL;
        DWORD cbData = 0;
        DWORD cbWritten = 0;

        hr = pIndex->GetCompletedIndex(pBuffer, cbIndexWritten);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pBuffer->Lock(&pData, NULL, &cbData);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStream->Write(pData, cbData, &cbWritten);

        (void)pBuffer->Unlock();

        if (FAILED(hr))
        {
            goto done;
        }

        cbIndexWritten += cbData;
    }

done:
    SafeRelease(&pBuffer);
    return hr;
};
```



## <a name="related-topics"></a><span data-ttu-id="2805d-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2805d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2805d-151">ASF-Indexer</span><span class="sxs-lookup"><span data-stu-id="2805d-151">ASF Indexer</span></span>](asf-index-object.md)
</dt> </dl>

 

 



