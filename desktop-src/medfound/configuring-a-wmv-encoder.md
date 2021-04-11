---
description: Konfigurieren eines WMV-Encoders
ms.assetid: 6e690d17-da17-452a-aa9a-9701a560856b
title: Konfigurieren eines WMV-Encoders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6324071257dd9d56e33d1dc6ece4886ee73661ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127960"
---
# <a name="configuring-a-wmv-encoder"></a><span data-ttu-id="dfda5-103">Konfigurieren eines WMV-Encoders</span><span class="sxs-lookup"><span data-stu-id="dfda5-103">Configuring a WMV Encoder</span></span>

<span data-ttu-id="dfda5-104">Um einen gültigen Ausgabetyp für einen Windows Media Video-Encoder (WMV) zu erstellen, müssen Sie über die folgenden Informationen verfügen:</span><span class="sxs-lookup"><span data-stu-id="dfda5-104">To create a valid output type for a Windows Media Video (WMV) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="dfda5-105">Das Format des unkomprimierten Videos, das codiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dfda5-105">The format of the uncompressed video that you will encode.</span></span>
-   <span data-ttu-id="dfda5-106">Der Video Untertyp, der das codierte WMV-Format repmmert.</span><span class="sxs-lookup"><span data-stu-id="dfda5-106">The video subtype that repesents the encoded WMV format.</span></span> <span data-ttu-id="dfda5-107">Siehe [Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="dfda5-107">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="dfda5-108">Die Ziel Bitrate für den codierten Stream.</span><span class="sxs-lookup"><span data-stu-id="dfda5-108">The target bitrate for the encoded stream.</span></span>
-   <span data-ttu-id="dfda5-109">Die Konfigurations Eigenschaften, die für den Encoder festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dfda5-109">The configuration properties to set on the encoder.</span></span>

<span data-ttu-id="dfda5-110">Die Konfigurations Eigenschaften sind in der Dokumentation zu Windows Media Audio und Video Codec und DSP-APIs dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="dfda5-110">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="dfda5-111">Weitere Informationen finden Sie unter "Video Stream Properties" unter [Codierungs Eigenschaften](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="dfda5-111">For more information, see "Video Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

<span data-ttu-id="dfda5-112">Um einen gültigen Ausgabetyp für den Encoder zu erhalten, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="dfda5-112">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="dfda5-113">Verwenden Sie die Funktion [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) oder [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) zum Erstellen einer Instanz des Encoders.</span><span class="sxs-lookup"><span data-stu-id="dfda5-113">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="dfda5-114">Fragen Sie den Encoder nach der **IPropertyStore** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="dfda5-114">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="dfda5-115">Verwenden Sie die **IPropertyStore** -Schnittstelle, um den Encoder zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dfda5-115">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="dfda5-116">Mit [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) wird der unkomprimierte Videotyp für den Encoder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dfda5-116">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed video type on the encoder.</span></span>
5.  <span data-ttu-id="dfda5-117">Wenn Sie [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) aufrufen, wird die Liste mit den Komprimierungs Formaten des Encoders abgerufen.</span><span class="sxs-lookup"><span data-stu-id="dfda5-117">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of compression formats from the encoder.</span></span> <span data-ttu-id="dfda5-118">Der WMV-Encoder gibt keinen kompletten Medientyp aus dieser Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="dfda5-118">The WMV encoders do not return a complete media type from this method.</span></span> <span data-ttu-id="dfda5-119">In den Medientypen fehlen zwei Informationen:</span><span class="sxs-lookup"><span data-stu-id="dfda5-119">The media types are missing two pieces of information:</span></span>

    -   <span data-ttu-id="dfda5-120">Die Ziel Bitrate.</span><span class="sxs-lookup"><span data-stu-id="dfda5-120">The target bitrate.</span></span>
    -   <span data-ttu-id="dfda5-121">Private Codec-Daten vom Encoder.</span><span class="sxs-lookup"><span data-stu-id="dfda5-121">Private codec data from the encoder.</span></span>

    <span data-ttu-id="dfda5-122">Bevor Sie den Ausgabetyp für den Encoder festlegen, müssen Sie beide Elemente zum Medientyp hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dfda5-122">Before setting the output type on the encoder, you must add both of these items to the media type.</span></span>

6.  <span data-ttu-id="dfda5-123">Um die Ziel Bitrate anzugeben, legen Sie das [**MF \_ MT \_ AVG- \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) -Attribut für den Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="dfda5-123">To specify the target bitrate, set the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
7.  <span data-ttu-id="dfda5-124">Fügen Sie die privaten Codec-Daten zum Medientyp hinzu, wie im nächsten Abschnitt erläutert.</span><span class="sxs-lookup"><span data-stu-id="dfda5-124">Add the private codec data to the media type, as explained in the next section.</span></span>
8.  <span data-ttu-id="dfda5-125">Aufrufen von [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , um den Medientyp für die Komprimierung für den Encoder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="dfda5-125">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="private-codec-data"></a><span data-ttu-id="dfda5-126">Private Codec-Daten</span><span class="sxs-lookup"><span data-stu-id="dfda5-126">Private Codec Data</span></span>

<span data-ttu-id="dfda5-127">Bei den privaten Codec-Daten handelt es sich um eine nicht transparente Datenstruktur, die Sie vom WMV-Encoder erhalten und zum Komprimierungstyp hinzufügen müssen, bevor Sie den Komprimierungstyp für den Encoder festlegen.</span><span class="sxs-lookup"><span data-stu-id="dfda5-127">The private codec data is an opaque data structure that you must get from the WMV encoder and add to the compression type, before setting the compression type on the encoder.</span></span> <span data-ttu-id="dfda5-128">Um die privaten Daten zu erhalten, müssen Sie die **iwmcodecprivatedata** -Schnittstelle verwenden, die im SDK für Windows Media-Format 11 dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="dfda5-128">To get the private data, you must use the **IWMCodecPrivateData** interface, which is documented in the Windows Media Format 11 SDK.</span></span>

<span data-ttu-id="dfda5-129">Um private Codec-Daten zu erhalten, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="dfda5-129">To get the private codec data, perform the following steps:</span></span>

1.  <span data-ttu-id="dfda5-130">Wenn Sie [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) aufrufen, erhalten Sie einen Medientyp aus dem Encoder.</span><span class="sxs-lookup"><span data-stu-id="dfda5-130">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a media type from the encoder.</span></span> <span data-ttu-id="dfda5-131">(Dies ist Schritt 6 aus dem vorherigen Abschnitt.)</span><span class="sxs-lookup"><span data-stu-id="dfda5-131">(This is step 6 from the previous section.)</span></span>
2.  <span data-ttu-id="dfda5-132">Geben Sie die Ziel Bitrate an, indem Sie das [**MF \_ MT \_ AVG \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) -Attribut für den Medientyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="dfda5-132">Specify the target bitrate by setting the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
3.  <span data-ttu-id="dfda5-133">Konvertieren Sie den Medientyp in eine [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur, indem Sie die Funktion [**mfinitammediatypfrommfmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dfda5-133">Convert the media type into a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure by calling the [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) function.</span></span>
4.  <span data-ttu-id="dfda5-134">Fragen Sie den Encoder für die **iwmcodecprivatedata** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="dfda5-134">Query the encoder for the **IWMCodecPrivateData** interface.</span></span>
5.  <span data-ttu-id="dfda5-135">Nennen Sie die **iwmcodecprivatedata:: setpartialoutputtype** -Methode, und übergeben Sie die konvertierte [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur.</span><span class="sxs-lookup"><span data-stu-id="dfda5-135">Call the **IWMCodecPrivateData::SetPartialOutputType** method, passing in the converted [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span>
6.  <span data-ttu-id="dfda5-136">Nennen Sie die **iwmcodecprivatedata:: getprivatedata** -Methode zweimal, einmal, um die Größe des Puffers für die privaten Daten abzurufen, und einmal, um die Daten in den Puffer zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="dfda5-136">Call the **IWMCodecPrivateData::GetPrivateData** method twice, once to get the size of the buffer for the private data, and once to copy the data into the buffer.</span></span>
7.  <span data-ttu-id="dfda5-137">Fügen Sie die privaten Daten dem Medientyp hinzu, indem Sie das [**MF \_ MT- \_ Benutzer \_ Daten**](mf-mt-user-data-attribute.md) Attribut für den Typ festlegen.</span><span class="sxs-lookup"><span data-stu-id="dfda5-137">Add the private data to the media type by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute on the type.</span></span>

<span data-ttu-id="dfda5-138">Im folgenden erweiterten Beispiel wird gezeigt, wie ein WMV-Komprimierungs Format aus einem unkomprimierten Videotyp erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="dfda5-138">The following extended example shows how to create a WMV compression format from an uncompressed video type:</span></span>


```C++
#include <wmcodecdsp.h>
#include <Wmsdk.h>
#include <Dmo.h>
#include <mfapi.h>
#include <uuids.h>

#include <mfidl.h>
#include <mftransform.h>
#include <mferror.h>

#pragma comment(lib, "Msdmo")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "strmiids")
#pragma comment(lib, "propsys")

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn, 
    REFGUID subtype,
    UINT32 TargetBitrate, 
    IPropertyStore *pEncoderProps, 
    IMFMediaType **ppEncodingType,
    DWORD mftEnumFlags = MFT_ENUM_FLAG_SYNCMFT
    );

HRESULT CreateVideoEncoder(REFGUID subtype, DWORD mftEnumFlags, IMFTransform **ppMFT);
HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut);
HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest);

//
// GetEncodedVideoType
// Given an uncompressed video type, finds a suitable WMV type.
//

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn,          // Uncompressed format
    REFGUID subtype,                // Compression format
    UINT32 TargetBitrate,           // Target bit rate
    IPropertyStore *pEncoderProps,  // Encoder properties (can be NULL)
    IMFMediaType **ppEncodingType,  // Receives the WMV type.
    DWORD mftEnumFlags              // MFTEnumEx flags
    )
{
    HRESULT hr = S_OK;

    IMFTransform *pMFT = NULL;
    IPropertyStore *pPropStore = NULL;
    IMFMediaType *pTypeOut = NULL;

    // Instantiate the encoder
    hr = CreateVideoEncoder(subtype, mftEnumFlags, &pMFT);

    // Copy the properties to the encoder.

    if (SUCCEEDED(hr))
    {
        if (pEncoderProps)
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPropStore));

            if (SUCCEEDED(hr))
            {
                hr = CopyPropertyStore(pEncoderProps, pPropStore);
            }
        }
    }

    // Set the uncompressed type.
    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetInputType(0, pTypeIn, 0);
    }

    // Get the partial output type
    if (SUCCEEDED(hr))
    {
        hr = pMFT->GetOutputAvailableType(0, 0, &pTypeOut);
    }

    // Set the bit rate.
    // You must set this before getting the codec private data.

    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetUINT32(MF_MT_AVG_BITRATE, TargetBitrate);   
    }

    if (SUCCEEDED(hr))
    {
        hr = AddPrivateData(pMFT, pTypeOut);
    }

    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetOutputType(0, pTypeOut, 0);
    }

    if (SUCCEEDED(hr))
    {
        *ppEncodingType = pTypeOut;
        (*ppEncodingType)->AddRef();
    }

    SafeRelease(&pMFT);
    SafeRelease(&pPropStore);
    SafeRelease(&pTypeOut);
    return hr;
}
```



<span data-ttu-id="dfda5-139">Die createvideoencoder-Funktion erstellt einen Video Encoder für einen angegebenen Video Untertyp, wie z. b. **MF-Format \_ WMV3**:</span><span class="sxs-lookup"><span data-stu-id="dfda5-139">The CreateVideoEncoder function creates a video encoder for a specified video subtype, such as **MFVideoFormat\_WMV3**:</span></span>


```C++
//
// CreateVideoEncoder
// Creates a video encoder for a specified video subtype.
//

HRESULT CreateVideoEncoder(
    REFGUID subtype,            // Encoding subtype.
    DWORD mftEnumFlags,         // Flags for MFTEnumEx
    IMFTransform **ppMFT        // Receives a pointer to the encoder.
    )
{
    HRESULT hr = S_OK;
    IMFTransform *pMFT = NULL;

    MFT_REGISTER_TYPE_INFO info;
    info.guidMajorType = MFMediaType_Video;
    info.guidSubtype = subtype;

    IMFActivate **ppActivates = NULL;    
    UINT32 count = 0;

    hr = MFTEnumEx(
        MFT_CATEGORY_VIDEO_ENCODER,
        mftEnumFlags | MFT_ENUM_FLAG_SORTANDFILTER,
        NULL,
        &info,
        &ppActivates,
        &count
        );

    if (count == 0)
    {
        hr = E_FAIL;
    }

    if (SUCCEEDED(hr))
    {
        hr = ppActivates[0]->ActivateObject(
            __uuidof(IMFTransform),
            (void**)&pMFT
            );
    }

    if (SUCCEEDED(hr))
    {
        *ppMFT = pMFT;
        (*ppMFT)->AddRef();
    }

    // Clean up

    for (DWORD i = 0; i < count; i++)
    {
        ppActivates[i]->Release();
    }
    CoTaskMemFree(ppActivates);
    SafeRelease(&pMFT);
    return hr;
}
```



<span data-ttu-id="dfda5-140">Die addprivatedata-Funktion fügt dem Komprimierungstyp die privaten Codec-Daten hinzu:</span><span class="sxs-lookup"><span data-stu-id="dfda5-140">The AddPrivateData function adds the private codec data to the compression type:</span></span>


```C++
//
// AddPrivateData
// Appends the private codec data to a media type.
//
// pMFT: The video encoder
// pTypeOut: A video type from the encoder's type list.
//
// The function modifies pTypeOut by adding the codec data.
//

HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
{
    HRESULT hr = S_OK;
    ULONG cbData = 0;
    BYTE *pData = NULL;

    IWMCodecPrivateData *pPrivData = NULL;

    DMO_MEDIA_TYPE mtOut = { 0 };

    // Convert the type to a DMO type.
    hr = MFInitAMMediaTypeFromMFMediaType(
        pTypeOut, 
        FORMAT_VideoInfo, 
        (AM_MEDIA_TYPE*)&mtOut
        );
    
    if (SUCCEEDED(hr))
    {
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
    }

    if (SUCCEEDED(hr))
    {
        hr = pPrivData->SetPartialOutputType(&mtOut);
    }

    //
    // Get the private codec data
    //

    // First get the buffer size.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(NULL, &cbData);
    }

    if (SUCCEEDED(hr))
    {
        pData = new BYTE[cbData];

        if (pData == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Now get the data.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(pData, &cbData);
    }

    // Add the data to the media type.
    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
    }

    delete [] pData;
    MoFreeMediaType(&mtOut);
    SafeRelease(&pPrivData);
    return hr;
}
```



<span data-ttu-id="dfda5-141">Bei der copypropertystore-Funktion handelt es sich um eine Hilfsfunktion, die Eigenschaften aus einem Eigenschaften Speicher in einen anderen kopiert:</span><span class="sxs-lookup"><span data-stu-id="dfda5-141">The CopyPropertyStore function is a helper function that copies properties from one property store to another:</span></span>


```C++
//
// CopyPropertyStore
// Helper function to copy properties from one property
// store to another property store.
//

HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest)
{
    HRESULT hr = S_OK;
    DWORD cProps = 0;

    PROPERTYKEY key;
    PROPVARIANT var;

    PropVariantInit(&var);

    hr = pSrc->GetCount(&cProps);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cProps; i++)
        {
            hr = pSrc->GetAt(i, &key);

            if (FAILED(hr)) { break; }

            hr = pSrc->GetValue(key, &var);

            if (FAILED(hr)) { break; }

            hr = pDest->SetValue(key, var);

            if (FAILED(hr)) { break; }

            PropVariantClear(&var);
        }
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="dfda5-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dfda5-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfda5-143">Instanziieren eines MFT-Encoders</span><span class="sxs-lookup"><span data-stu-id="dfda5-143">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="dfda5-144">Windows Media Encoder</span><span class="sxs-lookup"><span data-stu-id="dfda5-144">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 
