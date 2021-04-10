---
title: Erhalten von Fehlermeldungen aus einer Senke
description: Erhalten von Fehlermeldungen aus einer Senke
ms.assetid: c948d06f-7728-4d89-8dc4-40d192c94099
keywords:
- Advanced Systems Format (ASF), Fehlermeldungen von senken
- ASF (Advanced Systems Format), Fehlermeldungen von senken
- Advanced Systems Format (ASF), senken
- ASF (Advanced Systems Format), senken
- senken, Fehlermeldungen
- Fehlermeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b3fbb43d72107dbffc13eb27425e253bc13839
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101266"
---
# <a name="getting-error-messages-from-a-sink"></a><span data-ttu-id="dd1ee-109">Erhalten von Fehlermeldungen aus einer Senke</span><span class="sxs-lookup"><span data-stu-id="dd1ee-109">Getting Error Messages from a Sink</span></span>

<span data-ttu-id="dd1ee-110">Das Writer-Objekt sendet keine Nachrichten an die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode.</span><span class="sxs-lookup"><span data-stu-id="dd1ee-110">The writer object does not send messages to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="dd1ee-111">Sie können jedoch Writer-senken festlegen, um Nachrichten an OnStatus zu senden.</span><span class="sxs-lookup"><span data-stu-id="dd1ee-111">However, you can set writer sinks to send messages to OnStatus.</span></span> <span data-ttu-id="dd1ee-112">Jede Senke muss so festgelegt werden, dass Sie den Status separat bereitstellt, aber alle senken können an denselben Rückruf Berichten.</span><span class="sxs-lookup"><span data-stu-id="dd1ee-112">Each sink must be set to deliver status separately, but all sinks can report to the same callback.</span></span>

<span data-ttu-id="dd1ee-113">Um eine Senke für die übermitteln von Statusmeldungen an **OnStatus** festzulegen, rufen Sie die [**iwmregistercallback:: Empfehlung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="dd1ee-113">To set a sink to deliver status messages to **OnStatus**, call the [**IWMRegisterCallback::Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) method.</span></span>

<span data-ttu-id="dd1ee-114">Der folgende Beispielcode veranschaulicht, wie Sie alle senken festlegen, um Statusmeldungen an einen **OnStatus** -Rückruf zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="dd1ee-114">The following example code demonstrates how to set all of the sinks to deliver status messages to an **OnStatus** callback.</span></span> <span data-ttu-id="dd1ee-115">In diesem Beispiel wird der Index jeder Senke als Kontext Parameter verwendet, sodass die **OnStatus** -Methode zwischen Nachrichten von den verschiedenen senken unterscheiden kann.</span><span class="sxs-lookup"><span data-stu-id="dd1ee-115">In this example, the index of each sink will be used as the context parameter so that the **OnStatus** method can differentiate between messages from the different sinks.</span></span> <span data-ttu-id="dd1ee-116">Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="dd1ee-116">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT SetSinksForStatus (IWMWriter* pWriter, IWMStatusCallback* pStatus)
{
    HRESULT hr          = S_OK;
    DWORD   cSinks      = 0;
    DWORD   dwSinkIndex = 0;

    IWMWriterAdvanced*   pWriterAdvanced = NULL;
    IWMWriterSink*       pSink           = NULL;
    IWMRegisterCallback* pRegisterCallbk = NULL;

    // Get the advanced writer interface.
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, 
                                 (void**)&pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the number of sinks that are added to the writer object.
    hr = pWriterAdvanced->GetSinkCount(&cSinks);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all of the sinks.
    for(dwSinkIndex = 0; dwSinkIndex < cSinks; dwSinkIndex++)
    {
        // Get the base interface for the next sink.
        hr = pWriterAdvanced->GetSink(dwSinkIndex, &pSink);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the callback registration interface for the sink.
        hr = pSink->QueryInterface(IID_IWMRegisterCallback,
                                   (void**)&pRegisterCallbk);
        GOTO_EXIT_IF_FAILED(hr);

        // Register the OnStatus callback.
        hr = pRegisterCallbk->Advise(pStatus, (void*) &dwSinkIndex);
        GOTO_EXIT_IF_FAILED(hr);

        // Release for the next iteration.
        SAFE_RELEASE(pSink);
        SAFE_RELEASE(pRegisterCallbk);
    } // end for dwSinkIndex

Exit:
    SAFE_RELEASE(pSink);
    SAFE_RELEASE(pRegisterCallbk);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="dd1ee-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd1ee-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd1ee-118">**Iwmregistercallback-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="dd1ee-118">**IWMRegisterCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
</dt> <dt>

[<span data-ttu-id="dd1ee-119">**Arbeiten mit Writer-senken**</span><span class="sxs-lookup"><span data-stu-id="dd1ee-119">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




