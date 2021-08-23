---
description: In diesem Thema wird gezeigt, wie Sie einen Index für eine ASF-Datei (Advanced Systems Format) schreiben.
ms.assetid: a14e3bef-0232-4259-930a-d860ed9230fd
title: Verwenden des Indexers zum Schreiben eines neuen Indexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fbc604a9493f7feea61e34500e0f620a051b05b1431ec2d4917df9f8ed15b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034528"
---
# <a name="using-the-indexer-to-write-a-new-index"></a>Verwenden des Indexers zum Schreiben eines neuen Indexes

In diesem Thema wird gezeigt, wie Sie einen Index für eine ASF-Datei (Advanced Systems Format) schreiben.

Dies ist das allgemeine Verfahren zum Erstellen eines ASF-Indexes:

1.  Initialisieren Sie eine neue Instanz des ASF-Indexerobjekts, wie unter [Indexererstellung und -konfiguration beschrieben.](indexer-creation-and-configuration.md)
2.  Konfigurieren Sie optional den Indexer.
3.  Senden sie ASF-Datenpakete an den Indexer.
4.  Commit des Indexes.
5.  Erhalten Sie den abgeschlossenen Index vom Indexer, und schreiben Sie ihn in einen Stream.

## <a name="configure-the-indexer"></a>Konfigurieren des Indexers

Damit der Indexer ein neues Indexobjekt schreiben kann, muss für das Indexerobjekt das Flag MFASF INDEXER WRITE NEW INDEX mit einem Aufruf von \_ \_ \_ \_ [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) festgelegt sein, bevor es mit [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize)initialisiert wird.

Wenn der Indexer für das Schreiben eines Index konfiguriert ist, wählt der Aufrufer die zu indizierten Datenströme aus. Standardmäßig versucht der Indexer, ein Indexobjekt für alle Datenströme zu erstellen. Das Standardzeitintervall ist eine Sekunde.

[**IMFASFIndexer::SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) kann verwendet werden, um die Standardauswahl von Datenströmen und Indextypen des Indexerobjekts zu überschreiben.

Der folgende Beispielcode zeigt die Initialisierung eines ASF INDEX DESCRIPTOR und eines ASF INDEX IDENTIFIER vor einem Aufruf \_ \_ von \_ \_ [**SetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).


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



Für den Indexbezeichner muss der GUID-Indextyp auf GUID NULL festgelegt sein, um anzugeben, dass der Indextyp auf der \_ Präsentationszeit basiert. Der Indexbezeichner muss auch mit der Streamnummer des asf-Streams initialisiert werden, der indiziert werden soll. Nachdem der Indexbezeichner festgelegt wurde, verwenden Sie ihn, um den Indexdeskriptor zu initialisieren.

Die Indexdeskriptorstruktur verfügt über Member, die vor dem Aufruf von [**SetIndexStatus festgelegt werden müssen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) **Bezeichner** ist eine [**ASF \_ INDEX \_ IDENTIFIER-Struktur,**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) die die Streamnummer und den Indextyp identifiziert. **cPerEntryBytes ist** die Anzahl von Bytes, die für jeden Indexeintrag verwendet werden. Wenn der Wert MFASFINDEXER PER ENTRY BYTES DYNAMIC ist, haben die \_ \_ \_ \_ Indexeinträge eine variable Größe. **dwInterval ist** das Indizierungsintervall. Der Wert MFASFINDEXER NO FIXED INTERVAL gibt an, dass \_ \_ es kein \_ festes Indizierungsintervall gibt.

## <a name="send-asf-data-packets-to-the-indexer"></a>Senden von ASF-Datenpaketen an den Indexer

Da der Indexer ein WMContainer-Ebenenobjekt ist, muss er während der Paketgenerierung in Verbindung mit dem Multiplexer verwendet werden.

Von [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) zurückgegebene Pakete können über Aufrufe von [**GenerateIndexEntries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) an das Indexerobjekt gesendet werden, wo Indexeinträge für jedes gesendete Paket erstellt werden.

Der folgende Code veranschaulicht, wie dies erfolgen kann:


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



Weitere Informationen finden Sie unter [Generieren neuer ASF-Datenpakete.](generating-new-asf-data-packets.md)

## <a name="commit-the-index"></a>Commit des Indexes

Nachdem für das letzte Paket ein Indexeintrag erstellt wurde, muss für den Index ein Committed für den Index erstellt werden. Dies erfolgt mit einem Aufruf von [**IMFASFIndexer::CommitIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex). **CommitIndex** verwendet einen Zeiger auf das ContentInfo-Objekt, das den Inhalt der ASF-Datei beschreibt. Das Committen des Indexes beendet die Indizierung und aktualisiert den Header mit neuen Informationen zur Dateigröße und Suchbarkeit.

## <a name="get-the-completed-index"></a>Get the Completed Index

Führen Sie die folgenden Schritte aus, um den abgeschlossenen Index vom Indexer zu erhalten:

1.  Rufen [**Sie IMFASFIndexer::GetIndexWriteSpace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) auf, um die Größe des Indexes zu erhalten.
2.  Rufen [**Sie MFCreateMemoryBuffer auf,**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) um einen Medienpuffer zu erstellen. Sie können entweder einen Puffer zuordnen, der groß genug ist, um den gesamten Index zu halten, einen kleineren Puffer zu zuordnen und den Index in Blocken zu erhalten.
3.  Rufen [**Sie IMFASFIndexer::GetCompletedIndex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) auf, um die Indexdaten zu erhalten. Legen Sie beim ersten Aufruf den *cbOffsetWithinIndex-Parameter* auf 0 (null) fest. Wenn Sie den Index in Blocken erhalten, erhöhen Sie *cbOffsetWithinIndex* jedes Mal um die Größe der Daten aus dem vorherigen Aufruf.
4.  Rufen [**SieGEMEDIABuffer::Lock auf,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) um einen Zeiger auf die Indexdaten und die Größe der Daten zu erhalten.
5.  Schreiben Sie die Indexdaten in die ASF-Datei.
6.  Rufen [**Sie DEN MEDIENPUFFER::Entsperren auf,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) um den Medienpuffer zu entsperren.
7.  Wiederholen Sie die Schritte 3 bis 6, bis Sie den gesamten Index geschrieben haben.

Diese Schritte sind im folgenden Code dargestellt:


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Indexer](asf-index-object.md)
</dt> </dl>

 

 



