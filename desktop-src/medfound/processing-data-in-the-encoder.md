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
# <a name="processing-data-in-the-encoder"></a>Verarbeiten von Daten im Encoder

Nachdem Sie den Eingabetyp und den Ausgabetyp für den Encoder-MFT ausgehandelt haben, wie in [Medientyp Aushandlung für den Encoder](media-type-negotiation-on-the-encoder.md)beschrieben, können Sie mit der Verarbeitung von Mediendaten Beispielen beginnen. Die Daten werden in Form von Medien Beispielen ([**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle) und auch von der Ausgabe als Medien Beispiele empfangen.

Bevor Sie Daten zur Verarbeitung an den Encoder senden, müssen Sie ein Medien Beispiel zuordnen und einen von weiteren Medien Puffern mit Mediendaten hinzufügen, die codiert werden müssen. Aufrufen von [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) und übergeben eines Zeigers an das zugeordnete Medien Beispiel. Zusätzlich zum Medien Beispiel benötigt **ProcessInput** auch den Eingabedaten Strom Bezeichner. Um den Datenstrom Bezeichner abzurufen, nennen Sie [**imftransform:: getstreamids**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids). Da ein Encoder nur eine und eine Ausgabe haben soll, haben diese Datenstrom Bezeichner immer den Wert 0.

Um Daten vom Encoder abzurufen, nennen Sie [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Bevor Sie [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput)aufzurufen, müssen Sie herausfinden, ob der Encoder die Ausgabemedien Beispiele zuordnet, oder Sie müssen dies explizit tun. Um dies zu erreichen, nennen Sie [**imftransform:: getoutputstreaminfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo). Dadurch werden Beispiel Informationen zu Ausgabemedien in der [**MFT- \_ Ausgabestream \_ \_**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) -Informationsstruktur zurückgegeben. Wenn der Encoder Medien Beispiele zuordnet, gibt er den MFT \_ -Ausgabestream enthält ein \_ \_ \_ beispielflag im **dwFlags** -Member und das **CBSIZE** -Element enthält 0 (null). Wenn der Encoder erwartet, dass Sie den Ausgabepuffer zuordnen, erstellen Sie das Ausgabemedien Beispiel und den zugehörigen Medien Puffer basierend auf der Größe, die in **CBSIZE** zurückgegeben wurde. Wenn Sie [**processsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)aufrufen, übergeben Sie einen Zeiger auf das neu erstellte Medien Beispiel. Während der Codierungs Sitzung füllt der Encoder die Medien Puffer, auf die das Ausgabemedien Beispiel verweist, mit den codierten Daten.

Zum Starten der Codierungs Sitzung übergeben Sie das Eingabemedien Beispiel durch Aufrufen von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)an den Encoder. Der Encoder startet die Verarbeitung und die Daten und erstellt ein oder mehrere Ausgabemedien Beispiele, die von [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) abgerufen werden müssen, solange die Rückgabe von MF \_ E \_ Transform \_ \_ mehr Eingaben erforderlich ist \_ . Wenn Sie **ProcessInput** aufrufen, um mehr Eingaben zu übergeben, solange Ausgabedaten abgerufen werden müssen, schlägt **ProcessInput** fehl, wenn MF \_ E \_ notakzeptiert. Der Encoder akzeptiert keine weiteren Eingaben, bis der Client **ProcessOutput** mindestens einmal aufruft.

Sie sollten genaue Zeitstempel und Dauer für alle bestandenen Eingabe Beispiele festlegen. Zeitstempel sind nicht unbedingt erforderlich, unterstützen jedoch die Verwaltung von Audiodaten und Videos. Wenn Sie nicht über die Zeitstempel für die Beispiele verfügen, ist es besser, Sie zu verlassen, als nicht unsichere Werte zu verwenden.

## <a name="encoder-processing-example"></a>Beispiel für Codierungs Verarbeitung

Der folgende Beispielcode zeigt, wie [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) aufgerufen wird, um ein codiertes Beispiel abzurufen. Den gesamten Kontext dieses Beispiels finden Sie unter [Encoder-Beispiel Code](encoder-example-code.md).


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF Multiplexer](asf-multiplexer.md)
</dt> <dt>

[Instanziieren eines MFT-Encoders](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> </dl>

 

 



