---
description: Gibt an, ob eine Media Foundation Transformation (MFT) asynchrone Verarbeitung durchführt.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: MF_TRANSFORM_ASYNC-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89622bd7bb7fa3e8306c94b02f90217b6367d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753152"
---
# <a name="mf_transform_async-attribute"></a>Asynchrones \_ Transform- \_ Attribut

Gibt an, ob eine Media Foundation Transformation (MFT) asynchrone Verarbeitung durchführt.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Das-Attribut ist ein boolescher Wert:

-   Wenn das-Attribut ungleich 0 (null) ist, führt die MFT die asynchrone Verarbeitung aus.
-   Wenn das Attribut 0 oder nicht festgelegt ist, ist der MFT synchron.

Zum Abrufen dieses Attributs müssen Sie zuerst [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) aufrufen, um den MFT-Attribut Speicher zu erhalten. Wenn diese Methode erfolgreich ausgeführt wird, müssen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) abrufen, um den Attribut Wert zu erhalten. Wenn eine der beiden Methoden fehlschlägt, ist die MFT synchron.

Für asynchrone MFTs muss dieses Attribut auf einen Wert ungleich 0 (null) festgelegt werden. Bei synchronen MFTs ist dieses Attribut optional, muss jedoch auf 0 (null) festgelegt werden, wenn es vorhanden ist.

Asynchrone MFTs sind nicht kompatibel mit früheren Versionen von Media Foundation. Um eine asynchrone MFT zu verwenden, muss der Client das Attribut " [**MF \_ Transform \_ Async \_ Unlock**](mf-transform-async-unlock.md) " auf dem MFT festlegen. (Die Microsoft Media Foundation Pipeline führt diesen Schritt automatisch aus.)

## <a name="examples"></a>Beispiele

Der folgende Code testet, ob eine MFT asynchrone Verarbeitung durchführt.


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
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
</dt> <dt>

[**MF- \_ Transformation \_ Async \_ Unlock**](mf-transform-async-unlock.md)
</dt> </dl>

 

 




