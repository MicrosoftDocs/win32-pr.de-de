---
description: Gibt an, ob eine Media Foundation-Transformation (MFT) eine asynchrone Verarbeitung ausführt.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: MF_TRANSFORM_ASYNC-Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92a647ca122c138f2ef7e90670798200fc3fa629be48d6242b4e71dbc93151e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714349"
---
# <a name="mf_transform_async-attribute"></a>MF \_ TRANSFORM \_ ASYNC-Attribut

Gibt an, ob eine Media Foundation-Transformation (MFT) eine asynchrone Verarbeitung ausführt.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Das Attribut ist ein boolescher Wert:

-   Wenn das Attribut ungleich 0 (null) ist, führt der MFT eine asynchrone Verarbeitung durch.
-   Wenn das Attribut 0 oder nicht festgelegt ist, ist der MFT synchron.

Rufen Sie zum Abrufen dieses Attributs zunächst [**DIE ATTRIBUTETransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) auf, um den Attributspeicher des MFT abzurufen. Wenn diese Methode erfolgreich ist, rufen [**Sie DIE ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) auf, um den Attributwert abzurufen. Wenn eine der beiden Methoden fehlschlägt, ist der MFT synchron.

Bei asynchronen MFTs muss dieses Attribut auf einen Wert ungleich 0 (null) festgelegt werden. Bei synchronen MFTs ist dieses Attribut optional, muss jedoch auf 0 (sofern vorhanden) festgelegt werden.

Asynchrone MFTs sind nicht mit früheren Versionen von Media Foundation kompatibel. Um einen asynchronen MFT zu verwenden, muss der Client das [**MF \_ TRANSFORM \_ ASYNC \_ UNLOCK-Attribut**](mf-transform-async-unlock.md) für den MFT festlegen. (Die Microsoft Media Foundation Pipeline führt diesen Schritt automatisch aus.)

## <a name="examples"></a>Beispiele

Der folgende Code testet, ob ein MFT eine asynchrone Verarbeitung ausführt.


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
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> <dt>

[**MF \_ TRANSFORM \_ ASYNC \_ UNLOCK**](mf-transform-async-unlock.md)
</dt> </dl>

 

 




