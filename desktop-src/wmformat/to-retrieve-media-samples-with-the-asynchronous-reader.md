---
title: So rufen Sie Medien Beispiele mit dem asynchronen Reader ab
description: So rufen Sie Medien Beispiele mit dem asynchronen Reader ab
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- Advanced Systems Format (ASF), Abrufen von Medien Beispielen
- ASF (Advanced Systems Format), Abrufen von Medien Beispielen
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- asynchrone Leser, Abrufen von Medien Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0419619ea99bd3734db67f8e658b1f3ff058a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038541"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a><span data-ttu-id="3373b-108">So rufen Sie Medien Beispiele mit dem asynchronen Reader ab</span><span class="sxs-lookup"><span data-stu-id="3373b-108">To Retrieve Media Samples with the Asynchronous Reader</span></span>

<span data-ttu-id="3373b-109">Nachdem Sie die WMT- \_ Statusmeldung "geöffnet" in ihrer Implementierung von " [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)" erhalten haben, können Sie mit dem Empfang von Beispielen beginnen, indem Sie [**iwmreader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3373b-109">After you have received the WMT\_OPENED status message in your implementation of [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus), you can begin receiving samples by calling [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start).</span></span> <span data-ttu-id="3373b-110">Der asynchrone Reader stellt Beispiele für Ihre Implementierung von [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample)bereit.</span><span class="sxs-lookup"><span data-stu-id="3373b-110">The asynchronous reader delivers samples to your implementation of [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span></span> <span data-ttu-id="3373b-111">Beispiele werden in der Präsentationszeit bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3373b-111">Samples are delivered in presentation-time order.</span></span>

<span data-ttu-id="3373b-112">**Start** ist ein asynchroner-Befehl.</span><span class="sxs-lookup"><span data-stu-id="3373b-112">**Start** is an asynchronous call.</span></span> <span data-ttu-id="3373b-113">Es wird fast sofort zurückgegeben und weiterhin in separaten Threads ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3373b-113">It will return almost immediately and continue to run on separate threads.</span></span> <span data-ttu-id="3373b-114">Der asynchrone Reader verwendet beim Decodieren von Inhalten und Bereitstellung von Beispielen mehrere Threads.</span><span class="sxs-lookup"><span data-stu-id="3373b-114">The asynchronous reader uses multiple threads when decoding content and delivering samples.</span></span> <span data-ttu-id="3373b-115">Wenn das Ende der Datei erreicht ist, sendet der Reader eine WMT \_ EOF-Statusmeldung an die Implementierung des **OnStatus** -Rückrufs.</span><span class="sxs-lookup"><span data-stu-id="3373b-115">When the end of the file is reached, the reader sends a WMT\_EOF status message to your implementation of the **OnStatus** callback.</span></span> <span data-ttu-id="3373b-116">Wenn WMT \_ EOF gesendet wird, beendet der Reader seine eigene Verarbeitung. Sie müssen nicht auf WMT \_ EOF mit einem [**callmreader:: Stopp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop)-Befehl reagieren.</span><span class="sxs-lookup"><span data-stu-id="3373b-116">When WMT\_EOF is sent, the reader stops its own processing; you do not need to respond to WMT\_EOF with a call to [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3373b-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3373b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3373b-118">**Iwmreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3373b-118">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="3373b-119">**So implementieren Sie readernachrichten im OnStatus-Rückruf**</span><span class="sxs-lookup"><span data-stu-id="3373b-119">**To Implement Reader Messages in the OnStatus Callback**</span></span>](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[<span data-ttu-id="3373b-120">**So implementieren Sie den onsample-Rückruf**</span><span class="sxs-lookup"><span data-stu-id="3373b-120">**To Implement the OnSample Callback**</span></span>](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 




