---
description: Aktiviert die Verwendung einer asynchronen Media Foundation Transformation (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: MF_TRANSFORM_ASYNC_UNLOCK-Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82a0a8f328095c3a5c567171fa6a625a77e5623d126dfb2be9f34fef556984be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244176"
---
# <a name="mf_transform_async_unlock-attribute"></a>MF \_ TRANSFORM \_ ASYNC \_ UNLOCK-Attribut

Aktiviert die Verwendung einer asynchronen Media Foundation Transformation (MFT).

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Asynchrone MFTs sind nicht mit früheren Versionen von Microsoft Media Foundation kompatibel. Um zu verhindern, dass vorhandene Anwendungen versehentlich einen asynchronen MFT verwenden, muss dieses Attribut auf einen Wert ungleich 0 (null) festgelegt werden, bevor ein asynchrones MFT verwendet werden kann. Die Media Foundation Pipeline legt das Attribut automatisch fest, sodass die meisten Anwendungen dieses Attribut nicht verwenden müssen. Wenn eine Anwendung jedoch einen asynchronen MFT außerhalb der Media Foundation Pipeline verwendet, muss die Anwendung dieses Attribut festlegen.

Synchrone MFTs erfordern dieses Attribut nicht.

Um zu testen, ob ein MFT asynchron ist, ruft den Wert des [MF \_ TRANSFORM \_ ASYNC-Attributs](mf-transform-async.md) für den MFT ab.

## <a name="examples"></a>Beispiele

Der folgende Code entsperrt einen asynchronen MFT.


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 




