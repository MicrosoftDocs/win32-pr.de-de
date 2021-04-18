---
description: Verwenden von privaten Videocodec-Daten
ms.assetid: 0cc24fe4-a5b6-4805-8c8e-3066d12ec4bd
title: Verwenden von privaten Videocodec-Daten (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e86fc31a50d2c4e553b5947717ea930698d812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358810"
---
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a>Verwenden von privaten Videocodec-Daten (Microsoft Media Foundation)

Die von den Windows Media Video 9-Codecs erzeugte komprimierte Ausgabe kann nicht ordnungsgemäß dekomprimiert werden, ohne dass einige Daten vom Encoder bereitgestellt werden. Diese Daten, die als Codec private-Daten bezeichnet werden, müssen an den Ausgabe Medientyp angehängt werden. Sie können die privaten Codec-Daten abrufen, indem Sie die Methoden der [iwmcodecprivatedata](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) -Schnittstelle aufrufen. Übergeben Sie die anderweitig abgeschlossene [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur an [iwmcodecprivatedata:: setpartialoutputtype](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype). Nennen Sie anschließend [iwmcodecprivatedata:: getprivatedata](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) zweimal, einmal, um die Größe der Daten abzurufen, und dann erneut, um die Daten in einen Puffer dieser Größe zu kopieren. Erstellen Sie einen neuen Puffer zum Speichern der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur mit den privaten Daten, und kopieren Sie die Struktur und die Daten in diesen Puffer. Legen Sie schließlich den **pbformat** -Member der **DMO \_ - \_ Medientyp** Struktur auf die Adresse des neu erstellten Puffers fest, und legen Sie den **cbformat** -Member auf die kombinierte Größe (in Bytes) des **videoinfoheaders** und der privaten Daten fest.

Wenn Sie mediafoundierung verwenden, können Sie eine [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur über eine [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle erstellen, indem Sie [**mfcreateammediatypeer-frommfmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)aufrufen.

Sie müssen die privaten Codec-Daten verwenden, die nach dem ersten Festlegen der Eigenschaften für den Encoder abgerufen wurden. Wenn Eigenschaften geändert werden, müssen Sie neue private Daten erhalten. Wenn Sie nicht die privaten Daten verwenden, die abgerufen wurden, nachdem alle Eigenschaften für die Codierungs Sitzung festgelegt wurden, ist der Decoder möglicherweise nicht in der Lage, die Daten zu dekomprimieren.

Im folgenden Codebeispiel wird veranschaulicht, wie Sie die privaten Daten für einen Videotyp abrufen:


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
> Die privaten Codec-Daten, die von einem Video Encoder übermittelt werden, sind nicht garantiert identisch mit den privaten Daten, die von einer anderen Implementierung desselben Codecs für die gleiche Konfiguration bereitgestellt werden. Dieser Wert muss immer mithilfe der in diesem Thema beschriebenen Schritte generiert werden. Kopieren Sie die privaten Daten niemals aus einer anderen Datei.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Video Codierung](configuringvideoencoding.md)
</dt> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 
