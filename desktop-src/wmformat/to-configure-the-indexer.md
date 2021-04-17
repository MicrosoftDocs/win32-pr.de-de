---
title: So konfigurieren Sie den Indexer
description: So konfigurieren Sie den Indexer
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- Windows Media-Format-SDK, Konfigurieren von Indexer
- Advanced Systems Format (ASF), Konfigurieren von indexatoren
- ASF (Advanced Systems Format), Konfigurieren von indexatoren
- Indizes, Konfigurieren von Indexer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618316e22b13ca05ff0fc1bbfb6b4583e79ca858
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389902"
---
# <a name="to-configure-the-indexer"></a>So konfigurieren Sie den Indexer

Sie können den Indexer konfigurieren, bevor Sie ihn zum Indizieren einer ASF-Datei verwenden. Jeder Stream in der Datei kann separat konfiguriert werden, oder Sie können die gleiche Konfiguration für alle Streams festlegen.

Wenn Sie mehrere Textstreams für die Indizierung in einer Datei konfigurieren, müssen Sie alle konfigurieren und dann die Indizierung starten. Wenn Sie einen Stream konfigurieren und indizieren und dann einen anderen Stream in derselben Datei konfigurieren, wird der erste Index durch das erneute Starten des Indexers gelöscht. Dies entspricht dem Format der ASF-Datei.

Der folgende Code zeigt, wie der Indexer konfiguriert wird. Der Code geht davon aus, dass die zu indizierende Datei zwei Streams hat: der erste ist ein Audiostream, der nicht indiziert werden muss, und der zweite ist ein Videostream. Dieser Code zeigt nur, wie der Indexer konfiguriert wird. Um eine Datei zu indizieren, müssen Sie die unter beschriebenen Schritte ausführen, [um eine ASF-Datei zu indizieren](to-index-an-asf-file.md).


```C++
IWMIndexer*  pBaseIndexer = NULL;
IWMIndexer2* pMyIndexer   = NULL;

DWORD          dwInterval;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create an indexer.
hr = WMCreateIndexer(&pBaseIndexer);

// Retrieve an IWMIndexer2 interface pointer for the indexer just created.
hr = pBaseIndexer->QueryInterface(IID_IWMIndexer2, (void**)&pMyIndexer);

// Release the base indexer.
pBaseIndexer->Release();
pBaseIndexer = NULL;

// Set the index interval to 5 frames.
dwInterval = 5;

// Configure the indexer to create a frame-based index.
hr = pMyIndexer->Configure(2,                    // Stream Number.
                           WMT_IT_FRAME_NUMBERS, // Indexer type.
                           (void *)&dwInterval,  // Index interval.
                           NULL;        // Index type, use default.

// TODO: Index the file. See To Index an ASF File.

// Release the remaining interface.
pMyIndexer->Release();
pMyIndexer = NULL;

```



> [!Note]  
> Der Standard Indextyp ist der \_ \_ nächste \_ Clean \_ Point (WMT). Obwohl der Indextyp auf andere Werte festgelegt werden kann, wird die Suche nach Leistung beeinträchtigt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMIndexer2:: Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[**So indizieren Sie eine ASF-Datei**](to-index-an-asf-file.md)
</dt> <dt>

[**Wmkreateingedexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




