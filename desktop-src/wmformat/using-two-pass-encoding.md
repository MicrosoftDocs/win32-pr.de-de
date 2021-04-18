---
title: Verwenden der Two-Pass Codierung (Windows Media Format 11 SDK)
description: Verwenden von Two-Pass Codierung
ms.assetid: 55fc768b-15f0-4236-ad0d-3792ccaa9b4f
keywords:
- Advanced Systems Format (ASF), zwei-Pass-Codierung
- ASF (Advanced Systems Format), Two-Pass Encoding
- zwei-Pass-Codierung, Informationen
- '2: Codierung, Informationen'
- Codecs, Two-Pass-Codierung
- Two-Pass-Codierung, IWMWriterPreprocess-Schnittstelle
- 2-Pass-Codierung, IWMWriterPreprocess-Schnittstelle
- IWMWriterPreprocess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3794856f47c1656cc53006268c41a063cdde96
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517336"
---
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a>Verwenden der Two-Pass Codierung (Windows Media Format 11 SDK)

Einige Codecs unterstützen die zwei-Pass-Codierung für bestimmte Formate. In einigen Fällen erfordert ein Codec, dass ein angegebenes Format mit zwei Durchläufen codiert wird. Wenn die zwei-Pass-Codierung verwendet wird, senden Sie die Beispiele für den Stream vor dem Codierungs Durchlauf an den Codec. Der Codec analysiert die Beispiele und konfiguriert den Codierungs Durchlauf basierend auf der Analyse. Dies führt zu einer effizienteren codierten Datei.

Um zu ermitteln, ob ein Codec eine Codierung mit nur einem oder zwei Pass-oder beides für ein bestimmtes Format unterstützt, müssen Sie [**IWMCodecInfo3:: setcodecenumerationsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) mit g \_ wsznumpass und den entsprechenden Wert aufrufen und dann die Formate auflisten, um festzustellen, ob die gewünschte zurückgegeben wird. Weitere Informationen zu den Windows Media-Codecs, die die zwei-Pass-Codierung unterstützen, finden Sie unter [Auswählen einer Codierungsmethode](choosing-an-encoding-method.md).

Sie können die zwei-Pass-Codierung mit dem Windows Media-Format-SDK verwenden, indem Sie Methoden der [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) -Schnittstelle aufrufen.

In Fällen, in denen die zwei-Pass-Codierung für ein bestimmtes Format erforderlich ist, aber die Anwendung einen Vorverarbeitungs Durchlauf nicht ausführen kann, schlägt der erste Schreibvorgang von " [**schreitesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) " mit NS \_ E \_ ungültige \_ NUM-Pässe fehl \_ .

Die folgende Beispiel Funktion veranschaulicht, wie die Codierung mit zwei durchlaufen wird. Diese Funktion wird aufgerufen, nachdem der Writer mit einem Profil festgelegt und gestartet wurde. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).


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

 

 




