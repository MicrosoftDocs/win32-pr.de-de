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
# <a name="configuring-a-wmv-encoder"></a>Konfigurieren eines WMV-Encoders

Um einen gültigen Ausgabetyp für einen Windows Media Video-Encoder (WMV) zu erstellen, müssen Sie über die folgenden Informationen verfügen:

-   Das Format des unkomprimierten Videos, das codiert werden soll.
-   Der Video Untertyp, der das codierte WMV-Format repmmert. Siehe [Video Untertyp-GUIDs](video-subtype-guids.md).
-   Die Ziel Bitrate für den codierten Stream.
-   Die Konfigurations Eigenschaften, die für den Encoder festgelegt werden sollen.

Die Konfigurations Eigenschaften sind in der Dokumentation zu Windows Media Audio und Video Codec und DSP-APIs dokumentiert. Weitere Informationen finden Sie unter "Video Stream Properties" unter [Codierungs Eigenschaften](configuring-the-encoder.md).

Um einen gültigen Ausgabetyp für den Encoder zu erhalten, führen Sie die folgenden Schritte aus.

1.  Verwenden Sie die Funktion [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) oder [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) zum Erstellen einer Instanz des Encoders.
2.  Fragen Sie den Encoder nach der **IPropertyStore** -Schnittstelle ab.
3.  Verwenden Sie die **IPropertyStore** -Schnittstelle, um den Encoder zu konfigurieren.
4.  Mit [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) wird der unkomprimierte Videotyp für den Encoder festgelegt.
5.  Wenn Sie [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) aufrufen, wird die Liste mit den Komprimierungs Formaten des Encoders abgerufen. Der WMV-Encoder gibt keinen kompletten Medientyp aus dieser Methode zurück. In den Medientypen fehlen zwei Informationen:

    -   Die Ziel Bitrate.
    -   Private Codec-Daten vom Encoder.

    Bevor Sie den Ausgabetyp für den Encoder festlegen, müssen Sie beide Elemente zum Medientyp hinzufügen.

6.  Um die Ziel Bitrate anzugeben, legen Sie das [**MF \_ MT \_ AVG- \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) -Attribut für den Medientyp fest.
7.  Fügen Sie die privaten Codec-Daten zum Medientyp hinzu, wie im nächsten Abschnitt erläutert.
8.  Aufrufen von [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , um den Medientyp für die Komprimierung für den Encoder festzulegen.

### <a name="private-codec-data"></a>Private Codec-Daten

Bei den privaten Codec-Daten handelt es sich um eine nicht transparente Datenstruktur, die Sie vom WMV-Encoder erhalten und zum Komprimierungstyp hinzufügen müssen, bevor Sie den Komprimierungstyp für den Encoder festlegen. Um die privaten Daten zu erhalten, müssen Sie die **iwmcodecprivatedata** -Schnittstelle verwenden, die im SDK für Windows Media-Format 11 dokumentiert ist.

Um private Codec-Daten zu erhalten, führen Sie die folgenden Schritte aus:

1.  Wenn Sie [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) aufrufen, erhalten Sie einen Medientyp aus dem Encoder. (Dies ist Schritt 6 aus dem vorherigen Abschnitt.)
2.  Geben Sie die Ziel Bitrate an, indem Sie das [**MF \_ MT \_ AVG \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) -Attribut für den Medientyp festlegen.
3.  Konvertieren Sie den Medientyp in eine [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur, indem Sie die Funktion [**mfinitammediatypfrommfmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) aufrufen.
4.  Fragen Sie den Encoder für die **iwmcodecprivatedata** -Schnittstelle ab.
5.  Nennen Sie die **iwmcodecprivatedata:: setpartialoutputtype** -Methode, und übergeben Sie die konvertierte [**DMO- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur.
6.  Nennen Sie die **iwmcodecprivatedata:: getprivatedata** -Methode zweimal, einmal, um die Größe des Puffers für die privaten Daten abzurufen, und einmal, um die Daten in den Puffer zu kopieren.
7.  Fügen Sie die privaten Daten dem Medientyp hinzu, indem Sie das [**MF \_ MT- \_ Benutzer \_ Daten**](mf-mt-user-data-attribute.md) Attribut für den Typ festlegen.

Im folgenden erweiterten Beispiel wird gezeigt, wie ein WMV-Komprimierungs Format aus einem unkomprimierten Videotyp erstellt wird:


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



Die createvideoencoder-Funktion erstellt einen Video Encoder für einen angegebenen Video Untertyp, wie z. b. **MF-Format \_ WMV3**:


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



Die addprivatedata-Funktion fügt dem Komprimierungstyp die privaten Codec-Daten hinzu:


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



Bei der copypropertystore-Funktion handelt es sich um eine Hilfsfunktion, die Eigenschaften aus einem Eigenschaften Speicher in einen anderen kopiert:


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

[Instanziieren eines MFT-Encoders](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> </dl>

 

 
