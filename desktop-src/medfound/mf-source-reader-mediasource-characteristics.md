---
description: Ruft die Merkmale der Medienquelle vom Quell Leser ab.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de4d1ed026f7b74f290446af74a6cf9947612617
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351709"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a>MF- \_ Quell \_ Leser \_ MediaSource- \_ Merkmale-Attribut

Ruft die Merkmale der Medienquelle vom [Quell Leser](source-reader.md)ab.

## <a name="data-type"></a>Datentyp

**UINT32**

Der Wert ist eine bitweise **or** -from-Flags aus der [**mfmediasource- \_ Eigenschaften**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) -Enumeration.

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut abzurufen, nennen Sie die [**imfsourcereader:: getpresentationattribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) -Methode für den Quell-Reader. Legen Sie den Parameter " *dwstreamindex* " auf den **MF- \_ Quell \_ Leser " \_ MediaSource** " und den *GuidAttribute* -Parameter auf "MF \_ Source \_ Reader \_ MediaSource" fest \_ .

Der **PROPVARIANT** -Typ für dieses Attribut ist " **VT \_ UI4**".

## <a name="examples"></a>Beispiele


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"Mfreadwrite. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Quell Leser](source-reader.md)
</dt> </dl>

 

 




