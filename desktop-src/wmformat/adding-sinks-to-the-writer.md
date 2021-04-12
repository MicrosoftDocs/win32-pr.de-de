---
title: Hinzufügen von senken zum Writer
description: Hinzufügen von senken zum Writer
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- Advanced Systems Format (ASF), Hinzufügen von senken zum Writer
- ASF (Advanced Systems Format), Hinzufügen von senken zum Writer
- Advanced Systems Format (ASF), senken
- ASF (Advanced Systems Format), senken
- Advanced Systems Format (ASF), Writer-senken
- ASF (Advanced Systems Format), Writer-senken
- senken, hinzufügen zum Writer
- Writer-senken, hinzufügen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886a6630a02d1fea56ce387077484f173ddf4dd3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389882"
---
# <a name="adding-sinks-to-the-writer"></a><span data-ttu-id="c4ef5-111">Hinzufügen von senken zum Writer</span><span class="sxs-lookup"><span data-stu-id="c4ef5-111">Adding Sinks to the Writer</span></span>

<span data-ttu-id="c4ef5-112">Writer-senken sind separate Objekte vom Writer und müssen dem Writer hinzugefügt werden, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4ef5-112">Writer sinks are separate objects from the writer and must be added to the writer to be used.</span></span> <span data-ttu-id="c4ef5-113">Wenn Sie in eine Datei schreiben, können Sie einfach [**iwmwriter:: setoutputfilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename)aufrufen, wodurch die Datei Senke automatisch eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="c4ef5-113">If you are writing to a file, you can simply call [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), which will set up the file sink automatically.</span></span> <span data-ttu-id="c4ef5-114">Um dem Writer eine Senke hinzuzufügen, müssen Sie andernfalls die Methode [**iwmschreiteradvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c4ef5-114">Otherwise, to add a sink to the writer, call the [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) method.</span></span> <span data-ttu-id="c4ef5-115">**Addsink** erfordert einen Zeiger auf die [**iwmschreitersink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) -Schnittstelle der Senke.</span><span class="sxs-lookup"><span data-stu-id="c4ef5-115">**AddSink** requires a pointer to the [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) interface of the sink.</span></span>

<span data-ttu-id="c4ef5-116">Wenn Sie mit der Verwendung einer Senke fertig sind, sollten Sie Sie schließen, indem Sie die entsprechende Methode aufrufen, abhängig vom Typ der Senke, und Sie dann aus dem Writer entfernen, indem Sie [**iwmschreiteradvanced:: removesink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c4ef5-116">When you are finished using a sink, you should close it by calling the appropriate method, depending on the type of sink, and then remove it from the writer by calling [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).</span></span>

<span data-ttu-id="c4ef5-117">Der folgende Beispielcode zeigt, wie eine Writer-Datei Senke erstellt und dem Writer hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c4ef5-117">The following example code shows how to create a writer file sink and add it to the writer.</span></span> <span data-ttu-id="c4ef5-118">Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="c4ef5-118">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT AddFileSink(IWMWriterFileSink** ppFileSink, IWMWriter* pWriter)
{
    HRESULT hr = S_OK;
    IWMWriterSink*     pSinkBase       = NULL;
    IWMWriterAdvanced* pWriterAdvanced = NULL;

    hr = CreateWriterFileSink(ppFileSink);
    GOTO_EXIT_IF_FAILED(hr);

    hr = *ppFileSink->QueryInterface(IID_IWMWriterSink, 
                                     (void**) &pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced,
                                 (void**) &pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriterAdvanced->AddSink(pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

Exit:
    SAFE_RELEASE(pSinkBase);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="c4ef5-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4ef5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4ef5-120">**Erhalten von Fehlermeldungen aus einer Senke**</span><span class="sxs-lookup"><span data-stu-id="c4ef5-120">**Getting Error Messages from a Sink**</span></span>](getting-error-messages-from-a-sink.md)
</dt> <dt>

[<span data-ttu-id="c4ef5-121">**Iwmschreiteradvanced-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c4ef5-121">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="c4ef5-122">**Arbeiten mit Writer-senken**</span><span class="sxs-lookup"><span data-stu-id="c4ef5-122">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




