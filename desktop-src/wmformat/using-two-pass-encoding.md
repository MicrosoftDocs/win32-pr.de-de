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
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a><span data-ttu-id="7a77a-111">Verwenden der Two-Pass Codierung (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="7a77a-111">Using Two-Pass Encoding (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="7a77a-112">Einige Codecs unterstützen die zwei-Pass-Codierung für bestimmte Formate.</span><span class="sxs-lookup"><span data-stu-id="7a77a-112">Some codecs support two-pass encoding for certain formats.</span></span> <span data-ttu-id="7a77a-113">In einigen Fällen erfordert ein Codec, dass ein angegebenes Format mit zwei Durchläufen codiert wird.</span><span class="sxs-lookup"><span data-stu-id="7a77a-113">In some cases, a codec requires that a specified format be encoded using two passes.</span></span> <span data-ttu-id="7a77a-114">Wenn die zwei-Pass-Codierung verwendet wird, senden Sie die Beispiele für den Stream vor dem Codierungs Durchlauf an den Codec.</span><span class="sxs-lookup"><span data-stu-id="7a77a-114">When two-pass encoding is used, you send the samples for the stream to the codec before the encoding pass.</span></span> <span data-ttu-id="7a77a-115">Der Codec analysiert die Beispiele und konfiguriert den Codierungs Durchlauf basierend auf der Analyse.</span><span class="sxs-lookup"><span data-stu-id="7a77a-115">The codec analyzes the samples and configures the encoding pass based on the analysis.</span></span> <span data-ttu-id="7a77a-116">Dies führt zu einer effizienteren codierten Datei.</span><span class="sxs-lookup"><span data-stu-id="7a77a-116">This results in a more efficiently encoded file.</span></span>

<span data-ttu-id="7a77a-117">Um zu ermitteln, ob ein Codec eine Codierung mit nur einem oder zwei Pass-oder beides für ein bestimmtes Format unterstützt, müssen Sie [**IWMCodecInfo3:: setcodecenumerationsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) mit g \_ wsznumpass und den entsprechenden Wert aufrufen und dann die Formate auflisten, um festzustellen, ob die gewünschte zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7a77a-117">To determine whether a codec supports one-pass encoding, or two-pass, or both, for a given format, call [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) with g\_wszNumPasses and the appropriate value, and then enumerate the formats to see if the one you want is returned.</span></span> <span data-ttu-id="7a77a-118">Weitere Informationen zu den Windows Media-Codecs, die die zwei-Pass-Codierung unterstützen, finden Sie unter [Auswählen einer Codierungsmethode](choosing-an-encoding-method.md).</span><span class="sxs-lookup"><span data-stu-id="7a77a-118">For more information about the Windows Media codecs that support two-pass encoding, see [Choosing an Encoding Method](choosing-an-encoding-method.md).</span></span>

<span data-ttu-id="7a77a-119">Sie können die zwei-Pass-Codierung mit dem Windows Media-Format-SDK verwenden, indem Sie Methoden der [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) -Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a77a-119">You can use two-pass encoding with the Windows Media Format SDK by calling methods of the [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) interface.</span></span>

<span data-ttu-id="7a77a-120">In Fällen, in denen die zwei-Pass-Codierung für ein bestimmtes Format erforderlich ist, aber die Anwendung einen Vorverarbeitungs Durchlauf nicht ausführen kann, schlägt der erste Schreibvorgang von " [**schreitesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) " mit NS \_ E \_ ungültige \_ NUM-Pässe fehl \_ .</span><span class="sxs-lookup"><span data-stu-id="7a77a-120">In cases where two-pass encoding is required for a particular format, but the application fails to perform a preprocessing pass, the first call to [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) will fail with NS\_E\_INVALID\_NUM\_PASSES.</span></span>

<span data-ttu-id="7a77a-121">Die folgende Beispiel Funktion veranschaulicht, wie die Codierung mit zwei durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="7a77a-121">The following example function demonstrates how to perform two-pass encoding.</span></span> <span data-ttu-id="7a77a-122">Diese Funktion wird aufgerufen, nachdem der Writer mit einem Profil festgelegt und gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="7a77a-122">This function is called after the writer has been set with a profile and started.</span></span> <span data-ttu-id="7a77a-123">Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="7a77a-123">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7a77a-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a77a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a77a-125">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="7a77a-125">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




