---
description: Konfigurieren eines WMV-Encoders
ms.assetid: 6e690d17-da17-452a-aa9a-9701a560856b
title: Konfigurieren eines WMV-Encoders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39001edd5901d09bc618fe92d251070d24633fb94812a9c2696b11866f3cb9cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880544"
---
# <a name="configuring-a-wmv-encoder"></a>Konfigurieren eines WMV-Encoders

Um einen gültigen Ausgabetyp für einen Windows Media Video (WMV)-Encoder zu erstellen, müssen Sie über die folgenden Informationen verfügen:

-   Das Format des unkomprimierten Videos, das Sie codieren.
-   Der Videountertyp, der das codierte WMV-Format wiederernennt. Weitere Informationen [finden Sie unter Video Subtype GUIDs](video-subtype-guids.md).
-   Die Zielbitrate für den codierten Stream.
-   Die Konfigurationseigenschaften, die für den Encoder festgelegt werden.

Die Konfigurationseigenschaften sind in der Dokumentation Windows Medienaudio- und Videocodec und DSP-APIs dokumentiert. Weitere Informationen finden Sie unter "Video Stream Properties" (Videostreameigenschaften) unter [Encoding Properties (Codierungseigenschaften).](configuring-the-encoder.md)

Führen Sie die folgenden Schritte aus, um einen gültigen Ausgabetyp für den Encoder zu erhalten.

1.  Verwenden Sie [**die MFTEnum-**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) oder [**MFTEnumEx-Funktion,**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) um eine Instanz des Encoders zu erstellen.
2.  Fragen Sie den Encoder nach der **IPropertyStore-Schnittstelle** ab.
3.  Verwenden Sie die **IPropertyStore-Schnittstelle,** um den Encoder zu konfigurieren.
4.  Rufen [**Sie DEN TYP DESTTRANSFORM::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) auf, um den unkomprimierten Videotyp für den Encoder zu festlegen.
5.  Rufen [**Sie DEN WERTTRANSFORM::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf, um die Liste der Komprimierungsformate vom Encoder zu erhalten. Die WMV-Encoder geben keinen vollständigen Medientyp von dieser Methode zurück. Den Medientypen fehlen zwei Informationen:

    -   Die Zielbitrate.
    -   Private Codec-Daten vom Encoder.

    Bevor Sie den Ausgabetyp für den Encoder festlegen, müssen Sie beide Elemente dem Medientyp hinzufügen.

6.  Um die Zielbitrate anzugeben, legen Sie das [**MF \_ MT \_ AVG \_ BITRATE-Attribut**](mf-mt-avg-bitrate-attribute.md) für den Medientyp fest.
7.  Fügen Sie dem Medientyp die privaten Codecdaten hinzu, wie im nächsten Abschnitt erläutert.
8.  Rufen [**Sie ZUM FESTLEGENTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) auf, um den Komprimierungsmedientyp für den Encoder festlegen.

### <a name="private-codec-data"></a>Private Codec-Daten

Die privaten Codecdaten sind eine nicht transparente Datenstruktur, die Sie vom WMV-Encoder erhalten und dem Komprimierungstyp hinzufügen müssen, bevor Sie den Komprimierungstyp für den Encoder festlegen. Um die privaten Daten zu erhalten, müssen Sie die **IWMCodecPrivateData-Schnittstelle** verwenden, die im Windows Media Format 11 SDK dokumentiert ist.

Führen Sie die folgenden Schritte aus, um die Privaten Codec-Daten zu erhalten:

1.  Rufen [**Sie DEN WERTTRANSFORM::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf, um einen Medientyp vom Encoder zu erhalten. (Dies ist Schritt 6 aus dem vorherigen Abschnitt.)
2.  Geben Sie die Zielbitrate an, indem Sie das [**MF \_ MT \_ AVG \_ BITRATE-Attribut**](mf-mt-avg-bitrate-attribute.md) für den Medientyp festlegen.
3.  Konvertieren Sie den Medientyp in eine [**DMO \_ MEDIA \_ TYPE-Struktur,**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) indem Sie die [**MFInitAMMediaTypeFromMFMediaType-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) aufrufen.
4.  Fragen Sie den Encoder für die **IWMCodecPrivateData-Schnittstelle** ab.
5.  Rufen Sie **die IWMCodecPrivateData::SetPartialOutputType-Methode** auf, und übergeben Sie die konvertierte DMO [**MEDIA \_ \_ TYPE-Struktur.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)
6.  Rufen Sie **die IWMCodecPrivateData::GetPrivateData-Methode** zweimal auf, einmal, um die Größe des Puffers für die privaten Daten zu erhalten, und einmal, um die Daten in den Puffer zu kopieren.
7.  Fügen Sie dem Medientyp die privaten Daten hinzu, indem Sie das [**MF \_ MT USER \_ \_ DATA-Attribut**](mf-mt-user-data-attribute.md) für den Typ festlegen.

Das folgende erweiterte Beispiel zeigt, wie Sie ein WMV-Komprimierungsformat aus einem nicht komprimierten Videotyp erstellen:


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



Die CreateVideoEncoder-Funktion erstellt einen Videoencoder für einen angegebenen Videountertyp, z. B. **MFVideoFormat \_ WMV3:**


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



Die AddPrivateData-Funktion fügt dem Komprimierungstyp die privaten Codecdaten hinzu:


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



Die CopyPropertyStore-Funktion ist eine Hilfsfunktion, die Eigenschaften aus einem Eigenschaftenspeicher in einen anderen kopiert:


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Instanziieren eines Encoder-MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> </dl>

 

 
