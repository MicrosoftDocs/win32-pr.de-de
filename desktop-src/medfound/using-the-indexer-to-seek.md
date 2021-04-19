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
# <a name="using-the-indexer-to-seek-within-an-asf-file"></a>Verwenden des Indexers zum Suchen in einer ASF-Datei

Der ASF- *Indexer* ist eine wmcontainer-Ebenenkomponente, die verwendet wird, um Index Objekte in einer ASF-Datei (Advanced Systems Format) zu lesen oder zu schreiben. Dieses Thema enthält Informationen zur Verwendung des-ASF-Indexers, um in einer ASF-Datei zu suchen.

-   [Initialisieren des Indexers für die Suche](#initializing-the-indexer-for-seeking)
-   [Die Such Position wird erhalten.](#getting-the-seek-position)
-   [Zugehörige Themen](#related-topics)

Weitere Informationen zur Struktur einer ASF-Datei finden Sie unter [Struktur der ASF-Datei](asf-file-structure.md).

## <a name="initializing-the-indexer-for-seeking"></a>Initialisieren des Indexers für die Suche

So initialisieren Sie den ASF-Indexer für die Suche:

1.  Rufen Sie [**mfkreateasfindexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) auf, um eine neue Instanz des ASF-Indexers zu erstellen.
2.  Um den Indexer zu initialisieren, wird [**imfasfindexer:: Initialisieren**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) aufgerufen. Diese Methode ruft Informationen aus dem ASF-Header ab, um zu bestimmen, welche ASF-Streams indiziert werden. Standardmäßig ist das Indexer-Objekt für die Suche konfiguriert.
3.  Aufrufen von [**imfasfindexer:: getindexposition**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexposition) , um den Offset des Indexes innerhalb der ASF-Datei zu ermitteln.
4.  Rufen Sie die [**mfkreateasfindexerbytestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexerbytestream) -Funktion auf, um einen Bytestream zum Lesen des Indexes zu erstellen. Die Eingabe für diese Funktion ist ein Zeiger auf einen Bytestream, der die ASF-Datei enthält, und auf den Offset des Indexes (aus dem vorherigen Schritt).
5.  Aufrufen von [**imfasfindexer:: setindexbytestreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setindexbytestreams) zum Festlegen des Index Byte-Streams für den Indexer.

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



## <a name="getting-the-seek-position"></a>Die Such Position wird erhalten.

1.  Um herauszufinden, ob ein bestimmter Stream indiziert ist, müssen Sie [**imfasfindexer:: getindexstatus**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getindexstatus)aufrufen. Wenn der Stream indiziert ist, erhält der *pfisindexed* -Parameter den Wert " **true**". Andernfalls wird der Wert **false** empfangen.
2.  Standardmäßig verwendet der Indexer Forward-Suche. Für Reverse-Suche (d. h. Durchsuchen am Ende der Datei), wird [**imfasfindexer:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) aufgerufen und der **mfasf- \_ Indexer-Lesevorgang für das \_ \_ \_ reverseplayback** -Flag festgelegt. Überspringen Sie andernfalls diesen Schritt.
3.  Wenn der Stream indiziert ist, rufen Sie die Suchposition für eine bestimmte Präsentationszeit durch Aufrufen von [**imfasfindexer:: getseekpositionforvalue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue)ab. Diese Methode liest den ASF-Index und findet den Index Eintrag, der der angeforderten Zeit am nächsten liegt. Die-Methode gibt den Byte Offset des Datenpakets zurück, das durch den Index Eintrag angegeben wird. Der Byte Offset ist relativ zum Anfang des ASF-Datenobjekts.

Die [**getseekpositionforvalue**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-getseekpositionforvalue) -Methode nimmt einen Zeiger auf die Struktur des [**ASF- \_ Index \_ Bezeichners**](/windows/desktop/api/wmcontainer/ns-wmcontainer-asf_index_identifier) an. Diese Struktur gibt einen Indextyp und einen Datenstrom Bezeichner an. Derzeit muss der Indextyp "GUID \_ null" sein, der die zeitbasierte Indizierung angibt.

Der folgende Code Ruft eine Suchposition ab, wenn ein Datenstrom Bezeichner und eine Ziel Präsentationszeit angegeben werden. Wenn der Aufruf erfolgreich ist, wird der Daten Offset im *pcbdataoffset* -Parameter und die ungefähre tatsächliche Suchzeit in *phnsapproxseektime* zurückgegeben.


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

[ASF-Indexer](asf-index-object.md)
</dt> </dl>

 

 



