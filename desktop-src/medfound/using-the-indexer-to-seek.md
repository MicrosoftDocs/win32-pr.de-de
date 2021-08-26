---
description: Der ASF-Indexer ist eine WMContainer-Schichtkomponente, die zum Lesen oder Schreiben von Indexobjekten in einer ASF-Datei (Advanced Systems Format) verwendet wird. Dieses Thema enthält Informationen zur Verwendung des ASF-Indexers zum Suchen innerhalb einer ASF-Datei.
ms.assetid: 9c501d33-847e-448e-a19c-39dfbc7757ca
title: Verwenden des Indexers zum Suchen innerhalb einer ASF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c674aa809c858856abf0c0e84c5d854b399c6fbc125ac9210e19b695380bd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887240"
---
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a>Verwenden des Indexers zum Suchen innerhalb einer ASF-Datei

Der *ASF-Indexer* ist eine WMContainer-Schichtkomponente, die zum Lesen oder Schreiben von Indexobjekten in einer ASF-Datei (Advanced Systems Format) verwendet wird. Dieses Thema enthält Informationen zur Verwendung des ASF-Indexers zum Suchen innerhalb einer ASF-Datei.

-   [Initialisieren des Indexers für Suche](#initializing-the-indexer-for-seeking)
-   [Abrufen der Suchposition.](#getting-the-seek-position)
-   [Zugehörige Themen](#related-topics)

Informationen zur Struktur einer ASF-Datei finden Sie unter [ASF-Dateistruktur.](asf-file-structure.md)

## <a name="initializing-the-indexer-for-seeking"></a>Initialisieren des Indexers für Suche

So initialisieren Sie den ASF-Indexer für die Suche:

1.  Rufen Sie [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) auf, um eine neue Instanz des ASF-Indexers zu erstellen.
2.  Rufen Sie [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) auf, um den Indexer zu initialisieren. Diese Methode ruft Informationen aus dem ASF-Header ab, um zu bestimmen, welche ASF-Streams indiziert werden. Standardmäßig ist das Indexerobjekt für die Suche konfiguriert.
3.  Rufen Sie [**IMFASFIndexer::GetIndexPosition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) auf, um den Offset des Indexes in der ASF-Datei zu suchen.
4.  Rufen Sie die [**MFCreateASFIndexerByteStream-Funktion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) auf, um einen Bytestream zum Lesen des Indexes zu erstellen. Die Eingabe für diese Funktion ist ein Zeiger auf einen Bytestream, der die ASF-Datei und den Offset des Indexes (aus dem vorherigen Schritt) enthält.
5.  Rufen Sie [**IMFASFIndexer::SetIndexByteStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) auf, um den Indexbytestream für den Indexer festzulegen.

Diese Schritte sind im folgenden Code dargestellt:


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



## <a name="getting-the-seek-position"></a>Abrufen der Suchposition.

1.  Um herauszufinden, ob ein bestimmter Stream indiziert ist, rufen Sie [**IMFASFIndexer::GetIndexStatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus)auf. Wenn der Stream indiziert ist, empfängt der *pfIsIndexed-Parameter* den Wert **TRUE**. Andernfalls wird der Wert **FALSE** empfangen.
2.  Standardmäßig verwendet der Indexer Vorwärtssuche. Rufen Sie bei umgekehrter Suche (d.h. suchen vom Ende der Datei) [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) auf, und legen Sie das **MFASF \_ INDEXER \_ READ FOR \_ \_ REVERSEPLAYBACK-Flag** fest. Überspringen Sie andernfalls diesen Schritt.
3.  Wenn der Stream indiziert ist, rufen Sie die Suchposition für eine angegebene Präsentationszeit ab, indem [**Sie IMFASFIndexer::GetSeekPositionForValue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue)aufrufen. Diese Methode liest den ASF-Index und sucht den Indexeintrag, der der angeforderten Zeit am nächsten liegt. Die -Methode gibt den Byteoffset des vom Indexeintrag angegebenen Datenpakets zurück. Der Byteoffset ist relativ zum Anfang des ASF-Datenobjekts.

Die [**GetSeekPositionForValue-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) verwendet einen Zeiger auf die [**ASF \_ INDEX \_ IDENTIFIER-Struktur.**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) Diese Struktur gibt einen Indextyp und einen Streambezeichner an. Derzeit muss der Indextyp GUID \_ NULL sein, der die zeitbasierte Indizierung angibt.

Der folgende Code ruft eine Suchposition ab, wenn ein Datenstrombezeichner und die Zielpräsentationszeit angegeben werden. Wenn der Aufruf erfolgreich ist, gibt er den Datenoffset im *parameterdataOffset* und die ungefähre tatsächliche Suchzeit in *phnsApproxSeekTime* zurück.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF Indexer](asf-index-object.md)
</dt> </dl>

 

 



