---
description: Verarbeiten von Daten im Encoder
ms.assetid: 7be4c5e7-db2c-4063-8e5c-af6ffb861aa5
title: Verarbeiten von Daten im Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b7fedef50df61851408d084b511497eacd0288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372914"
---
# <a name="processing-data-in-the-encoder"></a><span data-ttu-id="c4793-103">Verarbeiten von Daten im Encoder</span><span class="sxs-lookup"><span data-stu-id="c4793-103">Processing Data in the Encoder</span></span>

<span data-ttu-id="c4793-104">Nachdem Sie den Eingabetyp und den Ausgabetyp für den Encoder-MFT ausgehandelt haben, wie in [Medientyp Aushandlung für den Encoder](media-type-negotiation-on-the-encoder.md)beschrieben, können Sie mit der Verarbeitung von Mediendaten Beispielen beginnen.</span><span class="sxs-lookup"><span data-stu-id="c4793-104">After you have negotiated the input type and output type for the encoder MFT, as described in [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md), you can start processing media data samples.</span></span> <span data-ttu-id="c4793-105">Die Daten werden in Form von Medien Beispielen ([**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle) und auch von der Ausgabe als Medien Beispiele empfangen.</span><span class="sxs-lookup"><span data-stu-id="c4793-105">The data is passed in form of media samples ([**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface) and also received from the output as media samples.</span></span>

<span data-ttu-id="c4793-106">Bevor Sie Daten zur Verarbeitung an den Encoder senden, müssen Sie ein Medien Beispiel zuordnen und einen von weiteren Medien Puffern mit Mediendaten hinzufügen, die codiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c4793-106">Before sending data to the encoder for processing, you must allocate a media sample and add one of more media buffers containing media data that needs to be encoded.</span></span> <span data-ttu-id="c4793-107">Aufrufen von [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) und übergeben eines Zeigers an das zugeordnete Medien Beispiel.</span><span class="sxs-lookup"><span data-stu-id="c4793-107">Call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) and pass a pointer to the allocated media sample.</span></span> <span data-ttu-id="c4793-108">Zusätzlich zum Medien Beispiel benötigt **ProcessInput** auch den Eingabedaten Strom Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c4793-108">In addition to the media sample, **ProcessInput** also needs the input stream identifier.</span></span> <span data-ttu-id="c4793-109">Um den Datenstrom Bezeichner abzurufen, nennen Sie [**imftransform:: getstreamids**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids).</span><span class="sxs-lookup"><span data-stu-id="c4793-109">To get the stream identifier, call [**IMFTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids).</span></span> <span data-ttu-id="c4793-110">Da ein Encoder nur eine und eine Ausgabe haben soll, haben diese Datenstrom Bezeichner immer den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="c4793-110">Because an encoder is designed to have only one and one output, these stream identifiers always have the value of 0.</span></span>

<span data-ttu-id="c4793-111">Um Daten vom Encoder abzurufen, nennen Sie [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="c4793-111">To get data from the encoder, call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="c4793-112">Bevor Sie [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput)aufzurufen, müssen Sie herausfinden, ob der Encoder die Ausgabemedien Beispiele zuordnet, oder Sie müssen dies explizit tun.</span><span class="sxs-lookup"><span data-stu-id="c4793-112">Before you call [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), you need to find out whether the encoder allocates the output media samples or you must do so explicitly.</span></span> <span data-ttu-id="c4793-113">Um dies zu erreichen, nennen Sie [**imftransform:: getoutputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).</span><span class="sxs-lookup"><span data-stu-id="c4793-113">To do this, call [**IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).</span></span> <span data-ttu-id="c4793-114">Dadurch werden Beispiel Informationen zu Ausgabemedien in der [**MFT- \_ Ausgabestream \_ \_**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) -Informationsstruktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4793-114">This returns output media sample information in the [**MFT\_OUTPUT\_STREAM\_INFO**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) structure.</span></span> <span data-ttu-id="c4793-115">Wenn der Encoder Medien Beispiele zuordnet, gibt er den MFT \_ -Ausgabestream enthält ein \_ \_ \_ beispielflag im **dwFlags** -Member und das **CBSIZE** -Element enthält 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c4793-115">If the encoder allocates media samples, it returns the MFT\_OUTPUT\_STREAM\_PROVIDES\_SAMPLES flag in the **dwFlags** member and the **cbSize** member contains zero.</span></span> <span data-ttu-id="c4793-116">Wenn der Encoder erwartet, dass Sie den Ausgabepuffer zuordnen, erstellen Sie das Ausgabemedien Beispiel und den zugehörigen Medien Puffer basierend auf der Größe, die in **CBSIZE** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c4793-116">If the encoder expects you to allocate the output buffer, create the output media sample and the associated media buffer based on the size returned in **cbSize**.</span></span> <span data-ttu-id="c4793-117">Wenn Sie [**processsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)aufrufen, übergeben Sie einen Zeiger auf das neu erstellte Medien Beispiel.</span><span class="sxs-lookup"><span data-stu-id="c4793-117">When you call [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), pass a pointer to the newly created media sample.</span></span> <span data-ttu-id="c4793-118">Während der Codierungs Sitzung füllt der Encoder die Medien Puffer, auf die das Ausgabemedien Beispiel verweist, mit den codierten Daten.</span><span class="sxs-lookup"><span data-stu-id="c4793-118">During the encoding session, the encoder fills the media buffers, pointed by the output media sample, with the encoded data.</span></span>

<span data-ttu-id="c4793-119">Zum Starten der Codierungs Sitzung übergeben Sie das Eingabemedien Beispiel durch Aufrufen von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)an den Encoder.</span><span class="sxs-lookup"><span data-stu-id="c4793-119">To start the encoding session, pass the input media sample to the encoder by calling [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="c4793-120">Der Encoder startet die Verarbeitung und die Daten und erstellt ein oder mehrere Ausgabemedien Beispiele, die von [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) abgerufen werden müssen, solange die Rückgabe von MF \_ E \_ Transform \_ \_ mehr Eingaben erforderlich ist \_ .</span><span class="sxs-lookup"><span data-stu-id="c4793-120">The encoder starts processing and the data and produces one or more output media samples that must be retrieved by [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) as long as it returns MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT.</span></span> <span data-ttu-id="c4793-121">Wenn Sie **ProcessInput** aufrufen, um mehr Eingaben zu übergeben, solange Ausgabedaten abgerufen werden müssen, schlägt **ProcessInput** fehl, wenn MF \_ E \_ notakzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c4793-121">If you call **ProcessInput** to pass more input as long as there is output data to be retrieved, **ProcessInput** fails with MF\_E\_NOTACCEPTING.</span></span> <span data-ttu-id="c4793-122">Der Encoder akzeptiert keine weiteren Eingaben, bis der Client **ProcessOutput** mindestens einmal aufruft.</span><span class="sxs-lookup"><span data-stu-id="c4793-122">The encoder does not accept any more input until the client calls **ProcessOutput** at least once.</span></span>

<span data-ttu-id="c4793-123">Sie sollten genaue Zeitstempel und Dauer für alle bestandenen Eingabe Beispiele festlegen.</span><span class="sxs-lookup"><span data-stu-id="c4793-123">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="c4793-124">Zeitstempel sind nicht unbedingt erforderlich, unterstützen jedoch die Verwaltung von Audiodaten und Videos.</span><span class="sxs-lookup"><span data-stu-id="c4793-124">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="c4793-125">Wenn Sie nicht über die Zeitstempel für die Beispiele verfügen, ist es besser, Sie zu verlassen, als nicht unsichere Werte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4793-125">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="encoder-processing-example"></a><span data-ttu-id="c4793-126">Beispiel für Codierungs Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="c4793-126">Encoder Processing Example</span></span>

<span data-ttu-id="c4793-127">Der folgende Beispielcode zeigt, wie [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) aufgerufen wird, um ein codiertes Beispiel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c4793-127">The following example code shows how to call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) to get an encoded sample.</span></span> <span data-ttu-id="c4793-128">Den gesamten Kontext dieses Beispiels finden Sie unter [Encoder-Beispiel Code](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="c4793-128">For the complete context of this example, see [Encoder Example Code](encoder-example-code.md).</span></span>


```C++
HRESULT CWmaEncoder::ProcessOutput(IMFSample **ppSample)
{
    if (m_pMFT == NULL)
    {
        return MF_E_NOT_INITIALIZED;
    }

    *ppSample = NULL;

    IMFMediaBuffer* pBufferOut = NULL;
    IMFSample* pSampleOut = NULL;

    DWORD dwStatus;
  
    MFT_OUTPUT_STREAM_INFO mftStreamInfo = { 0 };
    MFT_OUTPUT_DATA_BUFFER mftOutputData = { 0 };

    HRESULT hr = m_pMFT->GetOutputStreamInfo(m_dwOutputID, &mftStreamInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //create a buffer for the output sample
    hr = MFCreateMemoryBuffer(mftStreamInfo.cbSize, &pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the output sample
    hr = MFCreateSample(&pSampleOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output buffer 
    hr = pSampleOut->AddBuffer(pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }
 
    //Set the output sample
    mftOutputData.pSample = pSampleOut;

    //Set the output id
    mftOutputData.dwStreamID = m_dwOutputID;

    //Generate the output sample
    hr = m_pMFT->ProcessOutput(0, 1, &mftOutputData, &dwStatus);
    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        hr = S_OK;
        goto done;
    }

    // TODO: Handle MF_E_TRANSFORM_STREAM_CHANGE

    if (FAILED(hr))
    {
        goto done;
    }

    *ppSample = pSampleOut;
    (*ppSample)->AddRef();

done:
    SafeRelease(&pBufferOut);
    SafeRelease(&pSampleOut);
    return hr;
};
```



## <a name="related-topics"></a><span data-ttu-id="c4793-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4793-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4793-130">ASF Multiplexer</span><span class="sxs-lookup"><span data-stu-id="c4793-130">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="c4793-131">Instanziieren eines MFT-Encoders</span><span class="sxs-lookup"><span data-stu-id="c4793-131">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="c4793-132">Windows Media Encoder</span><span class="sxs-lookup"><span data-stu-id="c4793-132">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



