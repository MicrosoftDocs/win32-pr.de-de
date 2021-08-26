---
description: Verwenden privater Videocodec-Daten
ms.assetid: 0cc24fe4-a5b6-4805-8c8e-3066d12ec4bd
title: Verwenden privater Videocodec-Daten (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e417d4d83cc3ae3174e1bbf3310a6abb2900e2c5f3323192a8d17643e4066f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887090"
---
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a>Verwenden privater Videocodec-Daten (Microsoft Media Foundation)

Die komprimierte Ausgabe, die von den Windows Media Video 9-Codecs erzeugt wird, kann nicht ordnungsgemäß dekomprimiert werden, ohne dass daten vom Encoder bereitgestellt werden. Diese Daten, die als private Codecdaten bezeichnet werden, müssen an den Ausgabemedientyp angefügt werden. Sie können die privaten Codecdaten abrufen, indem Sie die Methoden der [IWMCodecPrivateData-Schnittstelle](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) aufrufen. Übergeben Sie die andernfalls vollständige [**DMO \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) an [IWMCodecPrivateData::SetPartialOutputType.](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype) Rufen Sie dann [zweimal IWMCodecPrivateData::GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) auf, einmal, um die Größe der Daten abzurufen, und dann erneut, um die Daten in einen Puffer dieser Größe zu kopieren. Erstellen Sie einen neuen Puffer, um die [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) mit angefügten privaten Daten zu speichern, und kopieren Sie die Struktur und die Daten in diesen Puffer. Legen Sie abschließend den **pbFormat-Member** der **DMO MEDIA \_ \_ TYPE-Struktur** auf die Adresse des neu erstellten Puffers und den **cbFormat-Member** auf die kombinierte Größe des **VIDEOINFOHEADER** und der privaten Daten in Bytes fest.

Wenn Sie MediaFoundation verwenden, können Sie eine [**DMO \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) aus einer [**INTERFACESMediaType-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) erstellen, indem Sie [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)aufrufen.

Sie müssen die privaten Codecdaten verwenden, die sie nach dem ersten Festlegen der Eigenschaften im Encoder erhalten haben. Wenn Eigenschaften geändert werden, müssen Sie neue private Daten abrufen. Wenn Sie die privaten Daten nicht verwenden, die abgerufen werden, nachdem alle Eigenschaften für die Codierungssitzung festgelegt wurden, kann der Decoder die Daten möglicherweise nicht dekomprimieren.

Im folgenden Codebeispiel wird veranschaulicht, wie sie die privaten Daten für einen Videotyp abrufen:


```
HRESULT GetFinalOutputType(DMO_MEDIA_TYPE* pMedia, IMediaObject* pDMO)
{
    // WARNING //
    // This function does not deallocate the memory pointed to by 
    // pMedia->pbFormat. If the VIDEOINFOHEADER referenced by pbFormat
    // was dynamically allocated, a reference to it must be kept before
    //  calling this function so that it can be freed.

    // Perform simple parameter checks.
    if(pMedia == NULL || pDMO == NULL)
        return E_POINTER;
    if(pMedia->formattype != MEDIATYPE_VideoInfo)
        return E_INVALIDARG;

    HRESULT hr = S_OK;

    IWMCodecPrivateData* pPrivData = NULL;
    BYTE* pbData = NULL;
    DWORD cbData = 0;

    BYTE* pbNewVidInf  = NULL;
    DWORD cbNewVidInf  = 0;
    BYTE* pbNewPriv    = NULL;

    // Get the private data interface.
    hr = pDMO->QueryInterface(IID_IWMCodecPrivateData,
                              (void**)&pPrivData);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the partial media type.
    hr = pPrivData->SetPartialOutputType(pMedia);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the size of the private data.
    hr = pPrivData->GetPrivateData(NULL, &cbData);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the private data.
    pbData = new BYTE[cbData];
    if(pbData == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit:
    }

    // Get the private data.
    hr = pPrivData->GetPrivateData(pbData, &cbData);

    // Allocate memory for the new VIDEOINFOHEADER.
    cbNewVidInf = pMedia->cbFormat + cbData;
    pbNewVidInf = new BYTE[cbNewVidInf];

    // Copy the VIDEOINFOHEADER to the new buffer.
    memcpy((void*)pbNewVidInf, (void*)pMedia->pbFormat, pMedia->cbFormat);

    // Get the address of the first byte following the VIDEOINFOHEADER.
    pbNewPriv = pbNewVidInf + pMedia->cbFormat;

    // Copy the private data to the new buffer.
    memcpy((void*)pbNewPriv, (void*)pbData, cbData);

    // Set the new VIDEOINFOHEADER in the DMO_MEDIA_TYPE.
    pMedia->pbFormat = pbNewVidInf;
    pMedia->cbFormat = cbNewVidInf;

Exit:
    SAFE_RELEASE(pPrivData);
    SAFE_ARRAY_DELETE(pbData);
    pbNewPriv = NULL;
    return hr;
}
```



> [!Note]  
> Die privaten Codecdaten, die von einem Videoencoder bereitgestellt werden, sind nicht garantiert identisch mit den privaten Daten, die von einer anderen Implementierung desselben Codecs für dieselbe Konfiguration bereitgestellt werden. Sie müssen diesen Wert immer mithilfe der Schritte in diesem Thema generieren. Kopieren Sie die privaten Daten niemals aus einer anderen Datei.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Videocodierung](configuringvideoencoding.md)
</dt> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 
