---
description: Ruft die Merkmale der Medienquelle aus dem Quellleser ab.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS-Attribut (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5ec5461bc289517490ae11bdd507895cd1ad434c53b1665ac5c6394907f15a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739966"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a>MF \_ SOURCE \_ READER \_ MEDIASOURCE \_ CHARACTERISTICS-Attribut

Ruft die Merkmale der Medienquelle aus dem [Quellleseprogramm](source-reader.md)ab.

## <a name="data-type"></a>Datentyp

**UINT32**

Der Wert ist ein bitweises **OR** von Flags aus der [**MFMEDIASOURCE \_ CHARACTERISTICS-Enumeration.**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics)

## <a name="remarks"></a>Hinweise

Rufen Sie zum Abrufen dieses Attributs die [**METHODE "WFSourceReader::GetPresentationAttribute"**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) für den Quellleser auf. Legen Sie den *dwStreamIndex-Parameter* auf **MF SOURCE READER \_ \_ \_ MEDIASOURCE** und den *guidAttribute-Parameter* auf MF \_ SOURCE READER \_ \_ MEDIASOURCE CHARACTERISTICS \_ fest.

Der **PROPVARIANT-Typ** für dieses Attribut ist **VT \_ UI4.**

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
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Quellleser](source-reader.md)
</dt> </dl>

 

 




