---
title: Abrufen von Fehlermeldungen aus einer Senke
description: Abrufen von Fehlermeldungen aus einer Senke
ms.assetid: c948d06f-7728-4d89-8dc4-40d192c94099
keywords:
- Advanced Systems Format (ASF), Fehlermeldungen von Senken
- ASF (Advanced Systems Format), Fehlermeldungen von Senken
- Advanced Systems Format (ASF),sinks
- ASF (Advanced Systems Format), sinks
- sinks,error messages
- Fehlermeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e432f805b5e33de0e830a2f319713bccec328d429f8eb04064d87edc56bf375c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930870"
---
# <a name="getting-error-messages-from-a-sink"></a>Abrufen von Fehlermeldungen aus einer Senke

Das Writer-Objekt sendet keine Nachrichten an die [**IWMStatusCallback::OnStatus-Rückrufmethode.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Sie können jedoch Writer-Senken festlegen, um Nachrichten an OnStatus zu senden. Jede Senke muss so festgelegt werden, dass der Status separat zu liefern ist, aber alle Senken können einen Bericht an denselben Rückruf erstellen.

Um eine Senke für die Zustellung von Statusmeldungen an **OnStatus zu** festlegen, rufen Sie [**die IWMRegisterCallback::Advise-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) auf.

Der folgende Beispielcode veranschaulicht, wie alle Senken festgelegt werden, um Statusmeldungen an einen **OnStatus-Rückruf** zu senden. In diesem Beispiel wird der Index jeder Senke als Kontextparameter verwendet, sodass die **OnStatus-Methode** zwischen Nachrichten aus den verschiedenen Senken unterscheiden kann. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele.](using-the-code-examples.md)


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMRegisterCallback-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
</dt> <dt>

[**Arbeiten mit Writer-Senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




