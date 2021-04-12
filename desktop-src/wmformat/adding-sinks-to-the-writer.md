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
# <a name="adding-sinks-to-the-writer"></a>Hinzufügen von senken zum Writer

Writer-senken sind separate Objekte vom Writer und müssen dem Writer hinzugefügt werden, der verwendet werden soll. Wenn Sie in eine Datei schreiben, können Sie einfach [**iwmwriter:: setoutputfilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename)aufrufen, wodurch die Datei Senke automatisch eingerichtet wird. Um dem Writer eine Senke hinzuzufügen, müssen Sie andernfalls die Methode [**iwmschreiteradvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) aufzurufen. **Addsink** erfordert einen Zeiger auf die [**iwmschreitersink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) -Schnittstelle der Senke.

Wenn Sie mit der Verwendung einer Senke fertig sind, sollten Sie Sie schließen, indem Sie die entsprechende Methode aufrufen, abhängig vom Typ der Senke, und Sie dann aus dem Writer entfernen, indem Sie [**iwmschreiteradvanced:: removesink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink)aufrufen.

Der folgende Beispielcode zeigt, wie eine Writer-Datei Senke erstellt und dem Writer hinzugefügt wird. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erhalten von Fehlermeldungen aus einer Senke**](getting-error-messages-from-a-sink.md)
</dt> <dt>

[**Iwmschreiteradvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Arbeiten mit Writer-senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




