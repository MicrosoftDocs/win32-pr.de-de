---
description: Gibt an, ob eine Media Foundation Transformation (MFT) die DirectX-Video Beschleunigung (DXVA) unterstützt. Dieses Attribut gilt nur für Video-MFTs.
ms.assetid: db6a8b20-fda0-4ffe-b1b5-a77b7604d290
title: MF_SA_D3D_AWARE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb0de8c5a66eaa89f66becf6770f69e6449c1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368861"
---
# <a name="mf_sa_d3d_aware-attribute"></a>MF \_ sa \_ D3D \_ Aware-Attribut

Gibt an, ob eine Media Foundation Transformation (MFT) die DirectX-Video Beschleunigung (DXVA) unterstützt. Dieses Attribut gilt nur für Video-MFTs.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut abzufragen, müssen Sie [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) aufrufen, um den globalen Attribut Speicher des MFT abzurufen. Wenn **GetAttributes** erfolgreich ist, können Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)aufrufen.

Dieses Attribut teilt dem Client mit, ob der MFT Direct3D 9-Video verwenden kann:

-   Wenn das Attribut ungleich NULL ist, kann der Client dem MFT einen Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle übergeben, bevor das Streaming gestartet wird. Hierzu sendet der Client die [**MFT \_ Message \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) -Nachricht an die MFT. Der Client muss diese Nachricht nicht senden.
-   Wenn dieses Attribut NULL (**false**) ist, wird das Direct3D 9-Video vom MFT nicht unterstützt, und der Client sollte die [**MFT- \_ Nachricht \_ Set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) nicht an die MFT senden.

Der Standardwert dieses Attributs ist **false**. Behandeln Sie dieses Attribut als schreibgeschützt. Ändern Sie den Wert nicht. die MFT ignoriert alle Änderungen am Wert.

Weitere Informationen zum Implementieren dieses Attributs in einem benutzerdefinierten MFT finden Sie unter [Direct3D-Aware MFTs](direct3d-aware-mfts.md).

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="examples"></a>Beispiele

Der folgende Code testet, ob eine MFT DXVA unterstützt.


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Direct3D-kompatible MFTs](direct3d-aware-mfts.md)
</dt> <dt>

[Unterstützung von DXVA 2,0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> <dt>

[Transformations Attribute](transform-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[\_ \_ DXVA-Modus für MF-Topologie \_](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




