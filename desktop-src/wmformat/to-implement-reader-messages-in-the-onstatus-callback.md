---
title: So implementieren Sie readernachrichten im OnStatus-Rückruf
description: So implementieren Sie readernachrichten im OnStatus-Rückruf
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- Advanced Systems Format (ASF), Implementieren von Reader-Nachrichten
- ASF (Advanced Systems Format), Implementieren von Reader-Nachrichten
- Advanced Systems Format (ASF), OnStatus-Rückruf
- ASF (Advanced Systems Format), OnStatus-Rückruf
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- asynchrone Leser, Implementieren von Reader-Nachrichten
- OnStatus-Rückruf Methode, Implementieren von Reader-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384cf8df8628efa9bd2cc17920dc6b1303655691
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038544"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a><span data-ttu-id="719b1-111">So implementieren Sie readernachrichten im OnStatus-Rückruf</span><span class="sxs-lookup"><span data-stu-id="719b1-111">To Implement Reader Messages in the OnStatus Callback</span></span>

<span data-ttu-id="719b1-112">Um den asynchronen Reader zum Übermitteln von Inhalten aus einer ASF-Datei zu verwenden, müssen Sie mindestens zwei Rückruf Methoden ( [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) und [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample)) implementieren.</span><span class="sxs-lookup"><span data-stu-id="719b1-112">To use the asynchronous reader to deliver content from an ASF file, you must implement a minimum of two callback methods, [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) and [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span></span> <span data-ttu-id="719b1-113">In diesem Abschnitt wird beschrieben, wie Sie **iwmstatuscallback:: OnStatus** implementieren, um vom Reader gesendete Statusmeldungen zu empfangen und darauf zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="719b1-113">This section describes how to implement **IWMStatusCallback::OnStatus** to receive and respond to status messages sent by the reader.</span></span> <span data-ttu-id="719b1-114">**OnStatus** wird von anderen Objekten im Windows Media-Format-SDK verwendet.</span><span class="sxs-lookup"><span data-stu-id="719b1-114">**OnStatus** is used by other objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="719b1-115">Allgemeine Informationen zu **OnStatus** finden Sie unter [Verwenden des OnStatus-Rückrufs](using-the-onstatus-callback.md).</span><span class="sxs-lookup"><span data-stu-id="719b1-115">For general information about **OnStatus**, see [Using the OnStatus Callback](using-the-onstatus-callback.md).</span></span>

<span data-ttu-id="719b1-116">Wenn Sie den asynchronen Reader verwenden, müssen Sie die folgenden Meldungen in **iwmstatuscallback:: OnStatus** abfangen.</span><span class="sxs-lookup"><span data-stu-id="719b1-116">When using the asynchronous reader, you must trap the following messages in **IWMStatusCallback::OnStatus**.</span></span>



| <span data-ttu-id="719b1-117">Statusmeldung</span><span class="sxs-lookup"><span data-stu-id="719b1-117">Status message</span></span> | <span data-ttu-id="719b1-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="719b1-118">Description</span></span>                                     |
|----------------|-------------------------------------------------|
| <span data-ttu-id="719b1-119">WMT \_ geöffnet</span><span class="sxs-lookup"><span data-stu-id="719b1-119">WMT\_OPENED</span></span>    | <span data-ttu-id="719b1-120">Wird gesendet, wenn Datei öffnende Vorgänge beendet sind.</span><span class="sxs-lookup"><span data-stu-id="719b1-120">Sent when file opening operations are complete.</span></span> |
| <span data-ttu-id="719b1-121">WMT \_ geschlossen</span><span class="sxs-lookup"><span data-stu-id="719b1-121">WMT\_CLOSED</span></span>    | <span data-ttu-id="719b1-122">Wird gesendet, wenn Datei schließende Vorgänge abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="719b1-122">Sent when file closing operations are complete.</span></span> |



 

<span data-ttu-id="719b1-123">Verwenden Sie die oben aufgeführten Statusmeldungen, um die Ausführung der Leseanwendung zu steuern.</span><span class="sxs-lookup"><span data-stu-id="719b1-123">You should use the status messages listed above to control execution of your reading application.</span></span> <span data-ttu-id="719b1-124">Beispielsweise müssen Sie warten, bis die **\_ geöffnete WMT** -Nachricht empfangen wird, um den Reader zu starten oder andere Methoden aufzurufen, die erfordern, dass der Reader eine Datei bereit hat.</span><span class="sxs-lookup"><span data-stu-id="719b1-124">For example, you must wait until receiving the **WMT\_OPENED** message to start the reader or call other methods that require the reader to have a file ready.</span></span> <span data-ttu-id="719b1-125">Häufig verwenden Anwendungen, die mit dem asynchronen Reader erstellt wurden, ein Ereignis, um den Abschluss von asynchronen Aufrufen zu signalisieren und die Verarbeitung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="719b1-125">Frequently, applications built with the asynchronous reader use an event to signal the completion of asynchronous calls and proceed with processing.</span></span> <span data-ttu-id="719b1-126">Weitere Informationen zur Verwendung von Ereignissen, um den Abschluss von Vorgängen zu signalisieren, finden Sie unter [Verwenden von Ereignissen mit asynchronen Aufrufen](using-events-with-asynchronous-calls.md).</span><span class="sxs-lookup"><span data-stu-id="719b1-126">For more information about using events for signaling completion of operations, see [Using Events with Asynchronous Calls](using-events-with-asynchronous-calls.md).</span></span>

<span data-ttu-id="719b1-127">Viele andere Nachrichten werden vom Reader-Objekt an **OnStatus** gesendet, damit die Anwendung auf den Status von Lesevorgängen reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="719b1-127">Many other messages are sent to **OnStatus** by the reader object to enable the application to respond to the status of reading operations.</span></span> <span data-ttu-id="719b1-128">Die möglichen Status Meldungs Werte werden im Enumerationstyp " [**WMT- \_ Status**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) " definiert.</span><span class="sxs-lookup"><span data-stu-id="719b1-128">The possible status message values are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="719b1-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="719b1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="719b1-130">**Iwmstatuscallback:: OnStatus**</span><span class="sxs-lookup"><span data-stu-id="719b1-130">**IWMStatusCallback::OnStatus**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[<span data-ttu-id="719b1-131">**Lesen von Dateien mit dem asynchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="719b1-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="719b1-132">**Verwenden des OnStatus-Rückrufs**</span><span class="sxs-lookup"><span data-stu-id="719b1-132">**Using the OnStatus Callback**</span></span>](using-the-onstatus-callback.md)
</dt> </dl>

 

 




