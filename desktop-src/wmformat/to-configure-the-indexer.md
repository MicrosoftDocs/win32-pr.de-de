---
title: So konfigurieren Sie den Indexer
description: So konfigurieren Sie den Indexer
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- Windows Medienformat-SDK, Konfigurieren von Indexern
- Advanced Systems Format (ASF), Konfigurieren von Indexern
- ASF (Advanced Systems Format), Konfigurieren von Indexern
- Indizes,Konfigurieren von Indexern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5a624a4ed9ae749559a1908e3809500bf8aece2b29b8ad406769c5f639e547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845625"
---
# <a name="to-configure-the-indexer"></a>So konfigurieren Sie den Indexer

Sie können den Indexer konfigurieren, bevor Sie ihn zum Indizieren einer ASF-Datei verwenden. Jeder Stream in der Datei kann separat konfiguriert werden, oder Sie können die gleiche Konfiguration für alle Streams festlegen.

Wenn Sie mehrere Dämpfe für die Indizierung in einer Datei konfigurieren, müssen Sie sie alle konfigurieren und dann mit der Indizierung beginnen. Wenn Sie einen Stream konfigurieren und indizieren und dann einen anderen Stream in derselben Datei konfigurieren, wird beim erneuten Starten des Indexers der erste Index gelöscht. Dies soll dem ASF-Dateiformat entsprechen.

Der folgende Code zeigt, wie der Indexer konfiguriert wird. Der Code geht davon aus, dass die zu indizierende Datei über zwei Streams verfügt: der erste ist ein Audiostream, der nicht indiziert werden muss, und der zweite ist ein Videostream. Dieser Code zeigt nur, wie der Indexer konfiguriert wird. Um eine Datei zu indizieren, müssen Sie die Schritte unter So indizieren Sie [eine ASF-Datei ausführen.](to-index-an-asf-file.md)


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
> Der Standardindextyp ist WMT \_ IT \_ NEAREST CLEAN \_ \_ POINT. Obwohl Sie den Indextyp auf andere Werte festlegen können, beeinträchtigt dies die Suchleistung.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMIndexer2::Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[**So indizieren Sie eine ASF-Datei**](to-index-an-asf-file.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




