---
description: Verarbeiten von Daten im Encoder
ms.assetid: 7be4c5e7-db2c-4063-8e5c-af6ffb861aa5
title: Verarbeiten von Daten im Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666c2a2ff2139aadcb489022eb9b324eff1de523551244c2fd12ad0e11f68f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238731"
---
# <a name="processing-data-in-the-encoder"></a>Verarbeiten von Daten im Encoder

Nachdem Sie den Eingabe- und Ausgabetyp für den Encoder-MFT ausgehandelt haben, wie unter [Medientypaushandlung auf dem Encoder](media-type-negotiation-on-the-encoder.md)beschrieben, können Sie mit der Verarbeitung von Mediendatenbeispielen beginnen. Die Daten werden in Form von Medienbeispielen [**(SCHNITTSTELLE " NSSAMPLE")**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) übergeben und auch als Medienbeispiele aus der Ausgabe empfangen.

Bevor Sie Daten zur Verarbeitung an den Encoder senden, müssen Sie ein Medienbeispiel zuordnen und einen von mehreren Medienpuffern hinzufügen, die Mediendaten enthalten, die codiert werden müssen. Rufen Sie [**ÜBERTRANSFORM::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) auf, und übergeben Sie einen Zeiger auf das zugeordnete Medienbeispiel. Zusätzlich zum Medienbeispiel benötigt **ProcessInput** auch den Eingabestreambezeichner. Um den Streambezeichner abzurufen, rufen [**Sie ÜBERTRANSFORM::GetStreamIDs auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) Da ein Encoder so konzipiert ist, dass er nur eine und eine Ausgabe hat, weisen diese Streambezeichner immer den Wert 0 auf.

Rufen Sie ZUM Abrufen von Daten aus dem Encoder [**DENTRANSFORM::P rocessOutput auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) Bevor Sie [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput)aufrufen, müssen Sie herausfinden, ob der Encoder die Ausgabemedienbeispiele zuordnet, oder sie müssen dies explizit tun. Rufen Sie zu diesem Thema [**DIE FORMTRANSFORM::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)auf. Dadurch werden Ausgabemedienbeispielinformationen in der [**MFT \_ OUTPUT STREAM \_ \_ INFO-Struktur**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) zurückgegeben. Wenn der Encoder Medienbeispiele zuordnet, gibt er das Flag MFT \_ OUTPUT STREAM PROVIDES SAMPLES im \_ \_ \_ **dwFlags-Member** zurück, und der **cbSize-Member** enthält 0 (null). Wenn der Encoder erwartet, dass Sie den Ausgabepuffer zuordnen, erstellen Sie das Ausgabemedienbeispiel und den zugeordneten Medienpuffer basierend auf der in **cbSize zurückgegebenen** Größe. Wenn Sie [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)aufrufen, übergeben Sie einen Zeiger auf das neu erstellte Medienbeispiel. Während der Codierungssitzung füllt der Encoder die Medienpuffer, auf die das Ausgabemedienbeispiel zeigt, mit den codierten Daten.

Um die Codierungssitzung zu starten, übergeben Sie das Eingabemedienbeispiel an den Encoder, indem [**Sie ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)aufrufen. Der Encoder beginnt mit der Verarbeitung und den Daten und erzeugt mindestens ein Ausgabemedienbeispiel, das von [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) abgerufen werden muss, solange MF E TRANSFORM NEED MORE INPUT zurückgegeben \_ \_ \_ \_ \_ wird. Wenn Sie **ProcessInput** aufrufen, um mehr Eingaben zu übergeben, solange Ausgabedaten abgerufen werden müssen, schlägt **ProcessInput** mit MF \_ E \_ NOTACCEPTING fehl. Der Encoder akzeptiert keine weiteren Eingaben, bis der Client **ProcessOutput** mindestens einmal aufruft.

Sie sollten genaue Zeitstempel und Daueren für alle übergebenen Eingabebeispiele festlegen. Zeitstempel sind nicht unbedingt erforderlich, unterstützen aber die Aufrechterhaltung der Audio-/Videosynchronisierung. Wenn Sie nicht über die Zeitstempel für Ihre Stichproben verfügen, sollten Sie sie besser weglassen, als unsichere Werte zu verwenden.

## <a name="encoder-processing-example"></a>Encoderverarbeitungsbeispiel

Der folgende Beispielcode zeigt, wie [**SIE DIE DATEI "ROCTRANSFORM::P rocessOutput"**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) aufrufen, um ein codiertes Beispiel abzurufen. Den vollständigen Kontext dieses Beispiels finden Sie unter [Encoder-Beispielcode.](encoder-example-code.md)


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

[Instanziieren eines Encoder-MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Medienencoder](windows-media-encoders.md)
</dt> </dl>

 

 



