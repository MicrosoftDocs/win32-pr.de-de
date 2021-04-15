---
description: Aktiviert die Verwendung einer asynchronen Media Foundation Transformation (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: MF_TRANSFORM_ASYNC_UNLOCK-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7876b3f1fca80e881414399d40e69112a64d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527401"
---
# <a name="mf_transform_async_unlock-attribute"></a>MF \_ Transform \_ Async \_ Unlock Attribute

Aktiviert die Verwendung einer asynchronen Media Foundation Transformation (MFT).

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Asynchrone MFTs sind nicht kompatibel mit früheren Versionen von Microsoft Media Foundation. Um zu verhindern, dass vorhandene Anwendungen versehentlich ein asynchrones MFT verwenden, muss dieses Attribut auf einen Wert ungleich 0 (null) festgelegt werden, bevor ein asynchroner MFT verwendet werden kann. Das-Attribut wird von der Media Foundation Pipeline automatisch festgelegt, sodass die meisten Anwendungen dieses Attribut nicht verwenden müssen. Wenn eine Anwendung jedoch ein asynchrones MFT außerhalb der Media Foundation Pipeline verwendet, muss die Anwendung dieses Attribut festlegen.

Synchrone MFTs benötigen dieses Attribut nicht.

Um zu testen, ob eine MFT asynchron ist, erhalten Sie den Wert des " [MF \_ Transform \_ Async](mf-transform-async.md) "-Attributs für die MFT.

## <a name="examples"></a>Beispiele

Mit dem folgenden Code wird ein asynchroner MFT entsperrt.


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
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> <dt>

[Transformations Attribute](transform-attributes.md)
</dt> </dl>

 

 




