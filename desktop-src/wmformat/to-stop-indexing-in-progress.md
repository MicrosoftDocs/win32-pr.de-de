---
title: So verhindern Sie die Ausführung der Indizierung
description: So verhindern Sie die Ausführung der Indizierung
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- Windows Media-Format-SDK, die Indizierung wird angehalten
- Advanced Systems Format (ASF), die Indizierung wird angehalten
- ASF (Advanced Systems Format), die Indizierung wird angehalten
- Indizes, die Indizierung wird angehalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea40cbf020182250e0fb982af5b5f84327d5d9a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038578"
---
# <a name="to-stop-indexing-in-progress"></a><span data-ttu-id="a57d3-107">So verhindern Sie die Ausführung der Indizierung</span><span class="sxs-lookup"><span data-stu-id="a57d3-107">To Stop Indexing in Progress</span></span>

<span data-ttu-id="a57d3-108">Nachdem Sie mit der Indizierung mit einem Aufruf von [**iwmindexer:: startindizierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing)begonnen haben, wird der Indexer normalerweise so lange fortgesetzt, bis die Datei indiziert ist.</span><span class="sxs-lookup"><span data-stu-id="a57d3-108">After you begin indexing with a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), the indexer will normally continue until the file is indexed.</span></span> <span data-ttu-id="a57d3-109">Sie können die Indizierungs Vorgänge beenden, indem Sie die [**iwmindexer:: Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a57d3-109">You can stop indexing operations by calling the [**IWMIndexer::Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) method.</span></span> <span data-ttu-id="a57d3-110">Nachdem Sie die Indizierung abgebrochen haben, können Sie **startIndex** erneut aufrufen, aber der Indexer beginnt am Anfang der Datei, anstatt von dem Zeitpunkt des Abbruchs fortgesetzt zu werden.</span><span class="sxs-lookup"><span data-stu-id="a57d3-110">After you have canceled indexing, you can call **StartIndexing** again, but the indexer will start from the beginning of the file rather than resuming from the point of cancellation.</span></span>

<span data-ttu-id="a57d3-111">Da **startindizierung** ein asynchroner Rückruf ist, müssen Sie in der Regel **Abbrechen** von einem anderen Thread oder Ereignishandler in der Anwendung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a57d3-111">Because **StartIndexing** is an asynchronous call, you will normally need to call **Cancel** from some other thread or event handler in your application.</span></span> <span data-ttu-id="a57d3-112">In der Regel wird **Abbrechen** von einer Ereignis Prozedur aufgerufen, die einem Schaltflächen-Steuerelement einer Windows-Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a57d3-112">Typically **Cancel** will be called from an event procedure associated with a button control of a Windows application.</span></span>

<span data-ttu-id="a57d3-113">Wenn die Indizierung abgebrochen wird, übergibt der Indexer eine Statusmeldung von WMT \_ geschlossen, so als ob die Datei ordnungsgemäß indiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="a57d3-113">When indexing is canceled, the indexer will pass a status message of WMT\_CLOSED, just as if the file had been indexed properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a57d3-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a57d3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a57d3-115">**Iwmindexer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a57d3-115">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="a57d3-116">**Arbeiten mit Indizes**</span><span class="sxs-lookup"><span data-stu-id="a57d3-116">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




