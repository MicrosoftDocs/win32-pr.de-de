---
title: Using Two-Pass Encoding (Windows Media Format 11 SDK)
description: Verwenden der Two-Pass Codierung
ms.assetid: 55fc768b-15f0-4236-ad0d-3792ccaa9b4f
keywords:
- Advanced Systems Format (ASF), Zwei-Pass-Codierung
- ASF (Advanced Systems Format), 2-Pass-Codierung
- Codierung mit zwei Durchgangen, Informationen
- 2-Pass-Codierung,About
- Codecs,Zwei-Pass-Codierung
- Zweipasscodierung, IWMWriterPreprocess-Schnittstelle
- 2-Pass-Codierung, IWMWriterPreprocess-Schnittstelle
- IWMWriterPreprocess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0683af636197b3f8116fca4dea85ce15609d2c99b0d9e0c11dfe0a2662a424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653835"
---
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a>Using Two-Pass Encoding (Windows Media Format 11 SDK)

Einige Codecs unterstützen die Zwei-Pass-Codierung für bestimmte Formate. In einigen Fällen erfordert ein Codec, dass ein angegebenes Format mit zwei Durchläufen codiert wird. Wenn die Zwei-Pass-Codierung verwendet wird, senden Sie die Beispiele für den Stream vor dem Codierungspass an den Codec. Der Codec analysiert die Beispiele und konfiguriert den Codierungspass basierend auf der Analyse. Dies führt zu einer effizienter codierten Datei.

Um zu bestimmen, ob ein Codec 1-Pass-Codierung, Zwei-Durch-Codierung oder beides für ein bestimmtes Format unterstützt, rufen Sie [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) mit g wszNumPasses und dem entsprechenden Wert auf, und enumerieren Sie dann die Formate, um festzustellen, ob das formatierte zurückgegeben \_ wird. Weitere Informationen zu den Windows Mediencodecs, die die Zwei-Durch-Durch-Codierung unterstützen, finden Sie unter [Auswählen einer Codierungsmethode.](choosing-an-encoding-method.md)

Sie können die Zwei-Pass-Codierung mit dem Windows Media Format SDK verwenden, indem Sie Methoden der [**IWMWriterPreprocess-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) aufrufen.

In Fällen, in denen für ein bestimmtes Format eine Codierung mit zwei Durchläufen erforderlich ist, die Anwendung jedoch keine Vorverarbeitungsüberläufe ausführen kann, schlägt der erste Aufruf von [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) mit NS \_ E INVALID NUM PASSES \_ \_ \_ fehl.

Die folgende Beispielfunktion veranschaulicht das Ausführen der Codierung mit zwei Durchgangen. Diese Funktion wird aufgerufen, nachdem der Writer mit einem Profil festgelegt und gestartet wurde. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).


```C++
HRESULT PreProcess(IWMWriter* pWriter, DWORD dwInputNum)
{
    HRESULT hr        = S_OK;
    DWORD   dwMaxPass = 0;

    IWMWriterPreprocess* pPreProc = NULL;

    // Get the writer preprocessor interface.
    hr = pWriter->QueryInterface(IID_IWMWriterPreprocess, 
                                 (void**) &pPreProc);
    GOTO_EXIT_IF_FAILED(hr);

    // Check that the input can be preprocessed.
    hr = pPreProc->GetMaxPreprocessingPasses(dwInputNum,0, &dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    if(dwMaxPass == 0)
    {
        hr = NS_E_INVALID_REQUEST;
        goto Exit;
    }

    // Set the number of preprocessing passes to the maximum.
    hr = pPreProc->SetNumPreprocessingPasses(dwInputNum, 0, dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    // Call BeginWriting before calling BeginPreprocessingPass
    hr = pWriter->BeginWriting();

    // Start preprocessing the first pass.
    hr = pPreProc->BeginPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: Make repeated calls to pPreProc->PreprocessSample to
    // preprocess all the samples in the stream.

    // End preprocessing.
    hr = pPreProc->EndPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: If the maximum number of preprocessing passes is greater
    // than one, repeat the preprocessing steps for each pass.

Exit:
    SAFE_RELEASE(pPreProc);
    Return hr;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




