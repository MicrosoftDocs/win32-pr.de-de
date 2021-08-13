---
description: Enthält Flags für ein MFT-Aktivierungsobjekt (Media Foundation Transformation).
ms.assetid: de377132-19b0-4c8c-882e-193c31420739
title: MF_TRANSFORM_FLAGS_Attribute-Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d54d8775cb58980e0b5b4a8557ae4a3e8082b045eb3e87330841f75dfd057774
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739228"
---
# <a name="mf_transform_flags_attribute-attribute"></a>MF \_ TRANSFORM \_ \_ FLAGS-Attributattribut

Enthält Flags für ein MFT-Aktivierungsobjekt (Media Foundation Transformation).

## <a name="data-type"></a>Datentyp

**UINT32**

Der Wert ist ein bitweises **OR** von Flags aus der [**\_ \_ MFT-ENUM \_ FLAG-Enumeration.**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag)

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird für die VON der [**MFTEnumEx-Funktion zurückgegebenen**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) [**POINTERActivate-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) festgelegt. Das -Attribut enthält Flags, die den MFT beschreiben.

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

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 
