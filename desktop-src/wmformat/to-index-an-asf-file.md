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
# <a name="to-index-an-asf-file"></a><span data-ttu-id="78ea9-107">So indizieren Sie eine ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="78ea9-107">To Index an ASF File</span></span>

<span data-ttu-id="78ea9-108">Der Prozess der Indizierung einer ASF-Datei ist sehr einfach.</span><span class="sxs-lookup"><span data-stu-id="78ea9-108">The process of indexing an ASF file is very simple.</span></span> <span data-ttu-id="78ea9-109">Führen Sie einen Aufruf an [**iwmindexer:: startindizierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) aus, und übergeben Sie den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="78ea9-109">Make a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) and pass the file name.</span></span> <span data-ttu-id="78ea9-110">Der Indexer übernimmt den Rest.</span><span class="sxs-lookup"><span data-stu-id="78ea9-110">The indexer does the rest.</span></span> <span data-ttu-id="78ea9-111">Der **startIndex** -Aufrufs ist asynchron, sodass der Status mithilfe des **OnStatus** -Rückrufs überwacht werden muss.</span><span class="sxs-lookup"><span data-stu-id="78ea9-111">The call to **StartIndexing** is asynchronous, so status must be monitored using the **OnStatus** callback.</span></span>

<span data-ttu-id="78ea9-112">Der folgende Code zeigt, wie eine ASF-Datei indiziert wird.</span><span class="sxs-lookup"><span data-stu-id="78ea9-112">The following code shows how to index an ASF file.</span></span> <span data-ttu-id="78ea9-113">Wenn Sie den Indexer vor der Indizierung der Datei konfigurieren möchten, müssen Sie Code aus dem Beispiel in einbeziehen, [um den Indexer zu konfigurieren](to-configure-the-indexer.md).</span><span class="sxs-lookup"><span data-stu-id="78ea9-113">If you want to configure the indexer prior to indexing the file, you will need to include code from the example included in [To Configure the Indexer](to-configure-the-indexer.md).</span></span>

<span data-ttu-id="78ea9-114">In diesem Beispiel muss das Handle, das auf das Ereignis verweist, als globale Variable erstellt werden, damit der Rückruf darauf zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="78ea9-114">For this example, the handle that points to the event must be created as a global variable so it will be accessible by the callback.</span></span> <span data-ttu-id="78ea9-115">Die folgende Deklaration sollte in einem globalen Gültigkeitsbereich angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="78ea9-115">The following declaration should appear in a global scope.</span></span>


```C++
HANDLE g_hEvent = NULL;

```



<span data-ttu-id="78ea9-116">In einem realistischeren Szenario sollte das Ereignis Handle ein Datenmember der Klasse sein, die sowohl den Rückruf als auch die Logik zum Starten des Indexers enthält.</span><span class="sxs-lookup"><span data-stu-id="78ea9-116">In a more realistic scenario, the event handle should be a data member of the class that contains both the callback and the logic for starting the indexer.</span></span>

<span data-ttu-id="78ea9-117">Der Indexer sendet nach dem Aufruf von **iwmindexer:: startindizierung** mehrere Ereignisse an den **OnStatus** -Rückruf.</span><span class="sxs-lookup"><span data-stu-id="78ea9-117">The indexer sends several events to the **OnStatus** callback after the call to **IWMIndexer::StartIndexing**.</span></span> <span data-ttu-id="78ea9-118">Sie können Sie nach Bedarf für Ihre Anwendung abfangen.</span><span class="sxs-lookup"><span data-stu-id="78ea9-118">You can trap them as needed for your application.</span></span> <span data-ttu-id="78ea9-119">Sie müssen mindestens WMT \_ Closed beenden, das gesendet wird, wenn die Indizierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="78ea9-119">At a minimum, you need to trap WMT\_CLOSED, which is sent when indexing is complete.</span></span> <span data-ttu-id="78ea9-120">Verwenden Sie die folgende Logik innerhalb des Nachrichten Schalters in der Implementierung des **OnStatus** -Rückrufs.</span><span class="sxs-lookup"><span data-stu-id="78ea9-120">Use the following logic within the message switch in your implementation of the **OnStatus** callback.</span></span>


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



<span data-ttu-id="78ea9-121">Bei diesem Beispiel wird davon ausgegangen, dass auf Ihre Implementierung des **OnStatus** -Rückrufs über ein Objekt mit dem Namen "MyCallback" zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="78ea9-121">For this example it is assumed that your implementation of the **OnStatus** callback is accessed through an object called MyCallback.</span></span> <span data-ttu-id="78ea9-122">Weitere Informationen zum Verwenden von Ereignissen und Rückrufen mit diesem SDK finden Sie unter [Verwenden der Rückruf Methoden](using-the-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="78ea9-122">For more information about using events and callbacks with this SDK, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="78ea9-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78ea9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78ea9-124">**Iwmindexer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="78ea9-124">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="78ea9-125">**So konfigurieren Sie den Indexer**</span><span class="sxs-lookup"><span data-stu-id="78ea9-125">**To Configure the Indexer**</span></span>](to-configure-the-indexer.md)
</dt> <dt>

[<span data-ttu-id="78ea9-126">**Wmkreateingedexer**</span><span class="sxs-lookup"><span data-stu-id="78ea9-126">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="78ea9-127">**Arbeiten mit Indizes**</span><span class="sxs-lookup"><span data-stu-id="78ea9-127">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




