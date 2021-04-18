---
title: So indizieren Sie eine ASF-Datei
description: So indizieren Sie eine ASF-Datei
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows Media Format SDK, Indizieren von ASF-Dateien
- Advanced Systems Format (ASF), Indizieren von Dateien
- ASF (Advanced Systems Format), Indizieren von Dateien
- Indizes, Indizieren von ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7206e1856abb9705e18e885ba06cb8253a93c84b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106339041"
---
# <a name="to-index-an-asf-file"></a>So indizieren Sie eine ASF-Datei

Der Prozess der Indizierung einer ASF-Datei ist sehr einfach. Führen Sie einen Aufruf an [**iwmindexer:: startindizierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) aus, und übergeben Sie den Dateinamen. Der Indexer übernimmt den Rest. Der **startIndex** -Aufrufs ist asynchron, sodass der Status mithilfe des **OnStatus** -Rückrufs überwacht werden muss.

Der folgende Code zeigt, wie eine ASF-Datei indiziert wird. Wenn Sie den Indexer vor der Indizierung der Datei konfigurieren möchten, müssen Sie Code aus dem Beispiel in einbeziehen, [um den Indexer zu konfigurieren](to-configure-the-indexer.md).

In diesem Beispiel muss das Handle, das auf das Ereignis verweist, als globale Variable erstellt werden, damit der Rückruf darauf zugreifen kann. Die folgende Deklaration sollte in einem globalen Gültigkeitsbereich angezeigt werden.


```C++
HANDLE g_hEvent = NULL;

```



In einem realistischeren Szenario sollte das Ereignis Handle ein Datenmember der Klasse sein, die sowohl den Rückruf als auch die Logik zum Starten des Indexers enthält.

Der Indexer sendet nach dem Aufruf von **iwmindexer:: startindizierung** mehrere Ereignisse an den **OnStatus** -Rückruf. Sie können Sie nach Bedarf für Ihre Anwendung abfangen. Sie müssen mindestens WMT \_ Closed beenden, das gesendet wird, wenn die Indizierung abgeschlossen ist. Verwenden Sie die folgende Logik innerhalb des Nachrichten Schalters in der Implementierung des **OnStatus** -Rückrufs.


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



Bei diesem Beispiel wird davon ausgegangen, dass auf Ihre Implementierung des **OnStatus** -Rückrufs über ein Objekt mit dem Namen "MyCallback" zugegriffen wird. Weitere Informationen zum Verwenden von Ereignissen und Rückrufen mit diesem SDK finden Sie unter [Verwenden der Rückruf Methoden](using-the-callback-methods.md).


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

[**Iwmindexer-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**So konfigurieren Sie den Indexer**](to-configure-the-indexer.md)
</dt> <dt>

[**Wmkreateingedexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




