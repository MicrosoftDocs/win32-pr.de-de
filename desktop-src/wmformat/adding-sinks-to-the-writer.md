---
title: Hinzufügen von Senken zum Writer
description: Hinzufügen von Senken zum Writer
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- Advanced Systems Format (ASF), Hinzufügen von Senken zum Writer
- ASF (Advanced Systems Format), Hinzufügen von Senken zum Writer
- Advanced Systems Format (ASF), Senken
- ASF (Advanced Systems Format), Senken
- Advanced Systems Format (ASF), Writer-Senken
- ASF (Advanced Systems Format), Writer-Senken
- senken, hinzufügen zum Writer
- Writer-Senken, hinzufügen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca64b412dd83e9bbba1d8de66b2aef335573c9e50073c2afe898fed0c34761b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810020"
---
# <a name="adding-sinks-to-the-writer"></a>Hinzufügen von Senken zum Writer

Writer-Senken sind separate Objekte vom Writer und müssen dem Writer hinzugefügt werden, um verwendet zu werden. Wenn Sie in eine Datei schreiben, können Sie einfach [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename)aufrufen, wodurch die Dateisenke automatisch eingerichtet wird. Rufen Sie andernfalls die [**IWMWriterAdvanced::AddSink-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) auf, um dem Writer eine Senke hinzuzufügen. **AddSink** erfordert einen Zeiger auf die [**IWMWriterSink-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) der Senke.

Wenn Sie mit der Verwendung einer Senke fertig sind, sollten Sie sie schließen, indem Sie je nach Typ der Senke die entsprechende Methode aufrufen und sie dann aus dem Writer entfernen, indem [**Sie IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink)aufrufen.

Der folgende Beispielcode zeigt, wie Eine Writer-Dateisenke erstellt und dem Writer hinzugefügt wird. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele.](using-the-code-examples.md)


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

[**Abrufen von Fehlermeldungen aus einer Senke**](getting-error-messages-from-a-sink.md)
</dt> <dt>

[**IWMWriterErweiterte Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Arbeiten mit Writer-Senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




