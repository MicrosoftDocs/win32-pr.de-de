---
title: So indizen Sie eine ASF-Datei
description: So indizen Sie eine ASF-Datei
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows Medienformat-SDK, Indizieren von ASF-Dateien
- Advanced Systems Format (ASF), Indizieren von Dateien
- ASF (Advanced Systems Format), Indizieren von Dateien
- Indizes,Indizieren von ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c2e41ed60ecb8fcee39da35dbc79ec44cece8db62f3e040d42aee3374c5690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845578"
---
# <a name="to-index-an-asf-file"></a>So indizen Sie eine ASF-Datei

Der Prozess der Indizierung einer ASF-Datei ist sehr einfach. Rufen Sie [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) auf, und übergeben Sie den Dateinamen. Der Indexer führt den Rest aus. Der Aufruf von **StartIndexing** ist asynchron, sodass der Status mithilfe des **OnStatus-Rückrufs** überwacht werden muss.

Der folgende Code zeigt, wie eine ASF-Datei indiziert wird. Wenn Sie den Indexer vor dem Indizieren der Datei konfigurieren möchten, müssen Sie Code aus dem Beispiel in [So konfigurieren Sie den Indexer](to-configure-the-indexer.md)einschließen.

In diesem Beispiel muss das Handle, das auf das Ereignis verweist, als globale Variable erstellt werden, damit der Rückruf darauf zugreifen kann. Die folgende Deklaration sollte in einem globalen Bereich angezeigt werden.


```C++
HANDLE g_hEvent = NULL;

```



In einem realistischeren Szenario sollte das Ereignishandle ein Datenmember der -Klasse sein, die sowohl den Rückruf als auch die Logik zum Starten des Indexers enthält.

Der Indexer sendet nach dem Aufruf von **IWMIndexer::StartIndexing** mehrere Ereignisse an den **OnStatus-Rückruf.** Sie können sie nach Bedarf für Ihre Anwendung abfangen. Mindestens müssen Sie WMT \_ CLOSED abfangen, das gesendet wird, wenn die Indizierung abgeschlossen ist. Verwenden Sie die folgende Logik innerhalb des  Nachrichtenschalters in Ihrer Implementierung des OnStatus-Rückrufs.


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



In diesem Beispiel wird davon ausgegangen, dass auf Ihre Implementierung des **OnStatus-Rückrufs** über ein Objekt namens MyCallback zugegriffen wird. Weitere Informationen zur Verwendung von Ereignissen und Rückrufen mit diesem SDK finden Sie unter [Verwenden der Rückrufmethoden.](using-the-callback-methods.md)


```C++
IWMIndexer* pMyIndexer     = NULL;
HRESULT     hr             = S_OK;
WCHAR       pwszFileName[] = L"C:\SomeFile.wmv";

// Initialize COM.
hr = CoInitialize(NULL);

// Create an event for asynchronous calls.
g_hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

// Create an indexer.
hr = WMCreateIndexer(&pMyIndexer);

// TODO: Configure the indexer if needed. See To Configure the Indexer.

// Start the indexer.
hr = pMyIndexer->StartIndexing(pwszFileName, &MyCallback, NULL);

// Wait for the indexer to finish.
WaitForSingleObject(g_hEvent, INFINITE);

// Clean up.
pMyIndexer->Release();
pMyIndexer = NULL

CloseHandle(g_hEvent);
g_hEvent = NULL;

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMIndexer-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**So konfigurieren Sie den Indexer**](to-configure-the-indexer.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




