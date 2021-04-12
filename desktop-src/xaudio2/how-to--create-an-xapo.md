---
description: Die xapo-API stellt die ixapo-Schnittstelle und die cxapobase-Klasse zum Entwickeln neuer xapo-Typen bereit.
ms.assetid: 34f5c3d5-ee40-e304-7c97-d30c17621d26
title: "So wird's gemacht: Erstellen eines XAPOs"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 549739462a0e76cbb437f0aa1403b099f72f5224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218560"
---
# <a name="how-to-create-an-xapo"></a><span data-ttu-id="5e158-103">So wird's gemacht: Erstellen eines XAPOs</span><span class="sxs-lookup"><span data-stu-id="5e158-103">How to: Create an XAPO</span></span>

<span data-ttu-id="5e158-104">Die xapo-API stellt die [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo) -Schnittstelle und die [**cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) -Klasse zum Entwickeln neuer xapo-Typen bereit.</span><span class="sxs-lookup"><span data-stu-id="5e158-104">The XAPO API provides the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface and the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class for building new XAPO types.</span></span> <span data-ttu-id="5e158-105">Die **ixapo** -Schnittstelle enthält alle Methoden, die implementiert werden müssen, um eine neue xapo-Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5e158-105">The **IXAPO** interface contains all of the methods that need to be implemented to create a new XAPO.</span></span> <span data-ttu-id="5e158-106">Die **cxapobase** -Klasse stellt eine grundlegende Implementierung der **ixapo** -Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="5e158-106">The **CXAPOBase** class provides a basic implementation of the **IXAPO** interface.</span></span> <span data-ttu-id="5e158-107">**Cxapobase** implementiert alle **ixapo** -Schnittstellen Methoden außer der [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Methode, die für jedes xapo eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="5e158-107">**CXAPOBase** implements all of the **IXAPO** interface methods except the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, which is unique to each XAPO.</span></span>

## <a name="to-create-a-new-static-xapo"></a><span data-ttu-id="5e158-108">So erstellen Sie ein neues statisches xapo</span><span class="sxs-lookup"><span data-stu-id="5e158-108">To create a new static XAPO</span></span>

1.  <span data-ttu-id="5e158-109">Leiten Sie eine neue xapo-Klasse von der [**cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) -Basisklasse ab.</span><span class="sxs-lookup"><span data-stu-id="5e158-109">Derive a new XAPO class from the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) base class.</span></span>

    > [!Note]  
    > <span data-ttu-id="5e158-110">Xapos implementiert die **IUnknown** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5e158-110">XAPOs implement the **IUnknown** interface.</span></span> <span data-ttu-id="5e158-111">Die [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo) -und [**ixapoparameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) -Schnittstellen enthalten die drei **IUnknown** -Methoden: **QueryInterface**, **adressf** und **Release**.</span><span class="sxs-lookup"><span data-stu-id="5e158-111">The [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) and [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interfaces include the three **IUnknown** methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="5e158-112">[**Cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) stellt Implementierungen aller drei **IUnknown** -Methoden bereit.</span><span class="sxs-lookup"><span data-stu-id="5e158-112">[**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) provides implementations of all three of the **IUnknown** methods.</span></span> <span data-ttu-id="5e158-113">Eine neue Instanz von **cxapobase** erhält einen Verweis Zähler von 1.</span><span class="sxs-lookup"><span data-stu-id="5e158-113">A new instance of **CXAPOBase** will have a reference count of 1.</span></span> <span data-ttu-id="5e158-114">Er wird zerstört, wenn der Verweis Zähler 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="5e158-114">It will be destroyed when its reference count becomes 0.</span></span> <span data-ttu-id="5e158-115">Um zuzulassen, dass XAudio2 eine Instanz von xapo zerstört, wenn Sie nicht mehr benötigt wird, nennen Sie **IUnknown:: Release** auf dem xapo, nachdem es einer XAudio2-Wirkungskette hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="5e158-115">To allow XAudio2 to destroy an instance of an XAPO when it is no longer needed, call **IUnknown::Release** on the XAPO after it is added to an XAudio2 effect chain.</span></span> <span data-ttu-id="5e158-116">Weitere Informationen zur Verwendung von xapo mit XAudio2 finden Sie unter Gewusst [wie: Verwenden von xapo in XAudio2](how-to--use-an-xapo-in-xaudio2.md) .</span><span class="sxs-lookup"><span data-stu-id="5e158-116">See [How to: Use an XAPO in XAudio2](how-to--use-an-xapo-in-xaudio2.md) for more information about using an XAPO with XAudio2.</span></span>

     

2.  <span data-ttu-id="5e158-117">Überschreiben Sie die Implementierung der [**cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) -Klasse der [**ixapo:: lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5e158-117">Override the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class implementation of the [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) method.</span></span>

    <span data-ttu-id="5e158-118">Durch das Überschreiben von [**lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) können Informationen über das Format der Audiodaten für die Verwendung in [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="5e158-118">Overriding [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) allows information about the format of audio data to be stored for use in [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

3.  <span data-ttu-id="5e158-119">Implementieren Sie die [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5e158-119">Implement the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method.</span></span>

    <span data-ttu-id="5e158-120">XAudio2 Ruft die [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Methode auf, wenn ein xapo Audiodaten verarbeiten muss.</span><span class="sxs-lookup"><span data-stu-id="5e158-120">XAudio2 calls the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method whenever an XAPO needs to process audio data.</span></span> <span data-ttu-id="5e158-121">Der **Prozess** enthält den Großteil des Codes für ein xapo.</span><span class="sxs-lookup"><span data-stu-id="5e158-121">**Process** contains the bulk of the code for an XAPO.</span></span>

## <a name="implementing-the-process-method"></a><span data-ttu-id="5e158-122">Implementieren der Process-Methode</span><span class="sxs-lookup"><span data-stu-id="5e158-122">Implementing the Process Method</span></span>

<span data-ttu-id="5e158-123">Die [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Methode akzeptiert Streampuffer für Eingabe-und ausgabeaudiodaten.</span><span class="sxs-lookup"><span data-stu-id="5e158-123">The [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method accepts stream buffers for input and output audio data.</span></span> <span data-ttu-id="5e158-124">Ein typisches xapo-Objekt erwartet einen Eingabestreampuffer und einen ausgabestreampuffer.</span><span class="sxs-lookup"><span data-stu-id="5e158-124">A typical XAPO will expect one input stream buffer and one output stream buffer.</span></span> <span data-ttu-id="5e158-125">Sie sollten die Verarbeitung von Daten aus dem Eingabestreampuffer auf das in der [**lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) -Funktion angegebene Format und alle Flags, die an die **Prozess** Funktion mit dem Eingabestreampuffer weitergegeben wurden, basieren.</span><span class="sxs-lookup"><span data-stu-id="5e158-125">You should base the processing of data from the input stream buffer on the format specified in the [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) function and any flags passed to the **Process** function with the input stream buffer.</span></span> <span data-ttu-id="5e158-126">Kopieren Sie die verarbeiteten Eingabedaten Strom-Puffer Daten in den ausgabestreampuffer.</span><span class="sxs-lookup"><span data-stu-id="5e158-126">Copy the processed input stream buffer data to the output stream buffer.</span></span> <span data-ttu-id="5e158-127">Legen Sie den bufferflags-Parameter des ausgabestreampuffers entweder als [**\_ \_ gültiger xapo-Puffer**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) oder **xapo- \_ \_ Puffer** unbeaufsichtigt fest</span><span class="sxs-lookup"><span data-stu-id="5e158-127">Set the output stream buffer's BufferFlags parameter as either [**XAPO\_BUFFER\_VALID**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) or **XAPO\_BUFFER\_SILENT**.</span></span>

<span data-ttu-id="5e158-128">Im folgenden Beispiel wird eine [**lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) -und [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Implementierung veranschaulicht, mit der Daten einfach aus einem Eingabepuffer in einen Ausgabepuffer kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="5e158-128">The following example demonstrates a [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) and [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation that simply copies data from an input buffer to an output buffer.</span></span> <span data-ttu-id="5e158-129">Es gibt jedoch keine Verarbeitung, wenn der Eingabepuffer mit dem automatischen [**xapo \_ - \_ Puffer**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags)markiert ist.</span><span class="sxs-lookup"><span data-stu-id="5e158-129">However, there is no processing if the input buffer is marked with [**XAPO\_BUFFER\_SILENT**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).</span></span>


```
STDMETHOD(LockForProcess) (UINT32 InputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pInputLockedParameters,
          UINT32 OutputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pOutputLockedParameters)
{
    assert(!IsLocked());
    assert(InputLockedParameterCount == 1);
    assert(OutputLockedParameterCount == 1);
    assert(pInputLockedParameters != NULL);
    assert(pOutputLockedParameters != NULL);
    assert(pInputLockedParameters[0].pFormat != NULL);
    assert(pOutputLockedParameters[0].pFormat != NULL);


    m_uChannels = pInputLockedParameters[0].pFormat->nChannels;
    m_uBytesPerSample = (pInputLockedParameters[0].pFormat->wBitsPerSample >> 3);

    return CXAPOBase::LockForProcess(
        InputLockedParameterCount,
        pInputLockedParameters,
        OutputLockedParameterCount,
        pOutputLockedParameters);
}
STDMETHOD_(void, Process)(UINT32 InputProcessParameterCount,
           const XAPO_PROCESS_BUFFER_PARAMETERS* pInputProcessParameters,
           UINT32 OutputProcessParameterCount,
           XAPO_PROCESS_BUFFER_PARAMETERS* pOutputProcessParameters,
           BOOL IsEnabled)
{
    assert(IsLocked());
    assert(InputProcessParameterCount == 1);
    assert(OutputProcessParameterCount == 1);
    assert(NULL != pInputProcessParameters);
    assert(NULL != pOutputProcessParameters);


    XAPO_BUFFER_FLAGS inFlags = pInputProcessParameters[0].BufferFlags;
    XAPO_BUFFER_FLAGS outFlags = pOutputProcessParameters[0].BufferFlags;

    // assert buffer flags are legitimate
    assert(inFlags == XAPO_BUFFER_VALID || inFlags == XAPO_BUFFER_SILENT);
    assert(outFlags == XAPO_BUFFER_VALID || outFlags == XAPO_BUFFER_SILENT);

    // check input APO_BUFFER_FLAGS
    switch (inFlags)
    {
    case XAPO_BUFFER_VALID:
        {
            void* pvSrc = pInputProcessParameters[0].pBuffer;
            assert(pvSrc != NULL);

            void* pvDst = pOutputProcessParameters[0].pBuffer;
            assert(pvDst != NULL);

            memcpy(pvDst,pvSrc,pInputProcessParameters[0].ValidFrameCount * m_uChannels * m_uBytesPerSample);
            break;
        }

    case XAPO_BUFFER_SILENT:
        {
            // All that needs to be done for this case is setting the
            // output buffer flag to XAPO_BUFFER_SILENT which is done below.
            break;
        }

    }

    // set destination valid frame count, and buffer flags
    pOutputProcessParameters[0].ValidFrameCount = pInputProcessParameters[0].ValidFrameCount; // set destination frame count same as source
    pOutputProcessParameters[0].BufferFlags     = pInputProcessParameters[0].BufferFlags;     // set destination buffer flags same as source

}
```



<span data-ttu-id="5e158-130">Beim Schreiben einer [**Prozess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) Methode ist es wichtig zu beachten, dass sich XAudio2 Audiodaten überlappen.</span><span class="sxs-lookup"><span data-stu-id="5e158-130">When writing a [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, it is important to note XAudio2 audio data is interleaved.</span></span> <span data-ttu-id="5e158-131">Dies bedeutet, dass die Daten aus den einzelnen Kanälen für eine bestimmte Stichproben Nummer nebeneinander liegen.</span><span class="sxs-lookup"><span data-stu-id="5e158-131">This means data from each channel is adjacent for a particular sample number.</span></span> <span data-ttu-id="5e158-132">Wenn z. b. eine 4-Kanal-Welle in einer XAudio2 Source-Sprache vorhanden ist, sind die Audiodaten ein Beispiel für Channel 0, ein Beispiel für Channel 1, ein Beispiel für Channel 2, ein Beispiel für Channel 3 und anschließend das nächste Beispiel der Kanäle 0, 1, 2, 3 usw.</span><span class="sxs-lookup"><span data-stu-id="5e158-132">For example, if there is a 4-channel wave playing into an XAudio2 source voice, the audio data is a sample of channel 0, a sample of channel 1, a sample of channel 2, a sample of channel 3, and then the next sample of channels 0, 1, 2, 3, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e158-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e158-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e158-134">Audioeffekte</span><span class="sxs-lookup"><span data-stu-id="5e158-134">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="5e158-135">Übersicht über xapo</span><span class="sxs-lookup"><span data-stu-id="5e158-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
