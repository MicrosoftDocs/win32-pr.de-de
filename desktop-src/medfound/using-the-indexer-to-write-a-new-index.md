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
# <a name="using-the-indexer-to-write-a-new-index"></a>Verwenden des Indexers zum Schreiben eines neuen Indexes

In diesem Thema wird gezeigt, wie Sie einen Index für eine ASF-Datei (Advanced Systems Format) schreiben.

Im folgenden finden Sie das allgemeine Verfahren zum Erstellen eines ASF-Indexes:

1.  Initialisieren Sie eine neue Instanz des ASF [-indexerobjekts, wie unter Indexer-Erstellung und-Konfiguration](indexer-creation-and-configuration.md)beschrieben.
2.  Konfigurieren Sie optional den Indexer.
3.  Senden von ASF-Datenpaketen an den Indexer.
4.  Commit für den Index durchsetzen.
5.  Holen Sie den abgeschlossenen Index aus dem Indexer, und schreiben Sie ihn in einen Stream.

## <a name="configure-the-indexer"></a>Konfigurieren des Indexers

Um den Indexer zum Schreiben eines neuen Index Objekts zu verwenden, muss das Indexer-Objekt über das Flag "mfasf \_ Indexer \_ schreiben \_ neuen \_ indexset mit einem Aufruf an [**imfasfindexer:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) " verfügen, bevor es mit [**imfasfindexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize)initialisiert wird.

Wenn der Indexer zum Schreiben eines Indexes konfiguriert ist, wählt der Aufrufer die zu indizierenden Datenströme aus. Standardmäßig versucht der Indexer, ein Index Objekt für alle Streams zu erstellen. Das Standardzeit Intervall beträgt eine Sekunde.

[**Imfasfindexer:: setindexstatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus) kann verwendet werden, um die standardmäßige Auswahl von Streams und Index Typen des indexerobjekts zu überschreiben.

Der folgende Beispielcode zeigt die Initialisierung eines ASF \_ -Index \_ Deskriptors und einen ASF- \_ Index \_ Bezeichner vor einem Aufrufen von [**setindexstatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus).


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



Für den Index Bezeichner muss der GUID-Indextyp auf GUID NULL festgelegt sein \_ , um anzugeben, dass es sich bei dem Indextyp um eine Präsentationszeit basiert. Der Index Bezeichner muss ebenfalls mit der streamnummer des zu indizierenden ASF-Datenstroms initialisiert werden. Nachdem der Index Bezeichner festgelegt wurde, verwenden Sie ihn, um den Index Deskriptor zu initialisieren.

Die Index deskriptorstruktur enthält Member, die vor dem Aufrufen von [**setindexstatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexstatus)festgelegt werden müssen. Der **Bezeichner** ist eine Struktur des [**ASF- \_ Index \_ Bezeichners**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) , die die streamnummer und den Indextyp identifiziert. **cperentrybytes** ist die Anzahl der Bytes, die für jeden Index Eintrag verwendet werden. Wenn der Wert "mfasfindexer" für " \_ \_ Dynamic Entry Bytes" ist \_ \_ , haben die Indexeinträge eine Variable Größe. **dwinterval** ist das Indizierungs Intervall. Der Wert mfasfindexer \_ kein \_ festes Intervall gibt an \_ , dass kein festes Indizierungs Intervall vorliegt.

## <a name="send-asf-data-packets-to-the-indexer"></a>Senden von ASF-Datenpaketen an den Indexer

Da der Indexer ein wmcontainer-Objekt ist, muss es während der Paket Generierung in Verbindung mit dem Multiplexer verwendet werden.

Von [**getnextpacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) zurückgegebene Pakete können durch Aufrufe von [**generateindexentries**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-generateindexentries) an das Indexer-Objekt gesendet werden, wobei Indexeinträge für jedes gesendete Paket erstellt werden.

Der folgende Code veranschaulicht, wie dies möglich ist:


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



Weitere Informationen finden Sie unter [Erstellen neuer ASF-Datenpakete](generating-new-asf-data-packets.md).

## <a name="commit-the-index"></a>Commit für den Index

Nachdem für das letzte Paket ein Index Eintrag erstellt wurde, muss für den Index ein Commit ausgeführt werden. Dies erfolgt mit einem Rückruf von [**imfasfindexer:: commitindex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-commitindex). **Commitindex** übernimmt einen Zeiger auf das ContentInfo-Objekt, das den Inhalt der ASF-Datei beschreibt. Das Ausführen eines Commits für den Index schließt die Indizierung ein und aktualisiert den Header mit neuen Informationen über die Dateigröße und die seekzulässigkeit.

## <a name="get-the-completed-index"></a>Abgeschlossener Index erhalten

Um den abgeschlossenen Index vom Indexer zu erhalten, führen Sie die folgenden Schritte aus:

1.  Aufrufen von [**imfasfindexer:: getindexwrite tespace**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexwritespace) , um die Größe des Indexes zu erhalten.
2.  Rufen Sie [**mfkreatememorybuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) auf, um einen Medien Puffer zu erstellen. Sie können entweder einen Puffer zuordnen, der groß genug ist, um den gesamten Index aufzunehmen, indem Sie einen kleineren Puffer zuordnen und den Index in Blöcken erhalten.
3.  Zum Abrufen der Indexdaten muss [**imfasfindexer:: getcompletedindex**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getcompletedindex) aufgerufen werden. Legen Sie beim ersten Aufrufen den *cboffsetwithinindex* -Parameter auf 0 (null) fest. Wenn Sie den Index in Blöcken abrufen, erhöhen Sie *cboffsetwithinindex* jedes Mal um die Größe der Daten aus dem vorherigen Aufruf.
4.  Um einen Zeiger auf die Indexdaten und die Größe der Daten zu erhalten, wird [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) aufgerufen.
5.  Schreiben Sie die Indexdaten in die ASF-Datei.
6.  Zum Entsperren des Medien Puffers wird [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) aufgerufen.
7.  Wiederholen Sie die Schritte 3 – 6, bis Sie den gesamten Index geschrieben haben.

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

 

 



