---
title: Verwenden von benutzerdefinierten senken
description: Verwenden von benutzerdefinierten senken
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- Advanced Systems Format (ASF), benutzerdefinierte senken
- ASF (Advanced Systems Format), Custom Sinks
- Advanced Systems Format (ASF), senken
- ASF (Advanced Systems Format), senken
- senken, benutzerdefinierte senken
- benutzerdefinierte senken, Informationen zu
- Writer-senken, benutzerdefinierte senken
- benutzerdefinierte senken, iwmschreitersink-Schnittstelle
- Iwmschreibsink
- Writer-senken, iwmschreitersink-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723480"
---
# <a name="using-custom-sinks"></a><span data-ttu-id="55cc0-113">Verwenden von benutzerdefinierten senken</span><span class="sxs-lookup"><span data-stu-id="55cc0-113">Using Custom Sinks</span></span>

<span data-ttu-id="55cc0-114">Wenn Sie einen speziellen Schreib Bedarf haben, können Sie eigene Writer-senken erstellen.</span><span class="sxs-lookup"><span data-stu-id="55cc0-114">If you have a special writing need, you can create your own writer sinks.</span></span> <span data-ttu-id="55cc0-115">Der Writer verwaltet die unidirektionale Kommunikation mit einer Senke, indem er die Methoden von [**iwmschreitersink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)aufruft.</span><span class="sxs-lookup"><span data-stu-id="55cc0-115">The writer maintains one-way communication with a sink by making calls to the methods of [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink).</span></span> <span data-ttu-id="55cc0-116">Um eine eigene Senke zu erstellen, implementieren Sie die **iwmschreitersink** -Schnittstelle in einer Klasse in Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="55cc0-116">To create your own sink, implement the **IWMWriterSink** interface in a class in your application.</span></span> <span data-ttu-id="55cc0-117">Dieser Prozess ähnelt dem Implementieren anderer Rückruf Schnittstellen, die von den Objekten des Windows Media Format SDK verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55cc0-117">This process is very similar to implementing any other callback interface used by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="55cc0-118">Weitere Informationen über Rückrufe finden Sie unter [Verwenden der Rückruf Methoden](using-the-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="55cc0-118">For more information about callbacks, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>

<span data-ttu-id="55cc0-119">Der in [**iwmwrite:: onheader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) empfangene Puffer sollte an den Anfang der Datei geschrieben werden, und alle in [**ondataunit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) empfangenen Puffer sollten sequenziell ausgeschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="55cc0-119">The buffer received in [**IWMWriterSink::OnHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) should be written to the beginning of the file, and all buffers received in [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) should be written out sequentially.</span></span> <span data-ttu-id="55cc0-120">**Onheader** wird zu Beginn aufgerufen, kann aber auch zu anderen Zeiten aufgerufen werden. wenn dies der Fall ist, sollten Sie, wenn möglich, den ursprünglichen Header überschreiben.</span><span class="sxs-lookup"><span data-stu-id="55cc0-120">**OnHeader** will be called at the beginning but might be called at other times, too, and if it is, you should, if possible, overwrite the original header.</span></span> <span data-ttu-id="55cc0-121">Wenn die Anwendung aus irgendeinem Grund nicht in der Lage ist, sollten Sie die nachfolgenden **onheader** -Aufrufe einfach ignorieren.</span><span class="sxs-lookup"><span data-stu-id="55cc0-121">If your application is not able to do this for some reason, then simply ignore the subsequent **OnHeader** calls.</span></span>

<span data-ttu-id="55cc0-122">Die benutzerdefinierte Senke sollte ihren Status an Ihre Schreib Anwendung übermitteln, indem Sie Aufrufe an die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode sendet.</span><span class="sxs-lookup"><span data-stu-id="55cc0-122">Your custom sink should communicate its status to your writing application by making calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="55cc0-123">Wenn Sie die Senke als COM-Objekt implementieren, möchten Sie möglicherweise die [**iwmregistercallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="55cc0-123">If you implement your sink as a COM object, you may want to expose the [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) interface.</span></span> <span data-ttu-id="55cc0-124">Sie können jedoch die Adresse des **OnStatus** -Rückrufs an die Senke übergeben und in beliebiger Weise einen Kontext festlegen.</span><span class="sxs-lookup"><span data-stu-id="55cc0-124">However, you can pass the address of the **OnStatus** callback to your sink and set a context in any way you like.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55cc0-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55cc0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55cc0-126">**Arbeiten mit Writer-senken**</span><span class="sxs-lookup"><span data-stu-id="55cc0-126">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




