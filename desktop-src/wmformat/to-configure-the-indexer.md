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
# <a name="to-configure-the-indexer"></a><span data-ttu-id="0e151-107">So konfigurieren Sie den Indexer</span><span class="sxs-lookup"><span data-stu-id="0e151-107">To Configure the Indexer</span></span>

<span data-ttu-id="0e151-108">Sie können den Indexer konfigurieren, bevor Sie ihn zum Indizieren einer ASF-Datei verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e151-108">You can configure the indexer before using it to index an ASF file.</span></span> <span data-ttu-id="0e151-109">Jeder Stream in der Datei kann separat konfiguriert werden, oder Sie können die gleiche Konfiguration für alle Streams festlegen.</span><span class="sxs-lookup"><span data-stu-id="0e151-109">Each stream in the file can be configured separately, or you can set the same configuration for all streams.</span></span>

<span data-ttu-id="0e151-110">Wenn Sie mehrere Textstreams für die Indizierung in einer Datei konfigurieren, müssen Sie alle konfigurieren und dann die Indizierung starten.</span><span class="sxs-lookup"><span data-stu-id="0e151-110">If you are configuring multiple steams for indexing in a file, you must configure them all and then begin indexing.</span></span> <span data-ttu-id="0e151-111">Wenn Sie einen Stream konfigurieren und indizieren und dann einen anderen Stream in derselben Datei konfigurieren, wird der erste Index durch das erneute Starten des Indexers gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0e151-111">If you configure and index a stream and then configure another stream in the same file, starting the indexer again will delete the first index.</span></span> <span data-ttu-id="0e151-112">Dies entspricht dem Format der ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="0e151-112">This is to comply with the ASF file format.</span></span>

<span data-ttu-id="0e151-113">Der folgende Code zeigt, wie der Indexer konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="0e151-113">The following code shows how to configure the indexer.</span></span> <span data-ttu-id="0e151-114">Der Code geht davon aus, dass die zu indizierende Datei zwei Streams hat: der erste ist ein Audiostream, der nicht indiziert werden muss, und der zweite ist ein Videostream.</span><span class="sxs-lookup"><span data-stu-id="0e151-114">The code assumes that the file to be indexed has two streams: the first is an audio stream which does not need to be indexed, and the second is a video stream.</span></span> <span data-ttu-id="0e151-115">Dieser Code zeigt nur, wie der Indexer konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="0e151-115">This code shows only how to configure the indexer.</span></span> <span data-ttu-id="0e151-116">Um eine Datei zu indizieren, müssen Sie die unter beschriebenen Schritte ausführen, [um eine ASF-Datei zu indizieren](to-index-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="0e151-116">To index a file, you must follow the steps presented in [To Index an ASF File](to-index-an-asf-file.md).</span></span>


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
> <span data-ttu-id="0e151-117">Der Standard Indextyp ist der \_ \_ nächste \_ Clean \_ Point (WMT).</span><span class="sxs-lookup"><span data-stu-id="0e151-117">The default index type is WMT\_IT\_NEAREST\_CLEAN\_POINT.</span></span> <span data-ttu-id="0e151-118">Obwohl der Indextyp auf andere Werte festgelegt werden kann, wird die Suche nach Leistung beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="0e151-118">Although you can set the index type to other values, doing so will degrade seeking performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0e151-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e151-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e151-120">**IWMIndexer2:: Configure**</span><span class="sxs-lookup"><span data-stu-id="0e151-120">**IWMIndexer2::Configure**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[<span data-ttu-id="0e151-121">**So indizieren Sie eine ASF-Datei**</span><span class="sxs-lookup"><span data-stu-id="0e151-121">**To Index an ASF File**</span></span>](to-index-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="0e151-122">**Wmkreateingedexer**</span><span class="sxs-lookup"><span data-stu-id="0e151-122">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="0e151-123">**Arbeiten mit Indizes**</span><span class="sxs-lookup"><span data-stu-id="0e151-123">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




