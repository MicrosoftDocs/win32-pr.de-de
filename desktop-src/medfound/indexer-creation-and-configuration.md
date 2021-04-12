---
description: Dieses Thema enthält Informationen zum Erstellen des Standardindexer-Objekts, das von Media Foundation bereitgestellt wird.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Erstellung und Konfiguration von Indexern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e97bb558866fda021245b1597ead2a073c659c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217035"
---
# <a name="indexer-creation-and-configuration"></a>Erstellung und Konfiguration von Indexern

Der ASF- *Indexer* ist eine wmcontainer-Ebenenkomponente, die verwendet wird, um Index Objekte in einer ASF-Datei (Advanced Systems Format) zu lesen oder zu schreiben. Dieses Thema enthält Informationen zum Erstellen des Standardindexer-Objekts, das von Media Foundation bereitgestellt wird.

Weitere Informationen zur Struktur einer ASF-Datei finden Sie unter [Struktur der ASF-Datei](asf-file-structure.md).

**So erstellen und initialisieren Sie den ASF-Indexer**

1.  Ruft die [**mfkreateasfindexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) -Funktion auf, um einen [**imfasfindexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) -Zeiger auf das Indexer-Objekt zu empfangen.
2.  Aufrufen von [**imfasfindexer:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) zum Angeben des Lese-oder Schreibmodus für das Indexer-Objekt. Standardmäßig ist der Indexer für die vorwärts Suche konfiguriert.

    

    | Zweck                       | Flag                                           |
    |---------------------------|------------------------------------------------|
    | Lesen (vorwärts Suche) | NULL (Standard)                                 |
    | Lesen (Reverse-Suche) | **mfasf- \_ Indexer- \_ Lesevorgang \_ für \_ reverleplayback** |
    | Schreiben                   | mfasf- \_ Indexer \_ schreiben \_ neuer \_ Index              |

    

     

    > [!Note]  
    > Die gleiche Instanz des Indexers kann nicht sowohl für Lese-als auch für Schreibvorgänge verwendet werden. Sie müssen den Indexer für einen oder den anderen konfigurieren.

     

3.  Zum Initialisieren des [**Indexers wird imfasfindexer:: Initialisieren**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) aufgerufen, indem der [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Zeiger des ContentInfo-Objekts angegeben wird, das die zu schreibenden oder zu lesende Datei beschreibt. Das ContentInfo-Objekt enthält Informationen, die das [ASF-Header Objekt](asf-file-structure.md)bilden. Das Indexer-Objekt benötigt ein gültiges ContentInfo-Objekt, bevor Indexeinträge einer ASF-Datei erzeugt oder gelesen werden.

Im folgenden Codebeispiel wird gezeigt, wie eine Anwendung das Indexer-Objekt erstellen und initialisieren kann, um mit einem bestimmten ASF-Inhalt zu arbeiten. Das ContentInfo-Objekt stellt das ASF-Header Objekt dar. der Inhalt wird als Bytestream übermittelt.


```C++
HRESULT CreateASFIndexer(
    IMFASFContentInfo* pContentInfo, 
    DWORD dwFlags,
    IMFASFIndexer** ppIndexer
    )
{
    *ppIndexer = NULL;

    IMFASFIndexer *pIndexer = NULL;

    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pIndexer->SetFlags(dwFlags);
    if (FAILED(hr))
    {
        goto done;
    }

    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the object to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    // Clean up.
    SafeRelease(&pIndexer);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Indexer](asf-index-object.md)
</dt> <dt>

[Verwenden des Indexers zum Suchen in einer ASF-Datei](using-the-indexer-to-seek.md)
</dt> <dt>

[Verwenden des Indexers zum Schreiben eines neuen Indexes](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



