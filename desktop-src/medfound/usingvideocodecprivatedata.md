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
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a><span data-ttu-id="03ec0-103">Verwenden von privaten Videocodec-Daten (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="03ec0-103">Using Video Codec Private Data (Microsoft Media Foundation)</span></span>

<span data-ttu-id="03ec0-104">Die von den Windows Media Video 9-Codecs erzeugte komprimierte Ausgabe kann nicht ordnungsgemäß dekomprimiert werden, ohne dass einige Daten vom Encoder bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="03ec0-104">The compressed output produced by the Windows Media Video 9 codecs cannot be properly decompressed without some data provided by the encoder.</span></span> <span data-ttu-id="03ec0-105">Diese Daten, die als Codec private-Daten bezeichnet werden, müssen an den Ausgabe Medientyp angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="03ec0-105">This data, called codec private data, must be appended to the output media type.</span></span> <span data-ttu-id="03ec0-106">Sie können die privaten Codec-Daten abrufen, indem Sie die Methoden der [iwmcodecprivatedata](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) -Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="03ec0-106">You can get the codec private data by calling the methods of the [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) interface.</span></span> <span data-ttu-id="03ec0-107">Übergeben Sie die anderweitig abgeschlossene [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur an [iwmcodecprivatedata:: setpartialoutputtype](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype).</span><span class="sxs-lookup"><span data-stu-id="03ec0-107">Pass the otherwise complete [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure to [IWMCodecPrivateData::SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype).</span></span> <span data-ttu-id="03ec0-108">Nennen Sie anschließend [iwmcodecprivatedata:: getprivatedata](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) zweimal, einmal, um die Größe der Daten abzurufen, und dann erneut, um die Daten in einen Puffer dieser Größe zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="03ec0-108">Then call [IWMCodecPrivateData::GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) twice, once to get the size of the data, and then again to copy the data to a buffer of that size.</span></span> <span data-ttu-id="03ec0-109">Erstellen Sie einen neuen Puffer zum Speichern der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur mit den privaten Daten, und kopieren Sie die Struktur und die Daten in diesen Puffer.</span><span class="sxs-lookup"><span data-stu-id="03ec0-109">Create a new buffer to hold the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure with the private data appended, and copy the structure and the data to that buffer.</span></span> <span data-ttu-id="03ec0-110">Legen Sie schließlich den **pbformat** -Member der **DMO \_ - \_ Medientyp** Struktur auf die Adresse des neu erstellten Puffers fest, und legen Sie den **cbformat** -Member auf die kombinierte Größe (in Bytes) des **videoinfoheaders** und der privaten Daten fest.</span><span class="sxs-lookup"><span data-stu-id="03ec0-110">Finally, set the **pbFormat** member of the **DMO\_MEDIA\_TYPE** structure to the address of the newly created buffer and set the **cbFormat** member to the combined size, in bytes, of the **VIDEOINFOHEADER** and the private data.</span></span>

<span data-ttu-id="03ec0-111">Wenn Sie mediafoundierung verwenden, können Sie eine [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur über eine [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle erstellen, indem Sie [**mfcreateammediatypeer-frommfmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="03ec0-111">If you are using MediaFoundation you can construct a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure from an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface by calling [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).</span></span>

<span data-ttu-id="03ec0-112">Sie müssen die privaten Codec-Daten verwenden, die nach dem ersten Festlegen der Eigenschaften für den Encoder abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="03ec0-112">You must use the codec private data obtained after first setting the properties on the encoder.</span></span> <span data-ttu-id="03ec0-113">Wenn Eigenschaften geändert werden, müssen Sie neue private Daten erhalten.</span><span class="sxs-lookup"><span data-stu-id="03ec0-113">If any properties are changed, you must get new private data.</span></span> <span data-ttu-id="03ec0-114">Wenn Sie nicht die privaten Daten verwenden, die abgerufen wurden, nachdem alle Eigenschaften für die Codierungs Sitzung festgelegt wurden, ist der Decoder möglicherweise nicht in der Lage, die Daten zu dekomprimieren.</span><span class="sxs-lookup"><span data-stu-id="03ec0-114">If you do not use the private data obtained after all the properties are set for the encoding session, the decoder may not be able to decompress the data.</span></span>

<span data-ttu-id="03ec0-115">Im folgenden Codebeispiel wird veranschaulicht, wie Sie die privaten Daten für einen Videotyp abrufen:</span><span class="sxs-lookup"><span data-stu-id="03ec0-115">The following code example demonstrates how to obtain the private data for a video type:</span></span>


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
> <span data-ttu-id="03ec0-116">Die privaten Codec-Daten, die von einem Video Encoder übermittelt werden, sind nicht garantiert identisch mit den privaten Daten, die von einer anderen Implementierung desselben Codecs für die gleiche Konfiguration bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="03ec0-116">The codec private data delivered by a video encoder is not guaranteed to be the same as the private data delivered by a different implementation of the same codec for the same configuration.</span></span> <span data-ttu-id="03ec0-117">Dieser Wert muss immer mithilfe der in diesem Thema beschriebenen Schritte generiert werden. Kopieren Sie die privaten Daten niemals aus einer anderen Datei.</span><span class="sxs-lookup"><span data-stu-id="03ec0-117">You must always generate this value using the steps in this topic; never copy the private data from another file.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="03ec0-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="03ec0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03ec0-119">Konfigurieren der Video Codierung</span><span class="sxs-lookup"><span data-stu-id="03ec0-119">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="03ec0-120">Arbeiten mit Videos</span><span class="sxs-lookup"><span data-stu-id="03ec0-120">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
