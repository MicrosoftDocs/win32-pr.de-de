---
description: Dieses Thema enthält Informationen zum Erstellen des standarden Indexerobjekts, das von Media Foundation.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Indexererstellung und -konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e0a341e3074ca44aa4403a3f2f518b4fb9082d4c6eadee1f4ca94a69e17bd98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061200"
---
# <a name="indexer-creation-and-configuration"></a>Indexererstellung und -konfiguration

Der *ASF-Indexer* ist eine WMContainer-Ebenenkomponente, die zum Lesen oder Schreiben von Indexobjekten in einer ASF-Datei (Advanced Systems Format) verwendet wird. Dieses Thema enthält Informationen zum Erstellen des standarden Indexerobjekts, das von Media Foundation.

Informationen zur Struktur einer ASF-Datei finden Sie unter [ASF-Dateistruktur.](asf-file-structure.md)

**So erstellen und initialisieren Sie den ASF-Indexer**

1.  Rufen Sie [**die MFCreateASFIndexer-Funktion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) auf, um einen [**IMFASFIndexer-Zeiger**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) auf das Indexerobjekt zu empfangen.
2.  Rufen [**Sie IMFASFIndexer::SetFlags auf,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) um den Lese- oder Schreibmodus für das Indexerobjekt anzugeben. Standardmäßig ist der Indexer für Vorwärtssuchen konfiguriert.

    

    | Zweck                       | Flag                                           |
    |---------------------------|------------------------------------------------|
    | Lesen (Vorwärtssuche) | 0 (Standard)                                 |
    | Lesen (Umgekehrtes Suchen) | **LESEN DES \_ MFASF-INDEXERS \_ \_ FÜR \_ REVERSEPLAYBACK** |
    | Schreiben                   | MFASF \_ INDEXER \_ WRITE \_ NEW \_ INDEX              |

    

     

    > [!Note]  
    > Dieselbe Instanz des Indexers kann nicht sowohl zum Lesen als auch zum Schreiben verwendet werden. Sie müssen den Indexer für das eine oder das andere konfigurieren.

     

3.  Rufen [**Sie IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) auf, um den Indexer zu initialisieren, indem Sie den [**IMFASFContentInfo-Zeiger**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) des ContentInfo-Objekts angeben, das die zu schreibende oder zu lesende Datei beschreibt. Das ContentInfo-Objekt enthält Informationen, die das [ASF-Headerobjekt bilden.](asf-file-structure.md) Das Indexerobjekt erfordert ein gültiges ContentInfo-Objekt, bevor Indexeinträge einer ASF-Datei generiert oder gelesen werden.

Das folgende Codebeispiel zeigt, wie eine Anwendung das Indexerobjekt erstellen und initialisieren kann, um mit bestimmten ASF-Inhalten zu arbeiten. Das ContentInfo-Objekt stellt das ASF-Headerobjekt dar. Der Inhalt wird als Bytestream übergeben.


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

[Verwenden des Indexers zum Suchen innerhalb einer ASF-Datei](using-the-indexer-to-seek.md)
</dt> <dt>

[Verwenden des Indexers zum Schreiben eines neuen Indexes](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



